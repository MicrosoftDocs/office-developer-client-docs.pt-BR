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
ms.openlocfilehash: 813fab28e3e865c9f04f85c854b292ce7229dad5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357495"
---
# <a name="scbinfromhexbounded"></a><span data-ttu-id="42be3-103">ScBinFromHexBounded</span><span class="sxs-lookup"><span data-stu-id="42be3-103">ScBinFromHexBounded</span></span>

  
  
<span data-ttu-id="42be3-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="42be3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="42be3-105">Converte a parte especificada de uma representação de cadeia de caracteres de um número hexadecimal em um número binário.</span><span class="sxs-lookup"><span data-stu-id="42be3-105">Converts the specified portion of a string representation of a hexadecimal number into a binary number.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="42be3-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="42be3-106">Header file:</span></span>  <br/> |<span data-ttu-id="42be3-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="42be3-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="42be3-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="42be3-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="42be3-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="42be3-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="42be3-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="42be3-110">Called by:</span></span>  <br/> |<span data-ttu-id="42be3-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="42be3-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScBinFromHexBounded(
  LPSTR sz,
  LPBYTE pb,
  ULONG cb
);
```

## <a name="parameters"></a><span data-ttu-id="42be3-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="42be3-112">Parameters</span></span>

 <span data-ttu-id="42be3-113">_v_</span><span class="sxs-lookup"><span data-stu-id="42be3-113">_sz_</span></span>
  
> <span data-ttu-id="42be3-114">no Ponteiro para a cadeia de caracteres terminada em nulo a ser convertido.</span><span class="sxs-lookup"><span data-stu-id="42be3-114">[in] Pointer to the null-terminated string to be converted.</span></span> <span data-ttu-id="42be3-115">Os caracteres válidos incluem os caracteres hexadecimais de 0 a 9 e os caracteres maiúsculos e minúsculos de a a f.</span><span class="sxs-lookup"><span data-stu-id="42be3-115">Valid characters include the hexadecimal characters 0 through 9 and both uppercase and lowercase characters a through f.</span></span>
    
 <span data-ttu-id="42be3-116">_pb_</span><span class="sxs-lookup"><span data-stu-id="42be3-116">_pb_</span></span>
  
> <span data-ttu-id="42be3-117">bota Ponteiro para o número binário retornado.</span><span class="sxs-lookup"><span data-stu-id="42be3-117">[out] Pointer to the returned binary number.</span></span>
    
 <span data-ttu-id="42be3-118">_cb_</span><span class="sxs-lookup"><span data-stu-id="42be3-118">_cb_</span></span>
  
> <span data-ttu-id="42be3-119">no Tamanho, em bytes, do parâmetro _PB_ .</span><span class="sxs-lookup"><span data-stu-id="42be3-119">[in] Size, in bytes, of the  _pb_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="42be3-120">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="42be3-120">Return value</span></span>

<span data-ttu-id="42be3-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="42be3-121">S_OK</span></span>
  
> <span data-ttu-id="42be3-122">A conversão foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="42be3-122">Conversion was successful.</span></span>
    
<span data-ttu-id="42be3-123">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="42be3-123">MAPI_E_CALL_FAILED</span></span>
  
> <span data-ttu-id="42be3-124">Foram encontrados caracteres inVálidos.</span><span class="sxs-lookup"><span data-stu-id="42be3-124">Invalid characters were encountered.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="42be3-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="42be3-125">See also</span></span>



[<span data-ttu-id="42be3-126">FBinFromHex</span><span class="sxs-lookup"><span data-stu-id="42be3-126">FBinFromHex</span></span>](fbinfromhex.md)

