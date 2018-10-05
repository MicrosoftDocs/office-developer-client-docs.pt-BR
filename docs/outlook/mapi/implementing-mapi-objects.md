---
title: Implementar objetos MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b1ee2533-8077-4976-846b-d42d148bf8c6
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: c0d67d10d54591de926724cbf594a44f17e9ea14
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397097"
---
# <a name="implementing-mapi-objects"></a><span data-ttu-id="1be40-103">Implementar objetos MAPI</span><span class="sxs-lookup"><span data-stu-id="1be40-103">Implementing MAPI Objects</span></span>

  
  
<span data-ttu-id="1be40-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1be40-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1be40-105">Objetos MAPI podem ser implementados usando classes C++ ou C estruturas de dados, dependendo do idioma e a API definido um cliente ou usando o provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="1be40-105">MAPI objects can be implemented by using C++ classes or C data structures, depending on the language and the API set a client or service provider is using.</span></span> <span data-ttu-id="1be40-106">Provedores de serviço podem ser escritos em C ou C++ com a interface do provedor de serviços MAPI; aplicativos cliente também podem usar C ou C++.</span><span class="sxs-lookup"><span data-stu-id="1be40-106">Service providers can be written in C or C++ with the MAPI service provider interface; client applications can also use C or C++.</span></span> <span data-ttu-id="1be40-107">Se possível, clientes e provedores de serviços que usam a interface de programação orientado a objetos devem usar C++.</span><span class="sxs-lookup"><span data-stu-id="1be40-107">If possible, clients and service providers that use the object-oriented programming interface should use C++.</span></span> 
  
<span data-ttu-id="1be40-108">C++ é a opção preferida porque MAPI é uma tecnologia orientada e C++ presta mais prontamente a desenvolvimento orientado a objetos.</span><span class="sxs-lookup"><span data-stu-id="1be40-108">C++ is the preferred choice because MAPI is an object-oriented technology, and C++ lends itself more readily to object-oriented development.</span></span> <span data-ttu-id="1be40-109">O código resultante é mais simples e mais ágil, facilitando a manutenção.</span><span class="sxs-lookup"><span data-stu-id="1be40-109">The resulting code is simpler and more straightforward, making it easier to maintain.</span></span> <span data-ttu-id="1be40-110">A documentação de MAPI foi escrita principalmente para desenvolvedores de C++; todas as descrições de sintaxe para os métodos de interface MAPI nesta referência estão em C++.</span><span class="sxs-lookup"><span data-stu-id="1be40-110">The MAPI documentation is written primarily for C++ developers; all of the syntax descriptions for the MAPI interface methods in this Reference are in C++.</span></span>
  
<span data-ttu-id="1be40-111">Os desenvolvedores podem usar o Microsoft Visual Studio e ferramentas de desenvolvimento de terceiros para desenvolver soluções que chamam MAPI.</span><span class="sxs-lookup"><span data-stu-id="1be40-111">Developers can use Microsoft Visual Studio and third-party development tools to develop solutions that call MAPI.</span></span> <span data-ttu-id="1be40-112">Observe que os desenvolvedores devem usar C ou C++ não gerenciado, mas não gerenciadas do C++ para gravar as soluções MAPI.</span><span class="sxs-lookup"><span data-stu-id="1be40-112">Note that developers should use C or unmanaged C++, but not managed C++ to write MAPI solutions.</span></span>
  
<span data-ttu-id="1be40-113">Quando um objeto MAPI é implementado, um provedor de cliente ou serviço cria código para todos os métodos de interface, o código para quaisquer métodos privados que são específicas para a implementação e o código para dar suporte a membros de dados particulares para manutenção de informações de estado.</span><span class="sxs-lookup"><span data-stu-id="1be40-113">When a MAPI object is implemented, a client or service provider creates code for all of the interface methods, code for any private methods that are specific to the implementation, and code to support private data members for maintaining state information.</span></span> <span data-ttu-id="1be40-114">O código para os métodos de interface deve seguir as especificações publicadas pela MAPI que documentam o comportamento esperado.</span><span class="sxs-lookup"><span data-stu-id="1be40-114">The code for the interface methods must follow the specifications published by MAPI that document expected behavior.</span></span> 
  
<span data-ttu-id="1be40-115">Há muitas macros no arquivo de cabeçalho Mapidefs.h e arquivos de cabeçalho OLE que os clientes e provedores de serviços em qualquer idioma podem usar para ajudá-los com suas definições de objetos MAPI.</span><span class="sxs-lookup"><span data-stu-id="1be40-115">There are many macros in the Mapidefs.h header file and OLE header files that clients and service providers in either language can use to help them with their definitions of MAPI objects.</span></span> <span data-ttu-id="1be40-116">Por exemplo, há uma macro para definir os métodos de cada uma das interfaces de MAPI.</span><span class="sxs-lookup"><span data-stu-id="1be40-116">For example, there is a macro to define the methods of each of the MAPI interfaces.</span></span> <span data-ttu-id="1be40-117">A macro para definir os métodos da interface [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) aparece no Mapidefs.h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="1be40-117">The macro to define the methods of the [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) interface appears in Mapidefs.h as follows:</span></span> 
  
```cpp
#define MAPI_IUNKNOWN_METHODS(IPURE)          \
    MAPIMETHOD(QueryInterface)                \
        (THIS_ REFIID riid, LPVOID FAR * ppvObj) IPURE;    \
    MAPIMETHOD_(ULONG,AddRef)  (THIS) IPURE;               \
    MAPIMETHOD_(ULONG,Release) (THIS) IPURE;   \
 
```

## <a name="see-also"></a><span data-ttu-id="1be40-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="1be40-118">See also</span></span>



[<span data-ttu-id="1be40-119">Objeto MAPI e visão geral da Interface</span><span class="sxs-lookup"><span data-stu-id="1be40-119">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

