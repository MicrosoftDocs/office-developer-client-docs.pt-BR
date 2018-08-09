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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: f99843bcdf3689acad72145a33d6a9804175a413
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767277"
---
# <a name="imapisupportopentemplateid"></a><span data-ttu-id="38e0d-103">IMAPISupport::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="38e0d-103">IMAPISupport::OpenTemplateID</span></span>

  
  
<span data-ttu-id="38e0d-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="38e0d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="38e0d-105">Abre uma entrada de destinatários em um provedor de catálogo de endereço estrangeiro.</span><span class="sxs-lookup"><span data-stu-id="38e0d-105">Opens a recipient entry in a foreign address book provider.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="38e0d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="38e0d-106">Parameters</span></span>

 <span data-ttu-id="38e0d-107">_cbTemplateID_</span><span class="sxs-lookup"><span data-stu-id="38e0d-107">_cbTemplateID_</span></span>
  
> <span data-ttu-id="38e0d-108">[in] A contagem de bytes do identificador de modelo apontado pela _lpTemplateID_.</span><span class="sxs-lookup"><span data-stu-id="38e0d-108">[in] The byte count in the template identifier pointed to by  _lpTemplateID_.</span></span> 
    
 <span data-ttu-id="38e0d-109">_lpTemplateID_</span><span class="sxs-lookup"><span data-stu-id="38e0d-109">_lpTemplateID_</span></span>
  
> <span data-ttu-id="38e0d-110">[in] Um ponteiro para o identificador de modelo de propriedade **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) da entrada do destinatário a serem abertas.</span><span class="sxs-lookup"><span data-stu-id="38e0d-110">[in] A pointer to the template identifier **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property of the recipient entry to be opened.</span></span>
    
 <span data-ttu-id="38e0d-111">_ulTemplateFlags_</span><span class="sxs-lookup"><span data-stu-id="38e0d-111">_ulTemplateFlags_</span></span>
  
> <span data-ttu-id="38e0d-112">[in] Uma bitmask dos sinalizadores usados para descrever como abrir a entrada.</span><span class="sxs-lookup"><span data-stu-id="38e0d-112">[in] A bitmask of flags used to describe how to open the entry.</span></span> <span data-ttu-id="38e0d-113">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="38e0d-113">The following flag can be set:</span></span>
    
<span data-ttu-id="38e0d-114">FILL_ENTRY</span><span class="sxs-lookup"><span data-stu-id="38e0d-114">FILL_ENTRY</span></span> 
  
> <span data-ttu-id="38e0d-115">Uma nova entrada está sendo criada.</span><span class="sxs-lookup"><span data-stu-id="38e0d-115">A new entry is being created.</span></span> <span data-ttu-id="38e0d-116">Quando o provedor estrangeiro recebe a chamada de [IABLogon:: OpenTemplateID](iablogon-opentemplateid.md) subsequente de MAPI, pode controlar como a entrada é criada, modificando propriedades apontadas pelo parâmetro _lpMAPIPropData_ ou, retornando uma interface específica implementação em _lppMAPIPropNew_ para controlar como propriedades para a nova entrada estiverem definidas.</span><span class="sxs-lookup"><span data-stu-id="38e0d-116">When the foreign provider receives the subsequent [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) call from MAPI, it can control how the entry is created by modifying properties pointed to by the  _lpMAPIPropData_ parameter or by returning a specific interface implementation in  _lppMAPIPropNew_ to control how properties for the new entry are set.</span></span> 
    
 <span data-ttu-id="38e0d-117">_lpMAPIPropData_</span><span class="sxs-lookup"><span data-stu-id="38e0d-117">_lpMAPIPropData_</span></span>
  
