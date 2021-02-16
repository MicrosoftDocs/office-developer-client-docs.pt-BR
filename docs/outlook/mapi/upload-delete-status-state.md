---
title: Carregar Estado de Status de Exclusão
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dee566ad-b46d-1015-4b0b-6c3313060142
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: dda9d23a572446a5fa79a9500eb69558b6e0debd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425838"
---
# <a name="upload-delete-status-state"></a><span data-ttu-id="93118-103">Carregar Estado de Status de Exclusão</span><span class="sxs-lookup"><span data-stu-id="93118-103">Upload Delete Status State</span></span>

  
  
<span data-ttu-id="93118-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="93118-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="93118-105">Este tópico descreve o que acontece durante o estado de status de exclusão de upload da máquina de estado de replicação.</span><span class="sxs-lookup"><span data-stu-id="93118-105">This topic describes what happens during the upload delete status state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="93118-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="93118-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="93118-107">Identificador de Estado:</span><span class="sxs-lookup"><span data-stu-id="93118-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="93118-108">**LR_SYNC_UPLOAD_MESSAGE_DEL**</span><span class="sxs-lookup"><span data-stu-id="93118-108">**LR_SYNC_UPLOAD_MESSAGE_DEL**</span></span> <br/> |
|<span data-ttu-id="93118-109">Estrutura de dados relacionada:</span><span class="sxs-lookup"><span data-stu-id="93118-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="93118-110">**[UPDEL](updel.md)**</span><span class="sxs-lookup"><span data-stu-id="93118-110">**[UPDEL](updel.md)**</span></span> <br/> |
|<span data-ttu-id="93118-111">Desse estado:</span><span class="sxs-lookup"><span data-stu-id="93118-111">From this state:</span></span>  <br/> |[<span data-ttu-id="93118-112">Estado carregar tabela</span><span class="sxs-lookup"><span data-stu-id="93118-112">Upload table state</span></span>](upload-table-state.md) <br/> |
|<span data-ttu-id="93118-113">Para esse estado:</span><span class="sxs-lookup"><span data-stu-id="93118-113">To this state:</span></span>  <br/> |<span data-ttu-id="93118-114">Estado carregar tabela</span><span class="sxs-lookup"><span data-stu-id="93118-114">Upload table state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="93118-115">A máquina de estado de replicação é uma máquina de estado determinística.</span><span class="sxs-lookup"><span data-stu-id="93118-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="93118-116">Um cliente que sai de um estado para outro eventualmente deve retornar ao primeiro do último.</span><span class="sxs-lookup"><span data-stu-id="93118-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="93118-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="93118-117">Description</span></span>

<span data-ttu-id="93118-118">Esse estado inicia a atualização em um servidor desses itens do Outlook (email, calendário, contato, tarefa, anotação ou diário) que foram excluídos em uma pasta em um armazenamento local especificado em um estado de tabela de carregamento anterior.</span><span class="sxs-lookup"><span data-stu-id="93118-118">This state initiates updating on a server those Outlook items (mail, calendar, contact, task, note, or journal) that have been deleted in a folder on a local store specified in a preceding upload table state.</span></span> <span data-ttu-id="93118-119">Durante esse estado, o Outlook inicializa membros na estrutura de dados **UPDEL** associada com informações para os itens que foram excluídos ou movidos da pasta.</span><span class="sxs-lookup"><span data-stu-id="93118-119">During this state, Outlook initializes members in the associated **UPDEL** data structure with information for the items that have been deleted or moved from the folder.</span></span> 
  
<span data-ttu-id="93118-120">Em seguida, o cliente exclui os itens especificados na pasta no servidor.</span><span class="sxs-lookup"><span data-stu-id="93118-120">The client then deletes the specified items in the folder on the server.</span></span> <span data-ttu-id="93118-121">Para distinguir os itens que foram movidos, em vez de terem sido excluídos, o cliente deve verificar os membros de *therunmov* identificados na estrutura **UPDEL.**</span><span class="sxs-lookup"><span data-stu-id="93118-121">To distinguish items that have been moved as opposed to having been deleted, the client must check the  *pupmov*  members identified in the **UPDEL** structure.</span></span> 
  
<span data-ttu-id="93118-122">Quando esse estado termina, o Outlook limpa as informações internas indicando que o item foi excluído; consequentemente, o Outlook não terá mais um registro do item.</span><span class="sxs-lookup"><span data-stu-id="93118-122">When this state ends, Outlook clears the internal information indicating that the item has been deleted; consequently, Outlook will no longer have a record of the item.</span></span> <span data-ttu-id="93118-123">O armazenamento local retorna ao estado da tabela de carregamento.</span><span class="sxs-lookup"><span data-stu-id="93118-123">The local store returns to the upload table state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="93118-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="93118-124">See also</span></span>



[<span data-ttu-id="93118-125">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="93118-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="93118-126">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="93118-126">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="93118-127">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="93118-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="93118-128">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="93118-128">SYNCSTATE</span></span>](syncstate.md)

