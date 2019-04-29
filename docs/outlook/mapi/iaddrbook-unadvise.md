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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 2988f1fc149bbfc2d724b62b12bd12ae4f4664a6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436150"
---
# <a name="iaddrbookunadvise"></a>IAddrBook::Unadvise

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cancela um registro de notificação estabelecido previamente para uma entrada do catálogo de endereços.
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>Parâmetros

 _ulConnection_
  
> no Um número de conexão que representa o registro a ser cancelado. O parâmetro _ulConnection_ deve conter um valor retornado por uma chamada anterior para o método [IAddrBook:: Advise](iaddrbook-advise.md) . 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O registro foi cancelado com êxito.
    
## <a name="remarks"></a>Comentários

Os clientes chamam o método **Unadvise** para parar de receber notificações sobre alterações em uma entrada de catálogo de endereços específica. Quando um registro de notificação é cancelado, o provedor de catálogo de endereços libera o ponteiro para o coletor de aviso do chamador. No enTanto, o lançamento pode ocorrer durante a chamada a **Unadvise** ou, posteriormente, se outro thread estiver no processo de chamar o método [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) . Quando uma notificação estiver em andamento, a versão será atrasada até o **** método OnNotify retornar. 
  
## <a name="see-also"></a>Confira também



[IAddrBook::Advise](iaddrbook-advise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

