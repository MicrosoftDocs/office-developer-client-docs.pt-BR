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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419608"
---
# <a name="ulvalidateparms"></a><span data-ttu-id="b4283-103">UlValidateParms</span><span class="sxs-lookup"><span data-stu-id="b4283-103">UlValidateParms</span></span>

  
  
<span data-ttu-id="b4283-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b4283-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b4283-105">Chama uma função interna para verificar os parâmetros que os aplicativos cliente passaram para provedores de serviços e MAPI.</span><span class="sxs-lookup"><span data-stu-id="b4283-105">Calls an internal function to check the parameters client applications have passed to service providers and MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b4283-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="b4283-106">Header file:</span></span>  <br/> |<span data-ttu-id="b4283-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="b4283-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="b4283-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="b4283-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b4283-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b4283-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b4283-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="b4283-110">Called by:</span></span>  <br/> |<span data-ttu-id="b4283-111">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="b4283-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT UlValidateParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="b4283-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b4283-112">Parameters</span></span>

 <span data-ttu-id="b4283-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="b4283-113">_eMethod_</span></span>
  
> <span data-ttu-id="b4283-114">[in] Especifica, por enumeração, o método a ser validado.</span><span class="sxs-lookup"><span data-stu-id="b4283-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="b4283-115">_Primeira_</span><span class="sxs-lookup"><span data-stu-id="b4283-115">_First_</span></span>
  
> <span data-ttu-id="b4283-116">[in] Ponteiro para o primeiro argumento na pilha.</span><span class="sxs-lookup"><span data-stu-id="b4283-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b4283-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b4283-117">Return value</span></span>

<span data-ttu-id="b4283-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="b4283-118">S_OK</span></span> 
  
> <span data-ttu-id="b4283-119">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="b4283-119">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="b4283-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="b4283-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="b4283-121">Um erro impedia a conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="b4283-121">An error prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b4283-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="b4283-122">Remarks</span></span>

<span data-ttu-id="b4283-123">Os parâmetros passados entre o MAPI e os provedores de serviços são assumidos como corretos e passam apenas pela validação de depuração com a macro [CheckParms.](checkparms.md)</span><span class="sxs-lookup"><span data-stu-id="b4283-123">Parameters passed between MAPI and service providers are assumed to be correct and undergo only debug validation with the [CheckParms](checkparms.md) macro.</span></span> <span data-ttu-id="b4283-124">Os provedores devem verificar todos os parâmetros passados pelos aplicativos cliente, mas os clientes devem presumir que os parâmetros MAPI e provedor estão corretos.</span><span class="sxs-lookup"><span data-stu-id="b4283-124">Providers should check all parameters passed in by client applications, but clients should assume that MAPI and provider parameters are correct.</span></span> <span data-ttu-id="b4283-125">Use a **macro HR_FAILED** para testar os valores de retorno.</span><span class="sxs-lookup"><span data-stu-id="b4283-125">Use the **HR_FAILED** macro to test return values.</span></span> 
  
<span data-ttu-id="b4283-126">A macro **UlValidateParms** é chamada de forma diferente, dependendo se o código de chamada é C ou C++.</span><span class="sxs-lookup"><span data-stu-id="b4283-126">The **UlValidateParms** macro is called differently depending on whether the calling code is C or C++.</span></span> <span data-ttu-id="b4283-127">Essa macro é usada para validar parâmetros para os poucos **métodos IUnknown** e MAPI que retornam ULONG em vez de valores HRESULT; a macro [ValidateParms](validateparms.md) funciona para todos os outros.</span><span class="sxs-lookup"><span data-stu-id="b4283-127">This macro is used to validate parameters for the few **IUnknown** and MAPI methods that return ULONG instead of HRESULT values; the [ValidateParms](validateparms.md) macro works for all others.</span></span> 
  

