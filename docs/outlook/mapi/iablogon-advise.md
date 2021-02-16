---
title: IABLogonAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.Advise
api_type:
- COM
ms.assetid: 375d65b1-607d-4e2a-8052-9bcbf08fc2ac
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 4ab0e4b023e6af19f650abf421aed122dcc21879
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428225"
---
# <a name="iablogonadvise"></a>IABLogon::Advise

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Registra o chamador para receber notificação de eventos especificados que afetam um contêiner, um usuário de mensagens ou uma lista de distribuição.
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a>Parâmetros

 _cbEntryID_
  
> [in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID._ 
    
 _lpEntryID_
  
> [in] Um ponteiro para o identificador de entrada do objeto sobre o qual as notificações devem ser geradas.
    
 _ulEventMask_
  
> [in] Uma bitmask de valores que indicam os tipos de eventos de notificação nos quais o chamador está interessado e devem ser incluídos no registro. Há uma estrutura [notification](notification.md) correspondente associada a cada tipo de evento que contém informações sobre o evento. A tabela a seguir lista os valores válidos para o  _parâmetro ulEventMask_ e as estruturas associadas a cada valor. 
    
|**Tipo de evento de notificação**|**Estrutura **NOTIFICATION** correspondente**|
|:-----|:-----|
|**fnevCriticalError** <br/> |[ERROR_NOTIFICATION](error_notification.md) <br/> |
|**fnevObjectCreated** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectDeleted** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectModified** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectCopied** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectMoved** <br/> |**OBJECT_NOTIFICATION** <br/> |
   
 _lpAdviseSink_
  
> [in] Um ponteiro para um objeto sink de aviso para receber as notificações subsequentes.
    
 _lpulConnection_
  
> [out] Um ponteiro para um valor que não é zero que representa o registro de notificação.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O registro de notificação foi bem-sucedido.
    
MAPI_E_INVALID_ENTRYID 
  
> O identificador de entrada passado no  _parâmetro lpEntryID_ não está no formato apropriado. 
    
MAPI_E_NO_SUPPORT 
  
> O provedor de agendas não dá suporte à notificação, possivelmente porque não permite que as alterações sejam feitas em seus objetos.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> O provedor de agendas não pode manipular o identificador de entrada passado em  _lpEntryID_.
    
## <a name="remarks"></a>Comentários

Os provedores de agendamento implementam o método **IABLogon::Advise** para registrar o chamador a ser notificado quando ocorre uma alteração em um objeto em um de seus contêineres. Os chamadores podem se registrar para receber notificações sobre usuários de mensagens, listas de distribuição ou contêineres inteiros. 
  
Os clientes normalmente chamam o [método IAddrBook::Advise](iaddrbook-advise.md) para se registrar para notificações do address book. MAPI then calls the **Advise** method of the address book provider that is responsible for the object represented by the entry identifier in  _lpEntryID_.
  
When a change occurs to the indicated object of the type represented in  _ulEventMask_, a call is made to the **OnNotify** method of the advise sink pointed to by  _lpAdviseSink_. Os dados passados **na estrutura NOTIFICATION** para a rotina **OnNotify** descrevem o evento. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Você pode dar suporte à notificação com ou sem ajuda do MAPI. O MAPI tem três métodos de objeto de suporte para ajudar os provedores de serviços a implementar a notificação:
  
- [IMAPISupport::Subscribe](imapisupport-subscribe.md)
    
- [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)
    
- [IMAPISupport::Notify](imapisupport-notify.md)
    
Se você optar por usar os métodos de suporte MAPI, chame **Subscribe** quando o método **Advise** for chamado e libere o ponteiro _lpAdviseSink._ 
  
Se você optar por dar suporte à notificação por conta própria, chame o método **AddRef** do sink de aviso representado pelo parâmetro  _lpAdviseSink_ para manter uma cópia desse ponteiro. Mantenha essa cópia até que o [método IABLogon::Unadvise](iablogon-unadvise.md) seja chamado para cancelar o registro. 
  
Independentemente de como você suporta a notificação, atribua um número de conexão não zero ao registro de notificação e retorne-o no parâmetro _lpulConnection._ Não libere esse número de conexão até que **o método Unadvise** tenha sido chamado. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

O ponteiro do pia de avisar que você passa no parâmetro _lpAdviseSink_ para **Advise** pode apontar para um objeto que você criou ou que MAPI criou por meio da função [HrThisThreadAdviseSink.](hrthisthreadadvisesink.md) Talvez você queira usar **HrThisThreadAdviseSink** se tiver suporte para vários threads de execução e quiser ter certeza de que as chamadas subsequentes para o método **OnNotify** ocorram em um horário apropriado em um thread apropriado. 
  
Esteja preparado para que seu objeto sink de aconselhá-lo seja liberado a qualquer momento após sua chamada para **Advise** e antes de sua chamada para **Unadvise**. Portanto, você deve liberar seu objeto sink de aconselhá-lo após o retorno de **Advise,** a menos que você tenha um uso específico a longo prazo para ele. 
  
Para obter mais informações sobre o processo de notificação, consulte [Notificação de Evento em MAPI](event-notification-in-mapi.md). For information about how to use the **IMAPISupport** methods to support notification, see [Supporting Event Notification](supporting-event-notification.md). Para obter mais informações sobre multithreading e MAPI, consulte [Threading em MAPI](threading-in-mapi.md).
  
## <a name="see-also"></a>Confira também



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IABLogon::Unadvise](iablogon-unadvise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[NOTIFICAÇÃO](notification.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

