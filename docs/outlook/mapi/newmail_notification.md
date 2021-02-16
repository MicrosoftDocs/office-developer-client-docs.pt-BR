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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439853"
---
# <a name="newmail_notification"></a>NEWMAIL_NOTIFICATION

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve informações relacionadas à chegada de uma nova mensagem. 
  
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
  
> Contagem de bytes no identificador de entrada apontado pelo membro **lpEntryID.** 
    
 **lpEntryID**
  
> Ponteiro para o identificador de entrada da mensagem recém-chegada.
    
 **cbParentID**
  
> Contagem de bytes no identificador de entrada apontado pelo membro **lpParentID.** 
    
 **lpParentID**
  
> Ponteiro para o identificador de entrada da pasta de recebimento da mensagem recém-chegada.
    
 **ulFlags**
  
> Bitmask de sinalizadores usados para descrever o formato das propriedades de cadeia de caracteres incluídas na mensagem. O sinalizador a seguir pode ser definido:
    
MAPI_UNICODE 
  
> As cadeias de caracteres passadas estão no formato Unicode. Se o MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.
    
 **lpszMessageClass**
  
> Ponteiro para a classe de mensagem da mensagem recém-chegada. 
    
 **ulMessageFlags**
  
> Bitmask de sinalizadores que descreve o estado atual da mensagem recém-chegada. O **membro ulMessageFlags** é uma cópia da propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) da mensagem.
    
## <a name="remarks"></a>Comentários

A **NEWMAIL_NOTIFICATION** estrutura é um dos membros da união de estruturas incluídas no membro **info** da estrutura [NOTIFICATION.](notification.md) Quando o **membro de** informações de uma estrutura **NOTIFICATION** contém uma estrutura **NEWMAIL_NOTIFICATION,** o membro **ulEventType** da estrutura **NOTIFICATION** é definido como  _fnevNewMail._
  
MAPI uses the **NEWMAIL_NOTIFICATION** structure only as a member of the **NOTIFICATION** structure, which holds information about a notification event for the advise sink. 
  
Para obter mais informações sobre a notificação, consulte os tópicos descritos na tabela a seguir.
  
|**Tópico**|**Descrição**|
|:-----|:-----|
|[Notificação de evento em MAPI](event-notification-in-mapi.md) <br/> |Visão geral dos eventos de notificação e notificação.  <br/> |
|[Manipulando notificações](handling-notifications.md) <br/> |Discussão sobre como os clientes devem lidar com notificações.  <br/> |
|[Suporte à notificação de evento](supporting-event-notification.md) <br/> |Discussão sobre como os provedores de serviços podem usar o [método IMAPISupport](imapisupportiunknown.md) para gerar notificações.  <br/> |
   
## <a name="see-also"></a>Confira também



[NOTIFICAÇÃO](notification.md)
  
[Propriedade canônica PidTagMessageFlags](pidtagmessageflags-canonical-property.md)


[Estruturas MAPI](mapi-structures.md)

