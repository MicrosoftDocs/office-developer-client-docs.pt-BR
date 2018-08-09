---
title: Manipulação de notificação do repositório de mensagem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3e0cc2f9-a88d-4cec-bef5-b60f2ec80f1c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 898f8b6ff3d0b0dd42a670596b54171f18b4a5e3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766679"
---
# <a name="handling-message-store-notification"></a>Manipulação de notificação do repositório de mensagem
  
**Aplica-se a**: Outlook 
  
Para registrar para notificações do repositório de mensagens, chame o método o [IMAPISession::Advise](imapisession-advise.md) ou [IMsgStore::Advise](imsgstore-advise.md) e especifique um armazenamento de mensagens, uma pasta ou um identificador de entrada de mensagem no conteúdo do parâmetro _lpEntryID_ . Provedores de armazenamento de mensagem suportam a notificações de objeto e a tabela. Se você registrar com objetos de repositório de mensagem específica, com as tabelas de hierarquias e conteúdo de pasta que descrevem esses objetos ou com ambos os objetos e tabelas depende as notificações que o esperado, as chamadas feitas para executar operações, e como o provedor de armazenamento de mensagens oferece suporte a notificação. 
  
Como MAPI permite flexibilidade em como provedores de suportam a notificações, lembre-se de que você não sempre receberá o mesmo tipo de notificação em resposta a um evento específico de todos os provedores de armazenamento de mensagem. Alguns provedores de armazenamento de mensagem não têm suporte em todas as notificações. Para determinar se você estiver usando o armazenamento de mensagens oferece suporte a notificação, procure por estará definido o bit STORE_NOTIFY_OK na sua propriedade **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).
  
Em uma extremidade do espectro de armazenamento de mensagens os provedores que oferecem suporte a notificação são os provedores que geram notificações "rich"; Esses provedores enviam fontes de aviso descritivas notificações para todos registrado. Na outra extremidade é a mensagem provedores de armazenamento que oferecem suporte a notificações limitadas; Esses provedores enviar notificações gerais para um número restrito de advise fontes. 
  
Por exemplo, se você copiar uma mensagem para uma pasta com o qual você registrou para receber as duas objeto copiado e objeto movido notificações, você pode ou não pode receber a notificação de objeto copiado. Receber ou não depende:
  
- O método é chamado para realizar a cópia. Isso poderia ser [IMAPIFolder::CopyMessages](imapifolder-copymessages.md), [IMAPIProp::CopyTo](imapiprop-copyto.md)ou [IMAPIProp::CopyProps](imapiprop-copyprops.md).
    
- Como a mensagem armazenar provedor implementa o método copy.
    
- Ou não o provedor de armazenamento de mensagem dá suporte a notificações de objeto copiado nas pastas.
    
Porque há nenhum estrita diretrizes que descrevem como implementar a notificação de evento para mensagem provedores de armazenamento, os clientes não podem esperam um comportamento consistente. MAPI fazer recomendações de como a mensagem armazenar a notificação de evento de implementar provedores e a tabela a seguir descreve essas recomendações. Ler a tabela da seguinte maneira: depois de executar a operação na primeira coluna, espera receber uma notificação do tipo listado na segunda coluna se você registrou para aquele tipo com o objeto listado na terceira coluna. Por exemplo, depois de criar uma pasta, você receberá uma notificação _fnevObjectCreated_ somente se você registrou para notificações de _fnevObjectCreated_ com o armazenamento de mensagens. 
  
|**Operação**|**Tipo de evento**|**Aviso de origem**|
|:-----|:-----|:-----|
|Criar uma pasta  <br/> | _fnevObjectCreated_ <br/> |Armazenamento de mensagens  <br/> |
|Excluir uma pasta  <br/> | _fnevObjectDeleted_ <br/> |Pasta excluído do armazenamento de mensagens  <br/> |
|Mover uma pasta de uma pasta para outro  <br/> | _fnevObjectMoved_ <br/> |Pasta foi movido de armazenamento de mensagens  <br/> |
|Copiar uma pasta de uma pasta para outro  <br/> | _fnevObjectCopied_ <br/> |Mensagem armazenar e copiou pasta (nenhuma notificação _fnevObjectCreated_ enviada para a nova cópia da pasta)  <br/> |
|Alterar em uma propriedade de pasta computada (**PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md)), **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md)), **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))  <br/> | _fnevObjectModified_ <br/> |Mensagem armazenar pasta Changed (nenhuma notificação para a pasta pai)  <br/> |
|Criar uma mensagem  <br/> | _fnevObjectCreated_ <br/> |Armazenamento de mensagens  <br/> |
|Excluir uma mensagem, fazendo com que uma alteração no pai propriedade **PR_CONTENT_COUNT** da pasta  <br/> | _fnevObjectDeleted_ <br/> |Armazenamento de mensagens mensagem Deleted  <br/> |
|Mover uma mensagem de uma pasta para outro  <br/> | _fnevObjectMoved_ <br/> |Mensagem armazenar mensagem foram movidas  <br/> |
|Copiar uma mensagem de uma pasta para outro  <br/> | _fnevObjectCopied_ <br/> |Armazenamento de mensagens copiado mensagem (nenhum _fnevObjectCreated_ notificação para a nova cópia da mensagem)  <br/> |
|Salvar uma mensagem, fazendo com que uma alteração no pai propriedade **PR_CONTENT_COUNT** da pasta  <br/> | _fnevObjectCreated_ <br/> |Armazenamento de mensagens na primeira salvar somente  <br/> |
|Salvar uma mensagem  <br/> | _fnevObjectModified_ <br/> |Armazenamento de mensagens em gravações após o primeiro salvar mensagem Changed (nenhuma notificação para a pasta pai)  <br/> |
|Concluir uma operação de pesquisa  <br/> | _fnevSearchComplete_ <br/> |Pasta de pesquisa de armazenamento de mensagens  <br/> |
|Nova mensagem  <br/> | _fnevNewMail_ <br/> |Armazenamento de mensagens  <br/> |
   
> [!NOTE]
> Quando você recebe uma notificação de objeto modificado, lembre-se de que a parte de matriz de marca de propriedade da estrutura [OBJECT_NOTIFICATION](object_notification.md) apontada pelo parâmetro _lpNotifications_ na chamada **OnNotify** pode ou não pode ser NULL. Provedores de armazenamento de mensagens não são necessárias para inserir informações sobre a propriedade nessa matriz e mais não. Verifique se o que seu método de **OnNotify** pode manipular o caso em que o ponteiro _lpPropTagArray_ é NULL. 
  
Para a maioria, se não todos os objeto notificações, atualize o modo de exibição da pasta afetada ou pastas.
  

