---
title: SizedSPropTagArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSPropTagArray
api_type:
- COM
ms.assetid: 1d2dc6e9-735d-4b5b-af6f-adf6a32a666d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7505c5dbcfc98a8b868424ae51cbe9c47b1d4338
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770422"
---
# <a name="sizedsproptagarray"></a><span data-ttu-id="09c1c-103">SizedSPropTagArray</span><span class="sxs-lookup"><span data-stu-id="09c1c-103">SizedSPropTagArray</span></span>

<span data-ttu-id="09c1c-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="09c1c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="09c1c-105">Cria uma estrutura [SPropTagArray](sproptagarray.md) nomeada que inclua um número especificado de marcas de propriedade.</span><span class="sxs-lookup"><span data-stu-id="09c1c-105">Creates a named [SPropTagArray](sproptagarray.md) structure that includes a specified number of property tags.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="09c1c-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="09c1c-106">Header file:</span></span>  <br/> |<span data-ttu-id="09c1c-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="09c1c-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="09c1c-108">Estrutura relacionada:</span><span class="sxs-lookup"><span data-stu-id="09c1c-108">Related structure:</span></span>  <br/> |<span data-ttu-id="09c1c-109">**SPropTagArray**</span><span class="sxs-lookup"><span data-stu-id="09c1c-109">**SPropTagArray**</span></span> <br/> |
   
```cpp
SizedSPropTagArray (_ctag, _name)
```

## <a name="parameters"></a><span data-ttu-id="09c1c-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="09c1c-110">Parameters</span></span>

<span data-ttu-id="09c1c-111">__ctag_</span><span class="sxs-lookup"><span data-stu-id="09c1c-111">__ctag_</span></span>
  
> <span data-ttu-id="09c1c-112">Contagem de marcas de propriedade a ser incluído na nova estrutura.</span><span class="sxs-lookup"><span data-stu-id="09c1c-112">Count of property tags to be included in the new structure.</span></span>
    
<span data-ttu-id="09c1c-113">__nome_</span><span class="sxs-lookup"><span data-stu-id="09c1c-113">__name_</span></span>
  
> <span data-ttu-id="09c1c-114">Nome para a nova estrutura.</span><span class="sxs-lookup"><span data-stu-id="09c1c-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="09c1c-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="09c1c-115">Remarks</span></span>

<span data-ttu-id="09c1c-116">Use a macro **SizedSPropTagArray** para criar uma matriz de marca de propriedade com limites explícitos.</span><span class="sxs-lookup"><span data-stu-id="09c1c-116">Use the **SizedSPropTagArray** macro to create a property tag array with explicit bounds.</span></span> 
  
<span data-ttu-id="09c1c-117">Para usar a nova estrutura que é resultado da macro **SizedSPropTagArray** como um ponteiro para uma estrutura **SPropTagArray** , execute a seguinte projeção:</span><span class="sxs-lookup"><span data-stu-id="09c1c-117">To use the new structure that results from the **SizedSPropTagArray** macro as a pointer to an **SPropTagArray** structure, perform the following cast:</span></span> 
  
```cpp
lpPropTagArray = (LPPropTagArray) &SizedSPropTagArray;

```

## <a name="see-also"></a><span data-ttu-id="09c1c-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="09c1c-118">See also</span></span>

- [<span data-ttu-id="09c1c-119">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="09c1c-119">SPropTagArray</span></span>](sproptagarray.md)
- [<span data-ttu-id="09c1c-120">Macros relacionadas a estruturas</span><span class="sxs-lookup"><span data-stu-id="09c1c-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)

