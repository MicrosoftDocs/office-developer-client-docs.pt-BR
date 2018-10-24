---
title: Implementar interface IUnknown em C
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 807b6dc4-cdb7-40a4-87d7-ebc1ad5fab76
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 3c634defcad76755fc6604a23d2091bb21e15111
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391441"
---
# <a name="implementing-iunknown-in-c"></a>Implementar interface IUnknown em C

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Implementações do método [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) na C serão bastante similares às implementações de C++. Há duas etapas básicas para a implementação: 
  
1. Validando parâmetros.
    
2. O identificador da interface solicitada em relação à lista de interfaces suportadas pelo objeto de verificação e retornar o valor E_NO_INTERFACE ou um ponteiro de interface válido. Se um ponteiro de interface for retornado, a implementação também deve chamar o método [AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) para incrementar a contagem de referência. 
    
A principal diferença entre uma implementação de **QueryInterface** em C e C++ é o primeiro parâmetro adicional na versão C. Como o ponteiro de objeto é adicionado à lista de parâmetros, uma implementação do C de **QueryInterface** deve ter mais de validação de parâmetro que uma implementação do C++. A lógica para o identificador de interface de verificação, incrementar a contagem de referência e retornando um ponteiro de objeto deve ser idêntica em ambos os idiomas. 
  
O exemplo de código a seguir mostra como implementar **QueryInterface** em C para um objeto de status. 
  
```cpp
STDMETHODIMP STATUS_QueryInterface(LPMYSTATUSOBJ lpMyObj, REFIID riid,
                                   LPVOID FAR * lppvObj)
{
    HRESULT hr = hrSuccess;
    // Validate the object pointer.
    if (!lpMyObj || lpMyObj->lpVtbl != &vtblSTATUS )
    {
        hr = ResultFromScode(E_INVALIDARG);
        return hr;
    }
    // Validate other parameters.
    if (!lppvObj)
    {
        hr = ResultFromScode(E_INVALIDARG);
        return hr;
    }
    // Set the output pointer to NULL.
    *lppvObj = NULL;
    // Check the interface identifier.
    if (memcmp(riid, &IID_IUnknown, sizeof(IID)) &&
        memcmp(riid, &IID_IMAPIProp, sizeof(IID)) &&
        memcmp(riid, &IID_IMAPIStatus, sizeof(IID)))
    {
        hr = ResultFromScode(E_NOINTERFACE);
        return hr;
    }
    // The interface is supported. Increment the reference count and return.
    lpMyObj->lpVtbl->AddRef(lpMyObj);
    *lppvObj = lpMyObj;
    return hr;
}

```

Enquanto a implementação do método **AddRef** em C é semelhante a uma implementação do C++, uma implementação do C do método [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) pode obter mais elaborada do que uma versão do C++. Isso ocorre porque muitas das funcionalidades envolvidas com dispensando a um objeto pode ser incorporada no construtor de C++ e destrutor e C tem esse mecanismo não. Toda essa funcionalidade deve ser incluída no método **Release** . Além disso, devido ao parâmetro adicional e seu vtable explícita, mais de validação é necessária. 
  
A chamada de método **AddRef** a seguir ilustra uma implementação C típica para um objeto de status. 
  
```cpp
STDMETHODIMP_(ULONG) STATUS_AddRef(LPMYSTATUSOBJ lpMyObj)
{
    LONG cRef;
    // Check to see whether it has a lpVtbl object member.
    if (!lpMyObj || lpMyObj->lpVtbl != &vtblSTATUS)
    {
        return 1;
    }
    // Check the method.
    if (STATUS_AddRef != lpMyObj->lpVtbl->AddRef)
    {
        return 1;
    }
    InterlockedIncrement(lpMyObj->cRef);
    cRef = ++lpMyObj->cRef;
    InterlockedDecrement (lpMyObj->cRef);
    return cRef;
}

```

O exemplo de código a seguir mostra uma implementação típica da **versão** de um objeto de status C. Se a contagem de referência for 0, depois que ele é diminuído, uma implementação do objeto de status C deve executar as seguintes tarefas: 
  
- Libere qualquer mantidos ponteiros para objetos. 
    
- Defina o vtable como NULL, facilitando a depuração no caso onde usuário de um objeto chamado **lançamento** ainda continuação tentar usar o objeto. 
    
- Chame **MAPIFreeBuffer** para liberar o objeto. 
    
```cpp
STDMETHODIMP_(ULONG) STATUS_Release(LPMYSTATUSOBJ lpMyObj)
{
    LONG cRef;
    // Check the size of the vtable.
    if (!lpMyObj)
    {
        return 1;
    }
    // Check whether the vtable is correct.
    if (lpMyObj->lpVtbl != &vtblSTATUS)
    {
        return 1;
    }
    InterlockedIncrement(lpMyObj->cRef);
    cRef = --lpMyObj->cRef;
    InterlockedIncrement (lpMyObj->cRef);
    if (cRef == 0)
    {
        lpMyObj->lpVtbl->Release(lpMyObj);
        DeleteCriticalSection(&lpMyObj->cs);
        // Release the IMAPIProp pointer.
        lpMyObj->lpProp->Release(lpMyObj->lpProp);
        lpMyObj->lpVtbl = NULL;
        lpMyObj->lpFreeBuff(lpMyObj);
        return 0;
    }
    return cRef;
}

```

## <a name="see-also"></a>Confira também

- [Implementar objetos de MAPI](implementing-mapi-objects.md)
- [Implementando a Interface IUnknown](implementing-the-iunknown-interface.md)

