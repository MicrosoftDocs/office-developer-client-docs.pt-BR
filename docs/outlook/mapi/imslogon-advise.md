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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382754"
---
# <a name="imslogonadvise"></a>IMSLogon::Advise

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Registra um objeto com um provedor de armazenamento de mensagem para notificações sobre alterações no armazenamento de mensagens. O armazenamento de mensagens, em seguida, enviará notificações sobre alterações ao objeto registrado.
  
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
  
> [in] O tamanho, em bytes, do identificador de entrada apontado pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Um ponteiro para o identificador de entrada do objeto notificações sobre quais devem ser geradas. Este objeto pode ser uma pasta, uma mensagem ou qualquer outro objeto no repositório de mensagem. Como alternativa, se MAPI define o parâmetro _cbEntryID_ como 0 e passa **Nulo** para _lpEntryID_, o coletor de eventos advise fornece notificações sobre alterações no repositório de toda a mensagem.
    
 _ulEventMask_
  
> [in] Uma máscara de evento dos tipos de eventos de notificação que ocorrem para o objeto sobre quais MAPI irá gerar notificações. A máscara filtra casos específicos. Cada tipo de evento tem uma estrutura associada a ela que contém informações adicionais sobre o evento. A tabela a seguir lista os tipos de evento possíveis, juntamente com suas estruturas correspondentes.
    
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
  
> [in] Um ponteiro para um objeto de coletor de eventos advise a ser chamado quando ocorre um evento para o objeto de sessão notificação sobre quais tiver sido solicitada. Este objeto de coletor de eventos advise já deve existir.
    
 _lpulConnection_
  
> [out] Um ponteiro para uma variável que contém o número de conexão para o registro de notificação após um retorno bem-sucedido. O número de conexão deve ser diferente de zero.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
MAPI_E_NO_SUPPORT 
  
> A operação não é suportada por MAPI ou por um ou mais provedores de serviço.
    
## <a name="remarks"></a>Comentários

Provedores de armazenamento de mensagem implementam o método **IMSLogon::Advise** para registrar um objeto para retornos de chamada de notificação. Sempre que ocorre uma alteração no objeto indicado, o provedor verifica quais bits de máscara de evento foi definida no parâmetro _ulEventMask_ e, portanto, o tipo de alteração que ocorreu. Se um pouco estiver definida, o provedor chama o método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) para o objeto coletor de eventos de advise indicado pelo parâmetro _lpAdviseSink_ para relatar o evento. Dados passados na estrutura de notificação para a rotina de **OnNotify** descrevem o evento. 
  
A chamada para **OnNotify** pode ocorrer durante a chamada que altera o objeto ou a qualquer momento posterior. Nos sistemas que oferecem suporte a vários threads de execução, a chamada para **OnNotify** pode ocorrer em qualquer segmento. Para manipular com segurança uma chamada para **OnNotify** que pode acontecer momento inoportunos, um aplicativo cliente deve usar a função [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) . 
  
Para fornecer notificações, o provedor de armazenamento de mensagem que implementa as necessidades de **Advise** manter uma cópia do ponteiro para o _lpAdviseSink_ avise o objeto coletor de eventos; Para fazer isso, o provedor chama o método de [AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) para o coletor de eventos advise manter seu indicador de objeto até que o registro de notificação será cancelado com uma chamada ao método [IMSLogon::Unadvise](imslogon-unadvise.md) . A implementação de **Advise** deve atribuir um número de conexão para o registro de notificação e chamar **AddRef** este número de conexão antes de retorná-lo no parâmetro _lpulConnection_ . Provedores de serviços podem liberar o objeto coletor de eventos advise antes que o registro será cancelado, mas eles não devem liberar o número de conexão até que tenha sido chamado **Unadvise** . 
  
Depois que uma chamada para **Advise** teve sucesso e antes de **Unadvise** tiver sido chamado, provedores devem ser preparados para o objeto coletor de eventos de advise ser liberada. Portanto, um provedor deve liberar seu objeto de coletor advise depois **Advise** retorna, a menos que ele tem um uso específico de longo prazo para que ele. 
  
Para obter mais informações sobre o processo de notificação, consulte [Notificação de evento em MAPI](event-notification-in-mapi.md). 
  
## <a name="see-also"></a>Confira também



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMSLogon::Unadvise](imslogon-unadvise.md)
  
[NOTIFICATION](notification.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

