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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348934"
---
# <a name="iablogonopenentry"></a><span data-ttu-id="7a08c-103">IABLogon::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="7a08c-103">IABLogon::OpenEntry</span></span>

  
  
<span data-ttu-id="7a08c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7a08c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7a08c-105">Abre um contêiner, um usuário de mensagens ou uma lista de distribuição e retorna um ponteiro para uma implementação de interface para fornecer acesso adicional.</span><span class="sxs-lookup"><span data-stu-id="7a08c-105">Opens a container, messaging user, or distribution list, and returns a pointer to an interface implementation to provide further access.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="7a08c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7a08c-106">Parameters</span></span>

 <span data-ttu-id="7a08c-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="7a08c-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="7a08c-108">no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="7a08c-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="7a08c-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="7a08c-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="7a08c-110">no Um ponteiro para o identificador de entrada do contêiner, usuário de mensagens ou lista de distribuição a ser aberto.</span><span class="sxs-lookup"><span data-stu-id="7a08c-110">[in] A pointer to the entry identifier of the container, messaging user, or distribution list to open.</span></span>
    
 <span data-ttu-id="7a08c-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="7a08c-111">_lpInterface_</span></span>
  
> <span data-ttu-id="7a08c-112">no Um ponteiro para o identificador de interface (IID) que representa a interface a ser usada para acessar o objeto Open.</span><span class="sxs-lookup"><span data-stu-id="7a08c-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the open object.</span></span> <span data-ttu-id="7a08c-113">Passar nulo retorna o identificador da interface padrão do objeto.</span><span class="sxs-lookup"><span data-stu-id="7a08c-113">Passing NULL returns the identifier for the object's standard interface.</span></span> <span data-ttu-id="7a08c-114">Para contêineres, a interface padrão é [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="7a08c-114">For containers, the standard interface is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="7a08c-115">As interfaces padrão para os objetos do catálogo de endereços são [IDistList: IMAPIContainer](idistlistimapicontainer.md) para uma lista de distribuição e [IMailUser: IMAPIProp](imailuserimapiprop.md) para um usuário de mensagens.</span><span class="sxs-lookup"><span data-stu-id="7a08c-115">The standard interfaces for address book objects are [IDistList : IMAPIContainer](idistlistimapicontainer.md) for a distribution list and [IMailUser : IMAPIProp](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="7a08c-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7a08c-116">_ulFlags_</span></span>
  
> <span data-ttu-id="7a08c-117">no Uma bitmask de sinalizadores que controla como o objeto é aberto.</span><span class="sxs-lookup"><span data-stu-id="7a08c-117">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="7a08c-118">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="7a08c-118">The following flags can be set:</span></span>
    
<span data-ttu-id="7a08c-119">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="7a08c-119">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="7a08c-120">Solicita que o objeto seja aberto com as permissões de rede máximas permitidas para o usuário e o acesso ao aplicativo cliente máximo.</span><span class="sxs-lookup"><span data-stu-id="7a08c-120">Requests that the object be opened with the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="7a08c-121">Por exemplo, se o cliente tiver permissão de leitura/gravação, o objeto deverá ser aberto com permissão de leitura/gravação; Se o cliente tiver permissão somente leitura, o objeto deverá ser aberto com permissão somente leitura.</span><span class="sxs-lookup"><span data-stu-id="7a08c-121">For example, if the client has read/write permission, the object should be opened with read/write permission; if the client has read-only permission, the object should be opened with read-only permission.</span></span>
    
<span data-ttu-id="7a08c-122">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="7a08c-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="7a08c-123">Permite que o método **OpenEntry** seja retornado com êxito, possivelmente antes que o cliente de chamada tenha acessado o objeto completamente.</span><span class="sxs-lookup"><span data-stu-id="7a08c-123">Allows the **OpenEntry** method to return successfully, possibly before the calling client has fully accessed the object.</span></span> <span data-ttu-id="7a08c-124">Se o objeto não for acessado, fazer uma chamada de objeto subsequente poderá gerar um erro.</span><span class="sxs-lookup"><span data-stu-id="7a08c-124">If the object is not accessed, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="7a08c-125">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="7a08c-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="7a08c-126">Solicita permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="7a08c-126">Requests read/write permission.</span></span> <span data-ttu-id="7a08c-127">Por padrão, os objetos são abertos com acesso somente leitura e os clientes não devem supor que a permissão de leitura/gravação tenha sido concedida.</span><span class="sxs-lookup"><span data-stu-id="7a08c-127">By default, objects are opened with read-only access, and clients should not assume that read/write permission has been granted.</span></span>
    
 <span data-ttu-id="7a08c-128">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="7a08c-128">_lpulObjType_</span></span>
  
> <span data-ttu-id="7a08c-129">bota Um ponteiro para o tipo do objeto aberto.</span><span class="sxs-lookup"><span data-stu-id="7a08c-129">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="7a08c-130">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="7a08c-130">_lppUnk_</span></span>
  
> <span data-ttu-id="7a08c-131">bota Um ponteiro para um ponteiro para o objeto aberto.</span><span class="sxs-lookup"><span data-stu-id="7a08c-131">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7a08c-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="7a08c-132">Remarks</span></span>

<span data-ttu-id="7a08c-133">S_OK</span><span class="sxs-lookup"><span data-stu-id="7a08c-133">S_OK</span></span> 
  
> <span data-ttu-id="7a08c-134">O objeto foi aberto com êxito.</span><span class="sxs-lookup"><span data-stu-id="7a08c-134">The object was successfully opened.</span></span>
    
