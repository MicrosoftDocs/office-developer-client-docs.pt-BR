---
title: Gerenciando memória nos MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9eee6925-ab91-413e-8907-c747ab4a4bb5
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5859d94f85ca3fe7a0c738ed596d3c1a11fb2e8d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767785"
---
# <a name="managing-memory-in-mapi"></a><span data-ttu-id="8cbf0-103">Gerenciando memória nos MAPI</span><span class="sxs-lookup"><span data-stu-id="8cbf0-103">Managing Memory in MAPI</span></span>

  
  
<span data-ttu-id="8cbf0-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8cbf0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8cbf0-105">Saber como e quando alocar e liberar memória é uma parte importante da programação com MAPI.</span><span class="sxs-lookup"><span data-stu-id="8cbf0-105">Knowing how and when to allocate and free memory is an important part of programming with MAPI.</span></span> <span data-ttu-id="8cbf0-106">MAPI fornece funções e macros que seu provedor de cliente ou serviço pode usar para gerenciar memória de maneira consistente.</span><span class="sxs-lookup"><span data-stu-id="8cbf0-106">MAPI provides both functions and macros that your client or service provider can use to manage memory in a consistent way.</span></span> <span data-ttu-id="8cbf0-107">As três funções são:</span><span class="sxs-lookup"><span data-stu-id="8cbf0-107">The three functions are as follows:</span></span>
  
