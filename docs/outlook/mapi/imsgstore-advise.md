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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 6a315cef8263f7e241a815a0f054dc3174d88fa7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767481"
---
# <a name="imsgstoreadvise"></a>IMsgStore::Advise

  
  
**Aplica-se a**: Outlook 
  
Registra para receber notificações de eventos especificados que afetam o armazenamento de mensagens.
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a>Par�metros

 _cbEntryID_
  
> [in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Um ponteiro para o identificador de entrada da pasta ou mensagem sobre o qual as notificações devem ser geradas ou **Nulo**. Se _lpEntryID_ for definido como NULL, **Advise** registra para notificações no repositório de toda a mensagem. 
    
 _ulEventMask_
  
> [in] Uma máscara de valores que indicam os tipos de eventos de notificação que o chamador está interessado em e deve ser incluído no registro. Há uma estrutura de [notificação](notification.md) correspondente associada a cada tipo de evento que contém informações sobre o evento. Estes são os valores válidos para o parâmetro _ulEventMask_ : 
    
 _fnevCriticalError_
  
> Registradores para notificações sobre erros graves, como as de memória insuficiente.
    
 _fnevExtended_
  
> Provedor de armazenamento de registradores para notificações sobre eventos específicos à mensagem específica.
    
 _fnevNewMail_
  
> Registradores para notificações sobre a chegada de novas mensagens. 
    
 _fnevObjectCreated_
  
> Registradores para notificações sobre a criação de uma nova pasta ou mensagem.
    
 _fnevObjectCopied_
  
> Registradores para notificações sobre uma pasta ou uma mensagem que está sendo copiada.
    
 _fnevObjectDeleted_
  
> Registradores para notificações sobre uma pasta ou uma mensagem que está sendo excluído.
    
 _fnevObjectModified_
  
> Registradores para notificações sobre uma pasta ou mensagem está sendo modificado.
    
 _fnevObjectMoved_
  
> Registradores para notificações sobre uma pasta ou uma mensagem que está sendo movido.
    
 _fnevSearchComplete_
  
> Registradores para notificações sobre a conclusão de uma operação de pesquisa.
    
 _lpAdviseSink_
  
> [in] Um ponteiro para um objeto de coletor de eventos advise para receber as notificações subsequentes. Este objeto de coletor de eventos advise deve já foram alocado.
    
 _lpulConnection_
  
> [out] Um ponteiro para um número diferente de zero que representa a conexão entre o chamador avise o objeto coletor de eventos e a sessão. 
    
 _lpAdviseSink_
  
> [in] Um ponteiro para um objeto de coletor de eventos advise para receber as notificações subsequentes. Este objeto de coletor de eventos advise deve já foram alocado. 
    
 _lpulConnection_
  
> [out] Um ponteiro para um número diferente de zero de conexão que representa a conexão entre o chamador avise o objeto coletor de eventos e o armazenamento de mensagens.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O registro foi bem-sucedida.
    
MAPI_E_NO_SUPPORT 
  
> O provedor de armazenamento de mensagem não suporta o registro para notificação por meio de armazenamento de mensagens.
    
## <a name="remarks"></a>Coment�rios

O método **IMsgStore::Advise** estabelece uma conexão entre o chamador do aviso de objeto coletor de eventos e o armazenamento de mensagens ou um objeto no repositório de mensagem. Essa conexão é usado para enviar notificações para o coletor de advise quando um ou mais eventos, conforme especificado no parâmetro _ulEventMask_ , ocorrem para o objeto de origem advise. Quando os pontos de parâmetro _lpEntryID_ a um identificador de entrada válida, a fonte de advise é o objeto identificado por esse identificador de entrada. Quando _lpEntryID_ for NULL, a fonte de advise é o armazenamento de mensagens. 
  
Para enviar uma notificação, o provedor de armazenamento de mensagem ou MAPI chama o método de [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) do coletor de eventos registrados advise. Um dos parâmetros para **OnNotify**, uma estrutura de notificação, contém informações que descrevem o evento específico.
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Você pode oferecer suporte a notificação com ou sem a Ajuda de MAPI. MAPI possui três métodos de objeto de suporte para ajudar os provedores de serviço a implementar notificação: [IMAPISupport::Subscribe](imapisupport-subscribe.md), [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)e [IMAPISupport::Notify](imapisupport-notify.md). Se você optar por usar os métodos de suporte MAPI, ligue para **inscrever-se** ao seu método **Advise** é chamado e liberar o ponteiro _lpAdviseSink_ . 
  
Se você optar por suporte a notificação, chame o método de [AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) do coletor advise representado pelo parâmetro _lpAdviseSink_ para manter uma cópia deste ponteiro. Manter essa cópia até seu método [IMsgStore::Unadvise](imsgstore-unadvise.md) é chamado para cancelar o registro. 
  
Independentemente de como você oferecer suporte à notificação, atribua um número diferente de zero de conexão para o registro de notificação e retorná-lo no parâmetro _lpulConnection_ . Não libere esse número de conexão até **Unadvise** foi chamado e foi concluída. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Nos sistemas que oferecem suporte a vários threads de execução, a chamada para **OnNotify** também pode ocorrer em qualquer segmento a qualquer momento. Se você deve ter certeza de que as notificações ocorrem apenas em um momento específico em um determinado thread, chame a função de [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) para gerar o objeto coletor de eventos advise que você passa para **Advise**. 
  
Após uma chamada para **Advise** teve sucesso e antes que tenha sido chamado **Unadvise** para cancelar o registro, estar preparado para o objeto coletor de eventos de advise ser liberada. Você deve liberar seu objeto de coletor de eventos advise depois **Advise** retorna a menos que tenha um uso específico de longo prazo para ele. 
  
Para obter mais informações sobre o processo de notificação, consulte [Notificação de evento em MAPI](event-notification-in-mapi.md). 
  
Para obter mais informações sobre como manipular notificações, consulte [Manipulação de notificações](handling-notifications.md). 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnNotificationsOn  <br/> |MFCMAPI usa o método **IMsgStore::Advise** para registrar para notificações no repositório de toda a mensagem.  <br/> |
   
## <a name="see-also"></a>Confira também



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMsgStore::Unadvise](imsgstore-unadvise.md)
  
[NOTIFICAÇÃO](notification.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

