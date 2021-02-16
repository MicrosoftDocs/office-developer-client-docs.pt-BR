---
title: Sobre notificações de tabela
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 00c9c6c2-fc21-4b9c-91fa-629450a22d37
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 9a42ed1e196e8ac498ab5889b4419ff407db4748
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417949"
---
# <a name="about-table-notifications"></a><span data-ttu-id="8ff40-103">Sobre notificações de tabela</span><span class="sxs-lookup"><span data-stu-id="8ff40-103">About Table Notifications</span></span>

  
  
<span data-ttu-id="8ff40-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8ff40-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8ff40-105">Os clientes geralmente dependem de notificações de tabela para aprender sobre alterações em objetos em vez de se registrar para receber notificações diretamente dos objetos.</span><span class="sxs-lookup"><span data-stu-id="8ff40-105">Clients often rely on table notifications to learn of changes to objects instead of registering to receive notifications directly from the objects.</span></span> <span data-ttu-id="8ff40-106">As alterações típicas que causam o enviar notificações incluem a adição, exclusão ou modificação de uma linha e qualquer erro crítico.</span><span class="sxs-lookup"><span data-stu-id="8ff40-106">Typical changes that cause notifications to be sent include the addition, deletion, or modification of a row and any critical error.</span></span> <span data-ttu-id="8ff40-107">Quando as notificações chegam, os clientes podem determinar se devem fazer outra chamada para recarregar a tabela.</span><span class="sxs-lookup"><span data-stu-id="8ff40-107">When notifications arrive, clients can determine whether to make another call to reload the table.</span></span> 
  
<span data-ttu-id="8ff40-108">Como as notificações de tabela são assíncronas, há alguns problemas que podem tornar o tratamento de notificações menos simples:</span><span class="sxs-lookup"><span data-stu-id="8ff40-108">Because table notifications are asynchronous, there are a few issues that can make handling notifications less than straightforward:</span></span>
  
- <span data-ttu-id="8ff40-109">Os dados passados [na TABLE_NOTIFICATION](table_notification.md) estrutura podem não representar o estado mais atual da tabela.</span><span class="sxs-lookup"><span data-stu-id="8ff40-109">The data passed in the [TABLE_NOTIFICATION](table_notification.md) structure might not represent the table's most current state.</span></span> <span data-ttu-id="8ff40-110">Por exemplo, um cliente pode fazer uma alteração em uma mensagem e decidir excluí-la.</span><span class="sxs-lookup"><span data-stu-id="8ff40-110">For example, a client might make a change to a message and then decide to delete it.</span></span> <span data-ttu-id="8ff40-111">O provedor de armazenamento de mensagens que implementa o índice de conteúdo que incluiu a mensagem envia duas notificações: um evento de TABLE_ROW_MODIFIED seguido por um TABLE_ROW_DELETED evento.</span><span class="sxs-lookup"><span data-stu-id="8ff40-111">The message store provider implementing the contents table that included the message sends two notifications: a TABLE_ROW_MODIFIED event followed by a TABLE_ROW_DELETED event.</span></span> <span data-ttu-id="8ff40-112">Dependendo de como o provedor de armazenamento de mensagens tempo notificações, o cliente pode receber a notificação de TABLE_ROW_MODIFIED após a exclusão da linha.</span><span class="sxs-lookup"><span data-stu-id="8ff40-112">Depending on how the message store provider times notifications, the client might receive the TABLE_ROW_MODIFIED notification after the deletion of the row.</span></span> 
    
- <span data-ttu-id="8ff40-113">O conjunto de colunas incluído em uma notificação pode ser diferente do conjunto de colunas atual da tabela.</span><span class="sxs-lookup"><span data-stu-id="8ff40-113">The column set included with a notification might be different from the table's current column set.</span></span> <span data-ttu-id="8ff40-114">MAPI requires that the notification column set match the column set that was in effect at the time that the notification was generated.</span><span class="sxs-lookup"><span data-stu-id="8ff40-114">MAPI requires that the notification column set match the column set that was in effect at the time that the notification was generated.</span></span> <span data-ttu-id="8ff40-115">Como é possível que um cliente chame [IMAPITable::SetColumns](imapitable-setcolumns.md) para alterar o conjunto de colunas a qualquer momento — incluindo após uma notificação — os dois conjuntos de colunas podem não ser sincronizados.</span><span class="sxs-lookup"><span data-stu-id="8ff40-115">Because it is possible for a client to call [IMAPITable::SetColumns](imapitable-setcolumns.md) to alter the column set at any time — including after a notification — the two column sets may not be synchronized.</span></span> 
    
- <span data-ttu-id="8ff40-116">As notificações de tabela são enviadas apenas para linhas que fazem parte do exibição.</span><span class="sxs-lookup"><span data-stu-id="8ff40-116">Table notifications are only sent for rows that are part of the view.</span></span> <span data-ttu-id="8ff40-117">Ou seja, se uma linha for excluída da exibição devido a uma restrição ou porque a tabela está em um estado recolhido, nenhuma notificação será enviada se essa linha for mudada.</span><span class="sxs-lookup"><span data-stu-id="8ff40-117">That is, if a row is excluded from the view due to a restriction or because the table is in a collapsed state, no notification will be sent if that row changes.</span></span> <span data-ttu-id="8ff40-118">Além disso, nenhuma notificação é enviada para informar um cliente sobre uma alteração no estado da categoria.</span><span class="sxs-lookup"><span data-stu-id="8ff40-118">Also, no notifications are sent to inform a client about a change in category state.</span></span>
    
<span data-ttu-id="8ff40-119">Os clientes devem estar cientes de que nem todas as tabelas suportam a notificação TABLE_SORT_DONE e devem estar preparados para lidar com essa condição ao:</span><span class="sxs-lookup"><span data-stu-id="8ff40-119">Clients should be aware that not all tables support the TABLE_SORT_DONE notification and should be prepared to handle this condition by:</span></span>
  
1. <span data-ttu-id="8ff40-120">Forçar a classificação a ser síncrona.</span><span class="sxs-lookup"><span data-stu-id="8ff40-120">Forcing the sort to be synchronous.</span></span>
    
2. <span data-ttu-id="8ff40-121">Recarregando as linhas da tabela quando [IMAPITable::SortTable retorna.](imapitable-sorttable.md)</span><span class="sxs-lookup"><span data-stu-id="8ff40-121">Reloading the rows of the table when [IMAPITable::SortTable](imapitable-sorttable.md) returns.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="8ff40-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="8ff40-122">See also</span></span>



[<span data-ttu-id="8ff40-123">Tabelas MAPI</span><span class="sxs-lookup"><span data-stu-id="8ff40-123">MAPI Tables</span></span>](mapi-tables.md)

