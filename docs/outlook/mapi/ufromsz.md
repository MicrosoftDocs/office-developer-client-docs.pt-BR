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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346533"
---
# <a name="ufromsz"></a><span data-ttu-id="cf552-103">UFromSz</span><span class="sxs-lookup"><span data-stu-id="cf552-103">UFromSz</span></span>

  
  
<span data-ttu-id="cf552-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cf552-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cf552-105">Converte uma cadeia de caracteres decimal terminada em nulo em um inteiro não assinado.</span><span class="sxs-lookup"><span data-stu-id="cf552-105">Converts a null-terminated string of decimal digits into an unsigned integer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cf552-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="cf552-106">Header file:</span></span>  <br/> |<span data-ttu-id="cf552-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="cf552-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="cf552-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="cf552-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="cf552-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="cf552-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="cf552-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="cf552-110">Called by:</span></span>  <br/> |<span data-ttu-id="cf552-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="cf552-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
UINT UFromSz(
  LPCSTR lpsz
);
```

## <a name="parameters"></a><span data-ttu-id="cf552-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cf552-112">Parameters</span></span>

 <span data-ttu-id="cf552-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="cf552-113">_lpsz_</span></span>
  
> <span data-ttu-id="cf552-114">no Ponteiro para a cadeia de caracteres terminada em nulo a ser convertido.</span><span class="sxs-lookup"><span data-stu-id="cf552-114">[in] Pointer to the null-terminated string to be converted.</span></span> <span data-ttu-id="cf552-115">O parâmetro _lpsz_ não deve exceder 65536 caracteres.</span><span class="sxs-lookup"><span data-stu-id="cf552-115">The  _lpsz_ parameter must not exceed 65536 characters.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="cf552-116">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="cf552-116">Return value</span></span>

 <span data-ttu-id="cf552-117">**UFromSz** retorna um inteiro não assinado.</span><span class="sxs-lookup"><span data-stu-id="cf552-117">**UFromSz** returns an unsigned integer.</span></span> <span data-ttu-id="cf552-118">Se a cadeia de caracteres não começar com pelo menos um dígito decimal, zero será retornado.</span><span class="sxs-lookup"><span data-stu-id="cf552-118">If the string does not begin with at least one decimal digit, zero is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="cf552-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="cf552-119">Remarks</span></span>

<span data-ttu-id="cf552-120">A função **UFromSz** para de converter quando atinge o primeiro caractere na cadeia de caracteres que não é um dígito decimal.</span><span class="sxs-lookup"><span data-stu-id="cf552-120">The **UFromSz** function stops converting when it reaches the first character in the string that is not a decimal digit.</span></span> <span data-ttu-id="cf552-121">Por exemplo, dado a cadeia de caracteres "55", **UFromSz** retorna o valor inteiro 55.</span><span class="sxs-lookup"><span data-stu-id="cf552-121">For example, given the string "55", **UFromSz** returns the integer value 55.</span></span> <span data-ttu-id="cf552-122">Dada a cadeia de caracteres "5a5b", a função retorna o valor inteiro 5.</span><span class="sxs-lookup"><span data-stu-id="cf552-122">Given the string "5a5b", the function returns the integer value 5.</span></span> <span data-ttu-id="cf552-123">Dada a cadeia de caracteres "A5B5", **UFromSz** retorna zero.</span><span class="sxs-lookup"><span data-stu-id="cf552-123">Given the string "a5b5", **UFromSz** returns zero.</span></span> 
  
 <span data-ttu-id="cf552-124">**UFromSz** é sensível a diferenças diacrítico.</span><span class="sxs-lookup"><span data-stu-id="cf552-124">**UFromSz** is sensitive to diacritical differences.</span></span> <span data-ttu-id="cf552-125">As cadeias de caracteres nos formatos Unicode e DBCS são suportadas.</span><span class="sxs-lookup"><span data-stu-id="cf552-125">Strings in the Unicode and DBCS formats are supported.</span></span> <span data-ttu-id="cf552-126">O limite de tamanho no _lpsz_ está em caracteres, não necessariamente em bytes.</span><span class="sxs-lookup"><span data-stu-id="cf552-126">The length limit on  _lpsz_ is in characters, not necessarily bytes.</span></span> 
  

