---
title: OBJECT_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OBJECT_NOTIFICATION
api_type:
- COM
ms.assetid: de3a2297-e0cc-427b-a978-52bade4d9bce
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 876c8fc3667929e3c2e7403e71e6d392981d34f1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573352"
---
# <a name="objectnotification"></a>OBJECT_NOTIFICATION

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém informações sobre um objeto que sofreram uma alteração, tais como sendo copiado ou modificado.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _OBJECT_NOTIFICATION
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  ULONG ulObjType;
  ULONG cbParentID;
  LPENTRYID lpParentID;
  ULONG cbOldID;
  LPENTRYID lpOldID;
  ULONG cbOldParentID;
  LPENTRYID lpOldParentID;
  LPSPropTagArray lpPropTagArray;
} OBJECT_NOTIFICATION;

```

## <a name="members"></a>Members

 **cbEntryID**
  
> Contagem de bytes no identificador de entrada apontado pelo membro **lpEntryID** . 
    
 **lpEntryID**
  
> Ponteiro para o identificador de entrada do objeto afetado.
    
 **ulObjType**
  
> Tipo de objeto afetado. Os tipos possíveis são:
    
MAPI_STORE 
  
> Armazenamento de mensagens. 
    
MAPI_ADDRBOOK 
  
> Catálogo de endereços. 
    
MAPI_FOLDER 
  
> Pasta.
    
MAPI_ABCONT 
  
> Contêiner de catálogo de endereços.
    
MAPI_MESSAGE 
  
> Mensagem.
    
MAPI_MAILUSER 
  
> Usuário de mensagens.
    
MAPI_ATTACH 
  
> Anexo.
    
MAPI_DISTLIST 
  
> Lista de distribuição.
    
MAPI_PROFSECT 
  
> Seção de perfil.
    
MAPI_STATUS 
  
> Objeto de status.
    
MAPI_SESSION 
  
> Objeto da sessão.
    
 **cbParentID**
  
> Contagem de bytes no identificador de entrada apontado pelo membro **lpParentID** . 
    
 **lpParentID**
  
> Ponteiro para o identificador de entrada do pai do objeto afetado.
    
 **cbOldID**
  
> Contagem de bytes no identificador de entrada apontado pelo membro **lpOldID** . 
    
 **lpOldID**
  
> Ponteiro para o identificador de entrada do objeto original. Esse ponteiro pode ser NULL se o evento não exigir um objeto original.
    
 **cbOldParentID**
  
> Contagem de bytes no identificador de entrada apontado pelo membro **lpOldParentID** . 
    
 **lpOldParentID**
  
> Ponteiro para o identificador de entrada do pai do objeto original. Esse ponteiro pode ser NULL se o evento não exigir um objeto original.
    
 **lpPropTagArray**
  
> Ponteiro para uma estrutura [SPropTagArray](sproptagarray.md) que contém as marcas de propriedade identificando propriedades afetadas pelo evento. 
    
## <a name="remarks"></a>Comentários

A estrutura **OBJECT_NOTIFICATION** é um dos membros da união de estruturas incluídos no membro **info** da estrutura de [notificação](notification.md) . Quando o membro de **informações** de uma estrutura de **notificação** contém uma estrutura **OBJECT_NOTIFICATION** , o membro **ulEventType** da estrutura de **notificação** é definido como um dos seguintes tipos de eventos: 
  
- fnevObjectCreated
    
- fnevObjectModified
    
- fnevObjectDeleted
    
- fnevObjectMoved
    
- fnevObjectCopied
    
- fnevSearchComplete
    
O evento complete de pesquisa, representado pelo tipo de evento fnevSearchComplete, indica se a pesquisa inicial do domínio para a pasta de pesquisa de um foi concluída.
  
Os seguintes membros que contêm informações sobre o objeto original são usados somente nos eventos de mover e copiar. 
  
- **cbOldID**
    
- **lpOldID**
    
- **cbOldParentID**
    
- **lpOldParentID**
    
Esses membros não se aplicam aos outros tipos de eventos.
  
Para obter mais informações sobre a notificação, consulte os tópicos descritos na tabela a seguir.
  
|**Tópico**|**Descrição**|
|:-----|:-----|
|[Notificações de eventos no MAPI](event-notification-in-mapi.md) <br/> |Visão geral de notificação e eventos de notificação.  <br/> |
|[Lidar com notificações](handling-notifications.md) <br/> |Discussão sobre como os clientes devem manipular notificações.  <br/> |
|[Suporte à notificação de eventos](supporting-event-notification.md) <br/> |Discussão sobre como provedores de serviços podem usar o método [IMAPISupport](imapisupportiunknown.md) para gerar notificações.  <br/> |
   
## <a name="see-also"></a>Confira também



[NOTIFICAÇÃO](notification.md)
  
[SPropTagArray](sproptagarray.md)


[Estruturas MAPI](mapi-structures.md)

