---
title: UPTBLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f7fcb385-186d-d5fe-7104-fe0af09d5768
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: d0b440f01aad7078ed76cd37d36c5ad506215438
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413837"
---
# <a name="uptble"></a><span data-ttu-id="45b39-103">UPTBLE</span><span class="sxs-lookup"><span data-stu-id="45b39-103">UPTBLE</span></span>

<span data-ttu-id="45b39-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="45b39-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="45b39-105">Informações estendidas para carregar o conteúdo de uma pasta durante o [estado da tabela de carregamento.](upload-table-state.md)</span><span class="sxs-lookup"><span data-stu-id="45b39-105">Extended information for uploading the contents of a folder during the [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="45b39-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="45b39-106">Quick info</span></span>

```cpp
struct UPTBLE 
{ 
    UINTiEntMod; 
    UINTcEntMod; 
    UINTiEntRead; 
    UINTcEntRead; 
    UINTiEntDel; 
    UINTcEntDel; 
};
```

## <a name="members"></a><span data-ttu-id="45b39-107">Membros</span><span class="sxs-lookup"><span data-stu-id="45b39-107">Members</span></span>

 <span data-ttu-id="45b39-108">_iEntMod_</span><span class="sxs-lookup"><span data-stu-id="45b39-108">_iEntMod_</span></span>
  
>  <span data-ttu-id="45b39-109">[out] Index to tracking the  _cEntMod_ number of new or modified items.</span><span class="sxs-lookup"><span data-stu-id="45b39-109">[out] Index to track uploading the  _cEntMod_ number of new or modified items.</span></span> 
    
 <span data-ttu-id="45b39-110">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="45b39-110">_cEntMod_</span></span>
  
>  <span data-ttu-id="45b39-111">[out] Número de itens novos ou modificados na pasta.</span><span class="sxs-lookup"><span data-stu-id="45b39-111">[out] Number of new or modified items in the folder.</span></span> 
    
 <span data-ttu-id="45b39-112">_iEntRead_</span><span class="sxs-lookup"><span data-stu-id="45b39-112">_iEntRead_</span></span>
  
>  <span data-ttu-id="45b39-113">[out] Index to track uploading the number of  _cEntRead_ read items.</span><span class="sxs-lookup"><span data-stu-id="45b39-113">[out] Index to track uploading the number of  _cEntRead_ read items.</span></span> 
    
 <span data-ttu-id="45b39-114">_cEntRead_</span><span class="sxs-lookup"><span data-stu-id="45b39-114">_cEntRead_</span></span>
  
>  <span data-ttu-id="45b39-115">[out] Número de itens de leitura na pasta.</span><span class="sxs-lookup"><span data-stu-id="45b39-115">[out] Number of read items in the folder.</span></span> 
    
 <span data-ttu-id="45b39-116">_iEntDel_</span><span class="sxs-lookup"><span data-stu-id="45b39-116">_iEntDel_</span></span>
  
>  <span data-ttu-id="45b39-117">[out] Index to track uploading the number of  _cEntDel_ deleted items.</span><span class="sxs-lookup"><span data-stu-id="45b39-117">[out] Index to track uploading the number of  _cEntDel_ deleted items.</span></span> 
    
 <span data-ttu-id="45b39-118">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="45b39-118">_cEntDel_</span></span>
  
>  <span data-ttu-id="45b39-119">[out] Número de itens excluídos na pasta.</span><span class="sxs-lookup"><span data-stu-id="45b39-119">[out] Number of deleted items in the folder.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="45b39-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="45b39-120">See also</span></span>

- [<span data-ttu-id="45b39-121">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="45b39-121">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="45b39-122">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="45b39-122">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="45b39-123">UPTBL</span><span class="sxs-lookup"><span data-stu-id="45b39-123">UPTBL</span></span>](uptbl.md)

