---
title: Carregar o estado das mensagens
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7fdc1494-4f40-38bd-d363-144ca70e5906
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 752756cbcf6c1ce487188dd4b9ba55eee6506cd4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770673"
---
# <a name="upload-message-state"></a><span data-ttu-id="bda40-103">Carregar o estado das mensagens</span><span class="sxs-lookup"><span data-stu-id="bda40-103">Upload Message State</span></span>

  
  
<span data-ttu-id="bda40-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bda40-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="bda40-105">Este tópico descreve o que acontece durante o estado de mensagem de carregamento da máquina de estado de replicação.</span><span class="sxs-lookup"><span data-stu-id="bda40-105">This topic describes what happens during the upload message state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="bda40-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="bda40-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bda40-107">Identificador de controle de sessão:</span><span class="sxs-lookup"><span data-stu-id="bda40-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="bda40-108">**LR_SYNC_UPLOAD_MESSAGE**</span><span class="sxs-lookup"><span data-stu-id="bda40-108">**LR_SYNC_UPLOAD_MESSAGE**</span></span> <br/> |
|<span data-ttu-id="bda40-109">Estrutura de dados relacionados:</span><span class="sxs-lookup"><span data-stu-id="bda40-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="bda40-110">**[UPMSG](upmsg.md)**</span><span class="sxs-lookup"><span data-stu-id="bda40-110">**[UPMSG](upmsg.md)**</span></span> <br/> |
|<span data-ttu-id="bda40-111">Desse estado:</span><span class="sxs-lookup"><span data-stu-id="bda40-111">From this state:</span></span>  <br/> |[<span data-ttu-id="bda40-112">Carregar o estado da tabela</span><span class="sxs-lookup"><span data-stu-id="bda40-112">Upload table state</span></span>](upload-table-state.md) <br/> |
|<span data-ttu-id="bda40-113">Com esse estado:</span><span class="sxs-lookup"><span data-stu-id="bda40-113">To this state:</span></span>  <br/> |<span data-ttu-id="bda40-114">Carregar o estado da tabela</span><span class="sxs-lookup"><span data-stu-id="bda40-114">Upload table state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="bda40-115">A máquina de estado de replicação é uma máquina de estado determinantes.</span><span class="sxs-lookup"><span data-stu-id="bda40-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="bda40-116">Um cliente partindo de um estado para outro eventualmente deve retornar para o anterior do último.</span><span class="sxs-lookup"><span data-stu-id="bda40-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="bda40-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="bda40-117">Description</span></span>

<span data-ttu-id="bda40-118">Nesse estado inicia o carregamento de um item do Outlook (email, calendário, contatos, tarefas, nota ou diário) que há de novo ou foi movida para a pasta atual ou que tenha sido modificado.</span><span class="sxs-lookup"><span data-stu-id="bda40-118">This state initiates uploading an Outlook item (mail, calendar, contact, task, note, or journal) that is new or has been moved to the current folder, or that has been modified.</span></span> <span data-ttu-id="bda40-119">Outlook inicializa a estrutura de dados **UPMSG** correpsonding com as informações apropriadas para o item, como sendo adicionado, movido ou modificado.</span><span class="sxs-lookup"><span data-stu-id="bda40-119">Outlook initializes the correpsonding **UPMSG** data structure with the appropriate information for the item as being added, moved, or modified.</span></span> 
  
<span data-ttu-id="bda40-120">Se o item foi adicionado ou movido, o cliente, em seguida, apropriadamente adiciona ou atualiza o item no servidor.</span><span class="sxs-lookup"><span data-stu-id="bda40-120">If the item has been added or moved, the client then appropriately adds or updates the item on the server.</span></span> 
  
<span data-ttu-id="bda40-121">Se o item tiver sido modificado, Outlook ainda mais especifica na estrutura de dados **UPMSG** se as modificações estão em um cabeçalho de mensagem (caso em que o item é o cabeçalho da mensagem), nas propriedades do item ou no próprio item que requer o conflito resolução.</span><span class="sxs-lookup"><span data-stu-id="bda40-121">If the item has been modified, Outlook further specifies in the **UPMSG** data structure whether the modifications are in a message header (in which case the item is the message header), in the item properties, or in the item itself that requires conflict resolution.</span></span> <span data-ttu-id="bda40-122">O cliente, em seguida, atualiza o item no servidor.</span><span class="sxs-lookup"><span data-stu-id="bda40-122">The client then updates the item on the server.</span></span> 
  
<span data-ttu-id="bda40-123">Quando o carregamento do item for encerrada, Outlook notas que a mensagem foi carregada, para que ele não será processado em um carregamento subsequente.</span><span class="sxs-lookup"><span data-stu-id="bda40-123">When the item upload ends, Outlook notes that the message has been uploaded, so that it will not be processed in a subsequent upload.</span></span> <span data-ttu-id="bda40-124">Armazenamento local retorna para o estado da tabela de carregamento.</span><span class="sxs-lookup"><span data-stu-id="bda40-124">The local store returns to the upload table state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bda40-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="bda40-125">See also</span></span>



[<span data-ttu-id="bda40-126">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="bda40-126">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="bda40-127">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="bda40-127">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="bda40-128">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="bda40-128">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="bda40-129">ESTADO DE SINCRONIZAÇÃO</span><span class="sxs-lookup"><span data-stu-id="bda40-129">SYNCSTATE</span></span>](syncstate.md)

