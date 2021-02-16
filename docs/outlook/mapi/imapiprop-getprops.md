---
title: IMAPIPropGetProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetProps
api_type:
- COM
ms.assetid: 1c7a9cd2-d765-4218-9aee-52df1a2aae6c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9b03775d495f7d1f51142eb0ed06fc9ecdf6d1a3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412454"
---
# <a name="imapipropgetprops"></a><span data-ttu-id="39b75-103">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="39b75-103">IMAPIProp::GetProps</span></span>

  
  
<span data-ttu-id="39b75-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="39b75-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="39b75-105">Recupera o valor da propriedade de uma ou mais propriedades de um objeto.</span><span class="sxs-lookup"><span data-stu-id="39b75-105">Retrieves the property value of one or more properties of an object.</span></span>
  
```cpp
HRESULT GetProps(
  LPSPropTagArray lpPropTagArray,
  ULONG ulFlags,
  ULONG FAR * lpcValues,
  LPSPropValue FAR * lppPropArray
);
```

## <a name="parameters"></a><span data-ttu-id="39b75-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="39b75-106">Parameters</span></span>

 <span data-ttu-id="39b75-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="39b75-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="39b75-108">[in] Um ponteiro para uma matriz de marcas de propriedade que identificam as propriedades cujos valores devem ser recuperados.</span><span class="sxs-lookup"><span data-stu-id="39b75-108">[in] A pointer to an array of property tags that identify the properties whose values are to be retrieved.</span></span> <span data-ttu-id="39b75-109">O  _parâmetro lpPropTagArray_ deve ser NULL, indicando que os valores de todas as propriedades do objeto devem ser retornados ou apontar para uma estrutura [SPropTagArray](sproptagarray.md) que contém uma ou mais marcas de propriedade.</span><span class="sxs-lookup"><span data-stu-id="39b75-109">The  _lpPropTagArray_ parameter must be either NULL, indicating that values for all properties of the object should be returned, or point to an [SPropTagArray](sproptagarray.md) structure that contains one or more property tags.</span></span> 
    
 <span data-ttu-id="39b75-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="39b75-110">_ulFlags_</span></span>
  
> <span data-ttu-id="39b75-111">[in] Uma máscara de bits de sinalizadores que indica o formato das propriedades que têm o tipo PT_UNSPECIFIED.</span><span class="sxs-lookup"><span data-stu-id="39b75-111">[in] A bitmask of flags that indicates the format for properties that have the type PT_UNSPECIFIED.</span></span> <span data-ttu-id="39b75-112">O sinalizador a seguir pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="39b75-112">The following flag can be set:</span></span>
    
<span data-ttu-id="39b75-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="39b75-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="39b75-114">Os valores de cadeia de caracteres dessas propriedades devem ser retornados no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="39b75-114">The string values for these properties should be returned in the Unicode format.</span></span> <span data-ttu-id="39b75-115">Se o MAPI_UNICODE não estiver definido, os valores da cadeia de caracteres deverão ser retornados no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="39b75-115">If the MAPI_UNICODE flag is not set, the string values should be returned in the ANSI format.</span></span>
    
 <span data-ttu-id="39b75-116">_lpcValues_</span><span class="sxs-lookup"><span data-stu-id="39b75-116">_lpcValues_</span></span>
  
> <span data-ttu-id="39b75-117">[out] Um ponteiro para uma contagem de valores de propriedade apontados pelo _parâmetro lppPropArray._</span><span class="sxs-lookup"><span data-stu-id="39b75-117">[out] A pointer to a count of property values pointed to by the  _lppPropArray_ parameter.</span></span> <span data-ttu-id="39b75-118">Se  _lppPropArray_ for NULL, o conteúdo do parâmetro  _lpcValues_ será zero.</span><span class="sxs-lookup"><span data-stu-id="39b75-118">If  _lppPropArray_ is NULL, the content of the  _lpcValues_ parameter is zero.</span></span> 
    
 <span data-ttu-id="39b75-119">_lppPropArray_</span><span class="sxs-lookup"><span data-stu-id="39b75-119">_lppPropArray_</span></span>
  
> <span data-ttu-id="39b75-120">[out] Um ponteiro para um ponteiro para os valores de propriedade recuperados.</span><span class="sxs-lookup"><span data-stu-id="39b75-120">[out] A pointer to a pointer to the retrieved property values.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="39b75-121">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="39b75-121">Return value</span></span>

