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
ms.openlocfilehash: 3d20a0932de0fb29ea73e56c37e262c0ccd062c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339211"
---
# <a name="sguidarray"></a><span data-ttu-id="8e1fa-103">SGuidArray</span><span class="sxs-lookup"><span data-stu-id="8e1fa-103">SGuidArray</span></span>

  
  
<span data-ttu-id="8e1fa-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e1fa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8e1fa-105">Contém uma matriz de estruturas [GUID](guid.md) que são usadas para descrever uma propriedade do tipo PT_MV_CLSID.</span><span class="sxs-lookup"><span data-stu-id="8e1fa-105">Contains an array of [GUID](guid.md) structures that are used to describe a property of type PT_MV_CLSID.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8e1fa-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="8e1fa-106">Header file:</span></span>  <br/> |<span data-ttu-id="8e1fa-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="8e1fa-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SGuidArray
{
  ULONG cValues;
  GUID FAR *lpguid;
} SGuidArray;

```

## <a name="members"></a><span data-ttu-id="8e1fa-108">Members</span><span class="sxs-lookup"><span data-stu-id="8e1fa-108">Members</span></span>

 <span data-ttu-id="8e1fa-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="8e1fa-109">**cValues**</span></span>
  
> <span data-ttu-id="8e1fa-110">Contagem de valores na matriz apontada pelo membro **lpguid** .</span><span class="sxs-lookup"><span data-stu-id="8e1fa-110">Count of values in the array pointed to by the **lpguid** member.</span></span> 
    
 <span data-ttu-id="8e1fa-111">**lpguid**</span><span class="sxs-lookup"><span data-stu-id="8e1fa-111">**lpguid**</span></span>
  
> <span data-ttu-id="8e1fa-112">Ponteiro para uma matriz de estruturas **GUID** que contém os valores de identificador de classe.</span><span class="sxs-lookup"><span data-stu-id="8e1fa-112">Pointer to an array of **GUID** structures that contains the class identifier values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8e1fa-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="8e1fa-113">Remarks</span></span>

<span data-ttu-id="8e1fa-114">Para obter mais informações sobre o PT_MV_CLSID, confira [lista de tipos de propriedade](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="8e1fa-114">For more information about PT_MV_CLSID, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8e1fa-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="8e1fa-115">See also</span></span>



[<span data-ttu-id="8e1fa-116">GUID</span><span class="sxs-lookup"><span data-stu-id="8e1fa-116">GUID</span></span>](guid.md)
  
[<span data-ttu-id="8e1fa-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="8e1fa-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="8e1fa-118">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="8e1fa-118">MAPI Structures</span></span>](mapi-structures.md)

