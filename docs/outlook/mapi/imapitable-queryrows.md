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
ms.openlocfilehash: 26d6ffe66a5e7749c9d8c4e5210e9f72de808932
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416290"
---
# <a name="imapitablequeryrows"></a><span data-ttu-id="b8464-103">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="b8464-103">IMAPITable::QueryRows</span></span>

  
  
<span data-ttu-id="b8464-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b8464-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b8464-105">Retorna uma ou mais linhas de uma tabela, começando na posição atual do cursor.</span><span class="sxs-lookup"><span data-stu-id="b8464-105">Returns one or more rows from a table, beginning at the current cursor position.</span></span>
  
```cpp
HRESULT QueryRows(
LONG lRowCount,
ULONG ulFlags,
LPSRowSet FAR * lppRows
);
```

## <a name="parameters"></a><span data-ttu-id="b8464-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b8464-106">Parameters</span></span>

 <span data-ttu-id="b8464-107">_lRowCount_</span><span class="sxs-lookup"><span data-stu-id="b8464-107">_lRowCount_</span></span>
  
> <span data-ttu-id="b8464-108">[in] Número máximo de linhas a serem retornadas.</span><span class="sxs-lookup"><span data-stu-id="b8464-108">[in] Maximum number of rows to be returned.</span></span>
    
 <span data-ttu-id="b8464-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b8464-109">_ulFlags_</span></span>
  
> <span data-ttu-id="b8464-110">[in] Máscara de bits de sinalizadores que controlam como as linhas são retornadas.</span><span class="sxs-lookup"><span data-stu-id="b8464-110">[in] Bitmask of flags that control how rows are returned.</span></span> <span data-ttu-id="b8464-111">O sinalizador a seguir pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="b8464-111">The following flag can be set:</span></span>
    
<span data-ttu-id="b8464-112">TBL_NOADVANCE</span><span class="sxs-lookup"><span data-stu-id="b8464-112">TBL_NOADVANCE</span></span> 
  
> <span data-ttu-id="b8464-113">Impede que o cursor avança como resultado da recuperação de linha.</span><span class="sxs-lookup"><span data-stu-id="b8464-113">Prevents the cursor from advancing as a result of the row retrieval.</span></span> <span data-ttu-id="b8464-114">Se o TBL_NOADVANCE sinalizador estiver definido, o cursor aponta para a primeira linha retornada.</span><span class="sxs-lookup"><span data-stu-id="b8464-114">If the TBL_NOADVANCE flag is set, the cursor points to the first row returned.</span></span> <span data-ttu-id="b8464-115">Se o TBL_NOADVANCE sinalizador não estiver definido, o cursor aponta para a linha após a última linha retornada.</span><span class="sxs-lookup"><span data-stu-id="b8464-115">If the TBL_NOADVANCE flag is not set, the cursor points to the row following the last row returned.</span></span>
    
 <span data-ttu-id="b8464-116">_lppRows_</span><span class="sxs-lookup"><span data-stu-id="b8464-116">_lppRows_</span></span>
  
> <span data-ttu-id="b8464-117">[out] Ponteiro para um ponteiro para uma [estrutura SRowSet](srowset.md) segurando as linhas da tabela.</span><span class="sxs-lookup"><span data-stu-id="b8464-117">[out] Pointer to a pointer to an [SRowSet](srowset.md) structure holding the table rows.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b8464-118">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b8464-118">Return value</span></span>

<span data-ttu-id="b8464-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="b8464-119">S_OK</span></span> 
  
> <span data-ttu-id="b8464-120">As linhas foram retornadas com êxito.</span><span class="sxs-lookup"><span data-stu-id="b8464-120">The rows were successfully returned.</span></span>
    
<span data-ttu-id="b8464-121">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="b8464-121">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="b8464-122">Outra operação está em andamento que impede o início da operação de recuperação de linha.</span><span class="sxs-lookup"><span data-stu-id="b8464-122">Another operation is in progress that prevents the row retrieval operation from starting.</span></span> <span data-ttu-id="b8464-123">A operação em andamento deve ter permissão para ser concluída ou deve ser interrompida.</span><span class="sxs-lookup"><span data-stu-id="b8464-123">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="b8464-124">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b8464-124">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="b8464-125">O  _parâmetro IRowCount_ é definido como zero.</span><span class="sxs-lookup"><span data-stu-id="b8464-125">The  _IRowCount_ parameter is set to zero.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b8464-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="b8464-126">Remarks</span></span>

