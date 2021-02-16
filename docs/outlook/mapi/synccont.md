---
title: SYNCCONT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7b4307a3-5a8c-89bf-1113-2549556a7fe7
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: afba7fa718a35d33966d45289461313e349ef2e2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430403"
---
# <a name="synccont"></a><span data-ttu-id="9ebc6-103">SYNCCONT</span><span class="sxs-lookup"><span data-stu-id="9ebc6-103">SYNCCONT</span></span>

<span data-ttu-id="9ebc6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9ebc6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9ebc6-105">Informações para sincronizar o conteúdo de pastas especificadas em um armazenamento local com o servidor durante o estado [de sincronização de conteúdo.](synchronize-contents-state.md)</span><span class="sxs-lookup"><span data-stu-id="9ebc6-105">Information for synchronizing the contents of specified folders in a local store with the server during the [synchronize contents state](synchronize-contents-state.md).</span></span> <span data-ttu-id="9ebc6-106">Isso envolve apenas carregar ou uma sincronização completa envolvendo um upload e, em seguida, um download.</span><span class="sxs-lookup"><span data-stu-id="9ebc6-106">This involves just uploading, or a full synchronization involving an upload and then a download.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="9ebc6-107">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="9ebc6-107">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="9ebc6-108">Membros</span><span class="sxs-lookup"><span data-stu-id="9ebc6-108">Members</span></span>

<span data-ttu-id="9ebc6-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9ebc6-109">_ulFlags_</span></span>
  
> <span data-ttu-id="9ebc6-110">[in] Sinalizadores para determinar o comportamento apropriado durante a sincronização.</span><span class="sxs-lookup"><span data-stu-id="9ebc6-110">[in] Flags to determine the appropriate behavior during synchronization.</span></span>
    
  - <span data-ttu-id="9ebc6-111">UPC_OK</span><span class="sxs-lookup"><span data-stu-id="9ebc6-111">UPC_OK</span></span>
    
  - <span data-ttu-id="9ebc6-112">[in] A sincronização de carregamento ou completa foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="9ebc6-112">[in] Upload or full synchronization was successful.</span></span> <span data-ttu-id="9ebc6-113">O cliente define isso depois de sincronizar informações com o servidor.</span><span class="sxs-lookup"><span data-stu-id="9ebc6-113">The client sets this after synchronizing information with the server.</span></span>
    
<span data-ttu-id="9ebc6-114">_iEnt_</span><span class="sxs-lookup"><span data-stu-id="9ebc6-114">_iEnt_</span></span>
  
> <span data-ttu-id="9ebc6-115">[out] Index to track synchronizing the contents in the number of folders specified by  _cEnt_.</span><span class="sxs-lookup"><span data-stu-id="9ebc6-115">[out] Index to track synchronizing the contents in the number of folders specified by  _cEnt_.</span></span>
    
<span data-ttu-id="9ebc6-116">_cEnt_</span><span class="sxs-lookup"><span data-stu-id="9ebc6-116">_cEnt_</span></span>
  
> <span data-ttu-id="9ebc6-117">[out] Número de pastas a serem replicadas.</span><span class="sxs-lookup"><span data-stu-id="9ebc6-117">[out] Number of folders to be replicated.</span></span>
    
<span data-ttu-id="9ebc6-118">_pvReserved_</span><span class="sxs-lookup"><span data-stu-id="9ebc6-118">_pvReserved_</span></span>
  
> <span data-ttu-id="9ebc6-119">Este membro é reservado para uso interno do Outlook e não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="9ebc6-119">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="9ebc6-120">_ptagaReserved_</span><span class="sxs-lookup"><span data-stu-id="9ebc6-120">_ptagaReserved_</span></span>
  
> <span data-ttu-id="9ebc6-121">Este membro é reservado para uso interno do Outlook e não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="9ebc6-121">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="9ebc6-122">_psosReserved_</span><span class="sxs-lookup"><span data-stu-id="9ebc6-122">_psosReserved_</span></span>
  
> <span data-ttu-id="9ebc6-123">Este membro está reservado para uso interno do Outlook e não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="9ebc6-123">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="9ebc6-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="9ebc6-124">See also</span></span>

- [<span data-ttu-id="9ebc6-125">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="9ebc6-125">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="9ebc6-126">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="9ebc6-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="9ebc6-127">Constantes de MAPI</span><span class="sxs-lookup"><span data-stu-id="9ebc6-127">MAPI Constants</span></span>](mapi-constants.md)

