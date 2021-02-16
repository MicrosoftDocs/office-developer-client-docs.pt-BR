---
title: Sincronizar o estado do conteúdo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 52216bc3-8cbd-3856-ea46-78f7d0dd66ff
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3ebe1f5f48f9becdf01ea184c2b76fa2c8fa21e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438467"
---
# <a name="synchronize-contents-state"></a><span data-ttu-id="4e658-103">Sincronizar o estado do conteúdo</span><span class="sxs-lookup"><span data-stu-id="4e658-103">Synchronize Contents State</span></span>

  
  
<span data-ttu-id="4e658-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4e658-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="4e658-105">Este tópico descreve o que acontece durante o estado de sincronização do conteúdo da máquina de estado de replicação.</span><span class="sxs-lookup"><span data-stu-id="4e658-105">This topic describes what happens during the synchronize contents state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="4e658-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="4e658-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4e658-107">Identificador de Estado:</span><span class="sxs-lookup"><span data-stu-id="4e658-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="4e658-108">**LR_SYNC_CONTENTS**</span><span class="sxs-lookup"><span data-stu-id="4e658-108">**LR_SYNC_CONTENTS**</span></span> <br/> |
|<span data-ttu-id="4e658-109">Estrutura de dados relacionada:</span><span class="sxs-lookup"><span data-stu-id="4e658-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="4e658-110">**[SYNCCONT](synccont.md)**</span><span class="sxs-lookup"><span data-stu-id="4e658-110">**[SYNCCONT](synccont.md)**</span></span> <br/> |
|<span data-ttu-id="4e658-111">Desse estado:</span><span class="sxs-lookup"><span data-stu-id="4e658-111">From this state:</span></span>  <br/> |[<span data-ttu-id="4e658-112">Estado Sincronizar</span><span class="sxs-lookup"><span data-stu-id="4e658-112">Synchronize state</span></span>](synchronize-state.md) <br/> |
|<span data-ttu-id="4e658-113">Para esse estado:</span><span class="sxs-lookup"><span data-stu-id="4e658-113">To this state:</span></span>  <br/> |<span data-ttu-id="4e658-114">[Estado de download da tabela,](download-table-state.md) [estado de carregamento da](upload-table-state.md)tabela ou estado de sincronização</span><span class="sxs-lookup"><span data-stu-id="4e658-114">[Download table state](download-table-state.md), [upload table state](upload-table-state.md), or synchronize state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="4e658-115">A máquina de estado de replicação é uma máquina de estado determinística.</span><span class="sxs-lookup"><span data-stu-id="4e658-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="4e658-116">Um cliente que sai de um estado para outro eventualmente deve retornar ao primeiro do último.</span><span class="sxs-lookup"><span data-stu-id="4e658-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="4e658-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="4e658-117">Description</span></span>

<span data-ttu-id="4e658-118">Esse estado inicia um dos dois processos de replicação: carregar o conteúdo das pastas especificadas em um armazenamento local ou uma sincronização completa.</span><span class="sxs-lookup"><span data-stu-id="4e658-118">This state initiates one of the two replication processes: uploading the contents of specified folders on a local store, or a full synchronization.</span></span> <span data-ttu-id="4e658-119">Em uma sincronização completa, para cada uma das pastas especificadas, o conteúdo é carregado primeiro e, em seguida, baixado.</span><span class="sxs-lookup"><span data-stu-id="4e658-119">In a full synchronization, for each of the specified folders, contents are uploaded first and then downloaded.</span></span> <span data-ttu-id="4e658-120">Dependendo do  *ulFlags*  definido na estrutura **[SYNC](sync.md)** correspondente no estado de sincronização anterior, o Outlook inicializa membros [out] na estrutura **SYNCCONT** para fornecer informações sobre o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="4e658-120">Depending on the  *ulFlags*  set in the corresponding **[SYNC](sync.md)** structure in the preceding synchronize state, Outlook initializes [out] members in the **SYNCCONT** structure to provide information about the contents.</span></span> 
  
<span data-ttu-id="4e658-121">Por meio da mesma **estrutura SYNCCONT,** o cliente obtém a contagem das pastas que têm conteúdo a ser carregado ou baixado.</span><span class="sxs-lookup"><span data-stu-id="4e658-121">Through the same **SYNCCONT** structure, the client obtains the count of the folders that have content to be uploaded or downloaded.</span></span> <span data-ttu-id="4e658-122">O cliente fará um loop por cada uma dessas pastas movendo o armazenamento local para o estado carregar tabela para carregar uma pasta ou movendo o armazenamento local para o estado de tabela de download para baixar a pasta.</span><span class="sxs-lookup"><span data-stu-id="4e658-122">The client will loop through each of these folders by moving the local store to the upload table state to upload a folder, or moving the local store to the download table state to download the folder.</span></span> 
  
<span data-ttu-id="4e658-123">Além disso, o cliente obtém IDs de entrada para as pastas que exigem replicação.</span><span class="sxs-lookup"><span data-stu-id="4e658-123">In addition, the client obtains entry IDs for the folders requiring replication.</span></span>
  
<span data-ttu-id="4e658-124">Quando esse estado termina, o Outlook limpa suas informações internas.</span><span class="sxs-lookup"><span data-stu-id="4e658-124">When this state ends, Outlook cleans up its internal information.</span></span> <span data-ttu-id="4e658-125">O armazenamento local retorna ao estado de sincronização.</span><span class="sxs-lookup"><span data-stu-id="4e658-125">The local store returns to the synchronize state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4e658-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="4e658-126">See also</span></span>



[<span data-ttu-id="4e658-127">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="4e658-127">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="4e658-128">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="4e658-128">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="4e658-129">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="4e658-129">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="4e658-130">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="4e658-130">SYNCSTATE</span></span>](syncstate.md)

