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
ms.openlocfilehash: fa8b84e7baed74bda25ec1b20bd79fb121a838fd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587569"
---
# <a name="upmsg"></a><span data-ttu-id="58de3-103">UPMSG</span><span class="sxs-lookup"><span data-stu-id="58de3-103">UPMSG</span></span>

<span data-ttu-id="58de3-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="58de3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="58de3-105">Informações de carregamento de um item do Outlook durante o [carregamento do estado da mensagem](upload-message-state.md).</span><span class="sxs-lookup"><span data-stu-id="58de3-105">Information for uploading an Outlook item during the [upload message state](upload-message-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="58de3-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="58de3-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="58de3-107">Membros</span><span class="sxs-lookup"><span data-stu-id="58de3-107">Members</span></span>

 <span data-ttu-id="58de3-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="58de3-108">_ulFlags_</span></span>
  
> <span data-ttu-id="58de3-109">[out] / [in] sinalizadores para determinar o comportamento apropriado durante o carregamento.</span><span class="sxs-lookup"><span data-stu-id="58de3-109">[out]/[in] Flags to determine appropriate behavior during the upload.</span></span> 
    
  - <span data-ttu-id="58de3-110">UPM_ASSOC</span><span class="sxs-lookup"><span data-stu-id="58de3-110">UPM_ASSOC</span></span>
    
    - <span data-ttu-id="58de3-111">[out] Item está associado.</span><span class="sxs-lookup"><span data-stu-id="58de3-111">[out] Item is associated.</span></span>
    
  - <span data-ttu-id="58de3-112">UPM_NEW</span><span class="sxs-lookup"><span data-stu-id="58de3-112">UPM_NEW</span></span>
    
    - <span data-ttu-id="58de3-113">[out] Novo item.</span><span class="sxs-lookup"><span data-stu-id="58de3-113">[out] New item.</span></span> 
    
  - <span data-ttu-id="58de3-114">UPM_MOV</span><span class="sxs-lookup"><span data-stu-id="58de3-114">UPM_MOV</span></span>
    
    - <span data-ttu-id="58de3-115">[out] Item foi movido aqui.</span><span class="sxs-lookup"><span data-stu-id="58de3-115">[out] Item was moved here.</span></span>
    
  - <span data-ttu-id="58de3-116">UPM_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="58de3-116">UPM_MOD_PROPS</span></span>
    
    - <span data-ttu-id="58de3-117">[out] Propriedades do item foram modificadas.</span><span class="sxs-lookup"><span data-stu-id="58de3-117">[out] Item properties were modified.</span></span>
    
  - <span data-ttu-id="58de3-118">UPM_HEADER</span><span class="sxs-lookup"><span data-stu-id="58de3-118">UPM_HEADER</span></span>
    
    - <span data-ttu-id="58de3-119">[out] O item é o cabeçalho da mensagem.</span><span class="sxs-lookup"><span data-stu-id="58de3-119">[out] Item is a message header.</span></span>
    
  - <span data-ttu-id="58de3-120">UPM_OK</span><span class="sxs-lookup"><span data-stu-id="58de3-120">UPM_OK</span></span>
    
    - <span data-ttu-id="58de3-121">[in] Carregamento foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="58de3-121">[in] Upload was successful.</span></span> <span data-ttu-id="58de3-122">O cliente define esta após carregar as informações para o servidor.</span><span class="sxs-lookup"><span data-stu-id="58de3-122">The client sets this after uploading information to the server.</span></span>
    
  - <span data-ttu-id="58de3-123">UPM_MOVED</span><span class="sxs-lookup"><span data-stu-id="58de3-123">UPM_MOVED</span></span>
    
    - <span data-ttu-id="58de3-124">[in] Item foi movido com êxito.</span><span class="sxs-lookup"><span data-stu-id="58de3-124">[in] Item was moved successfully.</span></span>
    
  - <span data-ttu-id="58de3-125">UPM_COMMIT</span><span class="sxs-lookup"><span data-stu-id="58de3-125">UPM_COMMIT</span></span>
    
    - <span data-ttu-id="58de3-126">[in] Confirme o estado de carregamento agora.</span><span class="sxs-lookup"><span data-stu-id="58de3-126">[in] Commit upload state now.</span></span>
    
  - <span data-ttu-id="58de3-127">UPM_DELETE</span><span class="sxs-lookup"><span data-stu-id="58de3-127">UPM_DELETE</span></span>
    
    - <span data-ttu-id="58de3-128">[in] Exclua item agora.</span><span class="sxs-lookup"><span data-stu-id="58de3-128">[in] Delete item now.</span></span>
    
  - <span data-ttu-id="58de3-129">UPM_SAVE</span><span class="sxs-lookup"><span data-stu-id="58de3-129">UPM_SAVE</span></span>
    
    - <span data-ttu-id="58de3-130">[in] Salve alterações no item.</span><span class="sxs-lookup"><span data-stu-id="58de3-130">[in] Save changes to the item.</span></span>
    
<span data-ttu-id="58de3-131">_pmsg_</span><span class="sxs-lookup"><span data-stu-id="58de3-131">_pmsg_</span></span>
  
> <span data-ttu-id="58de3-132">[out] Objeto de item aberto.</span><span class="sxs-lookup"><span data-stu-id="58de3-132">[out] Open item object.</span></span> <span data-ttu-id="58de3-133">Consulte mapidefs.h para a definição de tipo de **LPMESSAGE**.</span><span class="sxs-lookup"><span data-stu-id="58de3-133">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span> 
    
<span data-ttu-id="58de3-134">_meid_</span><span class="sxs-lookup"><span data-stu-id="58de3-134">_meid_</span></span>
  
> <span data-ttu-id="58de3-135">[out] Identificação de entrada do item.</span><span class="sxs-lookup"><span data-stu-id="58de3-135">[out] Entry ID of item.</span></span>
    
<span data-ttu-id="58de3-136">_binReserved1_</span><span class="sxs-lookup"><span data-stu-id="58de3-136">_binReserved1_</span></span>
  
> <span data-ttu-id="58de3-137">[in] Este membro é reservado para uso interno do Outlook e não é suportado.</span><span class="sxs-lookup"><span data-stu-id="58de3-137">[in] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="58de3-138">_binReserved2_</span><span class="sxs-lookup"><span data-stu-id="58de3-138">_binReserved2_</span></span>
  
> <span data-ttu-id="58de3-139">[in] Este membro é reservado para uso interno do Outlook e não é suportado.</span><span class="sxs-lookup"><span data-stu-id="58de3-139">[in] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="58de3-140">_feid_</span><span class="sxs-lookup"><span data-stu-id="58de3-140">_feid_</span></span>
  
> <span data-ttu-id="58de3-141">[out] Identificação de entrada da pasta de origem, se o item foi movido.</span><span class="sxs-lookup"><span data-stu-id="58de3-141">[out] Entry ID of the source folder, if item was moved.</span></span>
    
<span data-ttu-id="58de3-142">_binChg_</span><span class="sxs-lookup"><span data-stu-id="58de3-142">_binChg_</span></span>
  
> <span data-ttu-id="58de3-143">[out] Alterar chave do item de destino, se o item foi movido.</span><span class="sxs-lookup"><span data-stu-id="58de3-143">[out] Change key of the destination item, if item was moved.</span></span> <span data-ttu-id="58de3-144">Consulte mapidefs.h para a definição de tipo de **SBinary**.</span><span class="sxs-lookup"><span data-stu-id="58de3-144">See mapidefs.h for the type definition of **SBinary**.</span></span> 
    
<span data-ttu-id="58de3-145">_binPcl_</span><span class="sxs-lookup"><span data-stu-id="58de3-145">_binPcl_</span></span>
  
> <span data-ttu-id="58de3-146">[out] Alterar a lista do item de destino, se o item foi movido.</span><span class="sxs-lookup"><span data-stu-id="58de3-146">[out] Change list of the destination item, if item was moved.</span></span> <span data-ttu-id="58de3-147">Consulte mapidefs.h para a definição de tipo de **SBinary**.</span><span class="sxs-lookup"><span data-stu-id="58de3-147">See mapidefs.h for the type definition of **SBinary**.</span></span> 
    
<span data-ttu-id="58de3-148">_skeySrc_</span><span class="sxs-lookup"><span data-stu-id="58de3-148">_skeySrc_</span></span>
  
> <span data-ttu-id="58de3-149">[out] Chave de origem do item de origem, se o item foi movido.</span><span class="sxs-lookup"><span data-stu-id="58de3-149">[out] Source key of the source item, if item was moved.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="58de3-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="58de3-150">See also</span></span>

- [<span data-ttu-id="58de3-151">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="58de3-151">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="58de3-152">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="58de3-152">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="58de3-153">Constantes de MAPI</span><span class="sxs-lookup"><span data-stu-id="58de3-153">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="58de3-154">FEID</span><span class="sxs-lookup"><span data-stu-id="58de3-154">FEID</span></span>](feid.md)
- [<span data-ttu-id="58de3-155">MEID</span><span class="sxs-lookup"><span data-stu-id="58de3-155">MEID</span></span>](meid.md)
- [<span data-ttu-id="58de3-156">SKEY</span><span class="sxs-lookup"><span data-stu-id="58de3-156">SKEY</span></span>](skey.md)

