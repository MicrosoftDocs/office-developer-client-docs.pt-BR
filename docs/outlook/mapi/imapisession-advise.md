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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338616"
---
# <a name="imapisessionadvise"></a>IMAPISession::Advise

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Registra para receber notificações de eventos específicos que afetam a sessão.
  
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
  
> no Um ponteiro para o identificador de entrada do objeto do catálogo de endereços ou do repositório de mensagens sobre quais notificações devem ser geradas, ou NULL, que indica que o cliente está se registrando para receber notificações sobre eventos que afetam apenas a sessão. 
    
 _ulEventMask_
  
> no Uma máscara de valores que indica os tipos de eventos de notificação em que o cliente está interessado e deve ser incluído no registro. Se _lpEntryID_ for NULL, MAPI registrará automaticamente o cliente para eventos de erro críticos que afetam apenas a sessão. Quando o _lpEntryID_ aponta para um identificador de entrada, os seguintes valores são válidos para o parâmetro _ulEventMask_ : 
    
fnevCriticalError 
  
> Registra para notificações sobre erros graves, como memória insuficiente.
    
fnevExtended 
  
> Registra para notificações sobre eventos específicos de um determinado catálogo de endereços ou provedor de mensagens sobre o desligamento de sessão.
    
fnevNewMail 
  
> Registra as notificações sobre a chegada de novas mensagens. 
    
fnevObjectCreated 
  
> Registra as notificações sobre a criação de um novo objeto.
    
fnevObjectCopied
  
> Registra para notificações sobre um objeto que está sendo copiado.
    
fnevObjectDeleted
  
> Registra as notificações sobre um objeto que está sendo excluído.
    
fnevObjectModified
  
> Registra para notificações sobre um objeto que está sendo modificado.
    
fnevObjectMoved
  
> Registra as notificações sobre um objeto que está sendo movido.
    
fnevSearchComplete
  
> Registra as notificações sobre a conclusão de uma operação de pesquisa.
    
 _lpAdviseSink_
  
> no Um ponteiro para um objeto de coletor de aviso para receber as notificações subsequentes. Este objeto de coletor de aviso deve já ter sido alocado.
    
 _lpulConnection_
  
> bota Um ponteiro para um número diferente de zero que representa a conexão entre o objeto de coletor de aviso do chamador e a sessão.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O registro foi bem-sucedido.
    
MAPI_E_INVALID_ENTRYID 
  
> O identificador de entrada apontado por _lpEntryID_ não representa um identificador de entrada válido. 
    
MAPI_E_NO_SUPPORT 
  
> O provedor de serviços responsável pelo identificador de entrada apontado pelo _lpEntryID_ não oferece suporte ao tipo de eventos especificado no parâmetro _ulEventMask_ ou não dá suporte à notificação. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> O identificador de entrada indicado pelo _lpEntryID_ não pode ser manipulado por nenhum dos provedores de serviços no perfil. 
    
## <a name="remarks"></a>Comentários

O método **IMAPISession:: Advise** estabelece uma conexão entre o objeto de coletor de aviso do chamador, a sessão e, opcionalmente, um provedor de serviços. Essa conexão é usada para enviar notificações para o coletor de avisos quando um ou mais eventos especificados no parâmetro _ulEventMask_ ocorrem ao objeto apontado por _lpEntryID_. Quando _lpEntryID_ é nulo, o objeto de destino é a sessão e as notificações são enviadas somente para erros críticos e eventos estendidos. 
  
Quando o _lpEntryID_ aponta para um identificador de entrada válido, o MAPI chama o método **Advise** do objeto de logon que pertence ao provedor de serviços responsável. Por exemplo, se _lpEntryID_ apontar para o identificador de entrada de uma lista de distribuição, o MAPI chamará o método [IABLogon:: Advise](iablogon-advise.md) do provedor de catálogo de endereços apropriado. 
  
Para enviar uma notificação, o provedor de serviços ou MAPI chama o método [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) do coletor de avisos registrado. Um dos parâmetros para **OnNotify**, uma estrutura de notificação, contém informações que descrevem o evento específico.
  
## <a name="notes-to-callers"></a>Notas para chamadores

Em sistemas que dão suporte a vários threads de execução, **** a chamada para OnNotify também pode ocorrer em qualquer thread a qualquer momento. Se você precisar de garantia de que as notificações ocorrerão apenas em um determinado momento em um thread específico, chame a função [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) para gerar o objeto de coletor de aviso que você passa para o método **Advise** . 
  
Para determinar quando um cliente fez logoff, registre-se para notificações no seu provedor de serviços chamando **avisar** com _lpEntryID_ definido como nulo e _cbEntryID_ definido como 0. Quando o logoff ocorrer, você receberá uma notificação fnevExtended. 
  
Após uma chamada a **Advise** ter sido bem-sucedida e antes de [IMAPISession:: Unadvise](imapisession-unadvise.md) foi chamado para cancelar o registro, libere seu objeto de coletor de aviso, a menos que você tenha um uso específico de longo prazo para ele. 
  
Para obter uma visão geral do processo de notificação, consulte [Event Notification in MAPI](event-notification-in-mapi.md). 
  
Para obter mais informações sobre como lidar com notificações, consulte [Handling Notifications](handling-notifications.md). 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|BaseDialog. cpp  <br/> |CBaseDialog:: onNotification  <br/> |MFCMAPI usa o método **IMAPISession:: Advise** para registrar notificações em relação à sessão.  <br/> |
   
## <a name="see-also"></a>Confira também



[IABLogon::Advise](iablogon-advise.md)
  
[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISession::Unadvise](imapisession-unadvise.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Notificação de evento no MAPI](event-notification-in-mapi.md)

