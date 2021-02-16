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
ms.openlocfilehash: e9468d0c7fc7e46475afe19f12f225e53196639e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439398"
---
# <a name="scurrencyarray"></a><span data-ttu-id="9efbf-103">SCurrencyArray</span><span class="sxs-lookup"><span data-stu-id="9efbf-103">SCurrencyArray</span></span>

  
  
<span data-ttu-id="9efbf-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9efbf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9efbf-105">Contém uma matriz de valores de moeda que são usados para descrever uma propriedade do tipo PT_MV_CURRENCY.</span><span class="sxs-lookup"><span data-stu-id="9efbf-105">Contains an array of currency values that are used to describe a property of type PT_MV_CURRENCY.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9efbf-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="9efbf-106">Header file:</span></span>  <br/> |<span data-ttu-id="9efbf-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9efbf-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SCurrencyArray
{
  ULONG         cValues;
  CURRENCY FAR *lpcur;
} SCurrencyArray;

```

## <a name="members"></a><span data-ttu-id="9efbf-108">Members</span><span class="sxs-lookup"><span data-stu-id="9efbf-108">Members</span></span>

 <span data-ttu-id="9efbf-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="9efbf-109">**cValues**</span></span>
  
> <span data-ttu-id="9efbf-110">Contagem de valores na matriz apontada pelo membro **lpcur.**</span><span class="sxs-lookup"><span data-stu-id="9efbf-110">Count of values in the array pointed to by the **lpcur** member.</span></span> 
    
 <span data-ttu-id="9efbf-111">**lpcur**</span><span class="sxs-lookup"><span data-stu-id="9efbf-111">**lpcur**</span></span>
  
> <span data-ttu-id="9efbf-112">Ponteiro para uma matriz de [estruturas CURRENCY](currency.md) que contêm os valores de moeda.</span><span class="sxs-lookup"><span data-stu-id="9efbf-112">Pointer to an array of [CURRENCY](currency.md) structures that contain the currency values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="9efbf-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="9efbf-113">Remarks</span></span>

<span data-ttu-id="9efbf-114">Para obter informações sobre PT_MV_CURRENCY, consulte [Lista de tipos de propriedade.](property-types.md)</span><span class="sxs-lookup"><span data-stu-id="9efbf-114">For information about PT_MV_CURRENCY, see [List of Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9efbf-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="9efbf-115">See also</span></span>



[<span data-ttu-id="9efbf-116">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="9efbf-116">CURRENCY</span></span>](currency.md)
  
[<span data-ttu-id="9efbf-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="9efbf-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="9efbf-118">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="9efbf-118">MAPI Structures</span></span>](mapi-structures.md)

