---
title: STATUS_OBJECT_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.STATUS_OBJECT_NOTIFICATION
api_type:
- COM
ms.assetid: 2872130d-a36b-46ea-bfd1-4700fe3dd41b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 71e0a08436c925f0d68d63111722cc01bd73cc5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770517"
---
# <a name="statusobjectnotification"></a>STATUS_OBJECT_NOTIFICATION

  
  
**Aplica-se a**: Outlook 
  
Descreve um objeto de status que tenha sido afetado por uma alteração. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  ULONG cValues;
  LPSPropValue lpPropVals;
} STATUS_OBJECT_NOTIFICATION;

```

## <a name="members"></a>Members

 **cbEntryID**
  
> Contagem de bytes no identificador de entrada apontado pelo membro **lpEntryID** . 
    
 **lpEntryID**
  
> Ponteiro para o identificador de entrada do objeto status alterado.
    
 **cValues**
  
> Contagem de estruturas de [SPropValue](spropvalue.md) na matriz apontado pelo membro **lpPropVals** . 
    
 **lpPropVals**
  
> Ponteiro para uma matriz de estruturas de **SPropValue** que descrevem as propriedades do objeto status alterado. 
    
## <a name="remarks"></a>Comentários

A estrutura **STATUS_OBJECT_NOTIFICATION** é um dos membros da união de estruturas incluídos no membro **info** da estrutura de [notificação](notification.md) . A estrutura **STATUS_OBJECT_NOTIFICATION** está incluída com uma notificação de objeto de status para um evento do tipo _fnevStatusObjectModified_. Notificação de status de objeto é uma notificação de MAPI interna; clientes e provedores de serviços não é possível registrar para ele e provedores de serviços não é possível gerar a ele.
  
Para obter mais informações sobre a notificação, consulte os tópicos descritos na tabela a seguir.
  
|**Tópico**|**Descrição**|
|:-----|:-----|
|[Notificações de eventos no MAPI](event-notification-in-mapi.md) <br/> |Visão geral de notificação e eventos de notificação.  <br/> |
|[Lidar com notificações](handling-notifications.md) <br/> |Discussão sobre como os clientes devem manipular notificações.  <br/> |
|[Suporte à notificação de eventos](supporting-event-notification.md) <br/> |Discussão sobre como provedores de serviços podem usar o método **IMAPISupport** para gerar notificações.  <br/> |
   
## <a name="see-also"></a>Confira também



[NOTIFICAÇÃO](notification.md)
  
[SPropValue](spropvalue.md)


[Estruturas MAPI](mapi-structures.md)

