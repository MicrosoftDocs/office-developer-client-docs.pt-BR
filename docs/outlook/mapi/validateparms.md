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
ms.openlocfilehash: a22f7628b306707474e4ffb6fdf4525e00bf0771
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770727"
---
# <a name="validateparms"></a><span data-ttu-id="cc153-103">ValidateParms</span><span class="sxs-lookup"><span data-stu-id="cc153-103">ValidateParms</span></span>

  
  
<span data-ttu-id="cc153-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cc153-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cc153-105">Chama uma função interna para verificar que os aplicativos de cliente parâmetros já se passaram a provedores de serviços.</span><span class="sxs-lookup"><span data-stu-id="cc153-105">Calls an internal function to check the parameters client applications have passed to service providers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cc153-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="cc153-106">Header file:</span></span>  <br/> |<span data-ttu-id="cc153-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="cc153-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="cc153-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="cc153-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="cc153-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="cc153-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="cc153-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="cc153-110">Called by:</span></span>  <br/> |<span data-ttu-id="cc153-111">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="cc153-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT ValidateParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="cc153-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cc153-112">Parameters</span></span>

 <span data-ttu-id="cc153-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="cc153-113">_eMethod_</span></span>
  
> <span data-ttu-id="cc153-114">[in] Especifica o enumeração, o método para validar.</span><span class="sxs-lookup"><span data-stu-id="cc153-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="cc153-115">_Primeira_</span><span class="sxs-lookup"><span data-stu-id="cc153-115">_First_</span></span>
  
> <span data-ttu-id="cc153-116">[in] Ponteiro para o primeiro argumento na pilha.</span><span class="sxs-lookup"><span data-stu-id="cc153-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cc153-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="cc153-117">Return value</span></span>

<span data-ttu-id="cc153-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="cc153-118">S_OK</span></span> 
  
> <span data-ttu-id="cc153-119">Todos os parâmetros são válidos.</span><span class="sxs-lookup"><span data-stu-id="cc153-119">All of the parameters are valid.</span></span> 
    
<span data-ttu-id="cc153-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="cc153-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="cc153-121">Um ou mais dos parâmetros não são válidos.</span><span class="sxs-lookup"><span data-stu-id="cc153-121">One or more of the parameters are not valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cc153-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="cc153-122">Remarks</span></span>

<span data-ttu-id="cc153-123">Parâmetros passados entre MAPI e serviço são considerados provedores estejam corretas e são submetidos a validação de depuração somente à macro [CheckParms](checkparms.md) .</span><span class="sxs-lookup"><span data-stu-id="cc153-123">Parameters passed between MAPI and service providers are assumed to be correct and undergo only debug validation with the [CheckParms](checkparms.md) macro.</span></span> <span data-ttu-id="cc153-124">Provedores devem verificar todos os parâmetros passados por aplicativos do cliente, mas os clientes devem presumir que parâmetros MAPI e o provedor estão corretos.</span><span class="sxs-lookup"><span data-stu-id="cc153-124">Providers should check all parameters passed in by client applications, but clients should assume that MAPI and provider parameters are correct.</span></span> <span data-ttu-id="cc153-125">Use a macro **HR_FAILED** para testar valores de retorno.</span><span class="sxs-lookup"><span data-stu-id="cc153-125">Use the **HR_FAILED** macro to test return values.</span></span> 
  
 <span data-ttu-id="cc153-126">**ValidateParms** é chamado de forma diferente, dependendo se o código de chamada é C ou C++.</span><span class="sxs-lookup"><span data-stu-id="cc153-126">**ValidateParms** is called differently depending on whether the calling code is C or C++.</span></span> <span data-ttu-id="cc153-127">C++ passa um parâmetro implícito conhecido como _Este_ para cada chamada de método, que se torna explícitas em C e é o endereço do objeto.</span><span class="sxs-lookup"><span data-stu-id="cc153-127">C++ passes an implicit parameter known as  _this_ to each method call, which becomes explicit in C and is the address of the object.</span></span> <span data-ttu-id="cc153-128">O primeiro parâmetro, _eMethod_, é um enumerador feito a interface e o método sendo validado e informa quais parâmetros esperar encontrar na pilha.</span><span class="sxs-lookup"><span data-stu-id="cc153-128">The first parameter,  _eMethod_, is an enumerator made from the interface and method being validated and tells what parameters to expect to find on the stack.</span></span> <span data-ttu-id="cc153-129">O segundo parâmetro é diferente para C e C++.</span><span class="sxs-lookup"><span data-stu-id="cc153-129">The second parameter is different for C and C++.</span></span> <span data-ttu-id="cc153-130">No C++, ele é chamado _primeiro_, e é o primeiro parâmetro para o método sendo validado.</span><span class="sxs-lookup"><span data-stu-id="cc153-130">In C++ it is called  _First_, and it is the first parameter to the method being validated.</span></span> <span data-ttu-id="cc153-131">O segundo parâmetro para o idioma do C, _ppThis_, é o endereço do primeiro parâmetro para o método que é sempre um ponteiro de objeto.</span><span class="sxs-lookup"><span data-stu-id="cc153-131">The second parameter for the C language,  _ppThis_, is the address of the first parameter to the method which is always an object pointer.</span></span> <span data-ttu-id="cc153-132">Em ambos os casos, o segundo parâmetro fornece o endereço do início da lista de parâmetros do método e com base em _eMethod_, move para baixo a pilha de itens e valida os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="cc153-132">In both cases, the second parameter gives the address of the beginning of the method's parameter list, and based on  _eMethod_, moves down the stack and validates the parameters.</span></span> 
  
