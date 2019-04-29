---
title: IMAPIPropGetIDsFromNames
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetIDsFromNames
api_type:
- COM
ms.assetid: e3f501a4-a8ee-43d7-bd83-c94e7980c398
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 28880b818bc80e31cae0c695d4aac92eb9555cac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433581"
---
# <a name="imapipropgetidsfromnames"></a><span data-ttu-id="01a0d-103">IMAPIProp::GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="01a0d-103">IMAPIProp::GetIDsFromNames</span></span>

  
  
<span data-ttu-id="01a0d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="01a0d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="01a0d-105">Fornece os identificadores de propriedade que correspondem a um ou mais nomes de propriedade.</span><span class="sxs-lookup"><span data-stu-id="01a0d-105">Provides the property identifiers that correspond to one or more property names.</span></span>
  
```cpp
HRESULT GetIDsFromNames(
  ULONG cPropNames,
  LPMAPINAMEID FAR * lppPropNames,
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTags
);
```

## <a name="parameters"></a><span data-ttu-id="01a0d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="01a0d-106">Parameters</span></span>

 <span data-ttu-id="01a0d-107">_cPropNames_</span><span class="sxs-lookup"><span data-stu-id="01a0d-107">_cPropNames_</span></span>
  
> <span data-ttu-id="01a0d-108">no A contagem de nomes de propriedade apontados pelo parâmetro _lppPropNames_ .</span><span class="sxs-lookup"><span data-stu-id="01a0d-108">[in] The count of property names pointed to by the  _lppPropNames_ parameter.</span></span> <span data-ttu-id="01a0d-109">Se _lppPropNames_ for nulo, o parâmetro _cPropNames_ deverá ser 0.</span><span class="sxs-lookup"><span data-stu-id="01a0d-109">If  _lppPropNames_ is NULL, the  _cPropNames_ parameter must be 0.</span></span> 
    
 <span data-ttu-id="01a0d-110">_lppPropNames_</span><span class="sxs-lookup"><span data-stu-id="01a0d-110">_lppPropNames_</span></span>
  
> <span data-ttu-id="01a0d-111">no Um ponteiro para uma matriz de nomes de propriedade ou nulo.</span><span class="sxs-lookup"><span data-stu-id="01a0d-111">[in] A pointer to an array of property names, or NULL.</span></span> <span data-ttu-id="01a0d-112">Passando identificadores de propriedade de solicitações nulos para todos os nomes de propriedade em todos os conjuntos de propriedades sobre os quais o objeto tem informações.</span><span class="sxs-lookup"><span data-stu-id="01a0d-112">Passing NULL requests property identifiers for all property names in all property sets about which the object has information.</span></span> <span data-ttu-id="01a0d-113">O parâmetro _lppPropNames_ não deve ser nulo se o sinalizador MAPI_CREATE estiver definido no parâmetro _parâmetroulflags_ .</span><span class="sxs-lookup"><span data-stu-id="01a0d-113">The  _lppPropNames_ parameter must not be NULL if the MAPI_CREATE flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="01a0d-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="01a0d-114">_ulFlags_</span></span>
  
> <span data-ttu-id="01a0d-115">no Uma bitmask de sinalizadores que indica como os identificadores de propriedade devem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="01a0d-115">[in] A bitmask of flags that indicates how the property identifiers should be returned.</span></span> <span data-ttu-id="01a0d-116">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="01a0d-116">The following flag can be set:</span></span>
    
<span data-ttu-id="01a0d-117">MAPI_CREATE</span><span class="sxs-lookup"><span data-stu-id="01a0d-117">MAPI_CREATE</span></span> 
  
> <span data-ttu-id="01a0d-118">Atribui um identificador de propriedade, se ainda não tiver sido atribuído um ou mais dos nomes incluídos na matriz de nomes de propriedade apontada por _lppPropNames_.</span><span class="sxs-lookup"><span data-stu-id="01a0d-118">Assigns a property identifier, if one has not yet been assigned, to one or more of the names included in the property name array pointed to by  _lppPropNames_.</span></span> <span data-ttu-id="01a0d-119">Este sinalizador registra internamente o identificador na tabela de mapeamento de nome para identificador.</span><span class="sxs-lookup"><span data-stu-id="01a0d-119">This flag internally registers the identifier in the name-to-identifier mapping table.</span></span>
    
 <span data-ttu-id="01a0d-120">_lppPropTags_</span><span class="sxs-lookup"><span data-stu-id="01a0d-120">_lppPropTags_</span></span>
  
