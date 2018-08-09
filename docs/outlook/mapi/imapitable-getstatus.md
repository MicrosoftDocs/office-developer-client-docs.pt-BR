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
ms.openlocfilehash: 6478f2c6c8196fa332a7b019269e6a6266485d1d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767341"
---
# <a name="imapitablegetstatus"></a><span data-ttu-id="1cafc-103">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="1cafc-103">IMAPITable::GetStatus</span></span>

  
  
<span data-ttu-id="1cafc-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1cafc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1cafc-105">Retorna o status e o tipo da tabela.</span><span class="sxs-lookup"><span data-stu-id="1cafc-105">Returns the table's status and type.</span></span>
  
```cpp
HRESULT GetStatus(
ULONG FAR * lpulTableStatus,
ULONG FAR * lpulTableType
);
```

## <a name="parameters"></a><span data-ttu-id="1cafc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1cafc-106">Parameters</span></span>

 <span data-ttu-id="1cafc-107">_lpulTableStatus_</span><span class="sxs-lookup"><span data-stu-id="1cafc-107">_lpulTableStatus_</span></span>
  
> <span data-ttu-id="1cafc-108">[out] Ponteiro para um valor que indica o status da tabela.</span><span class="sxs-lookup"><span data-stu-id="1cafc-108">[out] Pointer to a value indicating the status of the table.</span></span> <span data-ttu-id="1cafc-109">Pode ser retornado um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="1cafc-109">One of the following values can be returned:</span></span>
    
<span data-ttu-id="1cafc-110">TBLSTAT_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="1cafc-110">TBLSTAT_COMPLETE</span></span> 
  
> <span data-ttu-id="1cafc-111">Nenhuma operações estejam em andamento.</span><span class="sxs-lookup"><span data-stu-id="1cafc-111">No operations are in progress.</span></span>
    
<span data-ttu-id="1cafc-112">TBLSTAT_QCHANGED</span><span class="sxs-lookup"><span data-stu-id="1cafc-112">TBLSTAT_QCHANGED</span></span> 
  
> <span data-ttu-id="1cafc-113">O conteúdo da tabela expectantly foram alteradas.</span><span class="sxs-lookup"><span data-stu-id="1cafc-113">The contents of the table have expectantly changed.</span></span> <span data-ttu-id="1cafc-114">Esse valor de status não será retornado para que as alterações resultantes das operações de classificação ou restrição.</span><span class="sxs-lookup"><span data-stu-id="1cafc-114">This status value is not returned for changes that result from sort or restriction operations.</span></span>
    
<span data-ttu-id="1cafc-115">TBLSTAT_RESTRICT_ERROR</span><span class="sxs-lookup"><span data-stu-id="1cafc-115">TBLSTAT_RESTRICT_ERROR</span></span> 
  
> <span data-ttu-id="1cafc-116">Ocorreu um erro durante uma operação [IMAPITable:: Restrict](imapitable-restrict.md) .</span><span class="sxs-lookup"><span data-stu-id="1cafc-116">An error occurred during an [IMAPITable::Restrict](imapitable-restrict.md) operation.</span></span> 
    
<span data-ttu-id="1cafc-117">TBLSTAT_RESTRICTING</span><span class="sxs-lookup"><span data-stu-id="1cafc-117">TBLSTAT_RESTRICTING</span></span> 
  
> <span data-ttu-id="1cafc-118">Uma operação **IMAPITable:: Restrict** está em andamento.</span><span class="sxs-lookup"><span data-stu-id="1cafc-118">An **IMAPITable::Restrict** operation is in progress.</span></span> 
    
<span data-ttu-id="1cafc-119">TBLSTAT_SETCOL_ERROR</span><span class="sxs-lookup"><span data-stu-id="1cafc-119">TBLSTAT_SETCOL_ERROR</span></span> 
  
