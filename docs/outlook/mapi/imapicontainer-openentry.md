---
title: IMAPIContainerOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.OpenEntry
api_type:
- COM
ms.assetid: 0c46c1fb-dd63-4ac5-960e-80f68e75d8f4
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 9598e0c90c16db14cdc3a46d2b2ae74e0d9a9300
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423633"
---
# <a name="imapicontaineropenentry"></a><span data-ttu-id="5db7b-103">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="5db7b-103">IMAPIContainer::OpenEntry</span></span>

  
  
<span data-ttu-id="5db7b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5db7b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5db7b-105">Abre um objeto no contêiner, retornando um ponteiro de interface para acesso adicional.</span><span class="sxs-lookup"><span data-stu-id="5db7b-105">Opens an object in the container, returning an interface pointer for further access.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="5db7b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5db7b-106">Parameters</span></span>

 <span data-ttu-id="5db7b-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="5db7b-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="5db7b-108">no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="5db7b-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="5db7b-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="5db7b-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="5db7b-110">no Um ponteiro para o identificador de entrada do objeto a ser aberto.</span><span class="sxs-lookup"><span data-stu-id="5db7b-110">[in] A pointer to the entry identifier of the object to open.</span></span> <span data-ttu-id="5db7b-111">Se _lpEntryID_ estiver definido como nulo, o contêiner de nível superior na hierarquia do contêiner será aberto.</span><span class="sxs-lookup"><span data-stu-id="5db7b-111">If  _lpEntryID_ is set to NULL, the top-level container in the container's hierarchy is opened.</span></span> 
    
 <span data-ttu-id="5db7b-112">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="5db7b-112">_lpInterface_</span></span>
  
> <span data-ttu-id="5db7b-113">no Um ponteiro para o identificador de interface (IID) que representa a interface a ser usada para acessar o objeto.</span><span class="sxs-lookup"><span data-stu-id="5db7b-113">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object.</span></span> <span data-ttu-id="5db7b-114">Passar resultados nulos no identificador para a interface padrão do objeto que está sendo retornada.</span><span class="sxs-lookup"><span data-stu-id="5db7b-114">Passing NULL results in the identifier for the object's standard interface being returned.</span></span> <span data-ttu-id="5db7b-115">Para mensagens, a interface padrão é [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md); para pastas, é [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="5db7b-115">For messages, the standard interface is [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md); for folders, it is [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="5db7b-116">As interfaces padrão para os objetos do catálogo de endereços são [IDistList: IMAPIContainer](idistlistimapicontainer.md) para uma lista de distribuição e [IMailUser: IMAPIProp](imailuserimapiprop.md) para um usuário de mensagens.</span><span class="sxs-lookup"><span data-stu-id="5db7b-116">The standard interfaces for address book objects are [IDistList : IMAPIContainer](idistlistimapicontainer.md) for a distribution list and [IMailUser : IMAPIProp](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="5db7b-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5db7b-117">_ulFlags_</span></span>
  
> <span data-ttu-id="5db7b-118">no Uma bitmask de sinalizadores que controla como o objeto é aberto.</span><span class="sxs-lookup"><span data-stu-id="5db7b-118">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="5db7b-119">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="5db7b-119">The following flags can be set:</span></span>
    
<span data-ttu-id="5db7b-120">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="5db7b-120">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="5db7b-121">Solicita que o objeto será aberto com as permissões de rede máximas permitidas para o usuário e o acesso ao aplicativo cliente máximo.</span><span class="sxs-lookup"><span data-stu-id="5db7b-121">Requests that the object will be opened with the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="5db7b-122">Por exemplo, se o cliente tiver permissão de leitura/gravação, o objeto deverá ser aberto com permissão de leitura/gravação; Se o cliente tiver acesso somente leitura, o objeto deverá ser aberto com acesso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="5db7b-122">For example, if the client has read/write permission, the object should be opened with read/write permission; if the client has read-only access, the object should be opened with read-only access.</span></span> 
    
<span data-ttu-id="5db7b-123">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="5db7b-123">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="5db7b-124">Permite que o **OpenEntry** seja retornado com êxito, possivelmente antes que o objeto esteja totalmente disponível para o cliente de chamada.</span><span class="sxs-lookup"><span data-stu-id="5db7b-124">Allows **OpenEntry** to return successfully, possibly before the object is fully available to the calling client.</span></span> <span data-ttu-id="5db7b-125">Se o objeto não estiver disponível, fazer uma chamada de objeto subsequente poderá gerar um erro.</span><span class="sxs-lookup"><span data-stu-id="5db7b-125">If the object is not available, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="5db7b-126">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="5db7b-126">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="5db7b-127">Solicita permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="5db7b-127">Requests read/write permission.</span></span> <span data-ttu-id="5db7b-128">Por padrão, os objetos são abertos com acesso somente leitura e os clientes não devem funcionar na pressuposição de que a permissão de leitura/gravação tenha sido concedida.</span><span class="sxs-lookup"><span data-stu-id="5db7b-128">By default, objects are opened with read-only access, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
<span data-ttu-id="5db7b-129">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="5db7b-129">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="5db7b-130">Mostra os itens atualmente marcados como excluídos por software, ou seja, estão na fase de tempo de retenção de item excluído.</span><span class="sxs-lookup"><span data-stu-id="5db7b-130">Shows items that are currently marked as soft deleted—that is, they are in the deleted item retention time phase.</span></span>
    
 <span data-ttu-id="5db7b-131">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="5db7b-131">_lpulObjType_</span></span>
  
