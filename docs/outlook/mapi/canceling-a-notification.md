---
title: Cancelamento de uma notificação
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: decd5d7d-1f47-47c2-b9c4-be0e652c99dd
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 8cd96dd22daeb98646a62672bd17f7de4d2f7dab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766248"
---
# <a name="canceling-a-notification"></a><span data-ttu-id="cfd12-103">Cancelamento de uma notificação</span><span class="sxs-lookup"><span data-stu-id="cfd12-103">Canceling a Notification</span></span>

  
  
<span data-ttu-id="cfd12-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cfd12-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cfd12-105">Para cancelar uma notificação, clientes chame método de **Unadvise** de uma fonte advise.</span><span class="sxs-lookup"><span data-stu-id="cfd12-105">To cancel a notification, clients call an advise source's **Unadvise** method.</span></span> <span data-ttu-id="cfd12-106">Chamar **Unadvise** é importante, porque ele faz com que o provedor de serviços liberar a sua referência para o seu coletor advise.</span><span class="sxs-lookup"><span data-stu-id="cfd12-106">Calling **Unadvise** is important because it causes the service provider to release its reference to your advise sink.</span></span> <span data-ttu-id="cfd12-107">Um provedor de serviço mantém uma referência para um coletor advise, desde que o coletor de eventos advise pode continuar a receber chamadas de [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="cfd12-107">As long as a service provider maintains a reference to an advise sink, the advise sink can continue to receive [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) calls.</span></span> <span data-ttu-id="cfd12-108">Na verdade, devido à natureza assíncrona da notificação de evento, clientes podem ser notificados mesmo depois de chamar um bem-sucedida **Unadvise** .</span><span class="sxs-lookup"><span data-stu-id="cfd12-108">In fact, because of the asynchronous nature of event notification, clients can be notified even after a successful **Unadvise** call.</span></span> <span data-ttu-id="cfd12-109">Clientes devem estar aptos a lidar com o recebimento de notificações a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="cfd12-109">Clients must be able to handle the receipt of notifications at any time.</span></span> 
  
<span data-ttu-id="cfd12-110">Como diferem de implementações de provedor de serviço, a clientes que falham ao **Unadvise** para cancelar uma notificação de chamada não podem assumir-nada sobre, quando um provedor lançará sua referência para seu coletor de eventos advise.</span><span class="sxs-lookup"><span data-stu-id="cfd12-110">Because service provider implementations differ, clients that fail to call **Unadvise** to cancel a notification cannot assume anything about when a provider will release its reference to their advise sink.</span></span> <span data-ttu-id="cfd12-111">Alguns provedores de serviços release suas referências para avisar PIAs quando eles liberam suas fontes advise.</span><span class="sxs-lookup"><span data-stu-id="cfd12-111">Some service providers release their references to advise sinks when they release their advise sources.</span></span> <span data-ttu-id="cfd12-112">Alguns provedores de serviços tem não.</span><span class="sxs-lookup"><span data-stu-id="cfd12-112">Some service providers do not.</span></span> <span data-ttu-id="cfd12-113">Desde que um provedor de serviço mantém uma referência para um coletor advise, o coletor de eventos que advise pode continuar a receber notificações.</span><span class="sxs-lookup"><span data-stu-id="cfd12-113">As long as a service provider maintains a reference to an advise sink, that advise sink can continue to receive notifications.</span></span> 
  

