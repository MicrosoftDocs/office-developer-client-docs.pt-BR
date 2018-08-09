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
ms.openlocfilehash: c27472a309c26882051744a23fbe05e41c36aa3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770329"
---
# <a name="sccountnotifications"></a><span data-ttu-id="0ec48-103">ScCountNotifications</span><span class="sxs-lookup"><span data-stu-id="0ec48-103">ScCountNotifications</span></span>

  
  
<span data-ttu-id="0ec48-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0ec48-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0ec48-105">Determina o tamanho, em bytes, de uma matriz de notificações de evento e valida a memória associada a matriz.</span><span class="sxs-lookup"><span data-stu-id="0ec48-105">Determines the size, in bytes, of an array of event notifications, and validates the memory associated with the array.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0ec48-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="0ec48-106">Header file:</span></span>  <br/> |<span data-ttu-id="0ec48-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="0ec48-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="0ec48-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="0ec48-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0ec48-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0ec48-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0ec48-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="0ec48-110">Called by:</span></span>  <br/> |<span data-ttu-id="0ec48-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="0ec48-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCountNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="0ec48-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0ec48-112">Parameters</span></span>

 <span data-ttu-id="0ec48-113">_cntf_</span><span class="sxs-lookup"><span data-stu-id="0ec48-113">_cntf_</span></span>
  
> <span data-ttu-id="0ec48-114">[in] Contagem de estruturas de [notificação](notification.md) na matriz indicado pelo parâmetro _rgntf_ .</span><span class="sxs-lookup"><span data-stu-id="0ec48-114">[in] Count of [NOTIFICATION](notification.md) structures in the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="0ec48-115">_rgntf_</span><span class="sxs-lookup"><span data-stu-id="0ec48-115">_rgntf_</span></span>
  
> <span data-ttu-id="0ec48-116">[in] Ponteiro para a matriz de estruturas de **notificação** cujo tamanho é seja determinado.</span><span class="sxs-lookup"><span data-stu-id="0ec48-116">[in] Pointer to the array of **NOTIFICATION** structures whose size is to be determined.</span></span> 
    
 <span data-ttu-id="0ec48-117">_PCB_</span><span class="sxs-lookup"><span data-stu-id="0ec48-117">_pcb_</span></span>
  
> <span data-ttu-id="0ec48-118">[out] Ponteiro opcional para o tamanho, em bytes, da matriz apontado pelo parâmetro _rgntf_ .</span><span class="sxs-lookup"><span data-stu-id="0ec48-118">[out] Optional pointer to the size, in bytes, of the array pointed to by the  _rgntf_ parameter.</span></span> <span data-ttu-id="0ec48-119">Se for NULL, **ScCountNotifications** valida a matriz de notificações.</span><span class="sxs-lookup"><span data-stu-id="0ec48-119">If NULL, **ScCountNotifications** validates the array of notifications.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0ec48-120">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="0ec48-120">Return value</span></span>

<span data-ttu-id="0ec48-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="0ec48-121">S_OK</span></span>
  
> <span data-ttu-id="0ec48-122">Contagem de determinada com êxito.</span><span class="sxs-lookup"><span data-stu-id="0ec48-122">Count was determined successfully.</span></span>
    
<span data-ttu-id="0ec48-123">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0ec48-123">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="0ec48-124">Uma notificação inválida foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="0ec48-124">An invalid notification was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0ec48-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="0ec48-125">Remarks</span></span>

<span data-ttu-id="0ec48-126">Se NULL é passada no parâmetro _pcb_ , a função **ScCountNotifications** somente valida a matriz de notificações, mas nenhum contando é feito; Se um valor não-nulo é passado _pcb_, **ScCountNotifications** determina o tamanho da matriz e armazena a causa _pcb_.</span><span class="sxs-lookup"><span data-stu-id="0ec48-126">If NULL is passed in the  _pcb_ parameter, the **ScCountNotifications** function only validates the array of notifications but no counting is done; if a non-null value is passed in  _pcb_, **ScCountNotifications** determines the size of the array and stores the cause  _pcb_.</span></span> <span data-ttu-id="0ec48-127">O parâmetro _pcb_ deve ser grande o suficiente para conter toda a matriz.</span><span class="sxs-lookup"><span data-stu-id="0ec48-127">The  _pcb_ parameter must be large enough to contain the entire array.</span></span> 
  

