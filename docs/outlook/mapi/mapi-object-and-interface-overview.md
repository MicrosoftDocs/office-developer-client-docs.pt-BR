---
title: Visão geral de objetos e interface MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d4ece3af-cb54-4727-8072-0c055381ec11
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: fcd85bf518f4e6466bf15a09e417767bc34df78d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345784"
---
# <a name="mapi-object-and-interface-overview"></a><span data-ttu-id="d1e17-103">Visão geral de objetos e interface MAPI</span><span class="sxs-lookup"><span data-stu-id="d1e17-103">MAPI Object and Interface Overview</span></span>

  
  
<span data-ttu-id="d1e17-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d1e17-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d1e17-105">Um objeto MAPI é uma classe de objeto C++ ou estrutura de dados C herdada de uma ou mais interfaces MAPI ou coleções de funções relacionadas.</span><span class="sxs-lookup"><span data-stu-id="d1e17-105">A MAPI object is a C++ object class or C data structure inherited from one or more MAPI interfaces, or collections of related functions.</span></span> <span data-ttu-id="d1e17-106">Essas coleções de funções relacionadas são conhecidas por desenvolvedores C++ como funções virtuais puras.</span><span class="sxs-lookup"><span data-stu-id="d1e17-106">These collections of related functions are known to C++ developers as pure virtual functions.</span></span> <span data-ttu-id="d1e17-107">Para uma função virtual pura, MAPI fornece apenas o protótipo de função, não uma implementação.</span><span class="sxs-lookup"><span data-stu-id="d1e17-107">For a pure virtual function, MAPI supplies only the function prototype, not an implementation.</span></span> <span data-ttu-id="d1e17-108">Espera-se que um aplicativo cliente, um provedor de serviços ou MAPI forneça essa implementação criando uma classe de objeto que herda da interface e está em conformidade com as descrições de função da API de Mensagens.</span><span class="sxs-lookup"><span data-stu-id="d1e17-108">It is expected that a client application, a service provider, or MAPI will provide this implementation by creating an object class that inherits from the interface and conforms to the function descriptions of the Messaging API.</span></span> <span data-ttu-id="d1e17-109">Uma interface MAPI só pode ser instariada por meio de uma classe herdada.</span><span class="sxs-lookup"><span data-stu-id="d1e17-109">A MAPI interface can be instantiated only through an inherited class.</span></span>
  
<span data-ttu-id="d1e17-110">Há muitos objetos MAPI diferentes, cada objeto herdado de uma interface que é herdada por fim da interface [IUnknown.](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d1e17-110">There are many different MAPI objects, each object inheriting from an interface that is ultimately inherited from the [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) interface.</span></span> <span data-ttu-id="d1e17-111">**IUnknown** é a interface base do COM (Modelo de Objeto de Componente OLE).</span><span class="sxs-lookup"><span data-stu-id="d1e17-111">**IUnknown** is the OLE Component Object Model (COM) base interface.</span></span> <span data-ttu-id="d1e17-112">Ele fornece objetos MAPI com um mecanismo padrão para comunicação e controle.</span><span class="sxs-lookup"><span data-stu-id="d1e17-112">It provides MAPI objects with a standard mechanism for communication and control.</span></span> <span data-ttu-id="d1e17-113">O COM determina como os implementadores de objeto lidam com problemas como gerenciamento de memória, gerenciamento de parâmetros e multithreading.</span><span class="sxs-lookup"><span data-stu-id="d1e17-113">COM dictates how object implementers handle issues such as memory management, parameter management, and multithreading.</span></span> <span data-ttu-id="d1e17-114">Em conformidade com esse modelo, um implementador de objeto segue um contrato conforme especificado pelas interfaces incluídas no objeto.</span><span class="sxs-lookup"><span data-stu-id="d1e17-114">By conforming to this model, an object implementer adheres to a contract as specified by the interfaces included in the object.</span></span> 
  
<span data-ttu-id="d1e17-115">Muitas interfaces MAPI são herdadas diretamente de **IUnknown**, enquanto outras são herdadas indiretamente por meio de uma de duas outras interfaces base: [IMAPIProp : IUnknown](imapipropiunknown.md) para gerenciamento de propriedade e [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) para acesso à pasta e ao livro de endereços.</span><span class="sxs-lookup"><span data-stu-id="d1e17-115">Many MAPI interfaces are inherited directly from **IUnknown**, while others are inherited indirectly through one of two other base interfaces: [IMAPIProp : IUnknown](imapipropiunknown.md) for property management and [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) for folder and address book access.</span></span> <span data-ttu-id="d1e17-116">As interfaces base nunca são implementadas como objetos separados e autônomos; eles são sempre implementados como parte de outros objetos, objetos que implementam interfaces derivadas.</span><span class="sxs-lookup"><span data-stu-id="d1e17-116">Base interfaces are never implemented as separate, standalone objects; they are always implemented as part of other objects, objects that implement derived interfaces.</span></span> 
  
<span data-ttu-id="d1e17-117">MAPI define muitos tipos de objetos, cada um implementado por um ou mais componentes MAPI.</span><span class="sxs-lookup"><span data-stu-id="d1e17-117">MAPI defines many types of objects, each implemented by one or more MAPI components.</span></span> <span data-ttu-id="d1e17-118">Os objetos implementados pelos clientes são usados por MAPI, por provedores de serviços e por componentes de formulário personalizados.</span><span class="sxs-lookup"><span data-stu-id="d1e17-118">Objects implemented by clients are used by MAPI, by service providers, and by custom form components.</span></span> <span data-ttu-id="d1e17-119">Objetos implementados por provedores de serviços geralmente são usados por MAPI e por clientes.</span><span class="sxs-lookup"><span data-stu-id="d1e17-119">Objects implemented by service providers are typically used by MAPI and by clients.</span></span> <span data-ttu-id="d1e17-120">Objetos implementados por provedores de biblioteca de formulário e servidores de formulário são usados por outros componentes de formulário e por clientes.</span><span class="sxs-lookup"><span data-stu-id="d1e17-120">Objects implemented by form library providers and form servers are used by other form components and by clients.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d1e17-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="d1e17-121">See also</span></span>



[<span data-ttu-id="d1e17-122">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d1e17-122">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="d1e17-123">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="d1e17-123">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="d1e17-124">Conceitos de MAPI</span><span class="sxs-lookup"><span data-stu-id="d1e17-124">MAPI Concepts</span></span>](mapi-concepts.md)

