---
title: SizedDtblButton
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblButton
api_type:
- COM
ms.assetid: ee73ced9-14d8-4a30-9b9f-d54ed9c3a454
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3de56b12fa7d34004fddbfe3633b8b8307c0ffc1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770405"
---
# <a name="sizeddtblbutton"></a><span data-ttu-id="fe625-103">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="fe625-103">SizedDtblButton</span></span>

  
  
<span data-ttu-id="fe625-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fe625-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fe625-105">Cria uma estrutura nomeada que inclui uma estrutura [DTBLBUTTON](dtblbutton.md) para descrever um botão e um rótulo de um comprimento especificado.</span><span class="sxs-lookup"><span data-stu-id="fe625-105">Creates a named structure that includes a [DTBLBUTTON](dtblbutton.md) structure for describing a button and a label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fe625-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="fe625-106">Header file:</span></span>  <br/> |<span data-ttu-id="fe625-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fe625-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="fe625-108">Estrutura relacionada:</span><span class="sxs-lookup"><span data-stu-id="fe625-108">Related structure:</span></span>  <br/> |<span data-ttu-id="fe625-109">**DTBLBUTTON**</span><span class="sxs-lookup"><span data-stu-id="fe625-109">**DTBLBUTTON**</span></span> <br/> |
   
```cpp
SizedDtblButton (n, u)
```

## <a name="parameters"></a><span data-ttu-id="fe625-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fe625-110">Parameters</span></span>

 <span data-ttu-id="fe625-111">_n_</span><span class="sxs-lookup"><span data-stu-id="fe625-111">_n_</span></span>
  
> <span data-ttu-id="fe625-112">Comprimento do rótulo a ser incluído na nova estrutura.</span><span class="sxs-lookup"><span data-stu-id="fe625-112">Length of the label to be included in the new structure.</span></span>
    
 <span data-ttu-id="fe625-113">_u_</span><span class="sxs-lookup"><span data-stu-id="fe625-113">_u_</span></span>
  
> <span data-ttu-id="fe625-114">Nome para a nova estrutura.</span><span class="sxs-lookup"><span data-stu-id="fe625-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fe625-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="fe625-115">Remarks</span></span>

<span data-ttu-id="fe625-116">A nova estrutura é criada com os seguintes membros:</span><span class="sxs-lookup"><span data-stu-id="fe625-116">The new structure is created with the following members:</span></span>
  
```
DTBLBUTTON dtblbutton;
TCHAR lpszLabel[n];

```

## <a name="see-also"></a><span data-ttu-id="fe625-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="fe625-117">See also</span></span>



[<span data-ttu-id="fe625-118">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="fe625-118">DTBLBUTTON</span></span>](dtblbutton.md)


[<span data-ttu-id="fe625-119">Macros relacionadas a estruturas</span><span class="sxs-lookup"><span data-stu-id="fe625-119">Macros Related to Structures</span></span>](macros-related-to-structures.md)

