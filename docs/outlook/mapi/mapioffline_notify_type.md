---
title: MAPIOFFLINE_NOTIFY_TYPE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a111d7b7-6e87-4958-8f9b-0f2adbeb8b63
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: e7120b843eae8df70cb2c4f9cbf581dcf0e09c11
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566884"
---
# <a name="mapiofflinenotifytype"></a><span data-ttu-id="e8766-103">MAPIOFFLINE_NOTIFY_TYPE</span><span class="sxs-lookup"><span data-stu-id="e8766-103">MAPIOFFLINE_NOTIFY_TYPE</span></span>

  
  
<span data-ttu-id="e8766-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8766-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8766-105">O MAPIOFFLINE_NOTIFY_TYPE de uma notificação identifica se está prestes a ser realizada uma alteração no estado de conexão, está sendo realizada ou foi concluída.</span><span class="sxs-lookup"><span data-stu-id="e8766-105">The MAPIOFFLINE_NOTIFY_TYPE of a notification identifies if a change in the connection state is going to take place, is taking place, or has completed.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="e8766-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="e8766-106">Quick info</span></span>

<span data-ttu-id="e8766-107">Consulte **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="e8766-107">See **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
  
```cpp
typedef enum { 
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START = 1,  
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE = 2,  
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE = 3  
} MAPIOFFLINE_NOTIFY_TYPE;
```

## <a name="see-also"></a><span data-ttu-id="e8766-108">Confira também</span><span class="sxs-lookup"><span data-stu-id="e8766-108">See also</span></span>



[<span data-ttu-id="e8766-109">Sobre a API de estado offline</span><span class="sxs-lookup"><span data-stu-id="e8766-109">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="e8766-110">Constantes de MAPI</span><span class="sxs-lookup"><span data-stu-id="e8766-110">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="e8766-111">MAPIOFFLINE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="e8766-111">MAPIOFFLINE_NOTIFY</span></span>](mapioffline_notify.md)

