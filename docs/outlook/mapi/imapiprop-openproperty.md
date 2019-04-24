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
# <a name="imapipropopenproperty"></a><span data-ttu-id="9f959-103">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="9f959-103">IMAPIProp::OpenProperty</span></span>

<span data-ttu-id="9f959-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9f959-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9f959-105">Retorna um ponteiro para uma interface que pode ser usada para acessar uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="9f959-105">Returns a pointer to an interface that can be used to access a property.</span></span>
  
```cpp
HRESULT OpenProperty(
  ULONG ulPropTag,
  LPCIID lpiid,
  ULONG ulInterfaceOptions,
  ULONG ulFlags,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="9f959-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9f959-106">Parameters</span></span>

 <span data-ttu-id="9f959-107">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="9f959-107">_ulPropTag_</span></span>
  
> <span data-ttu-id="9f959-108">no A marca de propriedade da propriedade a ser acessada.</span><span class="sxs-lookup"><span data-stu-id="9f959-108">[in] The property tag for the property to be accessed.</span></span> <span data-ttu-id="9f959-109">Tanto o identificador quanto o tipo devem ser incluídos na marca da propriedade.</span><span class="sxs-lookup"><span data-stu-id="9f959-109">Both the identifier and the type must be included in the property tag.</span></span>
    
 <span data-ttu-id="9f959-110">_lpiid_</span><span class="sxs-lookup"><span data-stu-id="9f959-110">_lpiid_</span></span>
  
> <span data-ttu-id="9f959-111">no Um ponteiro para o identificador da interface a ser usada para acessar a propriedade.</span><span class="sxs-lookup"><span data-stu-id="9f959-111">[in] A pointer to the identifier for the interface to be used to access the property.</span></span> <span data-ttu-id="9f959-112">O parâmetro _lpiid_ não deve ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="9f959-112">The  _lpiid_ parameter must not be **null**.</span></span>
    
 <span data-ttu-id="9f959-113">_ulInterfaceOptions_</span><span class="sxs-lookup"><span data-stu-id="9f959-113">_ulInterfaceOptions_</span></span>
  
> <span data-ttu-id="9f959-114">no Dados relacionados à interface identificada pelo parâmetro _lpiid_ .</span><span class="sxs-lookup"><span data-stu-id="9f959-114">[in] Data that relates to the interface identified by the  _lpiid_ parameter.</span></span> 
    
 <span data-ttu-id="9f959-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9f959-115">_ulFlags_</span></span>
  
> <span data-ttu-id="9f959-116">no Uma bitmask de sinalizadores que controla o acesso à propriedade.</span><span class="sxs-lookup"><span data-stu-id="9f959-116">[in] A bitmask of flags that controls access to the property.</span></span> <span data-ttu-id="9f959-117">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="9f959-117">The following flags can be set:</span></span>
    
<span data-ttu-id="9f959-118">MAPI_CREATE</span><span class="sxs-lookup"><span data-stu-id="9f959-118">MAPI_CREATE</span></span> 
  
> <span data-ttu-id="9f959-119">Se a propriedade não existir, ela deverá ser criada.</span><span class="sxs-lookup"><span data-stu-id="9f959-119">If the property does not exist, it should be created.</span></span> <span data-ttu-id="9f959-120">Se a propriedade existir, o valor atual da propriedade deverá ser Descartado.</span><span class="sxs-lookup"><span data-stu-id="9f959-120">If the property does exist, the current value of the property should be discarded.</span></span> <span data-ttu-id="9f959-121">Quando um chamador define o sinalizador MAPI_CREATE, ele também deve definir o sinalizador MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="9f959-121">When a caller sets the MAPI_CREATE flag, it should also set the MAPI_MODIFY flag.</span></span>
    
<span data-ttu-id="9f959-122">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="9f959-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="9f959-123">Permite \*\*\*\* que OpenProperty seja retornado com êxito, possivelmente antes que o objeto esteja totalmente disponível para o chamador.</span><span class="sxs-lookup"><span data-stu-id="9f959-123">Allows **OpenProperty** to return successfully, possibly before the object is fully available to the caller.</span></span> <span data-ttu-id="9f959-124">Se o objeto não estiver disponível, fazer uma chamada de objeto subsequente poderá gerar um erro.</span><span class="sxs-lookup"><span data-stu-id="9f959-124">If the object is not available, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="9f959-125">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="9f959-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="9f959-126">O MAPI_MODIFY é necessário nestas situações:</span><span class="sxs-lookup"><span data-stu-id="9f959-126">MAPI_MODIFY is required in these situations:</span></span>
    
  - <span data-ttu-id="9f959-127">Ao abrir uma propriedade Stream, como **IID_IStream**, para modificá-la.</span><span class="sxs-lookup"><span data-stu-id="9f959-127">When opening a stream property, such as **IID_IStream**, to modify it.</span></span>
    
  - <span data-ttu-id="9f959-128">Ao abrir um anexo de mensagem incorporado, como [PR_ATTACH_DATA_OBJ](pidtagattachdataobject-canonical-property.md) aberto com **IID_IMessage**, para modificá-lo.</span><span class="sxs-lookup"><span data-stu-id="9f959-128">When opening an embedded message attachment, such as [PR_ATTACH_DATA_OBJ](pidtagattachdataobject-canonical-property.md) opened with **IID_IMessage**, to modify it.</span></span>
    
 <span data-ttu-id="9f959-129">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="9f959-129">_lppUnk_</span></span>
  
> <span data-ttu-id="9f959-130">bota Um ponteiro para a interface solicitada a ser usada para acesso de propriedade.</span><span class="sxs-lookup"><span data-stu-id="9f959-130">[out] A pointer to the requested interface to be used for property access.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9f959-131">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9f959-131">Return value</span></span>

<span data-ttu-id="9f959-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="9f959-132">S_OK</span></span> 
  
> <span data-ttu-id="9f959-133">O ponteiro de interface solicitado foi retornado com êxito.</span><span class="sxs-lookup"><span data-stu-id="9f959-133">The requested interface pointer was successfully returned.</span></span>
    
<span data-ttu-id="9f959-134">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="9f959-134">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="9f959-135">A interface solicitada não tem suporte para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="9f959-135">The requested interface is not supported for this property.</span></span>
    
<span data-ttu-id="9f959-136">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="9f959-136">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="9f959-137">O chamador tem permissões insuficientes para acessar a propriedade.</span><span class="sxs-lookup"><span data-stu-id="9f959-137">The caller has insufficient permissions to access the property.</span></span>
    
<span data-ttu-id="9f959-138">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="9f959-138">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="9f959-139">O objeto não pode fornecer acesso a essa propriedade por meio da interface solicitada.</span><span class="sxs-lookup"><span data-stu-id="9f959-139">The object cannot provide access to this property through the requested interface.</span></span>
    
<span data-ttu-id="9f959-140">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="9f959-140">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="9f959-141">A propriedade solicitada não existe e MAPI_CREATE não foi definida no parâmetro _parâmetroulflags_ .</span><span class="sxs-lookup"><span data-stu-id="9f959-141">The requested property does not exist and MAPI_CREATE was not set in the  _ulFlags_ parameter.</span></span> 
    
<span data-ttu-id="9f959-142">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9f959-142">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="9f959-143">O tipo de propriedade na marca é definido como PT_UNSPECIFIED.</span><span class="sxs-lookup"><span data-stu-id="9f959-143">The property type in the tag is set to PT_UNSPECIFIED.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9f959-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="9f959-144">Remarks</span></span>

<span data-ttu-id="9f959-145">O método **IMAPIProp:: OpenProperty** fornece acesso a uma propriedade por meio de uma interface específica.</span><span class="sxs-lookup"><span data-stu-id="9f959-145">The **IMAPIProp::OpenProperty** method provides access to a property through a particular interface.</span></span> <span data-ttu-id="9f959-146">**OpenProperty** é uma alternativa para os métodos [IMAPIProp::](imapiprop-getprops.md) GetProps e [IMAPIProp::](imapiprop-setprops.md) SetProps.</span><span class="sxs-lookup"><span data-stu-id="9f959-146">**OpenProperty** is an alternative to the [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPIProp::SetProps](imapiprop-setprops.md) methods.</span></span> <span data-ttu-id="9f959-147">Quando getProps ou setProps falham porque a propriedade é muito grande ou muito complexa, chame **OpenProperty**. \*\*\*\* \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="9f959-147">When either **GetProps** or **SetProps** fails because the property is too large or too complex, call **OpenProperty**.</span></span> <span data-ttu-id="9f959-148">**OpenProperty** normalmente é usado para acessar propriedades do tipo PT_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="9f959-148">**OpenProperty** is typically used to access properties of type PT_OBJECT.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9f959-149">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="9f959-149">Notes to callers</span></span>

<span data-ttu-id="9f959-150">Para acessar os anexos de mensagens, abra a propriedade **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) com um identificador de interface diferente, dependendo do tipo de anexo.</span><span class="sxs-lookup"><span data-stu-id="9f959-150">To access message attachments, open the **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property with a different interface identifier, depending on the type of attachment.</span></span> <span data-ttu-id="9f959-151">A tabela a seguir descreve como chamar **OpenProperty** para os diferentes tipos de anexos:</span><span class="sxs-lookup"><span data-stu-id="9f959-151">The following table describes how to call **OpenProperty** for the different types of attachments:</span></span> 
  
|<span data-ttu-id="9f959-152">**Tipo de anexo**</span><span class="sxs-lookup"><span data-stu-id="9f959-152">**Type of attachment**</span></span>|<span data-ttu-id="9f959-153">**Identificador de interface a ser usado**</span><span class="sxs-lookup"><span data-stu-id="9f959-153">**Interface identifier to use**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9f959-154">Binary</span><span class="sxs-lookup"><span data-stu-id="9f959-154">Binary</span></span>  <br/> |<span data-ttu-id="9f959-155">IID_IStream</span><span class="sxs-lookup"><span data-stu-id="9f959-155">IID_IStream</span></span>  <br/> |
|<span data-ttu-id="9f959-156">String</span><span class="sxs-lookup"><span data-stu-id="9f959-156">String</span></span>  <br/> |<span data-ttu-id="9f959-157">IID_IStream</span><span class="sxs-lookup"><span data-stu-id="9f959-157">IID_IStream</span></span>  <br/> |
|<span data-ttu-id="9f959-158">Mensagem</span><span class="sxs-lookup"><span data-stu-id="9f959-158">Message</span></span>  <br/> |<span data-ttu-id="9f959-159">IID_IMessage</span><span class="sxs-lookup"><span data-stu-id="9f959-159">IID_IMessage</span></span>  <br/> |
|<span data-ttu-id="9f959-160">OLE 2,0</span><span class="sxs-lookup"><span data-stu-id="9f959-160">OLE 2.0</span></span>  <br/> |<span data-ttu-id="9f959-161">IID_IStreamDocfile</span><span class="sxs-lookup"><span data-stu-id="9f959-161">IID_IStreamDocfile</span></span>  <br/> |
   
<span data-ttu-id="9f959-162">**IStreamDocfile** é uma derivada da interface [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) que se baseia em um arquivo composto OLE 2,0.</span><span class="sxs-lookup"><span data-stu-id="9f959-162">**IStreamDocfile** is a derivative of the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface that is based on an OLE 2.0 compound file.</span></span> <span data-ttu-id="9f959-163">**IStreamDocfile** é a melhor opção para acessar anexos de OLE 2,0 porque envolve a menor quantidade de sobrecarga.</span><span class="sxs-lookup"><span data-stu-id="9f959-163">**IStreamDocfile** is the best choice for accessing OLE 2.0 attachments because it involves the least amount of overhead.</span></span> <span data-ttu-id="9f959-164">Você pode usar IID_IStreamDocFile para as propriedades que contenham dados armazenados em um armazenamento estruturado disponível através da interface [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="9f959-164">You can use IID_IStreamDocFile for those properties that contain data stored in structured storage available through the [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) interface.</span></span> 
  
<span data-ttu-id="9f959-165">Para obter mais informações sobre como usar **OpenProperty** com anexos, consulte a propriedade **PR_ATTACH_DATA_OBJ** e [abrir um anexo](opening-an-attachment.md).</span><span class="sxs-lookup"><span data-stu-id="9f959-165">For more information about how to use **OpenProperty** with attachments, see the **PR_ATTACH_DATA_OBJ** property and [Opening an Attachment](opening-an-attachment.md).</span></span>
  
<span data-ttu-id="9f959-166">Não use o ponteiro de **IStream** que você recebeu para chamar o método [Seek](https://msdn.microsoft.com/library/aa380043%28v=VS.85%29.aspx) ou [SetSize](https://msdn.microsoft.com/library/aa380044%28v=VS.85%29.aspx) , a menos que você use uma posição zero de tamanho ou variável.</span><span class="sxs-lookup"><span data-stu-id="9f959-166">Do not use the **IStream** pointer that you receive to call either its [Seek](https://msdn.microsoft.com/library/aa380043%28v=VS.85%29.aspx) or [SetSize](https://msdn.microsoft.com/library/aa380044%28v=VS.85%29.aspx) method unless you use a zero position or size variable.</span></span> <span data-ttu-id="9f959-167">Além disso, não confie no valor do parâmetro de saída _plibNewPosition_ retornado da chamada de **busca** .</span><span class="sxs-lookup"><span data-stu-id="9f959-167">Also, do not rely on the value of the  _plibNewPosition_ output parameter returned from the **Seek** call.</span></span> 
  
<span data-ttu-id="9f959-168">Se você chamar **OpenProperty** para acessar uma propriedade com a interface **IStream** , use somente essa interface para fazer alterações nele.</span><span class="sxs-lookup"><span data-stu-id="9f959-168">If you call **OpenProperty** to access a property with the **IStream** interface, use only that interface to make changes to it.</span></span> <span data-ttu-id="9f959-169">Não tente atualizar a propriedade com nenhum dos outros métodos [IMAPIProp: IUnknown](imapipropiunknown.md) , como SetProps ou \*\*\*\* [IMAPIProp::D eleteprops](imapiprop-deleteprops.md).</span><span class="sxs-lookup"><span data-stu-id="9f959-169">Do not attempt to update the property with any of the other [IMAPIProp : IUnknown](imapipropiunknown.md) methods, such as **SetProps** or [IMAPIProp::DeleteProps](imapiprop-deleteprops.md).</span></span> 
  
<span data-ttu-id="9f959-170">Não tente abrir uma propriedade com OpenProperty \*\*\*\* mais de uma vez.</span><span class="sxs-lookup"><span data-stu-id="9f959-170">Do not try to open a property with **OpenProperty** more than once.</span></span> <span data-ttu-id="9f959-171">Os resultados estão indefinidos porque podem variar de provedor para provedor.</span><span class="sxs-lookup"><span data-stu-id="9f959-171">The results are undefined because they can vary from provider to provider.</span></span> 
  
<span data-ttu-id="9f959-172">Se você precisar modificar a propriedade a ser aberta, defina o sinalizador MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="9f959-172">If you need to modify the property to be opened, set the MAPI_MODIFY flag.</span></span> <span data-ttu-id="9f959-173">Se você não tem certeza se o objeto oferece suporte à propriedade, mas você acha que deveria, defina os sinalizadores MAPI_CREATE e MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="9f959-173">If you are not sure whether the object supports the property but you think it should, set the MAPI_CREATE and MAPI_MODIFY flags.</span></span> <span data-ttu-id="9f959-174">Sempre que MAPI_CREATE for definido, MAPI_MODIFY também deverá ser definido.</span><span class="sxs-lookup"><span data-stu-id="9f959-174">Whenever MAPI_CREATE is set, MAPI_MODIFY must also be set.</span></span>
  
<span data-ttu-id="9f959-175">Você é responsável por retransmitir o ponteiro de interface retornado no parâmetro _lppUnk_ para um que seja apropriado para a interface especificada no parâmetro _lpiid_ .</span><span class="sxs-lookup"><span data-stu-id="9f959-175">You are responsible for recasting the interface pointer returned in the  _lppUnk_ parameter to one that is appropriate for the interface specified in the  _lpiid_ parameter.</span></span> <span data-ttu-id="9f959-176">Você também deve usar o ponteiro retornado para chamar seu método [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) quando terminar de usá-lo.</span><span class="sxs-lookup"><span data-stu-id="9f959-176">You must also use the returned pointer to call its [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method when you are finished with it.</span></span> 
  
<span data-ttu-id="9f959-177">Às vezes, definir os sinalizadores no parâmetro _parâmetroulflags_ não é suficiente para indicar o tipo de acesso à propriedade que é necessária.</span><span class="sxs-lookup"><span data-stu-id="9f959-177">Sometimes setting the flags in the  _ulFlags_ parameter is not enough to indicate the type of access to the property that is required.</span></span> <span data-ttu-id="9f959-178">Você pode colocar dados adicionais, como sinalizadores, no parâmetro _ulInterfaceOptions_ .</span><span class="sxs-lookup"><span data-stu-id="9f959-178">You can put additional data, such as flags, in the  _ulInterfaceOptions_ parameter.</span></span> <span data-ttu-id="9f959-179">Esses dados são dependentes da interface.</span><span class="sxs-lookup"><span data-stu-id="9f959-179">This data is interface dependent.</span></span> <span data-ttu-id="9f959-180">Algumas interfaces (como **IStream**) o utilizam, e outras não.</span><span class="sxs-lookup"><span data-stu-id="9f959-180">Some interfaces (such as **IStream**) use it, and others do not.</span></span> <span data-ttu-id="9f959-181">Por exemplo, ao abrir uma propriedade a ser modificada com **IStream**, defina o sinalizador STGM_WRITE no parâmetro _ulInterfaceOptions_ , além de MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="9f959-181">For example, when you open a property to be modified with **IStream**, set the STGM_WRITE flag in the  _ulInterfaceOptions_ parameter in addition to MAPI_MODIFY.</span></span> <span data-ttu-id="9f959-182">Ao abrir uma tabela usando a interface imApitable, você pode definir _ulInterfaceOptions_ como MAPI_UNICODE para indicar se as colunas na tabela que contém as propriedades da cadeia de caracteres devem estar no formato Unicode. [](imapitableiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="9f959-182">When you open a table by using the [IMAPITable](imapitableiunknown.md) interface, you can set  _ulInterfaceOptions_ to MAPI_UNICODE to indicate whether the columns in the table that hold string properties should be in Unicode format.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9f959-183">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="9f959-183">MFCMAPI reference</span></span>

<span data-ttu-id="9f959-184">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="9f959-184">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9f959-185">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="9f959-185">**File**</span></span>|<span data-ttu-id="9f959-186">**Função**</span><span class="sxs-lookup"><span data-stu-id="9f959-186">**Function**</span></span>|<span data-ttu-id="9f959-187">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="9f959-187">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9f959-188">StreamEditor. cpp</span><span class="sxs-lookup"><span data-stu-id="9f959-188">StreamEditor.cpp</span></span>  <br/> |<span data-ttu-id="9f959-189">CStreamEditor:: ReadTextStreamFromProperty</span><span class="sxs-lookup"><span data-stu-id="9f959-189">CStreamEditor::ReadTextStreamFromProperty</span></span>  <br/> |<span data-ttu-id="9f959-190">MFCMAPI usa o método **IMAPIProp:: OpenProperty** para recuperar uma interface de fluxo para propriedades de texto e binário grandes.</span><span class="sxs-lookup"><span data-stu-id="9f959-190">MFCMAPI uses the **IMAPIProp::OpenProperty** method to retrieve a stream interface for large text and binary properties.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9f959-191">Confira também</span><span class="sxs-lookup"><span data-stu-id="9f959-191">See also</span></span>

- [<span data-ttu-id="9f959-192">HrIStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="9f959-192">HrIStorageFromStream</span></span>](hristoragefromstream.md) 
- [<span data-ttu-id="9f959-193">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="9f959-193">IMAPIProp::DeleteProps</span></span>](imapiprop-deleteprops.md) 
- [<span data-ttu-id="9f959-194">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="9f959-194">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
- [<span data-ttu-id="9f959-195">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="9f959-195">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
- [<span data-ttu-id="9f959-196">IMAPISupport::IStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="9f959-196">IMAPISupport::IStorageFromStream</span></span>](imapisupport-istoragefromstream.md)
- [<span data-ttu-id="9f959-197">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9f959-197">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
- [<span data-ttu-id="9f959-198">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9f959-198">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
- [<span data-ttu-id="9f959-199">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="9f959-199">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
- [<span data-ttu-id="9f959-200">Abrir um anexo</span><span class="sxs-lookup"><span data-stu-id="9f959-200">Opening an Attachment</span></span>](opening-an-attachment.md)

