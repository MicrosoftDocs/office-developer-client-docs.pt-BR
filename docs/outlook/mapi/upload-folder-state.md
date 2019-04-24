---
title: Carregar estado da pasta
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270b1df0-c5cd-0d0f-7b57-2726dee978ab
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c20f2998a2fef1ddb53b13708dcf56f9d7b50dbe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348423"
---
# <a name="upload-folder-state"></a><span data-ttu-id="f9ebb-103">Carregar estado da pasta</span><span class="sxs-lookup"><span data-stu-id="f9ebb-103">Upload Folder State</span></span>

  
  
<span data-ttu-id="f9ebb-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f9ebb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="f9ebb-105">Este tópico descreve o que acontece durante o estado da pasta de carregamento da máquina de estado de replicação.</span><span class="sxs-lookup"><span data-stu-id="f9ebb-105">This topic describes what happens during the upload folder state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="f9ebb-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="f9ebb-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f9ebb-107">Identificador de Estado:</span><span class="sxs-lookup"><span data-stu-id="f9ebb-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="f9ebb-108">**LR_SYNC_UPLOAD_FOLDER**</span><span class="sxs-lookup"><span data-stu-id="f9ebb-108">**LR_SYNC_UPLOAD_FOLDER**</span></span> <br/> |
|<span data-ttu-id="f9ebb-109">Estrutura de dados relacionada:</span><span class="sxs-lookup"><span data-stu-id="f9ebb-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="f9ebb-110">**[UPFLD](upfld.md)**</span><span class="sxs-lookup"><span data-stu-id="f9ebb-110">**[UPFLD](upfld.md)**</span></span> <br/> |
|<span data-ttu-id="f9ebb-111">A partir deste Estado:</span><span class="sxs-lookup"><span data-stu-id="f9ebb-111">From this state:</span></span>  <br/> |[<span data-ttu-id="f9ebb-112">Estado de hierarquia de upload</span><span class="sxs-lookup"><span data-stu-id="f9ebb-112">Upload hierarchy state</span></span>](upload-hierarchy-state.md) <br/> |
|<span data-ttu-id="f9ebb-113">Para este Estado:</span><span class="sxs-lookup"><span data-stu-id="f9ebb-113">To this state:</span></span>  <br/> |<span data-ttu-id="f9ebb-114">Estado de hierarquia de upload</span><span class="sxs-lookup"><span data-stu-id="f9ebb-114">Upload hierarchy state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="f9ebb-115">A máquina de estado de replicação é uma máquina de estado determinista.</span><span class="sxs-lookup"><span data-stu-id="f9ebb-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="f9ebb-116">Um cliente que faz parte de um estado para outro deve eventualmente retornar para o primeiro a partir do último.</span><span class="sxs-lookup"><span data-stu-id="f9ebb-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="f9ebb-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="f9ebb-117">Description</span></span>

<span data-ttu-id="f9ebb-118">Este estado inicia o carregamento de uma pasta em uma hierarquia que tenha sido especificada em um estado de hierarquia de carregamento anterior.</span><span class="sxs-lookup"><span data-stu-id="f9ebb-118">This state initiates uploading a folder in a hierarchy that has been specified in a preceding upload hierarchy state.</span></span> <span data-ttu-id="f9ebb-119">Durante esse Estado, o Outlook fornece o objeto Folder (se ele não tiver sido excluído) e os sinalizadores que indicam o estado da pasta (novo, movido, modificado ou excluído) como parte da estrutura de dados **UPFLD** correspondente.</span><span class="sxs-lookup"><span data-stu-id="f9ebb-119">During this state, Outlook provides the folder object (if it has not been deleted) and the flags indicating the state of the folder (new, moved, modified, or deleted) as part of the corresponding **UPFLD** data structure.</span></span> <span data-ttu-id="f9ebb-120">O cliente carrega essas informações no servidor.</span><span class="sxs-lookup"><span data-stu-id="f9ebb-120">The client then uploads this information to the server.</span></span> 
  
<span data-ttu-id="f9ebb-121">Se o upload for bem-sucedido, o cliente define *parâmetroulflags* no **UPFLD** como **UPF_OK**.</span><span class="sxs-lookup"><span data-stu-id="f9ebb-121">If the upload is successful, the client sets  *ulFlags*  in **UPFLD** to **UPF_OK**.</span></span> <span data-ttu-id="f9ebb-122">O Outlook, em seguida, limpa suas informações internas sobre a solicitação para carregar a pasta.</span><span class="sxs-lookup"><span data-stu-id="f9ebb-122">Outlook then clears its internal information about the request to upload the folder.</span></span> 
  
<span data-ttu-id="f9ebb-123">Quando o carregamento da pasta termina, o repositório local retorna ao estado de hierarquia de upload.</span><span class="sxs-lookup"><span data-stu-id="f9ebb-123">When the folder upload ends, the local store returns to the upload hierarchy state.</span></span> <span data-ttu-id="f9ebb-124">Com base na estrutura **[UPHIER](uphier.md)** correspondente ao estado de hierarquia de carregamento anterior, o Outlook determina se deve continuar carregando a próxima pasta e se preparar para o próximo estado de pasta de carregamento.</span><span class="sxs-lookup"><span data-stu-id="f9ebb-124">Based on the **[UPHIER](uphier.md)** structure corresponding to the preceding upload hierarchy state, Outlook determines whether to proceed with uploading the next folder and to prepare for the next upload folder state.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f9ebb-125">Se o cliente precisar carregar apenas uma pasta, o cliente poderá iniciar a replicação por meio do [estado de sincronização](synchronize-state.md) sem entrar no estado de hierarquia de carregamento.</span><span class="sxs-lookup"><span data-stu-id="f9ebb-125">If the client needs to upload only one folder, the client can initiate the replication through the [synchronize state](synchronize-state.md) without entering the upload hierarchy state.</span></span> <span data-ttu-id="f9ebb-126">O cliente define determinados membros de **[Sync](sync.md)** — *parâmetroulflags* para **UPS_UPLOAD_ONLY** e **UPS_ONE_FOLDER** e *feid* para a ID da pasta, para informar ao Outlook que apenas uma pasta será carregada.</span><span class="sxs-lookup"><span data-stu-id="f9ebb-126">The client sets certain members of **[SYNC](sync.md)** —  *ulFlags*  to **UPS_UPLOAD_ONLY** and **UPS_ONE_FOLDER** and  *feid*  to the folder's ID — to tell Outlook that only one folder will be uploaded.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f9ebb-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="f9ebb-127">See also</span></span>



[<span data-ttu-id="f9ebb-128">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="f9ebb-128">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="f9ebb-129">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="f9ebb-129">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="f9ebb-130">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="f9ebb-130">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="f9ebb-131">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="f9ebb-131">SYNCSTATE</span></span>](syncstate.md)

