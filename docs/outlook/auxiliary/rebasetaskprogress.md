---
title: RebaseTaskProgress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8b8368d2-b04b-42a5-fdc3-955fc873c2f5
description: Relatórios de progresso para enumeração e a alteração da Base de compromissos.
ms.openlocfilehash: 4219ab1d59b596bebbe3ced03651716b04b51f81
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766077"
---
# <a name="rebasetaskprogress"></a><span data-ttu-id="ef1ad-103">RebaseTaskProgress</span><span class="sxs-lookup"><span data-stu-id="ef1ad-103">RebaseTaskProgress</span></span>

<span data-ttu-id="ef1ad-104">Relatórios de progresso para enumeração e a alteração da Base de compromissos.</span><span class="sxs-lookup"><span data-stu-id="ef1ad-104">Reports progress for enumeration and rebasing of appointments.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ef1ad-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="ef1ad-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ef1ad-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="ef1ad-106">Header file:</span></span>  <br/> |<span data-ttu-id="ef1ad-107">tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="ef1ad-107">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="ef1ad-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="ef1ad-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ef1ad-109">Aplicativos de cliente MAPI</span><span class="sxs-lookup"><span data-stu-id="ef1ad-109">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="ef1ad-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="ef1ad-110">Called by:</span></span>  <br/> |<span data-ttu-id="ef1ad-111">REBASE de objeto do Outlook</span><span class="sxs-lookup"><span data-stu-id="ef1ad-111">Outlook rebasing object</span></span>  <br/> |
|<span data-ttu-id="ef1ad-112">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="ef1ad-112">Pointer type:</span></span>  <br/> |<span data-ttu-id="ef1ad-113">**PFNREBASETASKPROGRESS** conforme definido em tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="ef1ad-113">**PFNREBASETASKPROGRESS** as defined in tzmovelib.h</span></span>  <br/> |
   
```cpp
void STDAPICALLTYPE RebaseTaskProgress(  
    ULONG ulMin, 
    ULONG ulMax, 
    ULONG ulCur, 
    REBASE_APPT_STATE State, 
    const SRow* pRowCur); 

```

## <a name="parameters"></a><span data-ttu-id="ef1ad-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ef1ad-114">Parameters</span></span>

<span data-ttu-id="ef1ad-115">_ulMin_</span><span class="sxs-lookup"><span data-stu-id="ef1ad-115">_ulMin_</span></span>
  
> <span data-ttu-id="ef1ad-116">[in] O término de baixo do intervalo de compromissos que estão sendo processadas.</span><span class="sxs-lookup"><span data-stu-id="ef1ad-116">[in] The low end of the range of appointments being processed.</span></span> <span data-ttu-id="ef1ad-117">Normalmente é zero.</span><span class="sxs-lookup"><span data-stu-id="ef1ad-117">It is usually zero.</span></span>
    
<span data-ttu-id="ef1ad-118">_ulMax_</span><span class="sxs-lookup"><span data-stu-id="ef1ad-118">_ulMax_</span></span>
  
> <span data-ttu-id="ef1ad-119">[in] High-end do intervalo de compromissos que estão sendo processadas.</span><span class="sxs-lookup"><span data-stu-id="ef1ad-119">[in] The high end of the range of appointments being processed.</span></span> <span data-ttu-id="ef1ad-120">Geralmente é o número de itens na pasta de calendário que estão sendo processadas.</span><span class="sxs-lookup"><span data-stu-id="ef1ad-120">It is usually the number of items in the calendar folder being processed.</span></span>
    
<span data-ttu-id="ef1ad-121">_ulCur_</span><span class="sxs-lookup"><span data-stu-id="ef1ad-121">_ulCur_</span></span>
  
> <span data-ttu-id="ef1ad-122">[in] O item atual que está sendo processado.</span><span class="sxs-lookup"><span data-stu-id="ef1ad-122">[in] The current item being processed.</span></span>
    
<span data-ttu-id="ef1ad-123">_Estado_</span><span class="sxs-lookup"><span data-stu-id="ef1ad-123">_State_</span></span>
  
