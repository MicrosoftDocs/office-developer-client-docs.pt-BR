---
title: SShortArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SShortArray
api_type:
- COM
ms.assetid: 201ceb76-41bc-4d7b-835d-5196bf3dc234
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 59911531b6d8f9c094ef8563510aaa176e3a63b8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770502"
---
# <a name="sshortarray"></a><span data-ttu-id="da3d8-103">SShortArray</span><span class="sxs-lookup"><span data-stu-id="da3d8-103">SShortArray</span></span>

  
  
<span data-ttu-id="da3d8-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="da3d8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="da3d8-105">Contém uma matriz de valores de inteiro não assinado que são usadas para descrever uma propriedade do tipo PT_MV_SHORT.</span><span class="sxs-lookup"><span data-stu-id="da3d8-105">Contains an array of unsigned integer values that are used to describe a property of type PT_MV_SHORT.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="da3d8-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="da3d8-106">Header file:</span></span>  <br/> |<span data-ttu-id="da3d8-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="da3d8-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SShortArray
{
  ULONG cValues;
  short int FAR *lpi;
} SShortArray;

```

## <a name="members"></a><span data-ttu-id="da3d8-108">Members</span><span class="sxs-lookup"><span data-stu-id="da3d8-108">Members</span></span>

 <span data-ttu-id="da3d8-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="da3d8-109">**cValues**</span></span>
  
> <span data-ttu-id="da3d8-110">Contagem de valores na matriz apontado pelo membro **lpi** .</span><span class="sxs-lookup"><span data-stu-id="da3d8-110">Count of values in the array pointed to by the **lpi** member.</span></span> 
    
 <span data-ttu-id="da3d8-111">**lpi**</span><span class="sxs-lookup"><span data-stu-id="da3d8-111">**lpi**</span></span>
  
> <span data-ttu-id="da3d8-112">Ponteiro para uma matriz de valores de inteiro não assinado.</span><span class="sxs-lookup"><span data-stu-id="da3d8-112">Pointer to an array of unsigned integer values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="da3d8-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="da3d8-113">Remarks</span></span>

<span data-ttu-id="da3d8-114">Para obter mais informações sobre PT_MV_SHORT e outros tipos de propriedade, consulte [Tipos de propriedade](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="da3d8-114">For more information about PT_MV_SHORT and other property types, see [Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="da3d8-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="da3d8-115">See also</span></span>



[<span data-ttu-id="da3d8-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="da3d8-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="da3d8-117">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="da3d8-117">MAPI Structures</span></span>](mapi-structures.md)

