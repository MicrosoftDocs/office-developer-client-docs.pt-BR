---
title: IMAPITableSeekRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SeekRow
api_type:
- COM
ms.assetid: 93ac63ae-f254-45e1-a9b1-347d69d2ed9f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: fbc990a8c962883aa07987b200d1d2fd55434f93
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413042"
---
# <a name="imapitableseekrow"></a><span data-ttu-id="ec41d-103">IMAPITable::SeekRow</span><span class="sxs-lookup"><span data-stu-id="ec41d-103">IMAPITable::SeekRow</span></span>

  
  
<span data-ttu-id="ec41d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ec41d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ec41d-105">Move o cursor para uma posição específica na tabela.</span><span class="sxs-lookup"><span data-stu-id="ec41d-105">Moves the cursor to a specific position in the table.</span></span>
  
```cpp
HRESULT SeekRow(
BOOKMARK bkOrigin,
LONG lRowCount,
LONG FAR * lplRowsSought
);
```

## <a name="parameters"></a><span data-ttu-id="ec41d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ec41d-106">Parameters</span></span>

 <span data-ttu-id="ec41d-107">_bkOrigin_</span><span class="sxs-lookup"><span data-stu-id="ec41d-107">_bkOrigin_</span></span>
  
> <span data-ttu-id="ec41d-108">[in] O indicador que identifica a posição inicial da operação de busca.</span><span class="sxs-lookup"><span data-stu-id="ec41d-108">[in] The bookmark identifying the starting position for the seek operation.</span></span> <span data-ttu-id="ec41d-109">Um indicador pode ser criado usando o método [IMAPITable::CreateBookmark](imapitable-createbookmark.md) ou um dos seguintes valores predefinidos pode ser passado.</span><span class="sxs-lookup"><span data-stu-id="ec41d-109">A bookmark can be created using the [IMAPITable::CreateBookmark](imapitable-createbookmark.md) method, or one of the following predefined values can be passed.</span></span> 
    
<span data-ttu-id="ec41d-110">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="ec41d-110">BOOKMARK_BEGINNING</span></span> 
  
> <span data-ttu-id="ec41d-111">Inicia a operação de busca desde o início da tabela.</span><span class="sxs-lookup"><span data-stu-id="ec41d-111">Starts the seek operation from the beginning of the table.</span></span> 
    
<span data-ttu-id="ec41d-112">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="ec41d-112">BOOKMARK_CURRENT</span></span> 
  
> <span data-ttu-id="ec41d-113">Inicia a operação de busca a partir da linha na tabela onde o cursor está localizado.</span><span class="sxs-lookup"><span data-stu-id="ec41d-113">Starts the seek operation from the row in the table where the cursor is located.</span></span> 
    
<span data-ttu-id="ec41d-114">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="ec41d-114">BOOKMARK_END</span></span> 
  
> <span data-ttu-id="ec41d-115">Inicia a operação de busca no final da tabela.</span><span class="sxs-lookup"><span data-stu-id="ec41d-115">Starts the seek operation from the end of the table.</span></span> 
    
 <span data-ttu-id="ec41d-116">_lRowCount_</span><span class="sxs-lookup"><span data-stu-id="ec41d-116">_lRowCount_</span></span>
  
> <span data-ttu-id="ec41d-117">[in] A contagem assinada do número de linhas a mover, começando pelo indicador identificado pelo _parâmetro bkOrigin._</span><span class="sxs-lookup"><span data-stu-id="ec41d-117">[in] The signed count of the number of rows to move, starting from the bookmark identified by the  _bkOrigin_ parameter.</span></span> 
    
 <span data-ttu-id="ec41d-118">_lplRowsSought_</span><span class="sxs-lookup"><span data-stu-id="ec41d-118">_lplRowsSought_</span></span>
  
