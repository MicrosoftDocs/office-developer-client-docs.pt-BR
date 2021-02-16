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
ms.openlocfilehash: 65ed848907e196c315e8ddb61c4afd2fe03faa18
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413427"
---
# <a name="mapioffline_notify_type"></a><span data-ttu-id="c40bb-103">MAPIOFFLINE_NOTIFY_TYPE</span><span class="sxs-lookup"><span data-stu-id="c40bb-103">MAPIOFFLINE_NOTIFY_TYPE</span></span>

  
  
<span data-ttu-id="c40bb-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c40bb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c40bb-105">O MAPIOFFLINE_NOTIFY_TYPE de uma notificação identifica se uma alteração no estado da conexão ocorrerá, se está ocorrendo ou se foi concluída.</span><span class="sxs-lookup"><span data-stu-id="c40bb-105">The MAPIOFFLINE_NOTIFY_TYPE of a notification identifies if a change in the connection state is going to take place, is taking place, or has completed.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="c40bb-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="c40bb-106">Quick info</span></span>

<span data-ttu-id="c40bb-107">Consulte **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="c40bb-107">See **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
  
```cpp
typedef enum { 
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START = 1,  
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE = 2,  
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE = 3  
} MAPIOFFLINE_NOTIFY_TYPE;
```

## <a name="see-also"></a><span data-ttu-id="c40bb-108">Confira também</span><span class="sxs-lookup"><span data-stu-id="c40bb-108">See also</span></span>



[<span data-ttu-id="c40bb-109">Sobre a API de estado offline</span><span class="sxs-lookup"><span data-stu-id="c40bb-109">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="c40bb-110">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="c40bb-110">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="c40bb-111">MAPIOFFLINE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="c40bb-111">MAPIOFFLINE_NOTIFY</span></span>](mapioffline_notify.md)

