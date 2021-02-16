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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425600"
---
# <a name="imapitablegetrowcount"></a><span data-ttu-id="80600-103">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="80600-103">IMAPITable::GetRowCount</span></span>

  
  
<span data-ttu-id="80600-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="80600-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="80600-105">Retorna o número total de linhas na tabela.</span><span class="sxs-lookup"><span data-stu-id="80600-105">Returns the total number of rows in the table.</span></span> 
  
```cpp
HRESULT GetRowCount(
ULONG ulFlags,
ULONG FAR * lpulCount
);
```

## <a name="parameters"></a><span data-ttu-id="80600-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="80600-106">Parameters</span></span>

 <span data-ttu-id="80600-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="80600-107">_ulFlags_</span></span>
  
> <span data-ttu-id="80600-108">Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="80600-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="80600-109">_lpulCount_</span><span class="sxs-lookup"><span data-stu-id="80600-109">_lpulCount_</span></span>
  
> <span data-ttu-id="80600-110">[out] Ponteiro para o número de linhas na tabela.</span><span class="sxs-lookup"><span data-stu-id="80600-110">[out] Pointer to the number of rows in the table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="80600-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="80600-111">Return value</span></span>

<span data-ttu-id="80600-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="80600-112">S_OK</span></span> 
  
> <span data-ttu-id="80600-113">A contagem de linhas foi retornada com êxito.</span><span class="sxs-lookup"><span data-stu-id="80600-113">The row count was successfully returned.</span></span>
    
<span data-ttu-id="80600-114">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="80600-114">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="80600-115">Outra operação está em andamento que impede o início da operação de recuperação de contagem de linhas.</span><span class="sxs-lookup"><span data-stu-id="80600-115">Another operation is in progress that prevents the row count retrieval operation from starting.</span></span> <span data-ttu-id="80600-116">A operação em andamento deve ter permissão para ser concluída ou deve ser interrompida.</span><span class="sxs-lookup"><span data-stu-id="80600-116">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="80600-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="80600-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="80600-118">A tabela não pode calcular o número de linhas.</span><span class="sxs-lookup"><span data-stu-id="80600-118">The table cannot calculate the number of rows.</span></span>
    
<span data-ttu-id="80600-119">MAPI_W_APPROX_COUNT</span><span class="sxs-lookup"><span data-stu-id="80600-119">MAPI_W_APPROX_COUNT</span></span> 
  
