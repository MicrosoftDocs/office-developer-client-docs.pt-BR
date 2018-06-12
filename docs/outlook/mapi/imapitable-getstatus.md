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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 6478f2c6c8196fa332a7b019269e6a6266485d1d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767341"
---
# <a name="imapitablegetstatus"></a><span data-ttu-id="9973f-103">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="9973f-103">IMAPITable::GetStatus</span></span>

  
  
<span data-ttu-id="9973f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9973f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9973f-105">Retorna o status e o tipo da tabela.</span><span class="sxs-lookup"><span data-stu-id="9973f-105">Returns the table's status and type.</span></span>
  
```cpp
HRESULT GetStatus(
ULONG FAR * lpulTableStatus,
ULONG FAR * lpulTableType
);
```

## <a name="parameters"></a><span data-ttu-id="9973f-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="9973f-106">Parameters</span></span>

 <span data-ttu-id="9973f-107">_lpulTableStatus_</span><span class="sxs-lookup"><span data-stu-id="9973f-107">_lpulTableStatus_</span></span>
  
> <span data-ttu-id="9973f-108">[out] Ponteiro para um valor que indica o status da tabela.</span><span class="sxs-lookup"><span data-stu-id="9973f-108">[out] Pointer to a value indicating the status of the table.</span></span> <span data-ttu-id="9973f-109">Pode ser retornado um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="9973f-109">One of the following values can be returned:</span></span>
    
<span data-ttu-id="9973f-110">TBLSTAT_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="9973f-110">TBLSTAT_COMPLETE</span></span> 
  
> <span data-ttu-id="9973f-111">Nenhuma operações estejam em andamento.</span><span class="sxs-lookup"><span data-stu-id="9973f-111">No operations are in progress.</span></span>
    
<span data-ttu-id="9973f-112">TBLSTAT_QCHANGED</span><span class="sxs-lookup"><span data-stu-id="9973f-112">TBLSTAT_QCHANGED</span></span> 
  
> <span data-ttu-id="9973f-113">O conteúdo da tabela expectantly foram alteradas.</span><span class="sxs-lookup"><span data-stu-id="9973f-113">The contents of the table have expectantly changed.</span></span> <span data-ttu-id="9973f-114">Esse valor de status não será retornado para que as alterações resultantes das operações de classificação ou restrição.</span><span class="sxs-lookup"><span data-stu-id="9973f-114">This status value is not returned for changes that result from sort or restriction operations.</span></span>
    
<span data-ttu-id="9973f-115">TBLSTAT_RESTRICT_ERROR</span><span class="sxs-lookup"><span data-stu-id="9973f-115">TBLSTAT_RESTRICT_ERROR</span></span> 
  
> <span data-ttu-id="9973f-116">Ocorreu um erro durante uma operação [IMAPITable:: Restrict](imapitable-restrict.md) .</span><span class="sxs-lookup"><span data-stu-id="9973f-116">An error occurred during an [IMAPITable::Restrict](imapitable-restrict.md) operation.</span></span> 
    
<span data-ttu-id="9973f-117">TBLSTAT_RESTRICTING</span><span class="sxs-lookup"><span data-stu-id="9973f-117">TBLSTAT_RESTRICTING</span></span> 
  
> <span data-ttu-id="9973f-118">Uma operação **IMAPITable:: Restrict** está em andamento.</span><span class="sxs-lookup"><span data-stu-id="9973f-118">An **IMAPITable::Restrict** operation is in progress.</span></span> 
    
<span data-ttu-id="9973f-119">TBLSTAT_SETCOL_ERROR</span><span class="sxs-lookup"><span data-stu-id="9973f-119">TBLSTAT_SETCOL_ERROR</span></span> 
  
> <span data-ttu-id="9973f-120">Ocorreu um erro durante uma operação de [IMAPITable::SetColumns](imapitable-setcolumns.md) .</span><span class="sxs-lookup"><span data-stu-id="9973f-120">An error occurred during an [IMAPITable::SetColumns](imapitable-setcolumns.md) operation.</span></span> 
    