<span data-ttu-id="39b75-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="39b75-122">S_OK</span></span> 
  
> <span data-ttu-id="39b75-123">Os valores da propriedade foram recuperados com êxito.</span><span class="sxs-lookup"><span data-stu-id="39b75-123">The property values were successfully retrieved.</span></span>
    
<span data-ttu-id="39b75-124">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="39b75-124">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="39b75-125">A chamada foi bem-sucedida em geral, mas uma ou mais propriedades não puderam ser acessadas.</span><span class="sxs-lookup"><span data-stu-id="39b75-125">The call succeeded overall, but one or more properties could not be accessed.</span></span> <span data-ttu-id="39b75-126">O **membro aulPropTag** do valor da propriedade para cada propriedade indisponível tem um tipo de PT_ERROR e um identificador zero.</span><span class="sxs-lookup"><span data-stu-id="39b75-126">The **aulPropTag** member of the property value for each unavailable property has a property type of PT_ERROR and an identifier of zero.</span></span> <span data-ttu-id="39b75-127">Quando esse aviso é retornado, a chamada deve ser tratada como bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="39b75-127">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="39b75-128">Para testar esse aviso, use a **HR_FAILED** macro.</span><span class="sxs-lookup"><span data-stu-id="39b75-128">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="39b75-129">Para obter mais informações, consulte [Usando macros para tratamento de erros.](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="39b75-129">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
<span data-ttu-id="39b75-130">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="39b75-130">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="39b75-131">Zero foi passado no **membro cValues** da **estrutura SPropTagArray** apontado por  _lpPropTagArray_.</span><span class="sxs-lookup"><span data-stu-id="39b75-131">Zero was passed in the **cValues** member of the **SPropTagArray** structure pointed to by  _lpPropTagArray_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="39b75-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="39b75-132">Remarks</span></span>

<span data-ttu-id="39b75-133">O **método IMAPIProp::GetProps** obtém os valores de propriedade de uma ou mais propriedades de um objeto.</span><span class="sxs-lookup"><span data-stu-id="39b75-133">The **IMAPIProp::GetProps** method obtains the property values of one or more properties of an object.</span></span> 
  
<span data-ttu-id="39b75-134">Os valores de propriedade são retornados na mesma ordem em que foram solicitados (ou seja, a ordem das propriedades na matriz de marca de propriedade apontada por  _lpPropTagArray_ corresponde à ordem na matriz de estruturas de valores de propriedade apontadas por  _lppPropArray_).</span><span class="sxs-lookup"><span data-stu-id="39b75-134">The property values are returned in the same order as they were requested (that is, the order of properties in the property tag array pointed to by  _lpPropTagArray_ matches the order in the array of property value structures pointed to by  _lppPropArray_).</span></span> 
  
<span data-ttu-id="39b75-135">Os tipos de propriedade especificados nos membros **aulPropTag** da matriz de marca de propriedade indicam o tipo de valor que deve ser retornado no membro **Value** de cada estrutura de valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="39b75-135">The property types specified in the **aulPropTag** members of the property tag array indicate the type of value that should be returned in the **Value** member of each property value structure.</span></span> <span data-ttu-id="39b75-136">No entanto, se o chamador não sabe o tipo de uma propriedade, o tipo no membro **aulPropTag** pode ser definido como PT_UNSPECIFIED.</span><span class="sxs-lookup"><span data-stu-id="39b75-136">However, if the caller does not know the type of a property, the type in the **aulPropTag** member can be set instead to PT_UNSPECIFIED.</span></span> <span data-ttu-id="39b75-137">Ao recuperar o valor, **GetProps** define o tipo correto no membro **aulPropTag** da estrutura de valores da propriedade para a propriedade.</span><span class="sxs-lookup"><span data-stu-id="39b75-137">In retrieving the value, **GetProps** sets the correct type in the **aulPropTag** member of the property value structure for the property.</span></span> 
  
<span data-ttu-id="39b75-138">Se os tipos de propriedade são especificados em **SPropTagArray** em  _lpPropTagArray_, os valores de propriedade em **SPropValue** retornados em  _lppPropArray_ têm tipos que exatamente corresponder aos tipos solicitados, a menos que um valor de erro seja retornado em vez disso.</span><span class="sxs-lookup"><span data-stu-id="39b75-138">If property types are specified in the **SPropTagArray** in  _lpPropTagArray_, the property values in the **SPropValue** returned in  _lppPropArray_ have types that exactly match the requested types, unless an error value is returned instead.</span></span> 
  
<span data-ttu-id="39b75-139">Propriedades de cadeia de caracteres podem ter um de dois tipos de propriedade: PT_UNICODE para representar o formato Unicode e PT_STRING8 para representar o formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="39b75-139">String properties can have one of two property types: PT_UNICODE to represent the Unicode format and PT_STRING8 to represent the ANSI format.</span></span> <span data-ttu-id="39b75-140">Se o sinalizador MAPI_UNICODE for definido no parâmetro  _ulFlags,_ sempre que **GetProps** não puder determinar o formato apropriado para uma propriedade de cadeia de caracteres, ele retornará seu valor no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="39b75-140">If the MAPI_UNICODE flag is set in the  _ulFlags_ parameter, whenever **GetProps** cannot determine the appropriate format for a string property, it returns its value in the Unicode format.</span></span> <span data-ttu-id="39b75-141">**GetProps** não pode determinar um tipo de propriedade de cadeia de caracteres exata nas seguintes situações:</span><span class="sxs-lookup"><span data-stu-id="39b75-141">**GetProps** cannot determine an exact string property type in the following situations:</span></span> 
  
- <span data-ttu-id="39b75-142">O  _parâmetro lpPropTagArray_ é definido como NULL para solicitar todas as propriedades.</span><span class="sxs-lookup"><span data-stu-id="39b75-142">The  _lpPropTagArray_ parameter is set to NULL to request all properties.</span></span> 
    
- <span data-ttu-id="39b75-143">O **membro aulPropTag** inclui o valor PT_UNSPECIFIED como seu tipo de propriedade na matriz de marca de propriedade.</span><span class="sxs-lookup"><span data-stu-id="39b75-143">The **aulPropTag** member includes the value PT_UNSPECIFIED as its property type in the property tag array.</span></span> 
    
<span data-ttu-id="39b75-144">Se o  _parâmetro lpPropTagArray_ for definido como NULL para recuperar todas as propriedades do objeto e nenhuma propriedade existir, **GetProps** faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="39b75-144">If the  _lpPropTagArray_ parameter is set to NULL to retrieve all of the properties of the object and no properties exist, **GetProps** does the following:</span></span> 
  
- <span data-ttu-id="39b75-145">Retorna S_OK.</span><span class="sxs-lookup"><span data-stu-id="39b75-145">Returns S_OK.</span></span>
    
- <span data-ttu-id="39b75-146">Define o valor de contagem no **membro cValues** da estrutura de valores da propriedade como 0.</span><span class="sxs-lookup"><span data-stu-id="39b75-146">Sets the count value in the **cValues** member of the property value structure to 0.</span></span> 
    
- <span data-ttu-id="39b75-147">Define o conteúdo de  _lpcValues_ como 0.</span><span class="sxs-lookup"><span data-stu-id="39b75-147">Sets the contents of  _lpcValues_ to 0.</span></span> 
    
- <span data-ttu-id="39b75-148">Define  _lppPropArray_ como NULL.</span><span class="sxs-lookup"><span data-stu-id="39b75-148">Sets  _lppPropArray_ to NULL.</span></span> 
    
 <span data-ttu-id="39b75-149">**GetProps** não deve retornar propriedades de vários valores com **cValues** definido como 0.</span><span class="sxs-lookup"><span data-stu-id="39b75-149">**GetProps** must not return multiple-value properties with **cValues** set to 0.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="39b75-150">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="39b75-150">Notes to implementers</span></span>

<span data-ttu-id="39b75-151">Chame a [função MAPIAllocateBuffer](mapiallocatebuffer.md) para alocar memória inicialmente para a estrutura [SPropValue](spropvalue.md) apontada por  _lpPropTagArray_; chame [MAPIAllocateMore](mapiallocatemore.md) para alocar qualquer memória adicional necessária para os membros da estrutura.</span><span class="sxs-lookup"><span data-stu-id="39b75-151">Call the [MAPIAllocateBuffer](mapiallocatebuffer.md) function to allocate memory initially for the [SPropValue](spropvalue.md) structure pointed to by  _lpPropTagArray_; call [MAPIAllocateMore](mapiallocatemore.md) to allocate any additional memory needed for the structure's members.</span></span> 
  
<span data-ttu-id="39b75-152">Retorne MAPI_W_ERRORS_RETURNED se não for possível recuperar o valor de uma ou mais das propriedades solicitadas.</span><span class="sxs-lookup"><span data-stu-id="39b75-152">Return MAPI_W_ERRORS_RETURNED if you cannot retrieve the value for one or more of the requested properties.</span></span> <span data-ttu-id="39b75-153">Na estrutura de valores de propriedade, de definir o tipo no membro **aulPropTag** como PT_ERROR e o membro **Value** como um código de status que descreve o erro.</span><span class="sxs-lookup"><span data-stu-id="39b75-153">In the property value structure, set the type in the **aulPropTag** member to PT_ERROR and the **Value** member to a status code that describes the error.</span></span> <span data-ttu-id="39b75-154">Por exemplo, se você tiver que converter uma cadeia de caracteres em Unicode e não suportar Unicode, de definir o membro **Value** como MAPI_E_BAD_CHARWIDTH.</span><span class="sxs-lookup"><span data-stu-id="39b75-154">For example, if you have to convert a string to Unicode and do not support Unicode, set the **Value** member to MAPI_E_BAD_CHARWIDTH.</span></span> <span data-ttu-id="39b75-155">Se a propriedade for muito grande, de definida como MAPI_E_NOT_ENOUGH_MEMORY.</span><span class="sxs-lookup"><span data-stu-id="39b75-155">If the property is too large, set it to MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="39b75-156">Se o objeto não suportar a propriedade, de definida como MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="39b75-156">If the object does not support the property, set it to MAPI_E_NOT_FOUND.</span></span> 
  
<span data-ttu-id="39b75-157">A implementação do método **GetProps** de um provedor de transporte remoto deve retornar os valores de propriedade da pasta para as propriedades solicitadas pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="39b75-157">A remote transport provider's implementation of the **GetProps** method must return the folder's property values for properties requested by the caller.</span></span> <span data-ttu-id="39b75-158">Sua implementação deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="39b75-158">Your implementation must do the following:</span></span> 
  
- <span data-ttu-id="39b75-159">Aloce uma matriz de valores de propriedade para retornar ao chamador e armazenar seu endereço no parâmetro de ponteiro de valor de propriedade passado para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="39b75-159">Allocate a property value array to return to the caller and store its address in the property value pointer parameter passed in for that purpose.</span></span>
    
- <span data-ttu-id="39b75-160">Copie as marcas de propriedade das propriedades da pasta para as marcas de propriedade na matriz de valores de propriedade de acordo com a matriz de marcas de propriedade passadas para **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="39b75-160">Copy the property tags from the folder's properties into the property tags in the property value array according to the array of property tags passed to **GetProps**.</span></span>
    
- <span data-ttu-id="39b75-161">Certifique-se de que o tipo de propriedade está definido para todas as marcas de propriedade **passadas para GetProps**.</span><span class="sxs-lookup"><span data-stu-id="39b75-161">Ensure that the property type is set for all property tags passed to **GetProps**.</span></span> <span data-ttu-id="39b75-162">O chamador pode passar um tipo de propriedade PT_UNSPECIFIED, nesse **caso, GetProps** deve definir o tipo de propriedade correto para essa marca de propriedade.</span><span class="sxs-lookup"><span data-stu-id="39b75-162">The caller can pass in a property type of PT_UNSPECIFIED, in which case **GetProps** must set the correct property type for that property tag.</span></span> 
    
- <span data-ttu-id="39b75-163">Definir o valor de cada propriedade na matriz de valores de propriedade de acordo com sua marca.</span><span class="sxs-lookup"><span data-stu-id="39b75-163">Set the value of each property in the property value array according to its tag.</span></span> <span data-ttu-id="39b75-164">Por exemplo, se a marca de propriedade solicitada pelo chamador for **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)), **GetProps** poderá definir o valor como MAPI_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="39b75-164">For example, if the property tag requested by the caller is **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)), **GetProps** can set the value to MAPI_FOLDER.</span></span> 
    
