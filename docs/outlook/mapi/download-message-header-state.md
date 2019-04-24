---
title: Baixar o estado do cabeçalho da mensagem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 03f69592-a5ea-e30b-9674-9cfa895163d8
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c8e83119d724f583d40583a6a5227bc467dc94da
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338833"
---
# <a name="download-message-header-state"></a><span data-ttu-id="43964-103">Baixar o estado do cabeçalho da mensagem</span><span class="sxs-lookup"><span data-stu-id="43964-103">Download Message Header State</span></span>

  
  
<span data-ttu-id="43964-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="43964-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="43964-105">Este tópico descreve o que acontece durante o status de cabeçalho da mensagem de download da máquina de estado de replicação.</span><span class="sxs-lookup"><span data-stu-id="43964-105">This topic describes what happens during the download message header state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="43964-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="43964-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="43964-107">Identificador de Estado:</span><span class="sxs-lookup"><span data-stu-id="43964-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="43964-108">**LR_SYNC_DOWNLOAD_HEADER**</span><span class="sxs-lookup"><span data-stu-id="43964-108">**LR_SYNC_DOWNLOAD_HEADER**</span></span> <br/> |
|<span data-ttu-id="43964-109">Estrutura de dados relacionada:</span><span class="sxs-lookup"><span data-stu-id="43964-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="43964-110">**[HDRSYNC](hdrsync.md)**</span><span class="sxs-lookup"><span data-stu-id="43964-110">**[HDRSYNC](hdrsync.md)**</span></span> <br/> |
|<span data-ttu-id="43964-111">A partir deste Estado:</span><span class="sxs-lookup"><span data-stu-id="43964-111">From this state:</span></span>  <br/> |[<span data-ttu-id="43964-112">Estado Ocioso</span><span class="sxs-lookup"><span data-stu-id="43964-112">Idle state</span></span>](idle-state.md) <br/> |
|<span data-ttu-id="43964-113">Para este Estado:</span><span class="sxs-lookup"><span data-stu-id="43964-113">To this state:</span></span>  <br/> |<span data-ttu-id="43964-114">Estado Ocioso</span><span class="sxs-lookup"><span data-stu-id="43964-114">Idle state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="43964-115">A máquina de estado de replicação é uma máquina de estado determinista.</span><span class="sxs-lookup"><span data-stu-id="43964-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="43964-116">Um cliente que faz parte de um estado para outro deve eventualmente retornar para o primeiro a partir do último.</span><span class="sxs-lookup"><span data-stu-id="43964-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="43964-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="43964-117">Description</span></span>

<span data-ttu-id="43964-118">Durante esse Estado, o cliente atualiza o cabeçalho de uma mensagem em um repositório local.</span><span class="sxs-lookup"><span data-stu-id="43964-118">During this state, the client updates the header of a message on a local store.</span></span> <span data-ttu-id="43964-119">O repositório local entra nesse estado no **[IOSTX:: SyncHdrBeg](iostx-synchdrbeg.md)** e sai quando **[IOSTX:: SyncHdrEnd](iostx-synchdrend.md)** é chamado.</span><span class="sxs-lookup"><span data-stu-id="43964-119">The local store enters this state upon **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** and exits when **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)** is called.</span></span> <span data-ttu-id="43964-120">Durante esse Estado, o Outlook Inicializa membros da estrutura de dados do **HDRSYNC** associada com informações sobre o cabeçalho de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="43964-120">During this state, Outlook initializes members of the associated **HDRSYNC** data structure with information about the header of a message.</span></span> <span data-ttu-id="43964-121">O cliente primeiro baixa o item de mensagem completo do servidor e, em seguida, atualiza o cabeçalho do item de mensagem localmente.</span><span class="sxs-lookup"><span data-stu-id="43964-121">The client first downloads the full message item from the server and then updates the header of the message item locally.</span></span> 
  
<span data-ttu-id="43964-122">Quando o sincronização termina, o cliente define os resultados do download.</span><span class="sxs-lookup"><span data-stu-id="43964-122">When syncrhonization ends, the client sets the download results.</span></span> <span data-ttu-id="43964-123">O repositório local retorna ao estado ocioso.</span><span class="sxs-lookup"><span data-stu-id="43964-123">The local store returns to the idle state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="43964-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="43964-124">See also</span></span>



[<span data-ttu-id="43964-125">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="43964-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="43964-126">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="43964-126">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="43964-127">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="43964-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="43964-128">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="43964-128">SYNCSTATE</span></span>](syncstate.md)

