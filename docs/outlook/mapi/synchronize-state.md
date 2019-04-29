---
title: Sincronizar estado
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
# <a name="synchronize-state"></a><span data-ttu-id="54e7c-103">Sincronizar estado</span><span class="sxs-lookup"><span data-stu-id="54e7c-103">Synchronize State</span></span>

  
  
<span data-ttu-id="54e7c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="54e7c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="54e7c-105">Este tópico descreve o que acontece durante o estado de sincronização da máquina de estado de replicação.</span><span class="sxs-lookup"><span data-stu-id="54e7c-105">This topic describes what happens during the synchronize state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="54e7c-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="54e7c-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="54e7c-107">Identificador de Estado:</span><span class="sxs-lookup"><span data-stu-id="54e7c-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="54e7c-108">**LR_SYNC**</span><span class="sxs-lookup"><span data-stu-id="54e7c-108">**LR_SYNC**</span></span> <br/> |
|<span data-ttu-id="54e7c-109">Estrutura de dados relacionada:</span><span class="sxs-lookup"><span data-stu-id="54e7c-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="54e7c-110">**[SINCRONIZAÇÃO](sync.md)**</span><span class="sxs-lookup"><span data-stu-id="54e7c-110">**[SYNC](sync.md)**</span></span> <br/> |
|<span data-ttu-id="54e7c-111">A partir deste Estado:</span><span class="sxs-lookup"><span data-stu-id="54e7c-111">From this state:</span></span>  <br/> |[<span data-ttu-id="54e7c-112">Estado Ocioso</span><span class="sxs-lookup"><span data-stu-id="54e7c-112">Idle state</span></span>](idle-state.md) <br/> |
|<span data-ttu-id="54e7c-113">Para este Estado:</span><span class="sxs-lookup"><span data-stu-id="54e7c-113">To this state:</span></span>  <br/> |<span data-ttu-id="54e7c-114">[Estado de hierarquia de download](download-hierarchy-state.md), sincronizar estado do [conteúdo](synchronize-contents-state.md), estado da [hierarquia de carregamento](upload-hierarchy-state.md)ou estado ocioso</span><span class="sxs-lookup"><span data-stu-id="54e7c-114">[Download hierarchy state](download-hierarchy-state.md), [synchronize contents state](synchronize-contents-state.md), [upload hierarchy state](upload-hierarchy-state.md), or idle state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="54e7c-115">A máquina de estado de replicação é uma máquina de estado determinista.</span><span class="sxs-lookup"><span data-stu-id="54e7c-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="54e7c-116">Um cliente que faz parte de um estado para outro deve eventualmente retornar para o primeiro a partir do último.</span><span class="sxs-lookup"><span data-stu-id="54e7c-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="54e7c-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="54e7c-117">Description</span></span>

<span data-ttu-id="54e7c-118">Este estado inicia a sincronização.</span><span class="sxs-lookup"><span data-stu-id="54e7c-118">This state initiates synchronization.</span></span> <span data-ttu-id="54e7c-119">Um repositório local pode fazer a transição para um upload ou um estado de download a partir daqui.</span><span class="sxs-lookup"><span data-stu-id="54e7c-119">A local store can transition to an upload or a download state from here.</span></span> <span data-ttu-id="54e7c-120">Por exemplo, um repositório local pode ser movido para o estado de hierarquia de upload para carregar uma hierarquia de pastas para o servidor ou pode executar uma sincronização completa carregando primeiro a hierarquia e, em seguida, baixando a hierarquia do servidor.</span><span class="sxs-lookup"><span data-stu-id="54e7c-120">For example, a local store can move to the upload hierarchy state to upload a folder hierarchy to the server, or it can perform a full synchronization by first uploading the hierarchy and then downloading the hierarchy from the server.</span></span>
  
<span data-ttu-id="54e7c-121">Durante esse Estado, o Outlook Inicializa a estrutura de dados de **sincronização** associada com o caminho para o repositório local, para que o Outlook Veja modificações durante outros Estados.</span><span class="sxs-lookup"><span data-stu-id="54e7c-121">During this state, Outlook initializes the associated **SYNC** data structure with the path to the local store, so that Outlook sees modifications during other states.</span></span> 
  
<span data-ttu-id="54e7c-122">O cliente define os membros [in] de **Sync**, que dizem ao Outlook como lidar com outros Estados.</span><span class="sxs-lookup"><span data-stu-id="54e7c-122">The client sets the [in] members of **SYNC**, which tells Outlook how to handle other states.</span></span> <span data-ttu-id="54e7c-123">Por exemplo, o cliente pode definir *parâmetroulflags* como **UPS_UPLOAD_ONLY** e **UPS_THESE_FOLDERS** e *PEL* como uma lista de identificadores de entrada das pastas para informar ao Outlook que somente essas pastas serão carregadas.</span><span class="sxs-lookup"><span data-stu-id="54e7c-123">For example, the client can set  *ulFlags*  to **UPS_UPLOAD_ONLY** and **UPS_THESE_FOLDERS** and  *pel*  to a list of entry identifiers of the folders to tell Outlook that only these folders will be uploaded.</span></span> <span data-ttu-id="54e7c-124">Quando esse estado termina, o repositório local reverte para o estado ocioso.</span><span class="sxs-lookup"><span data-stu-id="54e7c-124">When this state ends, the local store reverts to the idle state.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="54e7c-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="54e7c-125">See also</span></span>



[<span data-ttu-id="54e7c-126">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="54e7c-126">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="54e7c-127">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="54e7c-127">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="54e7c-128">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="54e7c-128">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="54e7c-129">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="54e7c-129">SYNCSTATE</span></span>](syncstate.md)

