---
title: Cronometrar uma notificação
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6981a3b0-96eb-44a2-b051-1c5efc70e9e3
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: fa3b155820c64ff55e324c5611eed7348cb93e2b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411145"
---
# <a name="timing-a-notification"></a>Cronometrar uma notificação

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Como a notificação de eventos é um processo assíncrono, você pode ser notificado a qualquer momento, não necessariamente imediatamente após o evento ter ocorrido.
  
 O intervalo de chamadas para o método [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) varia de acordo com o provedor de serviços que está implementando a fonte de aviso. Os provedores de serviços podem notificar seu cliente: 
  
- Simultaneamente com o evento.
    
- Diretamente após o evento.
    
- Em algum momento, depois de seguir o evento, possivelmente após uma chamada de **aviso** . 
    
A maioria dos provedores **** de serviços chama OnNotify após o método MAPI responsável pelo evento ter retornado ao chamador. Por exemplo, as notificações nas mensagens são enviadas quando as alterações da mensagem são salvas, após a chamada [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) , ou quando a mensagem é liberada, após a chamada **IUnknown:: Release** . Até que a notificação seja enviada, nenhuma alteração ficará visível no repositório de mensagens. 
  
Você pode receber notificações de uma fonte de aviso após ter chamado **Unadvise** para cancelar um registro. Não se esqueça de liberar o seu coletor de aviso somente depois que a contagem de referência tiver saído de zero, não seguindo uma chamada de **aviso** bem-sucedido. Não presuma que porque você chamou **Unadvise** que o coletor de avisos não é mais necessário. 
  

