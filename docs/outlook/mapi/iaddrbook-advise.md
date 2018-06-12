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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 8214390af883432d72f608452b8b944417884fd2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766866"
---
# <a name="iaddrbookadvise"></a>IAddrBook::Advise

  
  
**Aplica-se a**: Outlook 
  
Registra um provedor de serviço ou cliente para receber notificações sobre alterações em uma ou mais entradas no catálogo de endereços.
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a>Par�metros

 _cbEntryID_
  
> [in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Um ponteiro para o identificador de entrada do recipiente de catálogo de endereços, usuário ou lista de distribuição que irá gerar uma notificação quando ocorre uma alteração do tipo ou tipos descritos no parâmetro _ulEventMask_ de mensagens. 
    
 _ulEventMask_
  
> [in] Um ou mais eventos de notificação que o chamador está registrando para receber. Cada evento é associado uma estrutura de notificação em particular que contém informações sobre a alteração que ocorreu. A tabela a seguir lista os valores válidos para _ulEventMask_ e suas estruturas correspondentes. 
    
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
  
> [in] Um ponteiro para o objeto coletor de eventos de advise a ser chamado quando ocorre o evento para o qual a notificação tiver sido solicitada.
    
 _lpulConnection_
  
> [out] Um ponteiro para um número diferente de zero de conexão que representa o registro de notificação.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O registro de notificação foi bem-sucedida.
    
MAPI_E_INVALID_ENTRYID 
  
> O provedor de catálogo de endereços para o identificador de entrada passado _lpEntryID_ responsável não pôde registrar uma notificação para a entrada correspondente. 
    
MAPI_E_NO_SUPPORT 
  
> Notificação não é suportada pelo provedor de catálogo de endereços responsável pelo objeto identificado pelo identificador de entrada passado no parâmetro _lpEntryID_ . 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> O identificador de entrada passado _lpEntryID_ não pode ser manipulado por qualquer um dos provedores de catálogo de endereços no perfil. 
    
## <a name="remarks"></a>Coment�rios

Provedores de serviços e clientes chame o método de **Advise** para se registrar em um determinado tipo ou tipos de notificação em uma entrada do catálogo de endereços. Os tipos de notificação são indicados pela máscara de evento passada com o parâmetro _ulEventMask_ . 
  
MAPI encaminha essa chamada **Advise** para o provedor de catálogo de endereços que é responsável pela entrada, conforme indicado pelo identificador de entrada no parâmetro _lpEntryID_ . O provedor de catálogo de endereços manipula o registro em si ou chama o método de suporte, [IMAPISupport::Subscribe](imapisupport-subscribe.md), para solicitar o MAPI para registrar o chamador. Um número diferente de zero conexão é retornado para representar o registro com êxito.
  
Sempre que ocorre uma alteração para a entrada do tipo indicado pelo registro notificação, o provedor de catálogo de endereços chama o método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) para o objeto coletor de eventos de advise especificado no parâmetro _lpAdviseSink_ . O método **OnNotify** inclui uma estrutura de [notificação](notification.md) como um parâmetro de entrada que contém dados para descrever o evento. 
  
Dependendo do provedor de catálogo de endereços, a chamada para **OnNotify** pode ocorrer imediatamente após a alteração no objeto registrados ou mais tarde. Nos sistemas que oferecem suporte a vários threads de execução, a chamada para **OnNotify** pode ocorrer em qualquer segmento. Os clientes podem requisitar que essas notificações ocorrerem em um determinado thread chamando a função [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) para criar o objeto de coletor de eventos de advise é passado para **Advise**. 
  
Porque um fornecedor de catálogo de endereços pode liberar o objeto coletor de eventos de advise passado pelos clientes a qualquer momento após a conclusão bem-sucedida do **Advise** e um [IAddrBook::Unadvise](iaddrbook-unadvise.md) antes de chamar para cancelar a notificação, clientes devem liberar seus objetos de coletor advise quando **Advise** retorna. 
  
Para obter mais informações sobre o processo de notificação, consulte [Notificação de evento em MAPI](event-notification-in-mapi.md).
  
## <a name="see-also"></a>Confira também



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IAddrBook::Unadvise](iaddrbook-unadvise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[NOTIFICAÇÃO](notification.md)
  
[IAddrBook: IMAPIProp](iaddrbookimapiprop.md)

