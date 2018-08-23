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
ms.openlocfilehash: a8f4e62a8eb1b5e61cb0223c66b921e15ab9423b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577678"
---
# <a name="spropattrarray"></a><span data-ttu-id="64ace-103">SPropAttrArray</span><span class="sxs-lookup"><span data-stu-id="64ace-103">SPropAttrArray</span></span>

  
  
<span data-ttu-id="64ace-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="64ace-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="64ace-105">Contém uma lista de atributos para propriedades de um objeto.</span><span class="sxs-lookup"><span data-stu-id="64ace-105">Contains a list of attributes for properties of an object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="64ace-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="64ace-106">Header file:</span></span>  <br/> |<span data-ttu-id="64ace-107">IMessage.h</span><span class="sxs-lookup"><span data-stu-id="64ace-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="64ace-108">Macros relacionadas:</span><span class="sxs-lookup"><span data-stu-id="64ace-108">Related macros:</span></span>  <br/> |<span data-ttu-id="64ace-109">[CbNewSPropAttrArray](cbnewspropattrarray.md), [CbSPropAttrArray](cbspropattrarray.md)</span><span class="sxs-lookup"><span data-stu-id="64ace-109">[CbNewSPropAttrArray](cbnewspropattrarray.md), [CbSPropAttrArray](cbspropattrarray.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cValues;
  ULONG aPropAttr[MAPI_DIM];
} SPropAttrArray, FAR *LPSPropAttrArray;

```

## <a name="members"></a><span data-ttu-id="64ace-110">Members</span><span class="sxs-lookup"><span data-stu-id="64ace-110">Members</span></span>

 <span data-ttu-id="64ace-111">**cValues**</span><span class="sxs-lookup"><span data-stu-id="64ace-111">**cValues**</span></span>
  
> <span data-ttu-id="64ace-112">Contagem de atributos de propriedade no membro **aPropAttr** .</span><span class="sxs-lookup"><span data-stu-id="64ace-112">Count of property attributes in the **aPropAttr** member.</span></span> 
    
 <span data-ttu-id="64ace-113">**aPropAttr**</span><span class="sxs-lookup"><span data-stu-id="64ace-113">**aPropAttr**</span></span>
  
> <span data-ttu-id="64ace-114">Uma matriz de atributos de propriedade.</span><span class="sxs-lookup"><span data-stu-id="64ace-114">An array of property attributes.</span></span> <span data-ttu-id="64ace-115">Os valores válidos para os atributos são:</span><span class="sxs-lookup"><span data-stu-id="64ace-115">Valid values for attributes are as follows:</span></span>
    
    - <span data-ttu-id="64ace-116">PROPATTR_MANDATORY</span><span class="sxs-lookup"><span data-stu-id="64ace-116">PROPATTR_MANDATORY</span></span>
    
    - <span data-ttu-id="64ace-117">PROPATTR_READABLE</span><span class="sxs-lookup"><span data-stu-id="64ace-117">PROPATTR_READABLE</span></span>
    
    - <span data-ttu-id="64ace-118">PROPATTR_WRITEABLE</span><span class="sxs-lookup"><span data-stu-id="64ace-118">PROPATTR_WRITEABLE</span></span>
    
    - <span data-ttu-id="64ace-119">PROPATTR_NOT_PRESENT</span><span class="sxs-lookup"><span data-stu-id="64ace-119">PROPATTR_NOT_PRESENT</span></span>
    
## <a name="remarks"></a><span data-ttu-id="64ace-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="64ace-120">Remarks</span></span>

<span data-ttu-id="64ace-121">A estrutura **SPropAttrArray** é utilizada pelos objetos de dados de propriedade que implementam o [IPropData: IMAPIProp](ipropdataimapiprop.md) interface.</span><span class="sxs-lookup"><span data-stu-id="64ace-121">The **SPropAttrArray** structure is used by property data objects that implement the [IPropData : IMAPIProp](ipropdataimapiprop.md) interface.</span></span> <span data-ttu-id="64ace-122">Ele também é usado pela implementação do MAPI do [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) ou seja com base no armazenamento estruturado.</span><span class="sxs-lookup"><span data-stu-id="64ace-122">It is also used by MAPI's implementation of [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) that is based on structured storage.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="64ace-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="64ace-123">See also</span></span>



[<span data-ttu-id="64ace-124">IPropData: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="64ace-124">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)
  
[<span data-ttu-id="64ace-125">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="64ace-125">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)
  
[<span data-ttu-id="64ace-126">CbNewSPropAttrArray</span><span class="sxs-lookup"><span data-stu-id="64ace-126">CbNewSPropAttrArray</span></span>](cbnewspropattrarray.md)
  
[<span data-ttu-id="64ace-127">CbSPropAttrArray</span><span class="sxs-lookup"><span data-stu-id="64ace-127">CbSPropAttrArray</span></span>](cbspropattrarray.md)


[<span data-ttu-id="64ace-128">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="64ace-128">MAPI Structures</span></span>](mapi-structures.md)

