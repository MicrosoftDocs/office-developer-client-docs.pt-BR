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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328347"
---
# <a name="removing-address-book-entries"></a><span data-ttu-id="bc742-103">Remover entradas do catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="bc742-103">Removing address book entries</span></span>
  
<span data-ttu-id="bc742-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bc742-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bc742-105">O método IABContainer do seu contêiner [::D eleteentries](iabcontainer-deleteentries.md) é chamado para remover um ou mais destinatários.</span><span class="sxs-lookup"><span data-stu-id="bc742-105">Your container's [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) method is called to remove one or more recipients.</span></span> <span data-ttu-id="bc742-106">**DeleteEntries** tem dois parâmetros: uma matriz de identificadores de entrada que representa os destinatários a serem excluídos e um valor de sinalizadores reservados.</span><span class="sxs-lookup"><span data-stu-id="bc742-106">**DeleteEntries** has two parameters: an array of entry identifiers representing the recipients to be deleted and a reserved flags value.</span></span> <span data-ttu-id="bc742-107">A exclusão de um destinatário afeta a tabela de conteúdo do seu contêiner; Além de excluir o destinatário, seu contêiner deve excluir a linha da tabela de conteúdo que representa o destinatário.</span><span class="sxs-lookup"><span data-stu-id="bc742-107">Deleting a recipient affects the contents table of your container; in addition to deleting the recipient, your container must delete the contents table row that represents the recipient.</span></span> <span data-ttu-id="bc742-108">Quando a linha foi removida da tabela, seu contêiner deve emitir uma notificação de tabela para cada cliente registrado.</span><span class="sxs-lookup"><span data-stu-id="bc742-108">When the row has been removed from the table, your container must issue a table notification to each registered client.</span></span> 
  
### <a name="to-implement-iabcontainerdeleteentries"></a><span data-ttu-id="bc742-109">Para implementar o IABContainer::D eleteEntries</span><span class="sxs-lookup"><span data-stu-id="bc742-109">To implement IABContainer::DeleteEntries</span></span>
  
1. <span data-ttu-id="bc742-110">Exclua cada destinatário representado pelo identificador de entrada de seu contêiner.</span><span class="sxs-lookup"><span data-stu-id="bc742-110">Delete each recipient represented by the entry identifier from your container.</span></span>
    
2. <span data-ttu-id="bc742-111">Se a tabela de conteúdo do seu contêiner estiver aberta:</span><span class="sxs-lookup"><span data-stu-id="bc742-111">If your container's contents table is open:</span></span>
    
   - <span data-ttu-id="bc742-112">Envie uma notificação do _fnevTableModified_ com o membro **ULTABLEEVENT** definido como TABLE_ROW_DELETED para clientes registrados para cada linha de tabela de conteúdo excluída.</span><span class="sxs-lookup"><span data-stu-id="bc742-112">Send an  _fnevTableModified_ notification with the **ulTableEvent** member set to TABLE_ROW_DELETED to registered clients for each deleted contents table row.</span></span> <span data-ttu-id="bc742-113">Se seu provedor usar o utilitário de notificação, chame [IMAPISupport:: Notify](imapisupport-notify.md) para enviar essas notificações.</span><span class="sxs-lookup"><span data-stu-id="bc742-113">If your provider uses the notification utility, call [IMAPISupport::Notify](imapisupport-notify.md) to send these notifications.</span></span> 
    
   - <span data-ttu-id="bc742-114">Se o provedor oferecer suporte a notificações de objeto, envie também uma notificação _fnevObjectDeleted_ .</span><span class="sxs-lookup"><span data-stu-id="bc742-114">If your provider supports object notifications, also send an  _fnevObjectDeleted_ notification.</span></span> 
    

