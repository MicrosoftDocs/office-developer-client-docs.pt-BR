---
title: UPFLD
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6da9d6b6-a016-ccef-77da-3e037c30450d
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: c8f7bdc5864c049d8db6f38e92a69c97b6f9dc73
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360477"
---
# <a name="upfld"></a><span data-ttu-id="e1d62-103">UPFLD</span><span class="sxs-lookup"><span data-stu-id="e1d62-103">UPFLD</span></span>

<span data-ttu-id="e1d62-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1d62-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1d62-105">Informações para carregar uma pasta durante o estado de [pasta de carregamento](upload-folder-state.md).</span><span class="sxs-lookup"><span data-stu-id="e1d62-105">Information for uploading a folder during the [upload folder state](upload-folder-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e1d62-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="e1d62-106">Quick info</span></span>

```cpp
struct UPFLD 
{ 
    ULONG ulFlags; 
    LPMAPIFOLDER pfld; 
    FEID feid; 
}; 

```

## <a name="members"></a><span data-ttu-id="e1d62-107">Membros</span><span class="sxs-lookup"><span data-stu-id="e1d62-107">Members</span></span>

<span data-ttu-id="e1d62-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e1d62-108">_ulFlags_</span></span>
  
>  <span data-ttu-id="e1d62-109">[out]/[in] flags para determinar as ações apropriadas para o uplaod.</span><span class="sxs-lookup"><span data-stu-id="e1d62-109">[out]/[in] Flags to determine appropriate actions for the uplaod.</span></span> 
    
  - <span data-ttu-id="e1d62-110">UPF_NEW</span><span class="sxs-lookup"><span data-stu-id="e1d62-110">UPF_NEW</span></span>
    
    - <span data-ttu-id="e1d62-111">bota A pasta é nova.</span><span class="sxs-lookup"><span data-stu-id="e1d62-111">[out] Folder is new.</span></span>
    
  - <span data-ttu-id="e1d62-112">UPF_MOD_PARENT</span><span class="sxs-lookup"><span data-stu-id="e1d62-112">UPF_MOD_PARENT</span></span>
    
    - <span data-ttu-id="e1d62-113">bota A pasta foi movida.</span><span class="sxs-lookup"><span data-stu-id="e1d62-113">[out] Folder has been moved.</span></span>
    
  - <span data-ttu-id="e1d62-114">UPF_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="e1d62-114">UPF_MOD_PROPS</span></span>
    
    - <span data-ttu-id="e1d62-115">bota As propriedades da pasta foram modificadas.</span><span class="sxs-lookup"><span data-stu-id="e1d62-115">[out] Folder properties have been modified.</span></span>
    
  - <span data-ttu-id="e1d62-116">UPF_DEL</span><span class="sxs-lookup"><span data-stu-id="e1d62-116">UPF_DEL</span></span>
    
    - <span data-ttu-id="e1d62-117">bota A pasta foi excluída.</span><span class="sxs-lookup"><span data-stu-id="e1d62-117">[out] Folder was deleted.</span></span>
    
  - <span data-ttu-id="e1d62-118">UPF_OK</span><span class="sxs-lookup"><span data-stu-id="e1d62-118">UPF_OK</span></span>
    
    - <span data-ttu-id="e1d62-119">no O upload foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="e1d62-119">[in] Upload was successful.</span></span> <span data-ttu-id="e1d62-120">O cliente define isso após carregar as informações da pasta no servidor.</span><span class="sxs-lookup"><span data-stu-id="e1d62-120">The client sets this after uploading folder information to the server.</span></span>
    
<span data-ttu-id="e1d62-121">_pfld_</span><span class="sxs-lookup"><span data-stu-id="e1d62-121">_pfld_</span></span>
  
> <span data-ttu-id="e1d62-122">bota O objeto Folder aberto a ser carregado.</span><span class="sxs-lookup"><span data-stu-id="e1d62-122">[out] The open folder object to upload.</span></span>
    
<span data-ttu-id="e1d62-123">_feid_</span><span class="sxs-lookup"><span data-stu-id="e1d62-123">_feid_</span></span>
  
> <span data-ttu-id="e1d62-124">[out] ID da entrada da pasta.</span><span class="sxs-lookup"><span data-stu-id="e1d62-124">[out] Entry ID of the folder.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e1d62-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="e1d62-125">See also</span></span>

- [<span data-ttu-id="e1d62-126">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="e1d62-126">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="e1d62-127">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="e1d62-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="e1d62-128">Constantes de MAPI</span><span class="sxs-lookup"><span data-stu-id="e1d62-128">MAPI Constants</span></span>](mapi-constants.md)

