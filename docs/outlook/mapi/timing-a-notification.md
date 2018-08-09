---
title: Sincronizar uma notificação
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6981a3b0-96eb-44a2-b051-1c5efc70e9e3
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 9ee999841b53f358dcee85d4d92c5056f665dbf1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770598"
---
# <a name="timing-a-notification"></a><span data-ttu-id="8670e-103">Sincronizar uma notificação</span><span class="sxs-lookup"><span data-stu-id="8670e-103">Timing a Notification</span></span>

  
  
<span data-ttu-id="8670e-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8670e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8670e-105">Porque a notificação de evento é um processo assíncrono, você pode ser notificado a qualquer momento, não necessariamente imediatamente após o evento ocorreu.</span><span class="sxs-lookup"><span data-stu-id="8670e-105">Because event notification is an asynchronous process, you can be notified at any time, not necessarily immediately after the event has occurred.</span></span>
  
 <span data-ttu-id="8670e-106">O tempo de chamadas para seu método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) varia, dependendo de provedor de serviços de implementação a fonte advise.</span><span class="sxs-lookup"><span data-stu-id="8670e-106">The timing of calls to your [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method varies depending on the service provider implementing the advise source.</span></span> <span data-ttu-id="8670e-107">Provedores de serviços podem notificá seja o seu cliente:</span><span class="sxs-lookup"><span data-stu-id="8670e-107">Service providers can notify your client either:</span></span> 
  
- <span data-ttu-id="8670e-108">Simultaneamente, com o evento.</span><span class="sxs-lookup"><span data-stu-id="8670e-108">Simultaneously with the event.</span></span>
    
- <span data-ttu-id="8670e-109">Diretamente após o evento.</span><span class="sxs-lookup"><span data-stu-id="8670e-109">Directly after the event.</span></span>
    
- <span data-ttu-id="8670e-110">Em algum posteriormente momento após o evento, possivelmente após uma chamada **Unadvise** .</span><span class="sxs-lookup"><span data-stu-id="8670e-110">At some later point following the event, possibly after an **Unadvise** call.</span></span> 
    
<span data-ttu-id="8670e-111">A maioria dos provedores de serviço chame **OnNotify** após o método MAPI responsável pelo evento ter retornado para seu chamador.</span><span class="sxs-lookup"><span data-stu-id="8670e-111">Most service providers call **OnNotify** after the MAPI method responsible for the event has returned to its caller.</span></span> <span data-ttu-id="8670e-112">Por exemplo, as notificações de mensagens são enviadas quando a mensagem as alterações são salvas, após a chamada [IMAPIProp::SaveChanges](imapiprop-savechanges.md) , ou quando a mensagem é liberada, após a chamada **IUnknown:: Release** .</span><span class="sxs-lookup"><span data-stu-id="8670e-112">For example, notifications on messages are sent either when changes to the message are saved, after the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) call, or when the message is released, after the **IUnknown::Release** call.</span></span> <span data-ttu-id="8670e-113">Até que a notificação é enviada, nenhuma alteração é visíveis no repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="8670e-113">Until the notification is sent, no changes are visible in the message store.</span></span> 
  
<span data-ttu-id="8670e-114">Você pode receber notificações de uma fonte de advise depois de ter chamado **Unadvise** para cancelar um registro.</span><span class="sxs-lookup"><span data-stu-id="8670e-114">You can receive notifications from an advise source after you have called **Unadvise** to cancel a registration.</span></span> <span data-ttu-id="8670e-115">Certifique-se liberar seu coletor advise somente após sua contagem de referência caiu para zero, não após uma chamada **Unadvise** bem sucedida.</span><span class="sxs-lookup"><span data-stu-id="8670e-115">Be sure to release your advise sink only after its reference count has fallen to zero, not following a successful **Unadvise** call.</span></span> <span data-ttu-id="8670e-116">Não presuma que porque você chamou **Unadvise** que o coletor de eventos advise não é mais necessária.</span><span class="sxs-lookup"><span data-stu-id="8670e-116">Do not assume that because you have called **Unadvise** that the advise sink is no longer necessary.</span></span> 
  

