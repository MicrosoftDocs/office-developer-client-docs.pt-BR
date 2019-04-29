---
title: Estado de hierarquia de upload
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: e39c4198-4913-5e86-900a-32e5ba5d801c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f789f4d7bbaf585d0d80f2208c35313542dfc191
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415422"
---
# <a name="upload-hierarchy-state"></a><span data-ttu-id="b3483-103">Estado de hierarquia de upload</span><span class="sxs-lookup"><span data-stu-id="b3483-103">Upload Hierarchy State</span></span>

  
  
<span data-ttu-id="b3483-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b3483-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="b3483-105">Este tópico descreve o que acontece durante o estado de hierarquia de upload da máquina de estado de replicação.</span><span class="sxs-lookup"><span data-stu-id="b3483-105">This topic describes what happens during the upload hierarchy state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="b3483-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="b3483-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b3483-107">Identificador de Estado:</span><span class="sxs-lookup"><span data-stu-id="b3483-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="b3483-108">**LR_SYNC_UPLOAD_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="b3483-108">**LR_SYNC_UPLOAD_HIERARCHY**</span></span> <br/> |
|<span data-ttu-id="b3483-109">Estrutura de dados relacionada:</span><span class="sxs-lookup"><span data-stu-id="b3483-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="b3483-110">**[UPHIER](uphier.md)**</span><span class="sxs-lookup"><span data-stu-id="b3483-110">**[UPHIER](uphier.md)**</span></span> <br/> |
|<span data-ttu-id="b3483-111">A partir deste Estado:</span><span class="sxs-lookup"><span data-stu-id="b3483-111">From this state:</span></span>  <br/> |[<span data-ttu-id="b3483-112">Estado Sincronizar</span><span class="sxs-lookup"><span data-stu-id="b3483-112">Synchronize state</span></span>](synchronize-state.md) <br/> |
|<span data-ttu-id="b3483-113">Para este Estado:</span><span class="sxs-lookup"><span data-stu-id="b3483-113">To this state:</span></span>  <br/> |<span data-ttu-id="b3483-114">[Carregar o estado da pasta](upload-folder-state.md)ou sincronizar estado</span><span class="sxs-lookup"><span data-stu-id="b3483-114">[Upload folder state](upload-folder-state.md), or synchronize state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="b3483-115">A máquina de estado de replicação é uma máquina de estado determinista.</span><span class="sxs-lookup"><span data-stu-id="b3483-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="b3483-116">Um cliente que faz parte de um estado para outro deve eventualmente retornar para o primeiro a partir do último.</span><span class="sxs-lookup"><span data-stu-id="b3483-116">A client departing one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="b3483-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="b3483-117">Description</span></span>

<span data-ttu-id="b3483-118">Este estado inicia o carregamento de uma hierarquia de árvore de pastas que foi especificada em um estado de sincronização anterior.</span><span class="sxs-lookup"><span data-stu-id="b3483-118">This state initiates uploading a folder tree hierarchy that has been specified in a preceding synchronize state.</span></span> <span data-ttu-id="b3483-119">O Outlook determina o número de pastas que foram criadas ou modificadas nessa hierarquia e inicializa a *centavos* no **UPHIER**.</span><span class="sxs-lookup"><span data-stu-id="b3483-119">Outlook determines the number of folders that have been created or modified in that hierarchy and initializes  *cEnt*  in **UPHIER**.</span></span> <span data-ttu-id="b3483-120">O Outlook também mantém uma contagem do número de pastas carregadas com outro membro *iEnt* .</span><span class="sxs-lookup"><span data-stu-id="b3483-120">Outlook also keeps a count of the number of uploaded folders with another member  *iEnt*  .</span></span> <span data-ttu-id="b3483-121">Para carregar cada uma das pastas de *centésimo* , o cliente move o repositório local para o estado de pasta de carregamento, retornando ao estado de hierarquia de carregamento quando o carregamento da pasta é concluído.</span><span class="sxs-lookup"><span data-stu-id="b3483-121">To upload each of the  *cEnt*  folders, the client moves the local store into the upload folder state, returning to the upload hierarchy state when the folder upload finishes.</span></span> 
  
<span data-ttu-id="b3483-122">Quando o estado de hierarquia de upload termina, o repositório local retorna ao estado de sincronização.</span><span class="sxs-lookup"><span data-stu-id="b3483-122">When the upload hierarchy state ends, the local store returns to the synchronize state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b3483-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="b3483-123">See also</span></span>



[<span data-ttu-id="b3483-124">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="b3483-124">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="b3483-125">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="b3483-125">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="b3483-126">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="b3483-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="b3483-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="b3483-127">SYNCSTATE</span></span>](syncstate.md)