- <span data-ttu-id="39b75-165">Se o chamador passar qualquer marca de propriedade que sua implementação não manipular, você poderá definir a marca de propriedade como PT_ERROR para essas propriedades e definir o valor da propriedade como MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="39b75-165">If the caller passes in any property tags that your implementation does not handle, you can set the property tag to PT_ERROR for those properties, and set the property value to MAPI_E_NOT_FOUND.</span></span>
    
- <span data-ttu-id="39b75-166">Retorne S_OK se não houver erros ou MAPI_W_ERRORS_RETURNED se houver erros.</span><span class="sxs-lookup"><span data-stu-id="39b75-166">Return S_OK if no errors occurred or MAPI_W_ERRORS_RETURNED if there were errors.</span></span>
    
<span data-ttu-id="39b75-167">A implementação do método **GetProps** de um provedor de transporte remoto deve dar suporte mínimo às seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="39b75-167">A remote transport provider's implementation of the **GetProps** method must support the following properties at a minimum:</span></span> 
  
- <span data-ttu-id="39b75-168">**PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="39b75-168">**PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md))</span></span>
    
- <span data-ttu-id="39b75-169">**PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="39b75-169">**PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))</span></span>
    
- <span data-ttu-id="39b75-170">**PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="39b75-170">**PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="39b75-171">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="39b75-171">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="39b75-172">**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="39b75-172">**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="39b75-173">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="39b75-173">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="39b75-174">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="39b75-174">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
- <span data-ttu-id="39b75-175">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="39b75-175">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span></span>
    