> <span data-ttu-id="ec41d-119">[out] Se  _lRowCount_ for um ponteiro válido na entrada,  _lplRowsSought_ apontará para o número de linhas que foram processadas na operação de busca, o sinal indicando a direção da pesquisa, para frente ou para trás.</span><span class="sxs-lookup"><span data-stu-id="ec41d-119">[out] If  _lRowCount_ is a valid pointer on input,  _lplRowsSought_ points to the number of rows that were processed in the seek operation, the sign of which indicates the direction of search, forward or backward.</span></span> <span data-ttu-id="ec41d-120">Se  _lRowCount_ for negativo,  _lplRowsSought_ será negativo.</span><span class="sxs-lookup"><span data-stu-id="ec41d-120">If  _lRowCount_ is negative, then  _lplRowsSought_ is negative.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ec41d-121">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ec41d-121">Return value</span></span>

<span data-ttu-id="ec41d-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="ec41d-122">S_OK</span></span> 
  
> <span data-ttu-id="ec41d-123">A operação de busca foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="ec41d-123">The seek operation was successful.</span></span>
    
<span data-ttu-id="ec41d-124">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="ec41d-124">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="ec41d-125">Outra operação está em andamento que impede o início da operação de busca de linhas.</span><span class="sxs-lookup"><span data-stu-id="ec41d-125">Another operation is in progress that prevents the row-seeking operation from starting.</span></span> <span data-ttu-id="ec41d-126">A operação em andamento deve ter permissão para ser concluída ou deve ser interrompida.</span><span class="sxs-lookup"><span data-stu-id="ec41d-126">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="ec41d-127">MAPI_E_INVALID_BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="ec41d-127">MAPI_E_INVALID_BOOKMARK</span></span> 
  
> <span data-ttu-id="ec41d-128">O indicador especificado no parâmetro  _bkOrigin_ é inválido porque foi removido ou porque está além da última linha solicitada.</span><span class="sxs-lookup"><span data-stu-id="ec41d-128">The bookmark specified in the  _bkOrigin_ parameter is invalid because it was removed or because it is beyond the last row requested.</span></span> 
    
<span data-ttu-id="ec41d-129">MAPI_W_POSITION_CHANGED</span><span class="sxs-lookup"><span data-stu-id="ec41d-129">MAPI_W_POSITION_CHANGED</span></span> 
  
