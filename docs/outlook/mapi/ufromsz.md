---
title: UFromSz
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UFromSz
api_type:
- COM
ms.assetid: 4a67faa2-8c2e-49a7-8c92-690a0a65c8f7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5be5cd7c352201159c0257861c0072b56da65082
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770665"
---
# <a name="ufromsz"></a><span data-ttu-id="e48e8-103">UFromSz</span><span class="sxs-lookup"><span data-stu-id="e48e8-103">UFromSz</span></span>

  
  
<span data-ttu-id="e48e8-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e48e8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e48e8-105">Converte uma cadeia de caracteres terminada em nulo de dígitos decimais em um inteiro não assinado.</span><span class="sxs-lookup"><span data-stu-id="e48e8-105">Converts a null-terminated string of decimal digits into an unsigned integer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e48e8-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="e48e8-106">Header file:</span></span>  <br/> |<span data-ttu-id="e48e8-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e48e8-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="e48e8-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="e48e8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e48e8-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e48e8-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e48e8-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="e48e8-110">Called by:</span></span>  <br/> |<span data-ttu-id="e48e8-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="e48e8-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
UINT UFromSz(
  LPCSTR lpsz
);
```

## <a name="parameters"></a><span data-ttu-id="e48e8-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e48e8-112">Parameters</span></span>

 <span data-ttu-id="e48e8-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="e48e8-113">_lpsz_</span></span>
  
> <span data-ttu-id="e48e8-114">[in] Ponteiro para a cadeia de caracteres terminada em nulo a ser convertido.</span><span class="sxs-lookup"><span data-stu-id="e48e8-114">[in] Pointer to the null-terminated string to be converted.</span></span> <span data-ttu-id="e48e8-115">O parâmetro _lpsz_ não deve exceder 65.536 caracteres.</span><span class="sxs-lookup"><span data-stu-id="e48e8-115">The  _lpsz_ parameter must not exceed 65536 characters.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e48e8-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="e48e8-116">Return value</span></span>

 <span data-ttu-id="e48e8-117">**UFromSz** retorna um inteiro não assinado.</span><span class="sxs-lookup"><span data-stu-id="e48e8-117">**UFromSz** returns an unsigned integer.</span></span> <span data-ttu-id="e48e8-118">Se a cadeia de caracteres não começa com pelo menos um dígito decimal, zero será retornado.</span><span class="sxs-lookup"><span data-stu-id="e48e8-118">If the string does not begin with at least one decimal digit, zero is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e48e8-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="e48e8-119">Remarks</span></span>

<span data-ttu-id="e48e8-120">A função **UFromSz** interrompe convertendo quando atingir o primeiro caractere na cadeia de caracteres que não é um dígito decimal.</span><span class="sxs-lookup"><span data-stu-id="e48e8-120">The **UFromSz** function stops converting when it reaches the first character in the string that is not a decimal digit.</span></span> <span data-ttu-id="e48e8-121">Por exemplo, devido a cadeia de caracteres "55", **UFromSz** retorna o valor inteiro 55.</span><span class="sxs-lookup"><span data-stu-id="e48e8-121">For example, given the string "55", **UFromSz** returns the integer value 55.</span></span> <span data-ttu-id="e48e8-122">Considerando a cadeia de caracteres "5a5b", a função retornará o valor de inteiro 5.</span><span class="sxs-lookup"><span data-stu-id="e48e8-122">Given the string "5a5b", the function returns the integer value 5.</span></span> <span data-ttu-id="e48e8-123">Considerando a cadeia de caracteres "a5b5", **UFromSz** retornará zero.</span><span class="sxs-lookup"><span data-stu-id="e48e8-123">Given the string "a5b5", **UFromSz** returns zero.</span></span> 
  
 <span data-ttu-id="e48e8-124">**UFromSz** é sensível diferenças diacríticos.</span><span class="sxs-lookup"><span data-stu-id="e48e8-124">**UFromSz** is sensitive to diacritical differences.</span></span> <span data-ttu-id="e48e8-125">As cadeias de caracteres nos formatos Unicode e DBCS são suportadas.</span><span class="sxs-lookup"><span data-stu-id="e48e8-125">Strings in the Unicode and DBCS formats are supported.</span></span> <span data-ttu-id="e48e8-126">O limite de tamanho em _lpsz_ é em caracteres, não necessariamente bytes.</span><span class="sxs-lookup"><span data-stu-id="e48e8-126">The length limit on  _lpsz_ is in characters, not necessarily bytes.</span></span> 
  

