---
title: Gerenciamento de memória para as estruturas ADRLIST e SRowSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d009f6b6-d151-4d52-b7cc-a15127142354
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: ef20cf8460aa7d3d160208109e42b2de66658d54
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589725"
---
# <a name="managing-memory-for-adrlist-and-srowset-structures"></a><span data-ttu-id="7b8dc-103">Gerenciando a memória para as estruturas ADRLIST e SRowSet"</span><span class="sxs-lookup"><span data-stu-id="7b8dc-103">Managing memory for ADRLIST and SRowSet structures"</span></span>

<span data-ttu-id="7b8dc-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7b8dc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7b8dc-105">O requisito de alocar memória todos para um buffer sempre que possível, com uma única chamada **MAPIAllocateBuffer** não se aplica ao usar a lista de endereços ou estruturas **ADRLIST**e **SRowSet**ou conjunto de linhas.</span><span class="sxs-lookup"><span data-stu-id="7b8dc-105">The requirement to allocate all memory for a buffer whenever possible with a single **MAPIAllocateBuffer** call does not apply when using the address list, or **ADRLIST**, and row set, or **SRowSet**, structures.</span></span> 
  
<span data-ttu-id="7b8dc-106">Essas duas estruturas são exceções às regras padrão de alocação e da liberação de memória.</span><span class="sxs-lookup"><span data-stu-id="7b8dc-106">These two structures are exceptions to the standard rules for allocating and releasing memory.</span></span> <span data-ttu-id="7b8dc-107">Elas contêm vários níveis de estruturas e são projetadas para permitir que membros individuais sejam adicionadas ou removidas.</span><span class="sxs-lookup"><span data-stu-id="7b8dc-107">They contain multiple levels of structures and are designed to enable individual members to be added or removed.</span></span> <span data-ttu-id="7b8dc-108">Portanto, cada propriedade deve ser uma alocação separada.</span><span class="sxs-lookup"><span data-stu-id="7b8dc-108">Therefore, each property must be a separate allocation.</span></span> 

<span data-ttu-id="7b8dc-109">Onde a maioria das estruturas são liberadas com uma chamada de **MAPIFreeBuffer**, cada entrada individual em uma estrutura **ADRLIST** ou **SRowSet** devem ser liberada com sua própria chamada para **MAPIFreeBuffer** ou uma única chamada para **FreeProws** ou ** FreePadrlist**.</span><span class="sxs-lookup"><span data-stu-id="7b8dc-109">Where most structures are freed with one call to **MAPIFreeBuffer**, each individual entry in an **ADRLIST** or **SRowSet** structure must be freed with its own call to **MAPIFreeBuffer** or a single call to either **FreeProws** or **FreePadrlist**.</span></span> <span data-ttu-id="7b8dc-110">Para obter mais informações, consulte [MAPIFreeBuffer](mapifreebuffer.md), [ADRLIST](adrlist.md)e [SRowSet](srowset.md).</span><span class="sxs-lookup"><span data-stu-id="7b8dc-110">For more information, see [MAPIFreeBuffer](mapifreebuffer.md), [ADRLIST](adrlist.md), and [SRowSet](srowset.md).</span></span> 

<span data-ttu-id="7b8dc-111">**FreeProws** e **FreePadrlist** são funções fornecidas pelo MAPI para simplificar o dispensando dessas estruturas de dados.</span><span class="sxs-lookup"><span data-stu-id="7b8dc-111">**FreeProws** and **FreePadrlist** are functions provided by MAPI for simplifying the freeing of these data structures.</span></span> <span data-ttu-id="7b8dc-112">Para obter mais informações, consulte [FreeProws](freeprows.md) e [FreePadrlist](freepadrlist.md).</span><span class="sxs-lookup"><span data-stu-id="7b8dc-112">For more information, see [FreeProws](freeprows.md) and [FreePadrlist](freepadrlist.md).</span></span> <span data-ttu-id="7b8dc-113">**FreePadrlist** libera a memória para a estrutura **ADRLIST** plus todos os respectivos memória para os membros de estrutura; **FreeProws** faz o mesmo para a estrutura **SRowSet** .</span><span class="sxs-lookup"><span data-stu-id="7b8dc-113">**FreePadrlist** frees the memory for the **ADRLIST** structure plus all associated memory for the structure members; **FreeProws** does the same for the **SRowSet** structure.</span></span> 
  
<span data-ttu-id="7b8dc-114">O diagrama a seguir mostra o layout de uma estrutura de dados **ADRLIST** , indicando as alocações de memória separado necessárias.</span><span class="sxs-lookup"><span data-stu-id="7b8dc-114">The following diagram shows the layout of an **ADRLIST** data structure, indicating the separate memory allocations required.</span></span> <span data-ttu-id="7b8dc-115">As caixas cinzas mostram a memória que pode ser alocada e lançada com uma chamada.</span><span class="sxs-lookup"><span data-stu-id="7b8dc-115">The gray boxes show memory that can be allocated and released with one call.</span></span> 
  
<span data-ttu-id="7b8dc-116">**ADRLIST memory allocation**</span><span class="sxs-lookup"><span data-stu-id="7b8dc-116">**ADRLIST memory allocation**</span></span>
  
<span data-ttu-id="7b8dc-117">![Alocação de memória ADRLIST] (media/amapi_52.gif "Alocação de memória ADRLIST")</span><span class="sxs-lookup"><span data-stu-id="7b8dc-117">![ADRLIST memory allocation](media/amapi_52.gif "ADRLIST memory allocation")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7b8dc-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="7b8dc-118">See also</span></span>

- [<span data-ttu-id="7b8dc-119">Gerenciando memória nos MAPI</span><span class="sxs-lookup"><span data-stu-id="7b8dc-119">Managing Memory in MAPI</span></span>](managing-memory-in-mapi.md)

