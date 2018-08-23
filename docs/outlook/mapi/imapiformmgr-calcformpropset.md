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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 5380b6541e609c17a9005c3390c6d5db06155306
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567241"
---
# <a name="imapiformmgrcalcformpropset"></a><span data-ttu-id="a6289-103">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="a6289-103">IMAPIFormMgr::CalcFormPropSet</span></span>

  
  
<span data-ttu-id="a6289-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a6289-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a6289-105">Retorna uma matriz das propriedades que usa um grupo de formulários.</span><span class="sxs-lookup"><span data-stu-id="a6289-105">Returns an array of the properties that a group of forms uses.</span></span>
  
```cpp
HRESULT CalcFormPropSet(
  LPSMAPIFORMINFOARRAY pfrminfoarray,
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a><span data-ttu-id="a6289-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a6289-106">Parameters</span></span>

 <span data-ttu-id="a6289-107">_pfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="a6289-107">_pfrminfoarray_</span></span>
  
> <span data-ttu-id="a6289-108">[in] Um ponteiro para uma matriz de objetos de informações de formulário que identificam os formulários para o qual retornar propriedades.</span><span class="sxs-lookup"><span data-stu-id="a6289-108">[in] A pointer to an array of form information objects that identify the forms for which to return properties.</span></span>
    
 <span data-ttu-id="a6289-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a6289-109">_ulFlags_</span></span>
  
> <span data-ttu-id="a6289-110">[in] Uma bitmask dos sinalizadores que controla como a matriz de propriedade no parâmetro _ppResults_ é retornada.</span><span class="sxs-lookup"><span data-stu-id="a6289-110">[in] A bitmask of flags that controls how the property array in the  _ppResults_ parameter is returned.</span></span> <span data-ttu-id="a6289-111">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="a6289-111">The following flags can be set:</span></span> 
    
<span data-ttu-id="a6289-112">FORMPROPSET_INTERSECTION</span><span class="sxs-lookup"><span data-stu-id="a6289-112">FORMPROPSET_INTERSECTION</span></span> 
  
> <span data-ttu-id="a6289-113">A matriz retornada contém a interseção de propriedades do formulário.</span><span class="sxs-lookup"><span data-stu-id="a6289-113">The returned array contains the intersection of the form's properties.</span></span>
    
<span data-ttu-id="a6289-114">FORMPROPSET_UNION</span><span class="sxs-lookup"><span data-stu-id="a6289-114">FORMPROPSET_UNION</span></span> 
  
> <span data-ttu-id="a6289-115">A matriz retornada contém a união de propriedades do formulário.</span><span class="sxs-lookup"><span data-stu-id="a6289-115">The returned array contains the union of the form's properties.</span></span>
    
<span data-ttu-id="a6289-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a6289-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="a6289-117">As cadeias de caracteres retornadas na matriz estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="a6289-117">The strings returned in the array are in Unicode format.</span></span> <span data-ttu-id="a6289-118">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="a6289-118">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="a6289-119">_ppResults_</span><span class="sxs-lookup"><span data-stu-id="a6289-119">_ppResults_</span></span>
  
> <span data-ttu-id="a6289-120">[out] Um ponteiro para um ponteiro para a estrutura de [SMAPIFormPropArray](smapiformproparray.md) retornado, que contém as propriedades que usam os formulários.</span><span class="sxs-lookup"><span data-stu-id="a6289-120">[out] A pointer to a pointer to the returned [SMAPIFormPropArray](smapiformproparray.md) structure, which contains the properties that the forms use.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a6289-121">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="a6289-121">Return value</span></span>

<span data-ttu-id="a6289-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="a6289-122">S_OK</span></span> 
  
> <span data-ttu-id="a6289-123">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="a6289-123">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="a6289-124">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="a6289-124">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="a6289-125">Tanto o sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode, ou MAPI_UNICODE não foi definido e a implementação suporta somente Unicode.</span><span class="sxs-lookup"><span data-stu-id="a6289-125">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a6289-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6289-126">Remarks</span></span>

<span data-ttu-id="a6289-127">Visualizadores de formulário chamar o método **IMAPIFormMgr::CalcFormPropSet** para obter uma matriz das propriedades que usa um grupo de formulários.</span><span class="sxs-lookup"><span data-stu-id="a6289-127">Form viewers call the **IMAPIFormMgr::CalcFormPropSet** method to obtain an array of the properties that a group of forms uses.</span></span> <span data-ttu-id="a6289-128">**CalcFormPropSet** leva a uma interseção ou uma união de propriedade desses formulários define, dependendo do sinalizador definido no parâmetro _ulFlags_ e ele retorna uma estrutura **SMAPIFormPropArray** que contém o grupo resultante de Propriedades.</span><span class="sxs-lookup"><span data-stu-id="a6289-128">**CalcFormPropSet** takes either an intersection or a union of these forms' property sets, depending on the flag set in the  _ulFlags_ parameter, and it returns an **SMAPIFormPropArray** structure that contains the resulting group of properties.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="a6289-129">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="a6289-129">Notes to implementers</span></span>

<span data-ttu-id="a6289-130">Se um visualizador de formulário passa o sinalizador MAPI_UNICODE no parâmetro _ulFlags_ , todas as cadeias de caracteres devem ser retornadas como sequências de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="a6289-130">If a form viewer passes the MAPI_UNICODE flag in the  _ulFlags_ parameter, all strings should be returned as Unicode strings.</span></span> <span data-ttu-id="a6289-131">Provedores de biblioteca de formulário que não oferecem suporte a cadeias de caracteres Unicode devem retornar MAPI_E_BAD_CHARWIDTH se MAPI_UNICODE é passado.</span><span class="sxs-lookup"><span data-stu-id="a6289-131">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a6289-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="a6289-132">See also</span></span>



[<span data-ttu-id="a6289-133">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="a6289-133">SMAPIFormPropArray</span></span>](smapiformproparray.md)
  
[<span data-ttu-id="a6289-134">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a6289-134">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

