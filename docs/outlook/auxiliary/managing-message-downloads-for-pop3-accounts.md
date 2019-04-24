---
title: Gerenciar o download de mensagens de contas POP3
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b4218aa6-1591-49db-9782-f286135fc79a
description: Esta seção descreve como o provedor POP3 do Outlook usa o histórico de listagem de ID exclusiva (UIDL) em uma conta POP3 para identificar mensagens que o provedor tem baixado ou excluído do servidor POP3, para evitar que a mesma mensagem seja baixada mais de uma vez.
ms.openlocfilehash: 35c50d83c317ebefa52fd9bfcb348c8411a06f25
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322243"
---
# <a name="managing-message-downloads-for-pop3-accounts"></a>Gerenciar o download de mensagens de contas POP3

Esta seção descreve como o provedor POP3 do Outlook usa o histórico de listagem de ID exclusiva (UIDL) em uma conta POP3 para identificar mensagens que o provedor tem baixado ou excluído do servidor POP3, para evitar que a mesma mensagem seja baixada mais de uma vez.
  
## <a name="introduction-to-pop"></a>Introdução ao POP

O protocolo POP (Post Office) especifica um protocolo de camada de aplicativos para um cliente de email como o Outlook para baixar emails em um servidor de email. Ela permite ao usuário baixar uma cópia de uma mensagem de email para um dispositivo local (como um Smartphone ou computador) e o deixar uma cópia no servidor ou excluí-lo. O protocolo aceita apenas um cliente de email conectado à caixa de correio ao mesmo tempo. Especifica apenas como recuperar, mas não enviar mensagens de email do servidor de email. Ao usar o POP, um cliente de email normalmente verifica se há novas mensagens de email, se conecta ao servidor de emails apenas durante a quantidade de tempo que demora para baixar as novas mensagens e não se mantém conectado ao servidor para obter novas notificações de email. O POP dá suporte somente a mensagens de email, mas não outros tipos de itens como compromissos e contatos, a menos que eles sejam encapsulados em um email. POP3 é a versão 3 do protocolo.
  
Mensagens de uma conta POP são identificadas por identificadores exclusivos (UIDs). Um cliente de email que deixa o email no servidor usa o comando UIDL para recuperar o mapa UIDL que associa cada mensagem que foi entregue à caixa de correio para o UID. O cliente também obtém o histórico UIDL para mensagens baixadas ou excluídas na caixa de entrada desse cliente. Baseado no histórico UIDL, o cliente pode determinar quais mensagens são novas e devem ser baixadas.

- [Localizar o histórico de download da mensagem para uma conta POP3](locating-the-message-download-history-for-a-pop3-account.md): Este tópico descreve como um cliente de email acessa a propriedade[PidTagAttachDataBinary](https://msdn.microsoft.com/library/3b0a8b28-863e-4b96-a4c0-fdb8f40555b9%28Office.15%29.aspx) para receber o histórico UIDL de mensagens na caixa de entrade de um cliente de uma conta POP3. 
    
- [Análise o histórico de download da mensagem para uma conta POP3](parsing-the-message-download-history-for-a-pop3-account.md): Este tópico descreve como analisar o POP3 BLOB que representa o histórico UIDL para mensagens na caixa de entrada do cliente em uma conta POP3 e identifica mensagens baixadas ou excluídas nessa conta.
    
## <a name="see-also"></a>Confira também

- [Gerenciamento de contas do Outlook](outlook-account-management.md)    
- [Localizar o histórico de download de mensagens de uma conta POP3](locating-the-message-download-history-for-a-pop3-account.md) 
- [Analisar o histórico de download de mensagens de uma conta POP3](parsing-the-message-download-history-for-a-pop3-account.md)   
- [PROP_POP_LEAVE_ON_SERVER](prop_pop_leave_on_server.md)  
- [Constantes (PI de gerenciamento de contas)](constants-account-management-api.md)    
- [Propriedades (PI de gerenciamento de contas)](properties-account-management-api.md)
    

