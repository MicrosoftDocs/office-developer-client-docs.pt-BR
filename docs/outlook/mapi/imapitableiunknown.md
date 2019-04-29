---
title: A imApitable IUnknown
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
ms.openlocfilehash: d6a13799da4ef9315f9c23317fa18853d71c72f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420112"
---
# <a name="imapitable--iunknown"></a><span data-ttu-id="be040-103">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="be040-103">IMAPITable : IUnknown</span></span>

  
  
<span data-ttu-id="be040-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be040-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="be040-105">Fornece um modo de exibição somente leitura de uma tabela.</span><span class="sxs-lookup"><span data-stu-id="be040-105">Provides a read-only view of a table.</span></span> <span data-ttu-id="be040-106">\*\*\*\* IMAPITable é usado por clientes e provedores de serviço para manipular a forma como uma tabela é exibida.</span><span class="sxs-lookup"><span data-stu-id="be040-106">**IMAPITable** is used by clients and service providers to manipulate the way a table appears.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="be040-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="be040-107">Header file:</span></span>  <br/> |<span data-ttu-id="be040-108">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="be040-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="be040-109">Exposto por:</span><span class="sxs-lookup"><span data-stu-id="be040-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="be040-110">Objetos table</span><span class="sxs-lookup"><span data-stu-id="be040-110">Table objects</span></span>  <br/> |
|<span data-ttu-id="be040-111">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="be040-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="be040-112">Provedores de serviços e MAPI</span><span class="sxs-lookup"><span data-stu-id="be040-112">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="be040-113">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="be040-113">Called by:</span></span>  <br/> |<span data-ttu-id="be040-114">Aplicativos cliente, provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="be040-114">Client applications, service providers</span></span>  <br/> |
|<span data-ttu-id="be040-115">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="be040-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="be040-116">IID_IMAPITable</span><span class="sxs-lookup"><span data-stu-id="be040-116">IID_IMAPITable</span></span>  <br/> |
|<span data-ttu-id="be040-117">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="be040-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="be040-118">LPMAPITABLE</span><span class="sxs-lookup"><span data-stu-id="be040-118">LPMAPITABLE</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="be040-119">Vtable order</span><span class="sxs-lookup"><span data-stu-id="be040-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="be040-120">GetLastError</span><span class="sxs-lookup"><span data-stu-id="be040-120">GetLastError</span></span>](imapitable-getlasterror.md) <br/> |<span data-ttu-id="be040-121">Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior na tabela.</span><span class="sxs-lookup"><span data-stu-id="be040-121">Returns a [MAPIERROR](mapierror.md) structure containing information about the previous error on the table.</span></span>  <br/> |
|[<span data-ttu-id="be040-122">Utilizar</span><span class="sxs-lookup"><span data-stu-id="be040-122">Advise</span></span>](imapitable-advise.md) <br/> |<span data-ttu-id="be040-123">Registra para receber notificações de eventos especificados que afetam a tabela.</span><span class="sxs-lookup"><span data-stu-id="be040-123">Registers to receive notification of specified events affecting the table.</span></span>  <br/> |
|[<span data-ttu-id="be040-124">Cancelar</span><span class="sxs-lookup"><span data-stu-id="be040-124">Unadvise</span></span>](imapitable-unadvise.md) <br/> |<span data-ttu-id="be040-125">Cancela o envio de notificações previamente configuradas com uma chamada para o método imApitable **:: Advise** .</span><span class="sxs-lookup"><span data-stu-id="be040-125">Cancels the sending of notifications previously set up with a call to the **IMAPITable::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="be040-126">GetStatus</span><span class="sxs-lookup"><span data-stu-id="be040-126">GetStatus</span></span>](imapitable-getstatus.md) <br/> |<span data-ttu-id="be040-127">Retorna o tipo e o status da tabela.</span><span class="sxs-lookup"><span data-stu-id="be040-127">Returns the table's status and type.</span></span>  <br/> |
|[<span data-ttu-id="be040-128">SetColumns</span><span class="sxs-lookup"><span data-stu-id="be040-128">SetColumns</span></span>](imapitable-setcolumns.md) <br/> |<span data-ttu-id="be040-129">Define as propriedades específicas e a ordem das propriedades a serem exibidas como colunas na tabela.</span><span class="sxs-lookup"><span data-stu-id="be040-129">Defines the particular properties and order of properties to appear as columns in the table.</span></span>  <br/> |
|[<span data-ttu-id="be040-130">QueryColumns</span><span class="sxs-lookup"><span data-stu-id="be040-130">QueryColumns</span></span>](imapitable-querycolumns.md) <br/> |<span data-ttu-id="be040-131">Retorna uma lista de colunas da tabela.</span><span class="sxs-lookup"><span data-stu-id="be040-131">Returns a list of columns for the table.</span></span>  <br/> |
|[<span data-ttu-id="be040-132">GetRowCount</span><span class="sxs-lookup"><span data-stu-id="be040-132">GetRowCount</span></span>](imapitable-getrowcount.md) <br/> |<span data-ttu-id="be040-133">Retorna o número total de linhas na tabela.</span><span class="sxs-lookup"><span data-stu-id="be040-133">Returns the total number of rows in the table.</span></span>  <br/> |
|[<span data-ttu-id="be040-134">SeekRow</span><span class="sxs-lookup"><span data-stu-id="be040-134">SeekRow</span></span>](imapitable-seekrow.md) <br/> |<span data-ttu-id="be040-135">Move o cursor para uma posição específica na tabela.</span><span class="sxs-lookup"><span data-stu-id="be040-135">Moves the cursor to a specific position in the table.</span></span>  <br/> |
|[<span data-ttu-id="be040-136">SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="be040-136">SeekRowApprox</span></span>](imapitable-seekrowapprox.md) <br/> |<span data-ttu-id="be040-137">Move o cursor para uma posição fracionária aproximada na tabela.</span><span class="sxs-lookup"><span data-stu-id="be040-137">Moves the cursor to an approximate fractional position in the table.</span></span>  <br/> |
|[<span data-ttu-id="be040-138">QueryPosition</span><span class="sxs-lookup"><span data-stu-id="be040-138">QueryPosition</span></span>](imapitable-queryposition.md) <br/> |<span data-ttu-id="be040-139">Recupera a posição de linha atual da tabela do cursor, com base em um valor fracionário.</span><span class="sxs-lookup"><span data-stu-id="be040-139">Retrieves the current table row position of the cursor, based on a fractional value.</span></span>  <br/> |
|[<span data-ttu-id="be040-140">FindRow</span><span class="sxs-lookup"><span data-stu-id="be040-140">FindRow</span></span>](imapitable-findrow.md) <br/> |<span data-ttu-id="be040-141">Localiza a próxima linha em uma tabela que corresponde aos critérios de pesquisa específicos.</span><span class="sxs-lookup"><span data-stu-id="be040-141">Finds the next row in a table that matches specific search criteria.</span></span>  <br/> |
|[<span data-ttu-id="be040-142">Restrict</span><span class="sxs-lookup"><span data-stu-id="be040-142">Restrict</span></span>](imapitable-restrict.md) <br/> |<span data-ttu-id="be040-143">Aplica um filtro a uma tabela, reduzindo o conjunto de linhas somente para as linhas que correspondam aos critérios especificados.</span><span class="sxs-lookup"><span data-stu-id="be040-143">Applies a filter to a table, reducing the row set to only those rows matching the specified criteria.</span></span>  <br/> |
|[<span data-ttu-id="be040-144">CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="be040-144">CreateBookmark</span></span>](imapitable-createbookmark.md) <br/> |<span data-ttu-id="be040-145">Marca a posição atual da tabela.</span><span class="sxs-lookup"><span data-stu-id="be040-145">Marks the table's current position.</span></span>  <br/> |
|[<span data-ttu-id="be040-146">FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="be040-146">FreeBookmark</span></span>](imapitable-freebookmark.md) <br/> |<span data-ttu-id="be040-147">Libera a memória associada a um indicador.</span><span class="sxs-lookup"><span data-stu-id="be040-147">Releases the memory associated with a bookmark.</span></span>  <br/> |
|[<span data-ttu-id="be040-148">SortTable</span><span class="sxs-lookup"><span data-stu-id="be040-148">SortTable</span></span>](imapitable-sorttable.md) <br/> |<span data-ttu-id="be040-149">Ordena as linhas da tabela com base nos critérios de classificação.</span><span class="sxs-lookup"><span data-stu-id="be040-149">Orders the rows of the table based on sort criteria.</span></span>  <br/> |
|[<span data-ttu-id="be040-150">QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="be040-150">QuerySortOrder</span></span>](imapitable-querysortorder.md) <br/> |<span data-ttu-id="be040-151">Recupera a ordem de classificação atual para uma tabela.</span><span class="sxs-lookup"><span data-stu-id="be040-151">Retrieves the current sort order for a table.</span></span>  <br/> |
|[<span data-ttu-id="be040-152">QueryRows</span><span class="sxs-lookup"><span data-stu-id="be040-152">QueryRows</span></span>](imapitable-queryrows.md) <br/> |<span data-ttu-id="be040-153">Retorna uma ou mais linhas de uma tabela, começando na posição atual do cursor.</span><span class="sxs-lookup"><span data-stu-id="be040-153">Returns one or more rows from a table, beginning at the current cursor position.</span></span>  <br/> |
|<span data-ttu-id="be040-154">Anular\*\*</span><span class="sxs-lookup"><span data-stu-id="be040-154">[Abort](imapitable-abort.md)</span></span> <br/> |<span data-ttu-id="be040-155">Para todas as operações assíncronas atualmente em andamento para a tabela.</span><span class="sxs-lookup"><span data-stu-id="be040-155">Stops any asynchronous operations currently in progress for the table.</span></span>  <br/> |
|[<span data-ttu-id="be040-156">ExpandRow</span><span class="sxs-lookup"><span data-stu-id="be040-156">ExpandRow</span></span>](imapitable-expandrow.md) <br/> |<span data-ttu-id="be040-157">Expande uma categoria de tabela recolhida, adicionando as linhas de folha pertencentes à categoria para o modo de exibição de tabela.</span><span class="sxs-lookup"><span data-stu-id="be040-157">Expands a collapsed table category, adding the leaf rows belonging to the category to the table view.</span></span>  <br/> |
|[<span data-ttu-id="be040-158">CollapseRow</span><span class="sxs-lookup"><span data-stu-id="be040-158">CollapseRow</span></span>](imapitable-collapserow.md) <br/> |<span data-ttu-id="be040-159">Recolhe uma categoria de tabela expandida, removendo as linhas de folha pertencentes à categoria do modo de exibição de tabela.</span><span class="sxs-lookup"><span data-stu-id="be040-159">Collapses an expanded table category, removing the leaf rows belonging to the category from the table view.</span></span>  <br/> |
|[<span data-ttu-id="be040-160">WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="be040-160">WaitForCompletion</span></span>](imapitable-waitforcompletion.md) <br/> |<span data-ttu-id="be040-161">Suspende o processamento até que uma ou mais operações assíncronas em andamento na tabela tenham sido concluídas.</span><span class="sxs-lookup"><span data-stu-id="be040-161">Suspends processing until one or more asynchronous operations in progress on the table have completed.</span></span>  <br/> |
|[<span data-ttu-id="be040-162">GetCollapsestate</span><span class="sxs-lookup"><span data-stu-id="be040-162">GetCollapseState</span></span>](imapitable-getcollapsestate.md) <br/> |<span data-ttu-id="be040-163">Retorna os dados necessários para reconstruir o estado atual recolhido ou expandido de uma tabela categorizada.</span><span class="sxs-lookup"><span data-stu-id="be040-163">Returns the data necessary to rebuild the current collapsed or expanded state of a categorized table.</span></span>  <br/> |
|[<span data-ttu-id="be040-164">SetCollapsestate</span><span class="sxs-lookup"><span data-stu-id="be040-164">SetCollapseState</span></span>](imapitable-setcollapsestate.md) <br/> |<span data-ttu-id="be040-165">Recria o estado atual expandido ou recolhido de uma tabela categorizada usando dados que foram salvos por uma chamada anterior para o método **IMAPITable::** getcollapsestate.</span><span class="sxs-lookup"><span data-stu-id="be040-165">Rebuilds the current expanded or collapsed state of a categorized table using data that was saved by a prior call to the **IMAPITable::GetCollapseState** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="be040-166">Confira também</span><span class="sxs-lookup"><span data-stu-id="be040-166">See also</span></span>



[<span data-ttu-id="be040-167">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="be040-167">MAPI Interfaces</span></span>](mapi-interfaces.md)

