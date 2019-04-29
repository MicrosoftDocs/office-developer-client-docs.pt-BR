---
title: IMAPISupportOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenEntry
api_type:
- COM
ms.assetid: 84662230-6a25-4403-b87e-871427a40c6e
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: cfbb799336aa1e75fa36e03e55d82c3af3409f10
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409612"
---
# <a name="imapisupportopenentry"></a><span data-ttu-id="47544-103">IMAPISupport::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="47544-103">IMAPISupport::OpenEntry</span></span>

  
  
<span data-ttu-id="47544-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47544-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47544-105">Abre um objeto e retorna um ponteiro de interface para acesso adicional.</span><span class="sxs-lookup"><span data-stu-id="47544-105">Opens an object and returns an interface pointer for further access.</span></span> 
  
```cpp
HRESULT OpenEntry(
ULONG cbEntryID,
LPENTRYID lpEntryID,
LPCIID lpInterface,
ULONG ulOpenFlags,
ULONG FAR * lpulObjType,
LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="47544-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="47544-106">Parameters</span></span>

 <span data-ttu-id="47544-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="47544-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="47544-108">no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="47544-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="47544-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="47544-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="47544-110">no Um ponteiro para o identificador de entrada do objeto a ser aberto.</span><span class="sxs-lookup"><span data-stu-id="47544-110">[in] A pointer to the entry identifier of the object to open.</span></span>
    
 <span data-ttu-id="47544-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="47544-111">_lpInterface_</span></span>
  
> <span data-ttu-id="47544-112">no Um ponteiro para o identificador de interface (IID) que representa a interface a ser usada para acessar o objeto.</span><span class="sxs-lookup"><span data-stu-id="47544-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object.</span></span> <span data-ttu-id="47544-113">Passar resultados nulos na interface padrão do objeto que está sendo retornado.</span><span class="sxs-lookup"><span data-stu-id="47544-113">Passing NULL results in the object's standard interface being returned.</span></span> <span data-ttu-id="47544-114">Por exemplo, se o objeto a ser aberto for uma mensagem, a interface padrão será [IMessage](imessageimapiprop.md); para pastas, é [IMAPIFolder](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="47544-114">For example, if the object to be opened is a message, the standard interface is [IMessage](imessageimapiprop.md); for folders, it is [IMAPIFolder](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="47544-115">As interfaces padrão dos objetos do catálogo de endereços são [IDistList](idistlistimapicontainer.md) para uma lista de distribuição e o [IMailUser](imailuserimapiprop.md) para um usuário de mensagens.</span><span class="sxs-lookup"><span data-stu-id="47544-115">The standard interfaces for address book objects are [IDistList](idistlistimapicontainer.md) for a distribution list and [IMailUser](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="47544-116">_ulOpenFlags_</span><span class="sxs-lookup"><span data-stu-id="47544-116">_ulOpenFlags_</span></span>
  
> <span data-ttu-id="47544-117">no Uma bitmask de sinalizadores que controla como o objeto é aberto.</span><span class="sxs-lookup"><span data-stu-id="47544-117">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="47544-118">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="47544-118">The following flags can be set:</span></span>
    
<span data-ttu-id="47544-119">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="47544-119">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="47544-120">Solicita que o objeto seja aberto com as permissões de rede máximas permitidas para o chamador.</span><span class="sxs-lookup"><span data-stu-id="47544-120">Requests that the object be opened with the maximum network permissions allowed for the caller.</span></span> <span data-ttu-id="47544-121">Por exemplo, se o chamador tiver permissão de leitura/gravação, o objeto deverá ser aberto como leitura/gravação; Se o chamador tiver permissão somente leitura, o objeto deverá ser aberto como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="47544-121">For example, if the caller has read/write permission, the object should be opened as read/write; if the caller has read-only permission, the object should be opened as read-only.</span></span> 
    
<span data-ttu-id="47544-122">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="47544-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="47544-123">Permite que o **OpenEntry** seja retornado com êxito, possivelmente antes que o objeto fique totalmente acessível ao chamador.</span><span class="sxs-lookup"><span data-stu-id="47544-123">Allows **OpenEntry** to return successfully, possibly before the object is fully accessible to the caller.</span></span> <span data-ttu-id="47544-124">Se o objeto não estiver acessível, fazer uma chamada de objeto subsequente pode resultar em um erro.</span><span class="sxs-lookup"><span data-stu-id="47544-124">If the object is not accessible, making a subsequent object call can result in an error.</span></span> 
    
<span data-ttu-id="47544-125">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="47544-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="47544-126">Solicita permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="47544-126">Requests read/write permission.</span></span> <span data-ttu-id="47544-127">Por padrão, os objetos são abertos como somente leitura, e os chamadores não devem funcionar na pressuposição de que a permissão de leitura/gravação tenha sido concedida.</span><span class="sxs-lookup"><span data-stu-id="47544-127">By default, objects are opened as read-only, and callers should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="47544-128">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="47544-128">_lpulObjType_</span></span>
  
> <span data-ttu-id="47544-129">bota Um ponteiro para o tipo do objeto aberto.</span><span class="sxs-lookup"><span data-stu-id="47544-129">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="47544-130">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="47544-130">_lppUnk_</span></span>
  
> <span data-ttu-id="47544-131">bota Um ponteiro para um ponteiro para o objeto aberto.</span><span class="sxs-lookup"><span data-stu-id="47544-131">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="47544-132">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="47544-132">Return value</span></span>

<span data-ttu-id="47544-133">S_OK</span><span class="sxs-lookup"><span data-stu-id="47544-133">S_OK</span></span> 
  
> <span data-ttu-id="47544-134">O objeto foi aberto com êxito.</span><span class="sxs-lookup"><span data-stu-id="47544-134">The object was successfully opened.</span></span>
    
<span data-ttu-id="47544-135">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="47544-135">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="47544-136">Foi feita uma tentativa de modificar um objeto somente leitura ou uma tentativa de acessar um objeto para o qual o usuário tem permissões insuficientes.</span><span class="sxs-lookup"><span data-stu-id="47544-136">An attempt was made to modify a read-only object, or an attempt was made to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="47544-137">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="47544-137">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="47544-138">Não há um objeto associado ao identificador de entrada passado no parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="47544-138">There is not an object associated with the entry identifier passed in the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="47544-139">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="47544-139">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="47544-140">O identificador de entrada passado no parâmetro _lpEntryID_ está em um formato irreconhecível.</span><span class="sxs-lookup"><span data-stu-id="47544-140">The entry identifier passed in the  _lpEntryID_ parameter is in an unrecognizable format.</span></span> <span data-ttu-id="47544-141">Esse valor normalmente é retornado se o provedor de catálogo de endereços que contém o objeto não estiver aberto.</span><span class="sxs-lookup"><span data-stu-id="47544-141">This value is typically returned if the address book provider that contains the object is not open.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="47544-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="47544-142">Remarks</span></span>

<span data-ttu-id="47544-143">O método **IMAPISupport:: OpenEntry** é implementado para todos os objetos de suporte do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="47544-143">The **IMAPISupport::OpenEntry** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="47544-144">Os provedores de serviços chamam **IMAPISupport:: OpenEntry** para recuperar um ponteiro para uma interface que pode ser usada para acessar um objeto específico.</span><span class="sxs-lookup"><span data-stu-id="47544-144">Service providers call **IMAPISupport::OpenEntry** to retrieve a pointer to an interface that can be used to access a particular object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="47544-145">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="47544-145">Notes to callers</span></span>

<span data-ttu-id="47544-146">Call **IMAPISupport:: OpenEntry** somente quando você não sabe qual tipo de objeto você está abrindo.</span><span class="sxs-lookup"><span data-stu-id="47544-146">Call **IMAPISupport::OpenEntry** only when you do not know what kind of object you are opening.</span></span> <span data-ttu-id="47544-147">Se você souber que está abrindo uma pasta ou uma mensagem, chame [IMsgStore:: OpenEntry](imsgstore-openentry.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="47544-147">If you know you are opening a folder or a message, call [IMsgStore::OpenEntry](imsgstore-openentry.md) instead.</span></span> <span data-ttu-id="47544-148">Se você souber que está abrindo um contêiner de catálogo de endereços, um usuário de mensagens ou uma lista de distribuição, chame [IAddrBook:: OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="47544-148">If you know you are opening an address book container, a messaging user, or a distribution list, call [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> <span data-ttu-id="47544-149">Esses métodos mais específicos são mais rápidos do que **IMAPISupport:: OpenEntry**.</span><span class="sxs-lookup"><span data-stu-id="47544-149">These more specific methods are faster than **IMAPISupport::OpenEntry**.</span></span> 
  
 <span data-ttu-id="47544-150">**IMAPISupport:: OpenEntry** abre todos os objetos como somente leitura, a menos que você defina o sinalizador MAPI_MODIFY ou MAPI_BEST_ACCESS no parâmetro _parâmetroulflags_ e suas permissões sejam suficientes.</span><span class="sxs-lookup"><span data-stu-id="47544-150">**IMAPISupport::OpenEntry** opens all objects as read-only, unless you set the MAPI_MODIFY or MAPI_BEST_ACCESS flag in the  _ulFlags_ parameter and your permissions are sufficient.</span></span> <span data-ttu-id="47544-151">A definição de um desses sinalizadores não garante um tipo de acesso específico; as permissões que você recebe dependem do seu nível de acesso, do objeto e do provedor de serviços que possui o objeto.</span><span class="sxs-lookup"><span data-stu-id="47544-151">Setting one of these flags does not guarantee a particular type of access; the permissions that you are granted depend on your access level, the object, and the service provider that owns the object.</span></span> <span data-ttu-id="47544-152">Para determinar o nível de acesso do objeto aberto, recupere sua propriedade **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="47544-152">To determine the access level of the opened object, retrieve its **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="47544-153">Verifique o valor retornado no parâmetro _lpulObjType_ para determinar que o tipo de objeto retornado é o esperado.</span><span class="sxs-lookup"><span data-stu-id="47544-153">Check the value returned in the  _lpulObjType_ parameter to determine that the object type returned is what you expected.</span></span> <span data-ttu-id="47544-154">Se o tipo de objeto for conforme o esperado, converta o ponteiro do parâmetro _lppUnk_ para um ponteiro do tipo apropriado.</span><span class="sxs-lookup"><span data-stu-id="47544-154">If the object type is as expected, cast the pointer from the  _lppUnk_ parameter to a pointer of the appropriate type.</span></span> <span data-ttu-id="47544-155">Por exemplo, se você estiver abrindo uma pasta, converta _lppUnk_ para um ponteiro do tipo LPMAPIFOLDER.</span><span class="sxs-lookup"><span data-stu-id="47544-155">For example, if you are opening a folder, cast  _lppUnk_ to a pointer of type LPMAPIFOLDER.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="47544-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="47544-156">See also</span></span>



[<span data-ttu-id="47544-157">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="47544-157">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

