---
title: Baixar o estado do cabeçalho da mensagem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 03f69592-a5ea-e30b-9674-9cfa895163d8
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7407b6606634ecc0151f582e4481ecbff5e7dc57
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766443"
---
# <a name="download-message-header-state"></a><span data-ttu-id="9a929-103">Baixar o estado do cabeçalho da mensagem</span><span class="sxs-lookup"><span data-stu-id="9a929-103">Download Message Header State</span></span>

  
  
<span data-ttu-id="9a929-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9a929-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="9a929-105">Este tópico descreve o que acontece durante o estado de cabeçalho de mensagem de download da máquina de estado de replicação.</span><span class="sxs-lookup"><span data-stu-id="9a929-105">This topic describes what happens during the download message header state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="9a929-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="9a929-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9a929-107">Identificador de controle de sessão:</span><span class="sxs-lookup"><span data-stu-id="9a929-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="9a929-108">**LR_SYNC_DOWNLOAD_HEADER**</span><span class="sxs-lookup"><span data-stu-id="9a929-108">**LR_SYNC_DOWNLOAD_HEADER**</span></span> <br/> |
|<span data-ttu-id="9a929-109">Estrutura de dados relacionados:</span><span class="sxs-lookup"><span data-stu-id="9a929-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="9a929-110">**[HDRSYNC](hdrsync.md)**</span><span class="sxs-lookup"><span data-stu-id="9a929-110">**[HDRSYNC](hdrsync.md)**</span></span> <br/> |
|<span data-ttu-id="9a929-111">Desse estado:</span><span class="sxs-lookup"><span data-stu-id="9a929-111">From this state:</span></span>  <br/> |[<span data-ttu-id="9a929-112">Estado ocioso</span><span class="sxs-lookup"><span data-stu-id="9a929-112">Idle state</span></span>](idle-state.md) <br/> |
|<span data-ttu-id="9a929-113">Com esse estado:</span><span class="sxs-lookup"><span data-stu-id="9a929-113">To this state:</span></span>  <br/> |<span data-ttu-id="9a929-114">Estado ocioso</span><span class="sxs-lookup"><span data-stu-id="9a929-114">Idle state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="9a929-115">A máquina de estado de replicação é uma máquina de estado determinantes.</span><span class="sxs-lookup"><span data-stu-id="9a929-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="9a929-116">Um cliente partindo de um estado para outro eventualmente deve retornar para o anterior do último.</span><span class="sxs-lookup"><span data-stu-id="9a929-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="9a929-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="9a929-117">Description</span></span>

<span data-ttu-id="9a929-118">Durante esse estado, o cliente atualiza o cabeçalho de uma mensagem em um repositório local.</span><span class="sxs-lookup"><span data-stu-id="9a929-118">During this state, the client updates the header of a message on a local store.</span></span> <span data-ttu-id="9a929-119">Armazenamento local entra neste estado após **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** e sai quando **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)** é chamado.</span><span class="sxs-lookup"><span data-stu-id="9a929-119">The local store enters this state upon **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** and exits when **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)** is called.</span></span> <span data-ttu-id="9a929-120">Durante esse estado, o Outlook inicializa membros da estrutura de dados **HDRSYNC** associada com informações sobre o cabeçalho de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="9a929-120">During this state, Outlook initializes members of the associated **HDRSYNC** data structure with information about the header of a message.</span></span> <span data-ttu-id="9a929-121">O cliente primeiramente baixa o item de mensagem completa do servidor e atualiza o cabeçalho do item mensagem localmente.</span><span class="sxs-lookup"><span data-stu-id="9a929-121">The client first downloads the full message item from the server and then updates the header of the message item locally.</span></span> 
  
<span data-ttu-id="9a929-122">Quando a sincronização for encerrada, o cliente define os resultados de download.</span><span class="sxs-lookup"><span data-stu-id="9a929-122">When syncrhonization ends, the client sets the download results.</span></span> <span data-ttu-id="9a929-123">Armazenamento local retorna ao estado ocioso.</span><span class="sxs-lookup"><span data-stu-id="9a929-123">The local store returns to the idle state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9a929-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="9a929-124">See also</span></span>



[<span data-ttu-id="9a929-125">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="9a929-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="9a929-126">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="9a929-126">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="9a929-127">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="9a929-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="9a929-128">ESTADO DE SINCRONIZAÇÃO</span><span class="sxs-lookup"><span data-stu-id="9a929-128">SYNCSTATE</span></span>](syncstate.md)

