---
title: IMsgStoreAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.Advise
api_type:
- COM
ms.assetid: 8c57e743-a798-4e39-a61a-46dff8b1ac7c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3b4abef731541e308b2c2ebc6f4aaddf4458e257
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317322"
---
# <a name="imsgstoreadvise"></a>IMsgStore::Advise

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Registra para receber notificações de eventos específicos que afetam o repositório de mensagens.
  
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
  
> no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
> no Um ponteiro para o identificador de entrada da pasta ou da mensagem sobre a qual as notificações devem ser geradas ou **NULL**. Se _lpEntryID_ estiver definido como nulo, **avisará** os registros para notificações em todo o repositório de mensagens. 
    
 _ulEventMask_
  
> no Uma máscara de valores que indica os tipos de eventos de notificação nos quais o chamador está interessado e deve ser incluído no registro. Há uma estrutura de [notificação](notification.md) correspondente associada a cada tipo de evento que contém informações sobre o evento. Estes são os valores válidos para o parâmetro _ulEventMask_ : 
    
 _fnevCriticalError_
  
> Registra para notificações sobre erros graves, como memória insuficiente.
    
 _fnevExtended_
  
> Registra as notificações sobre eventos específicos para o provedor de armazenamento de mensagens específico.
    
 _fnevNewMail_
  
> Registra as notificações sobre a chegada de novas mensagens. 
    
 _fnevObjectCreated_
  
> Registra para notificações sobre a criação de uma nova pasta ou mensagem.
    
 _fnevObjectCopied_
  
> Registra para notificações sobre uma pasta ou mensagem que está sendo copiada.
    
 _fnevObjectDeleted_
  
> Registra para notificações sobre uma pasta ou mensagem que está sendo excluída.
    
 _fnevObjectModified_
  
> Registra para notificações sobre uma pasta ou mensagem que está sendo modificada.
    
 _fnevObjectMoved_
  
> Registra para notificações sobre uma pasta ou mensagem que está sendo movida.
    
 _fnevSearchComplete_
  
> Registra as notificações sobre a conclusão de uma operação de pesquisa.
    
 _lpAdviseSink_
  
> no Um ponteiro para um objeto de coletor de aviso para receber as notificações subsequentes. Este objeto de coletor de aviso deve já ter sido alocado.
    
 _lpulConnection_
  
> bota Um ponteiro para um número diferente de zero que representa a conexão entre o objeto de coletor de aviso do chamador e a sessão. 
    
 _lpAdviseSink_
  
> no Um ponteiro para um objeto de coletor de aviso para receber as notificações subsequentes. Este objeto de coletor de aviso deve já ter sido alocado. 
    
 _lpulConnection_
  
> bota Um ponteiro para um número de conexão diferente de zero que representa a conexão entre o objeto de coletor de aviso do chamador e o repositório de mensagens.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O registro foi bem-sucedido.
    
MAPI_E_NO_SUPPORT 
  
> O provedor de repositório de mensagens não oferece suporte ao registro de notificação por meio do repositório de mensagens.
    
## <a name="remarks"></a>Comentários

O método **IMsgStore:: Advise** estabelece uma conexão entre o objeto de coletor de aviso do chamador e o repositório de mensagens ou um objeto no repositório de mensagens. Essa conexão é usada para enviar notificações ao coletor de avisos quando um ou mais eventos, conforme especificado no parâmetro _ulEventMask_ , ocorrem no objeto de origem de aviso. Quando o parâmetro _lpEntryID_ aponta para um identificador de entrada válido, a fonte de aviso é o objeto identificado por esse identificador de entrada. Quando _lpEntryID_ é nulo, a fonte de aviso é o repositório de mensagens. 
  
Para enviar uma notificação, o provedor de armazenamento de mensagens ou MAPI chama o método [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) do coletor de avisos registrado. Um dos parâmetros para **OnNotify**, uma estrutura de notificação, contém informações que descrevem o evento específico.
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Você pode dar suporte à notificação com ou sem a ajuda do MAPI. O MAPI tem três métodos de objeto de suporte para ajudar os provedores de serviços a implementar a notificação: [IMAPISupport:: Subscribe](imapisupport-subscribe.md), [IMAPISupport:: unsubscribe](imapisupport-unsubscribe.md)e [IMAPISupport:: Notify](imapisupport-notify.md). Se você optar por usar os métodos de suporte MAPI, chame **Subscribe** quando seu método **Advise** for chamado e libere o ponteiro _lpAdviseSink_ . 
  
Se você optar por dar suporte a uma notificação por conta própria, chame o método [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) do coletor de avisos representado pelo parâmetro _lpAdviseSink_ para manter uma cópia desse ponteiro. Mantenha essa cópia até que o método [IMsgStore:: Unadvise](imsgstore-unadvise.md) seja chamado para cancelar o registro. 
  
Independentemente de como você dá suporte à notificação, atribua um número de conexão diferente de zero para o registro de notificação e devolva-o no parâmetro _lpulConnection_ . Não libera esse número de conexão até que **Unadvise** seja chamado e concluído. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Em sistemas que dão suporte a vários threads de execução, **** a chamada para OnNotify também pode ocorrer em qualquer thread a qualquer momento. Se você precisa ter certeza de que as notificações ocorrem somente em um determinado momento em um thread específico, chame a função [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) para gerar o objeto de coletor de aviso que você passa para **avisar**. 
  
Após uma chamada para **Advise** ter sido bem-sucedida e antes que **Unadvise** seja chamado para cancelar o registro, esteja preparado para o objeto de coletor de aviso a ser liberado. Você deve liberar seu objeto de coletor de aviso após o **aviso de alerta** , a menos que tenha um uso específico de longo prazo para ele. 
  
Para obter mais informações sobre o processo de notificação, consulte [Event Notification in MAPI](event-notification-in-mapi.md). 
  
Para obter mais informações sobre como lidar com notificações, consulte [Handling Notifications](handling-notifications.md). 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|BaseDialog. cpp  <br/> |CBaseDialog:: onNotification  <br/> |MFCMAPI usa o método **IMsgStore:: Advise** para registrar notificações em todo o repositório de mensagens.  <br/> |
   
## <a name="see-also"></a>Confira também



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMsgStore::Unadvise](imsgstore-unadvise.md)
  
[NOTIFICATION](notification.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

