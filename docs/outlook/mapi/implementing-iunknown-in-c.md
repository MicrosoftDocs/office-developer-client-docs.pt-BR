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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346771"
---
# <a name="implementing-iunknown-in-c"></a>Implementar interface IUnknown em C

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Implementações do [método IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) em C são muito semelhantes às implementações de C++. Há duas etapas básicas para a implementação: 
  
1. Validação de parâmetros.
    
2. Verificando o identificador da interface solicitada em relação à lista de interfaces suportadas pelo objeto e retornando o valor E_NO_INTERFACE ou um ponteiro de interface válido. Se um ponteiro da interface for retornado, a implementação também deverá chamar o método [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) para incrementar a contagem de referência. 
    
A principal diferença entre uma implementação de **QueryInterface** em C e C++ é o primeiro parâmetro adicional na versão C. Como o ponteiro do objeto é adicionado à lista de parâmetros, uma implementação em C de **QueryInterface** deve ter mais validação de parâmetro do que uma implementação C++. A lógica para verificar o identificador da interface, incrementar a contagem de referência e retornar um ponteiro de objeto deve ser idêntica em ambos os idiomas. 
  
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

Enquanto a implementação do método **AddRef** em C é semelhante a uma implementação de C++, uma implementação em C do método [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) pode ser mais elaborada do que uma versão C++. Isso porque grande parte da funcionalidade envolvida na liberação de um objeto pode ser incorporada ao construtor e destruidor C++, e C não tem esse mecanismo. Todas essas funcionalidades devem ser incluídas no método **Release.** Além disso, devido ao parâmetro adicional e à vtable explícita, é necessária mais validação. 
  
A chamada **do método AddRef** a seguir ilustra uma implementação típica de C para um objeto de status. 
  
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

O exemplo de código a seguir mostra uma implementação típica **de Release** para um objeto de status C. Se a contagem de referência for 0 após ser rebaixada, uma implementação de objeto de status C deverá executar as seguintes tarefas: 
  
- Libere ponteiros para objetos. 
    
- Definir a vtable como NULL, facilitando a depuração no caso em que o usuário de um objeto chamado **Release** ainda continua a tentar usar o objeto. 
    
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

- [Implementando objetos MAPI](implementing-mapi-objects.md)
- [Implementando a interface IUnknown](implementing-the-iunknown-interface.md)

