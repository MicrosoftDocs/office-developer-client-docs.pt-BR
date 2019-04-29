---
title: IMAPIPropGetNamesFromIDs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetNamesFromIDs
api_type:
- COM
ms.assetid: 3efa4731-cf32-4a6c-9ba8-d059e58b0d98
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f6688afde9b36a7722eaaf768f091481c15b7308
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423570"
---
# <a name="imapipropgetnamesfromids"></a><span data-ttu-id="929f1-103">IMAPIProp::GetNamesFromIDs</span><span class="sxs-lookup"><span data-stu-id="929f1-103">IMAPIProp::GetNamesFromIDs</span></span>

  
  
<span data-ttu-id="929f1-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="929f1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="929f1-105">Fornece os nomes de propriedade que correspondem a um ou mais identificadores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="929f1-105">Provides the property names that correspond to one or more property identifiers.</span></span>
  
```cpp
HRESULT GetNamesFromIDs(
  LPSPropTagArray FAR * lppPropTags,
  LPGUID lpPropSetGuid,
  ULONG ulFlags,
  ULONG FAR * lpcPropNames,
  LPMAPINAMEID FAR * FAR * lpppPropNames
);
```

## <a name="parameters"></a><span data-ttu-id="929f1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="929f1-106">Parameters</span></span>

 <span data-ttu-id="929f1-107">_lppPropTags_</span><span class="sxs-lookup"><span data-stu-id="929f1-107">_lppPropTags_</span></span>
  
> <span data-ttu-id="929f1-108">[in, out] Na entrada, um ponteiro para uma estrutura [SPropTagArray](sproptagarray.md) que contém uma matriz de marcas de propriedade; caso contrário, NULL, indicando que todos os nomes devem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="929f1-108">[in, out] On input, a pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags; otherwise, NULL, indicating that all names should be returned.</span></span> <span data-ttu-id="929f1-109">O membro **cValues** da matriz de marca de propriedade não pode ser 0.</span><span class="sxs-lookup"><span data-stu-id="929f1-109">The **cValues** member for the property tag array cannot be 0.</span></span> <span data-ttu-id="929f1-110">Se _lppPropTags_ for um ponteiro válido na entrada, **GetNamesFromIDs** retornará nomes para cada identificador de propriedade incluído na matriz.</span><span class="sxs-lookup"><span data-stu-id="929f1-110">If  _lppPropTags_ is a valid pointer on input, **GetNamesFromIDs** returns names for each property identifier included in the array.</span></span> 
    
 <span data-ttu-id="929f1-111">_lpPropSetGuid_</span><span class="sxs-lookup"><span data-stu-id="929f1-111">_lpPropSetGuid_</span></span>
  
> <span data-ttu-id="929f1-112">no Um ponteiro para um GUID ou uma estrutura [GUID](guid.md) , que identifica um conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="929f1-112">[in] A pointer to a GUID, or [GUID](guid.md) structure, that identifies a property set.</span></span> <span data-ttu-id="929f1-113">O parâmetro _lpPropSetGuid_ pode apontar para um conjunto de propriedades válido ou pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="929f1-113">The  _lpPropSetGuid_ parameter can point to a valid property set or can be NULL.</span></span> 
    
 <span data-ttu-id="929f1-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="929f1-114">_ulFlags_</span></span>
  
> <span data-ttu-id="929f1-115">no Uma bitmask de sinalizadores que indica o tipo de nome a ser retornado.</span><span class="sxs-lookup"><span data-stu-id="929f1-115">[in] A bitmask of flags that indicates the type of names to be returned.</span></span> <span data-ttu-id="929f1-116">Os seguintes sinalizadores podem ser usados (se ambos os sinalizadores estiverem definidos, nenhum nome será retornado):</span><span class="sxs-lookup"><span data-stu-id="929f1-116">The following flags can be used (if both flags are set, no names will be returned):</span></span>
    
<span data-ttu-id="929f1-117">MAPI_NO_IDS</span><span class="sxs-lookup"><span data-stu-id="929f1-117">MAPI_NO_IDS</span></span> 
  
