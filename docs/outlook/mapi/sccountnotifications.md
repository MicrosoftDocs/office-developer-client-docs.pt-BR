---
title: ScCountNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCountNotifications
api_type:
- COM
ms.assetid: 13e80bdc-cb59-47a5-8de0-404e22f87f82
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f5298620239d1e42e4ba613c22a98f0cf6f7d457
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351367"
---
# <a name="sccountnotifications"></a><span data-ttu-id="6ef8f-103">ScCountNotifications</span><span class="sxs-lookup"><span data-stu-id="6ef8f-103">ScCountNotifications</span></span>

  
  
<span data-ttu-id="6ef8f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6ef8f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6ef8f-105">Determina o tamanho, em bytes, de uma matriz de notificações de eventos e valida a memória associada à matriz.</span><span class="sxs-lookup"><span data-stu-id="6ef8f-105">Determines the size, in bytes, of an array of event notifications, and validates the memory associated with the array.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6ef8f-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="6ef8f-106">Header file:</span></span>  <br/> |<span data-ttu-id="6ef8f-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="6ef8f-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="6ef8f-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="6ef8f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6ef8f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6ef8f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6ef8f-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="6ef8f-110">Called by:</span></span>  <br/> |<span data-ttu-id="6ef8f-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="6ef8f-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCountNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="6ef8f-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6ef8f-112">Parameters</span></span>

 <span data-ttu-id="6ef8f-113">_CNTF_</span><span class="sxs-lookup"><span data-stu-id="6ef8f-113">_cntf_</span></span>
  
> <span data-ttu-id="6ef8f-114">no Contagem de estruturas de [notificação](notification.md) na matriz indicada pelo parâmetro _rgntf_ .</span><span class="sxs-lookup"><span data-stu-id="6ef8f-114">[in] Count of [NOTIFICATION](notification.md) structures in the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="6ef8f-115">_rgntf_</span><span class="sxs-lookup"><span data-stu-id="6ef8f-115">_rgntf_</span></span>
  
> <span data-ttu-id="6ef8f-116">no Ponteiro para a matriz de estruturas de **notificação** cujo tamanho deve ser determinado.</span><span class="sxs-lookup"><span data-stu-id="6ef8f-116">[in] Pointer to the array of **NOTIFICATION** structures whose size is to be determined.</span></span> 
    
 <span data-ttu-id="6ef8f-117">_PCB_</span><span class="sxs-lookup"><span data-stu-id="6ef8f-117">_pcb_</span></span>
  
> <span data-ttu-id="6ef8f-118">bota Ponteiro opcional para o tamanho, em bytes, da matriz apontada pelo parâmetro _rgntf_ .</span><span class="sxs-lookup"><span data-stu-id="6ef8f-118">[out] Optional pointer to the size, in bytes, of the array pointed to by the  _rgntf_ parameter.</span></span> <span data-ttu-id="6ef8f-119">Se NULL, **ScCountNotifications** valida a matriz de notificações.</span><span class="sxs-lookup"><span data-stu-id="6ef8f-119">If NULL, **ScCountNotifications** validates the array of notifications.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6ef8f-120">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6ef8f-120">Return value</span></span>

<span data-ttu-id="6ef8f-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="6ef8f-121">S_OK</span></span>
  
> <span data-ttu-id="6ef8f-122">A contagem foi determinada com êxito.</span><span class="sxs-lookup"><span data-stu-id="6ef8f-122">Count was determined successfully.</span></span>
    
<span data-ttu-id="6ef8f-123">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6ef8f-123">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="6ef8f-124">Uma notificação inválida foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="6ef8f-124">An invalid notification was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6ef8f-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="6ef8f-125">Remarks</span></span>

<span data-ttu-id="6ef8f-126">Se NULL for passado no parâmetro _PCB_ , a função **ScCountNotifications** validará apenas a matriz de notificações, mas nenhuma contagem será feita; se um valor não nulo for passado em _PCB_, **ScCountNotifications** determinará o tamanho da matriz e armazenará a _PCB_de causa.</span><span class="sxs-lookup"><span data-stu-id="6ef8f-126">If NULL is passed in the  _pcb_ parameter, the **ScCountNotifications** function only validates the array of notifications but no counting is done; if a non-null value is passed in  _pcb_, **ScCountNotifications** determines the size of the array and stores the cause  _pcb_.</span></span> <span data-ttu-id="6ef8f-127">O parâmetro _PCB_ deve ser grande o suficiente para conter toda a matriz.</span><span class="sxs-lookup"><span data-stu-id="6ef8f-127">The  _pcb_ parameter must be large enough to contain the entire array.</span></span> 
  

