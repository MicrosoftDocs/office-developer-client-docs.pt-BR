---
title: Receber mensagens usando provedores do repositório de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4763951e-ccfd-453e-b99c-5c7d5efb90c2
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 8a5df2e8f50d8de05ec43b03ae5b56887e76d505
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590187"
---
# <a name="receiving-messages-by-using-message-store-providers"></a>Receber mensagens usando provedores do repositório de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Provedores de armazenamento de mensagem não precisa suportar envios de mensagem de entrada (ou seja, oferecem suporte para o repositório provedor de provedores de transporte e o MAPI spooler para usar a mensagem como um ponto de entrega de mensagens). No entanto, se o seu provedor de armazenamento de mensagens não oferece suporte a envios de mensagem de entrada, ele não pode ser usado como o armazenamento de mensagens padrão.
  
Para oferecer suporte a envios de mensagem de entrada, seu provedor de armazenamento de mensagem deve fazer o seguinte:
  
- Suporte aos métodos [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) e [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) para que aplicativos clientes possam encontrar as mensagens de entrada. 
    
- Suporte ao método [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) para que o MAPI spooler pode informar o provedor de armazenamento de mensagem que uma nova mensagem chegou. 
    
- Implementar notificações para que os clientes podem se inscrever para fins de notificação de mensagem nova. As notificações são opcionais, mas seu provedor deve implementá-las.
    
A sequência de chamadas de método que ocorre quando uma mensagem de entrada é entregue a um armazenamento de mensagens é da seguinte maneira:
  
1. O MAPI spooler chama [IMsgStore::OpenEntry](imsgstore-openentry.md) com a caixa de entrada [EntryID](entryid.md) para obter uma interface [IMAPIFolder](imapifolderimapicontainer.md) . 
    
2. O MAPI spooler chama [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) para obter um novo objeto de mensagem. 
    
3. O MAPI spooler passa o objeto de mensagem para o provedor de transporte.
    
4. O provedor de transporte preenche as propriedades da mensagem com dados de sistema de mensagens subjacente e chama o método de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) do objeto de mensagem. 
    
5. O provedor de armazenamento de mensagem usa seu método de notificação para informar aos clientes registrados que uma nova mensagem chegou.
    
6. O MAPI spooler chama o método de [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) do armazenamento de mensagens. 
    
## <a name="see-also"></a>Confira também



[Recursos do repositório de mensagens](message-store-features.md)