> <span data-ttu-id="1cafc-120">Ocorreu um erro durante uma operação de [IMAPITable::SetColumns](imapitable-setcolumns.md) .</span><span class="sxs-lookup"><span data-stu-id="1cafc-120">An error occurred during an [IMAPITable::SetColumns](imapitable-setcolumns.md) operation.</span></span> 
    
<span data-ttu-id="1cafc-121">TBLSTAT_SETTING_COLS</span><span class="sxs-lookup"><span data-stu-id="1cafc-121">TBLSTAT_SETTING_COLS</span></span> 
  
> <span data-ttu-id="1cafc-122">Uma operação **IMAPITable::SetColumns** está em andamento.</span><span class="sxs-lookup"><span data-stu-id="1cafc-122">An **IMAPITable::SetColumns** operation is in progress.</span></span> 
    
<span data-ttu-id="1cafc-123">TBLSTAT_SORT_ERROR</span><span class="sxs-lookup"><span data-stu-id="1cafc-123">TBLSTAT_SORT_ERROR</span></span> 
  
> <span data-ttu-id="1cafc-124">Ocorreu um erro durante uma operação [IMAPITable:: SortTable](imapitable-sorttable.md) .</span><span class="sxs-lookup"><span data-stu-id="1cafc-124">An error occurred during an [IMAPITable::SortTable](imapitable-sorttable.md) operation.</span></span> 
    
<span data-ttu-id="1cafc-125">TBLSTAT_SORTING</span><span class="sxs-lookup"><span data-stu-id="1cafc-125">TBLSTAT_SORTING</span></span> 
  
> <span data-ttu-id="1cafc-126">Uma operação **IMAPITable:: SortTable** está em andamento.</span><span class="sxs-lookup"><span data-stu-id="1cafc-126">An **IMAPITable::SortTable** operation is in progress.</span></span> 
    
 <span data-ttu-id="1cafc-127">_lpulTableType_</span><span class="sxs-lookup"><span data-stu-id="1cafc-127">_lpulTableType_</span></span>
  
> <span data-ttu-id="1cafc-128">[out] Ponteiro para um valor que indica o tipo de tabela.</span><span class="sxs-lookup"><span data-stu-id="1cafc-128">[out] Pointer to a value that indicates the table's type.</span></span> <span data-ttu-id="1cafc-129">Um dos seguintes tipos de três tabela pode ser retornado:</span><span class="sxs-lookup"><span data-stu-id="1cafc-129">One of the following three table types can be returned:</span></span>
    
<span data-ttu-id="1cafc-130">TBLTYPE_DYNAMIC</span><span class="sxs-lookup"><span data-stu-id="1cafc-130">TBLTYPE_DYNAMIC</span></span> 
  
> <span data-ttu-id="1cafc-131">O conteúdo da tabela é dinâmico; as linhas e os valores de coluna podem alterar como as alterações de dados subjacente.</span><span class="sxs-lookup"><span data-stu-id="1cafc-131">The table's contents are dynamic; the rows and column values can change as the underlying data changes.</span></span>
    
<span data-ttu-id="1cafc-132">TBLTYPE_KEYSET</span><span class="sxs-lookup"><span data-stu-id="1cafc-132">TBLTYPE_KEYSET</span></span> 
  
> <span data-ttu-id="1cafc-133">As linhas dentro da tabela são corrigidas, mas os valores das colunas dentro nessas linhas são dinâmicos e podem alterar como as alterações de dados subjacente.</span><span class="sxs-lookup"><span data-stu-id="1cafc-133">The rows within the table are fixed, but the values of the columns within these rows are dynamic and can change as the underlying data changes.</span></span>
    
<span data-ttu-id="1cafc-134">TBLTYPE_SNAPSHOT</span><span class="sxs-lookup"><span data-stu-id="1cafc-134">TBLTYPE_SNAPSHOT</span></span> 
  
