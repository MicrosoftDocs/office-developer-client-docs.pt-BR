---
title: Cronometrar uma notificação
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6981a3b0-96eb-44a2-b051-1c5efc70e9e3
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: fa3b155820c64ff55e324c5611eed7348cb93e2b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360393"
---
# <a name="timing-a-notification"></a><span data-ttu-id="4898f-103">Cronometrar uma notificação</span><span class="sxs-lookup"><span data-stu-id="4898f-103">Timing a Notification</span></span>

  
  
<span data-ttu-id="4898f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4898f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4898f-105">Como a notificação de eventos é um processo assíncrono, você pode ser notificado a qualquer momento, não necessariamente imediatamente após o evento ter ocorrido.</span><span class="sxs-lookup"><span data-stu-id="4898f-105">Because event notification is an asynchronous process, you can be notified at any time, not necessarily immediately after the event has occurred.</span></span>
  
 <span data-ttu-id="4898f-106">O intervalo de chamadas para o método [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) varia de acordo com o provedor de serviços que está implementando a fonte de aviso.</span><span class="sxs-lookup"><span data-stu-id="4898f-106">The timing of calls to your [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method varies depending on the service provider implementing the advise source.</span></span> <span data-ttu-id="4898f-107">Os provedores de serviços podem notificar seu cliente:</span><span class="sxs-lookup"><span data-stu-id="4898f-107">Service providers can notify your client either:</span></span> 
  
- <span data-ttu-id="4898f-108">Simultaneamente com o evento.</span><span class="sxs-lookup"><span data-stu-id="4898f-108">Simultaneously with the event.</span></span>
    
- <span data-ttu-id="4898f-109">Diretamente após o evento.</span><span class="sxs-lookup"><span data-stu-id="4898f-109">Directly after the event.</span></span>
    
- <span data-ttu-id="4898f-110">Em algum momento, depois de seguir o evento, possivelmente após uma chamada de **aviso** .</span><span class="sxs-lookup"><span data-stu-id="4898f-110">At some later point following the event, possibly after an **Unadvise** call.</span></span> 
    
<span data-ttu-id="4898f-111">A maioria dos provedores \*\*\*\* de serviços chama OnNotify após o método MAPI responsável pelo evento ter retornado ao chamador.</span><span class="sxs-lookup"><span data-stu-id="4898f-111">Most service providers call **OnNotify** after the MAPI method responsible for the event has returned to its caller.</span></span> <span data-ttu-id="4898f-112">Por exemplo, as notificações nas mensagens são enviadas quando as alterações da mensagem são salvas, após a chamada [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) , ou quando a mensagem é liberada, após a chamada **IUnknown:: Release** .</span><span class="sxs-lookup"><span data-stu-id="4898f-112">For example, notifications on messages are sent either when changes to the message are saved, after the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) call, or when the message is released, after the **IUnknown::Release** call.</span></span> <span data-ttu-id="4898f-113">Até que a notificação seja enviada, nenhuma alteração ficará visível no repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="4898f-113">Until the notification is sent, no changes are visible in the message store.</span></span> 
  
<span data-ttu-id="4898f-114">Você pode receber notificações de uma fonte de aviso após ter chamado **Unadvise** para cancelar um registro.</span><span class="sxs-lookup"><span data-stu-id="4898f-114">You can receive notifications from an advise source after you have called **Unadvise** to cancel a registration.</span></span> <span data-ttu-id="4898f-115">Não se esqueça de liberar o seu coletor de aviso somente depois que a contagem de referência tiver saído de zero, não seguindo uma chamada de **aviso** bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="4898f-115">Be sure to release your advise sink only after its reference count has fallen to zero, not following a successful **Unadvise** call.</span></span> <span data-ttu-id="4898f-116">Não presuma que porque você chamou **Unadvise** que o coletor de avisos não é mais necessário.</span><span class="sxs-lookup"><span data-stu-id="4898f-116">Do not assume that because you have called **Unadvise** that the advise sink is no longer necessary.</span></span> 
  

