---
title: ISocialProviderGetSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 371b48c5-6d77-4d2d-890c-bb234c7eaabc
description: Obtém uma interface ISocialSession.
ms.openlocfilehash: 59e6f61e1954f64d875c6336b211dcb530100252
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770860"
---
# <a name="isocialprovidergetsession"></a><span data-ttu-id="730e7-103">ISocialProvider::GetSession</span><span class="sxs-lookup"><span data-stu-id="730e7-103">ISocialProvider::GetSession</span></span>

<span data-ttu-id="730e7-104">Obtém uma interface [ISocialSession](isocialsessioniunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="730e7-104">Gets an [ISocialSession](isocialsessioniunknown.md) interface.</span></span> 
  
```cpp
HRESULT _stdcall GetSession([out, retval] ISocialSession** session);
```

## <a name="parameters"></a><span data-ttu-id="730e7-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="730e7-105">Parameters</span></span>

<span data-ttu-id="730e7-106">_session_</span><span class="sxs-lookup"><span data-stu-id="730e7-106">_session_</span></span>
  
> <span data-ttu-id="730e7-107">[out] Uma interface **ISocialSession**.</span><span class="sxs-lookup"><span data-stu-id="730e7-107">[out] An **ISocialSession** interface.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="730e7-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="730e7-108">Remarks</span></span>

<span data-ttu-id="730e7-109">Outlook Social Connector (OSC) usa a interface de **ISocialSession** para fazer logon rede social.</span><span class="sxs-lookup"><span data-stu-id="730e7-109">The Outlook Social Connector (OSC) uses the **ISocialSession** interface to log on to the social network.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="730e7-110">Confira também</span><span class="sxs-lookup"><span data-stu-id="730e7-110">See also</span></span>

- [<span data-ttu-id="730e7-111">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="730e7-111">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