<span data-ttu-id="cc153-133">Provedores implementando interfaces comuns, como **IMAPITable** e **IMAPIProp** sempre devem verificar parâmetros usando a função **ValidateParms** para tornar-se de consistência entre todos os provedores.</span><span class="sxs-lookup"><span data-stu-id="cc153-133">Providers implementing common interfaces such as **IMAPITable** and **IMAPIProp** should always check parameters using the **ValidateParms** function in order to make sure consistency across all providers.</span></span> <span data-ttu-id="cc153-134">Funções de validação de parâmetro adicional tiverem sido definidas para alguns tipos de parâmetro complexo a ser usado em vez disso conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="cc153-134">Additional parameter validation functions have been defined for some complex parameter types to be used instead as appropriate.</span></span> <span data-ttu-id="cc153-135">Consulte os tópicos de referência para as seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="cc153-135">See the reference topics for the following functions:</span></span> 
  
- [<span data-ttu-id="cc153-136">FBadColumnSet</span><span class="sxs-lookup"><span data-stu-id="cc153-136">FBadColumnSet</span></span>](fbadcolumnset.md)
    
- [<span data-ttu-id="cc153-137">FBadEntryList</span><span class="sxs-lookup"><span data-stu-id="cc153-137">FBadEntryList</span></span>](fbadentrylist.md)
    
- [<span data-ttu-id="cc153-138">FBadProp</span><span class="sxs-lookup"><span data-stu-id="cc153-138">FBadProp</span></span>](fbadprop.md)
    
- [<span data-ttu-id="cc153-139">FBadProp</span><span class="sxs-lookup"><span data-stu-id="cc153-139">FBadProp</span></span>](fbadprop.md)
    
- [<span data-ttu-id="cc153-140">FBadRestriction</span><span class="sxs-lookup"><span data-stu-id="cc153-140">FBadRestriction</span></span>](fbadrestriction.md)
    
- [<span data-ttu-id="cc153-141">FBadRestriction</span><span class="sxs-lookup"><span data-stu-id="cc153-141">FBadRestriction</span></span>](fbadrestriction.md)
    
- [<span data-ttu-id="cc153-142">FBadRglpszW</span><span class="sxs-lookup"><span data-stu-id="cc153-142">FBadRglpszW</span></span>](fbadrglpszw.md)
    
- [<span data-ttu-id="cc153-143">FBadRow</span><span class="sxs-lookup"><span data-stu-id="cc153-143">FBadRow</span></span>](fbadrow.md)
    
- [<span data-ttu-id="cc153-144">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="cc153-144">FBadRowSet</span></span>](fbadrowset.md)
    
- [<span data-ttu-id="cc153-145">FBadSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="cc153-145">FBadSortOrderSet</span></span>](fbadsortorderset.md)
    
<span data-ttu-id="cc153-146">Métodos herdados usam a mesma validação de parâmetro como a interface do qual eles herdam.</span><span class="sxs-lookup"><span data-stu-id="cc153-146">Inherited methods use the same parameter validation as the interface from which they inherit.</span></span> <span data-ttu-id="cc153-147">Por exemplo, o parâmetro de verificação de **IMessage** e **IMAPIProp** deve ser o mesmo.</span><span class="sxs-lookup"><span data-stu-id="cc153-147">For example, the parameter checking for **IMessage** and **IMAPIProp** should be the same.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cc153-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="cc153-148">See also</span></span>



[<span data-ttu-id="cc153-149">UlValidateParms</span><span class="sxs-lookup"><span data-stu-id="cc153-149">UlValidateParms</span></span>](ulvalidateparms.md)

