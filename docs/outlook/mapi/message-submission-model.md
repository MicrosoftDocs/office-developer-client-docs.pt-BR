---
title: Modelo de envio de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4bcd19f6-c225-43ac-8c27-c46388e9097a
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 653a9df6ec414aa18c44d8035a59f021d7cc19b8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768146"
---
# <a name="message-submission-model"></a>Modelo de envio de mensagens

  
  
**Aplica-se a**: Outlook 
  
Envio de mensagem é realizado através de uma série de chamadas do spooler MAPI para o provedor de transporte. As chamadas são sequenciadas da seguinte maneira:
  
1. O MAPI spooler chama [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), passando um [IMessage: IMAPIProp](imessageimapiprop.md) instância, para começar o processo. 
    
2. O provedor de transporte, em seguida, coloca um valor de referência — um identificador definido pelo transporte usada em futuras referências a esta mensagem — no local referenciado na **SubmitMessage**.
    
3. O provedor de transporte acessa os dados de mensagem usando a instância **IMessage** passada. Para cada destinatário no passado **IMessage** para o qual ela aceita a responsabilidade, o provedor de transporte define a propriedade **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) e, em seguida, retorna.
    
4. Provedor de transporte que pode usar o método [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) para indicar se ele reconhece quaisquer destinatários que não possam ser entregues, ou para criar um relatório de entrega padrão. **StatusRecips** é uma conveniência para provedores de transporte que determinou que alguns dos destinatários não podem ser entregues em ou que tenha recebido informações de entrega de seu sistema de mensagens subjacente que talvez o aplicativo cliente ou de usuário Encontre útil. 
    
5. Chamada do spooler MAPI para [IXPLogon::EndMessage](ixplogon-endmessage.md) é o final responsabilidade início da mensagem do spooler MAPI para o provedor de transporte. 
    
6. O MAPI spooler pode usar [IXPLogon::TransportNotify](ixplogon-transportnotify.md) para cancelar durante as chamadas **SubmitMessage** ou **EndMessage** de processamento de mensagens. 
    