<span data-ttu-id="b8464-127">O **método IMAPITable::QueryRows** obtém uma ou mais linhas de dados de uma tabela.</span><span class="sxs-lookup"><span data-stu-id="b8464-127">The **IMAPITable::QueryRows** method gets one or more rows of data from a table.</span></span> <span data-ttu-id="b8464-128">O valor do parâmetro  _IRowCount_ afeta o ponto de partida para a recuperação.</span><span class="sxs-lookup"><span data-stu-id="b8464-128">The value of the  _IRowCount_ parameter affects the starting point for the retrieval.</span></span> <span data-ttu-id="b8464-129">Se  _IRowCount_ for positivo, as linhas serão lidas em uma direção à frente, começando na posição atual.</span><span class="sxs-lookup"><span data-stu-id="b8464-129">If  _IRowCount_ is positive, rows are read in a forward direction, starting at the current position.</span></span> <span data-ttu-id="b8464-130">Se  _IRowCount_ for negativo, **QueryRows** redefine o ponto inicial movendo para trás o número de linhas indicado.</span><span class="sxs-lookup"><span data-stu-id="b8464-130">If  _IRowCount_ is negative, **QueryRows** resets the starting point by moving backward the indicated number of rows.</span></span> <span data-ttu-id="b8464-131">Depois que o cursor é redefinido, as linhas são lidas na ordem de avanço.</span><span class="sxs-lookup"><span data-stu-id="b8464-131">After the cursor is reset, rows are read in forward order.</span></span> 
  
<span data-ttu-id="b8464-132">O **membro cRows** na [estrutura SRowSet](srowset.md) apontado pelo parâmetro  _lppRows_ indica o número de linhas retornadas.</span><span class="sxs-lookup"><span data-stu-id="b8464-132">The **cRows** member in the [SRowSet](srowset.md) structure pointed to by the  _lppRows_ parameter indicates the number of rows returned.</span></span> <span data-ttu-id="b8464-133">Se zero linhas são retornadas:</span><span class="sxs-lookup"><span data-stu-id="b8464-133">If zero rows are returned:</span></span> 
  
- <span data-ttu-id="b8464-134">O cursor já foi posicionado no início da tabela e o valor de  _IRowCount_ é negativo.</span><span class="sxs-lookup"><span data-stu-id="b8464-134">The cursor was already positioned at the beginning of the table and the value of  _IRowCount_ is negative.</span></span> <span data-ttu-id="b8464-135">-Ou-</span><span class="sxs-lookup"><span data-stu-id="b8464-135">-Or-</span></span> 
    
- <span data-ttu-id="b8464-136">O cursor já foi posicionado no final da tabela e o valor de  _IRowCount_ é positivo.</span><span class="sxs-lookup"><span data-stu-id="b8464-136">The cursor was already positioned at the end of the table and the value of  _IRowCount_ is positive.</span></span> 
    
<span data-ttu-id="b8464-137">O número de colunas e sua ordenação são as mesmas para cada linha.</span><span class="sxs-lookup"><span data-stu-id="b8464-137">The number of columns and their ordering is the same for each row.</span></span> <span data-ttu-id="b8464-138">Se uma propriedade não existir para uma linha ou se houver um erro ao ler uma propriedade, a estrutura **SPropValue** da propriedade na linha conterá os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="b8464-138">If a property does not exist for a row or there is an error reading a property, the **SPropValue** structure for the property in the row contains the following values:</span></span> 
  
- <span data-ttu-id="b8464-139">PT_ERROR para o tipo de propriedade no **membro ulPropTag.**</span><span class="sxs-lookup"><span data-stu-id="b8464-139">PT_ERROR for the property type in the **ulPropTag** member.</span></span> 
    
- <span data-ttu-id="b8464-140">MAPI_E_NOT_FOUND para o **membro** Value.</span><span class="sxs-lookup"><span data-stu-id="b8464-140">MAPI_E_NOT_FOUND for the **Value** member.</span></span> 
    
