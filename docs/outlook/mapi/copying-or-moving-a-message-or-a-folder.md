---
title: Copiar ou mover uma mensagem ou uma pasta
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 72290fd3-00d7-4055-bbfa-0c47b6e0f62d
description: 'Modificado pela última vez: 08 de novembro de 2011'
ms.openlocfilehash: 26fe135da93e0f5f94d9f7d264453b74f97a518b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766348"
---
# <a name="copying-or-moving-a-message-or-a-folder"></a>Copiar ou mover uma mensagem ou uma pasta
  
**Aplica-se a**: Outlook 
  
Um cliente pode usar um dos quatro métodos para copiar ou mover uma mensagem ou uma pasta:
  
- [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md)
    
- [IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
    
- [IMAPIProp::CopyTo](imapiprop-copyto.md)
    
- [IMAPIProp::CopyProps](imapiprop-copyprops.md)
    
Definindo os parâmetros e os sinalizadores apropriados, **CopyTo** e **CopyProps** podem ser feitas para funcionar como **CopyFolder** ou **CopyMessages**. Ao decidir qual método de chamada, considere as seguintes questões:
  
- Você copiar ou mover uma pasta ou uma mensagem?
    
- Quanto você sabe sobre a pasta ou a mensagem a ser movido ou copiadas?
    
- Quantos da pasta ou propriedades da mensagem serão movidas ou copiadas?
    
Você pode usar os métodos **IMAPIProp** para copiar ou mover uma pasta ou uma mensagem. **IMAPIFolder::CopyMessages** funciona com mensagens apenas; **IMAPIFolder::CopyFolder** funciona com pastas apenas. 
  
Enquanto usando os métodos **IMAPIFolder** não requer nenhum conhecimento das propriedades compatíveis com a pasta ou mensagem devem ser copiados ou movidos, você deve ter algum conhecimento usar os métodos **IMAPIProp** . Com **IMAPIProp::CopyProps**, você deve ser capaz de especificar explicitamente que as propriedades de pasta ou uma mensagem que você deseja copiar ou mover. Com **IMAPIProp::CopyTo**, a menos que você deseja copiar ou mover todas as propriedades, você deve especificar explicitamente quais devem ser excluídos. Para obter mais informações sobre esses métodos, consulte [Copiando propriedades de MAPI](copying-mapi-properties.md).
  
O número de propriedades devem ser copiados ou movidos pode afetar sua decisão sobre qual método usar. Se você estiver copiar ou mover várias mensagens, chame **IMAPIFolder::CopyMessages**. Escolha uma alternativa é chamar **IMAPIProp::CopyProps** para copiar somente as propriedades da pasta **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)). O procedimento a seguir mostra como usar **CopyMessages**. 
  
### <a name="to-copy-or-move-one-or-more-messages"></a>Para copiar ou mover uma ou mais mensagens
  
1. Localize os identificadores de entrada válida para as pastas de origem e destino.
    
2. Abra essas pastas no modo leitura/gravação chamando [IMAPISession::OpenEntry](imapisession-openentry.md) ou [IMsgStore::OpenEntry](imsgstore-openentry.md) e definindo o sinalizador MAPI_MODIFY. 
    
3. Verifique se o ponteiro de interface retornado da **OpenEntry** é um ponteiro de interface **IMAPIFolder** . Caso contrário, converta-a para o tipo LPMAPIFOLDER. 
    
4. Crie uma matriz de identificadores de entrada que representa uma ou mais mensagens devem ser copiados ou movidos. 
    
5. Chame **IMAPIFolder::CopyMessages** com o conjunto de sinalizadores a seguir: 
    
   - MESSAGE_MOVE, se você quiser realizar uma operação de movimentação. 
    
   - MESSAGE_DIALOG e passar uma janela manipulam no parâmetro _ulUIParam_ , se quiser que a pasta para mostrar um indicador de progresso. 
    
6. Libere os ponteiros **IMAPIFolder** para as pastas de origem e destino. 
    
Se você desejar copiar todo o conteúdo de uma pasta para outra pasta, chame o método de **IMAPIFolder::CopyFolder** ou **IMAPIProp::CopyTo** da pasta de origem. 
  
Para copiar algumas das propriedades de uma pasta, chame seu método de **IMAPIProp::CopyProps** . Para copiar a maioria das propriedades de uma pasta, chame **IMAPIProp::CopyTo**. 
  
Por exemplo, se desejar copiar **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) e propriedades de **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) de uma pasta, você tem as seguintes opções:
  
- Chame **IMAPIFolder::CopyFolder** para copiar todas as propriedades de pasta e exclua aqueles indesejadas da nova pasta. 
    
- Chame **CopyTo** e exclua todas as propriedades da pasta exceto **PR_DISPLAY_NAME** e **PR_COMMENT**. 
    
- Chame **CopyProps**, passando a matriz de incluir **PR_DISPLAY_NAME** e **PR_COMMENT** . 
    
Nesse caso, **CopyProps** é a melhor opção, pois ele se destina a ser usado para copiar um pequeno conjunto de propriedades e é a chamada mais fácil para implementar. 
  
Para copiar ou mover somente as propriedades de pasta, sem incluir mensagens, chame o método de **IMAPIProp::CopyTo** da pasta e excluir as seguintes propriedades: 
  
- **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))
    
- **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))
    
Os métodos de cópia podem retornar S_OK, indicando sucesso total, MAPI_W_PARTIAL_COMPLETION, indicando êxito parcial, ou um erro. Se MAPI_W_PARTIAL_COMPLETION for retornada, use a macro **HR_FAILED** para acessar um erro mais específico. Para obter mais informações, consulte [Usando Macros para tratamento de erros](using-macros-for-error-handling.md).
  
Se você copiar mensagens do repositório de uma mensagem para outro e Unicode não é suportado para ambos, lembre-se de que as informações podem ser perdidas devido à conversão de página de código. Geralmente você não pode saber se os repositórios de mensagem dão suporte a formatos de um ou ambos, tornando impossível determinar se deseja copiar as propriedades de texto, como sequências de caracteres ASCII ou como sequências de caracteres Unicode. Caso você ofereça suporte a Unicode, tente realizar uma cópia de Unicode; Se ele falhar com o valor de erro MAPI_E_BAD_CHARWIDTH, recorrer a ASCII.
  

