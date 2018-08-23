---
title: ERROR_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ERROR_NOTIFICATION
api_type:
- COM
ms.assetid: 6c5bb383-f8e2-4d79-bcf2-aa86c130e8b1
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2405799fa59abf58583553f8e2d3718d68411a19
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574969"
---
# <a name="errornotification"></a>ERROR_NOTIFICATION

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve as informações que se relacionam com um erro crítico. Isso faz com que uma notificação de erro a serem gerados. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _ERROR_NOTIFICATION
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  SCODE scode;
  ULONG ulFlags;
  LPMAPIERROR lpMAPIError;
} ERROR_NOTIFICATION;
```

## <a name="members"></a>Members

 **cbEntryID**
  
> Contagem de bytes no identificador de entrada apontado pela **lpEntryID**. 
    
 **lpEntryID**
  
> Ponteiro para o identificador de entrada do objeto que faz com que o erro.
    
 **SCODE**
  
> Valor de erro para o erro crítico. 
    
 **ulFlags**
  
> Bitmask dos sinalizadores usados para designar o formato do texto apontado pelo membro **lpszError** na estrutura apontado pela **lpMAPIError**. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> As cadeias de caracteres passada na estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.
    
 **lpMAPIError**
  
> Ponteiro para uma estrutura [MAPIERROR](mapierror.md) descrevendo o erro. 
    
## <a name="remarks"></a>Comentários

A estrutura **ERROR_NOTIFICATION** é um dos membros da união de estruturas incluídos no membro **info** da estrutura de [notificação](notification.md) . Quando o membro de **informações** de uma estrutura de **notificação** contém uma estrutura **ERROR_NOTIFICATION** , o membro **ulEventType** da estrutura de **notificação** é definido para _fnevCriticalError_.
  
O valor do membro **cbEntryID** e o membro **lpEntryID** pode ser NULL. 
  
Para obter mais informações sobre a notificação, consulte os tópicos descritos na tabela a seguir.
  
|**Tópico**|**Descrição**|
|:-----|:-----|
|[Notificações de eventos no MAPI](event-notification-in-mapi.md) <br/> |Visão geral de notificação e eventos de notificação.  <br/> |
|[Lidar com notificações](handling-notifications.md) <br/> |Discussão sobre como os clientes devem manipular notificações.  <br/> |
|[Suporte à notificação de eventos](supporting-event-notification.md) <br/> |Discussão sobre como provedores de serviços podem usar o método **IMAPISupport** para gerar notificações.  <br/> |
   
## <a name="see-also"></a>Confira também



[MAPIERROR](mapierror.md)
  
[NOTIFICAÇÃO](notification.md)


[Estruturas MAPI](mapi-structures.md)