<span data-ttu-id="b8464-141">A memória usada para as [estruturas SPropValue](spropvalue.md) no conjunto de linhas apontado pelo parâmetro  _lppRows_ deve ser alocada e liberada separadamente para cada linha.</span><span class="sxs-lookup"><span data-stu-id="b8464-141">Memory used for the [SPropValue](spropvalue.md) structures in the row set pointed to by the  _lppRows_ parameter must be separately allocated and freed for each row.</span></span> <span data-ttu-id="b8464-142">Use [MAPIFreeBuffer](mapifreebuffer.md) para liberar as estruturas de valor de propriedade e liberar o conjunto de linhas.</span><span class="sxs-lookup"><span data-stu-id="b8464-142">Use [MAPIFreeBuffer](mapifreebuffer.md) to free the property value structures and to free the row set.</span></span> <span data-ttu-id="b8464-143">No entanto, quando uma chamada para **QueryRows** retorna zero, indicando o início ou o fim da tabela, somente a própria estrutura **SRowSet** precisa ser liberada.</span><span class="sxs-lookup"><span data-stu-id="b8464-143">When a call to **QueryRows** returns zero, however, indicating the beginning or end of the table, only the **SRowSet** structure itself needs to be freed.</span></span> <span data-ttu-id="b8464-144">Para obter mais informações sobre como alocar e liberar memória em uma estrutura **SRowSet,** consulte Gerenciando memória para [estruturas ADRLIST e SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="b8464-144">For more information about how to allocate and free memory in an **SRowSet** structure, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
<span data-ttu-id="b8464-145">As linhas retornadas e a ordem em que são retornadas dependem se chamadas bem-sucedidas foram feitas ou não para [IMAPITable::Restrict](imapitable-restrict.md) e [IMAPITable::SortTable](imapitable-sorttable.md).</span><span class="sxs-lookup"><span data-stu-id="b8464-145">The rows that are returned and the order in which they are returned depend on whether or not successful calls have been made to [IMAPITable::Restrict](imapitable-restrict.md) and [IMAPITable::SortTable](imapitable-sorttable.md).</span></span> <span data-ttu-id="b8464-146">**Restrinja** linhas de filtros do ponto de vista, fazendo com que **QueryRows** retorne apenas as linhas que corresponderem aos critérios especificados na restrição.</span><span class="sxs-lookup"><span data-stu-id="b8464-146">**Restrict** filters rows from the view, causing **QueryRows** to return only the rows that match the criteria specified in the restriction.</span></span> <span data-ttu-id="b8464-147">**SortTable** estabelece uma ordem de classificação padrão ou categorizada, afetando a sequência de linhas retornadas por **QueryRows**.</span><span class="sxs-lookup"><span data-stu-id="b8464-147">**SortTable** establishes a standard or categorized sort order, affecting the sequence of rows returned by **QueryRows**.</span></span> <span data-ttu-id="b8464-148">As linhas retornadas estão na ordem especificada na [estrutura SSortOrderSet](ssortorderset.md) passada para **SortTable**.</span><span class="sxs-lookup"><span data-stu-id="b8464-148">The returned rows are in the order specified in the [SSortOrderSet](ssortorderset.md) structure passed to **SortTable**.</span></span>
  
<span data-ttu-id="b8464-149">As colunas retornadas para cada linha e a ordem em que são retornadas dependem se uma chamada bem-sucedida foi feita ou não para [IMAPITable::SetColumns](imapitable-setcolumns.md).</span><span class="sxs-lookup"><span data-stu-id="b8464-149">The columns returned for each row and the order in which they are returned depend on whether or not a successful call has been made to [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span> <span data-ttu-id="b8464-150">**SetColumns** estabelece um conjunto de colunas, especificando as propriedades a serem incluídas nas colunas da tabela e a ordem na qual elas devem ser incluídas.</span><span class="sxs-lookup"><span data-stu-id="b8464-150">**SetColumns** establishes a column set, specifying the properties to be included in columns in the table and the order in which they should be included.</span></span> <span data-ttu-id="b8464-151">Se uma **chamada SetColumns** tiver sido feita, as colunas específicas em cada linha e a ordem dessas colunas corresponderão ao conjunto de colunas especificado na chamada.</span><span class="sxs-lookup"><span data-stu-id="b8464-151">If a **SetColumns** call has been made, the particular columns in each row and the order of those columns match the column set specified in the call.</span></span> <span data-ttu-id="b8464-152">Se nenhuma **chamada SetColumns** tiver sido feita, a tabela retornará seu conjunto de colunas padrão.</span><span class="sxs-lookup"><span data-stu-id="b8464-152">If no **SetColumns** call has been made, the table returns its default column set.</span></span> 
  
<span data-ttu-id="b8464-153">Se nenhuma dessas chamadas tiver sido feita, **QueryRows** retornará todas as linhas na tabela.</span><span class="sxs-lookup"><span data-stu-id="b8464-153">If none of these calls has been made, **QueryRows** returns all of the rows in the table.</span></span> <span data-ttu-id="b8464-154">Cada linha contém o conjunto de colunas padrão na ordem padrão.</span><span class="sxs-lookup"><span data-stu-id="b8464-154">Each row contains the default column set in default order.</span></span> 
  
<span data-ttu-id="b8464-155">Quando o conjunto de colunas estabelecido em uma chamada para [IMAPITable::SetColumns](imapitable-setcolumns.md) inclui colunas definidas como PR_NULL, a matriz [SPropValue](spropvalue.md) dentro do conjunto de linhas retornado em  _lppRows_ conterá slots vazios.</span><span class="sxs-lookup"><span data-stu-id="b8464-155">When the column set established in a call to [IMAPITable::SetColumns](imapitable-setcolumns.md) includes columns set to PR_NULL, the [SPropValue](spropvalue.md) array within the row set returned in  _lppRows_ will contain empty slots.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="b8464-156">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="b8464-156">Notes to implementers</span></span>

<span data-ttu-id="b8464-157">Você pode permitir que um chamador solicite que uma coluna sem suporte seja incluída no conjunto de colunas.</span><span class="sxs-lookup"><span data-stu-id="b8464-157">You can allow a caller to request an unsupported column to be included in the column set.</span></span> <span data-ttu-id="b8464-158">Quando isso ocorrer, PT_ERROR na parte do tipo de propriedade da marca de propriedade e MAPI_E_NOT_FOUND no valor da propriedade da coluna sem suporte.</span><span class="sxs-lookup"><span data-stu-id="b8464-158">When this occurs, place PT_ERROR in the property type portion of the property tag and MAPI_E_NOT_FOUND in the property value for the unsupported column.</span></span> 
  
<span data-ttu-id="b8464-159">Trate a contagem de linhas como uma solicitação em vez de um requisito.</span><span class="sxs-lookup"><span data-stu-id="b8464-159">Treat the row count as a request rather than a requirement.</span></span> <span data-ttu-id="b8464-160">Você pode retornar de qualquer lugar a partir de zero linhas, se não houver linhas na direção da consulta, para o número solicitado.</span><span class="sxs-lookup"><span data-stu-id="b8464-160">You can return anywhere from zero rows, if there are no rows in the direction of the query, to the number requested.</span></span> 
  
<span data-ttu-id="b8464-161">Retorne apenas as linhas que o usuário verá quando as linhas são solicitadas de uma exibição de tabela categorizada, permitindo que o chamador faça suposições válidas sobre o escopo dos dados e evite trabalho extra.</span><span class="sxs-lookup"><span data-stu-id="b8464-161">Return only the rows that the user will see when rows are requested from a categorized table view, allowing the caller to make valid assumptions about the scope of the data and avoid extra work.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b8464-162">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="b8464-162">Notes to callers</span></span>

<span data-ttu-id="b8464-163">Normalmente, você terminará com quantas linhas tiver especificado no parâmetro _lRowCount._</span><span class="sxs-lookup"><span data-stu-id="b8464-163">Usually you will end up with as many rows as you have specified in the  _lRowCount_ parameter.</span></span> <span data-ttu-id="b8464-164">No entanto, quando os limites de memória ou implementação são um problema ou quando a operação atinge o início ou o fim da tabela prematuramente, **QueryRows** retornará menos linhas do que o solicitado.</span><span class="sxs-lookup"><span data-stu-id="b8464-164">However, when memory or implementation limits are an issue or when the operation reaches the beginning or end of the table prematurely, **QueryRows** will return less rows than requested.</span></span> 
  
<span data-ttu-id="b8464-165">Se **QueryRows** retornar MAPI_E_BUSY, chame o método [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) e repetir a chamada para **QueryRows** quando a operação assíncrona for concluída.</span><span class="sxs-lookup"><span data-stu-id="b8464-165">If **QueryRows** returns MAPI_E_BUSY, call the [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) method and retry the call to **QueryRows** when the asynchronous operation is complete.</span></span> 
  
<span data-ttu-id="b8464-166">Ao chamar **QueryRows,** esteja ciente de que o tempo de notificações assíncronas pode fazer com que o conjunto de linhas que você recebe de **QueryRows** não represente precisamente os dados subjacentes.</span><span class="sxs-lookup"><span data-stu-id="b8464-166">When calling **QueryRows**, be aware that the timing of asynchronous notifications can potentially cause the row set that you get back from **QueryRows** not to accurately represent the underlying data.</span></span> <span data-ttu-id="b8464-167">Por exemplo, uma chamada para **QueryRows** para a tabela de conteúdo de uma pasta após a exclusão de uma mensagem, mas antes do recebimento da notificação correspondente fará com que a linha excluída seja retornada no conjunto de linhas.</span><span class="sxs-lookup"><span data-stu-id="b8464-167">For example, a call to **QueryRows** to a folder's contents table following the deletion of a message but prior to the receipt of the corresponding notification will cause the deleted row to be returned in the row set.</span></span> <span data-ttu-id="b8464-168">Aguarde até que uma notificação chegue antes de atualizar a exibição dos dados do usuário.</span><span class="sxs-lookup"><span data-stu-id="b8464-168">Always wait for a notification to arrive before updating the user's view of the data.</span></span> 
  
<span data-ttu-id="b8464-169">Para obter mais informações sobre como recuperar linhas de tabelas, consulte Recuperando dados de linhas [de tabela.](retrieving-data-from-table-rows.md)</span><span class="sxs-lookup"><span data-stu-id="b8464-169">For more information about retrieving rows from tables, see [Retrieving Data from Table Rows](retrieving-data-from-table-rows.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b8464-170">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="b8464-170">MFCMAPI reference</span></span>

<span data-ttu-id="b8464-171">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b8464-171">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b8464-172">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="b8464-172">**File**</span></span>|<span data-ttu-id="b8464-173">**Função**</span><span class="sxs-lookup"><span data-stu-id="b8464-173">**Function**</span></span>|<span data-ttu-id="b8464-174">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="b8464-174">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b8464-175">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="b8464-175">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="b8464-176">DwThreadFuncLoadTable</span><span class="sxs-lookup"><span data-stu-id="b8464-176">DwThreadFuncLoadTable</span></span>  <br/> |<span data-ttu-id="b8464-177">MFCMAPI usa o **método IMAPITable::QueryRows** para recuperar linhas na tabela para carregar no modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="b8464-177">MFCMAPI uses the **IMAPITable::QueryRows** method to retrieve rows in the table to load into the view.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b8464-178">Confira também</span><span class="sxs-lookup"><span data-stu-id="b8464-178">See also</span></span>



[<span data-ttu-id="b8464-179">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="b8464-179">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="b8464-180">FreeProws</span><span class="sxs-lookup"><span data-stu-id="b8464-180">FreeProws</span></span>](freeprows.md)
  
[<span data-ttu-id="b8464-181">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="b8464-181">HrQueryAllRows</span></span>](hrqueryallrows.md)
  
[<span data-ttu-id="b8464-182">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="b8464-182">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="b8464-183">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="b8464-183">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="b8464-184">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="b8464-184">IMAPITable::WaitForCompletion</span></span>](imapitable-waitforcompletion.md)
  
[<span data-ttu-id="b8464-185">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="b8464-185">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="b8464-186">SRow</span><span class="sxs-lookup"><span data-stu-id="b8464-186">SRow</span></span>](srow.md)
  
[<span data-ttu-id="b8464-187">SRowSet</span><span class="sxs-lookup"><span data-stu-id="b8464-187">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="b8464-188">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b8464-188">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="b8464-189">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="b8464-189">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