[<span data-ttu-id="8cbf0-108">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="8cbf0-108">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="8cbf0-109">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="8cbf0-109">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="8cbf0-110">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="8cbf0-110">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
<span data-ttu-id="8cbf0-111">Quando os clientes e provedores de serviços usam essas funções, o problema de "responsável" — ou seja, sabe como liberar — um bloco de memória particular foram eliminado.</span><span class="sxs-lookup"><span data-stu-id="8cbf0-111">When clients and service providers use these functions, the issue of who "owns" — that is, knows how to release — a particular block of memory is eliminated.</span></span> <span data-ttu-id="8cbf0-112">Um cliente chamar um método de provedor de serviço não precisa passar um grande o suficiente para armazenar um valor de retorno de qualquer tamanho do buffer.</span><span class="sxs-lookup"><span data-stu-id="8cbf0-112">A client calling a service provider method need not pass a buffer large enough to hold a return value of any size.</span></span> <span data-ttu-id="8cbf0-113">O provedor de serviços pode simplesmente alocar a quantidade apropriada de memória usando **MAPIAllocateBuffer** e, se necessário, **MAPIAllocateMore**e o cliente podem posteriormente liberá-la à vontade usando **MAPIFreeBuffer**, independente do serviço provedor.</span><span class="sxs-lookup"><span data-stu-id="8cbf0-113">The service provider can simply allocate the appropriate amount of memory using **MAPIAllocateBuffer** and, if necessary, **MAPIAllocateMore**, and the client can later release it at will using **MAPIFreeBuffer**, independent of the service provider.</span></span> 
  
<span data-ttu-id="8cbf0-114">As macros de memória são usadas para alocar estruturas ou matrizes de estruturas de um determinado tamanho.</span><span class="sxs-lookup"><span data-stu-id="8cbf0-114">The memory macros are used to allocate structures or arrays of structures of a specific size.</span></span> <span data-ttu-id="8cbf0-115">Provedores de serviços e clientes devem usar estas macros em vez de alocar a memória manualmente.</span><span class="sxs-lookup"><span data-stu-id="8cbf0-115">Clients and service providers should use these macros rather than allocate the memory manually.</span></span> <span data-ttu-id="8cbf0-116">Por exemplo, se um cliente precisar realizar a resolução de nomes de processamento em uma lista de destinatários com três entradas, a macro de **SizedADRLIST** pode ser usada para criar uma estrutura **ADRLIST** a serem passados para **IAddrBook::ResolveName** com o número correto de Membros do **ADRENTRY** .</span><span class="sxs-lookup"><span data-stu-id="8cbf0-116">For example, if a client needs to perform name resolution processing on a recipient list with three entries, the **SizedADRLIST** macro can be used to create an **ADRLIST** structure to pass to **IAddrBook::ResolveName** with the correct number of **ADRENTRY** members.</span></span> <span data-ttu-id="8cbf0-117">Todas as macros de memória são definidas no MAPIDEFS. Arquivo de cabeçalho H.</span><span class="sxs-lookup"><span data-stu-id="8cbf0-117">All of the memory macros are defined in the MAPIDEFS.H header file.</span></span> <span data-ttu-id="8cbf0-118">Estas macros são:</span><span class="sxs-lookup"><span data-stu-id="8cbf0-118">These macros are:</span></span> 
  
|||
|:-----|:-----|
|[<span data-ttu-id="8cbf0-119">SizedADRLIST</span><span class="sxs-lookup"><span data-stu-id="8cbf0-119">SizedADRLIST</span></span>](sizedadrlist.md) <br/> |[<span data-ttu-id="8cbf0-120">SizedDtblPage</span><span class="sxs-lookup"><span data-stu-id="8cbf0-120">SizedDtblPage</span></span>](sizeddtblpage.md) <br/> |
|[<span data-ttu-id="8cbf0-121">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="8cbf0-121">SizedDtblButton</span></span>](sizeddtblbutton.md) <br/> |[<span data-ttu-id="8cbf0-122">SizedENTRYID</span><span class="sxs-lookup"><span data-stu-id="8cbf0-122">SizedENTRYID</span></span>](sizedentryid.md) <br/> |
|[<span data-ttu-id="8cbf0-123">SizedDtblCheckBox</span><span class="sxs-lookup"><span data-stu-id="8cbf0-123">SizedDtblCheckBox</span></span>](sizeddtblcheckbox.md) <br/> |[<span data-ttu-id="8cbf0-124">SizedSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="8cbf0-124">SizedSPropProblemArray</span></span>](sizedspropproblemarray.md) <br/> |
|[<span data-ttu-id="8cbf0-125">SizedDtblComboBox</span><span class="sxs-lookup"><span data-stu-id="8cbf0-125">SizedDtblComboBox</span></span>](sizeddtblcombobox.md) <br/> |[<span data-ttu-id="8cbf0-126">SizedSPropTagArray</span><span class="sxs-lookup"><span data-stu-id="8cbf0-126">SizedSPropTagArray</span></span>](sizedsproptagarray.md) <br/> |
|[<span data-ttu-id="8cbf0-127">SizedDtblEdit</span><span class="sxs-lookup"><span data-stu-id="8cbf0-127">SizedDtblEdit</span></span>](sizeddtbledit.md) <br/> |[<span data-ttu-id="8cbf0-128">SizedSRowSet</span><span class="sxs-lookup"><span data-stu-id="8cbf0-128">SizedSRowSet</span></span>](sizedsrowset.md) <br/> |
|[<span data-ttu-id="8cbf0-129">SizedDtblGroupBox</span><span class="sxs-lookup"><span data-stu-id="8cbf0-129">SizedDtblGroupBox</span></span>](sizeddtblgroupbox.md) <br/> |[<span data-ttu-id="8cbf0-130">SizedSSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="8cbf0-130">SizedSSortOrderSet</span></span>](sizedssortorderset.md) <br/> |
|[<span data-ttu-id="8cbf0-131">SizedDtblLabel</span><span class="sxs-lookup"><span data-stu-id="8cbf0-131">SizedDtblLabel</span></span>](sizeddtbllabel.md) <br/> | <br/> |
   
<span data-ttu-id="8cbf0-132">MAPI também suporta o uso da interface COM [IMalloc](http://msdn.microsoft.com/en-us/library/ms678425%28VS.85%29.aspx) para gerenciamento de memória.</span><span class="sxs-lookup"><span data-stu-id="8cbf0-132">MAPI also supports the use of the COM interface [IMalloc](http://msdn.microsoft.com/en-us/library/ms678425%28VS.85%29.aspx) for memory management.</span></span> <span data-ttu-id="8cbf0-133">Provedores de serviço recebem um ponteiro de interface **IMalloc** por MAPI em tempo de inicialização e também podem recuperar um por meio da função [MAPIGetDefaultMalloc](mapigetdefaultmalloc.md) .</span><span class="sxs-lookup"><span data-stu-id="8cbf0-133">Service providers are given an **IMalloc** interface pointer by MAPI at initialization time and can also retrieve one through the [MAPIGetDefaultMalloc](mapigetdefaultmalloc.md) function.</span></span> <span data-ttu-id="8cbf0-134">A principal vantagem de usar os métodos **IMalloc** para gerenciar memória sobre as funções MAPI é que com os métodos COM é possível realocar um buffer existente.</span><span class="sxs-lookup"><span data-stu-id="8cbf0-134">The main advantage to using the **IMalloc** methods for managing memory over the MAPI functions is that with the COM methods it is possible to reallocate an existing buffer.</span></span> <span data-ttu-id="8cbf0-135">As funções de memória MAPI não dão suporte a realocação.</span><span class="sxs-lookup"><span data-stu-id="8cbf0-135">The MAPI memory functions do not support reallocation.</span></span> 
  

