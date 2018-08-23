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
ms.openlocfilehash: 363a85e1c6f111936b16e471eda6b9f962f8b65d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573618"
---
# <a name="sizedsproptagarray"></a><span data-ttu-id="82c85-103">SizedSPropTagArray</span><span class="sxs-lookup"><span data-stu-id="82c85-103">SizedSPropTagArray</span></span>

<span data-ttu-id="82c85-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="82c85-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="82c85-105">Cria uma estrutura [SPropTagArray](sproptagarray.md) nomeada que inclua um número especificado de marcas de propriedade.</span><span class="sxs-lookup"><span data-stu-id="82c85-105">Creates a named [SPropTagArray](sproptagarray.md) structure that includes a specified number of property tags.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="82c85-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="82c85-106">Header file:</span></span>  <br/> |<span data-ttu-id="82c85-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="82c85-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="82c85-108">Estrutura relacionada:</span><span class="sxs-lookup"><span data-stu-id="82c85-108">Related structure:</span></span>  <br/> |<span data-ttu-id="82c85-109">**SPropTagArray**</span><span class="sxs-lookup"><span data-stu-id="82c85-109">**SPropTagArray**</span></span> <br/> |
   
```cpp
SizedSPropTagArray (_ctag, _name)
```

## <a name="parameters"></a><span data-ttu-id="82c85-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="82c85-110">Parameters</span></span>

<span data-ttu-id="82c85-111">__ctag_</span><span class="sxs-lookup"><span data-stu-id="82c85-111">__ctag_</span></span>
  
> <span data-ttu-id="82c85-112">Contagem de marcas de propriedade a ser incluído na nova estrutura.</span><span class="sxs-lookup"><span data-stu-id="82c85-112">Count of property tags to be included in the new structure.</span></span>
    
<span data-ttu-id="82c85-113">__nome_</span><span class="sxs-lookup"><span data-stu-id="82c85-113">__name_</span></span>
  
> <span data-ttu-id="82c85-114">Nome para a nova estrutura.</span><span class="sxs-lookup"><span data-stu-id="82c85-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="82c85-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="82c85-115">Remarks</span></span>

<span data-ttu-id="82c85-116">Use a macro **SizedSPropTagArray** para criar uma matriz de marca de propriedade com limites explícitos.</span><span class="sxs-lookup"><span data-stu-id="82c85-116">Use the **SizedSPropTagArray** macro to create a property tag array with explicit bounds.</span></span> 
  
<span data-ttu-id="82c85-117">Para usar a nova estrutura que é resultado da macro **SizedSPropTagArray** como um ponteiro para uma estrutura **SPropTagArray** , execute a seguinte projeção:</span><span class="sxs-lookup"><span data-stu-id="82c85-117">To use the new structure that results from the **SizedSPropTagArray** macro as a pointer to an **SPropTagArray** structure, perform the following cast:</span></span> 
  
```cpp
lpPropTagArray = (LPPropTagArray) &SizedSPropTagArray;

```

## <a name="see-also"></a><span data-ttu-id="82c85-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="82c85-118">See also</span></span>

- [<span data-ttu-id="82c85-119">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="82c85-119">SPropTagArray</span></span>](sproptagarray.md)
- [<span data-ttu-id="82c85-120">Macros relacionadas a estruturas</span><span class="sxs-lookup"><span data-stu-id="82c85-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)

