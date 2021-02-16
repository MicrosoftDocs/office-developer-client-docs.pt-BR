---
title: Copiar ou mover uma mensagem ou uma pasta
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 72290fd3-00d7-4055-bbfa-0c47b6e0f62d
description: 'Last modified: November 08, 2011'
ms.openlocfilehash: c5e92c44d7078560ed84d72b3477d5cf2e809353
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413497"
---
# <a name="copying-or-moving-a-message-or-a-folder"></a>Copiar ou mover uma mensagem ou uma pasta
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um cliente pode usar um dos quatro métodos para copiar ou mover uma mensagem ou uma pasta:
  
- [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md)
    
- [IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
    
- [IMAPIProp::CopyTo](imapiprop-copyto.md)
    
- [IMAPIProp::CopyProps](imapiprop-copyprops.md)
    
Definindo os sinalizadores e parâmetros apropriados, **CopyTo** e **CopyProps** podem ser feitos para funcionar exatamente como **CopyFolder** ou **CopyMessages**. Considere os seguintes problemas ao decidir qual método chamar:
  
- Você está copiando ou movendo uma pasta ou uma mensagem?
    
- Quanto você sabe sobre a pasta ou a mensagem a ser movida ou copiada?
    
- Quantas propriedades da pasta ou da mensagem serão movidas ou copiadas?
    
Você pode usar os **métodos IMAPIProp** para copiar ou mover uma pasta ou uma mensagem. **IMAPIFolder::CopyMessages** funciona apenas com mensagens; **IMAPIFolder::CopyFolder** funciona somente com pastas. 
  
Enquanto o uso dos métodos **IMAPIFolder** não requer nenhum conhecimento das propriedades com suporte da pasta ou da mensagem a serem copiadas ou movidas, você deve ter algum conhecimento para usar os métodos **IMAPIProp.** Com **IMAPIProp::CopyProps**, você deve ser capaz de especificar explicitamente quais das propriedades de pasta ou mensagem você deseja copiar ou mover. Com **IMAPIProp::CopyTo**, a menos que você queira copiar ou mover todas as propriedades, especifique explicitamente quais devem ser excluídas. Para obter mais informações sobre esses métodos, consulte [Copying MAPI Properties](copying-mapi-properties.md).
  
O número de propriedades a serem copiadas ou movidas pode afetar sua decisão sobre qual método usar. Se você estiver copiando ou movendo várias mensagens, chame **IMAPIFolder::CopyMessages**. Uma opção alternativa é chamar **IMAPIProp::CopyProps** para copiar apenas a propriedade **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) da pasta. O procedimento a seguir mostra como usar **CopyMessages**. 
  
### <a name="to-copy-or-move-one-or-more-messages"></a>Para copiar ou mover uma ou mais mensagens
  
1. Localize identificadores de entrada válidos para as pastas de origem e destino.
    
2. Abra essas pastas no modo de leitura/gravação chamando [IMAPISession::OpenEntry](imapisession-openentry.md) ou [IMsgStore::OpenEntry](imsgstore-openentry.md) e definindo o sinalizador MAPI_MODIFY leitura. 
    
3. Verifique se o ponteiro da interface retornado de **OpenEntry** é um ponteiro da interface **IMAPIFolder.** Caso não seja, cast it to the LPMAPIFOLDER type. 
    
4. Crie uma matriz de identificadores de entrada representando uma ou mais mensagens a serem copiadas ou movidas. 
    
5. Chame **IMAPIFolder::CopyMessages** com os seguintes sinalizadores definidos: 
    
   - MESSAGE_MOVE, se você quiser executar uma operação de movimentação. 
    
   - MESSAGE_DIALOG e passe uma alça de janela no  _parâmetro ulUIParam,_ se quiser que a pasta mostre um indicador de progresso. 
    
6. Libere os **ponteiros IMAPIFolder** para as pastas de origem e destino. 
    
Se você quiser copiar o conteúdo completo de uma pasta para outra pasta, chame o método **IMAPIFolder::CopyFolder** ou **IMAPIProp::CopyTo** da pasta de origem. 
  
Para copiar algumas das propriedades de uma pasta, chame seu **método IMAPIProp::CopyProps.** Para copiar a maioria das propriedades de uma pasta, chame **IMAPIProp::CopyTo**. 
  
Por exemplo, se você quiser copiar as propriedades **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) e **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)), terá as seguintes opções:
  
- Chame **IMAPIFolder::CopyFolder** para copiar todas as propriedades da pasta e excluir as indesejadas da nova pasta. 
    
- Chame **CopyTo** e exclua todas as propriedades da pasta, exceto **PR_DISPLAY_NAME** e **PR_COMMENT**. 
    
- Chame **CopyProps**, passando **PR_DISPLAY_NAME** **e PR_COMMENT** na matriz de inclusão. 
    
Nesse caso, **CopyProps** é a melhor opção porque ela deve ser usada para copiar um pequeno conjunto de propriedades e é a chamada mais fácil de implementar. 
  
Para copiar ou mover apenas as propriedades da pasta, sem incluir mensagens, chame o método **IMAPIProp::CopyTo** da pasta e exclua as seguintes propriedades: 
  
- **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))
    
- **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))
    
Os métodos de cópia podem retornar S_OK, indicando sucesso total, MAPI_W_PARTIAL_COMPLETION, indicando sucesso parcial ou um erro. Se MAPI_W_PARTIAL_COMPLETION for retornado, use a **HR_FAILED** macro para acessar um erro mais específico. Para obter mais informações, consulte [Usando macros para tratamento de erros.](using-macros-for-error-handling.md)
  
Se você copiar mensagens de um armazenamento de mensagens para outro e Unicode não for suportado por ambos, esteja ciente de que as informações podem ser perdidas devido à conversão de página de código. Normalmente, você não pode saber se os armazenamentos de mensagens suportam um ou ambos os formatos, tornando impossível determinar se as propriedades de texto são copiadas como cadeias de caracteres ASCII ou como cadeias de caracteres Unicode. Se você tiver suporte para Unicode, tente executar uma cópia Unicode; se falhar com o valor de erro MAPI_E_BAD_CHARWIDTH, recora a ASCII.
  

