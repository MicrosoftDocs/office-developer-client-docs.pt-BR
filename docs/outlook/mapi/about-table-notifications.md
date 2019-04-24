---
title: Sobre as notificações de tabela
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 00c9c6c2-fc21-4b9c-91fa-629450a22d37
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 9a42ed1e196e8ac498ab5889b4419ff407db4748
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321837"
---
# <a name="about-table-notifications"></a><span data-ttu-id="c3e47-103">Sobre as notificações de tabela</span><span class="sxs-lookup"><span data-stu-id="c3e47-103">About Table Notifications</span></span>

  
  
<span data-ttu-id="c3e47-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c3e47-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c3e47-105">Os clientes freqüentemente dependem de notificações de tabela para aprender as alterações nos objetos em vez de se registrarem para receber notificações diretamente dos objetos.</span><span class="sxs-lookup"><span data-stu-id="c3e47-105">Clients often rely on table notifications to learn of changes to objects instead of registering to receive notifications directly from the objects.</span></span> <span data-ttu-id="c3e47-106">As alterações típicas que fazem com que as notificações sejam enviadas incluem adição, exclusão ou modificação de uma linha e qualquer erro crítico.</span><span class="sxs-lookup"><span data-stu-id="c3e47-106">Typical changes that cause notifications to be sent include the addition, deletion, or modification of a row and any critical error.</span></span> <span data-ttu-id="c3e47-107">Quando as notificações chegam, os clientes podem determinar se deseja fazer outra chamada para recarregar a tabela.</span><span class="sxs-lookup"><span data-stu-id="c3e47-107">When notifications arrive, clients can determine whether to make another call to reload the table.</span></span> 
  
<span data-ttu-id="c3e47-108">Como as notificações de tabela são assíncronas, há alguns problemas que podem tornar as notificações de tratamento menores do que o simples:</span><span class="sxs-lookup"><span data-stu-id="c3e47-108">Because table notifications are asynchronous, there are a few issues that can make handling notifications less than straightforward:</span></span>
  
- <span data-ttu-id="c3e47-109">Os dados passados na estrutura [TABLE_NOTIFICATION](table_notification.md) podem não representar o estado mais atual da tabela.</span><span class="sxs-lookup"><span data-stu-id="c3e47-109">The data passed in the [TABLE_NOTIFICATION](table_notification.md) structure might not represent the table's most current state.</span></span> <span data-ttu-id="c3e47-110">Por exemplo, um cliente pode fazer uma alteração em uma mensagem e, em seguida, decidir excluí-la.</span><span class="sxs-lookup"><span data-stu-id="c3e47-110">For example, a client might make a change to a message and then decide to delete it.</span></span> <span data-ttu-id="c3e47-111">O provedor de repositório de mensagens que está implementando a tabela de conteúdo que incluía a mensagem envia duas notificações: um evento TABLE_ROW_MODIFIED seguido por um evento TABLE_ROW_DELETED.</span><span class="sxs-lookup"><span data-stu-id="c3e47-111">The message store provider implementing the contents table that included the message sends two notifications: a TABLE_ROW_MODIFIED event followed by a TABLE_ROW_DELETED event.</span></span> <span data-ttu-id="c3e47-112">Dependendo de como o provedor do repositório de mensagens expira as notificações, o cliente pode receber a notificação TABLE_ROW_MODIFIED após a exclusão da linha.</span><span class="sxs-lookup"><span data-stu-id="c3e47-112">Depending on how the message store provider times notifications, the client might receive the TABLE_ROW_MODIFIED notification after the deletion of the row.</span></span> 
    
- <span data-ttu-id="c3e47-113">O conjunto de colunas incluído com uma notificação pode ser diferente do conjunto de colunas atual da tabela.</span><span class="sxs-lookup"><span data-stu-id="c3e47-113">The column set included with a notification might be different from the table's current column set.</span></span> <span data-ttu-id="c3e47-114">MAPI exige que o conjunto de colunas de notificação coincida com o conjunto de colunas que estava em vigor no momento em que a notificação foi gerada.</span><span class="sxs-lookup"><span data-stu-id="c3e47-114">MAPI requires that the notification column set match the column set that was in effect at the time that the notification was generated.</span></span> <span data-ttu-id="c3e47-115">Como é possível para um cliente chamar imApitable [::](imapitable-setcolumns.md) SetColumns para alterar o conjunto de colunas a qualquer momento, incluindo após uma notificação, os dois conjuntos de colunas podem não ser sincronizados.</span><span class="sxs-lookup"><span data-stu-id="c3e47-115">Because it is possible for a client to call [IMAPITable::SetColumns](imapitable-setcolumns.md) to alter the column set at any time — including after a notification — the two column sets may not be synchronized.</span></span> 
    
- <span data-ttu-id="c3e47-116">As notificações de tabela são enviadas somente para as linhas que fazem parte do modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="c3e47-116">Table notifications are only sent for rows that are part of the view.</span></span> <span data-ttu-id="c3e47-117">Ou seja, se uma linha for excluída do modo de exibição devido a uma restrição ou porque a tabela está em um estado recolhido, nenhuma notificação será enviada se essa linha for alterada.</span><span class="sxs-lookup"><span data-stu-id="c3e47-117">That is, if a row is excluded from the view due to a restriction or because the table is in a collapsed state, no notification will be sent if that row changes.</span></span> <span data-ttu-id="c3e47-118">Além disso, nenhuma notificação é enviada para informar um cliente sobre uma alteração no estado de categoria.</span><span class="sxs-lookup"><span data-stu-id="c3e47-118">Also, no notifications are sent to inform a client about a change in category state.</span></span>
    
<span data-ttu-id="c3e47-119">Os clientes devem estar cientes de que nem todas as tabelas oferecem suporte à notificação TABLE_SORT_DONE e devem estar preparados para lidar com essa condição:</span><span class="sxs-lookup"><span data-stu-id="c3e47-119">Clients should be aware that not all tables support the TABLE_SORT_DONE notification and should be prepared to handle this condition by:</span></span>
  
1. <span data-ttu-id="c3e47-120">Forçar a classificação a ser síncrona.</span><span class="sxs-lookup"><span data-stu-id="c3e47-120">Forcing the sort to be synchronous.</span></span>
    
2. <span data-ttu-id="c3e47-121">Recarregar as linhas da tabela quando imApitable [:: SortTable](imapitable-sorttable.md) retorna.</span><span class="sxs-lookup"><span data-stu-id="c3e47-121">Reloading the rows of the table when [IMAPITable::SortTable](imapitable-sorttable.md) returns.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="c3e47-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3e47-122">See also</span></span>



[<span data-ttu-id="c3e47-123">Tabelas MAPI</span><span class="sxs-lookup"><span data-stu-id="c3e47-123">MAPI Tables</span></span>](mapi-tables.md)

