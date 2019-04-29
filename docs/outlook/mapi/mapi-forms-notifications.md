---
title: Notificações de formulários MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 97ff2733-a2b1-4da0-b628-00850fc7925b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: e9c10f78af6dff2e0d0c59d0bfe59be07dccd4b2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418607"
---
# <a name="mapi-forms-notifications"></a>Notificações de formulários MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Registrar e lidar com notificações de objetos de formulário é um processo diferente de outros objetos MAPI. Avisar coletores para notificações de formulário implementam a interface **IMAPIViewAdviseSink** ou **IMAPIFormAdviseSink** , em vez de **IMAPIAdviseSink**. [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) e [IMAPIFormAdviseSink: IUnknown](imapiformadvisesinkiunknown.md) têm vários métodos, um para cada um dos possíveis eventos que a fonte de aviso correspondente é capaz de gerar. Por exemplo, **IMAPIFormAdviseSink** tem dois métodos: [IMAPIFormAdviseSink::](imapiformadvisesink-onchange.md) OnChange para lidar com uma alteração no status do Visualizador de formulários e [IMAPIFormAdviseSink:: OnActivateNext](imapiformadvisesink-onactivatenext.md) para exibir uma nova mensagem com o formato correto. 
  
A estratégia de manipulação de eventos para formulários é semelhante à estratégia de manipulação de eventos implementada no OLE. Os clientes não se registram para tipos de eventos específicos como eles fazem para a maioria dos objetos MAPI. A pressuposição é que o registro para notificação permite que eles recebam qualquer tipo de evento que possa ser gerado pela fonte de aviso específica. Como o **IMAPIAdviseSink:: OnNotify** deve ser escrito para lidar com todos os eventos registrados, implementá-lo pode ser complexo para clientes que se registram em vários eventos diferentes. Como os métodos no formulário aconselham que os objetos do coletor direcionem um único evento, a implementação desses métodos é mais simples. 
  

