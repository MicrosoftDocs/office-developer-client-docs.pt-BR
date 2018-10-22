---
title: RebaseTaskProgress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8b8368d2-b04b-42a5-fdc3-955fc873c2f5
description: Relata o andamento da enumeração e alteração programática de compromissos.
ms.openlocfilehash: e5df0cd6df10ab86b1a125b9807637438976726f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384350"
---
# <a name="rebasetaskprogress"></a><span data-ttu-id="6b988-103">RebaseTaskProgress</span><span class="sxs-lookup"><span data-stu-id="6b988-103">RebaseTaskProgress</span></span>

<span data-ttu-id="6b988-104">Relata o andamento da enumeração e alteração programática de compromissos.</span><span class="sxs-lookup"><span data-stu-id="6b988-104">Reports progress for enumeration and rebasing of appointments.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="6b988-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="6b988-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6b988-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="6b988-106">Header file:</span></span>  <br/> |<span data-ttu-id="6b988-107">tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="6b988-107">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="6b988-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="6b988-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6b988-109">Aplicativos clientes MAPI</span><span class="sxs-lookup"><span data-stu-id="6b988-109">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="6b988-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="6b988-110">Called by:</span></span>  <br/> |<span data-ttu-id="6b988-111">Objeto rebasing do Outlook</span><span class="sxs-lookup"><span data-stu-id="6b988-111">Outlook rebasing object</span></span>  <br/> |
|<span data-ttu-id="6b988-112">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="6b988-112">Pointer type:</span></span>  <br/> |<span data-ttu-id="6b988-113">**PFNREBASETASKPROGRESS**, conforme definido em tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="6b988-113">**PFNREBASETASKPROGRESS** as defined in tzmovelib.h</span></span>  <br/> |
   
```cpp
void STDAPICALLTYPE RebaseTaskProgress(  
    ULONG ulMin, 
    ULONG ulMax, 
    ULONG ulCur, 
    REBASE_APPT_STATE State, 
    const SRow* pRowCur); 

```

## <a name="parameters"></a><span data-ttu-id="6b988-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6b988-114">Parameters</span></span>

<span data-ttu-id="6b988-115">_ulMin_</span><span class="sxs-lookup"><span data-stu-id="6b988-115">_ulMin_</span></span>
  
> <span data-ttu-id="6b988-116">[in] A extremidade inferior do intervalo de compromissos sendo processados.</span><span class="sxs-lookup"><span data-stu-id="6b988-116">[in] The low end of the range of appointments being processed.</span></span> <span data-ttu-id="6b988-117">Geralmente, é zero.</span><span class="sxs-lookup"><span data-stu-id="6b988-117">It is usually zero.</span></span>
    
<span data-ttu-id="6b988-118">_ulMax_</span><span class="sxs-lookup"><span data-stu-id="6b988-118">_ulMax_</span></span>
  
> <span data-ttu-id="6b988-119">[in] A extremidade superior do intervalo de compromissos sendo processados.</span><span class="sxs-lookup"><span data-stu-id="6b988-119">[in] The high end of the range of appointments being processed.</span></span> <span data-ttu-id="6b988-120">Geralmente, é o número de itens na pasta do calendário que está sendo processado.</span><span class="sxs-lookup"><span data-stu-id="6b988-120">It is usually the number of items in the calendar folder being processed.</span></span>
    
<span data-ttu-id="6b988-121">_ulCur_</span><span class="sxs-lookup"><span data-stu-id="6b988-121">_ulCur_</span></span>
  
> <span data-ttu-id="6b988-122">[in] O item atual sendo processado.</span><span class="sxs-lookup"><span data-stu-id="6b988-122">[in] The current item being processed.</span></span>
    
<span data-ttu-id="6b988-123">_State_</span><span class="sxs-lookup"><span data-stu-id="6b988-123">_State_</span></span>
  
