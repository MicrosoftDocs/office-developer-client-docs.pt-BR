---
title: Objeto MAPI e visão geral da Interface
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d4ece3af-cb54-4727-8072-0c055381ec11
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 8882457ff99f4150f2c9b086b92af32de29d60a7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767887"
---
# <a name="mapi-object-and-interface-overview"></a><span data-ttu-id="6f5a2-103">Objeto MAPI e visão geral da Interface</span><span class="sxs-lookup"><span data-stu-id="6f5a2-103">MAPI Object and Interface Overview</span></span>

  
  
<span data-ttu-id="6f5a2-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6f5a2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6f5a2-105">Um objeto MAPI é uma classe de objeto C++ ou a estrutura de dados C herdadas de uma ou mais interfaces MAPI ou conjuntos de funções relacionadas.</span><span class="sxs-lookup"><span data-stu-id="6f5a2-105">A MAPI object is a C++ object class or C data structure inherited from one or more MAPI interfaces, or collections of related functions.</span></span> <span data-ttu-id="6f5a2-106">Essas coleções de funções relacionadas são conhecidas para desenvolvedores do C++ como funções virtuais puras.</span><span class="sxs-lookup"><span data-stu-id="6f5a2-106">These collections of related functions are known to C++ developers as pure virtual functions.</span></span> <span data-ttu-id="6f5a2-107">Para uma função essencialmente virtual MAPI fontes somente o protótipo de função, não uma implementação.</span><span class="sxs-lookup"><span data-stu-id="6f5a2-107">For a pure virtual function, MAPI supplies only the function prototype, not an implementation.</span></span> <span data-ttu-id="6f5a2-108">Espera-se que um aplicativo cliente, um provedor de serviços ou MAPI fornecerá essa implementação criando uma classe de objeto que herda da interface e está em conformidade com as descrições de função da API de mensagens.</span><span class="sxs-lookup"><span data-stu-id="6f5a2-108">It is expected that a client application, a service provider, or MAPI will provide this implementation by creating an object class that inherits from the interface and conforms to the function descriptions of the Messaging API.</span></span> <span data-ttu-id="6f5a2-109">Uma interface MAPI pode ser instanciada apenas por meio de uma classe herdada.</span><span class="sxs-lookup"><span data-stu-id="6f5a2-109">A MAPI interface can be instantiated only through an inherited class.</span></span>
  
<span data-ttu-id="6f5a2-110">Há muitos objetos MAPI diferentes, cada objeto que herda de uma interface que é basicamente herdada da interface [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="6f5a2-110">There are many different MAPI objects, each object inheriting from an interface that is ultimately inherited from the [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) interface.</span></span> <span data-ttu-id="6f5a2-111">**IUnknown** é a interface de base OLE COM Component Object Model ().</span><span class="sxs-lookup"><span data-stu-id="6f5a2-111">**IUnknown** is the OLE Component Object Model (COM) base interface.</span></span> <span data-ttu-id="6f5a2-112">Ele fornece objetos MAPI com um mecanismo padrão para comunicação e controle.</span><span class="sxs-lookup"><span data-stu-id="6f5a2-112">It provides MAPI objects with a standard mechanism for communication and control.</span></span> <span data-ttu-id="6f5a2-113">COM dita como implementadores do objeto lidar com problemas, como gerenciamento de memória, gerenciamento de parâmetro e multithreading.</span><span class="sxs-lookup"><span data-stu-id="6f5a2-113">COM dictates how object implementers handle issues such as memory management, parameter management, and multithreading.</span></span> <span data-ttu-id="6f5a2-114">Conforme esse modelo, Implementador de um objeto de acordo com um contrato conforme especificado pelas interfaces incluídos no objeto.</span><span class="sxs-lookup"><span data-stu-id="6f5a2-114">By conforming to this model, an object implementer adheres to a contract as specified by the interfaces included in the object.</span></span> 
  
<span data-ttu-id="6f5a2-115">Muitas interfaces MAPI são herdadas diretamente do **IUnknown**, enquanto outras são herdadas indiretamente por meio de uma das duas interfaces de base: [IMAPIProp: IUnknown](imapipropiunknown.md) para gerenciamento de propriedade e [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md) para a pasta e acesso do catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="6f5a2-115">Many MAPI interfaces are inherited directly from **IUnknown**, while others are inherited indirectly through one of two other base interfaces: [IMAPIProp : IUnknown](imapipropiunknown.md) for property management and [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) for folder and address book access.</span></span> <span data-ttu-id="6f5a2-116">Interfaces base nunca são implementados como separado, objetos de autônomo; sempre são implementados como parte de outros objetos, derivado de objetos que implementam interfaces.</span><span class="sxs-lookup"><span data-stu-id="6f5a2-116">Base interfaces are never implemented as separate, standalone objects; they are always implemented as part of other objects, objects that implement derived interfaces.</span></span> 
  
<span data-ttu-id="6f5a2-117">MAPI define vários tipos de objetos, cada um implementado por um ou mais componentes MAPI.</span><span class="sxs-lookup"><span data-stu-id="6f5a2-117">MAPI defines many types of objects, each implemented by one or more MAPI components.</span></span> <span data-ttu-id="6f5a2-118">Objetos implementados por clientes são usados pelo MAPI, por provedores de serviços e pelos componentes do formulário personalizado.</span><span class="sxs-lookup"><span data-stu-id="6f5a2-118">Objects implemented by clients are used by MAPI, by service providers, and by custom form components.</span></span> <span data-ttu-id="6f5a2-119">Objetos implementados pelos provedores de serviço geralmente são usados por MAPI e pelos clientes.</span><span class="sxs-lookup"><span data-stu-id="6f5a2-119">Objects implemented by service providers are typically used by MAPI and by clients.</span></span> <span data-ttu-id="6f5a2-120">Objetos implementada por provedores de biblioteca de formulário e servidores de formulário são usados por outros componentes do formulário e pelos clientes.</span><span class="sxs-lookup"><span data-stu-id="6f5a2-120">Objects implemented by form library providers and form servers are used by other form components and by clients.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6f5a2-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="6f5a2-121">See also</span></span>



[<span data-ttu-id="6f5a2-122">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6f5a2-122">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="6f5a2-123">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="6f5a2-123">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="6f5a2-124">Conceitos MAPI</span><span class="sxs-lookup"><span data-stu-id="6f5a2-124">MAPI Concepts</span></span>](mapi-concepts.md)

