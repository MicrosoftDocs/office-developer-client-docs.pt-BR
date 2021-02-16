---
title: Remover entradas do catálogo de endereços
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 107ebcd7-b612-4139-b676-c3851f15bc74
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 1d5ae33b08c85c9ee93764d762c2ec251fddd265
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425257"
---
# <a name="removing-address-book-entries"></a><span data-ttu-id="49b67-103">Remover entradas do catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="49b67-103">Removing address book entries</span></span>
  
<span data-ttu-id="49b67-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="49b67-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="49b67-105">O método [IABContainer::D eleteEntries](iabcontainer-deleteentries.md) do contêiner é chamado para remover um ou mais destinatários.</span><span class="sxs-lookup"><span data-stu-id="49b67-105">Your container's [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) method is called to remove one or more recipients.</span></span> <span data-ttu-id="49b67-106">**DeleteEntries** tem dois parâmetros: uma matriz de identificadores de entrada que representam os destinatários a serem excluídos e um valor de sinalizadores reservados.</span><span class="sxs-lookup"><span data-stu-id="49b67-106">**DeleteEntries** has two parameters: an array of entry identifiers representing the recipients to be deleted and a reserved flags value.</span></span> <span data-ttu-id="49b67-107">A exclusão de um destinatário afeta o índice de conteúdo do contêiner; além de excluir o destinatário, o contêiner deve excluir a linha da tabela de conteúdo que representa o destinatário.</span><span class="sxs-lookup"><span data-stu-id="49b67-107">Deleting a recipient affects the contents table of your container; in addition to deleting the recipient, your container must delete the contents table row that represents the recipient.</span></span> <span data-ttu-id="49b67-108">Quando a linha tiver sido removida da tabela, o contêiner deverá emitir uma notificação de tabela para cada cliente registrado.</span><span class="sxs-lookup"><span data-stu-id="49b67-108">When the row has been removed from the table, your container must issue a table notification to each registered client.</span></span> 
  
### <a name="to-implement-iabcontainerdeleteentries"></a><span data-ttu-id="49b67-109">Para implementar IABContainer::D eleteEntries</span><span class="sxs-lookup"><span data-stu-id="49b67-109">To implement IABContainer::DeleteEntries</span></span>
  
1. <span data-ttu-id="49b67-110">Exclua cada destinatário representado pelo identificador de entrada do contêiner.</span><span class="sxs-lookup"><span data-stu-id="49b67-110">Delete each recipient represented by the entry identifier from your container.</span></span>
    
2. <span data-ttu-id="49b67-111">Se a tabela de conteúdo do contêiner estiver aberta:</span><span class="sxs-lookup"><span data-stu-id="49b67-111">If your container's contents table is open:</span></span>
    
   - <span data-ttu-id="49b67-112">Envie uma  _notificação fnevTableModified_ com o membro **ulTableEvent** definido como TABLE_ROW_DELETED clientes registrados para cada linha de tabela de conteúdo excluída.</span><span class="sxs-lookup"><span data-stu-id="49b67-112">Send an  _fnevTableModified_ notification with the **ulTableEvent** member set to TABLE_ROW_DELETED to registered clients for each deleted contents table row.</span></span> <span data-ttu-id="49b67-113">Se o provedor usar o utilitário de notificação, chame [IMAPISupport::Notify](imapisupport-notify.md) para enviar essas notificações.</span><span class="sxs-lookup"><span data-stu-id="49b67-113">If your provider uses the notification utility, call [IMAPISupport::Notify](imapisupport-notify.md) to send these notifications.</span></span> 
    
   - <span data-ttu-id="49b67-114">Se o provedor suportar notificações de objeto, envie também uma _notificação fnevObjectDeleted._</span><span class="sxs-lookup"><span data-stu-id="49b67-114">If your provider supports object notifications, also send an  _fnevObjectDeleted_ notification.</span></span> 
    

