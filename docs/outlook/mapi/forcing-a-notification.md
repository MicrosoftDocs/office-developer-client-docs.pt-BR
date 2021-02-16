---
title: Forçar uma notificação
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9c7d6605-73ee-468c-981b-e0853106c9ba
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 54eaf9e67da1b520896122c937508a90700a0b84
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433280"
---
# <a name="forcing-a-notification"></a><span data-ttu-id="7d338-103">Forçar uma notificação</span><span class="sxs-lookup"><span data-stu-id="7d338-103">Forcing a Notification</span></span>

  
  
<span data-ttu-id="7d338-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7d338-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7d338-105">Quando os provedores de serviços usam os métodos [IMAPISupport : IUnknown](imapisupportiunknown.md) para notificação, MAPI entrega notificações usando uma janela oculta e seu procedimento de janela correspondente.</span><span class="sxs-lookup"><span data-stu-id="7d338-105">When service providers use the [IMAPISupport : IUnknown](imapisupportiunknown.md) methods for notification, MAPI delivers notifications using a hidden window and its corresponding window procedure.</span></span> <span data-ttu-id="7d338-106">Para cada processo receber uma notificação, o MAPI posta uma mensagem especial na janela oculta.</span><span class="sxs-lookup"><span data-stu-id="7d338-106">For each process to receive a notification, MAPI posts a special message to the hidden window.</span></span> <span data-ttu-id="7d338-107">Essa mensagem é nomeada com a **constante szMAPINotificationMsg** definida em MAPIDEFS.H.</span><span class="sxs-lookup"><span data-stu-id="7d338-107">This message is named with the constant **szMAPINotificationMsg** which is defined in MAPIDEFS.H.</span></span> 
  
<span data-ttu-id="7d338-108">Você recebe essas notificações quando o procedimento de janela oculta processa a **mensagem szMAPINotificationMsg.**</span><span class="sxs-lookup"><span data-stu-id="7d338-108">You receive these notifications when the hidden window's window procedure processes the **szMAPINotificationMsg** message.</span></span> <span data-ttu-id="7d338-109">Para garantir que as notificações sejam entregues, é necessário aguardar e despachar essa **mensagem szMAPINotificationMsg.**</span><span class="sxs-lookup"><span data-stu-id="7d338-109">To guarantee that notifications are delivered, it is necessary to wait for and dispatch this **szMAPINotificationMsg** message.</span></span> <span data-ttu-id="7d338-110">Implementar a lógica para fazer isso pode ser feito de forma bastante simples, mas o MAPI fornece um ponto de entrada na DLL MAPI chamada [HrDispatchNotifications](hrdispatchnotifications.md) para tornar o processamento ainda mais simples.</span><span class="sxs-lookup"><span data-stu-id="7d338-110">Implementing the logic to achieve this can be done fairly simply, but MAPI provides an entry point into the MAPI DLL called [HrDispatchNotifications](hrdispatchnotifications.md) to make processing even simpler.</span></span> <span data-ttu-id="7d338-111">Chame **HrDispatchNotifications** da seguinte forma para receber notificações em seu cliente:</span><span class="sxs-lookup"><span data-stu-id="7d338-111">Call **HrDispatchNotifications** as follows to receive notifications in your client:</span></span> 
  
```cpp
HRESULT hr = HrDispatchNotifications(0);
 
```


