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
# <a name="access-a-message-on-an-imap-store-without-downloading-the-entire-message"></a><span data-ttu-id="e412d-103">Acessar uma mensagem em um repositório IMAP sem baixar a mensagem completa</span><span class="sxs-lookup"><span data-stu-id="e412d-103">Access a message on an IMAP store without downloading the entire message</span></span>

<span data-ttu-id="e412d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e412d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e412d-105">Este tópico mostra um exemplo de código em C++ que consulta um repositório de mensagens para a interface **[IProxyStoreObject](iproxystoreobject.md)** e usa o ponteiro retornado e a função **[IProxyStoreObject::UnwrapNoRef](iproxystoreobject-unwrapnoref.md)** para obter um ponteiro para um objeto de repositório IMAP que não foi mapeado.</span><span class="sxs-lookup"><span data-stu-id="e412d-105">This topic shows a code sample in C++ that queries a message store for the **[IProxyStoreObject](iproxystoreobject.md)** interface, and uses the returned pointer and the **[IProxyStoreObject::UnwrapNoRef](iproxystoreobject-unwrapnoref.md)** function to obtain a pointer to an IMAP store object that has been unwrapped.</span></span> <span data-ttu-id="e412d-106">O uso desse armazenamento não mapeado permite o acesso a uma mensagem em seu estado atual sem invocar um download da mensagem inteira.</span><span class="sxs-lookup"><span data-stu-id="e412d-106">Using this unwrapped store allows access to a message in its current state without invoking a download of the entire message.</span></span> 
  
<span data-ttu-id="e412d-107">Como **UnwrapNoRef** não incrementa a contagem de referência desse novo ponteiro para o objeto de armazenamento não mapeado, depois de chamar **UnwrapNoRef** com êxito, você deve chamar [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) para manter a contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="e412d-107">Because **UnwrapNoRef** does not increment the reference count for this new pointer to the unwrapped store object, after successfully calling **UnwrapNoRef**, you must call [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) to maintain the reference count.</span></span> 
  
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