- <span data-ttu-id="39b75-176">**PR_OBJECT_TYPE**</span><span class="sxs-lookup"><span data-stu-id="39b75-176">**PR_OBJECT_TYPE**</span></span>
    
- <span data-ttu-id="39b75-177">**PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="39b75-177">**PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="39b75-178">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="39b75-178">Notes to callers</span></span>

<span data-ttu-id="39b75-179">Para propriedades do tipo PT_OBJECT, chame o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) em vez de **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="39b75-179">For properties of type PT_OBJECT, call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method instead of **GetProps**.</span></span> 
  
<span data-ttu-id="39b75-180">Para propriedades seguras, não espere recuperá-las chamando **GetProps** com o parâmetro  _lppPropTagArray_ definido como NULL.</span><span class="sxs-lookup"><span data-stu-id="39b75-180">For secure properties, do not expect to retrieve them by calling **GetProps** with the  _lppPropTagArray_ parameter set to NULL.</span></span> <span data-ttu-id="39b75-181">Você deve definir explicitamente o identificador de uma propriedade segura no membro **aulPropTag** de sua matriz de marca de propriedade ao chamar **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="39b75-181">You must explicitly set a secure property's identifier in the **aulPropTag** member of its property tag array when you call **GetProps**.</span></span> <span data-ttu-id="39b75-182">Quando e como uma propriedade segura está disponível fica para o provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="39b75-182">When and how a secure property is available is up to the service provider.</span></span> 
  
