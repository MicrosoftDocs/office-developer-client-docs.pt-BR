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
ms.openlocfilehash: d5ba7e7bc52ba041e9fe6c9a01b35dc91d3b947b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770655"
---
# <a name="ulfromszhex"></a><span data-ttu-id="ada37-103">UlFromSzHex</span><span class="sxs-lookup"><span data-stu-id="ada37-103">UlFromSzHex</span></span>

  
  
<span data-ttu-id="ada37-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ada37-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ada37-105">Converte uma cadeia de caracteres terminada em nulo de dígitos hexadecimais em um inteiro não assinado de longo.</span><span class="sxs-lookup"><span data-stu-id="ada37-105">Converts a null-terminated string of hexadecimal digits into an unsigned long integer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ada37-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="ada37-106">Header file:</span></span>  <br/> |<span data-ttu-id="ada37-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ada37-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="ada37-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="ada37-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ada37-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ada37-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ada37-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="ada37-110">Called by:</span></span>  <br/> |<span data-ttu-id="ada37-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="ada37-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlFromSzHex(
LPCSTR lpsz
);
```

## <a name="parameters"></a><span data-ttu-id="ada37-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ada37-112">Parameters</span></span>

 <span data-ttu-id="ada37-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="ada37-113">_lpsz_</span></span>
  
> <span data-ttu-id="ada37-114">[in] Ponteiro para a cadeia de caracteres terminada em nulo a ser convertido.</span><span class="sxs-lookup"><span data-stu-id="ada37-114">[in] Pointer to the null-terminated string to be converted.</span></span> <span data-ttu-id="ada37-115">O parâmetro _lpsz_ não deve exceder 65.536 caracteres.</span><span class="sxs-lookup"><span data-stu-id="ada37-115">The  _lpsz_ parameter must not exceed 65536 characters.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ada37-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="ada37-116">Return value</span></span>

 <span data-ttu-id="ada37-117">**UlFromSzHex** retorna um inteiro longo não assinado.</span><span class="sxs-lookup"><span data-stu-id="ada37-117">**UlFromSzHex** returns an unsigned long integer.</span></span> <span data-ttu-id="ada37-118">Se a cadeia de caracteres não começa com pelo menos um dígito hexadecimal, zero será retornado.</span><span class="sxs-lookup"><span data-stu-id="ada37-118">If the string does not begin with at least one hexadecimal digit, zero is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ada37-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="ada37-119">Remarks</span></span>

<span data-ttu-id="ada37-120">A função **UlFromSzHex** interrompe convertendo quando atingir o primeiro caractere na cadeia de caracteres que não é um dígito hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="ada37-120">The **UlFromSzHex** function stops converting when it reaches the first character in the string that is not a hexadecimal digit.</span></span> <span data-ttu-id="ada37-121">Por exemplo, devido a cadeia de caracteres "5a", **UlFromSzHex** retorna o valor inteiro 90.</span><span class="sxs-lookup"><span data-stu-id="ada37-121">For example, given the string "5a", **UlFromSzHex** returns the integer value 90.</span></span> <span data-ttu-id="ada37-122">Considerando a cadeia de caracteres "5g5h", a função retornará o valor de inteiro 5.</span><span class="sxs-lookup"><span data-stu-id="ada37-122">Given the string "5g5h", the function returns the integer value 5.</span></span> <span data-ttu-id="ada37-123">Considerando a cadeia de caracteres "g5h5", **UlFromSzHex** retornará zero.</span><span class="sxs-lookup"><span data-stu-id="ada37-123">Given the string "g5h5", **UlFromSzHex** returns zero.</span></span> 
  
 <span data-ttu-id="ada37-124">**UlFromSzHex** é afetado pela diferenças diacríticos, mas permite que o 'a' a 'f' e 'A' a 'F' para dígitos hexadecimais.</span><span class="sxs-lookup"><span data-stu-id="ada37-124">**UlFromSzHex** is sensitive to diacritical differences but allows both 'a' through 'f' and 'A' through 'F' for hexadecimal digits.</span></span> <span data-ttu-id="ada37-125">As cadeias de caracteres nos formatos Unicode e DBCS são suportadas.</span><span class="sxs-lookup"><span data-stu-id="ada37-125">Strings in the Unicode and DBCS formats are supported.</span></span> <span data-ttu-id="ada37-126">O limite de tamanho em _lpsz_ é em caracteres, não necessariamente bytes.</span><span class="sxs-lookup"><span data-stu-id="ada37-126">The length limit on  _lpsz_ is in characters, not necessarily bytes.</span></span> 
  

