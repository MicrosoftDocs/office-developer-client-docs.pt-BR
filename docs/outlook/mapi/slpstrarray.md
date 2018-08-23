---
title: SLPSTRArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SLPSTRArray
api_type:
- COM
ms.assetid: 5f570d9b-eb3d-4fc7-bcbe-348a0b8fe9e9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ccad74a9f2553bf29af124821c6d6a87dcde3303
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572869"
---
# <a name="slpstrarray"></a><span data-ttu-id="1df21-103">SLPSTRArray</span><span class="sxs-lookup"><span data-stu-id="1df21-103">SLPSTRArray</span></span>

  
  
<span data-ttu-id="1df21-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1df21-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1df21-105">Contém uma matriz de valores de cadeia de caracteres que são usadas para descrever uma propriedade do tipo PT_MV_STRING8.</span><span class="sxs-lookup"><span data-stu-id="1df21-105">Contains an array of string values that are used to describe a property of type PT_MV_STRING8.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1df21-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="1df21-106">Header file:</span></span>  <br/> |<span data-ttu-id="1df21-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1df21-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SLPSTRArray
{
  ULONG cValues;
  LPSTR FAR *lppszA;
} SLPSTRArray;

```

## <a name="members"></a><span data-ttu-id="1df21-108">Members</span><span class="sxs-lookup"><span data-stu-id="1df21-108">Members</span></span>

 <span data-ttu-id="1df21-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="1df21-109">**cValues**</span></span>
  
> <span data-ttu-id="1df21-110">Contagem de valores na matriz apontado pelo membro **lppszA** .</span><span class="sxs-lookup"><span data-stu-id="1df21-110">Count of values in the array pointed to by the **lppszA** member.</span></span> 
    
 <span data-ttu-id="1df21-111">**lppszA**</span><span class="sxs-lookup"><span data-stu-id="1df21-111">**lppszA**</span></span>
  
> <span data-ttu-id="1df21-112">Ponteiro para uma matriz de cadeias de caracteres de 8 bits terminou de null.</span><span class="sxs-lookup"><span data-stu-id="1df21-112">Pointer to an array of null-ended 8-bit character strings.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1df21-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="1df21-113">Remarks</span></span>

<span data-ttu-id="1df21-114">Para obter mais informações sobre PT_MV_STRING8, consulte a [Lista de tipos de propriedade](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="1df21-114">For more information about PT_MV_STRING8, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1df21-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="1df21-115">See also</span></span>



[<span data-ttu-id="1df21-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="1df21-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="1df21-117">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="1df21-117">MAPI Structures</span></span>](mapi-structures.md)

