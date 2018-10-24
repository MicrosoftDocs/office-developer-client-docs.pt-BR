---
title: Manipular notificações
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 451b71da-a888-4d8f-9814-12f9f846de05
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 4c19e88ac1cfb29a9841ec78516410e23b3e5403
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567577"
---
# <a name="handling-notifications"></a><span data-ttu-id="16668-103">Manipular notificações</span><span class="sxs-lookup"><span data-stu-id="16668-103">Handling notifications</span></span>

<span data-ttu-id="16668-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="16668-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="16668-105">Notificações de habilitar um objeto para informar outro objeto que ele passou por uma alteração.</span><span class="sxs-lookup"><span data-stu-id="16668-105">Notifications enable one object to inform another object that it has undergone a change.</span></span> <span data-ttu-id="16668-106">O tipo de alteração é conhecido como um evento.</span><span class="sxs-lookup"><span data-stu-id="16668-106">The type of change is referred to as an event.</span></span> <span data-ttu-id="16668-107">MAPI define vários eventos para o qual as notificações são geradas.</span><span class="sxs-lookup"><span data-stu-id="16668-107">MAPI defines several events for which notifications are generated.</span></span> 
  
<span data-ttu-id="16668-108">Clientes geralmente registrar para um ou mais eventos com um ou mais objetos.</span><span class="sxs-lookup"><span data-stu-id="16668-108">Clients typically register for one or more events with one or more objects.</span></span> <span data-ttu-id="16668-109">Esses objetos são conhecidos como fontes de aviso.</span><span class="sxs-lookup"><span data-stu-id="16668-109">These objects are referred to as advise sources.</span></span> <span data-ttu-id="16668-110">Os objetos que podem atuar como fontes de aviso incluem o objeto de sessão, sob o controle do MAPI ou um objeto criado por um provedor de serviço, como uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="16668-110">Objects that can act as advise sources include the session object, under MAPI's control, or an object created by a service provider, such as a message.</span></span> <span data-ttu-id="16668-111">O objeto informado, conhecido como o coletor de advise, contém qualquer uma implementação do [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) interface ou o [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) interface e está contido em um aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="16668-111">The informed object, referred to as the advise sink, contains either an implementation of the [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) interface or the [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) interface and is within a client application.</span></span> 
  
<span data-ttu-id="16668-112">Objetos de origem Advise implementam um método **Advise** , que é chamado pelos clientes para registrar para notificações e um método **Unadvise** , que é chamado para cancelar um registro.</span><span class="sxs-lookup"><span data-stu-id="16668-112">Advise source objects implement an **Advise** method, which is called by clients to register for notifications, and an **Unadvise** method, which is called to cancel a registration.</span></span> <span data-ttu-id="16668-113">Um dos parâmetros para **Advise** é um ponteiro para uma implementação do **IMAPIAdviseSink** ou \* \* IMAPIViewAdviseSink \* \*.</span><span class="sxs-lookup"><span data-stu-id="16668-113">One of the parameters to **Advise** is a pointer to an implementation of **IMAPIAdviseSink** or \*\* IMAPIViewAdviseSink \*\*.</span></span> <span data-ttu-id="16668-114">A fonte de advise caches esse ponteiro para que ele possa chamar [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) ou um dos métodos em **IMAPIViewAdviseSink** quando ocorre uma alteração.</span><span class="sxs-lookup"><span data-stu-id="16668-114">The advise source caches this pointer so that it can call [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) or one of the methods in **IMAPIViewAdviseSink** when a change occurs.</span></span> 
  
<span data-ttu-id="16668-115">Como receber notificações permite aos usuários exibir as informações mais atualizadas, é recomendável que todos os clientes se registrar e manipular notificações.</span><span class="sxs-lookup"><span data-stu-id="16668-115">Because receiving notifications enables users to view the most up-to-date information, it is recommended that all clients register for and handle notifications.</span></span> <span data-ttu-id="16668-116">No entanto, é opcional.</span><span class="sxs-lookup"><span data-stu-id="16668-116">However, it is optional.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="16668-117">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="16668-117">In this section</span></span>

- <span data-ttu-id="16668-118">[Registrando uma notificação](registering-for-a-notification.md): descreve como registrar um cliente para notificações como parte do seu processo de inicialização.</span><span class="sxs-lookup"><span data-stu-id="16668-118">[Registering for a Notification](registering-for-a-notification.md): Describes how to register a client for notifications as a part of its initialization process.</span></span>
    
- <span data-ttu-id="16668-119">[Cancelamento de uma notificação](canceling-a-notification.md): descreve como cancelar uma assinatura para uma notificação.</span><span class="sxs-lookup"><span data-stu-id="16668-119">[Canceling a Notification](canceling-a-notification.md): Describes how to cancel a subscription to a notification.</span></span>
    
- <span data-ttu-id="16668-120">[Notificação de armazenar de mensagem manipulação](handling-message-store-notification.md): descreve como registrar para notificações do repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="16668-120">[Handling Message Store Notification](handling-message-store-notification.md): Describes how to register for message store notifications.</span></span>
    
- <span data-ttu-id="16668-121">[Notificação de catálogo de endereço de manusear](handing-address-book-notification.md): descreve como se registrar e manipular notificações de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="16668-121">[Handing Address Book Notification](handing-address-book-notification.md): Describes how to register for and handle address book notifications.</span></span>
    
- <span data-ttu-id="16668-122">[Notificação de tabela manipulação](handling-table-notification.md): descreve como registrar para notificações da tabela de hierarquia.</span><span class="sxs-lookup"><span data-stu-id="16668-122">[Handling Table Notification](handling-table-notification.md): Describes how to register for notifications from the hierarchy table.</span></span>
    
- <span data-ttu-id="16668-123">[Implementação de um objeto de coletor de eventos de aviso](implementing-an-advise-sink-object.md): descreve como implementar um objeto de coletor de eventos advise.</span><span class="sxs-lookup"><span data-stu-id="16668-123">[Implementing an Advise Sink Object](implementing-an-advise-sink-object.md): Describes how to implement an advise sink object.</span></span>
    
- <span data-ttu-id="16668-124">[Uma notificação de intervalos](timing-a-notification.md): descreve a temporização da notificação de cliente por provedores de serviços.</span><span class="sxs-lookup"><span data-stu-id="16668-124">[Timing a Notification](timing-a-notification.md): Describes the timing of client notification by service providers.</span></span>
    
- <span data-ttu-id="16668-125">[Garantindo que uma notificação de Thread-Safe](ensuring-a-thread-safe-notification.md): descreve como garantir a notificação de thread-safe com MAPI.</span><span class="sxs-lookup"><span data-stu-id="16668-125">[Ensuring a Thread-Safe Notification](ensuring-a-thread-safe-notification.md): Describes how to ensure thread-safe notification with MAPI.</span></span>
    
- <span data-ttu-id="16668-126">[Forçar uma notificação](forcing-a-notification.md): descreve como forçar uma notificação de MAPI.</span><span class="sxs-lookup"><span data-stu-id="16668-126">[Forcing a Notification](forcing-a-notification.md): Describes how to force a notification in MAPI.</span></span>
    

