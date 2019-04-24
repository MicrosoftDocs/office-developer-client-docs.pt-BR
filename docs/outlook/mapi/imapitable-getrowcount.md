---
title: IMAPITableGetRowCount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetRowCount
api_type:
- COM
ms.assetid: 44a12c92-7462-4acf-9520-5d4c2d7f1d47
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b13bf3bdd8392efc42ad189e48dffad8636f0708
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328885"
---
# <a name="imapitablegetrowcount"></a><span data-ttu-id="631fa-103">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="631fa-103">IMAPITable::GetRowCount</span></span>

  
  
<span data-ttu-id="631fa-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="631fa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="631fa-105">Retorna o número total de linhas na tabela.</span><span class="sxs-lookup"><span data-stu-id="631fa-105">Returns the total number of rows in the table.</span></span> 
  
```cpp
HRESULT GetRowCount(
ULONG ulFlags,
ULONG FAR * lpulCount
);
```

## <a name="parameters"></a><span data-ttu-id="631fa-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="631fa-106">Parameters</span></span>

 <span data-ttu-id="631fa-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="631fa-107">_ulFlags_</span></span>
  
> <span data-ttu-id="631fa-108">Serve deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="631fa-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="631fa-109">_lpulCount_</span><span class="sxs-lookup"><span data-stu-id="631fa-109">_lpulCount_</span></span>
  
> <span data-ttu-id="631fa-110">bota Ponteiro para o número de linhas na tabela.</span><span class="sxs-lookup"><span data-stu-id="631fa-110">[out] Pointer to the number of rows in the table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="631fa-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="631fa-111">Return value</span></span>

<span data-ttu-id="631fa-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="631fa-112">S_OK</span></span> 
  
> <span data-ttu-id="631fa-113">A contagem de linhas foi retornada com êxito.</span><span class="sxs-lookup"><span data-stu-id="631fa-113">The row count was successfully returned.</span></span>
    
<span data-ttu-id="631fa-114">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="631fa-114">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="631fa-115">Outra operação está em andamento, o que impede a inicialização da operação de recuperação de contagem de linhas.</span><span class="sxs-lookup"><span data-stu-id="631fa-115">Another operation is in progress that prevents the row count retrieval operation from starting.</span></span> <span data-ttu-id="631fa-116">A operação em andamento deve ter permissão para ser concluída ou deve ser interrompida.</span><span class="sxs-lookup"><span data-stu-id="631fa-116">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="631fa-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="631fa-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="631fa-118">A tabela não pode calcular o número de linhas.</span><span class="sxs-lookup"><span data-stu-id="631fa-118">The table cannot calculate the number of rows.</span></span>
    
<span data-ttu-id="631fa-119">MAPI_W_APPROX_COUNT</span><span class="sxs-lookup"><span data-stu-id="631fa-119">MAPI_W_APPROX_COUNT</span></span> 
  
