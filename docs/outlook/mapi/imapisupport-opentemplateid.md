---
title: IMAPISupportOpenTemplateID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenTemplateID
api_type:
- COM
ms.assetid: 532f7af0-b2cc-49dd-b1de-e3ec1dc9a3e7
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 07aa508b473f4a87d5b4909f83771549c301a600
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418502"
---
# <a name="imapisupportopentemplateid"></a><span data-ttu-id="691ad-103">IMAPISupport::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="691ad-103">IMAPISupport::OpenTemplateID</span></span>

  
  
<span data-ttu-id="691ad-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="691ad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="691ad-105">Abre uma entrada de destinatário em um provedor de agendas externas.</span><span class="sxs-lookup"><span data-stu-id="691ad-105">Opens a recipient entry in a foreign address book provider.</span></span>
  
```cpp
HRESULT OpenTemplateID(
ULONG cbTemplateID,
LPENTRYID lpTemplateID,
ULONG ulTemplateFlags,
LPMAPIPROP lpMAPIPropData,
LPCIID lpInterface,
LPMAPIPROP FAR * lppMAPIPropNew,
LPMAPIPROP lpMAPIPropSibling
);
```

## <a name="parameters"></a><span data-ttu-id="691ad-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="691ad-106">Parameters</span></span>

 <span data-ttu-id="691ad-107">_cbTemplateID_</span><span class="sxs-lookup"><span data-stu-id="691ad-107">_cbTemplateID_</span></span>
  
> <span data-ttu-id="691ad-108">[in] A contagem de byte no identificador de modelo apontado por  _lpTemplateID_.</span><span class="sxs-lookup"><span data-stu-id="691ad-108">[in] The byte count in the template identifier pointed to by  _lpTemplateID_.</span></span> 
    
 <span data-ttu-id="691ad-109">_lpTemplateID_</span><span class="sxs-lookup"><span data-stu-id="691ad-109">_lpTemplateID_</span></span>
  
> <span data-ttu-id="691ad-110">[in] Um ponteiro para o identificador **de PR_TEMPLATEID** propriedade ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) da entrada do destinatário a ser aberta.</span><span class="sxs-lookup"><span data-stu-id="691ad-110">[in] A pointer to the template identifier **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property of the recipient entry to be opened.</span></span>
    
 <span data-ttu-id="691ad-111">_ulTemplateFlags_</span><span class="sxs-lookup"><span data-stu-id="691ad-111">_ulTemplateFlags_</span></span>
  
> <span data-ttu-id="691ad-112">[in] Uma máscara de bits de sinalizadores usada para descrever como abrir a entrada.</span><span class="sxs-lookup"><span data-stu-id="691ad-112">[in] A bitmask of flags used to describe how to open the entry.</span></span> <span data-ttu-id="691ad-113">O sinalizador a seguir pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="691ad-113">The following flag can be set:</span></span>
    
<span data-ttu-id="691ad-114">FILL_ENTRY</span><span class="sxs-lookup"><span data-stu-id="691ad-114">FILL_ENTRY</span></span> 
  
> <span data-ttu-id="691ad-115">Uma nova entrada está sendo criada.</span><span class="sxs-lookup"><span data-stu-id="691ad-115">A new entry is being created.</span></span> <span data-ttu-id="691ad-116">Quando o provedor estrangeiro recebe a chamada [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) subsequente do MAPI, ele pode controlar como a entrada é criada modificando as propriedades apontadas pelo parâmetro  _lpMAPIPropData_ ou retornando uma implementação de interface específica em  _lppMAPIPropNew_ para controlar como as propriedades da nova entrada são definidas.</span><span class="sxs-lookup"><span data-stu-id="691ad-116">When the foreign provider receives the subsequent [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) call from MAPI, it can control how the entry is created by modifying properties pointed to by the  _lpMAPIPropData_ parameter or by returning a specific interface implementation in  _lppMAPIPropNew_ to control how properties for the new entry are set.</span></span> 
    
 <span data-ttu-id="691ad-117">_lpMAPIPropData_</span><span class="sxs-lookup"><span data-stu-id="691ad-117">_lpMAPIPropData_</span></span>
  
