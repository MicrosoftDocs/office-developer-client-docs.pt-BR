---
title: ValidateParms
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ValidateParms
api_type:
- COM
ms.assetid: 3ede1a35-4acc-4b8f-a1bd-027f35798a37
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f2669f703827924493387c4beac0b64b25672860
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436795"
---
# <a name="validateparms"></a><span data-ttu-id="a8e31-103">ValidateParms</span><span class="sxs-lookup"><span data-stu-id="a8e31-103">ValidateParms</span></span>

  
  
<span data-ttu-id="a8e31-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a8e31-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a8e31-105">Chama uma função interna para verificar os parâmetros que os aplicativos clientes passaram para os provedores de serviço.</span><span class="sxs-lookup"><span data-stu-id="a8e31-105">Calls an internal function to check the parameters client applications have passed to service providers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a8e31-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="a8e31-106">Header file:</span></span>  <br/> |<span data-ttu-id="a8e31-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="a8e31-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="a8e31-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="a8e31-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a8e31-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a8e31-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a8e31-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="a8e31-110">Called by:</span></span>  <br/> |<span data-ttu-id="a8e31-111">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="a8e31-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT ValidateParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="a8e31-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a8e31-112">Parameters</span></span>

 <span data-ttu-id="a8e31-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="a8e31-113">_eMethod_</span></span>
  
> <span data-ttu-id="a8e31-114">no Especifica, por enumeração, o método a ser validado.</span><span class="sxs-lookup"><span data-stu-id="a8e31-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="a8e31-115">_Primeira_</span><span class="sxs-lookup"><span data-stu-id="a8e31-115">_First_</span></span>
  
> <span data-ttu-id="a8e31-116">no Ponteiro para o primeiro argumento na pilha.</span><span class="sxs-lookup"><span data-stu-id="a8e31-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a8e31-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a8e31-117">Return value</span></span>

<span data-ttu-id="a8e31-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="a8e31-118">S_OK</span></span> 
  
> <span data-ttu-id="a8e31-119">Todos os parâmetros são válidos.</span><span class="sxs-lookup"><span data-stu-id="a8e31-119">All of the parameters are valid.</span></span> 
    
<span data-ttu-id="a8e31-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="a8e31-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="a8e31-121">Um ou mais parâmetros não são válidos.</span><span class="sxs-lookup"><span data-stu-id="a8e31-121">One or more of the parameters are not valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a8e31-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="a8e31-122">Remarks</span></span>

<span data-ttu-id="a8e31-123">Os parâmetros passados entre MAPI e provedores de serviço são considerados corretos e passam apenas na validação da depuração com a macro [CheckParms](checkparms.md) .</span><span class="sxs-lookup"><span data-stu-id="a8e31-123">Parameters passed between MAPI and service providers are assumed to be correct and undergo only debug validation with the [CheckParms](checkparms.md) macro.</span></span> <span data-ttu-id="a8e31-124">Os provedores devem verificar todos os parâmetros passados por aplicativos cliente, mas os clientes devem supor que os parâmetros MAPI e Provider estejam corretos.</span><span class="sxs-lookup"><span data-stu-id="a8e31-124">Providers should check all parameters passed in by client applications, but clients should assume that MAPI and provider parameters are correct.</span></span> <span data-ttu-id="a8e31-125">Use a macro **HR_FAILED** para testar valores de retorno.</span><span class="sxs-lookup"><span data-stu-id="a8e31-125">Use the **HR_FAILED** macro to test return values.</span></span> 
  
 <span data-ttu-id="a8e31-126">**ValidateParms** é chamado de forma diferente, dependendo se o código de chamada é C ou C++.</span><span class="sxs-lookup"><span data-stu-id="a8e31-126">**ValidateParms** is called differently depending on whether the calling code is C or C++.</span></span> <span data-ttu-id="a8e31-127">O C++ passa um parâmetro implícito conhecido como _este_ para cada chamada de método, que se torna explícita em C e é o endereço do objeto.</span><span class="sxs-lookup"><span data-stu-id="a8e31-127">C++ passes an implicit parameter known as  _this_ to each method call, which becomes explicit in C and is the address of the object.</span></span> <span data-ttu-id="a8e31-128">O primeiro parâmetro, _eMethod_, é um enumerador feito a partir da interface e do método que está sendo validado e informa quais parâmetros esperar localizar na pilha.</span><span class="sxs-lookup"><span data-stu-id="a8e31-128">The first parameter,  _eMethod_, is an enumerator made from the interface and method being validated and tells what parameters to expect to find on the stack.</span></span> <span data-ttu-id="a8e31-129">O segundo parâmetro é diferente para C e C++.</span><span class="sxs-lookup"><span data-stu-id="a8e31-129">The second parameter is different for C and C++.</span></span> <span data-ttu-id="a8e31-130">Em C++, ele é chamado _primeiro_e é o primeiro parâmetro para o método que está sendo validado.</span><span class="sxs-lookup"><span data-stu-id="a8e31-130">In C++ it is called  _First_, and it is the first parameter to the method being validated.</span></span> <span data-ttu-id="a8e31-131">O segundo parâmetro da linguagem C, _ppThis_, é o endereço do primeiro parâmetro para o método que é sempre um ponteiro de objeto.</span><span class="sxs-lookup"><span data-stu-id="a8e31-131">The second parameter for the C language,  _ppThis_, is the address of the first parameter to the method which is always an object pointer.</span></span> <span data-ttu-id="a8e31-132">Em ambos os casos, o segundo parâmetro retorna o endereço do início da lista de parâmetros do método e, com base no _eMethod_, move para baixo a pilha e valida os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="a8e31-132">In both cases, the second parameter gives the address of the beginning of the method's parameter list, and based on  _eMethod_, moves down the stack and validates the parameters.</span></span> 
  
