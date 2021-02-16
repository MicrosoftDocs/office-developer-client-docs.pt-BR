---
title: IMAPITableGetStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetStatus
api_type:
- COM
ms.assetid: f114f1fa-bc05-4587-875b-71548c5912ea
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ec305fc872d1bf1718592dabdd230617d50d3f54
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434330"
---
# <a name="imapitablegetstatus"></a><span data-ttu-id="f080f-103">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="f080f-103">IMAPITable::GetStatus</span></span>

  
  
<span data-ttu-id="f080f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f080f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f080f-105">Retorna o status e o tipo da tabela.</span><span class="sxs-lookup"><span data-stu-id="f080f-105">Returns the table's status and type.</span></span>
  
```cpp
HRESULT GetStatus(
ULONG FAR * lpulTableStatus,
ULONG FAR * lpulTableType
);
```

## <a name="parameters"></a><span data-ttu-id="f080f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f080f-106">Parameters</span></span>

 <span data-ttu-id="f080f-107">_lpulTableStatus_</span><span class="sxs-lookup"><span data-stu-id="f080f-107">_lpulTableStatus_</span></span>
  
> <span data-ttu-id="f080f-108">[out] Ponteiro para um valor que indica o status da tabela.</span><span class="sxs-lookup"><span data-stu-id="f080f-108">[out] Pointer to a value indicating the status of the table.</span></span> <span data-ttu-id="f080f-109">Um dos seguintes valores pode ser retornado:</span><span class="sxs-lookup"><span data-stu-id="f080f-109">One of the following values can be returned:</span></span>
    
<span data-ttu-id="f080f-110">TBLSTAT_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="f080f-110">TBLSTAT_COMPLETE</span></span> 
  
> <span data-ttu-id="f080f-111">Nenhuma operação está em andamento.</span><span class="sxs-lookup"><span data-stu-id="f080f-111">No operations are in progress.</span></span>
    
<span data-ttu-id="f080f-112">TBLSTAT_QCHANGED</span><span class="sxs-lookup"><span data-stu-id="f080f-112">TBLSTAT_QCHANGED</span></span> 
  
> <span data-ttu-id="f080f-113">O conteúdo da tabela foi alterado de forma esperada.</span><span class="sxs-lookup"><span data-stu-id="f080f-113">The contents of the table have expectantly changed.</span></span> <span data-ttu-id="f080f-114">Esse valor de status não é retornado para alterações resultantes de operações de classificação ou restrição.</span><span class="sxs-lookup"><span data-stu-id="f080f-114">This status value is not returned for changes that result from sort or restriction operations.</span></span>
    
<span data-ttu-id="f080f-115">TBLSTAT_RESTRICT_ERROR</span><span class="sxs-lookup"><span data-stu-id="f080f-115">TBLSTAT_RESTRICT_ERROR</span></span> 
  
> <span data-ttu-id="f080f-116">Ocorreu um erro durante uma [operação IMAPITable::Restrict.](imapitable-restrict.md)</span><span class="sxs-lookup"><span data-stu-id="f080f-116">An error occurred during an [IMAPITable::Restrict](imapitable-restrict.md) operation.</span></span> 
    
<span data-ttu-id="f080f-117">TBLSTAT_RESTRICTING</span><span class="sxs-lookup"><span data-stu-id="f080f-117">TBLSTAT_RESTRICTING</span></span> 
  
> <span data-ttu-id="f080f-118">Uma **operação IMAPITable::Restrict** está em andamento.</span><span class="sxs-lookup"><span data-stu-id="f080f-118">An **IMAPITable::Restrict** operation is in progress.</span></span> 
    
<span data-ttu-id="f080f-119">TBLSTAT_SETCOL_ERROR</span><span class="sxs-lookup"><span data-stu-id="f080f-119">TBLSTAT_SETCOL_ERROR</span></span> 
  
> <span data-ttu-id="f080f-120">Ocorreu um erro durante uma [operação IMAPITable::SetColumns.](imapitable-setcolumns.md)</span><span class="sxs-lookup"><span data-stu-id="f080f-120">An error occurred during an [IMAPITable::SetColumns](imapitable-setcolumns.md) operation.</span></span> 
    
<span data-ttu-id="f080f-121">TBLSTAT_SETTING_COLS</span><span class="sxs-lookup"><span data-stu-id="f080f-121">TBLSTAT_SETTING_COLS</span></span> 
  
> <span data-ttu-id="f080f-122">Uma **operação IMAPITable::SetColumns** está em andamento.</span><span class="sxs-lookup"><span data-stu-id="f080f-122">An **IMAPITable::SetColumns** operation is in progress.</span></span> 
    
<span data-ttu-id="f080f-123">TBLSTAT_SORT_ERROR</span><span class="sxs-lookup"><span data-stu-id="f080f-123">TBLSTAT_SORT_ERROR</span></span> 
  
> <span data-ttu-id="f080f-124">Ocorreu um erro durante uma [operação IMAPITable::SortTable.](imapitable-sorttable.md)</span><span class="sxs-lookup"><span data-stu-id="f080f-124">An error occurred during an [IMAPITable::SortTable](imapitable-sorttable.md) operation.</span></span> 
    
<span data-ttu-id="f080f-125">TBLSTAT_SORTING</span><span class="sxs-lookup"><span data-stu-id="f080f-125">TBLSTAT_SORTING</span></span> 
  
> <span data-ttu-id="f080f-126">Uma **operação IMAPITable::SortTable** está em andamento.</span><span class="sxs-lookup"><span data-stu-id="f080f-126">An **IMAPITable::SortTable** operation is in progress.</span></span> 
    
 <span data-ttu-id="f080f-127">_lpulTableType_</span><span class="sxs-lookup"><span data-stu-id="f080f-127">_lpulTableType_</span></span>
  
