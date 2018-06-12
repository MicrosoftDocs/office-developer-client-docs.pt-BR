---
title: Sobre a indexação do repositório baseada em notificação
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: b3685890-117c-9acc-e19f-cf22a349a088
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 338ae3c3c8d8b4037ab0c7b46916e45cf5a8ded2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766093"
---
# <a name="about-notification-based-store-indexing"></a>Sobre a indexação do repositório baseada em notificação

  
  
**Aplica-se a**: Outlook 
  
Um provedor de repositório MAPI pode especificar se o manipulador de protocolo MAPI rastreamentos e índices de mensagens no repositório ou se o repositório envia notificações para o indexador quando há mensagens a serem indexados. O último é conhecido como indexação baseada em notificação e um repositório que ofereça suporte a indexação baseada em notificação é um conhecido como um repositório pusher.
  
Um provedor de armazenamento que ofereça suporte a conjuntos de indexação baseados em notificação o sinalizador **STORE_PUSHER_OK** na propriedade **[PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** . O manipulador de protocolo MAPI ou um cliente pode obter a propriedade **PR_STORE_SUPPORT_MASK** para determinar as características do repositório. 
  
Sempre que houver um anexo, pasta ou uma mensagem a ser indexado, o provedor de armazenamento gera um MAPI URL Uniform Resource Locator () que identifica o objeto a ser indexado e enviá-la para o indexador. Essa URL MAPI é codificado em Unicode e deve identificar exclusivamente o objeto para o manipulador de protocolo de MAPI. Para obter mais informações sobre URLs de MAPI, consulte [Sobre URLs de MAPI para indexação com base em notificação](about-mapi-urls-for-notification-based-indexing.md).
  
Porque um indexador sempre não pode indexar tudo antes da ocorrência de um desligamento em um repositório pusher, o repositório de pusher deve persistir o que precisa ser enviada. Quando um provedor de armazenamento envia uma notificação sobre um objeto que precisa ser indexado, ele especifica o tipo de notificação **fnevIndexing** no membro **ulEventType** da estrutura de **[notificação](notification.md)** . O membro **info** da estrutura de **notificação** contém uma estrutura **[EXTENDED_NOTIFICATION](extended_notification.md)** . O provedor de armazenamento identifica o processo na propriedade **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)** . Ele também identifica o processo na estrutura de [INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md) e passa essas informações como parte do membro **pbEventParameters** da estrutura **EXTENDED_NOTIFICATION** . Se o processo for desligado ou falha, o manipulador de protocolo MAPI poderão detectar que imediatamente e interromper a indexação o repositório pusher. 
  
## <a name="see-also"></a>Confira também



[Sobre o API de armazenamento](about-the-store-api.md)
  
[Constantes MAPI](mapi-constants.md)

