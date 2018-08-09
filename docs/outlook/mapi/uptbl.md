---
title: UPTBL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 39d9ad3b-ff4b-8378-a3ac-d5621c7ef7f1
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 70d23bebfda10339ffb05f573c8c309a44f09d7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770706"
---
# <a name="uptbl"></a><span data-ttu-id="44a7a-103">UPTBL</span><span class="sxs-lookup"><span data-stu-id="44a7a-103">UPTBL</span></span>

<span data-ttu-id="44a7a-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="44a7a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="44a7a-105">Informações para carregar o conteúdo de uma pasta durante a [carregar o estado da tabela](upload-table-state.md).</span><span class="sxs-lookup"><span data-stu-id="44a7a-105">Information for uploading the contents of a folder during the [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="44a7a-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="44a7a-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="44a7a-107">Members</span><span class="sxs-lookup"><span data-stu-id="44a7a-107">Members</span></span>

<span data-ttu-id="44a7a-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="44a7a-108">_ulFlags_</span></span>
  
> <span data-ttu-id="44a7a-109">[in] Sinalizadores para determinar o comportamento apropriado durante o carregamento.</span><span class="sxs-lookup"><span data-stu-id="44a7a-109">[in] Flags to determine the appropriate behavior during the upload.</span></span>
    
  - <span data-ttu-id="44a7a-110">UPT_OK</span><span class="sxs-lookup"><span data-stu-id="44a7a-110">UPT_OK</span></span>
    
    - <span data-ttu-id="44a7a-111">[in] Carregamento foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="44a7a-111">[in] Upload was successful.</span></span> <span data-ttu-id="44a7a-112">O cliente define esta após carregar o conteúdo da pasta no servidor.</span><span class="sxs-lookup"><span data-stu-id="44a7a-112">The client sets this after uploading the folder contents to the server.</span></span>
    
<span data-ttu-id="44a7a-113">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="44a7a-113">_pstmReserved_</span></span>
  
> <span data-ttu-id="44a7a-114">[out] Este membro é reservado para uso interno do Outlook e não é suportado.</span><span class="sxs-lookup"><span data-stu-id="44a7a-114">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="44a7a-115">_pszName_</span><span class="sxs-lookup"><span data-stu-id="44a7a-115">_pszName_</span></span>
  
> <span data-ttu-id="44a7a-116">[out] Nome da pasta.</span><span class="sxs-lookup"><span data-stu-id="44a7a-116">[out] Name of the folder.</span></span>
    
<span data-ttu-id="44a7a-117">_feid_</span><span class="sxs-lookup"><span data-stu-id="44a7a-117">_feid_</span></span>
  
> <span data-ttu-id="44a7a-118">[out] Identificação de entrada da pasta.</span><span class="sxs-lookup"><span data-stu-id="44a7a-118">[out] Entry ID of the folder.</span></span>
    
<span data-ttu-id="44a7a-119">_uintReserved_</span><span class="sxs-lookup"><span data-stu-id="44a7a-119">_uintReserved_</span></span>
  
> <span data-ttu-id="44a7a-120">[out] Este membro é reservado para uso interno do Outlook e não é suportado.</span><span class="sxs-lookup"><span data-stu-id="44a7a-120">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="44a7a-121">_rgte_</span><span class="sxs-lookup"><span data-stu-id="44a7a-121">_rgte_</span></span>
  
> <span data-ttu-id="44a7a-122">[out] Estrutura para armazenar as seguintes informações para itens de normais (ou não ocultos) e os itens associados (ou ocultos) na pasta: _rgte [0]_ é para itens normais e _rgte [1]_ é para itens associados.</span><span class="sxs-lookup"><span data-stu-id="44a7a-122">[out] Structure to hold the following information for normal (or non-hidden) items and associated (or hidden) items in the folder:  _rgte[0]_ is for normal items, and  _rgte[1]_ is for associated items.</span></span> 
    
   - <span data-ttu-id="44a7a-123">o número de itens de novos ou modificados</span><span class="sxs-lookup"><span data-stu-id="44a7a-123">the number of new or modified items</span></span>
   - <span data-ttu-id="44a7a-124">o número de itens de leitura</span><span class="sxs-lookup"><span data-stu-id="44a7a-124">the number of read items</span></span> 
   - <span data-ttu-id="44a7a-125">o número de itens excluídos</span><span class="sxs-lookup"><span data-stu-id="44a7a-125">the number of deleted items</span></span>
    
 <span data-ttu-id="44a7a-126">_iEnt_</span><span class="sxs-lookup"><span data-stu-id="44a7a-126">_iEnt_</span></span>
  
> <span data-ttu-id="44a7a-127">[out] Índice para rastrear carregando o número de alterações especificado pelo _cEnt_.</span><span class="sxs-lookup"><span data-stu-id="44a7a-127">[out] Index to track uploading the number of changes specified by  _cEnt_.</span></span>
    
<span data-ttu-id="44a7a-128">_cEnt_</span><span class="sxs-lookup"><span data-stu-id="44a7a-128">_cEnt_</span></span>
  
> <span data-ttu-id="44a7a-129">[out] Número de alterações para a pasta.</span><span class="sxs-lookup"><span data-stu-id="44a7a-129">[out] Number of changes to the folder.</span></span>
    
<span data-ttu-id="44a7a-130">_pupmovHead_</span><span class="sxs-lookup"><span data-stu-id="44a7a-130">_pupmovHead_</span></span>
  
> <span data-ttu-id="44a7a-131">[out] Cadeia de estruturas [UPMOV](upmov.md) .</span><span class="sxs-lookup"><span data-stu-id="44a7a-131">[out] Chain of [UPMOV](upmov.md) structures.</span></span> 
    
<span data-ttu-id="44a7a-132">_Preservadas_</span><span class="sxs-lookup"><span data-stu-id="44a7a-132">_pReserved_</span></span>
  
> <span data-ttu-id="44a7a-133">[out] Este membro é reservado para uso interno do Outlook e não é suportado.</span><span class="sxs-lookup"><span data-stu-id="44a7a-133">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="44a7a-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="44a7a-134">See also</span></span>

- [<span data-ttu-id="44a7a-135">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="44a7a-135">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="44a7a-136">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="44a7a-136">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="44a7a-137">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="44a7a-137">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="44a7a-138">UPTBLE</span><span class="sxs-lookup"><span data-stu-id="44a7a-138">UPTBLE</span></span>](uptble.md)

