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
ms.openlocfilehash: 9947558975098316a547abfaefcdf5e7d4cd2f41
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439006"
---
# <a name="ufromsz"></a><span data-ttu-id="6bc9d-103">UFromSz</span><span class="sxs-lookup"><span data-stu-id="6bc9d-103">UFromSz</span></span>

  
  
<span data-ttu-id="6bc9d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6bc9d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6bc9d-105">Converte uma cadeia de caracteres terminada em nulo de dígitos decimais em um inteiro não assinado.</span><span class="sxs-lookup"><span data-stu-id="6bc9d-105">Converts a null-terminated string of decimal digits into an unsigned integer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6bc9d-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="6bc9d-106">Header file:</span></span>  <br/> |<span data-ttu-id="6bc9d-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6bc9d-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="6bc9d-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="6bc9d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6bc9d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6bc9d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6bc9d-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="6bc9d-110">Called by:</span></span>  <br/> |<span data-ttu-id="6bc9d-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="6bc9d-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
UINT UFromSz(
  LPCSTR lpsz
);
```

## <a name="parameters"></a><span data-ttu-id="6bc9d-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6bc9d-112">Parameters</span></span>

 <span data-ttu-id="6bc9d-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="6bc9d-113">_lpsz_</span></span>
  
> <span data-ttu-id="6bc9d-114">[in] Ponteiro para a cadeia de caracteres terminada por nulo a ser convertida.</span><span class="sxs-lookup"><span data-stu-id="6bc9d-114">[in] Pointer to the null-terminated string to be converted.</span></span> <span data-ttu-id="6bc9d-115">O  _parâmetro lpsz_ não deve exceder 65536 caracteres.</span><span class="sxs-lookup"><span data-stu-id="6bc9d-115">The  _lpsz_ parameter must not exceed 65536 characters.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6bc9d-116">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6bc9d-116">Return value</span></span>

 <span data-ttu-id="6bc9d-117">**UFromSz** retorna um inteiro não assinado.</span><span class="sxs-lookup"><span data-stu-id="6bc9d-117">**UFromSz** returns an unsigned integer.</span></span> <span data-ttu-id="6bc9d-118">Se a cadeia de caracteres não começar com pelo menos um dígito decimal, zero será retornado.</span><span class="sxs-lookup"><span data-stu-id="6bc9d-118">If the string does not begin with at least one decimal digit, zero is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6bc9d-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="6bc9d-119">Remarks</span></span>

<span data-ttu-id="6bc9d-120">A **função UFromSz** para de converter quando atinge o primeiro caractere na cadeia de caracteres que não é um dígito decimal.</span><span class="sxs-lookup"><span data-stu-id="6bc9d-120">The **UFromSz** function stops converting when it reaches the first character in the string that is not a decimal digit.</span></span> <span data-ttu-id="6bc9d-121">Por exemplo, dada a cadeia de caracteres "55", **UFromSz** retorna o valor inteiro 55.</span><span class="sxs-lookup"><span data-stu-id="6bc9d-121">For example, given the string "55", **UFromSz** returns the integer value 55.</span></span> <span data-ttu-id="6bc9d-122">Dada a cadeia de caracteres "5a5b", a função retorna o valor inteiro 5.</span><span class="sxs-lookup"><span data-stu-id="6bc9d-122">Given the string "5a5b", the function returns the integer value 5.</span></span> <span data-ttu-id="6bc9d-123">Dada a cadeia de caracteres "a5b5", **UFromSz** retorna zero.</span><span class="sxs-lookup"><span data-stu-id="6bc9d-123">Given the string "a5b5", **UFromSz** returns zero.</span></span> 
  
 <span data-ttu-id="6bc9d-124">**UFromSz é** sensível a diferenças diacríticas.</span><span class="sxs-lookup"><span data-stu-id="6bc9d-124">**UFromSz** is sensitive to diacritical differences.</span></span> <span data-ttu-id="6bc9d-125">Cadeias de caracteres nos formatos Unicode e DBCS são suportadas.</span><span class="sxs-lookup"><span data-stu-id="6bc9d-125">Strings in the Unicode and DBCS formats are supported.</span></span> <span data-ttu-id="6bc9d-126">O limite de comprimento  _em lpsz_ está em caracteres, não necessariamente bytes.</span><span class="sxs-lookup"><span data-stu-id="6bc9d-126">The length limit on  _lpsz_ is in characters, not necessarily bytes.</span></span> 
  

