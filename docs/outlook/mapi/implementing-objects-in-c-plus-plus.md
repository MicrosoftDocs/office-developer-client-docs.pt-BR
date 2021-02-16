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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432951"
---
# <a name="implementing-objects-in-c"></a>Implementar objetos em C++

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os clientes C++ e provedores de serviços definem objetos MAPI criando classes que herdam das interfaces que estão implementando. Cada um dos métodos de interface é público, assim como o construtor e destruidor da classe. Se a classe tiver métodos adicionais, elas poderão ser públicas ou privadas, dependendo da implementação. Todos os membros de dados são privados. 
  
O código de exemplo a seguir mostra como definir um objeto de status C++. A `CMyMAPIObject` classe herda da [interface IMAPIStatus : IMAPIProp.](imapistatusimapiprop.md) Muitas das macros usadas neste exemplo são definidas no arquivo de header OLE Compobj.h. Os primeiros membros da classe são os métodos da interface base, seguidos pelos métodos das interfaces herdadas em ordem de herança. Após as definições de interface estão quaisquer métodos adicionais, o construtor e o destruidor e os membros de dados. 
  
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

Para usar uma instância da classe, os clientes C++ ou provedores de serviços fazem uma chamada para um de  `CMyMAPIObject` seus métodos da seguinte forma: 
  
```cpp
lpMyObj->ValidateState(ulUIParam, ulFlags);

```

## <a name="see-also"></a>Confira também

- [Implementando objetos MAPI](implementing-mapi-objects.md)

