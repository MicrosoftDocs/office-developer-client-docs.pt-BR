---
title: Copiar ou mover uma mensagem ou uma pasta
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 72290fd3-00d7-4055-bbfa-0c47b6e0f62d
description: 'Última modificação: 08 de novembro de 2011'
ms.openlocfilehash: c5e92c44d7078560ed84d72b3477d5cf2e809353
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32333037"
---
# <a name="copying-or-moving-a-message-or-a-folder"></a>Copiar ou mover uma mensagem ou uma pasta
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um cliente pode usar um dos quatro métodos para copiar ou mover uma mensagem ou uma pasta:
  
- [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md)
    
- [IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
    
- [IMAPIProp::CopyTo](imapiprop-copyto.md)
    
- [IMAPIProp::CopyProps](imapiprop-copyprops.md)
    
Configurando os sinalizadores e parâmetros apropriados, **CopyTo** e **CopyProps** podem ser feitos para funcionar da mesma forma que o **CopyFolder** ou o **CopyMessages**. Considere os seguintes problemas ao decidir qual método chamar:
  
- Você está copiando ou movendo uma pasta ou uma mensagem?
    
- Quanto você sabe sobre a pasta ou a mensagem a ser movida ou copiada?
    
- Quantas Propriedades da pasta ou da mensagem serão movidas ou copiadas?
    
Você pode usar os métodos **IMAPIProp** para copiar ou mover uma pasta ou uma mensagem. **IMAPIFolder:: CopyMessages** funciona somente com mensagens; **IMAPIFolder:: CopyFolder** funciona somente com pastas. 
  
Enquanto o uso dos métodos **IMAPIFolder** não exige nenhum conhecimento das propriedades com suporte na pasta ou na mensagem a ser copiada ou movida, você deve ter algum conhecimento para usar os métodos **IMAPIProp** . Com o **IMAPIProp:: CopyProps**, você deve ser capaz de especificar explicitamente quais das propriedades de pasta ou de mensagem que você deseja copiar ou mover. Com **IMAPIProp:: CopyTo**, a menos que você queira copiar ou mover todas as propriedades, você deve especificar explicitamente quais delas devem ser excluídas. Para obter mais informações sobre esses métodos, consulte [copyING MAPI Properties](copying-mapi-properties.md).
  
O número de propriedades a serem copiadas ou movidas pode afetar sua decisão quanto ao método a ser usado. Se você estiver copiando ou movendo várias mensagens, chame **IMAPIFolder:: CopyMessages**. Uma opção alternativa é chamar **IMAPIProp:: CopyProps** para copiar apenas a propriedade **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) da pasta. O procedimento a seguir mostra como usar o **CopyMessages**. 
  
### <a name="to-copy-or-move-one-or-more-messages"></a>Para copiar ou mover uma ou mais mensagens
  
1. Localize identificadores de entrada válidos para as pastas de origem e de destino.
    
2. Abra essas pastas no modo de leitura/gravação chamando [IMAPISession:: OpenEntry](imapisession-openentry.md) ou [IMsgStore:: OpenEntry](imsgstore-openentry.md) e definindo o sinalizador MAPI_MODIFY. 
    
3. Verifique se o ponteiro de interface retornado de **OpenEntry** é um ponteiro de interface **IMAPIFolder** . Caso contrário, converta-o para o tipo LPMAPIFOLDER. 
    
4. Criar uma matriz de identificadores de entrada que representam uma ou mais mensagens a serem copiadas ou movidas. 
    
5. Chamar **IMAPIFolder:: CopyMessages** com os seguintes sinalizadores definidos: 
    
   - MESSAGE_MOVE, se você quiser realizar uma operação de movimentação. 
    
   - MESSAGE_DIALOG e passe um identificador de janela no parâmetro _ulUIParam_ , se você quiser que a pasta mostre um indicador de progresso. 
    
6. Libere os ponteiros do **IMAPIFolder** para as pastas de origem e destino. 
    
Se você quiser copiar todo o conteúdo de uma pasta para outra pasta, chame o método **IMAPIFolder:: CopyFolder** ou **IMAPIProp:** : a pasta de origem. 
  
Para copiar algumas das propriedades de uma pasta, chame seu método **IMAPIProp:: CopyProps** . Para copiar a maioria das propriedades de uma pasta, chame **IMAPIProp:: CopyTo**. 
  
Por exemplo, se você deseja copiar as propriedades **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) e **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) de uma pasta, você tem as seguintes opções:
  
- Chame **IMAPIFolder:: CopyFolder** para copiar todas as propriedades da pasta e exclua os indesejados da nova pasta. 
    
- Chame **CopyTo** e exclua todas as propriedades da pasta, exceto **PR_DISPLAY_NAME** e **PR_COMMENT**. 
    
- Chame **CopyProps**, passando **PR_DISPLAY_NAME** e **PR_COMMENT** na matriz include. 
    
Nesse caso, **CopyProps** é a melhor opção porque deve ser usada para copiar um pequeno conjunto de propriedades e é a chamada mais fácil de implementar. 
  
Para copiar ou mover somente as propriedades da pasta, sem incluir as mensagens, chame o método **IMAPIProp:: CopyTo** da pasta e exclua as seguintes propriedades: 
  
- **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))
    
- **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))
    
Os métodos Copy podem retornar S_OK, indicando o êxito total, MAPI_W_PARTIAL_COMPLETION, indicando o êxito parcial ou um erro. Se MAPI_W_PARTIAL_COMPLETION for retornado, use a macro **HR_FAILED** para acessar um erro mais específico. Para obter mais informações, consulte [usando macros para tratamento de erros](using-macros-for-error-handling.md).
  
Se você copiar mensagens de um repositório de mensagens para outro e Unicode não for suportada por ambas, lembre-se de que as informações podem ser perdidas devido à conversão da página de código. Normalmente, você não pode saber se os repositórios de mensagens dão suporte a um ou ambos formatos, tornando impossível determinar se as propriedades de texto serão copiadas como cadeias de caracteres ASCII ou como cadeias de caracteres Unicode. Se você oferecer suporte a Unicode, tente executar uma cópia Unicode; Se ele falhar com o valor de erro MAPI_E_BAD_CHARWIDTH, recorrer a ASCII.
  

