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
ms.openlocfilehash: 968768fe75286b93bf12e349a4845fdfaa1923e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767724"
---
# <a name="itabledata--iunknown"></a><span data-ttu-id="42a1b-103">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="42a1b-103">ITableData : IUnknown</span></span>

  
  
<span data-ttu-id="42a1b-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="42a1b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="42a1b-105">Fornece os métodos de utilitário para trabalhar com tabelas.</span><span class="sxs-lookup"><span data-stu-id="42a1b-105">Provides utility methods for working with tables.</span></span> <span data-ttu-id="42a1b-106">MAPI fornece objetos de dados de tabela ou objetos que implementam **ITableData** para ajudar a executar manutenção da tabela de provedores de serviços.</span><span class="sxs-lookup"><span data-stu-id="42a1b-106">MAPI provides table data objects or objects that implement **ITableData** to help service providers perform table maintenance.</span></span> <span data-ttu-id="42a1b-107">Para obter um objeto de dados de tabela, provedores de serviços de chamarem a função de [CreateTable](createtable.md) .</span><span class="sxs-lookup"><span data-stu-id="42a1b-107">To obtain a table data object, service providers call the [CreateTable](createtable.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="42a1b-108">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="42a1b-108">Header file:</span></span>  <br/> |<span data-ttu-id="42a1b-109">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="42a1b-109">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="42a1b-110">Expostos pelo:</span><span class="sxs-lookup"><span data-stu-id="42a1b-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="42a1b-111">Objetos de dados de tabela</span><span class="sxs-lookup"><span data-stu-id="42a1b-111">Table data objects</span></span>  <br/> |
|<span data-ttu-id="42a1b-112">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="42a1b-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="42a1b-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="42a1b-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="42a1b-114">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="42a1b-114">Called by:</span></span>  <br/> |<span data-ttu-id="42a1b-115">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="42a1b-115">Service providers</span></span>  <br/> |
|<span data-ttu-id="42a1b-116">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="42a1b-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="42a1b-117">IID_IMAPITableData</span><span class="sxs-lookup"><span data-stu-id="42a1b-117">IID_IMAPITableData</span></span>  <br/> |
|<span data-ttu-id="42a1b-118">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="42a1b-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="42a1b-119">LPTABLEDATA</span><span class="sxs-lookup"><span data-stu-id="42a1b-119">LPTABLEDATA</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="42a1b-120">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="42a1b-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="42a1b-121">HrGetView</span><span class="sxs-lookup"><span data-stu-id="42a1b-121">HrGetView</span></span>](itabledata-hrgetview.md) <br/> |<span data-ttu-id="42a1b-122">Cria um modo de exibição de tabela, retornando um ponteiro para uma implementação [IMAPITable](imapitableiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="42a1b-122">Creates a table view, returning a pointer to an [IMAPITable](imapitableiunknown.md) implementation.</span></span>  <br/> |
|[<span data-ttu-id="42a1b-123">HrModifyRow</span><span class="sxs-lookup"><span data-stu-id="42a1b-123">HrModifyRow</span></span>](itabledata-hrmodifyrow.md) <br/> |<span data-ttu-id="42a1b-124">Insere uma nova linha de tabela, possivelmente, substituindo uma linha existente.</span><span class="sxs-lookup"><span data-stu-id="42a1b-124">Inserts a new table row, possibly replacing an existing row.</span></span>  <br/> |
|[<span data-ttu-id="42a1b-125">HrDeleteRow</span><span class="sxs-lookup"><span data-stu-id="42a1b-125">HrDeleteRow</span></span>](itabledata-hrdeleterow.md) <br/> |<span data-ttu-id="42a1b-126">Exclui uma linha da tabela.</span><span class="sxs-lookup"><span data-stu-id="42a1b-126">Deletes a table row.</span></span>  <br/> |
|[<span data-ttu-id="42a1b-127">HrQueryRow</span><span class="sxs-lookup"><span data-stu-id="42a1b-127">HrQueryRow</span></span>](itabledata-hrqueryrow.md) <br/> |<span data-ttu-id="42a1b-128">Recupera uma linha da tabela.</span><span class="sxs-lookup"><span data-stu-id="42a1b-128">Retrieves a table row.</span></span>  <br/> |
|[<span data-ttu-id="42a1b-129">HrEnumRow</span><span class="sxs-lookup"><span data-stu-id="42a1b-129">HrEnumRow</span></span>](itabledata-hrenumrow.md) <br/> |<span data-ttu-id="42a1b-130">Recupera uma linha com base em sua posição na tabela.</span><span class="sxs-lookup"><span data-stu-id="42a1b-130">Retrieves a row based on its position in the table.</span></span>  <br/> |
|[<span data-ttu-id="42a1b-131">HrNotify</span><span class="sxs-lookup"><span data-stu-id="42a1b-131">HrNotify</span></span>](itabledata-hrnotify.md) <br/> |<span data-ttu-id="42a1b-132">Envia uma notificação para uma linha da tabela.</span><span class="sxs-lookup"><span data-stu-id="42a1b-132">Sends a notification for a table row.</span></span>  <br/> |
|[<span data-ttu-id="42a1b-133">HrInsertRow</span><span class="sxs-lookup"><span data-stu-id="42a1b-133">HrInsertRow</span></span>](itabledata-hrinsertrow.md) <br/> |<span data-ttu-id="42a1b-134">Insere uma linha de tabela.</span><span class="sxs-lookup"><span data-stu-id="42a1b-134">Inserts a table row.</span></span>  <br/> |
|[<span data-ttu-id="42a1b-135">HrModifyRows</span><span class="sxs-lookup"><span data-stu-id="42a1b-135">HrModifyRows</span></span>](itabledata-hrmodifyrows.md) <br/> |<span data-ttu-id="42a1b-136">Insere várias linhas de tabela, substituindo possivelmente linhas existentes.</span><span class="sxs-lookup"><span data-stu-id="42a1b-136">Inserts multiple table rows, possibly replacing existing rows.</span></span>  <br/> |
|[<span data-ttu-id="42a1b-137">HrDeleteRows</span><span class="sxs-lookup"><span data-stu-id="42a1b-137">HrDeleteRows</span></span>](itabledata-hrdeleterows.md) <br/> |<span data-ttu-id="42a1b-138">Exclui a várias linhas de tabela.</span><span class="sxs-lookup"><span data-stu-id="42a1b-138">Deletes multiple table rows.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="42a1b-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="42a1b-139">Remarks</span></span>

<span data-ttu-id="42a1b-140">A implementação de MAPI do **ITableData** funciona com tabelas, mantendo todos os dados e qualquer restrição associada na memória, tornando-o inadequados para uso com tabelas muito grandes.</span><span class="sxs-lookup"><span data-stu-id="42a1b-140">The MAPI implementation of **ITableData** works with tables by holding all of the data and any associated restrictions in memory, making it unsuitable for use with very large tables.</span></span> <span data-ttu-id="42a1b-141">Restrições de grandes e operações complexas, como categorização não são suportadas.</span><span class="sxs-lookup"><span data-stu-id="42a1b-141">Large restrictions and complex operations such as categorization are not supported.</span></span> 
  
<span data-ttu-id="42a1b-142">Objetos de dados de tabela identificam linhas usando uma coluna de índice, uma propriedade que é garantida que tenha um valor exclusivo para cada linha.</span><span class="sxs-lookup"><span data-stu-id="42a1b-142">Table data objects identify rows by using an index column, a property that is guaranteed to have a unique value for each row.</span></span> <span data-ttu-id="42a1b-143">A maioria dos provedores de serviço use a propriedade **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) como a coluna de índice.</span><span class="sxs-lookup"><span data-stu-id="42a1b-143">Most service providers use the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property as the index column.</span></span> <span data-ttu-id="42a1b-144">Propriedades com vários valores não podem ser usadas como uma coluna de índice.</span><span class="sxs-lookup"><span data-stu-id="42a1b-144">Properties that have multiple values cannot be used as an index column.</span></span>
  
<span data-ttu-id="42a1b-145">Objetos de dados de tabela geram uma única notificação, independentemente do número de linhas afetadas por uma alteração ou exclusão.</span><span class="sxs-lookup"><span data-stu-id="42a1b-145">Table data objects generate a single notification regardless of the number of rows affected by a change or deletion.</span></span> <span data-ttu-id="42a1b-146">Se não existir uma linha de destino em uma operação, uma linha será adicionada.</span><span class="sxs-lookup"><span data-stu-id="42a1b-146">If a target row in an operation does not exist, a row is added.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="42a1b-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="42a1b-147">See also</span></span>



[<span data-ttu-id="42a1b-148">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="42a1b-148">MAPI Interfaces</span></span>](mapi-interfaces.md)

