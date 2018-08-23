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
ms.openlocfilehash: 1b262ba9c83e9890719f716a373c566be172ae73
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572449"
---
# <a name="scurrencyarray"></a><span data-ttu-id="589d9-103">SCurrencyArray</span><span class="sxs-lookup"><span data-stu-id="589d9-103">SCurrencyArray</span></span>

  
  
<span data-ttu-id="589d9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="589d9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="589d9-105">Contém uma matriz de valores de moeda que são usadas para descrever uma propriedade do tipo PT_MV_CURRENCY.</span><span class="sxs-lookup"><span data-stu-id="589d9-105">Contains an array of currency values that are used to describe a property of type PT_MV_CURRENCY.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="589d9-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="589d9-106">Header file:</span></span>  <br/> |<span data-ttu-id="589d9-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="589d9-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SCurrencyArray
{
  ULONG         cValues;
  CURRENCY FAR *lpcur;
} SCurrencyArray;

```

## <a name="members"></a><span data-ttu-id="589d9-108">Members</span><span class="sxs-lookup"><span data-stu-id="589d9-108">Members</span></span>

 <span data-ttu-id="589d9-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="589d9-109">**cValues**</span></span>
  
> <span data-ttu-id="589d9-110">Contagem de valores na matriz apontado pelo membro **lpcur** .</span><span class="sxs-lookup"><span data-stu-id="589d9-110">Count of values in the array pointed to by the **lpcur** member.</span></span> 
    
 <span data-ttu-id="589d9-111">**lpcur**</span><span class="sxs-lookup"><span data-stu-id="589d9-111">**lpcur**</span></span>
  
> <span data-ttu-id="589d9-112">Ponteiro para uma matriz de estruturas de [moeda](currency.md) que contêm os valores de moeda.</span><span class="sxs-lookup"><span data-stu-id="589d9-112">Pointer to an array of [CURRENCY](currency.md) structures that contain the currency values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="589d9-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="589d9-113">Remarks</span></span>

<span data-ttu-id="589d9-114">Para obter informações sobre PT_MV_CURRENCY, consulte a [Lista de tipos de propriedade](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="589d9-114">For information about PT_MV_CURRENCY, see [List of Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="589d9-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="589d9-115">See also</span></span>



[<span data-ttu-id="589d9-116">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="589d9-116">CURRENCY</span></span>](currency.md)
  
[<span data-ttu-id="589d9-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="589d9-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="589d9-118">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="589d9-118">MAPI Structures</span></span>](mapi-structures.md)