<span data-ttu-id="9973f-121">TBLSTAT_SETTING_COLS</span><span class="sxs-lookup"><span data-stu-id="9973f-121">TBLSTAT_SETTING_COLS</span></span> 
  
> <span data-ttu-id="9973f-122">Uma operação **IMAPITable::SetColumns** está em andamento.</span><span class="sxs-lookup"><span data-stu-id="9973f-122">An **IMAPITable::SetColumns** operation is in progress.</span></span> 
    
<span data-ttu-id="9973f-123">TBLSTAT_SORT_ERROR</span><span class="sxs-lookup"><span data-stu-id="9973f-123">TBLSTAT_SORT_ERROR</span></span> 
  
> <span data-ttu-id="9973f-124">Ocorreu um erro durante uma operação [IMAPITable:: SortTable](imapitable-sorttable.md) .</span><span class="sxs-lookup"><span data-stu-id="9973f-124">An error occurred during an [IMAPITable::SortTable](imapitable-sorttable.md) operation.</span></span> 
    
<span data-ttu-id="9973f-125">TBLSTAT_SORTING</span><span class="sxs-lookup"><span data-stu-id="9973f-125">TBLSTAT_SORTING</span></span> 
  
> <span data-ttu-id="9973f-126">Uma operação **IMAPITable:: SortTable** está em andamento.</span><span class="sxs-lookup"><span data-stu-id="9973f-126">An **IMAPITable::SortTable** operation is in progress.</span></span> 
    
 <span data-ttu-id="9973f-127">_lpulTableType_</span><span class="sxs-lookup"><span data-stu-id="9973f-127">_lpulTableType_</span></span>
  
> <span data-ttu-id="9973f-128">[out] Ponteiro para um valor que indica o tipo de tabela.</span><span class="sxs-lookup"><span data-stu-id="9973f-128">[out] Pointer to a value that indicates the table's type.</span></span> <span data-ttu-id="9973f-129">Um dos seguintes tipos de três tabela pode ser retornado:</span><span class="sxs-lookup"><span data-stu-id="9973f-129">One of the following three table types can be returned:</span></span>
    
<span data-ttu-id="9973f-130">TBLTYPE_DYNAMIC</span><span class="sxs-lookup"><span data-stu-id="9973f-130">TBLTYPE_DYNAMIC</span></span> 
  
> <span data-ttu-id="9973f-131">O conteúdo da tabela é dinâmico; as linhas e os valores de coluna podem alterar como as alterações de dados subjacente.</span><span class="sxs-lookup"><span data-stu-id="9973f-131">The table's contents are dynamic; the rows and column values can change as the underlying data changes.</span></span>
    
<span data-ttu-id="9973f-132">TBLTYPE_KEYSET</span><span class="sxs-lookup"><span data-stu-id="9973f-132">TBLTYPE_KEYSET</span></span> 
  
> <span data-ttu-id="9973f-133">As linhas dentro da tabela são corrigidas, mas os valores das colunas dentro nessas linhas são dinâmicos e podem alterar como as alterações de dados subjacente.</span><span class="sxs-lookup"><span data-stu-id="9973f-133">The rows within the table are fixed, but the values of the columns within these rows are dynamic and can change as the underlying data changes.</span></span>
    
<span data-ttu-id="9973f-134">TBLTYPE_SNAPSHOT</span><span class="sxs-lookup"><span data-stu-id="9973f-134">TBLTYPE_SNAPSHOT</span></span> 
  
> <span data-ttu-id="9973f-135">A tabela é estática e seu conteúdo não é alterados quando os dados subjacentes forem alterados.</span><span class="sxs-lookup"><span data-stu-id="9973f-135">The table is static, and its contents do not change when the underlying data changes.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9973f-136">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="9973f-136">Return value</span></span>

