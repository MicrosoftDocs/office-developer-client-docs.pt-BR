---
title: Fornecer notificações para provedores do repositório de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0e1cdba-ceb6-4a3f-8449-79d1a0ad1adf
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 3722893ae57a108b338725e46c975e92c0f8ff72
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587506"
---
# <a name="providing-notifications-for-message-store-providers"></a><span data-ttu-id="639ac-103">Fornecer notificações para provedores do repositório de mensagens</span><span class="sxs-lookup"><span data-stu-id="639ac-103">Providing Notifications for Message Store Providers</span></span>

  
  
<span data-ttu-id="639ac-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="639ac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="639ac-105">Embora as notificações são opcionais, eles são uma parte muito importante de um provedor de armazenamento de mensagem de boas.</span><span class="sxs-lookup"><span data-stu-id="639ac-105">While notifications are optional, they are a very important part of a good message store provider.</span></span> <span data-ttu-id="639ac-106">Aplicativos cliente e o MAPI spooler contam com notificações do provedor de repositório de mensagem para obter um bom desempenho ao enviar mensagens de saída ou o recebimento de mensagens de entrada.</span><span class="sxs-lookup"><span data-stu-id="639ac-106">Client applications and the MAPI spooler rely on notifications from the message store provider to get good performance when submitting outgoing messages or receiving incoming messages.</span></span> <span data-ttu-id="639ac-107">Clientes e o MAPI spooler podem funcionar sem receber notificações do provedor de armazenamento de mensagem, mas não será capazes de informar os usuários das alterações no repositório de mensagem sem eles.</span><span class="sxs-lookup"><span data-stu-id="639ac-107">Clients and the MAPI spooler can function without receiving notifications from the message store provider, but they will not be able to inform users of changes in the message store without them.</span></span> <span data-ttu-id="639ac-108">Normalmente, isso significa que os usuários não poderão ver o que uma nova mensagem chegou até seu cliente Avançar abre o armazenamento de mensagens pasta de recebimento.</span><span class="sxs-lookup"><span data-stu-id="639ac-108">Typically, this means that users will be unable to see that a new message has arrived until their client next opens the message store's receive folder.</span></span>
  
<span data-ttu-id="639ac-109">Os clientes se registrar para notificações chamando o método [IMsgStore::Advise](imsgstore-advise.md) .</span><span class="sxs-lookup"><span data-stu-id="639ac-109">Clients register for notifications by calling the [IMsgStore::Advise](imsgstore-advise.md) method.</span></span> <span data-ttu-id="639ac-110">O cliente passa em uma [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) interface, uma bitmask que indica que tipo de notificações, o cliente está interessado em receber, e uma **EntryID** que indica qual objeto na mensagem de armazenar o **Advise** solicitação se aplica a.</span><span class="sxs-lookup"><span data-stu-id="639ac-110">The client passes in an [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) interface, a bitmask that indicates what type of notifications the client is interested in receiving, and an **EntryID** that indicates which object in the message store the **Advise** request applies to.</span></span> <span data-ttu-id="639ac-111">Quando ocorrem eventos de relevantes no objeto (por exemplo, quando uma nova mensagem chega na pasta de recebimento no repositório de mensagem), o provedor de armazenamento de mensagem ou o próprio objeto deve chamar o método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) para todos os \*\* IMAPIAdviseSink\*\* objetos que foram registrados para esse tipo de evento.</span><span class="sxs-lookup"><span data-stu-id="639ac-111">When relevant events occur in the object (for example, when a new message arrives in the receive folder in the message store), the message store provider or the object itself should call the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for all of the **IMAPIAdviseSink** objects that have registered for that event type.</span></span> 
  
<span data-ttu-id="639ac-112">Mesmo que sua mensagem armazenar o provedor notifica nunca outros componentes MAPI das alterações no armazenamento da mensagem, que ele ainda deve implementar **IMsgStore::Advise** para retornar MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="639ac-112">Even if your message store provider never notifies other MAPI components of changes in the message store, it should still implement **IMsgStore::Advise** to return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="639ac-113">Isso informa que outros componentes para não esperar que o provedor de armazenamento de notificações da mensagem.</span><span class="sxs-lookup"><span data-stu-id="639ac-113">This informs other components not to expect notifications from the message store provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="639ac-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="639ac-114">See also</span></span>



[<span data-ttu-id="639ac-115">Recursos de armazenamento de mensagens</span><span class="sxs-lookup"><span data-stu-id="639ac-115">Message Store Features</span></span>](message-store-features.md)

