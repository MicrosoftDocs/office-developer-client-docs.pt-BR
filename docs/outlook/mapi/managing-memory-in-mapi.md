---
title: Gerenciando memória em MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9eee6925-ab91-413e-8907-c747ab4a4bb5
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 66489c09be641d8fe9ae5f3ffff46a6d5004f473
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32298093"
---
# <a name="managing-memory-in-mapi"></a><span data-ttu-id="9654a-103">Gerenciando memória no MAPI</span><span class="sxs-lookup"><span data-stu-id="9654a-103">Managing Memory in MAPI</span></span>

  
  
<span data-ttu-id="9654a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9654a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9654a-105">Saber como e quando alocar e liberar memória é uma parte importante da programação com MAPI.</span><span class="sxs-lookup"><span data-stu-id="9654a-105">Knowing how and when to allocate and free memory is an important part of programming with MAPI.</span></span> <span data-ttu-id="9654a-106">MAPI provides both functions and macros that your client or service provider can use to manage memory in a consistent way.</span><span class="sxs-lookup"><span data-stu-id="9654a-106">MAPI provides both functions and macros that your client or service provider can use to manage memory in a consistent way.</span></span> <span data-ttu-id="9654a-107">As três funções são as seguinte:</span><span class="sxs-lookup"><span data-stu-id="9654a-107">The three functions are as follows:</span></span>
  
