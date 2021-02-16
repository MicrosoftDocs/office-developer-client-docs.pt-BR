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
  
Registrar e manipular notificações de objetos de formulário é um processo diferente de outros objetos MAPI. Avisar os sinks para notificações de formulário implemente a interface **IMAPIViewAdviseSink** ou **IMAPIFormAdviseSink** em vez de **IMAPIAdviseSink**. [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) e [IMAPIFormAdviseSink : cada IUnknown](imapiformadvisesinkiunknown.md) tem vários métodos, um para cada um dos eventos possíveis que a fonte de alerta correspondente é capaz de gerar. Por exemplo, **IMAPIFormAdviseSink** tem dois métodos: [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) para manipular uma alteração no status do visualizador de formulário e [IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md) para exibir uma nova mensagem com o formulário correto. 
  
A estratégia de manipulação de eventos para formulários é semelhante à estratégia de manipulação de eventos implementada no OLE. Os clientes não se registram para tipos de eventos específicos como fazem para a maioria dos objetos MAPI. A suposição é de que o registro para notificação permite que eles recebam qualquer tipo de evento que possa ser gerado pela fonte de aviso específica. Como **IMAPIAdviseSink::OnNotify** deve ser escrito para manipular todos os eventos registrados, implementá-lo pode ser complexo para clientes que se registram para vários eventos diferentes. Como os métodos no formulário aconselham objetos sink direcionam um único evento, implementar esses métodos é mais simples. 
  

