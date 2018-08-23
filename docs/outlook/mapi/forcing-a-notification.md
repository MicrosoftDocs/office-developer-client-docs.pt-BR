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
ms.openlocfilehash: 5affce8ab7a8b08019816ad9485641c401dd80c9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578770"
---
# <a name="forcing-a-notification"></a><span data-ttu-id="637b9-103">Forçar uma notificação</span><span class="sxs-lookup"><span data-stu-id="637b9-103">Forcing a Notification</span></span>

  
  
<span data-ttu-id="637b9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="637b9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="637b9-105">Quando provedores de serviço usam o [IMAPISupport: IUnknown](imapisupportiunknown.md) métodos de notificação, MAPI envia notificações usando uma janela oculta e seu procedimento de janela correspondente.</span><span class="sxs-lookup"><span data-stu-id="637b9-105">When service providers use the [IMAPISupport : IUnknown](imapisupportiunknown.md) methods for notification, MAPI delivers notifications using a hidden window and its corresponding window procedure.</span></span> <span data-ttu-id="637b9-106">Para cada processo recebe uma notificação, MAPI posta uma mensagem especial para a janela oculta.</span><span class="sxs-lookup"><span data-stu-id="637b9-106">For each process to receive a notification, MAPI posts a special message to the hidden window.</span></span> <span data-ttu-id="637b9-107">Essa mensagem é chamada com a constante **szMAPINotificationMsg** , que é definida em MAPIDEFS. H.</span><span class="sxs-lookup"><span data-stu-id="637b9-107">This message is named with the constant **szMAPINotificationMsg** which is defined in MAPIDEFS.H.</span></span> 
  
<span data-ttu-id="637b9-108">Você receber essas notificações quando o procedimento de janela da janela ocultas processa a mensagem **szMAPINotificationMsg** .</span><span class="sxs-lookup"><span data-stu-id="637b9-108">You receive these notifications when the hidden window's window procedure processes the **szMAPINotificationMsg** message.</span></span> <span data-ttu-id="637b9-109">Para garantir que as notificações sejam entregues, é necessário aguardar e expedir essa mensagem **szMAPINotificationMsg** .</span><span class="sxs-lookup"><span data-stu-id="637b9-109">To guarantee that notifications are delivered, it is necessary to wait for and dispatch this **szMAPINotificationMsg** message.</span></span> <span data-ttu-id="637b9-110">Implementando a lógica para conseguir isso pode ser feito regularmente simplesmente, mas MAPI fornece um ponto de entrada a DLL MAPI chamado [HrDispatchNotifications](hrdispatchnotifications.md) para tornar o processamento ainda mais simples.</span><span class="sxs-lookup"><span data-stu-id="637b9-110">Implementing the logic to achieve this can be done fairly simply, but MAPI provides an entry point into the MAPI DLL called [HrDispatchNotifications](hrdispatchnotifications.md) to make processing even simpler.</span></span> <span data-ttu-id="637b9-111">Chamada **HrDispatchNotifications** da seguinte maneira para receber notificações em seu cliente:</span><span class="sxs-lookup"><span data-stu-id="637b9-111">Call **HrDispatchNotifications** as follows to receive notifications in your client:</span></span> 
  
```cpp
HRESULT hr = HrDispatchNotifications(0);
 
```


