---
title: Recebendo mensagens usando provedores de repositórios de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4763951e-ccfd-453e-b99c-5c7d5efb90c2
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: c93a4b56489c2bfb458e2e1cd872073e64d9998a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328445"
---
# <a name="receiving-messages-by-using-message-store-providers"></a><span data-ttu-id="df9ab-103">Recebendo mensagens usando provedores de repositórios de mensagens</span><span class="sxs-lookup"><span data-stu-id="df9ab-103">Receiving Messages by Using Message Store Providers</span></span>

  
  
<span data-ttu-id="df9ab-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="df9ab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="df9ab-105">Os provedores de repositórios de mensagens não precisam suportar envios de mensagens de entrada (ou seja, oferecem suporte à capacidade de provedores de transporte e ao spooler MAPI para usar o provedor de armazenamento de mensagens como um ponto de entrega para mensagens).</span><span class="sxs-lookup"><span data-stu-id="df9ab-105">Message store providers do not have to support incoming message submissions (that is, support the ability for transport providers and the MAPI spooler to use the message store provider as a delivery point for messages).</span></span> <span data-ttu-id="df9ab-106">No enTanto, se o seu provedor de repositório de mensagens não oferecer suporte a envios de mensagens de entrada, ele não poderá ser usado como o repositório de mensagens padrão.</span><span class="sxs-lookup"><span data-stu-id="df9ab-106">However, if your message store provider does not support incoming message submissions, it cannot be used as the default message store.</span></span>
  
<span data-ttu-id="df9ab-107">Para dar suporte a envios de mensagens de entrada, seu provedor de repositório de mensagens deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="df9ab-107">To support incoming message submissions, your message store provider must do the following:</span></span>
  
- <span data-ttu-id="df9ab-108">Suporte para os métodos [IMsgStore:: GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) e [IMsgStore:: GetReceiveFolder](imsgstore-getreceivefolder.md) para que os aplicativos clientes possam encontrar mensagens de entrada.</span><span class="sxs-lookup"><span data-stu-id="df9ab-108">Support the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) and [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) methods so client applications can find incoming messages.</span></span> 
    
- <span data-ttu-id="df9ab-109">Suporta o método [IMsgStore:: NotifyNewMail](imsgstore-notifynewmail.md) para que o spooler MAPI possa informar ao provedor de repositório de mensagens que uma nova mensagem chegou.</span><span class="sxs-lookup"><span data-stu-id="df9ab-109">Support the [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) method so that the MAPI spooler can inform the message store provider that a new message has arrived.</span></span> 
    
- <span data-ttu-id="df9ab-110">Implementar notificações para que os clientes possam se registrar para notificação de nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="df9ab-110">Implement notifications so that clients can register for new message notification.</span></span> <span data-ttu-id="df9ab-111">As notificações são opcionais, mas o provedor deve implementá-las.</span><span class="sxs-lookup"><span data-stu-id="df9ab-111">Notifications are optional, but your provider should implement them.</span></span>
    
<span data-ttu-id="df9ab-112">A sequência de chamadas de método que ocorre quando uma mensagem de entrada é entregue a um repositório de mensagens é da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="df9ab-112">The sequence of method calls that occurs when an incoming message is delivered to a message store is as follows:</span></span>
  
1. <span data-ttu-id="df9ab-113">O spooler MAPI chama [IMsgStore:: OpenEntry](imsgstore-openentry.md) com a EntryID [](entryid.md) da caixa de entrada para obter uma interface [IMAPIFolder](imapifolderimapicontainer.md) .</span><span class="sxs-lookup"><span data-stu-id="df9ab-113">The MAPI spooler calls [IMsgStore::OpenEntry](imsgstore-openentry.md) with the Inbox [EntryID](entryid.md) to get an [IMAPIFolder](imapifolderimapicontainer.md) interface.</span></span> 
    
2. <span data-ttu-id="df9ab-114">O spooler MAPI chama [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) para obter um novo objeto Message.</span><span class="sxs-lookup"><span data-stu-id="df9ab-114">The MAPI spooler calls [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) to get a new message object.</span></span> 
    
3. <span data-ttu-id="df9ab-115">O spooler MAPI transmite o objeto Message para o provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="df9ab-115">The MAPI spooler passes the message object to the transport provider.</span></span>
    
4. <span data-ttu-id="df9ab-116">O provedor de transporte preenche as propriedades da mensagem com dados do sistema de mensagens subjacente e chama o método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) do objeto Message.</span><span class="sxs-lookup"><span data-stu-id="df9ab-116">The transport provider fills in the message's properties with data from the underlying messaging system and calls the message object's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
    
5. <span data-ttu-id="df9ab-117">O provedor de repositório de mensagens usa seu método de notificação para informar aos clientes registrados que uma nova mensagem chegou.</span><span class="sxs-lookup"><span data-stu-id="df9ab-117">The message store provider uses its notification method to inform registered clients that a new message has arrived.</span></span>
    
6. <span data-ttu-id="df9ab-118">O spooler MAPI chama o método [IMsgStore:: NotifyNewMail](imsgstore-notifynewmail.md) do repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="df9ab-118">The MAPI spooler calls the message store's [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) method.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="df9ab-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="df9ab-119">See also</span></span>



[<span data-ttu-id="df9ab-120">Recursos do repositório de mensagens</span><span class="sxs-lookup"><span data-stu-id="df9ab-120">Message Store Features</span></span>](message-store-features.md)

