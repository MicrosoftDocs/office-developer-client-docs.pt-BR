---
title: Acessar uma mensagem em um repositório IMAP sem fazer o download de toda a mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2a93ab3e-798f-5741-d5e0-bba8c6b437c7
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 5a5a327ff74a4058d8eb15928912ca075e55ea95
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564385"
---
# <a name="access-a-message-on-an-imap-store-without-downloading-the-entire-message"></a>Acessar uma mensagem em um repositório IMAP sem fazer o download de toda a mensagem

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
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


