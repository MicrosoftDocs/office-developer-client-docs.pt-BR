---
title: Estado de Sincronização
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270ff414-514c-b1fc-db48-761bf6de8867
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7abbf049a848d417f640528e5030e37a954413e5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414624"
---
# <a name="synchronize-state"></a><span data-ttu-id="2f1a4-103">Estado de Sincronização</span><span class="sxs-lookup"><span data-stu-id="2f1a4-103">Synchronize State</span></span>

  
  
<span data-ttu-id="2f1a4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2f1a4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="2f1a4-105">Este tópico descreve o que acontece durante o estado de sincronização da máquina de estado de replicação.</span><span class="sxs-lookup"><span data-stu-id="2f1a4-105">This topic describes what happens during the synchronize state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="2f1a4-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="2f1a4-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2f1a4-107">Identificador de Estado:</span><span class="sxs-lookup"><span data-stu-id="2f1a4-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="2f1a4-108">**LR_SYNC**</span><span class="sxs-lookup"><span data-stu-id="2f1a4-108">**LR_SYNC**</span></span> <br/> |
|<span data-ttu-id="2f1a4-109">Estrutura de dados relacionada:</span><span class="sxs-lookup"><span data-stu-id="2f1a4-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="2f1a4-110">**[SYNC](sync.md)**</span><span class="sxs-lookup"><span data-stu-id="2f1a4-110">**[SYNC](sync.md)**</span></span> <br/> |
|<span data-ttu-id="2f1a4-111">Desse estado:</span><span class="sxs-lookup"><span data-stu-id="2f1a4-111">From this state:</span></span>  <br/> |[<span data-ttu-id="2f1a4-112">Estado Ocioso</span><span class="sxs-lookup"><span data-stu-id="2f1a4-112">Idle state</span></span>](idle-state.md) <br/> |
|<span data-ttu-id="2f1a4-113">Para esse estado:</span><span class="sxs-lookup"><span data-stu-id="2f1a4-113">To this state:</span></span>  <br/> |<span data-ttu-id="2f1a4-114">[Estado de hierarquia de download,](download-hierarchy-state.md) [estado de sincronização de conteúdo,](synchronize-contents-state.md)estado [de hierarquia de carregamento](upload-hierarchy-state.md)ou estado ocioso</span><span class="sxs-lookup"><span data-stu-id="2f1a4-114">[Download hierarchy state](download-hierarchy-state.md), [synchronize contents state](synchronize-contents-state.md), [upload hierarchy state](upload-hierarchy-state.md), or idle state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="2f1a4-115">A máquina de estado de replicação é uma máquina de estado determinística.</span><span class="sxs-lookup"><span data-stu-id="2f1a4-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="2f1a4-116">Um cliente que sai de um estado para outro eventualmente deve retornar ao primeiro do último.</span><span class="sxs-lookup"><span data-stu-id="2f1a4-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="2f1a4-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="2f1a4-117">Description</span></span>

<span data-ttu-id="2f1a4-118">Esse estado inicia a sincronização.</span><span class="sxs-lookup"><span data-stu-id="2f1a4-118">This state initiates synchronization.</span></span> <span data-ttu-id="2f1a4-119">Um armazenamento local pode fazer a transição para um estado de upload ou download a partir daqui.</span><span class="sxs-lookup"><span data-stu-id="2f1a4-119">A local store can transition to an upload or a download state from here.</span></span> <span data-ttu-id="2f1a4-120">Por exemplo, um armazenamento local pode mover para o estado de hierarquia de carregamento para carregar uma hierarquia de pastas para o servidor ou pode executar uma sincronização completa carregando primeiro a hierarquia e, em seguida, baixando a hierarquia do servidor.</span><span class="sxs-lookup"><span data-stu-id="2f1a4-120">For example, a local store can move to the upload hierarchy state to upload a folder hierarchy to the server, or it can perform a full synchronization by first uploading the hierarchy and then downloading the hierarchy from the server.</span></span>
  
<span data-ttu-id="2f1a4-121">Durante esse estado, o Outlook inicializa a estrutura de dados **SYNC** associada com o caminho para o armazenamento local, para que o Outlook veja modificações durante outros estados.</span><span class="sxs-lookup"><span data-stu-id="2f1a4-121">During this state, Outlook initializes the associated **SYNC** data structure with the path to the local store, so that Outlook sees modifications during other states.</span></span> 
  
<span data-ttu-id="2f1a4-122">O cliente define os membros [in] de **SYNC**, que informa ao Outlook como lidar com outros estados.</span><span class="sxs-lookup"><span data-stu-id="2f1a4-122">The client sets the [in] members of **SYNC**, which tells Outlook how to handle other states.</span></span> <span data-ttu-id="2f1a4-123">Por exemplo, o cliente pode definir  *ulFlags*  como **UPS_UPLOAD_ONLY** e **UPS_THESE_FOLDERS** e  *pel*  para uma lista de identificadores de entrada das pastas para dizer ao Outlook que somente essas pastas serão carregadas.</span><span class="sxs-lookup"><span data-stu-id="2f1a4-123">For example, the client can set  *ulFlags*  to **UPS_UPLOAD_ONLY** and **UPS_THESE_FOLDERS** and  *pel*  to a list of entry identifiers of the folders to tell Outlook that only these folders will be uploaded.</span></span> <span data-ttu-id="2f1a4-124">Quando esse estado termina, o armazenamento local reverte para o estado ocioso.</span><span class="sxs-lookup"><span data-stu-id="2f1a4-124">When this state ends, the local store reverts to the idle state.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2f1a4-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="2f1a4-125">See also</span></span>



[<span data-ttu-id="2f1a4-126">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="2f1a4-126">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="2f1a4-127">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="2f1a4-127">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="2f1a4-128">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="2f1a4-128">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="2f1a4-129">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="2f1a4-129">SYNCSTATE</span></span>](syncstate.md)

