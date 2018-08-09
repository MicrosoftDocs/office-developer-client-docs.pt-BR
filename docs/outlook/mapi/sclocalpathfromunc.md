---
title: ScLocalPathFromUNC
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScLocalPathFromUNC
api_type:
- COM
ms.assetid: ef5eb5c6-251e-4a3a-8855-7c28804a29ab
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e94692ac4eb401109fcb522e6224c8748bef37f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770325"
---
# <a name="sclocalpathfromunc"></a><span data-ttu-id="b7eab-103">ScLocalPathFromUNC</span><span class="sxs-lookup"><span data-stu-id="b7eab-103">ScLocalPathFromUNC</span></span>

  
  
<span data-ttu-id="b7eab-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b7eab-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b7eab-105">Localiza um equivalente do caminho local para o determinado caminho universal naming convention (UNC).</span><span class="sxs-lookup"><span data-stu-id="b7eab-105">Locates a local path counterpart to the given universal naming convention (UNC) path.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b7eab-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="b7eab-106">Header file:</span></span>  <br/> |<span data-ttu-id="b7eab-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="b7eab-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="b7eab-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="b7eab-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b7eab-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b7eab-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b7eab-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="b7eab-110">Called by:</span></span>  <br/> |<span data-ttu-id="b7eab-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="b7eab-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScLocalPathFromUNC(
  LPSTR szUNC,
  LPSTR szLocal,
  UINT cchLocal
);
```

## <a name="parameters"></a><span data-ttu-id="b7eab-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b7eab-112">Parameters</span></span>

 <span data-ttu-id="b7eab-113">_szUNC_</span><span class="sxs-lookup"><span data-stu-id="b7eab-113">_szUNC_</span></span>
  
> <span data-ttu-id="b7eab-114">[in] Um caminho no formato \\[ _servidor_]\[ _compartilhar_]\[ _caminho_] de um arquivo ou diretório.</span><span class="sxs-lookup"><span data-stu-id="b7eab-114">[in] A path in the format \\[ _server_]\[ _share_]\[ _path_] of a file or directory.</span></span>
    
 <span data-ttu-id="b7eab-115">_szLocal_</span><span class="sxs-lookup"><span data-stu-id="b7eab-115">_szLocal_</span></span>
  
> <span data-ttu-id="b7eab-116">[out] Um caminho no formato [ _unidade:_]\[ _caminho_] do arquivo ou diretório para o parâmetro _szUNC_ da mesma.</span><span class="sxs-lookup"><span data-stu-id="b7eab-116">[out] A path in the format [ _drive:_]\[ _path_] of the same file or directory as for the  _szUNC_ parameter.</span></span> 
    
 <span data-ttu-id="b7eab-117">_cchLocal_</span><span class="sxs-lookup"><span data-stu-id="b7eab-117">_cchLocal_</span></span>
  
> <span data-ttu-id="b7eab-118">[in] Tamanho do buffer da cadeia de caracteres de saída.</span><span class="sxs-lookup"><span data-stu-id="b7eab-118">[in] Size of the buffer for the output string.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b7eab-119">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="b7eab-119">Return value</span></span>

<span data-ttu-id="b7eab-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="b7eab-120">S_OK</span></span>
  
> <span data-ttu-id="b7eab-121">Um caminho local foi localizado com êxito.</span><span class="sxs-lookup"><span data-stu-id="b7eab-121">A local path was successfully located.</span></span>
    
<span data-ttu-id="b7eab-122">MAPI_E_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="b7eab-122">MAPI_E_TOO_BIG</span></span>
  
>  <span data-ttu-id="b7eab-123">_szLocal_ não era grande o suficiente para armazenar o resultado.</span><span class="sxs-lookup"><span data-stu-id="b7eab-123">_szLocal_ was not large enough to hold the result.</span></span> 
    
<span data-ttu-id="b7eab-124">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="b7eab-124">S_FALSE</span></span>
  
> <span data-ttu-id="b7eab-125">A cadeia de caracteres UNC já era um caminho local.</span><span class="sxs-lookup"><span data-stu-id="b7eab-125">The UNC string was already a local path.</span></span>
    
<span data-ttu-id="b7eab-126">E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="b7eab-126">MAPI_E_NOT_FOUND</span></span>
  
> <span data-ttu-id="b7eab-127">Um caminho local não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="b7eab-127">A local path was not found.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b7eab-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="b7eab-128">See also</span></span>



[<span data-ttu-id="b7eab-129">ScUNCFromLocalPath</span><span class="sxs-lookup"><span data-stu-id="b7eab-129">ScUNCFromLocalPath</span></span>](scuncfromlocalpath.md)

