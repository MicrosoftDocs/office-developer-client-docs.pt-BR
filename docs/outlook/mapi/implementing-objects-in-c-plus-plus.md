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
# <a name="implementing-objects-in-c"></a><span data-ttu-id="13b53-103">Implementar objetos em C++</span><span class="sxs-lookup"><span data-stu-id="13b53-103">Implementing objects in C++</span></span>

<span data-ttu-id="13b53-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="13b53-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="13b53-105">Clientes C++ e provedores de serviços definem as classes que herdam as interfaces que estão implementando.</span><span class="sxs-lookup"><span data-stu-id="13b53-105">C++ clients and service providers define MAPI objects by creating classes that inherit from the interfaces they are implementing.</span></span> <span data-ttu-id="13b53-106">Cada um dos métodos de interface é público, como é o construtor e o destruidor da classe.</span><span class="sxs-lookup"><span data-stu-id="13b53-106">Each of the interface methods is public, as are the constructor and destructor for the class.</span></span> <span data-ttu-id="13b53-107">Se a classe tem métodos adicionais, elas podem ser públicas ou privadas, dependendo da implementação.</span><span class="sxs-lookup"><span data-stu-id="13b53-107">If the class has additional methods, they can be public or private, depending on the implementation.</span></span> <span data-ttu-id="13b53-108">Todos os membros de dados são privados.</span><span class="sxs-lookup"><span data-stu-id="13b53-108">All data members are private.</span></span> 
  
<span data-ttu-id="13b53-109">O código de exemplo a seguir mostra como definir um objeto status do C++.</span><span class="sxs-lookup"><span data-stu-id="13b53-109">The following example code shows how to define a C++ status object.</span></span> <span data-ttu-id="13b53-110">A `CMyMAPIObject` classe herda da interface [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="13b53-110">The  `CMyMAPIObject` class inherits from the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="13b53-111">Muitas das macros usadas neste exemplo são definidas no arquivo de cabeçalho OLE COMPOBJ. h.</span><span class="sxs-lookup"><span data-stu-id="13b53-111">Many of the macros used in this example are defined in the OLE header file Compobj.h.</span></span> <span data-ttu-id="13b53-112">Os primeiros membros da classe são os métodos da interface base, seguidos pelos métodos das interfaces herdadas em ordem de herança.</span><span class="sxs-lookup"><span data-stu-id="13b53-112">The first members of the class are the methods of the base interface, followed by the methods of the inherited interfaces in order of inheritance.</span></span> <span data-ttu-id="13b53-113">Seguir as definições de interface são quaisquer métodos adicionais, o construtor e o destruidor e os membros de dados.</span><span class="sxs-lookup"><span data-stu-id="13b53-113">Following the interface definitions are any additional methods, the constructor and destructor, and the data members.</span></span> 
  
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

<span data-ttu-id="13b53-114">Para usar uma instância da `CMyMAPIObject` classe, os clientes C++ ou provedores de serviços fazem uma chamada para um dos seus métodos da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="13b53-114">To use an instance of the  `CMyMAPIObject` class, C++ clients or service providers make a call to one of its methods as follows:</span></span> 
  
```cpp
lpMyObj->ValidateState(ulUIParam, ulFlags);

```

## <a name="see-also"></a><span data-ttu-id="13b53-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="13b53-115">See also</span></span>

- [<span data-ttu-id="13b53-116">Implementar objetos MAPI</span><span class="sxs-lookup"><span data-stu-id="13b53-116">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)

