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
# <a name="implementing-iunknown-in-c"></a>Implementando IUnknown em C++

**Aplica-se a**: Outlook 
  
Implementar os métodos [IUnknown:: QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx), [AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx)e [IUnknown:: Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) da interface [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) em C++ é razoavelmente simple. Após algum validação padrão dos parâmetros que sejam passados, uma implementação de **QueryInterface** verifica o identificador da interface solicitada contra a lista das interfaces com suporte. Se o identificador solicitado for entre aqueles que têm suporte, **AddRef** é chamado e o ponteiro **this** é retornado. Se o identificador solicitado não estiver ligado a lista com suporte, o ponteiro de saída é definido como nulo e o valor MAPI_E_INTERFACE_NOT_SUPPORTED será retornado. 
  
O exemplo de código a seguir mostra como você pode implementar **QueryInterface** em C++ para um objeto de status, um objeto que é uma subclasse do [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) interface. **IMAPIStatus** herda de **IUnknown** através de [IMAPIProp: IUnknown](imapipropiunknown.md). Portanto, se um chamador pedir para qualquer uma dessas interfaces, o ponteiro **this** pode ser retornado porque as interfaces estão relacionadas por meio de herança. 
  
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

O exemplo de código a seguir mostra como implementar os métodos **AddRef** e **Release** para o `CMyMAPIObject` objeto. Como implementar **AddRef** e **Release** seja simples, muitos provedores de serviço escolher implementá-las embutida. As chamadas para as funções de Win32 **InterlockedIncrement** e **InterlockedDecrement** garantem a segurança do thread. A memória para o objeto é liberada pelo destrutor, o que é chamado quando o método **versão** exclui o objeto. 
  
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

## <a name="see-also"></a>Confira também

- [Implementar objetos de MAPI](implementing-mapi-objects.md)
- [Implementando a Interface IUnknown](implementing-the-iunknown-interface.md)