> <span data-ttu-id="38e0d-118">[in] Um ponteiro para a implementação de interface que o chamador usa para acessar a entrada.</span><span class="sxs-lookup"><span data-stu-id="38e0d-118">[in] A pointer to the interface implementation that the caller uses to access the entry.</span></span> <span data-ttu-id="38e0d-119">Esta é a implementação que o provedor estrangeiro pode quebrar automaticamente com sua própria implementação e retornar no parâmetro _lppMAPIPropNew_ .</span><span class="sxs-lookup"><span data-stu-id="38e0d-119">This is the implementation that the foreign provider can wrap with its own implementation and return in the  _lppMAPIPropNew_ parameter.</span></span> <span data-ttu-id="38e0d-120">O parâmetro _lpMAPIPropData_ deve apontar para uma implementação de interface de leitura/gravação que derive da [IMAPIProp: IUnknown](imapipropiunknown.md) e dá suporte à interface sendo solicitada no parâmetro _lpInterface_ .</span><span class="sxs-lookup"><span data-stu-id="38e0d-120">The  _lpMAPIPropData_ parameter must point to a read/write interface implementation that derives from [IMAPIProp : IUnknown](imapipropiunknown.md) and supports the interface being requested in the  _lpInterface_ parameter.</span></span> 
    
 <span data-ttu-id="38e0d-121">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="38e0d-121">_lpInterface_</span></span>
  
> <span data-ttu-id="38e0d-122">[in] Um ponteiro para o identificador de interface (IID) que representa a interface que será usada para acessar a entrada.</span><span class="sxs-lookup"><span data-stu-id="38e0d-122">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the entry.</span></span> <span data-ttu-id="38e0d-123">O parâmetro _lppMAPIPropNew_ aponta para uma interface do tipo especificado pelo _lpInterface_.</span><span class="sxs-lookup"><span data-stu-id="38e0d-123">The  _lppMAPIPropNew_ parameter points to an interface of the type specified by  _lpInterface_.</span></span> <span data-ttu-id="38e0d-124">Passar NULL retorna a interface padrão para um usuário de mensagens, IID_IMailUser.</span><span class="sxs-lookup"><span data-stu-id="38e0d-124">Passing NULL returns the standard interface for a messaging user, IID_IMailUser.</span></span> 
    
 <span data-ttu-id="38e0d-125">_lppMAPIPropNew_</span><span class="sxs-lookup"><span data-stu-id="38e0d-125">_lppMAPIPropNew_</span></span>
  
> <span data-ttu-id="38e0d-126">[out] Um ponteiro para a implementação de interface que o provedor estrangeiro fornece para acessar a entrada.</span><span class="sxs-lookup"><span data-stu-id="38e0d-126">[out] A pointer to the interface implementation that the foreign provider supplies for accessing the entry.</span></span>
    
 <span data-ttu-id="38e0d-127">_lpMAPIPropSibling_</span><span class="sxs-lookup"><span data-stu-id="38e0d-127">_lpMAPIPropSibling_</span></span>
  
> <span data-ttu-id="38e0d-128">Reservado; deve ser NULL.</span><span class="sxs-lookup"><span data-stu-id="38e0d-128">Reserved; must be NULL.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="38e0d-129">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="38e0d-129">Return value</span></span>

<span data-ttu-id="38e0d-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="38e0d-130">S_OK</span></span> 
  
> <span data-ttu-id="38e0d-131">O processo de ligação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="38e0d-131">The binding process was successful.</span></span>
    
<span data-ttu-id="38e0d-132">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="38e0d-132">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="38e0d-133">O provedor de catálogo de endereço estrangeiro não existe.</span><span class="sxs-lookup"><span data-stu-id="38e0d-133">The foreign address book provider doesn't exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="38e0d-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="38e0d-134">Remarks</span></span>

