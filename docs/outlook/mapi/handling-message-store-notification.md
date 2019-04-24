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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299424"
---
# <a name="handling-message-store-notification"></a>Manipular notificações do repositório de mensagens
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para registrar notificações do repositório de mensagens, chame o método [IMAPISession:: Advise](imapisession-advise.md) ou [IMsgStore:: Advise](imsgstore-advise.md) e especifique um repositório de mensagens, pasta ou identificador de entrada de mensagem no conteúdo do parâmetro _lpEntryID_ . Os provedores de repositórios de mensagens dão suporte a notificações de objeto e de tabela. Quer você se registre com objetos de repositório de mensagens específicos, com as tabelas de hierarquia de pastas e conteúdo que descrevem esses objetos, ou com os objetos e tabelas depende das notificações que você espera que você veja, as chamadas feitas para realizar operações e como o provedor de repositório de mensagens oferece suporte a notificações. 
  
Como o MAPI permite flexibilidade em como os provedores dão suporte a notificações, lembre-se de que você nem sempre receberá o mesmo tipo de notificação em resposta a um evento específico de todos os provedores de repositório de mensagens. Alguns provedores de repositórios de mensagens não dão suporte a notificações. Para determinar se o repositório de mensagens que você está usando oferece suporte à notificação, procure o bit STORE_NOTIFY_OK em sua propriedade **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).
  
Em uma extremidade do espectro de provedores de repositórios de mensagens que suportam notificações são os provedores que geram notificações "ricas"; esses provedores enviam notificações descritivas para todas as fontes de aviso registradas. No outro lado estão os provedores de repositórios de mensagens que dão suporte a notificações limitadas; esses provedores enviam notificações gerais para um número restrito de fontes de aviso. 
  
Por exemplo, se você copiar uma mensagem para uma pasta com a qual você se registrou para receber as notificações de objeto copiado e de objeto movido, poderá ou não receber a notificação de cópia do objeto. Se você recebe ou não depende de:
  
- O método que você chamou para executar a cópia. Pode ser [IMAPIFolder:: CopyMessages](imapifolder-copymessages.md), [IMAPIProp:: CopyTo](imapiprop-copyto.md)ou [IMAPIProp:: CopyProps](imapiprop-copyprops.md).
    
- Como o provedor de repositório de mensagens implementa o método Copy.
    
- Se o provedor de repositório de mensagens oferece suporte a notificações de cópia de objeto em pastas.
    
Como não há diretrizes estritas que descrevam como implementar a notificação de eventos para provedores de repositórios de mensagens, os clientes não podem esperar um comportamento consistente. O MAPI faz recomendações sobre como os provedores de repositório de mensagens implementam a notificação de eventos e a tabela a seguir descreve essas recomendações. Leia a tabela da seguinte maneira: após realizar a operação na primeira coluna, espere receber uma notificação do tipo listado na segunda coluna se você tiver registrado para esse tipo com o objeto listado na terceira coluna. Por exemplo, depois de criar uma pasta, você receberá uma notificação _fnevObjectCreated_ somente se tiver registrado para notificações do _fnevObjectCreated_ com o repositório de mensagens. 
  
|**Operação**|**Tipo de evento**|**Fonte de aviso**|
|:-----|:-----|:-----|
|Criar uma pasta  <br/> | _fnevObjectCreated_ <br/> |Repositório de mensagens  <br/> |
|Excluir uma pasta  <br/> | _fnevObjectDeleted_ <br/> |Pasta excluída do repositório de mensagens  <br/> |
|Mover uma pasta de uma pasta para outra  <br/> | _fnevObjectMoved_ <br/> |Pasta movida do repositório de mensagens  <br/> |
|Copiar uma pasta de uma pasta para outra  <br/> | _fnevObjectCopied_ <br/> |Repositório de mensagens e pasta copiada (nenhuma notificação de _fnevObjectCreated_ enviada para a nova cópia da pasta)  <br/> |
|Alterar em uma propriedade de pasta computada (**PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md)), **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md)), **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))  <br/> | _fnevObjectModified_ <br/> |Pasta de repositório de mensagens alterado (sem notificação para a pasta pai)  <br/> |
|Criar uma mensagem  <br/> | _fnevObjectCreated_ <br/> |Repositório de mensagens  <br/> |
|Excluir uma mensagem, causando uma alteração na propriedade **PR_CONTENT_COUNT** da pasta pai  <br/> | _fnevObjectDeleted_ <br/> |Mensagem excluída do repositório de mensagens  <br/> |
|Mover uma mensagem de uma pasta para outra  <br/> | _fnevObjectMoved_ <br/> |Mensagem movida do repositório de mensagens  <br/> |
|Copiar uma mensagem de uma pasta para outra  <br/> | _fnevObjectCopied_ <br/> |Mensagem de repositório de mensagens coPiada (nenhuma notificação _fnevObjectCreated_ para a nova cópia da mensagem)  <br/> |
|Salvar uma mensagem, causando uma alteração na propriedade **PR_CONTENT_COUNT** da pasta pai  <br/> | _fnevObjectCreated_ <br/> |Repositório de mensagens no primeiro salvamento  <br/> |
|Salvar uma mensagem  <br/> | _fnevObjectModified_ <br/> |Repositório de mensagens em salva após a primeira mensagem de salvamento alterada (sem notificação para a pasta pai)  <br/> |
|Concluir uma operação de pesquisa  <br/> | _fnevSearchComplete_ <br/> |Pasta de pesquisa do repositório de mensagens  <br/> |
|Nova mensagem  <br/> | _fnevNewMail_ <br/> |Repositório de mensagens  <br/> |
   
> [!NOTE]
> Quando você receber uma notificação de modificação de objeto, lembre-se de que a parte de matriz de marca de propriedade da estrutura [OBJECT_NOTIFICATION](object_notification.md) apontada pelo parâmetro _lpNotifications_ na chamada OnNotify pode ou não ser nula. **** Os provedores de repositórios de mensagens não são necessários para inserir informações de propriedade nesta matriz e a maioria não. Certifique-se **** de que o método OnNotify possa lidar com o caso em que o ponteiro _lpPropTagArray_ é nulo. 
  
Para a maioria, se não todas as notificações de objeto, atualize o modo de exibição da pasta ou pastas afetadas.
  

