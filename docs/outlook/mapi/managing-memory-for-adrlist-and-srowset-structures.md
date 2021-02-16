---
title: Gerenciar memória das estruturas ADRLIST e SRowSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d009f6b6-d151-4d52-b7cc-a15127142354
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a5636cad7cad23bb5114bdbd34aff48c3639773b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407862"
---
# <a name="managing-memory-for-adrlist-and-srowset-structures"></a><span data-ttu-id="6c6db-103">Gerenciando memória para estruturas ADRLIST e SRowSet"</span><span class="sxs-lookup"><span data-stu-id="6c6db-103">Managing memory for ADRLIST and SRowSet structures"</span></span>

<span data-ttu-id="6c6db-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c6db-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c6db-105">O requisito de alocar toda a memória para um buffer sempre que possível com uma única chamada **MAPIAllocateBuffer** não se aplica ao usar a lista de endereços, ou **ADRLIST** e conjunto de linhas, ou **SRowSet**, estruturas.</span><span class="sxs-lookup"><span data-stu-id="6c6db-105">The requirement to allocate all memory for a buffer whenever possible with a single **MAPIAllocateBuffer** call does not apply when using the address list, or **ADRLIST**, and row set, or **SRowSet**, structures.</span></span> 
  
<span data-ttu-id="6c6db-106">Essas duas estruturas são exceções às regras padrão para alocar e liberar memória.</span><span class="sxs-lookup"><span data-stu-id="6c6db-106">These two structures are exceptions to the standard rules for allocating and releasing memory.</span></span> <span data-ttu-id="6c6db-107">Eles contêm vários níveis de estruturas e são projetados para permitir que membros individuais sejam adicionados ou removidos.</span><span class="sxs-lookup"><span data-stu-id="6c6db-107">They contain multiple levels of structures and are designed to enable individual members to be added or removed.</span></span> <span data-ttu-id="6c6db-108">Portanto, cada propriedade deve ser uma alocação separada.</span><span class="sxs-lookup"><span data-stu-id="6c6db-108">Therefore, each property must be a separate allocation.</span></span> 

<span data-ttu-id="6c6db-109">Onde a maioria das estruturas são liberadas com uma chamada para **MAPIFreeBuffer**, cada entrada individual em uma **estrutura ADRLIST** ou **SRowSet** deve ser liberada com sua própria chamada para **MAPIFreeBuffer** ou uma única chamada para **FreeProws** ou **FreePadrlist**.</span><span class="sxs-lookup"><span data-stu-id="6c6db-109">Where most structures are freed with one call to **MAPIFreeBuffer**, each individual entry in an **ADRLIST** or **SRowSet** structure must be freed with its own call to **MAPIFreeBuffer** or a single call to either **FreeProws** or **FreePadrlist**.</span></span> <span data-ttu-id="6c6db-110">Para obter mais informações, [consulte MAPIFreeBuffer](mapifreebuffer.md), [ADRLIST](adrlist.md)e [SRowSet](srowset.md).</span><span class="sxs-lookup"><span data-stu-id="6c6db-110">For more information, see [MAPIFreeBuffer](mapifreebuffer.md), [ADRLIST](adrlist.md), and [SRowSet](srowset.md).</span></span> 

<span data-ttu-id="6c6db-111">**FreeProws** e **FreePadrlist** são funções fornecidas pelo MAPI para simplificar a liberação dessas estruturas de dados.</span><span class="sxs-lookup"><span data-stu-id="6c6db-111">**FreeProws** and **FreePadrlist** are functions provided by MAPI for simplifying the freeing of these data structures.</span></span> <span data-ttu-id="6c6db-112">Para obter mais informações, [consulte FreeProws](freeprows.md) e [FreePadrlist](freepadrlist.md).</span><span class="sxs-lookup"><span data-stu-id="6c6db-112">For more information, see [FreeProws](freeprows.md) and [FreePadrlist](freepadrlist.md).</span></span> <span data-ttu-id="6c6db-113">**FreePadrlist** libera a memória para a estrutura **ADRLIST,** além de toda a memória associada para os membros da estrutura; **FreeProws** faz o mesmo para a **estrutura SRowSet.**</span><span class="sxs-lookup"><span data-stu-id="6c6db-113">**FreePadrlist** frees the memory for the **ADRLIST** structure plus all associated memory for the structure members; **FreeProws** does the same for the **SRowSet** structure.</span></span> 
  
<span data-ttu-id="6c6db-114">O diagrama a seguir mostra o layout de uma estrutura de dados **ADRLIST,** indicando as alocações de memória separadas necessárias.</span><span class="sxs-lookup"><span data-stu-id="6c6db-114">The following diagram shows the layout of an **ADRLIST** data structure, indicating the separate memory allocations required.</span></span> <span data-ttu-id="6c6db-115">As caixas cinza mostram a memória que pode ser alocada e liberada com uma chamada.</span><span class="sxs-lookup"><span data-stu-id="6c6db-115">The gray boxes show memory that can be allocated and released with one call.</span></span> 
  
<span data-ttu-id="6c6db-116">**ADRLIST memory allocation**</span><span class="sxs-lookup"><span data-stu-id="6c6db-116">**ADRLIST memory allocation**</span></span>
  
<span data-ttu-id="6c6db-117">![Alocação de memória ADRLIST](media/amapi_52.gif "da ADRLIST")</span><span class="sxs-lookup"><span data-stu-id="6c6db-117">![ADRLIST memory allocation](media/amapi_52.gif "ADRLIST memory allocation")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6c6db-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="6c6db-118">See also</span></span>

- [<span data-ttu-id="6c6db-119">Gerenciando memória no MAPI</span><span class="sxs-lookup"><span data-stu-id="6c6db-119">Managing Memory in MAPI</span></span>](managing-memory-in-mapi.md)

