---
title: IAddrBookAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.Advise
api_type:
- COM
ms.assetid: 2def89ed-e4ce-446a-8b80-132d11ae8f8b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7abafafd3d4bd9618d85a7dac34e4556545167bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406273"
---
# <a name="iaddrbookadvise"></a>IAddrBook::Advise

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Registra um cliente ou provedor de serviços para receber notificações sobre alterações em uma ou mais entradas no livro de endereços.
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a>Parâmetros

 _cbEntryID_
  
> [in] A contagem de byte no identificador de entrada apontado pelo parâmetro _lpEntryID._ 
    
 _lpEntryID_
  
> [in] Um ponteiro para o identificador de entrada do contêiner do address book, do usuário de mensagens ou da lista de distribuição que gerará uma notificação quando ocorrer uma alteração do tipo ou dos tipos descritos no _parâmetro ulEventMask._ 
    
 _ulEventMask_
  
> [in] Um ou mais eventos de notificação que o chamador está se registrando para receber. Cada evento é associado a uma estrutura de notificação específica que contém informações sobre a alteração que ocorreu. A tabela a seguir lista os valores válidos para  _ulEventMask_ e suas estruturas correspondentes. 
    
|**Evento de notificação**|**Estrutura correspondente**|
|:-----|:-----|
|**fnevCriticalError** <br/> |[ERROR_NOTIFICATION](error_notification.md) <br/> |
|**fnevObjectCreated** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectDeleted** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectModified** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectCopied** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectMoved** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevTableModified** <br/> |[TABLE_NOTIFICATION](table_notification.md) <br/> |
   
 _lpAdviseSink_
  
> [in] Um ponteiro para o objeto sink de aviso a ser chamado quando o evento para o qual a notificação foi solicitada ocorre.
    
 _lpulConnection_
  
> [out] Um ponteiro para um número de conexão que não seja zero que representa o registro de notificação.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O registro de notificação foi bem-sucedido.
    
MAPI_E_INVALID_ENTRYID 
  
> O provedor de agendamento responsável pelo identificador de entrada passado  _em lpEntryID_ não pôde registrar uma notificação para a entrada correspondente. 
    
MAPI_E_NO_SUPPORT 
  
> A notificação não é suportada pelo provedor de agendas responsável pelo objeto identificador de entrada passado no _parâmetro lpEntryID._ 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> O identificador de entrada passado  _em lpEntryID_ não pode ser manipulado por nenhum dos provedores de agendas no perfil. 
    
## <a name="remarks"></a>Comentários

Os clientes e provedores de serviços chamam o **método Advise** para se registrar para um tipo específico ou tipos de notificação em uma entrada do livro de endereços. Os tipos de notificação são indicados pela máscara de evento passada com o _parâmetro ulEventMask._ 
  
MAPI forwards this **Advise** call to the address book provider that is responsible for the entry as indicated by the entry identifier in the  _lpEntryID_ parameter. O provedor de agendamento de endereço trata o registro em si ou chama o método de suporte, [IMAPISupport::Subscribe](imapisupport-subscribe.md), para solicitar MAPI para registrar o chamador. Um número de conexão que não seja zero é retornado para representar o registro bem-sucedido.
  
Sempre que ocorre uma alteração na entrada do tipo indicado pelo registro de notificação, o provedor de agendamento chama o método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) para o objeto sink de aviso especificado no parâmetro _lpAdviseSink._ O **método OnNotify** inclui uma estrutura [NOTIFICATION](notification.md) como um parâmetro de entrada que contém dados para descrever o evento. 
  
Dependendo do provedor de agendamento de endereços, a chamada para **OnNotify** pode ocorrer imediatamente após a alteração no objeto registrado ou posteriormente. Em sistemas que suportam vários threads de execução, a chamada para **OnNotify** pode ocorrer em qualquer thread. Os clientes podem solicitar que essas notificações ocorram em um thread específico chamando a função [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) para criar o objeto de evento de aviso que é passado para **Advise**. 
  
Como um provedor de livro de endereços pode liberar o objeto de  evento de aviso passado pelos clientes a qualquer momento após a conclusão bem-sucedida  da chamada advise e antes de uma chamada [IAddrBook::Unadvise](iaddrbook-unadvise.md) para cancelar a notificação, os clientes devem liberar seus objetos de evento de aviso quando Advise retorna. 
  
Para obter mais informações sobre o processo de notificação, consulte [Notificação de Evento em MAPI](event-notification-in-mapi.md).
  
## <a name="see-also"></a>Confira também



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IAddrBook::Unadvise](iaddrbook-unadvise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[NOTIFICAÇÃO](notification.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

