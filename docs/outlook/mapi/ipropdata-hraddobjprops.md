---
title: IPropDataHrAddObjProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData.HrAddObjProps
api_type:
- COM
ms.assetid: 683cf476-3c02-4b3b-939f-6fff6611f9aa
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: ae0d6d58f96738a9686dbdda86336c040c2e2f68
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591678"
---
# <a name="ipropdatahraddobjprops"></a><span data-ttu-id="e9015-103">IPropData::HrAddObjProps</span><span class="sxs-lookup"><span data-stu-id="e9015-103">IPropData::HrAddObjProps</span></span>

  
  
<span data-ttu-id="e9015-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e9015-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e9015-105">Adiciona uma ou mais propriedades do tipo PT_OBJECT ao objeto.</span><span class="sxs-lookup"><span data-stu-id="e9015-105">Adds one or more properties of type PT_OBJECT to the object.</span></span>
  
```cpp
HRESULT HrAddObjProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="e9015-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="e9015-106">Parameters</span></span>

 <span data-ttu-id="e9015-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="e9015-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="e9015-108">[in] Um ponteiro para uma matriz de marcas de propriedade que indicam as propriedades para adicionar.</span><span class="sxs-lookup"><span data-stu-id="e9015-108">[in] A pointer to an array of property tags that indicate the properties to add.</span></span>
    
 <span data-ttu-id="e9015-109">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="e9015-109">_lppProblems_</span></span>
  
> <span data-ttu-id="e9015-110">[além, out] Na entrada, um ponteiro para uma estrutura [SPropProblemArray](spropproblemarray.md) , válido ou nulo.</span><span class="sxs-lookup"><span data-stu-id="e9015-110">[in, out] On input, a valid pointer to an [SPropProblemArray](spropproblemarray.md) structure, or NULL.</span></span> <span data-ttu-id="e9015-111">Na saída, um ponteiro para um ponteiro para uma estrutura que contém informações sobre propriedades não puderam ser adicionados ou nulo.</span><span class="sxs-lookup"><span data-stu-id="e9015-111">On output, a pointer to a pointer to a structure that contains information about properties that could not be added, or NULL.</span></span> <span data-ttu-id="e9015-112">Um ponteiro para uma estrutura de matriz de problema de propriedade será retornado somente se um ponteiro válido é transmitido em.</span><span class="sxs-lookup"><span data-stu-id="e9015-112">A pointer to a property problem array structure is returned only if a valid pointer is passed in.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e9015-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="e9015-113">Return value</span></span>

<span data-ttu-id="e9015-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="e9015-114">S_OK</span></span> 
  
> <span data-ttu-id="e9015-115">As propriedades foram adicionadas com êxito.</span><span class="sxs-lookup"><span data-stu-id="e9015-115">The properties were successfully added.</span></span>
    
<span data-ttu-id="e9015-116">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="e9015-116">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="e9015-117">Uma propriedade digite diferente de PT_OBJECT foi passado na matriz que o parâmetro _lpPropTagArray_ aponta para.</span><span class="sxs-lookup"><span data-stu-id="e9015-117">A property type other than PT_OBJECT was passed in the array that the  _lpPropTagArray_ parameter points to.</span></span> 
    
<span data-ttu-id="e9015-118">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="e9015-118">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="e9015-119">O objeto tiver sido definido para não permitir a permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="e9015-119">The object has been set not to allow read/write permission.</span></span>
    
<span data-ttu-id="e9015-120">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="e9015-120">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="e9015-121">Alguns, mas não todos, das propriedades foram adicionados.</span><span class="sxs-lookup"><span data-stu-id="e9015-121">Some, but not all, of the properties were added.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e9015-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="e9015-122">Remarks</span></span>

<span data-ttu-id="e9015-123">O método **IPropData::HrAddObjProps** adiciona uma ou mais propriedades do tipo PT_OBJECT ao objeto.</span><span class="sxs-lookup"><span data-stu-id="e9015-123">The **IPropData::HrAddObjProps** method adds one or more properties of type PT_OBJECT to the object.</span></span> <span data-ttu-id="e9015-124">**HrAddObjProps** oferece uma alternativa ao método [IMAPIProp::SetProps](imapiprop-setprops.md) para propriedades de objeto, porque as propriedades de objeto não podem ser criadas chamando **SetProps**.</span><span class="sxs-lookup"><span data-stu-id="e9015-124">**HrAddObjProps** provides an alternative to the [IMAPIProp::SetProps](imapiprop-setprops.md) method for object properties, because object properties cannot be created by calling **SetProps**.</span></span> <span data-ttu-id="e9015-125">Adicionando um resultado de propriedade do objeto na marca de propriedade sejam incluída na lista de marcas de propriedade que o método [IMAPIProp::GetPropList](imapiprop-getproplist.md) retorna.</span><span class="sxs-lookup"><span data-stu-id="e9015-125">Adding an object property results in the property tag being included in the list of property tags that the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method returns.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e9015-126">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="e9015-126">Notes to callers</span></span>

<span data-ttu-id="e9015-127">Se **HrAddObjProps** retorna MAPI_W_PARTIAL_COMPLETION e você tiver definido _lppProblems_ como um ponteiro válido, verifique a estrutura [SPropProblemArray](spropproblemarray.md) retornada para descobrir quais propriedades não foram adicionadas.</span><span class="sxs-lookup"><span data-stu-id="e9015-127">If **HrAddObjProps** returns MAPI_W_PARTIAL_COMPLETION and you have set  _lppProblems_ to a valid pointer, check the returned [SPropProblemArray](spropproblemarray.md) structure to find out which properties were not added.</span></span> <span data-ttu-id="e9015-128">Geralmente, o único problema ocorre é falta de memória.</span><span class="sxs-lookup"><span data-stu-id="e9015-128">Typically, the only problem that occurs is lack of memory.</span></span> <span data-ttu-id="e9015-129">Libere a estrutura **SPropProblemArray** chamando-se a função [MAPIFreeBuffer](mapifreebuffer.md) quando terminar com ele.</span><span class="sxs-lookup"><span data-stu-id="e9015-129">Free the **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function when you are finished with it.</span></span> 
  
<span data-ttu-id="e9015-130">Para adicionar uma propriedade, o objeto de destino deve ter permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="e9015-130">To add a property, the target object must have read/write permission.</span></span> <span data-ttu-id="e9015-131">Se **HrAddObjProps** retornar MAPI_E_NO_ACCESS, você não pode adicionar propriedades para o objeto porque não permite a modificação.</span><span class="sxs-lookup"><span data-stu-id="e9015-131">If **HrAddObjProps** returns MAPI_E_NO_ACCESS, you cannot add properties to the object because it does not permit modification.</span></span> <span data-ttu-id="e9015-132">Para obter a permissão de leitura/gravação para um objeto antes de chamar **HrAddObjProps**, chame [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) e defina o parâmetro _ulAccess_ como IPROP_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="e9015-132">To obtain read/write permission to an object prior to calling **HrAddObjProps**, call [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) and set the  _ulAccess_ parameter to IPROP_READWRITE.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e9015-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="e9015-133">See also</span></span>



[<span data-ttu-id="e9015-134">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="e9015-134">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="e9015-135">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="e9015-135">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="e9015-136">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="e9015-136">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="e9015-137">IPropData: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="e9015-137">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)

