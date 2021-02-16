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
ms.openlocfilehash: 8e8a6ac07e14af52337b6e280fa58274df453c65
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412741"
---
# <a name="getdefcachedmode"></a><span data-ttu-id="a94be-103">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="a94be-103">GetDefCachedMode</span></span>

  
  
<span data-ttu-id="a94be-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a94be-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a94be-105">Indica se o Modo Cache do Exchange para o armazenamento particular do Exchange está habilitado e se isso é imposto pela política.</span><span class="sxs-lookup"><span data-stu-id="a94be-105">Indicates whether Cached Exchange Mode for the private Exchange store is enabled, and whether this is enforced by policy.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a94be-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="a94be-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a94be-107">Exportado por:</span><span class="sxs-lookup"><span data-stu-id="a94be-107">Exported by:</span></span>  <br/> |<span data-ttu-id="a94be-108">msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="a94be-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="a94be-109">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="a94be-109">Called by:</span></span>  <br/> |<span data-ttu-id="a94be-110">Cliente</span><span class="sxs-lookup"><span data-stu-id="a94be-110">Client</span></span>  <br/> |
|<span data-ttu-id="a94be-111">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="a94be-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="a94be-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="a94be-112">Outlook</span></span>  <br/> |
   
```cpp
BOOL GetDefCachedMode(BOOL *pfPolicy); 

```

## <a name="parameters"></a><span data-ttu-id="a94be-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a94be-113">Parameters</span></span>

 <span data-ttu-id="a94be-114">_pfPolicy_</span><span class="sxs-lookup"><span data-stu-id="a94be-114">_pfPolicy_</span></span>
  
> <span data-ttu-id="a94be-115">[out] **true** se o valor de retorno for imposto pela política, **false** se não for.</span><span class="sxs-lookup"><span data-stu-id="a94be-115">[out] **true** if the return value is enforced by policy, **false** if it is not.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="a94be-116">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a94be-116">Return values</span></span>

 <span data-ttu-id="a94be-117">**verdadeiro**</span><span class="sxs-lookup"><span data-stu-id="a94be-117">**true**</span></span>
  
- <span data-ttu-id="a94be-118">O cache está habilitado.</span><span class="sxs-lookup"><span data-stu-id="a94be-118">Caching is enabled.</span></span>
    
 <span data-ttu-id="a94be-119">**falso**</span><span class="sxs-lookup"><span data-stu-id="a94be-119">**false**</span></span>
  
- <span data-ttu-id="a94be-120">O cache está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="a94be-120">Caching is disabled.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a94be-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="a94be-121">See also</span></span>



[<span data-ttu-id="a94be-122">GetDefCachedModeDownloadPubFoldFavs</span><span class="sxs-lookup"><span data-stu-id="a94be-122">GetDefCachedModeDownloadPubFoldFavs</span></span>](getdefcachedmodedownloadpubfoldfavs.md)

