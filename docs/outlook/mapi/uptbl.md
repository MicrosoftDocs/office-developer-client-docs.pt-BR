---
title: UPTBL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 39d9ad3b-ff4b-8378-a3ac-d5621c7ef7f1
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: b401f54df020fb6553cbdcc5b85206ee422a8429
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438110"
---
# <a name="uptbl"></a><span data-ttu-id="e5b1c-103">UPTBL</span><span class="sxs-lookup"><span data-stu-id="e5b1c-103">UPTBL</span></span>

<span data-ttu-id="e5b1c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e5b1c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e5b1c-105">Informações para carregar o conteúdo de uma pasta durante o estado [da tabela de carregamento.](upload-table-state.md)</span><span class="sxs-lookup"><span data-stu-id="e5b1c-105">Information for uploading the contents of a folder during the [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e5b1c-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="e5b1c-106">Quick info</span></span>

```cpp
struct UPTBL 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    LPSTR pszName; 
    FEID feid; 
    UINT uintReserved; 
    UPTBLE rgte[2]; 
    UINT iEnt; 
    UINT cEnt; 
    PUPMOV pupmovHead; 
    void* pReserved; 
};
```

## <a name="members"></a><span data-ttu-id="e5b1c-107">Membros</span><span class="sxs-lookup"><span data-stu-id="e5b1c-107">Members</span></span>

<span data-ttu-id="e5b1c-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e5b1c-108">_ulFlags_</span></span>
  
> <span data-ttu-id="e5b1c-109">[in] Sinalizadores para determinar o comportamento apropriado durante o carregamento.</span><span class="sxs-lookup"><span data-stu-id="e5b1c-109">[in] Flags to determine the appropriate behavior during the upload.</span></span>
    
  - <span data-ttu-id="e5b1c-110">UPT_OK</span><span class="sxs-lookup"><span data-stu-id="e5b1c-110">UPT_OK</span></span>
    
    - <span data-ttu-id="e5b1c-111">[in] O carregamento foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="e5b1c-111">[in] Upload was successful.</span></span> <span data-ttu-id="e5b1c-112">O cliente define isso depois de carregar o conteúdo da pasta no servidor.</span><span class="sxs-lookup"><span data-stu-id="e5b1c-112">The client sets this after uploading the folder contents to the server.</span></span>
    
<span data-ttu-id="e5b1c-113">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="e5b1c-113">_pstmReserved_</span></span>
  
> <span data-ttu-id="e5b1c-114">[uto] Esse membro é reservado para uso interno do Outlook e não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="e5b1c-114">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="e5b1c-115">_pszName_</span><span class="sxs-lookup"><span data-stu-id="e5b1c-115">_pszName_</span></span>
  
> <span data-ttu-id="e5b1c-116">[out] Nome da pasta.</span><span class="sxs-lookup"><span data-stu-id="e5b1c-116">[out] Name of the folder.</span></span>
    
<span data-ttu-id="e5b1c-117">_feid_</span><span class="sxs-lookup"><span data-stu-id="e5b1c-117">_feid_</span></span>
  
> <span data-ttu-id="e5b1c-118">[out] ID da entrada da pasta.</span><span class="sxs-lookup"><span data-stu-id="e5b1c-118">[out] Entry ID of the folder.</span></span>
    
<span data-ttu-id="e5b1c-119">_uintReserved_</span><span class="sxs-lookup"><span data-stu-id="e5b1c-119">_uintReserved_</span></span>
  
> <span data-ttu-id="e5b1c-120">[out] Esse membro é reservado para uso interno do Outlook e não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="e5b1c-120">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="e5b1c-121">_rgte_</span><span class="sxs-lookup"><span data-stu-id="e5b1c-121">_rgte_</span></span>
  
> <span data-ttu-id="e5b1c-122">[out] Estrutura para manter as seguintes informações para itens normais (ou não ocultos) e itens associados (ou ocultos) na pasta:  _rgte[0]_ é para itens normais e  _rgte[1]_ é para itens associados.</span><span class="sxs-lookup"><span data-stu-id="e5b1c-122">[out] Structure to hold the following information for normal (or non-hidden) items and associated (or hidden) items in the folder:  _rgte[0]_ is for normal items, and  _rgte[1]_ is for associated items.</span></span> 
    
   - <span data-ttu-id="e5b1c-123">o número de itens novos ou modificados</span><span class="sxs-lookup"><span data-stu-id="e5b1c-123">the number of new or modified items</span></span>
   - <span data-ttu-id="e5b1c-124">o número de itens lidos</span><span class="sxs-lookup"><span data-stu-id="e5b1c-124">the number of read items</span></span> 
   - <span data-ttu-id="e5b1c-125">o número de itens excluídos</span><span class="sxs-lookup"><span data-stu-id="e5b1c-125">the number of deleted items</span></span>
    
 <span data-ttu-id="e5b1c-126">_iEnt_</span><span class="sxs-lookup"><span data-stu-id="e5b1c-126">_iEnt_</span></span>
  
> <span data-ttu-id="e5b1c-127">[out] Index to track uploading the number of changes specified by  _cEnt_.</span><span class="sxs-lookup"><span data-stu-id="e5b1c-127">[out] Index to track uploading the number of changes specified by  _cEnt_.</span></span>
    
<span data-ttu-id="e5b1c-128">_cEnt_</span><span class="sxs-lookup"><span data-stu-id="e5b1c-128">_cEnt_</span></span>
  
> <span data-ttu-id="e5b1c-129">[out] Número de alterações na pasta.</span><span class="sxs-lookup"><span data-stu-id="e5b1c-129">[out] Number of changes to the folder.</span></span>
    
<span data-ttu-id="e5b1c-130">_entremovHead_</span><span class="sxs-lookup"><span data-stu-id="e5b1c-130">_pupmovHead_</span></span>
  
> <span data-ttu-id="e5b1c-131">[out] Cadeia de [estruturas UPMOV.](upmov.md)</span><span class="sxs-lookup"><span data-stu-id="e5b1c-131">[out] Chain of [UPMOV](upmov.md) structures.</span></span> 
    
<span data-ttu-id="e5b1c-132">_pReserved_</span><span class="sxs-lookup"><span data-stu-id="e5b1c-132">_pReserved_</span></span>
  
> <span data-ttu-id="e5b1c-133">[out] Esse membro é reservado para uso interno do Outlook e não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="e5b1c-133">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e5b1c-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="e5b1c-134">See also</span></span>

- [<span data-ttu-id="e5b1c-135">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="e5b1c-135">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="e5b1c-136">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="e5b1c-136">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="e5b1c-137">Constantes de MAPI</span><span class="sxs-lookup"><span data-stu-id="e5b1c-137">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="e5b1c-138">UPTBLE</span><span class="sxs-lookup"><span data-stu-id="e5b1c-138">UPTBLE</span></span>](uptble.md)

