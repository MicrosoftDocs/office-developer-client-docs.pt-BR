---
title: IPropDataHrSetObjAccess
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData.HrSetObjAccess
api_type:
- COM
ms.assetid: 01bd3235-22cc-4ff3-b2b6-341ce622128b
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 06cad6e80a2def1c1c3d692a80efeebe0e654a92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767627"
---
# <a name="ipropdatahrsetobjaccess"></a><span data-ttu-id="c6cf9-103">IPropData::HrSetObjAccess</span><span class="sxs-lookup"><span data-stu-id="c6cf9-103">IPropData::HrSetObjAccess</span></span>

  
  
<span data-ttu-id="c6cf9-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c6cf9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c6cf9-105">Define o n�vel de acesso para o objeto.</span><span class="sxs-lookup"><span data-stu-id="c6cf9-105">Sets the access level for the object.</span></span>
  
```cpp
HRESULT HrSetObjAccess(
  ULONG ulAccess
);
```

## <a name="parameters"></a><span data-ttu-id="c6cf9-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="c6cf9-106">Parameters</span></span>

 <span data-ttu-id="c6cf9-107">_ulAccess_</span><span class="sxs-lookup"><span data-stu-id="c6cf9-107">_ulAccess_</span></span>
  
> <span data-ttu-id="c6cf9-p101">[in] Uma bitmask dos sinalizadores que especifica o n�vel de acesso do objeto. Um dos sinalizadores a seguir pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="c6cf9-p101">[in] A bitmask of flags that specifies the object's access level. One of the following flags can be set:</span></span>
    
<span data-ttu-id="c6cf9-110">IPROP_READONLY</span><span class="sxs-lookup"><span data-stu-id="c6cf9-110">IPROP_READONLY</span></span> 
  
> <span data-ttu-id="c6cf9-111">Define o n�vel de acesso do objeto como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="c6cf9-111">Sets the object's access level to read-only.</span></span> 
    
<span data-ttu-id="c6cf9-112">IPROP_READWRITE</span><span class="sxs-lookup"><span data-stu-id="c6cf9-112">IPROP_READWRITE</span></span> 
  
> <span data-ttu-id="c6cf9-113">Define o n�vel de acesso do objeto como leitura/grava��o.</span><span class="sxs-lookup"><span data-stu-id="c6cf9-113">Sets the object's access level to read/write.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c6cf9-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="c6cf9-114">Return value</span></span>

<span data-ttu-id="c6cf9-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="c6cf9-115">S_OK</span></span> 
  
> <span data-ttu-id="c6cf9-116">N�vel de acesso do objeto foi definido com �xito.</span><span class="sxs-lookup"><span data-stu-id="c6cf9-116">The object's access level was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c6cf9-117">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="c6cf9-117">Remarks</span></span>

<span data-ttu-id="c6cf9-p102">O m�todo **IPropData::HrSetObjAccess** define o n�vel de acesso para um objeto inteiro, em vez de propriedades individuais. **HrSetObjAccess** pode ser usado para alterar o n�vel de acesso estabelecido quando o objeto foi criado.</span><span class="sxs-lookup"><span data-stu-id="c6cf9-p102">The **IPropData::HrSetObjAccess** method sets the access level for an entire object, rather than for individual properties. **HrSetObjAccess** can be used to change the access level established when the object was created.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c6cf9-120">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="c6cf9-120">Notes to callers</span></span>

<span data-ttu-id="c6cf9-p103">Para definir um n�vel de acesso em uma propriedade, primeiro chame **HrSetObjAccess** com o sinalizador IPROP_READWRITE definido no par�metro  _ulAccess_ para tornar o objeto pode ser modificado. Em seguida, chame o m�todo de [IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md) , especificando a propriedade de meta na matriz apontada pelo par�metro  _lpPropTagArray_.</span><span class="sxs-lookup"><span data-stu-id="c6cf9-p103">To set an access level on a property, first call **HrSetObjAccess** with the IPROP_READWRITE flag set in the  _ulAccess_ parameter to make the object modifiable. Then call the [IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md) method, specifying the target property in the array pointed to by the  _lpPropTagArray_ parameter.</span></span> 
  
<span data-ttu-id="c6cf9-123">Para criar um objeto com propriedades que ser�o somente leitura para clientes, criar um objeto de leitura/grava��o, adicione as propriedades necess�rias e, em seguida, chame **HrSetObjAccess** para alterar o acesso do objeto como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="c6cf9-123">To create an object with properties that will be read-only to clients, create a read/write object, add the necessary properties, and then call **HrSetObjAccess** to change the object's access to read-only.</span></span> 
  
<span data-ttu-id="c6cf9-124">Voc� tamb�m pode usar **HrSetObjAccess** para impedir que os clientes criem novas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c6cf9-124">You can also use **HrSetObjAccess** to prevent clients from creating new properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c6cf9-125">Ver tamb�m</span><span class="sxs-lookup"><span data-stu-id="c6cf9-125">See also</span></span>



[<span data-ttu-id="c6cf9-126">IPropData::HrGetPropAccess</span><span class="sxs-lookup"><span data-stu-id="c6cf9-126">IPropData::HrGetPropAccess</span></span>](ipropdata-hrgetpropaccess.md)
  
[<span data-ttu-id="c6cf9-127">IPropData::HrSetPropAccess</span><span class="sxs-lookup"><span data-stu-id="c6cf9-127">IPropData::HrSetPropAccess</span></span>](ipropdata-hrsetpropaccess.md)
  
[<span data-ttu-id="c6cf9-128">IPropData: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="c6cf9-128">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)

