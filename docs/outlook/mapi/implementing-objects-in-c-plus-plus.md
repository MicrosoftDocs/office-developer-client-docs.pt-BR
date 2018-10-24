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
ms.openlocfilehash: 4c233f9855674080496b2e54ba9548a53738ead8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574724"
---
# <a name="implementing-objects-in-c"></a><span data-ttu-id="03e89-103">Implementar objetos em C++</span><span class="sxs-lookup"><span data-stu-id="03e89-103">Implementing objects in C++</span></span>

<span data-ttu-id="03e89-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="03e89-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="03e89-105">Provedores de serviços e clientes C++ definem os objetos MAPI, criando classes que herdam as interfaces estão implementando.</span><span class="sxs-lookup"><span data-stu-id="03e89-105">C++ clients and service providers define MAPI objects by creating classes that inherit from the interfaces they are implementing.</span></span> <span data-ttu-id="03e89-106">Cada um dos métodos interface é pública, assim como o construtor e destrutor para a classe.</span><span class="sxs-lookup"><span data-stu-id="03e89-106">Each of the interface methods is public, as are the constructor and destructor for the class.</span></span> <span data-ttu-id="03e89-107">Se a classe tem métodos adicionais, eles podem ser pública ou privada, dependendo da implementação.</span><span class="sxs-lookup"><span data-stu-id="03e89-107">If the class has additional methods, they can be public or private, depending on the implementation.</span></span> <span data-ttu-id="03e89-108">Todos os membros de dados são privados.</span><span class="sxs-lookup"><span data-stu-id="03e89-108">All data members are private.</span></span> 
  
<span data-ttu-id="03e89-109">O exemplo de código a seguir mostra como definir um objeto de status do C++.</span><span class="sxs-lookup"><span data-stu-id="03e89-109">The following example code shows how to define a C++ status object.</span></span> <span data-ttu-id="03e89-110">O `CMyMAPIObject` classe herda a partir do [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) interface.</span><span class="sxs-lookup"><span data-stu-id="03e89-110">The  `CMyMAPIObject` class inherits from the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="03e89-111">Muitas das macros usadas neste exemplo são definidas no arquivo de cabeçalho OLE Compobj.h.</span><span class="sxs-lookup"><span data-stu-id="03e89-111">Many of the macros used in this example are defined in the OLE header file Compobj.h.</span></span> <span data-ttu-id="03e89-112">Os primeiro membros da classe são os métodos da interface base, seguido os métodos para as interfaces herdadas na ordem de herança.</span><span class="sxs-lookup"><span data-stu-id="03e89-112">The first members of the class are the methods of the base interface, followed by the methods of the inherited interfaces in order of inheritance.</span></span> <span data-ttu-id="03e89-113">Seguir as definições de interface é quaisquer métodos adicionais, o construtor e destrutor e os membros de dados.</span><span class="sxs-lookup"><span data-stu-id="03e89-113">Following the interface definitions are any additional methods, the constructor and destructor, and the data members.</span></span> 
  
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

<span data-ttu-id="03e89-114">Para usar uma instância do `CMyMAPIObject` classe, clientes C++ ou provedores de serviços de fazer uma chamada para um de seus métodos das seguintes formas:</span><span class="sxs-lookup"><span data-stu-id="03e89-114">To use an instance of the  `CMyMAPIObject` class, C++ clients or service providers make a call to one of its methods as follows:</span></span> 
  
```cpp
lpMyObj->ValidateState(ulUIParam, ulFlags);

```

## <a name="see-also"></a><span data-ttu-id="03e89-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="03e89-115">See also</span></span>

- [<span data-ttu-id="03e89-116">Implementar objetos de MAPI</span><span class="sxs-lookup"><span data-stu-id="03e89-116">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)