> <span data-ttu-id="01a0d-121">bota Um ponteiro para um ponteiro para uma matriz de marcas de propriedade que contém identificadores de propriedade recém-criados ou existentes.</span><span class="sxs-lookup"><span data-stu-id="01a0d-121">[out] A pointer to a pointer to an array of property tags that contains existing or newly assigned property identifiers.</span></span> <span data-ttu-id="01a0d-122">Os tipos de propriedade para as marcas de propriedade nesta matriz são definidos como **PT_UNSPECIFIED**.</span><span class="sxs-lookup"><span data-stu-id="01a0d-122">The property types for the property tags in this array are set to **PT_UNSPECIFIED**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="01a0d-123">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="01a0d-123">Return value</span></span>

<span data-ttu-id="01a0d-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="01a0d-124">S_OK</span></span> 
  
> <span data-ttu-id="01a0d-125">Os identificadores para os nomes das propriedades especificadas foram retornados com êxito.</span><span class="sxs-lookup"><span data-stu-id="01a0d-125">The identifiers for the specified property names were successfully returned.</span></span>
    
<span data-ttu-id="01a0d-126">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="01a0d-126">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="01a0d-127">O objeto não dá suporte a propriedades nomeadas.</span><span class="sxs-lookup"><span data-stu-id="01a0d-127">The object does not support named properties.</span></span>
    
<span data-ttu-id="01a0d-128">MAPI_E_NOT_ENOUGH_MEMORY</span><span class="sxs-lookup"><span data-stu-id="01a0d-128">MAPI_E_NOT_ENOUGH_MEMORY</span></span> 
  
> <span data-ttu-id="01a0d-129">Memória inSuficiente disponível para recuperar os identificadores.</span><span class="sxs-lookup"><span data-stu-id="01a0d-129">Insufficient memory was available to retrieve the identifiers.</span></span>
    
<span data-ttu-id="01a0d-130">MAPI_E_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="01a0d-130">MAPI_E_TOO_BIG</span></span> 
  
> <span data-ttu-id="01a0d-131">A operação não pode ser executada porque requer muitas marcas de propriedade a serem retornadas.</span><span class="sxs-lookup"><span data-stu-id="01a0d-131">The operation cannot be performed because it requires too many property tags to be returned.</span></span>
    
