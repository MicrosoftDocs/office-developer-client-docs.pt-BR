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
ms.openlocfilehash: 656e5c5532edfc6c791ca30aa30f4c4d96847295
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767153"
---
# <a name="imapipropopenproperty"></a><span data-ttu-id="7c38b-103">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="7c38b-103">IMAPIProp::OpenProperty</span></span>

<span data-ttu-id="7c38b-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7c38b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7c38b-105">Retorna um ponteiro para uma interface que pode ser usada para acessar uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="7c38b-105">Returns a pointer to an interface that can be used to access a property.</span></span>
  
```cpp
HRESULT OpenProperty(
  ULONG ulPropTag,
  LPCIID lpiid,
  ULONG ulInterfaceOptions,
  ULONG ulFlags,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="7c38b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7c38b-106">Parameters</span></span>

 <span data-ttu-id="7c38b-107">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="7c38b-107">_ulPropTag_</span></span>
  
> <span data-ttu-id="7c38b-108">[in] A marca de propriedade para a propriedade a ser acessado.</span><span class="sxs-lookup"><span data-stu-id="7c38b-108">[in] The property tag for the property to be accessed.</span></span> <span data-ttu-id="7c38b-109">O identificador do e o tipo devem ser incluídos na marca de propriedade.</span><span class="sxs-lookup"><span data-stu-id="7c38b-109">Both the identifier and the type must be included in the property tag.</span></span>
    
 <span data-ttu-id="7c38b-110">_lpiid_</span><span class="sxs-lookup"><span data-stu-id="7c38b-110">_lpiid_</span></span>
  
> <span data-ttu-id="7c38b-111">[in] Um ponteiro para o identificador para a interface que será usada para acessar a propriedade.</span><span class="sxs-lookup"><span data-stu-id="7c38b-111">[in] A pointer to the identifier for the interface to be used to access the property.</span></span> <span data-ttu-id="7c38b-112">O parâmetro _lpiid_ não deve ser **nula**.</span><span class="sxs-lookup"><span data-stu-id="7c38b-112">The  _lpiid_ parameter must not be **null**.</span></span>
    
 <span data-ttu-id="7c38b-113">_ulInterfaceOptions_</span><span class="sxs-lookup"><span data-stu-id="7c38b-113">_ulInterfaceOptions_</span></span>
  
> <span data-ttu-id="7c38b-114">[in] Dados relacionados à interface identificada pelo parâmetro _lpiid_ .</span><span class="sxs-lookup"><span data-stu-id="7c38b-114">[in] Data that relates to the interface identified by the  _lpiid_ parameter.</span></span> 
    
 <span data-ttu-id="7c38b-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7c38b-115">_ulFlags_</span></span>
  
> <span data-ttu-id="7c38b-116">[in] Uma bitmask dos sinalizadores que controla o acesso à propriedade.</span><span class="sxs-lookup"><span data-stu-id="7c38b-116">[in] A bitmask of flags that controls access to the property.</span></span> <span data-ttu-id="7c38b-117">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="7c38b-117">The following flags can be set:</span></span>
    
<span data-ttu-id="7c38b-118">MAPI_CREATE</span><span class="sxs-lookup"><span data-stu-id="7c38b-118">MAPI_CREATE</span></span> 
  
> <span data-ttu-id="7c38b-119">Se a propriedade não existir, ele deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="7c38b-119">If the property does not exist, it should be created.</span></span> <span data-ttu-id="7c38b-120">Se a propriedade existir, o valor atual da propriedade deverão ser descartado.</span><span class="sxs-lookup"><span data-stu-id="7c38b-120">If the property does exist, the current value of the property should be discarded.</span></span> <span data-ttu-id="7c38b-121">Quando um chamador define o sinalizador MAPI_CREATE, ele também deve definir o sinalizador MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="7c38b-121">When a caller sets the MAPI_CREATE flag, it should also set the MAPI_MODIFY flag.</span></span>
    
<span data-ttu-id="7c38b-122">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="7c38b-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="7c38b-123">Permite **OpenProperty** retornar com êxito, possivelmente antes que o objeto esteja totalmente disponível ao chamador.</span><span class="sxs-lookup"><span data-stu-id="7c38b-123">Allows **OpenProperty** to return successfully, possibly before the object is fully available to the caller.</span></span> <span data-ttu-id="7c38b-124">Se o objeto não estiver disponível, fazendo uma chamada do objeto subsequente pode gerar um erro.</span><span class="sxs-lookup"><span data-stu-id="7c38b-124">If the object is not available, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="7c38b-125">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="7c38b-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="7c38b-126">Nesses casos, é necessário MAPI_MODIFY:</span><span class="sxs-lookup"><span data-stu-id="7c38b-126">MAPI_MODIFY is required in these situations:</span></span>
    
  - <span data-ttu-id="7c38b-127">Ao abrir uma propriedade de stream, como **IID_IStream**, para modificá-la.</span><span class="sxs-lookup"><span data-stu-id="7c38b-127">When opening a stream property, such as **IID_IStream**, to modify it.</span></span>
    
  - <span data-ttu-id="7c38b-128">Ao abrir um anexo de mensagens inseridas, como [PR_ATTACH_DATA_OBJ](pidtagattachdataobject-canonical-property.md) aberto com **IID_IMessage**, para modificá-la.</span><span class="sxs-lookup"><span data-stu-id="7c38b-128">When opening an embedded message attachment, such as [PR_ATTACH_DATA_OBJ](pidtagattachdataobject-canonical-property.md) opened with **IID_IMessage**, to modify it.</span></span>
    
 <span data-ttu-id="7c38b-129">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="7c38b-129">_lppUnk_</span></span>
  
> <span data-ttu-id="7c38b-130">[out] Um ponteiro para a interface solicitada a ser usada para acesso à propriedade.</span><span class="sxs-lookup"><span data-stu-id="7c38b-130">[out] A pointer to the requested interface to be used for property access.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7c38b-131">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="7c38b-131">Return value</span></span>

<span data-ttu-id="7c38b-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="7c38b-132">S_OK</span></span> 
  
> <span data-ttu-id="7c38b-133">O ponteiro de interface solicitada foi retornado com êxito.</span><span class="sxs-lookup"><span data-stu-id="7c38b-133">The requested interface pointer was successfully returned.</span></span>
    
<span data-ttu-id="7c38b-134">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="7c38b-134">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="7c38b-135">A interface solicitada não é suportada para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="7c38b-135">The requested interface is not supported for this property.</span></span>
    
<span data-ttu-id="7c38b-136">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="7c38b-136">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="7c38b-137">O chamador tem permissões insuficientes para acessar a propriedade.</span><span class="sxs-lookup"><span data-stu-id="7c38b-137">The caller has insufficient permissions to access the property.</span></span>
    
<span data-ttu-id="7c38b-138">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="7c38b-138">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="7c38b-139">O objeto não pode fornecer acesso a essa propriedade por meio da interface solicitada.</span><span class="sxs-lookup"><span data-stu-id="7c38b-139">The object cannot provide access to this property through the requested interface.</span></span>
    
<span data-ttu-id="7c38b-140">E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="7c38b-140">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="7c38b-141">A propriedade solicitada não existe e MAPI_CREATE não foi definida no parâmetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="7c38b-141">The requested property does not exist and MAPI_CREATE was not set in the  _ulFlags_ parameter.</span></span> 
    
<span data-ttu-id="7c38b-142">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7c38b-142">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="7c38b-143">O tipo de propriedade na marca é definido como PT_UNSPECIFIED.</span><span class="sxs-lookup"><span data-stu-id="7c38b-143">The property type in the tag is set to PT_UNSPECIFIED.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7c38b-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="7c38b-144">Remarks</span></span>

<span data-ttu-id="7c38b-145">O método **IMAPIProp::OpenProperty** fornece acesso a uma propriedade por meio de uma interface específica.</span><span class="sxs-lookup"><span data-stu-id="7c38b-145">The **IMAPIProp::OpenProperty** method provides access to a property through a particular interface.</span></span> <span data-ttu-id="7c38b-146">**OpenProperty** é uma alternativa para os métodos [IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPIProp::SetProps](imapiprop-setprops.md) .</span><span class="sxs-lookup"><span data-stu-id="7c38b-146">**OpenProperty** is an alternative to the [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPIProp::SetProps](imapiprop-setprops.md) methods.</span></span> <span data-ttu-id="7c38b-147">Quando **GetProps** ou **SetProps** falha porque a propriedade é muito grande ou muito complexa, chame **OpenProperty**.</span><span class="sxs-lookup"><span data-stu-id="7c38b-147">When either **GetProps** or **SetProps** fails because the property is too large or too complex, call **OpenProperty**.</span></span> <span data-ttu-id="7c38b-148">**OpenProperty** geralmente é utilizado para acessar as propriedades do tipo PT_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="7c38b-148">**OpenProperty** is typically used to access properties of type PT_OBJECT.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7c38b-149">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="7c38b-149">Notes to callers</span></span>

<span data-ttu-id="7c38b-150">Para acessar os anexos de mensagens, abra a propriedade **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) com um identificador de interface diferente, dependendo do tipo de anexo.</span><span class="sxs-lookup"><span data-stu-id="7c38b-150">To access message attachments, open the **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property with a different interface identifier, depending on the type of attachment.</span></span> <span data-ttu-id="7c38b-151">A tabela a seguir descreve como chamar **OpenProperty** para os diferentes tipos de anexos:</span><span class="sxs-lookup"><span data-stu-id="7c38b-151">The following table describes how to call **OpenProperty** for the different types of attachments:</span></span> 
  
|<span data-ttu-id="7c38b-152">**Tipo de anexo**</span><span class="sxs-lookup"><span data-stu-id="7c38b-152">**Type of attachment**</span></span>|<span data-ttu-id="7c38b-153">**Identificador de interface usar**</span><span class="sxs-lookup"><span data-stu-id="7c38b-153">**Interface identifier to use**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7c38b-154">Binário</span><span class="sxs-lookup"><span data-stu-id="7c38b-154">Binary</span></span>  <br/> |<span data-ttu-id="7c38b-155">IID_IStream</span><span class="sxs-lookup"><span data-stu-id="7c38b-155">IID_IStream</span></span>  <br/> |
|<span data-ttu-id="7c38b-156">String</span><span class="sxs-lookup"><span data-stu-id="7c38b-156">String</span></span>  <br/> |<span data-ttu-id="7c38b-157">IID_IStream</span><span class="sxs-lookup"><span data-stu-id="7c38b-157">IID_IStream</span></span>  <br/> |
|<span data-ttu-id="7c38b-158">Message</span><span class="sxs-lookup"><span data-stu-id="7c38b-158">Message</span></span>  <br/> |<span data-ttu-id="7c38b-159">IID_IMessage</span><span class="sxs-lookup"><span data-stu-id="7c38b-159">IID_IMessage</span></span>  <br/> |
|<span data-ttu-id="7c38b-160">OLE 2.0</span><span class="sxs-lookup"><span data-stu-id="7c38b-160">OLE 2.0</span></span>  <br/> |<span data-ttu-id="7c38b-161">IID_IStreamDocfile</span><span class="sxs-lookup"><span data-stu-id="7c38b-161">IID_IStreamDocfile</span></span>  <br/> |
   
<span data-ttu-id="7c38b-162">**IStreamDocfile** é um derivado da interface [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) que baseia-se em um arquivo de compostos OLE 2.0.</span><span class="sxs-lookup"><span data-stu-id="7c38b-162">**IStreamDocfile** is a derivative of the [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) interface that is based on an OLE 2.0 compound file.</span></span> <span data-ttu-id="7c38b-163">**IStreamDocfile** é a melhor opção para acessar os anexos OLE 2.0 porque envolve o mínimo de sobrecarga.</span><span class="sxs-lookup"><span data-stu-id="7c38b-163">**IStreamDocfile** is the best choice for accessing OLE 2.0 attachments because it involves the least amount of overhead.</span></span> <span data-ttu-id="7c38b-164">Você pode usar o IID_IStreamDocFile para essas propriedades que contenham dados armazenados em armazenamento estruturado disponível por meio da interface [IStorage](http://msdn.microsoft.com/en-us/library/aa380015%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="7c38b-164">You can use IID_IStreamDocFile for those properties that contain data stored in structured storage available through the [IStorage](http://msdn.microsoft.com/en-us/library/aa380015%28VS.85%29.aspx) interface.</span></span> 
  
<span data-ttu-id="7c38b-165">Para obter mais informações sobre como usar **OpenProperty** com anexos, consulte a propriedade **PR_ATTACH_DATA_OBJ** e a [abertura de um anexo](opening-an-attachment.md).</span><span class="sxs-lookup"><span data-stu-id="7c38b-165">For more information about how to use **OpenProperty** with attachments, see the **PR_ATTACH_DATA_OBJ** property and [Opening an Attachment](opening-an-attachment.md).</span></span>
  
<span data-ttu-id="7c38b-166">Não use o ponteiro de **IStream** recebidos para chamar o método seu [Seek](http://msdn.microsoft.com/en-us/library/aa380043%28v=VS.85%29.aspx) ou [SetSize](http://msdn.microsoft.com/en-us/library/aa380044%28v=VS.85%29.aspx) , a menos que você use uma zero variável de tamanho ou posição.</span><span class="sxs-lookup"><span data-stu-id="7c38b-166">Do not use the **IStream** pointer that you receive to call either its [Seek](http://msdn.microsoft.com/en-us/library/aa380043%28v=VS.85%29.aspx) or [SetSize](http://msdn.microsoft.com/en-us/library/aa380044%28v=VS.85%29.aspx) method unless you use a zero position or size variable.</span></span> <span data-ttu-id="7c38b-167">Além disso, não confie no valor do parâmetro de saída _plibNewPosition_ retornado da chamada **Seek** .</span><span class="sxs-lookup"><span data-stu-id="7c38b-167">Also, do not rely on the value of the  _plibNewPosition_ output parameter returned from the **Seek** call.</span></span> 
  
<span data-ttu-id="7c38b-168">Se você chamar **OpenProperty** para acessar uma propriedade com a interface **IStream** , use apenas essa interface para fazer alterações nele.</span><span class="sxs-lookup"><span data-stu-id="7c38b-168">If you call **OpenProperty** to access a property with the **IStream** interface, use only that interface to make changes to it.</span></span> <span data-ttu-id="7c38b-169">Não tente atualizar a propriedade com qualquer uma das outras [IMAPIProp: IUnknown](imapipropiunknown.md) métodos, como **SetProps** ou [IMAPIProp::DeleteProps](imapiprop-deleteprops.md).</span><span class="sxs-lookup"><span data-stu-id="7c38b-169">Do not attempt to update the property with any of the other [IMAPIProp : IUnknown](imapipropiunknown.md) methods, such as **SetProps** or [IMAPIProp::DeleteProps](imapiprop-deleteprops.md).</span></span> 
  
<span data-ttu-id="7c38b-170">Não tente abrir uma propriedade com **OpenProperty** mais de uma vez.</span><span class="sxs-lookup"><span data-stu-id="7c38b-170">Do not try to open a property with **OpenProperty** more than once.</span></span> <span data-ttu-id="7c38b-171">Os resultados são indefinidos porque eles podem variar de provedor.</span><span class="sxs-lookup"><span data-stu-id="7c38b-171">The results are undefined because they can vary from provider to provider.</span></span> 
  
<span data-ttu-id="7c38b-172">Se você precisar modificar a propriedade a ser aberto, defina o sinalizador MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="7c38b-172">If you need to modify the property to be opened, set the MAPI_MODIFY flag.</span></span> <span data-ttu-id="7c38b-173">Se não esteja certo se o objeto oferece suporte à propriedade, mas você acha que deveria, defina os sinalizadores MAPI_CREATE e MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="7c38b-173">If you are not sure whether the object supports the property but you think it should, set the MAPI_CREATE and MAPI_MODIFY flags.</span></span> <span data-ttu-id="7c38b-174">Sempre que MAPI_CREATE for definido, MAPI_MODIFY também deve ser definida.</span><span class="sxs-lookup"><span data-stu-id="7c38b-174">Whenever MAPI_CREATE is set, MAPI_MODIFY must also be set.</span></span>
  
<span data-ttu-id="7c38b-175">Você é responsável por reformulação o ponteiro de interface retornado no parâmetro _lppUnk_ para um que é apropriado para a interface especificada no parâmetro _lpiid_ .</span><span class="sxs-lookup"><span data-stu-id="7c38b-175">You are responsible for recasting the interface pointer returned in the  _lppUnk_ parameter to one that is appropriate for the interface specified in the  _lpiid_ parameter.</span></span> <span data-ttu-id="7c38b-176">Você também deve usar o ponteiro retornado para chamar seu método de [IUnknown:: Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) quando terminar com ele.</span><span class="sxs-lookup"><span data-stu-id="7c38b-176">You must also use the returned pointer to call its [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) method when you are finished with it.</span></span> 
  
<span data-ttu-id="7c38b-177">Em alguns casos, definindo os sinalizadores no parâmetro _ulFlags_ não é suficiente para indicar o tipo de acesso para a propriedade que é necessário.</span><span class="sxs-lookup"><span data-stu-id="7c38b-177">Sometimes setting the flags in the  _ulFlags_ parameter is not enough to indicate the type of access to the property that is required.</span></span> <span data-ttu-id="7c38b-178">Você pode colocar os dados adicionais, como sinalizadores, no parâmetro _ulInterfaceOptions_ .</span><span class="sxs-lookup"><span data-stu-id="7c38b-178">You can put additional data, such as flags, in the  _ulInterfaceOptions_ parameter.</span></span> <span data-ttu-id="7c38b-179">Esses dados são dependentes de interface.</span><span class="sxs-lookup"><span data-stu-id="7c38b-179">This data is interface dependent.</span></span> <span data-ttu-id="7c38b-180">Algumas interfaces (por exemplo, **IStream**) usá-lo e outros não.</span><span class="sxs-lookup"><span data-stu-id="7c38b-180">Some interfaces (such as **IStream**) use it, and others do not.</span></span> <span data-ttu-id="7c38b-181">Por exemplo, quando você abre uma propriedade a ser modificado com **IStream**, defina o sinalizador STGM_WRITE no parâmetro _ulInterfaceOptions_ além dos MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="7c38b-181">For example, when you open a property to be modified with **IStream**, set the STGM_WRITE flag in the  _ulInterfaceOptions_ parameter in addition to MAPI_MODIFY.</span></span> <span data-ttu-id="7c38b-182">Quando você abre uma tabela por meio da interface [IMAPITable](imapitableiunknown.md) , você pode definir _ulInterfaceOptions_ como MAPI_UNICODE para indicar se as colunas na tabela que armazenam as propriedades de cadeia de caracteres devem estar no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="7c38b-182">When you open a table by using the [IMAPITable](imapitableiunknown.md) interface, you can set  _ulInterfaceOptions_ to MAPI_UNICODE to indicate whether the columns in the table that hold string properties should be in Unicode format.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7c38b-183">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="7c38b-183">MFCMAPI reference</span></span>

<span data-ttu-id="7c38b-184">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="7c38b-184">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7c38b-185">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="7c38b-185">**File**</span></span>|<span data-ttu-id="7c38b-186">**Function**</span><span class="sxs-lookup"><span data-stu-id="7c38b-186">**Function**</span></span>|<span data-ttu-id="7c38b-187">**Comment**</span><span class="sxs-lookup"><span data-stu-id="7c38b-187">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7c38b-188">StreamEditor.cpp</span><span class="sxs-lookup"><span data-stu-id="7c38b-188">StreamEditor.cpp</span></span>  <br/> |<span data-ttu-id="7c38b-189">CStreamEditor::ReadTextStreamFromProperty</span><span class="sxs-lookup"><span data-stu-id="7c38b-189">CStreamEditor::ReadTextStreamFromProperty</span></span>  <br/> |<span data-ttu-id="7c38b-190">MFCMAPI usa o método **IMAPIProp::OpenProperty** para recuperar uma interface de fluxo de texto grande e propriedades binárias.</span><span class="sxs-lookup"><span data-stu-id="7c38b-190">MFCMAPI uses the **IMAPIProp::OpenProperty** method to retrieve a stream interface for large text and binary properties.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7c38b-191">Confira também</span><span class="sxs-lookup"><span data-stu-id="7c38b-191">See also</span></span>

- [<span data-ttu-id="7c38b-192">HrIStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="7c38b-192">HrIStorageFromStream</span></span>](hristoragefromstream.md) 
- [<span data-ttu-id="7c38b-193">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="7c38b-193">IMAPIProp::DeleteProps</span></span>](imapiprop-deleteprops.md) 
- [<span data-ttu-id="7c38b-194">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="7c38b-194">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
- [<span data-ttu-id="7c38b-195">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="7c38b-195">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
- [<span data-ttu-id="7c38b-196">IMAPISupport::IStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="7c38b-196">IMAPISupport::IStorageFromStream</span></span>](imapisupport-istoragefromstream.md)
- [<span data-ttu-id="7c38b-197">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7c38b-197">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
- [<span data-ttu-id="7c38b-198">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7c38b-198">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
- [<span data-ttu-id="7c38b-199">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="7c38b-199">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
- [<span data-ttu-id="7c38b-200">Abrir um anexo</span><span class="sxs-lookup"><span data-stu-id="7c38b-200">Opening an Attachment</span></span>](opening-an-attachment.md)

