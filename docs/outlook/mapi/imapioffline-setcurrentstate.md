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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 15e2d5c2aca595c3a06d215cd069c23da3e48125
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767112"
---
# <a name="imapiofflinesetcurrentstate"></a><span data-ttu-id="576ec-103">IMAPIOffline::SetCurrentState</span><span class="sxs-lookup"><span data-stu-id="576ec-103">IMAPIOffline::SetCurrentState</span></span>

  
  
<span data-ttu-id="576ec-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="576ec-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="576ec-105">Define o estado atual de um objeto offline para online ou offline.</span><span class="sxs-lookup"><span data-stu-id="576ec-105">Sets the current state of an offline object to online or offline.</span></span>
  
```cpp
HRESULT SetCurrentState( 
    ULONG ulFlags, 
    ULONG ulMask, 
    ULONG ulState, 
    void* pReserved 
);
```

## <a name="parameters"></a><span data-ttu-id="576ec-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="576ec-106">Parameters</span></span>

 <span data-ttu-id="576ec-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="576ec-107">_ulFlags_</span></span>
  
> <span data-ttu-id="576ec-108">[in] Modifica o comportamento desta chamada.</span><span class="sxs-lookup"><span data-stu-id="576ec-108">[in] Modifies the behavior of this call.</span></span> <span data-ttu-id="576ec-109">Os valores suportados são:</span><span class="sxs-lookup"><span data-stu-id="576ec-109">The supported values are:</span></span>
    
<span data-ttu-id="576ec-110">MAPIOFFLINE_FLAG_BLOCK</span><span class="sxs-lookup"><span data-stu-id="576ec-110">MAPIOFFLINE_FLAG_BLOCK</span></span>
  
> <span data-ttu-id="576ec-111">A definição de _ulFlags_ como esse valor bloqueará a chamada **SetCurrentState** até que a alteração de estado seja concluída.</span><span class="sxs-lookup"><span data-stu-id="576ec-111">Setting  _ulFlags_ to this value will block the **SetCurrentState** call until the state change is complete.</span></span> <span data-ttu-id="576ec-112">Por padrão a transição é feita de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="576ec-112">By default the transition takes place asynchronously.</span></span> <span data-ttu-id="576ec-113">Quando a transição está ocorrendo de forma assíncrona, todas as chamadas **SetCurrentState** retornará **E_PENDING** até que a alteração seja concluída.</span><span class="sxs-lookup"><span data-stu-id="576ec-113">When the transition is occuring asynchronously, all **SetCurrentState** calls will return **E_PENDING** until the change is complete.</span></span> 
    
<span data-ttu-id="576ec-114">MAPIOFFLINE_FLAG_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="576ec-114">MAPIOFFLINE_FLAG_DEFAULT</span></span>
  
> <span data-ttu-id="576ec-115">Define o estado atual sem bloqueio.</span><span class="sxs-lookup"><span data-stu-id="576ec-115">Sets the current state without blocking.</span></span>
    
 <span data-ttu-id="576ec-116">_ulMask_</span><span class="sxs-lookup"><span data-stu-id="576ec-116">_ulMask_</span></span>
  
> <span data-ttu-id="576ec-117">[in] A parte do estado para alterar.</span><span class="sxs-lookup"><span data-stu-id="576ec-117">[in] The part of the state to change.</span></span> <span data-ttu-id="576ec-118">O único valor com suporte é MAPIOFFLINE_STATE_OFFLINE_MASK.</span><span class="sxs-lookup"><span data-stu-id="576ec-118">The only supported value is MAPIOFFLINE_STATE_OFFLINE_MASK.</span></span>
    
 <span data-ttu-id="576ec-119">_ulState_</span><span class="sxs-lookup"><span data-stu-id="576ec-119">_ulState_</span></span>
  
> <span data-ttu-id="576ec-120">[in] Para alterar para o estado.</span><span class="sxs-lookup"><span data-stu-id="576ec-120">[in] The state to change to.</span></span> <span data-ttu-id="576ec-121">Ele deve ser um destes dois valores:</span><span class="sxs-lookup"><span data-stu-id="576ec-121">It must be one of these two values:</span></span>
    
<span data-ttu-id="576ec-122">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="576ec-122">MAPIOFFLINE_STATE_ONLINE</span></span>
  
> 
    
<span data-ttu-id="576ec-123">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="576ec-123">MAPIOFFLINE_STATE_OFFLINE</span></span>
  
> 
    
 <span data-ttu-id="576ec-124">_Preservadas_</span><span class="sxs-lookup"><span data-stu-id="576ec-124">_pReserved_</span></span>
  
> <span data-ttu-id="576ec-125">Este parâmetro é reservado para uso interno do Outlook e não é suportado.</span><span class="sxs-lookup"><span data-stu-id="576ec-125">This parameter is reserved for Outlook internal use and is not supported.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="576ec-126">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="576ec-126">Return value</span></span>

<span data-ttu-id="576ec-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="576ec-127">S_OK</span></span>
  
> <span data-ttu-id="576ec-128">O estado do objeto offline foi alterado com êxito.</span><span class="sxs-lookup"><span data-stu-id="576ec-128">The state of the offline object has been changed successfully.</span></span>
    
<span data-ttu-id="576ec-129">E_PENDING</span><span class="sxs-lookup"><span data-stu-id="576ec-129">E_PENDING</span></span>
  
> <span data-ttu-id="576ec-130">Isso indica que o estado do objeto offline está mudando de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="576ec-130">This indicates that the state of the offline object is changing asynchronously.</span></span> <span data-ttu-id="576ec-131">Esse problema ocorre quando _ulFlags_ estiver definido como MAPIOFFLINE_FLAG_BLOCK em uma chamada de **SetCurrentState** anterior e qualquer chamada **SetCurrentState** subsequente irá retornar esse valor até que a alteração de estado assíncrona seja concluída.</span><span class="sxs-lookup"><span data-stu-id="576ec-131">This occurs when  _ulFlags_ is set to MAPIOFFLINE_FLAG_BLOCK in an earlier **SetCurrentState** call, and any subsequent **SetCurrentState** call will return this value until the asynchronous state change is complete.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="576ec-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="576ec-132">See also</span></span>



[<span data-ttu-id="576ec-133">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="576ec-133">IMAPIOffline::GetCapabilities</span></span>](imapioffline-getcapabilities.md)
  
[<span data-ttu-id="576ec-134">IMAPIOffline::GetCurrentState</span><span class="sxs-lookup"><span data-stu-id="576ec-134">IMAPIOffline::GetCurrentState</span></span>](imapioffline-getcurrentstate.md)


[<span data-ttu-id="576ec-135">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="576ec-135">MAPI Constants</span></span>](mapi-constants.md)