<span data-ttu-id="01a0d-132">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="01a0d-132">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="01a0d-133">A chamada teve êxito geral, mas não foi possível retornar um ou mais identificadores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="01a0d-133">The call succeeded overall, but one or more property identifiers could not be returned.</span></span> <span data-ttu-id="01a0d-134">O tipo de propriedade correspondente para cada propriedade indisponível é definido como **PT_ERROR** e seu identificador como zero.</span><span class="sxs-lookup"><span data-stu-id="01a0d-134">The corresponding property type for each unavailable property is set to **PT_ERROR** and its identifier to zero.</span></span> <span data-ttu-id="01a0d-135">Quando esse aviso for retornado, manipule a chamada como bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="01a0d-135">When this warning is returned, handle the call as successful.</span></span> <span data-ttu-id="01a0d-136">Para testar esse aviso, use a macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="01a0d-136">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="01a0d-137">Consulte [usando macros para tratamento de erros](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="01a0d-137">See [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="01a0d-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="01a0d-138">Remarks</span></span>

<span data-ttu-id="01a0d-139">O método **IMAPIProp:: GetIDsFromNames** recupera uma matriz de marcas de propriedade que mantêm os identificadores de propriedade para uma ou mais propriedades nomeadas.</span><span class="sxs-lookup"><span data-stu-id="01a0d-139">The **IMAPIProp::GetIDsFromNames** method retrieves an array of property tags that hold the property identifiers for one or more named properties.</span></span> <span data-ttu-id="01a0d-140">**IMAPIProp:: GetIDsFromNames** pode ser chamado para fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="01a0d-140">**IMAPIProp::GetIDsFromNames** can be called to do the following:</span></span> 
  
- <span data-ttu-id="01a0d-141">Criar identificadores para novos nomes.</span><span class="sxs-lookup"><span data-stu-id="01a0d-141">Create identifiers for new names.</span></span>
    
- <span data-ttu-id="01a0d-142">Recuperar identificadores para nomes específicos.</span><span class="sxs-lookup"><span data-stu-id="01a0d-142">Retrieve identifiers for specific names.</span></span>
    
- <span data-ttu-id="01a0d-143">Recuperar identificadores de todas as propriedades nomeadas incluídas no mapeamento do objeto.</span><span class="sxs-lookup"><span data-stu-id="01a0d-143">Retrieve identifiers for all named properties that are included in the object's mapping.</span></span>
    
<span data-ttu-id="01a0d-144">Propriedades nomeadas normalmente são usadas por provedores de repositórios de mensagens para pastas e mensagens.</span><span class="sxs-lookup"><span data-stu-id="01a0d-144">Named properties are typically used by message store providers for folders and messages.</span></span> <span data-ttu-id="01a0d-145">Outros objetos, como usuários de mensagens e seções de perfil, podem não oferecer suporte à associação de nomes aos identificadores de propriedade e podem retornar MAPI_E_NO_SUPPORT de **GetIDsFromNames**.</span><span class="sxs-lookup"><span data-stu-id="01a0d-145">Other objects, such as messaging users and profile sections, might not support the association of names to property identifiers and might return MAPI_E_NO_SUPPORT from **GetIDsFromNames**.</span></span>
  
<span data-ttu-id="01a0d-146">Se houver um erro que retorne um identificador para um nome específico, **GetIDsFromNames** retornará MAPI_W_ERRORS_RETURNED e definirá o tipo de propriedade na entrada de matriz da marca de propriedade que corresponde ao nome como **PT_ERROR** e o identificador como zero.</span><span class="sxs-lookup"><span data-stu-id="01a0d-146">If there is an error that returns an identifier for a particular name, **GetIDsFromNames** returns MAPI_W_ERRORS_RETURNED and sets the property type in the property tag array entry that corresponds to the name to **PT_ERROR** and the identifier to zero.</span></span> 
  
<span data-ttu-id="01a0d-147">O mapeamento de nome para identificador é representado pela propriedade **PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)) de um objeto.</span><span class="sxs-lookup"><span data-stu-id="01a0d-147">Name-to-identifier mapping is represented by an object's **PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)) property.</span></span> <span data-ttu-id="01a0d-148">**PR_MAPPING_SIGNATURE** contém uma estrutura [MAPIUID](mapiuid.md) que indica o provedor de serviços responsável pelo objeto.</span><span class="sxs-lookup"><span data-stu-id="01a0d-148">**PR_MAPPING_SIGNATURE** contains a [MAPIUID](mapiuid.md) structure that indicates the service provider responsible for the object.</span></span> <span data-ttu-id="01a0d-149">Se a propriedade **PR_MAPPING_SIGNATURE** for a mesma de dois objetos, suponha que esses objetos usem o mesmo mapeamento de nome para identificador.</span><span class="sxs-lookup"><span data-stu-id="01a0d-149">If the **PR_MAPPING_SIGNATURE** property is the same for two objects, assume that these objects use the same name-to-identifier mapping.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="01a0d-150">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="01a0d-150">Notes to implementers</span></span>

<span data-ttu-id="01a0d-151">Os identificadores que você passa de volta na matriz de marca de propriedade apontada pelo parâmetro _lppPropNames_ devem estar no intervalo 0X8000 para 0xFFFE.</span><span class="sxs-lookup"><span data-stu-id="01a0d-151">The identifiers that you pass back in the property tag array pointed to by the  _lppPropNames_ parameter must be in the 0x8000 to 0xFFFE range.</span></span> <span data-ttu-id="01a0d-152">As entradas nessa matriz devem estar na mesma ordem que os nomes passados na matriz de nomes de propriedade apontada por _lppPropNames_.</span><span class="sxs-lookup"><span data-stu-id="01a0d-152">The entries in this array must be in the same order as the names passed in the property name array pointed to by  _lppPropNames_.</span></span> 
  
<span data-ttu-id="01a0d-153">Se você oferecer suporte a propriedades nomeadas em um contêiner, use o mesmo mapeamento de nome para todos os objetos em seu contêiner (ou seja, não use um mapeamento diferente para cada pasta em seu repositório de mensagens ou cada mensagem em sua pasta).</span><span class="sxs-lookup"><span data-stu-id="01a0d-153">If you support named properties on a container, use the same name-to-identifier mapping for all objects in your container (that is, do not use a different mapping for each folder in your message store or each message in your folder).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="01a0d-154">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="01a0d-154">Notes to callers</span></span>

<span data-ttu-id="01a0d-155">Como os tipos de propriedade para os identificadores retornados na matriz de marca de propriedade apontada por _lppPropTags_ estão definidos como **PT_UNSPECIFIED**, você precisará chamar o método [IMAPIProp::](imapiprop-setprops.md) SetProps para recuperar os tipos precisos.</span><span class="sxs-lookup"><span data-stu-id="01a0d-155">Because the property types for the returned identifiers in the property tag array pointed to by  _lppPropTags_ are set to **PT_UNSPECIFIED**, you will have to call the [IMAPIProp::SetProps](imapiprop-setprops.md) method to retrieve the accurate types.</span></span> 
  
