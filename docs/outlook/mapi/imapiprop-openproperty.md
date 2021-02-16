---
title: IMAPIPropOpenProperty
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.OpenProperty
api_type:
- COM
ms.assetid: e400e6cc-4e36-43fc-9304-b688a0a7fd77
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7bf1d6912e44319c36e288cd3870218e8c4e45ff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319807"
---
# <a name="imapipropopenproperty"></a><span data-ttu-id="e9b29-103">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="e9b29-103">IMAPIProp::OpenProperty</span></span>

<span data-ttu-id="e9b29-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e9b29-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e9b29-105">Retorna um ponteiro para uma interface que pode ser usada para acessar uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="e9b29-105">Returns a pointer to an interface that can be used to access a property.</span></span>
  
```cpp
HRESULT OpenProperty(
  ULONG ulPropTag,
  LPCIID lpiid,
  ULONG ulInterfaceOptions,
  ULONG ulFlags,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="e9b29-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e9b29-106">Parameters</span></span>

 <span data-ttu-id="e9b29-107">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="e9b29-107">_ulPropTag_</span></span>
  
> <span data-ttu-id="e9b29-108">[in] A marca da propriedade a ser acessada.</span><span class="sxs-lookup"><span data-stu-id="e9b29-108">[in] The property tag for the property to be accessed.</span></span> <span data-ttu-id="e9b29-109">O identificador e o tipo devem ser incluídos na marca de propriedade.</span><span class="sxs-lookup"><span data-stu-id="e9b29-109">Both the identifier and the type must be included in the property tag.</span></span>
    
 <span data-ttu-id="e9b29-110">_lpiid_</span><span class="sxs-lookup"><span data-stu-id="e9b29-110">_lpiid_</span></span>
  
> <span data-ttu-id="e9b29-111">[in] Um ponteiro para o identificador da interface a ser usada para acessar a propriedade.</span><span class="sxs-lookup"><span data-stu-id="e9b29-111">[in] A pointer to the identifier for the interface to be used to access the property.</span></span> <span data-ttu-id="e9b29-112">O _parâmetro lpiid_ não deve ser **nulo.**</span><span class="sxs-lookup"><span data-stu-id="e9b29-112">The  _lpiid_ parameter must not be **null**.</span></span>
    
 <span data-ttu-id="e9b29-113">_ulInterfaceOptions_</span><span class="sxs-lookup"><span data-stu-id="e9b29-113">_ulInterfaceOptions_</span></span>
  
> <span data-ttu-id="e9b29-114">[in] Dados relacionados à interface identificada pelo _parâmetro lpiid._</span><span class="sxs-lookup"><span data-stu-id="e9b29-114">[in] Data that relates to the interface identified by the  _lpiid_ parameter.</span></span> 
    
 <span data-ttu-id="e9b29-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e9b29-115">_ulFlags_</span></span>
  
> <span data-ttu-id="e9b29-116">[in] Uma máscara de bits de sinalizadores que controla o acesso à propriedade.</span><span class="sxs-lookup"><span data-stu-id="e9b29-116">[in] A bitmask of flags that controls access to the property.</span></span> <span data-ttu-id="e9b29-117">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="e9b29-117">The following flags can be set:</span></span>
    
<span data-ttu-id="e9b29-118">MAPI_CREATE</span><span class="sxs-lookup"><span data-stu-id="e9b29-118">MAPI_CREATE</span></span> 
  
> <span data-ttu-id="e9b29-119">Se a propriedade não existir, ela deverá ser criada.</span><span class="sxs-lookup"><span data-stu-id="e9b29-119">If the property does not exist, it should be created.</span></span> <span data-ttu-id="e9b29-120">Se a propriedade existir, o valor atual da propriedade deverá ser descartado.</span><span class="sxs-lookup"><span data-stu-id="e9b29-120">If the property does exist, the current value of the property should be discarded.</span></span> <span data-ttu-id="e9b29-121">Quando um chamador define o sinalizador MAPI_CREATE, ele também deve definir o MAPI_MODIFY sinalizador.</span><span class="sxs-lookup"><span data-stu-id="e9b29-121">When a caller sets the MAPI_CREATE flag, it should also set the MAPI_MODIFY flag.</span></span>
    
<span data-ttu-id="e9b29-122">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="e9b29-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="e9b29-123">Permite que **OpenProperty** retorne com êxito, possivelmente antes que o objeto seja totalmente disponível para o chamador.</span><span class="sxs-lookup"><span data-stu-id="e9b29-123">Allows **OpenProperty** to return successfully, possibly before the object is fully available to the caller.</span></span> <span data-ttu-id="e9b29-124">Se o objeto não estiver disponível, fazer uma chamada de objeto subsequente poderá criar um erro.</span><span class="sxs-lookup"><span data-stu-id="e9b29-124">If the object is not available, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="e9b29-125">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="e9b29-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="e9b29-126">MAPI_MODIFY é necessário nestas situações:</span><span class="sxs-lookup"><span data-stu-id="e9b29-126">MAPI_MODIFY is required in these situations:</span></span>
    
  - <span data-ttu-id="e9b29-127">Ao abrir uma propriedade de fluxo, como **IID_IStream,** modifique-a.</span><span class="sxs-lookup"><span data-stu-id="e9b29-127">When opening a stream property, such as **IID_IStream**, to modify it.</span></span>
    
  - <span data-ttu-id="e9b29-128">Ao abrir um anexo de mensagem incorporado, como [PR_ATTACH_DATA_OBJ](pidtagattachdataobject-canonical-property.md) aberto **com IID_IMessage**, para modificá-lo.</span><span class="sxs-lookup"><span data-stu-id="e9b29-128">When opening an embedded message attachment, such as [PR_ATTACH_DATA_OBJ](pidtagattachdataobject-canonical-property.md) opened with **IID_IMessage**, to modify it.</span></span>
    
 <span data-ttu-id="e9b29-129">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="e9b29-129">_lppUnk_</span></span>
  
> <span data-ttu-id="e9b29-130">[out] Um ponteiro para a interface solicitada a ser usada para o acesso à propriedade.</span><span class="sxs-lookup"><span data-stu-id="e9b29-130">[out] A pointer to the requested interface to be used for property access.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e9b29-131">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e9b29-131">Return value</span></span>

<span data-ttu-id="e9b29-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="e9b29-132">S_OK</span></span> 
  
> <span data-ttu-id="e9b29-133">O ponteiro da interface solicitado foi retornado com êxito.</span><span class="sxs-lookup"><span data-stu-id="e9b29-133">The requested interface pointer was successfully returned.</span></span>
    
<span data-ttu-id="e9b29-134">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="e9b29-134">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="e9b29-135">A interface solicitada não tem suporte para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="e9b29-135">The requested interface is not supported for this property.</span></span>
    
<span data-ttu-id="e9b29-136">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="e9b29-136">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="e9b29-137">O chamador tem permissões insuficientes para acessar a propriedade.</span><span class="sxs-lookup"><span data-stu-id="e9b29-137">The caller has insufficient permissions to access the property.</span></span>
    
<span data-ttu-id="e9b29-138">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="e9b29-138">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="e9b29-139">O objeto não pode fornecer acesso a essa propriedade por meio da interface solicitada.</span><span class="sxs-lookup"><span data-stu-id="e9b29-139">The object cannot provide access to this property through the requested interface.</span></span>
    
<span data-ttu-id="e9b29-140">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="e9b29-140">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="e9b29-141">A propriedade solicitada não existe e MAPI_CREATE não foi definida no _parâmetro ulFlags._</span><span class="sxs-lookup"><span data-stu-id="e9b29-141">The requested property does not exist and MAPI_CREATE was not set in the  _ulFlags_ parameter.</span></span> 
    
<span data-ttu-id="e9b29-142">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e9b29-142">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="e9b29-143">O tipo de propriedade na marca é definido como PT_UNSPECIFIED.</span><span class="sxs-lookup"><span data-stu-id="e9b29-143">The property type in the tag is set to PT_UNSPECIFIED.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e9b29-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="e9b29-144">Remarks</span></span>

<span data-ttu-id="e9b29-145">O **método IMAPIProp::OpenProperty** fornece acesso a uma propriedade por meio de uma interface específica.</span><span class="sxs-lookup"><span data-stu-id="e9b29-145">The **IMAPIProp::OpenProperty** method provides access to a property through a particular interface.</span></span> <span data-ttu-id="e9b29-146">**OpenProperty é** uma alternativa aos métodos [IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPIProp::SetProps.](imapiprop-setprops.md)</span><span class="sxs-lookup"><span data-stu-id="e9b29-146">**OpenProperty** is an alternative to the [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPIProp::SetProps](imapiprop-setprops.md) methods.</span></span> <span data-ttu-id="e9b29-147">Quando **GetProps ou** **SetProps** falhar porque a propriedade é muito grande ou muito complexa, chame **OpenProperty**.</span><span class="sxs-lookup"><span data-stu-id="e9b29-147">When either **GetProps** or **SetProps** fails because the property is too large or too complex, call **OpenProperty**.</span></span> <span data-ttu-id="e9b29-148">**OpenProperty** é normalmente usado para acessar propriedades do tipo PT_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="e9b29-148">**OpenProperty** is typically used to access properties of type PT_OBJECT.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e9b29-149">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="e9b29-149">Notes to callers</span></span>

<span data-ttu-id="e9b29-150">Para acessar anexos de mensagens, abra a propriedade **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) com um identificador de interface diferente, dependendo do tipo de anexo.</span><span class="sxs-lookup"><span data-stu-id="e9b29-150">To access message attachments, open the **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property with a different interface identifier, depending on the type of attachment.</span></span> <span data-ttu-id="e9b29-151">A tabela a seguir descreve como chamar **OpenProperty** para os diferentes tipos de anexos:</span><span class="sxs-lookup"><span data-stu-id="e9b29-151">The following table describes how to call **OpenProperty** for the different types of attachments:</span></span> 
  
|<span data-ttu-id="e9b29-152">**Tipo de anexo**</span><span class="sxs-lookup"><span data-stu-id="e9b29-152">**Type of attachment**</span></span>|<span data-ttu-id="e9b29-153">**Identificador de interface a ser usado**</span><span class="sxs-lookup"><span data-stu-id="e9b29-153">**Interface identifier to use**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e9b29-154">Binária</span><span class="sxs-lookup"><span data-stu-id="e9b29-154">Binary</span></span>  <br/> |<span data-ttu-id="e9b29-155">IID_IStream</span><span class="sxs-lookup"><span data-stu-id="e9b29-155">IID_IStream</span></span>  <br/> |
|<span data-ttu-id="e9b29-156">String</span><span class="sxs-lookup"><span data-stu-id="e9b29-156">String</span></span>  <br/> |<span data-ttu-id="e9b29-157">IID_IStream</span><span class="sxs-lookup"><span data-stu-id="e9b29-157">IID_IStream</span></span>  <br/> |
|<span data-ttu-id="e9b29-158">Mensagem</span><span class="sxs-lookup"><span data-stu-id="e9b29-158">Message</span></span>  <br/> |<span data-ttu-id="e9b29-159">IID_IMessage</span><span class="sxs-lookup"><span data-stu-id="e9b29-159">IID_IMessage</span></span>  <br/> |
|<span data-ttu-id="e9b29-160">OLE 2.0</span><span class="sxs-lookup"><span data-stu-id="e9b29-160">OLE 2.0</span></span>  <br/> |<span data-ttu-id="e9b29-161">IID_IStreamDocfile</span><span class="sxs-lookup"><span data-stu-id="e9b29-161">IID_IStreamDocfile</span></span>  <br/> |
   
<span data-ttu-id="e9b29-162">**IStreamDocfile** é uma derivativa da interface [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) baseada em um arquivo composto OLE 2.0.</span><span class="sxs-lookup"><span data-stu-id="e9b29-162">**IStreamDocfile** is a derivative of the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface that is based on an OLE 2.0 compound file.</span></span> <span data-ttu-id="e9b29-163">**IStreamDocfile** é a melhor opção para acessar anexos OLE 2.0 porque envolve a menor quantidade de sobrecarga.</span><span class="sxs-lookup"><span data-stu-id="e9b29-163">**IStreamDocfile** is the best choice for accessing OLE 2.0 attachments because it involves the least amount of overhead.</span></span> <span data-ttu-id="e9b29-164">Você pode usar IID_IStreamDocFile para as propriedades que contêm dados armazenados em armazenamento estruturado disponível por meio da interface [IStorage.](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9b29-164">You can use IID_IStreamDocFile for those properties that contain data stored in structured storage available through the [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) interface.</span></span> 
  
<span data-ttu-id="e9b29-165">For more information about how to use **OpenProperty** with attachments, see the **PR_ATTACH_DATA_OBJ** property and [Opening an Attachment](opening-an-attachment.md).</span><span class="sxs-lookup"><span data-stu-id="e9b29-165">For more information about how to use **OpenProperty** with attachments, see the **PR_ATTACH_DATA_OBJ** property and [Opening an Attachment](opening-an-attachment.md).</span></span>
  
<span data-ttu-id="e9b29-166">Não use o ponteiro **IStream** recebido para chamar o método [Seek](https://msdn.microsoft.com/library/aa380043%28v=VS.85%29.aspx) ou [SetSize,](https://msdn.microsoft.com/library/aa380044%28v=VS.85%29.aspx) a menos que você use uma variável de posição zero ou tamanho.</span><span class="sxs-lookup"><span data-stu-id="e9b29-166">Do not use the **IStream** pointer that you receive to call either its [Seek](https://msdn.microsoft.com/library/aa380043%28v=VS.85%29.aspx) or [SetSize](https://msdn.microsoft.com/library/aa380044%28v=VS.85%29.aspx) method unless you use a zero position or size variable.</span></span> <span data-ttu-id="e9b29-167">Além disso, não confie no valor do parâmetro de saída _plibNewPosition_ retornado da **chamada Seek.**</span><span class="sxs-lookup"><span data-stu-id="e9b29-167">Also, do not rely on the value of the  _plibNewPosition_ output parameter returned from the **Seek** call.</span></span> 
  
<span data-ttu-id="e9b29-168">Se você chamar **OpenProperty para** acessar uma propriedade com a interface **IStream,** use somente essa interface para fazer alterações a ela.</span><span class="sxs-lookup"><span data-stu-id="e9b29-168">If you call **OpenProperty** to access a property with the **IStream** interface, use only that interface to make changes to it.</span></span> <span data-ttu-id="e9b29-169">Não tente atualizar a propriedade com nenhum dos outros [métodos IMAPIProp : IUnknown,](imapipropiunknown.md) como **SetProps** ou [IMAPIProp::D eleteProps](imapiprop-deleteprops.md).</span><span class="sxs-lookup"><span data-stu-id="e9b29-169">Do not attempt to update the property with any of the other [IMAPIProp : IUnknown](imapipropiunknown.md) methods, such as **SetProps** or [IMAPIProp::DeleteProps](imapiprop-deleteprops.md).</span></span> 
  
<span data-ttu-id="e9b29-170">Não tente abrir uma propriedade com **OpenProperty** mais de uma vez.</span><span class="sxs-lookup"><span data-stu-id="e9b29-170">Do not try to open a property with **OpenProperty** more than once.</span></span> <span data-ttu-id="e9b29-171">Os resultados são indefinido porque podem variar de provedor para provedor.</span><span class="sxs-lookup"><span data-stu-id="e9b29-171">The results are undefined because they can vary from provider to provider.</span></span> 
  
<span data-ttu-id="e9b29-172">Se você precisar modificar a propriedade a ser aberta, de definida a MAPI_MODIFY sinalizador.</span><span class="sxs-lookup"><span data-stu-id="e9b29-172">If you need to modify the property to be opened, set the MAPI_MODIFY flag.</span></span> <span data-ttu-id="e9b29-173">Se você não tiver certeza se o objeto dá suporte à propriedade, mas acha que deve, de definida a MAPI_CREATE e MAPI_MODIFY sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="e9b29-173">If you are not sure whether the object supports the property but you think it should, set the MAPI_CREATE and MAPI_MODIFY flags.</span></span> <span data-ttu-id="e9b29-174">Sempre MAPI_CREATE configuração, MAPI_MODIFY também deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="e9b29-174">Whenever MAPI_CREATE is set, MAPI_MODIFY must also be set.</span></span>
  
<span data-ttu-id="e9b29-175">Você é responsável por recasting do ponteiro da interface retornado no parâmetro _lppUnk_ para um que seja apropriado para a interface especificada no parâmetro _lpiid._</span><span class="sxs-lookup"><span data-stu-id="e9b29-175">You are responsible for recasting the interface pointer returned in the  _lppUnk_ parameter to one that is appropriate for the interface specified in the  _lpiid_ parameter.</span></span> <span data-ttu-id="e9b29-176">Você também deve usar o ponteiro retornado para chamar seu [método IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) quando terminar.</span><span class="sxs-lookup"><span data-stu-id="e9b29-176">You must also use the returned pointer to call its [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method when you are finished with it.</span></span> 
  
<span data-ttu-id="e9b29-177">Às vezes, definir os sinalizadores no  _parâmetro ulFlags_ não é suficiente para indicar o tipo de acesso à propriedade necessária.</span><span class="sxs-lookup"><span data-stu-id="e9b29-177">Sometimes setting the flags in the  _ulFlags_ parameter is not enough to indicate the type of access to the property that is required.</span></span> <span data-ttu-id="e9b29-178">Você pode colocar dados adicionais, como sinalizadores, no _parâmetro ulInterfaceOptions._</span><span class="sxs-lookup"><span data-stu-id="e9b29-178">You can put additional data, such as flags, in the  _ulInterfaceOptions_ parameter.</span></span> <span data-ttu-id="e9b29-179">Esses dados dependem da interface.</span><span class="sxs-lookup"><span data-stu-id="e9b29-179">This data is interface dependent.</span></span> <span data-ttu-id="e9b29-180">Algumas interfaces (como **IStream**) o usam e outras não.</span><span class="sxs-lookup"><span data-stu-id="e9b29-180">Some interfaces (such as **IStream**) use it, and others do not.</span></span> <span data-ttu-id="e9b29-181">Por exemplo, quando você abre uma propriedade a ser modificada com **IStream**, de definir o sinalizador STGM_WRITE no  _parâmetro ulInterfaceOptions_ além de MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="e9b29-181">For example, when you open a property to be modified with **IStream**, set the STGM_WRITE flag in the  _ulInterfaceOptions_ parameter in addition to MAPI_MODIFY.</span></span> <span data-ttu-id="e9b29-182">Ao abrir uma tabela usando a interface [IMAPITable,](imapitableiunknown.md) você pode definir  _ulInterfaceOptions_ como MAPI_UNICODE para indicar se as colunas na tabela que reter as propriedades de cadeia de caracteres devem estar no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="e9b29-182">When you open a table by using the [IMAPITable](imapitableiunknown.md) interface, you can set  _ulInterfaceOptions_ to MAPI_UNICODE to indicate whether the columns in the table that hold string properties should be in Unicode format.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e9b29-183">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="e9b29-183">MFCMAPI reference</span></span>

<span data-ttu-id="e9b29-184">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e9b29-184">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e9b29-185">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="e9b29-185">**File**</span></span>|<span data-ttu-id="e9b29-186">**Função**</span><span class="sxs-lookup"><span data-stu-id="e9b29-186">**Function**</span></span>|<span data-ttu-id="e9b29-187">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="e9b29-187">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e9b29-188">StreamEditor.cpp</span><span class="sxs-lookup"><span data-stu-id="e9b29-188">StreamEditor.cpp</span></span>  <br/> |<span data-ttu-id="e9b29-189">CStreamEditor::ReadTextStreamFromProperty</span><span class="sxs-lookup"><span data-stu-id="e9b29-189">CStreamEditor::ReadTextStreamFromProperty</span></span>  <br/> |<span data-ttu-id="e9b29-190">MFCMAPI usa o **método IMAPIProp::OpenProperty** para recuperar uma interface de fluxo para texto grande e propriedades binárias.</span><span class="sxs-lookup"><span data-stu-id="e9b29-190">MFCMAPI uses the **IMAPIProp::OpenProperty** method to retrieve a stream interface for large text and binary properties.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e9b29-191">Confira também</span><span class="sxs-lookup"><span data-stu-id="e9b29-191">See also</span></span>

- [<span data-ttu-id="e9b29-192">HrIStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="e9b29-192">HrIStorageFromStream</span></span>](hristoragefromstream.md) 
- [<span data-ttu-id="e9b29-193">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="e9b29-193">IMAPIProp::DeleteProps</span></span>](imapiprop-deleteprops.md) 
- [<span data-ttu-id="e9b29-194">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="e9b29-194">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
- [<span data-ttu-id="e9b29-195">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="e9b29-195">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
- [<span data-ttu-id="e9b29-196">IMAPISupport::IStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="e9b29-196">IMAPISupport::IStorageFromStream</span></span>](imapisupport-istoragefromstream.md)
- [<span data-ttu-id="e9b29-197">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e9b29-197">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
- [<span data-ttu-id="e9b29-198">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e9b29-198">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
- [<span data-ttu-id="e9b29-199">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="e9b29-199">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
- [<span data-ttu-id="e9b29-200">Abrir um anexo</span><span class="sxs-lookup"><span data-stu-id="e9b29-200">Opening an Attachment</span></span>](opening-an-attachment.md)

