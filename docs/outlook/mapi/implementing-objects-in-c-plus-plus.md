---
title: Implementando objetos em C++
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d1a050ff-3cf9-4bf7-812d-b7c1b31056e7
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: ea9f37183f33459b09f2730b3efbb7afed3d4766
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767429"
---
# <a name="implementing-objects-in-c"></a>Implementando objetos em C++

**Aplica-se a**: Outlook 
  
Provedores de serviços e clientes C++ definem os objetos MAPI, criando classes que herdam as interfaces estão implementando. Cada um dos métodos interface é pública, assim como o construtor e destrutor para a classe. Se a classe tem métodos adicionais, eles podem ser pública ou privada, dependendo da implementação. Todos os membros de dados são privados. 
  
O exemplo de código a seguir mostra como definir um objeto de status do C++. O `CMyMAPIObject` classe herda a partir do [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) interface. Muitas das macros usadas neste exemplo são definidas no arquivo de cabeçalho OLE Compobj.h. Os primeiro membros da classe são os métodos da interface base, seguido os métodos para as interfaces herdadas na ordem de herança. Seguir as definições de interface é quaisquer métodos adicionais, o construtor e destrutor e os membros de dados. 
  
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

Para usar uma instância do `CMyMAPIObject` classe, clientes C++ ou provedores de serviços de fazer uma chamada para um de seus métodos das seguintes formas: 
  
```cpp
lpMyObj->ValidateState(ulUIParam, ulFlags);

```

## <a name="see-also"></a>Confira também

- [Implementar objetos MAPI](implementing-mapi-objects.md)

