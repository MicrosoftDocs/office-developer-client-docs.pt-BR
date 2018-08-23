---
title: Removendo entradas do catálogo de endereços
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 107ebcd7-b612-4139-b676-c3851f15bc74
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 2c5d7a2114f4a85b9f63cd778e899a83d335ff45
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581276"
---
# <a name="removing-address-book-entries"></a><span data-ttu-id="9cb62-103">Removendo entradas do catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="9cb62-103">Removing address book entries</span></span>
  
<span data-ttu-id="9cb62-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9cb62-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9cb62-105">Método de [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) do seu contêiner é chamado para remover um ou mais destinatários.</span><span class="sxs-lookup"><span data-stu-id="9cb62-105">Your container's [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) method is called to remove one or more recipients.</span></span> <span data-ttu-id="9cb62-106">**DeleteEntries** tem dois parâmetros: uma matriz de identificadores de entrada que representa os destinatários a ser excluído e um valor de flags reservado.</span><span class="sxs-lookup"><span data-stu-id="9cb62-106">**DeleteEntries** has two parameters: an array of entry identifiers representing the recipients to be deleted and a reserved flags value.</span></span> <span data-ttu-id="9cb62-107">Excluir um destinatário afeta o índice de conteúdo de seu contêiner; Além de excluir o destinatário, seu contêiner deve excluir a linha da tabela de conteúdo que representa o destinatário.</span><span class="sxs-lookup"><span data-stu-id="9cb62-107">Deleting a recipient affects the contents table of your container; in addition to deleting the recipient, your container must delete the contents table row that represents the recipient.</span></span> <span data-ttu-id="9cb62-108">Quando a linha foi removida da tabela, seu contêiner deve emitir uma notificação de tabela para cada cliente registrado.</span><span class="sxs-lookup"><span data-stu-id="9cb62-108">When the row has been removed from the table, your container must issue a table notification to each registered client.</span></span> 
  
### <a name="to-implement-iabcontainerdeleteentries"></a><span data-ttu-id="9cb62-109">Para implementar IABContainer::DeleteEntries</span><span class="sxs-lookup"><span data-stu-id="9cb62-109">To implement IABContainer::DeleteEntries</span></span>
  
1. <span data-ttu-id="9cb62-110">Exclua cada destinatário representado pelo identificador de entrada do seu contêiner.</span><span class="sxs-lookup"><span data-stu-id="9cb62-110">Delete each recipient represented by the entry identifier from your container.</span></span>
    
2. <span data-ttu-id="9cb62-111">Se a tabela de conteúdo do seu contêiner estiver aberta:</span><span class="sxs-lookup"><span data-stu-id="9cb62-111">If your container's contents table is open:</span></span>
    
   - <span data-ttu-id="9cb62-112">Envie uma notificação de _fnevTableModified_ com o membro **ulTableEvent** definido como TABLE_ROW_DELETED aos clientes registrados para cada linha da tabela de conteúdo excluído.</span><span class="sxs-lookup"><span data-stu-id="9cb62-112">Send an  _fnevTableModified_ notification with the **ulTableEvent** member set to TABLE_ROW_DELETED to registered clients for each deleted contents table row.</span></span> <span data-ttu-id="9cb62-113">Se seu provedor de usar o utilitário de notificação, chame [IMAPISupport::Notify](imapisupport-notify.md) para enviar essas notificações.</span><span class="sxs-lookup"><span data-stu-id="9cb62-113">If your provider uses the notification utility, call [IMAPISupport::Notify](imapisupport-notify.md) to send these notifications.</span></span> 
    
   - <span data-ttu-id="9cb62-114">Se o provedor oferece suporte a notificações de objeto, também envie uma notificação _fnevObjectDeleted_ .</span><span class="sxs-lookup"><span data-stu-id="9cb62-114">If your provider supports object notifications, also send an  _fnevObjectDeleted_ notification.</span></span> 
    

