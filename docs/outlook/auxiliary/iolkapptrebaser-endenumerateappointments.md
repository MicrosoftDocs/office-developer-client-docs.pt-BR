---
title: IOlkApptRebaserEndEnumerateAppointments
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bc4506c7-7a4f-940d-d0a6-e0fab4561a88
description: Aguarda a conclusão da enumeração de compromissos em uma pasta de calendário e retorna uma lista de compromissos que precisam de alteração programática.
ms.openlocfilehash: 5be6fd9ce33374725b36429cd0fbc717776c9ab9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321900"
---
# <a name="iolkapptrebaserendenumerateappointments"></a><span data-ttu-id="9cd4f-103">IOlkApptRebaser::EndEnumerateAppointments</span><span class="sxs-lookup"><span data-stu-id="9cd4f-103">IOlkApptRebaser::EndEnumerateAppointments</span></span>

<span data-ttu-id="9cd4f-104">Aguarda a conclusão da enumeração de compromissos em uma pasta de calendário e retorna uma lista de compromissos que precisam de alteração programática.</span><span class="sxs-lookup"><span data-stu-id="9cd4f-104">Waits for appointment enumeration in a calendar folder to complete and returns a list of appointments that need rebasing.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="9cd4f-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="9cd4f-105">Quick info</span></span>

<span data-ttu-id="9cd4f-106">Confira [IOlkApptRebaser](iolkapptrebaser.md).</span><span class="sxs-lookup"><span data-stu-id="9cd4f-106">See [IOlkApptRebaser](iolkapptrebaser.md).</span></span>
  
```cpp
HRESULT EndEnumerateAppointments( 
    void *pContext, 
    HRESULT *phResult, 
    MAPIERROR **ppError, 
    SRowSet **ppRows);
```

## <a name="parameters"></a><span data-ttu-id="9cd4f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9cd4f-107">Parameters</span></span>

<span data-ttu-id="9cd4f-108">_pContext_</span><span class="sxs-lookup"><span data-stu-id="9cd4f-108">_pContext_</span></span>
  
> <span data-ttu-id="9cd4f-109">[in] Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="9cd4f-109">[in] Required.</span></span> <span data-ttu-id="9cd4f-110">Um ponteiro para o contexto obtido em uma chamada anterior para [IOlkApptRebaser::BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md).</span><span class="sxs-lookup"><span data-stu-id="9cd4f-110">A pointer to the context obtained from a prior call to [IOlkApptRebaser::BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md).</span></span>
    
<span data-ttu-id="9cd4f-111">_phResult_</span><span class="sxs-lookup"><span data-stu-id="9cd4f-111">_phResult_</span></span>
  
> <span data-ttu-id="9cd4f-112">[out] Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="9cd4f-112">[out] Required.</span></span> <span data-ttu-id="9cd4f-113">Um ponteiro para um **HRESULT** para recuperar os resultados da operação de enumeração.</span><span class="sxs-lookup"><span data-stu-id="9cd4f-113">A pointer to an **HRESULT** to retrieve the results of the enumeration operation.</span></span> 
    
<span data-ttu-id="9cd4f-114">_ppError_</span><span class="sxs-lookup"><span data-stu-id="9cd4f-114">_ppError_</span></span>
  
> <span data-ttu-id="9cd4f-115">[out] Opcional.</span><span class="sxs-lookup"><span data-stu-id="9cd4f-115">[out] Optional.</span></span> <span data-ttu-id="9cd4f-116">Um ponteiro para uma estrutura **MAPIERROR** para recuperar informações sobre erros estendidas.</span><span class="sxs-lookup"><span data-stu-id="9cd4f-116">A pointer to a pointer to a **MAPIERROR** structure to retrieve extended error information.</span></span> 
    
<span data-ttu-id="9cd4f-117">_ppRows_</span><span class="sxs-lookup"><span data-stu-id="9cd4f-117">_ppRows_</span></span>
  
> <span data-ttu-id="9cd4f-118">[out] Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="9cd4f-118">[out] Required.</span></span> <span data-ttu-id="9cd4f-119">Um ponteiro para uma estrutura [SRowSet](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx) que descreve os compromissos que precisam de alteração programática.</span><span class="sxs-lookup"><span data-stu-id="9cd4f-119">A pointer to a pointer to an [SRowSet](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx) structure that describes the appointments that need rebasing.</span></span> <span data-ttu-id="9cd4f-120">Essa estrutura geralmente é passada para [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).</span><span class="sxs-lookup"><span data-stu-id="9cd4f-120">This structure will usually be passed to [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).</span></span>
    
## <a name="return-values"></a><span data-ttu-id="9cd4f-121">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9cd4f-121">Return values</span></span>

<span data-ttu-id="9cd4f-122">S_OK se a chamada foi bem-sucedida. Caso contrário, um código de erro.</span><span class="sxs-lookup"><span data-stu-id="9cd4f-122">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9cd4f-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="9cd4f-123">See also</span></span>

- [<span data-ttu-id="9cd4f-124">Sobre a alteração programática da base de calendários para o horário de verão</span><span class="sxs-lookup"><span data-stu-id="9cd4f-124">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

