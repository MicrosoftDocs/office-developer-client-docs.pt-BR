---
title: IPropDataHrSetPropAccess
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData.HrSetPropAccess
api_type:
- COM
ms.assetid: 02365050-5e8b-437c-925f-4eb0df646356
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 9e443302e49bad4a586b657a6de298dafbeefab4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437851"
---
# <a name="ipropdatahrsetpropaccess"></a><span data-ttu-id="0e79f-103">IPropData::HrSetPropAccess</span><span class="sxs-lookup"><span data-stu-id="0e79f-103">IPropData::HrSetPropAccess</span></span>

  
  
<span data-ttu-id="0e79f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0e79f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0e79f-105">Define o n�vel de acesso ou o status de uma ou mais das propriedades do objeto.</span><span class="sxs-lookup"><span data-stu-id="0e79f-105">Sets the access level or status for one or more of the object's properties.</span></span>
  
```cpp
HRESULT HrSetPropAccess(
  LPSPropTagArray lpPropTagArray,
  ULONG FAR * rgulAccess
);
```

## <a name="parameters"></a><span data-ttu-id="0e79f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0e79f-106">Parameters</span></span>

 <span data-ttu-id="0e79f-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="0e79f-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="0e79f-108">[in] Um ponteiro para uma matriz de marcas de propriedade que indicam as propriedades a serem modificadas.</span><span class="sxs-lookup"><span data-stu-id="0e79f-108">[in] A pointer to an array of property tags that indicate the properties to be modified.</span></span> 
    
 <span data-ttu-id="0e79f-109">_rgulAccess_</span><span class="sxs-lookup"><span data-stu-id="0e79f-109">_rgulAccess_</span></span>
  
> <span data-ttu-id="0e79f-p101">[in] Uma matriz de m�scaras de bits de sinalizador. Cada bitmask indica os n�veis de acesso ou status ou ambos, para cada uma das propriedades identificadas na matriz que o par�metro  _lpPropTagArray_ aponta para. As duas matrizes s�o posicionais que a primeira bitmask em  _rgulAccess_ descreve a primeira propriedade que aponta de  _lpPropTagArray_ para, e assim por diante. Para cada marca de propriedade, um sinalizador de n�vel de acesso e o sinalizador de status de um pode ser definido. A tabela a seguir mostra os sinalizadores poss�veis.</span><span class="sxs-lookup"><span data-stu-id="0e79f-p101">[in] An array of flag bitmasks. Each bitmask indicates the access levels or status, or both, for each of the properties identified in the array that the  _lpPropTagArray_ parameter points to. The two arrays are positional in that the first bitmask in  _rgulAccess_ describes the first property that  _lpPropTagArray_ points to, and so on. For each property tag, one access-level flag and one status flag can be set. The following table shows the possible flags.</span></span> 
    
|<span data-ttu-id="0e79f-115">**Sinalizador de n�vel de acesso**</span><span class="sxs-lookup"><span data-stu-id="0e79f-115">**Access-level flag**</span></span>|<span data-ttu-id="0e79f-116">**Sinalizador de status**</span><span class="sxs-lookup"><span data-stu-id="0e79f-116">**Status flag**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0e79f-117">IPROP_READONLY, que indica que a propriedade n�o pode ser modificada.</span><span class="sxs-lookup"><span data-stu-id="0e79f-117">IPROP_READONLY, which indicates that the property cannot be modified</span></span>  <br/> |<span data-ttu-id="0e79f-118">IPROP_CLEAN, que indica que a propriedade n�o foi modificada.</span><span class="sxs-lookup"><span data-stu-id="0e79f-118">IPROP_CLEAN, which indicates that the property has not been modified.</span></span>  <br/> |
|<span data-ttu-id="0e79f-119">IPROP_READWRITE, que indica que a propriedade pode ser modificada.</span><span class="sxs-lookup"><span data-stu-id="0e79f-119">IPROP_READWRITE, which indicates that the property can be modified.</span></span>  <br/> |<span data-ttu-id="0e79f-120">IPROP_DIRTY, que indica que a propriedade foi modificada.</span><span class="sxs-lookup"><span data-stu-id="0e79f-120">IPROP_DIRTY, which indicates that the property has been modified.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="0e79f-121">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="0e79f-121">Return value</span></span>

<span data-ttu-id="0e79f-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="0e79f-122">S_OK</span></span> 
  
> <span data-ttu-id="0e79f-123">Os sinalizadores de status e o n�vel de acesso foram definidos com �xito.</span><span class="sxs-lookup"><span data-stu-id="0e79f-123">The access-level and status flags have been successfully set.</span></span>
    
<span data-ttu-id="0e79f-124">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="0e79f-124">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="0e79f-125">Foi feita uma tentativa para definir uma propriedade em um objeto somente leitura ou de um objeto para o qual o chamador tem permiss�es insuficientes.</span><span class="sxs-lookup"><span data-stu-id="0e79f-125">An attempt was made to set a property on a read-only object or an object for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="0e79f-126">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0e79f-126">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="0e79f-127">O par�metro  _rgulAccess_ cont�m uma combina��o de sinalizadores, como IPROP_READONLY e IPROP_READWRITE inv�lida.</span><span class="sxs-lookup"><span data-stu-id="0e79f-127">The  _rgulAccess_ parameter contains an invalid combination of flags, such as IPROP_READONLY and IPROP_READWRITE.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0e79f-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="0e79f-128">Remarks</span></span>

<span data-ttu-id="0e79f-p102">O m�todo **IPropData::HrSetPropAccess** altera o n�vel de acesso e o status para as propriedades que s�o identificados pelas marcas de propriedade na estrutura [SPropTagArray](sproptagarray.md) apontado pelo par�metro  _lpPropTagArray_. Para cada propriedade, h� uma entrada correspondente na matriz  _rgulAccess_. A entrada pode ser definida como um sinalizador que indica o n�vel de acesso da propriedade e outro sinalizador que indica seu status.</span><span class="sxs-lookup"><span data-stu-id="0e79f-p102">The **IPropData::HrSetPropAccess** method changes the access level and status for the properties that are identified by the property tags in the [SPropTagArray](sproptagarray.md) structure pointed to by the  _lpPropTagArray_ parameter. For each property, there is a corresponding entry in the  _rgulAccess_ array. The entry can be set to one flag that indicates the property's access level and another flag that indicates its status.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="0e79f-132">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="0e79f-132">Notes to callers</span></span>

<span data-ttu-id="0e79f-133">Use **HrSetPropAccess** para determinar quando um valor da propriedade espec�fica alterado e alterar o n�vel de acesso para uma ou mais das propriedades de um objeto.</span><span class="sxs-lookup"><span data-stu-id="0e79f-133">Use **HrSetPropAccess** to determine when a particular property value changes and to change the access level for one or more of an object's properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0e79f-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="0e79f-134">See also</span></span>



[<span data-ttu-id="0e79f-135">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="0e79f-135">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="0e79f-136">IPropData: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="0e79f-136">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)

