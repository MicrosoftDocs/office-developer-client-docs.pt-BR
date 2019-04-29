---
title: ITableData IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData
api_type:
- COM
ms.assetid: ac7ae09f-ce19-45cf-8963-fad5bba75452
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3992bea899239ee5975505dec366490d6bbe1698
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430592"
---
# <a name="itabledata--iunknown"></a><span data-ttu-id="ed9cc-103">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ed9cc-103">ITableData : IUnknown</span></span>

  
  
<span data-ttu-id="ed9cc-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ed9cc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ed9cc-105">Fornece métodos utilitários para trabalhar com tabelas.</span><span class="sxs-lookup"><span data-stu-id="ed9cc-105">Provides utility methods for working with tables.</span></span> <span data-ttu-id="ed9cc-106">O MAPI fornece objetos de dados de tabela ou objetos que implementam o **ITableData** para ajudar os provedores de serviços a executar a manutenção da tabela.</span><span class="sxs-lookup"><span data-stu-id="ed9cc-106">MAPI provides table data objects or objects that implement **ITableData** to help service providers perform table maintenance.</span></span> <span data-ttu-id="ed9cc-107">Para obter um objeto de dados de tabela, os provedores [](createtable.md) de serviços chamam a função CreateTable.</span><span class="sxs-lookup"><span data-stu-id="ed9cc-107">To obtain a table data object, service providers call the [CreateTable](createtable.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ed9cc-108">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="ed9cc-108">Header file:</span></span>  <br/> |<span data-ttu-id="ed9cc-109">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="ed9cc-109">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="ed9cc-110">Exposto por:</span><span class="sxs-lookup"><span data-stu-id="ed9cc-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="ed9cc-111">Objetos de dados de tabela</span><span class="sxs-lookup"><span data-stu-id="ed9cc-111">Table data objects</span></span>  <br/> |
|<span data-ttu-id="ed9cc-112">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="ed9cc-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="ed9cc-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="ed9cc-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="ed9cc-114">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="ed9cc-114">Called by:</span></span>  <br/> |<span data-ttu-id="ed9cc-115">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="ed9cc-115">Service providers</span></span>  <br/> |
|<span data-ttu-id="ed9cc-116">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="ed9cc-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="ed9cc-117">IID_IMAPITableData</span><span class="sxs-lookup"><span data-stu-id="ed9cc-117">IID_IMAPITableData</span></span>  <br/> |
|<span data-ttu-id="ed9cc-118">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="ed9cc-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="ed9cc-119">LPTABLEDATA</span><span class="sxs-lookup"><span data-stu-id="ed9cc-119">LPTABLEDATA</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="ed9cc-120">Vtable order</span><span class="sxs-lookup"><span data-stu-id="ed9cc-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="ed9cc-121">HrGetView</span><span class="sxs-lookup"><span data-stu-id="ed9cc-121">HrGetView</span></span>](itabledata-hrgetview.md) <br/> |<span data-ttu-id="ed9cc-122">Cria um modo de exibição de tabela, retornando [](imapitableiunknown.md) um ponteiro para uma implementação IMAPITable.</span><span class="sxs-lookup"><span data-stu-id="ed9cc-122">Creates a table view, returning a pointer to an [IMAPITable](imapitableiunknown.md) implementation.</span></span>  <br/> |
|[<span data-ttu-id="ed9cc-123">HrModifyRow</span><span class="sxs-lookup"><span data-stu-id="ed9cc-123">HrModifyRow</span></span>](itabledata-hrmodifyrow.md) <br/> |<span data-ttu-id="ed9cc-124">Insere uma nova linha de tabela, possivelmente substituindo uma linha existente.</span><span class="sxs-lookup"><span data-stu-id="ed9cc-124">Inserts a new table row, possibly replacing an existing row.</span></span>  <br/> |
|[<span data-ttu-id="ed9cc-125">HrDeleteRow</span><span class="sxs-lookup"><span data-stu-id="ed9cc-125">HrDeleteRow</span></span>](itabledata-hrdeleterow.md) <br/> |<span data-ttu-id="ed9cc-126">Exclui uma linha de tabela.</span><span class="sxs-lookup"><span data-stu-id="ed9cc-126">Deletes a table row.</span></span>  <br/> |
|[<span data-ttu-id="ed9cc-127">HrQueryRow</span><span class="sxs-lookup"><span data-stu-id="ed9cc-127">HrQueryRow</span></span>](itabledata-hrqueryrow.md) <br/> |<span data-ttu-id="ed9cc-128">Recupera uma linha de tabela.</span><span class="sxs-lookup"><span data-stu-id="ed9cc-128">Retrieves a table row.</span></span>  <br/> |
|[<span data-ttu-id="ed9cc-129">HrEnumRow</span><span class="sxs-lookup"><span data-stu-id="ed9cc-129">HrEnumRow</span></span>](itabledata-hrenumrow.md) <br/> |<span data-ttu-id="ed9cc-130">Recupera uma linha com base em sua posição na tabela.</span><span class="sxs-lookup"><span data-stu-id="ed9cc-130">Retrieves a row based on its position in the table.</span></span>  <br/> |
|[<span data-ttu-id="ed9cc-131">HrNotify</span><span class="sxs-lookup"><span data-stu-id="ed9cc-131">HrNotify</span></span>](itabledata-hrnotify.md) <br/> |<span data-ttu-id="ed9cc-132">Envia uma notificação para uma linha de tabela.</span><span class="sxs-lookup"><span data-stu-id="ed9cc-132">Sends a notification for a table row.</span></span>  <br/> |
|[<span data-ttu-id="ed9cc-133">HrInsertRow</span><span class="sxs-lookup"><span data-stu-id="ed9cc-133">HrInsertRow</span></span>](itabledata-hrinsertrow.md) <br/> |<span data-ttu-id="ed9cc-134">Insere uma linha de tabela.</span><span class="sxs-lookup"><span data-stu-id="ed9cc-134">Inserts a table row.</span></span>  <br/> |
|[<span data-ttu-id="ed9cc-135">HrModifyRows</span><span class="sxs-lookup"><span data-stu-id="ed9cc-135">HrModifyRows</span></span>](itabledata-hrmodifyrows.md) <br/> |<span data-ttu-id="ed9cc-136">Insere várias linhas de tabela, possivelmente substituindo linhas existentes.</span><span class="sxs-lookup"><span data-stu-id="ed9cc-136">Inserts multiple table rows, possibly replacing existing rows.</span></span>  <br/> |
|[<span data-ttu-id="ed9cc-137">HrDeleteRows</span><span class="sxs-lookup"><span data-stu-id="ed9cc-137">HrDeleteRows</span></span>](itabledata-hrdeleterows.md) <br/> |<span data-ttu-id="ed9cc-138">Exclui várias linhas de tabela.</span><span class="sxs-lookup"><span data-stu-id="ed9cc-138">Deletes multiple table rows.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ed9cc-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed9cc-139">Remarks</span></span>

