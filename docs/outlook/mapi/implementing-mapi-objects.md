---
title: Implementar objetos MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b1ee2533-8077-4976-846b-d42d148bf8c6
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: c0d67d10d54591de926724cbf594a44f17e9ea14
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310168"
---
# <a name="implementing-mapi-objects"></a><span data-ttu-id="9ae91-103">Implementar objetos MAPI</span><span class="sxs-lookup"><span data-stu-id="9ae91-103">Implementing MAPI Objects</span></span>

  
  
<span data-ttu-id="9ae91-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9ae91-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9ae91-105">Os objetos MAPI podem ser implementados usando classes C++ ou estruturas de dados C, dependendo do idioma e do conjunto de APIs que um cliente ou provedor de serviços está usando.</span><span class="sxs-lookup"><span data-stu-id="9ae91-105">MAPI objects can be implemented by using C++ classes or C data structures, depending on the language and the API set a client or service provider is using.</span></span> <span data-ttu-id="9ae91-106">Os provedores de serviços podem ser escritos em C ou C++ com a interface do provedor de serviços MAPI; os aplicativos cliente também podem usar C ou C++.</span><span class="sxs-lookup"><span data-stu-id="9ae91-106">Service providers can be written in C or C++ with the MAPI service provider interface; client applications can also use C or C++.</span></span> <span data-ttu-id="9ae91-107">Se possível, os clientes e provedores de serviço que usam a interface de programação orientada a objeto devem usar C++.</span><span class="sxs-lookup"><span data-stu-id="9ae91-107">If possible, clients and service providers that use the object-oriented programming interface should use C++.</span></span> 
  
<span data-ttu-id="9ae91-108">O C++ é a escolha preferida porque MAPI é uma tecnologia orientada a objeto e o C++ presta-se mais prontamente ao desenvolvimento orientado a objeto.</span><span class="sxs-lookup"><span data-stu-id="9ae91-108">C++ is the preferred choice because MAPI is an object-oriented technology, and C++ lends itself more readily to object-oriented development.</span></span> <span data-ttu-id="9ae91-109">O código resultante é mais simples e mais simples, facilitando a manutenção.</span><span class="sxs-lookup"><span data-stu-id="9ae91-109">The resulting code is simpler and more straightforward, making it easier to maintain.</span></span> <span data-ttu-id="9ae91-110">A documentação MAPI é escrita principalmente para desenvolvedores do C++; todas as descrições de sintaxe dos métodos de interface MAPI nesta referência estão em C++.</span><span class="sxs-lookup"><span data-stu-id="9ae91-110">The MAPI documentation is written primarily for C++ developers; all of the syntax descriptions for the MAPI interface methods in this Reference are in C++.</span></span>
  
<span data-ttu-id="9ae91-111">Os desenvolvedores podem usar o Microsoft Visual Studio e ferramentas de desenvolvimento de terceiros para desenvolver soluções que chamam MAPI.</span><span class="sxs-lookup"><span data-stu-id="9ae91-111">Developers can use Microsoft Visual Studio and third-party development tools to develop solutions that call MAPI.</span></span> <span data-ttu-id="9ae91-112">Observe que os desenvolvedores devem usar o C++ C ou não gerenciado, mas não o C++ para escrever soluções MAPI.</span><span class="sxs-lookup"><span data-stu-id="9ae91-112">Note that developers should use C or unmanaged C++, but not managed C++ to write MAPI solutions.</span></span>
  
<span data-ttu-id="9ae91-113">Quando um objeto MAPI é implementado, um cliente ou provedor de serviços cria código para todos os métodos de interface, código para qualquer método privado específico da implementação e código para dar suporte a membros de dados privados para manter informações de estado.</span><span class="sxs-lookup"><span data-stu-id="9ae91-113">When a MAPI object is implemented, a client or service provider creates code for all of the interface methods, code for any private methods that are specific to the implementation, and code to support private data members for maintaining state information.</span></span> <span data-ttu-id="9ae91-114">O código dos métodos de interface deve seguir as especificações publicadas por MAPI que documentam o comportamento esperado.</span><span class="sxs-lookup"><span data-stu-id="9ae91-114">The code for the interface methods must follow the specifications published by MAPI that document expected behavior.</span></span> 
  
<span data-ttu-id="9ae91-115">Há muitas macros no arquivo de cabeçalho mapidefs. h e arquivos de cabeçalho OLE que os clientes e provedores de serviço em qualquer idioma podem usar para ajudá-los com suas definições de objetos MAPI.</span><span class="sxs-lookup"><span data-stu-id="9ae91-115">There are many macros in the Mapidefs.h header file and OLE header files that clients and service providers in either language can use to help them with their definitions of MAPI objects.</span></span> <span data-ttu-id="9ae91-116">Por exemplo, há uma macro para definir os métodos de cada uma das interfaces MAPI.</span><span class="sxs-lookup"><span data-stu-id="9ae91-116">For example, there is a macro to define the methods of each of the MAPI interfaces.</span></span> <span data-ttu-id="9ae91-117">A macro para definir os métodos da interface [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) aparece em mapidefs. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="9ae91-117">The macro to define the methods of the [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) interface appears in Mapidefs.h as follows:</span></span> 
  
```cpp
#define MAPI_IUNKNOWN_METHODS(IPURE)          \
    MAPIMETHOD(QueryInterface)                \
        (THIS_ REFIID riid, LPVOID FAR * ppvObj) IPURE;    \
    MAPIMETHOD_(ULONG,AddRef)  (THIS) IPURE;               \
    MAPIMETHOD_(ULONG,Release) (THIS) IPURE;   \
 
```

## <a name="see-also"></a><span data-ttu-id="9ae91-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="9ae91-118">See also</span></span>



[<span data-ttu-id="9ae91-119">Visão geral de interface e objeto MAPI</span><span class="sxs-lookup"><span data-stu-id="9ae91-119">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

