---
title: Sincronizar o estado do conteúdo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 52216bc3-8cbd-3856-ea46-78f7d0dd66ff
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3ebe1f5f48f9becdf01ea184c2b76fa2c8fa21e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349564"
---
# <a name="synchronize-contents-state"></a><span data-ttu-id="bd350-103">Sincronizar o estado do conteúdo</span><span class="sxs-lookup"><span data-stu-id="bd350-103">Synchronize Contents State</span></span>

  
  
<span data-ttu-id="bd350-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bd350-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="bd350-105">Este tópico descreve o que acontece durante o estado sincronizar conteúdo da máquina de estado de replicação.</span><span class="sxs-lookup"><span data-stu-id="bd350-105">This topic describes what happens during the synchronize contents state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="bd350-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="bd350-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bd350-107">Identificador de Estado:</span><span class="sxs-lookup"><span data-stu-id="bd350-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="bd350-108">**LR_SYNC_CONTENTS**</span><span class="sxs-lookup"><span data-stu-id="bd350-108">**LR_SYNC_CONTENTS**</span></span> <br/> |
|<span data-ttu-id="bd350-109">Estrutura de dados relacionada:</span><span class="sxs-lookup"><span data-stu-id="bd350-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="bd350-110">**[SYNCCONT](synccont.md)**</span><span class="sxs-lookup"><span data-stu-id="bd350-110">**[SYNCCONT](synccont.md)**</span></span> <br/> |
|<span data-ttu-id="bd350-111">A partir deste Estado:</span><span class="sxs-lookup"><span data-stu-id="bd350-111">From this state:</span></span>  <br/> |[<span data-ttu-id="bd350-112">Estado Sincronizar</span><span class="sxs-lookup"><span data-stu-id="bd350-112">Synchronize state</span></span>](synchronize-state.md) <br/> |
|<span data-ttu-id="bd350-113">Para este Estado:</span><span class="sxs-lookup"><span data-stu-id="bd350-113">To this state:</span></span>  <br/> |<span data-ttu-id="bd350-114">[Baixar o estado da tabela](download-table-state.md), carregar o estado da [tabela](upload-table-state.md)ou sincronizar estado</span><span class="sxs-lookup"><span data-stu-id="bd350-114">[Download table state](download-table-state.md), [upload table state](upload-table-state.md), or synchronize state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="bd350-115">A máquina de estado de replicação é uma máquina de estado determinista.</span><span class="sxs-lookup"><span data-stu-id="bd350-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="bd350-116">Um cliente que faz parte de um estado para outro deve eventualmente retornar para o primeiro a partir do último.</span><span class="sxs-lookup"><span data-stu-id="bd350-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="bd350-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="bd350-117">Description</span></span>

<span data-ttu-id="bd350-118">Este estado inicia um dos dois processos de replicação: carregar o conteúdo de pastas especificadas em um repositório local ou uma sincronização completa.</span><span class="sxs-lookup"><span data-stu-id="bd350-118">This state initiates one of the two replication processes: uploading the contents of specified folders on a local store, or a full synchronization.</span></span> <span data-ttu-id="bd350-119">Em uma sincronização completa, para cada uma das pastas especificadas, o conteúdo é carregado primeiro e, em seguida, baixado.</span><span class="sxs-lookup"><span data-stu-id="bd350-119">In a full synchronization, for each of the specified folders, contents are uploaded first and then downloaded.</span></span> <span data-ttu-id="bd350-120">Dependendo do conjunto *parâmetroulflags* na estrutura de **[sincronização](sync.md)** correspondente no estado de sincronização anterior, o Outlook inicializará [out] Membros na estrutura **SYNCCONT** para fornecer informações sobre o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="bd350-120">Depending on the  *ulFlags*  set in the corresponding **[SYNC](sync.md)** structure in the preceding synchronize state, Outlook initializes [out] members in the **SYNCCONT** structure to provide information about the contents.</span></span> 
  
<span data-ttu-id="bd350-121">Através da mesma estrutura **SYNCCONT** , o cliente obtém a contagem das pastas que têm conteúdo a ser carregado ou baixado.</span><span class="sxs-lookup"><span data-stu-id="bd350-121">Through the same **SYNCCONT** structure, the client obtains the count of the folders that have content to be uploaded or downloaded.</span></span> <span data-ttu-id="bd350-122">O cliente executará um loop através de cada uma dessas pastas movendo o repositório local para o estado de carregamento da tabela para carregar uma pasta ou mover o repositório local para o estado de download da tabela para baixar a pasta.</span><span class="sxs-lookup"><span data-stu-id="bd350-122">The client will loop through each of these folders by moving the local store to the upload table state to upload a folder, or moving the local store to the download table state to download the folder.</span></span> 
  
<span data-ttu-id="bd350-123">Além disso, o cliente obtém IDs de entrada para as pastas que requerem replicação.</span><span class="sxs-lookup"><span data-stu-id="bd350-123">In addition, the client obtains entry IDs for the folders requiring replication.</span></span>
  
<span data-ttu-id="bd350-124">Quando esse estado termina, o Outlook limpa suas informações internas.</span><span class="sxs-lookup"><span data-stu-id="bd350-124">When this state ends, Outlook cleans up its internal information.</span></span> <span data-ttu-id="bd350-125">O repositório local retorna ao estado de sincronização.</span><span class="sxs-lookup"><span data-stu-id="bd350-125">The local store returns to the synchronize state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bd350-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="bd350-126">See also</span></span>



[<span data-ttu-id="bd350-127">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="bd350-127">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="bd350-128">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="bd350-128">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="bd350-129">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="bd350-129">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="bd350-130">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="bd350-130">SYNCSTATE</span></span>](syncstate.md)

