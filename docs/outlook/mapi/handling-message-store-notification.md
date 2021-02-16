---
title: Manipular notificações do repositório de mensagens
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3e0cc2f9-a88d-4cec-bef5-b60f2ec80f1c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d370603dc7cfc015fe7b2757d1cf0525b3092c5e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428022"
---
# <a name="handling-message-store-notification"></a>Manipular notificações do repositório de mensagens
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para registrar as notificações do repositório de mensagens, chame o método [IMAPISession::Advise](imapisession-advise.md) ou [IMsgStore::Advise](imsgstore-advise.md) e especifique um identificador de entrada de mensagem, pasta ou repositório de mensagens no conteúdo do parâmetro _lpEntryID._ Provedores de armazenamento de mensagens suportam notificações de objeto e tabela. Se você se registrar com objetos de armazenamento de mensagens específicos, com a hierarquia de pastas e as tabelas de conteúdo que descrevem esses objetos ou com objetos e tabelas depende das notificações que você espera ver, das chamadas que você faz para executar operações e de como o provedor de armazenamento de mensagens oferece suporte à notificação. 
  
Como o MAPI permite flexibilidade na forma como os provedores oferecem suporte a notificações, esteja ciente de que você nem sempre receberá o mesmo tipo de notificação em resposta a um evento específico de todos os provedores de armazenamento de mensagens. Alguns provedores de armazenamento de mensagens não suportam notificações. Para determinar se o repositório de mensagens que você está usando oferece suporte à notificação, procure o STORE_NOTIFY_OK bit em sua **propriedade PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).
  
Em uma extremidade do espectro de provedores de armazenamento de mensagens que suportam a notificação estão os provedores que geram notificações "rica"; esses provedores enviam notificações descritivas para todas as fontes de aviso registradas. Na outra extremidade estão os provedores de armazenamento de mensagens que suportam notificações limitadas; esses provedores enviam notificações gerais para um número restrito de fontes de aviso. 
  
Por exemplo, se você copiar uma mensagem para uma pasta com a qual registrou para receber notificações de objeto copiado e movido de objeto, poderá ou não receber a notificação de objeto copiado. O recebimento ou não depende de:
  
- O método que você chamou para executar a cópia. Pode ser [IMAPIFolder::CopyMessages](imapifolder-copymessages.md), [IMAPIProp::CopyTo](imapiprop-copyto.md)ou [IMAPIProp::CopyProps](imapiprop-copyprops.md).
    
- Como o provedor de armazenamento de mensagens implementa o método de cópia.
    
- Se o provedor de armazenamento de mensagens oferece suporte ou não a notificações de objeto copiado em pastas.
    
Como não há diretrizes estritas que descrevem como implementar a notificação de eventos para provedores de armazenamento de mensagens, os clientes não podem esperar um comportamento consistente. O MAPI faz recomendações sobre como os provedores de armazenamento de mensagens implementam a notificação de eventos e a tabela a seguir descreve essas recomendações. Leia a tabela da seguinte forma: depois de executar a operação na primeira coluna, espere receber uma notificação do tipo listado na segunda coluna se você tiver registrado para esse tipo com o objeto listado na terceira coluna. Por exemplo, depois de criar uma pasta, você receberá uma notificação  _fnevObjectCreated_ somente se tiver registrado notificações  _fnevObjectCreated_ com o armazenamento de mensagens. 
  
|**Operação**|**Tipo de evento**|**Fonte de consultoria**|
|:-----|:-----|:-----|
|Criar uma pasta  <br/> | _fnevObjectCreated_ <br/> |Armazenamento de mensagens  <br/> |
|Excluir uma pasta  <br/> | _fnevObjectDeleted_ <br/> |Pasta Excluída do armazenamento de mensagens  <br/> |
|Mover uma pasta de uma pasta para outra  <br/> | _fnevObjectMoved_ <br/> |Pasta De movimentada do armazenamento de mensagens  <br/> |
|Copiar uma pasta de uma pasta para outra  <br/> | _fnevObjectCopied_ <br/> |Armazenamento de mensagens e pasta copiada (nenhuma  _notificação fnevObjectCreated_ enviada para a nova cópia da pasta)  <br/> |
|Alterar em uma propriedade de pasta computada (**PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md)), **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md)), **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))  <br/> | _fnevObjectModified_ <br/> |Pasta De alterações do armazenamento de mensagens (sem notificação para a pasta pai)  <br/> |
|Criar uma mensagem  <br/> | _fnevObjectCreated_ <br/> |Armazenamento de mensagens  <br/> |
|Excluir uma mensagem, causando uma alteração na propriedade PR_CONTENT_COUNT **pasta** pai  <br/> | _fnevObjectDeleted_ <br/> |Mensagem excluída do armazenamento de mensagens  <br/> |
|Mover uma mensagem de uma pasta para outra  <br/> | _fnevObjectMoved_ <br/> |Mensagem movida do armazenamento de mensagens  <br/> |
|Copiar uma mensagem de uma pasta para outra  <br/> | _fnevObjectCopied_ <br/> |Mensagem copiada do armazenamento de mensagens (nenhuma  _notificação fnevObjectCreated_ para nova cópia da mensagem)  <br/> |
|Salvar uma mensagem, causando uma alteração na propriedade PR_CONTENT_COUNT **pasta** pai  <br/> | _fnevObjectCreated_ <br/> |Armazenamento de mensagens no primeiro salvar somente  <br/> |
|Salvar uma mensagem  <br/> | _fnevObjectModified_ <br/> |Armazenamento de mensagens ao salvar após a primeira mensagem de salvar Alterado (nenhuma notificação para a pasta pai)  <br/> |
|Concluir uma operação de pesquisa  <br/> | _fnevSearchComplete_ <br/> |Pasta de Pesquisa do armazenamento de mensagens  <br/> |
|Nova mensagem  <br/> | _fnevNewMail_ <br/> |Armazenamento de mensagens  <br/> |
   
> [!NOTE]
> Quando você receber uma notificação de modificação de objeto, lembre-se de que a parte da matriz de marca de propriedade da estrutura [OBJECT_NOTIFICATION](object_notification.md) apontada pelo parâmetro  _lpNotifications_ na chamada **OnNotify** pode ou não ser NULL. Os provedores de armazenamento de mensagens não são obrigados a inserir informações de propriedade nessa matriz e a maioria não. Certifique-se **de que seu método OnNotify** possa lidar com o caso em que o ponteiro  _lpPropTagArray_ é NULL. 
  
Para a maioria, se não todas as notificações de objeto, atualize a exibição da pasta ou pastas afetadas.
  

