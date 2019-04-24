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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360708"
---
# <a name="screlocnotifications"></a><span data-ttu-id="7ed76-103">ScRelocNotifications</span><span class="sxs-lookup"><span data-stu-id="7ed76-103">ScRelocNotifications</span></span>

  
  
<span data-ttu-id="7ed76-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7ed76-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7ed76-105">Ajusta um ponteiro dentro de uma matriz de notificação de eventos especificada.</span><span class="sxs-lookup"><span data-stu-id="7ed76-105">Adjusts a pointer within a specified event notification array.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7ed76-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="7ed76-106">Header file:</span></span>  <br/> |<span data-ttu-id="7ed76-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="7ed76-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="7ed76-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="7ed76-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7ed76-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7ed76-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7ed76-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="7ed76-110">Called by:</span></span>  <br/> |<span data-ttu-id="7ed76-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="7ed76-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScRelocNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  LPVOID pvBaseOld,
  LPVOID pvBaseNew,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="7ed76-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7ed76-112">Parameters</span></span>

 <span data-ttu-id="7ed76-113">_CNTF_</span><span class="sxs-lookup"><span data-stu-id="7ed76-113">_cntf_</span></span>
  
> <span data-ttu-id="7ed76-114">no Contagem de estruturas de [notificação](notification.md) na matriz indicada pelo parâmetro _rgntf_ .</span><span class="sxs-lookup"><span data-stu-id="7ed76-114">[in] Count of [NOTIFICATION](notification.md) structures in the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="7ed76-115">_rgntf_</span><span class="sxs-lookup"><span data-stu-id="7ed76-115">_rgntf_</span></span>
  
> <span data-ttu-id="7ed76-116">no Ponteiro para a matriz de estruturas de **notificação** definindo notificações de eventos em que um ponteiro deve ser ajustado.</span><span class="sxs-lookup"><span data-stu-id="7ed76-116">[in] Pointer to the array of **NOTIFICATION** structures defining event notifications within which a pointer is to be adjusted.</span></span> 
    
 <span data-ttu-id="7ed76-117">_pvBaseOld_</span><span class="sxs-lookup"><span data-stu-id="7ed76-117">_pvBaseOld_</span></span>
  
> <span data-ttu-id="7ed76-118">no Ponteiro para o endereço base original da matriz indicada pelo parâmetro _rgntf_ .</span><span class="sxs-lookup"><span data-stu-id="7ed76-118">[in] Pointer to the original base address of the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="7ed76-119">_pvBaseNew_</span><span class="sxs-lookup"><span data-stu-id="7ed76-119">_pvBaseNew_</span></span>
  
> <span data-ttu-id="7ed76-120">no O local para o qual o **ScRelocNotifications** grava o novo endereço base da matriz indicada pelo parâmetro _rgntf_ .</span><span class="sxs-lookup"><span data-stu-id="7ed76-120">[in] The location to which **ScRelocNotifications** writes the new base address of the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="7ed76-121">_PCB_</span><span class="sxs-lookup"><span data-stu-id="7ed76-121">_pcb_</span></span>
  
> <span data-ttu-id="7ed76-122">bota Ponteiro para o tamanho, em bytes, da matriz indicada pelo parâmetro _pvBaseNew_ .</span><span class="sxs-lookup"><span data-stu-id="7ed76-122">[out] Pointer to the size, in bytes, of the array indicated by the  _pvBaseNew_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7ed76-123">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="7ed76-123">Return value</span></span>

<span data-ttu-id="7ed76-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="7ed76-124">S_OK</span></span>
  
> <span data-ttu-id="7ed76-125">Um ponteiro foi ajustado com êxito.</span><span class="sxs-lookup"><span data-stu-id="7ed76-125">A pointer was adjusted successfully.</span></span>
    
<span data-ttu-id="7ed76-126">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7ed76-126">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="7ed76-127">Uma notificação inválida foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="7ed76-127">An invalid notification was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7ed76-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="7ed76-128">Remarks</span></span>

<span data-ttu-id="7ed76-129">O parâmetro _PCB_ para a função **ScRelocNotifications** é opcional.</span><span class="sxs-lookup"><span data-stu-id="7ed76-129">The  _pcb_ parameter to the **ScRelocNotifications** function is optional.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7ed76-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="7ed76-130">See also</span></span>



[<span data-ttu-id="7ed76-131">ScRelocProps</span><span class="sxs-lookup"><span data-stu-id="7ed76-131">ScRelocProps</span></span>](screlocprops.md)

