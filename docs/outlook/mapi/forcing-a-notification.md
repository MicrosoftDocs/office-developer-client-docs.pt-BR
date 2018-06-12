---
title: Forçar uma notificação
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9c7d6605-73ee-468c-981b-e0853106c9ba
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 40fc763071f7113e222c6987dfd70fb7d89bab4b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766583"
---
# <a name="forcing-a-notification"></a><span data-ttu-id="453bf-103">Forçar uma notificação</span><span class="sxs-lookup"><span data-stu-id="453bf-103">Forcing a Notification</span></span>

  
  
<span data-ttu-id="453bf-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="453bf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="453bf-105">Quando provedores de serviço usam o [IMAPISupport: IUnknown](imapisupportiunknown.md) métodos de notificação, MAPI envia notificações usando uma janela oculta e seu procedimento de janela correspondente.</span><span class="sxs-lookup"><span data-stu-id="453bf-105">When service providers use the [IMAPISupport : IUnknown](imapisupportiunknown.md) methods for notification, MAPI delivers notifications using a hidden window and its corresponding window procedure.</span></span> <span data-ttu-id="453bf-106">Para cada processo recebe uma notificação, MAPI posta uma mensagem especial para a janela oculta.</span><span class="sxs-lookup"><span data-stu-id="453bf-106">For each process to receive a notification, MAPI posts a special message to the hidden window.</span></span> <span data-ttu-id="453bf-107">Essa mensagem é chamada com a constante **szMAPINotificationMsg** , que é definida em MAPIDEFS. H.</span><span class="sxs-lookup"><span data-stu-id="453bf-107">This message is named with the constant **szMAPINotificationMsg** which is defined in MAPIDEFS.H.</span></span> 
  
<span data-ttu-id="453bf-108">Você receber essas notificações quando o procedimento de janela da janela ocultas processa a mensagem **szMAPINotificationMsg** .</span><span class="sxs-lookup"><span data-stu-id="453bf-108">You receive these notifications when the hidden window's window procedure processes the **szMAPINotificationMsg** message.</span></span> <span data-ttu-id="453bf-109">Para garantir que as notificações sejam entregues, é necessário aguardar e expedir essa mensagem **szMAPINotificationMsg** .</span><span class="sxs-lookup"><span data-stu-id="453bf-109">To guarantee that notifications are delivered, it is necessary to wait for and dispatch this **szMAPINotificationMsg** message.</span></span> <span data-ttu-id="453bf-110">Implementando a lógica para conseguir isso pode ser feito regularmente simplesmente, mas MAPI fornece um ponto de entrada a DLL MAPI chamado [HrDispatchNotifications](hrdispatchnotifications.md) para tornar o processamento ainda mais simples.</span><span class="sxs-lookup"><span data-stu-id="453bf-110">Implementing the logic to achieve this can be done fairly simply, but MAPI provides an entry point into the MAPI DLL called [HrDispatchNotifications](hrdispatchnotifications.md) to make processing even simpler.</span></span> <span data-ttu-id="453bf-111">Chamada **HrDispatchNotifications** da seguinte maneira para receber notificações em seu cliente:</span><span class="sxs-lookup"><span data-stu-id="453bf-111">Call **HrDispatchNotifications** as follows to receive notifications in your client:</span></span> 
  
```cpp
HRESULT hr = HrDispatchNotifications(0);
 
```