<span data-ttu-id="a8e31-133">Os provedores que implementam interfaces \*\*\*\* comuns como IMAPITable e **IMAPIProp** devem sempre verificar parâmetros usando a função **ValidateParms** para garantir a consistência entre todos os provedores.</span><span class="sxs-lookup"><span data-stu-id="a8e31-133">Providers implementing common interfaces such as **IMAPITable** and **IMAPIProp** should always check parameters using the **ValidateParms** function in order to make sure consistency across all providers.</span></span> <span data-ttu-id="a8e31-134">Funções de validação de parâmetro adicionais foram definidas para alguns tipos de parâmetros complexos a serem usados, conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="a8e31-134">Additional parameter validation functions have been defined for some complex parameter types to be used instead as appropriate.</span></span> <span data-ttu-id="a8e31-135">Consulte os tópicos de referência para as seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="a8e31-135">See the reference topics for the following functions:</span></span> 
  
- [<span data-ttu-id="a8e31-136">FBadColumnSet</span><span class="sxs-lookup"><span data-stu-id="a8e31-136">FBadColumnSet</span></span>](fbadcolumnset.md)
    
- [<span data-ttu-id="a8e31-137">FBadEntryList</span><span class="sxs-lookup"><span data-stu-id="a8e31-137">FBadEntryList</span></span>](fbadentrylist.md)
    
- [<span data-ttu-id="a8e31-138">FBadProp</span><span class="sxs-lookup"><span data-stu-id="a8e31-138">FBadProp</span></span>](fbadprop.md)
    
- [<span data-ttu-id="a8e31-139">FBadProp</span><span class="sxs-lookup"><span data-stu-id="a8e31-139">FBadProp</span></span>](fbadprop.md)
    
- [<span data-ttu-id="a8e31-140">FBadRestriction</span><span class="sxs-lookup"><span data-stu-id="a8e31-140">FBadRestriction</span></span>](fbadrestriction.md)
    
- [<span data-ttu-id="a8e31-141">FBadRestriction</span><span class="sxs-lookup"><span data-stu-id="a8e31-141">FBadRestriction</span></span>](fbadrestriction.md)
    
- [<span data-ttu-id="a8e31-142">FBadRglpszW</span><span class="sxs-lookup"><span data-stu-id="a8e31-142">FBadRglpszW</span></span>](fbadrglpszw.md)
    
- [<span data-ttu-id="a8e31-143">FBadRow</span><span class="sxs-lookup"><span data-stu-id="a8e31-143">FBadRow</span></span>](fbadrow.md)
    
- [<span data-ttu-id="a8e31-144">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="a8e31-144">FBadRowSet</span></span>](fbadrowset.md)
    
- [<span data-ttu-id="a8e31-145">FBadSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="a8e31-145">FBadSortOrderSet</span></span>](fbadsortorderset.md)
    
<span data-ttu-id="a8e31-146">Os métodos herdados usam a mesma validação de parâmetro que a interface da qual eles herdam.</span><span class="sxs-lookup"><span data-stu-id="a8e31-146">Inherited methods use the same parameter validation as the interface from which they inherit.</span></span> <span data-ttu-id="a8e31-147">Por exemplo, a verificação de parâmetros para **IMessage** e **IMAPIProp** deve ser a mesma.</span><span class="sxs-lookup"><span data-stu-id="a8e31-147">For example, the parameter checking for **IMessage** and **IMAPIProp** should be the same.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a8e31-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="a8e31-148">See also</span></span>



[<span data-ttu-id="a8e31-149">UlValidateParms</span><span class="sxs-lookup"><span data-stu-id="a8e31-149">UlValidateParms</span></span>](ulvalidateparms.md)