> <span data-ttu-id="691ad-118">[in] Um ponteiro para a implementação da interface que o chamador usa para acessar a entrada.</span><span class="sxs-lookup"><span data-stu-id="691ad-118">[in] A pointer to the interface implementation that the caller uses to access the entry.</span></span> <span data-ttu-id="691ad-119">Esta é a implementação que o provedor externo pode quebrar com sua própria implementação e retornar no _parâmetro lppMAPIPropNew._</span><span class="sxs-lookup"><span data-stu-id="691ad-119">This is the implementation that the foreign provider can wrap with its own implementation and return in the  _lppMAPIPropNew_ parameter.</span></span> <span data-ttu-id="691ad-120">O _parâmetro lpMAPIPropData_ deve apontar para uma implementação de interface de leitura/gravação derivada de [IMAPIProp : IUnknown](imapipropiunknown.md) e dá suporte à interface que está sendo solicitada no parâmetro _lpInterface._</span><span class="sxs-lookup"><span data-stu-id="691ad-120">The  _lpMAPIPropData_ parameter must point to a read/write interface implementation that derives from [IMAPIProp : IUnknown](imapipropiunknown.md) and supports the interface being requested in the  _lpInterface_ parameter.</span></span> 
    
 <span data-ttu-id="691ad-121">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="691ad-121">_lpInterface_</span></span>
  
> <span data-ttu-id="691ad-122">[in] Um ponteiro para o identificador de interface (IID) que representa a interface a ser usada para acessar a entrada.</span><span class="sxs-lookup"><span data-stu-id="691ad-122">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the entry.</span></span> <span data-ttu-id="691ad-123">O  _parâmetro lppMAPIPropNew_ aponta para uma interface do tipo especificado por  _lpInterface_.</span><span class="sxs-lookup"><span data-stu-id="691ad-123">The  _lppMAPIPropNew_ parameter points to an interface of the type specified by  _lpInterface_.</span></span> <span data-ttu-id="691ad-124">Passar NULL retorna a interface padrão para um usuário de mensagens, IID_IMailUser.</span><span class="sxs-lookup"><span data-stu-id="691ad-124">Passing NULL returns the standard interface for a messaging user, IID_IMailUser.</span></span> 
    
 <span data-ttu-id="691ad-125">_lppMAPIPropNew_</span><span class="sxs-lookup"><span data-stu-id="691ad-125">_lppMAPIPropNew_</span></span>
  
> <span data-ttu-id="691ad-126">[out] Um ponteiro para a implementação da interface que o provedor estrangeiro fornece para acessar a entrada.</span><span class="sxs-lookup"><span data-stu-id="691ad-126">[out] A pointer to the interface implementation that the foreign provider supplies for accessing the entry.</span></span>
    
 <span data-ttu-id="691ad-127">_lpMAPIPropSibling_</span><span class="sxs-lookup"><span data-stu-id="691ad-127">_lpMAPIPropSibling_</span></span>
  
> <span data-ttu-id="691ad-128">Reservado; deve ser NULL.</span><span class="sxs-lookup"><span data-stu-id="691ad-128">Reserved; must be NULL.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="691ad-129">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="691ad-129">Return value</span></span>

<span data-ttu-id="691ad-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="691ad-130">S_OK</span></span> 
  
> <span data-ttu-id="691ad-131">O processo de associação foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="691ad-131">The binding process was successful.</span></span>
    
<span data-ttu-id="691ad-132">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="691ad-132">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="691ad-133">O provedor de agendas externas não existe.</span><span class="sxs-lookup"><span data-stu-id="691ad-133">The foreign address book provider doesn't exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="691ad-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="691ad-134">Remarks</span></span>

