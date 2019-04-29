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
ms.openlocfilehash: e7607a57da5b618a20d6c8e360c7e3cb4f933856
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432230"
---
# <a name="sclocalpathfromunc"></a><span data-ttu-id="d2848-103">ScLocalPathFromUNC</span><span class="sxs-lookup"><span data-stu-id="d2848-103">ScLocalPathFromUNC</span></span>

  
  
<span data-ttu-id="d2848-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d2848-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d2848-105">Localiza uma contraparte de caminho local para o caminho especificado da Convenção Universal de nomenclatura (UNC).</span><span class="sxs-lookup"><span data-stu-id="d2848-105">Locates a local path counterpart to the given universal naming convention (UNC) path.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d2848-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="d2848-106">Header file:</span></span>  <br/> |<span data-ttu-id="d2848-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="d2848-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="d2848-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="d2848-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d2848-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d2848-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d2848-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="d2848-110">Called by:</span></span>  <br/> |<span data-ttu-id="d2848-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="d2848-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScLocalPathFromUNC(
  LPSTR szUNC,
  LPSTR szLocal,
  UINT cchLocal
);
```

## <a name="parameters"></a><span data-ttu-id="d2848-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2848-112">Parameters</span></span>

 <span data-ttu-id="d2848-113">_szUNC_</span><span class="sxs-lookup"><span data-stu-id="d2848-113">_szUNC_</span></span>
  
> <span data-ttu-id="d2848-114">no Um caminho \\no formato [ _Server_]\[ _share_]\[ _caminho_] de um arquivo ou diretório.</span><span class="sxs-lookup"><span data-stu-id="d2848-114">[in] A path in the format \\[ _server_]\[ _share_]\[ _path_] of a file or directory.</span></span>
    
 <span data-ttu-id="d2848-115">_szLocal_</span><span class="sxs-lookup"><span data-stu-id="d2848-115">_szLocal_</span></span>
  
> <span data-ttu-id="d2848-116">bota Um caminho no formato [ _unidade:_]\[ _caminho_] do mesmo arquivo ou diretório que o parâmetro _szUNC_ .</span><span class="sxs-lookup"><span data-stu-id="d2848-116">[out] A path in the format [ _drive:_]\[ _path_] of the same file or directory as for the  _szUNC_ parameter.</span></span> 
    
 <span data-ttu-id="d2848-117">_cchLocal_</span><span class="sxs-lookup"><span data-stu-id="d2848-117">_cchLocal_</span></span>
  
> <span data-ttu-id="d2848-118">no Tamanho do buffer para a cadeia de caracteres de saída.</span><span class="sxs-lookup"><span data-stu-id="d2848-118">[in] Size of the buffer for the output string.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d2848-119">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="d2848-119">Return value</span></span>

<span data-ttu-id="d2848-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="d2848-120">S_OK</span></span>
  
> <span data-ttu-id="d2848-121">Um caminho local foi localizado com êxito.</span><span class="sxs-lookup"><span data-stu-id="d2848-121">A local path was successfully located.</span></span>
    
<span data-ttu-id="d2848-122">MAPI_E_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="d2848-122">MAPI_E_TOO_BIG</span></span>
  
>  <span data-ttu-id="d2848-123">_szLocal_ não era grande o suficiente para armazenar o resultado.</span><span class="sxs-lookup"><span data-stu-id="d2848-123">_szLocal_ was not large enough to hold the result.</span></span> 
    
<span data-ttu-id="d2848-124">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="d2848-124">S_FALSE</span></span>
  
> <span data-ttu-id="d2848-125">A cadeia de caracteres UNC já era um caminho local.</span><span class="sxs-lookup"><span data-stu-id="d2848-125">The UNC string was already a local path.</span></span>
    
<span data-ttu-id="d2848-126">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="d2848-126">MAPI_E_NOT_FOUND</span></span>
  
> <span data-ttu-id="d2848-127">Um caminho local não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="d2848-127">A local path was not found.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d2848-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="d2848-128">See also</span></span>



[<span data-ttu-id="d2848-129">ScUNCFromLocalPath</span><span class="sxs-lookup"><span data-stu-id="d2848-129">ScUNCFromLocalPath</span></span>](scuncfromlocalpath.md)

