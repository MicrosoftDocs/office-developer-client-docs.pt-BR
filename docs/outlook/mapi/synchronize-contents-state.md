---
title: Sincronizar o estado do conteúdo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 52216bc3-8cbd-3856-ea46-78f7d0dd66ff
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 216691f2c1f94d658a5aa968d6a19148a9b3c06a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770557"
---
# <a name="synchronize-contents-state"></a><span data-ttu-id="024d7-103">Sincronizar o estado do conteúdo</span><span class="sxs-lookup"><span data-stu-id="024d7-103">Synchronize Contents State</span></span>

  
  
<span data-ttu-id="024d7-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="024d7-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="024d7-105">Este tópico descreve o que acontece durante o estado de conteúdo de sincronizar da máquina de estado de replicação.</span><span class="sxs-lookup"><span data-stu-id="024d7-105">This topic describes what happens during the synchronize contents state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="024d7-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="024d7-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="024d7-107">Identificador de controle de sessão:</span><span class="sxs-lookup"><span data-stu-id="024d7-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="024d7-108">**LR_SYNC_CONTENTS**</span><span class="sxs-lookup"><span data-stu-id="024d7-108">**LR_SYNC_CONTENTS**</span></span> <br/> |
|<span data-ttu-id="024d7-109">Estrutura de dados relacionados:</span><span class="sxs-lookup"><span data-stu-id="024d7-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="024d7-110">**[SYNCCONT](synccont.md)**</span><span class="sxs-lookup"><span data-stu-id="024d7-110">**[SYNCCONT](synccont.md)**</span></span> <br/> |
|<span data-ttu-id="024d7-111">Desse estado:</span><span class="sxs-lookup"><span data-stu-id="024d7-111">From this state:</span></span>  <br/> |[<span data-ttu-id="024d7-112">Sincronizar o estado</span><span class="sxs-lookup"><span data-stu-id="024d7-112">Synchronize state</span></span>](synchronize-state.md) <br/> |
|<span data-ttu-id="024d7-113">Com esse estado:</span><span class="sxs-lookup"><span data-stu-id="024d7-113">To this state:</span></span>  <br/> |<span data-ttu-id="024d7-114">[Baixar o estado da tabela](download-table-state.md), [carregar o estado da tabela](upload-table-state.md), ou sincronizar o estado</span><span class="sxs-lookup"><span data-stu-id="024d7-114">[Download table state](download-table-state.md), [upload table state](upload-table-state.md), or synchronize state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="024d7-115">A máquina de estado de replicação é uma máquina de estado determinantes.</span><span class="sxs-lookup"><span data-stu-id="024d7-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="024d7-116">Um cliente partindo de um estado para outro eventualmente deve retornar para o anterior do último.</span><span class="sxs-lookup"><span data-stu-id="024d7-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="024d7-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="024d7-117">Description</span></span>

<span data-ttu-id="024d7-118">Nesse estado inicia um dos dois processos de replicação: carregar o conteúdo de especificado pastas em um repositório local ou uma sincronização completa.</span><span class="sxs-lookup"><span data-stu-id="024d7-118">This state initiates one of the two replication processes: uploading the contents of specified folders on a local store, or a full synchronization.</span></span> <span data-ttu-id="024d7-119">Em uma sincronização completa, para cada uma das pastas especificadas, o conteúdo é carregado pela primeira vez e então baixado.</span><span class="sxs-lookup"><span data-stu-id="024d7-119">In a full synchronization, for each of the specified folders, contents are uploaded first and then downloaded.</span></span> <span data-ttu-id="024d7-120">Dependendo da *ulFlags* definido na estrutura de **[sincronização](sync.md)** correspondente na anterior sincronizar o estado, Outlook inicializa [out] membros na estrutura de **SYNCCONT** para fornecer informações sobre o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="024d7-120">Depending on the  *ulFlags*  set in the corresponding **[SYNC](sync.md)** structure in the preceding synchronize state, Outlook initializes [out] members in the **SYNCCONT** structure to provide information about the contents.</span></span> 
  
<span data-ttu-id="024d7-121">Através da mesma estrutura **SYNCCONT** , o cliente obtém a contagem das pastas que possuem conteúdo sejam carregados ou baixados.</span><span class="sxs-lookup"><span data-stu-id="024d7-121">Through the same **SYNCCONT** structure, the client obtains the count of the folders that have content to be uploaded or downloaded.</span></span> <span data-ttu-id="024d7-122">O cliente fará um loop através de cada uma dessas pastas movendo o armazenamento local para o estado da tabela de carregar para carregar uma pasta ou mover o repositório de local para o estado da tabela de download para baixar a pasta.</span><span class="sxs-lookup"><span data-stu-id="024d7-122">The client will loop through each of these folders by moving the local store to the upload table state to upload a folder, or moving the local store to the download table state to download the folder.</span></span> 
  
<span data-ttu-id="024d7-123">Além disso, o cliente obtém IDs de entradas para as pastas que necessitam de replicação.</span><span class="sxs-lookup"><span data-stu-id="024d7-123">In addition, the client obtains entry IDs for the folders requiring replication.</span></span>
  
<span data-ttu-id="024d7-124">Quando for encerrada nesse estado, o Outlook limpa suas informações internas.</span><span class="sxs-lookup"><span data-stu-id="024d7-124">When this state ends, Outlook cleans up its internal information.</span></span> <span data-ttu-id="024d7-125">Armazenamento local retorna ao estado sincronizar.</span><span class="sxs-lookup"><span data-stu-id="024d7-125">The local store returns to the synchronize state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="024d7-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="024d7-126">See also</span></span>



[<span data-ttu-id="024d7-127">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="024d7-127">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="024d7-128">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="024d7-128">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="024d7-129">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="024d7-129">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="024d7-130">ESTADO DE SINCRONIZAÇÃO</span><span class="sxs-lookup"><span data-stu-id="024d7-130">SYNCSTATE</span></span>](syncstate.md)