> <span data-ttu-id="929f1-118">As solicitações que apenas os nomes armazenados como cadeias de caracteres Unicode serão retornadas.</span><span class="sxs-lookup"><span data-stu-id="929f1-118">Requests that only names stored as Unicode strings be returned.</span></span> 
    
<span data-ttu-id="929f1-119">MAPI_NO_STRINGS</span><span class="sxs-lookup"><span data-stu-id="929f1-119">MAPI_NO_STRINGS</span></span> 
  
> <span data-ttu-id="929f1-120">As solicitações que apenas os nomes armazenados como identificadores numéricos serão retornadas.</span><span class="sxs-lookup"><span data-stu-id="929f1-120">Requests that only names stored as numeric identifiers be returned.</span></span> 
    
 <span data-ttu-id="929f1-121">_lpcPropNames_</span><span class="sxs-lookup"><span data-stu-id="929f1-121">_lpcPropNames_</span></span>
  
> <span data-ttu-id="929f1-122">bota Um ponteiro para uma contagem dos ponteiros de nome da propriedade na matriz apontada pelo parâmetro _lppPropNames_ .</span><span class="sxs-lookup"><span data-stu-id="929f1-122">[out] A pointer to a count of the property name pointers in the array pointed to by the  _lppPropNames_ parameter.</span></span> 
    
 <span data-ttu-id="929f1-123">_lpppPropNames_</span><span class="sxs-lookup"><span data-stu-id="929f1-123">_lpppPropNames_</span></span>
  
> <span data-ttu-id="929f1-124">bota Um ponteiro para uma matriz de ponteiros para estruturas [MAPINAMEID](mapinameid.md) que contêm nomes de propriedade.</span><span class="sxs-lookup"><span data-stu-id="929f1-124">[out] A pointer to an array of pointers to [MAPINAMEID](mapinameid.md) structures that contains property names.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="929f1-125">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="929f1-125">Return value</span></span>

<span data-ttu-id="929f1-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="929f1-126">S_OK</span></span> 
  
> <span data-ttu-id="929f1-127">Os nomes das propriedades foram retornados com êxito.</span><span class="sxs-lookup"><span data-stu-id="929f1-127">The property names were successfully returned.</span></span> 
    
<span data-ttu-id="929f1-128">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="929f1-128">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="929f1-129">O objeto não dá suporte a propriedades nomeadas.</span><span class="sxs-lookup"><span data-stu-id="929f1-129">The object does not support named properties.</span></span> 
    
