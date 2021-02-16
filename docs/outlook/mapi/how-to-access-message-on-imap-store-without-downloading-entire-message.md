---
title: Acessar uma mensagem em um repositório IMAP sem baixar a mensagem completa
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2a93ab3e-798f-5741-d5e0-bba8c6b437c7
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 194131148cc36dfff791b4cfae01862e8bbef5cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299073"
---
# <a name="access-a-message-on-an-imap-store-without-downloading-the-entire-message"></a>Acessar uma mensagem em um repositório IMAP sem baixar a mensagem completa

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Este tópico mostra um exemplo de código em C++ que consulta um repositório de mensagens para a interface **[IProxyStoreObject](iproxystoreobject.md)** e usa o ponteiro retornado e a função **[IProxyStoreObject::UnwrapNoRef](iproxystoreobject-unwrapnoref.md)** para obter um ponteiro para um objeto de repositório IMAP que não foi mapeado. O uso desse armazenamento não mapeado permite o acesso a uma mensagem em seu estado atual sem invocar um download da mensagem inteira. 
  
Como **UnwrapNoRef** não incrementa a contagem de referência desse novo ponteiro para o objeto de armazenamento não mapeado, depois de chamar **UnwrapNoRef** com êxito, você deve chamar [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) para manter a contagem de referência. 
  
```cpp
HRESULT HrUnWrapMDB(LPMDB lpMDBIn, LPMDB* lppMDBOut) 
{ 
    HRESULT hRes = S_OK; 
    IProxyStoreObject* lpProxyObj = NULL; 
    LPMDB lpUnwrappedMDB = NULL; 
    hRes = lpMDBIn->QueryInterface(IID_IProxyStoreObject,(void**)&lpProxyObj); 
    if (SUCCEEDED(hRes) && lpProxyObj) 
    { 
        hRes = lpProxyObj->UnwrapNoRef((LPVOID*)&lpUnwrappedMDB); 
        if (SUCCEEDED(hRes) && lpUnwrappedMDB) 
        { 
            // UnwrapNoRef doesn't addref, so do it here 
            lpUnwrappedMDB->AddRef(); 
            (*lppMDBOut) = lpUnwrappedMDB; 
        } 
    } 
    if (lpProxyObj) lpProxyObj->Release(); 
    return hRes; 
}
```


