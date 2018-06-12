---
title: GetDefCachedModeDownloadPubFoldFavs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2dd95561-ed8f-8a3b-6532-b53556f16666
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: cb93d9ae4e6660c208d74e43bb26be4dbd55f4e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766681"
---
# <a name="getdefcachedmodedownloadpubfoldfavs"></a><span data-ttu-id="b7391-103">GetDefCachedModeDownloadPubFoldFavs</span><span class="sxs-lookup"><span data-stu-id="b7391-103">GetDefCachedModeDownloadPubFoldFavs</span></span>

  
  
<span data-ttu-id="b7391-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b7391-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b7391-105">Indica se o modo cache do Exchange para a pasta de **Pasta pública Favoritos** está habilitado e, se isso é imposto pela diretiva.</span><span class="sxs-lookup"><span data-stu-id="b7391-105">Indicates whether Cached Exchange Mode for the **Public Folder Favorites** folder is enabled, and whether this is enforced by policy.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="b7391-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="b7391-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b7391-107">Exportá-los por:</span><span class="sxs-lookup"><span data-stu-id="b7391-107">Exported by:</span></span>  <br/> |<span data-ttu-id="b7391-108">Msmapi32</span><span class="sxs-lookup"><span data-stu-id="b7391-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="b7391-109">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="b7391-109">Called by:</span></span>  <br/> |<span data-ttu-id="b7391-110">Cliente</span><span class="sxs-lookup"><span data-stu-id="b7391-110">Client</span></span>  <br/> |
|<span data-ttu-id="b7391-111">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="b7391-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="b7391-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="b7391-112">Outlook</span></span>  <br/> |
   
```cpp
BOOL GetDefCachedModeDownloadPubFoldFavs(BOOL *pfPolicy); 

```

## <a name="parameters"></a><span data-ttu-id="b7391-113">Par�metros</span><span class="sxs-lookup"><span data-stu-id="b7391-113">Parameters</span></span>

 <span data-ttu-id="b7391-114">_pfPolicy_</span><span class="sxs-lookup"><span data-stu-id="b7391-114">_pfPolicy_</span></span>
  
> <span data-ttu-id="b7391-115">[out] **true** se o valor de retorno é imposto pela diretiva, **false** caso não seja.</span><span class="sxs-lookup"><span data-stu-id="b7391-115">[out] **true** if the return value is enforced by policy, **false** if it is not.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="b7391-116">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="b7391-116">Return values</span></span>

 <span data-ttu-id="b7391-117">**True**</span><span class="sxs-lookup"><span data-stu-id="b7391-117">**true**</span></span>
  
- <span data-ttu-id="b7391-118">Armazenamento em cache está habilitado.</span><span class="sxs-lookup"><span data-stu-id="b7391-118">Caching is enabled.</span></span>
    
 <span data-ttu-id="b7391-119">**False**</span><span class="sxs-lookup"><span data-stu-id="b7391-119">**false**</span></span>
  
- <span data-ttu-id="b7391-120">O cache é desabilitado.</span><span class="sxs-lookup"><span data-stu-id="b7391-120">Caching is disabled.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b7391-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="b7391-121">See also</span></span>



[<span data-ttu-id="b7391-122">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="b7391-122">GetDefCachedMode</span></span>](getdefcachedmode.md)

