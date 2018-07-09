---
title: Implementando IUnknown em C++
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 68519f6c-fba8-47f5-9401-316e276f770e
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: c899eb0afd123b26e12081f5157be3bae7917813
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767436"
---
# <a name="implementing-iunknown-in-c"></a><span data-ttu-id="a7cb7-103">Implementando IUnknown em C++</span><span class="sxs-lookup"><span data-stu-id="a7cb7-103">Implementing IUnknown in C++</span></span>

<span data-ttu-id="a7cb7-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a7cb7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a7cb7-105">Implementar os métodos [IUnknown:: QueryInterface](http://msdn.microsoft.com/pt-br/library/ms682521%28v=VS.85%29.aspx), [AddRef](http://msdn.microsoft.com/pt-br/library/ms691379%28v=VS.85%29.aspx)e [IUnknown:: Release](http://msdn.microsoft.com/pt-br/library/ms682317%28v=VS.85%29.aspx) da interface [IUnknown](http://msdn.microsoft.com/pt-br/library/ms680509%28v=VS.85%29.aspx) em C++ é razoavelmente simple.</span><span class="sxs-lookup"><span data-stu-id="a7cb7-105">Implementing the [IUnknown::QueryInterface](http://msdn.microsoft.com/pt-br/library/ms682521%28v=VS.85%29.aspx), [IUnknown::AddRef](http://msdn.microsoft.com/pt-br/library/ms691379%28v=VS.85%29.aspx), and [IUnknown::Release](http://msdn.microsoft.com/pt-br/library/ms682317%28v=VS.85%29.aspx) methods of the [IUnknown](http://msdn.microsoft.com/pt-br/library/ms680509%28v=VS.85%29.aspx) interface in C++ is fairly simple.</span></span> <span data-ttu-id="a7cb7-106">Após algum validação padrão dos parâmetros que sejam passados, uma implementação de **QueryInterface** verifica o identificador da interface solicitada contra a lista das interfaces com suporte.</span><span class="sxs-lookup"><span data-stu-id="a7cb7-106">After some standard validation of the parameters that are passed in, an implementation of **QueryInterface** checks the identifier of the requested interface against the list of supported interfaces.</span></span> <span data-ttu-id="a7cb7-107">Se o identificador solicitado for entre aqueles que têm suporte, **AddRef** é chamado e o ponteiro **this** é retornado.</span><span class="sxs-lookup"><span data-stu-id="a7cb7-107">If the requested identifier is among those supported, **AddRef** is called and the **this** pointer is returned.</span></span> <span data-ttu-id="a7cb7-108">Se o identificador solicitado não estiver ligado a lista com suporte, o ponteiro de saída é definido como nulo e o valor MAPI_E_INTERFACE_NOT_SUPPORTED será retornado.</span><span class="sxs-lookup"><span data-stu-id="a7cb7-108">If the requested identifier is not on the supported list, the output pointer is set to NULL and the MAPI_E_INTERFACE_NOT_SUPPORTED value is returned.</span></span> 
  
<span data-ttu-id="a7cb7-109">O exemplo de código a seguir mostra como você pode implementar **QueryInterface** em C++ para um objeto de status, um objeto que é uma subclasse do [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) interface.</span><span class="sxs-lookup"><span data-stu-id="a7cb7-109">The following code example shows how you can implement **QueryInterface** in C++ for a status object, an object that is a subclass of the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="a7cb7-110">**IMAPIStatus** herda de **IUnknown** através de [IMAPIProp: IUnknown](imapipropiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="a7cb7-110">**IMAPIStatus** inherits from **IUnknown** through [IMAPIProp : IUnknown](imapipropiunknown.md).</span></span> <span data-ttu-id="a7cb7-111">Portanto, se um chamador pedir para qualquer uma dessas interfaces, o ponteiro **this** pode ser retornado porque as interfaces estão relacionadas por meio de herança.</span><span class="sxs-lookup"><span data-stu-id="a7cb7-111">Therefore, if a caller asks for any of these interfaces, the **this** pointer can be returned because the interfaces are related through inheritance.</span></span> 
  
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

<span data-ttu-id="a7cb7-112">O exemplo de código a seguir mostra como implementar os métodos **AddRef** e **Release** para o `CMyMAPIObject` objeto.</span><span class="sxs-lookup"><span data-stu-id="a7cb7-112">The following code example shows how to implement the **AddRef** and **Release** methods for the  `CMyMAPIObject` object.</span></span> <span data-ttu-id="a7cb7-113">Como implementar **AddRef** e **Release** seja simples, muitos provedores de serviço escolher implementá-las embutida.</span><span class="sxs-lookup"><span data-stu-id="a7cb7-113">Because implementing **AddRef** and **Release** is straightforward, many service providers choose to implement them inline.</span></span> <span data-ttu-id="a7cb7-114">As chamadas para as funções de Win32 **InterlockedIncrement** e **InterlockedDecrement** garantem a segurança do thread.</span><span class="sxs-lookup"><span data-stu-id="a7cb7-114">The calls to the Win32 functions **InterlockedIncrement** and **InterlockedDecrement** ensure thread safety.</span></span> <span data-ttu-id="a7cb7-115">A memória para o objeto é liberada pelo destrutor, o que é chamado quando o método **versão** exclui o objeto.</span><span class="sxs-lookup"><span data-stu-id="a7cb7-115">The memory for the object is freed by the destructor, which is called when the **Release** method deletes the object.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="a7cb7-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="a7cb7-116">See also</span></span>

- [<span data-ttu-id="a7cb7-117">Implementar objetos de MAPI</span><span class="sxs-lookup"><span data-stu-id="a7cb7-117">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)
- [<span data-ttu-id="a7cb7-118">Implementando a Interface IUnknown</span><span class="sxs-lookup"><span data-stu-id="a7cb7-118">Implementing the IUnknown Interface</span></span>](implementing-the-iunknown-interface.md)

