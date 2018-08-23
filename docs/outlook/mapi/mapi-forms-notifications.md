---
title: Notificações de formulários de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 97ff2733-a2b1-4da0-b628-00850fc7925b
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 38011c02791688ce5b1c291a1355ccaececd43fd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574731"
---
# <a name="mapi-forms-notifications"></a>Notificações de formulários de MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Registrando para e manipular notificações de objetos de formulário é um processo diferente para outros objetos MAPI. Aconselhe receptores de implementação de notificações de formulário seja o **IMAPIViewAdviseSink** ou interface **IMAPIFormAdviseSink** em vez de **IMAPIAdviseSink**. [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) e [IMAPIFormAdviseSink: IUnknown](imapiformadvisesinkiunknown.md) ter vários métodos de cada um, um para cada um dos eventos possíveis que a correspondente de aviso de origem é capaz de gerar. Por exemplo, **IMAPIFormAdviseSink** tem dois métodos: [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) para tratar uma alteração de status e a [IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md) para exibir uma nova mensagem com o formulário correto a tela de formulário. 
  
A estratégia para formulários de manipulação de eventos é semelhante ao evento manipulação estratégia implementada no OLE. Os clientes não registrar para tipos de evento específicos como fazem para a maioria dos objetos MAPI. Pressupõe-se que Registrando para fins de notificação, eles podem receber qualquer tipo de evento que pode ser gerado pela fonte advise específico. Porque **IMAPIAdviseSink::OnNotify** deve ser escrita para lidar com todos os eventos registrados, implementá-la pode ser complexo para clientes que registram para muitos eventos diferentes. Porque o destino de objetos do coletor de eventos de aviso os métodos no formulário um único evento, a implementação desses métodos é mais simples. 
  

