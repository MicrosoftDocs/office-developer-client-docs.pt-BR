---
title: RebaseTaskComplete
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 2de5c77c-3fac-cfb6-3719-68df4013cf11
description: Conclusão de relatórios para a alteração da Base de compromissos.
ms.openlocfilehash: 735d875b4151c86103a1ac0378bd33b84de64997
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766081"
---
# <a name="rebasetaskcomplete"></a><span data-ttu-id="b1ec7-103">RebaseTaskComplete</span><span class="sxs-lookup"><span data-stu-id="b1ec7-103">RebaseTaskComplete</span></span>

<span data-ttu-id="b1ec7-104">Conclusão de relatórios para a alteração da Base de compromissos.</span><span class="sxs-lookup"><span data-stu-id="b1ec7-104">Reports completion for rebasing of appointments.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b1ec7-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="b1ec7-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b1ec7-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="b1ec7-106">Header file:</span></span>  <br/> |<span data-ttu-id="b1ec7-107">tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="b1ec7-107">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="b1ec7-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="b1ec7-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b1ec7-109">Aplicativos de cliente MAPI</span><span class="sxs-lookup"><span data-stu-id="b1ec7-109">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="b1ec7-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="b1ec7-110">Called by:</span></span>  <br/> |<span data-ttu-id="b1ec7-111">REBASE de objeto do Outlook</span><span class="sxs-lookup"><span data-stu-id="b1ec7-111">Outlook rebasing object</span></span>  <br/> |
|<span data-ttu-id="b1ec7-112">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="b1ec7-112">Pointer type:</span></span>  <br/> |<span data-ttu-id="b1ec7-113">**PFNREBASETASKCOMPLETE** conforme definido em tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="b1ec7-113">**PFNREBASETASKCOMPLETE** as defined in tzmovelib.h</span></span>  <br/> |
   
```cpp
void STDAPICALLTYPE RebaseTaskComplete(  
    ULONG ulRowIndex, 
    const SRow* pRowCur, 
    HRESULT hrResult, 
    BOOL fModified, 
    BOOL fSentUpdate, 
    const MAPIERROR* pError); 

```

## <a name="parameters"></a><span data-ttu-id="b1ec7-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b1ec7-114">Parameters</span></span>

<span data-ttu-id="b1ec7-115">_ulRowIndex_</span><span class="sxs-lookup"><span data-stu-id="b1ec7-115">_ulRowIndex_</span></span>
  
> <span data-ttu-id="b1ec7-116">[in] Na linha que foi processada.</span><span class="sxs-lookup"><span data-stu-id="b1ec7-116">[in] The row that was processed.</span></span> <span data-ttu-id="b1ec7-117">Esse índice refere-se à estrutura **[SRowSet](http://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx)** passada para [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).</span><span class="sxs-lookup"><span data-stu-id="b1ec7-117">This index refers to the **[SRowSet](http://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx)** structure passed to [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).</span></span>
    
<span data-ttu-id="b1ec7-118">_pRowCur_</span><span class="sxs-lookup"><span data-stu-id="b1ec7-118">_pRowCur_</span></span>
  
> <span data-ttu-id="b1ec7-119">in] um ponteiro para uma estrutura **[SRow](http://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** descrevendo o item que foi processado.</span><span class="sxs-lookup"><span data-stu-id="b1ec7-119">in] A pointer to an **[SRow](http://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** structure describing the item that was processed.</span></span> 
    
<span data-ttu-id="b1ec7-120">_hrResult_</span><span class="sxs-lookup"><span data-stu-id="b1ec7-120">_hrResult_</span></span>
  
> <span data-ttu-id="b1ec7-121">[in] Um **HRESULT** indicando o resultado da operação REBASE.</span><span class="sxs-lookup"><span data-stu-id="b1ec7-121">[in] An **HRESULT** indicating the result of the rebasing operation.</span></span> 
    
<span data-ttu-id="b1ec7-122">_fModified_</span><span class="sxs-lookup"><span data-stu-id="b1ec7-122">_fModified_</span></span>
  
> <span data-ttu-id="b1ec7-123">[in] Especifica se o item foi modificado.</span><span class="sxs-lookup"><span data-stu-id="b1ec7-123">[in] Specifies whether the item was modified.</span></span>
    
<span data-ttu-id="b1ec7-124">_fSentUpdate_</span><span class="sxs-lookup"><span data-stu-id="b1ec7-124">_fSentUpdate_</span></span>
  
> <span data-ttu-id="b1ec7-125">[in] Especifica se uma reunião atualizar a mensagem foi enviada.</span><span class="sxs-lookup"><span data-stu-id="b1ec7-125">[in] Specifies whether a meeting update message was sent.</span></span> 
    
<span data-ttu-id="b1ec7-126">_pError_</span><span class="sxs-lookup"><span data-stu-id="b1ec7-126">_pError_</span></span>
  
> <span data-ttu-id="b1ec7-127">[in] Um ponteiro para uma estrutura **MAPIERROR** com informações de erro estendidas.</span><span class="sxs-lookup"><span data-stu-id="b1ec7-127">[in] A pointer to a **MAPIERROR** structure with extended error information.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="b1ec7-128">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="b1ec7-128">Return values</span></span>

<span data-ttu-id="b1ec7-129">S_OK se a chamada foi bem-sucedida; Caso contrário, um código de erro.</span><span class="sxs-lookup"><span data-stu-id="b1ec7-129">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b1ec7-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="b1ec7-130">Remarks</span></span>

<span data-ttu-id="b1ec7-131">Aplicativos de cliente MAPI que usam a interface [IOlkApptRebaser](iolkapptrebaser.md) implementam esta função para controlar a conclusão das atualizações de item.</span><span class="sxs-lookup"><span data-stu-id="b1ec7-131">MAPI client applications that use the [IOlkApptRebaser](iolkapptrebaser.md) interface implement this function to track completion of item updates.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b1ec7-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="b1ec7-132">See also</span></span>

- [<span data-ttu-id="b1ec7-133">Sobre alteração de calendários por meio de programação para horário de verão</span><span class="sxs-lookup"><span data-stu-id="b1ec7-133">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

