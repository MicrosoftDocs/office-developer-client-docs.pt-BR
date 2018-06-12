---
title: NOTIFICAÇÃO
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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 7a8d25dc7cac4226f38baab593b254108210549e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768175"
---
# <a name="notification"></a>NOTIFICAÇÃO
 
**Aplica-se a**: Outlook 
  
Contém informações sobre um evento que ocorreu e os dados que foi afetados pelo evento.
  
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

## <a name="members"></a>Membros

**ulEventType**
  
> Tipo de evento de notificação que ocorreu. O valor do membro **ulEventType** corresponde à estrutura que está incluída na União **info** . O membro **ulEventType** pode ser definido como um dos seguintes valores: 
    
 _fnevCriticalError_
  
> Ocorreu um erro global, como uma sessão desligar em andamento. O membro **info** contém uma estrutura [ERROR_NOTIFICATION](error_notification.md) . 
    
 _fnevExtended_
  
> Ocorreu um evento interno definido por um provedor de serviço específico. O membro **info** contém uma estrutura [EXTENDED_NOTIFICATION](extended_notification.md) . 
    
 _fnevNewMail_
  
> Uma mensagem foi entregue ao receber a pasta para a classe de mensagem e está aguardando processamento apropriada. O membro **info** contém uma estrutura [NEWMAIL_NOTIFICATION](newmail_notification.md) . 
    
 _fnevObjectCopied_
  
> Um objeto MAPI foi copiado. O membro **info** contém uma estrutura [OBJECT_NOTIFICATION](object_notification.md) . 
    
 _fnevObjectCreated_
  
> Um objeto MAPI foi criado. O membro **info** contém uma estrutura **OBJECT_NOTIFICATION** . 
    
 _fnevObjectDeleted_
  
> Um objeto MAPI foi excluído. O membro **info** contém uma estrutura **OBJECT_NOTIFICATION** . 
    
 _fnevObjectModified_
  
> Um objeto MAPI foi alterado. O membro **info** contém uma estrutura **OBJECT_NOTIFICATION** . 
    
 _fnevObjectMoved_
  
> Um armazenamento de mensagens ou endereço livro objeto tiver sido movido. O membro **info** contém uma estrutura **OBJECT_NOTIFICATION** . 
    
 _fnevSearchComplete_
  
> Uma operação de pesquisa foi concluída e os resultados estarão disponíveis. O membro **info** contém uma estrutura **OBJECT_NOTIFICATION** . 
    
 _fnevTableModified_
  
> Informações em uma tabela foi alterada. O membro **info** contém uma estrutura [TABLE_NOTIFICATION](table_notification.md) . 
    
**Info**
  
> União de estruturas de notificação descrevendo os dados afetados para um determinado tipo de evento. A estrutura incluída no membro **info** depende do valor do membro **ulEventType** . 
    
## <a name="remarks"></a>Coment�rios

Uma ou mais estruturas de **notificação** são passadas como parâmetros de entrada com cada chamada ao método de [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) um advise registrados do receptor. As estruturas de **notificação** contêm informações sobre as determinados eventos ocorridos e descrevem os objetos afetados. 
  
Antes de clientes ou receber uma notificação de provedores de serviços podem usar a estrutura para processar o evento, eles devem verificar o tipo de evento, conforme indicado no membro **ulEventType** . Por exemplo, o exemplo de código que é mostrado aqui verifica a chegada de uma nova mensagem e ao detectar um evento desse tipo, imprime a classe de mensagem da mensagem. 
  
```cpp
if (pNotif -> ulEventType == fnevNewMail)
{
printf("%s\n", pNotif -> newmail.lpszMessageClass)
}

```

Para obter mais informações sobre a notificação, consulte os tópicos descritos na tabela a seguir.
  
|**Tópico**|**Descrição**|
|:-----|:-----|
|[Notificação de evento em MAPI](event-notification-in-mapi.md) <br/> |Visão geral de notificação e eventos de notificação.  <br/> |
|[Manipular notificações](handling-notifications.md) <br/> |Discussão sobre como os clientes devem manipular notificações.  <br/> |
|[Suporte de notificação de evento](supporting-event-notification.md) <br/> |Discussão sobre como provedores de serviços podem usar o método [IMAPISupport](imapisupportiunknown.md) para gerar notificações.  <br/> |
   
## <a name="see-also"></a>Confira também


- [ERROR_NOTIFICATION](error_notification.md)  
- [EXTENDED_NOTIFICATION](extended_notification.md)  
- [NEWMAIL_NOTIFICATION](newmail_notification.md)  
- [OBJECT_NOTIFICATION](object_notification.md)  
- [STATUS_OBJECT_NOTIFICATION](status_object_notification.md)  
- [TABLE_NOTIFICATION](table_notification.md)
- [Estruturas MAPI](mapi-structures.md)

