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
ms.openlocfilehash: d052e7590ee502b55f2076d698587ab68820ca56
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576698"
---
# <a name="imapiadvisesinkonnotify"></a>IMAPIAdviseSink::OnNotify

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Responde a uma notificação, executando uma ou mais tarefas. As tarefas realizadas dependem do tipo de evento e o objeto que gera a notificação. 
  
```cpp
ULONG OnNotify(
  ULONG cNotif,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a>Parâmetros

 _cNotif_
  
> [in] A contagem de estruturas de [notificação](notification.md) apontado pelo parâmetro _lpNotifications_ . 
    
 _lpNotifications_
  
> [in] Um ponteiro para uma ou mais estruturas de **notificação** que fornecem informações sobre os eventos que ocorreram. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A notificação foi processada com êxito.
    
## <a name="remarks"></a>Comentários

O processo de notificação começa quando um cliente ou MAPI faz uma chamada para o método **Advise** de um provedor de serviços para registrar-se para receber uma notificação de um tipo específico de um determinado objeto. Um dos parâmetros para o método **Advise** é um ponteiro para um objeto de coletor de eventos advise que implementa a interface [IMAPIAdviseSink](imapiadvisesinkiunknown.md) . Quando um evento ocorre ao objeto de destino que corresponde à notificação registrada, o provedor de serviço, direta ou indiretamente por meio de MAPI, chama o método de **OnNotify** do coletor de eventos advise. 
  
A chamada para **OnNotify** pode ocorrer durante a chamada MAPI que está causando o evento ou em algum momento posterior. Nos sistemas que oferecem suporte a vários threads de execução, **OnNotify** pode ser chamado no mesmo thread que foi usado para registro ou em um segmento diferente. Os clientes podem Certifique-se de que a chamada **OnNotify** é feita no mesmo thread usado para chamar **Advise** criando o coletor de eventos advise que eles passam para **Advise** com a função [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) . 
  
O parâmetro _lpNotifications_ aponta para uma ou mais estruturas de **notificação** que descrevem o que mudou durante o evento. Há um tipo diferente de estrutura de **notificação** para cada tipo de evento. 
  
A tabela a seguir lista os valores que são usados para representar os tipos possíveis de eventos e as estruturas associadas a cada valor:
  
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
   
Para obter mais informações sobre como configurar e interromper notificações, consulte as entradas de referência para os métodos **Advise** e **Unadvise** para qualquer uma das seguintes interfaces: [IABLogon](iablogoniunknown.md), [IAddrBook](iaddrbookimapiprop.md), [IMAPIForm](imapiformiunknown.md), [ IMAPISession](imapisessioniunknown.md), [IMAPITable](imapitableiunknown.md), [IMsgStore](imsgstoreimapiprop.md)e [IMSLogon](imslogoniunknown.md). 
  
Para obter informações gerais sobre o processo de notificação, consulte a [Notificação de evento em MAPI](event-notification-in-mapi.md). 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

A implementação de **OnNotify** consistirá normalmente um ou mais blocos de código para cada tipo de notificação que você espera receber. Dentro desses blocos de código, execute qualquer tarefa que você considere necessário como uma resposta à notificação. Por exemplo, suponha que você registre-se para receber notificações de **fnevObjectModified** em uma pasta que está incluído em uma exibição da caixa de diálogo. No bloco de código que você incluir no seu método **OnNotify** para manipular notificações de **fnevObjectModified** , você pode enviar uma mensagem de Windows à caixa de diálogo para solicitar um vídeo atualizado. 
  
Não modifique ou livre a estrutura de **notificação** passada para **OnNotify**. Os dados na estrutura são válidos somente até **OnNotify** retorna. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Quando ocorrem alterações a vários objetos, você pode notificar um coletor de advise registrados em uma única chamada de **OnNotify** ou em várias chamadas dependendo restrições de memória. Isso ocorre mesmo se as alterações são o resultado da chamada de um método ou várias. Por exemplo, uma chamada para [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) pode afetar várias mensagens e pastas. Como um provedor de armazenamento de mensagem, você pode fazer uma chamada de **OnNotify** com um tipo de evento **fnevObjectModified** para a pasta de destino ou o número de chamadas, um para cada mensagens afetam. Da mesma forma, se um cliente faz chamadas repetidas para [IMAPIFolder::CreateMessage](imapifolder-createmessage.md), essas chamadas podem ser combinadas em um evento **fnevObjectModified** para a pasta ou separadas em individuais **fnevObjectCreated** eventos para cada nova mensagem. 
  
Para obter mais informações sobre como e quando gerar notificações, consulte [Notificação de evento em MAPI](event-notification-in-mapi.md) e [Suporte a notificação de evento](supporting-event-notification.md). 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|AdviseSink.h e AdviseSink.cpp  <br/> |CAdviseSink::OnNotifyDesc  <br/> |A classe CAdviseSink é implementada para lidar com todas as notificações de MFCMAPI.  <br/> |
   
## <a name="see-also"></a>Confira também



[HrAllocAdviseSink](hrallocadvisesink.md)
  
[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPISupport::Notify](imapisupport-notify.md)
  
[NOTIFICAÇÃO](notification.md)
  
[IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

