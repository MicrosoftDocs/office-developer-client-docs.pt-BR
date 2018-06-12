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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: a591a49c1cb0ec936d09d59b4632d15e4842dd2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767337"
---
# <a name="imapitablegetrowcount"></a><span data-ttu-id="5d340-103">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="5d340-103">IMAPITable::GetRowCount</span></span>

  
  
<span data-ttu-id="5d340-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5d340-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5d340-105">Retorna o número total de linhas na tabela.</span><span class="sxs-lookup"><span data-stu-id="5d340-105">Returns the total number of rows in the table.</span></span> 
  
```cpp
HRESULT GetRowCount(
ULONG ulFlags,
ULONG FAR * lpulCount
);
```

## <a name="parameters"></a><span data-ttu-id="5d340-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="5d340-106">Parameters</span></span>

 <span data-ttu-id="5d340-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5d340-107">_ulFlags_</span></span>
  
> <span data-ttu-id="5d340-108">Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="5d340-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="5d340-109">_lpulCount_</span><span class="sxs-lookup"><span data-stu-id="5d340-109">_lpulCount_</span></span>
  
> <span data-ttu-id="5d340-110">[out] Ponteiro para o número de linhas da tabela.</span><span class="sxs-lookup"><span data-stu-id="5d340-110">[out] Pointer to the number of rows in the table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5d340-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="5d340-111">Return value</span></span>

<span data-ttu-id="5d340-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="5d340-112">S_OK</span></span> 
  
> <span data-ttu-id="5d340-113">A contagem de linhas foi retornada com êxito.</span><span class="sxs-lookup"><span data-stu-id="5d340-113">The row count was successfully returned.</span></span>
    
<span data-ttu-id="5d340-114">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="5d340-114">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="5d340-115">Outra operação está em andamento que impede que a operação de recuperação de contagem de linha seja iniciado.</span><span class="sxs-lookup"><span data-stu-id="5d340-115">Another operation is in progress that prevents the row count retrieval operation from starting.</span></span> <span data-ttu-id="5d340-116">Ou a operação em andamento deve ter permissão para concluir ou ele deve ser interrompido.</span><span class="sxs-lookup"><span data-stu-id="5d340-116">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="5d340-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="5d340-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="5d340-118">A tabela não é possível calcular o número de linhas.</span><span class="sxs-lookup"><span data-stu-id="5d340-118">The table cannot calculate the number of rows.</span></span>
    
<span data-ttu-id="5d340-119">MAPI_W_APPROX_COUNT</span><span class="sxs-lookup"><span data-stu-id="5d340-119">MAPI_W_APPROX_COUNT</span></span> 
  
