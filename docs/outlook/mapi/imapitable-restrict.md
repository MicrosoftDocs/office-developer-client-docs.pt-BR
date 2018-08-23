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
ms.openlocfilehash: 924715f26e104739f2e60762511221da5facd5a5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578322"
---
# <a name="imapitablerestrict"></a><span data-ttu-id="b5f52-103">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="b5f52-103">IMAPITable::Restrict</span></span>

  
  
<span data-ttu-id="b5f52-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b5f52-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b5f52-105">Aplica um filtro a uma tabela, reduzindo a linha definida como apenas as linhas que correspondem aos critérios especificados.</span><span class="sxs-lookup"><span data-stu-id="b5f52-105">Applies a filter to a table, reducing the row set to only those rows matching the specified criteria.</span></span>
  
```cpp
HRESULT Restrict(
LPSRestriction lpRestriction,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="b5f52-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b5f52-106">Parameters</span></span>

 <span data-ttu-id="b5f52-107">_lpRestriction_</span><span class="sxs-lookup"><span data-stu-id="b5f52-107">_lpRestriction_</span></span>
  
> <span data-ttu-id="b5f52-108">[in] Ponteiro para uma estrutura de [SRestriction](srestriction.md) definindo as condições do filtro.</span><span class="sxs-lookup"><span data-stu-id="b5f52-108">[in] Pointer to an [SRestriction](srestriction.md) structure defining the conditions of the filter.</span></span> <span data-ttu-id="b5f52-109">Passar NULL no parâmetro _lpRestriction_ remove o filtro atual.</span><span class="sxs-lookup"><span data-stu-id="b5f52-109">Passing NULL in the  _lpRestriction_ parameter removes the current filter.</span></span> 
    
 <span data-ttu-id="b5f52-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b5f52-110">_ulFlags_</span></span>
  
> <span data-ttu-id="b5f52-111">[in] Bitmask dos sinalizadores que controla o tempo da operação de restrição.</span><span class="sxs-lookup"><span data-stu-id="b5f52-111">[in] Bitmask of flags that controls the timing of the restriction operation.</span></span> <span data-ttu-id="b5f52-112">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="b5f52-112">The following flags can be set:</span></span>
    
<span data-ttu-id="b5f52-113">TBL_ASYNC</span><span class="sxs-lookup"><span data-stu-id="b5f52-113">TBL_ASYNC</span></span> 
  
> <span data-ttu-id="b5f52-114">Inicia a operação assíncrona e retorna antes que a operação for concluída.</span><span class="sxs-lookup"><span data-stu-id="b5f52-114">Starts the operation asynchronously and returns before the operation completes.</span></span>
    
<span data-ttu-id="b5f52-115">TBL_BATCH</span><span class="sxs-lookup"><span data-stu-id="b5f52-115">TBL_BATCH</span></span> 
  
> <span data-ttu-id="b5f52-116">Submete-avaliação do filtro até que os dados na tabela são necessários.</span><span class="sxs-lookup"><span data-stu-id="b5f52-116">Defers evaluation of the filter until the data in the table is required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b5f52-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="b5f52-117">Return value</span></span>

<span data-ttu-id="b5f52-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="b5f52-118">S_OK</span></span> 
  
> <span data-ttu-id="b5f52-119">O filtro foi aplicado com êxito.</span><span class="sxs-lookup"><span data-stu-id="b5f52-119">The filter was successfully applied.</span></span>
    
<span data-ttu-id="b5f52-120">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="b5f52-120">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="b5f52-121">Outra operação está em andamento que impede que a operação de restrição seja iniciado.</span><span class="sxs-lookup"><span data-stu-id="b5f52-121">Another operation is in progress that prevents the restriction operation from starting.</span></span> <span data-ttu-id="b5f52-122">Ou a operação em andamento deve ter permissão para concluir ou ele deve ser interrompido.</span><span class="sxs-lookup"><span data-stu-id="b5f52-122">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="b5f52-123">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="b5f52-123">MAPI_E_TOO_COMPLEX</span></span> 
  
> <span data-ttu-id="b5f52-124">A tabela não é possível executar a operação porque o filtro determinado apontado pelo parâmetro _lpRestriction_ é muito complicado.</span><span class="sxs-lookup"><span data-stu-id="b5f52-124">The table cannot perform the operation because the particular filter pointed to by the  _lpRestriction_ parameter is too complicated.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b5f52-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="b5f52-125">Remarks</span></span>

<span data-ttu-id="b5f52-126">O método **IMAPITable:: Restrict** estabelece uma restrição, ou filtro em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="b5f52-126">The **IMAPITable::Restrict** method establishes a restriction, or filter, on a table.</span></span> <span data-ttu-id="b5f52-127">Se houver uma restrição anterior, ela é descartada e uma nova aplicada.</span><span class="sxs-lookup"><span data-stu-id="b5f52-127">If there is a previous restriction, it is discarded and the new one applied.</span></span> <span data-ttu-id="b5f52-128">Aplicar uma restrição não terá nenhum efeito nos dados subjacentes de uma tabela; ele simplesmente altera o modo de exibição, limitando as linhas que podem ser recuperadas às linhas que contêm dados que satisfazem a restrição.</span><span class="sxs-lookup"><span data-stu-id="b5f52-128">Applying a restriction has no affect on the underlying data of a table; it simply alters the view by limiting the rows that can be retrieved to rows containing data that satisfy the restriction.</span></span> 
  
<span data-ttu-id="b5f52-129">Há vários tipos diferentes de restrições, cada descrita com uma estrutura diferente.</span><span class="sxs-lookup"><span data-stu-id="b5f52-129">There are several different types of restrictions, each described with a different structure.</span></span> <span data-ttu-id="b5f52-130">A estrutura de [SRestriction](srestriction.md) contém dois membros: um valor que indica o tipo de restrição e a estrutura específica aplicável desse tipo.</span><span class="sxs-lookup"><span data-stu-id="b5f52-130">The [SRestriction](srestriction.md) structure contains two members: a value that indicates the type of restriction and the specific structure applicable for that type.</span></span> 
  
<span data-ttu-id="b5f52-131">Notificações de linhas da tabela que estão ocultas do modo por chamadas para **Restrict** nunca são geradas.</span><span class="sxs-lookup"><span data-stu-id="b5f52-131">Notifications for table rows that are hidden from view by calls to **Restrict** are never generated.</span></span> 
  
<span data-ttu-id="b5f52-132">Uma restrição de propriedade em uma propriedade de valores múltiplos funciona como uma restrição em uma propriedade de valor único.</span><span class="sxs-lookup"><span data-stu-id="b5f52-132">A property restriction on a multivalued property works like a restriction on a single-valued property.</span></span> <span data-ttu-id="b5f52-133">Uma propriedade de vários valores a serem usados em uma restrição de propriedade deve ter o sinalizador MVI_FLAG definido.</span><span class="sxs-lookup"><span data-stu-id="b5f52-133">A multivalued property to be used in a property restriction must have the MVI_FLAG flag set.</span></span> <span data-ttu-id="b5f52-134">Se ele não tiver esse sinalizador definido, ela é tratada como uma tupla totalmente ordenada.</span><span class="sxs-lookup"><span data-stu-id="b5f52-134">If it doesn't have this flag set, it is treated as a totally ordered tuple.</span></span> <span data-ttu-id="b5f52-135">Uma comparação de duas colunas multivaloradas compara os elementos de coluna em ordem, a relação entre as colunas na primeira inequação de emissão de relatórios.</span><span class="sxs-lookup"><span data-stu-id="b5f52-135">A comparison of two multivalued columns compares the column elements in order, reporting the relation of the columns at the first inequality.</span></span> <span data-ttu-id="b5f52-136">Igualdade será retornada somente se as colunas comparadas contêm os mesmos valores na mesma ordem.</span><span class="sxs-lookup"><span data-stu-id="b5f52-136">Equality is returned only if the columns compared contain the same values in the same order.</span></span> <span data-ttu-id="b5f52-137">Se uma coluna tiver valores menos que o outro, a relação relatada é de um valor nulo para o outro valor.</span><span class="sxs-lookup"><span data-stu-id="b5f52-137">If one column has fewer values than the other, the reported relation is that of a null value to the other value.</span></span>
  
<span data-ttu-id="b5f52-138">Para obter mais informações sobre as restrições, consulte [Sobre restrições](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="b5f52-138">For more information about restrictions, see [About Restrictions](about-restrictions.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="b5f52-139">Se você criar consultas dinâmicas para pesquisar dados no servidor, use o método **FindRow** em vez de usar o método **Restrict** e o método **QueryRows** juntos.</span><span class="sxs-lookup"><span data-stu-id="b5f52-139">If you create dynamic queries to search for data on the server, use the **FindRow** method instead of using the **Restrict** method and the **QueryRows** method together.</span></span> <span data-ttu-id="b5f52-140">O método **Restrict** cria um modo de exibição de cache que é usado para avaliar todas as mensagens adicionados a ou modificado na pasta base.</span><span class="sxs-lookup"><span data-stu-id="b5f52-140">The **Restrict** method creates a cached view that is used to evaluate all messages added to or modified in the base folder.</span></span> <span data-ttu-id="b5f52-141">Se um aplicativo cliente usa o método **Restrict** para cada consulta dinâmica, um modo de exibição em cache será criado para cada consulta.</span><span class="sxs-lookup"><span data-stu-id="b5f52-141">If a client application uses the **Restrict** method for each dynamic query, a cached view will be created for each query.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b5f52-142">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="b5f52-142">Notes to callers</span></span>

<span data-ttu-id="b5f52-143">Para descartar a restrição atual sem criar um novo, passe NULL no _lpRestriction_.</span><span class="sxs-lookup"><span data-stu-id="b5f52-143">To discard the current restriction without creating a new one, pass NULL in  _lpRestriction_.</span></span>
  
<span data-ttu-id="b5f52-144">Se outra chamada assíncrona tabela estiver em andamento, causando **Restrict** retornar MAPI_E_BUSY, é possível chamar [IMAPITable::Abort](imapitable-abort.md) para interromper a chamada.</span><span class="sxs-lookup"><span data-stu-id="b5f52-144">If another asynchronous table call is in progress, causing **Restrict** to return MAPI_E_BUSY, you can call [IMAPITable::Abort](imapitable-abort.md) to stop the call.</span></span> 
  
 <span data-ttu-id="b5f52-145">**Restrict** opera de maneira síncrona, a menos que você defina um dos sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="b5f52-145">**Restrict** operates synchronously unless you set one of the flags.</span></span> <span data-ttu-id="b5f52-146">Se você definir o sinalizador TBL_BATCH, **Restrict** adia a avaliação da restrição, a menos que você solicitar os dados.</span><span class="sxs-lookup"><span data-stu-id="b5f52-146">If you set the TBL_BATCH flag, **Restrict** postpones the evaluation of the restriction unless you request the data.</span></span> <span data-ttu-id="b5f52-147">Se o sinalizador TBL_ASYNC estiver definido, **Restrict**opera de forma assíncrona, retornando potencialmente antes da conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="b5f52-147">If the TBL_ASYNC flag is set, **Restrict**operates asynchronously, potentially returning before the completion of the operation.</span></span>
  
<span data-ttu-id="b5f52-148">Todos os indicadores para uma tabela são descartados quando é feita uma chamada para **Restrict** e BOOKMARK_CURRENT, a posição atual do cursor, é definida para o início da tabela.</span><span class="sxs-lookup"><span data-stu-id="b5f52-148">All bookmarks for a table are discarded when a call to **Restrict** is made, and BOOKMARK_CURRENT, the current cursor position, is set to the beginning of the table.</span></span> 
  
<span data-ttu-id="b5f52-149">Se você tentar impor uma restrição de propriedade em uma propriedade que não esteja no conjunto de colunas da tabela, os resultados são indefinidos.</span><span class="sxs-lookup"><span data-stu-id="b5f52-149">If you attempt to impose a property restriction on a property that is not in the table's column set, the results are undefined.</span></span> <span data-ttu-id="b5f52-150">Sempre que você não tiver certeza de como para se uma propriedade é suportada em uma tabela, combinar a restrição de propriedade com uma restrição de existir.</span><span class="sxs-lookup"><span data-stu-id="b5f52-150">Whenever you are unsure as to whether a property is supported in a table, combine the property restriction with an exists restriction.</span></span> <span data-ttu-id="b5f52-151">A restrição verifica a existência da propriedade antes de tentar impor a restrição de propriedade de existir.</span><span class="sxs-lookup"><span data-stu-id="b5f52-151">The exists restriction checks for the existence of the property before attempting to impose the property restriction.</span></span> 
  
<span data-ttu-id="b5f52-152">Não espera receber uma notificação de tabela em uma linha que tiver sido filtrada de uma tabela devido a uma restrição.</span><span class="sxs-lookup"><span data-stu-id="b5f52-152">Do not expect to receive a table notification on a row that has been filtered from a table due to a restriction.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b5f52-153">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="b5f52-153">MFCMAPI reference</span></span>

<span data-ttu-id="b5f52-154">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b5f52-154">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b5f52-155">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="b5f52-155">**File**</span></span>|<span data-ttu-id="b5f52-156">**Function**</span><span class="sxs-lookup"><span data-stu-id="b5f52-156">**Function**</span></span>|<span data-ttu-id="b5f52-157">**Comment**</span><span class="sxs-lookup"><span data-stu-id="b5f52-157">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b5f52-158">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="b5f52-158">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="b5f52-159">CContentsTableListCtrl::ApplyRestriction</span><span class="sxs-lookup"><span data-stu-id="b5f52-159">CContentsTableListCtrl::ApplyRestriction</span></span>  <br/> |<span data-ttu-id="b5f52-160">MFCMAPI usa o método **IMAPITable:: Restrict** para definir uma restrição em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="b5f52-160">MFCMAPI uses the **IMAPITable::Restrict** method to set a restriction on a table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b5f52-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="b5f52-161">See also</span></span>



[<span data-ttu-id="b5f52-162">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="b5f52-162">IMAPITable::Abort</span></span>](imapitable-abort.md)
  
[<span data-ttu-id="b5f52-163">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="b5f52-163">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
  
[<span data-ttu-id="b5f52-164">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="b5f52-164">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
  
[<span data-ttu-id="b5f52-165">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="b5f52-165">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="b5f52-166">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="b5f52-166">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="b5f52-167">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b5f52-167">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="b5f52-168">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="b5f52-168">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

