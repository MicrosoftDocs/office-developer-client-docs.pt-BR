---
title: EXTENDED_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.EXTENDED_NOTIFICATION
api_type:
- COM
ms.assetid: f01fce7b-a038-4002-8bad-0e6a51ae9d05
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a8b49d0b80102f6295f3f717fb123a6581854d5a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415716"
---
# <a name="extendednotification"></a>EXTENDED_NOTIFICATION

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve informações relacionadas a um evento que é específico do provedor de serviços. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _EXTENDED_NOTIFICATION
{
  ULONG ulEvent;
  ULONG cb;
  LPBYTE pbEventParameters;
} EXTENDED_NOTIFICATION;

```

## <a name="members"></a>Members

 **ulEvent**
  
> Código de evento estendido definido pelo provedor.
    
 **cb**
  
> Contagem de bytes nos parâmetros específicos de eventos apontados por **pbEventParameters**. 
    
 **pbEventParameters**
  
> Ponteiro para parâmetros específicos do evento. Os tipos de parâmetros usados dependem do valor do membro **ulEvent** ; esses parâmetros são documentados pelo provedor que emitiu o evento. 
    
## <a name="remarks"></a>Comentários

A estrutura **EXTENDED_NOTIFICATION** é um dos membros da União de estruturas incluído no membro **info** da estrutura de [notificação](notification.md) . Quando o membro **info** de uma estrutura de **notificação** contém uma estrutura **EXTENDED_NOTIFICATION** , o membro **ulEventType** da estrutura de **notificação** é definido como _fnevExtended_.
  
O evento estendido é definido por um provedor de serviços para representar um tipo de alteração que não pode ser abrangido por nenhum dos outros eventos predefinidos. Somente os clientes que conhecem antes eles se registram que um provedor de serviços suporta um evento estendido pode se registrar para esse evento. Não é possível para os clientes determinarem sem conhecimento avançado se um provedor de serviços oferecer suporte a um evento estendido. Se um provedor de serviços oferecer suporte a um evento estendido, mostrará como lidar com esse evento quando ele for recebido.
  
Uma notificação estendida é enviada pela sessão quando um cliente faz logoff. Registre-se para esta notificação chamando [IMAPISession:: Advise](imapisession-advise.md) com o parâmetro _lpEntryID_ definido como NULL e o parâmetro _cbEntryID_ definido como zero. 
  
Para obter mais informações sobre notificação, consulte os tópicos descritos na tabela a seguir.
  
|**Tópico**|**Descrição**|
|:-----|:-----|
|[Notificação de evento no MAPI](event-notification-in-mapi.md) <br/> |Visão geral dos eventos Notification e Notification.  <br/> |
|[Manipular notificações](handling-notifications.md) <br/> |Discussão sobre como os clientes devem lidar com notificações.  <br/> |
|[Notificação de evento de suporte](supporting-event-notification.md) <br/> |Discussão sobre como os provedores de serviços podem usar os métodos [IMAPISupport](imapisupportiunknown.md) para gerar notificações.  <br/> |
   
## <a name="see-also"></a>Confira também



[Notifica](notification.md)


[Estruturas MAPI](mapi-structures.md)

