---
title: ScBinFromHexBounded
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScBinFromHexBounded
api_type:
- COM
ms.assetid: edac715c-6edb-4b05-82e5-c08c3c7cb6d4
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a00a9b2200f76dfd600f72bf387467b5792599c6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770299"
---
# <a name="scbinfromhexbounded"></a><span data-ttu-id="1b076-103">ScBinFromHexBounded</span><span class="sxs-lookup"><span data-stu-id="1b076-103">ScBinFromHexBounded</span></span>

  
  
<span data-ttu-id="1b076-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1b076-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1b076-105">Converte a parte especificada de uma representação de cadeia de caracteres de um número hexadecimal em um número binário.</span><span class="sxs-lookup"><span data-stu-id="1b076-105">Converts the specified portion of a string representation of a hexadecimal number into a binary number.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1b076-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="1b076-106">Header file:</span></span>  <br/> |<span data-ttu-id="1b076-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="1b076-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="1b076-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="1b076-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1b076-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="1b076-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="1b076-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="1b076-110">Called by:</span></span>  <br/> |<span data-ttu-id="1b076-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="1b076-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScBinFromHexBounded(
  LPSTR sz,
  LPBYTE pb,
  ULONG cb
);
```

## <a name="parameters"></a><span data-ttu-id="1b076-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1b076-112">Parameters</span></span>

 <span data-ttu-id="1b076-113">_SZ_</span><span class="sxs-lookup"><span data-stu-id="1b076-113">_sz_</span></span>
  
> <span data-ttu-id="1b076-114">[in] Ponteiro para a cadeia de caracteres terminada em nulo a ser convertido.</span><span class="sxs-lookup"><span data-stu-id="1b076-114">[in] Pointer to the null-terminated string to be converted.</span></span> <span data-ttu-id="1b076-115">Caracteres válidos incluem os caracteres hexadecimais 0 a 9 e os dois caracteres maiusculos e minúsculos a até f.</span><span class="sxs-lookup"><span data-stu-id="1b076-115">Valid characters include the hexadecimal characters 0 through 9 and both uppercase and lowercase characters a through f.</span></span>
    
 <span data-ttu-id="1b076-116">_pb_</span><span class="sxs-lookup"><span data-stu-id="1b076-116">_pb_</span></span>
  
> <span data-ttu-id="1b076-117">[out] Ponteiro para o número binário retornado.</span><span class="sxs-lookup"><span data-stu-id="1b076-117">[out] Pointer to the returned binary number.</span></span>
    
 <span data-ttu-id="1b076-118">_cb_</span><span class="sxs-lookup"><span data-stu-id="1b076-118">_cb_</span></span>
  
> <span data-ttu-id="1b076-119">[in] Tamanho, em bytes, do parâmetro _pb_ .</span><span class="sxs-lookup"><span data-stu-id="1b076-119">[in] Size, in bytes, of the  _pb_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1b076-120">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="1b076-120">Return value</span></span>

<span data-ttu-id="1b076-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="1b076-121">S_OK</span></span>
  
> <span data-ttu-id="1b076-122">Conversão foi bem sucedida.</span><span class="sxs-lookup"><span data-stu-id="1b076-122">Conversion was successful.</span></span>
    
<span data-ttu-id="1b076-123">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="1b076-123">MAPI_E_CALL_FAILED</span></span>
  
> <span data-ttu-id="1b076-124">Caracteres inválidos encontrados.</span><span class="sxs-lookup"><span data-stu-id="1b076-124">Invalid characters were encountered.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1b076-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="1b076-125">See also</span></span>



[<span data-ttu-id="1b076-126">FBinFromHex</span><span class="sxs-lookup"><span data-stu-id="1b076-126">FBinFromHex</span></span>](fbinfromhex.md)

