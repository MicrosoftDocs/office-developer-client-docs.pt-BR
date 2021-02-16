---
title: ScRelocNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScRelocNotifications
api_type:
- COM
ms.assetid: 22de5d38-7be6-48b3-90a7-bc553dcdb042
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 81da4b77f0d2162a1119b7945b1e0ceb87ba9fb8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415198"
---
# <a name="screlocnotifications"></a><span data-ttu-id="503e7-103">ScRelocNotifications</span><span class="sxs-lookup"><span data-stu-id="503e7-103">ScRelocNotifications</span></span>

  
  
<span data-ttu-id="503e7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="503e7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="503e7-105">Ajusta um ponteiro dentro de uma matriz de notificação de evento especificada.</span><span class="sxs-lookup"><span data-stu-id="503e7-105">Adjusts a pointer within a specified event notification array.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="503e7-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="503e7-106">Header file:</span></span>  <br/> |<span data-ttu-id="503e7-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="503e7-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="503e7-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="503e7-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="503e7-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="503e7-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="503e7-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="503e7-110">Called by:</span></span>  <br/> |<span data-ttu-id="503e7-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="503e7-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScRelocNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  LPVOID pvBaseOld,
  LPVOID pvBaseNew,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="503e7-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="503e7-112">Parameters</span></span>

 <span data-ttu-id="503e7-113">_cntf_</span><span class="sxs-lookup"><span data-stu-id="503e7-113">_cntf_</span></span>
  
> <span data-ttu-id="503e7-114">[in] Contagem de [estruturas](notification.md) NOTIFICATION na matriz indicada pelo _parâmetro rgntf._</span><span class="sxs-lookup"><span data-stu-id="503e7-114">[in] Count of [NOTIFICATION](notification.md) structures in the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="503e7-115">_rgntf_</span><span class="sxs-lookup"><span data-stu-id="503e7-115">_rgntf_</span></span>
  
> <span data-ttu-id="503e7-116">[in] Ponteiro para a matriz de estruturas **notification** definindo notificações de evento dentro da qual um ponteiro deve ser ajustado.</span><span class="sxs-lookup"><span data-stu-id="503e7-116">[in] Pointer to the array of **NOTIFICATION** structures defining event notifications within which a pointer is to be adjusted.</span></span> 
    
 <span data-ttu-id="503e7-117">_pvBaseOld_</span><span class="sxs-lookup"><span data-stu-id="503e7-117">_pvBaseOld_</span></span>
  
> <span data-ttu-id="503e7-118">[in] Ponteiro para o endereço base original da matriz indicado pelo _parâmetro rgntf._</span><span class="sxs-lookup"><span data-stu-id="503e7-118">[in] Pointer to the original base address of the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="503e7-119">_pvBaseNew_</span><span class="sxs-lookup"><span data-stu-id="503e7-119">_pvBaseNew_</span></span>
  
> <span data-ttu-id="503e7-120">[in] O local no qual **ScRelocNotifications** grava o novo endereço base da matriz indicado pelo _parâmetro rgntf._</span><span class="sxs-lookup"><span data-stu-id="503e7-120">[in] The location to which **ScRelocNotifications** writes the new base address of the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="503e7-121">_pcb_</span><span class="sxs-lookup"><span data-stu-id="503e7-121">_pcb_</span></span>
  
> <span data-ttu-id="503e7-122">[out] Ponteiro para o tamanho, em bytes, da matriz indicada pelo _parâmetro pvBaseNew._</span><span class="sxs-lookup"><span data-stu-id="503e7-122">[out] Pointer to the size, in bytes, of the array indicated by the  _pvBaseNew_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="503e7-123">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="503e7-123">Return value</span></span>

<span data-ttu-id="503e7-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="503e7-124">S_OK</span></span>
  
> <span data-ttu-id="503e7-125">Um ponteiro foi ajustado com êxito.</span><span class="sxs-lookup"><span data-stu-id="503e7-125">A pointer was adjusted successfully.</span></span>
    
<span data-ttu-id="503e7-126">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="503e7-126">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="503e7-127">Uma notificação inválida foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="503e7-127">An invalid notification was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="503e7-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="503e7-128">Remarks</span></span>

<span data-ttu-id="503e7-129">O  _parâmetro pcb_ para a **função ScRelocNotifications** é opcional.</span><span class="sxs-lookup"><span data-stu-id="503e7-129">The  _pcb_ parameter to the **ScRelocNotifications** function is optional.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="503e7-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="503e7-130">See also</span></span>



[<span data-ttu-id="503e7-131">ScRelocProps</span><span class="sxs-lookup"><span data-stu-id="503e7-131">ScRelocProps</span></span>](screlocprops.md)