<span data-ttu-id="929f1-130">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="929f1-130">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="929f1-131">A chamada foi concluída com êxito, mas não foi possível retornar os nomes de uma ou mais propriedades.</span><span class="sxs-lookup"><span data-stu-id="929f1-131">The call succeeded overall, but names for one or more properties could not be returned.</span></span> <span data-ttu-id="929f1-132">As marcas de propriedade para as propriedades com falha têm um tipo de propriedade de **PT_ERROR**.</span><span class="sxs-lookup"><span data-stu-id="929f1-132">The property tags for the failing properties have a property type of **PT_ERROR**.</span></span> <span data-ttu-id="929f1-133">Quando esse aviso é retornado, a chamada deve ser tratada como bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="929f1-133">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="929f1-134">Para testar esse aviso, use a macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="929f1-134">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="929f1-135">Para obter mais informações, consulte [usando macros para tratamento de erros](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="929f1-135">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span> 
    
<span data-ttu-id="929f1-136">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="929f1-136">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="929f1-137">O membro **cValues** de uma ou mais das entradas na matriz de marca de propriedade apontada por _lppPropTags_ está definida como 0.</span><span class="sxs-lookup"><span data-stu-id="929f1-137">The **cValues** member of one or more of the entries in the property tag array pointed to by  _lppPropTags_ is set to 0.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="929f1-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="929f1-138">Remarks</span></span>

<span data-ttu-id="929f1-139">Embora o acesso à maioria das propriedades seja pelo identificador de propriedade, algumas propriedades podem ser acessadas pelo nome.</span><span class="sxs-lookup"><span data-stu-id="929f1-139">While access to most properties is by property identifier, some properties can be accessed by name.</span></span> <span data-ttu-id="929f1-140">O método **IMAPIProp:: GetNamesFromIDs** pode ser chamado para fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="929f1-140">The **IMAPIProp::GetNamesFromIDs** method can be called to do the following:</span></span> 
  
- <span data-ttu-id="929f1-141">Recuperar nomes de identificadores de propriedade específicos em um conjunto específico de propriedades.</span><span class="sxs-lookup"><span data-stu-id="929f1-141">Retrieve names for specific property identifiers in a specific property set.</span></span>
    
- <span data-ttu-id="929f1-142">Recupere nomes para identificadores de propriedade específicos em qualquer conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="929f1-142">Retrieve names for specific property identifiers in any property set.</span></span>
    
- <span data-ttu-id="929f1-143">Recuperar nomes de todas as propriedades nomeadas incluídas no mapeamento do objeto.</span><span class="sxs-lookup"><span data-stu-id="929f1-143">Retrieve names for all named properties that are included in the object's mapping.</span></span>
    
<span data-ttu-id="929f1-144">Se _lppPropTags_ apontar para uma matriz de marca de propriedade válida com um ou mais identificadores de propriedade e _lpPropSetGuid_ apontar para um conjunto de propriedades válido, **GetNamesFromIDs** ignorará o conjunto de propriedades e os tipos de propriedade e retornará todos os nomes que mapeiam para os identificadores especificados.</span><span class="sxs-lookup"><span data-stu-id="929f1-144">If  _lppPropTags_ points to a valid property tag array with one or more property identifiers, and  _lpPropSetGuid_ points to a valid property set, **GetNamesFromIDs** ignores the property set and the property types and returns all of the names that map to the specified identifiers.</span></span> 
  
<span data-ttu-id="929f1-145">Se _lppPropTags_ apontar para uma matriz de marca de propriedade válida com um ou mais identificadores de propriedade e _lpPropSetGuid_ for nulo, **GetNamesFromIDs** retornará todos os nomes que mapeiam para os identificadores especificados.</span><span class="sxs-lookup"><span data-stu-id="929f1-145">If  _lppPropTags_ points to a valid property tag array with one or more property identifiers and  _lpPropSetGuid_ is NULL, **GetNamesFromIDs** returns all of the names that map to the specified identifiers.</span></span> 
  
<span data-ttu-id="929f1-146">Se um identificador especificado não tiver um nome, **GetNamesFromIDs** retornará NULL no local desse identificador na estrutura retornada no _lpppPropNames_ e também retornará MAPI_W_ERRORS_RETURNED.</span><span class="sxs-lookup"><span data-stu-id="929f1-146">If a specified identifier does not have a name, **GetNamesFromIDs** returns NULL in that identifier's place in the structure returned in  _lpppPropNames_ and also returns MAPI_W_ERRORS_RETURNED.</span></span> 
  
<span data-ttu-id="929f1-147">Se _lpPropSetGuid_ e _lppPropTags_ forem nulos, **GetNamesFromIDs** aloca uma nova matriz de marca de propriedade e retorna todos os nomes de todas as propriedades nomeadas para o objeto.</span><span class="sxs-lookup"><span data-stu-id="929f1-147">If both  _lpPropSetGuid_ and  _lppPropTags_ are NULL, **GetNamesFromIDs** allocates a new property tag array and returns all of the names for all of the named properties for the object.</span></span> 
  
<span data-ttu-id="929f1-148">Quando não há nomes a serem retornados, talvez porque não há propriedades no conjunto de propriedades solicitadas ou todas as propriedades são de um tipo excluído pelos sinalizadores, **GetNamesFromIDs** faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="929f1-148">When there are no names to be returned, perhaps because there are no properties in the requested property set or all of the properties are of a type excluded by the flags, **GetNamesFromIDs** does the following:</span></span> 
  
- <span data-ttu-id="929f1-149">Retorna S_OK.</span><span class="sxs-lookup"><span data-stu-id="929f1-149">Returns S_OK.</span></span>
    
- <span data-ttu-id="929f1-150">Aloca uma nova estrutura **SPropTagArray** , definindo o membro **cValues** como 0.</span><span class="sxs-lookup"><span data-stu-id="929f1-150">Allocates a new **SPropTagArray** structure, setting the **cValues** member to 0.</span></span> 
    
- <span data-ttu-id="929f1-151">Define o conteúdo de _lpcPropNames_ como 0.</span><span class="sxs-lookup"><span data-stu-id="929f1-151">Sets the contents of  _lpcPropNames_ to 0.</span></span> 
    
- <span data-ttu-id="929f1-152">Define o conteúdo de _lpppPropNames_ como nulo.</span><span class="sxs-lookup"><span data-stu-id="929f1-152">Sets the contents of  _lpppPropNames_ to NULL.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="929f1-153">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="929f1-153">Notes to implementers</span></span>

<span data-ttu-id="929f1-154">Se _lpPropSetGuid_ apontar para um conjunto de propriedades válido e _lppPropTags_ for nulo, o resultado será indefinido.</span><span class="sxs-lookup"><span data-stu-id="929f1-154">If  _lpPropSetGuid_ points to a valid property set and  _lppPropTags_ is NULL, the result is undefined.</span></span> <span data-ttu-id="929f1-155">Você pode usar uma das seguintes estratégias:</span><span class="sxs-lookup"><span data-stu-id="929f1-155">You can use one of the following strategies:</span></span> 
  
- <span data-ttu-id="929f1-156">Ignore o conjunto de propriedades e retorne os nomes dos identificadores na matriz de marca de propriedade.</span><span class="sxs-lookup"><span data-stu-id="929f1-156">Ignore the property set and return the names for the identifiers in the property tag array.</span></span>
    
- <span data-ttu-id="929f1-157">ReTorne os nomes somente para os identificadores na matriz de marca de propriedade que pertencem ao conjunto de propriedades especificado.</span><span class="sxs-lookup"><span data-stu-id="929f1-157">Return the names for only the identifiers in the property tag array that belong to the specified property set.</span></span>
    
- <span data-ttu-id="929f1-158">Falha na chamada, retornando MAPI_E_INVALID_PARAMETER.</span><span class="sxs-lookup"><span data-stu-id="929f1-158">Fail the call, returning MAPI_E_INVALID_PARAMETER.</span></span> 
    
## <a name="notes-to-callers"></a><span data-ttu-id="929f1-159">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="929f1-159">Notes to callers</span></span>

<span data-ttu-id="929f1-160">Para recuperar todas as propriedades nomeadas de um objeto, primeiro você deve chamar o método [IMAPIProp::](imapiprop-getproplist.md) getproplist do objeto e, em seguida, passar os identificadores retornados que estão acima do intervalo da 0X8000 para **GetNamesFromIDs**.</span><span class="sxs-lookup"><span data-stu-id="929f1-160">To retrieve all of the named properties for an object, you must first call the object's [IMAPIProp::GetPropList](imapiprop-getproplist.md) method and then pass the returned identifiers that are above the 0x8000 range to **GetNamesFromIDs**.</span></span>
  
<span data-ttu-id="929f1-161">Se você passar um conjunto de propriedades válido, mas não uma matriz de marca de propriedade válida, esteja preparado para resultados imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="929f1-161">If you pass a valid property set but not a valid property tag array, be prepared for unpredictable results.</span></span> <span data-ttu-id="929f1-162">Algumas implementações de **GetNamesFromIDs** ignoram o conjunto de propriedades e retornam os nomes dos identificadores na matriz de marca de propriedade.</span><span class="sxs-lookup"><span data-stu-id="929f1-162">Some implementations of **GetNamesFromIDs** ignore the property set and return the names for the identifiers in the property tag array.</span></span> <span data-ttu-id="929f1-163">Algumas implementações retornam MAPI_E_INVALID_PARAMETER.</span><span class="sxs-lookup"><span data-stu-id="929f1-163">Some implementations return MAPI_E_INVALID_PARAMETER.</span></span> <span data-ttu-id="929f1-164">Ainda outras implementações retornam nomes para identificadores de todas as propriedades no conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="929f1-164">Still other implementations return names for identifiers of all properties in the property set.</span></span> <span data-ttu-id="929f1-165">Se o conjunto de Propriedades for PS_PUBLIC_STRINGS, **GetNamesFromIDs** poderá retornar todos os nomes que já foram criados.</span><span class="sxs-lookup"><span data-stu-id="929f1-165">If the property set is PS_PUBLIC_STRINGS, **GetNamesFromIDs** can return all names that were ever created.</span></span> <span data-ttu-id="929f1-166">Se o provedor de serviços armazena uma propriedade sob os identificadores associados com as cadeias de caracteres públicas é irrelevante.</span><span class="sxs-lookup"><span data-stu-id="929f1-166">Whether the service provider stores a property under the identifiers associated with the public strings is immaterial.</span></span> 
  
<span data-ttu-id="929f1-167">Quando você tiver concluído os nomes das propriedades, verifique o conteúdo do parâmetro _lpcPropNames_ para determinar se algum nome foi retornado.</span><span class="sxs-lookup"><span data-stu-id="929f1-167">When you are finished with the property names, check the contents of the  _lpcPropNames_ parameter to determine whether any names were returned.</span></span> <span data-ttu-id="929f1-168">Em caso afirmativo, chame a função [MAPIFreeBuffer](mapifreebuffer.md) para liberar a memória indicada por _lppPropTags_ e _lpppPropNames_ quando um resultado bem-sucedido é retornado.</span><span class="sxs-lookup"><span data-stu-id="929f1-168">If so, call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the memory pointed to by  _lppPropTags_ and  _lpppPropNames_ when a successful result is returned.</span></span> <span data-ttu-id="929f1-169">Uma chamada para **MAPIFreeBuffer** é suficiente para cada parâmetro; Você não precisa atravessar a matriz de ponteiros e liberar cada estrutura **MAPINAMEID** individualmente.</span><span class="sxs-lookup"><span data-stu-id="929f1-169">One call to **MAPIFreeBuffer** is sufficient for each parameter; you do not have to traverse the array of pointers and free each **MAPINAMEID** structure individually.</span></span> 
  
<span data-ttu-id="929f1-170">Para obter mais informações sobre propriedades nomeadas, consulte [MAPI Named Properties](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="929f1-170">For more information about named properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="929f1-171">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="929f1-171">MFCMAPI reference</span></span>

<span data-ttu-id="929f1-172">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="929f1-172">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="929f1-173">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="929f1-173">**File**</span></span>|<span data-ttu-id="929f1-174">**Função**</span><span class="sxs-lookup"><span data-stu-id="929f1-174">**Function**</span></span>|<span data-ttu-id="929f1-175">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="929f1-175">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="929f1-176">SingleMAPIPropListCtrl. cpp</span><span class="sxs-lookup"><span data-stu-id="929f1-176">SingleMAPIPropListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="929f1-177">CSingleMAPIPropListCtrl:: FindAllNamedProps</span><span class="sxs-lookup"><span data-stu-id="929f1-177">CSingleMAPIPropListCtrl::FindAllNamedProps</span></span>  <br/> |<span data-ttu-id="929f1-178">MFCMAPI usa o método **IMAPIProp:: GetNamesFromIDs** para pesquisar propriedades nomeadas que foram mapeadas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="929f1-178">MFCMAPI uses the **IMAPIProp::GetNamesFromIDs** method to look up named properties that have previously been mapped.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="929f1-179">Confira também</span><span class="sxs-lookup"><span data-stu-id="929f1-179">See also</span></span>



[<span data-ttu-id="929f1-180">GUID</span><span class="sxs-lookup"><span data-stu-id="929f1-180">GUID</span></span>](guid.md)
  
[<span data-ttu-id="929f1-181">IMAPIProp::GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="929f1-181">IMAPIProp::GetIDsFromNames</span></span>](imapiprop-getidsfromnames.md)
  
[<span data-ttu-id="929f1-182">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="929f1-182">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="929f1-183">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="929f1-183">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="929f1-184">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="929f1-184">MAPINAMEID</span></span>](mapinameid.md)
  
[<span data-ttu-id="929f1-185">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="929f1-185">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="929f1-186">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="929f1-186">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="929f1-187">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="929f1-187">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="929f1-188">MAPI denominada propriedades</span><span class="sxs-lookup"><span data-stu-id="929f1-188">MAPI Named Properties</span></span>](mapi-named-properties.md)
  
[<span data-ttu-id="929f1-189">Usando macros para tratamento de erros</span><span class="sxs-lookup"><span data-stu-id="929f1-189">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

