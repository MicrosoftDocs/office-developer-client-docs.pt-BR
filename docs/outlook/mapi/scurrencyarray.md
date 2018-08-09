---
title: SCurrencyArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SCurrencyArray
api_type:
- COM
ms.assetid: d28852ab-b542-40e1-b2ec-85d20a2eddfd
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c440bb7d8f3d2d3002a4d1a80ca3a671b49f4d2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770343"
---
# <a name="scurrencyarray"></a><span data-ttu-id="0c092-103">SCurrencyArray</span><span class="sxs-lookup"><span data-stu-id="0c092-103">SCurrencyArray</span></span>

  
  
<span data-ttu-id="0c092-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0c092-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0c092-105">Contém uma matriz de valores de moeda que são usadas para descrever uma propriedade do tipo PT_MV_CURRENCY.</span><span class="sxs-lookup"><span data-stu-id="0c092-105">Contains an array of currency values that are used to describe a property of type PT_MV_CURRENCY.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0c092-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="0c092-106">Header file:</span></span>  <br/> |<span data-ttu-id="0c092-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0c092-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SCurrencyArray
{
  ULONG         cValues;
  CURRENCY FAR *lpcur;
} SCurrencyArray;

```

## <a name="members"></a><span data-ttu-id="0c092-108">Members</span><span class="sxs-lookup"><span data-stu-id="0c092-108">Members</span></span>

 <span data-ttu-id="0c092-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="0c092-109">**cValues**</span></span>
  
> <span data-ttu-id="0c092-110">Contagem de valores na matriz apontado pelo membro **lpcur** .</span><span class="sxs-lookup"><span data-stu-id="0c092-110">Count of values in the array pointed to by the **lpcur** member.</span></span> 
    
 <span data-ttu-id="0c092-111">**lpcur**</span><span class="sxs-lookup"><span data-stu-id="0c092-111">**lpcur**</span></span>
  
> <span data-ttu-id="0c092-112">Ponteiro para uma matriz de estruturas de [moeda](currency.md) que contêm os valores de moeda.</span><span class="sxs-lookup"><span data-stu-id="0c092-112">Pointer to an array of [CURRENCY](currency.md) structures that contain the currency values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0c092-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="0c092-113">Remarks</span></span>

<span data-ttu-id="0c092-114">Para obter informações sobre PT_MV_CURRENCY, consulte a [Lista de tipos de propriedade](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="0c092-114">For information about PT_MV_CURRENCY, see [List of Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0c092-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="0c092-115">See also</span></span>



[<span data-ttu-id="0c092-116">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="0c092-116">CURRENCY</span></span>](currency.md)
  
[<span data-ttu-id="0c092-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="0c092-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="0c092-118">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="0c092-118">MAPI Structures</span></span>](mapi-structures.md)

