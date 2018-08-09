---
title: Definir uma posição de tabela com um indicador
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 56ab37f9-5aa6-4e9d-9dc8-b3d95aa19f35
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d53f15cb439494ae99ff45509ed14c0928756d8f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770379"
---
# <a name="setting-a-table-position-with-a-bookmark"></a><span data-ttu-id="dedd6-103">Definir uma posição de tabela com um indicador</span><span class="sxs-lookup"><span data-stu-id="dedd6-103">Setting a Table Position with a Bookmark</span></span>

  
  
<span data-ttu-id="dedd6-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dedd6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dedd6-105">Um indicador é um recurso que indica uma localidade específica em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="dedd6-105">A bookmark is a resource that indicates a particular location in a table.</span></span> <span data-ttu-id="dedd6-106">A definição de um indicador torna possível retornar para uma posição em um momento posterior, um recurso que pode melhorar significativamente o desempenho das operações de tabela.</span><span class="sxs-lookup"><span data-stu-id="dedd6-106">Setting a bookmark makes it possible to return to a position at a later time, a feature that can significantly improve the performance of table operations.</span></span> <span data-ttu-id="dedd6-107">MAPI define três indicadores padrão:</span><span class="sxs-lookup"><span data-stu-id="dedd6-107">MAPI defines three standard bookmarks:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dedd6-108">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="dedd6-108">BOOKMARK_CURRENT</span></span>  <br/> |<span data-ttu-id="dedd6-109">Aponta para a linha atual em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="dedd6-109">Points to the current row in a table.</span></span>  <br/> |
|<span data-ttu-id="dedd6-110">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="dedd6-110">BOOKMARK_BEGINNING</span></span>  <br/> |<span data-ttu-id="dedd6-111">Aponta para a primeira linha em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="dedd6-111">Points to the first row in a table.</span></span>  <br/> |
|<span data-ttu-id="dedd6-112">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="dedd6-112">BOOKMARK_END</span></span>  <br/> |<span data-ttu-id="dedd6-113">Aponta para a última linha em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="dedd6-113">Points to the last row in a table.</span></span>  <br/> |
   
<span data-ttu-id="dedd6-114">Implementadores de tabela são necessárias para dar suporte a esses indicadores standard e também podem suportar a outras pessoas.</span><span class="sxs-lookup"><span data-stu-id="dedd6-114">Table implementers are required to support these standard bookmarks and can also support others.</span></span> <span data-ttu-id="dedd6-115">No entanto, como indicadores são recursos e os recursos são limitados, os usuários do indicador devem liberá-los assim que possível.</span><span class="sxs-lookup"><span data-stu-id="dedd6-115">However, because bookmarks are resources and resources are limited, bookmark users should free them as soon as possible.</span></span> 
  
 <span data-ttu-id="dedd6-116">**Para definir um indicador na posição de tabela atual**</span><span class="sxs-lookup"><span data-stu-id="dedd6-116">**To set a bookmark at the current table position**</span></span>
  
- <span data-ttu-id="dedd6-117">Chame [IMAPITable::CreateBookmark](imapitable-createbookmark.md).</span><span class="sxs-lookup"><span data-stu-id="dedd6-117">Call [IMAPITable::CreateBookmark](imapitable-createbookmark.md).</span></span> <span data-ttu-id="dedd6-118">Ocasionalmente, haverá memória suficiente disponível para alocar no novo indicador, causando **CreateBookmark** retornar o valor de erro MAPI_E_UNABLE_TO_COMPLETE.</span><span class="sxs-lookup"><span data-stu-id="dedd6-118">Occasionally there will be insufficient memory available to allocate the new bookmark, causing **CreateBookmark** to return the MAPI_E_UNABLE_TO_COMPLETE error value.</span></span> 
    
 <span data-ttu-id="dedd6-119">**Para liberar um indicador**</span><span class="sxs-lookup"><span data-stu-id="dedd6-119">**To free a bookmark**</span></span>
  
- <span data-ttu-id="dedd6-120">Chame [IMAPITable::FreeBookmark](imapitable-freebookmark.md).</span><span class="sxs-lookup"><span data-stu-id="dedd6-120">Call [IMAPITable::FreeBookmark](imapitable-freebookmark.md).</span></span>
    
 <span data-ttu-id="dedd6-121">**Para mover o cursor para uma posição com indicador**</span><span class="sxs-lookup"><span data-stu-id="dedd6-121">**To move the cursor to a bookmarked position**</span></span>
  
- <span data-ttu-id="dedd6-122">Chame [IMAPITable::SeekRow](imapitable-seekrow.md).</span><span class="sxs-lookup"><span data-stu-id="dedd6-122">Call [IMAPITable::SeekRow](imapitable-seekrow.md).</span></span> <span data-ttu-id="dedd6-123">**SeekRow** estabelece um novo valor para a posição de BOOKMARK_CURRENT.</span><span class="sxs-lookup"><span data-stu-id="dedd6-123">**SeekRow** establishes a new value for the BOOKMARK_CURRENT position.</span></span> <span data-ttu-id="dedd6-124">**SeekRow** pode ser usado, por exemplo, para posicionar um linhas da tabela dez da posição atual ou para começar novamente no início.</span><span class="sxs-lookup"><span data-stu-id="dedd6-124">**SeekRow** can be used, for example, to position a table ten rows from the current position or to start over at the beginning.</span></span> <span data-ttu-id="dedd6-125">Provedores de serviço ou clientes seek à data atual, começando, ou terminar de uma tabela ou qualquer outra posição que é associada a um indicador predefinido.</span><span class="sxs-lookup"><span data-stu-id="dedd6-125">Clients or service providers can seek to the current, beginning, or end of a table, or any other position that is associated with a predefined bookmark.</span></span> <span data-ttu-id="dedd6-126">Eles podem mover em um limite a operação e direção de frente ou para trás até um número especificado de linhas.</span><span class="sxs-lookup"><span data-stu-id="dedd6-126">They can move in either a forward or backward direction and limit the operation to a specified number of rows.</span></span> <span data-ttu-id="dedd6-127">Como regra, os chamadores devem buscar por meio de não mais de 50 linhas com **SeekRow**; [IMAPITable:: SeekRowApprox](imapitable-seekrowapprox.md) deve ser usado com um número maior de linhas.</span><span class="sxs-lookup"><span data-stu-id="dedd6-127">As a rule, callers should seek through no more than 50 rows with **SeekRow**; [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) should be used with larger numbers of rows.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="dedd6-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="dedd6-128">See also</span></span>



[<span data-ttu-id="dedd6-129">Tabelas MAPI</span><span class="sxs-lookup"><span data-stu-id="dedd6-129">MAPI Tables</span></span>](mapi-tables.md)

