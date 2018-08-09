---
title: Manipular notificações
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 451b71da-a888-4d8f-9814-12f9f846de05
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: fdd66e4a27209e6b80757bcf52408eb0cea43794
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766675"
---
# <a name="handling-notifications"></a>Manipular notificações

**Aplica-se a**: Outlook 
  
Notificações de habilitar um objeto para informar outro objeto que ele passou por uma alteração. O tipo de alteração é conhecido como um evento. MAPI define vários eventos para o qual as notificações são geradas. 
  
Clientes geralmente registrar para um ou mais eventos com um ou mais objetos. Esses objetos são conhecidos como fontes de aviso. Os objetos que podem atuar como fontes de aviso incluem o objeto de sessão, sob o controle do MAPI ou um objeto criado por um provedor de serviço, como uma mensagem. O objeto informado, conhecido como o coletor de advise, contém qualquer uma implementação do [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) interface ou o [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) interface e está contido em um aplicativo cliente. 
  
Objetos de origem Advise implementam um método **Advise** , que é chamado pelos clientes para registrar para notificações e um método **Unadvise** , que é chamado para cancelar um registro. Um dos parâmetros para **Advise** é um ponteiro para uma implementação do **IMAPIAdviseSink** ou * * IMAPIViewAdviseSink * *. A fonte de advise caches esse ponteiro para que ele possa chamar [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) ou um dos métodos em **IMAPIViewAdviseSink** quando ocorre uma alteração. 
  
Como receber notificações permite aos usuários exibir as informações mais atualizadas, é recomendável que todos os clientes se registrar e manipular notificações. No entanto, é opcional.
  
## <a name="in-this-section"></a>Nesta seção

- [Registrando uma notificação](registering-for-a-notification.md): descreve como registrar um cliente para notificações como parte do seu processo de inicialização.
    
- [Cancelamento de uma notificação](canceling-a-notification.md): descreve como cancelar uma assinatura para uma notificação.
    
- [Notificação de armazenar de mensagem manipulação](handling-message-store-notification.md): descreve como registrar para notificações do repositório de mensagens.
    
- [Notificação de catálogo de endereço de manusear](handing-address-book-notification.md): descreve como se registrar e manipular notificações de catálogo de endereços.
    
- [Notificação de tabela manipulação](handling-table-notification.md): descreve como registrar para notificações da tabela de hierarquia.
    
- [Implementação de um objeto de coletor de eventos de aviso](implementing-an-advise-sink-object.md): descreve como implementar um objeto de coletor de eventos advise.
    
- [Uma notificação de intervalos](timing-a-notification.md): descreve a temporização da notificação de cliente por provedores de serviços.
    
- [Garantindo que uma notificação de Thread-Safe](ensuring-a-thread-safe-notification.md): descreve como garantir a notificação de thread-safe com MAPI.
    
- [Forçar uma notificação](forcing-a-notification.md): descreve como forçar uma notificação de MAPI.
    

