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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426265"
---
# <a name="status_object_notification"></a>STATUS_OBJECT_NOTIFICATION

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve um objeto de status que foi afetado por uma alteração. 
  
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
  
> Contagem de bytes no identificador de entrada apontado pelo membro **lpEntryID.** 
    
 **lpEntryID**
  
> Ponteiro para o identificador de entrada do objeto de status alterado.
    
 **cValues**
  
> Contagem de [estruturas SPropValue](spropvalue.md) na matriz apontada pelo membro **lpPropVals.** 
    
 **lpPropVals**
  
> Ponteiro para uma matriz de **estruturas SPropValue** que descrevem as propriedades do objeto de status alterado. 
    
## <a name="remarks"></a>Comentários

A **STATUS_OBJECT_NOTIFICATION** estrutura é um dos membros da união de estruturas incluídas no membro **info** da estrutura [NOTIFICATION.](notification.md) A **STATUS_OBJECT_NOTIFICATION** estrutura é incluída com uma notificação de objeto de status para um evento do tipo  _fnevStatusObjectModified_. Notificação de objeto de status é uma notificação MAPI interna; clientes e provedores de serviços não podem se registrar para ele e os provedores de serviços não podem gerá-lo.
  
Para obter mais informações sobre a notificação, consulte os tópicos descritos na tabela a seguir.
  
|**Tópico**|**Descrição**|
|:-----|:-----|
|[Notificação de evento em MAPI](event-notification-in-mapi.md) <br/> |Visão geral dos eventos de notificação e notificação.  <br/> |
|[Manipulando notificações](handling-notifications.md) <br/> |Discussão sobre como os clientes devem lidar com notificações.  <br/> |
|[Suporte à notificação de evento](supporting-event-notification.md) <br/> |Discussão sobre como os provedores de serviços podem usar o **método IMAPISupport** para gerar notificações.  <br/> |
   
## <a name="see-also"></a>Confira também



[NOTIFICAÇÃO](notification.md)
  
[SPropValue](spropvalue.md)


[Estruturas MAPI](mapi-structures.md)

