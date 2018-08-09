---
title: UPMSG
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5fe3956b-819a-3edf-0e49-7a44bcfbabcd
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: e281907931a493e82c44913a7c26f6df55876e70
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770685"
---
# <a name="upmsg"></a><span data-ttu-id="68512-103">UPMSG</span><span class="sxs-lookup"><span data-stu-id="68512-103">UPMSG</span></span>

<span data-ttu-id="68512-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="68512-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="68512-105">Informações de carregamento de um item do Outlook durante o [carregamento do estado da mensagem](upload-message-state.md).</span><span class="sxs-lookup"><span data-stu-id="68512-105">Information for uploading an Outlook item during the [upload message state](upload-message-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="68512-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="68512-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="68512-107">Members</span><span class="sxs-lookup"><span data-stu-id="68512-107">Members</span></span>

 <span data-ttu-id="68512-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="68512-108">_ulFlags_</span></span>
  
> <span data-ttu-id="68512-109">[out] / [in] sinalizadores para determinar o comportamento apropriado durante o carregamento.</span><span class="sxs-lookup"><span data-stu-id="68512-109">[out]/[in] Flags to determine appropriate behavior during the upload.</span></span> 
    
  - <span data-ttu-id="68512-110">UPM_ASSOC</span><span class="sxs-lookup"><span data-stu-id="68512-110">UPM_ASSOC</span></span>
    
    - <span data-ttu-id="68512-111">[out] Item está associado.</span><span class="sxs-lookup"><span data-stu-id="68512-111">[out] Item is associated.</span></span>
    
  - <span data-ttu-id="68512-112">UPM_NEW</span><span class="sxs-lookup"><span data-stu-id="68512-112">UPM_NEW</span></span>
    
    - <span data-ttu-id="68512-113">[out] Novo item.</span><span class="sxs-lookup"><span data-stu-id="68512-113">[out] New item.</span></span> 
    
  - <span data-ttu-id="68512-114">UPM_MOV</span><span class="sxs-lookup"><span data-stu-id="68512-114">UPM_MOV</span></span>
    
    - <span data-ttu-id="68512-115">[out] Item foi movido aqui.</span><span class="sxs-lookup"><span data-stu-id="68512-115">[out] Item was moved here.</span></span>
    
  - <span data-ttu-id="68512-116">UPM_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="68512-116">UPM_MOD_PROPS</span></span>
    
    - <span data-ttu-id="68512-117">[out] Propriedades do item foram modificadas.</span><span class="sxs-lookup"><span data-stu-id="68512-117">[out] Item properties were modified.</span></span>
    
  - <span data-ttu-id="68512-118">UPM_HEADER</span><span class="sxs-lookup"><span data-stu-id="68512-118">UPM_HEADER</span></span>
    
    - <span data-ttu-id="68512-119">[out] O item é o cabeçalho da mensagem.</span><span class="sxs-lookup"><span data-stu-id="68512-119">[out] Item is a message header.</span></span>
    
  - <span data-ttu-id="68512-120">UPM_OK</span><span class="sxs-lookup"><span data-stu-id="68512-120">UPM_OK</span></span>
    
    - <span data-ttu-id="68512-121">[in] Carregamento foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="68512-121">[in] Upload was successful.</span></span> <span data-ttu-id="68512-122">O cliente define esta após carregar as informações para o servidor.</span><span class="sxs-lookup"><span data-stu-id="68512-122">The client sets this after uploading information to the server.</span></span>
    
  - <span data-ttu-id="68512-123">UPM_MOVED</span><span class="sxs-lookup"><span data-stu-id="68512-123">UPM_MOVED</span></span>
    
    - <span data-ttu-id="68512-124">[in] Item foi movido com êxito.</span><span class="sxs-lookup"><span data-stu-id="68512-124">[in] Item was moved successfully.</span></span>
    
  - <span data-ttu-id="68512-125">UPM_COMMIT</span><span class="sxs-lookup"><span data-stu-id="68512-125">UPM_COMMIT</span></span>
    
    - <span data-ttu-id="68512-126">[in] Confirme o estado de carregamento agora.</span><span class="sxs-lookup"><span data-stu-id="68512-126">[in] Commit upload state now.</span></span>
    
  - <span data-ttu-id="68512-127">UPM_DELETE</span><span class="sxs-lookup"><span data-stu-id="68512-127">UPM_DELETE</span></span>
    
    - <span data-ttu-id="68512-128">[in] Exclua item agora.</span><span class="sxs-lookup"><span data-stu-id="68512-128">[in] Delete item now.</span></span>
    
  - <span data-ttu-id="68512-129">UPM_SAVE</span><span class="sxs-lookup"><span data-stu-id="68512-129">UPM_SAVE</span></span>
    
    - <span data-ttu-id="68512-130">[in] Salve alterações no item.</span><span class="sxs-lookup"><span data-stu-id="68512-130">[in] Save changes to the item.</span></span>
    
<span data-ttu-id="68512-131">_pmsg_</span><span class="sxs-lookup"><span data-stu-id="68512-131">_pmsg_</span></span>
  
> <span data-ttu-id="68512-132">[out] Objeto de item aberto.</span><span class="sxs-lookup"><span data-stu-id="68512-132">[out] Open item object.</span></span> <span data-ttu-id="68512-133">Consulte mapidefs.h para a definição de tipo de **LPMESSAGE**.</span><span class="sxs-lookup"><span data-stu-id="68512-133">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span> 
    
<span data-ttu-id="68512-134">_meid_</span><span class="sxs-lookup"><span data-stu-id="68512-134">_meid_</span></span>
  
> <span data-ttu-id="68512-135">[out] Identificação de entrada do item.</span><span class="sxs-lookup"><span data-stu-id="68512-135">[out] Entry ID of item.</span></span>
    
<span data-ttu-id="68512-136">_binReserved1_</span><span class="sxs-lookup"><span data-stu-id="68512-136">_binReserved1_</span></span>
  
> <span data-ttu-id="68512-137">[in] Este membro é reservado para uso interno do Outlook e não é suportado.</span><span class="sxs-lookup"><span data-stu-id="68512-137">[in] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="68512-138">_binReserved2_</span><span class="sxs-lookup"><span data-stu-id="68512-138">_binReserved2_</span></span>
  
> <span data-ttu-id="68512-139">[in] Este membro é reservado para uso interno do Outlook e não é suportado.</span><span class="sxs-lookup"><span data-stu-id="68512-139">[in] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="68512-140">_feid_</span><span class="sxs-lookup"><span data-stu-id="68512-140">_feid_</span></span>
  
> <span data-ttu-id="68512-141">[out] Identificação de entrada da pasta de origem, se o item foi movido.</span><span class="sxs-lookup"><span data-stu-id="68512-141">[out] Entry ID of the source folder, if item was moved.</span></span>
    
<span data-ttu-id="68512-142">_binChg_</span><span class="sxs-lookup"><span data-stu-id="68512-142">_binChg_</span></span>
  
> <span data-ttu-id="68512-143">[out] Alterar chave do item de destino, se o item foi movido.</span><span class="sxs-lookup"><span data-stu-id="68512-143">[out] Change key of the destination item, if item was moved.</span></span> <span data-ttu-id="68512-144">Consulte mapidefs.h para a definição de tipo de **SBinary**.</span><span class="sxs-lookup"><span data-stu-id="68512-144">See mapidefs.h for the type definition of **SBinary**.</span></span> 
    
<span data-ttu-id="68512-145">_binPcl_</span><span class="sxs-lookup"><span data-stu-id="68512-145">_binPcl_</span></span>
  
> <span data-ttu-id="68512-146">[out] Alterar a lista do item de destino, se o item foi movido.</span><span class="sxs-lookup"><span data-stu-id="68512-146">[out] Change list of the destination item, if item was moved.</span></span> <span data-ttu-id="68512-147">Consulte mapidefs.h para a definição de tipo de **SBinary**.</span><span class="sxs-lookup"><span data-stu-id="68512-147">See mapidefs.h for the type definition of **SBinary**.</span></span> 
    
<span data-ttu-id="68512-148">_skeySrc_</span><span class="sxs-lookup"><span data-stu-id="68512-148">_skeySrc_</span></span>
  
> <span data-ttu-id="68512-149">[out] Chave de origem do item de origem, se o item foi movido.</span><span class="sxs-lookup"><span data-stu-id="68512-149">[out] Source key of the source item, if item was moved.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="68512-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="68512-150">See also</span></span>

- [<span data-ttu-id="68512-151">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="68512-151">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="68512-152">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="68512-152">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="68512-153">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="68512-153">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="68512-154">FEID</span><span class="sxs-lookup"><span data-stu-id="68512-154">FEID</span></span>](feid.md)
- [<span data-ttu-id="68512-155">MEID</span><span class="sxs-lookup"><span data-stu-id="68512-155">MEID</span></span>](meid.md)
- [<span data-ttu-id="68512-156">SKEY</span><span class="sxs-lookup"><span data-stu-id="68512-156">SKEY</span></span>](skey.md)

