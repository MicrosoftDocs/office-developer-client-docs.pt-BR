---
title: Recebendo mensagens usando provedores de armazenamento de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4763951e-ccfd-453e-b99c-5c7d5efb90c2
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: c93a4b56489c2bfb458e2e1cd872073e64d9998a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418726"
---
# <a name="receiving-messages-by-using-message-store-providers"></a>Recebendo mensagens usando provedores de armazenamento de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os provedores de armazenamento de mensagens não têm que dar suporte a envios de mensagens de entrada (ou seja, dar suporte à capacidade de provedores de transporte e o spooler MAPI usarem o provedor de armazenamento de mensagens como um ponto de entrega para mensagens). No entanto, se seu provedor de armazenamento de mensagens não suportar envios de mensagens de entrada, ele não poderá ser usado como o armazenamento de mensagens padrão.
  
Para dar suporte a envios de mensagens de entrada, seu provedor de armazenamento de mensagens deve fazer o seguinte:
  
- Suporte aos métodos [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) e [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) para que os aplicativos cliente possam encontrar mensagens de entrada. 
    
- Suporte ao [método IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) para que o spooler MAPI possa informar ao provedor de repositório de mensagens que uma nova mensagem chegou. 
    
- Implemente notificações para que os clientes possam se registrar para nova notificação de mensagem. As notificações são opcionais, mas seu provedor deve implementá-las.
    
A sequência de chamadas de método que ocorre quando uma mensagem de entrada é entregue a um armazenamento de mensagens é a seguinte:
  
1. O spooler MAPI chama [IMsgStore::OpenEntry](imsgstore-openentry.md) com a [EntryID](entryid.md) da Caixa de Entrada para obter uma interface [IMAPIFolder.](imapifolderimapicontainer.md) 
    
2. O spooler MAPI chama [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) para obter um novo objeto de mensagem. 
    
3. O spooler MAPI passa o objeto de mensagem para o provedor de transporte.
    
4. O provedor de transporte preenche as propriedades da mensagem com dados do sistema de mensagens subjacente e chama o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) do objeto de mensagem. 
    
5. O provedor de armazenamento de mensagens usa seu método de notificação para informar aos clientes registrados que uma nova mensagem chegou.
    
6. O spooler MAPI chama o método [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) do repositório de mensagens. 
    
## <a name="see-also"></a>Confira também



[Recursos do Armazenamento de Mensagens](message-store-features.md)

