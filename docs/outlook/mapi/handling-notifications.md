---
title: Manipular notificações
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 451b71da-a888-4d8f-9814-12f9f846de05
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: e261b71a8e94d9db3b1b17168d84798dfe18955d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429156"
---
# <a name="handling-notifications"></a>Manipular notificações

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
As notificações permitem que um objeto informe a outro objeto que ele passou por uma alteração. O tipo de alteração é conhecido como um evento. MAPI define vários eventos para os quais as notificações são geradas. 
  
Os clientes normalmente se registram para um ou mais eventos com um ou mais objetos. Esses objetos são chamados de fontes de consultoria. Os objetos que podem atuar como fontes de consultoria incluem o objeto de sessão, sob o controle de MAPI ou um objeto criado por um provedor de serviços, como uma mensagem. O objeto informado, chamado de evento de alerta, contém uma implementação da interface [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) ou [IMAPIViewAdviseSink : interface IUnknown](imapiviewadvisesinkiunknown.md) e está dentro de um aplicativo cliente. 
  
Os objetos de origem de aviso implementam um método **Advise,** que é chamado pelos clientes para se registrarem para notificações e um método **Unadvise,** que é chamado para cancelar um registro. Um dos parâmetros  a ser aconselhado é um ponteiro para uma implementação de **IMAPIAdviseSink** ou ** IMAPIViewAdviseSink **. A fonte de consultoria armazena esse ponteiro em cache para que ele possa chamar [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) ou um dos métodos em **IMAPIViewAdviseSink** quando ocorrer uma alteração. 
  
Como o recebimento de notificações permite que os usuários vejam as informações mais atualizadas, é recomendável que todos os clientes se registrem e manipularem as notificações. No entanto, é opcional.
  
## <a name="in-this-section"></a>Nesta seção

- [Registro para uma notificação:](registering-for-a-notification.md)descreve como registrar um cliente para notificações como parte de seu processo de inicialização.
    
- [Cancelando uma notificação:](canceling-a-notification.md)descreve como cancelar uma assinatura para uma notificação.
    
- [Manipulação de notificação do armazenamento](handling-message-store-notification.md)de mensagens: descreve como registrar-se para notificações do armazenamento de mensagens.
    
- [Handing Address Book Notification](handing-address-book-notification.md): Descreve como registrar e manipular notificações do livro de endereços.
    
- [Manipulação de notificação de](handling-table-notification.md)tabela: descreve como registrar para notificações da tabela de hierarquia.
    
- [Implementando um objeto Sink advise:](implementing-an-advise-sink-object.md)descreve como implementar um objeto sink de aconselhá-lo.
    
- [Tempo de uma notificação:](timing-a-notification.md)descreve o tempo de notificação do cliente pelos provedores de serviços.
    
- [Garantir uma notificação Thread-Safe:](ensuring-a-thread-safe-notification.md)descreve como garantir a notificação de thread-safe com MAPI.
    
- [Forçar uma notificação:](forcing-a-notification.md)descreve como forçar uma notificação em MAPI.
    

