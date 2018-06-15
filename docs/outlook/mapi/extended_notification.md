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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 5e23d9b829a941e3add8b8d8e137c73052b08aa6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19766527"
---
# <a name="extendednotification"></a>EXTENDED_NOTIFICATION

  
  
**Aplica-se a**: Outlook 
  
Descreve as informações relacionadas a um evento que é específico do provedor de serviço. 
  
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

## <a name="members"></a>Membros

 **ulEvent**
  
> Código de evento estendidas que é definido pelo provedor.
    
 **cb**
  
> Contagem de bytes nos parâmetros específicos do evento apontado pela **pbEventParameters**. 
    
 **pbEventParameters**
  
> Ponteiro para os parâmetros de eventos específicos. O tipo de parâmetros que são usados depende do valor do membro **ulEvent** ; Esses parâmetros são documentados pelo provedor que emitiu o evento. 
    
## <a name="remarks"></a>Coment�rios

A estrutura **EXTENDED_NOTIFICATION** é um dos membros da união de estruturas incluídos no membro **info** da estrutura de [notificação](notification.md) . Quando o membro de **informações** de uma estrutura de **notificação** contém uma estrutura **EXTENDED_NOTIFICATION** , o membro **ulEventType** da estrutura de **notificação** é definido para _fnevExtended_.
  
O evento estendido é definido por um provedor de serviços para representar um tipo de alteração que não pode ser coberto por qualquer um dos outros eventos predefinidos. Somente os clientes que saber antes de se registram que um provedor de serviços oferece suporte a um evento estendido podem se inscrever para o evento. Não é possível para os clientes determinar sem o conhecimento avançado, se um evento estendido oferece suporte a um provedor de serviços. Se um provedor de serviços oferece suporte a um evento estendido, ele mostra como lidar com esse evento quando ele for recebido.
  
Uma notificação estendida é enviada da sessão quando um cliente fizer logoff. Registre-se para essa notificação chamando [IMAPISession::Advise](imapisession-advise.md) com o parâmetro _lpEntryID_ definido como NULL e o parâmetro _cbEntryID_ definido como zero. 
  
Para obter mais informações sobre a notificação, consulte os tópicos descritos na tabela a seguir.
  
|**Tópico**|**Descrição**|
|:-----|:-----|
|[Notificação de evento em MAPI](event-notification-in-mapi.md) <br/> |Visão geral de notificação e eventos de notificação.  <br/> |
|[Manipular notificações](handling-notifications.md) <br/> |Discussão sobre como os clientes devem manipular notificações.  <br/> |
|[Suporte de notificação de evento](supporting-event-notification.md) <br/> |Discussão sobre como provedores de serviços podem usar os métodos [IMAPISupport](imapisupportiunknown.md) para gerar notificações.  <br/> |
   
## <a name="see-also"></a>Confira também



[NOTIFICAÇÃO](notification.md)


[Estruturas MAPI](mapi-structures.md)