> <span data-ttu-id="ef1ad-124">[in] Um valor que indica o status do item que estão sendo processado.</span><span class="sxs-lookup"><span data-stu-id="ef1ad-124">[in] A value that indicates the status of the item being processed.</span></span> <span data-ttu-id="ef1ad-125">A enumeração **REBASE_APPT_STATE** é definida em tzmovelib.h.</span><span class="sxs-lookup"><span data-stu-id="ef1ad-125">The enumeration **REBASE_APPT_STATE** is defined in tzmovelib.h.</span></span>  <span data-ttu-id="ef1ad-126">_Estado_ é um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="ef1ad-126">_State_ is one of the following values:</span></span> 
    
   - <span data-ttu-id="ef1ad-127">**REBASE_APPT_STATE_SCANNING_EXAMINING** — digitalização e examinando a um item.</span><span class="sxs-lookup"><span data-stu-id="ef1ad-127">**REBASE_APPT_STATE_SCANNING_EXAMINING** —Scanning and examining an item.</span></span> 
    
   - <span data-ttu-id="ef1ad-128">**REBASE_APPT_STATE_SCANNING_FOUND** — examinando e encontrado um item.</span><span class="sxs-lookup"><span data-stu-id="ef1ad-128">**REBASE_APPT_STATE_SCANNING_FOUND** —Scanning and found an item.</span></span> 
    
   - <span data-ttu-id="ef1ad-129">**REBASE_APPT_STATE_BEGIN** — corrigindo e iniciando a um item.</span><span class="sxs-lookup"><span data-stu-id="ef1ad-129">**REBASE_APPT_STATE_BEGIN** —Fixing and starting an item.</span></span> 
    
   - <span data-ttu-id="ef1ad-130">**REBASE_APPT_STATE_REBASING** — corrigindo e ajustando um item.</span><span class="sxs-lookup"><span data-stu-id="ef1ad-130">**REBASE_APPT_STATE_REBASING** —Fixing and adjusting an item.</span></span> 
    
   - <span data-ttu-id="ef1ad-131">**REBASE_APPT_STATE_SENDING** — corrigindo e envio de uma atualização de reunião.</span><span class="sxs-lookup"><span data-stu-id="ef1ad-131">**REBASE_APPT_STATE_SENDING** —Fixing and sending a meeting update.</span></span> 
    
   - <span data-ttu-id="ef1ad-132">**REBASE_APPT_STATE_DONE** — corrigindo e concluído com um item.</span><span class="sxs-lookup"><span data-stu-id="ef1ad-132">**REBASE_APPT_STATE_DONE** —Fixing and done with an item.</span></span> 
    
<span data-ttu-id="ef1ad-133">_pRowCur_</span><span class="sxs-lookup"><span data-stu-id="ef1ad-133">_pRowCur_</span></span>
  
> <span data-ttu-id="ef1ad-134">[in] Um ponteiro para uma estrutura **[SRow](http://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** que descreve o item que estão sendo verificados ou fixa.</span><span class="sxs-lookup"><span data-stu-id="ef1ad-134">[in] A pointer to an **[SRow](http://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** structure that describes the item being scanned or fixed.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="ef1ad-135">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="ef1ad-135">Return values</span></span>

<span data-ttu-id="ef1ad-136">S_OK se a chamada foi bem-sucedida; Caso contrário, um código de erro.</span><span class="sxs-lookup"><span data-stu-id="ef1ad-136">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ef1ad-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="ef1ad-137">Remarks</span></span>

<span data-ttu-id="ef1ad-138">Aplicativos de cliente MAPI que usam a interface [IOlkApptRebaser](iolkapptrebaser.md) implementam esta função para controlar o processamento do item.</span><span class="sxs-lookup"><span data-stu-id="ef1ad-138">MAPI client applications that use the [IOlkApptRebaser](iolkapptrebaser.md) interface implement this function to track item processing.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ef1ad-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="ef1ad-139">See also</span></span>

- [<span data-ttu-id="ef1ad-140">Sobre alteração de calendários por meio de programação para horário de verão</span><span class="sxs-lookup"><span data-stu-id="ef1ad-140">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

