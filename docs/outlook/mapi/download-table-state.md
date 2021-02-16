---
title: Estado baixar tabela
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
# <a name="download-table-state"></a><span data-ttu-id="9994c-103">Estado baixar tabela</span><span class="sxs-lookup"><span data-stu-id="9994c-103">Download Table State</span></span>

  
  
<span data-ttu-id="9994c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9994c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="9994c-105">Este tópico descreve o que acontece durante o estado da tabela de download da máquina de estado de replicação.</span><span class="sxs-lookup"><span data-stu-id="9994c-105">This topic describes what happens during the download table state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="9994c-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="9994c-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9994c-107">Identificador de Estado:</span><span class="sxs-lookup"><span data-stu-id="9994c-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="9994c-108">**LR_SYNC_DOWNLOAD_TABLE**</span><span class="sxs-lookup"><span data-stu-id="9994c-108">**LR_SYNC_DOWNLOAD_TABLE**</span></span> <br/> |
|<span data-ttu-id="9994c-109">Estrutura de dados relacionada:</span><span class="sxs-lookup"><span data-stu-id="9994c-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="9994c-110">**[DNTBL](dntbl.md)**</span><span class="sxs-lookup"><span data-stu-id="9994c-110">**[DNTBL](dntbl.md)**</span></span> <br/> |
|<span data-ttu-id="9994c-111">Desse estado:</span><span class="sxs-lookup"><span data-stu-id="9994c-111">From this state:</span></span>  <br/> |[<span data-ttu-id="9994c-112">Sincronizar o estado do conteúdo</span><span class="sxs-lookup"><span data-stu-id="9994c-112">Synchronize contents state</span></span>](synchronize-contents-state.md) <br/> |
|<span data-ttu-id="9994c-113">Para esse estado:</span><span class="sxs-lookup"><span data-stu-id="9994c-113">To this state:</span></span>  <br/> |<span data-ttu-id="9994c-114">Sincronizar o estado do conteúdo</span><span class="sxs-lookup"><span data-stu-id="9994c-114">Synchronize contents state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="9994c-115">A máquina de estado de replicação é uma máquina de estado determinística.</span><span class="sxs-lookup"><span data-stu-id="9994c-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="9994c-116">Um cliente que sai de um estado para outro eventualmente deve retornar ao primeiro do último.</span><span class="sxs-lookup"><span data-stu-id="9994c-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="9994c-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="9994c-117">Description</span></span>

<span data-ttu-id="9994c-118">Esse estado inicia o download de uma pasta.</span><span class="sxs-lookup"><span data-stu-id="9994c-118">This state initiates downloading a folder.</span></span> <span data-ttu-id="9994c-119">Durante esse estado, o Outlook inicializa a estrutura de dados **DNTBL** associada com informações sobre a pasta.</span><span class="sxs-lookup"><span data-stu-id="9994c-119">During this state, Outlook initializes the associated **DNTBL** data structure with information about the folder.</span></span> <span data-ttu-id="9994c-120">O cliente baixa o conteúdo da pasta e atualiza a pasta no armazenamento local com novos conteúdos, modificações ou exclusões do servidor.</span><span class="sxs-lookup"><span data-stu-id="9994c-120">The client downloads the folder contents, and updates the folder on the local store with new contents, modifications, or deletions from the server.</span></span> <span data-ttu-id="9994c-121">O processo de download adota o Microsoft Exchange Incremental Change Synchronization (ICS).</span><span class="sxs-lookup"><span data-stu-id="9994c-121">The download process adopts Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="9994c-122">Confira mais informações sobre ICS em [Critérios de avaliação de ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="9994c-122">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
<span data-ttu-id="9994c-123">Quando esse estado termina, o armazenamento local retorna ao estado de sincronização do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="9994c-123">When this state ends, the local store returns to the synchronize contents state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9994c-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="9994c-124">See also</span></span>



[<span data-ttu-id="9994c-125">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="9994c-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="9994c-126">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="9994c-126">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="9994c-127">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="9994c-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="9994c-128">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="9994c-128">SYNCSTATE</span></span>](syncstate.md)

