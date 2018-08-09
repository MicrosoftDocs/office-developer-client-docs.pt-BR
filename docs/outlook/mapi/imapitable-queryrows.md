---
title: IMAPITableQueryRows
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.QueryRows
api_type:
- COM
ms.assetid: f26384f1-467e-4343-92b3-0425da9d2123
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a6659f64f6e8d2e3dc61819b2263efe672cdd15c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767357"
---
# <a name="imapitablequeryrows"></a><span data-ttu-id="e86d2-103">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="e86d2-103">IMAPITable::QueryRows</span></span>

  
  
<span data-ttu-id="e86d2-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e86d2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e86d2-105">Retorna uma ou mais linhas de uma tabela, começando à meia posição atual do cursor.</span><span class="sxs-lookup"><span data-stu-id="e86d2-105">Returns one or more rows from a table, beginning at the current cursor position.</span></span>
  
```cpp
HRESULT QueryRows(
LONG lRowCount,
ULONG ulFlags,
LPSRowSet FAR * lppRows
);
```

## <a name="parameters"></a><span data-ttu-id="e86d2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e86d2-106">Parameters</span></span>

 <span data-ttu-id="e86d2-107">_lRowCount_</span><span class="sxs-lookup"><span data-stu-id="e86d2-107">_lRowCount_</span></span>
  
> <span data-ttu-id="e86d2-108">[in] Número máximo de linhas a ser retornado.</span><span class="sxs-lookup"><span data-stu-id="e86d2-108">[in] Maximum number of rows to be returned.</span></span>
    
 <span data-ttu-id="e86d2-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e86d2-109">_ulFlags_</span></span>
  
> <span data-ttu-id="e86d2-110">[in] Bitmask dos sinalizadores que controlam como as linhas são retornadas.</span><span class="sxs-lookup"><span data-stu-id="e86d2-110">[in] Bitmask of flags that control how rows are returned.</span></span> <span data-ttu-id="e86d2-111">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="e86d2-111">The following flag can be set:</span></span>
    
<span data-ttu-id="e86d2-112">TBL_NOADVANCE</span><span class="sxs-lookup"><span data-stu-id="e86d2-112">TBL_NOADVANCE</span></span> 
  
> <span data-ttu-id="e86d2-113">Impede que o cursor avançando como resultado de recuperação de linha.</span><span class="sxs-lookup"><span data-stu-id="e86d2-113">Prevents the cursor from advancing as a result of the row retrieval.</span></span> <span data-ttu-id="e86d2-114">Se o sinalizador TBL_NOADVANCE estiver definido, os pontos de cursor à primeira linha é retornada.</span><span class="sxs-lookup"><span data-stu-id="e86d2-114">If the TBL_NOADVANCE flag is set, the cursor points to the first row returned.</span></span> <span data-ttu-id="e86d2-115">Se o sinalizador TBL_NOADVANCE não estiver definido, o cursor aponta para a linha após a última linha retornada.</span><span class="sxs-lookup"><span data-stu-id="e86d2-115">If the TBL_NOADVANCE flag is not set, the cursor points to the row following the last row returned.</span></span>
    
 <span data-ttu-id="e86d2-116">_lppRows_</span><span class="sxs-lookup"><span data-stu-id="e86d2-116">_lppRows_</span></span>
  
> <span data-ttu-id="e86d2-117">[out] Ponteiro para um ponteiro para uma estrutura [SRowSet](srowset.md) reter as linhas de tabela.</span><span class="sxs-lookup"><span data-stu-id="e86d2-117">[out] Pointer to a pointer to an [SRowSet](srowset.md) structure holding the table rows.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e86d2-118">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="e86d2-118">Return value</span></span>

<span data-ttu-id="e86d2-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="e86d2-119">S_OK</span></span> 
  
> <span data-ttu-id="e86d2-120">As linhas foram retornadas com êxito.</span><span class="sxs-lookup"><span data-stu-id="e86d2-120">The rows were successfully returned.</span></span>
    
