---
title: Carregar estado do status de exclusão
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dee566ad-b46d-1015-4b0b-6c3313060142
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 4a45cfafec5126c72f365858e41963bc95fa707a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574542"
---
# <a name="upload-delete-status-state"></a><span data-ttu-id="d422a-103">Carregar estado do status de exclusão</span><span class="sxs-lookup"><span data-stu-id="d422a-103">Upload Delete Status State</span></span>

  
  
<span data-ttu-id="d422a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d422a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="d422a-105">Este tópico descreve o que acontece durante o estado do carregamento excluir status da máquina de estado de replicação.</span><span class="sxs-lookup"><span data-stu-id="d422a-105">This topic describes what happens during the upload delete status state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="d422a-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="d422a-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d422a-107">Identificador de controle de sessão:</span><span class="sxs-lookup"><span data-stu-id="d422a-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="d422a-108">**LR_SYNC_UPLOAD_MESSAGE_DEL**</span><span class="sxs-lookup"><span data-stu-id="d422a-108">**LR_SYNC_UPLOAD_MESSAGE_DEL**</span></span> <br/> |
|<span data-ttu-id="d422a-109">Estrutura de dados relacionados:</span><span class="sxs-lookup"><span data-stu-id="d422a-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="d422a-110">**[UPDEL](updel.md)**</span><span class="sxs-lookup"><span data-stu-id="d422a-110">**[UPDEL](updel.md)**</span></span> <br/> |
|<span data-ttu-id="d422a-111">Desse estado:</span><span class="sxs-lookup"><span data-stu-id="d422a-111">From this state:</span></span>  <br/> |[<span data-ttu-id="d422a-112">Carregar o estado da tabela</span><span class="sxs-lookup"><span data-stu-id="d422a-112">Upload table state</span></span>](upload-table-state.md) <br/> |
|<span data-ttu-id="d422a-113">Com esse estado:</span><span class="sxs-lookup"><span data-stu-id="d422a-113">To this state:</span></span>  <br/> |<span data-ttu-id="d422a-114">Carregar o estado da tabela</span><span class="sxs-lookup"><span data-stu-id="d422a-114">Upload table state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="d422a-115">A máquina de estado de replicação é uma máquina de estado determinantes.</span><span class="sxs-lookup"><span data-stu-id="d422a-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="d422a-116">Um cliente partindo de um estado para outro eventualmente deve retornar para o anterior do último.</span><span class="sxs-lookup"><span data-stu-id="d422a-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="d422a-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="d422a-117">Description</span></span>

<span data-ttu-id="d422a-118">Nesse estado inicia os itens do Outlook (email, calendário, contatos, tarefas, nota ou diário) que foram excluídos em uma pasta em um repositório local especificado em um estado de tabela anterior para carregar a atualização em um servidor.</span><span class="sxs-lookup"><span data-stu-id="d422a-118">This state initiates updating on a server those Outlook items (mail, calendar, contact, task, note, or journal) that have been deleted in a folder on a local store specified in a preceding upload table state.</span></span> <span data-ttu-id="d422a-119">Durante esse estado, o Outlook inicializa membros na estrutura de dados **UPDEL** associada com informações para os itens que tenham sido excluído ou movido da pasta.</span><span class="sxs-lookup"><span data-stu-id="d422a-119">During this state, Outlook initializes members in the associated **UPDEL** data structure with information for the items that have been deleted or moved from the folder.</span></span> 
  
<span data-ttu-id="d422a-120">Em seguida, o cliente exclui os itens especificados na pasta no servidor.</span><span class="sxs-lookup"><span data-stu-id="d422a-120">The client then deletes the specified items in the folder on the server.</span></span> <span data-ttu-id="d422a-121">Para distinguir os itens que foram movidos em vez de ter sido excluído, o cliente deve verificar os membros de *pupmov* identificados na estrutura **UPDEL** .</span><span class="sxs-lookup"><span data-stu-id="d422a-121">To distinguish items that have been moved as opposed to having been deleted, the client must check the  *pupmov*  members identified in the **UPDEL** structure.</span></span> 
  
<span data-ttu-id="d422a-122">Quando for encerrada nesse estado, o Outlook limpa as informações internas, indicando que o item foi excluído; Consequentemente, o Outlook não terá mais um registro do item.</span><span class="sxs-lookup"><span data-stu-id="d422a-122">When this state ends, Outlook clears the internal information indicating that the item has been deleted; consequently, Outlook will no longer have a record of the item.</span></span> <span data-ttu-id="d422a-123">Armazenamento local retorna para o estado da tabela de carregamento.</span><span class="sxs-lookup"><span data-stu-id="d422a-123">The local store returns to the upload table state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d422a-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="d422a-124">See also</span></span>



[<span data-ttu-id="d422a-125">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="d422a-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="d422a-126">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="d422a-126">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="d422a-127">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="d422a-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="d422a-128">ESTADO DE SINCRONIZAÇÃO</span><span class="sxs-lookup"><span data-stu-id="d422a-128">SYNCSTATE</span></span>](syncstate.md)

