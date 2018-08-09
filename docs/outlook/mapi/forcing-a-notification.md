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
# <a name="forcing-a-notification"></a>Forçar uma notificação

  
  
**Aplica-se a**: Outlook 
  
Quando provedores de serviço usam o [IMAPISupport: IUnknown](imapisupportiunknown.md) métodos de notificação, MAPI envia notificações usando uma janela oculta e seu procedimento de janela correspondente. Para cada processo recebe uma notificação, MAPI posta uma mensagem especial para a janela oculta. Essa mensagem é chamada com a constante **szMAPINotificationMsg** , que é definida em MAPIDEFS. H. 
  
Você receber essas notificações quando o procedimento de janela da janela ocultas processa a mensagem **szMAPINotificationMsg** . Para garantir que as notificações sejam entregues, é necessário aguardar e expedir essa mensagem **szMAPINotificationMsg** . Implementando a lógica para conseguir isso pode ser feito regularmente simplesmente, mas MAPI fornece um ponto de entrada a DLL MAPI chamado [HrDispatchNotifications](hrdispatchnotifications.md) para tornar o processamento ainda mais simples. Chamada **HrDispatchNotifications** da seguinte maneira para receber notificações em seu cliente: 
  
```cpp
HRESULT hr = HrDispatchNotifications(0);
 
```


