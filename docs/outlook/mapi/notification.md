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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432874"
---
# <a name="notification"></a>NOTIFICATION
 
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém informações sobre um evento que ocorreu e os dados que foram afetados pelo evento.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
   
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
  
> Tipo de evento de notificação que ocorreu. O valor do **membro ulEventType** corresponde à estrutura incluída na união **de** informações. O **membro ulEventType** pode ser definido como um dos seguintes valores: 
    
 _fnevCriticalError_
  
> Ocorreu um erro global, como o desligar de uma sessão em andamento. O **membro de** informações contém uma [ERROR_NOTIFICATION](error_notification.md) estrutura. 
    
 _fnevExtended_
  
> Ocorreu um evento interno definido por um provedor de serviços específico. O **membro de** informações contém uma [EXTENDED_NOTIFICATION](extended_notification.md) estrutura. 
    
 _fnevNewMail_
  
> Uma mensagem foi entregue à pasta de recebimento apropriada para a classe de mensagens e está aguardando para ser processada. O **membro** de informações contém uma [NEWMAIL_NOTIFICATION](newmail_notification.md) estrutura. 
    
 _fnevObjectCopied_
  
> Um objeto MAPI foi copiado. O **membro** de informações contém uma [OBJECT_NOTIFICATION](object_notification.md) estrutura. 
    
 _fnevObjectCreated_
  
> Um objeto MAPI foi criado. O **membro** de informações contém uma **OBJECT_NOTIFICATION** estrutura. 
    
 _fnevObjectDeleted_
  
> Um objeto MAPI foi excluído. O **membro** de informações contém uma **OBJECT_NOTIFICATION** estrutura. 
    
 _fnevObjectModified_
  
> Um objeto MAPI foi alterado. O **membro** de informações contém uma **OBJECT_NOTIFICATION** estrutura. 
    
 _fnevObjectMoved_
  
> Um objeto de armazenamento de mensagens ou de um livro de endereços foi movido. O **membro** de informações contém uma **OBJECT_NOTIFICATION** estrutura. 
    
 _fnevSearchComplete_
  
> Uma operação de pesquisa foi concluída e os resultados estão disponíveis. O **membro** de informações contém uma **OBJECT_NOTIFICATION** estrutura. 
    
 _fnevTableModified_
  
> As informações em uma tabela foram alteradas. O **membro de** informações contém uma [TABLE_NOTIFICATION](table_notification.md) estrutura. 
    
**informações**
  
> União de estruturas de notificação que descrevem os dados afetados para um tipo específico de evento. A estrutura incluída no membro **info** depende do valor do **membro ulEventType.** 
    
## <a name="remarks"></a>Comentários

Uma ou mais estruturas **notification** são passadas como parâmetros de entrada com cada chamada para o método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) de um pia de aviso registrado. As **estruturas** NOTIFICATION contêm informações sobre os eventos específicos que ocorreram e descrevem os objetos afetados. 
  
Antes que os clientes ou provedores de serviços que recebem uma notificação possam usar a estrutura para processar o evento, eles devem verificar o tipo de evento conforme indicado no **membro ulEventType.** Por exemplo, o exemplo de código mostrado aqui verifica a chegada de uma nova mensagem e, ao detectar um evento desse tipo, imprime a classe de mensagem da mensagem. 
  
```cpp
if (pNotif -> ulEventType == fnevNewMail)
{
printf("%s\n", pNotif -> newmail.lpszMessageClass)
}

```

Para obter mais informações sobre a notificação, consulte os tópicos descritos na tabela a seguir.
  
|**Tópico**|**Descrição**|
|:-----|:-----|
|[Notificação de evento em MAPI](event-notification-in-mapi.md) <br/> |Visão geral dos eventos de notificação e notificação.  <br/> |
|[Manipulando notificações](handling-notifications.md) <br/> |Discussão sobre como os clientes devem lidar com notificações.  <br/> |
|[Suporte à notificação de evento](supporting-event-notification.md) <br/> |Discussão sobre como os provedores de serviços podem usar o [método IMAPISupport](imapisupportiunknown.md) para gerar notificações.  <br/> |
   
## <a name="see-also"></a>Confira também


- [ERROR_NOTIFICATION](error_notification.md)  
- [EXTENDED_NOTIFICATION](extended_notification.md)  
- [NEWMAIL_NOTIFICATION](newmail_notification.md)  
- [OBJECT_NOTIFICATION](object_notification.md)  
- [STATUS_OBJECT_NOTIFICATION](status_object_notification.md)  
- [TABLE_NOTIFICATION](table_notification.md)
- [Estruturas MAPI](mapi-structures.md)

