---
title: Sincronizar o estado
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270ff414-514c-b1fc-db48-761bf6de8867
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 36bdeecfaaa94492b1e719dbd1cf455bfa40db47
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770567"
---
# <a name="synchronize-state"></a><span data-ttu-id="11222-103">Sincronizar o estado</span><span class="sxs-lookup"><span data-stu-id="11222-103">Synchronize State</span></span>

  
  
<span data-ttu-id="11222-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="11222-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="11222-105">Este tópico descreve o que acontece durante o estado de sincronização da máquina de estado de replicação.</span><span class="sxs-lookup"><span data-stu-id="11222-105">This topic describes what happens during the synchronize state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="11222-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="11222-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="11222-107">Identificador de controle de sessão:</span><span class="sxs-lookup"><span data-stu-id="11222-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="11222-108">**LR_SYNC**</span><span class="sxs-lookup"><span data-stu-id="11222-108">**LR_SYNC**</span></span> <br/> |
|<span data-ttu-id="11222-109">Estrutura de dados relacionados:</span><span class="sxs-lookup"><span data-stu-id="11222-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="11222-110">**[SYNC](sync.md)**</span><span class="sxs-lookup"><span data-stu-id="11222-110">**[SYNC](sync.md)**</span></span> <br/> |
|<span data-ttu-id="11222-111">Desse estado:</span><span class="sxs-lookup"><span data-stu-id="11222-111">From this state:</span></span>  <br/> |[<span data-ttu-id="11222-112">Estado ocioso</span><span class="sxs-lookup"><span data-stu-id="11222-112">Idle state</span></span>](idle-state.md) <br/> |
|<span data-ttu-id="11222-113">Com esse estado:</span><span class="sxs-lookup"><span data-stu-id="11222-113">To this state:</span></span>  <br/> |<span data-ttu-id="11222-114">[Baixe o estado de hierarquia](download-hierarchy-state.md), [sincronizar o estado de conteúdo](synchronize-contents-state.md), [carregar o estado de hierarquia](upload-hierarchy-state.md)ou estado ocioso</span><span class="sxs-lookup"><span data-stu-id="11222-114">[Download hierarchy state](download-hierarchy-state.md), [synchronize contents state](synchronize-contents-state.md), [upload hierarchy state](upload-hierarchy-state.md), or idle state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="11222-115">A máquina de estado de replicação é uma máquina de estado determinantes.</span><span class="sxs-lookup"><span data-stu-id="11222-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="11222-116">Um cliente partindo de um estado para outro eventualmente deve retornar para o anterior do último.</span><span class="sxs-lookup"><span data-stu-id="11222-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="11222-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="11222-117">Description</span></span>

<span data-ttu-id="11222-118">Nesse estado inicia a sincronização.</span><span class="sxs-lookup"><span data-stu-id="11222-118">This state initiates synchronization.</span></span> <span data-ttu-id="11222-119">Um repositório local pode fazer a transição para um carregamento ou em um estado de download, a partir daqui.</span><span class="sxs-lookup"><span data-stu-id="11222-119">A local store can transition to an upload or a download state from here.</span></span> <span data-ttu-id="11222-120">Por exemplo, um repositório local pode mover para o estado de hierarquia de carregar para carregar uma hierarquia de pastas no servidor, ou ele pode executar uma sincronização completa primeiro carregamento da hierarquia e, em seguida, baixando a hierarquia do servidor.</span><span class="sxs-lookup"><span data-stu-id="11222-120">For example, a local store can move to the upload hierarchy state to upload a folder hierarchy to the server, or it can perform a full synchronization by first uploading the hierarchy and then downloading the hierarchy from the server.</span></span>
  
<span data-ttu-id="11222-121">Durante esse estado, o Outlook inicializa a estrutura de dados de **sincronização** associada com o caminho para o repositório local, para que o Outlook vê modificações durante outros estados.</span><span class="sxs-lookup"><span data-stu-id="11222-121">During this state, Outlook initializes the associated **SYNC** data structure with the path to the local store, so that Outlook sees modifications during other states.</span></span> 
  
<span data-ttu-id="11222-122">O cliente define o [in] membros de **sincronização**, que informa ao Outlook como lidar com outros estados.</span><span class="sxs-lookup"><span data-stu-id="11222-122">The client sets the [in] members of **SYNC**, which tells Outlook how to handle other states.</span></span> <span data-ttu-id="11222-123">Por exemplo, o cliente pode definir *ulFlags* **UPS_UPLOAD_ONLY** e **UPS_THESE_FOLDERS** e *pel* a uma lista de identificadores de entrada das pastas para informar ao Outlook que apenas essas pastas será carregado.</span><span class="sxs-lookup"><span data-stu-id="11222-123">For example, the client can set  *ulFlags*  to **UPS_UPLOAD_ONLY** and **UPS_THESE_FOLDERS** and  *pel*  to a list of entry identifiers of the folders to tell Outlook that only these folders will be uploaded.</span></span> <span data-ttu-id="11222-124">Quando for encerrada nesse estado, o armazenamento local será revertido para o estado ocioso.</span><span class="sxs-lookup"><span data-stu-id="11222-124">When this state ends, the local store reverts to the idle state.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="11222-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="11222-125">See also</span></span>



[<span data-ttu-id="11222-126">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="11222-126">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="11222-127">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="11222-127">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="11222-128">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="11222-128">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="11222-129">ESTADO DE SINCRONIZAÇÃO</span><span class="sxs-lookup"><span data-stu-id="11222-129">SYNCSTATE</span></span>](syncstate.md)

