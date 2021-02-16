---
title: Sobre Notification-Based Store Indexação
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: b3685890-117c-9acc-e19f-cf22a349a088
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 3dd551dd0c1ea229381e5dd01c5cf6fa04790c30
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409171"
---
# <a name="about-notification-based-store-indexing"></a>Sobre Notification-Based Store Indexação

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um provedor de armazenamento MAPI pode especificar se o Manipulador de Protocolo MAPI rastreará e indexa mensagens no armazenamento ou se o armazenamento enviará notificações ao indexador quando houver mensagens a serem indexadas. O último é conhecido como indexação baseada em notificação, e um armazenamento que oferece suporte à indexação baseada em notificação é conhecido como um armazenamento por push.
  
Um provedor de armazenamento que oferece suporte à indexação baseada em notificação define **o STORE_PUSHER_OK** de dados na **[PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** propriedade. O Manipulador de Protocolo MAPI ou um cliente pode obter a **PR_STORE_SUPPORT_MASK** para determinar as características do armazenamento. 
  
Sempre que houver um anexo, pasta ou mensagem a ser indexada, o provedor de armazenamento gera uma URL (Uniform Resource Locator) MAPI que identifica o objeto a ser indexado e o envia ao indexador. Essa URL MAPI é codificada em Unicode e deve identificar exclusivamente o objeto para o Manipulador de Protocolo MAPI. Para obter mais informações sobre URLs MAPI, consulte [Sobre URLs MAPI para Notification-Based indexação.](about-mapi-urls-for-notification-based-indexing.md)
  
Como um indexador não pode sempre indexar tudo antes que um desligamento ocorra em um armazenamento por push, o armazenamento do pusher deve manter o que precisa ser pressionado. Quando um provedor de armazenamento envia uma notificação sobre um objeto que precisa ser indexado, ele especifica o tipo de notificação **fnevIndexing** no **membro ulEventType** da estrutura **[NOTIFICATION.](notification.md)** A **estrutura** do membro de informações da **estrutura de** NOTIFICAÇÃO contém **[uma estrutura de](extended_notification.md)** EXTENDED_NOTIFICATION. O provedor do armazenamento identifica o processo **[na](pidtagsearchownerid-canonical-property.md)** PR_SEARCH_OWNER_ID propriedade. Ele também identifica o processo na estrutura [INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md) e passa essas informações como parte do membro **pbEventParameters** da estrutura **EXTENDED_NOTIFICATION** estrutura. Se o processo for encerrado ou falhar, o Manipulador de Protocolo MAPI poderá detectar imediatamente isso e parar de indexar o armazenamento do pusher. 
  
## <a name="see-also"></a>Confira também



[Sobre a API de Armazenamento](about-the-store-api.md)
  
[Constantes de MAPI](mapi-constants.md)

