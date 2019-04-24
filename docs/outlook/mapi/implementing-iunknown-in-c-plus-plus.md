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
# <a name="implementing-iunknown-in-c"></a><span data-ttu-id="24c03-103">Implementar interface IUnknown em C++</span><span class="sxs-lookup"><span data-stu-id="24c03-103">Implementing IUnknown in C++</span></span>

<span data-ttu-id="24c03-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="24c03-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="24c03-105">A implementação dos métodos [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx), [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)e [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) da interface [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) no C++ é muito simples.</span><span class="sxs-lookup"><span data-stu-id="24c03-105">Implementing the [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx), [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx), and [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) methods of the [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) interface in C++ is fairly simple.</span></span> <span data-ttu-id="24c03-106">Após algumas validações padrão dos parâmetros passados, uma implementação de **QueryInterface** verifica o identificador da interface solicitada em relação à lista de interfaces suportadas.</span><span class="sxs-lookup"><span data-stu-id="24c03-106">After some standard validation of the parameters that are passed in, an implementation of **QueryInterface** checks the identifier of the requested interface against the list of supported interfaces.</span></span> <span data-ttu-id="24c03-107">Se o identificador solicitado estiver entre eles com suporte, **AddRef** será chamado e \*\*\*\* o ponteiro será retornado.</span><span class="sxs-lookup"><span data-stu-id="24c03-107">If the requested identifier is among those supported, **AddRef** is called and the **this** pointer is returned.</span></span> <span data-ttu-id="24c03-108">Se o identificador solicitado não estiver na lista com suporte, o ponteiro de saída será definido como nulo e o valor MAPI_E_INTERFACE_NOT_SUPPORTED será retornado.</span><span class="sxs-lookup"><span data-stu-id="24c03-108">If the requested identifier is not on the supported list, the output pointer is set to NULL and the MAPI_E_INTERFACE_NOT_SUPPORTED value is returned.</span></span> 
  
<span data-ttu-id="24c03-109">O exemplo de código a seguir mostra como você pode implementar **QueryInterface** no C++ para um objeto status, um objeto que é uma subclasse da interface [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="24c03-109">The following code example shows how you can implement **QueryInterface** in C++ for a status object, an object that is a subclass of the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="24c03-110">**IMAPIStatus** herda de **IUnknown** a [IMAPIProp: IUnknown](imapipropiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="24c03-110">**IMAPIStatus** inherits from **IUnknown** through [IMAPIProp : IUnknown](imapipropiunknown.md).</span></span> <span data-ttu-id="24c03-111">Portanto, se um chamador solicitar qualquer uma dessas interfaces, o ponteiro \*\*\*\* pode ser retornado porque as interfaces estão relacionadas através de herança.</span><span class="sxs-lookup"><span data-stu-id="24c03-111">Therefore, if a caller asks for any of these interfaces, the **this** pointer can be returned because the interfaces are related through inheritance.</span></span> 
  
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

<span data-ttu-id="24c03-112">O exemplo de código a seguir mostra como implementar os métodos **AddRef** e **Release** para `CMyMAPIObject` o objeto.</span><span class="sxs-lookup"><span data-stu-id="24c03-112">The following code example shows how to implement the **AddRef** and **Release** methods for the  `CMyMAPIObject` object.</span></span> <span data-ttu-id="24c03-113">Como a implementação de **AddRef** e **Release** é direta, muitos provedores de serviço optam por implementá-los embutidos.</span><span class="sxs-lookup"><span data-stu-id="24c03-113">Because implementing **AddRef** and **Release** is straightforward, many service providers choose to implement them inline.</span></span> <span data-ttu-id="24c03-114">As chamadas para as funções do Win32 **InterlockedIncrement** e **InterlockedDecrement** garantem a segurança do thread.</span><span class="sxs-lookup"><span data-stu-id="24c03-114">The calls to the Win32 functions **InterlockedIncrement** and **InterlockedDecrement** ensure thread safety.</span></span> <span data-ttu-id="24c03-115">A memória do objeto é liberada pelo destruidor, que é chamado quando o método **Release** exclui o objeto.</span><span class="sxs-lookup"><span data-stu-id="24c03-115">The memory for the object is freed by the destructor, which is called when the **Release** method deletes the object.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="24c03-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="24c03-116">See also</span></span>

- [<span data-ttu-id="24c03-117">Implementar objetos MAPI</span><span class="sxs-lookup"><span data-stu-id="24c03-117">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)
- [<span data-ttu-id="24c03-118">Implementar a interface IUnknown</span><span class="sxs-lookup"><span data-stu-id="24c03-118">Implementing the IUnknown Interface</span></span>](implementing-the-iunknown-interface.md)

