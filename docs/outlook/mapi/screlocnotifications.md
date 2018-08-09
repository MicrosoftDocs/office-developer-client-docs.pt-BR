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
ms.openlocfilehash: bb4ff6a128b9fed29ff0be5325c21e5600389740
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770355"
---
# <a name="screlocnotifications"></a><span data-ttu-id="f5611-103">ScRelocNotifications</span><span class="sxs-lookup"><span data-stu-id="f5611-103">ScRelocNotifications</span></span>

  
  
<span data-ttu-id="f5611-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f5611-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f5611-105">Ajusta um ponteiro dentro de uma matriz de notificação de evento especificado.</span><span class="sxs-lookup"><span data-stu-id="f5611-105">Adjusts a pointer within a specified event notification array.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f5611-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="f5611-106">Header file:</span></span>  <br/> |<span data-ttu-id="f5611-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="f5611-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="f5611-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="f5611-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f5611-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f5611-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f5611-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="f5611-110">Called by:</span></span>  <br/> |<span data-ttu-id="f5611-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="f5611-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScRelocNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  LPVOID pvBaseOld,
  LPVOID pvBaseNew,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="f5611-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f5611-112">Parameters</span></span>

 <span data-ttu-id="f5611-113">_cntf_</span><span class="sxs-lookup"><span data-stu-id="f5611-113">_cntf_</span></span>
  
> <span data-ttu-id="f5611-114">[in] Contagem de estruturas de [notificação](notification.md) na matriz indicado pelo parâmetro _rgntf_ .</span><span class="sxs-lookup"><span data-stu-id="f5611-114">[in] Count of [NOTIFICATION](notification.md) structures in the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="f5611-115">_rgntf_</span><span class="sxs-lookup"><span data-stu-id="f5611-115">_rgntf_</span></span>
  
> <span data-ttu-id="f5611-116">[in] Ponteiro para a matriz de estruturas de **notificação** , definindo as notificações de evento dentro do qual um ponteiro deve ser ajustada.</span><span class="sxs-lookup"><span data-stu-id="f5611-116">[in] Pointer to the array of **NOTIFICATION** structures defining event notifications within which a pointer is to be adjusted.</span></span> 
    
 <span data-ttu-id="f5611-117">_pvBaseOld_</span><span class="sxs-lookup"><span data-stu-id="f5611-117">_pvBaseOld_</span></span>
  
> <span data-ttu-id="f5611-118">[in] Ponteiro para o endereço base original da matriz indicado pelo parâmetro _rgntf_ .</span><span class="sxs-lookup"><span data-stu-id="f5611-118">[in] Pointer to the original base address of the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="f5611-119">_pvBaseNew_</span><span class="sxs-lookup"><span data-stu-id="f5611-119">_pvBaseNew_</span></span>
  
> <span data-ttu-id="f5611-120">[in] A posição na qual **ScRelocNotifications** grava o novo endereço base da matriz indicado pelo parâmetro _rgntf_ .</span><span class="sxs-lookup"><span data-stu-id="f5611-120">[in] The location to which **ScRelocNotifications** writes the new base address of the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="f5611-121">_PCB_</span><span class="sxs-lookup"><span data-stu-id="f5611-121">_pcb_</span></span>
  
> <span data-ttu-id="f5611-122">[out] Ponteiro para o tamanho, em bytes, da matriz indicado pelo parâmetro _pvBaseNew_ .</span><span class="sxs-lookup"><span data-stu-id="f5611-122">[out] Pointer to the size, in bytes, of the array indicated by the  _pvBaseNew_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f5611-123">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="f5611-123">Return value</span></span>

<span data-ttu-id="f5611-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="f5611-124">S_OK</span></span>
  
> <span data-ttu-id="f5611-125">Um ponteiro foi ajustado com êxito.</span><span class="sxs-lookup"><span data-stu-id="f5611-125">A pointer was adjusted successfully.</span></span>
    
<span data-ttu-id="f5611-126">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f5611-126">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="f5611-127">Uma notificação inválida foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="f5611-127">An invalid notification was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f5611-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="f5611-128">Remarks</span></span>

<span data-ttu-id="f5611-129">O parâmetro _pcb_ para a função **ScRelocNotifications** é opcional.</span><span class="sxs-lookup"><span data-stu-id="f5611-129">The  _pcb_ parameter to the **ScRelocNotifications** function is optional.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f5611-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="f5611-130">See also</span></span>



[<span data-ttu-id="f5611-131">ScRelocProps</span><span class="sxs-lookup"><span data-stu-id="f5611-131">ScRelocProps</span></span>](screlocprops.md)

