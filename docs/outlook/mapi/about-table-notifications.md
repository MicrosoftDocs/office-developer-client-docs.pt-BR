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
ms.openlocfilehash: d6fd49e1a004202e0de02e262f6977ca8a07019d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571938"
---
# <a name="about-table-notifications"></a><span data-ttu-id="71003-103">Sobre as notificações de tabela</span><span class="sxs-lookup"><span data-stu-id="71003-103">About Table Notifications</span></span>

  
  
<span data-ttu-id="71003-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="71003-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="71003-105">Os clientes frequentemente dependem de notificações de tabela para saber das alterações aos objetos em vez de registro para receber notificações diretamente a partir de objetos.</span><span class="sxs-lookup"><span data-stu-id="71003-105">Clients often rely on table notifications to learn of changes to objects instead of registering to receive notifications directly from the objects.</span></span> <span data-ttu-id="71003-106">Alterações comuns que fazer com que as notificações sejam enviadas incluem a adição, exclusão ou modificação de uma linha e quaisquer erros críticos.</span><span class="sxs-lookup"><span data-stu-id="71003-106">Typical changes that cause notifications to be sent include the addition, deletion, or modification of a row and any critical error.</span></span> <span data-ttu-id="71003-107">Quando chegam de notificações, os clientes podem determinar se fazer outra chamada recarregar a tabela.</span><span class="sxs-lookup"><span data-stu-id="71003-107">When notifications arrive, clients can determine whether to make another call to reload the table.</span></span> 
  
<span data-ttu-id="71003-108">Como as notificações de tabela são assíncronas, existem alguns problemas que podem tornar o tratamento de notificações menores direta:</span><span class="sxs-lookup"><span data-stu-id="71003-108">Because table notifications are asynchronous, there are a few issues that can make handling notifications less than straightforward:</span></span>
  
- <span data-ttu-id="71003-109">Os dados passados na estrutura de [TABLE_NOTIFICATION](table_notification.md) podem não representar o estado de mais recente da tabela.</span><span class="sxs-lookup"><span data-stu-id="71003-109">The data passed in the [TABLE_NOTIFICATION](table_notification.md) structure might not represent the table's most current state.</span></span> <span data-ttu-id="71003-110">Por exemplo, um cliente pode fazer uma alteração em uma mensagem e decida excluí-lo.</span><span class="sxs-lookup"><span data-stu-id="71003-110">For example, a client might make a change to a message and then decide to delete it.</span></span> <span data-ttu-id="71003-111">O provedor de armazenamento de mensagem Implementando a tabela de conteúdo que incluem a mensagem envia notificações de duas: um evento TABLE_ROW_MODIFIED seguido de um evento TABLE_ROW_DELETED.</span><span class="sxs-lookup"><span data-stu-id="71003-111">The message store provider implementing the contents table that included the message sends two notifications: a TABLE_ROW_MODIFIED event followed by a TABLE_ROW_DELETED event.</span></span> <span data-ttu-id="71003-112">Dependendo de como o provedor de armazenamento de mensagem tempo notificações, o cliente pode receber a notificação de TABLE_ROW_MODIFIED após a exclusão da linha.</span><span class="sxs-lookup"><span data-stu-id="71003-112">Depending on how the message store provider times notifications, the client might receive the TABLE_ROW_MODIFIED notification after the deletion of the row.</span></span> 
    
- <span data-ttu-id="71003-113">O conjunto incluída com uma notificação de colunas podem ser diferente do conjunto atual de coluna da tabela.</span><span class="sxs-lookup"><span data-stu-id="71003-113">The column set included with a notification might be different from the table's current column set.</span></span> <span data-ttu-id="71003-114">MAPI exige que o conjunto de coluna de notificação corresponder ao conjunto de coluna que estava em vigor no momento em que a notificação foi gerada.</span><span class="sxs-lookup"><span data-stu-id="71003-114">MAPI requires that the notification column set match the column set that was in effect at the time that the notification was generated.</span></span> <span data-ttu-id="71003-115">Porque é possível para um cliente chamar [IMAPITable::SetColumns](imapitable-setcolumns.md) para alterar a coluna definida a qualquer momento — incluindo após uma notificação — os conjuntos de duas colunas não podem ser sincronizados.</span><span class="sxs-lookup"><span data-stu-id="71003-115">Because it is possible for a client to call [IMAPITable::SetColumns](imapitable-setcolumns.md) to alter the column set at any time — including after a notification — the two column sets may not be synchronized.</span></span> 
    
- <span data-ttu-id="71003-116">Notificações da tabela serão enviadas somente para as linhas que fazem parte do modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="71003-116">Table notifications are only sent for rows that are part of the view.</span></span> <span data-ttu-id="71003-117">Ou seja, se uma linha é excluída da exibição devido a uma restrição ou a tabela estiver recolhida, nenhuma notificação será enviada se essa linha for alterado.</span><span class="sxs-lookup"><span data-stu-id="71003-117">That is, if a row is excluded from the view due to a restriction or because the table is in a collapsed state, no notification will be sent if that row changes.</span></span> <span data-ttu-id="71003-118">Além disso, nenhuma notificação é enviadas para informar um cliente sobre uma alteração no estado de categoria.</span><span class="sxs-lookup"><span data-stu-id="71003-118">Also, no notifications are sent to inform a client about a change in category state.</span></span>
    
<span data-ttu-id="71003-119">Clientes devem estar cientes de que nem todas as tabelas suportam a notificação TABLE_SORT_DONE e devem estar preparadas para lidar com essa condição por:</span><span class="sxs-lookup"><span data-stu-id="71003-119">Clients should be aware that not all tables support the TABLE_SORT_DONE notification and should be prepared to handle this condition by:</span></span>
  
1. <span data-ttu-id="71003-120">Forçando a classificação estão sincronizados.</span><span class="sxs-lookup"><span data-stu-id="71003-120">Forcing the sort to be synchronous.</span></span>
    
2. <span data-ttu-id="71003-121">Recarregar as linhas da tabela quando [IMAPITable:: SortTable](imapitable-sorttable.md) retorna.</span><span class="sxs-lookup"><span data-stu-id="71003-121">Reloading the rows of the table when [IMAPITable::SortTable](imapitable-sorttable.md) returns.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="71003-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="71003-122">See also</span></span>



[<span data-ttu-id="71003-123">Tabelas MAPI</span><span class="sxs-lookup"><span data-stu-id="71003-123">MAPI Tables</span></span>](mapi-tables.md)

