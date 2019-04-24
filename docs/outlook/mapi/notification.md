---
title: NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.NOTIFICATION
api_type:
- COM
ms.assetid: 01b6e695-a649-4efd-a893-7586b476467e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a3235c2305d61318f482943167e5f307e5da0d70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280096"
---
# <a name="notification"></a>NOTIFICATION
 
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém informações sobre um evento que ocorreu e os dados afetados pelo evento.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct
{
  ULONG ulEventType;
  union
  {
    ERROR_NOTIFICATION err;
    NEWMAIL_NOTIFICATION newmail;
    OBJECT_NOTIFICATION obj;
    TABLE_NOTIFICATION tab;
    EXTENDED_NOTIFICATION ext;
    STATUS_OBJECT_NOTIFICATION statobj;
  } info;
} NOTIFICATION, FAR *LPNOTIFICATION;

```

## <a name="members"></a>Members

**ulEventType**
  
> Tipo de evento de notificação que ocorreu. O valor do membro **ulEventType** corresponde à estrutura que está incluída na União **info** . O membro **ulEventType** pode ser definido como um dos seguintes valores: 
    
 _fnevCriticalError_
  
> Ocorreu um erro global, como uma sessão desligada em andamento. O membro **info** contém uma estrutura [ERROR_NOTIFICATION](error_notification.md) . 
    
 _fnevExtended_
  
> Um evento interno definido por um determinado provedor de serviços ocorreu. O membro **info** contém uma estrutura [EXTENDED_NOTIFICATION](extended_notification.md) . 
    
 _fnevNewMail_
  
> Uma mensagem foi entregue à pasta de recebimento apropriada para a classe de mensagem e está aguardando para ser processada. O membro **info** contém uma estrutura [NEWMAIL_NOTIFICATION](newmail_notification.md) . 
    
 _fnevObjectCopied_
  
> Um objeto MAPI foi copiado. O membro **info** contém uma estrutura [OBJECT_NOTIFICATION](object_notification.md) . 
    
 _fnevObjectCreated_
  
> Um objeto MAPI foi criado. O membro **info** contém uma estrutura **OBJECT_NOTIFICATION** . 
    
 _fnevObjectDeleted_
  
> Um objeto MAPI foi excluído. O membro **info** contém uma estrutura **OBJECT_NOTIFICATION** . 
    
 _fnevObjectModified_
  
> Um objeto MAPI foi alterado. O membro **info** contém uma estrutura **OBJECT_NOTIFICATION** . 
    
 _fnevObjectMoved_
  
> Um objeto de repositório de mensagens ou de catálogo de endereços foi movido. O membro **info** contém uma estrutura **OBJECT_NOTIFICATION** . 
    
 _fnevSearchComplete_
  
> Uma operação de pesquisa foi concluída e os resultados estão disponíveis. O membro **info** contém uma estrutura **OBJECT_NOTIFICATION** . 
    
 _fnevTableModified_
  
> As informações em uma tabela foram alteradas. O membro **info** contém uma estrutura [TABLE_NOTIFICATION](table_notification.md) . 
    
**informações**
  
> União de estruturas de notificação descrevendo os dados afetados para um tipo específico de evento. A estrutura incluída no membro **info** depende do valor do membro **ulEventType** . 
    
## <a name="remarks"></a>Comentários

Uma ou mais estruturas de **notificação** são passadas como parâmetros de entrada com cada chamada para o método [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) de um coletor de aviso registrado. As estruturas de **notificação** contêm informações sobre os eventos específicos que ocorreram e descrevem os objetos afetados. 
  
Antes que os clientes ou provedores de serviços que recebem uma notificação podem usar a estrutura para processar o evento, eles devem verificar o tipo de evento conforme indicado no membro **ulEventType** . Por exemplo, o exemplo de código mostrado aqui verifica a chegada de uma nova mensagem e, após detectar um evento desse tipo, imprime a classe de mensagem da mensagem. 
  
```cpp
if (pNotif -> ulEventType == fnevNewMail)
{
printf("%s\n", pNotif -> newmail.lpszMessageClass)
}

```

Para obter mais informações sobre notificação, consulte os tópicos descritos na tabela a seguir.
  
|**Tópico**|**Descrição**|
|:-----|:-----|
|[Notificação de evento no MAPI](event-notification-in-mapi.md) <br/> |Visão geral dos eventos Notification e Notification.  <br/> |
|[Manipular notificações](handling-notifications.md) <br/> |Discussão sobre como os clientes devem lidar com notificações.  <br/> |
|[Notificação de evento de suporte](supporting-event-notification.md) <br/> |Discussão sobre como os provedores de serviços podem usar o método [IMAPISupport](imapisupportiunknown.md) para gerar notificações.  <br/> |
   
## <a name="see-also"></a>Confira também


- [ERROR_NOTIFICATION](error_notification.md)  
- [EXTENDED_NOTIFICATION](extended_notification.md)  
- [NEWMAIL_NOTIFICATION](newmail_notification.md)  
- [OBJECT_NOTIFICATION](object_notification.md)  
- [STATUS_OBJECT_NOTIFICATION](status_object_notification.md)  
- [TABLE_NOTIFICATION](table_notification.md)
- [Estruturas MAPI](mapi-structures.md)