<span data-ttu-id="691ad-135">O **método IMAPISupport::OpenTemplateID** é implementado somente para objetos de suporte do provedor de agendas de endereços.</span><span class="sxs-lookup"><span data-stu-id="691ad-135">The **IMAPISupport::OpenTemplateID** method is implemented only for address book provider support objects.</span></span> <span data-ttu-id="691ad-136">**OpenTemplateID** é chamado apenas por provedores de agendas que podem atuar como hosts para entradas que pertencem a outros provedores de agendas, também conhecidos como provedores externos.</span><span class="sxs-lookup"><span data-stu-id="691ad-136">**OpenTemplateID** is called only by address book providers that can act as hosts for entries that belong to other address book providers, also known as foreign providers.</span></span> <span data-ttu-id="691ad-137">Os provedores de host chamam **OpenTemplateID** para abrir uma entrada externa, que ocorre quando os dados no provedor host estão vinculados ao código no provedor estrangeiro.</span><span class="sxs-lookup"><span data-stu-id="691ad-137">Host providers call **OpenTemplateID** to open a foreign entry, which occurs when data in the host provider is bound to code in the foreign provider.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="691ad-138">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="691ad-138">Notes to callers</span></span>

<span data-ttu-id="691ad-139">Chame **OpenTemplateID** somente se você suportar o armazenamento de entradas com identificadores de modelo de provedores de agendamento externo.</span><span class="sxs-lookup"><span data-stu-id="691ad-139">Call **OpenTemplateID** only if you support the storage of entries with template identifiers from foreign address book providers.</span></span> <span data-ttu-id="691ad-140">Esse suporte coloca requisitos adicionais nas implementações [IABContainer::CreateEntry](iabcontainer-createentry.md) e [IABLogon::OpenEntry.](iablogon-openentry.md)</span><span class="sxs-lookup"><span data-stu-id="691ad-140">Such support places additional requirements on your [IABContainer::CreateEntry](iabcontainer-createentry.md) and [IABLogon::OpenEntry](iablogon-openentry.md) implementations.</span></span> <span data-ttu-id="691ad-141">Para obter mais informações, consulte as descrições desses métodos e agindo como um provedor de [agenda de endereços de host.](acting-as-a-host-address-book-provider.md)</span><span class="sxs-lookup"><span data-stu-id="691ad-141">For more information, see the descriptions of these methods and [Acting as a Host Address Book Provider](acting-as-a-host-address-book-provider.md).</span></span>
  
<span data-ttu-id="691ad-142">Se a **chamada OpenTemplateID** retornar como a interface vinculada da mesma implementação de objeto de propriedade que você passou, você poderá liberar sua referência ao objeto property.</span><span class="sxs-lookup"><span data-stu-id="691ad-142">If the **OpenTemplateID** call returns as the bound interface the same property object implementation that you passed in, you can release your reference to your property object.</span></span> <span data-ttu-id="691ad-143">Isso porque o provedor externo chamou o método **AddRef** do objeto para manter sua própria referência.</span><span class="sxs-lookup"><span data-stu-id="691ad-143">This is because the foreign provider has called the object's **AddRef** method to keep its own reference.</span></span> <span data-ttu-id="691ad-144">Se o provedor externo não precisar manter uma referência para o objeto de propriedade, **OpenTemplateID** retornará o objeto de propriedade não abound.</span><span class="sxs-lookup"><span data-stu-id="691ad-144">If the foreign provider does not need to keep a reference to the property object, then **OpenTemplateID** will return the unbound property object.</span></span> 
  
<span data-ttu-id="691ad-145">Se **OpenTemplateID** falhar com MAPI_E_UNKNOWN_ENTRYID, tente continuar tratando a entrada como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="691ad-145">If **OpenTemplateID** fails with MAPI_E_UNKNOWN_ENTRYID, try to continue by treating the entry as read-only.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="691ad-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="691ad-146">See also</span></span>



[<span data-ttu-id="691ad-147">IABLogon::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="691ad-147">IABLogon::OpenTemplateID</span></span>](iablogon-opentemplateid.md)
  
[<span data-ttu-id="691ad-148">IPropData: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="691ad-148">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)
  
[<span data-ttu-id="691ad-149">Propriedade canônica PidTagTemplateid</span><span class="sxs-lookup"><span data-stu-id="691ad-149">PidTagTemplateid Canonical Property</span></span>](pidtagtemplateid-canonical-property.md)
  
[<span data-ttu-id="691ad-150">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="691ad-150">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

