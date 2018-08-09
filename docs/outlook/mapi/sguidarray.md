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
ms.openlocfilehash: 553ec17e9caf9bf93278ff139eb94e02e6b48554
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19770397"
---
# <a name="sguidarray"></a><span data-ttu-id="0e3f6-103">SGuidArray</span><span class="sxs-lookup"><span data-stu-id="0e3f6-103">SGuidArray</span></span>

  
  
<span data-ttu-id="0e3f6-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0e3f6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0e3f6-105">Contém uma matriz de estruturas [GUID](guid.md) que são usadas para descrever uma propriedade do tipo PT_MV_CLSID.</span><span class="sxs-lookup"><span data-stu-id="0e3f6-105">Contains an array of [GUID](guid.md) structures that are used to describe a property of type PT_MV_CLSID.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0e3f6-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="0e3f6-106">Header file:</span></span>  <br/> |<span data-ttu-id="0e3f6-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0e3f6-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SGuidArray
{
  ULONG cValues;
  GUID FAR *lpguid;
} SGuidArray;

```

## <a name="members"></a><span data-ttu-id="0e3f6-108">Members</span><span class="sxs-lookup"><span data-stu-id="0e3f6-108">Members</span></span>

 <span data-ttu-id="0e3f6-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="0e3f6-109">**cValues**</span></span>
  
> <span data-ttu-id="0e3f6-110">Contagem de valores na matriz apontado pelo membro **lpguid** .</span><span class="sxs-lookup"><span data-stu-id="0e3f6-110">Count of values in the array pointed to by the **lpguid** member.</span></span> 
    
 <span data-ttu-id="0e3f6-111">**lpguid**</span><span class="sxs-lookup"><span data-stu-id="0e3f6-111">**lpguid**</span></span>
  
> <span data-ttu-id="0e3f6-112">Ponteiro para uma matriz de estruturas **GUID** que contém os valores de identificador de classe.</span><span class="sxs-lookup"><span data-stu-id="0e3f6-112">Pointer to an array of **GUID** structures that contains the class identifier values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0e3f6-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="0e3f6-113">Remarks</span></span>

<span data-ttu-id="0e3f6-114">Para obter mais informações sobre PT_MV_CLSID, consulte a [Lista de tipos de propriedade](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="0e3f6-114">For more information about PT_MV_CLSID, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0e3f6-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="0e3f6-115">See also</span></span>



[<span data-ttu-id="0e3f6-116">GUID</span><span class="sxs-lookup"><span data-stu-id="0e3f6-116">GUID</span></span>](guid.md)
  
[<span data-ttu-id="0e3f6-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="0e3f6-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="0e3f6-118">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="0e3f6-118">MAPI Structures</span></span>](mapi-structures.md)

