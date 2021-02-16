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
ms.openlocfilehash: c637b3b03a22f208123397f7277cf8968f2509a0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430165"
---
# <a name="object_notification"></a>OBJECT_NOTIFICATION

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém informações sobre um objeto que passou por uma alteração, como sendo copiado ou modificado.
  
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
  
> Contagem de bytes no identificador de entrada apontado pelo membro **lpEntryID.** 
    
 **lpEntryID**
  
> Ponteiro para o identificador de entrada do objeto afetado.
    
 **ulObjType**
  
> Tipo de objeto afetado. Os tipos possíveis são os seguinte:
    
MAPI_STORE 
  
> Armazenamento de mensagens. 
    
MAPI_ADDRBOOK 
  
> Address book. 
    
MAPI_FOLDER 
  
> Pasta.
    
MAPI_ABCONT 
  
> Contêiner do livro de endereços.
    
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
  
> Objeto Status.
    
MAPI_SESSION 
  
> Objeto Session.
    
 **cbParentID**
  
> Contagem de bytes no identificador de entrada apontado pelo membro **lpParentID.** 
    
 **lpParentID**
  
> Ponteiro para o identificador de entrada do pai do objeto afetado.
    
 **cbOldID**
  
> Contagem de bytes no identificador de entrada apontado pelo membro **lpOldID.** 
    
 **lpOldID**
  
> Ponteiro para o identificador de entrada do objeto original. Esse ponteiro poderá ser NULL se o evento não exigir um objeto original.
    
 **cbOldParentID**
  
> Contagem de bytes no identificador de entrada apontado pelo membro **lpOldParentID.** 
    
 **lpOldParentID**
  
> Ponteiro para o identificador de entrada do pai do objeto original. Esse ponteiro poderá ser NULL se o evento não exigir um objeto original.
    
 **lpPropTagArray**
  
> Ponteiro para uma [estrutura SPropTagArray](sproptagarray.md) que contém as marcas de propriedade que identificam as propriedades afetadas pelo evento. 
    
## <a name="remarks"></a>Comentários

A **OBJECT_NOTIFICATION** estrutura é um dos membros da união de estruturas incluídas no membro **info** da estrutura [NOTIFICATION.](notification.md) Quando o **membro de** informações de uma estrutura **NOTIFICATION** contém uma estrutura **OBJECT_NOTIFICATION,** o membro **ulEventType** da estrutura **NOTIFICATION** é definido como um dos seguintes tipos de eventos: 
  
- fnevObjectCreated
    
- fnevObjectModified
    
- fnevObjectDeleted
    
- fnevObjectMoved
    
- fnevObjectCopied
    
- fnevSearchComplete
    
O evento de pesquisa completa, representado pelo tipo de evento fnevSearchComplete, indica que a pesquisa inicial do domínio para uma pasta de pesquisa foi concluída.
  
Os membros a seguir que contêm informações sobre o objeto original são usados somente em eventos de movimentação e cópia. 
  
- **cbOldID**
    
- **lpOldID**
    
- **cbOldParentID**
    
- **lpOldParentID**
    
Esses membros não se aplicam aos outros tipos de eventos.
  
Para obter mais informações sobre a notificação, consulte os tópicos descritos na tabela a seguir.
  
|**Tópico**|**Descrição**|
|:-----|:-----|
|[Notificação de evento em MAPI](event-notification-in-mapi.md) <br/> |Visão geral dos eventos de notificação e notificação.  <br/> |
|[Manipulando notificações](handling-notifications.md) <br/> |Discussão sobre como os clientes devem lidar com notificações.  <br/> |
|[Suporte à notificação de evento](supporting-event-notification.md) <br/> |Discussão sobre como os provedores de serviços podem usar o [método IMAPISupport](imapisupportiunknown.md) para gerar notificações.  <br/> |
   
## <a name="see-also"></a>Confira também



[NOTIFICAÇÃO](notification.md)
  
[SPropTagArray](sproptagarray.md)


[Estruturas MAPI](mapi-structures.md)

