---
title: Baixar o estado da tabela
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5bcc8b0a-0ab7-6c3e-8334-9e83cf2882a7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7451d159ef97ef9d8160b386ec5bf88fb388706e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338336"
---
# <a name="download-table-state"></a><span data-ttu-id="b4509-103">Baixar o estado da tabela</span><span class="sxs-lookup"><span data-stu-id="b4509-103">Download Table State</span></span>

  
  
<span data-ttu-id="b4509-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b4509-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="b4509-105">Este tópico descreve o que acontece durante o estado de download da tabela da máquina de estado de replicação.</span><span class="sxs-lookup"><span data-stu-id="b4509-105">This topic describes what happens during the download table state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="b4509-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="b4509-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b4509-107">Identificador de Estado:</span><span class="sxs-lookup"><span data-stu-id="b4509-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="b4509-108">**LR_SYNC_DOWNLOAD_TABLE**</span><span class="sxs-lookup"><span data-stu-id="b4509-108">**LR_SYNC_DOWNLOAD_TABLE**</span></span> <br/> |
|<span data-ttu-id="b4509-109">Estrutura de dados relacionada:</span><span class="sxs-lookup"><span data-stu-id="b4509-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="b4509-110">**[DNTBL](dntbl.md)**</span><span class="sxs-lookup"><span data-stu-id="b4509-110">**[DNTBL](dntbl.md)**</span></span> <br/> |
|<span data-ttu-id="b4509-111">A partir deste Estado:</span><span class="sxs-lookup"><span data-stu-id="b4509-111">From this state:</span></span>  <br/> |[<span data-ttu-id="b4509-112">Sincronizar o estado do conteúdo</span><span class="sxs-lookup"><span data-stu-id="b4509-112">Synchronize contents state</span></span>](synchronize-contents-state.md) <br/> |
|<span data-ttu-id="b4509-113">Para este Estado:</span><span class="sxs-lookup"><span data-stu-id="b4509-113">To this state:</span></span>  <br/> |<span data-ttu-id="b4509-114">Sincronizar o estado do conteúdo</span><span class="sxs-lookup"><span data-stu-id="b4509-114">Synchronize contents state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="b4509-115">A máquina de estado de replicação é uma máquina de estado determinista.</span><span class="sxs-lookup"><span data-stu-id="b4509-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="b4509-116">Um cliente que faz parte de um estado para outro deve eventualmente retornar para o primeiro a partir do último.</span><span class="sxs-lookup"><span data-stu-id="b4509-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="b4509-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="b4509-117">Description</span></span>

<span data-ttu-id="b4509-118">Este estado inicia o download de uma pasta.</span><span class="sxs-lookup"><span data-stu-id="b4509-118">This state initiates downloading a folder.</span></span> <span data-ttu-id="b4509-119">Durante esse Estado, o Outlook Inicializa a estrutura de dados **DNTBL** associada com informações sobre a pasta.</span><span class="sxs-lookup"><span data-stu-id="b4509-119">During this state, Outlook initializes the associated **DNTBL** data structure with information about the folder.</span></span> <span data-ttu-id="b4509-120">O cliente baixa o conteúdo da pasta e atualiza a pasta no repositório local com novos conteúdos, modificações ou exclusões do servidor.</span><span class="sxs-lookup"><span data-stu-id="b4509-120">The client downloads the folder contents, and updates the folder on the local store with new contents, modifications, or deletions from the server.</span></span> <span data-ttu-id="b4509-121">O processo de download adota a sincronização de alteração incremental (ICS) do Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="b4509-121">The download process adopts Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="b4509-122">Confira mais informações sobre ICS em [Critérios de avaliação de ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="b4509-122">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
<span data-ttu-id="b4509-123">Quando esse estado termina, o repositório local retorna ao estado sincronizar conteúdo.</span><span class="sxs-lookup"><span data-stu-id="b4509-123">When this state ends, the local store returns to the synchronize contents state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b4509-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="b4509-124">See also</span></span>



[<span data-ttu-id="b4509-125">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="b4509-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="b4509-126">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="b4509-126">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="b4509-127">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="b4509-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="b4509-128">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="b4509-128">SYNCSTATE</span></span>](syncstate.md)

