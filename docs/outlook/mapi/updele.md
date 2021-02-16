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
ms.openlocfilehash: 9bd61739b14d0ec382a9d582689c1049fe89429b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424879"
---
# <a name="updele"></a><span data-ttu-id="aeec8-103">UPDELE</span><span class="sxs-lookup"><span data-stu-id="aeec8-103">UPDELE</span></span>

<span data-ttu-id="aeec8-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aeec8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aeec8-105">Informações estendidas para itens que foram excluídos em um armazenamento local.</span><span class="sxs-lookup"><span data-stu-id="aeec8-105">Extended information for items that have been deleted in a local store.</span></span> <span data-ttu-id="aeec8-106">Essas informações são usadas durante o [estado de status de exclusão de upload.](upload-delete-status-state.md)</span><span class="sxs-lookup"><span data-stu-id="aeec8-106">This information is used during the [upload delete status state](upload-delete-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="aeec8-107">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="aeec8-107">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="aeec8-108">Membros</span><span class="sxs-lookup"><span data-stu-id="aeec8-108">Members</span></span>

<span data-ttu-id="aeec8-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="aeec8-109">_ulFlags_</span></span>
  
> <span data-ttu-id="aeec8-110">[out]/[in] Sinalizadores para determinar o comportamento apropriado durante o carregamento.</span><span class="sxs-lookup"><span data-stu-id="aeec8-110">[out]/[in] Flags to determine appropriate behavior during uploading.</span></span>
    
  - <span data-ttu-id="aeec8-111">UPD_ASSOC</span><span class="sxs-lookup"><span data-stu-id="aeec8-111">UPD_ASSOC</span></span>
    
    - <span data-ttu-id="aeec8-112">[out] Item está associado.</span><span class="sxs-lookup"><span data-stu-id="aeec8-112">[out] Item is associated.</span></span>
    
  - <span data-ttu-id="aeec8-113">UPD_MOV</span><span class="sxs-lookup"><span data-stu-id="aeec8-113">UPD_MOV</span></span>
    
    - <span data-ttu-id="aeec8-114">[out] Item foi movido para fora.</span><span class="sxs-lookup"><span data-stu-id="aeec8-114">[out] Item was moved out.</span></span>
    
  - <span data-ttu-id="aeec8-115">UPD_OK</span><span class="sxs-lookup"><span data-stu-id="aeec8-115">UPD_OK</span></span> 
    
    - <span data-ttu-id="aeec8-116">[in] O carregamento foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="aeec8-116">[in] Upload was successful.</span></span> <span data-ttu-id="aeec8-117">O cliente define isso depois de carregar informações no servidor.</span><span class="sxs-lookup"><span data-stu-id="aeec8-117">The client sets this after uploading information to server.</span></span>
    
  - <span data-ttu-id="aeec8-118">UPD_MOVED</span><span class="sxs-lookup"><span data-stu-id="aeec8-118">UPD_MOVED</span></span>
    
    - <span data-ttu-id="aeec8-119">[in] Item foi movido com êxito.</span><span class="sxs-lookup"><span data-stu-id="aeec8-119">[in] Item was moved successfully.</span></span>
    
  - <span data-ttu-id="aeec8-120">UPD_UPDATE</span><span class="sxs-lookup"><span data-stu-id="aeec8-120">UPD_UPDATE</span></span>
    
    - <span data-ttu-id="aeec8-121">[in] Marque o item de origem como modificado.</span><span class="sxs-lookup"><span data-stu-id="aeec8-121">[in] Mark source item as modified.</span></span>
    
  - <span data-ttu-id="aeec8-122">UPD_COMMIT</span><span class="sxs-lookup"><span data-stu-id="aeec8-122">UPD_COMMIT</span></span>
    
    - <span data-ttu-id="aeec8-123">[in] Confirma o estado de carregamento agora (entrada 0).</span><span class="sxs-lookup"><span data-stu-id="aeec8-123">[in] Commit upload state now (entry 0).</span></span>
    
<span data-ttu-id="aeec8-124">_skey_</span><span class="sxs-lookup"><span data-stu-id="aeec8-124">_skey_</span></span>
  
> <span data-ttu-id="aeec8-125">[out] Chave de origem do item.</span><span class="sxs-lookup"><span data-stu-id="aeec8-125">[out] Source key of item.</span></span>
    
<span data-ttu-id="aeec8-126">_dwReserved_</span><span class="sxs-lookup"><span data-stu-id="aeec8-126">_dwReserved_</span></span>
  
> <span data-ttu-id="aeec8-127">[out] Esse membro é reservado para uso interno do Outlook e não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="aeec8-127">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
<span data-ttu-id="aeec8-128">_binChg_</span><span class="sxs-lookup"><span data-stu-id="aeec8-128">_binChg_</span></span>
  
> <span data-ttu-id="aeec8-129">[out] Alterar a chave do item de destino se o item tiver sido movido.</span><span class="sxs-lookup"><span data-stu-id="aeec8-129">[out] Change key of destination item if item has been moved.</span></span>
    
<span data-ttu-id="aeec8-130">_binPcl_</span><span class="sxs-lookup"><span data-stu-id="aeec8-130">_binPcl_</span></span>
  
> <span data-ttu-id="aeec8-131">[out] Alterar a lista de itens de destino se o item tiver sido movido.</span><span class="sxs-lookup"><span data-stu-id="aeec8-131">[out] Change list of destination item if item has been moved.</span></span>
    
<span data-ttu-id="aeec8-132">_skeyDst_</span><span class="sxs-lookup"><span data-stu-id="aeec8-132">_skeyDst_</span></span>
  
> <span data-ttu-id="aeec8-133">[out] Chave de origem do item de destino se o item tiver sido movido.</span><span class="sxs-lookup"><span data-stu-id="aeec8-133">[out] Source key of destination item if item has been moved.</span></span>
    
<span data-ttu-id="aeec8-134">_realizoumov_</span><span class="sxs-lookup"><span data-stu-id="aeec8-134">_pupmov_</span></span>
  
> <span data-ttu-id="aeec8-135">[out] Informações da pasta de destino se o item tiver sido movido.</span><span class="sxs-lookup"><span data-stu-id="aeec8-135">[out] Destination folder information if item has been moved.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="aeec8-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="aeec8-136">See also</span></span>

- [<span data-ttu-id="aeec8-137">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="aeec8-137">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="aeec8-138">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="aeec8-138">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="aeec8-139">Constantes de MAPI</span><span class="sxs-lookup"><span data-stu-id="aeec8-139">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="aeec8-140">SKEY</span><span class="sxs-lookup"><span data-stu-id="aeec8-140">SKEY</span></span>](skey.md)
- [<span data-ttu-id="aeec8-141">UPDEL</span><span class="sxs-lookup"><span data-stu-id="aeec8-141">UPDEL</span></span>](updel.md)
- [<span data-ttu-id="aeec8-142">UPMOV</span><span class="sxs-lookup"><span data-stu-id="aeec8-142">UPMOV</span></span>](upmov.md)

