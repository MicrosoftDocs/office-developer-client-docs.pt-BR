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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351440"
---
# <a name="imapiadvisesinkonnotify"></a>IMAPIAdviseSink::OnNotify

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Responde a uma notificação executando uma ou mais tarefas. As tarefas realizadas dependem do tipo de evento e do objeto que gera a notificação. 
  
```cpp
ULONG OnNotify(
  ULONG cNotif,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a>Parâmetros

 _cNotif_
  
> no A contagem de estruturas de [notificação](notification.md) apontadas pelo parâmetro _lpNotifications_ . 
    
 _lpNotifications_
  
> no Um ponteiro para uma ou mais estruturas de **notificação** que fornecem informações sobre os eventos que ocorreram. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A notificação foi processada com êxito.
    
## <a name="remarks"></a>Comentários

O processo de notificação é iniciado quando um cliente ou MAPI faz uma chamada para o método **Advise** de um provedor de serviços para se registrar para receber uma notificação de um tipo específico para um objeto específico. Um dos parâmetros para o método **Advise** é um ponteiro para um objeto de coletor de aviso que implementa a interface [IMAPIAdviseSink](imapiadvisesinkiunknown.md) . Quando ocorre um evento para o objeto de destino que corresponde à notificação registrada, o provedor de serviços, direta ou indiretamente por meio de MAPI, chama **** o método OnNotify do coletor de avisos. 
  
A chamada para **OnNotify** pode ocorrer durante a chamada MAPI que está causando o evento ou em algum momento posterior. Em sistemas que oferecem suporte a vários threads **** de execução, OnNotify pode ser chamado no mesmo thread que foi usado para registro ou em um thread diferente. Os clientes podem garantir que a **** chamada OnNotify seja feita no mesmo thread usado para chamar **Advise** , criando o coletor de avisos que eles passam para **avisar** com a função [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) . 
  
O parâmetro _lpNotifications_ aponta para uma ou mais estruturas de **notificação** que descrevem o que foi alterado durante o evento. Há um tipo diferente de estrutura de **notificação** para cada tipo de evento. 
  
A tabela a seguir lista os valores que são usados para representar os possíveis tipos de eventos e as estruturas associadas a cada valor:
  
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
   
Para obter mais informações sobre como configurar e interromper notificações, consulte as entradas de referência para os métodos **Advise** e **Unadvise** para qualquer uma das seguintes interfaces: [IABLogon](iablogoniunknown.md), [IAddrBook](iaddrbookimapiprop.md), [IMAPIForm](imapiformiunknown.md), [ IMAPISession](imapisessioniunknown.md), [](imapitableiunknown.md)IMAPITable, [IMsgStore](imsgstoreimapiprop.md)e [IMSLogon](imslogoniunknown.md). 
  
Para obter informações gerais sobre o processo de notificação, consulte [Event Notification in MAPI](event-notification-in-mapi.md). 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

A **** implementação onnotificar normalmente consiste em um ou mais blocos de código para cada tipo de notificação que você espera receber. Nesses blocos de código, execute quaisquer tarefas que você considere necessárias como resposta à notificação. Por exemplo, suponha que você se registre para receber notificações do **fnevObjectModified** em uma pasta incluída em uma caixa de diálogo exibida. No bloco de código que você inclui no seu método **OnNotify** para manipular notificações do **fnevObjectModified** , você pode enviar uma mensagem do Windows para a caixa de diálogo para solicitar uma exibição atualizada. 
  
Não modifique nem libere a estrutura de **notificação** passada para **OnNotify**. Os dados na estrutura são válidos somente até que **OnNotify** Returns seja retornado. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Quando ocorrem alterações em vários objetos, você pode notificar um coletor de aviso registrado em uma única **** chamada para OnNotify ou em várias chamadas, dependendo das restrições de memória. Isso é verdadeiro independentemente se as alterações são o resultado de uma chamada de método ou várias. Por exemplo, uma chamada para [IMAPIFolder:: CopyMessages](imapifolder-copymessages.md) pode afetar várias mensagens e pastas. Como um provedor de armazenamento de mensagens, você pode fazer uma **** chamada para onnotificar com um tipo de evento **fnevObjectModified** para a pasta de destino ou muitas chamadas, uma para cada uma das mensagens afetadas. Da mesma forma, se um cliente fizer chamadas repetidas para [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md), essas chamadas poderão ser combinadas em um evento **fnevObjectModified** para a pasta ou separados em eventos **fnevObjectCreated** individuais para cada nova mensagem. 
  
Para obter mais informações sobre como e quando gerar notificações, consulte [Event Notification in MAPI](event-notification-in-mapi.md) and [support Event Notification](supporting-event-notification.md). 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|AdviseSink. h e AdviseSink. cpp  <br/> |CAdviseSink:: OnNotifyDesc  <br/> |A classe CAdviseSink é implementada para lidar com todas as notificações no MFCMAPI.  <br/> |
   
## <a name="see-also"></a>Confira também



[HrAllocAdviseSink](hrallocadvisesink.md)
  
[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPISupport::Notify](imapisupport-notify.md)
  
[NOTIFICATION](notification.md)
  
[IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

