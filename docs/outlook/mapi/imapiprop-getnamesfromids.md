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
ms.openlocfilehash: 186afd6a80d0ae3ae0a767456e60b2ebaaa579b9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574381"
---
# <a name="imapipropgetnamesfromids"></a><span data-ttu-id="54173-103">IMAPIProp::GetNamesFromIDs</span><span class="sxs-lookup"><span data-stu-id="54173-103">IMAPIProp::GetNamesFromIDs</span></span>

  
  
<span data-ttu-id="54173-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="54173-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="54173-105">Fornece os nomes de propriedades que correspondem a um ou mais identificadores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="54173-105">Provides the property names that correspond to one or more property identifiers.</span></span>
  
```cpp
HRESULT GetNamesFromIDs(
  LPSPropTagArray FAR * lppPropTags,
  LPGUID lpPropSetGuid,
  ULONG ulFlags,
  ULONG FAR * lpcPropNames,
  LPMAPINAMEID FAR * FAR * lpppPropNames
);
```

## <a name="parameters"></a><span data-ttu-id="54173-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="54173-106">Parameters</span></span>

 <span data-ttu-id="54173-107">_lppPropTags_</span><span class="sxs-lookup"><span data-stu-id="54173-107">_lppPropTags_</span></span>
  
> <span data-ttu-id="54173-108">[além, out] Na entrada, um ponteiro para uma estrutura [SPropTagArray](sproptagarray.md) que contém uma matriz de marcas de propriedade; Caso contrário, NULL, indicando que todos os nomes devem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="54173-108">[in, out] On input, a pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags; otherwise, NULL, indicating that all names should be returned.</span></span> <span data-ttu-id="54173-109">O membro **cValues** para a matriz de marca de propriedade não pode ser 0.</span><span class="sxs-lookup"><span data-stu-id="54173-109">The **cValues** member for the property tag array cannot be 0.</span></span> <span data-ttu-id="54173-110">Se _lppPropTags_ for um ponteiro válido na entrada, **GetNamesFromIDs** retorna os nomes de cada identificador de propriedade incluídos na matriz.</span><span class="sxs-lookup"><span data-stu-id="54173-110">If  _lppPropTags_ is a valid pointer on input, **GetNamesFromIDs** returns names for each property identifier included in the array.</span></span> 
    
 <span data-ttu-id="54173-111">_lpPropSetGuid_</span><span class="sxs-lookup"><span data-stu-id="54173-111">_lpPropSetGuid_</span></span>
  
> <span data-ttu-id="54173-112">[in] Um ponteiro para um GUID ou um [GUID](guid.md) estrutura, que identifica um conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="54173-112">[in] A pointer to a GUID, or [GUID](guid.md) structure, that identifies a property set.</span></span> <span data-ttu-id="54173-113">O parâmetro _lpPropSetGuid_ pode apontar para um conjunto de propriedades válido ou pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="54173-113">The  _lpPropSetGuid_ parameter can point to a valid property set or can be NULL.</span></span> 
    
 <span data-ttu-id="54173-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="54173-114">_ulFlags_</span></span>
  
> <span data-ttu-id="54173-115">[in] Uma bitmask dos sinalizadores que indica o tipo de nomes a serem retornadas.</span><span class="sxs-lookup"><span data-stu-id="54173-115">[in] A bitmask of flags that indicates the type of names to be returned.</span></span> <span data-ttu-id="54173-116">Sinalizadores a seguir podem ser usados (se ambos os sinalizadores estão definidos, sem nomes serão retornados):</span><span class="sxs-lookup"><span data-stu-id="54173-116">The following flags can be used (if both flags are set, no names will be returned):</span></span>
    
<span data-ttu-id="54173-117">MAPI_NO_IDS</span><span class="sxs-lookup"><span data-stu-id="54173-117">MAPI_NO_IDS</span></span> 
  
> <span data-ttu-id="54173-118">Solicitações que somente os nomes armazenados como cadeias de caracteres Unicode ser retornado.</span><span class="sxs-lookup"><span data-stu-id="54173-118">Requests that only names stored as Unicode strings be returned.</span></span> 
    
