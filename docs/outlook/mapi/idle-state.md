---
title: Estado ocioso
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 46976bea-c6bb-2e37-2e67-4cbccaa03aec
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: dbe81a2a27f302a38eba6f3c5045df905d8db682
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19766909"
---
# <a name="idle-state"></a><span data-ttu-id="4c66d-103">Estado ocioso</span><span class="sxs-lookup"><span data-stu-id="4c66d-103">Idle State</span></span>

  
  
<span data-ttu-id="4c66d-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4c66d-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="4c66d-105">Este tópico descreve o que acontece durante o estado ocioso da máquina de estado de replicação.</span><span class="sxs-lookup"><span data-stu-id="4c66d-105">This topic describes what happens during the idle state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="4c66d-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="4c66d-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4c66d-107">Identificador de controle de sessão:</span><span class="sxs-lookup"><span data-stu-id="4c66d-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="4c66d-108">**LR_SYNC_IDLE**</span><span class="sxs-lookup"><span data-stu-id="4c66d-108">**LR_SYNC_IDLE**</span></span> <br/> |
|<span data-ttu-id="4c66d-109">Estrutura de dados relacionados:</span><span class="sxs-lookup"><span data-stu-id="4c66d-109">Related Data Structure:</span></span>  <br/> | <span data-ttu-id="4c66d-110">*None*</span><span class="sxs-lookup"><span data-stu-id="4c66d-110">*None*</span></span>  <br/> |
|<span data-ttu-id="4c66d-111">Desse estado:</span><span class="sxs-lookup"><span data-stu-id="4c66d-111">From this state:</span></span>  <br/> | <span data-ttu-id="4c66d-112">*Não aplicável*</span><span class="sxs-lookup"><span data-stu-id="4c66d-112">*Not applicable*</span></span>  <br/> |
|<span data-ttu-id="4c66d-113">Com esse estado:</span><span class="sxs-lookup"><span data-stu-id="4c66d-113">To this state:</span></span>  <br/> |[<span data-ttu-id="4c66d-114">Sincronizar o estado</span><span class="sxs-lookup"><span data-stu-id="4c66d-114">Synchronize state</span></span>](synchronize-state.md) <br/> |
   
> [!NOTE]
> <span data-ttu-id="4c66d-115">A máquina de estado de replicação é uma máquina de estado determinantes.</span><span class="sxs-lookup"><span data-stu-id="4c66d-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="4c66d-116">Um cliente partindo de um estado para outro eventualmente deve retornar para o anterior do último.</span><span class="sxs-lookup"><span data-stu-id="4c66d-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="4c66d-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="4c66d-117">Description</span></span>

<span data-ttu-id="4c66d-118">Nada acontece nesse estado.</span><span class="sxs-lookup"><span data-stu-id="4c66d-118">Nothing happens in this state.</span></span> <span data-ttu-id="4c66d-119">Um repositório local está nesse estado antes de replicação é iniciada e após a conclusão da replicação.</span><span class="sxs-lookup"><span data-stu-id="4c66d-119">A local store is in this state before replication is initiated and after replication is complete.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4c66d-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c66d-120">See also</span></span>



[<span data-ttu-id="4c66d-121">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="4c66d-121">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="4c66d-122">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="4c66d-122">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="4c66d-123">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="4c66d-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="4c66d-124">ESTADO DE SINCRONIZAÇÃO</span><span class="sxs-lookup"><span data-stu-id="4c66d-124">SYNCSTATE</span></span>](syncstate.md)

