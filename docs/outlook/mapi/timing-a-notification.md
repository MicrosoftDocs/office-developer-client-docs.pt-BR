---
title: Tempo de uma notificação
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6981a3b0-96eb-44a2-b051-1c5efc70e9e3
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: fa3b155820c64ff55e324c5611eed7348cb93e2b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411145"
---
# <a name="timing-a-notification"></a><span data-ttu-id="d78dd-103">Tempo de uma notificação</span><span class="sxs-lookup"><span data-stu-id="d78dd-103">Timing a Notification</span></span>

  
  
<span data-ttu-id="d78dd-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d78dd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d78dd-105">Como a notificação de evento é um processo assíncrono, você pode ser notificado a qualquer momento, não necessariamente imediatamente após o evento ter ocorrido.</span><span class="sxs-lookup"><span data-stu-id="d78dd-105">Because event notification is an asynchronous process, you can be notified at any time, not necessarily immediately after the event has occurred.</span></span>
  
 <span data-ttu-id="d78dd-106">O tempo de chamadas para seu [método IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) varia dependendo do provedor de serviços que implementa a fonte de consultoria.</span><span class="sxs-lookup"><span data-stu-id="d78dd-106">The timing of calls to your [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method varies depending on the service provider implementing the advise source.</span></span> <span data-ttu-id="d78dd-107">Os provedores de serviços podem notificar seu cliente:</span><span class="sxs-lookup"><span data-stu-id="d78dd-107">Service providers can notify your client either:</span></span> 
  
- <span data-ttu-id="d78dd-108">Simultaneamente com o evento.</span><span class="sxs-lookup"><span data-stu-id="d78dd-108">Simultaneously with the event.</span></span>
    
- <span data-ttu-id="d78dd-109">Logo após o evento.</span><span class="sxs-lookup"><span data-stu-id="d78dd-109">Directly after the event.</span></span>
    
- <span data-ttu-id="d78dd-110">Em algum momento posterior após o evento, possivelmente após uma **chamada Não** Prevista.</span><span class="sxs-lookup"><span data-stu-id="d78dd-110">At some later point following the event, possibly after an **Unadvise** call.</span></span> 
    
<span data-ttu-id="d78dd-111">A maioria dos provedores de serviços **chama OnNotify** após o método MAPI responsável pelo evento ter retornado ao chamador.</span><span class="sxs-lookup"><span data-stu-id="d78dd-111">Most service providers call **OnNotify** after the MAPI method responsible for the event has returned to its caller.</span></span> <span data-ttu-id="d78dd-112">Por exemplo, as notificações nas mensagens são enviadas quando as alterações na mensagem são salvas, após a chamada [IMAPIProp::SaveChanges](imapiprop-savechanges.md) ou quando a mensagem é liberada, após a chamada **IUnknown::Release.**</span><span class="sxs-lookup"><span data-stu-id="d78dd-112">For example, notifications on messages are sent either when changes to the message are saved, after the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) call, or when the message is released, after the **IUnknown::Release** call.</span></span> <span data-ttu-id="d78dd-113">Até que a notificação seja enviada, nenhuma alteração será visível no armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="d78dd-113">Until the notification is sent, no changes are visible in the message store.</span></span> 
  
<span data-ttu-id="d78dd-114">Você pode receber notificações de uma fonte de aviso depois de chamar **Unadvise** para cancelar um registro.</span><span class="sxs-lookup"><span data-stu-id="d78dd-114">You can receive notifications from an advise source after you have called **Unadvise** to cancel a registration.</span></span> <span data-ttu-id="d78dd-115">Certifique-se de liberar seu aconselhado somente depois que sua contagem de referência cair para zero, não seguindo uma chamada **Desconselhável** bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="d78dd-115">Be sure to release your advise sink only after its reference count has fallen to zero, not following a successful **Unadvise** call.</span></span> <span data-ttu-id="d78dd-116">Não presuma que, como você chamou **Unadvise,** o sink advise não é mais necessário.</span><span class="sxs-lookup"><span data-stu-id="d78dd-116">Do not assume that because you have called **Unadvise** that the advise sink is no longer necessary.</span></span> 
  