> <span data-ttu-id="631fa-120">A chamada teve êxito, mas uma contagem de linhas aproximada foi retornada porque a contagem de linhas exata não pôde ser determinada possivelmente devido a restrições de memória.</span><span class="sxs-lookup"><span data-stu-id="631fa-120">The call succeeded, but an approximate row count was returned because the exact row count could not be determined possibly due to memory constraints.</span></span> <span data-ttu-id="631fa-121">Para testar esse aviso, use a macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="631fa-121">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="631fa-122">Consulte [usando macros para tratamento de erros](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="631fa-122">See [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="631fa-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="631fa-123">Remarks</span></span>

<span data-ttu-id="631fa-124">O método imApitable **:: GetRowCount** recupera o número total de linhas em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="631fa-124">The **IMAPITable::GetRowCount** method retrieves the total number of rows in a table.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="631fa-125">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="631fa-125">Notes to implementers</span></span>

<span data-ttu-id="631fa-126">Se você não puder determinar a contagem exata da linha da tabela, retorne MAPI_W_APPROX_COUNT e uma contagem de linha aproximada no conteúdo do parâmetro _lpulCount_ .</span><span class="sxs-lookup"><span data-stu-id="631fa-126">If you cannot determine the table's exact row count, return MAPI_W_APPROX_COUNT and an approximate row count in the contents of the  _lpulCount_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="631fa-127">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="631fa-127">Notes to callers</span></span>

<span data-ttu-id="631fa-128">Use **GetRowCount** para descobrir quantas linhas uma tabela é mantida antes de fazer uma chamada para o método IMAPITable [:: QueryRows](imapitable-queryrows.md) para recuperar os dados.</span><span class="sxs-lookup"><span data-stu-id="631fa-128">Use **GetRowCount** to find out how many rows a table holds before making a call to the [IMAPITable::QueryRows](imapitable-queryrows.md) method to retrieve the data.</span></span> <span data-ttu-id="631fa-129">Se houver menos de vinte linhas na tabela, é seguro chamar o **QueryPosition** para recuperar a tabela inteira.</span><span class="sxs-lookup"><span data-stu-id="631fa-129">If there are less than twenty rows in the table, it is safe to call **QueryPosition** to retrieve the whole table.</span></span> <span data-ttu-id="631fa-130">Se houver mais de vinte linhas na tabela, considere fazer várias chamadas para **QueryPosition** e limitar o número de linhas recuperadas em cada chamada.</span><span class="sxs-lookup"><span data-stu-id="631fa-130">If there are more than twenty rows in the table, consider making multiple calls to **QueryPosition** and limit the number of rows retrieved in each call.</span></span> 
  
<span data-ttu-id="631fa-131">Algumas tabelas não dão suporte \*\*\*\* a GetRowCount e retornam MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="631fa-131">Some tables do not support **GetRowCount** and return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="631fa-132">Se **GetRowCount** não for suportado, uma alternativa pode ser chamar IMAPITable [:: QueryPosition](imapitable-queryposition.md).</span><span class="sxs-lookup"><span data-stu-id="631fa-132">If **GetRowCount** is not supported, an alternative might be to call [IMAPITable::QueryPosition](imapitable-queryposition.md).</span></span> <span data-ttu-id="631fa-133">Com os resultados de **QueryPosition**, você pode determinar a relação entre a linha atual e a última linha.</span><span class="sxs-lookup"><span data-stu-id="631fa-133">With the results from **QueryPosition**, you can determine the relationship between the current row and last row.</span></span> 
  
<span data-ttu-id="631fa-134">Quando **GetRowCount** Retorna MAPI_E_BUSY porque é temporariamente impossível recuperar uma contagem de linha, chame o método [IMAPITable:: WaitForCompletion](imapitable-waitforcompletion.md) .</span><span class="sxs-lookup"><span data-stu-id="631fa-134">When **GetRowCount** returns MAPI_E_BUSY because it is temporarily unable to retrieve a row count, call the [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) method.</span></span> <span data-ttu-id="631fa-135">Quando **WaitForCompletion** retornar, repita a chamada para **GetRowCount**.</span><span class="sxs-lookup"><span data-stu-id="631fa-135">When **WaitForCompletion** returns, retry the call to **GetRowCount**.</span></span> <span data-ttu-id="631fa-136">Outra maneira de detectar se uma operação assíncrona está em andamento é chamar o método imApitable [:: GetStatus](imapitable-getstatus.md) e verificar o conteúdo do parâmetro _lpulTableState_ .</span><span class="sxs-lookup"><span data-stu-id="631fa-136">Another way to detect whether an asynchronous operation is in progress is to call the [IMAPITable::GetStatus](imapitable-getstatus.md) method and check the contents of the  _lpulTableState_ parameter.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="631fa-137">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="631fa-137">MFCMAPI reference</span></span>

<span data-ttu-id="631fa-138">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="631fa-138">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="631fa-139">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="631fa-139">**File**</span></span>|<span data-ttu-id="631fa-140">**Função**</span><span class="sxs-lookup"><span data-stu-id="631fa-140">**Function**</span></span>|<span data-ttu-id="631fa-141">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="631fa-141">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="631fa-142">MAPIFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="631fa-142">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="631fa-143">CopyFolderContents</span><span class="sxs-lookup"><span data-stu-id="631fa-143">CopyFolderContents</span></span>  <br/> |<span data-ttu-id="631fa-144">MFCMAPI usa o método imApitable **:: GetRowCount** para determinar quantas linhas estão na tabela de origem para que a memória possa ser alocada para executar a cópia.</span><span class="sxs-lookup"><span data-stu-id="631fa-144">MFCMAPI uses the **IMAPITable::GetRowCount** method to determine how many rows are in the source table so memory can be allocated to perform the copy.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="631fa-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="631fa-145">See also</span></span>



[<span data-ttu-id="631fa-146">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="631fa-146">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md)
  
[<span data-ttu-id="631fa-147">IMAPITable::QueryPosition</span><span class="sxs-lookup"><span data-stu-id="631fa-147">IMAPITable::QueryPosition</span></span>](imapitable-queryposition.md)
  
[<span data-ttu-id="631fa-148">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="631fa-148">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="631fa-149">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="631fa-149">IMAPITable::WaitForCompletion</span></span>](imapitable-waitforcompletion.md)
  
[<span data-ttu-id="631fa-150">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="631fa-150">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="631fa-151">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="631fa-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

