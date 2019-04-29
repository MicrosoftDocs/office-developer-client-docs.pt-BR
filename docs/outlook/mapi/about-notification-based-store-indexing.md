---
title: Sobre a indexação de repositórios baseados em notificação
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
# <a name="about-notification-based-store-indexing"></a>Sobre a indexação de repositórios baseados em notificação

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um provedor de repositório MAPI pode especificar se o manipulador de protocolo MAPI rastreia e indexa mensagens no repositório ou se o repositório enviará notificações ao indexador quando houver mensagens a serem indexadas. O último é conhecido como indexação baseada em notificação, e um repositório que dá suporte à indexação baseada em notificação é conhecido como um repositório de envio.
  
Um provedor de repositório que oferece suporte à indexação baseada em notificação define o sinalizador **STORE_PUSHER_OK** na propriedade **[PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** . O manipulador de protocolo MAPI ou um cliente pode obter a propriedade **PR_STORE_SUPPORT_MASK** para determinar as características do repositório. 
  
Sempre que houver um anexo, uma pasta ou uma mensagem a ser indexada, o provedor de repositório gerará um URL (Uniform Resource Locator) MAPI que identifica o objeto a ser indexado e o enviará ao indexador. Essa URL MAPI é codificada em Unicode e deve identificar exclusivamente o objeto para o manipulador de protocolo MAPI. Para obter mais informações sobre URLs MAPI, consulte [sobre URLs MAPI para indexAção baseada em notificação](about-mapi-urls-for-notification-based-indexing.md).
  
Como o indexador não pode sempre indexar tudo antes que ocorra um desligamento em um repositório de envio, o repositório de envio deve persistir o que precisa ser enviado. Quando um provedor de armazenamento envia uma notificação sobre um objeto que precisa ser indexado, ele especifica o tipo de notificação **especificarfnevindexing** no membro **ulEventType** da estrutura de **[notificação](notification.md)** . A **estrutura** do membro de informações da **estrutura de **NOTIFICAÇÃO contém **[uma estrutura de ](extended_notification.md)** EXTENDED_NOTIFICATION. O provedor de repositório identifica o processo na propriedade **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)** . Ele também identifica o processo na estrutura [INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md) e passa essas informações como parte do membro **PbEventParameters** da estrutura **EXTENDED_NOTIFICATION** . Se o processo for desligado ou falhar, o manipulador de protocolo MAPI poderá detectar imediatamente e parar de indexar o repositório de envio. 
  
## <a name="see-also"></a>Confira também



[Sobre a API de Armazenamento](about-the-store-api.md)
  
[Constantes de MAPI](mapi-constants.md)

