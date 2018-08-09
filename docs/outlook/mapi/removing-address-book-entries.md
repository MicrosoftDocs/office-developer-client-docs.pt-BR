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
ms.openlocfilehash: 1fb7224e110bbee6844cf2820782aac8be213ba3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770225"
---
# <a name="removing-address-book-entries"></a><span data-ttu-id="760ee-103">Removendo entradas do catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="760ee-103">Removing address book entries</span></span>
  
<span data-ttu-id="760ee-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="760ee-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="760ee-105">Método de [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) do seu contêiner é chamado para remover um ou mais destinatários.</span><span class="sxs-lookup"><span data-stu-id="760ee-105">Your container's [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) method is called to remove one or more recipients.</span></span> <span data-ttu-id="760ee-106">**DeleteEntries** tem dois parâmetros: uma matriz de identificadores de entrada que representa os destinatários a ser excluído e um valor de flags reservado.</span><span class="sxs-lookup"><span data-stu-id="760ee-106">**DeleteEntries** has two parameters: an array of entry identifiers representing the recipients to be deleted and a reserved flags value.</span></span> <span data-ttu-id="760ee-107">Excluir um destinatário afeta o índice de conteúdo de seu contêiner; Além de excluir o destinatário, seu contêiner deve excluir a linha da tabela de conteúdo que representa o destinatário.</span><span class="sxs-lookup"><span data-stu-id="760ee-107">Deleting a recipient affects the contents table of your container; in addition to deleting the recipient, your container must delete the contents table row that represents the recipient.</span></span> <span data-ttu-id="760ee-108">Quando a linha foi removida da tabela, seu contêiner deve emitir uma notificação de tabela para cada cliente registrado.</span><span class="sxs-lookup"><span data-stu-id="760ee-108">When the row has been removed from the table, your container must issue a table notification to each registered client.</span></span> 
  
### <a name="to-implement-iabcontainerdeleteentries"></a><span data-ttu-id="760ee-109">Para implementar IABContainer::DeleteEntries</span><span class="sxs-lookup"><span data-stu-id="760ee-109">To implement IABContainer::DeleteEntries</span></span>
  
1. <span data-ttu-id="760ee-110">Exclua cada destinatário representado pelo identificador de entrada do seu contêiner.</span><span class="sxs-lookup"><span data-stu-id="760ee-110">Delete each recipient represented by the entry identifier from your container.</span></span>
    
2. <span data-ttu-id="760ee-111">Se a tabela de conteúdo do seu contêiner estiver aberta:</span><span class="sxs-lookup"><span data-stu-id="760ee-111">If your container's contents table is open:</span></span>
    
   - <span data-ttu-id="760ee-112">Envie uma notificação de _fnevTableModified_ com o membro **ulTableEvent** definido como TABLE_ROW_DELETED aos clientes registrados para cada linha da tabela de conteúdo excluído.</span><span class="sxs-lookup"><span data-stu-id="760ee-112">Send an  _fnevTableModified_ notification with the **ulTableEvent** member set to TABLE_ROW_DELETED to registered clients for each deleted contents table row.</span></span> <span data-ttu-id="760ee-113">Se seu provedor de usar o utilitário de notificação, chame [IMAPISupport::Notify](imapisupport-notify.md) para enviar essas notificações.</span><span class="sxs-lookup"><span data-stu-id="760ee-113">If your provider uses the notification utility, call [IMAPISupport::Notify](imapisupport-notify.md) to send these notifications.</span></span> 
    
   - <span data-ttu-id="760ee-114">Se o provedor oferece suporte a notificações de objeto, também envie uma notificação _fnevObjectDeleted_ .</span><span class="sxs-lookup"><span data-stu-id="760ee-114">If your provider supports object notifications, also send an  _fnevObjectDeleted_ notification.</span></span> 
    