<span data-ttu-id="39b75-183">Liberar a estrutura **SPropValue** retornada chamando a função [MAPIFreeBuffer](mapifreebuffer.md) somente se **GetProps** retornar S_OK ou MAPI_W_ERRORS_RETURNED.</span><span class="sxs-lookup"><span data-stu-id="39b75-183">Free the returned **SPropValue** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function only if **GetProps** returns S_OK or MAPI_W_ERRORS_RETURNED.</span></span> 
  
<span data-ttu-id="39b75-184">Se **GetProps** retornar MAPI_W_ERRORS_RETURNED porque não pôde acessar uma ou mais propriedades, verifique as marcas de propriedade das propriedades retornadas.</span><span class="sxs-lookup"><span data-stu-id="39b75-184">If **GetProps** returns MAPI_W_ERRORS_RETURNED because it could not access one or more properties, check the property tags of the returned properties.</span></span> <span data-ttu-id="39b75-185">As propriedades com falha terão os seguintes valores definidos em sua estrutura de valores de propriedade:</span><span class="sxs-lookup"><span data-stu-id="39b75-185">The failed properties will have the following values set in their property value structure:</span></span> 
  
- <span data-ttu-id="39b75-186">O tipo de propriedade no **membro aulPropTag** definido como PT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="39b75-186">The property type in the **aulPropTag** member set to PT_ERROR.</span></span> 
    
- <span data-ttu-id="39b75-187">O valor da propriedade no **membro Value** definido como um código de status para o erro, como MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="39b75-187">The property value in the **Value** member set to a status code for the error, such as MAPI_E_NOT_FOUND.</span></span> 
    
