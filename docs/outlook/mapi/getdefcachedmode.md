---
title: GetDefCachedMode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 325b6b47-b6a6-503e-e9bb-65ef7b73d659
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7595fac4346a537eed86550432f56a761c27c0ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766682"
---
# <a name="getdefcachedmode"></a><span data-ttu-id="ca5a3-103">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="ca5a3-103">GetDefCachedMode</span></span>

  
  
<span data-ttu-id="ca5a3-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ca5a3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ca5a3-105">Indica se o modo cache do Exchange para o armazenamento particular do Exchange está habilitado e, se isso é imposto pela diretiva.</span><span class="sxs-lookup"><span data-stu-id="ca5a3-105">Indicates whether Cached Exchange Mode for the private Exchange store is enabled, and whether this is enforced by policy.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ca5a3-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="ca5a3-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ca5a3-107">Exportá-los por:</span><span class="sxs-lookup"><span data-stu-id="ca5a3-107">Exported by:</span></span>  <br/> |<span data-ttu-id="ca5a3-108">Msmapi32</span><span class="sxs-lookup"><span data-stu-id="ca5a3-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="ca5a3-109">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="ca5a3-109">Called by:</span></span>  <br/> |<span data-ttu-id="ca5a3-110">Cliente</span><span class="sxs-lookup"><span data-stu-id="ca5a3-110">Client</span></span>  <br/> |
|<span data-ttu-id="ca5a3-111">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="ca5a3-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="ca5a3-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="ca5a3-112">Outlook</span></span>  <br/> |
   
```cpp
BOOL GetDefCachedMode(BOOL *pfPolicy); 

```

## <a name="parameters"></a><span data-ttu-id="ca5a3-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ca5a3-113">Parameters</span></span>

 <span data-ttu-id="ca5a3-114">_pfPolicy_</span><span class="sxs-lookup"><span data-stu-id="ca5a3-114">_pfPolicy_</span></span>
  
> <span data-ttu-id="ca5a3-115">[out] **true** se o valor de retorno é imposto pela diretiva, **false** caso não seja.</span><span class="sxs-lookup"><span data-stu-id="ca5a3-115">[out] **true** if the return value is enforced by policy, **false** if it is not.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="ca5a3-116">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="ca5a3-116">Return values</span></span>

 <span data-ttu-id="ca5a3-117">**True**</span><span class="sxs-lookup"><span data-stu-id="ca5a3-117">**true**</span></span>
  
- <span data-ttu-id="ca5a3-118">Armazenamento em cache está habilitado.</span><span class="sxs-lookup"><span data-stu-id="ca5a3-118">Caching is enabled.</span></span>
    
 <span data-ttu-id="ca5a3-119">**False**</span><span class="sxs-lookup"><span data-stu-id="ca5a3-119">**false**</span></span>
  
- <span data-ttu-id="ca5a3-120">O cache é desabilitado.</span><span class="sxs-lookup"><span data-stu-id="ca5a3-120">Caching is disabled.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ca5a3-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="ca5a3-121">See also</span></span>



[<span data-ttu-id="ca5a3-122">GetDefCachedModeDownloadPubFoldFavs</span><span class="sxs-lookup"><span data-stu-id="ca5a3-122">GetDefCachedModeDownloadPubFoldFavs</span></span>](getdefcachedmodedownloadpubfoldfavs.md)

