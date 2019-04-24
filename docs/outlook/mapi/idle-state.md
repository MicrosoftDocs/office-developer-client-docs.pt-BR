---
title: Estado ocioso
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 46976bea-c6bb-2e37-2e67-4cbccaa03aec
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3db4ead7e2485bbbae82f2a07659c934b394d6d5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351181"
---
# <a name="idle-state"></a><span data-ttu-id="9fbd6-103">Estado ocioso</span><span class="sxs-lookup"><span data-stu-id="9fbd6-103">Idle State</span></span>

  
  
<span data-ttu-id="9fbd6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9fbd6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="9fbd6-105">Este tópico descreve o que acontece durante o estado ocioso da máquina de estado de replicação.</span><span class="sxs-lookup"><span data-stu-id="9fbd6-105">This topic describes what happens during the idle state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="9fbd6-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="9fbd6-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9fbd6-107">Identificador de Estado:</span><span class="sxs-lookup"><span data-stu-id="9fbd6-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="9fbd6-108">**LR_SYNC_IDLE**</span><span class="sxs-lookup"><span data-stu-id="9fbd6-108">**LR_SYNC_IDLE**</span></span> <br/> |
|<span data-ttu-id="9fbd6-109">Estrutura de dados relacionada:</span><span class="sxs-lookup"><span data-stu-id="9fbd6-109">Related Data Structure:</span></span>  <br/> | <span data-ttu-id="9fbd6-110">*None*</span><span class="sxs-lookup"><span data-stu-id="9fbd6-110">*None*</span></span>  <br/> |
|<span data-ttu-id="9fbd6-111">A partir deste Estado:</span><span class="sxs-lookup"><span data-stu-id="9fbd6-111">From this state:</span></span>  <br/> | <span data-ttu-id="9fbd6-112">*Não aplicável*</span><span class="sxs-lookup"><span data-stu-id="9fbd6-112">*Not applicable*</span></span>  <br/> |
|<span data-ttu-id="9fbd6-113">Para este Estado:</span><span class="sxs-lookup"><span data-stu-id="9fbd6-113">To this state:</span></span>  <br/> |[<span data-ttu-id="9fbd6-114">Estado Sincronizar</span><span class="sxs-lookup"><span data-stu-id="9fbd6-114">Synchronize state</span></span>](synchronize-state.md) <br/> |
   
> [!NOTE]
> <span data-ttu-id="9fbd6-115">A máquina de estado de replicação é uma máquina de estado determinista.</span><span class="sxs-lookup"><span data-stu-id="9fbd6-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="9fbd6-116">Um cliente que faz parte de um estado para outro deve eventualmente retornar para o primeiro a partir do último.</span><span class="sxs-lookup"><span data-stu-id="9fbd6-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="9fbd6-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="9fbd6-117">Description</span></span>

<span data-ttu-id="9fbd6-118">Nada acontece nesse estado.</span><span class="sxs-lookup"><span data-stu-id="9fbd6-118">Nothing happens in this state.</span></span> <span data-ttu-id="9fbd6-119">Um repositório local está nesse estado antes que A replicação seja iniciada e após a conclusão da replicação.</span><span class="sxs-lookup"><span data-stu-id="9fbd6-119">A local store is in this state before replication is initiated and after replication is complete.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9fbd6-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="9fbd6-120">See also</span></span>



[<span data-ttu-id="9fbd6-121">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="9fbd6-121">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="9fbd6-122">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="9fbd6-122">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="9fbd6-123">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="9fbd6-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="9fbd6-124">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="9fbd6-124">SYNCSTATE</span></span>](syncstate.md)

