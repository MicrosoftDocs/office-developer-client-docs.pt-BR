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
# <a name="ulfromszhex"></a><span data-ttu-id="dad7a-103">UlFromSzHex</span><span class="sxs-lookup"><span data-stu-id="dad7a-103">UlFromSzHex</span></span>

  
  
<span data-ttu-id="dad7a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dad7a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dad7a-105">Converte uma cadeia de caracteres hexadecimal terminada em nulo em um inteiro longo não assinado.</span><span class="sxs-lookup"><span data-stu-id="dad7a-105">Converts a null-terminated string of hexadecimal digits into an unsigned long integer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dad7a-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="dad7a-106">Header file:</span></span>  <br/> |<span data-ttu-id="dad7a-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="dad7a-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="dad7a-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="dad7a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="dad7a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="dad7a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="dad7a-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="dad7a-110">Called by:</span></span>  <br/> |<span data-ttu-id="dad7a-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="dad7a-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlFromSzHex(
LPCSTR lpsz
);
```

## <a name="parameters"></a><span data-ttu-id="dad7a-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dad7a-112">Parameters</span></span>

 <span data-ttu-id="dad7a-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="dad7a-113">_lpsz_</span></span>
  
> <span data-ttu-id="dad7a-114">no Ponteiro para a cadeia de caracteres terminada em nulo a ser convertido.</span><span class="sxs-lookup"><span data-stu-id="dad7a-114">[in] Pointer to the null-terminated string to be converted.</span></span> <span data-ttu-id="dad7a-115">O parâmetro _lpsz_ não deve exceder 65536 caracteres.</span><span class="sxs-lookup"><span data-stu-id="dad7a-115">The  _lpsz_ parameter must not exceed 65536 characters.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="dad7a-116">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="dad7a-116">Return value</span></span>

 <span data-ttu-id="dad7a-117">**UlFromSzHex** retorna um inteiro longo sem sinal.</span><span class="sxs-lookup"><span data-stu-id="dad7a-117">**UlFromSzHex** returns an unsigned long integer.</span></span> <span data-ttu-id="dad7a-118">Se a cadeia de caracteres não começar com pelo menos um dígito hexadecimal, zero será retornado.</span><span class="sxs-lookup"><span data-stu-id="dad7a-118">If the string does not begin with at least one hexadecimal digit, zero is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="dad7a-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="dad7a-119">Remarks</span></span>

<span data-ttu-id="dad7a-120">A função **UlFromSzHex** para de converter quando atinge o primeiro caractere na cadeia de caracteres que não é um dígito hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="dad7a-120">The **UlFromSzHex** function stops converting when it reaches the first character in the string that is not a hexadecimal digit.</span></span> <span data-ttu-id="dad7a-121">Por exemplo, dada a cadeia de caracteres "5a", **UlFromSzHex** retorna o valor inteiro 90.</span><span class="sxs-lookup"><span data-stu-id="dad7a-121">For example, given the string "5a", **UlFromSzHex** returns the integer value 90.</span></span> <span data-ttu-id="dad7a-122">Dada a cadeia de caracteres "5g5h", a função retorna o valor inteiro 5.</span><span class="sxs-lookup"><span data-stu-id="dad7a-122">Given the string "5g5h", the function returns the integer value 5.</span></span> <span data-ttu-id="dad7a-123">Dada a cadeia de caracteres "g5h5", **UlFromSzHex** retorna zero.</span><span class="sxs-lookup"><span data-stu-id="dad7a-123">Given the string "g5h5", **UlFromSzHex** returns zero.</span></span> 
  
 <span data-ttu-id="dad7a-124">**UlFromSzHex** é sensível a diferenças diacrítico, mas permite que "a" até ' f ' E ' a ' A ' f ' para dígitos hexadecimais.</span><span class="sxs-lookup"><span data-stu-id="dad7a-124">**UlFromSzHex** is sensitive to diacritical differences but allows both 'a' through 'f' and 'A' through 'F' for hexadecimal digits.</span></span> <span data-ttu-id="dad7a-125">As cadeias de caracteres nos formatos Unicode e DBCS são suportadas.</span><span class="sxs-lookup"><span data-stu-id="dad7a-125">Strings in the Unicode and DBCS formats are supported.</span></span> <span data-ttu-id="dad7a-126">O limite de tamanho no _lpsz_ está em caracteres, não necessariamente em bytes.</span><span class="sxs-lookup"><span data-stu-id="dad7a-126">The length limit on  _lpsz_ is in characters, not necessarily bytes.</span></span> 
  

