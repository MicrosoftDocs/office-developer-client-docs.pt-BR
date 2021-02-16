---
title: IMAPITableRestrict
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.Restrict
api_type:
- COM
ms.assetid: a5bfc190-b58f-44c3-893c-8727df14ee58
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6cca6bc12fa6f100885b7bf705d79fa24a2e2f91
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414617"
---
# <a name="imapitablerestrict"></a><span data-ttu-id="79034-103">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="79034-103">IMAPITable::Restrict</span></span>

  
  
<span data-ttu-id="79034-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="79034-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="79034-105">Aplica um filtro a uma tabela, reduzindo o conjunto de linhas apenas para as linhas que corresponderem aos critérios especificados.</span><span class="sxs-lookup"><span data-stu-id="79034-105">Applies a filter to a table, reducing the row set to only those rows matching the specified criteria.</span></span>
  
```cpp
HRESULT Restrict(
LPSRestriction lpRestriction,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="79034-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="79034-106">Parameters</span></span>

 <span data-ttu-id="79034-107">_lpRestriction_</span><span class="sxs-lookup"><span data-stu-id="79034-107">_lpRestriction_</span></span>
  
> <span data-ttu-id="79034-108">[in] Ponteiro para uma [estrutura SRestriction](srestriction.md) definindo as condições do filtro.</span><span class="sxs-lookup"><span data-stu-id="79034-108">[in] Pointer to an [SRestriction](srestriction.md) structure defining the conditions of the filter.</span></span> <span data-ttu-id="79034-109">Passar NULL no  _parâmetro lpRestriction_ remove o filtro atual.</span><span class="sxs-lookup"><span data-stu-id="79034-109">Passing NULL in the  _lpRestriction_ parameter removes the current filter.</span></span> 
    
 <span data-ttu-id="79034-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="79034-110">_ulFlags_</span></span>
  
> <span data-ttu-id="79034-111">[in] Máscara de bits de sinalizadores que controla o tempo da operação de restrição.</span><span class="sxs-lookup"><span data-stu-id="79034-111">[in] Bitmask of flags that controls the timing of the restriction operation.</span></span> <span data-ttu-id="79034-112">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="79034-112">The following flags can be set:</span></span>
    
<span data-ttu-id="79034-113">TBL_ASYNC</span><span class="sxs-lookup"><span data-stu-id="79034-113">TBL_ASYNC</span></span> 
  
> <span data-ttu-id="79034-114">Inicia a operação de forma assíncrona e retorna antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="79034-114">Starts the operation asynchronously and returns before the operation completes.</span></span>
    
<span data-ttu-id="79034-115">TBL_BATCH</span><span class="sxs-lookup"><span data-stu-id="79034-115">TBL_BATCH</span></span> 
  
> <span data-ttu-id="79034-116">Adia a avaliação do filtro até que os dados na tabela são necessários.</span><span class="sxs-lookup"><span data-stu-id="79034-116">Defers evaluation of the filter until the data in the table is required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="79034-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="79034-117">Return value</span></span>

<span data-ttu-id="79034-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="79034-118">S_OK</span></span> 
  
> <span data-ttu-id="79034-119">O filtro foi aplicado com êxito.</span><span class="sxs-lookup"><span data-stu-id="79034-119">The filter was successfully applied.</span></span>
    
<span data-ttu-id="79034-120">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="79034-120">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="79034-121">Outra operação está em andamento que impede o início da operação de restrição.</span><span class="sxs-lookup"><span data-stu-id="79034-121">Another operation is in progress that prevents the restriction operation from starting.</span></span> <span data-ttu-id="79034-122">A operação em andamento deve ter permissão para ser concluída ou deve ser interrompida.</span><span class="sxs-lookup"><span data-stu-id="79034-122">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="79034-123">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="79034-123">MAPI_E_TOO_COMPLEX</span></span> 
  
> <span data-ttu-id="79034-124">A tabela não pode executar a operação porque o filtro específico apontado pelo parâmetro  _lpRestriction_ é muito complicado.</span><span class="sxs-lookup"><span data-stu-id="79034-124">The table cannot perform the operation because the particular filter pointed to by the  _lpRestriction_ parameter is too complicated.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="79034-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="79034-125">Remarks</span></span>

<span data-ttu-id="79034-126">O **método IMAPITable::Restrict** estabelece uma restrição ou filtro em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="79034-126">The **IMAPITable::Restrict** method establishes a restriction, or filter, on a table.</span></span> <span data-ttu-id="79034-127">Se houver uma restrição anterior, ela será descartada e a nova será aplicada.</span><span class="sxs-lookup"><span data-stu-id="79034-127">If there is a previous restriction, it is discarded and the new one applied.</span></span> <span data-ttu-id="79034-128">A aplicação de uma restrição não afeta os dados subjacentes de uma tabela; ele simplesmente altera o ponto de vista limitando as linhas que podem ser recuperadas a linhas que contêm dados que satisfazem a restrição.</span><span class="sxs-lookup"><span data-stu-id="79034-128">Applying a restriction has no affect on the underlying data of a table; it simply alters the view by limiting the rows that can be retrieved to rows containing data that satisfy the restriction.</span></span> 
  
<span data-ttu-id="79034-129">Há vários tipos diferentes de restrições, cada um descrito com uma estrutura diferente.</span><span class="sxs-lookup"><span data-stu-id="79034-129">There are several different types of restrictions, each described with a different structure.</span></span> <span data-ttu-id="79034-130">A [estrutura SRestriction](srestriction.md) contém dois membros: um valor que indica o tipo de restrição e a estrutura específica aplicável para esse tipo.</span><span class="sxs-lookup"><span data-stu-id="79034-130">The [SRestriction](srestriction.md) structure contains two members: a value that indicates the type of restriction and the specific structure applicable for that type.</span></span> 
  
<span data-ttu-id="79034-131">As notificações para linhas de tabela que estão ocultas da exibição por chamadas para **Restringir nunca** são geradas.</span><span class="sxs-lookup"><span data-stu-id="79034-131">Notifications for table rows that are hidden from view by calls to **Restrict** are never generated.</span></span> 
  
<span data-ttu-id="79034-132">Uma restrição de propriedade em uma propriedade de múltiplos valores funciona como uma restrição em uma propriedade de valor único.</span><span class="sxs-lookup"><span data-stu-id="79034-132">A property restriction on a multivalued property works like a restriction on a single-valued property.</span></span> <span data-ttu-id="79034-133">Uma propriedade de múltiplos valores a ser usada em uma restrição de propriedade deve ter o sinalizador MVI_FLAG definido.</span><span class="sxs-lookup"><span data-stu-id="79034-133">A multivalued property to be used in a property restriction must have the MVI_FLAG flag set.</span></span> <span data-ttu-id="79034-134">Se ele não tiver esse sinalizador definido, ele será tratado como uma tupla totalmente ordenada.</span><span class="sxs-lookup"><span data-stu-id="79034-134">If it doesn't have this flag set, it is treated as a totally ordered tuple.</span></span> <span data-ttu-id="79034-135">Uma comparação de duas colunas de múltiplos valores compara os elementos de coluna na ordem, relatando a relação das colunas na primeira responsabilidade.</span><span class="sxs-lookup"><span data-stu-id="79034-135">A comparison of two multivalued columns compares the column elements in order, reporting the relation of the columns at the first inequality.</span></span> <span data-ttu-id="79034-136">A igualdade será retornada somente se as colunas comparadas contêm os mesmos valores na mesma ordem.</span><span class="sxs-lookup"><span data-stu-id="79034-136">Equality is returned only if the columns compared contain the same values in the same order.</span></span> <span data-ttu-id="79034-137">Se uma coluna tiver menos valores do que a outra, a relação relatada será aquela de um valor nulo para o outro valor.</span><span class="sxs-lookup"><span data-stu-id="79034-137">If one column has fewer values than the other, the reported relation is that of a null value to the other value.</span></span>
  
<span data-ttu-id="79034-138">Para obter mais informações sobre restrições, consulte [Sobre restrições.](about-restrictions.md)</span><span class="sxs-lookup"><span data-stu-id="79034-138">For more information about restrictions, see [About Restrictions](about-restrictions.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="79034-139">Se você criar consultas dinâmicas para pesquisar dados no servidor, use o método **FindRow** em vez de usar o método **Restrict** e **o método QueryRows** juntos.</span><span class="sxs-lookup"><span data-stu-id="79034-139">If you create dynamic queries to search for data on the server, use the **FindRow** method instead of using the **Restrict** method and the **QueryRows** method together.</span></span> <span data-ttu-id="79034-140">O **método Restrict** cria um modo de exibição em cache que é usado para avaliar todas as mensagens adicionadas ou modificadas na pasta base.</span><span class="sxs-lookup"><span data-stu-id="79034-140">The **Restrict** method creates a cached view that is used to evaluate all messages added to or modified in the base folder.</span></span> <span data-ttu-id="79034-141">Se um aplicativo cliente usar **o método Restrict** para cada consulta dinâmica, um modo de exibição em cache será criado para cada consulta.</span><span class="sxs-lookup"><span data-stu-id="79034-141">If a client application uses the **Restrict** method for each dynamic query, a cached view will be created for each query.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="79034-142">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="79034-142">Notes to callers</span></span>

<span data-ttu-id="79034-143">Para descartar a restrição atual sem criar uma nova, passe NULL em  _lpRestriction_.</span><span class="sxs-lookup"><span data-stu-id="79034-143">To discard the current restriction without creating a new one, pass NULL in  _lpRestriction_.</span></span>
  
<span data-ttu-id="79034-144">Se outra chamada de tabela assíncrona estiver em andamento, fazendo com que **Restrict** retorne MAPI_E_BUSY, você poderá chamar [IMAPITable::Abort](imapitable-abort.md) para interromper a chamada.</span><span class="sxs-lookup"><span data-stu-id="79034-144">If another asynchronous table call is in progress, causing **Restrict** to return MAPI_E_BUSY, you can call [IMAPITable::Abort](imapitable-abort.md) to stop the call.</span></span> 
  
 <span data-ttu-id="79034-145">**Restringir** opera de forma síncrona, a menos que você de definir um dos sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="79034-145">**Restrict** operates synchronously unless you set one of the flags.</span></span> <span data-ttu-id="79034-146">Se você definir o sinalizador TBL_BATCH, **Restringir** adia a avaliação da restrição, a menos que solicite os dados.</span><span class="sxs-lookup"><span data-stu-id="79034-146">If you set the TBL_BATCH flag, **Restrict** postpones the evaluation of the restriction unless you request the data.</span></span> <span data-ttu-id="79034-147">Se o TBL_ASYNC sinalizador estiver definido, **Restringir** funcionará de forma assíncrona, potencialmente retornando antes da conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="79034-147">If the TBL_ASYNC flag is set, **Restrict** operates asynchronously, potentially returning before the completion of the operation.</span></span>
  
<span data-ttu-id="79034-148">Todos os indicadores de uma tabela são descartados quando uma chamada a **Restrict** é feita e BOOKMARK_CURRENT, a posição atual do cursor, é definida como o início da tabela.</span><span class="sxs-lookup"><span data-stu-id="79034-148">All bookmarks for a table are discarded when a call to **Restrict** is made, and BOOKMARK_CURRENT, the current cursor position, is set to the beginning of the table.</span></span> 
  
<span data-ttu-id="79034-149">Se você tentar impor uma restrição de propriedade em uma propriedade que não está no conjunto de colunas da tabela, os resultados serão indefinido.</span><span class="sxs-lookup"><span data-stu-id="79034-149">If you attempt to impose a property restriction on a property that is not in the table's column set, the results are undefined.</span></span> <span data-ttu-id="79034-150">Sempre que você não tiver certeza se uma propriedade é suportada em uma tabela, combine a restrição de propriedade com uma restrição existe.</span><span class="sxs-lookup"><span data-stu-id="79034-150">Whenever you are unsure as to whether a property is supported in a table, combine the property restriction with an exists restriction.</span></span> <span data-ttu-id="79034-151">A restrição existe verifica a existência da propriedade antes de tentar impor a restrição de propriedade.</span><span class="sxs-lookup"><span data-stu-id="79034-151">The exists restriction checks for the existence of the property before attempting to impose the property restriction.</span></span> 
  
<span data-ttu-id="79034-152">Não espere receber uma notificação de tabela em uma linha que tenha sido filtrada de uma tabela devido a uma restrição.</span><span class="sxs-lookup"><span data-stu-id="79034-152">Do not expect to receive a table notification on a row that has been filtered from a table due to a restriction.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="79034-153">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="79034-153">MFCMAPI reference</span></span>

<span data-ttu-id="79034-154">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="79034-154">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="79034-155">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="79034-155">**File**</span></span>|<span data-ttu-id="79034-156">**Função**</span><span class="sxs-lookup"><span data-stu-id="79034-156">**Function**</span></span>|<span data-ttu-id="79034-157">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="79034-157">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="79034-158">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="79034-158">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="79034-159">CContentsTableListCtrl::ApplyRestriction</span><span class="sxs-lookup"><span data-stu-id="79034-159">CContentsTableListCtrl::ApplyRestriction</span></span>  <br/> |<span data-ttu-id="79034-160">MFCMAPI usa o **método IMAPITable::Restrict** para definir uma restrição em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="79034-160">MFCMAPI uses the **IMAPITable::Restrict** method to set a restriction on a table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="79034-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="79034-161">See also</span></span>



[<span data-ttu-id="79034-162">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="79034-162">IMAPITable::Abort</span></span>](imapitable-abort.md)
  
[<span data-ttu-id="79034-163">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="79034-163">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
  
[<span data-ttu-id="79034-164">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="79034-164">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
  
[<span data-ttu-id="79034-165">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="79034-165">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="79034-166">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="79034-166">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="79034-167">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="79034-167">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="79034-168">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="79034-168">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

