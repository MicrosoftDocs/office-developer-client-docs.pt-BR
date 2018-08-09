---
title: FBadRglpszW
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRglpszW
api_type:
- COM
ms.assetid: 880eb35d-7045-4fdd-bb33-0f14557a7316
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: da31da0ae0437e1578a681d9232b0693932b2aec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766528"
---
# <a name="fbadrglpszw"></a><span data-ttu-id="0a697-103">FBadRglpszW</span><span class="sxs-lookup"><span data-stu-id="0a697-103">FBadRglpszW</span></span>

  
  
<span data-ttu-id="0a697-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0a697-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0a697-105">Valida todas as cadeias de caracteres em uma matriz de cadeias de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="0a697-105">Validates all strings in an array of Unicode strings.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0a697-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="0a697-106">Header file:</span></span>  <br/> |<span data-ttu-id="0a697-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="0a697-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="0a697-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="0a697-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0a697-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0a697-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0a697-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="0a697-110">Called by:</span></span>  <br/> |<span data-ttu-id="0a697-111">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="0a697-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadRglpszW(
  LPWSTR FAR * lppszW,
  ULONG cStrings
);
```

## <a name="parameters"></a><span data-ttu-id="0a697-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0a697-112">Parameters</span></span>

 <span data-ttu-id="0a697-113">_lppszW_</span><span class="sxs-lookup"><span data-stu-id="0a697-113">_lppszW_</span></span>
  
> <span data-ttu-id="0a697-114">[in] Ponteiro para uma matriz de cadeias de caracteres de Unicode terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="0a697-114">[in] Pointer to an array of null-terminated Unicode strings.</span></span> 
    
 <span data-ttu-id="0a697-115">_cStrings_</span><span class="sxs-lookup"><span data-stu-id="0a697-115">_cStrings_</span></span>
  
> <span data-ttu-id="0a697-116">[in] Contagem de cadeias de caracteres na matriz apontado pelo parâmetro _lppszW_ .</span><span class="sxs-lookup"><span data-stu-id="0a697-116">[in] Count of strings in the array pointed to by the  _lppszW_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0a697-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="0a697-117">Return value</span></span>

<span data-ttu-id="0a697-118">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="0a697-118">TRUE</span></span> 
  
> <span data-ttu-id="0a697-119">Um ou mais das cadeias de caracteres na matriz especificada são inválidos.</span><span class="sxs-lookup"><span data-stu-id="0a697-119">One or more of the strings in the specified array are invalid.</span></span> 
    
<span data-ttu-id="0a697-120">FALSO</span><span class="sxs-lookup"><span data-stu-id="0a697-120">FALSE</span></span> 
  
> <span data-ttu-id="0a697-121">As cadeias de caracteres na matriz especificada são válidas.</span><span class="sxs-lookup"><span data-stu-id="0a697-121">The strings in the specified array are valid.</span></span>
    

