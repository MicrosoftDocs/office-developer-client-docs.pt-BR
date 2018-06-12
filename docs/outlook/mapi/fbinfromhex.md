---
title: FBinFromHex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBinFromHex
api_type:
- COM
ms.assetid: 47e6c576-bd99-4410-8e41-7dd3159b23b7
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 64d205ee7f51c0ce6a6eb1e982659c6cda675f8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766549"
---
# <a name="fbinfromhex"></a><span data-ttu-id="5a668-103">FBinFromHex</span><span class="sxs-lookup"><span data-stu-id="5a668-103">FBinFromHex</span></span>

  
  
<span data-ttu-id="5a668-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5a668-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5a668-105">Converte uma representação de cadeia de caracteres de um número hexadecimal em dados binários.</span><span class="sxs-lookup"><span data-stu-id="5a668-105">Converts a string representation of a hexadecimal number to binary data.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5a668-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="5a668-106">Header file:</span></span>  <br/> |<span data-ttu-id="5a668-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="5a668-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="5a668-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="5a668-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="5a668-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="5a668-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="5a668-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="5a668-110">Called by:</span></span>  <br/> |<span data-ttu-id="5a668-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="5a668-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FBinFromHex(
  LPSTR sz,
  LPBYTE pb
);
```

## <a name="parameters"></a><span data-ttu-id="5a668-112">Par�metros</span><span class="sxs-lookup"><span data-stu-id="5a668-112">Parameters</span></span>

 <span data-ttu-id="5a668-113">_SZ_</span><span class="sxs-lookup"><span data-stu-id="5a668-113">_sz_</span></span>
  
> <span data-ttu-id="5a668-114">[in] Ponteiro para a cadeia de ASCII terminada em nulo a ser convertido.</span><span class="sxs-lookup"><span data-stu-id="5a668-114">[in] Pointer to the null-terminated ASCII string to be converted.</span></span> <span data-ttu-id="5a668-115">Não é uma cadeia de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="5a668-115">It is not a Unicode string.</span></span> <span data-ttu-id="5a668-116">Caracteres válidos incluem os caracteres hexadecimais zero através de tanto quanto nove caracteres maiusculos e minúsculos A até F.</span><span class="sxs-lookup"><span data-stu-id="5a668-116">Valid characters include the hexadecimal characters zero through nine and both uppercase and lowercase characters A through F.</span></span>
    
 <span data-ttu-id="5a668-117">_pb_</span><span class="sxs-lookup"><span data-stu-id="5a668-117">_pb_</span></span>
  
> <span data-ttu-id="5a668-118">[out] Ponteiro para o número binário retornado.</span><span class="sxs-lookup"><span data-stu-id="5a668-118">[out] Pointer to the returned binary number.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5a668-119">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="5a668-119">Return value</span></span>

<span data-ttu-id="5a668-120">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="5a668-120">TRUE</span></span> 
  
> <span data-ttu-id="5a668-121">A cadeia de caracteres com êxito foi convertida em um número binário.</span><span class="sxs-lookup"><span data-stu-id="5a668-121">The string was successfully converted into a binary number.</span></span> 
    
<span data-ttu-id="5a668-122">FALSO</span><span class="sxs-lookup"><span data-stu-id="5a668-122">FALSE</span></span> 
  
> <span data-ttu-id="5a668-123">A cadeia de caracteres de entrada contém caracteres inválidos de hexadecimais ASCII.</span><span class="sxs-lookup"><span data-stu-id="5a668-123">The input string contains invalid ASCII hexadecimal characters.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5a668-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="5a668-124">See also</span></span>



[<span data-ttu-id="5a668-125">ScBinFromHexBounded</span><span class="sxs-lookup"><span data-stu-id="5a668-125">ScBinFromHexBounded</span></span>](scbinfromhexbounded.md)

