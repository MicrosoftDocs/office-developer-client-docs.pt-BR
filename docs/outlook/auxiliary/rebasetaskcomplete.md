---
title: RebaseTaskComplete
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 2de5c77c-3fac-cfb6-3719-68df4013cf11
description: Relata a conclusão da alteração programática de compromissos.
ms.openlocfilehash: 9fab0d06bf0b9856b9a968f5c0db1bb15b0fe0bd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388914"
---
# <a name="rebasetaskcomplete"></a><span data-ttu-id="e983b-103">RebaseTaskComplete</span><span class="sxs-lookup"><span data-stu-id="e983b-103">RebaseTaskComplete</span></span>

<span data-ttu-id="e983b-104">Relata a conclusão da alteração programática de compromissos.</span><span class="sxs-lookup"><span data-stu-id="e983b-104">Reports completion for rebasing of appointments.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e983b-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="e983b-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e983b-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="e983b-106">Header file:</span></span>  <br/> |<span data-ttu-id="e983b-107">tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="e983b-107">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="e983b-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="e983b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e983b-109">Aplicativos clientes MAPI</span><span class="sxs-lookup"><span data-stu-id="e983b-109">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="e983b-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="e983b-110">Called by:</span></span>  <br/> |<span data-ttu-id="e983b-111">Objeto rebasing do Outlook</span><span class="sxs-lookup"><span data-stu-id="e983b-111">Outlook rebasing object</span></span>  <br/> |
|<span data-ttu-id="e983b-112">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="e983b-112">Pointer type:</span></span>  <br/> |<span data-ttu-id="e983b-113">**PFNREBASETASKCOMPLETE**, conforme definido em tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="e983b-113">**PFNREBASETASKCOMPLETE** as defined in tzmovelib.h</span></span>  <br/> |
   
```cpp
void STDAPICALLTYPE RebaseTaskComplete(  
    ULONG ulRowIndex, 
    const SRow* pRowCur, 
    HRESULT hrResult, 
    BOOL fModified, 
    BOOL fSentUpdate, 
    const MAPIERROR* pError); 

```

## <a name="parameters"></a><span data-ttu-id="e983b-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e983b-114">Parameters</span></span>

<span data-ttu-id="e983b-115">_ulRowIndex_</span><span class="sxs-lookup"><span data-stu-id="e983b-115">_ulRowIndex_</span></span>
  
> <span data-ttu-id="e983b-116">[in] A linha que foi processada.</span><span class="sxs-lookup"><span data-stu-id="e983b-116">[in] The row that was processed.</span></span> <span data-ttu-id="e983b-117">Este índice refere-se à estrutura **[SRowSet](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx)** passada para [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).</span><span class="sxs-lookup"><span data-stu-id="e983b-117">This index refers to the **[SRowSet](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx)** structure passed to [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).</span></span>
    
<span data-ttu-id="e983b-118">_pRowCur_</span><span class="sxs-lookup"><span data-stu-id="e983b-118">_pRowCur_</span></span>
  
> <span data-ttu-id="e983b-119">in] Um ponteiro para uma estrutura **[SRow](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** que descreve o item processado.</span><span class="sxs-lookup"><span data-stu-id="e983b-119">in] A pointer to an **[SRow](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** structure describing the item that was processed.</span></span> 
    
<span data-ttu-id="e983b-120">_hrResult_</span><span class="sxs-lookup"><span data-stu-id="e983b-120">_hrResult_</span></span>
  
> <span data-ttu-id="e983b-121">[in] Um **HRESULT** que indica o resultado da operação de alteração programática.</span><span class="sxs-lookup"><span data-stu-id="e983b-121">[in] An **HRESULT** indicating the result of the rebasing operation.</span></span> 
    
<span data-ttu-id="e983b-122">_fModified_</span><span class="sxs-lookup"><span data-stu-id="e983b-122">_fModified_</span></span>
  
> <span data-ttu-id="e983b-123">[in] Especifica se o item foi modificado.</span><span class="sxs-lookup"><span data-stu-id="e983b-123">[in] Specifies whether the item was modified.</span></span>
    
<span data-ttu-id="e983b-124">_fSentUpdate_</span><span class="sxs-lookup"><span data-stu-id="e983b-124">_fSentUpdate_</span></span>
  
> <span data-ttu-id="e983b-125">[em] Especifica se uma mensagem de atualização da reunião foi enviada.</span><span class="sxs-lookup"><span data-stu-id="e983b-125">[in] Specifies whether a meeting update message was sent.</span></span> 
    
<span data-ttu-id="e983b-126">_pError_</span><span class="sxs-lookup"><span data-stu-id="e983b-126">_pError_</span></span>
  
> <span data-ttu-id="e983b-127">[in] Um ponteiro para uma estrutura **MAPIERROR** com informações sobre erros estendidas.</span><span class="sxs-lookup"><span data-stu-id="e983b-127">[in] A pointer to a **MAPIERROR** structure with extended error information.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="e983b-128">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e983b-128">Return Values</span></span>

<span data-ttu-id="e983b-129">S_OK se a chamada foi bem-sucedida. Caso contrário, um código de erro.</span><span class="sxs-lookup"><span data-stu-id="e983b-129">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e983b-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="e983b-130">Remarks</span></span>

<span data-ttu-id="e983b-131">Aplicativos cliente MAPI que usam a interface [IOlkApptRebaser](iolkapptrebaser.md) implementam essa função para controlar a conclusão de atualizações do item.</span><span class="sxs-lookup"><span data-stu-id="e983b-131">MAPI client applications that use the [IOlkApptRebaser](iolkapptrebaser.md) interface implement this function to track completion of item updates.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e983b-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="e983b-132">See also</span></span>

- [<span data-ttu-id="e983b-133">Sobre a alteração programática da base de calendários para o horário de verão</span><span class="sxs-lookup"><span data-stu-id="e983b-133">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

