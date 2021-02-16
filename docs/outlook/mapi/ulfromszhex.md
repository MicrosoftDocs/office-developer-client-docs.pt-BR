---
title: UlFromSzHex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlFromSzHex
api_type:
- COM
ms.assetid: e2d6b6bf-f96d-460c-859a-21961ac9237c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 950f5513696a9dd9d52db7b7ee912d3f7d12cc48
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433049"
---
# <a name="ulfromszhex"></a><span data-ttu-id="a7e05-103">UlFromSzHex</span><span class="sxs-lookup"><span data-stu-id="a7e05-103">UlFromSzHex</span></span>

  
  
<span data-ttu-id="a7e05-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a7e05-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a7e05-105">Converte uma cadeia de caracteres terminada em nulo de dígitos hexadecimais em um inteiro longo não assinado.</span><span class="sxs-lookup"><span data-stu-id="a7e05-105">Converts a null-terminated string of hexadecimal digits into an unsigned long integer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a7e05-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="a7e05-106">Header file:</span></span>  <br/> |<span data-ttu-id="a7e05-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a7e05-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="a7e05-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="a7e05-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a7e05-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a7e05-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a7e05-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="a7e05-110">Called by:</span></span>  <br/> |<span data-ttu-id="a7e05-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="a7e05-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlFromSzHex(
LPCSTR lpsz
);
```

## <a name="parameters"></a><span data-ttu-id="a7e05-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a7e05-112">Parameters</span></span>

 <span data-ttu-id="a7e05-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="a7e05-113">_lpsz_</span></span>
  
> <span data-ttu-id="a7e05-114">[in] Ponteiro para a cadeia de caracteres terminada em nulo a ser convertida.</span><span class="sxs-lookup"><span data-stu-id="a7e05-114">[in] Pointer to the null-terminated string to be converted.</span></span> <span data-ttu-id="a7e05-115">O  _parâmetro lpsz_ não deve exceder 65536 caracteres.</span><span class="sxs-lookup"><span data-stu-id="a7e05-115">The  _lpsz_ parameter must not exceed 65536 characters.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a7e05-116">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a7e05-116">Return value</span></span>

 <span data-ttu-id="a7e05-117">**UlFromSzHex** retorna um inteiro longo não assinado.</span><span class="sxs-lookup"><span data-stu-id="a7e05-117">**UlFromSzHex** returns an unsigned long integer.</span></span> <span data-ttu-id="a7e05-118">Se a cadeia de caracteres não começar com pelo menos um dígito hexadecimal, zero será retornado.</span><span class="sxs-lookup"><span data-stu-id="a7e05-118">If the string does not begin with at least one hexadecimal digit, zero is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a7e05-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="a7e05-119">Remarks</span></span>

<span data-ttu-id="a7e05-120">A **função UlFromSzHex** para de converter quando atinge o primeiro caractere na cadeia de caracteres que não é um dígito hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="a7e05-120">The **UlFromSzHex** function stops converting when it reaches the first character in the string that is not a hexadecimal digit.</span></span> <span data-ttu-id="a7e05-121">Por exemplo, dada a cadeia de caracteres "5a", **UlFromSzHex** retorna o valor inteiro 90.</span><span class="sxs-lookup"><span data-stu-id="a7e05-121">For example, given the string "5a", **UlFromSzHex** returns the integer value 90.</span></span> <span data-ttu-id="a7e05-122">Dada a cadeia de caracteres "5g5h", a função retorna o valor inteiro 5.</span><span class="sxs-lookup"><span data-stu-id="a7e05-122">Given the string "5g5h", the function returns the integer value 5.</span></span> <span data-ttu-id="a7e05-123">Dada a cadeia de caracteres "g5h5", **UlFromSzHex** retorna zero.</span><span class="sxs-lookup"><span data-stu-id="a7e05-123">Given the string "g5h5", **UlFromSzHex** returns zero.</span></span> 
  
 <span data-ttu-id="a7e05-124">**UlFromSzHex** é sensível a diferenças diacríticas, mas permite 'a' até 'f' e 'A' até 'F' para dígitos hexadecimais.</span><span class="sxs-lookup"><span data-stu-id="a7e05-124">**UlFromSzHex** is sensitive to diacritical differences but allows both 'a' through 'f' and 'A' through 'F' for hexadecimal digits.</span></span> <span data-ttu-id="a7e05-125">Cadeias de caracteres nos formatos Unicode e DBCS são suportadas.</span><span class="sxs-lookup"><span data-stu-id="a7e05-125">Strings in the Unicode and DBCS formats are supported.</span></span> <span data-ttu-id="a7e05-126">O limite de comprimento  _em lpsz_ está em caracteres, não necessariamente bytes.</span><span class="sxs-lookup"><span data-stu-id="a7e05-126">The length limit on  _lpsz_ is in characters, not necessarily bytes.</span></span> 
  

