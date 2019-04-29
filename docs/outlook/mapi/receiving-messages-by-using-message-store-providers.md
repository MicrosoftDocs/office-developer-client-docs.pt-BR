---
title: Recebendo mensagens usando provedores de repositórios de mensagens
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
# <a name="receiving-messages-by-using-message-store-providers"></a>Recebendo mensagens usando provedores de repositórios de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os provedores de repositórios de mensagens não precisam suportar envios de mensagens de entrada (ou seja, oferecem suporte à capacidade de provedores de transporte e ao spooler MAPI para usar o provedor de armazenamento de mensagens como um ponto de entrega para mensagens). No enTanto, se o seu provedor de repositório de mensagens não oferecer suporte a envios de mensagens de entrada, ele não poderá ser usado como o repositório de mensagens padrão.
  
Para dar suporte a envios de mensagens de entrada, seu provedor de repositório de mensagens deve fazer o seguinte:
  
- Suporte para os métodos [IMsgStore:: GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) e [IMsgStore:: GetReceiveFolder](imsgstore-getreceivefolder.md) para que os aplicativos clientes possam encontrar mensagens de entrada. 
    
- Suporta o método [IMsgStore:: NotifyNewMail](imsgstore-notifynewmail.md) para que o spooler MAPI possa informar ao provedor de repositório de mensagens que uma nova mensagem chegou. 
    
- Implementar notificações para que os clientes possam se registrar para notificação de nova mensagem. As notificações são opcionais, mas o provedor deve implementá-las.
    
A sequência de chamadas de método que ocorre quando uma mensagem de entrada é entregue a um repositório de mensagens é da seguinte maneira:
  
1. O spooler MAPI chama [IMsgStore:: OpenEntry](imsgstore-openentry.md) com a EntryID [](entryid.md) da caixa de entrada para obter uma interface [IMAPIFolder](imapifolderimapicontainer.md) . 
    
2. O spooler MAPI chama [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) para obter um novo objeto Message. 
    
3. O spooler MAPI transmite o objeto Message para o provedor de transporte.
    
4. O provedor de transporte preenche as propriedades da mensagem com dados do sistema de mensagens subjacente e chama o método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) do objeto Message. 
    
5. O provedor de repositório de mensagens usa seu método de notificação para informar aos clientes registrados que uma nova mensagem chegou.
    
6. O spooler MAPI chama o método [IMsgStore:: NotifyNewMail](imsgstore-notifynewmail.md) do repositório de mensagens. 
    
## <a name="see-also"></a>Confira também



[Recursos do repositório de mensagens](message-store-features.md)

