---
title: Cancelando uma notificação
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: decd5d7d-1f47-47c2-b9c4-be0e652c99dd
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: fb0972638fdd062c99040694222724566281024f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409759"
---
# <a name="canceling-a-notification"></a><span data-ttu-id="7a32a-103">Cancelando uma notificação</span><span class="sxs-lookup"><span data-stu-id="7a32a-103">Canceling a Notification</span></span>

  
  
<span data-ttu-id="7a32a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7a32a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7a32a-105">Para cancelar uma notificação, os clientes chamam o método **Unadvise** de uma fonte de aviso.</span><span class="sxs-lookup"><span data-stu-id="7a32a-105">To cancel a notification, clients call an advise source's **Unadvise** method.</span></span> <span data-ttu-id="7a32a-106">Chamar **Unadvise é** importante porque faz com que o provedor de serviços libere sua referência ao seu cliente de consultoria.</span><span class="sxs-lookup"><span data-stu-id="7a32a-106">Calling **Unadvise** is important because it causes the service provider to release its reference to your advise sink.</span></span> <span data-ttu-id="7a32a-107">Contanto que um provedor de serviços mantenha uma referência a um sink de aconselhador, o evento de alerta pode continuar a receber chamadas [IMAPIAdviseSink::OnNotify.](imapiadvisesink-onnotify.md)</span><span class="sxs-lookup"><span data-stu-id="7a32a-107">As long as a service provider maintains a reference to an advise sink, the advise sink can continue to receive [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) calls.</span></span> <span data-ttu-id="7a32a-108">Na verdade, devido à natureza assíncrona da notificação de eventos, os clientes podem ser notificados mesmo depois de uma chamada Não **Prevista** bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="7a32a-108">In fact, because of the asynchronous nature of event notification, clients can be notified even after a successful **Unadvise** call.</span></span> <span data-ttu-id="7a32a-109">Os clientes devem ser capazes de lidar com o recebimento de notificações a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="7a32a-109">Clients must be able to handle the receipt of notifications at any time.</span></span> 
  
<span data-ttu-id="7a32a-110">Como as implementações do provedor de serviços são diferentes, os clientes que não conseguem chamar **Unadvise** para cancelar uma notificação não podem assumir nada sobre quando um provedor liberará sua referência ao seu cliente de aviso.</span><span class="sxs-lookup"><span data-stu-id="7a32a-110">Because service provider implementations differ, clients that fail to call **Unadvise** to cancel a notification cannot assume anything about when a provider will release its reference to their advise sink.</span></span> <span data-ttu-id="7a32a-111">Alguns provedores de serviços liberam suas referências para avisar os clientes quando liberam suas fontes de consultoria.</span><span class="sxs-lookup"><span data-stu-id="7a32a-111">Some service providers release their references to advise sinks when they release their advise sources.</span></span> <span data-ttu-id="7a32a-112">Alguns provedores de serviços não.</span><span class="sxs-lookup"><span data-stu-id="7a32a-112">Some service providers do not.</span></span> <span data-ttu-id="7a32a-113">Contanto que um provedor de serviços mantenha uma referência a um sink de aviso, esse evento de aviso pode continuar a receber notificações.</span><span class="sxs-lookup"><span data-stu-id="7a32a-113">As long as a service provider maintains a reference to an advise sink, that advise sink can continue to receive notifications.</span></span> 
  

