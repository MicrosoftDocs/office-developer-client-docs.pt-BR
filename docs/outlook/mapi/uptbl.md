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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338854"
---
# <a name="uptbl"></a><span data-ttu-id="1903a-103">UPTBL</span><span class="sxs-lookup"><span data-stu-id="1903a-103">UPTBL</span></span>

<span data-ttu-id="1903a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1903a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1903a-105">Informações para carregar o conteúdo de uma pasta durante o estado de [carregamento da tabela](upload-table-state.md).</span><span class="sxs-lookup"><span data-stu-id="1903a-105">Information for uploading the contents of a folder during the [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="1903a-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="1903a-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="1903a-107">Membros</span><span class="sxs-lookup"><span data-stu-id="1903a-107">Members</span></span>

<span data-ttu-id="1903a-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1903a-108">_ulFlags_</span></span>
  
> <span data-ttu-id="1903a-109">no Sinalizadores para determinar o comportamento apropriado durante o carregamento.</span><span class="sxs-lookup"><span data-stu-id="1903a-109">[in] Flags to determine the appropriate behavior during the upload.</span></span>
    
  - <span data-ttu-id="1903a-110">UPT_OK</span><span class="sxs-lookup"><span data-stu-id="1903a-110">UPT_OK</span></span>
    
    - <span data-ttu-id="1903a-111">no O upload foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="1903a-111">[in] Upload was successful.</span></span> <span data-ttu-id="1903a-112">O cliente define isso após carregar o conteúdo da pasta no servidor.</span><span class="sxs-lookup"><span data-stu-id="1903a-112">The client sets this after uploading the folder contents to the server.</span></span>
    
<span data-ttu-id="1903a-113">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="1903a-113">_pstmReserved_</span></span>
  
> <span data-ttu-id="1903a-114">[uto] Esse membro é reservado para uso interno do Outlook e não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="1903a-114">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="1903a-115">_pszName_</span><span class="sxs-lookup"><span data-stu-id="1903a-115">_pszName_</span></span>
  
> <span data-ttu-id="1903a-116">[out] Nome da pasta.</span><span class="sxs-lookup"><span data-stu-id="1903a-116">[out] Name of the folder.</span></span>
    
<span data-ttu-id="1903a-117">_feid_</span><span class="sxs-lookup"><span data-stu-id="1903a-117">_feid_</span></span>
  
> <span data-ttu-id="1903a-118">[out] ID da entrada da pasta.</span><span class="sxs-lookup"><span data-stu-id="1903a-118">[out] Entry ID of the folder.</span></span>
    
<span data-ttu-id="1903a-119">_uintReserved_</span><span class="sxs-lookup"><span data-stu-id="1903a-119">_uintReserved_</span></span>
  
> <span data-ttu-id="1903a-120">[out] Esse membro é reservado para uso interno do Outlook e não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="1903a-120">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="1903a-121">_rgte_</span><span class="sxs-lookup"><span data-stu-id="1903a-121">_rgte_</span></span>
  
> <span data-ttu-id="1903a-122">bota Estrutura para armazenar as seguintes informações para itens normais (ou não ocultos) e itens associados (ou ocultos) na pasta: _rgte [0]_ é para itens normais e _rgte [1]_ é para itens associados.</span><span class="sxs-lookup"><span data-stu-id="1903a-122">[out] Structure to hold the following information for normal (or non-hidden) items and associated (or hidden) items in the folder:  _rgte[0]_ is for normal items, and  _rgte[1]_ is for associated items.</span></span> 
    
   - <span data-ttu-id="1903a-123">o número de itens novos ou modificados</span><span class="sxs-lookup"><span data-stu-id="1903a-123">the number of new or modified items</span></span>
   - <span data-ttu-id="1903a-124">o número de itens de leitura</span><span class="sxs-lookup"><span data-stu-id="1903a-124">the number of read items</span></span> 
   - <span data-ttu-id="1903a-125">o número de itens excluídos</span><span class="sxs-lookup"><span data-stu-id="1903a-125">the number of deleted items</span></span>
    
 <span data-ttu-id="1903a-126">_iEnt_</span><span class="sxs-lookup"><span data-stu-id="1903a-126">_iEnt_</span></span>
  
> <span data-ttu-id="1903a-127">bota Índice para acompanhar o carregamento do número de alterações especificado por _cEnt_.</span><span class="sxs-lookup"><span data-stu-id="1903a-127">[out] Index to track uploading the number of changes specified by  _cEnt_.</span></span>
    
<span data-ttu-id="1903a-128">_cEnt_</span><span class="sxs-lookup"><span data-stu-id="1903a-128">_cEnt_</span></span>
  
> <span data-ttu-id="1903a-129">bota Número de alterações na pasta.</span><span class="sxs-lookup"><span data-stu-id="1903a-129">[out] Number of changes to the folder.</span></span>
    
<span data-ttu-id="1903a-130">_pupmovHead_</span><span class="sxs-lookup"><span data-stu-id="1903a-130">_pupmovHead_</span></span>
  
> <span data-ttu-id="1903a-131">bota Cadeia de estruturas [UPMOV](upmov.md) .</span><span class="sxs-lookup"><span data-stu-id="1903a-131">[out] Chain of [UPMOV](upmov.md) structures.</span></span> 
    
<span data-ttu-id="1903a-132">_Enquanto_</span><span class="sxs-lookup"><span data-stu-id="1903a-132">_pReserved_</span></span>
  
> <span data-ttu-id="1903a-133">[out] Esse membro é reservado para uso interno do Outlook e não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="1903a-133">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1903a-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="1903a-134">See also</span></span>

- [<span data-ttu-id="1903a-135">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="1903a-135">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="1903a-136">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="1903a-136">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="1903a-137">Constantes de MAPI</span><span class="sxs-lookup"><span data-stu-id="1903a-137">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="1903a-138">UPTBLE</span><span class="sxs-lookup"><span data-stu-id="1903a-138">UPTBLE</span></span>](uptble.md)

