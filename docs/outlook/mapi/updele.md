---
title: UPDELE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c38aa8be-ae77-0c40-9843-42e07b80db6b
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 4dd60ffe305d27db2c9118e11cccf692652d0d27
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770664"
---
# <a name="updele"></a><span data-ttu-id="9280b-103">UPDELE</span><span class="sxs-lookup"><span data-stu-id="9280b-103">UPDELE</span></span>

<span data-ttu-id="9280b-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9280b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9280b-105">Informações para itens que foram excluídos em um repositório local estendidas.</span><span class="sxs-lookup"><span data-stu-id="9280b-105">Extended information for items that have been deleted in a local store.</span></span> <span data-ttu-id="9280b-106">Essas informações são usadas durante o [carregamento excluir o estado de status](upload-delete-status-state.md).</span><span class="sxs-lookup"><span data-stu-id="9280b-106">This information is used during the [upload delete status state](upload-delete-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="9280b-107">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="9280b-107">Quick info</span></span>

```cpp
struct UPDELE 
{ 
    ULONG ulFlags; 
    SKEY skey; 
    DWORD   dwReserved; 
    SBinary binChg; 
    SBinary binPcl; 
    SKEY skeyDst; 
    PUPMOV pupmov; 
};
```

## <a name="members"></a><span data-ttu-id="9280b-108">Members</span><span class="sxs-lookup"><span data-stu-id="9280b-108">Members</span></span>

<span data-ttu-id="9280b-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9280b-109">_ulFlags_</span></span>
  
> <span data-ttu-id="9280b-110">[out] / [in] sinalizadores para determinar o comportamento apropriado durante o carregamento.</span><span class="sxs-lookup"><span data-stu-id="9280b-110">[out]/[in] Flags to determine appropriate behavior during uploading.</span></span>
    
  - <span data-ttu-id="9280b-111">UPD_ASSOC</span><span class="sxs-lookup"><span data-stu-id="9280b-111">UPD_ASSOC</span></span>
    
    - <span data-ttu-id="9280b-112">[out] Item está associado.</span><span class="sxs-lookup"><span data-stu-id="9280b-112">[out] Item is associated.</span></span>
    
  - <span data-ttu-id="9280b-113">UPD_MOV</span><span class="sxs-lookup"><span data-stu-id="9280b-113">UPD_MOV</span></span>
    
    - <span data-ttu-id="9280b-114">[out] Item foi movido check-out.</span><span class="sxs-lookup"><span data-stu-id="9280b-114">[out] Item was moved out.</span></span>
    
  - <span data-ttu-id="9280b-115">UPD_OK</span><span class="sxs-lookup"><span data-stu-id="9280b-115">UPD_OK</span></span> 
    
    - <span data-ttu-id="9280b-116">[in] Carregamento foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="9280b-116">[in] Upload was successful.</span></span> <span data-ttu-id="9280b-117">O cliente define esta após carregar informações ao servidor.</span><span class="sxs-lookup"><span data-stu-id="9280b-117">The client sets this after uploading information to server.</span></span>
    
  - <span data-ttu-id="9280b-118">UPD_MOVED</span><span class="sxs-lookup"><span data-stu-id="9280b-118">UPD_MOVED</span></span>
    
    - <span data-ttu-id="9280b-119">[in] Item foi movido com êxito.</span><span class="sxs-lookup"><span data-stu-id="9280b-119">[in] Item was moved successfully.</span></span>
    
  - <span data-ttu-id="9280b-120">UPD_UPDATE</span><span class="sxs-lookup"><span data-stu-id="9280b-120">UPD_UPDATE</span></span>
    
    - <span data-ttu-id="9280b-121">[in] Item de fonte de marca como modificado.</span><span class="sxs-lookup"><span data-stu-id="9280b-121">[in] Mark source item as modified.</span></span>
    
  - <span data-ttu-id="9280b-122">UPD_COMMIT</span><span class="sxs-lookup"><span data-stu-id="9280b-122">UPD_COMMIT</span></span>
    
    - <span data-ttu-id="9280b-123">[in] Confirme o estado de carregamento agora (entrada de 0).</span><span class="sxs-lookup"><span data-stu-id="9280b-123">[in] Commit upload state now (entry 0).</span></span>
    
<span data-ttu-id="9280b-124">_skey_</span><span class="sxs-lookup"><span data-stu-id="9280b-124">_skey_</span></span>
  
> <span data-ttu-id="9280b-125">[out] Chave de origem do item.</span><span class="sxs-lookup"><span data-stu-id="9280b-125">[out] Source key of item.</span></span>
    
<span data-ttu-id="9280b-126">_dwReserved_</span><span class="sxs-lookup"><span data-stu-id="9280b-126">_dwReserved_</span></span>
  
> <span data-ttu-id="9280b-127">[out] Este membro é reservado para uso interno do Outlook e não é suportado.</span><span class="sxs-lookup"><span data-stu-id="9280b-127">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
<span data-ttu-id="9280b-128">_binChg_</span><span class="sxs-lookup"><span data-stu-id="9280b-128">_binChg_</span></span>
  
> <span data-ttu-id="9280b-129">[out] Alterar chave de item de destino se o item foi movido.</span><span class="sxs-lookup"><span data-stu-id="9280b-129">[out] Change key of destination item if item has been moved.</span></span>
    
<span data-ttu-id="9280b-130">_binPcl_</span><span class="sxs-lookup"><span data-stu-id="9280b-130">_binPcl_</span></span>
  
> <span data-ttu-id="9280b-131">[out] Alterar a lista de item de destino se o item foi movido.</span><span class="sxs-lookup"><span data-stu-id="9280b-131">[out] Change list of destination item if item has been moved.</span></span>
    
<span data-ttu-id="9280b-132">_skeyDst_</span><span class="sxs-lookup"><span data-stu-id="9280b-132">_skeyDst_</span></span>
  
> <span data-ttu-id="9280b-133">[out] Chave de origem do item de destino se o item foi movida.</span><span class="sxs-lookup"><span data-stu-id="9280b-133">[out] Source key of destination item if item has been moved.</span></span>
    
<span data-ttu-id="9280b-134">_pupmov_</span><span class="sxs-lookup"><span data-stu-id="9280b-134">_pupmov_</span></span>
  
> <span data-ttu-id="9280b-135">[out] Informações da pasta de destino se o item foi movidas.</span><span class="sxs-lookup"><span data-stu-id="9280b-135">[out] Destination folder information if item has been moved.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9280b-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="9280b-136">See also</span></span>

- [<span data-ttu-id="9280b-137">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="9280b-137">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="9280b-138">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="9280b-138">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="9280b-139">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="9280b-139">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="9280b-140">SKEY</span><span class="sxs-lookup"><span data-stu-id="9280b-140">SKEY</span></span>](skey.md)
- [<span data-ttu-id="9280b-141">UPDEL</span><span class="sxs-lookup"><span data-stu-id="9280b-141">UPDEL</span></span>](updel.md)
- [<span data-ttu-id="9280b-142">UPMOV</span><span class="sxs-lookup"><span data-stu-id="9280b-142">UPMOV</span></span>](upmov.md)

