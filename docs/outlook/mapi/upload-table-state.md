---
title: Carregar estado da tabela
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: fe167c90-c817-b627-0728-5c6393477c22
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a2a9b3f214c76b8ec965c84c4731e0dc57e83352
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405818"
---
# <a name="upload-table-state"></a><span data-ttu-id="ef637-103">Carregar estado da tabela</span><span class="sxs-lookup"><span data-stu-id="ef637-103">Upload Table State</span></span>

  
  
<span data-ttu-id="ef637-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ef637-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="ef637-105">Este tópico descreve o que acontece durante o estado de carregamento da tabela da máquina de estado de replicação.</span><span class="sxs-lookup"><span data-stu-id="ef637-105">This topic describes what happens during the upload table state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="ef637-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="ef637-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ef637-107">Identificador de Estado:</span><span class="sxs-lookup"><span data-stu-id="ef637-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="ef637-108">**LR_SYNC_UPLOAD_TABLE**</span><span class="sxs-lookup"><span data-stu-id="ef637-108">**LR_SYNC_UPLOAD_TABLE**</span></span> <br/> |
|<span data-ttu-id="ef637-109">Estrutura de dados relacionada:</span><span class="sxs-lookup"><span data-stu-id="ef637-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="ef637-110">**[UPTBL](uptbl.md)**</span><span class="sxs-lookup"><span data-stu-id="ef637-110">**[UPTBL](uptbl.md)**</span></span> <br/> |
|<span data-ttu-id="ef637-111">A partir deste Estado:</span><span class="sxs-lookup"><span data-stu-id="ef637-111">From this state:</span></span>  <br/> |[<span data-ttu-id="ef637-112">Sincronizar o estado do conteúdo</span><span class="sxs-lookup"><span data-stu-id="ef637-112">Synchronize contents state</span></span>](synchronize-contents-state.md) <br/> |
|<span data-ttu-id="ef637-113">Para este Estado:</span><span class="sxs-lookup"><span data-stu-id="ef637-113">To this state:</span></span>  <br/> |<span data-ttu-id="ef637-114">[Carregar estado da mensagem](upload-message-state.md), [carregar estado de status de exclusão](upload-delete-status-state.md), carregar o estado de status de [leitura](upload-read-status-state.md)ou sincronizar o estado do conteúdo</span><span class="sxs-lookup"><span data-stu-id="ef637-114">[Upload message state](upload-message-state.md), [upload delete status state](upload-delete-status-state.md), [upload read status state](upload-read-status-state.md), or synchronize contents state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="ef637-115">A máquina de estado de replicação é uma máquina de estado determinista.</span><span class="sxs-lookup"><span data-stu-id="ef637-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="ef637-116">Um cliente que faz parte de um estado para outro deve eventualmente retornar para o primeiro a partir do último.</span><span class="sxs-lookup"><span data-stu-id="ef637-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="ef637-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="ef637-117">Description</span></span>

<span data-ttu-id="ef637-118">Este estado inicia o carregamento do conteúdo de uma pasta que foi especificada em um estado de sincronização anterior do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="ef637-118">This state initiates uploading the contents of a folder that has been specified in a preceding synchronize contents state.</span></span> <span data-ttu-id="ef637-119">A pasta pode ser uma pasta de email, calendário, contatos, tarefas, anotações ou diário.</span><span class="sxs-lookup"><span data-stu-id="ef637-119">The folder can be a mail, calendar, contacts, tasks, notes, or journal folder.</span></span> <span data-ttu-id="ef637-120">Durante esse Estado, o Outlook cria uma lista de itens que foram adicionados, modificados, movidos, excluídos ou marcados como lidos e prepara as informações internas apropriadas para o estado de mensagem de carregamento correspondente, carregar o estado de status de exclusão ou carregar o status de leitura Estado.</span><span class="sxs-lookup"><span data-stu-id="ef637-120">During this state, Outlook creates a list of items that have been added, modified, moved, deleted, or marked as read, and prepares the appropriate internal information for the corresponding upload message state, upload delete status state, or upload read status state.</span></span>
  
<span data-ttu-id="ef637-121">Quando esse estado termina, o Outlook marca a pasta como tendo seu conteúdo sincronizado, para que o conteúdo não seja carregado novamente até que outra modificação seja feita.</span><span class="sxs-lookup"><span data-stu-id="ef637-121">When this state ends, Outlook marks the folder as having its contents synchronized, so that the contents will not be uploaded again until another modification is made.</span></span> <span data-ttu-id="ef637-122">O repositório local retorna ao estado sincronizar conteúdo.</span><span class="sxs-lookup"><span data-stu-id="ef637-122">The local store returns to the synchronize contents state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ef637-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="ef637-123">See also</span></span>



[<span data-ttu-id="ef637-124">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="ef637-124">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="ef637-125">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="ef637-125">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="ef637-126">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="ef637-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="ef637-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="ef637-127">SYNCSTATE</span></span>](syncstate.md)

