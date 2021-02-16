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
# <a name="fbinfromhex"></a><span data-ttu-id="9d6dd-103">FBinFromHex</span><span class="sxs-lookup"><span data-stu-id="9d6dd-103">FBinFromHex</span></span>

  
  
<span data-ttu-id="9d6dd-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9d6dd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9d6dd-105">Converte uma representação de cadeia de caracteres de um número hexadecimal em dados binários.</span><span class="sxs-lookup"><span data-stu-id="9d6dd-105">Converts a string representation of a hexadecimal number to binary data.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9d6dd-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="9d6dd-106">Header file:</span></span>  <br/> |<span data-ttu-id="9d6dd-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="9d6dd-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="9d6dd-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="9d6dd-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="9d6dd-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="9d6dd-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="9d6dd-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="9d6dd-110">Called by:</span></span>  <br/> |<span data-ttu-id="9d6dd-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="9d6dd-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FBinFromHex(
  LPSTR sz,
  LPBYTE pb
);
```

## <a name="parameters"></a><span data-ttu-id="9d6dd-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9d6dd-112">Parameters</span></span>

 <span data-ttu-id="9d6dd-113">_sz_</span><span class="sxs-lookup"><span data-stu-id="9d6dd-113">_sz_</span></span>
  
> <span data-ttu-id="9d6dd-114">[in] Ponteiro para a cadeia de caracteres ASCII terminada em nulo a ser convertida.</span><span class="sxs-lookup"><span data-stu-id="9d6dd-114">[in] Pointer to the null-terminated ASCII string to be converted.</span></span> <span data-ttu-id="9d6dd-115">Não é uma cadeia de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="9d6dd-115">It is not a Unicode string.</span></span> <span data-ttu-id="9d6dd-116">Os caracteres válidos incluem os caracteres hexadecimais zero a nove e caracteres em maiúsculas e minúsculas de A a F.</span><span class="sxs-lookup"><span data-stu-id="9d6dd-116">Valid characters include the hexadecimal characters zero through nine and both uppercase and lowercase characters A through F.</span></span>
    
 <span data-ttu-id="9d6dd-117">_pb_</span><span class="sxs-lookup"><span data-stu-id="9d6dd-117">_pb_</span></span>
  
> <span data-ttu-id="9d6dd-118">[out] Ponteiro para o número binário retornado.</span><span class="sxs-lookup"><span data-stu-id="9d6dd-118">[out] Pointer to the returned binary number.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9d6dd-119">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9d6dd-119">Return value</span></span>

<span data-ttu-id="9d6dd-120">TRUE</span><span class="sxs-lookup"><span data-stu-id="9d6dd-120">TRUE</span></span> 
  
> <span data-ttu-id="9d6dd-121">A cadeia de caracteres foi convertida com êxito em um número binário.</span><span class="sxs-lookup"><span data-stu-id="9d6dd-121">The string was successfully converted into a binary number.</span></span> 
    
<span data-ttu-id="9d6dd-122">FALSE</span><span class="sxs-lookup"><span data-stu-id="9d6dd-122">FALSE</span></span> 
  
> <span data-ttu-id="9d6dd-123">A cadeia de caracteres de entrada contém caracteres hexadecimais ASCII inválidos.</span><span class="sxs-lookup"><span data-stu-id="9d6dd-123">The input string contains invalid ASCII hexadecimal characters.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9d6dd-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="9d6dd-124">See also</span></span>



[<span data-ttu-id="9d6dd-125">ScBinFromHexBounded</span><span class="sxs-lookup"><span data-stu-id="9d6dd-125">ScBinFromHexBounded</span></span>](scbinfromhexbounded.md)