<span data-ttu-id="ed9cc-140">A implementação de MAPI do **ITableData** funciona com tabelas mantendo todos os dados e restrições associadas na memória, tornando-a inadequada para uso com tabelas muito grandes.</span><span class="sxs-lookup"><span data-stu-id="ed9cc-140">The MAPI implementation of **ITableData** works with tables by holding all of the data and any associated restrictions in memory, making it unsuitable for use with very large tables.</span></span> <span data-ttu-id="ed9cc-141">Restrições grandes e operações complexas, como categorização, não são suportadas.</span><span class="sxs-lookup"><span data-stu-id="ed9cc-141">Large restrictions and complex operations such as categorization are not supported.</span></span> 
  
<span data-ttu-id="ed9cc-142">Objetos de dados de tabela identificam linhas usando uma coluna de índice, uma propriedade que tem a garantia de ter um valor exclusivo para cada linha.</span><span class="sxs-lookup"><span data-stu-id="ed9cc-142">Table data objects identify rows by using an index column, a property that is guaranteed to have a unique value for each row.</span></span> <span data-ttu-id="ed9cc-143">A maioria dos provedores de serviços usa a propriedade **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) como a coluna de índice.</span><span class="sxs-lookup"><span data-stu-id="ed9cc-143">Most service providers use the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property as the index column.</span></span> <span data-ttu-id="ed9cc-144">Propriedades que têm vários valores não podem ser usadas como uma coluna de índice.</span><span class="sxs-lookup"><span data-stu-id="ed9cc-144">Properties that have multiple values cannot be used as an index column.</span></span>
  
<span data-ttu-id="ed9cc-145">Os objetos de dados de tabela geram uma única notificação independentemente do número de linhas afetadas por uma alteração ou exclusão.</span><span class="sxs-lookup"><span data-stu-id="ed9cc-145">Table data objects generate a single notification regardless of the number of rows affected by a change or deletion.</span></span> <span data-ttu-id="ed9cc-146">Se uma linha de destino em uma operação não existir, uma linha será adicionada.</span><span class="sxs-lookup"><span data-stu-id="ed9cc-146">If a target row in an operation does not exist, a row is added.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ed9cc-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="ed9cc-147">See also</span></span>



[<span data-ttu-id="ed9cc-148">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="ed9cc-148">MAPI Interfaces</span></span>](mapi-interfaces.md)

