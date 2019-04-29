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
ms.openlocfilehash: ca436bc83d5170d55475c1dd9702a9d54e4b9d5a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436437"
---
# <a name="fbadrglpszw"></a><span data-ttu-id="a089f-103">FBadRglpszW</span><span class="sxs-lookup"><span data-stu-id="a089f-103">FBadRglpszW</span></span>

  
  
<span data-ttu-id="a089f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a089f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a089f-105">Valida todas as cadeias de caracteres em uma matriz de cadeias de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="a089f-105">Validates all strings in an array of Unicode strings.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a089f-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="a089f-106">Header file:</span></span>  <br/> |<span data-ttu-id="a089f-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="a089f-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="a089f-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="a089f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a089f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a089f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a089f-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="a089f-110">Called by:</span></span>  <br/> |<span data-ttu-id="a089f-111">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="a089f-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadRglpszW(
  LPWSTR FAR * lppszW,
  ULONG cStrings
);
```

## <a name="parameters"></a><span data-ttu-id="a089f-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a089f-112">Parameters</span></span>

 <span data-ttu-id="a089f-113">_lppszW_</span><span class="sxs-lookup"><span data-stu-id="a089f-113">_lppszW_</span></span>
  
> <span data-ttu-id="a089f-114">no Ponteiro para uma matriz de cadeias de caracteres Unicode terminadas por caractere nulo.</span><span class="sxs-lookup"><span data-stu-id="a089f-114">[in] Pointer to an array of null-terminated Unicode strings.</span></span> 
    
 <span data-ttu-id="a089f-115">_cStrings_</span><span class="sxs-lookup"><span data-stu-id="a089f-115">_cStrings_</span></span>
  
> <span data-ttu-id="a089f-116">no Contagem de cadeias de caracteres na matriz apontada pelo parâmetro _lppszW_ .</span><span class="sxs-lookup"><span data-stu-id="a089f-116">[in] Count of strings in the array pointed to by the  _lppszW_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a089f-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a089f-117">Return value</span></span>

<span data-ttu-id="a089f-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="a089f-118">TRUE</span></span> 
  
> <span data-ttu-id="a089f-119">Uma ou mais cadeias de caracteres na matriz especificada são inválidas.</span><span class="sxs-lookup"><span data-stu-id="a089f-119">One or more of the strings in the specified array are invalid.</span></span> 
    
<span data-ttu-id="a089f-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="a089f-120">FALSE</span></span> 
  
> <span data-ttu-id="a089f-121">As cadeias de caracteres na matriz especificada são válidas.</span><span class="sxs-lookup"><span data-stu-id="a089f-121">The strings in the specified array are valid.</span></span>
    

