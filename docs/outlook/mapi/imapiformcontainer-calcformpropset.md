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
ms.openlocfilehash: 9c6a6d210230fc305aef46371c22f67b3d445a81
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576579"
---
# <a name="imapiformcontainercalcformpropset"></a><span data-ttu-id="7e07f-103">IMAPIFormContainer::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="7e07f-103">IMAPIFormContainer::CalcFormPropSet</span></span>

  
  
<span data-ttu-id="7e07f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7e07f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7e07f-105">Retorna uma matriz das propriedades usadas por todos os formulários instalados em um contêiner de formulário.</span><span class="sxs-lookup"><span data-stu-id="7e07f-105">Returns an array of the properties used by all forms installed in a form container.</span></span>
  
```cpp
HRESULT CalcFormPropSet(
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a><span data-ttu-id="7e07f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7e07f-106">Parameters</span></span>

 <span data-ttu-id="7e07f-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7e07f-107">_ulFlags_</span></span>
  
> <span data-ttu-id="7e07f-108">[in] Uma bitmask dos sinalizadores que controla como a matriz de propriedade no parâmetro _ppResults_ é retornada.</span><span class="sxs-lookup"><span data-stu-id="7e07f-108">[in] A bitmask of flags that controls how the property array in the  _ppResults_ parameter is returned.</span></span> <span data-ttu-id="7e07f-109">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="7e07f-109">The following flags can be set:</span></span> 
    
<span data-ttu-id="7e07f-110">FORMPROPSET_INTERSECTION</span><span class="sxs-lookup"><span data-stu-id="7e07f-110">FORMPROPSET_INTERSECTION</span></span> 
  
> <span data-ttu-id="7e07f-111">A matriz retornada contém a interseção de propriedades dos formulários.</span><span class="sxs-lookup"><span data-stu-id="7e07f-111">The returned array contains the intersection of the forms' properties.</span></span>
    
<span data-ttu-id="7e07f-112">FORMPROPSET_UNION</span><span class="sxs-lookup"><span data-stu-id="7e07f-112">FORMPROPSET_UNION</span></span> 
  
> <span data-ttu-id="7e07f-113">A matriz retornada contém a união de propriedades dos formulários.</span><span class="sxs-lookup"><span data-stu-id="7e07f-113">The returned array contains the union of the forms' properties.</span></span>
    
<span data-ttu-id="7e07f-114">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7e07f-114">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="7e07f-115">As cadeias de caracteres retornadas na matriz estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="7e07f-115">The strings returned in the array are in Unicode format.</span></span> <span data-ttu-id="7e07f-116">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="7e07f-116">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="7e07f-117">_ppResults_</span><span class="sxs-lookup"><span data-stu-id="7e07f-117">_ppResults_</span></span>
  
> <span data-ttu-id="7e07f-118">[out] Um ponteiro para um ponteiro para a estrutura de [SMAPIFormPropArray](smapiformproparray.md) retornado.</span><span class="sxs-lookup"><span data-stu-id="7e07f-118">[out] A pointer to a pointer to the returned [SMAPIFormPropArray](smapiformproparray.md) structure.</span></span> <span data-ttu-id="7e07f-119">Essa estrutura contém todas as propriedades usadas pelos formulários instalados.</span><span class="sxs-lookup"><span data-stu-id="7e07f-119">This structure contains all properties used by the installed forms.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7e07f-120">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="7e07f-120">Return value</span></span>

<span data-ttu-id="7e07f-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="7e07f-121">S_OK</span></span> 
  
> <span data-ttu-id="7e07f-122">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="7e07f-122">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="7e07f-123">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="7e07f-123">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="7e07f-124">Tanto o sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode, ou MAPI_UNICODE não foi definido e a implementação suporta somente Unicode.</span><span class="sxs-lookup"><span data-stu-id="7e07f-124">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7e07f-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="7e07f-125">Remarks</span></span>

<span data-ttu-id="7e07f-126">Aplicativos cliente chamam o método de **IMAPIFormContainer::CalcFormPropSet** para obter uma matriz de propriedades usadas por todos os formulários instalados em um contêiner de formulário.</span><span class="sxs-lookup"><span data-stu-id="7e07f-126">Client applications call the **IMAPIFormContainer::CalcFormPropSet** method to obtain an array of properties used by all forms installed in a form container.</span></span> <span data-ttu-id="7e07f-127">**IMAPIFormContainer::CalcFormPropSet** funciona como o método [IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md) , exceto que ele opera em todos os formulários registrado em um contêiner específico.</span><span class="sxs-lookup"><span data-stu-id="7e07f-127">**IMAPIFormContainer::CalcFormPropSet** works like the [IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md) method, except that it operates on every form registered in a particular container.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="7e07f-128">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="7e07f-128">Notes to implementers</span></span>

<span data-ttu-id="7e07f-129">Provedores de biblioteca de formulário que não oferecem suporte a cadeias de caracteres Unicode devem retornar MAPI_E_BAD_CHARWIDTH se MAPI_UNICODE é passado.</span><span class="sxs-lookup"><span data-stu-id="7e07f-129">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="7e07f-130">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="7e07f-130">Notes to callers</span></span>

 <span data-ttu-id="7e07f-131">**IMAPIFormContainer::CalcFormPropSet** utiliza uma interseção ou uma união de conjuntos de propriedades dos formulários, dependendo do sinalizador definido no parâmetro _ulFlags_ , e ele retorna uma estrutura **SMAPIFormPropArray** que contém o grupo resultante de propriedades.</span><span class="sxs-lookup"><span data-stu-id="7e07f-131">**IMAPIFormContainer::CalcFormPropSet** takes either an intersection or a union of the forms' property sets, depending on the flag set in the  _ulFlags_ parameter, and it returns an **SMAPIFormPropArray** structure that contains the resulting group of properties.</span></span> 
  
<span data-ttu-id="7e07f-132">Se um cliente passa o sinalizador MAPI_UNICODE em _ulFlags_, todas as cadeias de caracteres retornadas são Unicode.</span><span class="sxs-lookup"><span data-stu-id="7e07f-132">If a client passes the MAPI_UNICODE flag in  _ulFlags_, all returned strings are Unicode.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7e07f-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="7e07f-133">See also</span></span>



[<span data-ttu-id="7e07f-134">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="7e07f-134">IMAPIFormMgr::CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md)
  
[<span data-ttu-id="7e07f-135">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="7e07f-135">SMAPIFormPropArray</span></span>](smapiformproparray.md)
  
[<span data-ttu-id="7e07f-136">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7e07f-136">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)

