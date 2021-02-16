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
# <a name="extended_notification"></a>EXTENDED_NOTIFICATION

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve informações relacionadas a um evento específico do provedor de serviços. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
   
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
  
> Contagem de bytes nos parâmetros específicos do evento apontados por **pbEventParameters**. 
    
 **pbEventParameters**
  
> Ponteiro para parâmetros específicos do evento. O tipo de parâmetros que são usados depende do valor do **membro ulEvent;** esses parâmetros são documentados pelo provedor que emitiu o evento. 
    
## <a name="remarks"></a>Comentários

A **EXTENDED_NOTIFICATION** estrutura é um dos membros da união de estruturas incluídas no membro **info** da estrutura [NOTIFICATION.](notification.md) Quando o **membro de** informações de uma estrutura **NOTIFICATION** contém uma estrutura **EXTENDED_NOTIFICATION,** o membro **ulEventType** da estrutura **NOTIFICATION** é definido como  _fnevExtended_.
  
O evento estendido é definido por um provedor de serviços para representar um tipo de alteração que não pode ser coberto por nenhum dos outros eventos predefinidos. Somente clientes que sabem antes de registrar que um provedor de serviços oferece suporte a um evento estendido podem se registrar para esse evento. Não é possível para os clientes determinar sem conhecimento avançado se um provedor de serviços oferece suporte a um evento estendido. Se um provedor de serviços suportar um evento estendido, ele mostra como manipular esse evento quando ele é recebido.
  
Uma notificação estendida é enviada pela sessão quando um cliente faz o login. Registre-se para essa notificação chamando [IMAPISession::Advise](imapisession-advise.md) com o parâmetro  _lpEntryID_ definido como NULL e o parâmetro  _cbEntryID_ definido como zero. 
  
Para obter mais informações sobre a notificação, consulte os tópicos descritos na tabela a seguir.
  
|**Tópico**|**Descrição**|
|:-----|:-----|
|[Notificação de evento em MAPI](event-notification-in-mapi.md) <br/> |Visão geral dos eventos de notificação e notificação.  <br/> |
|[Manipulando notificações](handling-notifications.md) <br/> |Discussão sobre como os clientes devem lidar com notificações.  <br/> |
|[Suporte à notificação de evento](supporting-event-notification.md) <br/> |Discussão sobre como os provedores de serviços podem usar os [métodos IMAPISupport](imapisupportiunknown.md) para gerar notificações.  <br/> |
   
## <a name="see-also"></a>Confira também



[NOTIFICAÇÃO](notification.md)


[Estruturas MAPI](mapi-structures.md)

