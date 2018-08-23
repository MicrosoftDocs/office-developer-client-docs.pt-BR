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
ms.openlocfilehash: 91a56acf4afc7453496fa89becd905184101c910
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591391"
---
# <a name="getdefcachedmode"></a><span data-ttu-id="db974-103">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="db974-103">GetDefCachedMode</span></span>

  
  
<span data-ttu-id="db974-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="db974-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="db974-105">Indica se o modo cache do Exchange para o armazenamento particular do Exchange está habilitado e, se isso é imposto pela diretiva.</span><span class="sxs-lookup"><span data-stu-id="db974-105">Indicates whether Cached Exchange Mode for the private Exchange store is enabled, and whether this is enforced by policy.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="db974-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="db974-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="db974-107">Exportá-los por:</span><span class="sxs-lookup"><span data-stu-id="db974-107">Exported by:</span></span>  <br/> |<span data-ttu-id="db974-108">Msmapi32</span><span class="sxs-lookup"><span data-stu-id="db974-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="db974-109">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="db974-109">Called by:</span></span>  <br/> |<span data-ttu-id="db974-110">Cliente</span><span class="sxs-lookup"><span data-stu-id="db974-110">Client</span></span>  <br/> |
|<span data-ttu-id="db974-111">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="db974-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="db974-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="db974-112">Outlook</span></span>  <br/> |
   
```cpp
BOOL GetDefCachedMode(BOOL *pfPolicy); 

```

## <a name="parameters"></a><span data-ttu-id="db974-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="db974-113">Parameters</span></span>

 <span data-ttu-id="db974-114">_pfPolicy_</span><span class="sxs-lookup"><span data-stu-id="db974-114">_pfPolicy_</span></span>
  
> <span data-ttu-id="db974-115">[out] **true** se o valor de retorno é imposto pela diretiva, **false** caso não seja.</span><span class="sxs-lookup"><span data-stu-id="db974-115">[out] **true** if the return value is enforced by policy, **false** if it is not.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="db974-116">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="db974-116">Return values</span></span>

 <span data-ttu-id="db974-117">**True**</span><span class="sxs-lookup"><span data-stu-id="db974-117">**true**</span></span>
  
- <span data-ttu-id="db974-118">Armazenamento em cache está habilitado.</span><span class="sxs-lookup"><span data-stu-id="db974-118">Caching is enabled.</span></span>
    
 <span data-ttu-id="db974-119">**False**</span><span class="sxs-lookup"><span data-stu-id="db974-119">**false**</span></span>
  
- <span data-ttu-id="db974-120">O cache é desabilitado.</span><span class="sxs-lookup"><span data-stu-id="db974-120">Caching is disabled.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="db974-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="db974-121">See also</span></span>



[<span data-ttu-id="db974-122">GetDefCachedModeDownloadPubFoldFavs</span><span class="sxs-lookup"><span data-stu-id="db974-122">GetDefCachedModeDownloadPubFoldFavs</span></span>](getdefcachedmodedownloadpubfoldfavs.md)

