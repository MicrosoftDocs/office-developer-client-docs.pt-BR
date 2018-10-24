---
title: UPDELE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c38aa8be-ae77-0c40-9843-42e07b80db6b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 2361d225c07d60fab40465b27ad393ca10f6d8eb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566583"
---
# <a name="updele"></a><span data-ttu-id="9ca66-103">UPDELE</span><span class="sxs-lookup"><span data-stu-id="9ca66-103">UPDELE</span></span>

<span data-ttu-id="9ca66-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9ca66-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9ca66-105">Informações para itens que foram excluídos em um repositório local estendidas.</span><span class="sxs-lookup"><span data-stu-id="9ca66-105">Extended information for items that have been deleted in a local store.</span></span> <span data-ttu-id="9ca66-106">Essas informações são usadas durante o [carregamento excluir o estado de status](upload-delete-status-state.md).</span><span class="sxs-lookup"><span data-stu-id="9ca66-106">This information is used during the [upload delete status state](upload-delete-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="9ca66-107">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="9ca66-107">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="9ca66-108">Membros</span><span class="sxs-lookup"><span data-stu-id="9ca66-108">Members</span></span>

<span data-ttu-id="9ca66-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9ca66-109">_ulFlags_</span></span>
  
> <span data-ttu-id="9ca66-110">[out] / [in] sinalizadores para determinar o comportamento apropriado durante o carregamento.</span><span class="sxs-lookup"><span data-stu-id="9ca66-110">[out]/[in] Flags to determine appropriate behavior during uploading.</span></span>
    
  - <span data-ttu-id="9ca66-111">UPD_ASSOC</span><span class="sxs-lookup"><span data-stu-id="9ca66-111">UPD_ASSOC</span></span>
    
    - <span data-ttu-id="9ca66-112">[out] Item está associado.</span><span class="sxs-lookup"><span data-stu-id="9ca66-112">[out] Item is associated.</span></span>
    
  - <span data-ttu-id="9ca66-113">UPD_MOV</span><span class="sxs-lookup"><span data-stu-id="9ca66-113">UPD_MOV</span></span>
    
    - <span data-ttu-id="9ca66-114">[out] Item foi movido check-out.</span><span class="sxs-lookup"><span data-stu-id="9ca66-114">[out] Item was moved out.</span></span>
    
  - <span data-ttu-id="9ca66-115">UPD_OK</span><span class="sxs-lookup"><span data-stu-id="9ca66-115">UPD_OK</span></span> 
    
    - <span data-ttu-id="9ca66-116">[in] Carregamento foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="9ca66-116">[in] Upload was successful.</span></span> <span data-ttu-id="9ca66-117">O cliente define esta após carregar informações ao servidor.</span><span class="sxs-lookup"><span data-stu-id="9ca66-117">The client sets this after uploading information to server.</span></span>
    
  - <span data-ttu-id="9ca66-118">UPD_MOVED</span><span class="sxs-lookup"><span data-stu-id="9ca66-118">UPD_MOVED</span></span>
    
    - <span data-ttu-id="9ca66-119">[in] Item foi movido com êxito.</span><span class="sxs-lookup"><span data-stu-id="9ca66-119">[in] Item was moved successfully.</span></span>
    
  - <span data-ttu-id="9ca66-120">UPD_UPDATE</span><span class="sxs-lookup"><span data-stu-id="9ca66-120">UPD_UPDATE</span></span>
    
    - <span data-ttu-id="9ca66-121">[in] Item de fonte de marca como modificado.</span><span class="sxs-lookup"><span data-stu-id="9ca66-121">[in] Mark source item as modified.</span></span>
    
  - <span data-ttu-id="9ca66-122">UPD_COMMIT</span><span class="sxs-lookup"><span data-stu-id="9ca66-122">UPD_COMMIT</span></span>
    
    - <span data-ttu-id="9ca66-123">[in] Confirme o estado de carregamento agora (entrada de 0).</span><span class="sxs-lookup"><span data-stu-id="9ca66-123">[in] Commit upload state now (entry 0).</span></span>
    
<span data-ttu-id="9ca66-124">_skey_</span><span class="sxs-lookup"><span data-stu-id="9ca66-124">_skey_</span></span>
  
> <span data-ttu-id="9ca66-125">[out] Chave de origem do item.</span><span class="sxs-lookup"><span data-stu-id="9ca66-125">[out] Source key of item.</span></span>
    
<span data-ttu-id="9ca66-126">_dwReserved_</span><span class="sxs-lookup"><span data-stu-id="9ca66-126">_dwReserved_</span></span>
  
> <span data-ttu-id="9ca66-127">[out] Esse membro é reservado para uso interno do Outlook e não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="9ca66-127">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
<span data-ttu-id="9ca66-128">_binChg_</span><span class="sxs-lookup"><span data-stu-id="9ca66-128">_binChg_</span></span>
  
> <span data-ttu-id="9ca66-129">[out] Alterar chave de item de destino se o item foi movido.</span><span class="sxs-lookup"><span data-stu-id="9ca66-129">[out] Change key of destination item if item has been moved.</span></span>
    
<span data-ttu-id="9ca66-130">_binPcl_</span><span class="sxs-lookup"><span data-stu-id="9ca66-130">_binPcl_</span></span>
  
> <span data-ttu-id="9ca66-131">[out] Alterar a lista de item de destino se o item foi movido.</span><span class="sxs-lookup"><span data-stu-id="9ca66-131">[out] Change list of destination item if item has been moved.</span></span>
    
<span data-ttu-id="9ca66-132">_skeyDst_</span><span class="sxs-lookup"><span data-stu-id="9ca66-132">_skeyDst_</span></span>
  
> <span data-ttu-id="9ca66-133">[out] Chave de origem do item de destino se o item foi movida.</span><span class="sxs-lookup"><span data-stu-id="9ca66-133">[out] Source key of destination item if item has been moved.</span></span>
    
<span data-ttu-id="9ca66-134">_pupmov_</span><span class="sxs-lookup"><span data-stu-id="9ca66-134">_pupmov_</span></span>
  
> <span data-ttu-id="9ca66-135">[out] Informações da pasta de destino se o item foi movidas.</span><span class="sxs-lookup"><span data-stu-id="9ca66-135">[out] Destination folder information if item has been moved.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9ca66-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="9ca66-136">See also</span></span>

- [<span data-ttu-id="9ca66-137">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="9ca66-137">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="9ca66-138">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="9ca66-138">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="9ca66-139">Constantes de MAPI</span><span class="sxs-lookup"><span data-stu-id="9ca66-139">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="9ca66-140">SKEY</span><span class="sxs-lookup"><span data-stu-id="9ca66-140">SKEY</span></span>](skey.md)
- [<span data-ttu-id="9ca66-141">UPDEL</span><span class="sxs-lookup"><span data-stu-id="9ca66-141">UPDEL</span></span>](updel.md)
- [<span data-ttu-id="9ca66-142">UPMOV</span><span class="sxs-lookup"><span data-stu-id="9ca66-142">UPMOV</span></span>](upmov.md)

