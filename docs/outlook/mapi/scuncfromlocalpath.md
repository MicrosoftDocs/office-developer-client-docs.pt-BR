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
ms.openlocfilehash: faba91d813d27f7ea45e978724ce0d4707803cba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590103"
---
# <a name="scuncfromlocalpath"></a><span data-ttu-id="d9019-103">ScUNCFromLocalPath</span><span class="sxs-lookup"><span data-stu-id="d9019-103">ScUNCFromLocalPath</span></span>

  
  
<span data-ttu-id="d9019-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d9019-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d9019-105">Localiza um equivalente universal de nomenclatura do caminho UNC (convenção) para o caminho local fornecido.</span><span class="sxs-lookup"><span data-stu-id="d9019-105">Locates a universal naming convention (UNC) path counterpart to the given local path.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d9019-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="d9019-106">Header file:</span></span>  <br/> |<span data-ttu-id="d9019-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d9019-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="d9019-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="d9019-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d9019-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d9019-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d9019-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="d9019-110">Called by:</span></span>  <br/> |<span data-ttu-id="d9019-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="d9019-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScUNCFromLocalPath(
  LPSTR szLocal,
  LPSTR szUNC,
  UINT cchUNC
);
```

## <a name="parameters"></a><span data-ttu-id="d9019-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d9019-112">Parameters</span></span>

 <span data-ttu-id="d9019-113">_szLocal_</span><span class="sxs-lookup"><span data-stu-id="d9019-113">_szLocal_</span></span>
  
> <span data-ttu-id="d9019-114">[in] Um caminho no formato [ _unidade:_]\[ _caminho_] de um arquivo ou diretório.</span><span class="sxs-lookup"><span data-stu-id="d9019-114">[in] A path in the format [ _drive:_]\[ _path_] of a file or directory.</span></span>
    
 <span data-ttu-id="d9019-115">_szUNC_</span><span class="sxs-lookup"><span data-stu-id="d9019-115">_szUNC_</span></span>
  
> <span data-ttu-id="d9019-116">[out] Um caminho no formato \\[ _servidor_]\[ _compartilhar_]\[ _caminho_] do arquivo ou diretório para o parâmetro _szLocal_ da mesma.</span><span class="sxs-lookup"><span data-stu-id="d9019-116">[out] A path in the format \\[ _server_]\[ _share_]\[ _path_] of the same file or directory as for the  _szLocal_ parameter.</span></span> 
    
 <span data-ttu-id="d9019-117">_cchUNC_</span><span class="sxs-lookup"><span data-stu-id="d9019-117">_cchUNC_</span></span>
  
> <span data-ttu-id="d9019-118">[in] Tamanho do buffer da cadeia de caracteres de saída.</span><span class="sxs-lookup"><span data-stu-id="d9019-118">[in] Size of the buffer for the output string.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d9019-119">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="d9019-119">Return value</span></span>

<span data-ttu-id="d9019-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="d9019-120">S_OK</span></span>
  
> <span data-ttu-id="d9019-121">O equivalente do caminho UNC foi localizado com êxito.</span><span class="sxs-lookup"><span data-stu-id="d9019-121">The UNC path counterpart was successfully located.</span></span>
    
<span data-ttu-id="d9019-122">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d9019-122">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="d9019-123">Um ou mais parâmetros são inválidos.</span><span class="sxs-lookup"><span data-stu-id="d9019-123">One or more parameters are invalid.</span></span>
    
<span data-ttu-id="d9019-124">MAPI_E_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="d9019-124">MAPI_E_TOO_BIG</span></span>
  
>  <span data-ttu-id="d9019-125">_szUNC_ não era grande o suficiente para armazenar o resultado.</span><span class="sxs-lookup"><span data-stu-id="d9019-125">_szUNC_ was not large enough to hold the result.</span></span> 
    
<span data-ttu-id="d9019-126">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="d9019-126">S_FALSE</span></span>
  
> <span data-ttu-id="d9019-127">O caminho local já foi uma cadeia de caracteres UNC.</span><span class="sxs-lookup"><span data-stu-id="d9019-127">The local path was already a UNC string.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d9019-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="d9019-128">See also</span></span>



[<span data-ttu-id="d9019-129">ScLocalPathFromUNC</span><span class="sxs-lookup"><span data-stu-id="d9019-129">ScLocalPathFromUNC</span></span>](sclocalpathfromunc.md)

