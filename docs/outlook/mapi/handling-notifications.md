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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299381"
---
# <a name="handling-notifications"></a>Manipular notificações

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
As notificações permitem que um objeto informe a outro objeto que passou por uma alteração. O tipo de alteração é conhecido como um evento. O MAPI define vários eventos para os quais as notificações são geradas. 
  
Os clientes normalmente se registram em um ou mais eventos com um ou mais objetos. Esses objetos são chamados de fontes de aviso. Os objetos que podem atuar como fontes de aviso incluem o objeto Session, no controle MAPI ou um objeto criado por um provedor de serviços, como uma mensagem. O objeto informado, chamado de coletor de aviso, contém uma implementação da interface [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) ou da interface [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) e está dentro de um aplicativo cliente. 
  
Avisar os objetos de origem implementam um método **Advise** , que é chamado por clientes para se registrarem para notificações, e um método **Unadvise** , que é chamado para cancelar um registro. Um dos parâmetros a serem **aconselhados** é um ponteiro para uma implementação de **IMAPIAdviseSink** ou * * IMAPIViewAdviseSink * *. A fonte de aviso armazena esse ponteiro para que ele possa chamar [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) ou um dos métodos no **IMAPIViewAdviseSink** quando ocorre uma alteração. 
  
Como as notificações de recebimento permitem que os usuários vejam as informações mais atualizadas, é recomendável que todos os clientes registrem e manipulem notificações. No enTanto, é opcional.
  
## <a name="in-this-section"></a>Nesta seção

- [Registro de uma notificação](registering-for-a-notification.md): descreve como registrar um cliente para notificações como parte do processo de inicialização.
    
- [Cancelar uma notificação](canceling-a-notification.md): descreve como cancelar uma assinatura para uma notificação.
    
- [Tratamento de notificação do repositório de mensagens](handling-message-store-notification.md): descreve como se registrar para notificações de repositório de mensagens.
    
- [Envio da notificação do catálogo de endereços](handing-address-book-notification.md): descreve como registrar e lidar com notificações do catálogo de endereços.
    
- [Tratamento da notificação de tabela](handling-table-notification.md): descreve como se registrar para notificações da tabela de hierarquia.
    
- [Implementar um objeto de coletor de aviso](implementing-an-advise-sink-object.md): descreve como implementar um objeto de coletor de aviso.
    
- [Cronometrar uma notificação](timing-a-notification.md): descreve o intervalo de notificação de cliente por provedores de serviços.
    
- [Garantir uma notificação segura para thread](ensuring-a-thread-safe-notification.md): descreve como garantir a notificação segura para thread com MAPI.
    
- [Forçar uma notificação](forcing-a-notification.md): descreve como forçar uma notificação em MAPI.
    