> <span data-ttu-id="80600-120">A chamada foi bem-sucedida, mas uma contagem aproximada de linhas foi retornada porque a contagem exata de linhas não pôde ser determinada possivelmente devido a restrições de memória.</span><span class="sxs-lookup"><span data-stu-id="80600-120">The call succeeded, but an approximate row count was returned because the exact row count could not be determined possibly due to memory constraints.</span></span> <span data-ttu-id="80600-121">Para testar esse aviso, use a **HR_FAILED** macro.</span><span class="sxs-lookup"><span data-stu-id="80600-121">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="80600-122">Consulte [Usando macros para tratamento de erros.](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="80600-122">See [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="80600-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="80600-123">Remarks</span></span>

<span data-ttu-id="80600-124">O **método IMAPITable::GetRowCount** recupera o número total de linhas em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="80600-124">The **IMAPITable::GetRowCount** method retrieves the total number of rows in a table.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="80600-125">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="80600-125">Notes to implementers</span></span>

<span data-ttu-id="80600-126">Se não for possível determinar a contagem exata de linhas da tabela, retorne MAPI_W_APPROX_COUNT uma contagem aproximada de linhas no conteúdo do parâmetro _lpulCount._</span><span class="sxs-lookup"><span data-stu-id="80600-126">If you cannot determine the table's exact row count, return MAPI_W_APPROX_COUNT and an approximate row count in the contents of the  _lpulCount_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="80600-127">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="80600-127">Notes to callers</span></span>

<span data-ttu-id="80600-128">Use **GetRowCount** para descobrir quantas linhas uma tabela contém antes de fazer uma chamada para o método [IMAPITable::QueryRows](imapitable-queryrows.md) para recuperar os dados.</span><span class="sxs-lookup"><span data-stu-id="80600-128">Use **GetRowCount** to find out how many rows a table holds before making a call to the [IMAPITable::QueryRows](imapitable-queryrows.md) method to retrieve the data.</span></span> <span data-ttu-id="80600-129">Se houver menos de vinte linhas na tabela, é seguro chamar **QueryPosition** para recuperar a tabela inteira.</span><span class="sxs-lookup"><span data-stu-id="80600-129">If there are less than twenty rows in the table, it is safe to call **QueryPosition** to retrieve the whole table.</span></span> <span data-ttu-id="80600-130">Se houver mais de vinte linhas na tabela, considere fazer várias chamadas para **QueryPosition** e limite o número de linhas recuperadas em cada chamada.</span><span class="sxs-lookup"><span data-stu-id="80600-130">If there are more than twenty rows in the table, consider making multiple calls to **QueryPosition** and limit the number of rows retrieved in each call.</span></span> 
  
<span data-ttu-id="80600-131">Algumas tabelas não suportam **GetRowCount** e retornam MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="80600-131">Some tables do not support **GetRowCount** and return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="80600-132">Se **GetRowCount** não tiver suporte, uma alternativa pode ser chamar [IMAPITable::QueryPosition](imapitable-queryposition.md).</span><span class="sxs-lookup"><span data-stu-id="80600-132">If **GetRowCount** is not supported, an alternative might be to call [IMAPITable::QueryPosition](imapitable-queryposition.md).</span></span> <span data-ttu-id="80600-133">Com os resultados de **QueryPosition**, você pode determinar a relação entre a linha atual e a última linha.</span><span class="sxs-lookup"><span data-stu-id="80600-133">With the results from **QueryPosition**, you can determine the relationship between the current row and last row.</span></span> 
  
<span data-ttu-id="80600-134">Quando **GetRowCount** retornar MAPI_E_BUSY porque não é possível recuperar temporariamente uma contagem de linhas, chame o método [IMAPITable::WaitForCompletion.](imapitable-waitforcompletion.md)</span><span class="sxs-lookup"><span data-stu-id="80600-134">When **GetRowCount** returns MAPI_E_BUSY because it is temporarily unable to retrieve a row count, call the [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) method.</span></span> <span data-ttu-id="80600-135">Quando **WaitForCompletion** retornar, repetir a chamada para **GetRowCount**.</span><span class="sxs-lookup"><span data-stu-id="80600-135">When **WaitForCompletion** returns, retry the call to **GetRowCount**.</span></span> <span data-ttu-id="80600-136">Outra maneira de detectar se uma operação assíncrona está em andamento é chamar o método [IMAPITable::GetStatus](imapitable-getstatus.md) e verificar o conteúdo do parâmetro _lpulTableState._</span><span class="sxs-lookup"><span data-stu-id="80600-136">Another way to detect whether an asynchronous operation is in progress is to call the [IMAPITable::GetStatus](imapitable-getstatus.md) method and check the contents of the  _lpulTableState_ parameter.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="80600-137">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="80600-137">MFCMAPI reference</span></span>

<span data-ttu-id="80600-138">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="80600-138">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="80600-139">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="80600-139">**File**</span></span>|<span data-ttu-id="80600-140">**Função**</span><span class="sxs-lookup"><span data-stu-id="80600-140">**Function**</span></span>|<span data-ttu-id="80600-141">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="80600-141">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="80600-142">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="80600-142">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="80600-143">CopyFolderContents</span><span class="sxs-lookup"><span data-stu-id="80600-143">CopyFolderContents</span></span>  <br/> |<span data-ttu-id="80600-144">MFCMAPI usa o método **IMAPITable::GetRowCount** para determinar quantas linhas estão na tabela de origem para que a memória possa ser alocada para executar a cópia.</span><span class="sxs-lookup"><span data-stu-id="80600-144">MFCMAPI uses the **IMAPITable::GetRowCount** method to determine how many rows are in the source table so memory can be allocated to perform the copy.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="80600-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="80600-145">See also</span></span>



[<span data-ttu-id="80600-146">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="80600-146">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md)
  
[<span data-ttu-id="80600-147">IMAPITable::QueryPosition</span><span class="sxs-lookup"><span data-stu-id="80600-147">IMAPITable::QueryPosition</span></span>](imapitable-queryposition.md)
  
[<span data-ttu-id="80600-148">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="80600-148">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="80600-149">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="80600-149">IMAPITable::WaitForCompletion</span></span>](imapitable-waitforcompletion.md)
  
[<span data-ttu-id="80600-150">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="80600-150">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="80600-151">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="80600-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

