---
title: IPropDataHrGetPropAccess
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData.HrGetPropAccess
api_type:
- COM
ms.assetid: 0101d291-00ca-4f66-b857-75d74b9f91a1
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 8441a4898659a5cd278265cb0199bb9097244aa3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767632"
---
# <a name="ipropdatahrgetpropaccess"></a><span data-ttu-id="26ac5-103">IPropData::HrGetPropAccess</span><span class="sxs-lookup"><span data-stu-id="26ac5-103">IPropData::HrGetPropAccess</span></span>

  
  
<span data-ttu-id="26ac5-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="26ac5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="26ac5-105">Recupera o n�vel de acesso e o status de uma ou mais das propriedades do objeto.</span><span class="sxs-lookup"><span data-stu-id="26ac5-105">Retrieves the access level and status for one or more of the object's properties.</span></span>
  
```cpp
HRESULT HrGetPropAccess(
  LPSPropTagArray FAR * lppPropTagArray,
  ULONG FAR * FAR * lprgulAccess
);
```

## <a name="parameters"></a><span data-ttu-id="26ac5-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="26ac5-106">Parameters</span></span>

 <span data-ttu-id="26ac5-107">_lppPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="26ac5-107">_lppPropTagArray_</span></span>
  
> <span data-ttu-id="26ac5-p101">[al�m, out] Na entrada, uma matriz de marcas de propriedade que indicam as propriedades para o qual recuperar os n�veis de acesso e o status; Caso contr�rio, um ponteiro para nulo, o que indica que **HrGetPropAccess** deve recuperar o status para todas as propriedades e os n�veis de acesso. Na sa�da, uma matriz de marcas de propriedade para a quais sinalizadores de acesso e o status foram recuperadas. Os sinalizadores s�o armazenados na matriz apontada pelo par�metro  _lprgulAccess_.</span><span class="sxs-lookup"><span data-stu-id="26ac5-p101">[in, out] On input, an array of property tags that indicate the properties for which to retrieve access levels and status; otherwise, a pointer to NULL, which indicates that **HrGetPropAccess** should retrieve access levels and status for all properties. On output, an array of property tags for which access and status flags were retrieved. The flags are stored in the array pointed to by the  _lprgulAccess_ parameter.</span></span> 
    
 <span data-ttu-id="26ac5-111">_lprgulAccess_</span><span class="sxs-lookup"><span data-stu-id="26ac5-111">_lprgulAccess_</span></span>
  
> <span data-ttu-id="26ac5-p102">[out] Um ponteiro para uma matriz de m�scaras de bits de sinalizador. Cada bitmask indica os n�veis de acesso ou status ou ambos, para cada uma das propriedades identificadas na matriz apontada pelo par�metro  _lpPropTagArray_. As duas matrizes s�o posicionais que a primeira bitmask que  _lprgulAccess_ aponta para a primeira propriedade descreve o que  _lpPropTagArray_ aponta para, e assim por diante. Para cada marca de propriedade, os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="26ac5-p102">[out] A pointer to an array of flag bitmasks. Each bitmask indicates the access levels or status, or both, for each of the properties identified in the array pointed to by the  _lpPropTagArray_ parameter. The two arrays are positional in that the first bitmask that  _lprgulAccess_ points to describes the first property that  _lpPropTagArray_ points to, and so on. For each property tag, the following flags can be set:</span></span> 
    
|<span data-ttu-id="26ac5-116">**Sinalizador de n�vel de acesso**</span><span class="sxs-lookup"><span data-stu-id="26ac5-116">**Access-level flag**</span></span>|<span data-ttu-id="26ac5-117">**Sinalizador de status**</span><span class="sxs-lookup"><span data-stu-id="26ac5-117">**Status flag**</span></span>|
|:-----|:-----|
|<span data-ttu-id="26ac5-118">IPROP_READONLY, que indica que a propriedade n�o pode ser modificada.</span><span class="sxs-lookup"><span data-stu-id="26ac5-118">IPROP_READONLY, which indicates that the property cannot be modified.</span></span>  <br/> |<span data-ttu-id="26ac5-119">IPROP_CLEAN, que indica que a propriedade n�o foi modificada.</span><span class="sxs-lookup"><span data-stu-id="26ac5-119">IPROP_CLEAN, which indicates that the property has not been modified.</span></span>  <br/> |
|<span data-ttu-id="26ac5-120">IPROP_READWRITE, que indica que a propriedade pode ser modificada.</span><span class="sxs-lookup"><span data-stu-id="26ac5-120">IPROP_READWRITE, which indicates that the property can be modified.</span></span>  <br/> |<span data-ttu-id="26ac5-121">IPROP_DIRTY, que indica que a propriedade foi modificada.</span><span class="sxs-lookup"><span data-stu-id="26ac5-121">IPROP_DIRTY, which indicates that the property has been modified.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="26ac5-122">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="26ac5-122">Return value</span></span>

