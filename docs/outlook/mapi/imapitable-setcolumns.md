---
title: IMAPITableSetColumns
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SetColumns
api_type:
- COM
ms.assetid: 9a39cf8d-df0f-493c-b272-f15c65b3f15e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 897330feb216dbc3ab143378977c77141cf488f0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416346"
---
# <a name="imapitablesetcolumns"></a><span data-ttu-id="e42cf-103">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="e42cf-103">IMAPITable::SetColumns</span></span>

  
  
<span data-ttu-id="e42cf-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e42cf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e42cf-105">Define as propriedades específicas e a ordem das propriedades a serem exibidas como colunas na tabela.</span><span class="sxs-lookup"><span data-stu-id="e42cf-105">Defines the particular properties and order of properties to appear as columns in the table.</span></span>
  
```cpp
HRESULT SetColumns(
LPSPropTagArray lpPropTagArray,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="e42cf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e42cf-106">Parameters</span></span>

 <span data-ttu-id="e42cf-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="e42cf-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="e42cf-108">no Ponteiro para uma matriz de marcas de propriedade que identificam as propriedades a serem incluídas como colunas na tabela.</span><span class="sxs-lookup"><span data-stu-id="e42cf-108">[in] Pointer to an array of property tags identifying properties to be included as columns in the table.</span></span> <span data-ttu-id="e42cf-109">A parte de tipo de propriedade de cada marca pode ser definida como um tipo válido ou **PR_NULL** para reservar espaço para adições subsequentes.</span><span class="sxs-lookup"><span data-stu-id="e42cf-109">The property type portion of each tag can be set to a valid type or to **PR_NULL** to reserve space for subsequent additions.</span></span> <span data-ttu-id="e42cf-110">O parâmetro _lpPropTagArray_ não pode ser definido como nulo; cada tabela deve ter pelo menos uma coluna.</span><span class="sxs-lookup"><span data-stu-id="e42cf-110">The  _lpPropTagArray_ parameter cannot be set to NULL; every table must have at least one column.</span></span> 
    
 <span data-ttu-id="e42cf-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e42cf-111">_ulFlags_</span></span>
  
> <span data-ttu-id="e42cf-112">no Bitmask de sinalizadores que controlam o retorno de uma chamada assíncrona para setColumns, por exemplo, quando setColumns é usado na notificação. \*\*\*\* \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="e42cf-112">[in] Bitmask of flags that controls the return of an asynchronous call to **SetColumns**, for example when **SetColumns** is used in notification.</span></span> <span data-ttu-id="e42cf-113">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="e42cf-113">The following flags can be set:</span></span> 
    
<span data-ttu-id="e42cf-114">TBL_ASYNC</span><span class="sxs-lookup"><span data-stu-id="e42cf-114">TBL_ASYNC</span></span> 
  
> <span data-ttu-id="e42cf-115">Solicita que a operação de configuração de coluna seja executada \*\*\*\* de forma assíncrona fazendo com que SetColumns possa retornar antes de a operação ter sido totalmente concluída.</span><span class="sxs-lookup"><span data-stu-id="e42cf-115">Requests that the column setting operation be performed asynchronously causing **SetColumns** to potentially return before the operation has fully completed.</span></span> 
    
<span data-ttu-id="e42cf-116">TBL_BATCH</span><span class="sxs-lookup"><span data-stu-id="e42cf-116">TBL_BATCH</span></span> 
  
> <span data-ttu-id="e42cf-117">Permite que a tabela adie a operação de configuração da coluna até que os dados sejam realmente necessários.</span><span class="sxs-lookup"><span data-stu-id="e42cf-117">Permits the table to postpone the column setting operation until the data is actually required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e42cf-118">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e42cf-118">Return value</span></span>

<span data-ttu-id="e42cf-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="e42cf-119">S_OK</span></span> 
  
> <span data-ttu-id="e42cf-120">A operação de configuração de coluna foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="e42cf-120">The column setting operation was successful.</span></span>
    
<span data-ttu-id="e42cf-121">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="e42cf-121">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="e42cf-122">Outra operação está em andamento, o que impede a inicialização da operação de configuração da coluna.</span><span class="sxs-lookup"><span data-stu-id="e42cf-122">Another operation is in progress that prevents the column setting operation from starting.</span></span> <span data-ttu-id="e42cf-123">A operação em andamento deve ter permissão para ser concluída ou deve ser interrompida.</span><span class="sxs-lookup"><span data-stu-id="e42cf-123">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e42cf-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="e42cf-124">Remarks</span></span>

<span data-ttu-id="e42cf-125">O conjunto de colunas de uma tabela é o grupo de propriedades que compõem as colunas das linhas da tabela.</span><span class="sxs-lookup"><span data-stu-id="e42cf-125">The column set of a table is the group of properties that make up the columns for the rows in the table.</span></span> <span data-ttu-id="e42cf-126">Há uma coluna padrão definida para cada tipo de tabela.</span><span class="sxs-lookup"><span data-stu-id="e42cf-126">There is a default column set for each type of table.</span></span> <span data-ttu-id="e42cf-127">O conjunto de colunas padrão é composto pelas propriedades que o implementador de tabelas inclui automaticamente.</span><span class="sxs-lookup"><span data-stu-id="e42cf-127">The default column set is made up of the properties that the table implementer automatically includes.</span></span> <span data-ttu-id="e42cf-128">Os usuários de tabela podem alterar esse conjunto padrão chamando o método imApitable **::** SetColumns.</span><span class="sxs-lookup"><span data-stu-id="e42cf-128">Table users can alter this default set by calling the **IMAPITable::SetColumns** method.</span></span> <span data-ttu-id="e42cf-129">Eles podem solicitar que outras colunas sejam adicionadas ao conjunto padrão se o implementador de tabelas oferecer suporte a essas colunas ou se a ordem das colunas for alterada.</span><span class="sxs-lookup"><span data-stu-id="e42cf-129">They can request that other columns be added to the default set if the table implementer supports them that columns be removed, or that the order of columns be changed.</span></span> <span data-ttu-id="e42cf-130">\*\*\*\* SetColumns especifica as colunas que são retornadas com cada linha e a ordem dessas colunas dentro da linha.</span><span class="sxs-lookup"><span data-stu-id="e42cf-130">**SetColumns** specifies the columns that are returned with each row and the order of these columns within the row.</span></span> 
  
<span data-ttu-id="e42cf-131">O sucesso da operação \*\*\*\* SetColumns é aparente somente depois que uma chamada subsequente foi feita para recuperar os dados da tabela.</span><span class="sxs-lookup"><span data-stu-id="e42cf-131">The success of the **SetColumns** operation is apparent only after a subsequent call has been made to retrieve the data of the table.</span></span> <span data-ttu-id="e42cf-132">Em seguida, os erros são relatados.</span><span class="sxs-lookup"><span data-stu-id="e42cf-132">It is then that any errors are reported.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="e42cf-133">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="e42cf-133">Notes to implementers</span></span>

<span data-ttu-id="e42cf-134">Alguns provedores permitem uma \*\*\*\* chamada SetColumns para ordenar somente colunas da tabela que fazem parte das colunas disponíveis para um modo de exibição de tabela.</span><span class="sxs-lookup"><span data-stu-id="e42cf-134">Some providers allow a **SetColumns** call to order only table columns that are part of the available columns for a table view.</span></span> <span data-ttu-id="e42cf-135">Outros provedores permitem uma \*\*\*\* chamada SetColumns para ordenar todas as colunas da tabela, incluindo as que contêm propriedades que não estão no conjunto de colunas original.</span><span class="sxs-lookup"><span data-stu-id="e42cf-135">Other providers allow a **SetColumns** call to order all table columns, including those containing properties not in the original column set.</span></span> 
  
<span data-ttu-id="e42cf-136">Quando TBL_BATCH é definido para operações assíncronas, os provedores devem retornar um tipo de propriedade de PT_ERROR e um valor de propriedade de NULL para colunas que não são suportadas.</span><span class="sxs-lookup"><span data-stu-id="e42cf-136">When TBL_BATCH is set for asynchronous operations, providers should return a property type of PT_ERROR and a property value of NULL for columns that are not supported.</span></span>
  
<span data-ttu-id="e42cf-137">Você não precisa responder ao sinalizador TBL_ASYNC solicitando que a operação seja assíncrona.</span><span class="sxs-lookup"><span data-stu-id="e42cf-137">You do not need to respond to the TBL_ASYNC flag requesting that the operation be asynchronous.</span></span> <span data-ttu-id="e42cf-138">Se você não oferecer suporte à definição de conjunto de colunas assíncrono, execute a operação de forma síncrona.</span><span class="sxs-lookup"><span data-stu-id="e42cf-138">If you do not support asynchronous column set definition, perform the operation synchronously.</span></span> <span data-ttu-id="e42cf-139">Se você puder suportar o sinalizador TBL_ASYNC e outra operação assíncrona ainda estiver em andamento, retorne MAPI_E_BUSY.</span><span class="sxs-lookup"><span data-stu-id="e42cf-139">If you can support the TBL_ASYNC flag and another asynchronous operation is still in progress, return MAPI_E_BUSY.</span></span> <span data-ttu-id="e42cf-140">Caso contrário, retorna S_OK independentemente de você ter ou não suporte a todas as propriedades incluídas na matriz de marca de propriedade.</span><span class="sxs-lookup"><span data-stu-id="e42cf-140">Otherwise, return S_OK regardless of whether or not you support all of the properties included in the property tag array.</span></span> <span data-ttu-id="e42cf-141">Os erros resultantes de propriedades sem suporte devem ser retornados \*\*\*\* de métodos imapitados que recuperam dados, como **QueryRows**.</span><span class="sxs-lookup"><span data-stu-id="e42cf-141">Errors resulting from unsupported properties should be returned from **IMAPITable** methods that retrieve data, such as **QueryRows**.</span></span> 
  
<span data-ttu-id="e42cf-142">Não gere notificações para linhas de tabela ocultas da exibição por chamadas para **restringir**.</span><span class="sxs-lookup"><span data-stu-id="e42cf-142">Do not generate notifications for table rows that are hidden from view by calls to **Restrict**.</span></span> 
  
<span data-ttu-id="e42cf-143">Ao enviar notificações de tabela, a ordem das propriedades no membro de **linha** da estrutura [TABLE_NOTIFICATION](table_notification.md) e a ordem especificada pela chamada SetColumns \*\*\*\* mais recente deve ser a mesma da hora em que a solicitação de notificação foi enviada.</span><span class="sxs-lookup"><span data-stu-id="e42cf-143">When sending table notifications, the order of the properties in the **row** member of the [TABLE_NOTIFICATION](table_notification.md) structure and the order specified by the most recent **SetColumns** call must be the same as of the time that the notification request was sent.</span></span> 
  
<span data-ttu-id="e42cf-144">Outro sinalizador, TBL_BATCH, permite que os chamadores especifiquem que o implementador de tabelas pode adiar a avaliação dos resultados da operação até um momento posterior.</span><span class="sxs-lookup"><span data-stu-id="e42cf-144">Another flag, TBL_BATCH, allows callers to specify that the table implementer can defer evaluating the results of the operation until a later time.</span></span> <span data-ttu-id="e42cf-145">Sempre que possível, os chamadores devem definir esse sinalizador porque a operação em lote melhora o desempenho.</span><span class="sxs-lookup"><span data-stu-id="e42cf-145">Whenever possible, callers should set this flag because batched operation improves performance.</span></span>
  
<span data-ttu-id="e42cf-146">É sempre conveniente que os chamadores reservem algumas colunas no conjunto de linhas recuperadas para que os valores sejam adicionados posteriormente.</span><span class="sxs-lookup"><span data-stu-id="e42cf-146">It is often convenient for callers to reserve some columns in the retrieved row set for values to be added later.</span></span> <span data-ttu-id="e42cf-147">Os chamadores fazem isso colocando **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) nas posições desejadas na matriz de marca de propriedade \*\*\*\* passadas para SetColumns; a tabela passará de volta **PR_NULL** nessas posições em todas as linhas recuperadas com o **QueryRows**.</span><span class="sxs-lookup"><span data-stu-id="e42cf-147">Callers do this by placing **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) at the desired positions in the property tag array passed to **SetColumns**; the table will then pass back **PR_NULL** at those positions in all rows retrieved with **QueryRows**.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="e42cf-148">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="e42cf-148">Notes to callers</span></span>

<span data-ttu-id="e42cf-149">Ao criar a matriz de marca de propriedade para o parâmetro _lpPropTagArray_ , ordene as marcas na ordem em que você deseja que as colunas apareçam no modo de exibição de tabela.</span><span class="sxs-lookup"><span data-stu-id="e42cf-149">When building the property tag array for the  _lpPropTagArray_ parameter, order the tags in the order that you want the columns to appear in the table view.</span></span> 
  
<span data-ttu-id="e42cf-150">Você pode especificar as propriedades de vários valores a serem incluídas no conjunto de colunas aplicando o sinalizador de instância de vários valores, ou a constante MVI_FLAG, à marca da propriedade.</span><span class="sxs-lookup"><span data-stu-id="e42cf-150">You can specify multivalued properties to be included in the column set by applying the multivalued instance flag, or MVI_FLAG constant, to the property tag.</span></span> <span data-ttu-id="e42cf-151">Defina esse sinalizador passando a marca de propriedade para a versão de valor único da propriedade como um parâmetro para a macro MVI_PROP da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="e42cf-151">Set this flag by passing the property tag for the single-valued version of the property as a parameter to the MVI_PROP macro as follows:</span></span>
  
```
MVI_PROP(ulPropTag)

