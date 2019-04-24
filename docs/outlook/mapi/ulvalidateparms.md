---
title: UlValidateParms
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlValidateParms
api_type:
- COM
ms.assetid: 02c66b46-1f01-43fb-832c-bac27aaae19f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e0cdcb92238dd4dffbcd6514e698e5511b05bf45
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360491"
---
# <a name="ulvalidateparms"></a><span data-ttu-id="9c239-103">UlValidateParms</span><span class="sxs-lookup"><span data-stu-id="9c239-103">UlValidateParms</span></span>

  
  
<span data-ttu-id="9c239-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9c239-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9c239-105">Chama uma função interna para verificar os parâmetros que os aplicativos clientes passaram para os provedores de serviço e MAPI.</span><span class="sxs-lookup"><span data-stu-id="9c239-105">Calls an internal function to check the parameters client applications have passed to service providers and MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9c239-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="9c239-106">Header file:</span></span>  <br/> |<span data-ttu-id="9c239-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="9c239-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="9c239-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="9c239-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="9c239-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="9c239-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="9c239-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="9c239-110">Called by:</span></span>  <br/> |<span data-ttu-id="9c239-111">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="9c239-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT UlValidateParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="9c239-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9c239-112">Parameters</span></span>

 <span data-ttu-id="9c239-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="9c239-113">_eMethod_</span></span>
  
> <span data-ttu-id="9c239-114">no Especifica, por enumeração, o método a ser validado.</span><span class="sxs-lookup"><span data-stu-id="9c239-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="9c239-115">_Primeira_</span><span class="sxs-lookup"><span data-stu-id="9c239-115">_First_</span></span>
  
> <span data-ttu-id="9c239-116">no Ponteiro para o primeiro argumento na pilha.</span><span class="sxs-lookup"><span data-stu-id="9c239-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9c239-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9c239-117">Return value</span></span>

<span data-ttu-id="9c239-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="9c239-118">S_OK</span></span> 
  
> <span data-ttu-id="9c239-119">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="9c239-119">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="9c239-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="9c239-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="9c239-121">Um erro impediu a conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="9c239-121">An error prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9c239-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="9c239-122">Remarks</span></span>

<span data-ttu-id="9c239-123">Os parâmetros passados entre MAPI e provedores de serviço são considerados corretos e passam apenas na validação da depuração com a macro [CheckParms](checkparms.md) .</span><span class="sxs-lookup"><span data-stu-id="9c239-123">Parameters passed between MAPI and service providers are assumed to be correct and undergo only debug validation with the [CheckParms](checkparms.md) macro.</span></span> <span data-ttu-id="9c239-124">Os provedores devem verificar todos os parâmetros passados por aplicativos cliente, mas os clientes devem supor que os parâmetros MAPI e Provider estejam corretos.</span><span class="sxs-lookup"><span data-stu-id="9c239-124">Providers should check all parameters passed in by client applications, but clients should assume that MAPI and provider parameters are correct.</span></span> <span data-ttu-id="9c239-125">Use a macro **HR_FAILED** para testar valores de retorno.</span><span class="sxs-lookup"><span data-stu-id="9c239-125">Use the **HR_FAILED** macro to test return values.</span></span> 
  
<span data-ttu-id="9c239-126">A macro **UlValidateParms** é chamada de forma diferente, dependendo se o código de chamada é C ou C++.</span><span class="sxs-lookup"><span data-stu-id="9c239-126">The **UlValidateParms** macro is called differently depending on whether the calling code is C or C++.</span></span> <span data-ttu-id="9c239-127">Essa macro é usada para validar parâmetros para os poucos métodos **IUnknown** e MAPI que retornam ULONG em vez de HRESULT valores; a macro [ValidateParms](validateparms.md) funciona para todos os outros.</span><span class="sxs-lookup"><span data-stu-id="9c239-127">This macro is used to validate parameters for the few **IUnknown** and MAPI methods that return ULONG instead of HRESULT values; the [ValidateParms](validateparms.md) macro works for all others.</span></span> 
  

