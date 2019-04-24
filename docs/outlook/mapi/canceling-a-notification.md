---
title: Cancelar uma notificação
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: decd5d7d-1f47-47c2-b9c4-be0e652c99dd
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: fb0972638fdd062c99040694222724566281024f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326401"
---
# <a name="canceling-a-notification"></a><span data-ttu-id="64b5d-103">Cancelar uma notificação</span><span class="sxs-lookup"><span data-stu-id="64b5d-103">Canceling a Notification</span></span>

  
  
<span data-ttu-id="64b5d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="64b5d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="64b5d-105">Para cancelar uma notificação, os clientes chamam o método **Unadvise** de origem de um aviso.</span><span class="sxs-lookup"><span data-stu-id="64b5d-105">To cancel a notification, clients call an advise source's **Unadvise** method.</span></span> <span data-ttu-id="64b5d-106">O **aviso** de chamada é importante porque faz com que o provedor de serviços Libere sua referência ao seu coletor de avisos.</span><span class="sxs-lookup"><span data-stu-id="64b5d-106">Calling **Unadvise** is important because it causes the service provider to release its reference to your advise sink.</span></span> <span data-ttu-id="64b5d-107">Desde que um provedor de serviços mantenha uma referência a um coletor de aviso, o coletor de avisos pode continuar a receber chamadas [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="64b5d-107">As long as a service provider maintains a reference to an advise sink, the advise sink can continue to receive [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) calls.</span></span> <span data-ttu-id="64b5d-108">Na verdade, por causa da natureza assíncrona da notificação de eventos, os clientes podem ser notificados mesmo após uma chamada de **aviso** de cancelamento bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="64b5d-108">In fact, because of the asynchronous nature of event notification, clients can be notified even after a successful **Unadvise** call.</span></span> <span data-ttu-id="64b5d-109">Os clientes devem ser capazes de lidar com o recebimento de notificações a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="64b5d-109">Clients must be able to handle the receipt of notifications at any time.</span></span> 
  
<span data-ttu-id="64b5d-110">Como as implementações do provedor de serviços diferem, os clientes que não podem chamar **Unadvise** para cancelar uma notificação não poderão supor nada sobre quando um provedor vai liberar sua referência ao seu coletor de avisos.</span><span class="sxs-lookup"><span data-stu-id="64b5d-110">Because service provider implementations differ, clients that fail to call **Unadvise** to cancel a notification cannot assume anything about when a provider will release its reference to their advise sink.</span></span> <span data-ttu-id="64b5d-111">Alguns provedores de serviços liberam suas referências para avisar os coletores quando liberam suas fontes de aviso.</span><span class="sxs-lookup"><span data-stu-id="64b5d-111">Some service providers release their references to advise sinks when they release their advise sources.</span></span> <span data-ttu-id="64b5d-112">Alguns provedores de serviços não.</span><span class="sxs-lookup"><span data-stu-id="64b5d-112">Some service providers do not.</span></span> <span data-ttu-id="64b5d-113">Desde que um provedor de serviços mantenha uma referência a um coletor de aviso, esse coletor de aviso pode continuar recebendo notificações.</span><span class="sxs-lookup"><span data-stu-id="64b5d-113">As long as a service provider maintains a reference to an advise sink, that advise sink can continue to receive notifications.</span></span> 
  

