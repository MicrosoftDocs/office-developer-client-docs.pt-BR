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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433805"
---
# <a name="sync"></a><span data-ttu-id="153e5-103">SYNC</span><span class="sxs-lookup"><span data-stu-id="153e5-103">SYNC</span></span>

  
  
<span data-ttu-id="153e5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="153e5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="153e5-105">Informações para iniciar a sincronização entre um armazenamento local e um servidor.</span><span class="sxs-lookup"><span data-stu-id="153e5-105">Information for starting synchronization between a local store and a server.</span></span> <span data-ttu-id="153e5-106">Essas informações são usadas durante o [estado de sincronização.](synchronize-state.md)</span><span class="sxs-lookup"><span data-stu-id="153e5-106">This information is used during the [synchronize state](synchronize-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="153e5-107">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="153e5-107">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="153e5-108">Membros</span><span class="sxs-lookup"><span data-stu-id="153e5-108">Members</span></span>

 <span data-ttu-id="153e5-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="153e5-109">_ulFlags_</span></span>
  
- <span data-ttu-id="153e5-110">[out]/[in] Uma máscara de bits dos seguintes sinalizadores que modifica o comportamento durante a sincronização:</span><span class="sxs-lookup"><span data-stu-id="153e5-110">[out]/[in] A bitmask of the following flags that modifies the behavior during synchronization:</span></span>
    
- <span data-ttu-id="153e5-111">UPS_UPLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="153e5-111">UPS_UPLOAD_ONLY</span></span>
    
  - <span data-ttu-id="153e5-112">[in] O cliente executará apenas o upload.</span><span class="sxs-lookup"><span data-stu-id="153e5-112">[in] The client will be performing only upload.</span></span> <span data-ttu-id="153e5-113">O Outlook só retorna pastas modificadas localmente.</span><span class="sxs-lookup"><span data-stu-id="153e5-113">Outlook only returns locally modified folders.</span></span>
    
- <span data-ttu-id="153e5-114">UPS_DNLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="153e5-114">UPS_DNLOAD_ONLY</span></span>
    
  - <span data-ttu-id="153e5-115">[in] O cliente executará apenas o download.</span><span class="sxs-lookup"><span data-stu-id="153e5-115">[in] The client will be performing only download.</span></span> <span data-ttu-id="153e5-116">Outlook should not clear upload bits for folders.</span><span class="sxs-lookup"><span data-stu-id="153e5-116">Outlook should not clear upload bits for folders.</span></span>
    
- <span data-ttu-id="153e5-117">UPS_THESE_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="153e5-117">UPS_THESE_FOLDERS</span></span>
    
  - <span data-ttu-id="153e5-118">[in] O cliente sincroniza um conjunto especificado de pastas com as IDs de entrada fornecidas.</span><span class="sxs-lookup"><span data-stu-id="153e5-118">[in] The client will be synchronizing a specified set of folders with the provided entry IDs.</span></span> <span data-ttu-id="153e5-119">Esse sinalizador pode ser combinado com o sinalizador **UPS_UPLOAD_ONLY** ou **UPS_DNLOAD_ONLY** sinalização.</span><span class="sxs-lookup"><span data-stu-id="153e5-119">This flag can be combined with either the **UPS_UPLOAD_ONLY** or **UPS_DNLOAD_ONLY** flag.</span></span> 
    
- <span data-ttu-id="153e5-120">UPS_OK</span><span class="sxs-lookup"><span data-stu-id="153e5-120">UPS_OK</span></span>
    
  - <span data-ttu-id="153e5-121">[out] A sincronização foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="153e5-121">[out] Synchronization was successful.</span></span> <span data-ttu-id="153e5-122">O cliente define isso após o carregamento ou uma sincronização completa é concluída.</span><span class="sxs-lookup"><span data-stu-id="153e5-122">The client sets this after uploading or a full synchronization completes.</span></span>
    
- 
    
    > [!NOTE]
    > <span data-ttu-id="153e5-123">Mesmo que o cliente possa carregar ou sincronizar totalmente (carregar e baixar) pastas e itens com a API de Replicação, o cliente especifica *ulFlags* com apenas uma direção da replicação por vez — o sinalizador **UPS_UPLOAD_ONLY** ou **UPS_DNLOAD_ONLY.**</span><span class="sxs-lookup"><span data-stu-id="153e5-123">Even though the client can either upload or fully synchronize (upload then download) folders and items with the Replication API, the client specifies  *ulFlags*  with only one direction of the replication at a time — either the **UPS_UPLOAD_ONLY** or **UPS_DNLOAD_ONLY** flag.</span></span> <span data-ttu-id="153e5-124">No caso de uma sincronização completa, o cliente primeiro faz um upload com o sinalizador **UPS_UPLOAD_ONLY** e, em seguida, um download com o sinalizador **UPS_DNLOAD_ONLY** cliente.</span><span class="sxs-lookup"><span data-stu-id="153e5-124">In the case of a full synchronization, the client first does an upload with the **UPS_UPLOAD_ONLY** flag, and then a download with the **UPS_DNLOAD_ONLY** flag.</span></span> 
  
 <span data-ttu-id="153e5-125">_pwzPath_</span><span class="sxs-lookup"><span data-stu-id="153e5-125">_pwzPath_</span></span>
  
- <span data-ttu-id="153e5-126">[out] Caminho para o armazenamento local.</span><span class="sxs-lookup"><span data-stu-id="153e5-126">[out] Path to the local store.</span></span>
    
 <span data-ttu-id="153e5-127">_Reserved1_</span><span class="sxs-lookup"><span data-stu-id="153e5-127">_Reserved1_</span></span>
  
- <span data-ttu-id="153e5-128">Este membro é reservado para uso interno do Outlook e não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="153e5-128">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="153e5-129">_Reserved2_</span><span class="sxs-lookup"><span data-stu-id="153e5-129">_Reserved2_</span></span>
  
- <span data-ttu-id="153e5-130">Este membro é reservado para uso interno do Outlook e não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="153e5-130">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="153e5-131">*pel*</span><span class="sxs-lookup"><span data-stu-id="153e5-131">*pel*</span></span> 
  
- <span data-ttu-id="153e5-132">[in] Esta é a lista de IDs de entrada das pastas a sincronizar **se** UPS_THESE_FOLDERS tiver sido definida.</span><span class="sxs-lookup"><span data-stu-id="153e5-132">[in] This is the list of entry IDs of the folders to synchronize if **UPS_THESE_FOLDERS** has been set.</span></span> <span data-ttu-id="153e5-133">Consulte mapidefs.h para a definição de tipo de **LPENTRYLIST**.</span><span class="sxs-lookup"><span data-stu-id="153e5-133">See mapidefs.h for the type definition of **LPENTRYLIST**.</span></span> 
    
 <span data-ttu-id="153e5-134">_porqueFolderOptions_</span><span class="sxs-lookup"><span data-stu-id="153e5-134">_pulFolderOptions_</span></span>
  
- <span data-ttu-id="153e5-135">[in] Esta é uma matriz de opções de pasta para pastas correspondentes no  *pel* **UPS_THESE_FOLDERS** tiver sido definida.</span><span class="sxs-lookup"><span data-stu-id="153e5-135">[in] This is an array of folder options for corresponding folders in  *pel*  if **UPS_THESE_FOLDERS** has been set.</span></span> <span data-ttu-id="153e5-136">Essas opções de pasta são usadas ao carregar cada uma das pastas listadas *na pel* durante o [estado da pasta de carregamento.](upload-folder-state.md)</span><span class="sxs-lookup"><span data-stu-id="153e5-136">These folder options are used when uploading each of the folders listed in  *pel*  during the [upload folder state](upload-folder-state.md).</span></span> <span data-ttu-id="153e5-137">Para obter mais informações sobre opções de pasta, consulte **[UPFLD](upfld.md)**.</span><span class="sxs-lookup"><span data-stu-id="153e5-137">For more information about folder options, see **[UPFLD](upfld.md)**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="153e5-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="153e5-138">See also</span></span>



[<span data-ttu-id="153e5-139">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="153e5-139">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="153e5-140">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="153e5-140">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="153e5-141">Constantes de MAPI</span><span class="sxs-lookup"><span data-stu-id="153e5-141">MAPI Constants</span></span>](mapi-constants.md)

