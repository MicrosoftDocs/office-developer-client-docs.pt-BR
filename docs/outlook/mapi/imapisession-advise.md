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
ms.openlocfilehash: 45033ab924dcf443e9d231b3a7b4348119758935
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767184"
---
# <a name="imapisessionadvise"></a>IMAPISession::Advise

  
  
**Aplica-se a**: Outlook 
  
Registra para receber notificações de eventos especificados que afetam a sessão.
  
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
  
> [in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Um ponteiro para o identificador de entrada do catálogo de endereços ou objeto de repositório de mensagem notificações sobre quais devem ser geradas ou nulo, o que indica que o cliente está registrando para receber notificações de eventos que afetam apenas a sessão. 
    
 _ulEventMask_
  
> [in] Uma máscara de valores que indicam os tipos de eventos de notificação que o cliente está interessado em e deve ser incluído no registro. Se _lpEntryID_ for NULL, MAPI registra automaticamente o cliente para eventos de erros críticos que afetam apenas a sessão. Quando _lpEntryID_ aponta para um identificador de entrada, os seguintes valores são válidos para o parâmetro _ulEventMask_ : 
    
fnevCriticalError 
  
> Registradores para notificações sobre erros graves, como as de memória insuficiente.
    
fnevExtended 
  
> Registradores notificações sobre eventos específicos a um catálogo de endereços particular ou mensagem de provedor de armazenamento e sobre sessão desligado.
    
fnevNewMail 
  
> Registradores para notificações sobre a chegada de novas mensagens. 
    
fnevObjectCreated 
  
> Registradores para notificações sobre a criação de um novo objeto.
    
fnevObjectCopied
  
> Registradores para notificações sobre um objeto que está sendo copiada.
    
fnevObjectDeleted
  
> Registradores para notificações sobre um objeto que está sendo excluído.
    
fnevObjectModified
  
> Registradores para notificações sobre um objeto que está sendo modificado.
    
fnevObjectMoved
  
> Registradores para notificações sobre um objeto que está sendo movido.
    
fnevSearchComplete
  
> Registradores para notificações sobre a conclusão de uma operação de pesquisa.
    
 _lpAdviseSink_
  
> [in] Um ponteiro para um objeto de coletor de eventos advise para receber as notificações subsequentes. Este objeto de coletor de eventos advise deve já foram alocado.
    
 _lpulConnection_
  
> [out] Um ponteiro para um número diferente de zero que representa a conexão entre o chamador avise o objeto coletor de eventos e a sessão.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O registro foi bem-sucedida.
    
MAPI_E_INVALID_ENTRYID 
  
> O identificador de entrada apontado pela _lpEntryID_ não representa um identificador de entrada válida. 
    
MAPI_E_NO_SUPPORT 
  
> O provedor de serviços para o identificador de entrada apontado pela _lpEntryID_ responsável não suporta o tipo de eventos especificado no parâmetro _ulEventMask_ ou não oferece suporte a notificação. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> O identificador de entrada apontado pela _lpEntryID_ não pode ser manipulado por qualquer um dos provedores de serviços no perfil. 
    
## <a name="remarks"></a>Comentários

O método **IMAPISession::Advise** estabelece uma conexão entre o chamador do objeto de coletor de eventos, a sessão e, opcionalmente, um provedor de serviços de aviso. Essa conexão é usado para enviar notificações para o coletor de advise quando um ou mais eventos especificados no parâmetro _ulEventMask_ ocorrem ao objeto apontado pela _lpEntryID_. Quando _lpEntryID_ for NULL, o objeto de destino é a sessão e notificações serão enviadas somente para erros críticos e eventos estendidos. 
  
Quando _lpEntryID_ aponta para um identificador de entrada válida, MAPI chama o método **Advise** do objeto de logon que pertence ao provedor de serviços responsável. Por exemplo, se _lpEntryID_ aponta para o identificador de entrada de uma lista de distribuição, MAPI chama o método de [IABLogon::Advise](iablogon-advise.md) do provedor de catálogo de endereço apropriado. 
  
Para enviar uma notificação, o provedor de serviços ou o MAPI chama o método de [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) do coletor de eventos registrados advise. Um dos parâmetros para **OnNotify**, uma estrutura de notificação, contém informações que descrevem o evento específico.
  
## <a name="notes-to-callers"></a>Notas para chamadores

Nos sistemas que oferecem suporte a vários threads de execução, a chamada para **OnNotify** também pode ocorrer em qualquer segmento a qualquer momento. Se você precisar de garantia de que as notificações ocorrerá apenas em um momento específico em um determinado thread, chame a função de [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) para gerar o objeto coletor de eventos advise que você passa para o método **Advise** . 
  
Para determinar quando um cliente tiverem feito logoff, registre-se para notificações no seu provedor de serviço chamando **Advise** com _lpEntryID_ definido como NULL e _cbEntryID_ definida como 0. Quando o logoff ocorre, você receberá uma notificação fnevExtended. 
  
Depois que uma chamada para **Advise** teve sucesso e antes de [IMAPISession::Unadvise](imapisession-unadvise.md) tiver sido chamado para cancelar o registro, libere seu objeto de coletor de eventos advise a menos que tenha um uso específico de longo prazo para ele. 
  
Para obter uma visão geral do processo de notificação, consulte [Notificação de evento em MAPI](event-notification-in-mapi.md). 
  
Para obter mais informações sobre como manipular notificações, consulte [Manipulação de notificações](handling-notifications.md). 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnNotificationsOn  <br/> |MFCMAPI usa o método **IMAPISession::Advise** para registrar para notificações contra a sessão.  <br/> |
   
## <a name="see-also"></a>Confira também



[IABLogon::Advise](iablogon-advise.md)
  
[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISession::Unadvise](imapisession-unadvise.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Notificações de eventos no MAPI](event-notification-in-mapi.md)