<span data-ttu-id="9973f-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="9973f-137">S_OK</span></span> 
  
> <span data-ttu-id="9973f-138">Status da tabela foi retornado com êxito.</span><span class="sxs-lookup"><span data-stu-id="9973f-138">The table's status was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9973f-139">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="9973f-139">Remarks</span></span>

<span data-ttu-id="9973f-140">O método **IMAPTable::GetStatus** recupera informações sobre o tipo e o status atual de uma tabela.</span><span class="sxs-lookup"><span data-stu-id="9973f-140">The **IMAPTable::GetStatus** method retrieves information about a table's type and current status.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9973f-141">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="9973f-141">Notes to callers</span></span>

<span data-ttu-id="9973f-142">Você pode usar **GetStatus** junto com três outros métodos **IMAPITable** para monitorar o status dessas operações e determinar o efeito sobre a tabela.</span><span class="sxs-lookup"><span data-stu-id="9973f-142">You can use **GetStatus** in conjunction with three other **IMAPITable** methods to monitor the status of those operations and determine the effect on the table.</span></span> <span data-ttu-id="9973f-143">Chame **GetStatus** depois de fazer uma das seguintes chamadas **IMAPITable** :</span><span class="sxs-lookup"><span data-stu-id="9973f-143">Call **GetStatus** after making one of the following **IMAPITable** calls:</span></span> 
  
- <span data-ttu-id="9973f-144">[IMAPITable:: Restrict](imapitable-restrict.md) para definir uma restrição.</span><span class="sxs-lookup"><span data-stu-id="9973f-144">[IMAPITable::Restrict](imapitable-restrict.md) to set a restriction.</span></span> 
    
- <span data-ttu-id="9973f-145">[IMAPITable:: SortTable](imapitable-sorttable.md) para estabelecer uma ordem de classificação.</span><span class="sxs-lookup"><span data-stu-id="9973f-145">[IMAPITable::SortTable](imapitable-sorttable.md) to establish a sort order.</span></span> 
    
- <span data-ttu-id="9973f-146">[IMAPITable::SetColumns](imapitable-setcolumns.md) para definir um conjunto de coluna.</span><span class="sxs-lookup"><span data-stu-id="9973f-146">[IMAPITable::SetColumns](imapitable-setcolumns.md) to define a column set.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="9973f-147">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="9973f-147">MFCMAPI reference</span></span>

<span data-ttu-id="9973f-148">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="9973f-148">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9973f-149">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="9973f-149">**File**</span></span>|<span data-ttu-id="9973f-150">**Function**</span><span class="sxs-lookup"><span data-stu-id="9973f-150">**Function**</span></span>|<span data-ttu-id="9973f-151">**Comment**</span><span class="sxs-lookup"><span data-stu-id="9973f-151">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9973f-152">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="9973f-152">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="9973f-153">CContentsTableListCtrl::GetStatus</span><span class="sxs-lookup"><span data-stu-id="9973f-153">CContentsTableListCtrl::GetStatus</span></span>  <br/> |<span data-ttu-id="9973f-154">MFCMAPI usa o método **IMAPITable::GetStatus** para informar o status de uma tabela.</span><span class="sxs-lookup"><span data-stu-id="9973f-154">MFCMAPI uses the **IMAPITable::GetStatus** method to report the status of a table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9973f-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="9973f-155">See also</span></span>



[<span data-ttu-id="9973f-156">IMAPITable:: Restrict</span><span class="sxs-lookup"><span data-stu-id="9973f-156">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="9973f-157">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="9973f-157">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="9973f-158">IMAPITable:: SortTable</span><span class="sxs-lookup"><span data-stu-id="9973f-158">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="9973f-159">IMAPITable: IUnknown</span><span class="sxs-lookup"><span data-stu-id="9973f-159">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="9973f-160">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="9973f-160">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

