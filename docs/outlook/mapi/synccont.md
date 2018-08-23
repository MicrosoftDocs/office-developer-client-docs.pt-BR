---
title: SYNCCONT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7b4307a3-5a8c-89bf-1113-2549556a7fe7
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: b1ab1bd4eb6badc75065ce54d009e034f0fc2b29
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584671"
---
# <a name="synccont"></a><span data-ttu-id="5564e-103">SYNCCONT</span><span class="sxs-lookup"><span data-stu-id="5564e-103">SYNCCONT</span></span>

<span data-ttu-id="5564e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5564e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5564e-105">Informações para sincronizar o conteúdo das pastas especificados em um armazenamento local com o servidor durante a [sincronizar o estado de conteúdo](synchronize-contents-state.md).</span><span class="sxs-lookup"><span data-stu-id="5564e-105">Information for synchronizing the contents of specified folders in a local store with the server during the [synchronize contents state](synchronize-contents-state.md).</span></span> <span data-ttu-id="5564e-106">Isso envolve apenas carregamento ou uma sincronização completa envolvendo um upload e download.</span><span class="sxs-lookup"><span data-stu-id="5564e-106">This involves just uploading, or a full synchronization involving an upload and then a download.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="5564e-107">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="5564e-107">Quick info</span></span>

```cpp
struct SYNCCONT 
{ 
   ULONG   ulFlags; 
   UINT   iEnt; 
   UINT   cEnt; 
   LPVOID    pvReserved; 
   LPSPropTagArray   ptagaReserved; 
   LPSSortOrderSet   psosReserved; 
};
```

## <a name="members"></a><span data-ttu-id="5564e-108">Members</span><span class="sxs-lookup"><span data-stu-id="5564e-108">Members</span></span>

<span data-ttu-id="5564e-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5564e-109">_ulFlags_</span></span>
  
> <span data-ttu-id="5564e-110">[in] Sinalizadores para determinar o comportamento apropriado durante a sincronização.</span><span class="sxs-lookup"><span data-stu-id="5564e-110">[in] Flags to determine the appropriate behavior during synchronization.</span></span>
    
  - <span data-ttu-id="5564e-111">UPC_OK</span><span class="sxs-lookup"><span data-stu-id="5564e-111">UPC_OK</span></span>
    
  - <span data-ttu-id="5564e-112">[in] Carregar ou sincronização completa foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="5564e-112">[in] Upload or full synchronization was successful.</span></span> <span data-ttu-id="5564e-113">O cliente define isso após a sincronização de informações com o servidor.</span><span class="sxs-lookup"><span data-stu-id="5564e-113">The client sets this after synchronizing information with the server.</span></span>
    
<span data-ttu-id="5564e-114">_iEnt_</span><span class="sxs-lookup"><span data-stu-id="5564e-114">_iEnt_</span></span>
  
> <span data-ttu-id="5564e-115">[out] Índice para controlar a sincronização de conteúdo no número de pastas especificadas pela _cEnt_.</span><span class="sxs-lookup"><span data-stu-id="5564e-115">[out] Index to track synchronizing the contents in the number of folders specified by  _cEnt_.</span></span>
    
<span data-ttu-id="5564e-116">_cEnt_</span><span class="sxs-lookup"><span data-stu-id="5564e-116">_cEnt_</span></span>
  
> <span data-ttu-id="5564e-117">[out] Número de pastas a serem replicadas.</span><span class="sxs-lookup"><span data-stu-id="5564e-117">[out] Number of folders to be replicated.</span></span>
    
<span data-ttu-id="5564e-118">_pvReserved_</span><span class="sxs-lookup"><span data-stu-id="5564e-118">_pvReserved_</span></span>
  
> <span data-ttu-id="5564e-119">Este membro é reservado para uso interno do Outlook e não é suportado.</span><span class="sxs-lookup"><span data-stu-id="5564e-119">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="5564e-120">_ptagaReserved_</span><span class="sxs-lookup"><span data-stu-id="5564e-120">_ptagaReserved_</span></span>
  
> <span data-ttu-id="5564e-121">Este membro é reservado para uso interno do Outlook e não é suportado.</span><span class="sxs-lookup"><span data-stu-id="5564e-121">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="5564e-122">_psosReserved_</span><span class="sxs-lookup"><span data-stu-id="5564e-122">_psosReserved_</span></span>
  
> <span data-ttu-id="5564e-123">Este membro é reservado para uso interno do Outlook e não é suportado.</span><span class="sxs-lookup"><span data-stu-id="5564e-123">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="5564e-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="5564e-124">See also</span></span>

- [<span data-ttu-id="5564e-125">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="5564e-125">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="5564e-126">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="5564e-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="5564e-127">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="5564e-127">MAPI Constants</span></span>](mapi-constants.md)

