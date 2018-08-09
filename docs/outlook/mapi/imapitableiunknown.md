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
ms.openlocfilehash: 0ffaf5909c978059343067c93a2b30f5969327e4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767344"
---
# <a name="imapitable--iunknown"></a><span data-ttu-id="ad989-103">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ad989-103">IMAPITable : IUnknown</span></span>

  
  
<span data-ttu-id="ad989-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ad989-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ad989-105">Fornece uma exibição somente leitura de uma tabela.</span><span class="sxs-lookup"><span data-stu-id="ad989-105">Provides a read-only view of a table.</span></span> <span data-ttu-id="ad989-106">**IMAPITable** é usado por clientes e provedores de serviços para manipular a maneira como uma tabela é exibida.</span><span class="sxs-lookup"><span data-stu-id="ad989-106">**IMAPITable** is used by clients and service providers to manipulate the way a table appears.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ad989-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="ad989-107">Header file:</span></span>  <br/> |<span data-ttu-id="ad989-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ad989-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="ad989-109">Expostos pelo:</span><span class="sxs-lookup"><span data-stu-id="ad989-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="ad989-110">Objetos Table</span><span class="sxs-lookup"><span data-stu-id="ad989-110">Table objects</span></span>  <br/> |
|<span data-ttu-id="ad989-111">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="ad989-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="ad989-112">Provedores de serviços e MAPI</span><span class="sxs-lookup"><span data-stu-id="ad989-112">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="ad989-113">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="ad989-113">Called by:</span></span>  <br/> |<span data-ttu-id="ad989-114">Aplicativos clientes, provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="ad989-114">Client applications, service providers</span></span>  <br/> |
|<span data-ttu-id="ad989-115">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="ad989-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="ad989-116">IID_IMAPITable</span><span class="sxs-lookup"><span data-stu-id="ad989-116">IID_IMAPITable</span></span>  <br/> |
|<span data-ttu-id="ad989-117">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="ad989-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="ad989-118">LPMAPITABLE</span><span class="sxs-lookup"><span data-stu-id="ad989-118">LPMAPITABLE</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="ad989-119">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="ad989-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="ad989-120">GetLastError</span><span class="sxs-lookup"><span data-stu-id="ad989-120">GetLastError</span></span>](imapitable-getlasterror.md) <br/> |<span data-ttu-id="ad989-121">Retorna uma estrutura [MAPIERROR](mapierror.md) contendo informações sobre o erro anterior na tabela.</span><span class="sxs-lookup"><span data-stu-id="ad989-121">Returns a [MAPIERROR](mapierror.md) structure containing information about the previous error on the table.</span></span>  <br/> |
|[<span data-ttu-id="ad989-122">Aviso</span><span class="sxs-lookup"><span data-stu-id="ad989-122">Advise</span></span>](imapitable-advise.md) <br/> |<span data-ttu-id="ad989-123">Registra para receber notificações de eventos especificados que afetam a tabela.</span><span class="sxs-lookup"><span data-stu-id="ad989-123">Registers to receive notification of specified events affecting the table.</span></span>  <br/> |
|[<span data-ttu-id="ad989-124">Unadvise</span><span class="sxs-lookup"><span data-stu-id="ad989-124">Unadvise</span></span>](imapitable-unadvise.md) <br/> |<span data-ttu-id="ad989-125">Cancela o envio de notificações configuradas anteriormente com uma chamada ao método **IMAPITable::Advise** .</span><span class="sxs-lookup"><span data-stu-id="ad989-125">Cancels the sending of notifications previously set up with a call to the **IMAPITable::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="ad989-126">GetStatus</span><span class="sxs-lookup"><span data-stu-id="ad989-126">GetStatus</span></span>](imapitable-getstatus.md) <br/> |<span data-ttu-id="ad989-127">Retorna o status e o tipo da tabela.</span><span class="sxs-lookup"><span data-stu-id="ad989-127">Returns the table's status and type.</span></span>  <br/> |
|[<span data-ttu-id="ad989-128">SetColumns</span><span class="sxs-lookup"><span data-stu-id="ad989-128">SetColumns</span></span>](imapitable-setcolumns.md) <br/> |<span data-ttu-id="ad989-129">Define as propriedades específicas e a ordem das propriedades aparecer como colunas na tabela.</span><span class="sxs-lookup"><span data-stu-id="ad989-129">Defines the particular properties and order of properties to appear as columns in the table.</span></span>  <br/> |
|[<span data-ttu-id="ad989-130">QueryColumns</span><span class="sxs-lookup"><span data-stu-id="ad989-130">QueryColumns</span></span>](imapitable-querycolumns.md) <br/> |<span data-ttu-id="ad989-131">Retorna uma lista das colunas da tabela.</span><span class="sxs-lookup"><span data-stu-id="ad989-131">Returns a list of columns for the table.</span></span>  <br/> |
|[<span data-ttu-id="ad989-132">GetRowCount</span><span class="sxs-lookup"><span data-stu-id="ad989-132">GetRowCount</span></span>](imapitable-getrowcount.md) <br/> |<span data-ttu-id="ad989-133">Retorna o número total de linhas na tabela.</span><span class="sxs-lookup"><span data-stu-id="ad989-133">Returns the total number of rows in the table.</span></span>  <br/> |
|[<span data-ttu-id="ad989-134">SeekRow</span><span class="sxs-lookup"><span data-stu-id="ad989-134">SeekRow</span></span>](imapitable-seekrow.md) <br/> |<span data-ttu-id="ad989-135">Move o cursor para uma posição específica na tabela.</span><span class="sxs-lookup"><span data-stu-id="ad989-135">Moves the cursor to a specific position in the table.</span></span>  <br/> |
|[<span data-ttu-id="ad989-136">SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="ad989-136">SeekRowApprox</span></span>](imapitable-seekrowapprox.md) <br/> |<span data-ttu-id="ad989-137">Move o cursor para uma posição fracional aproximada na tabela.</span><span class="sxs-lookup"><span data-stu-id="ad989-137">Moves the cursor to an approximate fractional position in the table.</span></span>  <br/> |
|[<span data-ttu-id="ad989-138">QueryPosition</span><span class="sxs-lookup"><span data-stu-id="ad989-138">QueryPosition</span></span>](imapitable-queryposition.md) <br/> |<span data-ttu-id="ad989-139">Recupera a posição da linha de tabela atual do cursor, com base em um valor fracionário.</span><span class="sxs-lookup"><span data-stu-id="ad989-139">Retrieves the current table row position of the cursor, based on a fractional value.</span></span>  <br/> |
|[<span data-ttu-id="ad989-140">FindRow</span><span class="sxs-lookup"><span data-stu-id="ad989-140">FindRow</span></span>](imapitable-findrow.md) <br/> |<span data-ttu-id="ad989-141">Localiza a próxima linha em uma tabela que corresponde a determinados critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="ad989-141">Finds the next row in a table that matches specific search criteria.</span></span>  <br/> |
|[<span data-ttu-id="ad989-142">Restringir</span><span class="sxs-lookup"><span data-stu-id="ad989-142">Restrict</span></span>](imapitable-restrict.md) <br/> |<span data-ttu-id="ad989-143">Aplica um filtro a uma tabela, reduzindo a linha definida como apenas as linhas que correspondem aos critérios especificados.</span><span class="sxs-lookup"><span data-stu-id="ad989-143">Applies a filter to a table, reducing the row set to only those rows matching the specified criteria.</span></span>  <br/> |
|[<span data-ttu-id="ad989-144">CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="ad989-144">CreateBookmark</span></span>](imapitable-createbookmark.md) <br/> |<span data-ttu-id="ad989-145">Marca a posição atual da tabela.</span><span class="sxs-lookup"><span data-stu-id="ad989-145">Marks the table's current position.</span></span>  <br/> |
|[<span data-ttu-id="ad989-146">FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="ad989-146">FreeBookmark</span></span>](imapitable-freebookmark.md) <br/> |<span data-ttu-id="ad989-147">Libera a memória associada a um indicador.</span><span class="sxs-lookup"><span data-stu-id="ad989-147">Releases the memory associated with a bookmark.</span></span>  <br/> |
|[<span data-ttu-id="ad989-148">SortTable</span><span class="sxs-lookup"><span data-stu-id="ad989-148">SortTable</span></span>](imapitable-sorttable.md) <br/> |<span data-ttu-id="ad989-149">Ordena as linhas da tabela com base nos critérios de classificação.</span><span class="sxs-lookup"><span data-stu-id="ad989-149">Orders the rows of the table based on sort criteria.</span></span>  <br/> |
|[<span data-ttu-id="ad989-150">QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="ad989-150">QuerySortOrder</span></span>](imapitable-querysortorder.md) <br/> |<span data-ttu-id="ad989-151">Recupera a ordem de classificação atual para uma tabela.</span><span class="sxs-lookup"><span data-stu-id="ad989-151">Retrieves the current sort order for a table.</span></span>  <br/> |
|[<span data-ttu-id="ad989-152">QueryRows</span><span class="sxs-lookup"><span data-stu-id="ad989-152">QueryRows</span></span>](imapitable-queryrows.md) <br/> |<span data-ttu-id="ad989-153">Retorna uma ou mais linhas de uma tabela, começando à meia posição atual do cursor.</span><span class="sxs-lookup"><span data-stu-id="ad989-153">Returns one or more rows from a table, beginning at the current cursor position.</span></span>  <br/> |
|[<span data-ttu-id="ad989-154">Abort</span><span class="sxs-lookup"><span data-stu-id="ad989-154">Abort</span></span>](imapitable-abort.md) <br/> |<span data-ttu-id="ad989-155">Interrompe a qualquer operação assíncrona em andamento atualmente para a tabela.</span><span class="sxs-lookup"><span data-stu-id="ad989-155">Stops any asynchronous operations currently in progress for the table.</span></span>  <br/> |
|[<span data-ttu-id="ad989-156">ExpandRow</span><span class="sxs-lookup"><span data-stu-id="ad989-156">ExpandRow</span></span>](imapitable-expandrow.md) <br/> |<span data-ttu-id="ad989-157">Expande uma categoria de tabela recolhida, adicionando as linhas da folha que pertencem à categoria para o modo de exibição de tabela.</span><span class="sxs-lookup"><span data-stu-id="ad989-157">Expands a collapsed table category, adding the leaf rows belonging to the category to the table view.</span></span>  <br/> |
|[<span data-ttu-id="ad989-158">CollapseRow</span><span class="sxs-lookup"><span data-stu-id="ad989-158">CollapseRow</span></span>](imapitable-collapserow.md) <br/> |<span data-ttu-id="ad989-159">Recolhe uma categoria de tabela expandida, removendo as linhas da folha que pertencem à categoria da visualização de tabela.</span><span class="sxs-lookup"><span data-stu-id="ad989-159">Collapses an expanded table category, removing the leaf rows belonging to the category from the table view.</span></span>  <br/> |
|[<span data-ttu-id="ad989-160">WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="ad989-160">WaitForCompletion</span></span>](imapitable-waitforcompletion.md) <br/> |<span data-ttu-id="ad989-161">Suspende o processamento até que um ou mais operações assíncronas em andamento na tabela forem concluídas.</span><span class="sxs-lookup"><span data-stu-id="ad989-161">Suspends processing until one or more asynchronous operations in progress on the table have completed.</span></span>  <br/> |
|[<span data-ttu-id="ad989-162">GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="ad989-162">GetCollapseState</span></span>](imapitable-getcollapsestate.md) <br/> |<span data-ttu-id="ad989-163">Retorna os dados necessários para recriar as atuais recolhido ou expandido o estado de uma tabela categorizado.</span><span class="sxs-lookup"><span data-stu-id="ad989-163">Returns the data necessary to rebuild the current collapsed or expanded state of a categorized table.</span></span>  <br/> |
|[<span data-ttu-id="ad989-164">SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="ad989-164">SetCollapseState</span></span>](imapitable-setcollapsestate.md) <br/> |<span data-ttu-id="ad989-165">Recriará o estado atual de expandidos ou recolhido de uma tabela categorizado usando os dados que foi salvo por uma chamada anterior para o método **IMAPITable::GetCollapseState** .</span><span class="sxs-lookup"><span data-stu-id="ad989-165">Rebuilds the current expanded or collapsed state of a categorized table using data that was saved by a prior call to the **IMAPITable::GetCollapseState** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ad989-166">Confira também</span><span class="sxs-lookup"><span data-stu-id="ad989-166">See also</span></span>



[<span data-ttu-id="ad989-167">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="ad989-167">MAPI Interfaces</span></span>](mapi-interfaces.md)

