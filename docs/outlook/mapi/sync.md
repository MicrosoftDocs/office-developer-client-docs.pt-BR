---
title: SYNC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3f07fddf-4c42-6ea7-162d-57022166a83f
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: c856dfd1d419fd7a4bf4f47852ffb69470f9281b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770559"
---
# <a name="sync"></a><span data-ttu-id="9f43c-103">SYNC</span><span class="sxs-lookup"><span data-stu-id="9f43c-103">SYNC</span></span>

  
  
<span data-ttu-id="9f43c-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9f43c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9f43c-105">Informações para iniciar a sincronização entre um repositório local e um servidor.</span><span class="sxs-lookup"><span data-stu-id="9f43c-105">Information for starting synchronization between a local store and a server.</span></span> <span data-ttu-id="9f43c-106">Essas informações são usadas durante o [estado de sincronização](synchronize-state.md).</span><span class="sxs-lookup"><span data-stu-id="9f43c-106">This information is used during the [synchronize state](synchronize-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="9f43c-107">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="9f43c-107">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="9f43c-108">Members</span><span class="sxs-lookup"><span data-stu-id="9f43c-108">Members</span></span>

 <span data-ttu-id="9f43c-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9f43c-109">_ulFlags_</span></span>
  
- <span data-ttu-id="9f43c-110">[out] / [in] uma bitmask dos seguintes sinalizadores que modifica o comportamento durante a sincronização:</span><span class="sxs-lookup"><span data-stu-id="9f43c-110">[out]/[in] A bitmask of the following flags that modifies the behavior during synchronization:</span></span>
    
- <span data-ttu-id="9f43c-111">UPS_UPLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="9f43c-111">UPS_UPLOAD_ONLY</span></span>
    
  - <span data-ttu-id="9f43c-112">[in] O cliente realizarão somente carregamento.</span><span class="sxs-lookup"><span data-stu-id="9f43c-112">[in] The client will be performing only upload.</span></span> <span data-ttu-id="9f43c-113">Outlook retorna apenas pastas modificadas localmente.</span><span class="sxs-lookup"><span data-stu-id="9f43c-113">Outlook only returns locally modified folders.</span></span>
    
- <span data-ttu-id="9f43c-114">UPS_DNLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="9f43c-114">UPS_DNLOAD_ONLY</span></span>
    
  - <span data-ttu-id="9f43c-115">[in] O cliente realizarão somente download.</span><span class="sxs-lookup"><span data-stu-id="9f43c-115">[in] The client will be performing only download.</span></span> <span data-ttu-id="9f43c-116">Outlook não deve limpar os bits de carregamento de pastas.</span><span class="sxs-lookup"><span data-stu-id="9f43c-116">Outlook should not clear upload bits for folders.</span></span>
    
- <span data-ttu-id="9f43c-117">UPS_THESE_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="9f43c-117">UPS_THESE_FOLDERS</span></span>
    
  - <span data-ttu-id="9f43c-118">[in] O cliente será sincronizando um conjunto especificado de pastas com as IDs da entrada fornecida.</span><span class="sxs-lookup"><span data-stu-id="9f43c-118">[in] The client will be synchronizing a specified set of folders with the provided entry IDs.</span></span> <span data-ttu-id="9f43c-119">Este sinalizador pode ser combinado com o **UPS_UPLOAD_ONLY** ou **UPS_DNLOAD_ONLY** sinalizador.</span><span class="sxs-lookup"><span data-stu-id="9f43c-119">This flag can be combined with either the **UPS_UPLOAD_ONLY** or **UPS_DNLOAD_ONLY** flag.</span></span> 
    
- <span data-ttu-id="9f43c-120">UPS_OK</span><span class="sxs-lookup"><span data-stu-id="9f43c-120">UPS_OK</span></span>
    
  - <span data-ttu-id="9f43c-121">[out] Sincronização foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="9f43c-121">[out] Synchronization was successful.</span></span> <span data-ttu-id="9f43c-122">O cliente define esta após carregar ou conclui uma sincronização completa.</span><span class="sxs-lookup"><span data-stu-id="9f43c-122">The client sets this after uploading or a full synchronization completes.</span></span>
    
- 
    
    > [!NOTE]
    > <span data-ttu-id="9f43c-123">Mesmo que o cliente pode carregar ou totalmente sincronizar (carregar e baixar) pastas e itens com a API de replicação, o cliente especifica *ulFlags* com apenas uma direção da replicação ao mesmo tempo — o **UPS_UPLOAD_ONLY** ou Sinalizador **UPS_DNLOAD_ONLY** .</span><span class="sxs-lookup"><span data-stu-id="9f43c-123">Even though the client can either upload or fully synchronize (upload then download) folders and items with the Replication API, the client specifies  *ulFlags*  with only one direction of the replication at a time — either the **UPS_UPLOAD_ONLY** or **UPS_DNLOAD_ONLY** flag.</span></span> <span data-ttu-id="9f43c-124">No caso de uma sincronização completa, o cliente primeiro faz um carregamento com o sinalizador **UPS_UPLOAD_ONLY** e, em seguida, um download com o sinalizador **UPS_DNLOAD_ONLY** .</span><span class="sxs-lookup"><span data-stu-id="9f43c-124">In the case of a full synchronization, the client first does an upload with the **UPS_UPLOAD_ONLY** flag, and then a download with the **UPS_DNLOAD_ONLY** flag.</span></span> 
  
 <span data-ttu-id="9f43c-125">_pwzPath_</span><span class="sxs-lookup"><span data-stu-id="9f43c-125">_pwzPath_</span></span>
  
- <span data-ttu-id="9f43c-126">[out] Caminho para o armazenamento local.</span><span class="sxs-lookup"><span data-stu-id="9f43c-126">[out] Path to the local store.</span></span>
    
 <span data-ttu-id="9f43c-127">_Reserved1_</span><span class="sxs-lookup"><span data-stu-id="9f43c-127">_Reserved1_</span></span>
  
- <span data-ttu-id="9f43c-128">Este membro é reservado para uso interno do Outlook e não é suportado.</span><span class="sxs-lookup"><span data-stu-id="9f43c-128">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="9f43c-129">_Reserved2_</span><span class="sxs-lookup"><span data-stu-id="9f43c-129">_Reserved2_</span></span>
  
- <span data-ttu-id="9f43c-130">Este membro é reservado para uso interno do Outlook e não é suportado.</span><span class="sxs-lookup"><span data-stu-id="9f43c-130">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="9f43c-131">*PEL*</span><span class="sxs-lookup"><span data-stu-id="9f43c-131">*pel*</span></span> 
  
- <span data-ttu-id="9f43c-132">[in] Esta é a lista de IDs das pastas para sincronizar se **UPS_THESE_FOLDERS** tiver sido definida de entrada.</span><span class="sxs-lookup"><span data-stu-id="9f43c-132">[in] This is the list of entry IDs of the folders to synchronize if **UPS_THESE_FOLDERS** has been set.</span></span> <span data-ttu-id="9f43c-133">Consulte mapidefs.h para a definição de tipo de **LPENTRYLIST**.</span><span class="sxs-lookup"><span data-stu-id="9f43c-133">See mapidefs.h for the type definition of **LPENTRYLIST**.</span></span> 
    
 <span data-ttu-id="9f43c-134">_pulFolderOptions_</span><span class="sxs-lookup"><span data-stu-id="9f43c-134">_pulFolderOptions_</span></span>
  
- <span data-ttu-id="9f43c-135">[in] Isso é uma matriz das opções de pasta para pastas correspondentes no *pel* se **UPS_THESE_FOLDERS** tiver sido definida.</span><span class="sxs-lookup"><span data-stu-id="9f43c-135">[in] This is an array of folder options for corresponding folders in  *pel*  if **UPS_THESE_FOLDERS** has been set.</span></span> <span data-ttu-id="9f43c-136">Essas opções de pasta são usadas quando o carregamento de cada uma das pastas listadas no *pel* durante o [carregamento do estado da pasta](upload-folder-state.md).</span><span class="sxs-lookup"><span data-stu-id="9f43c-136">These folder options are used when uploading each of the folders listed in  *pel*  during the [upload folder state](upload-folder-state.md).</span></span> <span data-ttu-id="9f43c-137">Para obter mais informações sobre opções de pasta, consulte **[UPFLD](upfld.md)**.</span><span class="sxs-lookup"><span data-stu-id="9f43c-137">For more information about folder options, see **[UPFLD](upfld.md)**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="9f43c-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="9f43c-138">See also</span></span>



[<span data-ttu-id="9f43c-139">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="9f43c-139">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="9f43c-140">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="9f43c-140">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="9f43c-141">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="9f43c-141">MAPI Constants</span></span>](mapi-constants.md)

