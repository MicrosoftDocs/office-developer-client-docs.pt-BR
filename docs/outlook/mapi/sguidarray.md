---
title: SGuidArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SGuidArray
api_type:
- COM
ms.assetid: 2091e5fc-75c8-4ea4-87e9-a9bf508e9c58
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: bc0ae6d69db6077c17d2efa66d04a5366f2395a0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585567"
---
# <a name="sguidarray"></a><span data-ttu-id="b8a07-103">SGuidArray</span><span class="sxs-lookup"><span data-stu-id="b8a07-103">SGuidArray</span></span>

  
  
<span data-ttu-id="b8a07-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b8a07-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b8a07-105">Contém uma matriz de estruturas [GUID](guid.md) que são usadas para descrever uma propriedade do tipo PT_MV_CLSID.</span><span class="sxs-lookup"><span data-stu-id="b8a07-105">Contains an array of [GUID](guid.md) structures that are used to describe a property of type PT_MV_CLSID.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b8a07-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="b8a07-106">Header file:</span></span>  <br/> |<span data-ttu-id="b8a07-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b8a07-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SGuidArray
{
  ULONG cValues;
  GUID FAR *lpguid;
} SGuidArray;

```

## <a name="members"></a><span data-ttu-id="b8a07-108">Members</span><span class="sxs-lookup"><span data-stu-id="b8a07-108">Members</span></span>

 <span data-ttu-id="b8a07-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="b8a07-109">**cValues**</span></span>
  
> <span data-ttu-id="b8a07-110">Contagem de valores na matriz apontado pelo membro **lpguid** .</span><span class="sxs-lookup"><span data-stu-id="b8a07-110">Count of values in the array pointed to by the **lpguid** member.</span></span> 
    
 <span data-ttu-id="b8a07-111">**lpguid**</span><span class="sxs-lookup"><span data-stu-id="b8a07-111">**lpguid**</span></span>
  
> <span data-ttu-id="b8a07-112">Ponteiro para uma matriz de estruturas **GUID** que contém os valores de identificador de classe.</span><span class="sxs-lookup"><span data-stu-id="b8a07-112">Pointer to an array of **GUID** structures that contains the class identifier values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b8a07-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="b8a07-113">Remarks</span></span>

<span data-ttu-id="b8a07-114">Para obter mais informações sobre PT_MV_CLSID, consulte a [Lista de tipos de propriedade](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="b8a07-114">For more information about PT_MV_CLSID, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b8a07-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="b8a07-115">See also</span></span>



[<span data-ttu-id="b8a07-116">GUID</span><span class="sxs-lookup"><span data-stu-id="b8a07-116">GUID</span></span>](guid.md)
  
[<span data-ttu-id="b8a07-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="b8a07-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="b8a07-118">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="b8a07-118">MAPI Structures</span></span>](mapi-structures.md)

