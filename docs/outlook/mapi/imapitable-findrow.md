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
ms.openlocfilehash: 2a50a5f536e337e5ca37e61f17d4dfd40aa9c51e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565330"
---
# <a name="imapitablefindrow"></a><span data-ttu-id="194d3-103">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="194d3-103">IMAPITable::FindRow</span></span>

  
  
<span data-ttu-id="194d3-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="194d3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="194d3-105">Localiza a próxima linha em uma tabela que corresponde a determinados critérios de pesquisa e move o cursor para essa linha.</span><span class="sxs-lookup"><span data-stu-id="194d3-105">Finds the next row in a table that matches specific search criteria and moves the cursor to that row.</span></span>
  
```cpp
HRESULT FindRow(
LPSRestriction lpRestriction,
BOOKMARK BkOrigin,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="194d3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="194d3-106">Parameters</span></span>

 <span data-ttu-id="194d3-107">_lpRestriction_</span><span class="sxs-lookup"><span data-stu-id="194d3-107">_lpRestriction_</span></span>
  
> <span data-ttu-id="194d3-108">[in] Um ponteiro para uma estrutura de [SRestriction](srestriction.md) que descreve os critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="194d3-108">[in] A pointer to an [SRestriction](srestriction.md) structure that describes the search criteria.</span></span> 
    
 <span data-ttu-id="194d3-109">_BkOrigin_</span><span class="sxs-lookup"><span data-stu-id="194d3-109">_BkOrigin_</span></span>
  
> <span data-ttu-id="194d3-110">[in] Um indicador que identifica a linha onde **FindRow** deve começar sua pesquisa.</span><span class="sxs-lookup"><span data-stu-id="194d3-110">[in] A bookmark identifying the row where **FindRow** should begin its search.</span></span> <span data-ttu-id="194d3-111">Um indicador pode ser criado usando o método [IMAPITable::CreateBookmark](imapitable-createbookmark.md) ou um dos seguintes valores predefinidos pode ser passado.</span><span class="sxs-lookup"><span data-stu-id="194d3-111">A bookmark can be created using the [IMAPITable::CreateBookmark](imapitable-createbookmark.md) method, or one of the following predefined values can be passed.</span></span> 
    
<span data-ttu-id="194d3-112">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="194d3-112">BOOKMARK_BEGINNING</span></span> 
  
> <span data-ttu-id="194d3-113">Pesquisas desde o início da tabela.</span><span class="sxs-lookup"><span data-stu-id="194d3-113">Searches from the beginning of the table.</span></span> 
    
<span data-ttu-id="194d3-114">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="194d3-114">BOOKMARK_CURRENT</span></span> 
  
> <span data-ttu-id="194d3-115">Pesquisas da linha da tabela onde o cursor está localizado.</span><span class="sxs-lookup"><span data-stu-id="194d3-115">Searches from the row in the table where the cursor is located.</span></span> 
    
<span data-ttu-id="194d3-116">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="194d3-116">BOOKMARK_END</span></span> 
  
> <span data-ttu-id="194d3-117">Pesquisas da extremidade da tabela.</span><span class="sxs-lookup"><span data-stu-id="194d3-117">Searches from the end of the table.</span></span> 
    
 <span data-ttu-id="194d3-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="194d3-118">_ulFlags_</span></span>
  
> <span data-ttu-id="194d3-119">[in] Uma bitmask dos sinalizadores que controla a direção da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="194d3-119">[in] A bitmask of flags that controls the direction of the search.</span></span> <span data-ttu-id="194d3-120">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="194d3-120">The following flag can be set:</span></span>
    
<span data-ttu-id="194d3-121">DIR_BACKWARD</span><span class="sxs-lookup"><span data-stu-id="194d3-121">DIR_BACKWARD</span></span> 
  
> <span data-ttu-id="194d3-122">Pesquisa para trás da linha identificada pelo indicador.</span><span class="sxs-lookup"><span data-stu-id="194d3-122">Searches backward from the row identified by the bookmark.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="194d3-123">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="194d3-123">Return value</span></span>

<span data-ttu-id="194d3-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="194d3-124">S_OK</span></span> 
  
> <span data-ttu-id="194d3-125">A operação de localização foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="194d3-125">The find operation was successful.</span></span>
    
<span data-ttu-id="194d3-126">MAPI_E_INVALID_BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="194d3-126">MAPI_E_INVALID_BOOKMARK</span></span> 
  
> <span data-ttu-id="194d3-127">O indicador no parâmetro _BkOrigin_ é inválido porque ele foi removido ou está além da última linha solicitada.</span><span class="sxs-lookup"><span data-stu-id="194d3-127">The bookmark in the  _BkOrigin_ parameter is invalid because it has been removed or because it is beyond the last row requested.</span></span> 
    
<span data-ttu-id="194d3-128">E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="194d3-128">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="194d3-129">Nenhuma linha foram encontrada que correspondem a restrição.</span><span class="sxs-lookup"><span data-stu-id="194d3-129">No rows were found that matched the restriction.</span></span>
    
<span data-ttu-id="194d3-130">MAPI_W_POSITION_CHANGED</span><span class="sxs-lookup"><span data-stu-id="194d3-130">MAPI_W_POSITION_CHANGED</span></span>
  
> <span data-ttu-id="194d3-131">A chamada foi bem-sucedida, mas o indicador usado na operação não é mais é definido na mesma linha que quando ele foi usado por último; Se o indicador não tiver sido usado, ele não está mais na mesma posição quando ele foi criado.</span><span class="sxs-lookup"><span data-stu-id="194d3-131">The call succeeded, but the bookmark used in the operation is no longer set at the same row as when it was last used; if the bookmark has not been used, it is no longer in the same position as when it was created.</span></span> <span data-ttu-id="194d3-132">Quando esse aviso é retornado, a chamada deve ser manipulada com êxito.</span><span class="sxs-lookup"><span data-stu-id="194d3-132">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="194d3-133">Para testar esse aviso, use a macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="194d3-133">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="194d3-134">Consulte [usando Macros para tratamento de erros](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="194d3-134">See [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="194d3-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="194d3-135">Remarks</span></span>

<span data-ttu-id="194d3-136">O método **IMAPITable:: FindRow** localiza a primeira linha da tabela para coincidir com um conjunto de critérios de pesquisa descrito na estrutura **SRestriction** apontada pelo parâmetro _lpRestriction_ .</span><span class="sxs-lookup"><span data-stu-id="194d3-136">The **IMAPITable::FindRow** method locates the first row in the table to match a set of search criteria described in the **SRestriction** structure pointed to by the  _lpRestriction_ parameter.</span></span> 
  
<span data-ttu-id="194d3-137">Geralmente, **FindRow** pesquisa frente do indicador especificado.</span><span class="sxs-lookup"><span data-stu-id="194d3-137">Usually, **FindRow** searches forward from the specified bookmark.</span></span> <span data-ttu-id="194d3-138">O chamador pode definir a pesquisa Retroceder do indicador, definindo o sinalizador DIR_BACKWARD no parâmetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="194d3-138">The caller can set the search to move backward from the bookmark by setting the DIR_BACKWARD flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="194d3-139">Encaminhar a pesquisa começa a partir do indicador atual; Pesquisar para trás começa a partir da linha antes do indicador.</span><span class="sxs-lookup"><span data-stu-id="194d3-139">Searching forward starts from the current bookmark; searching backward starts from the row prior to the bookmark.</span></span> <span data-ttu-id="194d3-140">A posição final da pesquisa é pouco antes da primeira linha encontrada que satisfeito a restrição.</span><span class="sxs-lookup"><span data-stu-id="194d3-140">The end position of the search is just before the first row found that satisfied the restriction.</span></span> 
  
<span data-ttu-id="194d3-141">Se a linha apontada pelo indicador no parâmetro _BkOrigin_ não existe mais na tabela e a tabela não é possível estabelecer uma nova posição para o indicador, **FindRow** retorna MAPI_E_INVALID_BOOKMARK.</span><span class="sxs-lookup"><span data-stu-id="194d3-141">If the row pointed to by the bookmark in the  _BkOrigin_ parameter no longer exists in the table and the table cannot establish a new position for the bookmark, **FindRow** returns MAPI_E_INVALID_BOOKMARK.</span></span> <span data-ttu-id="194d3-142">Se a linha apontada pela _BkOrigin_ não existe mais e a tabela é capaz de estabelecer uma nova posição para o indicador, **FindRow** retorna MAPI_W_POSITION_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="194d3-142">If the row pointed to by  _BkOrigin_ no longer exists and the table is able to establish a new position for the bookmark, **FindRow** returns MAPI_W_POSITION_CHANGED.</span></span> 
  
<span data-ttu-id="194d3-143">Se o indicador passado em _BkOrigin_ for BOOKMARK_BEGINNING ou BOOKMARK_END, **FindRow** retorna E_NOT_FOUND se sem linha correspondente for encontrada.</span><span class="sxs-lookup"><span data-stu-id="194d3-143">If the bookmark passed in  _BkOrigin_ is either BOOKMARK_BEGINNING or BOOKMARK_END, **FindRow** returns MAPI_E_NOT_FOUND if no matching row is found.</span></span> <span data-ttu-id="194d3-144">Se o indicador usado em _BkOrigin_ for BOOKMARK_CURRENT, **FindRow** pode retornar MAPI_W_POSITION_CHANGED, mas não MAPI_E_INVALID_BOOKMARK porque não há sempre uma posição atual do cursor.</span><span class="sxs-lookup"><span data-stu-id="194d3-144">If the bookmark used in  _BkOrigin_ is BOOKMARK_CURRENT, **FindRow** can return MAPI_W_POSITION_CHANGED but not MAPI_E_INVALID_BOOKMARK because there is always a current cursor position.</span></span> 
  
<span data-ttu-id="194d3-145">A coluna de propriedade **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) é necessária para todas as tabelas e todas as implementações de **FindRow** são necessárias para dar suporte a chamadas que buscam uma linha com base em PR_INSTANCE_KEY.</span><span class="sxs-lookup"><span data-stu-id="194d3-145">The **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property column is required for all tables, and all implementations of **FindRow** are required to support calls seeking a row based on PR_INSTANCE_KEY.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="194d3-146">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="194d3-146">Notes to implementers</span></span>

<span data-ttu-id="194d3-147">O tipo de prefixo pesquisando executadas pelos **FindRow** só é útil quando a pesquisa segue a mesma direção da organização da tabela.</span><span class="sxs-lookup"><span data-stu-id="194d3-147">The type of prefix searching performed by **FindRow** is only useful when the search follows the same direction as the table organization.</span></span> <span data-ttu-id="194d3-148">Para atingir o comportamento necessário, a função de comparação implicada **RELOP_GE** passado na estrutura de restrição de propriedade deve ser a mesma função de comparação em que baseia-se a ordem de classificação de tabela.</span><span class="sxs-lookup"><span data-stu-id="194d3-148">In order to achieve the required behavior, the comparison function implied by the **RELOP_GE** passed in the property restriction structure should be the same comparison function on which the table sort order is based.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="194d3-149">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="194d3-149">Notes to callers</span></span>

<span data-ttu-id="194d3-150">Você pode usar **FindRow** para suporte a rolagem com base em cadeias de caracteres digitadas pelo usuário, especialmente nas caixas de listagem em caixas de diálogo de endereço.</span><span class="sxs-lookup"><span data-stu-id="194d3-150">You can use **FindRow** to support scrolling based on strings typed in by the user, especially in list boxes within address dialog boxes.</span></span> <span data-ttu-id="194d3-151">Nesse tipo de rolagem, os usuários insiram prefixos progressivamente mais de um valor de cadeia de caracteres desejado e você pode emitir periodicamente uma chamada **FindRow** saltar à primeira linha que corresponde ao prefixo.</span><span class="sxs-lookup"><span data-stu-id="194d3-151">In this type of scrolling, users enter progressively longer prefixes of a desired string value, and you can periodically issue a **FindRow** call to jump to the first row that matches the prefix.</span></span> <span data-ttu-id="194d3-152">Direção saltos do cursor depende de qual direção a pesquisa é definido para ser executado.</span><span class="sxs-lookup"><span data-stu-id="194d3-152">Which direction the cursor jumps depends on which direction the search is set to run.</span></span> 
  
<span data-ttu-id="194d3-153">Para usar **FindRow**, um indicador deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="194d3-153">To use **FindRow**, a bookmark must be set.</span></span> <span data-ttu-id="194d3-154">A pesquisa de cadeia de caracteres pode ser originado de qualquer indicador, inclusive os indicadores predefinidos, que indica a posição atual e o início e fim da tabela.</span><span class="sxs-lookup"><span data-stu-id="194d3-154">The string search can originate from any bookmark, including from the preset bookmarks indicating the current position and the beginning and end of the table.</span></span> <span data-ttu-id="194d3-155">Se houver um grande número de linhas da tabela, a operação de pesquisa pode ser lenta.</span><span class="sxs-lookup"><span data-stu-id="194d3-155">If there are a large number of rows in the table, the search operation can be slow.</span></span>
  
<span data-ttu-id="194d3-156">Use uma restrição para encontrar um prefixo de cadeia de caracteres para a rolagem da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="194d3-156">Use a restriction to find a string prefix for scrolling as follows.</span></span> <span data-ttu-id="194d3-157">Para encaminhar a pesquisa em uma coluna classificada em ordem crescente e para a pesquisa para trás em uma coluna classificada em ordem decrescente, passe uma estrutura de restrição de propriedade no parâmetro _lpRestriction_ com relação a **RELOP_GE** e apropriada marca de propriedade e prefixo, usando o formato _tag_ **GE** _prefixo_.</span><span class="sxs-lookup"><span data-stu-id="194d3-157">For forward searching on a column sorted in ascending order and for backward searching on a column sorted in descending order, pass a property restriction structure in the  _lpRestriction_ parameter with the relation **RELOP_GE** and the appropriate property tag and prefix, using the format  _tag_ **GE** _prefix_.</span></span> 
  
<span data-ttu-id="194d3-158">Para obter mais informações sobre como usar as estruturas de restrição para especificar um filtro, consulte [Sobre restrições](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="194d3-158">For more information about using restriction structures to specify a filter, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="194d3-159">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="194d3-159">MFCMAPI reference</span></span>

<span data-ttu-id="194d3-160">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="194d3-160">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="194d3-161">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="194d3-161">**File**</span></span>|<span data-ttu-id="194d3-162">**Function**</span><span class="sxs-lookup"><span data-stu-id="194d3-162">**Function**</span></span>|<span data-ttu-id="194d3-163">**Comment**</span><span class="sxs-lookup"><span data-stu-id="194d3-163">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="194d3-164">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="194d3-164">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="194d3-165">DwThreadFuncLoadTable</span><span class="sxs-lookup"><span data-stu-id="194d3-165">DwThreadFuncLoadTable</span></span>  <br/> |<span data-ttu-id="194d3-166">MFCMAPI usa o método **IMAPITable:: FindRow** para localizar linhas que correspondam a uma restrição.</span><span class="sxs-lookup"><span data-stu-id="194d3-166">MFCMAPI uses the **IMAPITable::FindRow** method to find rows which match a restriction.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="194d3-167">Confira também</span><span class="sxs-lookup"><span data-stu-id="194d3-167">See also</span></span>



[<span data-ttu-id="194d3-168">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="194d3-168">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="194d3-169">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="194d3-169">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="194d3-170">SRestriction</span><span class="sxs-lookup"><span data-stu-id="194d3-170">SRestriction</span></span>](srestriction.md)
  
[<span data-ttu-id="194d3-171">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="194d3-171">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="194d3-172">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="194d3-172">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

