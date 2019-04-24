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
ms.openlocfilehash: 84b44b4b054a2b2617502a6a463a6d4a89546804
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336439"
---
# <a name="statusobjectnotification"></a>STATUS_OBJECT_NOTIFICATION

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve um objeto de status que foi afetado por uma alteração. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
   
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
  
> Contagem de estruturas [SPropValue](spropvalue.md) na matriz apontada pelo membro **lpPropVals** . 
    
 **lpPropVals**
  
> Ponteiro para uma matriz de estruturas **SPropValue** que descrevem as propriedades do objeto status alterado. 
    
## <a name="remarks"></a>Comentários

A estrutura **STATUS_OBJECT_NOTIFICATION** é um dos membros da União de estruturas incluído no membro **info** da estrutura de [notificação](notification.md) . A estrutura **STATUS_OBJECT_NOTIFICATION** é incluída em uma notificação de objeto status para um evento do tipo _fnevStatusObjectModified_. Status o objeto Notification é uma notificação de MAPI interno; Os clientes e provedores de serviço não podem se registrar para os provedores de serviços e de ti não podem gerá-lo.
  
Para obter mais informações sobre notificação, consulte os tópicos descritos na tabela a seguir.
  
|**Tópico**|**Descrição**|
|:-----|:-----|
|[Notificação de evento no MAPI](event-notification-in-mapi.md) <br/> |Visão geral dos eventos Notification e Notification.  <br/> |
|[Manipular notificações](handling-notifications.md) <br/> |Discussão sobre como os clientes devem lidar com notificações.  <br/> |
|[Notificação de evento de suporte](supporting-event-notification.md) <br/> |Discussão sobre como os provedores de serviços podem usar o método **IMAPISupport** para gerar notificações.  <br/> |
   
## <a name="see-also"></a>Confira também



[NOTIFICATION](notification.md)
  
[SPropValue](spropvalue.md)


[Estruturas MAPI](mapi-structures.md)

