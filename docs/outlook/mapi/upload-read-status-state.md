---
title: Carregar estado de status de leitura
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d45574e-df87-8c44-4aa7-d41b38406f0a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e8ad2acf019df3f07060c8e8c71a62afd3fca03c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431537"
---
# <a name="upload-read-status-state"></a><span data-ttu-id="d7cce-103">Carregar estado de status de leitura</span><span class="sxs-lookup"><span data-stu-id="d7cce-103">Upload Read Status State</span></span>

  
  
<span data-ttu-id="d7cce-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d7cce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="d7cce-105">Este tópico descreve o que acontece durante o estado de upload de status de leitura da máquina de estado de replicação.</span><span class="sxs-lookup"><span data-stu-id="d7cce-105">This topic describes what happens during the upload read status state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="d7cce-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="d7cce-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d7cce-107">Identificador de Estado:</span><span class="sxs-lookup"><span data-stu-id="d7cce-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="d7cce-108">**LR_SYNC_UPLOAD_MESSAGE_READ**</span><span class="sxs-lookup"><span data-stu-id="d7cce-108">**LR_SYNC_UPLOAD_MESSAGE_READ**</span></span> <br/> |
|<span data-ttu-id="d7cce-109">Estrutura de dados relacionada:</span><span class="sxs-lookup"><span data-stu-id="d7cce-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="d7cce-110">**[UPREAD](upread.md)**</span><span class="sxs-lookup"><span data-stu-id="d7cce-110">**[UPREAD](upread.md)**</span></span> <br/> |
|<span data-ttu-id="d7cce-111">A partir deste Estado:</span><span class="sxs-lookup"><span data-stu-id="d7cce-111">From this state:</span></span>  <br/> |[<span data-ttu-id="d7cce-112">Carregar estado da tabela</span><span class="sxs-lookup"><span data-stu-id="d7cce-112">Upload table state</span></span>](upload-table-state.md) <br/> |
|<span data-ttu-id="d7cce-113">Para este Estado:</span><span class="sxs-lookup"><span data-stu-id="d7cce-113">To this state:</span></span>  <br/> |<span data-ttu-id="d7cce-114">Carregar estado da tabela</span><span class="sxs-lookup"><span data-stu-id="d7cce-114">Upload table state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="d7cce-115">A máquina de estado de replicação é uma máquina de estado determinista.</span><span class="sxs-lookup"><span data-stu-id="d7cce-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="d7cce-116">Um cliente que faz parte de um estado para outro deve eventualmente retornar para o primeiro a partir do último.</span><span class="sxs-lookup"><span data-stu-id="d7cce-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="d7cce-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="d7cce-117">Description</span></span>

<span data-ttu-id="d7cce-118">Este estado inicia o carregamento do status de leitura dos itens em uma pasta especificada em um estado de tabela de carregamento anterior.</span><span class="sxs-lookup"><span data-stu-id="d7cce-118">This state initiates uploading the read status of items in a folder specified in a preceding upload table state.</span></span> <span data-ttu-id="d7cce-119">Durante esse Estado, o Outlook Inicializa a estrutura de dados de **leitura** associada com informações para os itens na pasta cujo status de leitura foi alterado.</span><span class="sxs-lookup"><span data-stu-id="d7cce-119">During this state, Outlook initializes the associated **UPREAD** data structure with information for those items in the folder whose read status has changed.</span></span> <span data-ttu-id="d7cce-120">O cliente atualiza o status de leitura desses itens no servidor como sendo lido ou não lido.</span><span class="sxs-lookup"><span data-stu-id="d7cce-120">The client then updates the read status of these items on the server as being read or unread.</span></span> 
  
<span data-ttu-id="d7cce-121">Quando esse estado termina, o Outlook limpa as informações internas sobre o status de leitura do item, impedindo que o status de leitura do item seja carregado novamente.</span><span class="sxs-lookup"><span data-stu-id="d7cce-121">When this state ends, Outlook clears the internal information about the item's read status, preventing the item's read status from being uploaded again.</span></span> <span data-ttu-id="d7cce-122">O repositório local retorna ao estado de carregamento da tabela.</span><span class="sxs-lookup"><span data-stu-id="d7cce-122">The local store returns to the upload table state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d7cce-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7cce-123">See also</span></span>



[<span data-ttu-id="d7cce-124">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="d7cce-124">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="d7cce-125">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="d7cce-125">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="d7cce-126">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="d7cce-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="d7cce-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="d7cce-127">SYNCSTATE</span></span>](syncstate.md)

