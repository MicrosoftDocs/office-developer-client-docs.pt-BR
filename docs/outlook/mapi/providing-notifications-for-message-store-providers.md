---
title: Fornecer notificações para provedores de repositórios de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0e1cdba-ceb6-4a3f-8449-79d1a0ad1adf
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a28e6e6f008517a6b1c2c82dfa391b478963880f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419930"
---
# <a name="providing-notifications-for-message-store-providers"></a><span data-ttu-id="525aa-103">Fornecer notificações para provedores de repositórios de mensagens</span><span class="sxs-lookup"><span data-stu-id="525aa-103">Providing Notifications for Message Store Providers</span></span>

  
  
<span data-ttu-id="525aa-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="525aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="525aa-105">Enquanto as notificações são opcionais, elas são uma parte muito importante de um bom provedor de armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="525aa-105">While notifications are optional, they are a very important part of a good message store provider.</span></span> <span data-ttu-id="525aa-106">Os aplicativos cliente e o spooler MAPI dependem de notificações do provedor de repositórios de mensagens para obter um bom desempenho ao enviar mensagens de saída ou receber mensagens de entrada.</span><span class="sxs-lookup"><span data-stu-id="525aa-106">Client applications and the MAPI spooler rely on notifications from the message store provider to get good performance when submitting outgoing messages or receiving incoming messages.</span></span> <span data-ttu-id="525aa-107">Os clientes e o spooler MAPI podem funcionar sem receber notificações do provedor de armazenamento de mensagens, mas não poderão informar os usuários sobre alterações no repositório de mensagens sem eles.</span><span class="sxs-lookup"><span data-stu-id="525aa-107">Clients and the MAPI spooler can function without receiving notifications from the message store provider, but they will not be able to inform users of changes in the message store without them.</span></span> <span data-ttu-id="525aa-108">Normalmente, isso significa que os usuários não conseguirão ver se uma nova mensagem chegou até que o cliente seguinte Abra a pasta de recebimento do repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="525aa-108">Typically, this means that users will be unable to see that a new message has arrived until their client next opens the message store's receive folder.</span></span>
  
<span data-ttu-id="525aa-109">Os clientes se registram para notificações chamando o método [IMsgStore:: Advise](imsgstore-advise.md) .</span><span class="sxs-lookup"><span data-stu-id="525aa-109">Clients register for notifications by calling the [IMsgStore::Advise](imsgstore-advise.md) method.</span></span> <span data-ttu-id="525aa-110">O cliente passa uma interface [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) , uma bitmask que indica o tipo de notificação que o cliente está interessado em receber e uma **EntryID** que indica qual objeto da mensagem armazena o **aviso** a solicitação se aplica ao.</span><span class="sxs-lookup"><span data-stu-id="525aa-110">The client passes in an [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) interface, a bitmask that indicates what type of notifications the client is interested in receiving, and an **EntryID** that indicates which object in the message store the **Advise** request applies to.</span></span> <span data-ttu-id="525aa-111">Quando eventos relevantes ocorrem no objeto (por exemplo, quando uma nova mensagem chega na pasta receber no repositório de mensagens), o provedor de armazenamento de mensagens ou o próprio objeto deve chamar o método [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) para todos os \*\* Objetos IMAPIAdviseSink\*\* registrados para esse tipo de evento.</span><span class="sxs-lookup"><span data-stu-id="525aa-111">When relevant events occur in the object (for example, when a new message arrives in the receive folder in the message store), the message store provider or the object itself should call the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for all of the **IMAPIAdviseSink** objects that have registered for that event type.</span></span> 
  
<span data-ttu-id="525aa-112">Mesmo que seu provedor de repositório de mensagens nunca notifique outros componentes MAPI de alterações no repositório de mensagens, ele ainda deve implementar **IMsgStore:: Advise** para retornar MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="525aa-112">Even if your message store provider never notifies other MAPI components of changes in the message store, it should still implement **IMsgStore::Advise** to return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="525aa-113">Isso informa outros componentes para não esperar notificações do provedor de armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="525aa-113">This informs other components not to expect notifications from the message store provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="525aa-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="525aa-114">See also</span></span>



[<span data-ttu-id="525aa-115">Recursos do repositório de mensagens</span><span class="sxs-lookup"><span data-stu-id="525aa-115">Message Store Features</span></span>](message-store-features.md)

