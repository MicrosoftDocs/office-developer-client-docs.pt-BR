---
title: IMAPISessionAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.Advise
api_type:
- COM
ms.assetid: a6a6b6b1-31e2-4899-a5fe-74d5d1c2ccfc
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d5d87d7be9cb3524445107e975a298d4afd5bf98
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419832"
---
# <a name="imapisessionadvise"></a>IMAPISession::Advise

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Registra para receber notificação de eventos especificados que afetam a sessão.
  
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
  
> [in] Um ponteiro para o identificador de entrada do livro de endereços ou objeto do armazenamento de mensagens sobre o qual as notificações devem ser geradas, ou NULL, que indica que o cliente está se registrando para receber notificações sobre eventos que afetam apenas a sessão. 
    
 _ulEventMask_
  
> [in] Uma máscara de valores que indicam os tipos de eventos de notificação nos quais o cliente está interessado e devem ser incluídos no registro. Se  _lpEntryID_ for NULL, MAPI registrará automaticamente o cliente para eventos de erro críticos que afetam apenas a sessão. Quando _lpEntryID_ aponta para um identificador de entrada, os seguintes valores são válidos para o _parâmetro ulEventMask:_ 
    
fnevCriticalError 
  
> Registra notificações sobre erros graves, como memória insuficiente.
    
fnevExtended 
  
> Registra notificações sobre eventos específicos de um determinado address book ou provedor de armazenamento de mensagens e sobre o desligar da sessão.
    
fnevNewMail 
  
> Registra notificações sobre a chegada de novas mensagens. 
    
fnevObjectCreated 
  
> Registra notificações sobre a criação de um novo objeto.
    
fnevObjectCopied
  
> Registra notificações sobre um objeto sendo copiado.
    
fnevObjectDeleted
  
> Registra notificações sobre um objeto que está sendo excluído.
    
fnevObjectModified
  
> Registra notificações sobre um objeto que está sendo modificado.
    
fnevObjectMoved
  
> Registra notificações sobre um objeto que está sendo movido.
    
fnevSearchComplete
  
> Registra notificações sobre a conclusão de uma operação de pesquisa.
    
 _lpAdviseSink_
  
> [in] Um ponteiro para um objeto sink de aviso para receber as notificações subsequentes. Esse objeto sink de aconselhmento já deve ter sido alocado.
    
 _lpulConnection_
  
> [out] Um ponteiro para um número que não seja zero que representa a conexão entre o objeto sink de alerta do chamador e a sessão.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O registro foi bem-sucedido.
    
MAPI_E_INVALID_ENTRYID 
  
> O identificador de entrada apontado por  _lpEntryID_ não representa um identificador de entrada válido. 
    
MAPI_E_NO_SUPPORT 
  
> O provedor de serviços responsável pelo identificador de entrada apontado por  _lpEntryID_ não suporta o tipo de eventos especificados no parâmetro  _ulEventMask_ ou não suporta notificação. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> O identificador de entrada apontado por  _lpEntryID_ não pode ser manipulado por nenhum dos provedores de serviços no perfil. 
    
## <a name="remarks"></a>Comentários

O **método IMAPISession::Advise** estabelece uma conexão entre o objeto sink de alerta do chamador, a sessão e, opcionalmente, um provedor de serviços. Essa conexão é usada para enviar notificações ao sink de aviso quando um ou mais eventos especificados no  _parâmetro ulEventMask_ ocorrem para o objeto apontado por  _lpEntryID_. Quando  _lpEntryID_ é NULL, o objeto de destino é a sessão e as notificações são enviadas apenas para erros críticos e eventos estendidos. 
  
Quando  _lpEntryID_ aponta para um identificador de entrada válido, MAPI chama o método **Advise** do objeto de logon que pertence ao provedor de serviços responsável. Por exemplo, se  _lpEntryID_ aponta para o identificador de entrada de uma lista de distribuição, o MAPI chama o método [IABLogon::Advise](iablogon-advise.md) do provedor de endereços apropriado. 
  
Para enviar uma notificação, o provedor de serviços ou o MAPI chama o método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) do pia registrado. Um dos parâmetros para **OnNotify**, uma estrutura de notificação, contém informações que descrevem o evento específico.
  
## <a name="notes-to-callers"></a>Notas para chamadores

Em sistemas que suportam vários threads de execução, a chamada para **OnNotify** também pode ocorrer em qualquer thread a qualquer momento. Se você precisar de garantia de que as notificações ocorrerão apenas em um determinado momento em um determinado thread, chame a função [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) para gerar o objeto de evento de aviso que você passa para o método **Advise.** 
  
Para determinar quando um cliente fez logon, registre-se para notificações em seu provedor de serviços chamando **Advise** com  _lpEntryID_ definido como NULL e  _cbEntryID_ definido como 0. Quando o logoff ocorrer, você receberá uma notificação fnevExtended. 
  
Depois que uma chamada para o **Advise** tiver sido bem-sucedida e antes de [IMAPISession::Unadvise](imapisession-unadvise.md) ter sido chamado para cancelar o registro, libere seu objeto de cliente a menos que você tenha um uso específico a longo prazo para ele. 
  
Para uma visão geral do processo de notificação, consulte [Notificação de evento em MAPI](event-notification-in-mapi.md). 
  
Para obter mais informações sobre como lidar com notificações, consulte [Manipulando notificações.](handling-notifications.md) 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnNotificationsOn  <br/> |MFCMAPI usa o **método IMAPISession::Advise** para se registrar para notificações contra a sessão.  <br/> |
   
## <a name="see-also"></a>Confira também



[IABLogon::Advise](iablogon-advise.md)
  
[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISession::Unadvise](imapisession-unadvise.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Notificação de evento em MAPI](event-notification-in-mapi.md)