```

<span data-ttu-id="e42cf-152">A macro MVI_PROP definirá MVI_FLAG para a propriedade, transformando a marca em uma marca de vários valores.</span><span class="sxs-lookup"><span data-stu-id="e42cf-152">The MVI_PROP macro will set MVI_FLAG for the property, turning the tag into a multivalued tag.</span></span> <span data-ttu-id="e42cf-153">Se você tentar chamar o MVI_PROP em uma propriedade de valor único, o MAPI ignorará a chamada e deixará a marca da propriedade inalterada.</span><span class="sxs-lookup"><span data-stu-id="e42cf-153">If you erroneously try to call MVI_PROP on a single-valued property, MAPI will ignore the call and leave the property tag unchanged.</span></span> 
  
<span data-ttu-id="e42cf-154">Você pode incluir as marcas de propriedade definidas como **PR_NULL** na matriz de marca de propriedade para reservar espaço no conjunto de colunas.</span><span class="sxs-lookup"><span data-stu-id="e42cf-154">You can include property tags set to **PR_NULL** in the property tag array to reserve space in the column set.</span></span> <span data-ttu-id="e42cf-155">Reservar espaço permite que você adicione a um conjunto de colunas sem precisar alocar uma nova matriz de marca de propriedade.</span><span class="sxs-lookup"><span data-stu-id="e42cf-155">Reserving space allows you to add to a column set without having to allocate a new property tag array.</span></span> 
  
<span data-ttu-id="e42cf-156">Quando sua chamada para \*\*\*\* SetColumns causa uma alteração na ordem das colunas de uma tabela e uma ou mais dessas colunas representam uma propriedade com vários valores, é possível que o número de linhas na tabela aumentem.</span><span class="sxs-lookup"><span data-stu-id="e42cf-156">When your call to **SetColumns** causes a change to the order of a table's columns and one or more of these columns represent a multivalued property, it is possible for the number of rows in the table to increase.</span></span> <span data-ttu-id="e42cf-157">Se isso ocorrer, todos os indicadores para a tabela serão descartados.</span><span class="sxs-lookup"><span data-stu-id="e42cf-157">If this occurs, all of the bookmarks for the table are discarded.</span></span> <span data-ttu-id="e42cf-158">Para obter mais informações sobre como as colunas com vários valores afetam as tabelas, confira [trabalhar com colunas com vários valores](working-with-multivalued-columns.md).</span><span class="sxs-lookup"><span data-stu-id="e42cf-158">For more information about how multivalued columns affect tables, see [Working with Multivalued Columns](working-with-multivalued-columns.md).</span></span>
  
<span data-ttu-id="e42cf-159">A configuração das colunas é, por padrão, uma operação síncrona.</span><span class="sxs-lookup"><span data-stu-id="e42cf-159">Setting columns is by default a synchronous operation.</span></span> <span data-ttu-id="e42cf-160">No enTanto, você pode permitir que a tabela adie a operação até o momento em que os dados são necessários, definindo o sinalizador TBL_BATCH.</span><span class="sxs-lookup"><span data-stu-id="e42cf-160">However, you can allow the table to postpone the operation until such time as the data is needed by setting the TBL_BATCH flag.</span></span> <span data-ttu-id="e42cf-161">A definição desse sinalizador pode melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="e42cf-161">Setting this flag can improve performance.</span></span> <span data-ttu-id="e42cf-162">Outro sinalizador, TBL_ASYNC, torna a operação assíncrona, \*\*\*\* permitindo que SetColumns seja retornado antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="e42cf-162">Another flag, TBL_ASYNC, makes the operation asynchronous, allowing **SetColumns** to return before the operation is complete.</span></span> <span data-ttu-id="e42cf-163">Para determinar quando a conclusão ocorre, chame imApitable [:: GetStatus](imapitable-getstatus.md).</span><span class="sxs-lookup"><span data-stu-id="e42cf-163">To determine when completion occurs, call [IMAPITable::GetStatus](imapitable-getstatus.md).</span></span>
  
<span data-ttu-id="e42cf-164">Se uma chamada a \*\*\*\* SetColumns retornar MAPI_E_BUSY, indicando que outra operação está impedindo a inicialização da operação, você poderá chamar IMAPITable [:: Abort](imapitable-abort.md) para interromper a operação em andamento.</span><span class="sxs-lookup"><span data-stu-id="e42cf-164">If a call to **SetColumns** returns MAPI_E_BUSY, indicating that another operation is preventing your operation from starting, you can call [IMAPITable::Abort](imapitable-abort.md) to stop the operation in progress.</span></span> 
  
<span data-ttu-id="e42cf-165">Você também pode chamar [HrAddColumnsEx](hraddcolumnsex.md) para alterar um conjunto de colunas.</span><span class="sxs-lookup"><span data-stu-id="e42cf-165">You can also call [HrAddColumnsEx](hraddcolumnsex.md) to change a column set.</span></span> <span data-ttu-id="e42cf-166">A diferença entre **HrAddColumnsEx** e **IMAPITable::** SetColumns é que o **HrAddColumnsEx** é menos flexível; Só é possível adicionar colunas.</span><span class="sxs-lookup"><span data-stu-id="e42cf-166">The difference between **HrAddColumnsEx** and **IMAPITable::SetColumns** is that **HrAddColumnsEx** is less flexible; it can only add columns.</span></span> <span data-ttu-id="e42cf-167">As colunas adicionais são colocadas no início do conjunto de colunas; todas as colunas existentes aparecem seguindo estas colunas.</span><span class="sxs-lookup"><span data-stu-id="e42cf-167">The additional columns are placed at the beginning of the column set; all existing columns appear following these columns.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e42cf-168">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="e42cf-168">MFCMAPI reference</span></span>

<span data-ttu-id="e42cf-169">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e42cf-169">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e42cf-170">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="e42cf-170">**File**</span></span>|<span data-ttu-id="e42cf-171">**Função**</span><span class="sxs-lookup"><span data-stu-id="e42cf-171">**Function**</span></span>|<span data-ttu-id="e42cf-172">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="e42cf-172">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e42cf-173">ContentsTableListCtrl. cpp</span><span class="sxs-lookup"><span data-stu-id="e42cf-173">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="e42cf-174">CContentsTableListCtrl::D oSetColumns</span><span class="sxs-lookup"><span data-stu-id="e42cf-174">CContentsTableListCtrl::DoSetColumns</span></span>  <br/> |<span data-ttu-id="e42cf-175">MFCMAPI usa o método imApitable **::** SetColumns para definir as colunas desejadas para a tabela.</span><span class="sxs-lookup"><span data-stu-id="e42cf-175">MFCMAPI uses the **IMAPITable::SetColumns** method to set the desired columns for the table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e42cf-176">Confira também</span><span class="sxs-lookup"><span data-stu-id="e42cf-176">See also</span></span>



[<span data-ttu-id="e42cf-177">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="e42cf-177">HrQueryAllRows</span></span>](hrqueryallrows.md)
  
[<span data-ttu-id="e42cf-178">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="e42cf-178">IMAPITable::Abort</span></span>](imapitable-abort.md)
  
[<span data-ttu-id="e42cf-179">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="e42cf-179">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
  
[<span data-ttu-id="e42cf-180">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="e42cf-180">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="e42cf-181">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="e42cf-181">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="e42cf-182">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="e42cf-182">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="e42cf-183">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="e42cf-183">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="e42cf-184">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="e42cf-184">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="e42cf-185">SPropValue</span><span class="sxs-lookup"><span data-stu-id="e42cf-185">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="e42cf-186">SRowSet</span><span class="sxs-lookup"><span data-stu-id="e42cf-186">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="e42cf-187">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="e42cf-187">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="e42cf-188">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e42cf-188">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="e42cf-189">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="e42cf-189">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

