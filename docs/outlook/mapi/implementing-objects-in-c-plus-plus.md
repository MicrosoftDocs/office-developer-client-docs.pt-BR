---
title: Implementar objetos em C++
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d1a050ff-3cf9-4bf7-812d-b7c1b31056e7
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 89247ca1b263d6f06af73f1ffa14709a2aff23de
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310147"
---
# <a name="implementing-objects-in-c"></a>Implementar objetos em C++

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Clientes C++ e provedores de serviços definem as classes que herdam as interfaces que estão implementando. Cada um dos métodos de interface é público, como é o construtor e o destruidor da classe. Se a classe tem métodos adicionais, elas podem ser públicas ou privadas, dependendo da implementação. Todos os membros de dados são privados. 
  
O código de exemplo a seguir mostra como definir um objeto status do C++. A `CMyMAPIObject` classe herda da interface [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) . Muitas das macros usadas neste exemplo são definidas no arquivo de cabeçalho OLE COMPOBJ. h. Os primeiros membros da classe são os métodos da interface base, seguidos pelos métodos das interfaces herdadas em ordem de herança. Seguir as definições de interface são quaisquer métodos adicionais, o construtor e o destruidor e os membros de dados. 
  
```cpp
class  CMyMAPIObject : public IMAPIStatus
{
public:
// Methods of IUnknown.
    STDMETHODIMP QueryInterface (REFIID riid, LPVOID * ppvObj);
    STDMETHODIMP_(ULONG) AddRef ();
    STDMETHODIMP_(ULONG) Release ();
    MAPI_IMAPIPROP_METHODS(IMPL);
    MAPI_IMAPISTATUS_METHODS(IMPL);
// Other methods specific to CMyMAPIObject.
    BOOL WINAPI Method1 ();
    void WINAPI Method2 ();
// Constructors and destructors.
public :
    CMyMAPIObject () {};
    ~CMyMAPIObject () {};
// Data members specific to CMyMAPIObject.
private :
    ULONG               m_cRef;
    CAnotherObj *       m_pObj;
};
 
```

Para usar uma instância da `CMyMAPIObject` classe, os clientes C++ ou provedores de serviços fazem uma chamada para um dos seus métodos da seguinte maneira: 
  
```cpp
lpMyObj->ValidateState(ulUIParam, ulFlags);

```

## <a name="see-also"></a>Confira também

- [Implementar objetos MAPI](implementing-mapi-objects.md)

