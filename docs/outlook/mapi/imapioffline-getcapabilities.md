---
title: IMAPIOfflineGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOffline.GetCapabilities
api_type:
- COM
ms.assetid: aa8dc48b-9e1c-8da0-9579-10b7174e99de
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 48d59d17d81da2ae78348a57ad8b1cb75486b1a0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321312"
---
# <a name="imapiofflinegetcapabilities"></a><span data-ttu-id="ff2dd-103">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="ff2dd-103">IMAPIOffline::GetCapabilities</span></span>

  
  
<span data-ttu-id="ff2dd-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff2dd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ff2dd-105">Obtém as condições para as quais os retornos de chamada são compatíveis com um objeto offline.</span><span class="sxs-lookup"><span data-stu-id="ff2dd-105">Gets the conditions for which callbacks are supported by an offline object.</span></span>
  
```cpp
HRESULT GetCapabilities( 
    ULONG *pulCapabilities 
);
```

## <a name="parameters"></a><span data-ttu-id="ff2dd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ff2dd-106">Parameters</span></span>

 <span data-ttu-id="ff2dd-107">_pulCapablities_</span><span class="sxs-lookup"><span data-stu-id="ff2dd-107">_pulCapablities_</span></span>
  
> <span data-ttu-id="ff2dd-108">bota Uma bitmask dos seguintes sinalizadores de recurso:</span><span class="sxs-lookup"><span data-stu-id="ff2dd-108">[out] A bitmask of the following capability flags:</span></span>
    
<span data-ttu-id="ff2dd-109">MAPIOFFLINE_CAPABILITY_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="ff2dd-109">MAPIOFFLINE_CAPABILITY_OFFLINE</span></span>
  
> <span data-ttu-id="ff2dd-110">O objeto offline é capaz de fornecer notificações offline.</span><span class="sxs-lookup"><span data-stu-id="ff2dd-110">The offline object is capable of providing offline notifications.</span></span>
    
<span data-ttu-id="ff2dd-111">MAPIOFFLINE_CAPABILITY_ONLINE</span><span class="sxs-lookup"><span data-stu-id="ff2dd-111">MAPIOFFLINE_CAPABILITY_ONLINE</span></span>
  
> <span data-ttu-id="ff2dd-112">O objeto offline é capaz de fornecer notificações online.</span><span class="sxs-lookup"><span data-stu-id="ff2dd-112">The offline object is capable of providing online notifications.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ff2dd-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="ff2dd-113">Remarks</span></span>

<span data-ttu-id="ff2dd-114">Ao abrir um objeto offline usando o **[HrOpenOfflineObj](hropenofflineobj.md)**, um cliente pode consultar no [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) para obter um ponteiro para uma interface do **IMAPIOffline** e chamar **IMAPIOffline:: GetCapabilities** para descobrir os retornos de chamada suportados pelo objeto.</span><span class="sxs-lookup"><span data-stu-id="ff2dd-114">Upon opening an offline object using **[HrOpenOfflineObj](hropenofflineobj.md)**, a client can query on [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) to obtain a pointer to an **IMAPIOffline** interface, and call **IMAPIOffline::GetCapabilities** to find out the callbacks supported by the object.</span></span> <span data-ttu-id="ff2dd-115">O cliente pode optar por configurar os retornos de chamada usando o **IMAPIOfflineMgr**.</span><span class="sxs-lookup"><span data-stu-id="ff2dd-115">The client can then choose to set up callbacks by using **IMAPIOfflineMgr**.</span></span>
  
<span data-ttu-id="ff2dd-116">Observe que, dependendo do servidor de email para um objeto offline, um objeto que oferece suporte a retornos de chamada para ficar online não necessariamente oferece suporte a retornos de chamada para ficar offline.</span><span class="sxs-lookup"><span data-stu-id="ff2dd-116">Note that, depending on the mail server for an offline object, an object that supports callbacks for going online does not necessarily support callbacks for going offline.</span></span>
  
<span data-ttu-id="ff2dd-117">Observe também que, enquanto um objeto offline pode dar suporte a retornos de chamada para alterações diferentes de online/offline, a API de estado offline oferece suporte somente a alterações online/offline, e os clientes devem verificar apenas esses recursos.</span><span class="sxs-lookup"><span data-stu-id="ff2dd-117">Also note that, while an offline object may support callbacks for changes other than online/offline, the Offline State API supports only online/offline changes, and clients must check for only such capabilities.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ff2dd-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="ff2dd-118">See also</span></span>



[<span data-ttu-id="ff2dd-119">IMAPIOffline::GetCurrentState</span><span class="sxs-lookup"><span data-stu-id="ff2dd-119">IMAPIOffline::GetCurrentState</span></span>](imapioffline-getcurrentstate.md)
  
[<span data-ttu-id="ff2dd-120">IMAPIOffline::SetCurrentState</span><span class="sxs-lookup"><span data-stu-id="ff2dd-120">IMAPIOffline::SetCurrentState</span></span>](imapioffline-setcurrentstate.md)
  
[<span data-ttu-id="ff2dd-121">IMAPIOfflineMgr : IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="ff2dd-121">IMAPIOfflineMgr : IMAPIOffline</span></span>](imapiofflinemgrimapioffline.md)


[<span data-ttu-id="ff2dd-122">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="ff2dd-122">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="ff2dd-123">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="ff2dd-123">HrOpenOfflineObj</span></span>](hropenofflineobj.md)

