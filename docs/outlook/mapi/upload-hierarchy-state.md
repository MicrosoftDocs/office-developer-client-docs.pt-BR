---
title: Carregar o estado da hierarquia
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: e39c4198-4913-5e86-900a-32e5ba5d801c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d53790cb51b660c781190cf41ca317c823a021e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770678"
---
# <a name="upload-hierarchy-state"></a><span data-ttu-id="bf547-103">Carregar o estado da hierarquia</span><span class="sxs-lookup"><span data-stu-id="bf547-103">Upload Hierarchy State</span></span>

  
  
<span data-ttu-id="bf547-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bf547-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="bf547-105">Este tópico descreve o que acontece durante o estado de hierarquia de carregamento da máquina de estado de replicação.</span><span class="sxs-lookup"><span data-stu-id="bf547-105">This topic describes what happens during the upload hierarchy state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="bf547-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="bf547-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bf547-107">Identificador de controle de sessão:</span><span class="sxs-lookup"><span data-stu-id="bf547-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="bf547-108">**LR_SYNC_UPLOAD_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="bf547-108">**LR_SYNC_UPLOAD_HIERARCHY**</span></span> <br/> |
|<span data-ttu-id="bf547-109">Estrutura de dados relacionados:</span><span class="sxs-lookup"><span data-stu-id="bf547-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="bf547-110">**[UPHIER](uphier.md)**</span><span class="sxs-lookup"><span data-stu-id="bf547-110">**[UPHIER](uphier.md)**</span></span> <br/> |
|<span data-ttu-id="bf547-111">Desse estado:</span><span class="sxs-lookup"><span data-stu-id="bf547-111">From this state:</span></span>  <br/> |[<span data-ttu-id="bf547-112">Sincronizar o estado</span><span class="sxs-lookup"><span data-stu-id="bf547-112">Synchronize state</span></span>](synchronize-state.md) <br/> |
|<span data-ttu-id="bf547-113">Com esse estado:</span><span class="sxs-lookup"><span data-stu-id="bf547-113">To this state:</span></span>  <br/> |<span data-ttu-id="bf547-114">[Carregar o estado de pasta](upload-folder-state.md), ou sincronizar o estado</span><span class="sxs-lookup"><span data-stu-id="bf547-114">[Upload folder state](upload-folder-state.md), or synchronize state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="bf547-115">A máquina de estado de replicação é uma máquina de estado determinantes.</span><span class="sxs-lookup"><span data-stu-id="bf547-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="bf547-116">Um cliente de um estado de início para outro eventualmente deve retornar para o anterior do último.</span><span class="sxs-lookup"><span data-stu-id="bf547-116">A client departing one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="bf547-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="bf547-117">Description</span></span>

<span data-ttu-id="bf547-118">Nesse estado inicia o carregamento de uma hierarquia de árvore de pastas que foi especificada na precedidos sincronizar o estado.</span><span class="sxs-lookup"><span data-stu-id="bf547-118">This state initiates uploading a folder tree hierarchy that has been specified in a preceding synchronize state.</span></span> <span data-ttu-id="bf547-119">O Outlook determina o número de pastas que foram criados ou modificados nessa hierarquia e inicializa *cEnt* em **UPHIER**.</span><span class="sxs-lookup"><span data-stu-id="bf547-119">Outlook determines the number of folders that have been created or modified in that hierarchy and initializes  *cEnt*  in **UPHIER**.</span></span> <span data-ttu-id="bf547-120">Além disso, o Outlook mantém uma contagem do número de pastas carregados com *iEnt* de outro membro.</span><span class="sxs-lookup"><span data-stu-id="bf547-120">Outlook also keeps a count of the number of uploaded folders with another member  *iEnt*  .</span></span> <span data-ttu-id="bf547-121">Para carregar a cada uma das pastas *cEnt* , o cliente move o armazenamento local para o estado da pasta de carregamento, retornando para o estado de hierarquia de carregamento quando termina o carregamento da pasta.</span><span class="sxs-lookup"><span data-stu-id="bf547-121">To upload each of the  *cEnt*  folders, the client moves the local store into the upload folder state, returning to the upload hierarchy state when the folder upload finishes.</span></span> 
  
<span data-ttu-id="bf547-122">Quando o estado de hierarquia de carregamento for encerrada, armazenamento local retorna ao estado sincronizar.</span><span class="sxs-lookup"><span data-stu-id="bf547-122">When the upload hierarchy state ends, the local store returns to the synchronize state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bf547-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="bf547-123">See also</span></span>



[<span data-ttu-id="bf547-124">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="bf547-124">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="bf547-125">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="bf547-125">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="bf547-126">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="bf547-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="bf547-127">ESTADO DE SINCRONIZAÇÃO</span><span class="sxs-lookup"><span data-stu-id="bf547-127">SYNCSTATE</span></span>](syncstate.md)

