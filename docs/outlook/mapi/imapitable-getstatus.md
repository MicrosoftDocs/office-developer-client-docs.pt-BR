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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328893"
---
# <a name="imapitablegetstatus"></a><span data-ttu-id="4ba24-103">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="4ba24-103">IMAPITable::GetStatus</span></span>

  
  
<span data-ttu-id="4ba24-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4ba24-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4ba24-105">Retorna o tipo e o status da tabela.</span><span class="sxs-lookup"><span data-stu-id="4ba24-105">Returns the table's status and type.</span></span>
  
```cpp
HRESULT GetStatus(
ULONG FAR * lpulTableStatus,
ULONG FAR * lpulTableType
);
```

## <a name="parameters"></a><span data-ttu-id="4ba24-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4ba24-106">Parameters</span></span>

 <span data-ttu-id="4ba24-107">_lpulTableStatus_</span><span class="sxs-lookup"><span data-stu-id="4ba24-107">_lpulTableStatus_</span></span>
  
> <span data-ttu-id="4ba24-108">bota Ponteiro para um valor que indica o status da tabela.</span><span class="sxs-lookup"><span data-stu-id="4ba24-108">[out] Pointer to a value indicating the status of the table.</span></span> <span data-ttu-id="4ba24-109">Um dos valores a seguir pode ser retornado:</span><span class="sxs-lookup"><span data-stu-id="4ba24-109">One of the following values can be returned:</span></span>
    
<span data-ttu-id="4ba24-110">TBLSTAT_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="4ba24-110">TBLSTAT_COMPLETE</span></span> 
  
> <span data-ttu-id="4ba24-111">Nenhuma operação está em andamento.</span><span class="sxs-lookup"><span data-stu-id="4ba24-111">No operations are in progress.</span></span>
    
<span data-ttu-id="4ba24-112">TBLSTAT_QCHANGED</span><span class="sxs-lookup"><span data-stu-id="4ba24-112">TBLSTAT_QCHANGED</span></span> 
  
> <span data-ttu-id="4ba24-113">O conteúdo da tabela tem expectantly alterado.</span><span class="sxs-lookup"><span data-stu-id="4ba24-113">The contents of the table have expectantly changed.</span></span> <span data-ttu-id="4ba24-114">Esse valor de status não é retornado para alterações resultantes de operações de classificação ou restrição.</span><span class="sxs-lookup"><span data-stu-id="4ba24-114">This status value is not returned for changes that result from sort or restriction operations.</span></span>
    
<span data-ttu-id="4ba24-115">TBLSTAT_RESTRICT_ERROR</span><span class="sxs-lookup"><span data-stu-id="4ba24-115">TBLSTAT_RESTRICT_ERROR</span></span> 
  
> <span data-ttu-id="4ba24-116">Ocorreu um erro durante uma operação imApitable [:: Restrict](imapitable-restrict.md) .</span><span class="sxs-lookup"><span data-stu-id="4ba24-116">An error occurred during an [IMAPITable::Restrict](imapitable-restrict.md) operation.</span></span> 
    
<span data-ttu-id="4ba24-117">TBLSTAT_RESTRICTING</span><span class="sxs-lookup"><span data-stu-id="4ba24-117">TBLSTAT_RESTRICTING</span></span> 
  
> <span data-ttu-id="4ba24-118">Uma operação imApitable **:: Restrict** está em andamento.</span><span class="sxs-lookup"><span data-stu-id="4ba24-118">An **IMAPITable::Restrict** operation is in progress.</span></span> 
    
<span data-ttu-id="4ba24-119">TBLSTAT_SETCOL_ERROR</span><span class="sxs-lookup"><span data-stu-id="4ba24-119">TBLSTAT_SETCOL_ERROR</span></span> 
  
