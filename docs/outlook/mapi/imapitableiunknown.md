---
title: IMAPITable IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable
api_type:
- COM
ms.assetid: f25be2b1-0f94-4a0c-b29d-d2201dc70ab7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a5504711bdeac4ef94cbe47395ceb8163b60ad68
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584328"
---
# <a name="imapitable--iunknown"></a><span data-ttu-id="bdf37-103">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bdf37-103">IMAPITable : IUnknown</span></span>

  
  
<span data-ttu-id="bdf37-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bdf37-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bdf37-105">Fornece uma exibição somente leitura de uma tabela.</span><span class="sxs-lookup"><span data-stu-id="bdf37-105">Provides a read-only view of a table.</span></span> <span data-ttu-id="bdf37-106">**IMAPITable** é usado por clientes e provedores de serviços para manipular a maneira como uma tabela é exibida.</span><span class="sxs-lookup"><span data-stu-id="bdf37-106">**IMAPITable** is used by clients and service providers to manipulate the way a table appears.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bdf37-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="bdf37-107">Header file:</span></span>  <br/> |<span data-ttu-id="bdf37-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bdf37-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="bdf37-109">Expostos pelo:</span><span class="sxs-lookup"><span data-stu-id="bdf37-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="bdf37-110">Objetos Table</span><span class="sxs-lookup"><span data-stu-id="bdf37-110">Table objects</span></span>  <br/> |
|<span data-ttu-id="bdf37-111">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="bdf37-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="bdf37-112">Provedores de serviços e MAPI</span><span class="sxs-lookup"><span data-stu-id="bdf37-112">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="bdf37-113">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="bdf37-113">Called by:</span></span>  <br/> |<span data-ttu-id="bdf37-114">Aplicativos clientes, provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="bdf37-114">Client applications, service providers</span></span>  <br/> |
|<span data-ttu-id="bdf37-115">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="bdf37-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="bdf37-116">IID_IMAPITable</span><span class="sxs-lookup"><span data-stu-id="bdf37-116">IID_IMAPITable</span></span>  <br/> |
|<span data-ttu-id="bdf37-117">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="bdf37-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="bdf37-118">LPMAPITABLE</span><span class="sxs-lookup"><span data-stu-id="bdf37-118">LPMAPITABLE</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="bdf37-119">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="bdf37-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="bdf37-120">GetLastError</span><span class="sxs-lookup"><span data-stu-id="bdf37-120">GetLastError</span></span>](imapitable-getlasterror.md) <br/> |<span data-ttu-id="bdf37-121">Retorna uma estrutura [MAPIERROR](mapierror.md) contendo informações sobre o erro anterior na tabela.</span><span class="sxs-lookup"><span data-stu-id="bdf37-121">Returns a [MAPIERROR](mapierror.md) structure containing information about the previous error on the table.</span></span>  <br/> |
|[<span data-ttu-id="bdf37-122">Aviso</span><span class="sxs-lookup"><span data-stu-id="bdf37-122">Advise</span></span>](imapitable-advise.md) <br/> |<span data-ttu-id="bdf37-123">Registra para receber notificações de eventos especificados que afetam a tabela.</span><span class="sxs-lookup"><span data-stu-id="bdf37-123">Registers to receive notification of specified events affecting the table.</span></span>  <br/> |
|[<span data-ttu-id="bdf37-124">Unadvise</span><span class="sxs-lookup"><span data-stu-id="bdf37-124">Unadvise</span></span>](imapitable-unadvise.md) <br/> |<span data-ttu-id="bdf37-125">Cancela o envio de notificações configuradas anteriormente com uma chamada ao método **IMAPITable::Advise** .</span><span class="sxs-lookup"><span data-stu-id="bdf37-125">Cancels the sending of notifications previously set up with a call to the **IMAPITable::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="bdf37-126">GetStatus</span><span class="sxs-lookup"><span data-stu-id="bdf37-126">GetStatus</span></span>](imapitable-getstatus.md) <br/> |<span data-ttu-id="bdf37-127">Retorna o status e o tipo da tabela.</span><span class="sxs-lookup"><span data-stu-id="bdf37-127">Returns the table's status and type.</span></span>  <br/> |
|[<span data-ttu-id="bdf37-128">SetColumns</span><span class="sxs-lookup"><span data-stu-id="bdf37-128">SetColumns</span></span>](imapitable-setcolumns.md) <br/> |<span data-ttu-id="bdf37-129">Define as propriedades específicas e a ordem das propriedades aparecer como colunas na tabela.</span><span class="sxs-lookup"><span data-stu-id="bdf37-129">Defines the particular properties and order of properties to appear as columns in the table.</span></span>  <br/> |
|[<span data-ttu-id="bdf37-130">QueryColumns</span><span class="sxs-lookup"><span data-stu-id="bdf37-130">QueryColumns</span></span>](imapitable-querycolumns.md) <br/> |<span data-ttu-id="bdf37-131">Retorna uma lista das colunas da tabela.</span><span class="sxs-lookup"><span data-stu-id="bdf37-131">Returns a list of columns for the table.</span></span>  <br/> |
|[<span data-ttu-id="bdf37-132">GetRowCount</span><span class="sxs-lookup"><span data-stu-id="bdf37-132">GetRowCount</span></span>](imapitable-getrowcount.md) <br/> |<span data-ttu-id="bdf37-133">Retorna o número total de linhas na tabela.</span><span class="sxs-lookup"><span data-stu-id="bdf37-133">Returns the total number of rows in the table.</span></span>  <br/> |
|[<span data-ttu-id="bdf37-134">SeekRow</span><span class="sxs-lookup"><span data-stu-id="bdf37-134">SeekRow</span></span>](imapitable-seekrow.md) <br/> |<span data-ttu-id="bdf37-135">Move o cursor para uma posição específica na tabela.</span><span class="sxs-lookup"><span data-stu-id="bdf37-135">Moves the cursor to a specific position in the table.</span></span>  <br/> |
|[<span data-ttu-id="bdf37-136">SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="bdf37-136">SeekRowApprox</span></span>](imapitable-seekrowapprox.md) <br/> |<span data-ttu-id="bdf37-137">Move o cursor para uma posição fracional aproximada na tabela.</span><span class="sxs-lookup"><span data-stu-id="bdf37-137">Moves the cursor to an approximate fractional position in the table.</span></span>  <br/> |
|[<span data-ttu-id="bdf37-138">QueryPosition</span><span class="sxs-lookup"><span data-stu-id="bdf37-138">QueryPosition</span></span>](imapitable-queryposition.md) <br/> |<span data-ttu-id="bdf37-139">Recupera a posição da linha de tabela atual do cursor, com base em um valor fracionário.</span><span class="sxs-lookup"><span data-stu-id="bdf37-139">Retrieves the current table row position of the cursor, based on a fractional value.</span></span>  <br/> |
|[<span data-ttu-id="bdf37-140">FindRow</span><span class="sxs-lookup"><span data-stu-id="bdf37-140">FindRow</span></span>](imapitable-findrow.md) <br/> |<span data-ttu-id="bdf37-141">Localiza a próxima linha em uma tabela que corresponde a determinados critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="bdf37-141">Finds the next row in a table that matches specific search criteria.</span></span>  <br/> |
|[<span data-ttu-id="bdf37-142">Restringir</span><span class="sxs-lookup"><span data-stu-id="bdf37-142">Restrict</span></span>](imapitable-restrict.md) <br/> |<span data-ttu-id="bdf37-143">Aplica um filtro a uma tabela, reduzindo a linha definida como apenas as linhas que correspondem aos critérios especificados.</span><span class="sxs-lookup"><span data-stu-id="bdf37-143">Applies a filter to a table, reducing the row set to only those rows matching the specified criteria.</span></span>  <br/> |
|[<span data-ttu-id="bdf37-144">CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="bdf37-144">CreateBookmark</span></span>](imapitable-createbookmark.md) <br/> |<span data-ttu-id="bdf37-145">Marca a posição atual da tabela.</span><span class="sxs-lookup"><span data-stu-id="bdf37-145">Marks the table's current position.</span></span>  <br/> |
|[<span data-ttu-id="bdf37-146">FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="bdf37-146">FreeBookmark</span></span>](imapitable-freebookmark.md) <br/> |<span data-ttu-id="bdf37-147">Libera a memória associada a um indicador.</span><span class="sxs-lookup"><span data-stu-id="bdf37-147">Releases the memory associated with a bookmark.</span></span>  <br/> |
|[<span data-ttu-id="bdf37-148">SortTable</span><span class="sxs-lookup"><span data-stu-id="bdf37-148">SortTable</span></span>](imapitable-sorttable.md) <br/> |<span data-ttu-id="bdf37-149">Ordena as linhas da tabela com base nos critérios de classificação.</span><span class="sxs-lookup"><span data-stu-id="bdf37-149">Orders the rows of the table based on sort criteria.</span></span>  <br/> |
|[<span data-ttu-id="bdf37-150">QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="bdf37-150">QuerySortOrder</span></span>](imapitable-querysortorder.md) <br/> |<span data-ttu-id="bdf37-151">Recupera a ordem de classificação atual para uma tabela.</span><span class="sxs-lookup"><span data-stu-id="bdf37-151">Retrieves the current sort order for a table.</span></span>  <br/> |
|[<span data-ttu-id="bdf37-152">QueryRows</span><span class="sxs-lookup"><span data-stu-id="bdf37-152">QueryRows</span></span>](imapitable-queryrows.md) <br/> |<span data-ttu-id="bdf37-153">Retorna uma ou mais linhas de uma tabela, começando à meia posição atual do cursor.</span><span class="sxs-lookup"><span data-stu-id="bdf37-153">Returns one or more rows from a table, beginning at the current cursor position.</span></span>  <br/> |
|[<span data-ttu-id="bdf37-154">Abort</span><span class="sxs-lookup"><span data-stu-id="bdf37-154">Abort</span></span>](imapitable-abort.md) <br/> |<span data-ttu-id="bdf37-155">Interrompe a qualquer operação assíncrona em andamento atualmente para a tabela.</span><span class="sxs-lookup"><span data-stu-id="bdf37-155">Stops any asynchronous operations currently in progress for the table.</span></span>  <br/> |
|[<span data-ttu-id="bdf37-156">ExpandRow</span><span class="sxs-lookup"><span data-stu-id="bdf37-156">ExpandRow</span></span>](imapitable-expandrow.md) <br/> |<span data-ttu-id="bdf37-157">Expande uma categoria de tabela recolhida, adicionando as linhas da folha que pertencem à categoria para o modo de exibição de tabela.</span><span class="sxs-lookup"><span data-stu-id="bdf37-157">Expands a collapsed table category, adding the leaf rows belonging to the category to the table view.</span></span>  <br/> |
|[<span data-ttu-id="bdf37-158">CollapseRow</span><span class="sxs-lookup"><span data-stu-id="bdf37-158">CollapseRow</span></span>](imapitable-collapserow.md) <br/> |<span data-ttu-id="bdf37-159">Recolhe uma categoria de tabela expandida, removendo as linhas da folha que pertencem à categoria da visualização de tabela.</span><span class="sxs-lookup"><span data-stu-id="bdf37-159">Collapses an expanded table category, removing the leaf rows belonging to the category from the table view.</span></span>  <br/> |
|[<span data-ttu-id="bdf37-160">WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="bdf37-160">WaitForCompletion</span></span>](imapitable-waitforcompletion.md) <br/> |<span data-ttu-id="bdf37-161">Suspende o processamento até que um ou mais operações assíncronas em andamento na tabela forem concluídas.</span><span class="sxs-lookup"><span data-stu-id="bdf37-161">Suspends processing until one or more asynchronous operations in progress on the table have completed.</span></span>  <br/> |
|[<span data-ttu-id="bdf37-162">GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="bdf37-162">GetCollapseState</span></span>](imapitable-getcollapsestate.md) <br/> |<span data-ttu-id="bdf37-163">Retorna os dados necessários para recriar as atuais recolhido ou expandido o estado de uma tabela categorizado.</span><span class="sxs-lookup"><span data-stu-id="bdf37-163">Returns the data necessary to rebuild the current collapsed or expanded state of a categorized table.</span></span>  <br/> |
|[<span data-ttu-id="bdf37-164">SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="bdf37-164">SetCollapseState</span></span>](imapitable-setcollapsestate.md) <br/> |<span data-ttu-id="bdf37-165">Recriará o estado atual de expandidos ou recolhido de uma tabela categorizado usando os dados que foi salvo por uma chamada anterior para o método **IMAPITable::GetCollapseState** .</span><span class="sxs-lookup"><span data-stu-id="bdf37-165">Rebuilds the current expanded or collapsed state of a categorized table using data that was saved by a prior call to the **IMAPITable::GetCollapseState** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bdf37-166">Confira também</span><span class="sxs-lookup"><span data-stu-id="bdf37-166">See also</span></span>



[<span data-ttu-id="bdf37-167">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="bdf37-167">MAPI Interfaces</span></span>](mapi-interfaces.md)

