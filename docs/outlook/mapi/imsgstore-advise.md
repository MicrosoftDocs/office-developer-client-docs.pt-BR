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
  
Registra para receber notificação de eventos especificados que afetam o armazenamento de mensagens.
  
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
  
> [in] Um ponteiro para o identificador de entrada da pasta ou mensagem sobre as notificações que devem ser geradas ou **nulo**. Se  _lpEntryID_ for definido como NULL, **Advise** registrará notificações em todo o armazenamento de mensagens. 
    
 _ulEventMask_
  
> [in] Uma máscara de valores que indicam os tipos de eventos de notificação nos quais o chamador está interessado e devem ser incluídos no registro. Há uma estrutura [notification](notification.md) correspondente associada a cada tipo de evento que contém informações sobre o evento. A seguir estão os valores válidos para _o parâmetro ulEventMask:_ 
    
 _fnevCriticalError_
  
> Registra notificações sobre erros graves, como memória insuficiente.
    
 _fnevExtended_
  
> Registra notificações sobre eventos específicos para o provedor de armazenamento de mensagens específico.
    
 _fnevNewMail_
  
> Registra notificações sobre a chegada de novas mensagens. 
    
 _fnevObjectCreated_
  
> Registra notificações sobre a criação de uma nova pasta ou mensagem.
    
 _fnevObjectCopied_
  
> Registra notificações sobre uma pasta ou mensagem que está sendo copiada.
    
 _fnevObjectDeleted_
  
> Registra notificações sobre uma pasta ou mensagem que está sendo excluída.
    
 _fnevObjectModified_
  
> Registra notificações sobre uma pasta ou mensagem que está sendo modificada.
    
 _fnevObjectMoved_
  
> Registra notificações sobre uma pasta ou mensagem que está sendo movida.
    
 _fnevSearchComplete_
  
> Registra notificações sobre a conclusão de uma operação de pesquisa.
    
 _lpAdviseSink_
  
> [in] Um ponteiro para um objeto sink de aviso para receber as notificações subsequentes. Esse objeto sink de aconselhmento já deve ter sido alocado.
    
 _lpulConnection_
  
> [out] Um ponteiro para um número que não é zero que representa a conexão entre o objeto sink de alerta do chamador e a sessão. 
    
 _lpAdviseSink_
  
> [in] Um ponteiro para um objeto sink de aviso para receber as notificações subsequentes. Esse objeto sink de aconselhmento já deve ter sido alocado. 
    
 _lpulConnection_
  
> [out] Um ponteiro para um número de conexão que não seja zero que representa a conexão entre o objeto sink de alerta do chamador e o armazenamento de mensagens.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O registro foi bem-sucedido.
    
MAPI_E_NO_SUPPORT 
  
> O provedor de armazenamento de mensagens não dá suporte ao registro para notificação por meio do armazenamento de mensagens.
    
## <a name="remarks"></a>Comentários

O **método IMsgStore::Advise** estabelece uma conexão entre o objeto sink de alerta do chamador e o repositório de mensagens ou um objeto no repositório de mensagens. Essa conexão é usada para enviar notificações ao sink de aviso quando um ou mais eventos, conforme especificado no parâmetro  _ulEventMask,_ ocorrerem para o objeto de origem de aviso. Quando o  _parâmetro lpEntryID_ aponta para um identificador de entrada válido, a origem do alerta é o objeto identificado por esse identificador de entrada. Quando  _lpEntryID_ é NULL, a fonte de conselhos é o armazenamento de mensagens. 
  
Para enviar uma notificação, o provedor de armazenamento de mensagens ou o MAPI chama o método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) do pia de aviso registrado. Um dos parâmetros para **OnNotify**, uma estrutura de notificação, contém informações que descrevem o evento específico.
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Você pode dar suporte à notificação com ou sem ajuda do MAPI. MAPI has three support object methods for helping service providers implement notification: [IMAPISupport::Subscribe](imapisupport-subscribe.md), [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md), and [IMAPISupport::Notify](imapisupport-notify.md). Se você optar por usar os métodos de suporte MAPI, chame **Subscribe** quando o método **Advise** for chamado e libere o ponteiro _lpAdviseSink._ 
  
Se você optar por dar suporte à notificação por conta própria, chame o método [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) do sink de aviso representado pelo parâmetro  _lpAdviseSink_ para manter uma cópia desse ponteiro. Mantenha essa cópia até que o [método IMsgStore::Unadvise](imsgstore-unadvise.md) seja chamado para cancelar o registro. 
  
Independentemente de como você suporta a notificação, atribua um número de conexão não zero ao registro de notificação e retorne-o no parâmetro _lpulConnection._ Não libere esse número de conexão **até que Unadvise** tenha sido chamado e tenha sido concluído. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Em sistemas que suportam vários threads de execução, a chamada para **OnNotify** também pode ocorrer em qualquer thread a qualquer momento. Se você deve ter certeza de que as notificações ocorrem apenas em um determinado momento em um determinado thread, chame a [função HrThisThreadAdviseSink](hrthisthreadadvisesink.md) para gerar o objeto de evento de aviso que você passa para **Advise**. 
  
Depois que uma chamada para **o Advise** tiver sido bem-sucedida e antes que **Unadvise** tenha sido chamada para cancelar o registro, esteja preparado para que o objeto de pia de aconselhá-lo seja liberado. Você deve liberar seu objeto sink de aconselhado após **o retorno de** Advise, a menos que você tenha um uso específico a longo prazo para ele. 
  
Para obter mais informações sobre o processo de notificação, consulte [Notificação de Evento em MAPI](event-notification-in-mapi.md). 
  
Para obter mais informações sobre como lidar com notificações, consulte [Manipulando notificações.](handling-notifications.md) 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnNotificationsOn  <br/> |MFCMAPI usa o **método IMsgStore::Advise** para registrar notificações em todo o repositório de mensagens.  <br/> |
   
## <a name="see-also"></a>Confira também



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMsgStore::Unadvise](imsgstore-unadvise.md)
  
[NOTIFICAÇÃO](notification.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

