---
title: ScUNCFromLocalPath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScUNCFromLocalPath
api_type:
- COM
ms.assetid: cc4abf1a-c08c-4462-9d7c-6af506dc07c9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 667eda2a018d2a5d712950a31e05ec0ba9bb32ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770341"
---
# <a name="scuncfromlocalpath"></a><span data-ttu-id="c1f4b-103">ScUNCFromLocalPath</span><span class="sxs-lookup"><span data-stu-id="c1f4b-103">ScUNCFromLocalPath</span></span>

  
  
<span data-ttu-id="c1f4b-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c1f4b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c1f4b-105">Localiza um equivalente universal de nomenclatura do caminho UNC (convenção) para o caminho local fornecido.</span><span class="sxs-lookup"><span data-stu-id="c1f4b-105">Locates a universal naming convention (UNC) path counterpart to the given local path.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c1f4b-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="c1f4b-106">Header file:</span></span>  <br/> |<span data-ttu-id="c1f4b-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c1f4b-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="c1f4b-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="c1f4b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c1f4b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c1f4b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c1f4b-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="c1f4b-110">Called by:</span></span>  <br/> |<span data-ttu-id="c1f4b-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="c1f4b-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScUNCFromLocalPath(
  LPSTR szLocal,
  LPSTR szUNC,
  UINT cchUNC
);
```

## <a name="parameters"></a><span data-ttu-id="c1f4b-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c1f4b-112">Parameters</span></span>

 <span data-ttu-id="c1f4b-113">_szLocal_</span><span class="sxs-lookup"><span data-stu-id="c1f4b-113">_szLocal_</span></span>
  
> <span data-ttu-id="c1f4b-114">[in] Um caminho no formato [ _unidade:_]\[ _caminho_] de um arquivo ou diretório.</span><span class="sxs-lookup"><span data-stu-id="c1f4b-114">[in] A path in the format [ _drive:_]\[ _path_] of a file or directory.</span></span>
    
 <span data-ttu-id="c1f4b-115">_szUNC_</span><span class="sxs-lookup"><span data-stu-id="c1f4b-115">_szUNC_</span></span>
  
> <span data-ttu-id="c1f4b-116">[out] Um caminho no formato \\[ _servidor_]\[ _compartilhar_]\[ _caminho_] do arquivo ou diretório para o parâmetro _szLocal_ da mesma.</span><span class="sxs-lookup"><span data-stu-id="c1f4b-116">[out] A path in the format \\[ _server_]\[ _share_]\[ _path_] of the same file or directory as for the  _szLocal_ parameter.</span></span> 
    
 <span data-ttu-id="c1f4b-117">_cchUNC_</span><span class="sxs-lookup"><span data-stu-id="c1f4b-117">_cchUNC_</span></span>
  
> <span data-ttu-id="c1f4b-118">[in] Tamanho do buffer da cadeia de caracteres de saída.</span><span class="sxs-lookup"><span data-stu-id="c1f4b-118">[in] Size of the buffer for the output string.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c1f4b-119">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="c1f4b-119">Return value</span></span>

<span data-ttu-id="c1f4b-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="c1f4b-120">S_OK</span></span>
  
> <span data-ttu-id="c1f4b-121">O equivalente do caminho UNC foi localizado com êxito.</span><span class="sxs-lookup"><span data-stu-id="c1f4b-121">The UNC path counterpart was successfully located.</span></span>
    
<span data-ttu-id="c1f4b-122">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c1f4b-122">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="c1f4b-123">Um ou mais parâmetros são inválidos.</span><span class="sxs-lookup"><span data-stu-id="c1f4b-123">One or more parameters are invalid.</span></span>
    
<span data-ttu-id="c1f4b-124">MAPI_E_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="c1f4b-124">MAPI_E_TOO_BIG</span></span>
  
>  <span data-ttu-id="c1f4b-125">_szUNC_ não era grande o suficiente para armazenar o resultado.</span><span class="sxs-lookup"><span data-stu-id="c1f4b-125">_szUNC_ was not large enough to hold the result.</span></span> 
    
<span data-ttu-id="c1f4b-126">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="c1f4b-126">S_FALSE</span></span>
  
> <span data-ttu-id="c1f4b-127">O caminho local já foi uma cadeia de caracteres UNC.</span><span class="sxs-lookup"><span data-stu-id="c1f4b-127">The local path was already a UNC string.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c1f4b-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="c1f4b-128">See also</span></span>



[<span data-ttu-id="c1f4b-129">ScLocalPathFromUNC</span><span class="sxs-lookup"><span data-stu-id="c1f4b-129">ScLocalPathFromUNC</span></span>](sclocalpathfromunc.md)

