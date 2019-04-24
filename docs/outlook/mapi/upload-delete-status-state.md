---
title: Carregar estado de status de exclusão
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dee566ad-b46d-1015-4b0b-6c3313060142
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: dda9d23a572446a5fa79a9500eb69558b6e0debd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357705"
---
# <a name="upload-delete-status-state"></a><span data-ttu-id="0972b-103">Carregar estado de status de exclusão</span><span class="sxs-lookup"><span data-stu-id="0972b-103">Upload Delete Status State</span></span>

  
  
<span data-ttu-id="0972b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0972b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="0972b-105">Este tópico descreve o que acontece durante o estado de upload de status de exclusão da máquina de estado de replicação.</span><span class="sxs-lookup"><span data-stu-id="0972b-105">This topic describes what happens during the upload delete status state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="0972b-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="0972b-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0972b-107">Identificador de Estado:</span><span class="sxs-lookup"><span data-stu-id="0972b-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="0972b-108">**LR_SYNC_UPLOAD_MESSAGE_DEL**</span><span class="sxs-lookup"><span data-stu-id="0972b-108">**LR_SYNC_UPLOAD_MESSAGE_DEL**</span></span> <br/> |
|<span data-ttu-id="0972b-109">Estrutura de dados relacionada:</span><span class="sxs-lookup"><span data-stu-id="0972b-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="0972b-110">**[UPDEL](updel.md)**</span><span class="sxs-lookup"><span data-stu-id="0972b-110">**[UPDEL](updel.md)**</span></span> <br/> |
|<span data-ttu-id="0972b-111">A partir deste Estado:</span><span class="sxs-lookup"><span data-stu-id="0972b-111">From this state:</span></span>  <br/> |[<span data-ttu-id="0972b-112">Carregar estado da tabela</span><span class="sxs-lookup"><span data-stu-id="0972b-112">Upload table state</span></span>](upload-table-state.md) <br/> |
|<span data-ttu-id="0972b-113">Para este Estado:</span><span class="sxs-lookup"><span data-stu-id="0972b-113">To this state:</span></span>  <br/> |<span data-ttu-id="0972b-114">Carregar estado da tabela</span><span class="sxs-lookup"><span data-stu-id="0972b-114">Upload table state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="0972b-115">A máquina de estado de replicação é uma máquina de estado determinista.</span><span class="sxs-lookup"><span data-stu-id="0972b-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="0972b-116">Um cliente que faz parte de um estado para outro deve eventualmente retornar para o primeiro a partir do último.</span><span class="sxs-lookup"><span data-stu-id="0972b-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="0972b-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="0972b-117">Description</span></span>

<span data-ttu-id="0972b-118">Este estado inicia a atualização em um servidor de itens do Outlook (email, calendário, contato, tarefa, anotação ou diário) que tenha sido excluído em uma pasta em um repositório local especificado em um estado de tabela de carregamento anterior.</span><span class="sxs-lookup"><span data-stu-id="0972b-118">This state initiates updating on a server those Outlook items (mail, calendar, contact, task, note, or journal) that have been deleted in a folder on a local store specified in a preceding upload table state.</span></span> <span data-ttu-id="0972b-119">Durante esse Estado, o Outlook Inicializa membros na estrutura de dados do **UPDEL** associada com informações sobre os itens que foram excluídos ou movidos da pasta.</span><span class="sxs-lookup"><span data-stu-id="0972b-119">During this state, Outlook initializes members in the associated **UPDEL** data structure with information for the items that have been deleted or moved from the folder.</span></span> 
  
<span data-ttu-id="0972b-120">O cliente, em seguida, exclui os itens especificados na pasta no servidor.</span><span class="sxs-lookup"><span data-stu-id="0972b-120">The client then deletes the specified items in the folder on the server.</span></span> <span data-ttu-id="0972b-121">Para diferenciar itens que foram movidos em vez de terem sido excluídos, o cliente deve verificar os membros *pupmov* identificados na estrutura **UPDEL** .</span><span class="sxs-lookup"><span data-stu-id="0972b-121">To distinguish items that have been moved as opposed to having been deleted, the client must check the  *pupmov*  members identified in the **UPDEL** structure.</span></span> 
  
<span data-ttu-id="0972b-122">Quando esse estado termina, o Outlook limpa as informações internas indicando que o item foi excluído; Consequentemente, o Outlook não terá mais um registro do item.</span><span class="sxs-lookup"><span data-stu-id="0972b-122">When this state ends, Outlook clears the internal information indicating that the item has been deleted; consequently, Outlook will no longer have a record of the item.</span></span> <span data-ttu-id="0972b-123">O repositório local retorna ao estado de carregamento da tabela.</span><span class="sxs-lookup"><span data-stu-id="0972b-123">The local store returns to the upload table state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0972b-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="0972b-124">See also</span></span>



[<span data-ttu-id="0972b-125">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="0972b-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="0972b-126">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="0972b-126">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="0972b-127">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="0972b-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="0972b-128">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="0972b-128">SYNCSTATE</span></span>](syncstate.md)

