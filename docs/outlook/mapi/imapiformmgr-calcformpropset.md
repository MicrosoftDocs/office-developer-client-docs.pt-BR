---
title: IMAPIFormMgrCalcFormPropSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.CalcFormPropSet
api_type:
- COM
ms.assetid: ab302bfd-5cff-49b4-b0d2-308ae5af478d
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: bf072aba27c90b7cea80c464e17fafb47524b695
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436423"
---
# <a name="imapiformmgrcalcformpropset"></a><span data-ttu-id="50fe2-103">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="50fe2-103">IMAPIFormMgr::CalcFormPropSet</span></span>

  
  
<span data-ttu-id="50fe2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50fe2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50fe2-105">Retorna uma matriz das propriedades que um grupo de formulários usa.</span><span class="sxs-lookup"><span data-stu-id="50fe2-105">Returns an array of the properties that a group of forms uses.</span></span>
  
```cpp
HRESULT CalcFormPropSet(
  LPSMAPIFORMINFOARRAY pfrminfoarray,
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a><span data-ttu-id="50fe2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="50fe2-106">Parameters</span></span>

 <span data-ttu-id="50fe2-107">_pfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="50fe2-107">_pfrminfoarray_</span></span>
  
> <span data-ttu-id="50fe2-108">[in] Um ponteiro para uma matriz de objetos de informações de formulário que identificam os formulários para os quais retornar propriedades.</span><span class="sxs-lookup"><span data-stu-id="50fe2-108">[in] A pointer to an array of form information objects that identify the forms for which to return properties.</span></span>
    
 <span data-ttu-id="50fe2-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="50fe2-109">_ulFlags_</span></span>
  
> <span data-ttu-id="50fe2-110">[in] Uma bitmask de sinalizadores que controla como a matriz de propriedades no  _parâmetro ppResults_ é retornada.</span><span class="sxs-lookup"><span data-stu-id="50fe2-110">[in] A bitmask of flags that controls how the property array in the  _ppResults_ parameter is returned.</span></span> <span data-ttu-id="50fe2-111">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="50fe2-111">The following flags can be set:</span></span> 
    
<span data-ttu-id="50fe2-112">FORMPROPSET_INTERSECTION</span><span class="sxs-lookup"><span data-stu-id="50fe2-112">FORMPROPSET_INTERSECTION</span></span> 
  
> <span data-ttu-id="50fe2-113">A matriz retornada contém a interseção das propriedades do formulário.</span><span class="sxs-lookup"><span data-stu-id="50fe2-113">The returned array contains the intersection of the form's properties.</span></span>
    
<span data-ttu-id="50fe2-114">FORMPROPSET_UNION</span><span class="sxs-lookup"><span data-stu-id="50fe2-114">FORMPROPSET_UNION</span></span> 
  
> <span data-ttu-id="50fe2-115">A matriz retornada contém a união das propriedades do formulário.</span><span class="sxs-lookup"><span data-stu-id="50fe2-115">The returned array contains the union of the form's properties.</span></span>
    
<span data-ttu-id="50fe2-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="50fe2-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="50fe2-117">As cadeias de caracteres retornadas na matriz estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="50fe2-117">The strings returned in the array are in Unicode format.</span></span> <span data-ttu-id="50fe2-118">Se o MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="50fe2-118">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="50fe2-119">_ppResults_</span><span class="sxs-lookup"><span data-stu-id="50fe2-119">_ppResults_</span></span>
  
> <span data-ttu-id="50fe2-120">[out] Um ponteiro para um ponteiro para a estrutura [SMAPIFormPropArray](smapiformproparray.md) retornada, que contém as propriedades que os formulários usam.</span><span class="sxs-lookup"><span data-stu-id="50fe2-120">[out] A pointer to a pointer to the returned [SMAPIFormPropArray](smapiformproparray.md) structure, which contains the properties that the forms use.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="50fe2-121">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="50fe2-121">Return value</span></span>

<span data-ttu-id="50fe2-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="50fe2-122">S_OK</span></span> 
  
> <span data-ttu-id="50fe2-123">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="50fe2-123">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="50fe2-124">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="50fe2-124">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="50fe2-125">O sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode ou MAPI_UNICODE não foi definido e a implementação dá suporte apenas a Unicode.</span><span class="sxs-lookup"><span data-stu-id="50fe2-125">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="50fe2-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="50fe2-126">Remarks</span></span>

<span data-ttu-id="50fe2-127">Visualizadores de formulário chamam o método **IMAPIFormMgr::CalcFormPropSet** para obter uma matriz das propriedades que um grupo de formulários usa.</span><span class="sxs-lookup"><span data-stu-id="50fe2-127">Form viewers call the **IMAPIFormMgr::CalcFormPropSet** method to obtain an array of the properties that a group of forms uses.</span></span> <span data-ttu-id="50fe2-128">**CalcFormPropSet** assume uma interseção ou uma união dos conjuntos de propriedades desses formulários, dependendo do sinalizador definido no parâmetro  _ulFlags,_ e retorna uma estrutura **SMAPIFormPropArray** que contém o grupo de propriedades resultante.</span><span class="sxs-lookup"><span data-stu-id="50fe2-128">**CalcFormPropSet** takes either an intersection or a union of these forms' property sets, depending on the flag set in the  _ulFlags_ parameter, and it returns an **SMAPIFormPropArray** structure that contains the resulting group of properties.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="50fe2-129">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="50fe2-129">Notes to implementers</span></span>

<span data-ttu-id="50fe2-130">Se um visualizador de formulário passar o sinalizador MAPI_UNICODE no parâmetro  _ulFlags,_ todas as cadeias de caracteres deverão ser retornadas como cadeias de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="50fe2-130">If a form viewer passes the MAPI_UNICODE flag in the  _ulFlags_ parameter, all strings should be returned as Unicode strings.</span></span> <span data-ttu-id="50fe2-131">Provedores de biblioteca de formulário que não suportam cadeias de caracteres Unicode devem retornar MAPI_E_BAD_CHARWIDTH se MAPI_UNICODE for passado.</span><span class="sxs-lookup"><span data-stu-id="50fe2-131">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="50fe2-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="50fe2-132">See also</span></span>



[<span data-ttu-id="50fe2-133">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="50fe2-133">SMAPIFormPropArray</span></span>](smapiformproparray.md)
  
[<span data-ttu-id="50fe2-134">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="50fe2-134">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