> <span data-ttu-id="5db7b-132">bota Um ponteiro para o tipo do objeto aberto.</span><span class="sxs-lookup"><span data-stu-id="5db7b-132">[out] A pointer to the opened object's type.</span></span>
    
 <span data-ttu-id="5db7b-133">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="5db7b-133">_lppUnk_</span></span>
  
> <span data-ttu-id="5db7b-134">bota Um ponteiro para um ponteiro para a implementação da interface a ser usada para acessar o objeto Open.</span><span class="sxs-lookup"><span data-stu-id="5db7b-134">[out] A pointer to a pointer to the interface implementation to use to access the open object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5db7b-135">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="5db7b-135">Return value</span></span>

<span data-ttu-id="5db7b-136">S_OK</span><span class="sxs-lookup"><span data-stu-id="5db7b-136">S_OK</span></span> 
  
> <span data-ttu-id="5db7b-137">O objeto foi aberto com êxito.</span><span class="sxs-lookup"><span data-stu-id="5db7b-137">The object was successfully opened.</span></span>
    
<span data-ttu-id="5db7b-138">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="5db7b-138">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="5db7b-139">O usuário tem permissões insuficientes para abrir o objeto ou foi feita uma tentativa de abrir um objeto somente leitura com permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="5db7b-139">Either the user has insufficient permissions to open the object or an attempt was made to open a read-only object with read/write permission.</span></span>
    
<span data-ttu-id="5db7b-140">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="5db7b-140">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="5db7b-141">O identificador de entrada especificado por _lpEntryID_ não representa um objeto.</span><span class="sxs-lookup"><span data-stu-id="5db7b-141">The entry identifier specified by  _lpEntryID_ does not represent an object.</span></span> 
    
<span data-ttu-id="5db7b-142">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="5db7b-142">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="5db7b-143">O identificador de entrada no parâmetro _lpEntryID_ não é de um formato reconhecido pelo contêiner.</span><span class="sxs-lookup"><span data-stu-id="5db7b-143">The entry identifier in the  _lpEntryID_ parameter is not of a format recognized by the container.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5db7b-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="5db7b-144">Remarks</span></span>

<span data-ttu-id="5db7b-145">O método **IMAPIContainer:: OpenEntry** abre um objeto em um contêiner e retorna um ponteiro para uma implementação de interface a ser usada para obter mais acesso.</span><span class="sxs-lookup"><span data-stu-id="5db7b-145">The **IMAPIContainer::OpenEntry** method opens an object throughout a container and returns a pointer to an interface implementation to use for further access.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="5db7b-146">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="5db7b-146">Notes to callers</span></span>

<span data-ttu-id="5db7b-147">Como os provedores de serviço não precisam retornar uma implementação de interface do tipo especificado pelo identificador de interface no parâmetro _lpInterface_ , verifique o valor apontado pelo parâmetro _lpulObjType_ .</span><span class="sxs-lookup"><span data-stu-id="5db7b-147">Because service providers are not required to return an interface implementation of the type specified by the interface identifier in the  _lpInterface_ parameter, check the value pointed to by the  _lpulObjType_ parameter.</span></span> <span data-ttu-id="5db7b-148">Se necessário, converta o ponteiro retornado em _lppUnk_ para um ponteiro do tipo apropriado.</span><span class="sxs-lookup"><span data-stu-id="5db7b-148">If necessary, cast the pointer returned in  _lppUnk_ to a pointer of the appropriate type.</span></span> 
  
<span data-ttu-id="5db7b-149">Por padrão, os provedores de serviços abrem objetos com acesso somente leitura, a menos que você defina o sinalizador MAPI_MODIFY ou MAPI_BEST_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="5db7b-149">By default, service providers open objects with read-only access unless you set either the MAPI_MODIFY or MAPI_BEST_ACCESS flag.</span></span> <span data-ttu-id="5db7b-150">Quando um desses sinalizadores é definido, os provedores de serviços tentam retornar um objeto modificável.</span><span class="sxs-lookup"><span data-stu-id="5db7b-150">When one of these flags is set, service providers attempt to return a modifiable object.</span></span> <span data-ttu-id="5db7b-151">No enTanto, não presuma que porque você solicitou um objeto modificável que o objeto aberto tem permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="5db7b-151">However, do not assume that because you requested a modifiable object that the opened object has read/write permission.</span></span> <span data-ttu-id="5db7b-152">Planeje a chance de uma modificação subsequente falhar ou recuperar a propriedade **PR_ACCESS_LEVEL** do objeto para determinar o nível de acesso concedido pelo **OpenEntry**.</span><span class="sxs-lookup"><span data-stu-id="5db7b-152">Either plan for the chance of a subsequent modification to fail or retrieve the object's **PR_ACCESS_LEVEL** property to determine the access level granted by **OpenEntry**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5db7b-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="5db7b-153">See also</span></span>



[<span data-ttu-id="5db7b-154">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="5db7b-154">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)

