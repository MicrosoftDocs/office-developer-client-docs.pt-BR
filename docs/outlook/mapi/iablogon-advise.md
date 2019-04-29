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
  
Registra o chamador para receber notificações de eventos específicos que afetam um contêiner, usuário de mensagens ou lista de distribuição.
  
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
  
> no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
> no Um ponteiro para o identificador de entrada do objeto sobre quais notificações devem ser geradas.
    
 _ulEventMask_
  
> no Uma máscara de valores que indica os tipos de eventos de notificação nos quais o chamador está interessado e deve ser incluído no registro. Há uma estrutura de [notificação](notification.md) correspondente associada a cada tipo de evento que contém informações sobre o evento. A tabela a seguir lista os valores válidos para o parâmetro _ulEventMask_ e as estruturas associadas a cada valor. 
    
|**Tipo de evento de notificação**|**Estrutura de **notificação** correspondente**|
|:-----|:-----|
|**fnevCriticalError** <br/> |[ERROR_NOTIFICATION](error_notification.md) <br/> |
|**fnevObjectCreated** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectDeleted** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectModified** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectCopied** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectMoved** <br/> |**OBJECT_NOTIFICATION** <br/> |
   
 _lpAdviseSink_
  
> no Um ponteiro para um objeto de coletor de aviso para receber as notificações subsequentes.
    
 _lpulConnection_
  
> bota Um ponteiro para um valor diferente de zero que representa o registro de notificação.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O registro de notificação foi bem-sucedido.
    
MAPI_E_INVALID_ENTRYID 
  
> O identificador de entrada passado no parâmetro _lpEntryID_ não está no formato apropriado. 
    
MAPI_E_NO_SUPPORT 
  
> O provedor de catálogo de endereços não oferece suporte a notificações, possivelmente porque não permite que as alterações sejam feitas em seus objetos.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> O provedor de catálogo de endereços não pode lidar com o identificador de entrada passado no _lpEntryID_.
    
## <a name="remarks"></a>Comentários

Os provedores de catálogo de endereços implementam o método **IABLogon:: Advise** para registrar o chamador para ser notificado quando uma alteração ocorre para um objeto em um de seus contêineres. Os chamadores podem se registrar para obter notificações sobre usuários de mensagens, listas de distribuição ou contêineres inteiros. 
  
Normalmente, os clientes chamam o método [IAddrBook:: Advise](iaddrbook-advise.md) para registrar notificações do catálogo de endereços. Em seguida, o MAPI chama o método **Advise** do provedor de catálogo de endereços responsável pelo objeto representado pelo identificador de entrada no _lpEntryID_.
  
Quando uma alteração ocorre para o objeto indicado do tipo representado no _ulEventMask_, uma chamada é feita ao método OnNotify do coletor de avisos apontado por _lpAdviseSink_. **** Dados passados na estrutura de **notificação** para a **** rotina OnNotify descreve o evento. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Você pode dar suporte à notificação com ou sem a ajuda do MAPI. O MAPI tem três métodos de objeto de suporte para ajudar os provedores de serviços a implementar a notificação:
  
- [IMAPISupport::Subscribe](imapisupport-subscribe.md)
    
- [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)
    
- [IMAPISupport::Notify](imapisupport-notify.md)
    
Se você optar por usar os métodos de suporte MAPI, chame **Subscribe** quando seu método **Advise** for chamado e libere o ponteiro _lpAdviseSink_ . 
  
Se você optar por dar suporte a uma notificação por conta própria, chame o método **AddRef** do coletor de avisos representado pelo parâmetro _lpAdviseSink_ para manter uma cópia desse ponteiro. Mantenha essa cópia até que o método [IABLogon:: Unadvise](iablogon-unadvise.md) seja chamado para cancelar o registro. 
  
Independentemente de como você dá suporte à notificação, atribua um número de conexão diferente de zero para o registro de notificação e devolva-o no parâmetro _lpulConnection_ . Não libere esse número de conexão até que o método **Unadvise** tenha sido chamado. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

O ponteiro de coletor de aviso que você passa no parâmetro _lpAdviseSink_ para **avisar** pode apontar para um objeto que você criou ou que o MAPI criou através da função [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) . Você pode querer usar **HrThisThreadAdviseSink** se você dá suporte a vários threads de execução e quer ter certeza de que as chamadas subsequentes para seu método OnNotify ocorram em um momento apropriado em um thread apropriado. **** 
  
Prepare-se para o seu objeto de coletor de aviso a ser liberado a qualquer momento após a chamada para **avisar** e antes da chamada para **Unadvise**. Portanto, você deve liberar seu objeto de coletor de **** aviso após a revisor, a menos que tenha um uso específico de longo prazo para ele. 
  
Para obter mais informações sobre o processo de notificação, consulte [Event Notification in MAPI](event-notification-in-mapi.md). Para obter informações sobre como usar os métodos **IMAPISupport** para dar suporte à notificação, consulte [support Event Notification](supporting-event-notification.md). Para obter mais informações sobre multithreading e MAPI, consulte [Threading in MAPI](threading-in-mapi.md).
  
## <a name="see-also"></a>Confira também



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IABLogon::Unadvise](iablogon-unadvise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[Notifica](notification.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

