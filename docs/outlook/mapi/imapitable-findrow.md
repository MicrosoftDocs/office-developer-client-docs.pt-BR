---
title: IMAPITableFindRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.FindRow
api_type:
- COM
ms.assetid: 6511368c-9777-497e-9eea-cf390c04b92e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a5364af229721d101f38d2f054f528169b48c09e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429569"
---
# <a name="imapitablefindrow"></a><span data-ttu-id="5b075-103">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="5b075-103">IMAPITable::FindRow</span></span>

  
  
<span data-ttu-id="5b075-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5b075-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5b075-105">Localiza a próxima linha em uma tabela que corresponde a critérios de pesquisa específicos e move o cursor para essa linha.</span><span class="sxs-lookup"><span data-stu-id="5b075-105">Finds the next row in a table that matches specific search criteria and moves the cursor to that row.</span></span>
  
```cpp
HRESULT FindRow(
LPSRestriction lpRestriction,
BOOKMARK BkOrigin,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="5b075-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5b075-106">Parameters</span></span>

 <span data-ttu-id="5b075-107">_lpRestriction_</span><span class="sxs-lookup"><span data-stu-id="5b075-107">_lpRestriction_</span></span>
  
> <span data-ttu-id="5b075-108">no Um ponteiro para uma estrutura [SRestriction](srestriction.md) que descreve os critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="5b075-108">[in] A pointer to an [SRestriction](srestriction.md) structure that describes the search criteria.</span></span> 
    
 <span data-ttu-id="5b075-109">_BkOrigin_</span><span class="sxs-lookup"><span data-stu-id="5b075-109">_BkOrigin_</span></span>
  
> <span data-ttu-id="5b075-110">no Um indicador identificando a linha onde o **FindRow** deve começar sua pesquisa.</span><span class="sxs-lookup"><span data-stu-id="5b075-110">[in] A bookmark identifying the row where **FindRow** should begin its search.</span></span> <span data-ttu-id="5b075-111">Um indicador pode ser criado usando o método imApitable [:: CreateBookmark](imapitable-createbookmark.md) ou um dos seguintes valores predefinidos pode ser passado.</span><span class="sxs-lookup"><span data-stu-id="5b075-111">A bookmark can be created using the [IMAPITable::CreateBookmark](imapitable-createbookmark.md) method, or one of the following predefined values can be passed.</span></span> 
    
<span data-ttu-id="5b075-112">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="5b075-112">BOOKMARK_BEGINNING</span></span> 
  
> <span data-ttu-id="5b075-113">Pesquisa a partir do início da tabela.</span><span class="sxs-lookup"><span data-stu-id="5b075-113">Searches from the beginning of the table.</span></span> 
    
<span data-ttu-id="5b075-114">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="5b075-114">BOOKMARK_CURRENT</span></span> 
  
> <span data-ttu-id="5b075-115">Pesquisa a partir da linha na tabela onde o cursor está localizado.</span><span class="sxs-lookup"><span data-stu-id="5b075-115">Searches from the row in the table where the cursor is located.</span></span> 
    
<span data-ttu-id="5b075-116">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="5b075-116">BOOKMARK_END</span></span> 
  
> <span data-ttu-id="5b075-117">Pesquisa a partir do final da tabela.</span><span class="sxs-lookup"><span data-stu-id="5b075-117">Searches from the end of the table.</span></span> 
    
 <span data-ttu-id="5b075-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5b075-118">_ulFlags_</span></span>
  
> <span data-ttu-id="5b075-119">no Uma bitmask de sinalizadores que controlam a direção da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="5b075-119">[in] A bitmask of flags that controls the direction of the search.</span></span> <span data-ttu-id="5b075-120">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="5b075-120">The following flag can be set:</span></span>
    
<span data-ttu-id="5b075-121">DIR_BACKWARD</span><span class="sxs-lookup"><span data-stu-id="5b075-121">DIR_BACKWARD</span></span> 
  
> <span data-ttu-id="5b075-122">Pesquisa retroativa a partir da linha identificada pelo indicador.</span><span class="sxs-lookup"><span data-stu-id="5b075-122">Searches backward from the row identified by the bookmark.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5b075-123">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="5b075-123">Return value</span></span>

<span data-ttu-id="5b075-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="5b075-124">S_OK</span></span> 
  
> <span data-ttu-id="5b075-125">A operação de localização foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="5b075-125">The find operation was successful.</span></span>
    
<span data-ttu-id="5b075-126">MAPI_E_INVALID_BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="5b075-126">MAPI_E_INVALID_BOOKMARK</span></span> 
  
> <span data-ttu-id="5b075-127">O indicador no parâmetro _BkOrigin_ é inválido porque foi removido ou porque está além da última linha solicitada.</span><span class="sxs-lookup"><span data-stu-id="5b075-127">The bookmark in the  _BkOrigin_ parameter is invalid because it has been removed or because it is beyond the last row requested.</span></span> 
    
<span data-ttu-id="5b075-128">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="5b075-128">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="5b075-129">Nenhuma linha que correspondeu à restrição foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="5b075-129">No rows were found that matched the restriction.</span></span>
    
<span data-ttu-id="5b075-130">MAPI_W_POSITION_CHANGED</span><span class="sxs-lookup"><span data-stu-id="5b075-130">MAPI_W_POSITION_CHANGED</span></span>
  
> <span data-ttu-id="5b075-131">A chamada foi bem-sucedida, mas o indicador usado na operação não é mais definido na mesma linha que o quando foi usado pela última vez; Se o indicador não tiver sido usado, ele não estará mais na mesma posição de quando foi criado.</span><span class="sxs-lookup"><span data-stu-id="5b075-131">The call succeeded, but the bookmark used in the operation is no longer set at the same row as when it was last used; if the bookmark has not been used, it is no longer in the same position as when it was created.</span></span> <span data-ttu-id="5b075-132">Quando esse aviso é retornado, a chamada deve ser tratada como bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="5b075-132">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="5b075-133">Para testar esse aviso, use a macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="5b075-133">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="5b075-134">Consulte [usando macros para tratamento de erros](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="5b075-134">See [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5b075-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="5b075-135">Remarks</span></span>

<span data-ttu-id="5b075-136">O método imApitable **:: FindRow** localiza a primeira linha na tabela para corresponder a um conjunto de critérios de pesquisa descritos na estrutura **SRestriction** apontada pelo parâmetro _lpRestriction_ .</span><span class="sxs-lookup"><span data-stu-id="5b075-136">The **IMAPITable::FindRow** method locates the first row in the table to match a set of search criteria described in the **SRestriction** structure pointed to by the  _lpRestriction_ parameter.</span></span> 
  
<span data-ttu-id="5b075-137">Normalmente, as pesquisas de **FindRow** são revertidas a partir do indicador especificado.</span><span class="sxs-lookup"><span data-stu-id="5b075-137">Usually, **FindRow** searches forward from the specified bookmark.</span></span> <span data-ttu-id="5b075-138">O chamador pode definir a pesquisa para mover para trás do indicador definindo o sinalizador DIR_BACKWARD no parâmetro _parâmetroulflags_ .</span><span class="sxs-lookup"><span data-stu-id="5b075-138">The caller can set the search to move backward from the bookmark by setting the DIR_BACKWARD flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="5b075-139">A pesquisa antecipada começa no indicador atual; a pesquisa de versões anteriores começa da linha anterior ao indicador.</span><span class="sxs-lookup"><span data-stu-id="5b075-139">Searching forward starts from the current bookmark; searching backward starts from the row prior to the bookmark.</span></span> <span data-ttu-id="5b075-140">A posição final da pesquisa é anterior à primeira linha encontrada e satisfeita na restrição.</span><span class="sxs-lookup"><span data-stu-id="5b075-140">The end position of the search is just before the first row found that satisfied the restriction.</span></span> 
  
<span data-ttu-id="5b075-141">Se a linha indicada pelo indicador no parâmetro _BkOrigin_ não existir mais na tabela e a tabela não puder estabelecer uma nova posição para o indicador, **FindRow** retornará MAPI_E_INVALID_BOOKMARK.</span><span class="sxs-lookup"><span data-stu-id="5b075-141">If the row pointed to by the bookmark in the  _BkOrigin_ parameter no longer exists in the table and the table cannot establish a new position for the bookmark, **FindRow** returns MAPI_E_INVALID_BOOKMARK.</span></span> <span data-ttu-id="5b075-142">Se a linha indicada por _BkOrigin_ não existir mais e a tabela puder estabelecer uma nova posição para o indicador, **FindRow** retornará MAPI_W_POSITION_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="5b075-142">If the row pointed to by  _BkOrigin_ no longer exists and the table is able to establish a new position for the bookmark, **FindRow** returns MAPI_W_POSITION_CHANGED.</span></span> 
  
<span data-ttu-id="5b075-143">Se o indicador passado no _BkOrigin_ for BOOKMARK_BEGINNING ou BOOKMARK_END, **FindRow** retornará MAPI_E_NOT_FOUND se nenhuma linha correspondente for encontrada.</span><span class="sxs-lookup"><span data-stu-id="5b075-143">If the bookmark passed in  _BkOrigin_ is either BOOKMARK_BEGINNING or BOOKMARK_END, **FindRow** returns MAPI_E_NOT_FOUND if no matching row is found.</span></span> <span data-ttu-id="5b075-144">Se o indicador usado no _BkOrigin_ for BOOKMARK_CURRENT, **FINDROW** poderá retornar MAPI_W_POSITION_CHANGED, mas não MAPI_E_INVALID_BOOKMARK, porque sempre há uma posição de cursor atual.</span><span class="sxs-lookup"><span data-stu-id="5b075-144">If the bookmark used in  _BkOrigin_ is BOOKMARK_CURRENT, **FindRow** can return MAPI_W_POSITION_CHANGED but not MAPI_E_INVALID_BOOKMARK because there is always a current cursor position.</span></span> 
  
<span data-ttu-id="5b075-145">A coluna da propriedade **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) é necessária para todas as tabelas, e todas as implementações de **FindRow** são necessárias para dar suporte a chamadas que buscam uma linha com base no PR_INSTANCE_KEY.</span><span class="sxs-lookup"><span data-stu-id="5b075-145">The **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property column is required for all tables, and all implementations of **FindRow** are required to support calls seeking a row based on PR_INSTANCE_KEY.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="5b075-146">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="5b075-146">Notes to implementers</span></span>

<span data-ttu-id="5b075-147">O tipo de pesquisa de prefixo realizado pelo **FindRow** só é útil quando a pesquisa segue a mesma direção da organização da tabela.</span><span class="sxs-lookup"><span data-stu-id="5b075-147">The type of prefix searching performed by **FindRow** is only useful when the search follows the same direction as the table organization.</span></span> <span data-ttu-id="5b075-148">Para obter o comportamento necessário, a função de comparação inferida pelo **RELOP_GE** passado na estrutura de restrição de propriedade deve ser a mesma função de comparação na qual a ordem de classificação da tabela se baseia.</span><span class="sxs-lookup"><span data-stu-id="5b075-148">In order to achieve the required behavior, the comparison function implied by the **RELOP_GE** passed in the property restriction structure should be the same comparison function on which the table sort order is based.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="5b075-149">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="5b075-149">Notes to callers</span></span>

<span data-ttu-id="5b075-150">Você pode usar o **FindRow** para dar suporte à rolagem com base em cadeias de caracteres digitadas pelo usuário, especialmente nas caixas de listagem nas caixas de diálogo de endereço.</span><span class="sxs-lookup"><span data-stu-id="5b075-150">You can use **FindRow** to support scrolling based on strings typed in by the user, especially in list boxes within address dialog boxes.</span></span> <span data-ttu-id="5b075-151">Nesse tipo de rolagem, os usuários inserem prefixos cada vez mais longos de um valor de cadeia de caracteres desejado e você pode emitir periodicamente uma chamada **FindRow** para saltar para a primeira linha que corresponde ao prefixo.</span><span class="sxs-lookup"><span data-stu-id="5b075-151">In this type of scrolling, users enter progressively longer prefixes of a desired string value, and you can periodically issue a **FindRow** call to jump to the first row that matches the prefix.</span></span> <span data-ttu-id="5b075-152">Qual direção o cursor salta depende da direção em que a pesquisa está definida para executar.</span><span class="sxs-lookup"><span data-stu-id="5b075-152">Which direction the cursor jumps depends on which direction the search is set to run.</span></span> 
  
<span data-ttu-id="5b075-153">Para usar **FindRow**, um indicador deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="5b075-153">To use **FindRow**, a bookmark must be set.</span></span> <span data-ttu-id="5b075-154">A pesquisa de cadeia de caracteres pode ser originada de qualquer indicador, incluindo os indicadores predefinidos que indicam a posição atual e o início e o fim da tabela.</span><span class="sxs-lookup"><span data-stu-id="5b075-154">The string search can originate from any bookmark, including from the preset bookmarks indicating the current position and the beginning and end of the table.</span></span> <span data-ttu-id="5b075-155">Se houver um grande número de linhas na tabela, a operação de pesquisa poderá ser lenta.</span><span class="sxs-lookup"><span data-stu-id="5b075-155">If there are a large number of rows in the table, the search operation can be slow.</span></span>
  
<span data-ttu-id="5b075-156">Use uma restrição para localizar um prefixo de cadeia de caracteres para a rolagem da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="5b075-156">Use a restriction to find a string prefix for scrolling as follows.</span></span> <span data-ttu-id="5b075-157">Para encaminhar a pesquisa em uma coluna classificada em ordem crescente e para pesquisa retroativa em uma coluna classificada em ordem decrescente, passe uma estrutura de restrição de propriedade no parâmetro _lpRestriction_ com a relação **RELOP_GE** e as marca de propriedade e prefixo, usando o __ \*\*\*\* _prefixo_GE da marca de formatação.</span><span class="sxs-lookup"><span data-stu-id="5b075-157">For forward searching on a column sorted in ascending order and for backward searching on a column sorted in descending order, pass a property restriction structure in the  _lpRestriction_ parameter with the relation **RELOP_GE** and the appropriate property tag and prefix, using the format  _tag_ **GE** _prefix_.</span></span> 
  
<span data-ttu-id="5b075-158">Para obter mais informações sobre como usar estruturas de restrição para especificar um filtro, consulte [about Restrictions](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="5b075-158">For more information about using restriction structures to specify a filter, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5b075-159">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="5b075-159">MFCMAPI reference</span></span>

<span data-ttu-id="5b075-160">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="5b075-160">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5b075-161">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="5b075-161">**File**</span></span>|<span data-ttu-id="5b075-162">**Função**</span><span class="sxs-lookup"><span data-stu-id="5b075-162">**Function**</span></span>|<span data-ttu-id="5b075-163">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="5b075-163">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5b075-164">ContentsTableListCtrl. cpp</span><span class="sxs-lookup"><span data-stu-id="5b075-164">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="5b075-165">DwThreadFuncLoadTable</span><span class="sxs-lookup"><span data-stu-id="5b075-165">DwThreadFuncLoadTable</span></span>  <br/> |<span data-ttu-id="5b075-166">MFCMAPI usa o método imApitable **:: FindRow** para localizar linhas que correspondem a uma restrição.</span><span class="sxs-lookup"><span data-stu-id="5b075-166">MFCMAPI uses the **IMAPITable::FindRow** method to find rows which match a restriction.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5b075-167">Confira também</span><span class="sxs-lookup"><span data-stu-id="5b075-167">See also</span></span>



[<span data-ttu-id="5b075-168">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="5b075-168">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="5b075-169">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="5b075-169">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="5b075-170">SRestriction</span><span class="sxs-lookup"><span data-stu-id="5b075-170">SRestriction</span></span>](srestriction.md)
  
[<span data-ttu-id="5b075-171">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5b075-171">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="5b075-172">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="5b075-172">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

