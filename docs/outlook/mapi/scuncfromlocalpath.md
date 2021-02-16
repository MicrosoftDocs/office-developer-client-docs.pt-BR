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
ms.openlocfilehash: b53dd9aaaf18dba5c7e33e0bc7d984de757634a4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414533"
---
# <a name="scuncfromlocalpath"></a><span data-ttu-id="86067-103">ScUNCFromLocalPath</span><span class="sxs-lookup"><span data-stu-id="86067-103">ScUNCFromLocalPath</span></span>

  
  
<span data-ttu-id="86067-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="86067-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="86067-105">Localiza uma contraparte de caminho UNC para o caminho local determinado.</span><span class="sxs-lookup"><span data-stu-id="86067-105">Locates a universal naming convention (UNC) path counterpart to the given local path.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="86067-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="86067-106">Header file:</span></span>  <br/> |<span data-ttu-id="86067-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="86067-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="86067-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="86067-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="86067-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="86067-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="86067-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="86067-110">Called by:</span></span>  <br/> |<span data-ttu-id="86067-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="86067-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScUNCFromLocalPath(
  LPSTR szLocal,
  LPSTR szUNC,
  UINT cchUNC
);
```

## <a name="parameters"></a><span data-ttu-id="86067-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="86067-112">Parameters</span></span>

 <span data-ttu-id="86067-113">_szLocal_</span><span class="sxs-lookup"><span data-stu-id="86067-113">_szLocal_</span></span>
  
> <span data-ttu-id="86067-114">[in] Um caminho no formato [ _unidade:_] \[ _caminho_] de um arquivo ou diretório.</span><span class="sxs-lookup"><span data-stu-id="86067-114">[in] A path in the format [ _drive:_]\[ _path_] of a file or directory.</span></span>
    
 <span data-ttu-id="86067-115">_szUNC_</span><span class="sxs-lookup"><span data-stu-id="86067-115">_szUNC_</span></span>
  
> <span data-ttu-id="86067-116">[out] Um caminho no formato [ servidor ] compartilhamento ] caminho ] do mesmo arquivo ou diretório \\ como para o parâmetro  \[  \[  _szLocal._</span><span class="sxs-lookup"><span data-stu-id="86067-116">[out] A path in the format \\[ _server_]\[ _share_]\[ _path_] of the same file or directory as for the  _szLocal_ parameter.</span></span> 
    
 <span data-ttu-id="86067-117">_cchUNC_</span><span class="sxs-lookup"><span data-stu-id="86067-117">_cchUNC_</span></span>
  
> <span data-ttu-id="86067-118">[in] Tamanho do buffer para a cadeia de caracteres de saída.</span><span class="sxs-lookup"><span data-stu-id="86067-118">[in] Size of the buffer for the output string.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="86067-119">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="86067-119">Return value</span></span>

<span data-ttu-id="86067-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="86067-120">S_OK</span></span>
  
> <span data-ttu-id="86067-121">A contraparte do caminho UNC foi localizada com êxito.</span><span class="sxs-lookup"><span data-stu-id="86067-121">The UNC path counterpart was successfully located.</span></span>
    
<span data-ttu-id="86067-122">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="86067-122">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="86067-123">Um ou mais parâmetros são inválidos.</span><span class="sxs-lookup"><span data-stu-id="86067-123">One or more parameters are invalid.</span></span>
    
<span data-ttu-id="86067-124">MAPI_E_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="86067-124">MAPI_E_TOO_BIG</span></span>
  
>  <span data-ttu-id="86067-125">_szUNC_ não era grande o suficiente para manter o resultado.</span><span class="sxs-lookup"><span data-stu-id="86067-125">_szUNC_ was not large enough to hold the result.</span></span> 
    
<span data-ttu-id="86067-126">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="86067-126">S_FALSE</span></span>
  
> <span data-ttu-id="86067-127">O caminho local já era uma cadeia de caracteres UNC.</span><span class="sxs-lookup"><span data-stu-id="86067-127">The local path was already a UNC string.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="86067-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="86067-128">See also</span></span>



[<span data-ttu-id="86067-129">ScLocalPathFromUNC</span><span class="sxs-lookup"><span data-stu-id="86067-129">ScLocalPathFromUNC</span></span>](sclocalpathfromunc.md)