<span data-ttu-id="e86d2-121">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="e86d2-121">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="e86d2-122">Outra operação está em andamento que impede que a operação de recuperação de linha seja iniciado.</span><span class="sxs-lookup"><span data-stu-id="e86d2-122">Another operation is in progress that prevents the row retrieval operation from starting.</span></span> <span data-ttu-id="e86d2-123">Ou a operação em andamento deve ter permissão para concluir ou ele deve ser interrompido.</span><span class="sxs-lookup"><span data-stu-id="e86d2-123">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="e86d2-124">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e86d2-124">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="e86d2-125">O parâmetro _IRowCount_ é definido como zero.</span><span class="sxs-lookup"><span data-stu-id="e86d2-125">The  _IRowCount_ parameter is set to zero.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e86d2-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="e86d2-126">Remarks</span></span>

<span data-ttu-id="e86d2-127">O método **IMAPITable:: QueryRows** obtém uma ou mais linhas de dados de uma tabela.</span><span class="sxs-lookup"><span data-stu-id="e86d2-127">The **IMAPITable::QueryRows** method gets one or more rows of data from a table.</span></span> <span data-ttu-id="e86d2-128">O valor do parâmetro _IRowCount_ afeta o ponto de partida para a recuperação.</span><span class="sxs-lookup"><span data-stu-id="e86d2-128">The value of the  _IRowCount_ parameter affects the starting point for the retrieval.</span></span> <span data-ttu-id="e86d2-129">Se _IRowCount_ for positivo, as linhas são lidas em uma direção sequencial, começando na posição atual.</span><span class="sxs-lookup"><span data-stu-id="e86d2-129">If  _IRowCount_ is positive, rows are read in a forward direction, starting at the current position.</span></span> <span data-ttu-id="e86d2-130">Se _IRowCount_ for negativo, **QueryRows** redefine o ponto de partida movendo para trás o número de linhas indicado.</span><span class="sxs-lookup"><span data-stu-id="e86d2-130">If  _IRowCount_ is negative, **QueryRows** resets the starting point by moving backward the indicated number of rows.</span></span> <span data-ttu-id="e86d2-131">Depois que o cursor é redefinido, linhas são lidas em ordem sequencial.</span><span class="sxs-lookup"><span data-stu-id="e86d2-131">After the cursor is reset, rows are read in forward order.</span></span> 
  
<span data-ttu-id="e86d2-132">O membro de **pássaros** na estrutura [SRowSet](srowset.md) apontado pelo parâmetro _lppRows_ indica o número de linhas retornadas.</span><span class="sxs-lookup"><span data-stu-id="e86d2-132">The **cRows** member in the [SRowSet](srowset.md) structure pointed to by the  _lppRows_ parameter indicates the number of rows returned.</span></span> <span data-ttu-id="e86d2-133">Se zero linhas são retornadas:</span><span class="sxs-lookup"><span data-stu-id="e86d2-133">If zero rows are returned:</span></span> 
  
- <span data-ttu-id="e86d2-134">O cursor já foi posicionado no início da tabela e o valor de _IRowCount_ for negativo.</span><span class="sxs-lookup"><span data-stu-id="e86d2-134">The cursor was already positioned at the beginning of the table and the value of  _IRowCount_ is negative.</span></span> <span data-ttu-id="e86d2-135">- Ou -</span><span class="sxs-lookup"><span data-stu-id="e86d2-135">-Or-</span></span> 
    
- <span data-ttu-id="e86d2-136">O cursor já foi posicionado no final da tabela e o valor de _IRowCount_ for positivo.</span><span class="sxs-lookup"><span data-stu-id="e86d2-136">The cursor was already positioned at the end of the table and the value of  _IRowCount_ is positive.</span></span> 
    
<span data-ttu-id="e86d2-137">O número de colunas e seus ordenação é o mesmo para cada linha.</span><span class="sxs-lookup"><span data-stu-id="e86d2-137">The number of columns and their ordering is the same for each row.</span></span> <span data-ttu-id="e86d2-138">Se não existir uma propriedade para uma linha ou não há um erro ao ler uma propriedade, a estrutura de **SPropValue** para a propriedade na linha contém os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="e86d2-138">If a property does not exist for a row or there is an error reading a property, the **SPropValue** structure for the property in the row contains the following values:</span></span> 
  
- <span data-ttu-id="e86d2-139">PT_ERROR para o tipo de propriedade no membro **ulPropTag** .</span><span class="sxs-lookup"><span data-stu-id="e86d2-139">PT_ERROR for the property type in the **ulPropTag** member.</span></span> 
    
- <span data-ttu-id="e86d2-140">E_NOT_FOUND para o membro de **valor** .</span><span class="sxs-lookup"><span data-stu-id="e86d2-140">MAPI_E_NOT_FOUND for the **Value** member.</span></span> 
    
