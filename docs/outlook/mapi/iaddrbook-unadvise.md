---
title: IAddrBookUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.Unadvise
api_type:
- COM
ms.assetid: e0db9e86-9528-43de-b8ba-a5af8b7bda4b
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: bf72e6f182f67861f909e21f0ec1871d76617974
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19766891"
---
# <a name="iaddrbookunadvise"></a>IAddrBook::Unadvise

  
  
**Aplica-se a**: Outlook 
  
Cancela um registro de notificação que tenha estabelecido para uma entrada do catálogo de endereços.
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>Par�metros

 _ulConnection_
  
> [in] Um número de conexão que representa o registro a ser cancelada. O parâmetro _ulConnection_ deve conter um valor retornado por uma chamada anterior para o método [IAddrBook::Advise](iaddrbook-advise.md) . 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O registro foi cancelado com êxito.
    
## <a name="remarks"></a>Coment�rios

Clientes chame o método de **Unadvise** para parar de receber notificações sobre alterações em uma entrada de catálogo de endereço específica. Quando um registro de notificação for cancelado, as versões de provedor de catálogo de endereços seu ponteiro para o chamador do coletor de eventos de aviso. No entanto, a versão pode ocorrer durante a chamada **Unadvise** ou em algum momento posterior, se outro thread no processo de chamar o método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) . Quando uma notificação estiver em andamento, a versão foi adiada até que o método **OnNotify** retorna. 
  
## <a name="see-also"></a>Confira também



[IAddrBook::Advise](iaddrbook-advise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IAddrBook: IMAPIProp](iaddrbookimapiprop.md)

