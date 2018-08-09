---
title: Baixar o estado da tabela
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5bcc8b0a-0ab7-6c3e-8334-9e83cf2882a7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6a29cc131b4fe352b067e343376b2b705e8e3244
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766465"
---
# <a name="download-table-state"></a><span data-ttu-id="d1cdf-103">Baixar o estado da tabela</span><span class="sxs-lookup"><span data-stu-id="d1cdf-103">Download Table State</span></span>

  
  
<span data-ttu-id="d1cdf-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d1cdf-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="d1cdf-105">Este tópico descreve o que acontece durante o estado da tabela de download da máquina de estado de replicação.</span><span class="sxs-lookup"><span data-stu-id="d1cdf-105">This topic describes what happens during the download table state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="d1cdf-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="d1cdf-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d1cdf-107">Identificador de controle de sessão:</span><span class="sxs-lookup"><span data-stu-id="d1cdf-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="d1cdf-108">**LR_SYNC_DOWNLOAD_TABLE**</span><span class="sxs-lookup"><span data-stu-id="d1cdf-108">**LR_SYNC_DOWNLOAD_TABLE**</span></span> <br/> |
|<span data-ttu-id="d1cdf-109">Estrutura de dados relacionados:</span><span class="sxs-lookup"><span data-stu-id="d1cdf-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="d1cdf-110">**[DNTBL](dntbl.md)**</span><span class="sxs-lookup"><span data-stu-id="d1cdf-110">**[DNTBL](dntbl.md)**</span></span> <br/> |
|<span data-ttu-id="d1cdf-111">Desse estado:</span><span class="sxs-lookup"><span data-stu-id="d1cdf-111">From this state:</span></span>  <br/> |[<span data-ttu-id="d1cdf-112">Sincronizar o estado de conteúdo</span><span class="sxs-lookup"><span data-stu-id="d1cdf-112">Synchronize contents state</span></span>](synchronize-contents-state.md) <br/> |
|<span data-ttu-id="d1cdf-113">Com esse estado:</span><span class="sxs-lookup"><span data-stu-id="d1cdf-113">To this state:</span></span>  <br/> |<span data-ttu-id="d1cdf-114">Sincronizar o estado de conteúdo</span><span class="sxs-lookup"><span data-stu-id="d1cdf-114">Synchronize contents state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="d1cdf-115">A máquina de estado de replicação é uma máquina de estado determinantes.</span><span class="sxs-lookup"><span data-stu-id="d1cdf-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="d1cdf-116">Um cliente partindo de um estado para outro eventualmente deve retornar para o anterior do último.</span><span class="sxs-lookup"><span data-stu-id="d1cdf-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="d1cdf-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="d1cdf-117">Description</span></span>

<span data-ttu-id="d1cdf-118">Nesse estado inicia baixando uma pasta.</span><span class="sxs-lookup"><span data-stu-id="d1cdf-118">This state initiates downloading a folder.</span></span> <span data-ttu-id="d1cdf-119">Durante esse estado, o Outlook inicializa a estrutura de dados **DNTBL** associada com informações sobre a pasta.</span><span class="sxs-lookup"><span data-stu-id="d1cdf-119">During this state, Outlook initializes the associated **DNTBL** data structure with information about the folder.</span></span> <span data-ttu-id="d1cdf-120">O cliente baixa o conteúdo da pasta e atualiza a pasta no armazenamento local com conteúdo novo, modificações ou exclusões do servidor.</span><span class="sxs-lookup"><span data-stu-id="d1cdf-120">The client downloads the folder contents, and updates the folder on the local store with new contents, modifications, or deletions from the server.</span></span> <span data-ttu-id="d1cdf-121">O processo de download adota sincronização de alteração Incremental do Microsoft Exchange (ICS).</span><span class="sxs-lookup"><span data-stu-id="d1cdf-121">The download process adopts Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="d1cdf-122">Para obter mais informações sobre ICS, consulte [ICS critérios de avaliação](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="d1cdf-122">For more information on ICS, see [ICS Evaluation Criteria](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
<span data-ttu-id="d1cdf-123">Quando for encerrada nesse estado, o armazenamento local retorna ao estado sincronizar conteúdo.</span><span class="sxs-lookup"><span data-stu-id="d1cdf-123">When this state ends, the local store returns to the synchronize contents state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d1cdf-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="d1cdf-124">See also</span></span>



[<span data-ttu-id="d1cdf-125">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="d1cdf-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="d1cdf-126">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="d1cdf-126">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="d1cdf-127">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="d1cdf-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="d1cdf-128">ESTADO DE SINCRONIZAÇÃO</span><span class="sxs-lookup"><span data-stu-id="d1cdf-128">SYNCSTATE</span></span>](syncstate.md)

