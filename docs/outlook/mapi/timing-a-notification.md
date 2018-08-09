---
title: Sincronizar uma notificação
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6981a3b0-96eb-44a2-b051-1c5efc70e9e3
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 9ee999841b53f358dcee85d4d92c5056f665dbf1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770598"
---
# <a name="timing-a-notification"></a>Sincronizar uma notificação

  
  
**Aplica-se a**: Outlook 
  
Porque a notificação de evento é um processo assíncrono, você pode ser notificado a qualquer momento, não necessariamente imediatamente após o evento ocorreu.
  
 O tempo de chamadas para seu método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) varia, dependendo de provedor de serviços de implementação a fonte advise. Provedores de serviços podem notificá seja o seu cliente: 
  
- Simultaneamente, com o evento.
    
- Diretamente após o evento.
    
- Em algum posteriormente momento após o evento, possivelmente após uma chamada **Unadvise** . 
    
A maioria dos provedores de serviço chame **OnNotify** após o método MAPI responsável pelo evento ter retornado para seu chamador. Por exemplo, as notificações de mensagens são enviadas quando a mensagem as alterações são salvas, após a chamada [IMAPIProp::SaveChanges](imapiprop-savechanges.md) , ou quando a mensagem é liberada, após a chamada **IUnknown:: Release** . Até que a notificação é enviada, nenhuma alteração é visíveis no repositório de mensagem. 
  
Você pode receber notificações de uma fonte de advise depois de ter chamado **Unadvise** para cancelar um registro. Certifique-se liberar seu coletor advise somente após sua contagem de referência caiu para zero, não após uma chamada **Unadvise** bem sucedida. Não presuma que porque você chamou **Unadvise** que o coletor de eventos advise não é mais necessária. 
  

