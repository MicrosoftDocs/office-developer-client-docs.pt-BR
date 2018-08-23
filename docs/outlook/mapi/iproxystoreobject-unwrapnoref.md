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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 8539f81ed1741063d878da492d925b63c488d1a9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586428"
---
# <a name="iproxystoreobjectunwrapnoref"></a>IProxyStoreObject::UnwrapNoRef

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Obtém um ponteiro para um objeto de repositório IMAP Internet Message Access Protocol () desfeita que fornece acesso para o arquivo de pastas particulares (. PST) subjacente sem sincronização de invocação e baixem os itens.
  
```cpp
HRESULT IProxyStoreObject::UnwrapNoRef (     LPVOID *ppvObject ); 
```

## <a name="parameters"></a>Parâmetros

 _ppvObject_
  
> [out] Ponteiro para uma [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) objeto store que será desfeito. 
    
## <a name="return-values"></a>Valores de retorno

S_OK
  
- A chamada foi bem-sucedida e um ponteiro para uma interface desfeita foi retornado no _ppvObject_.
    
## <a name="remarks"></a>Comentários

Sem primeiro desempacotamento um repositório IMAP, acessar uma mensagem no repositório de pode forçar uma sincronização que tenta fazer o download de toda a mensagem. Usando o repositório desfeito permite o acesso à mensagem em seu estado atual sem disparar um download.
  
Porque **UnwrapNoRef** não incrementa a contagem de referência para este novo ponteiro para o objeto de repositório desfeita, após chamar o **UnwrapNoRef**com êxito, você deve chamar [AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) para manter a contagem de referência. 
  
## <a name="see-also"></a>Confira também



[IProxyStoreObject](iproxystoreobject.md)

