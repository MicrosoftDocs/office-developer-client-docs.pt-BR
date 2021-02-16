---
title: Definindo uma posição de tabela com um indicador
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 56ab37f9-5aa6-4e9d-9dc8-b3d95aa19f35
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f0b041cecca92c0ced32631c67c72fcafdab2a16
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422457"
---
# <a name="setting-a-table-position-with-a-bookmark"></a><span data-ttu-id="44f4e-103">Definindo uma posição de tabela com um indicador</span><span class="sxs-lookup"><span data-stu-id="44f4e-103">Setting a Table Position with a Bookmark</span></span>

  
  
<span data-ttu-id="44f4e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="44f4e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="44f4e-105">Um indicador é um recurso que indica um local específico em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="44f4e-105">A bookmark is a resource that indicates a particular location in a table.</span></span> <span data-ttu-id="44f4e-106">A definição de um indicador possibilita retornar a uma posição posteriormente, um recurso que pode melhorar significativamente o desempenho das operações de tabela.</span><span class="sxs-lookup"><span data-stu-id="44f4e-106">Setting a bookmark makes it possible to return to a position at a later time, a feature that can significantly improve the performance of table operations.</span></span> <span data-ttu-id="44f4e-107">O MAPI define três indicadores padrão:</span><span class="sxs-lookup"><span data-stu-id="44f4e-107">MAPI defines three standard bookmarks:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="44f4e-108">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="44f4e-108">BOOKMARK_CURRENT</span></span>  <br/> |<span data-ttu-id="44f4e-109">Aponta para a linha atual em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="44f4e-109">Points to the current row in a table.</span></span>  <br/> |
|<span data-ttu-id="44f4e-110">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="44f4e-110">BOOKMARK_BEGINNING</span></span>  <br/> |<span data-ttu-id="44f4e-111">Aponta para a primeira linha em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="44f4e-111">Points to the first row in a table.</span></span>  <br/> |
|<span data-ttu-id="44f4e-112">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="44f4e-112">BOOKMARK_END</span></span>  <br/> |<span data-ttu-id="44f4e-113">Aponta para a última linha em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="44f4e-113">Points to the last row in a table.</span></span>  <br/> |
   
<span data-ttu-id="44f4e-114">Implementadores de tabela são necessários para dar suporte a esses indicadores padrão e também podem dar suporte a outros.</span><span class="sxs-lookup"><span data-stu-id="44f4e-114">Table implementers are required to support these standard bookmarks and can also support others.</span></span> <span data-ttu-id="44f4e-115">No entanto, como os indicadores são recursos e recursos são limitados, os usuários de indicadores devem libera-los assim que possível.</span><span class="sxs-lookup"><span data-stu-id="44f4e-115">However, because bookmarks are resources and resources are limited, bookmark users should free them as soon as possible.</span></span> 
  
 <span data-ttu-id="44f4e-116">**Para definir um indicador na posição atual da tabela**</span><span class="sxs-lookup"><span data-stu-id="44f4e-116">**To set a bookmark at the current table position**</span></span>
  
- <span data-ttu-id="44f4e-117">Chame [IMAPITable::CreateBookmark](imapitable-createbookmark.md).</span><span class="sxs-lookup"><span data-stu-id="44f4e-117">Call [IMAPITable::CreateBookmark](imapitable-createbookmark.md).</span></span> <span data-ttu-id="44f4e-118">Ocasionalmente, haverá memória insuficiente disponível para alocar o novo indicador, fazendo com que **CreateBookmark** retorne o valor MAPI_E_UNABLE_TO_COMPLETE erro.</span><span class="sxs-lookup"><span data-stu-id="44f4e-118">Occasionally there will be insufficient memory available to allocate the new bookmark, causing **CreateBookmark** to return the MAPI_E_UNABLE_TO_COMPLETE error value.</span></span> 
    
 <span data-ttu-id="44f4e-119">**Para liberar um indicador**</span><span class="sxs-lookup"><span data-stu-id="44f4e-119">**To free a bookmark**</span></span>
  
- <span data-ttu-id="44f4e-120">Chame [IMAPITable::FreeBookmark](imapitable-freebookmark.md).</span><span class="sxs-lookup"><span data-stu-id="44f4e-120">Call [IMAPITable::FreeBookmark](imapitable-freebookmark.md).</span></span>
    
 <span data-ttu-id="44f4e-121">**Para mover o cursor para uma posição com indicador**</span><span class="sxs-lookup"><span data-stu-id="44f4e-121">**To move the cursor to a bookmarked position**</span></span>
  
- <span data-ttu-id="44f4e-122">Chame [IMAPITable::SeekRow](imapitable-seekrow.md).</span><span class="sxs-lookup"><span data-stu-id="44f4e-122">Call [IMAPITable::SeekRow](imapitable-seekrow.md).</span></span> <span data-ttu-id="44f4e-123">**SeekRow** estabelece um novo valor para a BOOKMARK_CURRENT atual.</span><span class="sxs-lookup"><span data-stu-id="44f4e-123">**SeekRow** establishes a new value for the BOOKMARK_CURRENT position.</span></span> <span data-ttu-id="44f4e-124">**SeekRow** pode ser usado, por exemplo, para posicionar uma tabela a dez linhas a partir da posição atual ou para começar de novo no início.</span><span class="sxs-lookup"><span data-stu-id="44f4e-124">**SeekRow** can be used, for example, to position a table ten rows from the current position or to start over at the beginning.</span></span> <span data-ttu-id="44f4e-125">Os clientes ou provedores de serviços podem procurar o atual, o início ou o final de uma tabela ou qualquer outra posição associada a um indicador predefinido.</span><span class="sxs-lookup"><span data-stu-id="44f4e-125">Clients or service providers can seek to the current, beginning, or end of a table, or any other position that is associated with a predefined bookmark.</span></span> <span data-ttu-id="44f4e-126">Eles podem se mover em direção à frente ou para trás e limitar a operação a um número especificado de linhas.</span><span class="sxs-lookup"><span data-stu-id="44f4e-126">They can move in either a forward or backward direction and limit the operation to a specified number of rows.</span></span> <span data-ttu-id="44f4e-127">Como regra, os chamadores devem procurar por no máximo 50 linhas com **SeekRow**; [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) deve ser usado com um número maior de linhas.</span><span class="sxs-lookup"><span data-stu-id="44f4e-127">As a rule, callers should seek through no more than 50 rows with **SeekRow**; [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) should be used with larger numbers of rows.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="44f4e-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="44f4e-128">See also</span></span>



[<span data-ttu-id="44f4e-129">Tabelas MAPI</span><span class="sxs-lookup"><span data-stu-id="44f4e-129">MAPI Tables</span></span>](mapi-tables.md)

