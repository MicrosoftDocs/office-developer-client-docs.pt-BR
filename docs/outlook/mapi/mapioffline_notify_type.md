---
title: MAPIOFFLINE_NOTIFY_TYPE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a111d7b7-6e87-4958-8f9b-0f2adbeb8b63
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 468dfd634c4aaf18b019d06975ec9066c9d5f7a6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768004"
---
# <a name="mapiofflinenotifytype"></a><span data-ttu-id="4b08a-103">MAPIOFFLINE_NOTIFY_TYPE</span><span class="sxs-lookup"><span data-stu-id="4b08a-103">MAPIOFFLINE_NOTIFY_TYPE</span></span>

  
  
<span data-ttu-id="4b08a-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4b08a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4b08a-105">O MAPIOFFLINE_NOTIFY_TYPE de uma notificação identifica se está prestes a ser realizada uma alteração no estado de conexão, está sendo realizada ou foi concluída.</span><span class="sxs-lookup"><span data-stu-id="4b08a-105">The MAPIOFFLINE_NOTIFY_TYPE of a notification identifies if a change in the connection state is going to take place, is taking place, or has completed.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="4b08a-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="4b08a-106">Quick info</span></span>

<span data-ttu-id="4b08a-107">Consulte **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="4b08a-107">See **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
  
```cpp
typedef enum { 
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START = 1,  
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE = 2,  
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE = 3  
} MAPIOFFLINE_NOTIFY_TYPE;
```

## <a name="see-also"></a><span data-ttu-id="4b08a-108">Confira também</span><span class="sxs-lookup"><span data-stu-id="4b08a-108">See also</span></span>



[<span data-ttu-id="4b08a-109">Sobre a API de estado offline</span><span class="sxs-lookup"><span data-stu-id="4b08a-109">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="4b08a-110">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="4b08a-110">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="4b08a-111">MAPIOFFLINE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="4b08a-111">MAPIOFFLINE_NOTIFY</span></span>](mapioffline_notify.md)

