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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299703"
---
# <a name="getdefcachedmode"></a><span data-ttu-id="0611f-103">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="0611f-103">GetDefCachedMode</span></span>

  
  
<span data-ttu-id="0611f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0611f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0611f-105">Indica se o modo cache do Exchange para o repositório particular do Exchange está habilitado e se ele é imposto pela política.</span><span class="sxs-lookup"><span data-stu-id="0611f-105">Indicates whether Cached Exchange Mode for the private Exchange store is enabled, and whether this is enforced by policy.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="0611f-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="0611f-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0611f-107">Exportado por:</span><span class="sxs-lookup"><span data-stu-id="0611f-107">Exported by:</span></span>  <br/> |<span data-ttu-id="0611f-108">msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="0611f-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="0611f-109">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="0611f-109">Called by:</span></span>  <br/> |<span data-ttu-id="0611f-110">Cliente</span><span class="sxs-lookup"><span data-stu-id="0611f-110">Client</span></span>  <br/> |
|<span data-ttu-id="0611f-111">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="0611f-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="0611f-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="0611f-112">Outlook</span></span>  <br/> |
   
```cpp
BOOL GetDefCachedMode(BOOL *pfPolicy); 

```

## <a name="parameters"></a><span data-ttu-id="0611f-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0611f-113">Parameters</span></span>

 <span data-ttu-id="0611f-114">_pfPolicy_</span><span class="sxs-lookup"><span data-stu-id="0611f-114">_pfPolicy_</span></span>
  
> <span data-ttu-id="0611f-115">bota **true** se o valor de retorno é imposto por política, **false** se não for.</span><span class="sxs-lookup"><span data-stu-id="0611f-115">[out] **true** if the return value is enforced by policy, **false** if it is not.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="0611f-116">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="0611f-116">Return values</span></span>

 <span data-ttu-id="0611f-117">**verdadeiro**</span><span class="sxs-lookup"><span data-stu-id="0611f-117">**true**</span></span>
  
- <span data-ttu-id="0611f-118">O cache está habilitado.</span><span class="sxs-lookup"><span data-stu-id="0611f-118">Caching is enabled.</span></span>
    
 <span data-ttu-id="0611f-119">**false**</span><span class="sxs-lookup"><span data-stu-id="0611f-119">**false**</span></span>
  
- <span data-ttu-id="0611f-120">O armazenamento em cache está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="0611f-120">Caching is disabled.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0611f-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="0611f-121">See also</span></span>



[<span data-ttu-id="0611f-122">GetDefCachedModeDownloadPubFoldFavs</span><span class="sxs-lookup"><span data-stu-id="0611f-122">GetDefCachedModeDownloadPubFoldFavs</span></span>](getdefcachedmodedownloadpubfoldfavs.md)

