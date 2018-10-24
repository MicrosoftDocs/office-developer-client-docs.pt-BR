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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397832"
---
# <a name="implementing-iunknown-in-c"></a><span data-ttu-id="7cbdb-103">Implementar interface IUnknown em C++</span><span class="sxs-lookup"><span data-stu-id="7cbdb-103">Implementing IUnknown in C++</span></span>

<span data-ttu-id="7cbdb-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7cbdb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7cbdb-105">Implementar os métodos [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx), [AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)e [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) da interface [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) em C++ é razoavelmente simple.</span><span class="sxs-lookup"><span data-stu-id="7cbdb-105">Implementing the [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx), [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx), and [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) methods of the [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) interface in C++ is fairly simple.</span></span> <span data-ttu-id="7cbdb-106">Após algum validação padrão dos parâmetros que sejam passados, uma implementação de **QueryInterface** verifica o identificador da interface solicitada contra a lista das interfaces com suporte.</span><span class="sxs-lookup"><span data-stu-id="7cbdb-106">After some standard validation of the parameters that are passed in, an implementation of **QueryInterface** checks the identifier of the requested interface against the list of supported interfaces.</span></span> <span data-ttu-id="7cbdb-107">Se o identificador solicitado for entre aqueles que têm suporte, **AddRef** é chamado e o ponteiro **this** é retornado.</span><span class="sxs-lookup"><span data-stu-id="7cbdb-107">If the requested identifier is among those supported, **AddRef** is called and the **this** pointer is returned.</span></span> <span data-ttu-id="7cbdb-108">Se o identificador solicitado não estiver ligado a lista com suporte, o ponteiro de saída é definido como nulo e o valor MAPI_E_INTERFACE_NOT_SUPPORTED será retornado.</span><span class="sxs-lookup"><span data-stu-id="7cbdb-108">If the requested identifier is not on the supported list, the output pointer is set to NULL and the MAPI_E_INTERFACE_NOT_SUPPORTED value is returned.</span></span> 
  
<span data-ttu-id="7cbdb-109">O exemplo de código a seguir mostra como você pode implementar **QueryInterface** em C++ para um objeto de status, um objeto que é uma subclasse do [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) interface.</span><span class="sxs-lookup"><span data-stu-id="7cbdb-109">The following code example shows how you can implement **QueryInterface** in C++ for a status object, an object that is a subclass of the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="7cbdb-110">**IMAPIStatus** herda de **IUnknown** através de [IMAPIProp: IUnknown](imapipropiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="7cbdb-110">**IMAPIStatus** inherits from **IUnknown** through [IMAPIProp : IUnknown](imapipropiunknown.md).</span></span> <span data-ttu-id="7cbdb-111">Portanto, se um chamador pedir para qualquer uma dessas interfaces, o ponteiro **this** pode ser retornado porque as interfaces estão relacionadas por meio de herança.</span><span class="sxs-lookup"><span data-stu-id="7cbdb-111">Therefore, if a caller asks for any of these interfaces, the **this** pointer can be returned because the interfaces are related through inheritance.</span></span> 
  
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

<span data-ttu-id="7cbdb-112">O exemplo de código a seguir mostra como implementar os métodos **AddRef** e **Release** para o `CMyMAPIObject` objeto.</span><span class="sxs-lookup"><span data-stu-id="7cbdb-112">The following code example shows how to implement the **AddRef** and **Release** methods for the  `CMyMAPIObject` object.</span></span> <span data-ttu-id="7cbdb-113">Como implementar **AddRef** e **Release** seja simples, muitos provedores de serviço escolher implementá-las embutida.</span><span class="sxs-lookup"><span data-stu-id="7cbdb-113">Because implementing **AddRef** and **Release** is straightforward, many service providers choose to implement them inline.</span></span> <span data-ttu-id="7cbdb-114">As chamadas para as funções de Win32 **InterlockedIncrement** e **InterlockedDecrement** garantem a segurança do thread.</span><span class="sxs-lookup"><span data-stu-id="7cbdb-114">The calls to the Win32 functions **InterlockedIncrement** and **InterlockedDecrement** ensure thread safety.</span></span> <span data-ttu-id="7cbdb-115">A memória para o objeto é liberada pelo destrutor, o que é chamado quando o método **versão** exclui o objeto.</span><span class="sxs-lookup"><span data-stu-id="7cbdb-115">The memory for the object is freed by the destructor, which is called when the **Release** method deletes the object.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="7cbdb-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="7cbdb-116">See also</span></span>

- [<span data-ttu-id="7cbdb-117">Implementar objetos de MAPI</span><span class="sxs-lookup"><span data-stu-id="7cbdb-117">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)
- [<span data-ttu-id="7cbdb-118">Implementando a Interface IUnknown</span><span class="sxs-lookup"><span data-stu-id="7cbdb-118">Implementing the IUnknown Interface</span></span>](implementing-the-iunknown-interface.md)

