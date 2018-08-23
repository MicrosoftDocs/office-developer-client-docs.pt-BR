---
title: UPFLD
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6da9d6b6-a016-ccef-77da-3e037c30450d
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 34d6eb0653c3eb550bf03242a2c1b2acc3330a13
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572288"
---
# <a name="upfld"></a><span data-ttu-id="544d4-103">UPFLD</span><span class="sxs-lookup"><span data-stu-id="544d4-103">UPFLD</span></span>

<span data-ttu-id="544d4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="544d4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="544d4-105">Informações de carregamento de uma pasta durante o [carregamento do estado da pasta](upload-folder-state.md).</span><span class="sxs-lookup"><span data-stu-id="544d4-105">Information for uploading a folder during the [upload folder state](upload-folder-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="544d4-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="544d4-106">Quick info</span></span>

```cpp
struct UPFLD 
{ 
    ULONG ulFlags; 
    LPMAPIFOLDER pfld; 
    FEID feid; 
}; 

```

## <a name="members"></a><span data-ttu-id="544d4-107">Members</span><span class="sxs-lookup"><span data-stu-id="544d4-107">Members</span></span>

<span data-ttu-id="544d4-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="544d4-108">_ulFlags_</span></span>
  
>  <span data-ttu-id="544d4-109">[out] / [in] sinalizadores para determinar as ações apropriadas para a uplaod.</span><span class="sxs-lookup"><span data-stu-id="544d4-109">[out]/[in] Flags to determine appropriate actions for the uplaod.</span></span> 
    
  - <span data-ttu-id="544d4-110">UPF_NEW</span><span class="sxs-lookup"><span data-stu-id="544d4-110">UPF_NEW</span></span>
    
    - <span data-ttu-id="544d4-111">[out] Pasta é nova.</span><span class="sxs-lookup"><span data-stu-id="544d4-111">[out] Folder is new.</span></span>
    
  - <span data-ttu-id="544d4-112">UPF_MOD_PARENT</span><span class="sxs-lookup"><span data-stu-id="544d4-112">UPF_MOD_PARENT</span></span>
    
    - <span data-ttu-id="544d4-113">[out] Pasta foi movida.</span><span class="sxs-lookup"><span data-stu-id="544d4-113">[out] Folder has been moved.</span></span>
    
  - <span data-ttu-id="544d4-114">UPF_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="544d4-114">UPF_MOD_PROPS</span></span>
    
    - <span data-ttu-id="544d4-115">[out] Propriedades da pasta foram modificadas.</span><span class="sxs-lookup"><span data-stu-id="544d4-115">[out] Folder properties have been modified.</span></span>
    
  - <span data-ttu-id="544d4-116">UPF_DEL</span><span class="sxs-lookup"><span data-stu-id="544d4-116">UPF_DEL</span></span>
    
    - <span data-ttu-id="544d4-117">[out] Pasta foi excluída.</span><span class="sxs-lookup"><span data-stu-id="544d4-117">[out] Folder was deleted.</span></span>
    
  - <span data-ttu-id="544d4-118">UPF_OK</span><span class="sxs-lookup"><span data-stu-id="544d4-118">UPF_OK</span></span>
    
    - <span data-ttu-id="544d4-119">[in] Carregamento foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="544d4-119">[in] Upload was successful.</span></span> <span data-ttu-id="544d4-120">O cliente define esta após carregar as informações da pasta no servidor.</span><span class="sxs-lookup"><span data-stu-id="544d4-120">The client sets this after uploading folder information to the server.</span></span>
    
<span data-ttu-id="544d4-121">_pfld_</span><span class="sxs-lookup"><span data-stu-id="544d4-121">_pfld_</span></span>
  
> <span data-ttu-id="544d4-122">[out] O objeto de pasta aberta para carregar.</span><span class="sxs-lookup"><span data-stu-id="544d4-122">[out] The open folder object to upload.</span></span>
    
<span data-ttu-id="544d4-123">_feid_</span><span class="sxs-lookup"><span data-stu-id="544d4-123">_feid_</span></span>
  
> <span data-ttu-id="544d4-124">[out] Identificação de entrada da pasta.</span><span class="sxs-lookup"><span data-stu-id="544d4-124">[out] Entry ID of the folder.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="544d4-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="544d4-125">See also</span></span>

- [<span data-ttu-id="544d4-126">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="544d4-126">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="544d4-127">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="544d4-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="544d4-128">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="544d4-128">MAPI Constants</span></span>](mapi-constants.md)

