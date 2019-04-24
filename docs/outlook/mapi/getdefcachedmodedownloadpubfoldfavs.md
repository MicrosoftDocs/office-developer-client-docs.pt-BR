---
title: GetDefCachedModeDownloadPubFoldFavs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2dd95561-ed8f-8a3b-6532-b53556f16666
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5e623c9d40ffd2dd276bd9601676244644bb3402
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299885"
---
# <a name="getdefcachedmodedownloadpubfoldfavs"></a><span data-ttu-id="5be82-103">GetDefCachedModeDownloadPubFoldFavs</span><span class="sxs-lookup"><span data-stu-id="5be82-103">GetDefCachedModeDownloadPubFoldFavs</span></span>

  
  
<span data-ttu-id="5be82-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5be82-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5be82-105">Indica se o modo cache do Exchange para a pasta **favoritos da pasta pública** está habilitado e se isso é imposto pela política.</span><span class="sxs-lookup"><span data-stu-id="5be82-105">Indicates whether Cached Exchange Mode for the **Public Folder Favorites** folder is enabled, and whether this is enforced by policy.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="5be82-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="5be82-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5be82-107">Exportado por:</span><span class="sxs-lookup"><span data-stu-id="5be82-107">Exported by:</span></span>  <br/> |<span data-ttu-id="5be82-108">msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="5be82-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="5be82-109">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="5be82-109">Called by:</span></span>  <br/> |<span data-ttu-id="5be82-110">Cliente</span><span class="sxs-lookup"><span data-stu-id="5be82-110">Client</span></span>  <br/> |
|<span data-ttu-id="5be82-111">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="5be82-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="5be82-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="5be82-112">Outlook</span></span>  <br/> |
   
```cpp
BOOL GetDefCachedModeDownloadPubFoldFavs(BOOL *pfPolicy); 

```

## <a name="parameters"></a><span data-ttu-id="5be82-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5be82-113">Parameters</span></span>

 <span data-ttu-id="5be82-114">_pfPolicy_</span><span class="sxs-lookup"><span data-stu-id="5be82-114">_pfPolicy_</span></span>
  
> <span data-ttu-id="5be82-115">bota **true** se o valor de retorno é imposto por política, **false** se não for.</span><span class="sxs-lookup"><span data-stu-id="5be82-115">[out] **true** if the return value is enforced by policy, **false** if it is not.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="5be82-116">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="5be82-116">Return values</span></span>

 <span data-ttu-id="5be82-117">**verdadeiro**</span><span class="sxs-lookup"><span data-stu-id="5be82-117">**true**</span></span>
  
- <span data-ttu-id="5be82-118">O cache está habilitado.</span><span class="sxs-lookup"><span data-stu-id="5be82-118">Caching is enabled.</span></span>
    
 <span data-ttu-id="5be82-119">**false**</span><span class="sxs-lookup"><span data-stu-id="5be82-119">**false**</span></span>
  
- <span data-ttu-id="5be82-120">O armazenamento em cache está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="5be82-120">Caching is disabled.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5be82-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="5be82-121">See also</span></span>



[<span data-ttu-id="5be82-122">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="5be82-122">GetDefCachedMode</span></span>](getdefcachedmode.md)

