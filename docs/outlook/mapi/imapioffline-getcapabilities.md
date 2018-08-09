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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 205c9dd28692592ddf133b1b30989ba9fd4236f1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767104"
---
# <a name="imapiofflinegetcapabilities"></a><span data-ttu-id="f85d6-103">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="f85d6-103">IMAPIOffline::GetCapabilities</span></span>

  
  
<span data-ttu-id="f85d6-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f85d6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f85d6-105">Obtém as condições para o qual os retornos de chamada são suportados por um objeto offline.</span><span class="sxs-lookup"><span data-stu-id="f85d6-105">Gets the conditions for which callbacks are supported by an offline object.</span></span>
  
```cpp
HRESULT GetCapabilities( 
    ULONG *pulCapabilities 
);
```

## <a name="parameters"></a><span data-ttu-id="f85d6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f85d6-106">Parameters</span></span>

 <span data-ttu-id="f85d6-107">_pulCapablities_</span><span class="sxs-lookup"><span data-stu-id="f85d6-107">_pulCapablities_</span></span>
  
> <span data-ttu-id="f85d6-108">[out] Uma bitmask dos sinalizadores de recurso a seguir:</span><span class="sxs-lookup"><span data-stu-id="f85d6-108">[out] A bitmask of the following capability flags:</span></span>
    
<span data-ttu-id="f85d6-109">MAPIOFFLINE_CAPABILITY_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="f85d6-109">MAPIOFFLINE_CAPABILITY_OFFLINE</span></span>
  
> <span data-ttu-id="f85d6-110">O objeto offline é capaz de fornecer notificações offline.</span><span class="sxs-lookup"><span data-stu-id="f85d6-110">The offline object is capable of providing offline notifications.</span></span>
    
<span data-ttu-id="f85d6-111">MAPIOFFLINE_CAPABILITY_ONLINE</span><span class="sxs-lookup"><span data-stu-id="f85d6-111">MAPIOFFLINE_CAPABILITY_ONLINE</span></span>
  
> <span data-ttu-id="f85d6-112">O objeto offline é capaz de fornecer notificações online.</span><span class="sxs-lookup"><span data-stu-id="f85d6-112">The offline object is capable of providing online notifications.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f85d6-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="f85d6-113">Remarks</span></span>

<span data-ttu-id="f85d6-114">Ao abrir um objeto offline usando **[HrOpenOfflineObj](hropenofflineobj.md)**, um cliente pode consultar em [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) para obter um ponteiro para uma interface **IMAPIOffline** e chamadas **IMAPIOffline::GetCapabilities** para descobrir os retornos de chamada com suporte pelo objeto.</span><span class="sxs-lookup"><span data-stu-id="f85d6-114">Upon opening an offline object using **[HrOpenOfflineObj](hropenofflineobj.md)**, a client can query on [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) to obtain a pointer to an **IMAPIOffline** interface, and call **IMAPIOffline::GetCapabilities** to find out the callbacks supported by the object.</span></span> <span data-ttu-id="f85d6-115">O cliente pode optar por configurar retornos de chamada usando **IMAPIOfflineMgr**.</span><span class="sxs-lookup"><span data-stu-id="f85d6-115">The client can then choose to set up callbacks by using **IMAPIOfflineMgr**.</span></span>
  
<span data-ttu-id="f85d6-116">Observe que, dependendo do servidor de email para um objeto offline, um objeto que oferece suporte a retornos de chamada para o modo online não necessariamente suporta retornos de chamada para entrar no modo offline.</span><span class="sxs-lookup"><span data-stu-id="f85d6-116">Note that, depending on the mail server for an offline object, an object that supports callbacks for going online does not necessarily support callbacks for going offline.</span></span>
  
<span data-ttu-id="f85d6-117">Observe também que, enquanto um objeto offline pode suportar retornos de chamada para alterações que não seja online offline, a API de estado Offline suporta apenas alterações online offline e os clientes precisam verificar para apenas esses recursos.</span><span class="sxs-lookup"><span data-stu-id="f85d6-117">Also note that, while an offline object may support callbacks for changes other than online/offline, the Offline State API supports only online/offline changes, and clients must check for only such capabilities.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f85d6-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="f85d6-118">See also</span></span>



[<span data-ttu-id="f85d6-119">IMAPIOffline::GetCurrentState</span><span class="sxs-lookup"><span data-stu-id="f85d6-119">IMAPIOffline::GetCurrentState</span></span>](imapioffline-getcurrentstate.md)
  
[<span data-ttu-id="f85d6-120">IMAPIOffline::SetCurrentState</span><span class="sxs-lookup"><span data-stu-id="f85d6-120">IMAPIOffline::SetCurrentState</span></span>](imapioffline-setcurrentstate.md)
  
[<span data-ttu-id="f85d6-121">IMAPIOfflineMgr : IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="f85d6-121">IMAPIOfflineMgr : IMAPIOffline</span></span>](imapiofflinemgrimapioffline.md)


[<span data-ttu-id="f85d6-122">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="f85d6-122">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="f85d6-123">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="f85d6-123">HrOpenOfflineObj</span></span>](hropenofflineobj.md)