<span data-ttu-id="01a0d-156">Se você mover ou copiar objetos com propriedades nomeadas e os objetos de origem e de destino tiverem diferentes assinaturas de mapeamento conforme indicado pelos valores das suas propriedades **PR_MAPPING_SIGNATURE** , você deve preservar os nomes durante essas operações.</span><span class="sxs-lookup"><span data-stu-id="01a0d-156">If you move or copy objects with named properties, and the source and destination objects have different mapping signatures as indicated by the values of their **PR_MAPPING_SIGNATURE** properties, you must preserve the names during these operations.</span></span> <span data-ttu-id="01a0d-157">Para preservar os nomes de propriedade, ajuste os identificadores de propriedade correspondentes para corresponder ao mapeamento de nome para identificador do objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="01a0d-157">To preserve property names, adjust the corresponding property identifiers to match the name-to-identifier mapping of the destination object.</span></span> 
  
<span data-ttu-id="01a0d-158">Alguns objetos têm um limite quanto ao número de identificadores de propriedade que podem ser nomeados.</span><span class="sxs-lookup"><span data-stu-id="01a0d-158">Some objects have a limit as to the number of property identifiers they can name.</span></span> <span data-ttu-id="01a0d-159">Se uma chamada para **GetIDsFromNames** fizer com que esse limite seja excedido, o método retornará MAPI_E_TOO_BIG.</span><span class="sxs-lookup"><span data-stu-id="01a0d-159">If a call to **GetIDsFromNames** causes this limit to be exceeded, the method returns MAPI_E_TOO_BIG.</span></span> <span data-ttu-id="01a0d-160">Nesse caso, consulte por identificador.</span><span class="sxs-lookup"><span data-stu-id="01a0d-160">In this case, query by identifier.</span></span> 
  
<span data-ttu-id="01a0d-161">Para obter mais informações, consulte [MAPI Named Properties](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="01a0d-161">For more information, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="01a0d-162">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="01a0d-162">MFCMAPI reference</span></span>

<span data-ttu-id="01a0d-163">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="01a0d-163">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="01a0d-164">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="01a0d-164">**File**</span></span>|<span data-ttu-id="01a0d-165">**Função**</span><span class="sxs-lookup"><span data-stu-id="01a0d-165">**Function**</span></span>|<span data-ttu-id="01a0d-166">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="01a0d-166">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="01a0d-167">SingleMAPIPropListCtrl. cpp</span><span class="sxs-lookup"><span data-stu-id="01a0d-167">SingleMAPIPropListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="01a0d-168">CSingleMAPIPropListCtrl:: FindAllNamedPropsUsed</span><span class="sxs-lookup"><span data-stu-id="01a0d-168">CSingleMAPIPropListCtrl::FindAllNamedPropsUsed</span></span>  <br/> |<span data-ttu-id="01a0d-169">MFCMAPI usa o método **IMAPIProp:: GetIDsFromNames** para obter as marcas de propriedade de todas as propriedades nomeadas que foram mapeadas.</span><span class="sxs-lookup"><span data-stu-id="01a0d-169">MFCMAPI uses the **IMAPIProp::GetIDsFromNames** method to obtain property tags for all named properties that have been mapped.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="01a0d-170">Confira também</span><span class="sxs-lookup"><span data-stu-id="01a0d-170">See also</span></span>



[<span data-ttu-id="01a0d-171">IMAPIProp::GetNamesFromIDs</span><span class="sxs-lookup"><span data-stu-id="01a0d-171">IMAPIProp::GetNamesFromIDs</span></span>](imapiprop-getnamesfromids.md)
  
[<span data-ttu-id="01a0d-172">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="01a0d-172">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
  
[<span data-ttu-id="01a0d-173">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="01a0d-173">MAPINAMEID</span></span>](mapinameid.md)
  
[<span data-ttu-id="01a0d-174">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="01a0d-174">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="01a0d-175">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="01a0d-175">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="01a0d-176">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="01a0d-176">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="01a0d-177">MAPI denominada propriedades</span><span class="sxs-lookup"><span data-stu-id="01a0d-177">MAPI Named Properties</span></span>](mapi-named-properties.md)
  
[<span data-ttu-id="01a0d-178">Usando macros para tratamento de erros</span><span class="sxs-lookup"><span data-stu-id="01a0d-178">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

