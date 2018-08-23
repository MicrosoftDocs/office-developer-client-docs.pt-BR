---
title: NEWMAIL_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.NEWMAIL_NOTIFICATION
api_type:
- COM
ms.assetid: 49913050-900a-4b05-84c4-c596a93ce68b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 779585f73a7032ae0259b30ebfc16868c733c7fc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569509"
---
# <a name="newmailnotification"></a>NEWMAIL_NOTIFICATION

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve as informações que se relacionam com a chegada de uma nova mensagem. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _NEWMAIL_NOTIFICATION
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  ULONG cbParentID;
  LPENTRYID lpParentID;
  ULONG ulFlags;
  LPSTR lpszMessageClass;
  ULONG ulMessageFlags;
} NEWMAIL_NOTIFICATION;

```

## <a name="members"></a>Members

 **cbEntryID**
  
> Contagem de bytes no identificador de entrada apontado pelo membro **lpEntryID** . 
    
 **lpEntryID**
  
> Ponteiro para o identificador de entrada da mensagem chegar recentemente.
    
 **cbParentID**
  
> Contagem de bytes no identificador de entrada apontado pelo membro **lpParentID** . 
    
 **lpParentID**
  
> Ponteiro para o identificador de entrada da pasta de recebimento da mensagem que acabou de chegar.
    
 **ulFlags**
  
> Bitmask dos sinalizadores usados para descrever o formato das propriedades de cadeia de caracteres incluído na mensagem. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> As cadeias de caracteres passada na estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.
    
 **lpszMessageClass**
  
> Ponteiro para a classe de mensagem da mensagem chegar recentemente. 
    
 **ulMessageFlags**
  
> Bitmask dos sinalizadores que descreve o estado atual da mensagem chegar recentemente. O membro **ulMessageFlags** é uma cópia de propriedade de **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) da mensagem.
    
## <a name="remarks"></a>Comentários

A estrutura **NEWMAIL_NOTIFICATION** é um dos membros da união de estruturas incluídos no membro **info** da estrutura de [notificação](notification.md) . Quando o membro de **informações** de uma estrutura de **notificação** contém uma estrutura **NEWMAIL_NOTIFICATION** , o membro **ulEventType** da estrutura de **notificação** é definido como _fnevNewMail._
  
MAPI usa a estrutura **NEWMAIL_NOTIFICATION** somente como um membro da estrutura de **notificação** , que mantém informações sobre um evento de notificação para o coletor de eventos advise. 
  
Para obter mais informações sobre a notificação, consulte os tópicos descritos na tabela a seguir.
  
|**Tópico**|**Descrição**|
|:-----|:-----|
|[Notificações de eventos no MAPI](event-notification-in-mapi.md) <br/> |Visão geral de notificação e eventos de notificação.  <br/> |
|[Lidar com notificações](handling-notifications.md) <br/> |Discussão sobre como os clientes devem manipular notificações.  <br/> |
|[Suporte à notificação de eventos](supporting-event-notification.md) <br/> |Discussão sobre como provedores de serviços podem usar o método [IMAPISupport](imapisupportiunknown.md) para gerar notificações.  <br/> |
   
## <a name="see-also"></a>Confira também



[NOTIFICAÇÃO](notification.md)
  
[Propriedade canônica PidTagMessageFlags](pidtagmessageflags-canonical-property.md)


[Estruturas MAPI](mapi-structures.md)