<span data-ttu-id="39b75-188">As propriedades que falham porque são muito grandes para serem convenientemente retornadas na estrutura de valores da propriedade têm seu membro **Value** definido como MAPI_E_NOT_ENOUGH_MEMORY.</span><span class="sxs-lookup"><span data-stu-id="39b75-188">Properties that fail because they are too large to conveniently be returned in the property value structure have their **Value** member set to MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="39b75-189">Normalmente, isso ocorre com propriedades de cadeia de caracteres ou binárias do tipo PT_STRING8, PT_UNICODE ou PT_BINARY quando o valor da propriedade é 4 KB ou maior.</span><span class="sxs-lookup"><span data-stu-id="39b75-189">Typically, this occurs with string or binary properties of type PT_STRING8, PT_UNICODE, or PT_BINARY when the value of the property is 4 KB or larger.</span></span> <span data-ttu-id="39b75-190">Chame **IMAPIProp::OpenProperty** para recuperar propriedades grandes.</span><span class="sxs-lookup"><span data-stu-id="39b75-190">Call **IMAPIProp::OpenProperty** to retrieve large properties.</span></span> 
  
<span data-ttu-id="39b75-191">Nem todas as implementações de **GetProps** suportam os formatos Unicode e ANSI para cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="39b75-191">Not all implementations of **GetProps** support both the Unicode and ANSI formats for character strings.</span></span> <span data-ttu-id="39b75-192">Quando uma propriedade específica requer conversão de formato de cadeia de caracteres e **GetProps** não pode dar suporte a ela, o membro **Value** da propriedade é definido como MAPI_E_BAD_CHARWIDTH.</span><span class="sxs-lookup"><span data-stu-id="39b75-192">When a particular property requires string format conversion and **GetProps** cannot support it, the **Value** member for the property is set to MAPI_E_BAD_CHARWIDTH.</span></span> 
  
<span data-ttu-id="39b75-193">Para verificar se um PST é um PST do SharePoint, monte o PST usando [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md), em seguida, chame **GetProps** no objeto do repositório de mensagens solicitando essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="39b75-193">To check if a PST is a SharePoint PST, mount the PST using [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md), then call **GetProps** on the message store object requesting this property.</span></span> <span data-ttu-id="39b75-194">Se existir, você pode presumir que o PST foi configurado para o SharePoint; caso não tenha sido, o PST não foi configurado como um PST do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="39b75-194">If it exists, you can assume the PST has been configured for SharePoint; if not, the PST has not been configured as a SharePoint PST.</span></span> 
  
<span data-ttu-id="39b75-195">Para obter mais informações sobre como usar **GetProps** para acessar propriedades, consulte [Recuperando propriedades MAPI](retrieving-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="39b75-195">For more information about how to use **GetProps** to access properties, see [Retrieving MAPI Properties](retrieving-mapi-properties.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="39b75-196">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="39b75-196">MFCMAPI reference</span></span>

<span data-ttu-id="39b75-197">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="39b75-197">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="39b75-198">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="39b75-198">**File**</span></span>|<span data-ttu-id="39b75-199">**Função**</span><span class="sxs-lookup"><span data-stu-id="39b75-199">**Function**</span></span>|<span data-ttu-id="39b75-200">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="39b75-200">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="39b75-201">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="39b75-201">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="39b75-202">GetPropsNULL</span><span class="sxs-lookup"><span data-stu-id="39b75-202">GetPropsNULL</span></span>  <br/> |<span data-ttu-id="39b75-203">MFCMAPI usa o método **IMAPIProp::GetProps** para obter todas as propriedades de um objeto passando NULL ou a matriz retornada pelo método [IMAPIProp::GetPropList](imapiprop-getproplist.md) no parâmetro _lpPropTagArray._</span><span class="sxs-lookup"><span data-stu-id="39b75-203">MFCMAPI uses the **IMAPIProp::GetProps** method to obtain all properties for an object by passing either NULL or the array returned by the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method in the  _lpPropTagArray_ parameter.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="39b75-204">Confira também</span><span class="sxs-lookup"><span data-stu-id="39b75-204">See also</span></span>



[<span data-ttu-id="39b75-205">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="39b75-205">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="39b75-206">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="39b75-206">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="39b75-207">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="39b75-207">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="39b75-208">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="39b75-208">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="39b75-209">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="39b75-209">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="39b75-210">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="39b75-210">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="39b75-211">SPropValue</span><span class="sxs-lookup"><span data-stu-id="39b75-211">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="39b75-212">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="39b75-212">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="39b75-213">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="39b75-213">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="39b75-214">Recuperar propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="39b75-214">Retrieving MAPI Properties</span></span>](retrieving-mapi-properties.md)
  
[<span data-ttu-id="39b75-215">Usando macros para tratamento de erros</span><span class="sxs-lookup"><span data-stu-id="39b75-215">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

