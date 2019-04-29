---
title: IMAPIFormContainerCalcFormPropSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.CalcFormPropSet
api_type:
- COM
ms.assetid: 594e3aac-a00f-422e-8e7a-949e4c9a3f8d
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: ec1933f80f211c7c381f9de6b15d414932b9a78e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414911"
---
# <a name="imapiformcontainercalcformpropset"></a><span data-ttu-id="0ed6b-103">IMAPIFormContainer::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="0ed6b-103">IMAPIFormContainer::CalcFormPropSet</span></span>

  
  
<span data-ttu-id="0ed6b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0ed6b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0ed6b-105">Retorna uma matriz das propriedades usadas por todos os formulários instalados em um contêiner de formulários.</span><span class="sxs-lookup"><span data-stu-id="0ed6b-105">Returns an array of the properties used by all forms installed in a form container.</span></span>
  
```cpp
HRESULT CalcFormPropSet(
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a><span data-ttu-id="0ed6b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0ed6b-106">Parameters</span></span>

 <span data-ttu-id="0ed6b-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0ed6b-107">_ulFlags_</span></span>
  
> <span data-ttu-id="0ed6b-108">no Uma bitmask de sinalizadores que controla como a matriz de propriedades no parâmetro _ppResults_ é retornada.</span><span class="sxs-lookup"><span data-stu-id="0ed6b-108">[in] A bitmask of flags that controls how the property array in the  _ppResults_ parameter is returned.</span></span> <span data-ttu-id="0ed6b-109">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="0ed6b-109">The following flags can be set:</span></span> 
    
<span data-ttu-id="0ed6b-110">FORMPROPSET_INTERSECTION</span><span class="sxs-lookup"><span data-stu-id="0ed6b-110">FORMPROPSET_INTERSECTION</span></span> 
  
> <span data-ttu-id="0ed6b-111">A matriz retornada contém a interseção das propriedades de formulários.</span><span class="sxs-lookup"><span data-stu-id="0ed6b-111">The returned array contains the intersection of the forms' properties.</span></span>
    
<span data-ttu-id="0ed6b-112">FORMPROPSET_UNION</span><span class="sxs-lookup"><span data-stu-id="0ed6b-112">FORMPROPSET_UNION</span></span> 
  
> <span data-ttu-id="0ed6b-113">A matriz retornada contém a União das propriedades dos formulários.</span><span class="sxs-lookup"><span data-stu-id="0ed6b-113">The returned array contains the union of the forms' properties.</span></span>
    
<span data-ttu-id="0ed6b-114">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0ed6b-114">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="0ed6b-115">As cadeias de caracteres retornadas na matriz estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="0ed6b-115">The strings returned in the array are in Unicode format.</span></span> <span data-ttu-id="0ed6b-116">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="0ed6b-116">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="0ed6b-117">_ppResults_</span><span class="sxs-lookup"><span data-stu-id="0ed6b-117">_ppResults_</span></span>
  
> <span data-ttu-id="0ed6b-118">bota Um ponteiro para um ponteiro para a estrutura [SMAPIFormPropArray](smapiformproparray.md) retornada.</span><span class="sxs-lookup"><span data-stu-id="0ed6b-118">[out] A pointer to a pointer to the returned [SMAPIFormPropArray](smapiformproparray.md) structure.</span></span> <span data-ttu-id="0ed6b-119">Esta estrutura contém todas as propriedades usadas pelos formulários instalados.</span><span class="sxs-lookup"><span data-stu-id="0ed6b-119">This structure contains all properties used by the installed forms.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0ed6b-120">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="0ed6b-120">Return value</span></span>

<span data-ttu-id="0ed6b-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="0ed6b-121">S_OK</span></span> 
  
> <span data-ttu-id="0ed6b-122">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="0ed6b-122">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="0ed6b-123">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="0ed6b-123">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="0ed6b-124">O sinalizador MAPI_UNICODE foi definido e a implementação não tem suporte para Unicode ou o MAPI_UNICODE não foi definido e a implementação oferece suporte somente a Unicode.</span><span class="sxs-lookup"><span data-stu-id="0ed6b-124">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0ed6b-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="0ed6b-125">Remarks</span></span>

<span data-ttu-id="0ed6b-126">Os aplicativos cliente chamam o método **IMAPIFormContainer:: CalcFormPropSet** para obter uma matriz de propriedades usadas por todos os formulários instalados em um contêiner de formulários.</span><span class="sxs-lookup"><span data-stu-id="0ed6b-126">Client applications call the **IMAPIFormContainer::CalcFormPropSet** method to obtain an array of properties used by all forms installed in a form container.</span></span> <span data-ttu-id="0ed6b-127">**IMAPIFormContainer:: CalcFormPropSet** funciona como o método [IMAPIFormMgr:: CalcFormPropSet](imapiformmgr-calcformpropset.md) , exceto pelo fato de que ele opera em todos os formulários registrados em um contêiner específico.</span><span class="sxs-lookup"><span data-stu-id="0ed6b-127">**IMAPIFormContainer::CalcFormPropSet** works like the [IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md) method, except that it operates on every form registered in a particular container.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="0ed6b-128">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="0ed6b-128">Notes to implementers</span></span>

<span data-ttu-id="0ed6b-129">Os provedores de biblioteca de formulários que não dão suporte a cadeias de caracteres Unicode devem retornar MAPI_E_BAD_CHARWIDTH se MAPI_UNICODE é passado.</span><span class="sxs-lookup"><span data-stu-id="0ed6b-129">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="0ed6b-130">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="0ed6b-130">Notes to callers</span></span>

 <span data-ttu-id="0ed6b-131">**IMAPIFormContainer:: CalcFormPropSet** assume uma interseção ou uma União dos conjuntos de propriedades de formulários, dependendo do sinalizador definido no parâmetro _parâmetroulflags_ e retorna uma estrutura **SMAPIFormPropArray** que contém o grupo resultante de propriedades.</span><span class="sxs-lookup"><span data-stu-id="0ed6b-131">**IMAPIFormContainer::CalcFormPropSet** takes either an intersection or a union of the forms' property sets, depending on the flag set in the  _ulFlags_ parameter, and it returns an **SMAPIFormPropArray** structure that contains the resulting group of properties.</span></span> 
  
<span data-ttu-id="0ed6b-132">Se um cliente passar o sinalizador MAPI_UNICODE no _parâmetroulflags_, todas as cadeias de caracteres retornadas serão Unicode.</span><span class="sxs-lookup"><span data-stu-id="0ed6b-132">If a client passes the MAPI_UNICODE flag in  _ulFlags_, all returned strings are Unicode.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0ed6b-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="0ed6b-133">See also</span></span>



[<span data-ttu-id="0ed6b-134">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="0ed6b-134">IMAPIFormMgr::CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md)
  
[<span data-ttu-id="0ed6b-135">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="0ed6b-135">SMAPIFormPropArray</span></span>](smapiformproparray.md)
  
[<span data-ttu-id="0ed6b-136">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0ed6b-136">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)

