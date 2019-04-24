---
title: IAddrBookAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.Advise
api_type:
- COM
ms.assetid: 2def89ed-e4ce-446a-8b80-132d11ae8f8b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7abafafd3d4bd9618d85a7dac34e4556545167bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334752"
---
# <a name="iaddrbookadvise"></a>IAddrBook::Advise

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Registra um cliente ou provedor de serviços para receber notificações sobre alterações em uma ou mais entradas no catálogo de endereços.
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a>Parâmetros

 _cbEntryID_
  
> no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
> no Um ponteiro para o identificador de entrada do contêiner de catálogo de endereços, usuário de mensagens ou lista de distribuição que gerará uma notificação quando uma alteração ocorrer do tipo ou tipos descritos no parâmetro _ulEventMask_ . 
    
 _ulEventMask_
  
> no Um ou mais eventos de notificação que o chamador está registrando para receber. Cada evento é associado a uma estrutura de notificação específica que contém informações sobre a alteração que ocorreu. A tabela a seguir lista os valores válidos para _ulEventMask_ e suas estruturas correspondentes. 
    
|**Evento de notificação**|**Estrutura correspondente**|
|:-----|:-----|
|**fnevCriticalError** <br/> |[ERROR_NOTIFICATION](error_notification.md) <br/> |
|**fnevObjectCreated** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectDeleted** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectModified** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectCopied** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectMoved** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevTableModified** <br/> |[TABLE_NOTIFICATION](table_notification.md) <br/> |
   
 _lpAdviseSink_
  
> no Um ponteiro para o objeto do coletor de aviso a ser chamado quando o evento para o qual a notificação foi solicitada ocorre.
    
 _lpulConnection_
  
> bota Um ponteiro para um número de conexão diferente de zero que representa o registro de notificação.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O registro de notificação foi bem-sucedido.
    
MAPI_E_INVALID_ENTRYID 
  
> O provedor de catálogo de endereços responsável pelo identificador de entrada passado no _lpEntryID_ não pôde registrar uma notificação para a entrada correspondente. 
    
MAPI_E_NO_SUPPORT 
  
> A notificação não é suportada pelo provedor de catálogo de endereços responsável pelo objeto identificado pelo identificador de entrada passado no parâmetro _lpEntryID_ . 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> O identificador de entrada passado no _lpEntryID_ não pode ser manipulado por nenhum dos provedores de catálogo de endereços no perfil. 
    
## <a name="remarks"></a>Comentários

Os clientes e os provedores de serviços chamam o método **Advise** para registrar um tipo específico ou tipos de notificação em uma entrada de catálogo de endereços. Os tipos de notificação são indicados pela máscara de evento passada com o parâmetro _ulEventMask_ . 
  
O MAPI encaminha essa **** chamada para o provedor de catálogo de endereços responsável pela entrada, conforme indicado pelo identificador de entrada no parâmetro _lpEntryID_ . O provedor do catálogo de endereços trata o registro em si ou chama o método de suporte, [IMAPISupport:: Subscribe](imapisupport-subscribe.md), para solicitar MAPI para registrar o chamador. Um número de conexão diferente de zero é retornado para representar o registro bem-sucedido.
  
Sempre que uma alteração ocorre na entrada do tipo indicado pelo registro de notificação, o provedor de catálogo de endereços chama o método [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) para o objeto de coletor de aviso especificado no parâmetro _lpAdviseSink_ . O **** método OnNotify inclui uma estrutura de [notificação](notification.md) como um parâmetro de entrada que contém dados para descrever o evento. 
  
Dependendo do provedor de catálogo de endereços, a chamada para **OnNotify** pode ocorrer imediatamente após a alteração para o objeto registrado ou em um momento posterior. Em sistemas que oferecem suporte a vários threads de execução, **** a chamada para OnNotify pode ocorrer em qualquer thread. Os clientes podem solicitar que essas notificações ocorram em um thread específico chamando a função [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) para criar o objeto de coletor de aviso que é passado para **Advise**. 
  
Como um provedor de catálogo de endereços pode liberar o objeto de coletor de aviso aprovado por clientes a qualquer momento após a conclusão bem-sucedida da chamada de **aviso** e antes de uma chamada a [IAddrBook:: Unadvise](iaddrbook-unadvise.md) para cancelar a notificação, os clientes devem liberar seus objetos de coletor de aviso quando **Advise** retorna. 
  
Para obter mais informações sobre o processo de notificação, consulte [Event Notification in MAPI](event-notification-in-mapi.md).
  
## <a name="see-also"></a>Confira também



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IAddrBook::Unadvise](iaddrbook-unadvise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[NOTIFICATION](notification.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