<span data-ttu-id="26ac5-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="26ac5-123">S_OK</span></span> 
  
> <span data-ttu-id="26ac5-124">Os sinalizadores de status e o n�vel de acesso para as propriedades foram retornados com �xito.</span><span class="sxs-lookup"><span data-stu-id="26ac5-124">The access level and status flags for the properties were successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="26ac5-125">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="26ac5-125">Remarks</span></span>

<span data-ttu-id="26ac5-126">O m�todo **IPropData::HrGetPropAccess** recupera um conjunto de sinalizadores que indica o n�vel de acesso e o status de uma ou mais propriedades.</span><span class="sxs-lookup"><span data-stu-id="26ac5-126">The **IPropData::HrGetPropAccess** method retrieves a set of flags that indicates the access level and status for one or more properties.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="26ac5-127">Observações para chamadores:</span><span class="sxs-lookup"><span data-stu-id="26ac5-127">Notes to callers:</span></span>

<span data-ttu-id="26ac5-128">Voc� pode usar **HrGetPropAccess** para as seguintes finalidades:</span><span class="sxs-lookup"><span data-stu-id="26ac5-128">You can use **HrGetPropAccess** for the following purposes:</span></span> 
  
- <span data-ttu-id="26ac5-129">Para determinar se um cliente alterados ou exclu�dos de uma propriedade grav�vel.</span><span class="sxs-lookup"><span data-stu-id="26ac5-129">To determine whether a client changed or deleted a writable property.</span></span>
    
- <span data-ttu-id="26ac5-130">Para impedir que um cliente de alterar ou excluir uma propriedade usando os m�todos [IMAPIProp](imapipropiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="26ac5-130">To prevent a client from changing or deleting a property by using the [IMAPIProp](imapipropiunknown.md) methods.</span></span> 
    
<span data-ttu-id="26ac5-p103">Se uma das propriedades na propriedade tag matriz apontado pela  _lppPropTagArray_ tiver sido exclu�da, **HrGetPropAccess** define a entrada de matriz como 0 na sa�da. Se voc� definir  _lppPropTagArray_ como NULL, e uma das propriedades do objeto foi exclu�da, a propriedade exclu�da ser� retornada na matriz.</span><span class="sxs-lookup"><span data-stu-id="26ac5-p103">If one of the properties in the property tag array pointed to by  _lppPropTagArray_ has been deleted, **HrGetPropAccess** sets the array entry to 0 on output. If you set  _lppPropTagArray_ to NULL and one of the object's properties has been deleted, the deleted property is returned in the array.</span></span> 
  
<span data-ttu-id="26ac5-p104">Se uma propriedade tiver sido modificada, seu sinalizador IPROP_DIRTY � definido na entrada correspondente na matriz que aponta de  _lprgulAccess_ como. Nem IPROP_READONLY nem IPROP_READWRITE ser� definido.</span><span class="sxs-lookup"><span data-stu-id="26ac5-p104">If a property has been modified, its IPROP_DIRTY flag is set in the corresponding entry in the array that  _lprgulAccess_ points to. Neither IPROP_READONLY nor IPROP_READWRITE will be set.</span></span> 
  
<span data-ttu-id="26ac5-135">Se uma propriedade n�o foi modificada ou exclu�da, somente o sinalizador IPROP_READONLY ou IPROP_READWRITE ser� definido.</span><span class="sxs-lookup"><span data-stu-id="26ac5-135">If a property has not been modified or deleted, only the IPROP_READONLY or IPROP_READWRITE flag will be set.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="26ac5-136">Ver tamb�m</span><span class="sxs-lookup"><span data-stu-id="26ac5-136">See also</span></span>



[<span data-ttu-id="26ac5-137">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="26ac5-137">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="26ac5-138">IPropData: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="26ac5-138">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)

