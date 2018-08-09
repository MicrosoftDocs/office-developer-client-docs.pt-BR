---
title: UPTBLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f7fcb385-186d-d5fe-7104-fe0af09d5768
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 62c18ac609547563ad0e98cbd914866e05888ac8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770692"
---
# <a name="uptble"></a><span data-ttu-id="e2fb4-103">UPTBLE</span><span class="sxs-lookup"><span data-stu-id="e2fb4-103">UPTBLE</span></span>

<span data-ttu-id="e2fb4-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e2fb4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e2fb4-105">Informações para carregar o conteúdo de uma pasta durante o [estado da tabela de carregar](upload-table-state.md)estendidas.</span><span class="sxs-lookup"><span data-stu-id="e2fb4-105">Extended information for uploading the contents of a folder during the [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e2fb4-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="e2fb4-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="e2fb4-107">Members</span><span class="sxs-lookup"><span data-stu-id="e2fb4-107">Members</span></span>

 <span data-ttu-id="e2fb4-108">_iEntMod_</span><span class="sxs-lookup"><span data-stu-id="e2fb4-108">_iEntMod_</span></span>
  
>  <span data-ttu-id="e2fb4-109">[out] Índice para controlar o carregamento _cEntMod_ número de itens de novos ou modificados.</span><span class="sxs-lookup"><span data-stu-id="e2fb4-109">[out] Index to track uploading the  _cEntMod_ number of new or modified items.</span></span> 
    
 <span data-ttu-id="e2fb4-110">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="e2fb4-110">_cEntMod_</span></span>
  
>  <span data-ttu-id="e2fb4-111">[out] Número de itens de novos ou modificados na pasta.</span><span class="sxs-lookup"><span data-stu-id="e2fb4-111">[out] Number of new or modified items in the folder.</span></span> 
    
 <span data-ttu-id="e2fb4-112">_iEntRead_</span><span class="sxs-lookup"><span data-stu-id="e2fb4-112">_iEntRead_</span></span>
  
>  <span data-ttu-id="e2fb4-113">[out] Índice para acompanhar carregando o número de _cEntRead_ ler itens.</span><span class="sxs-lookup"><span data-stu-id="e2fb4-113">[out] Index to track uploading the number of  _cEntRead_ read items.</span></span> 
    
 <span data-ttu-id="e2fb4-114">_cEntRead_</span><span class="sxs-lookup"><span data-stu-id="e2fb4-114">_cEntRead_</span></span>
  
>  <span data-ttu-id="e2fb4-115">[out] Número de itens de leitura na pasta.</span><span class="sxs-lookup"><span data-stu-id="e2fb4-115">[out] Number of read items in the folder.</span></span> 
    
 <span data-ttu-id="e2fb4-116">_iEntDel_</span><span class="sxs-lookup"><span data-stu-id="e2fb4-116">_iEntDel_</span></span>
  
>  <span data-ttu-id="e2fb4-117">[out] Itens excluídos do índice para rastrear carregando o número de _cEntDel_ .</span><span class="sxs-lookup"><span data-stu-id="e2fb4-117">[out] Index to track uploading the number of  _cEntDel_ deleted items.</span></span> 
    
 <span data-ttu-id="e2fb4-118">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="e2fb4-118">_cEntDel_</span></span>
  
>  <span data-ttu-id="e2fb4-119">[out] Número de itens excluídos na pasta.</span><span class="sxs-lookup"><span data-stu-id="e2fb4-119">[out] Number of deleted items in the folder.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="e2fb4-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="e2fb4-120">See also</span></span>

- [<span data-ttu-id="e2fb4-121">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="e2fb4-121">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="e2fb4-122">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="e2fb4-122">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="e2fb4-123">UPTBL</span><span class="sxs-lookup"><span data-stu-id="e2fb4-123">UPTBL</span></span>](uptbl.md)

