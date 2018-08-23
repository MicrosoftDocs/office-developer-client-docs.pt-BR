---
title: Receber mensagens usando provedores do repositório de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4763951e-ccfd-453e-b99c-5c7d5efb90c2
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 8a5df2e8f50d8de05ec43b03ae5b56887e76d505
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590187"
---
# <a name="receiving-messages-by-using-message-store-providers"></a><span data-ttu-id="409d9-103">Receber mensagens usando provedores do repositório de mensagens</span><span class="sxs-lookup"><span data-stu-id="409d9-103">Receiving Messages by Using Message Store Providers</span></span>

  
  
<span data-ttu-id="409d9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="409d9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="409d9-105">Provedores de armazenamento de mensagem não precisa suportar envios de mensagem de entrada (ou seja, oferecem suporte para o repositório provedor de provedores de transporte e o MAPI spooler para usar a mensagem como um ponto de entrega de mensagens).</span><span class="sxs-lookup"><span data-stu-id="409d9-105">Message store providers do not have to support incoming message submissions (that is, support the ability for transport providers and the MAPI spooler to use the message store provider as a delivery point for messages).</span></span> <span data-ttu-id="409d9-106">No entanto, se o seu provedor de armazenamento de mensagens não oferece suporte a envios de mensagem de entrada, ele não pode ser usado como o armazenamento de mensagens padrão.</span><span class="sxs-lookup"><span data-stu-id="409d9-106">However, if your message store provider does not support incoming message submissions, it cannot be used as the default message store.</span></span>
  
<span data-ttu-id="409d9-107">Para oferecer suporte a envios de mensagem de entrada, seu provedor de armazenamento de mensagem deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="409d9-107">To support incoming message submissions, your message store provider must do the following:</span></span>
  
- <span data-ttu-id="409d9-108">Suporte aos métodos [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) e [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) para que aplicativos clientes possam encontrar as mensagens de entrada.</span><span class="sxs-lookup"><span data-stu-id="409d9-108">Support the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) and [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) methods so client applications can find incoming messages.</span></span> 
    
- <span data-ttu-id="409d9-109">Suporte ao método [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) para que o MAPI spooler pode informar o provedor de armazenamento de mensagem que uma nova mensagem chegou.</span><span class="sxs-lookup"><span data-stu-id="409d9-109">Support the [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) method so that the MAPI spooler can inform the message store provider that a new message has arrived.</span></span> 
    
- <span data-ttu-id="409d9-110">Implementar notificações para que os clientes podem se inscrever para fins de notificação de mensagem nova.</span><span class="sxs-lookup"><span data-stu-id="409d9-110">Implement notifications so that clients can register for new message notification.</span></span> <span data-ttu-id="409d9-111">As notificações são opcionais, mas seu provedor deve implementá-las.</span><span class="sxs-lookup"><span data-stu-id="409d9-111">Notifications are optional, but your provider should implement them.</span></span>
    
<span data-ttu-id="409d9-112">A sequência de chamadas de método que ocorre quando uma mensagem de entrada é entregue a um armazenamento de mensagens é da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="409d9-112">The sequence of method calls that occurs when an incoming message is delivered to a message store is as follows:</span></span>
  
1. <span data-ttu-id="409d9-113">O MAPI spooler chama [IMsgStore::OpenEntry](imsgstore-openentry.md) com a caixa de entrada [EntryID](entryid.md) para obter uma interface [IMAPIFolder](imapifolderimapicontainer.md) .</span><span class="sxs-lookup"><span data-stu-id="409d9-113">The MAPI spooler calls [IMsgStore::OpenEntry](imsgstore-openentry.md) with the Inbox [EntryID](entryid.md) to get an [IMAPIFolder](imapifolderimapicontainer.md) interface.</span></span> 
    
2. <span data-ttu-id="409d9-114">O MAPI spooler chama [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) para obter um novo objeto de mensagem.</span><span class="sxs-lookup"><span data-stu-id="409d9-114">The MAPI spooler calls [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) to get a new message object.</span></span> 
    
3. <span data-ttu-id="409d9-115">O MAPI spooler passa o objeto de mensagem para o provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="409d9-115">The MAPI spooler passes the message object to the transport provider.</span></span>
    
4. <span data-ttu-id="409d9-116">O provedor de transporte preenche as propriedades da mensagem com dados de sistema de mensagens subjacente e chama o método de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) do objeto de mensagem.</span><span class="sxs-lookup"><span data-stu-id="409d9-116">The transport provider fills in the message's properties with data from the underlying messaging system and calls the message object's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
    
5. <span data-ttu-id="409d9-117">O provedor de armazenamento de mensagem usa seu método de notificação para informar aos clientes registrados que uma nova mensagem chegou.</span><span class="sxs-lookup"><span data-stu-id="409d9-117">The message store provider uses its notification method to inform registered clients that a new message has arrived.</span></span>
    
6. <span data-ttu-id="409d9-118">O MAPI spooler chama o método de [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) do armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="409d9-118">The MAPI spooler calls the message store's [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) method.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="409d9-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="409d9-119">See also</span></span>



[<span data-ttu-id="409d9-120">Recursos do repositório de mensagens</span><span class="sxs-lookup"><span data-stu-id="409d9-120">Message Store Features</span></span>](message-store-features.md)

