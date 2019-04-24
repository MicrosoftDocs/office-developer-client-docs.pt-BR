---
title: SPropAttrArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropAttrArray
api_type:
- COM
ms.assetid: 30dd19d9-0840-49e9-aec6-ec8d19b1f91d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 55cba4f7cfb3fa8035117348b10ab1d6d3082710
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358111"
---
# <a name="spropattrarray"></a><span data-ttu-id="15aff-103">SPropAttrArray</span><span class="sxs-lookup"><span data-stu-id="15aff-103">SPropAttrArray</span></span>

  
  
<span data-ttu-id="15aff-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="15aff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="15aff-105">Contém uma lista de atributos para propriedades de um objeto.</span><span class="sxs-lookup"><span data-stu-id="15aff-105">Contains a list of attributes for properties of an object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="15aff-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="15aff-106">Header file:</span></span>  <br/> |<span data-ttu-id="15aff-107">IMessage. h</span><span class="sxs-lookup"><span data-stu-id="15aff-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="15aff-108">Macros relacionadas:</span><span class="sxs-lookup"><span data-stu-id="15aff-108">Related macros:</span></span>  <br/> |<span data-ttu-id="15aff-109">[CbNewSPropAttrArray](cbnewspropattrarray.md), [CbSPropAttrArray](cbspropattrarray.md)</span><span class="sxs-lookup"><span data-stu-id="15aff-109">[CbNewSPropAttrArray](cbnewspropattrarray.md), [CbSPropAttrArray](cbspropattrarray.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cValues;
  ULONG aPropAttr[MAPI_DIM];
} SPropAttrArray, FAR *LPSPropAttrArray;

```

## <a name="members"></a><span data-ttu-id="15aff-110">Members</span><span class="sxs-lookup"><span data-stu-id="15aff-110">Members</span></span>

 <span data-ttu-id="15aff-111">**cValues**</span><span class="sxs-lookup"><span data-stu-id="15aff-111">**cValues**</span></span>
  
> <span data-ttu-id="15aff-112">Contagem de atributos de propriedade no membro **aPropAttr** .</span><span class="sxs-lookup"><span data-stu-id="15aff-112">Count of property attributes in the **aPropAttr** member.</span></span> 
    
 <span data-ttu-id="15aff-113">**aPropAttr**</span><span class="sxs-lookup"><span data-stu-id="15aff-113">**aPropAttr**</span></span>
  
> <span data-ttu-id="15aff-114">Uma matriz de atributos de propriedade.</span><span class="sxs-lookup"><span data-stu-id="15aff-114">An array of property attributes.</span></span> <span data-ttu-id="15aff-115">Os valores válidos para atributos são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="15aff-115">Valid values for attributes are as follows:</span></span>
    
    - <span data-ttu-id="15aff-116">PROPATTR_MANDATORY</span><span class="sxs-lookup"><span data-stu-id="15aff-116">PROPATTR_MANDATORY</span></span>
    
    - <span data-ttu-id="15aff-117">PROPATTR_READABLE</span><span class="sxs-lookup"><span data-stu-id="15aff-117">PROPATTR_READABLE</span></span>
    
    - <span data-ttu-id="15aff-118">PROPATTR_WRITEABLE</span><span class="sxs-lookup"><span data-stu-id="15aff-118">PROPATTR_WRITEABLE</span></span>
    
    - <span data-ttu-id="15aff-119">PROPATTR_NOT_PRESENT</span><span class="sxs-lookup"><span data-stu-id="15aff-119">PROPATTR_NOT_PRESENT</span></span>
    
## <a name="remarks"></a><span data-ttu-id="15aff-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="15aff-120">Remarks</span></span>

<span data-ttu-id="15aff-121">A estrutura **SPropAttrArray** é usada por objetos de dados de propriedade que implementam a interface [IPropData: IMAPIProp](ipropdataimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="15aff-121">The **SPropAttrArray** structure is used by property data objects that implement the [IPropData : IMAPIProp](ipropdataimapiprop.md) interface.</span></span> <span data-ttu-id="15aff-122">Ele também é usado pela implementação de MAPI do [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) que se baseia no armazenamento estruturado.</span><span class="sxs-lookup"><span data-stu-id="15aff-122">It is also used by MAPI's implementation of [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) that is based on structured storage.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="15aff-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="15aff-123">See also</span></span>



[<span data-ttu-id="15aff-124">IPropData: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="15aff-124">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)
  
[<span data-ttu-id="15aff-125">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="15aff-125">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)
  
[<span data-ttu-id="15aff-126">CbNewSPropAttrArray</span><span class="sxs-lookup"><span data-stu-id="15aff-126">CbNewSPropAttrArray</span></span>](cbnewspropattrarray.md)
  
[<span data-ttu-id="15aff-127">CbSPropAttrArray</span><span class="sxs-lookup"><span data-stu-id="15aff-127">CbSPropAttrArray</span></span>](cbspropattrarray.md)


[<span data-ttu-id="15aff-128">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="15aff-128">MAPI Structures</span></span>](mapi-structures.md)

