---
title: IABLogonOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.OpenEntry
api_type:
- COM
ms.assetid: 1cfb82f7-5215-4faa-af25-5b1da7e31209
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 70f61ef553350f08eed96c1ee4e9ab790359d1fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409227"
---
# <a name="iablogonopenentry"></a><span data-ttu-id="aa46b-103">IABLogon::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="aa46b-103">IABLogon::OpenEntry</span></span>

  
  
<span data-ttu-id="aa46b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aa46b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aa46b-105">Abre um contêiner, um usuário de mensagens ou uma lista de distribuição e retorna um ponteiro para uma implementação de interface para fornecer mais acesso.</span><span class="sxs-lookup"><span data-stu-id="aa46b-105">Opens a container, messaging user, or distribution list, and returns a pointer to an interface implementation to provide further access.</span></span>
  
```cpp
HRESULT OpenEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="aa46b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aa46b-106">Parameters</span></span>

 <span data-ttu-id="aa46b-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="aa46b-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="aa46b-108">[in] A contagem de byte no identificador de entrada apontado pelo parâmetro _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="aa46b-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="aa46b-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="aa46b-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="aa46b-110">[in] Um ponteiro para o identificador de entrada do contêiner, do usuário de mensagens ou da lista de distribuição a ser aberta.</span><span class="sxs-lookup"><span data-stu-id="aa46b-110">[in] A pointer to the entry identifier of the container, messaging user, or distribution list to open.</span></span>
    
 <span data-ttu-id="aa46b-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="aa46b-111">_lpInterface_</span></span>
  
> <span data-ttu-id="aa46b-112">[in] Um ponteiro para o IID (identificador de interface) que representa a interface a ser usada para acessar o objeto aberto.</span><span class="sxs-lookup"><span data-stu-id="aa46b-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the open object.</span></span> <span data-ttu-id="aa46b-113">Passar NULL retorna o identificador da interface padrão do objeto.</span><span class="sxs-lookup"><span data-stu-id="aa46b-113">Passing NULL returns the identifier for the object's standard interface.</span></span> <span data-ttu-id="aa46b-114">Para contêineres, a interface padrão [é IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="aa46b-114">For containers, the standard interface is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="aa46b-115">As interfaces padrão para objetos de livro de endereços são [IDistList : IMAPIContainer](idistlistimapicontainer.md) para uma lista de distribuição e [IMailUser : IMAPIProp](imailuserimapiprop.md) para um usuário de mensagens.</span><span class="sxs-lookup"><span data-stu-id="aa46b-115">The standard interfaces for address book objects are [IDistList : IMAPIContainer](idistlistimapicontainer.md) for a distribution list and [IMailUser : IMAPIProp](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="aa46b-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="aa46b-116">_ulFlags_</span></span>
  
> <span data-ttu-id="aa46b-117">[in] Uma máscara de bits de sinalizadores que controla como o objeto é aberto.</span><span class="sxs-lookup"><span data-stu-id="aa46b-117">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="aa46b-118">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="aa46b-118">The following flags can be set:</span></span>
    
<span data-ttu-id="aa46b-119">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="aa46b-119">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="aa46b-120">Solicita que o objeto seja aberto com as permissões máximas de rede permitidas para o usuário e o acesso máximo ao aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="aa46b-120">Requests that the object be opened with the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="aa46b-121">Por exemplo, se o cliente tiver permissão de leitura/gravação, o objeto deverá ser aberto com permissão de leitura/gravação; se o cliente tiver permissão somente leitura, o objeto deverá ser aberto com permissão somente leitura.</span><span class="sxs-lookup"><span data-stu-id="aa46b-121">For example, if the client has read/write permission, the object should be opened with read/write permission; if the client has read-only permission, the object should be opened with read-only permission.</span></span>
    
<span data-ttu-id="aa46b-122">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="aa46b-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="aa46b-123">Permite que o **método OpenEntry** retorne com êxito, possivelmente antes do cliente de chamada ter acessado totalmente o objeto.</span><span class="sxs-lookup"><span data-stu-id="aa46b-123">Allows the **OpenEntry** method to return successfully, possibly before the calling client has fully accessed the object.</span></span> <span data-ttu-id="aa46b-124">Se o objeto não for acessado, fazer uma chamada de objeto subsequente poderá criar um erro.</span><span class="sxs-lookup"><span data-stu-id="aa46b-124">If the object is not accessed, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="aa46b-125">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="aa46b-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="aa46b-126">Solicita permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="aa46b-126">Requests read/write permission.</span></span> <span data-ttu-id="aa46b-127">Por padrão, os objetos são abertos com acesso somente leitura e os clientes não devem presumir que a permissão de leitura/gravação foi concedida.</span><span class="sxs-lookup"><span data-stu-id="aa46b-127">By default, objects are opened with read-only access, and clients should not assume that read/write permission has been granted.</span></span>
    
 <span data-ttu-id="aa46b-128">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="aa46b-128">_lpulObjType_</span></span>
  
> <span data-ttu-id="aa46b-129">[out] Um ponteiro para o tipo do objeto aberto.</span><span class="sxs-lookup"><span data-stu-id="aa46b-129">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="aa46b-130">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="aa46b-130">_lppUnk_</span></span>
  
> <span data-ttu-id="aa46b-131">[out] Um ponteiro para um ponteiro para o objeto aberto.</span><span class="sxs-lookup"><span data-stu-id="aa46b-131">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="aa46b-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="aa46b-132">Remarks</span></span>

<span data-ttu-id="aa46b-133">S_OK</span><span class="sxs-lookup"><span data-stu-id="aa46b-133">S_OK</span></span> 
  
> <span data-ttu-id="aa46b-134">O objeto foi aberto com êxito.</span><span class="sxs-lookup"><span data-stu-id="aa46b-134">The object was successfully opened.</span></span>
    
<span data-ttu-id="aa46b-135">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="aa46b-135">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="aa46b-136">O usuário tem permissões insuficientes para abrir o objeto ou foi feita uma tentativa de abrir um objeto somente leitura com permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="aa46b-136">Either the user has insufficient permissions to open the object, or an attempt was made to open a read-only object with read/write permission.</span></span>
    
<span data-ttu-id="aa46b-137">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="aa46b-137">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="aa46b-138">O identificador de entrada especificado por  _lpEntryID_ não representa um objeto.</span><span class="sxs-lookup"><span data-stu-id="aa46b-138">The entry identifier specified by  _lpEntryID_ does not represent an object.</span></span> 
    
<span data-ttu-id="aa46b-139">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="aa46b-139">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="aa46b-140">O identificador de entrada no  _parâmetro lpEntryID_ não tem um formato reconhecido pelo provedor do address book.</span><span class="sxs-lookup"><span data-stu-id="aa46b-140">The entry identifier in the  _lpEntryID_ parameter is not of a format recognized by the address book provider.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="aa46b-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="aa46b-141">Remarks</span></span>

<span data-ttu-id="aa46b-142">MAPI calls the **OpenEntry** method to open a container, messaging user, or distribution list.</span><span class="sxs-lookup"><span data-stu-id="aa46b-142">MAPI calls the **OpenEntry** method to open a container, messaging user, or distribution list.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="aa46b-143">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="aa46b-143">Notes to implementers</span></span>

<span data-ttu-id="aa46b-144">Antes de o MAPI chamar **o método OpenEntry,** ele determina que o identificador de entrada no parâmetro  _lpEntryID_ pertence a você e não a outro provedor.</span><span class="sxs-lookup"><span data-stu-id="aa46b-144">Before MAPI calls your **OpenEntry** method, it determines that the entry identifier in the  _lpEntryID_ parameter belongs to you and not to another provider.</span></span> <span data-ttu-id="aa46b-145">MAPI does this by matching the [MAPIUID](mapiuid.md) structure in the entry identifier with the **MAPIUID** that you registered by calling the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method at startup.</span><span class="sxs-lookup"><span data-stu-id="aa46b-145">MAPI does this by matching the [MAPIUID](mapiuid.md) structure in the entry identifier with the **MAPIUID** that you registered by calling the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method at startup.</span></span> 
  
<span data-ttu-id="aa46b-146">Abra o objeto como somente leitura, a menos que o sinalizador MAPI_MODIFY ou MAPI_BEST_ACCESS seja definido no _parâmetro ulFlags._</span><span class="sxs-lookup"><span data-stu-id="aa46b-146">Open the object as read-only, unless the MAPI_MODIFY or MAPI_BEST_ACCESS flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="aa46b-147">Se você não permitir a modificação para o objeto solicitado, não abra o objeto e retorne MAPI_E_NO_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="aa46b-147">If you do not allow modification for the requested object, do not open the object at all and return MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="aa46b-148">Se MAPI passar NULL para  _lpEntryID,_ abra o contêiner raiz em sua hierarquia de contêineres.</span><span class="sxs-lookup"><span data-stu-id="aa46b-148">If MAPI passes NULL for  _lpEntryID_, open the root container in your container hierarchy.</span></span>
  
<span data-ttu-id="aa46b-149">O objeto que você está sendo solicitado a abrir pode ser um objeto copiado de outro provedor.</span><span class="sxs-lookup"><span data-stu-id="aa46b-149">The object that you are being asked to open might be an object copied from another provider.</span></span> <span data-ttu-id="aa46b-150">Nesse caso, ele dará suporte à **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="aa46b-150">In this case, it will support the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property.</span></span> <span data-ttu-id="aa46b-151">Se o objeto suportar essa propriedade, chame o método [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) para vincular ao código dessa entrada no provedor estrangeiro, passando **PR_TEMPLATEID** no parâmetro _lpTemplateID_ e 0 no _parâmetro ulTemplateFlags._</span><span class="sxs-lookup"><span data-stu-id="aa46b-151">If the object does support this property, call the [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) method to bind to code for this entry in the foreign provider, passing **PR_TEMPLATEID** in the  _lpTemplateID_ parameter and 0 in the  _ulTemplateFlags_ parameter.</span></span> <span data-ttu-id="aa46b-152">**IMAPISupport::OpenTemplateID** passa essas informações para o provedor estrangeiro em uma chamada para o método [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) do provedor estrangeiro.</span><span class="sxs-lookup"><span data-stu-id="aa46b-152">**IMAPISupport::OpenTemplateID** passes this information to the foreign provider in a call to the foreign provider's [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) method.</span></span> <span data-ttu-id="aa46b-153">Se **IMAPISupport::OpenTemplateID** gera um erro, geralmente porque o provedor estrangeiro está indisponível ou não está incluído no perfil, tente continuar tratando a entrada desaprovada como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="aa46b-153">If **IMAPISupport::OpenTemplateID** raises an error, usually because the foreign provider is unavailable or not included in the profile, try to continue by treating the unbound entry as read-only.</span></span> <span data-ttu-id="aa46b-154">Para obter mais informações sobre como abrir entradas de livro de endereços externos, consulte [Agindo como um provedor de agenda de endereço de host.](acting-as-a-host-address-book-provider.md)</span><span class="sxs-lookup"><span data-stu-id="aa46b-154">For more information about opening foreign address book entries, see [Acting as a Host Address Book Provider](acting-as-a-host-address-book-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="aa46b-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="aa46b-155">See also</span></span>



[<span data-ttu-id="aa46b-156">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="aa46b-156">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

