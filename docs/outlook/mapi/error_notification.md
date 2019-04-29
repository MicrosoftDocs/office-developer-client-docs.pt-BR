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
ms.openlocfilehash: f8d4fb6b8cd7ad0ebf1e7660a0f3c0602274fa10
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425439"
---
# <a name="errornotification"></a>ERROR_NOTIFICATION

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve informações relacionadas a um erro crítico. Isso faz com que uma notificação de erro seja gerada. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
   
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
  
> Contagem de bytes no identificador de entrada apontado por **lpEntryID**. 
    
 **lpEntryID**
  
> Ponteiro para o identificador de entrada do objeto que causa o erro.
    
 **SCODE**
  
> Valor de erro para o erro crítico. 
    
 **ulFlags**
  
> Bitmask dos sinalizadores usados para designar o formato do texto apontado pelo membro **lpszError** na estrutura indicada por **lpMAPIError**. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> As cadeias de caracteres passadas estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI.
    
 **lpMAPIError**
  
> Ponteiro para uma estrutura [MAPIERROR](mapierror.md) descrevendo o erro. 
    
## <a name="remarks"></a>Comentários

A estrutura **ERROR_NOTIFICATION** é um dos membros da União de estruturas incluído no membro **info** da estrutura de [notificação](notification.md) . Quando o membro **info** de uma estrutura de **notificação** contém uma estrutura **ERROR_NOTIFICATION** , o membro **ulEventType** da estrutura de **notificação** é definido como _fnevCriticalError_.
  
O valor do membro **cbEntryID** e o membro **lpEntryID** podem ser nulos. 
  
Para obter mais informações sobre notificação, consulte os tópicos descritos na tabela a seguir.
  
|**Tópico**|**Descrição**|
|:-----|:-----|
|[Notificação de evento no MAPI](event-notification-in-mapi.md) <br/> |Visão geral dos eventos Notification e Notification.  <br/> |
|[Manipular notificações](handling-notifications.md) <br/> |Discussão sobre como os clientes devem lidar com notificações.  <br/> |
|[Notificação de evento de suporte](supporting-event-notification.md) <br/> |Discussão sobre como os provedores de serviços podem usar o método **IMAPISupport** para gerar notificações.  <br/> |
   
## <a name="see-also"></a>Confira também



[MAPIERROR](mapierror.md)
  
[Notifica](notification.md)


[Estruturas MAPI](mapi-structures.md)