<span data-ttu-id="54173-119">MAPI_NO_STRINGS</span><span class="sxs-lookup"><span data-stu-id="54173-119">MAPI_NO_STRINGS</span></span> 
  
> <span data-ttu-id="54173-120">Solicitações que somente os nomes armazenados como identificadores numéricos ser retornado.</span><span class="sxs-lookup"><span data-stu-id="54173-120">Requests that only names stored as numeric identifiers be returned.</span></span> 
    
 <span data-ttu-id="54173-121">_lpcPropNames_</span><span class="sxs-lookup"><span data-stu-id="54173-121">_lpcPropNames_</span></span>
  
> <span data-ttu-id="54173-122">[out] Um ponteiro para uma contagem dos ponteiros de nome de propriedade na matriz apontado pelo parâmetro _lppPropNames_ .</span><span class="sxs-lookup"><span data-stu-id="54173-122">[out] A pointer to a count of the property name pointers in the array pointed to by the  _lppPropNames_ parameter.</span></span> 
    
 <span data-ttu-id="54173-123">_lpppPropNames_</span><span class="sxs-lookup"><span data-stu-id="54173-123">_lpppPropNames_</span></span>
  
> <span data-ttu-id="54173-124">[out] Um ponteiro para uma matriz de ponteiros para estruturas [MAPINAMEID](mapinameid.md) que contém os nomes de propriedade.</span><span class="sxs-lookup"><span data-stu-id="54173-124">[out] A pointer to an array of pointers to [MAPINAMEID](mapinameid.md) structures that contains property names.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="54173-125">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="54173-125">Return value</span></span>

<span data-ttu-id="54173-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="54173-126">S_OK</span></span> 
  
> <span data-ttu-id="54173-127">Os nomes de propriedade foram retornados com êxito.</span><span class="sxs-lookup"><span data-stu-id="54173-127">The property names were successfully returned.</span></span> 
    
<span data-ttu-id="54173-128">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="54173-128">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="54173-129">O objeto não dá suporte a propriedades nomeadas.</span><span class="sxs-lookup"><span data-stu-id="54173-129">The object does not support named properties.</span></span> 
    
