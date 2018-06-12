---
title: Gerenciando mensagem downloads para contas POP3
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b4218aa6-1591-49db-9782-f286135fc79a
description: Esta seção descreve como o provedor de POP3 do Outlook usa o histórico de listagem de identificação exclusiva (UIDL) utilizando uma conta POP3 para identificar as mensagens que o provedor tenha baixado ou excluídas do servidor POP3, para evitar o download a mesma mensagem mais de uma vez.
ms.openlocfilehash: 7661797193b0d64979cf58ca384a8359bfa59cfc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766002"
---
# <a name="managing-message-downloads-for-pop3-accounts"></a>Gerenciando mensagem downloads para contas POP3

Esta seção descreve como o provedor de POP3 do Outlook usa o histórico de listagem de identificação exclusiva (UIDL) utilizando uma conta POP3 para identificar as mensagens que o provedor tenha baixado ou excluídas do servidor POP3, para evitar o download a mesma mensagem mais de uma vez.
  
## <a name="introduction-to-pop"></a>Introdução ao POP

Post Office Protocol (POP) especifica um protocolo de camada de aplicativo para um cliente de email, como o Outlook Baixe mensagens de email de um servidor de email. Ele permite que um usuário baixar uma cópia de uma mensagem de email para um dispositivo local (por exemplo, um computador ou telefone inteligente) e qualquer deixar uma cópia no servidor ou excluí-lo. O protocolo oferece suporte a apenas um cliente de email para ser conectado à caixa de correio de uma só vez. Especifica apenas como recuperar, mas não enviar mensagens de email do servidor de email. Ao usar o POP, o cliente de email normalmente tem que verificar se há novas mensagens de email, conecta-se ao servidor de email apenas para a quantidade de tempo que leva para baixar novas mensagens e não fique conectado ao servidor para obter novas notificações de email. POP suporta somente as mensagens de email, mas não de outros tipos de item como contatos e compromissos, a menos que eles são encapsulados em um email. POP3 é a versão 3 do protocolo.
  
Mensagens para uma conta POP são identificadas por identificadores exclusivos (UIDs). Um cliente de email que deixa o email no servidor usa o comando UIDL para recuperar o mapa UIDL que associa cada mensagem foi entregue à caixa de correio para o seu UID. O cliente também obtém o histórico UIDL para mensagens que foram baixadas ou excluídas da caixa de entrada em que o cliente. Com base no histórico de UIDL, o cliente pode determinar quais mensagens são novas e devem ser baixadas.

- [Localizar a mensagem baixar o histórico de uma conta POP3](locating-the-message-download-history-for-a-pop3-account.md): Este tópico descreve como o cliente de email acessa a propriedade [PidTagAttachDataBinary](http://msdn.microsoft.com/library/3b0a8b28-863e-4b96-a4c0-fdb8f40555b9%28Office.15%29.aspx) para obter o histórico UIDL para mensagens no cliente da caixa de entrada de uma conta POP3. 
    
- [Analisar a mensagem baixar o histórico de uma conta POP3](parsing-the-message-download-history-for-a-pop3-account.md): Este tópico descreve como analisar o BLOB POP3 que representa o histórico de UIDL para mensagens no cliente da caixa de entrada de uma conta POP3, para identificar as mensagens que foram baixadas ou excluídas em que conta.
    
## <a name="see-also"></a>Confira também

- [Gerenciamento de conta do Outlook](outlook-account-management.md)    
- [Localizando o histórico de download de mensagens para uma conta POP3](locating-the-message-download-history-for-a-pop3-account.md) 
- [Analisar o histórico de download de mensagens para uma conta POP3](parsing-the-message-download-history-for-a-pop3-account.md)   
- [PROP_POP_LEAVE_ON_SERVER](prop_pop_leave_on_server.md)  
- [Constantes (API de gerenciamento de conta)](constants-account-management-api.md)    
- [Propriedades (API de gerenciamento de conta)](properties-account-management-api.md)
    

