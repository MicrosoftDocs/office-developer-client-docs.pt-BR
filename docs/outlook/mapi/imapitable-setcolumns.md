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
ms.openlocfilehash: 9eeab1e1186aeb5a9b458facd59bd4cc155e8014
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767339"
---
# <a name="imapitablesetcolumns"></a><span data-ttu-id="b7c9f-103">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="b7c9f-103">IMAPITable::SetColumns</span></span>

  
  
<span data-ttu-id="b7c9f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b7c9f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b7c9f-105">Define as propriedades específicas e a ordem das propriedades aparecer como colunas na tabela.</span><span class="sxs-lookup"><span data-stu-id="b7c9f-105">Defines the particular properties and order of properties to appear as columns in the table.</span></span>
  
```cpp
HRESULT SetColumns(
LPSPropTagArray lpPropTagArray,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="b7c9f-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="b7c9f-106">Parameters</span></span>

 <span data-ttu-id="b7c9f-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="b7c9f-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="b7c9f-108">[in] Ponteiro para uma matriz de marcas de propriedade identificando propriedades a serem incluídos como colunas na tabela.</span><span class="sxs-lookup"><span data-stu-id="b7c9f-108">[in] Pointer to an array of property tags identifying properties to be included as columns in the table.</span></span> <span data-ttu-id="b7c9f-109">A parte de tipo de propriedade de cada marca pode ser definida para um tipo válido ou **PR_NULL** para reservar espaço para adições subsequentes.</span><span class="sxs-lookup"><span data-stu-id="b7c9f-109">The property type portion of each tag can be set to a valid type or to **PR_NULL** to reserve space for subsequent additions.</span></span> <span data-ttu-id="b7c9f-110">O parâmetro _lpPropTagArray_ não pode ser definido como NULL; cada tabela deve ter pelo menos uma coluna.</span><span class="sxs-lookup"><span data-stu-id="b7c9f-110">The  _lpPropTagArray_ parameter cannot be set to NULL; every table must have at least one column.</span></span> 
    
 <span data-ttu-id="b7c9f-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b7c9f-111">_ulFlags_</span></span>
  
> <span data-ttu-id="b7c9f-112">[in] Bitmask dos sinalizadores que controla o retorno de uma chamada assíncrona para **SetColumns**, por exemplo, quando **SetColumns** é usado na notificação.</span><span class="sxs-lookup"><span data-stu-id="b7c9f-112">[in] Bitmask of flags that controls the return of an asynchronous call to **SetColumns**, for example when **SetColumns** is used in notification.</span></span> <span data-ttu-id="b7c9f-113">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="b7c9f-113">The following flags can be set:</span></span> 
    
<span data-ttu-id="b7c9f-114">TBL_ASYNC</span><span class="sxs-lookup"><span data-stu-id="b7c9f-114">TBL_ASYNC</span></span> 
  
> <span data-ttu-id="b7c9f-115">Solicitações que a operação de configuração de coluna ser executada assincronamente causando **SetColumns** retornar potencialmente antes que a operação foi totalmente concluída.</span><span class="sxs-lookup"><span data-stu-id="b7c9f-115">Requests that the column setting operation be performed asynchronously causing **SetColumns** to potentially return before the operation has fully completed.</span></span> 
    
<span data-ttu-id="b7c9f-116">TBL_BATCH</span><span class="sxs-lookup"><span data-stu-id="b7c9f-116">TBL_BATCH</span></span> 
  
> <span data-ttu-id="b7c9f-117">Permite que a tabela para adiar a operação de configuração de coluna até que os dados são realmente necessários.</span><span class="sxs-lookup"><span data-stu-id="b7c9f-117">Permits the table to postpone the column setting operation until the data is actually required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b7c9f-118">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="b7c9f-118">Return value</span></span>

<span data-ttu-id="b7c9f-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="b7c9f-119">S_OK</span></span> 
  
> <span data-ttu-id="b7c9f-120">A operação de configuração de coluna foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="b7c9f-120">The column setting operation was successful.</span></span>
    
<span data-ttu-id="b7c9f-121">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="b7c9f-121">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="b7c9f-122">Outra operação está em andamento que impede que a coluna a definição de início da operação.</span><span class="sxs-lookup"><span data-stu-id="b7c9f-122">Another operation is in progress that prevents the column setting operation from starting.</span></span> <span data-ttu-id="b7c9f-123">Ou a operação em andamento deve ter permissão para concluir ou ele deve ser interrompido.</span><span class="sxs-lookup"><span data-stu-id="b7c9f-123">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b7c9f-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="b7c9f-124">Remarks</span></span>

<span data-ttu-id="b7c9f-125">O conjunto de colunas de uma tabela é o grupo de propriedades que compõem as colunas para as linhas da tabela.</span><span class="sxs-lookup"><span data-stu-id="b7c9f-125">The column set of a table is the group of properties that make up the columns for the rows in the table.</span></span> <span data-ttu-id="b7c9f-126">Não há uma coluna padrão definido para cada tipo de tabela.</span><span class="sxs-lookup"><span data-stu-id="b7c9f-126">There is a default column set for each type of table.</span></span> <span data-ttu-id="b7c9f-127">O conjunto de colunas padrão é formado pelas propriedades que o implementador tabela inclui automaticamente.</span><span class="sxs-lookup"><span data-stu-id="b7c9f-127">The default column set is made up of the properties that the table implementer automatically includes.</span></span> <span data-ttu-id="b7c9f-128">Os usuários da tabela podem alterar esse padrão definido chamando o método **IMAPITable::SetColumns** .</span><span class="sxs-lookup"><span data-stu-id="b7c9f-128">Table users can alter this default set by calling the **IMAPITable::SetColumns** method.</span></span> <span data-ttu-id="b7c9f-129">Eles podem solicitar que outras colunas seja adicionado ao padrão definido se o implementador tabela oferece suporte a eles que colunas seja removido ou que a ordem das colunas seja alterado.</span><span class="sxs-lookup"><span data-stu-id="b7c9f-129">They can request that other columns be added to the default set if the table implementer supports them that columns be removed, or that the order of columns be changed.</span></span> <span data-ttu-id="b7c9f-130">**SetColumns** Especifica as colunas que são retornadas com cada linha e a ordem dessas colunas dentro da linha.</span><span class="sxs-lookup"><span data-stu-id="b7c9f-130">**SetColumns** specifies the columns that are returned with each row and the order of these columns within the row.</span></span> 
  
<span data-ttu-id="b7c9f-131">O êxito da operação **SetColumns** seja aparente somente depois que uma chamada subsequente foi feita para recuperar os dados da tabela.</span><span class="sxs-lookup"><span data-stu-id="b7c9f-131">The success of the **SetColumns** operation is apparent only after a subsequent call has been made to retrieve the data of the table.</span></span> <span data-ttu-id="b7c9f-132">Em seguida, é que quaisquer erros informados.</span><span class="sxs-lookup"><span data-stu-id="b7c9f-132">It is then that any errors are reported.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="b7c9f-133">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="b7c9f-133">Notes to implementers</span></span>

<span data-ttu-id="b7c9f-134">Alguns provedores de permitir que uma chamada **SetColumns** somente as colunas de tabela que fazem parte das colunas disponíveis para um modo de exibição de tabela de pedidos.</span><span class="sxs-lookup"><span data-stu-id="b7c9f-134">Some providers allow a **SetColumns** call to order only table columns that are part of the available columns for a table view.</span></span> <span data-ttu-id="b7c9f-135">Outros provedores de permitir que uma chamada **SetColumns** solicitar todas as colunas de tabela, inclusive aquelas que contém as propriedades não no conjunto de coluna original.</span><span class="sxs-lookup"><span data-stu-id="b7c9f-135">Other providers allow a **SetColumns** call to order all table columns, including those containing properties not in the original column set.</span></span> 
  
<span data-ttu-id="b7c9f-136">Quando TBL_BATCH é definida para operações assíncronas, provedores devem retornar um tipo de propriedade de PT_ERROR e um valor de propriedade de valor nulo para as colunas que não são suportados.</span><span class="sxs-lookup"><span data-stu-id="b7c9f-136">When TBL_BATCH is set for asynchronous operations, providers should return a property type of PT_ERROR and a property value of NULL for columns that are not supported.</span></span>
  
<span data-ttu-id="b7c9f-137">Você não precisará responder ao sinalizador TBL_ASYNC solicitando que a operação ser assíncrona.</span><span class="sxs-lookup"><span data-stu-id="b7c9f-137">You do not need to respond to the TBL_ASYNC flag requesting that the operation be asynchronous.</span></span> <span data-ttu-id="b7c9f-138">Se você não têm suporte para a definição do conjunto de coluna assíncrona, execute a operação de maneira síncrona.</span><span class="sxs-lookup"><span data-stu-id="b7c9f-138">If you do not support asynchronous column set definition, perform the operation synchronously.</span></span> <span data-ttu-id="b7c9f-139">Se você pode suportar o sinalizador TBL_ASYNC e outro assíncrono operação ainda está em andamento, MAPI_E_BUSY retorno.</span><span class="sxs-lookup"><span data-stu-id="b7c9f-139">If you can support the TBL_ASYNC flag and another asynchronous operation is still in progress, return MAPI_E_BUSY.</span></span> <span data-ttu-id="b7c9f-140">Caso contrário, Retorna S_OK independentemente de estarem ou não suportam todas as propriedades incluídas na matriz de marca de propriedade.</span><span class="sxs-lookup"><span data-stu-id="b7c9f-140">Otherwise, return S_OK regardless of whether or not you support all of the properties included in the property tag array.</span></span> <span data-ttu-id="b7c9f-141">Erros resultantes das propriedades sem suporte devem ser retornados da **IMAPITable** métodos que recuperar dados, como **QueryRows**.</span><span class="sxs-lookup"><span data-stu-id="b7c9f-141">Errors resulting from unsupported properties should be returned from **IMAPITable** methods that retrieve data, such as **QueryRows**.</span></span> 
  
<span data-ttu-id="b7c9f-142">Não gere notificações de linhas da tabela que estão ocultas do modo por chamadas para **Restrict**.</span><span class="sxs-lookup"><span data-stu-id="b7c9f-142">Do not generate notifications for table rows that are hidden from view by calls to **Restrict**.</span></span> 
  
<span data-ttu-id="b7c9f-143">Quando envio de notificações de tabela, a ordem das propriedades no membro da **linha** da estrutura [TABLE_NOTIFICATION](table_notification.md) e a ordem especificada pela chamada mais recente do **SetColumns** deve ser iguais desde o momento em que a solicitação de notificação foi enviada.</span><span class="sxs-lookup"><span data-stu-id="b7c9f-143">When sending table notifications, the order of the properties in the **row** member of the [TABLE_NOTIFICATION](table_notification.md) structure and the order specified by the most recent **SetColumns** call must be the same as of the time that the notification request was sent.</span></span> 
  
<span data-ttu-id="b7c9f-144">Sinalizador de outro, TBL_BATCH, permite que os chamadores especificar que o implementador tabela pode adiar avaliando os resultados da operação até um momento posterior.</span><span class="sxs-lookup"><span data-stu-id="b7c9f-144">Another flag, TBL_BATCH, allows callers to specify that the table implementer can defer evaluating the results of the operation until a later time.</span></span> <span data-ttu-id="b7c9f-145">Sempre que possível, os chamadores devem definir este sinalizador como operação em lote melhora o desempenho.</span><span class="sxs-lookup"><span data-stu-id="b7c9f-145">Whenever possible, callers should set this flag because batched operation improves performance.</span></span>
  
<span data-ttu-id="b7c9f-146">Costuma ser conveniente para os chamadores reservar algumas colunas do conjunto de linha recuperados para valores sejam adicionados posteriormente.</span><span class="sxs-lookup"><span data-stu-id="b7c9f-146">It is often convenient for callers to reserve some columns in the retrieved row set for values to be added later.</span></span> <span data-ttu-id="b7c9f-147">Os chamadores fazer isso, colocando **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) nas posições desejadas na propriedade tag matriz passadas **SetColumns**; a tabela será então secreta volta **PR_NULL** nesses cargos em todas as linhas recuperadas com **QueryRows**.</span><span class="sxs-lookup"><span data-stu-id="b7c9f-147">Callers do this by placing **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) at the desired positions in the property tag array passed to **SetColumns**; the table will then pass back **PR_NULL** at those positions in all rows retrieved with **QueryRows**.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="b7c9f-148">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="b7c9f-148">Notes to callers</span></span>

<span data-ttu-id="b7c9f-149">Ao construir a matriz de marca de propriedade para o parâmetro _lpPropTagArray_ , ordem as marcas na ordem em que você deseja que as colunas apareçam na exibição da tabela.</span><span class="sxs-lookup"><span data-stu-id="b7c9f-149">When building the property tag array for the  _lpPropTagArray_ parameter, order the tags in the order that you want the columns to appear in the table view.</span></span> 
  
<span data-ttu-id="b7c9f-150">Você pode especificar vários valores de propriedades a serem incluídos na coluna definir aplicando o sinalizador multivalorado instância ou a constante MVI_FLAG, como a marca de propriedade.</span><span class="sxs-lookup"><span data-stu-id="b7c9f-150">You can specify multivalued properties to be included in the column set by applying the multivalued instance flag, or MVI_FLAG constant, to the property tag.</span></span> <span data-ttu-id="b7c9f-151">Defina esse sinalizador, passando a marca de propriedade para a versão de valor único da propriedade como um parâmetro para a macro MVI_PROP da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="b7c9f-151">Set this flag by passing the property tag for the single-valued version of the property as a parameter to the MVI_PROP macro as follows:</span></span>
  
```
MVI_PROP(ulPropTag)

