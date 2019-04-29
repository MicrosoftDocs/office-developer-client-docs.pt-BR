---
title: Fornecer notificações para provedores de repositórios de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0e1cdba-ceb6-4a3f-8449-79d1a0ad1adf
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a28e6e6f008517a6b1c2c82dfa391b478963880f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419930"
---
# <a name="providing-notifications-for-message-store-providers"></a>Fornecer notificações para provedores de repositórios de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Enquanto as notificações são opcionais, elas são uma parte muito importante de um bom provedor de armazenamento de mensagens. Os aplicativos cliente e o spooler MAPI dependem de notificações do provedor de repositórios de mensagens para obter um bom desempenho ao enviar mensagens de saída ou receber mensagens de entrada. Os clientes e o spooler MAPI podem funcionar sem receber notificações do provedor de armazenamento de mensagens, mas não poderão informar os usuários sobre alterações no repositório de mensagens sem eles. Normalmente, isso significa que os usuários não conseguirão ver se uma nova mensagem chegou até que o cliente seguinte Abra a pasta de recebimento do repositório de mensagens.
  
Os clientes se registram para notificações chamando o método [IMsgStore:: Advise](imsgstore-advise.md) . O cliente passa uma interface [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) , uma bitmask que indica o tipo de notificação que o cliente está interessado em receber e uma **EntryID** que indica qual objeto da mensagem armazena o **aviso** a solicitação se aplica ao. Quando eventos relevantes ocorrem no objeto (por exemplo, quando uma nova mensagem chega na pasta receber no repositório de mensagens), o provedor de armazenamento de mensagens ou o próprio objeto deve chamar o método [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) para todos os ** Objetos IMAPIAdviseSink** registrados para esse tipo de evento. 
  
Mesmo que seu provedor de repositório de mensagens nunca notifique outros componentes MAPI de alterações no repositório de mensagens, ele ainda deve implementar **IMsgStore:: Advise** para retornar MAPI_E_NO_SUPPORT. Isso informa outros componentes para não esperar notificações do provedor de armazenamento de mensagens. 
  
## <a name="see-also"></a>Confira também



[Recursos do repositório de mensagens](message-store-features.md)

