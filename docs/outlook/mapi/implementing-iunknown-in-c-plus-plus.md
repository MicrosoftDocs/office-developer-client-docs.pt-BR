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
# <a name="implementing-iunknown-in-c"></a>Implementar interface IUnknown em C++

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Implementar os métodos [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx), [AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)e [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) da interface [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) em C++ é razoavelmente simple. Após algum validação padrão dos parâmetros que sejam passados, uma implementação de **QueryInterface** verifica o identificador da interface solicitada contra a lista das interfaces com suporte. Se o identificador solicitado for entre aqueles que têm suporte, **AddRef** é chamado e o ponteiro **this** é retornado. Se o identificador solicitado não estiver ligado a lista com suporte, o ponteiro de saída é definido como nulo e o valor MAPI_E_INTERFACE_NOT_SUPPORTED será retornado. 
  
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

