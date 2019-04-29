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
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 55c7deec9d29ae22a07b2f5ccd1c832d56782c03
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414932"
---
# <a name="fbinfromhex"></a><span data-ttu-id="abca4-103">FBinFromHex</span><span class="sxs-lookup"><span data-stu-id="abca4-103">FBinFromHex</span></span>

  
  
<span data-ttu-id="abca4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="abca4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="abca4-105">Converte uma representação de cadeia de caracteres de um número hexadecimal em dados binários.</span><span class="sxs-lookup"><span data-stu-id="abca4-105">Converts a string representation of a hexadecimal number to binary data.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="abca4-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="abca4-106">Header file:</span></span>  <br/> |<span data-ttu-id="abca4-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="abca4-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="abca4-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="abca4-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="abca4-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="abca4-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="abca4-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="abca4-110">Called by:</span></span>  <br/> |<span data-ttu-id="abca4-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="abca4-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FBinFromHex(
  LPSTR sz,
  LPBYTE pb
);
```

## <a name="parameters"></a><span data-ttu-id="abca4-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="abca4-112">Parameters</span></span>

 <span data-ttu-id="abca4-113">_v_</span><span class="sxs-lookup"><span data-stu-id="abca4-113">_sz_</span></span>
  
> <span data-ttu-id="abca4-114">no Ponteiro para a cadeia de caracteres ASCII terminada em nulo para conversão.</span><span class="sxs-lookup"><span data-stu-id="abca4-114">[in] Pointer to the null-terminated ASCII string to be converted.</span></span> <span data-ttu-id="abca4-115">Não é uma cadeia de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="abca4-115">It is not a Unicode string.</span></span> <span data-ttu-id="abca4-116">Os caracteres válidos incluem os caracteres hexadecimais de zero a nove e os caracteres maiúsculos e minúsculos de A a F.</span><span class="sxs-lookup"><span data-stu-id="abca4-116">Valid characters include the hexadecimal characters zero through nine and both uppercase and lowercase characters A through F.</span></span>
    
 <span data-ttu-id="abca4-117">_pb_</span><span class="sxs-lookup"><span data-stu-id="abca4-117">_pb_</span></span>
  
> <span data-ttu-id="abca4-118">bota Ponteiro para o número binário retornado.</span><span class="sxs-lookup"><span data-stu-id="abca4-118">[out] Pointer to the returned binary number.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="abca4-119">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="abca4-119">Return value</span></span>

<span data-ttu-id="abca4-120">TRUE</span><span class="sxs-lookup"><span data-stu-id="abca4-120">TRUE</span></span> 
  
> <span data-ttu-id="abca4-121">A cadeia de caracteres foi convertida com êxito em um número binário.</span><span class="sxs-lookup"><span data-stu-id="abca4-121">The string was successfully converted into a binary number.</span></span> 
    
<span data-ttu-id="abca4-122">FALSE</span><span class="sxs-lookup"><span data-stu-id="abca4-122">FALSE</span></span> 
  
> <span data-ttu-id="abca4-123">A cadeia de caracteres de entrada contém caracteres hexadecimais ASCII inválidos.</span><span class="sxs-lookup"><span data-stu-id="abca4-123">The input string contains invalid ASCII hexadecimal characters.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="abca4-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="abca4-124">See also</span></span>



[<span data-ttu-id="abca4-125">ScBinFromHexBounded</span><span class="sxs-lookup"><span data-stu-id="abca4-125">ScBinFromHexBounded</span></span>](scbinfromhexbounded.md)