[<span data-ttu-id="9654a-108">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="9654a-108">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="9654a-109">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="9654a-109">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="9654a-110">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="9654a-110">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
<span data-ttu-id="9654a-111">Quando os clientes e provedores de serviços usam essas funções, o problema de quem "possui" — ou seja, sabe como liberar — um determinado bloco de memória é eliminado.</span><span class="sxs-lookup"><span data-stu-id="9654a-111">When clients and service providers use these functions, the issue of who "owns" — that is, knows how to release — a particular block of memory is eliminated.</span></span> <span data-ttu-id="9654a-112">Um cliente que chama um método de provedor de serviços não precisa passar um buffer grande o suficiente para manter um valor de retorno de qualquer tamanho.</span><span class="sxs-lookup"><span data-stu-id="9654a-112">A client calling a service provider method need not pass a buffer large enough to hold a return value of any size.</span></span> <span data-ttu-id="9654a-113">O provedor de serviços pode simplesmente alocar a quantidade adequada de memória usando **MAPIAllocateBuffer** e, se necessário, **MAPIAllocateMore**, e o cliente pode liberá-lo posteriormente usando **MAPIFreeBuffer**, independentemente do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="9654a-113">The service provider can simply allocate the appropriate amount of memory using **MAPIAllocateBuffer** and, if necessary, **MAPIAllocateMore**, and the client can later release it at will using **MAPIFreeBuffer**, independent of the service provider.</span></span> 
  
<span data-ttu-id="9654a-114">As macros de memória são usadas para alocar estruturas ou matrizes de estruturas de um tamanho específico.</span><span class="sxs-lookup"><span data-stu-id="9654a-114">The memory macros are used to allocate structures or arrays of structures of a specific size.</span></span> <span data-ttu-id="9654a-115">Os clientes e provedores de serviços devem usar essas macros em vez de alocar a memória manualmente.</span><span class="sxs-lookup"><span data-stu-id="9654a-115">Clients and service providers should use these macros rather than allocate the memory manually.</span></span> <span data-ttu-id="9654a-116">Por exemplo, se um cliente precisar executar o processamento de resolução de nomes em uma lista de destinatários com três entradas, a macro **SizedADRLIST** poderá ser usada para criar uma estrutura **ADRLIST** para passar para **IAddrBook::ResolveName** com o número correto de membros **ADRENTRY.**</span><span class="sxs-lookup"><span data-stu-id="9654a-116">For example, if a client needs to perform name resolution processing on a recipient list with three entries, the **SizedADRLIST** macro can be used to create an **ADRLIST** structure to pass to **IAddrBook::ResolveName** with the correct number of **ADRENTRY** members.</span></span> <span data-ttu-id="9654a-117">Todas as macros de memória são definidas em MAPIDEFS. Arquivo de header H.</span><span class="sxs-lookup"><span data-stu-id="9654a-117">All of the memory macros are defined in the MAPIDEFS.H header file.</span></span> <span data-ttu-id="9654a-118">Essas macros são:</span><span class="sxs-lookup"><span data-stu-id="9654a-118">These macros are:</span></span> 
  
|||
|:-----|:-----|
|[<span data-ttu-id="9654a-119">SizedADRLIST</span><span class="sxs-lookup"><span data-stu-id="9654a-119">SizedADRLIST</span></span>](sizedadrlist.md) <br/> |[<span data-ttu-id="9654a-120">SizedDtblPage</span><span class="sxs-lookup"><span data-stu-id="9654a-120">SizedDtblPage</span></span>](sizeddtblpage.md) <br/> |
|[<span data-ttu-id="9654a-121">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="9654a-121">SizedDtblButton</span></span>](sizeddtblbutton.md) <br/> |[<span data-ttu-id="9654a-122">SizedENTRYID</span><span class="sxs-lookup"><span data-stu-id="9654a-122">SizedENTRYID</span></span>](sizedentryid.md) <br/> |
|[<span data-ttu-id="9654a-123">SizedDtblCheckBox</span><span class="sxs-lookup"><span data-stu-id="9654a-123">SizedDtblCheckBox</span></span>](sizeddtblcheckbox.md) <br/> |[<span data-ttu-id="9654a-124">SizedSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="9654a-124">SizedSPropProblemArray</span></span>](sizedspropproblemarray.md) <br/> |
|[<span data-ttu-id="9654a-125">SizedDtblComboBox</span><span class="sxs-lookup"><span data-stu-id="9654a-125">SizedDtblComboBox</span></span>](sizeddtblcombobox.md) <br/> |[<span data-ttu-id="9654a-126">SizedSPropTagArray</span><span class="sxs-lookup"><span data-stu-id="9654a-126">SizedSPropTagArray</span></span>](sizedsproptagarray.md) <br/> |
|[<span data-ttu-id="9654a-127">SizedDtblEdit</span><span class="sxs-lookup"><span data-stu-id="9654a-127">SizedDtblEdit</span></span>](sizeddtbledit.md) <br/> |[<span data-ttu-id="9654a-128">SizedSRowSet</span><span class="sxs-lookup"><span data-stu-id="9654a-128">SizedSRowSet</span></span>](sizedsrowset.md) <br/> |
|[<span data-ttu-id="9654a-129">SizedDtblGroupBox</span><span class="sxs-lookup"><span data-stu-id="9654a-129">SizedDtblGroupBox</span></span>](sizeddtblgroupbox.md) <br/> |[<span data-ttu-id="9654a-130">SizedSSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="9654a-130">SizedSSortOrderSet</span></span>](sizedssortorderset.md) <br/> |
|[<span data-ttu-id="9654a-131">SizedDtblLabel</span><span class="sxs-lookup"><span data-stu-id="9654a-131">SizedDtblLabel</span></span>](sizeddtbllabel.md) <br/> | <br/> |
   
<span data-ttu-id="9654a-132">MAPI also supports the use of the COM interface [IMalloc](https://msdn.microsoft.com/library/ms678425%28VS.85%29.aspx) for memory management.</span><span class="sxs-lookup"><span data-stu-id="9654a-132">MAPI also supports the use of the COM interface [IMalloc](https://msdn.microsoft.com/library/ms678425%28VS.85%29.aspx) for memory management.</span></span> <span data-ttu-id="9654a-133">Os provedores de serviços receberão um ponteiro de interface **IMalloc** por MAPI no momento da inicialização e também podem recuperar um por meio da função [MAPIGetDefaultMalloc.](mapigetdefaultmalloc.md)</span><span class="sxs-lookup"><span data-stu-id="9654a-133">Service providers are given an **IMalloc** interface pointer by MAPI at initialization time and can also retrieve one through the [MAPIGetDefaultMalloc](mapigetdefaultmalloc.md) function.</span></span> <span data-ttu-id="9654a-134">A principal vantagem de usar os métodos **IMalloc** para gerenciar memória sobre as funções MAPI é que, com os métodos COM, é possível realocar um buffer existente.</span><span class="sxs-lookup"><span data-stu-id="9654a-134">The main advantage to using the **IMalloc** methods for managing memory over the MAPI functions is that with the COM methods it is possible to reallocate an existing buffer.</span></span> <span data-ttu-id="9654a-135">As funções de memória MAPI não suportam realocação.</span><span class="sxs-lookup"><span data-stu-id="9654a-135">The MAPI memory functions do not support reallocation.</span></span> 
  

