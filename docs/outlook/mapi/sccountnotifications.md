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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437991"
---
# <a name="sccountnotifications"></a><span data-ttu-id="3dfc9-103">ScCountNotifications</span><span class="sxs-lookup"><span data-stu-id="3dfc9-103">ScCountNotifications</span></span>

  
  
<span data-ttu-id="3dfc9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3dfc9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3dfc9-105">Determina o tamanho, em bytes, de uma matriz de notificações de eventos e valida a memória associada à matriz.</span><span class="sxs-lookup"><span data-stu-id="3dfc9-105">Determines the size, in bytes, of an array of event notifications, and validates the memory associated with the array.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3dfc9-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="3dfc9-106">Header file:</span></span>  <br/> |<span data-ttu-id="3dfc9-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="3dfc9-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="3dfc9-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="3dfc9-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="3dfc9-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="3dfc9-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="3dfc9-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="3dfc9-110">Called by:</span></span>  <br/> |<span data-ttu-id="3dfc9-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="3dfc9-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCountNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="3dfc9-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3dfc9-112">Parameters</span></span>

 <span data-ttu-id="3dfc9-113">_cntf_</span><span class="sxs-lookup"><span data-stu-id="3dfc9-113">_cntf_</span></span>
  
> <span data-ttu-id="3dfc9-114">[in] Contagem de [estruturas](notification.md) NOTIFICATION na matriz indicada pelo _parâmetro rgntf._</span><span class="sxs-lookup"><span data-stu-id="3dfc9-114">[in] Count of [NOTIFICATION](notification.md) structures in the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="3dfc9-115">_rgntf_</span><span class="sxs-lookup"><span data-stu-id="3dfc9-115">_rgntf_</span></span>
  
> <span data-ttu-id="3dfc9-116">[in] Ponteiro para a matriz de **estruturas NOTIFICATION** cujo tamanho deve ser determinado.</span><span class="sxs-lookup"><span data-stu-id="3dfc9-116">[in] Pointer to the array of **NOTIFICATION** structures whose size is to be determined.</span></span> 
    
 <span data-ttu-id="3dfc9-117">_pcb_</span><span class="sxs-lookup"><span data-stu-id="3dfc9-117">_pcb_</span></span>
  
> <span data-ttu-id="3dfc9-118">[out] Ponteiro opcional para o tamanho, em bytes, da matriz apontada pelo _parâmetro rgntf._</span><span class="sxs-lookup"><span data-stu-id="3dfc9-118">[out] Optional pointer to the size, in bytes, of the array pointed to by the  _rgntf_ parameter.</span></span> <span data-ttu-id="3dfc9-119">Se for NULL, **ScCountNotifications** validará a matriz de notificações.</span><span class="sxs-lookup"><span data-stu-id="3dfc9-119">If NULL, **ScCountNotifications** validates the array of notifications.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3dfc9-120">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="3dfc9-120">Return value</span></span>

<span data-ttu-id="3dfc9-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="3dfc9-121">S_OK</span></span>
  
> <span data-ttu-id="3dfc9-122">A contagem foi determinada com êxito.</span><span class="sxs-lookup"><span data-stu-id="3dfc9-122">Count was determined successfully.</span></span>
    
<span data-ttu-id="3dfc9-123">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3dfc9-123">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="3dfc9-124">Uma notificação inválida foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="3dfc9-124">An invalid notification was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3dfc9-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="3dfc9-125">Remarks</span></span>

<span data-ttu-id="3dfc9-126">Se NULL for passado no parâmetro  _pcb,_ a função **ScCountNotifications** só validará a matriz de notificações, mas nenhuma contagem será feita; se um valor não nulo for passado em  _pcb_, **ScCountNotifications** determinará o tamanho da matriz e armazenará a causa  _pcb_.</span><span class="sxs-lookup"><span data-stu-id="3dfc9-126">If NULL is passed in the  _pcb_ parameter, the **ScCountNotifications** function only validates the array of notifications but no counting is done; if a non-null value is passed in  _pcb_, **ScCountNotifications** determines the size of the array and stores the cause  _pcb_.</span></span> <span data-ttu-id="3dfc9-127">O  _parâmetro pcb_ deve ser grande o suficiente para conter toda a matriz.</span><span class="sxs-lookup"><span data-stu-id="3dfc9-127">The  _pcb_ parameter must be large enough to contain the entire array.</span></span> 
  

