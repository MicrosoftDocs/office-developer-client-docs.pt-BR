---
title: Implementar interface IUnknown em C++
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 68519f6c-fba8-47f5-9401-316e276f770e
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 08f3f3f937320d8a986b2002c761a37f0f749227
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330174"
---
# <a name="implementing-iunknown-in-c"></a><span data-ttu-id="d2e04-103">Implementar interface IUnknown em C++</span><span class="sxs-lookup"><span data-stu-id="d2e04-103">Implementing IUnknown in C++</span></span>

<span data-ttu-id="d2e04-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d2e04-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d2e04-105">Implementar os métodos [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx), [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)e [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) da interface [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) em C++ é bastante simples.</span><span class="sxs-lookup"><span data-stu-id="d2e04-105">Implementing the [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx), [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx), and [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) methods of the [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) interface in C++ is fairly simple.</span></span> <span data-ttu-id="d2e04-106">Após alguma validação padrão dos parâmetros que são passados, uma implementação de **QueryInterface** verifica o identificador da interface solicitada em relação à lista de interfaces com suporte.</span><span class="sxs-lookup"><span data-stu-id="d2e04-106">After some standard validation of the parameters that are passed in, an implementation of **QueryInterface** checks the identifier of the requested interface against the list of supported interfaces.</span></span> <span data-ttu-id="d2e04-107">Se o identificador solicitado estiver entre os suportados, **AddRef** será chamado e o **ponteiro** será retornado.</span><span class="sxs-lookup"><span data-stu-id="d2e04-107">If the requested identifier is among those supported, **AddRef** is called and the **this** pointer is returned.</span></span> <span data-ttu-id="d2e04-108">Se o identificador solicitado não estiver na lista com suporte, o ponteiro de saída será definido como NULL e o MAPI_E_INTERFACE_NOT_SUPPORTED valor será retornado.</span><span class="sxs-lookup"><span data-stu-id="d2e04-108">If the requested identifier is not on the supported list, the output pointer is set to NULL and the MAPI_E_INTERFACE_NOT_SUPPORTED value is returned.</span></span> 
  
<span data-ttu-id="d2e04-109">O exemplo de código a seguir mostra como você pode implementar **QueryInterface** em C++ para um objeto de status, um objeto que é uma subclasse da interface [IMAPIStatus : IMAPIProp.](imapistatusimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="d2e04-109">The following code example shows how you can implement **QueryInterface** in C++ for a status object, an object that is a subclass of the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="d2e04-110">**IMAPIStatus** herda de **IUnknown** através [de IMAPIProp : IUnknown](imapipropiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="d2e04-110">**IMAPIStatus** inherits from **IUnknown** through [IMAPIProp : IUnknown](imapipropiunknown.md).</span></span> <span data-ttu-id="d2e04-111">Portanto, se um chamador solicita qualquer uma  dessas interfaces, o ponteiro pode ser retornado porque as interfaces estão relacionadas por herança.</span><span class="sxs-lookup"><span data-stu-id="d2e04-111">Therefore, if a caller asks for any of these interfaces, the **this** pointer can be returned because the interfaces are related through inheritance.</span></span> 
  
```cpp
HRESULT CMyMAPIObject::QueryInterface (REFIID   riid,
                                       LPVOID * ppvObj)
{
    // Always set out parameter to NULL, validating it first.
    if (!ppvObj)
        return E_INVALIDARG;
    *ppvObj = NULL;
    if (riid == IID_IUnknown || riid == IID_IMAPIProp ||
        riid == IID_IMAPIStatus)
    {
        // Increment the reference count and return the pointer.
        *ppvObj = (LPVOID)this;
        AddRef();
        return NOERROR;
    }
    return E_NOINTERFACE;
}

```

<span data-ttu-id="d2e04-112">O exemplo de código a seguir mostra como implementar os **métodos AddRef** e **Release** para o  `CMyMAPIObject` objeto.</span><span class="sxs-lookup"><span data-stu-id="d2e04-112">The following code example shows how to implement the **AddRef** and **Release** methods for the  `CMyMAPIObject` object.</span></span> <span data-ttu-id="d2e04-113">Como implementar **AddRef** e **Release** é simples, muitos provedores de serviços optam por implementá-los em linha.</span><span class="sxs-lookup"><span data-stu-id="d2e04-113">Because implementing **AddRef** and **Release** is straightforward, many service providers choose to implement them inline.</span></span> <span data-ttu-id="d2e04-114">As chamadas para as funções Win32 **InterlockedIncrement** e **InterlockedDecrement** garantem a segurança do thread.</span><span class="sxs-lookup"><span data-stu-id="d2e04-114">The calls to the Win32 functions **InterlockedIncrement** and **InterlockedDecrement** ensure thread safety.</span></span> <span data-ttu-id="d2e04-115">A memória para o objeto é liberada pelo destruidor, que é chamado quando o **método Release** exclui o objeto.</span><span class="sxs-lookup"><span data-stu-id="d2e04-115">The memory for the object is freed by the destructor, which is called when the **Release** method deletes the object.</span></span> 
  
```cpp
ULONG CMyMAPIObject::AddRef()
{
    InterlockedIncrement(m_cRef);
    return m_cRef;
}
ULONG CMyMAPIObject::Release()
{
    // Decrement the object's internal counter.
    ULONG ulRefCount = InterlockedDecrement(m_cRef);
    if (0 == m_cRef)
    {
        delete this;
    }
    return ulRefCount;
}
 
```

## <a name="see-also"></a><span data-ttu-id="d2e04-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="d2e04-116">See also</span></span>

- [<span data-ttu-id="d2e04-117">Implementando objetos MAPI</span><span class="sxs-lookup"><span data-stu-id="d2e04-117">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)
- [<span data-ttu-id="d2e04-118">Implementando a interface IUnknown</span><span class="sxs-lookup"><span data-stu-id="d2e04-118">Implementing the IUnknown Interface</span></span>](implementing-the-iunknown-interface.md)

