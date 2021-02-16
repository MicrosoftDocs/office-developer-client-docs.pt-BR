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
# <a name="implementing-iunknown-in-c"></a><span data-ttu-id="4c123-103">Implementar interface IUnknown em C</span><span class="sxs-lookup"><span data-stu-id="4c123-103">Implementing IUnknown in C</span></span>

<span data-ttu-id="4c123-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4c123-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4c123-105">Implementações do [método IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) em C são muito semelhantes às implementações de C++.</span><span class="sxs-lookup"><span data-stu-id="4c123-105">Implementations of the [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) method in C are very similar to C++ implementations.</span></span> <span data-ttu-id="4c123-106">Há duas etapas básicas para a implementação:</span><span class="sxs-lookup"><span data-stu-id="4c123-106">There are two basic steps to the implementation:</span></span> 
  
1. <span data-ttu-id="4c123-107">Validação de parâmetros.</span><span class="sxs-lookup"><span data-stu-id="4c123-107">Validating parameters.</span></span>
    
2. <span data-ttu-id="4c123-108">Verificando o identificador da interface solicitada em relação à lista de interfaces suportadas pelo objeto e retornando o valor E_NO_INTERFACE ou um ponteiro de interface válido.</span><span class="sxs-lookup"><span data-stu-id="4c123-108">Checking the identifier of the requested interface against the list of interfaces supported by the object and returning either the E_NO_INTERFACE value or a valid interface pointer.</span></span> <span data-ttu-id="4c123-109">Se um ponteiro da interface for retornado, a implementação também deverá chamar o método [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) para incrementar a contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="4c123-109">If an interface pointer is returned, the implementation should also call the [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method to increment the reference count.</span></span> 
    
<span data-ttu-id="4c123-110">A principal diferença entre uma implementação de **QueryInterface** em C e C++ é o primeiro parâmetro adicional na versão C.</span><span class="sxs-lookup"><span data-stu-id="4c123-110">The main difference between an implementation of **QueryInterface** in C and C++ is the additional first parameter in the C version.</span></span> <span data-ttu-id="4c123-111">Como o ponteiro do objeto é adicionado à lista de parâmetros, uma implementação em C de **QueryInterface** deve ter mais validação de parâmetro do que uma implementação C++.</span><span class="sxs-lookup"><span data-stu-id="4c123-111">Because the object pointer is added to the parameter list, a C implementation of **QueryInterface** must have more parameter validation than a C++ implementation.</span></span> <span data-ttu-id="4c123-112">A lógica para verificar o identificador da interface, incrementar a contagem de referência e retornar um ponteiro de objeto deve ser idêntica em ambos os idiomas.</span><span class="sxs-lookup"><span data-stu-id="4c123-112">The logic for checking the interface identifier, incrementing the reference count, and returning an object pointer should be identical in both languages.</span></span> 
  
<span data-ttu-id="4c123-113">O exemplo de código a seguir mostra como implementar **QueryInterface** em C para um objeto de status.</span><span class="sxs-lookup"><span data-stu-id="4c123-113">The following code example shows how to implement **QueryInterface** in C for a status object.</span></span> 
  
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

<span data-ttu-id="4c123-114">Enquanto a implementação do método **AddRef** em C é semelhante a uma implementação de C++, uma implementação em C do método [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) pode ser mais elaborada do que uma versão C++.</span><span class="sxs-lookup"><span data-stu-id="4c123-114">Whereas the implementation of the **AddRef** method in C is similar to a C++ implementation, a C implementation of the [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method can get more elaborate than a C++ version.</span></span> <span data-ttu-id="4c123-115">Isso porque grande parte da funcionalidade envolvida na liberação de um objeto pode ser incorporada ao construtor e destruidor C++, e C não tem esse mecanismo.</span><span class="sxs-lookup"><span data-stu-id="4c123-115">This is because much of the functionality involved with freeing an object can be incorporated into the C++ constructor and destructor, and C has no such mechanism.</span></span> <span data-ttu-id="4c123-116">Todas essas funcionalidades devem ser incluídas no método **Release.**</span><span class="sxs-lookup"><span data-stu-id="4c123-116">All of this functionality must be included in the **Release** method.</span></span> <span data-ttu-id="4c123-117">Além disso, devido ao parâmetro adicional e à vtable explícita, é necessária mais validação.</span><span class="sxs-lookup"><span data-stu-id="4c123-117">Also, because of the additional parameter and its explicit vtable, more validation is required.</span></span> 
  
<span data-ttu-id="4c123-118">A chamada **do método AddRef** a seguir ilustra uma implementação típica de C para um objeto de status.</span><span class="sxs-lookup"><span data-stu-id="4c123-118">The following **AddRef** method call illustrates a typical C implementation for a status object.</span></span> 
  
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

<span data-ttu-id="4c123-119">O exemplo de código a seguir mostra uma implementação típica **de Release** para um objeto de status C.</span><span class="sxs-lookup"><span data-stu-id="4c123-119">The following code example shows a typical implementation of **Release** for a C status object.</span></span> <span data-ttu-id="4c123-120">Se a contagem de referência for 0 após ser rebaixada, uma implementação de objeto de status C deverá executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="4c123-120">If the reference count is 0 after it is decremented, a C status object implementation should perform the following tasks:</span></span> 
  
- <span data-ttu-id="4c123-121">Libere ponteiros para objetos.</span><span class="sxs-lookup"><span data-stu-id="4c123-121">Release any held pointers to objects.</span></span> 
    
- <span data-ttu-id="4c123-122">Definir a vtable como NULL, facilitando a depuração no caso em que o usuário de um objeto chamado **Release** ainda continua a tentar usar o objeto.</span><span class="sxs-lookup"><span data-stu-id="4c123-122">Set the vtable to NULL, facilitating debugging in the case where an object's user called **Release** yet continued to try to use the object.</span></span> 
    
- <span data-ttu-id="4c123-123">Chame **MAPIFreeBuffer** para liberar o objeto.</span><span class="sxs-lookup"><span data-stu-id="4c123-123">Call **MAPIFreeBuffer** to free the object.</span></span> 
    
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

## <a name="see-also"></a><span data-ttu-id="4c123-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c123-124">See also</span></span>

- [<span data-ttu-id="4c123-125">Implementando objetos MAPI</span><span class="sxs-lookup"><span data-stu-id="4c123-125">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)
- [<span data-ttu-id="4c123-126">Implementando a interface IUnknown</span><span class="sxs-lookup"><span data-stu-id="4c123-126">Implementing the IUnknown Interface</span></span>](implementing-the-iunknown-interface.md)

