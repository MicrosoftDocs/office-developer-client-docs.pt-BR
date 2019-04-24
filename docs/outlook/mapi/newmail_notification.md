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
ms.openlocfilehash: 25af1c1b05618d4f36a43721e71be6ff5c7c597f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326240"
---
# <a name="newmailnotification"></a>NEWMAIL_NOTIFICATION

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve informações relacionadas à chegada de uma nova mensagem. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
   
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
  
> Ponteiro para o identificador de entrada da mensagem recém-criada.
    
 **cbParentID**
  
> Contagem de bytes no identificador de entrada apontado pelo membro **lpParentID** . 
    
 **lpParentID**
  
> Ponteiro para o identificador de entrada da pasta de recebimento da mensagem recém-criada.
    
 **ulFlags**
  
> Bitmask dos sinalizadores usados para descrever o formato das propriedades de cadeia de caracteres incluídas na mensagem. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> As cadeias de caracteres passadas estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI.
    
 **lpszMessageClass**
  
> Ponteiro para a classe de mensagem da mensagem que chegou recentemente. 
    
 **ulMessageFlags**
  
> Bitmask de sinalizadores que descreve o estado atual da mensagem que acabou de chegar. O membro **ulMessageFlags** é uma cópia da propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) da mensagem.
    
## <a name="remarks"></a>Comentários

A estrutura **NEWMAIL_NOTIFICATION** é um dos membros da União de estruturas incluído no membro **info** da estrutura de [notificação](notification.md) . Quando o membro **info** de uma estrutura de **notificação** contém uma estrutura **NEWMAIL_NOTIFICATION** , o membro **ulEventType** da estrutura de **notificação** é definido como _fnevNewMail._
  
MAPI usa a estrutura **NEWMAIL_NOTIFICATION** somente como membro da estrutura de **notificação** , que contém informações sobre um evento de notificação para o coletor de aviso. 
  
Para obter mais informações sobre notificação, consulte os tópicos descritos na tabela a seguir.
  
|**Tópico**|**Descrição**|
|:-----|:-----|
|[Notificação de evento no MAPI](event-notification-in-mapi.md) <br/> |Visão geral dos eventos Notification e Notification.  <br/> |
|[Manipular notificações](handling-notifications.md) <br/> |Discussão sobre como os clientes devem lidar com notificações.  <br/> |
|[Notificação de evento de suporte](supporting-event-notification.md) <br/> |Discussão sobre como os provedores de serviços podem usar o método [IMAPISupport](imapisupportiunknown.md) para gerar notificações.  <br/> |
   
## <a name="see-also"></a>Confira também



[NOTIFICATION](notification.md)
  
[Propriedade canônica PidTagMessageFlags](pidtagmessageflags-canonical-property.md)


[Estruturas MAPI](mapi-structures.md)

