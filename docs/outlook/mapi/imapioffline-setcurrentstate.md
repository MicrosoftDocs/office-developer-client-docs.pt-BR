---
title: IMAPIOfflineSetCurrentState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOffline.SetCurrentState
api_type:
- COM
ms.assetid: c0aa0df2-79f9-2558-7eb6-accae9bef4b2
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 0b6837b51b09ecd9a60630c613e1806cb10c1d87
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321207"
---
# <a name="imapiofflinesetcurrentstate"></a><span data-ttu-id="c398f-103">IMAPIOffline::SetCurrentState</span><span class="sxs-lookup"><span data-stu-id="c398f-103">IMAPIOffline::SetCurrentState</span></span>

  
  
<span data-ttu-id="c398f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c398f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c398f-105">Define o estado atual de um objeto offline para online ou offline.</span><span class="sxs-lookup"><span data-stu-id="c398f-105">Sets the current state of an offline object to online or offline.</span></span>
  
```cpp
HRESULT SetCurrentState( 
    ULONG ulFlags, 
    ULONG ulMask, 
    ULONG ulState, 
    void* pReserved 
);
```

## <a name="parameters"></a><span data-ttu-id="c398f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c398f-106">Parameters</span></span>

 <span data-ttu-id="c398f-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c398f-107">_ulFlags_</span></span>
  
> <span data-ttu-id="c398f-108">no Modifica o comportamento dessa chamada.</span><span class="sxs-lookup"><span data-stu-id="c398f-108">[in] Modifies the behavior of this call.</span></span> <span data-ttu-id="c398f-109">Os valores com suporte são:</span><span class="sxs-lookup"><span data-stu-id="c398f-109">The supported values are:</span></span>
    
<span data-ttu-id="c398f-110">MAPIOFFLINE_FLAG_BLOCK</span><span class="sxs-lookup"><span data-stu-id="c398f-110">MAPIOFFLINE_FLAG_BLOCK</span></span>
  
> <span data-ttu-id="c398f-111">A definição de _parâmetroulflags_ para esse valor bloqueará a chamada setcurrentstate até a alteração de Estado ser concluída. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="c398f-111">Setting  _ulFlags_ to this value will block the **SetCurrentState** call until the state change is complete.</span></span> <span data-ttu-id="c398f-112">Por padrão, a transição ocorre de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="c398f-112">By default the transition takes place asynchronously.</span></span> <span data-ttu-id="c398f-113">Quando a transição ocorrer de forma assíncrona, \*\*\*\* todas as chamadas setcurrentstate retornarão **E_PENDING** até que a alteração seja concluída.</span><span class="sxs-lookup"><span data-stu-id="c398f-113">When the transition is occuring asynchronously, all **SetCurrentState** calls will return **E_PENDING** until the change is complete.</span></span> 
    
<span data-ttu-id="c398f-114">MAPIOFFLINE_FLAG_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="c398f-114">MAPIOFFLINE_FLAG_DEFAULT</span></span>
  
> <span data-ttu-id="c398f-115">Define o estado atual sem bloqueio.</span><span class="sxs-lookup"><span data-stu-id="c398f-115">Sets the current state without blocking.</span></span>
    
 <span data-ttu-id="c398f-116">_ulMask_</span><span class="sxs-lookup"><span data-stu-id="c398f-116">_ulMask_</span></span>
  
> <span data-ttu-id="c398f-117">no A parte do estado a ser alterada.</span><span class="sxs-lookup"><span data-stu-id="c398f-117">[in] The part of the state to change.</span></span> <span data-ttu-id="c398f-118">O único valor com suporte é MAPIOFFLINE_STATE_OFFLINE_MASK.</span><span class="sxs-lookup"><span data-stu-id="c398f-118">The only supported value is MAPIOFFLINE_STATE_OFFLINE_MASK.</span></span>
    
 <span data-ttu-id="c398f-119">_ulState_</span><span class="sxs-lookup"><span data-stu-id="c398f-119">_ulState_</span></span>
  
> <span data-ttu-id="c398f-120">no O estado para o qual mudar.</span><span class="sxs-lookup"><span data-stu-id="c398f-120">[in] The state to change to.</span></span> <span data-ttu-id="c398f-121">Deve ser um destes dois valores:</span><span class="sxs-lookup"><span data-stu-id="c398f-121">It must be one of these two values:</span></span>
    
<span data-ttu-id="c398f-122">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="c398f-122">MAPIOFFLINE_STATE_ONLINE</span></span>
  
> 
    
<span data-ttu-id="c398f-123">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="c398f-123">MAPIOFFLINE_STATE_OFFLINE</span></span>
  
> 
    
 <span data-ttu-id="c398f-124">_Enquanto_</span><span class="sxs-lookup"><span data-stu-id="c398f-124">_pReserved_</span></span>
  
> <span data-ttu-id="c398f-125">Este parâmetro é reservado para uso interno do Outlook e não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="c398f-125">This parameter is reserved for Outlook internal use and is not supported.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c398f-126">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="c398f-126">Return value</span></span>

<span data-ttu-id="c398f-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="c398f-127">S_OK</span></span>
  
> <span data-ttu-id="c398f-128">O estado do objeto offline foi alterado com êxito.</span><span class="sxs-lookup"><span data-stu-id="c398f-128">The state of the offline object has been changed successfully.</span></span>
    
<span data-ttu-id="c398f-129">E_PENDING</span><span class="sxs-lookup"><span data-stu-id="c398f-129">E_PENDING</span></span>
  
> <span data-ttu-id="c398f-130">Isso indica que o estado do objeto offline está mudando de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="c398f-130">This indicates that the state of the offline object is changing asynchronously.</span></span> <span data-ttu-id="c398f-131">Isso ocorre quando o _parâmetroulflags_ é definido como MAPIOFFLINE_FLAG_BLOCK em uma \*\*\*\* chamada setcurrentstate anterior e qualquer chamada \*\*\*\* setcurrentstate subsequente retornará esse valor até que a alteração de estado assíncrona seja concluída.</span><span class="sxs-lookup"><span data-stu-id="c398f-131">This occurs when  _ulFlags_ is set to MAPIOFFLINE_FLAG_BLOCK in an earlier **SetCurrentState** call, and any subsequent **SetCurrentState** call will return this value until the asynchronous state change is complete.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="c398f-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="c398f-132">See also</span></span>



[<span data-ttu-id="c398f-133">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="c398f-133">IMAPIOffline::GetCapabilities</span></span>](imapioffline-getcapabilities.md)
  
[<span data-ttu-id="c398f-134">IMAPIOffline::GetCurrentState</span><span class="sxs-lookup"><span data-stu-id="c398f-134">IMAPIOffline::GetCurrentState</span></span>](imapioffline-getcurrentstate.md)


[<span data-ttu-id="c398f-135">Constantes de MAPI</span><span class="sxs-lookup"><span data-stu-id="c398f-135">MAPI Constants</span></span>](mapi-constants.md)