> <span data-ttu-id="f080f-128">[out] Ponteiro para um valor que indica o tipo da tabela.</span><span class="sxs-lookup"><span data-stu-id="f080f-128">[out] Pointer to a value that indicates the table's type.</span></span> <span data-ttu-id="f080f-129">Um dos três tipos de tabela a seguir pode ser retornado:</span><span class="sxs-lookup"><span data-stu-id="f080f-129">One of the following three table types can be returned:</span></span>
    
<span data-ttu-id="f080f-130">TBLTYPE_DYNAMIC</span><span class="sxs-lookup"><span data-stu-id="f080f-130">TBLTYPE_DYNAMIC</span></span> 
  
> <span data-ttu-id="f080f-131">O conteúdo do índice é dinâmico; as linhas e os valores de coluna podem mudar à medida que os dados subjacentes mudam.</span><span class="sxs-lookup"><span data-stu-id="f080f-131">The table's contents are dynamic; the rows and column values can change as the underlying data changes.</span></span>
    
<span data-ttu-id="f080f-132">TBLTYPE_KEYSET</span><span class="sxs-lookup"><span data-stu-id="f080f-132">TBLTYPE_KEYSET</span></span> 
  
> <span data-ttu-id="f080f-133">As linhas dentro da tabela são fixas, mas os valores das colunas dentro dessas linhas são dinâmicos e podem mudar à medida que os dados subjacentes mudam.</span><span class="sxs-lookup"><span data-stu-id="f080f-133">The rows within the table are fixed, but the values of the columns within these rows are dynamic and can change as the underlying data changes.</span></span>
    
<span data-ttu-id="f080f-134">TBLTYPE_SNAPSHOT</span><span class="sxs-lookup"><span data-stu-id="f080f-134">TBLTYPE_SNAPSHOT</span></span> 
  
> <span data-ttu-id="f080f-135">A tabela é estática e seu conteúdo não muda quando os dados subjacentes mudam.</span><span class="sxs-lookup"><span data-stu-id="f080f-135">The table is static, and its contents do not change when the underlying data changes.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f080f-136">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f080f-136">Return value</span></span>

<span data-ttu-id="f080f-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="f080f-137">S_OK</span></span> 
  
> <span data-ttu-id="f080f-138">O status da tabela foi retornado com êxito.</span><span class="sxs-lookup"><span data-stu-id="f080f-138">The table's status was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f080f-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="f080f-139">Remarks</span></span>

<span data-ttu-id="f080f-140">O **método IMAPTable::GetStatus** recupera informações sobre o tipo e o status atual de uma tabela.</span><span class="sxs-lookup"><span data-stu-id="f080f-140">The **IMAPTable::GetStatus** method retrieves information about a table's type and current status.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f080f-141">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="f080f-141">Notes to callers</span></span>

<span data-ttu-id="f080f-142">Você pode usar **GetStatus** em conjunto com três outros métodos **IMAPITable** para monitorar o status dessas operações e determinar o efeito na tabela.</span><span class="sxs-lookup"><span data-stu-id="f080f-142">You can use **GetStatus** in conjunction with three other **IMAPITable** methods to monitor the status of those operations and determine the effect on the table.</span></span> <span data-ttu-id="f080f-143">Chame **GetStatus** depois de fazer uma das seguintes **chamadas IMAPITable:**</span><span class="sxs-lookup"><span data-stu-id="f080f-143">Call **GetStatus** after making one of the following **IMAPITable** calls:</span></span> 
  
- <span data-ttu-id="f080f-144">[IMAPITable::Restrict](imapitable-restrict.md) para definir uma restrição.</span><span class="sxs-lookup"><span data-stu-id="f080f-144">[IMAPITable::Restrict](imapitable-restrict.md) to set a restriction.</span></span> 
    
- <span data-ttu-id="f080f-145">[IMAPITable::SortTable](imapitable-sorttable.md) para estabelecer uma ordem de classificação.</span><span class="sxs-lookup"><span data-stu-id="f080f-145">[IMAPITable::SortTable](imapitable-sorttable.md) to establish a sort order.</span></span> 
    
- <span data-ttu-id="f080f-146">[IMAPITable::SetColumns](imapitable-setcolumns.md) para definir um conjunto de colunas.</span><span class="sxs-lookup"><span data-stu-id="f080f-146">[IMAPITable::SetColumns](imapitable-setcolumns.md) to define a column set.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="f080f-147">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f080f-147">MFCMAPI reference</span></span>

<span data-ttu-id="f080f-148">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f080f-148">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f080f-149">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="f080f-149">**File**</span></span>|<span data-ttu-id="f080f-150">**Função**</span><span class="sxs-lookup"><span data-stu-id="f080f-150">**Function**</span></span>|<span data-ttu-id="f080f-151">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="f080f-151">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f080f-152">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="f080f-152">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="f080f-153">CContentsTableListCtrl::GetStatus</span><span class="sxs-lookup"><span data-stu-id="f080f-153">CContentsTableListCtrl::GetStatus</span></span>  <br/> |<span data-ttu-id="f080f-154">MFCMAPI usa o **método IMAPITable::GetStatus** para relatar o status de uma tabela.</span><span class="sxs-lookup"><span data-stu-id="f080f-154">MFCMAPI uses the **IMAPITable::GetStatus** method to report the status of a table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f080f-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="f080f-155">See also</span></span>



[<span data-ttu-id="f080f-156">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="f080f-156">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="f080f-157">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="f080f-157">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="f080f-158">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="f080f-158">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="f080f-159">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f080f-159">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="f080f-160">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="f080f-160">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