> <span data-ttu-id="ec41d-130">A chamada foi bem-sucedida, mas o indicador especificado no parâmetro  _bkOrigin_ não é mais definido na mesma linha que estava quando foi usada pela última vez.</span><span class="sxs-lookup"><span data-stu-id="ec41d-130">The call succeeded, but the bookmark specified in the  _bkOrigin_ parameter is no longer set at the same row as it was when it was last used.</span></span> <span data-ttu-id="ec41d-131">Se o indicador não tiver sido usado, ele não está mais na mesma posição que estava quando foi criado.</span><span class="sxs-lookup"><span data-stu-id="ec41d-131">If the bookmark has not been used, it is no longer in the same position as it was when it was created.</span></span> <span data-ttu-id="ec41d-132">Quando esse aviso é retornado, a chamada deve ser tratada como bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="ec41d-132">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="ec41d-133">Para testar esse aviso, use a **HR_FAILED** macro.</span><span class="sxs-lookup"><span data-stu-id="ec41d-133">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="ec41d-134">Para obter mais informações, consulte [Usando macros para tratamento de erros.](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="ec41d-134">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ec41d-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="ec41d-135">Remarks</span></span>

<span data-ttu-id="ec41d-136">O **método IMAPITable::SeekRow** estabelece uma nova BOOKMARK_CURRENT para o cursor.</span><span class="sxs-lookup"><span data-stu-id="ec41d-136">The **IMAPITable::SeekRow** method establishes a new BOOKMARK_CURRENT position for the cursor.</span></span> <span data-ttu-id="ec41d-137">O  _parâmetro lRowCount_ indica o número de linhas que o cursor move e a direção do movimento.</span><span class="sxs-lookup"><span data-stu-id="ec41d-137">The  _lRowCount_ parameter indicates the number of rows that the cursor moves and the direction of movement.</span></span> 
  
<span data-ttu-id="ec41d-138">Se a posição resultante estiver além da última linha da tabela, o cursor será posicionado após a última linha.</span><span class="sxs-lookup"><span data-stu-id="ec41d-138">If the resulting position is beyond the last row of the table, the cursor is positioned after the last row.</span></span> <span data-ttu-id="ec41d-139">Se a posição resultante estiver antes da primeira linha da tabela, o cursor será posicionado no início da primeira linha.</span><span class="sxs-lookup"><span data-stu-id="ec41d-139">If the resulting position is before the first row of the table, the cursor is positioned at the beginning of the first row.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ec41d-140">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="ec41d-140">Notes to implementers</span></span>

<span data-ttu-id="ec41d-141">Se a linha apontada por  _bkOrigin_ não existir mais na tabela e você não puder estabelecer uma nova posição para o indicador, retorne MAPI_E_INVALID_BOOKMARK.</span><span class="sxs-lookup"><span data-stu-id="ec41d-141">If the row pointed to by  _bkOrigin_ no longer exists in the table and you cannot establish a new position for the bookmark, return MAPI_E_INVALID_BOOKMARK.</span></span> <span data-ttu-id="ec41d-142">Se a linha apontada por  _bkOrigin_ não existir mais e você puder estabelecer uma nova posição para o indicador, retorne MAPI_W_POSITION_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="ec41d-142">If the row pointed to by  _bkOrigin_ no longer exists and you can establish a new position for the bookmark, return MAPI_W_POSITION_CHANGED.</span></span> 
  
<span data-ttu-id="ec41d-143">Um indicador apontando para uma linha que está recolhido para fora do ponto de vista da tabela ainda pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="ec41d-143">A bookmark pointing to a row that is collapsed out of the table view can still be used.</span></span> <span data-ttu-id="ec41d-144">Se o chamador tentar mover o cursor para esse indicador, mova o cursor para a próxima linha visível e retorne MAPI_W_POSITION_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="ec41d-144">If the caller attempts to move the cursor to such a bookmark, move the cursor to the next visible row and return MAPI_W_POSITION_CHANGED.</span></span> 
  
<span data-ttu-id="ec41d-145">Você pode mover indicadores para posições recolhidos para fora da exibição, seja no momento do uso ou no momento em que a linha é colada.</span><span class="sxs-lookup"><span data-stu-id="ec41d-145">You can move bookmarks for positions collapsed out of view, either at the time of use or at the time that the row is collapsed.</span></span> <span data-ttu-id="ec41d-146">Se um indicador for movido no momento em que a linha estiver recolhido, mantenha um pouco no indicador que indica se o indicador foi movido desde seu último uso ou, se nunca foi usado, desde sua criação.</span><span class="sxs-lookup"><span data-stu-id="ec41d-146">If a bookmark is moved at the time that the row is collapsed, keep a bit in the bookmark that indicates whether the bookmark has moved since its last use or, if it has never been used, since its creation.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="ec41d-147">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="ec41d-147">Notes to callers</span></span>

<span data-ttu-id="ec41d-148">Para indicar um movimento para trás **para SeekRow**, passe um valor negativo em  _lRowCount_.</span><span class="sxs-lookup"><span data-stu-id="ec41d-148">To indicate a backward move for **SeekRow**, pass a negative value in  _lRowCount_.</span></span> <span data-ttu-id="ec41d-149">Para pesquisar no início da tabela, passe zero em  _lRowCount_ e o valor BOOKMARK_BEGINNING  _em bkOrigin_.</span><span class="sxs-lookup"><span data-stu-id="ec41d-149">To search to the beginning of the table, pass zero in  _lRowCount_ and the value BOOKMARK_BEGINNING in  _bkOrigin_.</span></span> 
  
<span data-ttu-id="ec41d-150">Se houver muitas linhas na tabela, a operação **SeekRow** poderá ser lenta.</span><span class="sxs-lookup"><span data-stu-id="ec41d-150">If there are lots of rows in the table, the **SeekRow** operation can be slow.</span></span> <span data-ttu-id="ec41d-151">O desempenho também pode ser afetado se você precisar que uma contagem de linhas seja retornada no conteúdo do _parâmetro lplRowsSought._</span><span class="sxs-lookup"><span data-stu-id="ec41d-151">Performance can also be affected if you require a row count to be returned in the contents of the  _lplRowsSought_ parameter.</span></span> 
  
 <span data-ttu-id="ec41d-152">**SeekRow** retorna o número de linhas pesquisadas, positivas ou negativas, na variável apontada por  _lRowCount_.</span><span class="sxs-lookup"><span data-stu-id="ec41d-152">**SeekRow** returns the number of rows actually searched through, positive or negative, in the variable pointed to by  _lRowCount_.</span></span> <span data-ttu-id="ec41d-153">Em uma operação comum, ele deve retornar o mesmo valor de  _lplRowsSought_ como passado para  _lRowCount_, a menos que a pesquisa tenha atingido o início ou o fim da tabela.</span><span class="sxs-lookup"><span data-stu-id="ec41d-153">In ordinary operation, it should return the same value for  _lplRowsSought_ as passed in for  _lRowCount_, unless the search reached the beginning or end of the table.</span></span> 
  
<span data-ttu-id="ec41d-154">Não de definir  _lRowCount como_ um número maior que 50.</span><span class="sxs-lookup"><span data-stu-id="ec41d-154">Do not set  _lRowCount_ to a number greater than 50.</span></span> <span data-ttu-id="ec41d-155">Para procurar um número maior de linhas, use o [método IMAPITable::SeekRowApprox.](imapitable-seekrowapprox.md)</span><span class="sxs-lookup"><span data-stu-id="ec41d-155">To seek through a larger number of rows, use the [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ec41d-156">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ec41d-156">MFCMAPI reference</span></span>

<span data-ttu-id="ec41d-157">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ec41d-157">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ec41d-158">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="ec41d-158">**File**</span></span>|<span data-ttu-id="ec41d-159">**Função**</span><span class="sxs-lookup"><span data-stu-id="ec41d-159">**Function**</span></span>|<span data-ttu-id="ec41d-160">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="ec41d-160">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ec41d-161">MAPIProcessor.cpp</span><span class="sxs-lookup"><span data-stu-id="ec41d-161">MAPIProcessor.cpp</span></span>  <br/> |<span data-ttu-id="ec41d-162">CMAPIProcessor::P rocessMailboxTable</span><span class="sxs-lookup"><span data-stu-id="ec41d-162">CMAPIProcessor::ProcessMailboxTable</span></span>  <br/> |<span data-ttu-id="ec41d-163">MFCMAPI usa o **método IMAPITable::SeekRow** para localizar o início da tabela antes do processamento.</span><span class="sxs-lookup"><span data-stu-id="ec41d-163">MFCMAPI uses the **IMAPITable::SeekRow** method to locate the beginning of the table before processing.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ec41d-164">Confira também</span><span class="sxs-lookup"><span data-stu-id="ec41d-164">See also</span></span>



[<span data-ttu-id="ec41d-165">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="ec41d-165">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="ec41d-166">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="ec41d-166">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
  
[<span data-ttu-id="ec41d-167">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="ec41d-167">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="ec41d-168">IMAPITable::SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="ec41d-168">IMAPITable::SeekRowApprox</span></span>](imapitable-seekrowapprox.md)
  
[<span data-ttu-id="ec41d-169">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ec41d-169">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="ec41d-170">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="ec41d-170">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