```

<span data-ttu-id="b7c9f-152">A macro MVI_PROP definirão MVI_FLAG para a propriedade, transformando a marca em uma marca de valores múltiplos.</span><span class="sxs-lookup"><span data-stu-id="b7c9f-152">The MVI_PROP macro will set MVI_FLAG for the property, turning the tag into a multivalued tag.</span></span> <span data-ttu-id="b7c9f-153">Se você tentar chamar MVI_PROP em uma propriedade de valor único erroneamente, MAPI irá ignorar a chamada e deixe a marca de propriedade inalterada.</span><span class="sxs-lookup"><span data-stu-id="b7c9f-153">If you erroneously try to call MVI_PROP on a single-valued property, MAPI will ignore the call and leave the property tag unchanged.</span></span> 
  
<span data-ttu-id="b7c9f-154">Você pode incluir marcas de propriedade definidas como **PR_NULL** na matriz de marca de propriedade para reservar espaço no conjunto de colunas.</span><span class="sxs-lookup"><span data-stu-id="b7c9f-154">You can include property tags set to **PR_NULL** in the property tag array to reserve space in the column set.</span></span> <span data-ttu-id="b7c9f-155">Reservar espaço permite que você adicione a uma coluna definida sem precisar alocar uma nova matriz de marca de propriedade.</span><span class="sxs-lookup"><span data-stu-id="b7c9f-155">Reserving space allows you to add to a column set without having to allocate a new property tag array.</span></span> 
  
<span data-ttu-id="b7c9f-156">Quando a chamada para **SetColumns** faz com que uma alteração à ordem de colunas de uma tabela e um ou mais dessas colunas representam uma propriedade de vários valores, é possível para o número de linhas da tabela para aumentar.</span><span class="sxs-lookup"><span data-stu-id="b7c9f-156">When your call to **SetColumns** causes a change to the order of a table's columns and one or more of these columns represent a multivalued property, it is possible for the number of rows in the table to increase.</span></span> <span data-ttu-id="b7c9f-157">Caso isso aconteça, todos os indicadores da tabela são descartados.</span><span class="sxs-lookup"><span data-stu-id="b7c9f-157">If this occurs, all of the bookmarks for the table are discarded.</span></span> <span data-ttu-id="b7c9f-158">Para obter mais informações sobre como colunas de valores múltiplos afetam as tabelas, consulte [Trabalhando com vários valores de colunas](working-with-multivalued-columns.md).</span><span class="sxs-lookup"><span data-stu-id="b7c9f-158">For more information about how multivalued columns affect tables, see [Working with Multivalued Columns](working-with-multivalued-columns.md).</span></span>
  
<span data-ttu-id="b7c9f-159">Definir colunas é por padrão uma operação síncrona.</span><span class="sxs-lookup"><span data-stu-id="b7c9f-159">Setting columns is by default a synchronous operation.</span></span> <span data-ttu-id="b7c9f-160">No entanto, você pode permitir que a tabela adiar a operação até que os dados forem necessários, definindo o sinalizador TBL_BATCH.</span><span class="sxs-lookup"><span data-stu-id="b7c9f-160">However, you can allow the table to postpone the operation until such time as the data is needed by setting the TBL_BATCH flag.</span></span> <span data-ttu-id="b7c9f-161">Defina esse sinalizador pode melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="b7c9f-161">Setting this flag can improve performance.</span></span> <span data-ttu-id="b7c9f-162">Sinalizador de outro, TBL_ASYNC, faz com que a operação assíncrona, permitindo que **SetColumns** retornar antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="b7c9f-162">Another flag, TBL_ASYNC, makes the operation asynchronous, allowing **SetColumns** to return before the operation is complete.</span></span> <span data-ttu-id="b7c9f-163">Para determinar quando ocorre de conclusão, chame [IMAPITable::GetStatus](imapitable-getstatus.md).</span><span class="sxs-lookup"><span data-stu-id="b7c9f-163">To determine when completion occurs, call [IMAPITable::GetStatus](imapitable-getstatus.md).</span></span>
  
<span data-ttu-id="b7c9f-164">Se uma chamada para **SetColumns** retornará MAPI_E_BUSY, indicando que a outra operação está impedindo a operação seja iniciado, é possível chamar [IMAPITable::Abort](imapitable-abort.md) para interromper a operação em andamento.</span><span class="sxs-lookup"><span data-stu-id="b7c9f-164">If a call to **SetColumns** returns MAPI_E_BUSY, indicating that another operation is preventing your operation from starting, you can call [IMAPITable::Abort](imapitable-abort.md) to stop the operation in progress.</span></span> 
  
<span data-ttu-id="b7c9f-165">Você também pode chamar [HrAddColumnsEx](hraddcolumnsex.md) para alterar um conjunto de colunas.</span><span class="sxs-lookup"><span data-stu-id="b7c9f-165">You can also call [HrAddColumnsEx](hraddcolumnsex.md) to change a column set.</span></span> <span data-ttu-id="b7c9f-166">A diferença entre **HrAddColumnsEx** e **IMAPITable::SetColumns** é que **HrAddColumnsEx** menos flexíveis; ele só poderá adicionar colunas.</span><span class="sxs-lookup"><span data-stu-id="b7c9f-166">The difference between **HrAddColumnsEx** and **IMAPITable::SetColumns** is that **HrAddColumnsEx** is less flexible; it can only add columns.</span></span> <span data-ttu-id="b7c9f-167">As colunas adicionais são colocadas no início do conjunto de colunas; todas as colunas existentes aparecem seguindo essas colunas.</span><span class="sxs-lookup"><span data-stu-id="b7c9f-167">The additional columns are placed at the beginning of the column set; all existing columns appear following these columns.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b7c9f-168">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="b7c9f-168">MFCMAPI reference</span></span>

<span data-ttu-id="b7c9f-169">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b7c9f-169">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b7c9f-170">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="b7c9f-170">**File**</span></span>|<span data-ttu-id="b7c9f-171">**Function**</span><span class="sxs-lookup"><span data-stu-id="b7c9f-171">**Function**</span></span>|<span data-ttu-id="b7c9f-172">**Comment**</span><span class="sxs-lookup"><span data-stu-id="b7c9f-172">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b7c9f-173">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="b7c9f-173">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="b7c9f-174">CContentsTableListCtrl::DoSetColumns</span><span class="sxs-lookup"><span data-stu-id="b7c9f-174">CContentsTableListCtrl::DoSetColumns</span></span>  <br/> |<span data-ttu-id="b7c9f-175">MFCMAPI usa o método **IMAPITable::SetColumns** para definir as colunas desejadas para a tabela.</span><span class="sxs-lookup"><span data-stu-id="b7c9f-175">MFCMAPI uses the **IMAPITable::SetColumns** method to set the desired columns for the table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b7c9f-176">Confira também</span><span class="sxs-lookup"><span data-stu-id="b7c9f-176">See also</span></span>



[<span data-ttu-id="b7c9f-177">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="b7c9f-177">HrQueryAllRows</span></span>](hrqueryallrows.md)
  
[<span data-ttu-id="b7c9f-178">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="b7c9f-178">IMAPITable::Abort</span></span>](imapitable-abort.md)
  
[<span data-ttu-id="b7c9f-179">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="b7c9f-179">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
  
[<span data-ttu-id="b7c9f-180">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="b7c9f-180">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="b7c9f-181">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="b7c9f-181">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="b7c9f-182">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="b7c9f-182">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="b7c9f-183">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="b7c9f-183">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="b7c9f-184">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="b7c9f-184">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="b7c9f-185">SPropValue</span><span class="sxs-lookup"><span data-stu-id="b7c9f-185">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="b7c9f-186">SRowSet</span><span class="sxs-lookup"><span data-stu-id="b7c9f-186">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="b7c9f-187">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="b7c9f-187">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="b7c9f-188">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b7c9f-188">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="b7c9f-189">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="b7c9f-189">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

