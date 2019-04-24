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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329705"
---
# <a name="uptble"></a><span data-ttu-id="8f9b0-103">UPTBLE</span><span class="sxs-lookup"><span data-stu-id="8f9b0-103">UPTBLE</span></span>

<span data-ttu-id="8f9b0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8f9b0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8f9b0-105">Informações estendidas para carregar o conteúdo de uma pasta durante o [estado de carregamento da tabela](upload-table-state.md).</span><span class="sxs-lookup"><span data-stu-id="8f9b0-105">Extended information for uploading the contents of a folder during the [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="8f9b0-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="8f9b0-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="8f9b0-107">Membros</span><span class="sxs-lookup"><span data-stu-id="8f9b0-107">Members</span></span>

 <span data-ttu-id="8f9b0-108">_iEntMod_</span><span class="sxs-lookup"><span data-stu-id="8f9b0-108">_iEntMod_</span></span>
  
>  <span data-ttu-id="8f9b0-109">bota Index para acompanhar o carregamento do número _cEntMod_ de itens novos ou modificados.</span><span class="sxs-lookup"><span data-stu-id="8f9b0-109">[out] Index to track uploading the  _cEntMod_ number of new or modified items.</span></span> 
    
 <span data-ttu-id="8f9b0-110">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="8f9b0-110">_cEntMod_</span></span>
  
>  <span data-ttu-id="8f9b0-111">bota Número de itens novos ou modificados na pasta.</span><span class="sxs-lookup"><span data-stu-id="8f9b0-111">[out] Number of new or modified items in the folder.</span></span> 
    
 <span data-ttu-id="8f9b0-112">_iEntRead_</span><span class="sxs-lookup"><span data-stu-id="8f9b0-112">_iEntRead_</span></span>
  
>  <span data-ttu-id="8f9b0-113">bota Index para acompanhar o carregamento do número de itens de leitura _cEntRead_ .</span><span class="sxs-lookup"><span data-stu-id="8f9b0-113">[out] Index to track uploading the number of  _cEntRead_ read items.</span></span> 
    
 <span data-ttu-id="8f9b0-114">_cEntRead_</span><span class="sxs-lookup"><span data-stu-id="8f9b0-114">_cEntRead_</span></span>
  
>  <span data-ttu-id="8f9b0-115">bota Número de itens lidos na pasta.</span><span class="sxs-lookup"><span data-stu-id="8f9b0-115">[out] Number of read items in the folder.</span></span> 
    
 <span data-ttu-id="8f9b0-116">_iEntDel_</span><span class="sxs-lookup"><span data-stu-id="8f9b0-116">_iEntDel_</span></span>
  
>  <span data-ttu-id="8f9b0-117">bota Index para acompanhar o carregamento do número de itens excluídos do _cEntDel_ .</span><span class="sxs-lookup"><span data-stu-id="8f9b0-117">[out] Index to track uploading the number of  _cEntDel_ deleted items.</span></span> 
    
 <span data-ttu-id="8f9b0-118">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="8f9b0-118">_cEntDel_</span></span>
  
>  <span data-ttu-id="8f9b0-119">bota Número de itens excluídos na pasta.</span><span class="sxs-lookup"><span data-stu-id="8f9b0-119">[out] Number of deleted items in the folder.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="8f9b0-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="8f9b0-120">See also</span></span>

- [<span data-ttu-id="8f9b0-121">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="8f9b0-121">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="8f9b0-122">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="8f9b0-122">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="8f9b0-123">UPTBL</span><span class="sxs-lookup"><span data-stu-id="8f9b0-123">UPTBL</span></span>](uptbl.md)

