---
title: SYNC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3f07fddf-4c42-6ea7-162d-57022166a83f
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: e856044a1b6345c4e495a75dfb7ca0defa52ceec
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349592"
---
# <a name="sync"></a><span data-ttu-id="6f419-103">SYNC</span><span class="sxs-lookup"><span data-stu-id="6f419-103">SYNC</span></span>

  
  
<span data-ttu-id="6f419-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6f419-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6f419-105">Informações para iniciar a sincronização entre um repositório local e um servidor.</span><span class="sxs-lookup"><span data-stu-id="6f419-105">Information for starting synchronization between a local store and a server.</span></span> <span data-ttu-id="6f419-106">Essas informações são usadas durante o [estado de sincronização](synchronize-state.md).</span><span class="sxs-lookup"><span data-stu-id="6f419-106">This information is used during the [synchronize state](synchronize-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="6f419-107">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="6f419-107">Quick info</span></span>

```cpp
struct SYNC 
{ 
    ULONG ulFlags; 
    LPWSTR pwzPath; 
    FEID Reserved1; 
    MEID Reserved2; 
    LPENTRYLIST pel; 
    ULONG const * pulFolderOptions; 
};
```

## <a name="members"></a><span data-ttu-id="6f419-108">Membros</span><span class="sxs-lookup"><span data-stu-id="6f419-108">Members</span></span>

 <span data-ttu-id="6f419-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6f419-109">_ulFlags_</span></span>
  
- <span data-ttu-id="6f419-110">[out]/[in] um bitmask dos seguintes sinalizadores que modifica o comportamento durante a sincronização:</span><span class="sxs-lookup"><span data-stu-id="6f419-110">[out]/[in] A bitmask of the following flags that modifies the behavior during synchronization:</span></span>
    
- <span data-ttu-id="6f419-111">UPS_UPLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="6f419-111">UPS_UPLOAD_ONLY</span></span>
    
  - <span data-ttu-id="6f419-112">no O cliente executará o carregamento apenas.</span><span class="sxs-lookup"><span data-stu-id="6f419-112">[in] The client will be performing only upload.</span></span> <span data-ttu-id="6f419-113">O Outlook retorna apenas as pastas modificadas localmente.</span><span class="sxs-lookup"><span data-stu-id="6f419-113">Outlook only returns locally modified folders.</span></span>
    
- <span data-ttu-id="6f419-114">UPS_DNLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="6f419-114">UPS_DNLOAD_ONLY</span></span>
    
  - <span data-ttu-id="6f419-115">no O cliente executará apenas o download.</span><span class="sxs-lookup"><span data-stu-id="6f419-115">[in] The client will be performing only download.</span></span> <span data-ttu-id="6f419-116">O Outlook não deve limpar bits de carregamento para pastas.</span><span class="sxs-lookup"><span data-stu-id="6f419-116">Outlook should not clear upload bits for folders.</span></span>
    
- <span data-ttu-id="6f419-117">UPS_THESE_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="6f419-117">UPS_THESE_FOLDERS</span></span>
    
  - <span data-ttu-id="6f419-118">no O cliente estará sincronizando um conjunto de pastas especificado com as IDs de entrada fornecidas.</span><span class="sxs-lookup"><span data-stu-id="6f419-118">[in] The client will be synchronizing a specified set of folders with the provided entry IDs.</span></span> <span data-ttu-id="6f419-119">Esse sinalizador pode ser combinado com o sinalizador **UPS_UPLOAD_ONLY** ou **UPS_DNLOAD_ONLY** .</span><span class="sxs-lookup"><span data-stu-id="6f419-119">This flag can be combined with either the **UPS_UPLOAD_ONLY** or **UPS_DNLOAD_ONLY** flag.</span></span> 
    
- <span data-ttu-id="6f419-120">UPS_OK</span><span class="sxs-lookup"><span data-stu-id="6f419-120">UPS_OK</span></span>
    
  - <span data-ttu-id="6f419-121">bota A sincronização foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="6f419-121">[out] Synchronization was successful.</span></span> <span data-ttu-id="6f419-122">O cliente define isso após o carregamento ou uma sincronização completa ser concluída.</span><span class="sxs-lookup"><span data-stu-id="6f419-122">The client sets this after uploading or a full synchronization completes.</span></span>
    
- 
    
    > [!NOTE]
    > <span data-ttu-id="6f419-123">Embora o cliente possa carregar ou sincronizar totalmente (carregar e baixar) pastas e itens com a API de replicação, o cliente especifica *parâmetroulflags* com apenas uma direção da replicação de cada vez, ou seja, o **UPS_UPLOAD_ONLY** ou Sinalizador **UPS_DNLOAD_ONLY** .</span><span class="sxs-lookup"><span data-stu-id="6f419-123">Even though the client can either upload or fully synchronize (upload then download) folders and items with the Replication API, the client specifies  *ulFlags*  with only one direction of the replication at a time — either the **UPS_UPLOAD_ONLY** or **UPS_DNLOAD_ONLY** flag.</span></span> <span data-ttu-id="6f419-124">No caso de uma sincronização completa, o cliente primeiro realiza um upload com o sinalizador **UPS_UPLOAD_ONLY** e, em seguida, um download com o sinalizador **UPS_DNLOAD_ONLY** .</span><span class="sxs-lookup"><span data-stu-id="6f419-124">In the case of a full synchronization, the client first does an upload with the **UPS_UPLOAD_ONLY** flag, and then a download with the **UPS_DNLOAD_ONLY** flag.</span></span> 
  
 <span data-ttu-id="6f419-125">_pwzPath_</span><span class="sxs-lookup"><span data-stu-id="6f419-125">_pwzPath_</span></span>
  
- <span data-ttu-id="6f419-126">bota Caminho para o repositório local.</span><span class="sxs-lookup"><span data-stu-id="6f419-126">[out] Path to the local store.</span></span>
    
 <span data-ttu-id="6f419-127">_Reserved1_</span><span class="sxs-lookup"><span data-stu-id="6f419-127">_Reserved1_</span></span>
  
- <span data-ttu-id="6f419-128">Este membro é reservado para uso interno do Outlook e não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="6f419-128">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="6f419-129">_Reserved2_</span><span class="sxs-lookup"><span data-stu-id="6f419-129">_Reserved2_</span></span>
  
- <span data-ttu-id="6f419-130">Este membro é reservado para uso interno do Outlook e não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="6f419-130">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="6f419-131">*PEL*</span><span class="sxs-lookup"><span data-stu-id="6f419-131">*pel*</span></span> 
  
- <span data-ttu-id="6f419-132">no Esta é a lista de IDs de entrada das pastas a serem sincronizadas se **UPS_THESE_FOLDERS** tiver sido definido.</span><span class="sxs-lookup"><span data-stu-id="6f419-132">[in] This is the list of entry IDs of the folders to synchronize if **UPS_THESE_FOLDERS** has been set.</span></span> <span data-ttu-id="6f419-133">Consulte mapidefs. h para a definição de tipo de **LPENTRYLIST**.</span><span class="sxs-lookup"><span data-stu-id="6f419-133">See mapidefs.h for the type definition of **LPENTRYLIST**.</span></span> 
    
 <span data-ttu-id="6f419-134">_pulFolderOptions_</span><span class="sxs-lookup"><span data-stu-id="6f419-134">_pulFolderOptions_</span></span>
  
- <span data-ttu-id="6f419-135">no Esta é uma matriz de opções de pasta para pastas correspondentes no *PEL* se **UPS_THESE_FOLDERS** tiver sido definido.</span><span class="sxs-lookup"><span data-stu-id="6f419-135">[in] This is an array of folder options for corresponding folders in  *pel*  if **UPS_THESE_FOLDERS** has been set.</span></span> <span data-ttu-id="6f419-136">Essas opções de pasta são usadas ao carregar cada uma das pastas listadas em *PEL* durante o [estado de carregamento da pasta](upload-folder-state.md).</span><span class="sxs-lookup"><span data-stu-id="6f419-136">These folder options are used when uploading each of the folders listed in  *pel*  during the [upload folder state](upload-folder-state.md).</span></span> <span data-ttu-id="6f419-137">Para obter mais informações sobre opções de pasta, consulte **[UPFLD](upfld.md)**.</span><span class="sxs-lookup"><span data-stu-id="6f419-137">For more information about folder options, see **[UPFLD](upfld.md)**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="6f419-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="6f419-138">See also</span></span>



[<span data-ttu-id="6f419-139">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="6f419-139">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="6f419-140">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="6f419-140">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="6f419-141">Constantes de MAPI</span><span class="sxs-lookup"><span data-stu-id="6f419-141">MAPI Constants</span></span>](mapi-constants.md)

