---
title: Modelo de envio de mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4bcd19f6-c225-43ac-8c27-c46388e9097a
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 090a765fd6c758e5f146caa0e7f36276b052f69e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421120"
---
# <a name="message-submission-model"></a>Modelo de envio de mensagem

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O envio de mensagens é realizado por uma série de chamadas do spooler MAPI para o provedor de transporte. As chamadas são sequenciadas da seguinte forma:
  
1. O spooler MAPI chama [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), passando uma [IMessage : instância IMAPIProp,](imessageimapiprop.md) para iniciar o processo. 
    
2. Em seguida, o provedor de transporte coloca um valor de referência — um identificador definido por transporte usado em referências futuras a essa mensagem — no local referenciado em **SubmitMessage**.
    
3. O provedor de transporte acessa os dados da mensagem usando a **instância IMessage** passada. Para cada destinatário no **IMessage** passado para o qual ele aceita responsabilidade, o provedor de transporte define a propriedade **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) e retorna.
    
4. O provedor de transporte pode usar o método [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) para indicar se reconhece destinatários que não podem ser entregues ou para criar um relatório de entrega padrão. **StatusRecips** é uma conveniência para provedores de transporte que determinaram que alguns dos destinatários não podem ser entregues ou que receberam informações de entrega de seu sistema de mensagens subjacente que o usuário ou aplicativo cliente pode achar útil. 
    
5. A chamada do spooler MAPI para [IXPLogon::EndMessage](ixplogon-endmessage.md) é a entrega de responsabilidade final da mensagem do spooler MAPI para o provedor de transporte. 
    
6. O spooler MAPI pode usar [IXPLogon::TransportNotify](ixplogon-transportnotify.md) para cancelar o processamento de mensagens durante as chamadas **SubmitMessage** ou **EndMessage.** 
    