> <span data-ttu-id="4ba24-120">Ocorreu um erro durante uma operação imApitable [::](imapitable-setcolumns.md) SetColumns.</span><span class="sxs-lookup"><span data-stu-id="4ba24-120">An error occurred during an [IMAPITable::SetColumns](imapitable-setcolumns.md) operation.</span></span> 
    
<span data-ttu-id="4ba24-121">TBLSTAT_SETTING_COLS</span><span class="sxs-lookup"><span data-stu-id="4ba24-121">TBLSTAT_SETTING_COLS</span></span> 
  
> <span data-ttu-id="4ba24-122">Uma operação imApitable **::** SetColumns está em andamento.</span><span class="sxs-lookup"><span data-stu-id="4ba24-122">An **IMAPITable::SetColumns** operation is in progress.</span></span> 
    
<span data-ttu-id="4ba24-123">TBLSTAT_SORT_ERROR</span><span class="sxs-lookup"><span data-stu-id="4ba24-123">TBLSTAT_SORT_ERROR</span></span> 
  
> <span data-ttu-id="4ba24-124">Ocorreu um erro durante uma operação imApitable [:: SortTable](imapitable-sorttable.md) .</span><span class="sxs-lookup"><span data-stu-id="4ba24-124">An error occurred during an [IMAPITable::SortTable](imapitable-sorttable.md) operation.</span></span> 
    
<span data-ttu-id="4ba24-125">TBLSTAT_SORTING</span><span class="sxs-lookup"><span data-stu-id="4ba24-125">TBLSTAT_SORTING</span></span> 
  
> <span data-ttu-id="4ba24-126">Uma operação imApitable **:: SortTable** está em andamento.</span><span class="sxs-lookup"><span data-stu-id="4ba24-126">An **IMAPITable::SortTable** operation is in progress.</span></span> 
    
 <span data-ttu-id="4ba24-127">_lpulTableType_</span><span class="sxs-lookup"><span data-stu-id="4ba24-127">_lpulTableType_</span></span>
  
> <span data-ttu-id="4ba24-128">bota Ponteiro para um valor que indica o tipo da tabela.</span><span class="sxs-lookup"><span data-stu-id="4ba24-128">[out] Pointer to a value that indicates the table's type.</span></span> <span data-ttu-id="4ba24-129">Um dos três tipos de tabela a seguir pode ser retornado:</span><span class="sxs-lookup"><span data-stu-id="4ba24-129">One of the following three table types can be returned:</span></span>
    
<span data-ttu-id="4ba24-130">TBLTYPE_DYNAMIC</span><span class="sxs-lookup"><span data-stu-id="4ba24-130">TBLTYPE_DYNAMIC</span></span> 
  
> <span data-ttu-id="4ba24-131">O conteúdo da tabela é dinâmico; os valores de linhas e colunas podem ser alterados à medida que os dados subjacentes são alterados.</span><span class="sxs-lookup"><span data-stu-id="4ba24-131">The table's contents are dynamic; the rows and column values can change as the underlying data changes.</span></span>
    
<span data-ttu-id="4ba24-132">TBLTYPE_KEYSET</span><span class="sxs-lookup"><span data-stu-id="4ba24-132">TBLTYPE_KEYSET</span></span> 
  
> <span data-ttu-id="4ba24-133">As linhas dentro da tabela são corrigidas, mas os valores das colunas dentro dessas linhas são dinâmicos e podem ser alterados à medida que os dados subjacentes são alterados.</span><span class="sxs-lookup"><span data-stu-id="4ba24-133">The rows within the table are fixed, but the values of the columns within these rows are dynamic and can change as the underlying data changes.</span></span>
    
<span data-ttu-id="4ba24-134">TBLTYPE_SNAPSHOT</span><span class="sxs-lookup"><span data-stu-id="4ba24-134">TBLTYPE_SNAPSHOT</span></span> 
  
> <span data-ttu-id="4ba24-135">A tabela é estática, e seu conteúdo não é alterado quando os dados subjacentes são alterados.</span><span class="sxs-lookup"><span data-stu-id="4ba24-135">The table is static, and its contents do not change when the underlying data changes.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4ba24-136">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="4ba24-136">Return value</span></span>

