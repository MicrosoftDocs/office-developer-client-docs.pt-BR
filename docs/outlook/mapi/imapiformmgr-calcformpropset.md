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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342081"
---
# <a name="imapiformmgrcalcformpropset"></a><span data-ttu-id="27912-103">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="27912-103">IMAPIFormMgr::CalcFormPropSet</span></span>

  
  
<span data-ttu-id="27912-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="27912-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="27912-105">Retorna uma matriz das propriedades usadas por um grupo de formulários.</span><span class="sxs-lookup"><span data-stu-id="27912-105">Returns an array of the properties that a group of forms uses.</span></span>
  
```cpp
HRESULT CalcFormPropSet(
  LPSMAPIFORMINFOARRAY pfrminfoarray,
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a><span data-ttu-id="27912-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="27912-106">Parameters</span></span>

 <span data-ttu-id="27912-107">_pfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="27912-107">_pfrminfoarray_</span></span>
  
> <span data-ttu-id="27912-108">no Um ponteiro para uma matriz de objetos de informação de formulário que identificam os formulários para os quais retornar propriedades.</span><span class="sxs-lookup"><span data-stu-id="27912-108">[in] A pointer to an array of form information objects that identify the forms for which to return properties.</span></span>
    
 <span data-ttu-id="27912-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="27912-109">_ulFlags_</span></span>
  
> <span data-ttu-id="27912-110">no Uma bitmask de sinalizadores que controla como a matriz de propriedades no parâmetro _ppResults_ é retornada.</span><span class="sxs-lookup"><span data-stu-id="27912-110">[in] A bitmask of flags that controls how the property array in the  _ppResults_ parameter is returned.</span></span> <span data-ttu-id="27912-111">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="27912-111">The following flags can be set:</span></span> 
    
<span data-ttu-id="27912-112">FORMPROPSET_INTERSECTION</span><span class="sxs-lookup"><span data-stu-id="27912-112">FORMPROPSET_INTERSECTION</span></span> 
  
> <span data-ttu-id="27912-113">A matriz retornada contém a interseção das propriedades do formulário.</span><span class="sxs-lookup"><span data-stu-id="27912-113">The returned array contains the intersection of the form's properties.</span></span>
    
<span data-ttu-id="27912-114">FORMPROPSET_UNION</span><span class="sxs-lookup"><span data-stu-id="27912-114">FORMPROPSET_UNION</span></span> 
  
> <span data-ttu-id="27912-115">A matriz retornada contém a União das propriedades do formulário.</span><span class="sxs-lookup"><span data-stu-id="27912-115">The returned array contains the union of the form's properties.</span></span>
    
<span data-ttu-id="27912-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="27912-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="27912-117">As cadeias de caracteres retornadas na matriz estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="27912-117">The strings returned in the array are in Unicode format.</span></span> <span data-ttu-id="27912-118">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="27912-118">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="27912-119">_ppResults_</span><span class="sxs-lookup"><span data-stu-id="27912-119">_ppResults_</span></span>
  
> <span data-ttu-id="27912-120">bota Um ponteiro para um ponteiro para a estrutura [SMAPIFormPropArray](smapiformproparray.md) retornada, que contém as propriedades que os formulários utilizam.</span><span class="sxs-lookup"><span data-stu-id="27912-120">[out] A pointer to a pointer to the returned [SMAPIFormPropArray](smapiformproparray.md) structure, which contains the properties that the forms use.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="27912-121">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="27912-121">Return value</span></span>

<span data-ttu-id="27912-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="27912-122">S_OK</span></span> 
  
> <span data-ttu-id="27912-123">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="27912-123">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="27912-124">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="27912-124">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="27912-125">O sinalizador MAPI_UNICODE foi definido e a implementação não tem suporte para Unicode ou o MAPI_UNICODE não foi definido e a implementação oferece suporte somente a Unicode.</span><span class="sxs-lookup"><span data-stu-id="27912-125">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="27912-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="27912-126">Remarks</span></span>

<span data-ttu-id="27912-127">Os visualizadores de formulários chamam o método **IMAPIFormMgr:: CalcFormPropSet** para obter uma matriz das propriedades usadas por um grupo de formulários.</span><span class="sxs-lookup"><span data-stu-id="27912-127">Form viewers call the **IMAPIFormMgr::CalcFormPropSet** method to obtain an array of the properties that a group of forms uses.</span></span> <span data-ttu-id="27912-128">O **CalcFormPropSet** utiliza uma interseção ou uma União desses conjuntos de propriedades de formulários, dependendo do sinalizador definido no parâmetro _parâmetroulflags_ e retorna uma estrutura **SMAPIFormPropArray** que contém o grupo resultante de Propriedades.</span><span class="sxs-lookup"><span data-stu-id="27912-128">**CalcFormPropSet** takes either an intersection or a union of these forms' property sets, depending on the flag set in the  _ulFlags_ parameter, and it returns an **SMAPIFormPropArray** structure that contains the resulting group of properties.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="27912-129">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="27912-129">Notes to implementers</span></span>

<span data-ttu-id="27912-130">Se um visualizador de formulários passar o sinalizador MAPI_UNICODE no parâmetro _parâmetroulflags_ , todas as cadeias de caracteres deverão ser retornadas como cadeias de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="27912-130">If a form viewer passes the MAPI_UNICODE flag in the  _ulFlags_ parameter, all strings should be returned as Unicode strings.</span></span> <span data-ttu-id="27912-131">Os provedores de biblioteca de formulários que não dão suporte a cadeias de caracteres Unicode devem retornar MAPI_E_BAD_CHARWIDTH se MAPI_UNICODE é passado.</span><span class="sxs-lookup"><span data-stu-id="27912-131">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="27912-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="27912-132">See also</span></span>



[<span data-ttu-id="27912-133">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="27912-133">SMAPIFormPropArray</span></span>](smapiformproparray.md)
  
[<span data-ttu-id="27912-134">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="27912-134">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

