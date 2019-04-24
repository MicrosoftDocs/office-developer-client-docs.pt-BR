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
ms.openlocfilehash: e261b71a8e94d9db3b1b17168d84798dfe18955d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299381"
---
# <a name="handling-notifications"></a><span data-ttu-id="ea32e-103">Manipular notificações</span><span class="sxs-lookup"><span data-stu-id="ea32e-103">Handling notifications</span></span>

<span data-ttu-id="ea32e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ea32e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ea32e-105">As notificações permitem que um objeto informe a outro objeto que passou por uma alteração.</span><span class="sxs-lookup"><span data-stu-id="ea32e-105">Notifications enable one object to inform another object that it has undergone a change.</span></span> <span data-ttu-id="ea32e-106">O tipo de alteração é conhecido como um evento.</span><span class="sxs-lookup"><span data-stu-id="ea32e-106">The type of change is referred to as an event.</span></span> <span data-ttu-id="ea32e-107">O MAPI define vários eventos para os quais as notificações são geradas.</span><span class="sxs-lookup"><span data-stu-id="ea32e-107">MAPI defines several events for which notifications are generated.</span></span> 
  
<span data-ttu-id="ea32e-108">Os clientes normalmente se registram em um ou mais eventos com um ou mais objetos.</span><span class="sxs-lookup"><span data-stu-id="ea32e-108">Clients typically register for one or more events with one or more objects.</span></span> <span data-ttu-id="ea32e-109">Esses objetos são chamados de fontes de aviso.</span><span class="sxs-lookup"><span data-stu-id="ea32e-109">These objects are referred to as advise sources.</span></span> <span data-ttu-id="ea32e-110">Os objetos que podem atuar como fontes de aviso incluem o objeto Session, no controle MAPI ou um objeto criado por um provedor de serviços, como uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="ea32e-110">Objects that can act as advise sources include the session object, under MAPI's control, or an object created by a service provider, such as a message.</span></span> <span data-ttu-id="ea32e-111">O objeto informado, chamado de coletor de aviso, contém uma implementação da interface [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) ou da interface [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) e está dentro de um aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="ea32e-111">The informed object, referred to as the advise sink, contains either an implementation of the [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) interface or the [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) interface and is within a client application.</span></span> 
  
<span data-ttu-id="ea32e-112">Avisar os objetos de origem implementam um método **Advise** , que é chamado por clientes para se registrarem para notificações, e um método **Unadvise** , que é chamado para cancelar um registro.</span><span class="sxs-lookup"><span data-stu-id="ea32e-112">Advise source objects implement an **Advise** method, which is called by clients to register for notifications, and an **Unadvise** method, which is called to cancel a registration.</span></span> <span data-ttu-id="ea32e-113">Um dos parâmetros a serem **aconselhados** é um ponteiro para uma implementação de **IMAPIAdviseSink** ou \* \* IMAPIViewAdviseSink \* \*.</span><span class="sxs-lookup"><span data-stu-id="ea32e-113">One of the parameters to **Advise** is a pointer to an implementation of **IMAPIAdviseSink** or \*\* IMAPIViewAdviseSink \*\*.</span></span> <span data-ttu-id="ea32e-114">A fonte de aviso armazena esse ponteiro para que ele possa chamar [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) ou um dos métodos no **IMAPIViewAdviseSink** quando ocorre uma alteração.</span><span class="sxs-lookup"><span data-stu-id="ea32e-114">The advise source caches this pointer so that it can call [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) or one of the methods in **IMAPIViewAdviseSink** when a change occurs.</span></span> 
  
<span data-ttu-id="ea32e-115">Como as notificações de recebimento permitem que os usuários vejam as informações mais atualizadas, é recomendável que todos os clientes registrem e manipulem notificações.</span><span class="sxs-lookup"><span data-stu-id="ea32e-115">Because receiving notifications enables users to view the most up-to-date information, it is recommended that all clients register for and handle notifications.</span></span> <span data-ttu-id="ea32e-116">No enTanto, é opcional.</span><span class="sxs-lookup"><span data-stu-id="ea32e-116">However, it is optional.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="ea32e-117">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="ea32e-117">In this section</span></span>

- <span data-ttu-id="ea32e-118">[Registro de uma notificação](registering-for-a-notification.md): descreve como registrar um cliente para notificações como parte do processo de inicialização.</span><span class="sxs-lookup"><span data-stu-id="ea32e-118">[Registering for a Notification](registering-for-a-notification.md): Describes how to register a client for notifications as a part of its initialization process.</span></span>
    
- <span data-ttu-id="ea32e-119">[Cancelar uma notificação](canceling-a-notification.md): descreve como cancelar uma assinatura para uma notificação.</span><span class="sxs-lookup"><span data-stu-id="ea32e-119">[Canceling a Notification](canceling-a-notification.md): Describes how to cancel a subscription to a notification.</span></span>
    
- <span data-ttu-id="ea32e-120">[Tratamento de notificação do repositório de mensagens](handling-message-store-notification.md): descreve como se registrar para notificações de repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="ea32e-120">[Handling Message Store Notification](handling-message-store-notification.md): Describes how to register for message store notifications.</span></span>
    
- <span data-ttu-id="ea32e-121">[Envio da notificação do catálogo de endereços](handing-address-book-notification.md): descreve como registrar e lidar com notificações do catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="ea32e-121">[Handing Address Book Notification](handing-address-book-notification.md): Describes how to register for and handle address book notifications.</span></span>
    
- <span data-ttu-id="ea32e-122">[Tratamento da notificação de tabela](handling-table-notification.md): descreve como se registrar para notificações da tabela de hierarquia.</span><span class="sxs-lookup"><span data-stu-id="ea32e-122">[Handling Table Notification](handling-table-notification.md): Describes how to register for notifications from the hierarchy table.</span></span>
    
- <span data-ttu-id="ea32e-123">[Implementar um objeto de coletor de aviso](implementing-an-advise-sink-object.md): descreve como implementar um objeto de coletor de aviso.</span><span class="sxs-lookup"><span data-stu-id="ea32e-123">[Implementing an Advise Sink Object](implementing-an-advise-sink-object.md): Describes how to implement an advise sink object.</span></span>
    
- <span data-ttu-id="ea32e-124">[Cronometrar uma notificação](timing-a-notification.md): descreve o intervalo de notificação de cliente por provedores de serviços.</span><span class="sxs-lookup"><span data-stu-id="ea32e-124">[Timing a Notification](timing-a-notification.md): Describes the timing of client notification by service providers.</span></span>
    
- <span data-ttu-id="ea32e-125">[Garantir uma notificação segura para thread](ensuring-a-thread-safe-notification.md): descreve como garantir a notificação segura para thread com MAPI.</span><span class="sxs-lookup"><span data-stu-id="ea32e-125">[Ensuring a Thread-Safe Notification](ensuring-a-thread-safe-notification.md): Describes how to ensure thread-safe notification with MAPI.</span></span>
    
- <span data-ttu-id="ea32e-126">[Forçar uma notificação](forcing-a-notification.md): descreve como forçar uma notificação em MAPI.</span><span class="sxs-lookup"><span data-stu-id="ea32e-126">[Forcing a Notification](forcing-a-notification.md): Describes how to force a notification in MAPI.</span></span>
    