<span data-ttu-id="e86d2-141">Memória usada para as estruturas de [SPropValue](spropvalue.md) no conjunto de linha apontado pelo parâmetro _lppRows_ deve ser alocada separadamente e liberada para cada linha.</span><span class="sxs-lookup"><span data-stu-id="e86d2-141">Memory used for the [SPropValue](spropvalue.md) structures in the row set pointed to by the  _lppRows_ parameter must be separately allocated and freed for each row.</span></span> <span data-ttu-id="e86d2-142">Use [MAPIFreeBuffer](mapifreebuffer.md) para liberar as estruturas de valor de propriedade e liberar a linha definido.</span><span class="sxs-lookup"><span data-stu-id="e86d2-142">Use [MAPIFreeBuffer](mapifreebuffer.md) to free the property value structures and to free the row set.</span></span> <span data-ttu-id="e86d2-143">Quando uma chamada para **QueryRows** retornará zero, no entanto, indicando o início ou fim da tabela, apenas a estrutura de **SRowSet** em si precisa ser liberada.</span><span class="sxs-lookup"><span data-stu-id="e86d2-143">When a call to **QueryRows** returns zero, however, indicating the beginning or end of the table, only the **SRowSet** structure itself needs to be freed.</span></span> <span data-ttu-id="e86d2-144">Para obter mais informações sobre como alocar e liberar memória em uma estrutura **SRowSet** , consulte [Gerenciando memória para ADRLIST e estruturas de SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="e86d2-144">For more information about how to allocate and free memory in an **SRowSet** structure, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
<span data-ttu-id="e86d2-145">As linhas que são retornadas e a ordem na qual eles são retornados dependem ou não chamadas bem-sucedidas tem sofridas [IMAPITable:: Restrict](imapitable-restrict.md) e [IMAPITable:: SortTable](imapitable-sorttable.md).</span><span class="sxs-lookup"><span data-stu-id="e86d2-145">The rows that are returned and the order in which they are returned depend on whether or not successful calls have been made to [IMAPITable::Restrict](imapitable-restrict.md) and [IMAPITable::SortTable](imapitable-sorttable.md).</span></span> <span data-ttu-id="e86d2-146">**Restrict** filtra linhas da exibição, causando **QueryRows** retornar somente as linhas que coincidem com os critérios especificados na restrição.</span><span class="sxs-lookup"><span data-stu-id="e86d2-146">**Restrict** filters rows from the view, causing **QueryRows** to return only the rows that match the criteria specified in the restriction.</span></span> <span data-ttu-id="e86d2-147">**SortTable** estabelece um padrão ou categorizados a ordem de classificação, que afetam a sequência de linhas retornadas por **QueryRows**.</span><span class="sxs-lookup"><span data-stu-id="e86d2-147">**SortTable** establishes a standard or categorized sort order, affecting the sequence of rows returned by **QueryRows**.</span></span> <span data-ttu-id="e86d2-148">As linhas retornadas são na ordem especificada na estrutura [SSortOrderSet](ssortorderset.md) passada para **SortTable**.</span><span class="sxs-lookup"><span data-stu-id="e86d2-148">The returned rows are in the order specified in the [SSortOrderSet](ssortorderset.md) structure passed to **SortTable**.</span></span>
  
<span data-ttu-id="e86d2-149">As colunas são retornadas para cada linha e a ordem na qual eles são retornados dependem se ou não uma chamada bem sucedida foi feita para [IMAPITable::SetColumns](imapitable-setcolumns.md).</span><span class="sxs-lookup"><span data-stu-id="e86d2-149">The columns returned for each row and the order in which they are returned depend on whether or not a successful call has been made to [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span> <span data-ttu-id="e86d2-150">**SetColumns** estabelece um conjunto de colunas, especificando as propriedades a serem incluídos nas colunas na tabela e a ordem em que eles devem ser incluídos.</span><span class="sxs-lookup"><span data-stu-id="e86d2-150">**SetColumns** establishes a column set, specifying the properties to be included in columns in the table and the order in which they should be included.</span></span> <span data-ttu-id="e86d2-151">Se foi feita uma chamada **SetColumns** , as colunas específicas de cada linha e a ordem das colunas correspondem a coluna definir especificada na chamada.</span><span class="sxs-lookup"><span data-stu-id="e86d2-151">If a **SetColumns** call has been made, the particular columns in each row and the order of those columns match the column set specified in the call.</span></span> <span data-ttu-id="e86d2-152">Se nenhuma chamada **SetColumns** tiverem sido feita, a tabela retorna seu conjunto de coluna padrão.</span><span class="sxs-lookup"><span data-stu-id="e86d2-152">If no **SetColumns** call has been made, the table returns its default column set.</span></span> 
  
<span data-ttu-id="e86d2-153">Se nenhuma dessas chamadas foi feita, **QueryRows** retorna todas as linhas na tabela.</span><span class="sxs-lookup"><span data-stu-id="e86d2-153">If none of these calls has been made, **QueryRows** returns all of the rows in the table.</span></span> <span data-ttu-id="e86d2-154">Cada linha contém a coluna padrão definida na ordem padrão.</span><span class="sxs-lookup"><span data-stu-id="e86d2-154">Each row contains the default column set in default order.</span></span> 
  
<span data-ttu-id="e86d2-155">Quando o conjunto de colunas estabelecido em uma chamada para [IMAPITable::SetColumns](imapitable-setcolumns.md) inclui colunas definidas como PR_NULL, a matriz de [SPropValue](spropvalue.md) dentro do conjunto de linhas retornada nos _lppRows_ irá conter slots vazios.</span><span class="sxs-lookup"><span data-stu-id="e86d2-155">When the column set established in a call to [IMAPITable::SetColumns](imapitable-setcolumns.md) includes columns set to PR_NULL, the [SPropValue](spropvalue.md) array within the row set returned in  _lppRows_ will contain empty slots.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="e86d2-156">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="e86d2-156">Notes to implementers</span></span>

<span data-ttu-id="e86d2-157">Você pode permitir que um chamador solicitar uma coluna sem suporte a serem incluídos no conjunto de colunas.</span><span class="sxs-lookup"><span data-stu-id="e86d2-157">You can allow a caller to request an unsupported column to be included in the column set.</span></span> <span data-ttu-id="e86d2-158">Quando isso ocorre, coloque PT_ERROR na parte de tipo de propriedade da marca de propriedade e E_NOT_FOUND no valor da propriedade para a coluna sem suporte.</span><span class="sxs-lookup"><span data-stu-id="e86d2-158">When this occurs, place PT_ERROR in the property type portion of the property tag and MAPI_E_NOT_FOUND in the property value for the unsupported column.</span></span> 
  
<span data-ttu-id="e86d2-159">Trate a contagem de linhas como uma solicitação ao invés um requisito.</span><span class="sxs-lookup"><span data-stu-id="e86d2-159">Treat the row count as a request rather than a requirement.</span></span> <span data-ttu-id="e86d2-160">Você pode retornar em qualquer lugar do zero linhas, se não houver nenhuma linha na direção da consulta, para o número solicitado.</span><span class="sxs-lookup"><span data-stu-id="e86d2-160">You can return anywhere from zero rows, if there are no rows in the direction of the query, to the number requested.</span></span> 
  
<span data-ttu-id="e86d2-161">Retorne somente as linhas que o usuário verá quando linhas são solicitadas a partir de um modo de exibição de tabela categorizados, permitindo que o chamador para tornar as suposições válidas sobre o escopo dos dados e evitar trabalho extra.</span><span class="sxs-lookup"><span data-stu-id="e86d2-161">Return only the rows that the user will see when rows are requested from a categorized table view, allowing the caller to make valid assumptions about the scope of the data and avoid extra work.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e86d2-162">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="e86d2-162">Notes to callers</span></span>

<span data-ttu-id="e86d2-163">Geralmente você acabará com quantas linhas você especificou no parâmetro _lRowCount_ .</span><span class="sxs-lookup"><span data-stu-id="e86d2-163">Usually you will end up with as many rows as you have specified in the  _lRowCount_ parameter.</span></span> <span data-ttu-id="e86d2-164">No entanto, quando os limites de memória ou implementação são um problema ou a operação atinge o início ou fim da tabela prematuramente, **QueryRows** vai retornar menos linhas do que o solicitado.</span><span class="sxs-lookup"><span data-stu-id="e86d2-164">However, when memory or implementation limits are an issue or when the operation reaches the beginning or end of the table prematurely, **QueryRows** will return less rows than requested.</span></span> 
  
<span data-ttu-id="e86d2-165">Se **QueryRows** retornar MAPI_E_BUSY, chame o método [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) e repetir a chamada para **QueryRows** quando a operação assíncrona seja concluída.</span><span class="sxs-lookup"><span data-stu-id="e86d2-165">If **QueryRows** returns MAPI_E_BUSY, call the [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) method and retry the call to **QueryRows** when the asynchronous operation is complete.</span></span> 
  
<span data-ttu-id="e86d2-166">Ao chamar **QueryRows**, lembre-se de que o tempo de notificações assíncronas poderão causar o conjunto de linhas que você obtenha volta de **QueryRows** não para representar com precisão os dados subjacentes.</span><span class="sxs-lookup"><span data-stu-id="e86d2-166">When calling **QueryRows**, be aware that the timing of asynchronous notifications can potentially cause the row set that you get back from **QueryRows** not to accurately represent the underlying data.</span></span> <span data-ttu-id="e86d2-167">Por exemplo, uma chamada para **QueryRows** seguinte de tabela de conteúdo de uma pasta da linha excluída a ser retornado na linha fará com que a exclusão de uma mensagem, mas antes do recebimento da notificação correspondente é definido.</span><span class="sxs-lookup"><span data-stu-id="e86d2-167">For example, a call to **QueryRows** to a folder's contents table following the deletion of a message but prior to the receipt of the corresponding notification will cause the deleted row to be returned in the row set.</span></span> <span data-ttu-id="e86d2-168">Aguarde sempre uma notificação chegar antes de atualizar o modo de exibição do usuário dos dados.</span><span class="sxs-lookup"><span data-stu-id="e86d2-168">Always wait for a notification to arrive before updating the user's view of the data.</span></span> 
  
<span data-ttu-id="e86d2-169">Para obter mais informações sobre como recuperar linhas de tabelas, consulte [Recuperando dados de linhas da tabela](retrieving-data-from-table-rows.md).</span><span class="sxs-lookup"><span data-stu-id="e86d2-169">For more information about retrieving rows from tables, see [Retrieving Data from Table Rows](retrieving-data-from-table-rows.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e86d2-170">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="e86d2-170">MFCMAPI reference</span></span>

<span data-ttu-id="e86d2-171">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e86d2-171">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e86d2-172">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="e86d2-172">**File**</span></span>|<span data-ttu-id="e86d2-173">**Function**</span><span class="sxs-lookup"><span data-stu-id="e86d2-173">**Function**</span></span>|<span data-ttu-id="e86d2-174">**Comment**</span><span class="sxs-lookup"><span data-stu-id="e86d2-174">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e86d2-175">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="e86d2-175">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="e86d2-176">DwThreadFuncLoadTable</span><span class="sxs-lookup"><span data-stu-id="e86d2-176">DwThreadFuncLoadTable</span></span>  <br/> |<span data-ttu-id="e86d2-177">MFCMAPI usa o método **IMAPITable:: QueryRows** para recuperar linhas da tabela para carregar no modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="e86d2-177">MFCMAPI uses the **IMAPITable::QueryRows** method to retrieve rows in the table to load into the view.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e86d2-178">Confira também</span><span class="sxs-lookup"><span data-stu-id="e86d2-178">See also</span></span>



[<span data-ttu-id="e86d2-179">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="e86d2-179">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="e86d2-180">FreeProws</span><span class="sxs-lookup"><span data-stu-id="e86d2-180">FreeProws</span></span>](freeprows.md)
  
[<span data-ttu-id="e86d2-181">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="e86d2-181">HrQueryAllRows</span></span>](hrqueryallrows.md)
  
[<span data-ttu-id="e86d2-182">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="e86d2-182">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="e86d2-183">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="e86d2-183">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="e86d2-184">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="e86d2-184">IMAPITable::WaitForCompletion</span></span>](imapitable-waitforcompletion.md)
  
[<span data-ttu-id="e86d2-185">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="e86d2-185">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="e86d2-186">SRow</span><span class="sxs-lookup"><span data-stu-id="e86d2-186">SRow</span></span>](srow.md)
  
[<span data-ttu-id="e86d2-187">SRowSet</span><span class="sxs-lookup"><span data-stu-id="e86d2-187">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="e86d2-188">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e86d2-188">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="e86d2-189">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="e86d2-189">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

