---
title: IMSLogonAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.Advise
api_type:
- COM
ms.assetid: a3c5d937-642b-463b-b5a0-5d099e651895
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: abe4867b965f05e781f931d2e72920474d007d78
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317308"
---
# <a name="imslogonadvise"></a>IMSLogon::Advise

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Registra um objeto com um provedor de armazenamento de mensagens para notificações sobre alterações no armazenamento de mensagens. Em seguida, o armazenamento de mensagens enviará notificações sobre alterações no objeto registrado.
  
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
  
> [in] O tamanho, em bytes, do identificador de entrada apontado pelo parâmetro _lpEntryID._ 
    
 _lpEntryID_
  
> [in] Um ponteiro para o identificador de entrada do objeto sobre o qual as notificações devem ser geradas. Esse objeto pode ser uma pasta, uma mensagem ou qualquer outro objeto no armazenamento de mensagens. Como alternativa, se MAPI define o parâmetro _cbEntryID_ como 0 e passa nulo para  _lpEntryID_, o sink de aviso fornece notificações sobre alterações em todo o armazenamento de mensagens.
    
 _ulEventMask_
  
> [in] Uma máscara de evento dos tipos de eventos de notificação que ocorrem para o objeto sobre o qual o MAPI gerará notificações. A máscara filtra casos específicos. Cada tipo de evento tem uma estrutura associada a ela que contém informações adicionais sobre o evento. A tabela a seguir lista os possíveis tipos de eventos juntamente com suas estruturas correspondentes.
    
|**Tipo de evento de notificação**|**Estrutura correspondente**|
|:-----|:-----|
|fnevCriticalError  <br/> |[ERROR_NOTIFICATION](error_notification.md) <br/> |
|fnevNewMail  <br/> |[NEWMAIL_NOTIFICATION](newmail_notification.md) <br/> |
|fnevObjectCreated  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevObjectDeleted  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevObjectModified  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevObjectCopied  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevObjectMoved  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevSearchComplete  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevStatusObjectModified  <br/> |[STATUS_OBJECT_NOTIFICATION](status_object_notification.md) <br/> |
   
 _lpAdviseSink_
  
> [in] Um ponteiro para um objeto sink de aviso a ser chamado quando ocorre um evento para o objeto de sessão sobre o qual a notificação foi solicitada. Esse objeto de pia de aconselhmento já deve existir.
    
 _lpulConnection_
  
> [out] Um ponteiro para uma variável que, após um retorno bem-sucedido, contém o número de conexão para o registro de notificação. O número da conexão deve ser não zero.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
MAPI_E_NO_SUPPORT 
  
> A operação não é suportada por MAPI ou por um ou mais provedores de serviços.
    
## <a name="remarks"></a>Comentários

Os provedores de armazenamento de mensagens implementam o **método IMSLogon::Advise** para registrar um objeto para retornos de chamada de notificação. Sempre que ocorre uma alteração no objeto indicado, o provedor verifica qual bit da máscara de eventos foi definido no parâmetro  _ulEventMask_ e, portanto, qual tipo de alteração ocorreu. Se um bit for definido, o provedor chamará o método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) para o objeto sink advise indicado pelo parâmetro  _lpAdviseSink_ para relatar o evento. Os dados passados na estrutura de notificação para a **rotina OnNotify** descrevem o evento. 
  
A chamada para **OnNotify** pode ocorrer durante a chamada que altera o objeto ou a qualquer momento posterior. Em sistemas que suportam vários threads de execução, a chamada para **OnNotify** pode ocorrer em qualquer thread. Para manipular com segurança uma chamada para **OnNotify** que pode acontecer em um momento inoportuno, um aplicativo cliente deve usar a função [HrThisThreadAdviseSink.](hrthisthreadadvisesink.md) 
  
Para fornecer notificações, o provedor de armazenamento de mensagens que implementa **Advise** precisa manter uma cópia do ponteiro para o objeto _sink de aviso lpAdviseSink;_ para fazer isso, o provedor chama o método [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) para o sink de aviso manter seu ponteiro de objeto até que o registro de notificação seja cancelado com uma chamada para o método [IMSLogon::Unadvise.](imslogon-unadvise.md) A **implementação de** Aviso deve atribuir um número de conexão ao registro de notificação e chamar **AddRef** nesse número de conexão antes de reenvolvê-lo no parâmetro _lpulConnection._ Os provedores de serviços podem liberar o objeto de cliente de alerta antes que o registro seja cancelado, mas não devem liberar o número de conexão até que **Unadvise** seja chamado. 
  
Depois que uma chamada para **o Advise** tiver sido bem-sucedida e antes de **Unadvise** ter sido chamada, os provedores devem estar preparados para que o objeto de sink de aconselhá-lo seja liberado. Portanto, um provedor deve liberar seu objeto de aconselhá-lo depois que **Advise** retornar, a menos que ele tenha um uso específico a longo prazo para ele. 
  
Para obter mais informações sobre o processo de notificação, consulte [Notificação de Evento em MAPI](event-notification-in-mapi.md). 
  
## <a name="see-also"></a>Confira também



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMSLogon::Unadvise](imslogon-unadvise.md)
  
[NOTIFICAÇÃO](notification.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

