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
ms.openlocfilehash: ea72a6fd2a22fe87ad63bb9c8fa6c1416d876b66
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564245"
---
# <a name="iablogonadvise"></a>IABLogon::Advise

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Registra o chamador para receber notificações de eventos especificados que afetam um contêiner, o usuário ou lista de distribuição de mensagens.
  
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
  
> [in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Um ponteiro para o identificador de entrada do objeto notificações sobre quais devem ser geradas.
    
 _ulEventMask_
  
> [in] Uma bitmask dos valores que indicam os tipos de eventos de notificação que o chamador está interessado em e deve ser incluído no registro. Há uma estrutura de [notificação](notification.md) correspondente associada a cada tipo de evento que contém informações sobre o evento. A tabela a seguir lista os valores válidos para o parâmetro _ulEventMask_ e as estruturas associadas a cada valor. 
    
|**Tipo de evento de notificação**|**Estrutura de **notificação** correspondente**|
|:-----|:-----|
|**fnevCriticalError** <br/> |[ERROR_NOTIFICATION](error_notification.md) <br/> |
|**fnevObjectCreated** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectDeleted** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectModified** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectCopied** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectMoved** <br/> |**OBJECT_NOTIFICATION** <br/> |
   
 _lpAdviseSink_
  
> [in] Um ponteiro para um objeto de coletor de eventos advise para receber as notificações subsequentes.
    
 _lpulConnection_
  
> [out] Um ponteiro para um valor diferente de zero que representa o registro de notificação.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O registro de notificação foi bem-sucedida.
    
MAPI_E_INVALID_ENTRYID 
  
> O identificador de entrada passado no parâmetro _lpEntryID_ não está no formato apropriado. 
    
MAPI_E_NO_SUPPORT 
  
> O provedor de catálogo de endereços não suporta notificação, possivelmente porque não permitem que as alterações sejam feitas para seus objetos.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> O provedor de catálogo de endereços não pode manipular o identificador de entrada passado _lpEntryID_.
    
## <a name="remarks"></a>Comentários

Provedores de catálogo de endereços implementam o método **IABLogon::Advise** para registrar o chamador para ser notificado quando ocorre uma alteração a um objeto em um dos seus contêineres. Os chamadores podem registrar para notificações sobre todo contêineres, listas de distribuição ou mensagens de usuários. 
  
Normalmente, os clientes chame o método de [IAddrBook::Advise](iaddrbook-advise.md) para registrar para notificações do catálogo de endereços. MAPI chama o método **Advise** do provedor de catálogo de endereços que é responsável pelo objeto representado pelo identificador de entrada no _lpEntryID_.
  
Quando ocorre uma alteração ao objeto do tipo representado na _ulEventMask_indicado, é feita uma chamada para o método **OnNotify** do coletor advise apontado pela _lpAdviseSink_. Dados passados na estrutura de **notificação** para a rotina de **OnNotify** descrevem o evento. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Você pode oferecer suporte a notificação com ou sem a Ajuda de MAPI. MAPI tem três métodos do objeto de suporte para ajudar a implementar a notificação de provedores de serviços:
  
- [IMAPISupport::Subscribe](imapisupport-subscribe.md)
    
- [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)
    
- [IMAPISupport::Notify](imapisupport-notify.md)
    
Se você optar por usar os métodos de suporte MAPI, ligue para **inscrever-se** ao seu método **Advise** é chamado e liberar o ponteiro _lpAdviseSink_ . 
  
Se você optar por suporte a notificação, chame o método de **AddRef** do coletor advise representado pelo parâmetro _lpAdviseSink_ para manter uma cópia deste ponteiro. Manter essa cópia até seu método [IABLogon::Unadvise](iablogon-unadvise.md) é chamado para cancelar o registro. 
  
Independentemente de como você oferecer suporte à notificação, atribua um número diferente de zero de conexão para o registro de notificação e retorná-lo no parâmetro _lpulConnection_ . Não libere esse número de conexão até que o método **Unadvise** foi chamado. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

O ponteiro advise do coletor de eventos que você passa no parâmetro _lpAdviseSink_ para **Advise** pode apontar para um objeto que você criou ou que MAPI criado por meio da função [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) . Você talvez queira usar **HrThisThreadAdviseSink** se você oferecer suporte a vários threads de execução e deseja Certifique-se de que as chamadas subsequentes para seu método de **OnNotify** ocorram em um horário adequado em um segmento apropriado. 
  
Esteja preparado para seu objeto de coletor de eventos advise ser liberada a qualquer momento após sua chamada **Advise** e antes de chamar **Unadvise**. Portanto, você deve liberar seu objeto de coletor de eventos advise depois **Advise** retorna, a menos que tenha um uso específico de longo prazo para ele. 
  
Para obter mais informações sobre o processo de notificação, consulte [Notificação de evento em MAPI](event-notification-in-mapi.md). Para obter informações sobre como usar os métodos **IMAPISupport** para oferecer suporte a notificação, consulte [Suporte a notificação de evento](supporting-event-notification.md). Para obter mais informações sobre multithreading e MAPI, consulte [Threading in MAPI](threading-in-mapi.md).
  
## <a name="see-also"></a>Confira também



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IABLogon::Unadvise](iablogon-unadvise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[NOTIFICAÇÃO](notification.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

