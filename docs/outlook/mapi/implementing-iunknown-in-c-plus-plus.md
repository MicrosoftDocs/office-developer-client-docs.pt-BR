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
# <a name="implementing-iunknown-in-c"></a>Implementar interface IUnknown em C++

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Implementar os métodos [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx), [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)e [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) da interface [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) em C++ é bastante simples. Após alguma validação padrão dos parâmetros que são passados, uma implementação de **QueryInterface** verifica o identificador da interface solicitada em relação à lista de interfaces com suporte. Se o identificador solicitado estiver entre os suportados, **AddRef** será chamado e o **ponteiro** será retornado. Se o identificador solicitado não estiver na lista com suporte, o ponteiro de saída será definido como NULL e o MAPI_E_INTERFACE_NOT_SUPPORTED valor será retornado. 
  
O exemplo de código a seguir mostra como você pode implementar **QueryInterface** em C++ para um objeto de status, um objeto que é uma subclasse da interface [IMAPIStatus : IMAPIProp.](imapistatusimapiprop.md) **IMAPIStatus** herda de **IUnknown** através [de IMAPIProp : IUnknown](imapipropiunknown.md). Portanto, se um chamador solicita qualquer uma  dessas interfaces, o ponteiro pode ser retornado porque as interfaces estão relacionadas por herança. 
  
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

O exemplo de código a seguir mostra como implementar os **métodos AddRef** e **Release** para o  `CMyMAPIObject` objeto. Como implementar **AddRef** e **Release** é simples, muitos provedores de serviços optam por implementá-los em linha. As chamadas para as funções Win32 **InterlockedIncrement** e **InterlockedDecrement** garantem a segurança do thread. A memória para o objeto é liberada pelo destruidor, que é chamado quando o **método Release** exclui o objeto. 
  
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

- [Implementando objetos MAPI](implementing-mapi-objects.md)
- [Implementando a interface IUnknown](implementing-the-iunknown-interface.md)

