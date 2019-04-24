---
title: IMAPITableSortTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SortTable
api_type:
- COM
ms.assetid: ff5f78ac-06cf-46fb-93da-5f4a3a5d1b22
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: f16ba9164d55fdb7bd688d4068f99dc4407e5413
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328851"
---
# <a name="imapitablesorttable"></a><span data-ttu-id="9d1b9-103">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="9d1b9-103">IMAPITable::SortTable</span></span>

<span data-ttu-id="9d1b9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9d1b9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9d1b9-105">O método imApitable **:: SortTable** ordena as linhas da tabela, dependendo dos critérios de classificação.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-105">The **IMAPITable::SortTable** method orders the rows of the table, depending on sort criteria.</span></span> 
  
```cpp
HRESULT SortTable(
LPSSortOrderSet lpSortCriteria,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="9d1b9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9d1b9-106">Parameters</span></span>

<span data-ttu-id="9d1b9-107">_lpSortCriteria_</span><span class="sxs-lookup"><span data-stu-id="9d1b9-107">_lpSortCriteria_</span></span>
  
> <span data-ttu-id="9d1b9-108">no Ponteiro para uma estrutura [SSortOrderSet](ssortorderset.md) que contém o critério de classificação a ser aplicado.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-108">[in] Pointer to an [SSortOrderSet](ssortorderset.md) structure that contains the sort criteria to apply.</span></span> <span data-ttu-id="9d1b9-109">Passar uma estrutura **SSortOrderSet** que contém zero colunas indica que a tabela não precisa ser classificada em uma ordem específica.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-109">Passing an **SSortOrderSet** structure that contains zero columns indicates that the table does not have to be sorted in any particular order.</span></span> 
    
<span data-ttu-id="9d1b9-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9d1b9-110">_ulFlags_</span></span>
  
> <span data-ttu-id="9d1b9-111">no Bitmask de sinalizadores que controlam o intervalo da operação imApitable **:: SortTable** .</span><span class="sxs-lookup"><span data-stu-id="9d1b9-111">[in] Bitmask of flags that controls the timing of the **IMAPITable::SortTable** operation.</span></span> <span data-ttu-id="9d1b9-112">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="9d1b9-112">The following flags can be set:</span></span> 
    
<span data-ttu-id="9d1b9-113">TBL_ASYNC</span><span class="sxs-lookup"><span data-stu-id="9d1b9-113">TBL_ASYNC</span></span> 
  
> <span data-ttu-id="9d1b9-114">Inicia a operação de forma assíncrona e retorna antes de a operação ser concluída.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-114">Starts the operation asynchronously and returns before the operation is complete.</span></span>
    
<span data-ttu-id="9d1b9-115">TBL_BATCH</span><span class="sxs-lookup"><span data-stu-id="9d1b9-115">TBL_BATCH</span></span> 
  
> <span data-ttu-id="9d1b9-116">Adia a conclusão da classificação até que os dados da tabela sejam necessários.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-116">Defers the completion of the sort until the data in the table is required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9d1b9-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9d1b9-117">Return value</span></span>

<span data-ttu-id="9d1b9-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="9d1b9-118">S_OK</span></span> 
  
> <span data-ttu-id="9d1b9-119">A operação de classificação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-119">The sort operation was successful.</span></span>
    
<span data-ttu-id="9d1b9-120">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="9d1b9-120">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="9d1b9-121">Outra operação está em andamento, o que impede a inicialização da operação de classificação.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-121">Another operation is in progress that prevents the sort operation from starting.</span></span> <span data-ttu-id="9d1b9-122">A operação em andamento deve ter permissão para ser concluída ou deve ser interrompida.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-122">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="9d1b9-123">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="9d1b9-123">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="9d1b9-124">A tabela não dá suporte ao tipo de classificação solicitada.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-124">The table does not support the type of sorting requested.</span></span>
    
<span data-ttu-id="9d1b9-125">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="9d1b9-125">MAPI_E_TOO_COMPLEX</span></span> 
  
> <span data-ttu-id="9d1b9-126">A tabela não pode executar a operação porque o critério de classificação específico apontado pelo parâmetro _lpSortCriteria_ é muito complexo.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-126">The table cannot perform the operation because the particular sort criteria pointed to by the  _lpSortCriteria_ parameter is too complex.</span></span> <span data-ttu-id="9d1b9-127">**SortTable** pode retornar MAPI_E_TOO_COMPLEX sob as condições a seguir.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-127">**SortTable** can return MAPI_E_TOO_COMPLEX under the following conditions.</span></span> 
    
   - <span data-ttu-id="9d1b9-128">Uma operação de classificação é solicitada para uma coluna de propriedade que a implementação não pode classificar.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-128">A sort operation is requested for a property column that the implementation cannot sort.</span></span>
    
   - <span data-ttu-id="9d1b9-129">A implementação não é compatível com a ordem de classificação solicitada no membro **ulOrder** da estrutura **SSortOrderSet** .</span><span class="sxs-lookup"><span data-stu-id="9d1b9-129">The implementation does not support the sort order requested in the **ulOrder** member of the **SSortOrderSet** structure.</span></span> 
    
   - <span data-ttu-id="9d1b9-130">O número de colunas a serem classificadas, conforme especificado no membro **cSorts** no **SSortOrderSet**, é maior do que a implementação pode lidar.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-130">The number of columns to be sorted, as specified in the **cSorts** member in **SSortOrderSet**, is larger than the implementation can handle.</span></span>
    
   - <span data-ttu-id="9d1b9-131">Uma operação de classificação é solicitada, conforme indicado por uma marca de propriedade no **SSortOrderSet**, com base em uma propriedade que não está no conjunto disponível ou ativo e a implementação não dá suporte à classificação de propriedades que não estão no conjunto disponível.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-131">A sort operation is requested, as indicated by a property tag in **SSortOrderSet**, based on a property that is not in the available or active set and the implementation does not support sorting on properties not in the available set.</span></span>
    
   - <span data-ttu-id="9d1b9-132">Uma propriedade é especificada várias vezes em um conjunto de ordem de classificação, conforme indicado por várias instâncias da mesma marca de propriedade e a implementação não pode executar tal operação de classificação.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-132">One property is specified multiple times in a sort order set, as indicated by multiple instances of the same property tag, and the implementation cannot perform such a sort operation.</span></span>
    
   - <span data-ttu-id="9d1b9-133">Uma operação de classificação baseada em colunas de propriedade com valores múltiplos é solicitada usando MVI_FLAG e a implementação não dá suporte à classificação em Propriedades de vários valores.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-133">A sort operation based on multivalued property columns is requested using MVI_FLAG and the implementation does not support sorting on multivalued properties.</span></span> 
    
   - <span data-ttu-id="9d1b9-134">Uma marca de propriedade para uma propriedade no **SSortOrderSet** especifica uma propriedade ou tipo que a implementação não suporta.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-134">A property tag for a property in **SSortOrderSet** specifies a property or type that the implementation does not support.</span></span> 
    
   - <span data-ttu-id="9d1b9-135">Uma operação de classificação diferente de uma que prossegue através da tabela da propriedade **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) forward é especificada somente para uma tabela de anexo que ofereça suporte a esse tipo de classificação.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-135">A sort operation other than one that proceeds through the table from the **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) property forward is specified only for an attachment table that supports this type of sorting.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9d1b9-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="9d1b9-136">Remarks</span></span>

<span data-ttu-id="9d1b9-137">O método imApitable **:: SortTable** ordena as linhas em um modo de exibição de tabela.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-137">The **IMAPITable::SortTable** method orders the rows in a table view.</span></span> <span data-ttu-id="9d1b9-138">Enquanto algumas tabelas oferecem suporte à classificação padrão e categorizadas em várias colunas de chave de classificação, outras tabelas são mais limitadas no suporte.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-138">Whereas some tables support both standard and categorized sorting on various sort key columns, other tables are more limited in their support.</span></span> <span data-ttu-id="9d1b9-139">Os provedores de catálogo de endereços normalmente não oferecem suporte à classificação de tabelas.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-139">Address book providers ordinarily do not support table sorting.</span></span> <span data-ttu-id="9d1b9-140">Os provedores de repositórios de mensagens geralmente dão suporte à ordenação de que eles mantêm a ordem de classificação das pastas que resultam quando uma tabela completa (uma tabela sem restrições) é classificada.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-140">Message store providers usually support sorting to the extent that they keep the sort order of folders that results when a full table (a table without restrictions) is sorted.</span></span> 
  
<span data-ttu-id="9d1b9-141">Algumas tabelas permitem que a classificação seja feita em qualquer coluna de tabela.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-141">Some tables allow sorting to be done on any table column.</span></span> <span data-ttu-id="9d1b9-142">Outras tabelas não; as colunas não incluídas no modo de exibição de tabela não são afetadas por uma chamada **SortTable** .</span><span class="sxs-lookup"><span data-stu-id="9d1b9-142">Other tables do not; columns not included in the table view are unaffected by a **SortTable** call.</span></span> <span data-ttu-id="9d1b9-143">Algumas tabelas exigem que as chaves de classificação sejam criadas apenas com colunas no conjunto de colunas atual da tabela.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-143">Some tables require that sort keys be built only with columns in the table's current column set.</span></span> 
  
<span data-ttu-id="9d1b9-144">Uma tabela pode retornar MAPI_E_NO_SUPPORT ou MAPI_E_TOO_COMPLEX de **SortTable** quando não puder concluir uma operação de classificação.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-144">A table can return either MAPI_E_NO_SUPPORT or MAPI_E_TOO_COMPLEX from **SortTable** when it cannot complete a sort operation.</span></span> <span data-ttu-id="9d1b9-145">Além disso, os provedores de repositório não são garantidos para honrar o conjunto de ordem de classificação especificado para tabelas de hierarquia.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-145">Moreover, store providers are not guaranteed to honor the sort order set specified for hierarchy tables.</span></span> 
  
<span data-ttu-id="9d1b9-146">Quando há zero colunas na estrutura [SSortOrderSet](ssortorderset.md) apontadas pelo parâmetro _lpSortCriteria_ , a tabela retorna o conjunto de colunas atual.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-146">When there are zero columns in the [SSortOrderSet](ssortorderset.md) structure pointed to by the  _lpSortCriteria_ parameter, the table returns the current column set.</span></span> <span data-ttu-id="9d1b9-147">A ordem de classificação atual pode ser recuperada chamando o método [IMAPITable:: QuerySortOrder](imapitable-querysortorder.md) da tabela.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-147">The current sort order can be retrieved by calling the table's [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
<span data-ttu-id="9d1b9-148">Todos os indicadores de uma tabela são invalidados e devem ser excluídos quando uma chamada para **SortTable** é feita, e o indicador BOOKMARK_CURRENT que indica a posição atual do cursor, deve ser definido para o início da tabela.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-148">All bookmarks for a table are invalidated and should be deleted when a call to **SortTable** is made, and the BOOKMARK_CURRENT bookmark that indicates the current cursor position, should be set to the beginning of the table.</span></span> 
  
<span data-ttu-id="9d1b9-149">Se você estiver classificando em uma coluna que contenha uma propriedade de vários valores sem o sinalizador MVI_FLAG definido, os valores da coluna serão tratados como uma tupla completamente ordenada.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-149">If you are sorting on a column that contains a multivalued property without the MVI_FLAG flag set, the column's values are treated as a completely ordered tuple.</span></span> <span data-ttu-id="9d1b9-150">Uma comparação de duas colunas com vários valores compara os elementos de coluna em ordem, relatando a relação entre as colunas na primeira inequação e retorna igualdade somente se as colunas que estão sendo comparadas contiverem os mesmos valores na mesma ordem.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-150">A comparison of two multivalued columns compares the column elements in order, reporting the relation of the columns at the first inequality, and returns equality only if the columns being compared contain the same values in the same order.</span></span> <span data-ttu-id="9d1b9-151">Se uma coluna tiver menos valores do que o outro, a relação relatada será a de um valor nulo para o outro valor.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-151">If one column has fewer values than the other, the reported relation is that of a null value to the other value.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="9d1b9-152">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="9d1b9-152">Notes to callers</span></span>

<span data-ttu-id="9d1b9-153">**SortTable** funciona de forma síncrona, a menos que você defina um dos sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-153">**SortTable** operates synchronously unless you set one of the flags.</span></span> <span data-ttu-id="9d1b9-154">Se você definir o sinalizador TBL_BATCH, **SortTable** adia a operação de classificação, a menos que você solicite os dados.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-154">If you set the TBL_BATCH flag, **SortTable** postpones the sort operation unless you request the data.</span></span> <span data-ttu-id="9d1b9-155">Se o sinalizador TBL_ASYNC for definido, **SortTable** funciona de forma assíncrona, potencialmente retornando antes da conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-155">If the TBL_ASYNC flag is set, **SortTable** operates asynchronously, potentially returning before the completion of the operation.</span></span> 
  
<span data-ttu-id="9d1b9-156">Chame o método imApitable [:: Abort](imapitable-abort.md) para interromper uma operação assíncrona em andamento se a classificação deve ser feita imediatamente.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-156">Call the [IMAPITable::Abort](imapitable-abort.md) method to stop an asynchronous operation in progress if your sort must be done immediately.</span></span> <span data-ttu-id="9d1b9-157">Se **SortTable** não puder continuar porque uma ou mais operações assíncronas na tabela estão em andamento, ela retornará MAPI_E_BUSY.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-157">If **SortTable** cannot continue because one or more asynchronous operations on the table are in progress, it returns MAPI_E_BUSY.</span></span> 
  
<span data-ttu-id="9d1b9-158">Para melhor desempenho, chame \*\*\*\* SetColumns para personalizar o conjunto de colunas da tabela e **restrinja** para limitar o número de linhas na tabela antes de chamar **SortTable** para executar a classificação.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-158">For best performance, call **SetColumns** to customize the table's column set and **Restrict** to limit the number of rows in the table before you call **SortTable** to perform the sort.</span></span> 
  
<span data-ttu-id="9d1b9-159">Sempre \*\*\*\* que SortTable falhar, a ordem de classificação que estava em vigor antes da falha ainda estará em vigor.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-159">Whenever **SortTable** fails, the sort order that was in effect before the failure is still in effect.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9d1b9-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="9d1b9-160">See also</span></span>

- [<span data-ttu-id="9d1b9-161">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="9d1b9-161">IMAPITable::Abort</span></span>](imapitable-abort.md)
- [<span data-ttu-id="9d1b9-162">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="9d1b9-162">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
- [<span data-ttu-id="9d1b9-163">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="9d1b9-163">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
- [<span data-ttu-id="9d1b9-164">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="9d1b9-164">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
- [<span data-ttu-id="9d1b9-165">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="9d1b9-165">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
- [<span data-ttu-id="9d1b9-166">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="9d1b9-166">SSortOrderSet</span></span>](ssortorderset.md)
- [<span data-ttu-id="9d1b9-167">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9d1b9-167">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