> <span data-ttu-id="6b988-124">[in] Um valor que indica o status do item que está sendo processado.</span><span class="sxs-lookup"><span data-stu-id="6b988-124">[in] A value that indicates the status of the item being processed.</span></span> <span data-ttu-id="6b988-125">A enumeração **REBASE_APPT_STATE** é definida em tzmovelib.h.</span><span class="sxs-lookup"><span data-stu-id="6b988-125">The enumeration **REBASE_APPT_STATE** is defined in tzmovelib.h.</span></span>  <span data-ttu-id="6b988-126">_State_ é um dos valores a seguir:</span><span class="sxs-lookup"><span data-stu-id="6b988-126">_State_ is one of the following values:</span></span> 
    
   - <span data-ttu-id="6b988-127">**REBASE_APPT_STATE_SCANNING_EXAMINING** —Digitalizar e examinar um item.</span><span class="sxs-lookup"><span data-stu-id="6b988-127">**REBASE_APPT_STATE_SCANNING_EXAMINING** —Scanning and examining an item.</span></span> 
    
   - <span data-ttu-id="6b988-128">**REBASE_APPT_STATE_SCANNING_FOUND** —Digitalizar e encontrar um item.</span><span class="sxs-lookup"><span data-stu-id="6b988-128">**REBASE_APPT_STATE_SCANNING_FOUND** —Scanning and found an item.</span></span> 
    
   - <span data-ttu-id="6b988-129">**REBASE_APPT_STATE_BEGIN** —Corrigir e iniciar um item.</span><span class="sxs-lookup"><span data-stu-id="6b988-129">**REBASE_APPT_STATE_BEGIN** —Fixing and starting an item.</span></span> 
    
   - <span data-ttu-id="6b988-130">**REBASE_APPT_STATE_REBASING** —Corrigir e ajustar um item.</span><span class="sxs-lookup"><span data-stu-id="6b988-130">**REBASE_APPT_STATE_REBASING** —Fixing and adjusting an item.</span></span> 
    
   - <span data-ttu-id="6b988-131">**REBASE_APPT_STATE_SENDING** —Corrigir e enviar uma atualização de reunião.</span><span class="sxs-lookup"><span data-stu-id="6b988-131">**REBASE_APPT_STATE_SENDING** —Fixing and sending a meeting update.</span></span> 
    
   - <span data-ttu-id="6b988-132">**REBASE_APPT_STATE_DONE** —Corrigir e concluir com um item.</span><span class="sxs-lookup"><span data-stu-id="6b988-132">**REBASE_APPT_STATE_DONE** —Fixing and done with an item.</span></span> 
    
<span data-ttu-id="6b988-133">_pRowCur_</span><span class="sxs-lookup"><span data-stu-id="6b988-133">_pRowCur_</span></span>
  
> <span data-ttu-id="6b988-134">[in] Um ponteiro para uma estrutura **[SRow](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** que descreve o item sendo verificado ou corrigido.</span><span class="sxs-lookup"><span data-stu-id="6b988-134">[in] A pointer to an **[SRow](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** structure that describes the item being scanned or fixed.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="6b988-135">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6b988-135">Return Values</span></span>

<span data-ttu-id="6b988-136">S_OK se a chamada for bem-sucedida; caso contrário, um código de erro.</span><span class="sxs-lookup"><span data-stu-id="6b988-136">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6b988-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="6b988-137">Remarks</span></span>

<span data-ttu-id="6b988-138">Aplicativos cliente MAPI que usam a interface [IOlkApptRebaser](iolkapptrebaser.md) implementam essa função para acompanhar o processamento de itens.</span><span class="sxs-lookup"><span data-stu-id="6b988-138">MAPI client applications that use the [IOlkApptRebaser](iolkapptrebaser.md) interface implement this function to track item processing.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6b988-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="6b988-139">See also</span></span>

- [<span data-ttu-id="6b988-140">Sobre a alteração programática da base de calendários para o horário de verão</span><span class="sxs-lookup"><span data-stu-id="6b988-140">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

