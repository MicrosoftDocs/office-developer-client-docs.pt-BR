---
title: Acessar uma mensagem em um repositório IMAP sem fazer o download de toda a mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2a93ab3e-798f-5741-d5e0-bba8c6b437c7
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: fa7a61da47169ca7c6a1521ad5b3e84685a9b9a3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766730"
---
# <a name="access-a-message-on-an-imap-store-without-downloading-the-entire-message"></a>Acessar uma mensagem em um repositório IMAP sem fazer o download de toda a mensagem

**Aplica-se a**: Outlook 
  
Este tópico mostra um exemplo de código em C++ que consultas a um armazenamento de mensagens para a interface **[IProxyStoreObject](iproxystoreobject.md)** e usa o ponteiro retornado e a função **[IProxyStoreObject::UnwrapNoRef](iproxystoreobject-unwrapnoref.md)** para obter um ponteiro para um objeto de repositório IMAP que tenha sido desfeita. Usando esse repositório desfeito permite o acesso a uma mensagem em seu estado atual sem chamar um download de toda a mensagem. 
  
Porque **UnwrapNoRef** não incrementa a contagem de referência para este novo ponteiro para o objeto de repositório desfeita, após chamar o **UnwrapNoRef**com êxito, você deve chamar [AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) para manter a contagem de referência. 
  
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


