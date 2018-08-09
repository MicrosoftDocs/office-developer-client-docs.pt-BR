---
title: Fornecer notificações para provedores do repositório de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0e1cdba-ceb6-4a3f-8449-79d1a0ad1adf
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 3abb4ba67ff5f0cf2284fa9286b6968698877b84
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770202"
---
# <a name="providing-notifications-for-message-store-providers"></a>Fornecer notificações para provedores do repositório de mensagens

  
  
**Aplica-se a**: Outlook 
  
Embora as notificações são opcionais, eles são uma parte muito importante de um provedor de armazenamento de mensagem de boas. Aplicativos cliente e o MAPI spooler contam com notificações do provedor de repositório de mensagem para obter um bom desempenho ao enviar mensagens de saída ou o recebimento de mensagens de entrada. Clientes e o MAPI spooler podem funcionar sem receber notificações do provedor de armazenamento de mensagem, mas não será capazes de informar os usuários das alterações no repositório de mensagem sem eles. Normalmente, isso significa que os usuários não poderão ver o que uma nova mensagem chegou até seu cliente Avançar abre o armazenamento de mensagens pasta de recebimento.
  
Os clientes se registrar para notificações chamando o método [IMsgStore::Advise](imsgstore-advise.md) . O cliente passa em uma [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) interface, uma bitmask que indica que tipo de notificações, o cliente está interessado em receber, e uma **EntryID** que indica qual objeto na mensagem de armazenar o **Advise** solicitação se aplica a. Quando ocorrem eventos de relevantes no objeto (por exemplo, quando uma nova mensagem chega na pasta de recebimento no repositório de mensagem), o provedor de armazenamento de mensagem ou o próprio objeto deve chamar o método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) para todos os ** IMAPIAdviseSink** objetos que foram registrados para esse tipo de evento. 
  
Mesmo que sua mensagem armazenar o provedor notifica nunca outros componentes MAPI das alterações no armazenamento da mensagem, que ele ainda deve implementar **IMsgStore::Advise** para retornar MAPI_E_NO_SUPPORT. Isso informa que outros componentes para não esperar que o provedor de armazenamento de notificações da mensagem. 
  
## <a name="see-also"></a>Confira também



[Recursos do repositório de mensagens](message-store-features.md)