<span data-ttu-id="38e0d-135">O método **IMAPISupport::OpenTemplateID** é implementado apenas para objetos de suporte do provedor de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="38e0d-135">The **IMAPISupport::OpenTemplateID** method is implemented only for address book provider support objects.</span></span> <span data-ttu-id="38e0d-136">**OpenTemplateID** é chamado somente por provedores de catálogo de endereços que podem atuar como hosts para entradas que pertencem a outros provedores de catálogo de endereços, também conhecido como estrangeira provedores.</span><span class="sxs-lookup"><span data-stu-id="38e0d-136">**OpenTemplateID** is called only by address book providers that can act as hosts for entries that belong to other address book providers, also known as foreign providers.</span></span> <span data-ttu-id="38e0d-137">Provedores de host chamarem **OpenTemplateID** para abrir uma entrada externa, o que ocorre quando os dados no provedor de host são vinculados ao código no provedor estrangeiro.</span><span class="sxs-lookup"><span data-stu-id="38e0d-137">Host providers call **OpenTemplateID** to open a foreign entry, which occurs when data in the host provider is bound to code in the foreign provider.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="38e0d-138">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="38e0d-138">Notes to callers</span></span>

<span data-ttu-id="38e0d-139">Chame **OpenTemplateID** somente se você oferecer suporte ao armazenamento de entradas com identificadores de modelo de provedores de catálogo de endereço estrangeiro.</span><span class="sxs-lookup"><span data-stu-id="38e0d-139">Call **OpenTemplateID** only if you support the storage of entries with template identifiers from foreign address book providers.</span></span> <span data-ttu-id="38e0d-140">Tal suporte coloca as implementações [IABContainer::CreateEntry](iabcontainer-createentry.md) e [IABLogon::OpenEntry](iablogon-openentry.md) requisitos adicionais.</span><span class="sxs-lookup"><span data-stu-id="38e0d-140">Such support places additional requirements on your [IABContainer::CreateEntry](iabcontainer-createentry.md) and [IABLogon::OpenEntry](iablogon-openentry.md) implementations.</span></span> <span data-ttu-id="38e0d-141">Para obter mais informações, consulte as descrições desses métodos e [atuando como um provedor de catálogo de endereço de Host](acting-as-a-host-address-book-provider.md).</span><span class="sxs-lookup"><span data-stu-id="38e0d-141">For more information, see the descriptions of these methods and [Acting as a Host Address Book Provider](acting-as-a-host-address-book-provider.md).</span></span>
  
<span data-ttu-id="38e0d-142">Se a chamada **OpenTemplateID** retornar como a interface acoplada a mesma implementação de objeto de propriedade que você passado, você pode liberar sua referência para seu objeto de propriedade.</span><span class="sxs-lookup"><span data-stu-id="38e0d-142">If the **OpenTemplateID** call returns as the bound interface the same property object implementation that you passed in, you can release your reference to your property object.</span></span> <span data-ttu-id="38e0d-143">Isso ocorre porque o provedor estrangeiro chamou o método do objeto **AddRef** para manter sua própria referência.</span><span class="sxs-lookup"><span data-stu-id="38e0d-143">This is because the foreign provider has called the object's **AddRef** method to keep its own reference.</span></span> <span data-ttu-id="38e0d-144">Se o provedor estrangeiro não precisa manter uma referência ao objeto de propriedade, **OpenTemplateID** retornará o objeto não acoplado property.</span><span class="sxs-lookup"><span data-stu-id="38e0d-144">If the foreign provider does not need to keep a reference to the property object, then **OpenTemplateID** will return the unbound property object.</span></span> 
  
<span data-ttu-id="38e0d-145">Se **OpenTemplateID** falhar com MAPI_E_UNKNOWN_ENTRYID, tente continuar tratando-se a entrada como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="38e0d-145">If **OpenTemplateID** fails with MAPI_E_UNKNOWN_ENTRYID, try to continue by treating the entry as read-only.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="38e0d-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="38e0d-146">See also</span></span>



[<span data-ttu-id="38e0d-147">IABLogon::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="38e0d-147">IABLogon::OpenTemplateID</span></span>](iablogon-opentemplateid.md)
  
[<span data-ttu-id="38e0d-148">IPropData: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="38e0d-148">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)
  
[<span data-ttu-id="38e0d-149">Propriedade canônica PidTagTemplateid</span><span class="sxs-lookup"><span data-stu-id="38e0d-149">PidTagTemplateid Canonical Property</span></span>](pidtagtemplateid-canonical-property.md)
  
[<span data-ttu-id="38e0d-150">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="38e0d-150">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