<span data-ttu-id="54173-130">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="54173-130">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="54173-131">Chamada bem-sucedida, mas os nomes para uma ou mais propriedades não puderam ser retornados.</span><span class="sxs-lookup"><span data-stu-id="54173-131">The call succeeded overall, but names for one or more properties could not be returned.</span></span> <span data-ttu-id="54173-132">As marcas de propriedade para as propriedades de falha têm um tipo de propriedade de **PT_ERROR**.</span><span class="sxs-lookup"><span data-stu-id="54173-132">The property tags for the failing properties have a property type of **PT_ERROR**.</span></span> <span data-ttu-id="54173-133">Quando esse aviso é retornado, a chamada deve ser manipulada com êxito.</span><span class="sxs-lookup"><span data-stu-id="54173-133">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="54173-134">Para testar esse aviso, use a macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="54173-134">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="54173-135">Para obter mais informações, consulte [Usando Macros para tratamento de erros](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="54173-135">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span> 
    
<span data-ttu-id="54173-136">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="54173-136">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="54173-137">O membro **cValues** de uma ou mais das entradas na matriz de marca de propriedade apontado pela _lppPropTags_ é definido como 0.</span><span class="sxs-lookup"><span data-stu-id="54173-137">The **cValues** member of one or more of the entries in the property tag array pointed to by  _lppPropTags_ is set to 0.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="54173-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="54173-138">Remarks</span></span>

<span data-ttu-id="54173-139">Enquanto o acesso a maioria das propriedades é por identificador de propriedade, algumas propriedades podem ser acessadas pelo nome.</span><span class="sxs-lookup"><span data-stu-id="54173-139">While access to most properties is by property identifier, some properties can be accessed by name.</span></span> <span data-ttu-id="54173-140">O método **IMAPIProp::GetNamesFromIDs** pode ser chamado para fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="54173-140">The **IMAPIProp::GetNamesFromIDs** method can be called to do the following:</span></span> 
  
- <span data-ttu-id="54173-141">Recupere os nomes de identificadores de propriedade específico em um conjunto específico de propriedade.</span><span class="sxs-lookup"><span data-stu-id="54173-141">Retrieve names for specific property identifiers in a specific property set.</span></span>
    
- <span data-ttu-id="54173-142">Recupere os nomes de identificadores de propriedade específica em qualquer conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="54173-142">Retrieve names for specific property identifiers in any property set.</span></span>
    
- <span data-ttu-id="54173-143">Recupere os nomes de todas as propriedades nomeados que estão incluídos no mapeamento do objeto.</span><span class="sxs-lookup"><span data-stu-id="54173-143">Retrieve names for all named properties that are included in the object's mapping.</span></span>
    
<span data-ttu-id="54173-144">Se definido de pontos de _lppPropTags_ para uma matriz de marca de propriedade válida com um ou mais identificadores de propriedade e pontos de _lpPropSetGuid_ para uma propriedade válida, **GetNamesFromIDs** ignora o conjunto de propriedades e os tipos de propriedade e retorna todos os nomes de que são mapeados para os identificadores especificados.</span><span class="sxs-lookup"><span data-stu-id="54173-144">If  _lppPropTags_ points to a valid property tag array with one or more property identifiers, and  _lpPropSetGuid_ points to a valid property set, **GetNamesFromIDs** ignores the property set and the property types and returns all of the names that map to the specified identifiers.</span></span> 
  
<span data-ttu-id="54173-145">Se for _lppPropTags_ pontos para uma matriz de marca de propriedade válida com um ou mais identificadores de propriedade e _lpPropSetGuid_ nulo, **GetNamesFromIDs** retorna todos os nomes que mapeiam para os identificadores especificados.</span><span class="sxs-lookup"><span data-stu-id="54173-145">If  _lppPropTags_ points to a valid property tag array with one or more property identifiers and  _lpPropSetGuid_ is NULL, **GetNamesFromIDs** returns all of the names that map to the specified identifiers.</span></span> 
  
<span data-ttu-id="54173-146">Se um identificador especificado não tem um nome, **GetNamesFromIDs** retornará NULL no lugar do identificador na estrutura retornada em _lpppPropNames_ e também retornará MAPI_W_ERRORS_RETURNED.</span><span class="sxs-lookup"><span data-stu-id="54173-146">If a specified identifier does not have a name, **GetNamesFromIDs** returns NULL in that identifier's place in the structure returned in  _lpppPropNames_ and also returns MAPI_W_ERRORS_RETURNED.</span></span> 
  
<span data-ttu-id="54173-147">Se _lpPropSetGuid_ e _lppPropTags_ forem NULL, **GetNamesFromIDs** aloca uma nova matriz de marca de propriedade e retorna todos os nomes de todas as propriedades nomeadas para o objeto.</span><span class="sxs-lookup"><span data-stu-id="54173-147">If both  _lpPropSetGuid_ and  _lppPropTags_ are NULL, **GetNamesFromIDs** allocates a new property tag array and returns all of the names for all of the named properties for the object.</span></span> 
  
<span data-ttu-id="54173-148">Quando não houver nenhum nome a ser retornado, talvez porque não existem propriedades no conjunto de propriedade solicitada ou todas as propriedades são de um tipo excluído com os sinalizadores, **GetNamesFromIDs** faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="54173-148">When there are no names to be returned, perhaps because there are no properties in the requested property set or all of the properties are of a type excluded by the flags, **GetNamesFromIDs** does the following:</span></span> 
  
- <span data-ttu-id="54173-149">Retorna S_OK.</span><span class="sxs-lookup"><span data-stu-id="54173-149">Returns S_OK.</span></span>
    
- <span data-ttu-id="54173-150">Aloca uma nova estrutura de **SPropTagArray** , definindo o membro **cValues** como 0.</span><span class="sxs-lookup"><span data-stu-id="54173-150">Allocates a new **SPropTagArray** structure, setting the **cValues** member to 0.</span></span> 
    
- <span data-ttu-id="54173-151">Define o conteúdo de _lpcPropNames_ como 0.</span><span class="sxs-lookup"><span data-stu-id="54173-151">Sets the contents of  _lpcPropNames_ to 0.</span></span> 
    
- <span data-ttu-id="54173-152">Define o conteúdo de _lpppPropNames_ como nulo.</span><span class="sxs-lookup"><span data-stu-id="54173-152">Sets the contents of  _lpppPropNames_ to NULL.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="54173-153">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="54173-153">Notes to implementers</span></span>

<span data-ttu-id="54173-154">Se _lpPropSetGuid_ pontos para um conjunto de propriedades válido e _lppPropTags_ for nulo, o resultado é indefinido.</span><span class="sxs-lookup"><span data-stu-id="54173-154">If  _lpPropSetGuid_ points to a valid property set and  _lppPropTags_ is NULL, the result is undefined.</span></span> <span data-ttu-id="54173-155">Você pode usar uma das seguintes estratégias:</span><span class="sxs-lookup"><span data-stu-id="54173-155">You can use one of the following strategies:</span></span> 
  
- <span data-ttu-id="54173-156">Ignorar o conjunto de propriedades e retornar os nomes para os identificadores na matriz de marca de propriedade.</span><span class="sxs-lookup"><span data-stu-id="54173-156">Ignore the property set and return the names for the identifiers in the property tag array.</span></span>
    
- <span data-ttu-id="54173-157">Retorna os nomes para apenas os identificadores da matriz de marca de propriedade que pertencem ao conjunto de propriedades especificado.</span><span class="sxs-lookup"><span data-stu-id="54173-157">Return the names for only the identifiers in the property tag array that belong to the specified property set.</span></span>
    
- <span data-ttu-id="54173-158">Transferir a chamada, retornando MAPI_E_INVALID_PARAMETER.</span><span class="sxs-lookup"><span data-stu-id="54173-158">Fail the call, returning MAPI_E_INVALID_PARAMETER.</span></span> 
    
## <a name="notes-to-callers"></a><span data-ttu-id="54173-159">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="54173-159">Notes to callers</span></span>

<span data-ttu-id="54173-160">Para recuperar todas as propriedades nomeadas para um objeto, você deve primeiro chamar o método do objeto [IMAPIProp::GetPropList](imapiprop-getproplist.md) e, em seguida, passa os identificadores retornados que estão acima do intervalo 0x8000 para **GetNamesFromIDs**.</span><span class="sxs-lookup"><span data-stu-id="54173-160">To retrieve all of the named properties for an object, you must first call the object's [IMAPIProp::GetPropList](imapiprop-getproplist.md) method and then pass the returned identifiers that are above the 0x8000 range to **GetNamesFromIDs**.</span></span>
  
<span data-ttu-id="54173-161">Se você passar um conjunto de propriedades válido, mas não uma matriz de marca de propriedade válida, estar preparado para resultados imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="54173-161">If you pass a valid property set but not a valid property tag array, be prepared for unpredictable results.</span></span> <span data-ttu-id="54173-162">Algumas implementações de **GetNamesFromIDs** ignorar o conjunto de propriedades e retornam os nomes para os identificadores na matriz de marca de propriedade.</span><span class="sxs-lookup"><span data-stu-id="54173-162">Some implementations of **GetNamesFromIDs** ignore the property set and return the names for the identifiers in the property tag array.</span></span> <span data-ttu-id="54173-163">Algumas implementações retornam MAPI_E_INVALID_PARAMETER.</span><span class="sxs-lookup"><span data-stu-id="54173-163">Some implementations return MAPI_E_INVALID_PARAMETER.</span></span> <span data-ttu-id="54173-164">Ainda outras implementações retornam nomes para os identificadores de todas as propriedades no conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="54173-164">Still other implementations return names for identifiers of all properties in the property set.</span></span> <span data-ttu-id="54173-165">Se o conjunto de propriedades for PS_PUBLIC_STRINGS, **GetNamesFromIDs** pode retornar todos os nomes que nunca foram criados.</span><span class="sxs-lookup"><span data-stu-id="54173-165">If the property set is PS_PUBLIC_STRINGS, **GetNamesFromIDs** can return all names that were ever created.</span></span> <span data-ttu-id="54173-166">Se o provedor de serviço armazena uma propriedade sob os identificadores associados as cadeias de caracteres públicas é irrelevante.</span><span class="sxs-lookup"><span data-stu-id="54173-166">Whether the service provider stores a property under the identifiers associated with the public strings is immaterial.</span></span> 
  
<span data-ttu-id="54173-167">Quando terminar com os nomes de propriedade, verifique o conteúdo do parâmetro _lpcPropNames_ para determinar se quaisquer nomes foram retornadas.</span><span class="sxs-lookup"><span data-stu-id="54173-167">When you are finished with the property names, check the contents of the  _lpcPropNames_ parameter to determine whether any names were returned.</span></span> <span data-ttu-id="54173-168">Em caso afirmativo, chame a função de [MAPIFreeBuffer](mapifreebuffer.md) para liberar a memória apontada pela _lppPropTags_ e _lpppPropNames_ quando um resultado bem-sucedido é retornado.</span><span class="sxs-lookup"><span data-stu-id="54173-168">If so, call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the memory pointed to by  _lppPropTags_ and  _lpppPropNames_ when a successful result is returned.</span></span> <span data-ttu-id="54173-169">Uma chamada de **MAPIFreeBuffer** é suficiente para cada parâmetro; Você não precisará percorrer a matriz de ponteiros e livre cada estrutura **MAPINAMEID** individualmente.</span><span class="sxs-lookup"><span data-stu-id="54173-169">One call to **MAPIFreeBuffer** is sufficient for each parameter; you do not have to traverse the array of pointers and free each **MAPINAMEID** structure individually.</span></span> 
  
<span data-ttu-id="54173-170">Para obter mais informações sobre propriedades nomeadas, consulte [Propriedades de chamada de MAPI](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="54173-170">For more information about named properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="54173-171">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="54173-171">MFCMAPI reference</span></span>

<span data-ttu-id="54173-172">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="54173-172">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="54173-173">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="54173-173">**File**</span></span>|<span data-ttu-id="54173-174">**Function**</span><span class="sxs-lookup"><span data-stu-id="54173-174">**Function**</span></span>|<span data-ttu-id="54173-175">**Comment**</span><span class="sxs-lookup"><span data-stu-id="54173-175">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="54173-176">SingleMAPIPropListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="54173-176">SingleMAPIPropListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="54173-177">CSingleMAPIPropListCtrl::FindAllNamedProps</span><span class="sxs-lookup"><span data-stu-id="54173-177">CSingleMAPIPropListCtrl::FindAllNamedProps</span></span>  <br/> |<span data-ttu-id="54173-178">MFCMAPI usa o método **IMAPIProp::GetNamesFromIDs** para procurar propriedades nomeadas que foram mapeadas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="54173-178">MFCMAPI uses the **IMAPIProp::GetNamesFromIDs** method to look up named properties that have previously been mapped.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="54173-179">Confira também</span><span class="sxs-lookup"><span data-stu-id="54173-179">See also</span></span>



[<span data-ttu-id="54173-180">GUID</span><span class="sxs-lookup"><span data-stu-id="54173-180">GUID</span></span>](guid.md)
  
[<span data-ttu-id="54173-181">IMAPIProp::GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="54173-181">IMAPIProp::GetIDsFromNames</span></span>](imapiprop-getidsfromnames.md)
  
[<span data-ttu-id="54173-182">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="54173-182">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="54173-183">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="54173-183">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="54173-184">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="54173-184">MAPINAMEID</span></span>](mapinameid.md)
  
[<span data-ttu-id="54173-185">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="54173-185">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="54173-186">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="54173-186">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="54173-187">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="54173-187">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="54173-188">MAPI denominada propriedades</span><span class="sxs-lookup"><span data-stu-id="54173-188">MAPI Named Properties</span></span>](mapi-named-properties.md)
  
[<span data-ttu-id="54173-189">Usar macros para lidar com erros</span><span class="sxs-lookup"><span data-stu-id="54173-189">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

