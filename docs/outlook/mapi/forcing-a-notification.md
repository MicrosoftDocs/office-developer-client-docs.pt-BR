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
# <a name="forcing-a-notification"></a>Forçar uma notificação

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Quando os provedores de serviços usam os métodos [IMAPISupport : IUnknown](imapisupportiunknown.md) para notificação, MAPI entrega notificações usando uma janela oculta e seu procedimento de janela correspondente. Para cada processo receber uma notificação, o MAPI posta uma mensagem especial na janela oculta. Essa mensagem é nomeada com a **constante szMAPINotificationMsg** definida em MAPIDEFS.H. 
  
Você recebe essas notificações quando o procedimento de janela oculta processa a **mensagem szMAPINotificationMsg.** Para garantir que as notificações sejam entregues, é necessário aguardar e despachar essa **mensagem szMAPINotificationMsg.** Implementar a lógica para fazer isso pode ser feito de forma bastante simples, mas o MAPI fornece um ponto de entrada na DLL MAPI chamada [HrDispatchNotifications](hrdispatchnotifications.md) para tornar o processamento ainda mais simples. Chame **HrDispatchNotifications** da seguinte forma para receber notificações em seu cliente: 
  
```cpp
HRESULT hr = HrDispatchNotifications(0);
 
```


