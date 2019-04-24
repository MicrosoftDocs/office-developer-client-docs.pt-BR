---
title: IProxyStoreObjectUnwrapNoRef
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProxyStoreObject.UnwrapNoRef
api_type:
- COM
ms.assetid: 1122b6e0-e7e1-e68a-e090-435777343d04
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: ef9f506c1a95fec86c7f092b0299198e6149d3ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320150"
---
# <a name="iproxystoreobjectunwrapnoref"></a>IProxyStoreObject::UnwrapNoRef

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Obtém um ponteiro para um objeto de armazenamento IMAP (Internet Message Access Protocol) que fornece acesso ao arquivo de pastas particulares (PST) subjacente sem chamar a sincronização e baixar os itens.
  
```cpp
HRESULT IProxyStoreObject::UnwrapNoRef (     LPVOID *ppvObject ); 
```

## <a name="parameters"></a>Parâmetros

 _ppvObject_
  
> bota Ponteiro para um objeto de repositório [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) que está desempacotado. 
    
## <a name="return-values"></a>Valor de retorno

S_OK
  
- A chamada foi bem-sucedida e um ponteiro para uma interface não Wrapped foi retornado no _ppvObject_.
    
## <a name="remarks"></a>Comentários

Sem antes desenvolver um repositório IMAP, acessar uma mensagem no repositório pode forçar uma sincronização que tenta baixar toda a mensagem. O uso do repositório desempacotado permite o acesso à mensagem em seu estado atual sem disparar um download.
  
Como o **UnwrapNoRef** não incrementa a contagem de referência desse novo ponteiro para o objeto de repositório não empacotado, após chamar **UnwrapNoRef**com êxito, você deve chamar [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) para manter a contagem de referência. 
  
## <a name="see-also"></a>Confira também



[IProxyStoreObject](iproxystoreobject.md)

