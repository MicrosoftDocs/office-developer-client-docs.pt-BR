---
title: Carregar Estado de Status de Leitura
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
# <a name="upload-read-status-state"></a><span data-ttu-id="9237a-103">Carregar Estado de Status de Leitura</span><span class="sxs-lookup"><span data-stu-id="9237a-103">Upload Read Status State</span></span>

  
  
<span data-ttu-id="9237a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9237a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="9237a-105">Este tópico descreve o que acontece durante o estado de status de leitura do upload da máquina de estado de replicação.</span><span class="sxs-lookup"><span data-stu-id="9237a-105">This topic describes what happens during the upload read status state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="9237a-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="9237a-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9237a-107">Identificador de Estado:</span><span class="sxs-lookup"><span data-stu-id="9237a-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="9237a-108">**LR_SYNC_UPLOAD_MESSAGE_READ**</span><span class="sxs-lookup"><span data-stu-id="9237a-108">**LR_SYNC_UPLOAD_MESSAGE_READ**</span></span> <br/> |
|<span data-ttu-id="9237a-109">Estrutura de dados relacionada:</span><span class="sxs-lookup"><span data-stu-id="9237a-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="9237a-110">**[UPREAD](upread.md)**</span><span class="sxs-lookup"><span data-stu-id="9237a-110">**[UPREAD](upread.md)**</span></span> <br/> |
|<span data-ttu-id="9237a-111">Desse estado:</span><span class="sxs-lookup"><span data-stu-id="9237a-111">From this state:</span></span>  <br/> |[<span data-ttu-id="9237a-112">Estado carregar tabela</span><span class="sxs-lookup"><span data-stu-id="9237a-112">Upload table state</span></span>](upload-table-state.md) <br/> |
|<span data-ttu-id="9237a-113">Para esse estado:</span><span class="sxs-lookup"><span data-stu-id="9237a-113">To this state:</span></span>  <br/> |<span data-ttu-id="9237a-114">Estado carregar tabela</span><span class="sxs-lookup"><span data-stu-id="9237a-114">Upload table state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="9237a-115">A máquina de estado de replicação é uma máquina de estado determinística.</span><span class="sxs-lookup"><span data-stu-id="9237a-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="9237a-116">Um cliente que sai de um estado para outro eventualmente deve retornar ao primeiro do último.</span><span class="sxs-lookup"><span data-stu-id="9237a-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="9237a-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="9237a-117">Description</span></span>

<span data-ttu-id="9237a-118">Esse estado inicia o upload do status de leitura dos itens em uma pasta especificada em um estado de tabela de carregamento anterior.</span><span class="sxs-lookup"><span data-stu-id="9237a-118">This state initiates uploading the read status of items in a folder specified in a preceding upload table state.</span></span> <span data-ttu-id="9237a-119">Durante esse estado, o Outlook inicializa a estrutura de dados **UPREAD** associada com informações para esses itens na pasta cujo status de leitura foi alterado.</span><span class="sxs-lookup"><span data-stu-id="9237a-119">During this state, Outlook initializes the associated **UPREAD** data structure with information for those items in the folder whose read status has changed.</span></span> <span data-ttu-id="9237a-120">Em seguida, o cliente atualiza o status de leitura desses itens no servidor como lidos ou não lidos.</span><span class="sxs-lookup"><span data-stu-id="9237a-120">The client then updates the read status of these items on the server as being read or unread.</span></span> 
  
<span data-ttu-id="9237a-121">Quando esse estado termina, o Outlook limpa as informações internas sobre o status de leitura do item, impedindo que o status de leitura do item seja carregado novamente.</span><span class="sxs-lookup"><span data-stu-id="9237a-121">When this state ends, Outlook clears the internal information about the item's read status, preventing the item's read status from being uploaded again.</span></span> <span data-ttu-id="9237a-122">O armazenamento local retorna ao estado da tabela de carregamento.</span><span class="sxs-lookup"><span data-stu-id="9237a-122">The local store returns to the upload table state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9237a-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="9237a-123">See also</span></span>



[<span data-ttu-id="9237a-124">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="9237a-124">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="9237a-125">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="9237a-125">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="9237a-126">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="9237a-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="9237a-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="9237a-127">SYNCSTATE</span></span>](syncstate.md)