> <span data-ttu-id="5d340-120">A chamada foi bem-sucedida, mas uma contagem de linhas aproximada foi retornada porque o número exato de linhas não pôde ser determinado possivelmente devido a restrições de memória.</span><span class="sxs-lookup"><span data-stu-id="5d340-120">The call succeeded, but an approximate row count was returned because the exact row count could not be determined possibly due to memory constraints.</span></span> <span data-ttu-id="5d340-121">Para testar esse aviso, use a macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="5d340-121">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="5d340-122">Consulte [usando Macros para tratamento de erros](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="5d340-122">See [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5d340-123">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="5d340-123">Remarks</span></span>

<span data-ttu-id="5d340-124">O método **IMAPITable::GetRowCount** recupera o número total de linhas em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="5d340-124">The **IMAPITable::GetRowCount** method retrieves the total number of rows in a table.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="5d340-125">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="5d340-125">Notes to implementers</span></span>

<span data-ttu-id="5d340-126">Se você não puder determinar a contagem de exato de linhas da tabela, retorno MAPI_W_APPROX_COUNT e uma linha aproximada contagem no conteúdo do parâmetro _lpulCount_ .</span><span class="sxs-lookup"><span data-stu-id="5d340-126">If you cannot determine the table's exact row count, return MAPI_W_APPROX_COUNT and an approximate row count in the contents of the  _lpulCount_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="5d340-127">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="5d340-127">Notes to callers</span></span>

<span data-ttu-id="5d340-128">Usar **GetRowCount** para descobrir quantas linhas uma tabela contém antes de fazer uma chamada para o método [IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar os dados.</span><span class="sxs-lookup"><span data-stu-id="5d340-128">Use **GetRowCount** to find out how many rows a table holds before making a call to the [IMAPITable::QueryRows](imapitable-queryrows.md) method to retrieve the data.</span></span> <span data-ttu-id="5d340-129">Se houver menos de vinte linhas na tabela, é seguro chamar **QueryPosition** para recuperar a tabela inteira.</span><span class="sxs-lookup"><span data-stu-id="5d340-129">If there are less than twenty rows in the table, it is safe to call **QueryPosition** to retrieve the whole table.</span></span> <span data-ttu-id="5d340-130">Se houver mais de vinte linhas da tabela, considere a possibilidade de várias chamadas para **QueryPosition** e limitar o número de linhas recuperadas em cada chamada.</span><span class="sxs-lookup"><span data-stu-id="5d340-130">If there are more than twenty rows in the table, consider making multiple calls to **QueryPosition** and limit the number of rows retrieved in each call.</span></span> 
  
<span data-ttu-id="5d340-131">Algumas tabelas não suportam **GetRowCount** e retornar MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="5d340-131">Some tables do not support **GetRowCount** and return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="5d340-132">Se não há suporte para **GetRowCount** , pode ser uma alternativa chamada [IMAPITable::QueryPosition](imapitable-queryposition.md).</span><span class="sxs-lookup"><span data-stu-id="5d340-132">If **GetRowCount** is not supported, an alternative might be to call [IMAPITable::QueryPosition](imapitable-queryposition.md).</span></span> <span data-ttu-id="5d340-133">Com os resultados do **QueryPosition**, você pode determinar a relação entre a linha atual e a última linha.</span><span class="sxs-lookup"><span data-stu-id="5d340-133">With the results from **QueryPosition**, you can determine the relationship between the current row and last row.</span></span> 
  
<span data-ttu-id="5d340-134">Quando **GetRowCount** retorna MAPI_E_BUSY porque ele é temporariamente não é possível recuperar uma contagem de linha, chame o método de [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) .</span><span class="sxs-lookup"><span data-stu-id="5d340-134">When **GetRowCount** returns MAPI_E_BUSY because it is temporarily unable to retrieve a row count, call the [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) method.</span></span> <span data-ttu-id="5d340-135">Quando **WaitForCompletion** retorna, repita a chamada para **GetRowCount**.</span><span class="sxs-lookup"><span data-stu-id="5d340-135">When **WaitForCompletion** returns, retry the call to **GetRowCount**.</span></span> <span data-ttu-id="5d340-136">Outra maneira para detectar se uma operação assíncrona está em andamento é chamar o método [IMAPITable::GetStatus](imapitable-getstatus.md) e verifique o conteúdo do parâmetro _lpulTableState_ .</span><span class="sxs-lookup"><span data-stu-id="5d340-136">Another way to detect whether an asynchronous operation is in progress is to call the [IMAPITable::GetStatus](imapitable-getstatus.md) method and check the contents of the  _lpulTableState_ parameter.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5d340-137">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="5d340-137">MFCMAPI reference</span></span>

<span data-ttu-id="5d340-138">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="5d340-138">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5d340-139">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="5d340-139">**File**</span></span>|<span data-ttu-id="5d340-140">**Function**</span><span class="sxs-lookup"><span data-stu-id="5d340-140">**Function**</span></span>|<span data-ttu-id="5d340-141">**Comment**</span><span class="sxs-lookup"><span data-stu-id="5d340-141">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5d340-142">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="5d340-142">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="5d340-143">CopyFolderContents</span><span class="sxs-lookup"><span data-stu-id="5d340-143">CopyFolderContents</span></span>  <br/> |<span data-ttu-id="5d340-144">MFCMAPI usa o método **IMAPITable::GetRowCount** para determinar quantas linhas estão na tabela de origem, portanto, é possível alocar memória para realizar a cópia.</span><span class="sxs-lookup"><span data-stu-id="5d340-144">MFCMAPI uses the **IMAPITable::GetRowCount** method to determine how many rows are in the source table so memory can be allocated to perform the copy.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5d340-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="5d340-145">See also</span></span>



[<span data-ttu-id="5d340-146">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="5d340-146">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md)
  
[<span data-ttu-id="5d340-147">IMAPITable::QueryPosition</span><span class="sxs-lookup"><span data-stu-id="5d340-147">IMAPITable::QueryPosition</span></span>](imapitable-queryposition.md)
  
[<span data-ttu-id="5d340-148">IMAPITable:: QueryRows</span><span class="sxs-lookup"><span data-stu-id="5d340-148">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="5d340-149">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="5d340-149">IMAPITable::WaitForCompletion</span></span>](imapitable-waitforcompletion.md)
  
[<span data-ttu-id="5d340-150">IMAPITable: IUnknown</span><span class="sxs-lookup"><span data-stu-id="5d340-150">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="5d340-151">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="5d340-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

