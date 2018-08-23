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
ms.openlocfilehash: ced6f2c6540e04a0bb4945ff98c4fda520322f03
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581724"
---
# <a name="getdefcachedmodedownloadpubfoldfavs"></a><span data-ttu-id="156e9-103">GetDefCachedModeDownloadPubFoldFavs</span><span class="sxs-lookup"><span data-stu-id="156e9-103">GetDefCachedModeDownloadPubFoldFavs</span></span>

  
  
<span data-ttu-id="156e9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="156e9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="156e9-105">Indica se o modo cache do Exchange para a pasta de **Pasta pública Favoritos** está habilitado e, se isso é imposto pela diretiva.</span><span class="sxs-lookup"><span data-stu-id="156e9-105">Indicates whether Cached Exchange Mode for the **Public Folder Favorites** folder is enabled, and whether this is enforced by policy.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="156e9-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="156e9-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="156e9-107">Exportá-los por:</span><span class="sxs-lookup"><span data-stu-id="156e9-107">Exported by:</span></span>  <br/> |<span data-ttu-id="156e9-108">Msmapi32</span><span class="sxs-lookup"><span data-stu-id="156e9-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="156e9-109">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="156e9-109">Called by:</span></span>  <br/> |<span data-ttu-id="156e9-110">Cliente</span><span class="sxs-lookup"><span data-stu-id="156e9-110">Client</span></span>  <br/> |
|<span data-ttu-id="156e9-111">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="156e9-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="156e9-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="156e9-112">Outlook</span></span>  <br/> |
   
```cpp
BOOL GetDefCachedModeDownloadPubFoldFavs(BOOL *pfPolicy); 

```

## <a name="parameters"></a><span data-ttu-id="156e9-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="156e9-113">Parameters</span></span>

 <span data-ttu-id="156e9-114">_pfPolicy_</span><span class="sxs-lookup"><span data-stu-id="156e9-114">_pfPolicy_</span></span>
  
> <span data-ttu-id="156e9-115">[out] **true** se o valor de retorno é imposto pela diretiva, **false** caso não seja.</span><span class="sxs-lookup"><span data-stu-id="156e9-115">[out] **true** if the return value is enforced by policy, **false** if it is not.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="156e9-116">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="156e9-116">Return values</span></span>

 <span data-ttu-id="156e9-117">**True**</span><span class="sxs-lookup"><span data-stu-id="156e9-117">**true**</span></span>
  
- <span data-ttu-id="156e9-118">Armazenamento em cache está habilitado.</span><span class="sxs-lookup"><span data-stu-id="156e9-118">Caching is enabled.</span></span>
    
 <span data-ttu-id="156e9-119">**False**</span><span class="sxs-lookup"><span data-stu-id="156e9-119">**false**</span></span>
  
- <span data-ttu-id="156e9-120">O cache é desabilitado.</span><span class="sxs-lookup"><span data-stu-id="156e9-120">Caching is disabled.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="156e9-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="156e9-121">See also</span></span>



[<span data-ttu-id="156e9-122">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="156e9-122">GetDefCachedMode</span></span>](getdefcachedmode.md)