> <span data-ttu-id="1cafc-135">A tabela é estática e seu conteúdo não é alterados quando os dados subjacentes forem alterados.</span><span class="sxs-lookup"><span data-stu-id="1cafc-135">The table is static, and its contents do not change when the underlying data changes.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1cafc-136">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="1cafc-136">Return value</span></span>

<span data-ttu-id="1cafc-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="1cafc-137">S_OK</span></span> 
  
> <span data-ttu-id="1cafc-138">Status da tabela foi retornado com êxito.</span><span class="sxs-lookup"><span data-stu-id="1cafc-138">The table's status was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1cafc-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="1cafc-139">Remarks</span></span>

<span data-ttu-id="1cafc-140">O método **IMAPTable::GetStatus** recupera informações sobre o tipo e o status atual de uma tabela.</span><span class="sxs-lookup"><span data-stu-id="1cafc-140">The **IMAPTable::GetStatus** method retrieves information about a table's type and current status.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1cafc-141">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="1cafc-141">Notes to callers</span></span>

<span data-ttu-id="1cafc-142">Você pode usar **GetStatus** junto com três outros métodos **IMAPITable** para monitorar o status dessas operações e determinar o efeito sobre a tabela.</span><span class="sxs-lookup"><span data-stu-id="1cafc-142">You can use **GetStatus** in conjunction with three other **IMAPITable** methods to monitor the status of those operations and determine the effect on the table.</span></span> <span data-ttu-id="1cafc-143">Chame **GetStatus** depois de fazer uma das seguintes chamadas **IMAPITable** :</span><span class="sxs-lookup"><span data-stu-id="1cafc-143">Call **GetStatus** after making one of the following **IMAPITable** calls:</span></span> 
  
- <span data-ttu-id="1cafc-144">[IMAPITable:: Restrict](imapitable-restrict.md) para definir uma restrição.</span><span class="sxs-lookup"><span data-stu-id="1cafc-144">[IMAPITable::Restrict](imapitable-restrict.md) to set a restriction.</span></span> 
    
- <span data-ttu-id="1cafc-145">[IMAPITable:: SortTable](imapitable-sorttable.md) para estabelecer uma ordem de classificação.</span><span class="sxs-lookup"><span data-stu-id="1cafc-145">[IMAPITable::SortTable](imapitable-sorttable.md) to establish a sort order.</span></span> 
    
- <span data-ttu-id="1cafc-146">[IMAPITable::SetColumns](imapitable-setcolumns.md) para definir um conjunto de coluna.</span><span class="sxs-lookup"><span data-stu-id="1cafc-146">[IMAPITable::SetColumns](imapitable-setcolumns.md) to define a column set.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="1cafc-147">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="1cafc-147">MFCMAPI reference</span></span>

<span data-ttu-id="1cafc-148">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="1cafc-148">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1cafc-149">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="1cafc-149">**File**</span></span>|<span data-ttu-id="1cafc-150">**Function**</span><span class="sxs-lookup"><span data-stu-id="1cafc-150">**Function**</span></span>|<span data-ttu-id="1cafc-151">**Comment**</span><span class="sxs-lookup"><span data-stu-id="1cafc-151">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1cafc-152">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="1cafc-152">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="1cafc-153">CContentsTableListCtrl::GetStatus</span><span class="sxs-lookup"><span data-stu-id="1cafc-153">CContentsTableListCtrl::GetStatus</span></span>  <br/> |<span data-ttu-id="1cafc-154">MFCMAPI usa o método **IMAPITable::GetStatus** para informar o status de uma tabela.</span><span class="sxs-lookup"><span data-stu-id="1cafc-154">MFCMAPI uses the **IMAPITable::GetStatus** method to report the status of a table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1cafc-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="1cafc-155">See also</span></span>



[<span data-ttu-id="1cafc-156">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="1cafc-156">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="1cafc-157">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="1cafc-157">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="1cafc-158">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="1cafc-158">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="1cafc-159">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1cafc-159">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="1cafc-160">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="1cafc-160">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

