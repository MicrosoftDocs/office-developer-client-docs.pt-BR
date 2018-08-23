---
title: Carregar o estado das pastas
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270b1df0-c5cd-0d0f-7b57-2726dee978ab
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ae8c3c4012874e1ca35761b103066cceebb1b165
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576747"
---
# <a name="upload-folder-state"></a><span data-ttu-id="746a0-103">Carregar o estado das pastas</span><span class="sxs-lookup"><span data-stu-id="746a0-103">Upload Folder State</span></span>

  
  
<span data-ttu-id="746a0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="746a0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="746a0-105">Este tópico descreve o que acontece durante o estado da pasta de carregamento da máquina de estado de replicação.</span><span class="sxs-lookup"><span data-stu-id="746a0-105">This topic describes what happens during the upload folder state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="746a0-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="746a0-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="746a0-107">Identificador de controle de sessão:</span><span class="sxs-lookup"><span data-stu-id="746a0-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="746a0-108">**LR_SYNC_UPLOAD_FOLDER**</span><span class="sxs-lookup"><span data-stu-id="746a0-108">**LR_SYNC_UPLOAD_FOLDER**</span></span> <br/> |
|<span data-ttu-id="746a0-109">Estrutura de dados relacionados:</span><span class="sxs-lookup"><span data-stu-id="746a0-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="746a0-110">**[UPFLD](upfld.md)**</span><span class="sxs-lookup"><span data-stu-id="746a0-110">**[UPFLD](upfld.md)**</span></span> <br/> |
|<span data-ttu-id="746a0-111">Desse estado:</span><span class="sxs-lookup"><span data-stu-id="746a0-111">From this state:</span></span>  <br/> |[<span data-ttu-id="746a0-112">Carregar o estado de hierarquia</span><span class="sxs-lookup"><span data-stu-id="746a0-112">Upload hierarchy state</span></span>](upload-hierarchy-state.md) <br/> |
|<span data-ttu-id="746a0-113">Com esse estado:</span><span class="sxs-lookup"><span data-stu-id="746a0-113">To this state:</span></span>  <br/> |<span data-ttu-id="746a0-114">Carregar o estado de hierarquia</span><span class="sxs-lookup"><span data-stu-id="746a0-114">Upload hierarchy state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="746a0-115">A máquina de estado de replicação é uma máquina de estado determinantes.</span><span class="sxs-lookup"><span data-stu-id="746a0-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="746a0-116">Um cliente partindo de um estado para outro eventualmente deve retornar para o anterior do último.</span><span class="sxs-lookup"><span data-stu-id="746a0-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="746a0-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="746a0-117">Description</span></span>

<span data-ttu-id="746a0-118">Nesse estado inicia o carregamento de uma pasta em uma hierarquia que foi especificada em um estado de hierarquia de carregamento anterior.</span><span class="sxs-lookup"><span data-stu-id="746a0-118">This state initiates uploading a folder in a hierarchy that has been specified in a preceding upload hierarchy state.</span></span> <span data-ttu-id="746a0-119">Durante esse estado, o Outlook fornece o objeto folder (se não tiver sido excluída) e os sinalizadores que indica o estado da pasta (novas e movidas, modificados ou excluídos) como parte da estrutura de dados **UPFLD** correspondente.</span><span class="sxs-lookup"><span data-stu-id="746a0-119">During this state, Outlook provides the folder object (if it has not been deleted) and the flags indicating the state of the folder (new, moved, modified, or deleted) as part of the corresponding **UPFLD** data structure.</span></span> <span data-ttu-id="746a0-120">O cliente então carrega essas informações ao servidor.</span><span class="sxs-lookup"><span data-stu-id="746a0-120">The client then uploads this information to the server.</span></span> 
  
<span data-ttu-id="746a0-121">Se o carregamento for bem-sucedida, o cliente define *ulFlags* **UPFLD** para **UPF_OK**.</span><span class="sxs-lookup"><span data-stu-id="746a0-121">If the upload is successful, the client sets  *ulFlags*  in **UPFLD** to **UPF_OK**.</span></span> <span data-ttu-id="746a0-122">Outlook depois limpá suas informações internas sobre a solicitação para carregar a pasta.</span><span class="sxs-lookup"><span data-stu-id="746a0-122">Outlook then clears its internal information about the request to upload the folder.</span></span> 
  
<span data-ttu-id="746a0-123">Quando o carregamento da pasta for encerrada, armazenamento local retorna ao estado de hierarquia de carregamento.</span><span class="sxs-lookup"><span data-stu-id="746a0-123">When the folder upload ends, the local store returns to the upload hierarchy state.</span></span> <span data-ttu-id="746a0-124">Com base na estrutura **[UPHIER](uphier.md)** correspondente para o estado anterior de hierarquia de carregamento, o Outlook determina se para prosseguir com a carregar a pasta próxima e preparar para o próximo estado de pasta de carregamento.</span><span class="sxs-lookup"><span data-stu-id="746a0-124">Based on the **[UPHIER](uphier.md)** structure corresponding to the preceding upload hierarchy state, Outlook determines whether to proceed with uploading the next folder and to prepare for the next upload folder state.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="746a0-125">Se o cliente precisar carregar apenas uma pasta, o cliente pode iniciar a replicação por meio do [estado de sincronizar](synchronize-state.md) sem digitar o estado de hierarquia de carregamento.</span><span class="sxs-lookup"><span data-stu-id="746a0-125">If the client needs to upload only one folder, the client can initiate the replication through the [synchronize state](synchronize-state.md) without entering the upload hierarchy state.</span></span> <span data-ttu-id="746a0-126">O cliente define determinados membros de **[sincronização](sync.md)** — *ulFlags* **UPS_UPLOAD_ONLY** e **UPS_ONE_FOLDER** e *feid* a identificação da pasta — informar ao Outlook que apenas uma pasta será carregado.</span><span class="sxs-lookup"><span data-stu-id="746a0-126">The client sets certain members of **[SYNC](sync.md)** —  *ulFlags*  to **UPS_UPLOAD_ONLY** and **UPS_ONE_FOLDER** and  *feid*  to the folder's ID — to tell Outlook that only one folder will be uploaded.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="746a0-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="746a0-127">See also</span></span>



[<span data-ttu-id="746a0-128">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="746a0-128">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="746a0-129">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="746a0-129">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="746a0-130">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="746a0-130">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="746a0-131">ESTADO DE SINCRONIZAÇÃO</span><span class="sxs-lookup"><span data-stu-id="746a0-131">SYNCSTATE</span></span>](syncstate.md)