<span data-ttu-id="7a08c-135">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="7a08c-135">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="7a08c-136">O usuário tem permissões insuficientes para abrir o objeto ou foi feita uma tentativa de abrir um objeto somente leitura com permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="7a08c-136">Either the user has insufficient permissions to open the object, or an attempt was made to open a read-only object with read/write permission.</span></span>
    
<span data-ttu-id="7a08c-137">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="7a08c-137">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="7a08c-138">O identificador de entrada especificado por _lpEntryID_ não representa um objeto.</span><span class="sxs-lookup"><span data-stu-id="7a08c-138">The entry identifier specified by  _lpEntryID_ does not represent an object.</span></span> 
    
<span data-ttu-id="7a08c-139">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="7a08c-139">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="7a08c-140">O identificador de entrada no parâmetro _lpEntryID_ não é de um formato reconhecido pelo provedor de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="7a08c-140">The entry identifier in the  _lpEntryID_ parameter is not of a format recognized by the address book provider.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7a08c-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="7a08c-141">Remarks</span></span>

<span data-ttu-id="7a08c-142">MAPI chama o método **OpenEntry** para abrir um contêiner, usuário de mensagens ou lista de distribuição.</span><span class="sxs-lookup"><span data-stu-id="7a08c-142">MAPI calls the **OpenEntry** method to open a container, messaging user, or distribution list.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="7a08c-143">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="7a08c-143">Notes to implementers</span></span>

<span data-ttu-id="7a08c-144">Antes de o MAPI chamar o método **OpenEntry** , ele determina que o identificador de entrada no parâmetro _lpEntryID_ pertence a você e não a outro provedor.</span><span class="sxs-lookup"><span data-stu-id="7a08c-144">Before MAPI calls your **OpenEntry** method, it determines that the entry identifier in the  _lpEntryID_ parameter belongs to you and not to another provider.</span></span> <span data-ttu-id="7a08c-145">O MAPI faz isso combinando a estrutura [MAPIUID](mapiuid.md) no identificador de entrada com o **MAPIUID** que você registrou chamando o método [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md) na inicialização.</span><span class="sxs-lookup"><span data-stu-id="7a08c-145">MAPI does this by matching the [MAPIUID](mapiuid.md) structure in the entry identifier with the **MAPIUID** that you registered by calling the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method at startup.</span></span> 
  
<span data-ttu-id="7a08c-146">Abra o objeto como somente leitura, a menos que o sinalizador MAPI_MODIFY ou MAPI_BEST_ACCESS esteja definido no parâmetro _parâmetroulflags_ .</span><span class="sxs-lookup"><span data-stu-id="7a08c-146">Open the object as read-only, unless the MAPI_MODIFY or MAPI_BEST_ACCESS flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="7a08c-147">Se você não permitir modificações para o objeto solicitado, não abra o objeto e retorne MAPI_E_NO_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="7a08c-147">If you do not allow modification for the requested object, do not open the object at all and return MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="7a08c-148">Se MAPI passar NULL para _lpEntryID_, abra o contêiner raiz na sua hierarquia de contêineres.</span><span class="sxs-lookup"><span data-stu-id="7a08c-148">If MAPI passes NULL for  _lpEntryID_, open the root container in your container hierarchy.</span></span>
  
<span data-ttu-id="7a08c-149">O objeto que você está sendo solicitado a abrir pode ser um objeto copiado de outro provedor.</span><span class="sxs-lookup"><span data-stu-id="7a08c-149">The object that you are being asked to open might be an object copied from another provider.</span></span> <span data-ttu-id="7a08c-150">Nesse caso, ele dará suporte à propriedade **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="7a08c-150">In this case, it will support the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property.</span></span> <span data-ttu-id="7a08c-151">Se o objeto não oferecer suporte a essa propriedade, chame o método [IMAPISupport:: OpenTemplateID](imapisupport-opentemplateid.md) para vincular ao código para esta entrada no provedor estrangeiro, passando **PR_TEMPLATEID** no parâmetro _lpTemplateID_ e 0 no _ulTemplateFlags _parâmetro.</span><span class="sxs-lookup"><span data-stu-id="7a08c-151">If the object does support this property, call the [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) method to bind to code for this entry in the foreign provider, passing **PR_TEMPLATEID** in the  _lpTemplateID_ parameter and 0 in the  _ulTemplateFlags_ parameter.</span></span> <span data-ttu-id="7a08c-152">**IMAPISupport:: OpenTemplateID** passa essas informações para o provedor estrangeiro em uma chamada para o método [IABLogon:: OpenTemplateID](iablogon-opentemplateid.md) do provedor estrangeiro.</span><span class="sxs-lookup"><span data-stu-id="7a08c-152">**IMAPISupport::OpenTemplateID** passes this information to the foreign provider in a call to the foreign provider's [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) method.</span></span> <span data-ttu-id="7a08c-153">Se **IMAPISupport:: OpenTemplateID** gerar um erro, geralmente porque o provedor estrangeiro não está disponível ou não está incluído no perfil, tente continuar tratando a entrada não associada como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="7a08c-153">If **IMAPISupport::OpenTemplateID** raises an error, usually because the foreign provider is unavailable or not included in the profile, try to continue by treating the unbound entry as read-only.</span></span> <span data-ttu-id="7a08c-154">Para obter mais informações sobre como abrir entradas do catálogo de endereços estrangeiros, consulte [atuando como um provedor de catálogo de endereços de host](acting-as-a-host-address-book-provider.md).</span><span class="sxs-lookup"><span data-stu-id="7a08c-154">For more information about opening foreign address book entries, see [Acting as a Host Address Book Provider](acting-as-a-host-address-book-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7a08c-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="7a08c-155">See also</span></span>



[<span data-ttu-id="7a08c-156">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7a08c-156">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

