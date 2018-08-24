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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: bf6386ae3a7d835c8748e332235d8737c7a502e8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589466"
---
# <a name="iablogonopenentry"></a><span data-ttu-id="adb71-103">IABLogon::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="adb71-103">IABLogon::OpenEntry</span></span>

  
  
<span data-ttu-id="adb71-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="adb71-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="adb71-105">Abre um contêiner, o usuário ou lista de distribuição de mensagens e retorna um ponteiro para uma implementação de interface para fornecer mais acesso.</span><span class="sxs-lookup"><span data-stu-id="adb71-105">Opens a container, messaging user, or distribution list, and returns a pointer to an interface implementation to provide further access.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="adb71-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="adb71-106">Parameters</span></span>

 <span data-ttu-id="adb71-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="adb71-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="adb71-108">[in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="adb71-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="adb71-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="adb71-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="adb71-110">[in] Um ponteiro para o identificador de entrada do contêiner, mensagens de usuário ou lista de distribuição para abrir.</span><span class="sxs-lookup"><span data-stu-id="adb71-110">[in] A pointer to the entry identifier of the container, messaging user, or distribution list to open.</span></span>
    
 <span data-ttu-id="adb71-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="adb71-111">_lpInterface_</span></span>
  
> <span data-ttu-id="adb71-112">[in] Um ponteiro para o identificador de interface (IID) que representa a interface para ser usado para acessar o objeto aberto.</span><span class="sxs-lookup"><span data-stu-id="adb71-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the open object.</span></span> <span data-ttu-id="adb71-113">Passar NULL retorna o identificador de interface de padrão do objeto.</span><span class="sxs-lookup"><span data-stu-id="adb71-113">Passing NULL returns the identifier for the object's standard interface.</span></span> <span data-ttu-id="adb71-114">Para contêineres, a interface padrão é [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="adb71-114">For containers, the standard interface is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="adb71-115">O padrão de interfaces para objetos de catálogo de endereços estão [IDistList: IMAPIContainer](idistlistimapicontainer.md) para obter uma lista de distribuição e [IMailUser: IMAPIProp](imailuserimapiprop.md) para um usuário de mensagens.</span><span class="sxs-lookup"><span data-stu-id="adb71-115">The standard interfaces for address book objects are [IDistList : IMAPIContainer](idistlistimapicontainer.md) for a distribution list and [IMailUser : IMAPIProp](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="adb71-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="adb71-116">_ulFlags_</span></span>
  
> <span data-ttu-id="adb71-117">[in] Uma bitmask dos sinalizadores que controla como o objeto é aberto.</span><span class="sxs-lookup"><span data-stu-id="adb71-117">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="adb71-118">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="adb71-118">The following flags can be set:</span></span>
    
<span data-ttu-id="adb71-119">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="adb71-119">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="adb71-120">Solicita que o objeto seja aberto com as permissões de rede máximo permitidas para o usuário e o acesso do aplicativo de cliente máximo.</span><span class="sxs-lookup"><span data-stu-id="adb71-120">Requests that the object be opened with the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="adb71-121">Por exemplo, se o cliente tem a permissão de leitura/gravação, o objeto deve ser aberto com permissão de leitura/gravação; Se o cliente tem a permissão somente leitura, o objeto deve ser aberto com permissão somente leitura.</span><span class="sxs-lookup"><span data-stu-id="adb71-121">For example, if the client has read/write permission, the object should be opened with read/write permission; if the client has read-only permission, the object should be opened with read-only permission.</span></span>
    
<span data-ttu-id="adb71-122">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="adb71-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="adb71-123">Permite que o método **OpenEntry** retornar com êxito, possivelmente antes que o cliente da chamada acessou totalmente o objeto.</span><span class="sxs-lookup"><span data-stu-id="adb71-123">Allows the **OpenEntry** method to return successfully, possibly before the calling client has fully accessed the object.</span></span> <span data-ttu-id="adb71-124">Se o objeto não é acessado, fazendo uma chamada do objeto subsequente pode gerar um erro.</span><span class="sxs-lookup"><span data-stu-id="adb71-124">If the object is not accessed, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="adb71-125">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="adb71-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="adb71-126">Permissão de leitura/gravação solicitações.</span><span class="sxs-lookup"><span data-stu-id="adb71-126">Requests read/write permission.</span></span> <span data-ttu-id="adb71-127">Por padrão, os objetos são abertos com acesso somente leitura e os clientes não devem presumir que foi concedida permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="adb71-127">By default, objects are opened with read-only access, and clients should not assume that read/write permission has been granted.</span></span>
    
 <span data-ttu-id="adb71-128">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="adb71-128">_lpulObjType_</span></span>
  
> <span data-ttu-id="adb71-129">[out] Um ponteiro para o tipo de objeto aberto.</span><span class="sxs-lookup"><span data-stu-id="adb71-129">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="adb71-130">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="adb71-130">_lppUnk_</span></span>
  
> <span data-ttu-id="adb71-131">[out] Um ponteiro para um ponteiro para o objeto aberto.</span><span class="sxs-lookup"><span data-stu-id="adb71-131">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="adb71-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="adb71-132">Remarks</span></span>

<span data-ttu-id="adb71-133">S_OK</span><span class="sxs-lookup"><span data-stu-id="adb71-133">S_OK</span></span> 
  
> <span data-ttu-id="adb71-134">O objeto foi aberto com êxito.</span><span class="sxs-lookup"><span data-stu-id="adb71-134">The object was successfully opened.</span></span>
    
<span data-ttu-id="adb71-135">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="adb71-135">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="adb71-136">O usuário tem permissões insuficientes para abrir o objeto ou foi feita uma tentativa de abrir um objeto de somente leitura com permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="adb71-136">Either the user has insufficient permissions to open the object, or an attempt was made to open a read-only object with read/write permission.</span></span>
    
<span data-ttu-id="adb71-137">E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="adb71-137">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="adb71-138">O identificador de entrada especificado pelo _lpEntryID_ não representa um objeto.</span><span class="sxs-lookup"><span data-stu-id="adb71-138">The entry identifier specified by  _lpEntryID_ does not represent an object.</span></span> 
    
<span data-ttu-id="adb71-139">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="adb71-139">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="adb71-140">O identificador de entrada no parâmetro _lpEntryID_ não tem um formato reconhecido pelo provedor de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="adb71-140">The entry identifier in the  _lpEntryID_ parameter is not of a format recognized by the address book provider.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="adb71-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="adb71-141">Remarks</span></span>

<span data-ttu-id="adb71-142">MAPI chama o método de **OpenEntry** para abrir um contêiner, o usuário ou lista de distribuição de mensagens.</span><span class="sxs-lookup"><span data-stu-id="adb71-142">MAPI calls the **OpenEntry** method to open a container, messaging user, or distribution list.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="adb71-143">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="adb71-143">Notes to implementers</span></span>

<span data-ttu-id="adb71-144">Antes de MAPI chama seu método de **OpenEntry** , ele determina que o identificador de entrada no parâmetro _lpEntryID_ pertence a você e não a outro provedor.</span><span class="sxs-lookup"><span data-stu-id="adb71-144">Before MAPI calls your **OpenEntry** method, it determines that the entry identifier in the  _lpEntryID_ parameter belongs to you and not to another provider.</span></span> <span data-ttu-id="adb71-145">MAPI realiza isso mediante correspondentes a estrutura [MAPIUID](mapiuid.md) do identificador de entrada com o **MAPIUID** que você registrou chamando o método [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) na inicialização.</span><span class="sxs-lookup"><span data-stu-id="adb71-145">MAPI does this by matching the [MAPIUID](mapiuid.md) structure in the entry identifier with the **MAPIUID** that you registered by calling the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method at startup.</span></span> 
  
<span data-ttu-id="adb71-146">Abra o objeto como somente leitura, exceto se o sinalizador MAPI_MODIFY ou MAPI_BEST_ACCESS estiver definido no parâmetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="adb71-146">Open the object as read-only, unless the MAPI_MODIFY or MAPI_BEST_ACCESS flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="adb71-147">Se você não permitir a modificação do objeto solicitada, não abre o objeto nisso e retornar MAPI_E_NO_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="adb71-147">If you do not allow modification for the requested object, do not open the object at all and return MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="adb71-148">Se o MAPI transmite NULL para _lpEntryID_, abra o contêiner de raiz na sua hierarquia de contêiner.</span><span class="sxs-lookup"><span data-stu-id="adb71-148">If MAPI passes NULL for  _lpEntryID_, open the root container in your container hierarchy.</span></span>
  
<span data-ttu-id="adb71-149">O objeto que você está sendo solicitado para abrir pode ser um objeto copiado de outro provedor.</span><span class="sxs-lookup"><span data-stu-id="adb71-149">The object that you are being asked to open might be an object copied from another provider.</span></span> <span data-ttu-id="adb71-150">Nesse caso, ele dará suporte a propriedade **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="adb71-150">In this case, it will support the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property.</span></span> <span data-ttu-id="adb71-151">Se o objeto dá suporte a essa propriedade, chame o método de [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) para vincular ao código para essa entrada no provedor estrangeira, passando o parâmetro _lpTemplateID_ e de 0 a ulTemplateFlags _ **PR_TEMPLATEID** _parâmetro.</span><span class="sxs-lookup"><span data-stu-id="adb71-151">If the object does support this property, call the [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) method to bind to code for this entry in the foreign provider, passing **PR_TEMPLATEID** in the  _lpTemplateID_ parameter and 0 in the  _ulTemplateFlags_ parameter.</span></span> <span data-ttu-id="adb71-152">**IMAPISupport::OpenTemplateID** passa essas informações para o provedor externo em uma chamada ao método de [IABLogon:: OpenTemplateID](iablogon-opentemplateid.md) do provedor estrangeira.</span><span class="sxs-lookup"><span data-stu-id="adb71-152">**IMAPISupport::OpenTemplateID** passes this information to the foreign provider in a call to the foreign provider's [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) method.</span></span> <span data-ttu-id="adb71-153">Se **IMAPISupport::OpenTemplateID** gera um erro, geralmente porque o provedor estrangeiro está indisponível ou não foi incluído no perfil, tente continuar tratando-se a entrada não acoplada como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="adb71-153">If **IMAPISupport::OpenTemplateID** raises an error, usually because the foreign provider is unavailable or not included in the profile, try to continue by treating the unbound entry as read-only.</span></span> <span data-ttu-id="adb71-154">Para obter mais informações sobre a abertura de entradas do catálogo de endereço estrangeiro, consulte [atuando como um provedor de catálogo de endereço de Host](acting-as-a-host-address-book-provider.md).</span><span class="sxs-lookup"><span data-stu-id="adb71-154">For more information about opening foreign address book entries, see [Acting as a Host Address Book Provider](acting-as-a-host-address-book-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="adb71-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="adb71-155">See also</span></span>



[<span data-ttu-id="adb71-156">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="adb71-156">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

