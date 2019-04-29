---
title: UPMSG
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5fe3956b-819a-3edf-0e49-7a44bcfbabcd
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 1e0e2f9b794c4cee25488a754290922e58b7658d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427266"
---
# <a name="upmsg"></a><span data-ttu-id="b527d-103">UPMSG</span><span class="sxs-lookup"><span data-stu-id="b527d-103">UPMSG</span></span>

<span data-ttu-id="b527d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b527d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b527d-105">Informações para carregar um item do Outlook durante o [estado de mensagem de carregamento](upload-message-state.md).</span><span class="sxs-lookup"><span data-stu-id="b527d-105">Information for uploading an Outlook item during the [upload message state](upload-message-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b527d-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="b527d-106">Quick info</span></span>

```cpp
struct UPMSG 
{ 
    ULONG ulFlags; 
    LPMESSAGE pmsg; 
    MEID meid; 
    SBinary binReserved1; 
    SBinary binReserved2; 
    FEID feid; 
    SBinary binChg; 
    SBinary binPcl; 
    SKEY skeySrc; 
};
```

## <a name="members"></a><span data-ttu-id="b527d-107">Membros</span><span class="sxs-lookup"><span data-stu-id="b527d-107">Members</span></span>

 <span data-ttu-id="b527d-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b527d-108">_ulFlags_</span></span>
  
> <span data-ttu-id="b527d-109">[out]/[in] flags para determinar o comportamento apropriado durante o carregamento.</span><span class="sxs-lookup"><span data-stu-id="b527d-109">[out]/[in] Flags to determine appropriate behavior during the upload.</span></span> 
    
  - <span data-ttu-id="b527d-110">UPM_ASSOC</span><span class="sxs-lookup"><span data-stu-id="b527d-110">UPM_ASSOC</span></span>
    
    - <span data-ttu-id="b527d-111">bota Item está associado.</span><span class="sxs-lookup"><span data-stu-id="b527d-111">[out] Item is associated.</span></span>
    
  - <span data-ttu-id="b527d-112">UPM_NEW</span><span class="sxs-lookup"><span data-stu-id="b527d-112">UPM_NEW</span></span>
    
    - <span data-ttu-id="b527d-113">bota Novo item.</span><span class="sxs-lookup"><span data-stu-id="b527d-113">[out] New item.</span></span> 
    
  - <span data-ttu-id="b527d-114">UPM_MOV</span><span class="sxs-lookup"><span data-stu-id="b527d-114">UPM_MOV</span></span>
    
    - <span data-ttu-id="b527d-115">bota O item foi movido aqui.</span><span class="sxs-lookup"><span data-stu-id="b527d-115">[out] Item was moved here.</span></span>
    
  - <span data-ttu-id="b527d-116">UPM_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="b527d-116">UPM_MOD_PROPS</span></span>
    
    - <span data-ttu-id="b527d-117">bota As propriedades do item foram modificadas.</span><span class="sxs-lookup"><span data-stu-id="b527d-117">[out] Item properties were modified.</span></span>
    
  - <span data-ttu-id="b527d-118">UPM_HEADER</span><span class="sxs-lookup"><span data-stu-id="b527d-118">UPM_HEADER</span></span>
    
    - <span data-ttu-id="b527d-119">bota Item é um cabeçalho de mensagem.</span><span class="sxs-lookup"><span data-stu-id="b527d-119">[out] Item is a message header.</span></span>
    
  - <span data-ttu-id="b527d-120">UPM_OK</span><span class="sxs-lookup"><span data-stu-id="b527d-120">UPM_OK</span></span>
    
    - <span data-ttu-id="b527d-121">no O upload foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="b527d-121">[in] Upload was successful.</span></span> <span data-ttu-id="b527d-122">O cliente define isso após carregar informações no servidor.</span><span class="sxs-lookup"><span data-stu-id="b527d-122">The client sets this after uploading information to the server.</span></span>
    
  - <span data-ttu-id="b527d-123">UPM_MOVED</span><span class="sxs-lookup"><span data-stu-id="b527d-123">UPM_MOVED</span></span>
    
    - <span data-ttu-id="b527d-124">no O item foi movido com êxito.</span><span class="sxs-lookup"><span data-stu-id="b527d-124">[in] Item was moved successfully.</span></span>
    
  - <span data-ttu-id="b527d-125">UPM_COMMIT</span><span class="sxs-lookup"><span data-stu-id="b527d-125">UPM_COMMIT</span></span>
    
    - <span data-ttu-id="b527d-126">no Confirme o estado de carregamento agora.</span><span class="sxs-lookup"><span data-stu-id="b527d-126">[in] Commit upload state now.</span></span>
    
  - <span data-ttu-id="b527d-127">UPM_DELETE</span><span class="sxs-lookup"><span data-stu-id="b527d-127">UPM_DELETE</span></span>
    
    - <span data-ttu-id="b527d-128">no Excluir o item agora.</span><span class="sxs-lookup"><span data-stu-id="b527d-128">[in] Delete item now.</span></span>
    
  - <span data-ttu-id="b527d-129">UPM_SAVE</span><span class="sxs-lookup"><span data-stu-id="b527d-129">UPM_SAVE</span></span>
    
    - <span data-ttu-id="b527d-130">no Salvar alterações no item.</span><span class="sxs-lookup"><span data-stu-id="b527d-130">[in] Save changes to the item.</span></span>
    
<span data-ttu-id="b527d-131">_pMsg_</span><span class="sxs-lookup"><span data-stu-id="b527d-131">_pmsg_</span></span>
  
> <span data-ttu-id="b527d-132">bota Objeto Open item.</span><span class="sxs-lookup"><span data-stu-id="b527d-132">[out] Open item object.</span></span> <span data-ttu-id="b527d-133">Consulte mapidefs. h para a definição de tipo de **lpMessage**.</span><span class="sxs-lookup"><span data-stu-id="b527d-133">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span> 
    
<span data-ttu-id="b527d-134">_MEID_</span><span class="sxs-lookup"><span data-stu-id="b527d-134">_meid_</span></span>
  
> <span data-ttu-id="b527d-135">bota ID de entrada do item.</span><span class="sxs-lookup"><span data-stu-id="b527d-135">[out] Entry ID of item.</span></span>
    
<span data-ttu-id="b527d-136">_binReserved1_</span><span class="sxs-lookup"><span data-stu-id="b527d-136">_binReserved1_</span></span>
  
> <span data-ttu-id="b527d-137">no Este membro é reservado para uso interno do Outlook e não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="b527d-137">[in] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="b527d-138">_binReserved2_</span><span class="sxs-lookup"><span data-stu-id="b527d-138">_binReserved2_</span></span>
  
> <span data-ttu-id="b527d-139">no Este membro é reservado para uso interno do Outlook e não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="b527d-139">[in] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="b527d-140">_feid_</span><span class="sxs-lookup"><span data-stu-id="b527d-140">_feid_</span></span>
  
> <span data-ttu-id="b527d-141">bota ID de entrada da pasta de origem, se o item foi movido.</span><span class="sxs-lookup"><span data-stu-id="b527d-141">[out] Entry ID of the source folder, if item was moved.</span></span>
    
<span data-ttu-id="b527d-142">_binChg_</span><span class="sxs-lookup"><span data-stu-id="b527d-142">_binChg_</span></span>
  
> <span data-ttu-id="b527d-143">bota Altere a chave do item de destino, se o item foi movido.</span><span class="sxs-lookup"><span data-stu-id="b527d-143">[out] Change key of the destination item, if item was moved.</span></span> <span data-ttu-id="b527d-144">Consulte mapidefs. h para a definição de tipo de **SBinary**.</span><span class="sxs-lookup"><span data-stu-id="b527d-144">See mapidefs.h for the type definition of **SBinary**.</span></span> 
    
<span data-ttu-id="b527d-145">_binPcl_</span><span class="sxs-lookup"><span data-stu-id="b527d-145">_binPcl_</span></span>
  
> <span data-ttu-id="b527d-146">bota Altere a lista do item de destino, se o item foi movido.</span><span class="sxs-lookup"><span data-stu-id="b527d-146">[out] Change list of the destination item, if item was moved.</span></span> <span data-ttu-id="b527d-147">Consulte mapidefs. h para a definição de tipo de **SBinary**.</span><span class="sxs-lookup"><span data-stu-id="b527d-147">See mapidefs.h for the type definition of **SBinary**.</span></span> 
    
<span data-ttu-id="b527d-148">_skeySrc_</span><span class="sxs-lookup"><span data-stu-id="b527d-148">_skeySrc_</span></span>
  
> <span data-ttu-id="b527d-149">bota Chave de origem do item de origem, se o item foi movido.</span><span class="sxs-lookup"><span data-stu-id="b527d-149">[out] Source key of the source item, if item was moved.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b527d-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="b527d-150">See also</span></span>

- [<span data-ttu-id="b527d-151">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="b527d-151">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="b527d-152">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="b527d-152">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="b527d-153">Constantes de MAPI</span><span class="sxs-lookup"><span data-stu-id="b527d-153">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="b527d-154">FEID</span><span class="sxs-lookup"><span data-stu-id="b527d-154">FEID</span></span>](feid.md)
- [<span data-ttu-id="b527d-155">MEID</span><span class="sxs-lookup"><span data-stu-id="b527d-155">MEID</span></span>](meid.md)
- [<span data-ttu-id="b527d-156">SKEY</span><span class="sxs-lookup"><span data-stu-id="b527d-156">SKEY</span></span>](skey.md)

