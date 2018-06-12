---
title: IOlkApptRebaserEndEnumerateAppointments
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bc4506c7-7a4f-940d-d0a6-e0fab4561a88
description: Aguardará enumeração de compromisso em uma pasta de calendário para a conclusão e retorna uma lista de compromissos essa necessidade alteração da base.
ms.openlocfilehash: d7d29a88114d7b3973b8f04e924dc1dd8489a097
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765994"
---
# <a name="iolkapptrebaserendenumerateappointments"></a><span data-ttu-id="aa628-103">IOlkApptRebaser::EndEnumerateAppointments</span><span class="sxs-lookup"><span data-stu-id="aa628-103">IOlkApptRebaser::EndEnumerateAppointments</span></span>

<span data-ttu-id="aa628-104">Aguardará enumeração de compromisso em uma pasta de calendário para a conclusão e retorna uma lista de compromissos essa necessidade alteração da base.</span><span class="sxs-lookup"><span data-stu-id="aa628-104">Waits for appointment enumeration in a calendar folder to complete and returns a list of appointments that need rebasing.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="aa628-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="aa628-105">Quick info</span></span>

<span data-ttu-id="aa628-106">Consulte [IOlkApptRebaser](iolkapptrebaser.md).</span><span class="sxs-lookup"><span data-stu-id="aa628-106">See [IOlkApptRebaser](iolkapptrebaser.md).</span></span>
  
```cpp
HRESULT EndEnumerateAppointments( 
    void *pContext, 
    HRESULT *phResult, 
    MAPIERROR **ppError, 
    SRowSet **ppRows);
```

## <a name="parameters"></a><span data-ttu-id="aa628-107">Par�metros</span><span class="sxs-lookup"><span data-stu-id="aa628-107">Parameters</span></span>

<span data-ttu-id="aa628-108">_pContext_</span><span class="sxs-lookup"><span data-stu-id="aa628-108">_pContext_</span></span>
  
> <span data-ttu-id="aa628-109">[in] Necessário.</span><span class="sxs-lookup"><span data-stu-id="aa628-109">[in] Required.</span></span> <span data-ttu-id="aa628-110">Um ponteiro para o contexto obtido de uma chamada anterior ao [IOlkApptRebaser::BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md).</span><span class="sxs-lookup"><span data-stu-id="aa628-110">A pointer to the context obtained from a prior call to [IOlkApptRebaser::BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md).</span></span>
    
<span data-ttu-id="aa628-111">_phResult_</span><span class="sxs-lookup"><span data-stu-id="aa628-111">_phResult_</span></span>
  
> <span data-ttu-id="aa628-112">[out] Necessário.</span><span class="sxs-lookup"><span data-stu-id="aa628-112">[out] Required.</span></span> <span data-ttu-id="aa628-113">Um ponteiro para um **HRESULT** para recuperar os resultados da operação de enumeração.</span><span class="sxs-lookup"><span data-stu-id="aa628-113">A pointer to an **HRESULT** to retrieve the results of the enumeration operation.</span></span> 
    
<span data-ttu-id="aa628-114">_ppError_</span><span class="sxs-lookup"><span data-stu-id="aa628-114">_ppError_</span></span>
  
> <span data-ttu-id="aa628-115">[out] Opcional.</span><span class="sxs-lookup"><span data-stu-id="aa628-115">[out] Optional.</span></span> <span data-ttu-id="aa628-116">Um ponteiro para um ponteiro para uma estrutura **MAPIERROR** para recuperar informações de erro estendidas.</span><span class="sxs-lookup"><span data-stu-id="aa628-116">A pointer to a pointer to a **MAPIERROR** structure to retrieve extended error information.</span></span> 
    
<span data-ttu-id="aa628-117">_ppRows_</span><span class="sxs-lookup"><span data-stu-id="aa628-117">_ppRows_</span></span>
  
> <span data-ttu-id="aa628-118">[out] Necessário.</span><span class="sxs-lookup"><span data-stu-id="aa628-118">[out] Required.</span></span> <span data-ttu-id="aa628-119">Um ponteiro para um ponteiro para uma estrutura de [SRowSet](http://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx) que descreve os compromissos que precisam a alteração da base.</span><span class="sxs-lookup"><span data-stu-id="aa628-119">A pointer to a pointer to an [SRowSet](http://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx) structure that describes the appointments that need rebasing.</span></span> <span data-ttu-id="aa628-120">Essa estrutura geralmente será transmitida ao [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).</span><span class="sxs-lookup"><span data-stu-id="aa628-120">This structure will usually be passed to [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).</span></span>
    
## <a name="return-values"></a><span data-ttu-id="aa628-121">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="aa628-121">Return values</span></span>

<span data-ttu-id="aa628-122">S_OK se a chamada foi bem-sucedida; Caso contrário, um código de erro.</span><span class="sxs-lookup"><span data-stu-id="aa628-122">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="aa628-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="aa628-123">See also</span></span>

- [<span data-ttu-id="aa628-124">Sobre alteração de calendários por meio de programação para horário de verão</span><span class="sxs-lookup"><span data-stu-id="aa628-124">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

