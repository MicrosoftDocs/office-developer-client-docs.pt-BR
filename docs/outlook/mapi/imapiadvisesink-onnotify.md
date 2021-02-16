---
title: IMAPIAdviseSinkOnNotify
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIAdviseSink.OnNotify
api_type:
- COM
ms.assetid: 9eec90d3-2369-4340-86ed-0efa58918ed5
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5983ed3229f6b0053f15a614116cf5680e942587
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407358"
---
# <a name="imapiadvisesinkonnotify"></a>IMAPIAdviseSink::OnNotify

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Responde a uma notificação executando uma ou mais tarefas. As tarefas executadas dependem do tipo de evento e do objeto que gera a notificação. 
  
```cpp
ULONG OnNotify(
  ULONG cNotif,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a>Parâmetros

 _cNotif_
  
> [in] A contagem de [estruturas NOTIFICATION](notification.md) apontadas pelo _parâmetro lpNotifications._ 
    
 _lpNotifications_
  
> [in] Um ponteiro para uma ou mais estruturas **de** NOTIFICAÇÃO que fornecem informações sobre os eventos que ocorreram. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A notificação foi processada com êxito.
    
## <a name="remarks"></a>Comentários

O processo de notificação começa quando um cliente ou MAPI faz uma chamada para o método **Advise** de um provedor de serviços para se registrar para receber uma notificação de um tipo específico para um objeto específico. Um dos parâmetros para o método **Advise** é um ponteiro para um objeto sink que implementa a interface [IMAPIAdviseSink.](imapiadvisesinkiunknown.md) Quando ocorre um evento para o objeto de destino que corresponde à notificação registrada, o provedor de serviços, direta ou indiretamente através de MAPI, chama o método **OnNotify** do evento de aviso. 
  
A chamada para **OnNotify** pode ocorrer durante a chamada MAPI que está causando o evento ou em algum momento posterior. Em sistemas que suportam vários threads de execução, **OnNotify** pode ser chamado no mesmo thread que foi usado para registro ou em um thread diferente. Os clientes podem se certificar de que a chamada **OnNotify** seja feita no mesmo  thread usado para chamar o **Advise,** criando o evento de alerta que eles passam para Advise com a função [HrThisThreadAdviseSink.](hrthisthreadadvisesink.md) 
  
O  _parâmetro lpNotifications_ aponta para uma ou mais estruturas **notification** que descrevem o que foi alterado durante o evento. Há um tipo diferente de estrutura **DE NOTIFICAÇÃO** para cada tipo de evento. 
  
A tabela a seguir lista os valores usados para representar os possíveis tipos de eventos e as estruturas associadas a cada valor:
  
|**Tipo de evento de notificação**|**Estrutura correspondente**|
|:-----|:-----|
|**fnevCriticalError** <br/> |[ERROR_NOTIFICATION](error_notification.md) <br/> |
|**fnevNewMail** <br/> |[NEWMAIL_NOTIFICATION](newmail_notification.md) <br/> |
|**fnevObjectCreated** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectDeleted** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectModified** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectCopied** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevSearchComplete** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevTableModified** <br/> |[TABLE_NOTIFICATION](table_notification.md) <br/> |
|**fnevStatusObjectModified** <br/> |[STATUS_OBJECT_NOTIFICATION](status_object_notification.md) <br/> |
|**fnevExtended** <br/> |[EXTENDED_NOTIFICATION](extended_notification.md) <br/> |
   
For more information about how to set up and stop notifications, see the reference entries for the **Advise** and **Unadvise** methods for any of the following interfaces: [IABLogon](iablogoniunknown.md), [IAddrBook](iaddrbookimapiprop.md), [IMAPIForm](imapiformiunknown.md), [IMAPISession](imapisessioniunknown.md), [IMAPITable](imapitableiunknown.md), [IMsgStore](imsgstoreimapiprop.md), and [IMSLogon](imslogoniunknown.md). 
  
Para obter informações gerais sobre o processo de notificação, consulte [Notificação de Evento em MAPI](event-notification-in-mapi.md). 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Sua **implementação OnNotify** geralmente consiste em um ou mais blocos de código para cada tipo de notificação que você espera receber. Dentro desses blocos de código, execute as tarefas que você considera necessárias como resposta à notificação. Por exemplo, suponha que você se registre para receber notificações **fnevObjectModified** em uma pasta incluída em uma exibição de caixa de diálogo. No bloco de código incluído no método **OnNotify** para manipular notificações **fnevObjectModified,** você pode enviar uma mensagem do Windows para a caixa de diálogo para solicitar uma exibição atualizada. 
  
Não modifique ou free a **estrutura NOTIFICATION** passada para **OnNotify**. Os dados na estrutura são válidos apenas até **OnNotify** retornar. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Quando ocorrem alterações em vários objetos, você pode notificar um sink de aviso registrado em uma única chamada para **OnNotify** ou em várias chamadas, dependendo das restrições de memória. Isso é verdadeiro independentemente das alterações ser o resultado de uma chamada de método ou várias. Por exemplo, uma chamada para [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) pode afetar várias mensagens e pastas. Como provedor de armazenamento de mensagens, você pode fazer uma chamada para **OnNotify** com um tipo de evento **fnevObjectModified** para a pasta de destino ou muitas chamadas, uma para cada uma afeta mensagens. Da mesma forma, se um cliente fizer chamadas repetidas para [IMAPIFolder::CreateMessage](imapifolder-createmessage.md), essas chamadas poderão ser combinadas em um evento **fnevObjectModified** para a pasta ou separadas em eventos **fnevObjectCreated** individuais para cada nova mensagem. 
  
For more information about how and when to generate notifications, see [Event Notification in MAPI](event-notification-in-mapi.md) and [Supporting Event Notification](supporting-event-notification.md). 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|AdviseSink.h e AdviseSink.cpp  <br/> |CAdviseSink::OnNotifyDesc  <br/> |A classe CAdviseSink é implementada para manipular todas as notificações em MFCMAPI.  <br/> |
   
## <a name="see-also"></a>Confira também



[HrAllocAdviseSink](hrallocadvisesink.md)
  
[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPISupport::Notify](imapisupport-notify.md)
  
[NOTIFICAÇÃO](notification.md)
  
[IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

