---
title: Carregar o estado do status de leitura
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d45574e-df87-8c44-4aa7-d41b38406f0a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 41815a88fe1215d2a85a38592e04b0d0bbd43cc6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573044"
---
# <a name="upload-read-status-state"></a><span data-ttu-id="5b300-103">Carregar o estado do status de leitura</span><span class="sxs-lookup"><span data-stu-id="5b300-103">Upload Read Status State</span></span>

  
  
<span data-ttu-id="5b300-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5b300-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="5b300-105">Este tópico descreve o que acontece durante o carregamento ler o estado de status da máquina de estado de replicação.</span><span class="sxs-lookup"><span data-stu-id="5b300-105">This topic describes what happens during the upload read status state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="5b300-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="5b300-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5b300-107">Identificador de controle de sessão:</span><span class="sxs-lookup"><span data-stu-id="5b300-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="5b300-108">**LR_SYNC_UPLOAD_MESSAGE_READ**</span><span class="sxs-lookup"><span data-stu-id="5b300-108">**LR_SYNC_UPLOAD_MESSAGE_READ**</span></span> <br/> |
|<span data-ttu-id="5b300-109">Estrutura de dados relacionados:</span><span class="sxs-lookup"><span data-stu-id="5b300-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="5b300-110">**[UPREAD](upread.md)**</span><span class="sxs-lookup"><span data-stu-id="5b300-110">**[UPREAD](upread.md)**</span></span> <br/> |
|<span data-ttu-id="5b300-111">Desse estado:</span><span class="sxs-lookup"><span data-stu-id="5b300-111">From this state:</span></span>  <br/> |[<span data-ttu-id="5b300-112">Carregar o estado da tabela</span><span class="sxs-lookup"><span data-stu-id="5b300-112">Upload table state</span></span>](upload-table-state.md) <br/> |
|<span data-ttu-id="5b300-113">Com esse estado:</span><span class="sxs-lookup"><span data-stu-id="5b300-113">To this state:</span></span>  <br/> |<span data-ttu-id="5b300-114">Carregar o estado da tabela</span><span class="sxs-lookup"><span data-stu-id="5b300-114">Upload table state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="5b300-115">A máquina de estado de replicação é uma máquina de estado determinantes.</span><span class="sxs-lookup"><span data-stu-id="5b300-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="5b300-116">Um cliente partindo de um estado para outro eventualmente deve retornar para o anterior do último.</span><span class="sxs-lookup"><span data-stu-id="5b300-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="5b300-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="5b300-117">Description</span></span>

<span data-ttu-id="5b300-118">Nesse estado inicia o carregamento do status de itens em uma pasta especificada em um estado de tabela anterior do carregamento leitura.</span><span class="sxs-lookup"><span data-stu-id="5b300-118">This state initiates uploading the read status of items in a folder specified in a preceding upload table state.</span></span> <span data-ttu-id="5b300-119">Durante esse estado, o Outlook inicializa a estrutura de dados **UPREAD** associada com informações para os itens na pasta cujo status de leitura foi alterada.</span><span class="sxs-lookup"><span data-stu-id="5b300-119">During this state, Outlook initializes the associated **UPREAD** data structure with information for those items in the folder whose read status has changed.</span></span> <span data-ttu-id="5b300-120">O cliente, em seguida, atualiza o status de leitura desses itens no servidor como sendo lidos ou não lidos.</span><span class="sxs-lookup"><span data-stu-id="5b300-120">The client then updates the read status of these items on the server as being read or unread.</span></span> 
  
<span data-ttu-id="5b300-121">Quando for encerrada nesse estado, o Outlook limpa as informações internas sobre o status do item leitura, impedindo que o status de leitura do item que está sendo carregado novamente.</span><span class="sxs-lookup"><span data-stu-id="5b300-121">When this state ends, Outlook clears the internal information about the item's read status, preventing the item's read status from being uploaded again.</span></span> <span data-ttu-id="5b300-122">Armazenamento local retorna para o estado da tabela de carregamento.</span><span class="sxs-lookup"><span data-stu-id="5b300-122">The local store returns to the upload table state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5b300-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="5b300-123">See also</span></span>



[<span data-ttu-id="5b300-124">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="5b300-124">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="5b300-125">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="5b300-125">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="5b300-126">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="5b300-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="5b300-127">ESTADO DE SINCRONIZAÇÃO</span><span class="sxs-lookup"><span data-stu-id="5b300-127">SYNCSTATE</span></span>](syncstate.md)

