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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432363"
---
# <a name="imapitablesorttable"></a><span data-ttu-id="af427-103">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="af427-103">IMAPITable::SortTable</span></span>

<span data-ttu-id="af427-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="af427-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="af427-105">O **método IMAPITable::SortTable** ordena as linhas da tabela, dependendo dos critérios de classificação.</span><span class="sxs-lookup"><span data-stu-id="af427-105">The **IMAPITable::SortTable** method orders the rows of the table, depending on sort criteria.</span></span> 
  
```cpp
HRESULT SortTable(
LPSSortOrderSet lpSortCriteria,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="af427-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="af427-106">Parameters</span></span>

<span data-ttu-id="af427-107">_lpSortCriteria_</span><span class="sxs-lookup"><span data-stu-id="af427-107">_lpSortCriteria_</span></span>
  
> <span data-ttu-id="af427-108">[in] Ponteiro para uma [estrutura SSortOrderSet](ssortorderset.md) que contém os critérios de classificação a aplicar.</span><span class="sxs-lookup"><span data-stu-id="af427-108">[in] Pointer to an [SSortOrderSet](ssortorderset.md) structure that contains the sort criteria to apply.</span></span> <span data-ttu-id="af427-109">Passar uma **estrutura SSortOrderSet** que contém zero colunas indica que a tabela não precisa ser ordenada em nenhuma ordem específica.</span><span class="sxs-lookup"><span data-stu-id="af427-109">Passing an **SSortOrderSet** structure that contains zero columns indicates that the table does not have to be sorted in any particular order.</span></span> 
    
<span data-ttu-id="af427-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="af427-110">_ulFlags_</span></span>
  
> <span data-ttu-id="af427-111">[in] Máscara de bits de sinalizadores que controla o tempo da **operação IMAPITable::SortTable.**</span><span class="sxs-lookup"><span data-stu-id="af427-111">[in] Bitmask of flags that controls the timing of the **IMAPITable::SortTable** operation.</span></span> <span data-ttu-id="af427-112">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="af427-112">The following flags can be set:</span></span> 
    
<span data-ttu-id="af427-113">TBL_ASYNC</span><span class="sxs-lookup"><span data-stu-id="af427-113">TBL_ASYNC</span></span> 
  
> <span data-ttu-id="af427-114">Inicia a operação de forma assíncrona e retorna antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="af427-114">Starts the operation asynchronously and returns before the operation is complete.</span></span>
    
<span data-ttu-id="af427-115">TBL_BATCH</span><span class="sxs-lookup"><span data-stu-id="af427-115">TBL_BATCH</span></span> 
  
> <span data-ttu-id="af427-116">Adia a conclusão da classificação até que os dados na tabela são necessários.</span><span class="sxs-lookup"><span data-stu-id="af427-116">Defers the completion of the sort until the data in the table is required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="af427-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="af427-117">Return value</span></span>

<span data-ttu-id="af427-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="af427-118">S_OK</span></span> 
  
> <span data-ttu-id="af427-119">A operação de classificação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="af427-119">The sort operation was successful.</span></span>
    
<span data-ttu-id="af427-120">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="af427-120">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="af427-121">Outra operação está em andamento que impede o início da operação de classificação.</span><span class="sxs-lookup"><span data-stu-id="af427-121">Another operation is in progress that prevents the sort operation from starting.</span></span> <span data-ttu-id="af427-122">A operação em andamento deve ter permissão para ser concluída ou deve ser interrompida.</span><span class="sxs-lookup"><span data-stu-id="af427-122">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="af427-123">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="af427-123">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="af427-124">A tabela não dá suporte ao tipo de classificação solicitado.</span><span class="sxs-lookup"><span data-stu-id="af427-124">The table does not support the type of sorting requested.</span></span>
    
<span data-ttu-id="af427-125">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="af427-125">MAPI_E_TOO_COMPLEX</span></span> 
  
> <span data-ttu-id="af427-126">A tabela não pode executar a operação porque os critérios de classificação específicos apontados pelo parâmetro  _lpSortCriteria_ são muito complexos.</span><span class="sxs-lookup"><span data-stu-id="af427-126">The table cannot perform the operation because the particular sort criteria pointed to by the  _lpSortCriteria_ parameter is too complex.</span></span> <span data-ttu-id="af427-127">**SortTable** pode retornar MAPI_E_TOO_COMPLEX sob as seguintes condições.</span><span class="sxs-lookup"><span data-stu-id="af427-127">**SortTable** can return MAPI_E_TOO_COMPLEX under the following conditions.</span></span> 
    
   - <span data-ttu-id="af427-128">Uma operação de classificação é solicitada para uma coluna de propriedade que a implementação não pode classificar.</span><span class="sxs-lookup"><span data-stu-id="af427-128">A sort operation is requested for a property column that the implementation cannot sort.</span></span>
    
   - <span data-ttu-id="af427-129">A implementação não dá suporte à ordem de classificação solicitada no **membro ulOrder** da **estrutura SSortOrderSet.**</span><span class="sxs-lookup"><span data-stu-id="af427-129">The implementation does not support the sort order requested in the **ulOrder** member of the **SSortOrderSet** structure.</span></span> 
    
   - <span data-ttu-id="af427-130">O número de colunas a serem ordenadas, conforme especificado no membro **cSorts** em **SSortOrderSet**, é maior do que a implementação pode manipular.</span><span class="sxs-lookup"><span data-stu-id="af427-130">The number of columns to be sorted, as specified in the **cSorts** member in **SSortOrderSet**, is larger than the implementation can handle.</span></span>
    
   - <span data-ttu-id="af427-131">Uma operação de classificação é solicitada, conforme indicado por uma marca de propriedade em **SSortOrderSet**, com base em uma propriedade que não está no conjunto disponível ou ativo e a implementação não suporta a classificação em propriedades que não estão no conjunto disponível.</span><span class="sxs-lookup"><span data-stu-id="af427-131">A sort operation is requested, as indicated by a property tag in **SSortOrderSet**, based on a property that is not in the available or active set and the implementation does not support sorting on properties not in the available set.</span></span>
    
   - <span data-ttu-id="af427-132">Uma propriedade é especificada várias vezes em um conjunto de ordem de classificação, conforme indicado por várias instâncias da mesma marca de propriedade, e a implementação não pode executar essa operação de classificação.</span><span class="sxs-lookup"><span data-stu-id="af427-132">One property is specified multiple times in a sort order set, as indicated by multiple instances of the same property tag, and the implementation cannot perform such a sort operation.</span></span>
    
   - <span data-ttu-id="af427-133">Uma operação de classificação com base em colunas de propriedade de múltiplos valores é solicitada usando MVI_FLAG e a implementação não dá suporte à classificação em propriedades de vários valores.</span><span class="sxs-lookup"><span data-stu-id="af427-133">A sort operation based on multivalued property columns is requested using MVI_FLAG and the implementation does not support sorting on multivalued properties.</span></span> 
    
   - <span data-ttu-id="af427-134">A property tag for a property in **SSortOrderSet** specifies a property or type that the implementation does not support.</span><span class="sxs-lookup"><span data-stu-id="af427-134">A property tag for a property in **SSortOrderSet** specifies a property or type that the implementation does not support.</span></span> 
    
   - <span data-ttu-id="af427-135">Uma operação de classificação diferente de uma que prossiga pela tabela a partir da propriedade **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) para frente é especificada apenas para uma tabela de anexos que oferece suporte a esse tipo de classificação.</span><span class="sxs-lookup"><span data-stu-id="af427-135">A sort operation other than one that proceeds through the table from the **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) property forward is specified only for an attachment table that supports this type of sorting.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="af427-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="af427-136">Remarks</span></span>

<span data-ttu-id="af427-137">O **método IMAPITable::SortTable** ordena as linhas em um modo de exibição de tabela.</span><span class="sxs-lookup"><span data-stu-id="af427-137">The **IMAPITable::SortTable** method orders the rows in a table view.</span></span> <span data-ttu-id="af427-138">Enquanto algumas tabelas suportam classificação padrão e categorizada em várias colunas de chave de classificação, outras tabelas são mais limitadas em seu suporte.</span><span class="sxs-lookup"><span data-stu-id="af427-138">Whereas some tables support both standard and categorized sorting on various sort key columns, other tables are more limited in their support.</span></span> <span data-ttu-id="af427-139">Os provedores de agendamento de endereço normalmente não suportam a classificação de tabelas.</span><span class="sxs-lookup"><span data-stu-id="af427-139">Address book providers ordinarily do not support table sorting.</span></span> <span data-ttu-id="af427-140">Os provedores de armazenamento de mensagens geralmente suportam a classificação na medida em que mantêm a ordem de classificação de pastas que resulta quando uma tabela completa (uma tabela sem restrições) é ordenada.</span><span class="sxs-lookup"><span data-stu-id="af427-140">Message store providers usually support sorting to the extent that they keep the sort order of folders that results when a full table (a table without restrictions) is sorted.</span></span> 
  
<span data-ttu-id="af427-141">Algumas tabelas permitem que a classificação seja feita em qualquer coluna de tabela.</span><span class="sxs-lookup"><span data-stu-id="af427-141">Some tables allow sorting to be done on any table column.</span></span> <span data-ttu-id="af427-142">Outras tabelas não; colunas não incluídas no exibição de tabela não são afetadas por uma **chamada SortTable.**</span><span class="sxs-lookup"><span data-stu-id="af427-142">Other tables do not; columns not included in the table view are unaffected by a **SortTable** call.</span></span> <span data-ttu-id="af427-143">Algumas tabelas exigem que as chaves de classificação sejam criadas somente com colunas no conjunto de colunas atual da tabela.</span><span class="sxs-lookup"><span data-stu-id="af427-143">Some tables require that sort keys be built only with columns in the table's current column set.</span></span> 
  
<span data-ttu-id="af427-144">Uma tabela pode retornar uma MAPI_E_NO_SUPPORT ou MAPI_E_TOO_COMPLEX da **Tabela** de Classificação quando não puder concluir uma operação de classificação.</span><span class="sxs-lookup"><span data-stu-id="af427-144">A table can return either MAPI_E_NO_SUPPORT or MAPI_E_TOO_COMPLEX from **SortTable** when it cannot complete a sort operation.</span></span> <span data-ttu-id="af427-145">Além disso, os provedores de armazenamento não têm garantia de atender ao conjunto de ordem de classificação especificado para tabelas de hierarquia.</span><span class="sxs-lookup"><span data-stu-id="af427-145">Moreover, store providers are not guaranteed to honor the sort order set specified for hierarchy tables.</span></span> 
  
<span data-ttu-id="af427-146">Quando há zero colunas na estrutura [SSortOrderSet](ssortorderset.md) apontada pelo parâmetro  _lpSortCriteria,_ a tabela retorna o conjunto de colunas atual.</span><span class="sxs-lookup"><span data-stu-id="af427-146">When there are zero columns in the [SSortOrderSet](ssortorderset.md) structure pointed to by the  _lpSortCriteria_ parameter, the table returns the current column set.</span></span> <span data-ttu-id="af427-147">A ordem de classificação atual pode ser recuperada chamando o método [IMAPITable::QuerySortOrder da](imapitable-querysortorder.md) tabela.</span><span class="sxs-lookup"><span data-stu-id="af427-147">The current sort order can be retrieved by calling the table's [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
<span data-ttu-id="af427-148">Todos os indicadores de uma tabela são invalidados e devem ser excluídos quando uma chamada para **SortTable** é feita, e o indicador BOOKMARK_CURRENT que indica a posição atual do cursor deve ser definido como o início da tabela.</span><span class="sxs-lookup"><span data-stu-id="af427-148">All bookmarks for a table are invalidated and should be deleted when a call to **SortTable** is made, and the BOOKMARK_CURRENT bookmark that indicates the current cursor position, should be set to the beginning of the table.</span></span> 
  
<span data-ttu-id="af427-149">Se você estiver classificação em uma coluna que contém uma propriedade de valores múltiplos sem o MVI_FLAG de sinalização definido, os valores da coluna serão tratados como uma tupla completamente ordenada.</span><span class="sxs-lookup"><span data-stu-id="af427-149">If you are sorting on a column that contains a multivalued property without the MVI_FLAG flag set, the column's values are treated as a completely ordered tuple.</span></span> <span data-ttu-id="af427-150">Uma comparação de duas colunas de múltiplos valores compara os elementos de coluna na ordem, relatando a relação das colunas na primeira situação e retorna a igualdade somente se as colunas que estão sendo comparadas contêm os mesmos valores na mesma ordem.</span><span class="sxs-lookup"><span data-stu-id="af427-150">A comparison of two multivalued columns compares the column elements in order, reporting the relation of the columns at the first inequality, and returns equality only if the columns being compared contain the same values in the same order.</span></span> <span data-ttu-id="af427-151">Se uma coluna tiver menos valores do que a outra, a relação relatada será aquela de um valor nulo para o outro valor.</span><span class="sxs-lookup"><span data-stu-id="af427-151">If one column has fewer values than the other, the reported relation is that of a null value to the other value.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="af427-152">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="af427-152">Notes to callers</span></span>

<span data-ttu-id="af427-153">**SortTable** funciona de forma síncrona, a menos que você de definir um dos sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="af427-153">**SortTable** operates synchronously unless you set one of the flags.</span></span> <span data-ttu-id="af427-154">Se você definir o sinalizador TBL_BATCH, **SortTable** adia a operação de classificação, a menos que você solicite os dados.</span><span class="sxs-lookup"><span data-stu-id="af427-154">If you set the TBL_BATCH flag, **SortTable** postpones the sort operation unless you request the data.</span></span> <span data-ttu-id="af427-155">Se o TBL_ASYNC sinalizador estiver definido, **SortTable** opera de forma assíncrona, potencialmente retornando antes da conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="af427-155">If the TBL_ASYNC flag is set, **SortTable** operates asynchronously, potentially returning before the completion of the operation.</span></span> 
  
<span data-ttu-id="af427-156">Chame o [método IMAPITable::Abort](imapitable-abort.md) para interromper uma operação assíncrona em andamento se sua classificação tiver que ser feita imediatamente.</span><span class="sxs-lookup"><span data-stu-id="af427-156">Call the [IMAPITable::Abort](imapitable-abort.md) method to stop an asynchronous operation in progress if your sort must be done immediately.</span></span> <span data-ttu-id="af427-157">Se **SortTable não** puder continuar porque uma ou mais operações assíncronas na tabela estão em andamento, ela retornará MAPI_E_BUSY.</span><span class="sxs-lookup"><span data-stu-id="af427-157">If **SortTable** cannot continue because one or more asynchronous operations on the table are in progress, it returns MAPI_E_BUSY.</span></span> 
  
<span data-ttu-id="af427-158">Para melhorar o desempenho, chame **SetColumns** para personalizar o conjunto de colunas da tabela e **Restringir** para limitar o número de linhas na tabela antes de chamar **SortTable** para executar a classificação.</span><span class="sxs-lookup"><span data-stu-id="af427-158">For best performance, call **SetColumns** to customize the table's column set and **Restrict** to limit the number of rows in the table before you call **SortTable** to perform the sort.</span></span> 
  
<span data-ttu-id="af427-159">Sempre **que SortTable** falhar, a ordem de classificação que estava em vigor antes da falha ainda está em vigor.</span><span class="sxs-lookup"><span data-stu-id="af427-159">Whenever **SortTable** fails, the sort order that was in effect before the failure is still in effect.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="af427-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="af427-160">See also</span></span>

- [<span data-ttu-id="af427-161">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="af427-161">IMAPITable::Abort</span></span>](imapitable-abort.md)
- [<span data-ttu-id="af427-162">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="af427-162">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
- [<span data-ttu-id="af427-163">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="af427-163">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
- [<span data-ttu-id="af427-164">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="af427-164">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
- [<span data-ttu-id="af427-165">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="af427-165">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
- [<span data-ttu-id="af427-166">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="af427-166">SSortOrderSet</span></span>](ssortorderset.md)
- [<span data-ttu-id="af427-167">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="af427-167">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

