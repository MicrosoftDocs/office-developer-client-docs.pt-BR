---
title: Carregar estado da mensagem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7fdc1494-4f40-38bd-d363-144ca70e5906
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 61cda23557a501a2651385d192f1dc7432ef1cb5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433798"
---
# <a name="upload-message-state"></a><span data-ttu-id="a954b-103">Carregar estado da mensagem</span><span class="sxs-lookup"><span data-stu-id="a954b-103">Upload Message State</span></span>

  
  
<span data-ttu-id="a954b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a954b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="a954b-105">Este tópico descreve o que acontece durante o estado de mensagem de carregamento da máquina de estado de replicação.</span><span class="sxs-lookup"><span data-stu-id="a954b-105">This topic describes what happens during the upload message state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="a954b-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="a954b-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a954b-107">Identificador de Estado:</span><span class="sxs-lookup"><span data-stu-id="a954b-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="a954b-108">**LR_SYNC_UPLOAD_MESSAGE**</span><span class="sxs-lookup"><span data-stu-id="a954b-108">**LR_SYNC_UPLOAD_MESSAGE**</span></span> <br/> |
|<span data-ttu-id="a954b-109">Estrutura de dados relacionada:</span><span class="sxs-lookup"><span data-stu-id="a954b-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="a954b-110">**[UPMSG](upmsg.md)**</span><span class="sxs-lookup"><span data-stu-id="a954b-110">**[UPMSG](upmsg.md)**</span></span> <br/> |
|<span data-ttu-id="a954b-111">A partir deste Estado:</span><span class="sxs-lookup"><span data-stu-id="a954b-111">From this state:</span></span>  <br/> |[<span data-ttu-id="a954b-112">Carregar estado da tabela</span><span class="sxs-lookup"><span data-stu-id="a954b-112">Upload table state</span></span>](upload-table-state.md) <br/> |
|<span data-ttu-id="a954b-113">Para este Estado:</span><span class="sxs-lookup"><span data-stu-id="a954b-113">To this state:</span></span>  <br/> |<span data-ttu-id="a954b-114">Carregar estado da tabela</span><span class="sxs-lookup"><span data-stu-id="a954b-114">Upload table state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="a954b-115">A máquina de estado de replicação é uma máquina de estado determinista.</span><span class="sxs-lookup"><span data-stu-id="a954b-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="a954b-116">Um cliente que faz parte de um estado para outro deve eventualmente retornar para o primeiro a partir do último.</span><span class="sxs-lookup"><span data-stu-id="a954b-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="a954b-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="a954b-117">Description</span></span>

<span data-ttu-id="a954b-118">Este estado inicia o carregamento de um item do Outlook (email, calendário, contato, tarefa, anotação ou diário) que é novo ou que foi movido para a pasta atual ou que foi modificado.</span><span class="sxs-lookup"><span data-stu-id="a954b-118">This state initiates uploading an Outlook item (mail, calendar, contact, task, note, or journal) that is new or has been moved to the current folder, or that has been modified.</span></span> <span data-ttu-id="a954b-119">O Outlook Inicializa a estrutura de dados do correpsonding **UPMSG** com as informações apropriadas para o item como sendo adicionado, movido ou modificado.</span><span class="sxs-lookup"><span data-stu-id="a954b-119">Outlook initializes the correpsonding **UPMSG** data structure with the appropriate information for the item as being added, moved, or modified.</span></span> 
  
<span data-ttu-id="a954b-120">Se o item tiver sido adicionado ou movido, o cliente adicionará ou atualizará o item, apropriadamente, no servidor.</span><span class="sxs-lookup"><span data-stu-id="a954b-120">If the item has been added or moved, the client then appropriately adds or updates the item on the server.</span></span> 
  
<span data-ttu-id="a954b-121">Se o item tiver sido modificado, o Outlook especificará ainda mais na estrutura de dados do **UPMSG** se as modificações estiverem em um cabeçalho de mensagem (caso em que o item é o cabeçalho da mensagem), nas propriedades do item ou no próprio item que requer conflito solução.</span><span class="sxs-lookup"><span data-stu-id="a954b-121">If the item has been modified, Outlook further specifies in the **UPMSG** data structure whether the modifications are in a message header (in which case the item is the message header), in the item properties, or in the item itself that requires conflict resolution.</span></span> <span data-ttu-id="a954b-122">O cliente atualiza o item no servidor.</span><span class="sxs-lookup"><span data-stu-id="a954b-122">The client then updates the item on the server.</span></span> 
  
<span data-ttu-id="a954b-123">Quando o carregamento do item termina, o Outlook observa que a mensagem foi carregada, de forma que ela não seja processada em um carregamento subsequente.</span><span class="sxs-lookup"><span data-stu-id="a954b-123">When the item upload ends, Outlook notes that the message has been uploaded, so that it will not be processed in a subsequent upload.</span></span> <span data-ttu-id="a954b-124">O repositório local retorna ao estado de carregamento da tabela.</span><span class="sxs-lookup"><span data-stu-id="a954b-124">The local store returns to the upload table state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a954b-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="a954b-125">See also</span></span>



[<span data-ttu-id="a954b-126">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="a954b-126">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="a954b-127">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="a954b-127">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="a954b-128">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="a954b-128">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="a954b-129">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="a954b-129">SYNCSTATE</span></span>](syncstate.md)