<span data-ttu-id="4ba24-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="4ba24-137">S_OK</span></span> 
  
> <span data-ttu-id="4ba24-138">O status da tabela foi retornado com êxito.</span><span class="sxs-lookup"><span data-stu-id="4ba24-138">The table's status was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4ba24-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="4ba24-139">Remarks</span></span>

<span data-ttu-id="4ba24-140">O método **imaptable:: GetStatus** recupera informações sobre o tipo de tabela e o status atual.</span><span class="sxs-lookup"><span data-stu-id="4ba24-140">The **IMAPTable::GetStatus** method retrieves information about a table's type and current status.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="4ba24-141">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="4ba24-141">Notes to callers</span></span>

<span data-ttu-id="4ba24-142">Você pode usar **GetStatus** em conjunto com três outros \*\*\*\* métodos IMAPITable para monitorar o status dessas operações e determinar o efeito sobre a tabela.</span><span class="sxs-lookup"><span data-stu-id="4ba24-142">You can use **GetStatus** in conjunction with three other **IMAPITable** methods to monitor the status of those operations and determine the effect on the table.</span></span> <span data-ttu-id="4ba24-143">Chame **GetStatus** após fazer uma das seguintes chamadas \*\*\*\* IMAPITable:</span><span class="sxs-lookup"><span data-stu-id="4ba24-143">Call **GetStatus** after making one of the following **IMAPITable** calls:</span></span> 
  
- <span data-ttu-id="4ba24-144">[IMAPITable:: strict](imapitable-restrict.md) para definir uma restrição.</span><span class="sxs-lookup"><span data-stu-id="4ba24-144">[IMAPITable::Restrict](imapitable-restrict.md) to set a restriction.</span></span> 
    
- <span data-ttu-id="4ba24-145">[IMAPITable:: SortTable](imapitable-sorttable.md) para estabelecer uma ordem de classificação.</span><span class="sxs-lookup"><span data-stu-id="4ba24-145">[IMAPITable::SortTable](imapitable-sorttable.md) to establish a sort order.</span></span> 
    
- <span data-ttu-id="4ba24-146">[IMAPITable::](imapitable-setcolumns.md) SetColumns para definir um conjunto de colunas.</span><span class="sxs-lookup"><span data-stu-id="4ba24-146">[IMAPITable::SetColumns](imapitable-setcolumns.md) to define a column set.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="4ba24-147">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="4ba24-147">MFCMAPI reference</span></span>

<span data-ttu-id="4ba24-148">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="4ba24-148">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="4ba24-149">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="4ba24-149">**File**</span></span>|<span data-ttu-id="4ba24-150">**Função**</span><span class="sxs-lookup"><span data-stu-id="4ba24-150">**Function**</span></span>|<span data-ttu-id="4ba24-151">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="4ba24-151">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4ba24-152">ContentsTableListCtrl. cpp</span><span class="sxs-lookup"><span data-stu-id="4ba24-152">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="4ba24-153">CContentsTableListCtrl:: GetStatus</span><span class="sxs-lookup"><span data-stu-id="4ba24-153">CContentsTableListCtrl::GetStatus</span></span>  <br/> |<span data-ttu-id="4ba24-154">MFCMAPI usa o método imApitable **:: GetStatus** para relatar o status de uma tabela.</span><span class="sxs-lookup"><span data-stu-id="4ba24-154">MFCMAPI uses the **IMAPITable::GetStatus** method to report the status of a table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4ba24-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="4ba24-155">See also</span></span>



[<span data-ttu-id="4ba24-156">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="4ba24-156">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="4ba24-157">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="4ba24-157">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="4ba24-158">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="4ba24-158">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="4ba24-159">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4ba24-159">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="4ba24-160">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="4ba24-160">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

