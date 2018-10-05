---
title: Baixar estado da hierarquia
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8e0400ba-8530-e6ac-5de8-a62aeec5e10a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 45535eef75c6fc091c02ec35b669675a51e4cf48
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384854"
---
# <a name="download-hierarchy-state"></a><span data-ttu-id="1d34a-103">Baixar estado da hierarquia</span><span class="sxs-lookup"><span data-stu-id="1d34a-103">Download Hierarchy State</span></span>

  
  
<span data-ttu-id="1d34a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1d34a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="1d34a-105">Este tópico descreve o que acontece durante o estado de hierarquia de download da máquina de estado de replicação.</span><span class="sxs-lookup"><span data-stu-id="1d34a-105">This topic describes what happens during the download hierarchy state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="1d34a-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="1d34a-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1d34a-107">Identificador de controle de sessão:</span><span class="sxs-lookup"><span data-stu-id="1d34a-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="1d34a-108">**LR_SYNC_DOWNLOAD_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="1d34a-108">**LR_SYNC_DOWNLOAD_HIERARCHY**</span></span> <br/> |
|<span data-ttu-id="1d34a-109">Estrutura de dados relacionados:</span><span class="sxs-lookup"><span data-stu-id="1d34a-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="1d34a-110">**[DNHIER](dnhier.md)**</span><span class="sxs-lookup"><span data-stu-id="1d34a-110">**[DNHIER](dnhier.md)**</span></span> <br/> |
|<span data-ttu-id="1d34a-111">Desse estado:</span><span class="sxs-lookup"><span data-stu-id="1d34a-111">From this state:</span></span>  <br/> |[<span data-ttu-id="1d34a-112">Sincronizar o estado</span><span class="sxs-lookup"><span data-stu-id="1d34a-112">Synchronize state</span></span>](synchronize-state.md) <br/> |
|<span data-ttu-id="1d34a-113">Com esse estado:</span><span class="sxs-lookup"><span data-stu-id="1d34a-113">To this state:</span></span>  <br/> |<span data-ttu-id="1d34a-114">Sincronizar o estado</span><span class="sxs-lookup"><span data-stu-id="1d34a-114">Synchronize state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="1d34a-115">A máquina de estado de replicação é uma máquina de estado determinantes.</span><span class="sxs-lookup"><span data-stu-id="1d34a-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="1d34a-116">Um cliente partindo de um estado para outro eventualmente deve retornar para o anterior do último.</span><span class="sxs-lookup"><span data-stu-id="1d34a-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="1d34a-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="1d34a-117">Description</span></span>

<span data-ttu-id="1d34a-118">Nesse estado inicia o download de uma hierarquia de árvore de pastas de um servidor no repositório local.</span><span class="sxs-lookup"><span data-stu-id="1d34a-118">This state initiates downloading a tree hierarchy of folders from a server to the local store.</span></span> 
  
<span data-ttu-id="1d34a-119">Outlook inicializa a estrutura de dados **DNHIER** associada com um ponteiro para a hierarquia.</span><span class="sxs-lookup"><span data-stu-id="1d34a-119">Outlook initializes the associated **DNHIER** data structure with a pointer to the hierarchy.</span></span> <span data-ttu-id="1d34a-120">O cliente downloads da hierarquia e insere novas pastas ou modificações em pastas no armazenamento local.</span><span class="sxs-lookup"><span data-stu-id="1d34a-120">The client downloads the hierarchy, and inserts new folders or modifications to folders in the local store.</span></span> <span data-ttu-id="1d34a-121">O processo de download adota sincronização de alteração Incremental do Microsoft Exchange (ICS).</span><span class="sxs-lookup"><span data-stu-id="1d34a-121">The download process adopts Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="1d34a-122">Para obter mais informações sobre ICS, consulte [ICS critérios de avaliação](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="1d34a-122">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
<span data-ttu-id="1d34a-123">Quando for encerrada nesse estado, o armazenamento local retorna para o estado de sincronização.</span><span class="sxs-lookup"><span data-stu-id="1d34a-123">When this state ends, the local store returns to the synchronize state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1d34a-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="1d34a-124">See also</span></span>



[<span data-ttu-id="1d34a-125">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="1d34a-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="1d34a-126">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="1d34a-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="1d34a-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="1d34a-127">SYNCSTATE</span></span>](syncstate.md)

