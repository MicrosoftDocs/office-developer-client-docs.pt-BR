---
title: Carregar o estado da tabela
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: fe167c90-c817-b627-0728-5c6393477c22
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: bd54c30e8701a13637235e28ddcfef4c21d10a2b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576978"
---
# <a name="upload-table-state"></a><span data-ttu-id="19b27-103">Carregar o estado da tabela</span><span class="sxs-lookup"><span data-stu-id="19b27-103">Upload Table State</span></span>

  
  
<span data-ttu-id="19b27-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="19b27-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="19b27-105">Este tópico descreve o que acontece durante o estado da tabela de carregamento da máquina de estado de replicação.</span><span class="sxs-lookup"><span data-stu-id="19b27-105">This topic describes what happens during the upload table state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="19b27-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="19b27-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="19b27-107">Identificador de controle de sessão:</span><span class="sxs-lookup"><span data-stu-id="19b27-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="19b27-108">**LR_SYNC_UPLOAD_TABLE**</span><span class="sxs-lookup"><span data-stu-id="19b27-108">**LR_SYNC_UPLOAD_TABLE**</span></span> <br/> |
|<span data-ttu-id="19b27-109">Estrutura de dados relacionados:</span><span class="sxs-lookup"><span data-stu-id="19b27-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="19b27-110">**[UPTBL](uptbl.md)**</span><span class="sxs-lookup"><span data-stu-id="19b27-110">**[UPTBL](uptbl.md)**</span></span> <br/> |
|<span data-ttu-id="19b27-111">Desse estado:</span><span class="sxs-lookup"><span data-stu-id="19b27-111">From this state:</span></span>  <br/> |[<span data-ttu-id="19b27-112">Sincronizar o estado de conteúdo</span><span class="sxs-lookup"><span data-stu-id="19b27-112">Synchronize contents state</span></span>](synchronize-contents-state.md) <br/> |
|<span data-ttu-id="19b27-113">Com esse estado:</span><span class="sxs-lookup"><span data-stu-id="19b27-113">To this state:</span></span>  <br/> |<span data-ttu-id="19b27-114">[Carregar o estado da mensagem](upload-message-state.md), [carregamento excluir estado de status](upload-delete-status-state.md), [carregamento ler o estado de status](upload-read-status-state.md), ou sincronizar o estado de conteúdo</span><span class="sxs-lookup"><span data-stu-id="19b27-114">[Upload message state](upload-message-state.md), [upload delete status state](upload-delete-status-state.md), [upload read status state](upload-read-status-state.md), or synchronize contents state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="19b27-115">A máquina de estado de replicação é uma máquina de estado determinantes.</span><span class="sxs-lookup"><span data-stu-id="19b27-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="19b27-116">Um cliente partindo de um estado para outro eventualmente deve retornar para o anterior do último.</span><span class="sxs-lookup"><span data-stu-id="19b27-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="19b27-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="19b27-117">Description</span></span>

<span data-ttu-id="19b27-118">Nesse estado inicia carregar o conteúdo de uma pasta que foi especificado em um estado de conteúdo anterior sincronizar.</span><span class="sxs-lookup"><span data-stu-id="19b27-118">This state initiates uploading the contents of a folder that has been specified in a preceding synchronize contents state.</span></span> <span data-ttu-id="19b27-119">A pasta pode ser uma pasta de email, calendário, contatos, tarefas, anotações ou diário.</span><span class="sxs-lookup"><span data-stu-id="19b27-119">The folder can be a mail, calendar, contacts, tasks, notes, or journal folder.</span></span> <span data-ttu-id="19b27-120">Durante esse estado, Outlook cria uma lista de itens que foram adicionados, modificado, movido, excluído ou marcado como lido e prepara as informações apropriadas de internas para o estado de mensagem de carregamento correspondente, carregar o estado de status de excluir ou carregar o status de leitura estado.</span><span class="sxs-lookup"><span data-stu-id="19b27-120">During this state, Outlook creates a list of items that have been added, modified, moved, deleted, or marked as read, and prepares the appropriate internal information for the corresponding upload message state, upload delete status state, or upload read status state.</span></span>
  
<span data-ttu-id="19b27-121">Quando for encerrada nesse estado, o Outlook marca a pasta como tendo seu conteúdo sincronizado, para que o conteúdo não será carregado novamente até que a outra modificação for feita.</span><span class="sxs-lookup"><span data-stu-id="19b27-121">When this state ends, Outlook marks the folder as having its contents synchronized, so that the contents will not be uploaded again until another modification is made.</span></span> <span data-ttu-id="19b27-122">Armazenamento local retorna ao estado sincronizar conteúdo.</span><span class="sxs-lookup"><span data-stu-id="19b27-122">The local store returns to the synchronize contents state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="19b27-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="19b27-123">See also</span></span>



[<span data-ttu-id="19b27-124">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="19b27-124">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="19b27-125">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="19b27-125">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="19b27-126">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="19b27-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="19b27-127">ESTADO DE SINCRONIZAÇÃO</span><span class="sxs-lookup"><span data-stu-id="19b27-127">SYNCSTATE</span></span>](syncstate.md)

