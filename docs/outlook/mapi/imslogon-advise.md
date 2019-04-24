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
  
Registra um objeto com um provedor de repositório de mensagens para notificações sobre alterações no repositório de mensagens. O repositório de mensagens enviará notificações sobre alterações no objeto registrado.
  
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
  
> no O tamanho, em bytes, do identificador de entrada apontado pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
> no Um ponteiro para o identificador de entrada do objeto sobre quais notificações devem ser geradas. Este objeto pode ser uma pasta, uma mensagem ou qualquer outro objeto no repositório de mensagens. Como alternativa, se MAPI define o parâmetro _cbEntryID_ como 0 e passa **NULL** para _lpEntryID_, o coletor de avisos fornece notificações sobre alterações em todo o repositório de mensagens.
    
 _ulEventMask_
  
> no Uma máscara de evento dos tipos de eventos de notificação que ocorrem para o objeto sobre o qual o MAPI irá gerar notificações. A máscara filtra casos específicos. Cada tipo de evento tem uma estrutura associada a ele que contém informações adicionais sobre o evento. A tabela a seguir lista os possíveis tipos de evento juntamente com suas estruturas correspondentes.
    
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
  
> no Um ponteiro para um objeto de coletor de aviso a ser chamado quando ocorre um evento para o objeto Session sobre o qual a notificação foi solicitada. Este objeto de coletor de aviso já deve existir.
    
 _lpulConnection_
  
> bota Um ponteiro para uma variável que em um retorno bem-sucedido contém o número de conexão para o registro de notificação. O número de conexão deve ser diferente de zero.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
MAPI_E_NO_SUPPORT 
  
> A operação não é suportada pelo MAPI ou por um ou mais provedores de serviços.
    
## <a name="remarks"></a>Comentários

Os provedores de repositórios de mensagens implementam o método **IMSLogon:: Advise** para registrar um objeto para retornos de chamada de notificação. Sempre que uma alteração ocorre no objeto indicado, o provedor verifica se o bit de máscara de evento foi definido no parâmetro _ulEventMask_ e, portanto, que tipo de alteração ocorreu. Se um bit for definido, o provedor chamará o método [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) para o objeto de coletor de aviso indicado pelo parâmetro _lpAdviseSink_ para relatar o evento. Dados passados na estrutura de notificação para a **** rotina OnNotify descreve o evento. 
  
A chamada para **OnNotify** pode ocorrer durante a chamada que altera o objeto ou em qualquer momento posterior. Em sistemas que oferecem suporte a vários threads de execução, **** a chamada para OnNotify pode ocorrer em qualquer thread. Para lidar com segurança uma chamada para **** onnotificar que pode ocorrer em um momento de inopportune, um aplicativo cliente deve usar a função [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) . 
  
Para fornecer notificações, o provedor de repositório de mensagens que implementa o **aviso** precisa manter uma cópia do ponteiro para o objeto de coletor de aviso _lpAdviseSink_ ; para fazer isso, o provedor chama o método [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) para o coletor de avisos para manter seu ponteiro de objeto até que o registro de notificação seja cancelado com uma chamada para o método [IMSLogon:: Unadvise](imslogon-unadvise.md) . A implementação de **aviso** deve atribuir um número de conexão ao registro de notificação e chamar **AddRef** nesse número de conexão antes de devolvê-lo no parâmetro _lpulConnection_ . Os provedores de serviços podem liberar o objeto de coletor de aviso antes de o registro ser cancelado, mas não devem liberar o número de conexão até que **Unadvise** seja chamado. 
  
Após uma chamada a **Advise** ter sido bem-sucedida e antes que **Unadvise** seja chamado, os provedores devem estar preparados para que o objeto de coletor de aviso seja liberado. Portanto, um provedor deve liberar seu objeto de coletor de aviso depois que **Advise** retornar, a menos que tenha um uso específico de longo prazo para ele. 
  
Para obter mais informações sobre o processo de notificação, consulte [Event Notification in MAPI](event-notification-in-mapi.md). 
  
## <a name="see-also"></a>Confira também



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMSLogon::Unadvise](imslogon-unadvise.md)
  
[NOTIFICATION](notification.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

