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
# <a name="imapicontaineropenentry"></a><span data-ttu-id="06316-103">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="06316-103">IMAPIContainer::OpenEntry</span></span>

  
  
<span data-ttu-id="06316-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="06316-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="06316-105">Abre um objeto no contêiner, retornando um ponteiro de interface para mais acesso.</span><span class="sxs-lookup"><span data-stu-id="06316-105">Opens an object in the container, returning an interface pointer for further access.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="06316-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="06316-106">Parameters</span></span>

 <span data-ttu-id="06316-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="06316-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="06316-108">[in] A contagem de byte no identificador de entrada apontado pelo parâmetro _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="06316-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="06316-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="06316-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="06316-110">[in] Um ponteiro para o identificador de entrada do objeto a ser aberto.</span><span class="sxs-lookup"><span data-stu-id="06316-110">[in] A pointer to the entry identifier of the object to open.</span></span> <span data-ttu-id="06316-111">Se  _lpEntryID_ estiver definido como NULL, o contêiner de nível superior na hierarquia do contêiner será aberto.</span><span class="sxs-lookup"><span data-stu-id="06316-111">If  _lpEntryID_ is set to NULL, the top-level container in the container's hierarchy is opened.</span></span> 
    
 <span data-ttu-id="06316-112">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="06316-112">_lpInterface_</span></span>
  
> <span data-ttu-id="06316-113">[in] Um ponteiro para o IID (identificador de interface) que representa a interface a ser usada para acessar o objeto.</span><span class="sxs-lookup"><span data-stu-id="06316-113">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object.</span></span> <span data-ttu-id="06316-114">Passar resultados NULL no identificador para a interface padrão do objeto que está sendo retornada.</span><span class="sxs-lookup"><span data-stu-id="06316-114">Passing NULL results in the identifier for the object's standard interface being returned.</span></span> <span data-ttu-id="06316-115">Para mensagens, a interface padrão [é IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md); para pastas, é [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="06316-115">For messages, the standard interface is [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md); for folders, it is [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="06316-116">As interfaces padrão para objetos de livro de endereços são [IDistList : IMAPIContainer](idistlistimapicontainer.md) para uma lista de distribuição e [IMailUser : IMAPIProp](imailuserimapiprop.md) para um usuário de mensagens.</span><span class="sxs-lookup"><span data-stu-id="06316-116">The standard interfaces for address book objects are [IDistList : IMAPIContainer](idistlistimapicontainer.md) for a distribution list and [IMailUser : IMAPIProp](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="06316-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="06316-117">_ulFlags_</span></span>
  
> <span data-ttu-id="06316-118">[in] Uma máscara de bits de sinalizadores que controla como o objeto é aberto.</span><span class="sxs-lookup"><span data-stu-id="06316-118">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="06316-119">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="06316-119">The following flags can be set:</span></span>
    
<span data-ttu-id="06316-120">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="06316-120">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="06316-121">Solicita que o objeto seja aberto com as permissões máximas de rede permitidas para o usuário e o acesso máximo ao aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="06316-121">Requests that the object will be opened with the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="06316-122">Por exemplo, se o cliente tiver permissão de leitura/gravação, o objeto deverá ser aberto com permissão de leitura/gravação; se o cliente tiver acesso somente leitura, o objeto deverá ser aberto com acesso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="06316-122">For example, if the client has read/write permission, the object should be opened with read/write permission; if the client has read-only access, the object should be opened with read-only access.</span></span> 
    
<span data-ttu-id="06316-123">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="06316-123">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="06316-124">Permite que **OpenEntry** retorne com êxito, possivelmente antes do objeto estar totalmente disponível para o cliente de chamada.</span><span class="sxs-lookup"><span data-stu-id="06316-124">Allows **OpenEntry** to return successfully, possibly before the object is fully available to the calling client.</span></span> <span data-ttu-id="06316-125">Se o objeto não estiver disponível, fazer uma chamada de objeto subsequente poderá criar um erro.</span><span class="sxs-lookup"><span data-stu-id="06316-125">If the object is not available, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="06316-126">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="06316-126">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="06316-127">Solicita permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="06316-127">Requests read/write permission.</span></span> <span data-ttu-id="06316-128">Por padrão, os objetos são abertos com acesso somente leitura e os clientes não devem trabalhar com a suposição de que a permissão de leitura/gravação foi concedida.</span><span class="sxs-lookup"><span data-stu-id="06316-128">By default, objects are opened with read-only access, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
<span data-ttu-id="06316-129">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="06316-129">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="06316-130">Mostra itens que estão marcados como excluídos de forma suave, ou seja, eles estão na fase de tempo de retenção de itens excluídos.</span><span class="sxs-lookup"><span data-stu-id="06316-130">Shows items that are currently marked as soft deleted—that is, they are in the deleted item retention time phase.</span></span>
    
 <span data-ttu-id="06316-131">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="06316-131">_lpulObjType_</span></span>
  
> <span data-ttu-id="06316-132">[out] Um ponteiro para o tipo do objeto aberto.</span><span class="sxs-lookup"><span data-stu-id="06316-132">[out] A pointer to the opened object's type.</span></span>
    
 <span data-ttu-id="06316-133">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="06316-133">_lppUnk_</span></span>
  
> <span data-ttu-id="06316-134">[out] Um ponteiro para um ponteiro para a implementação da interface a ser usada para acessar o objeto aberto.</span><span class="sxs-lookup"><span data-stu-id="06316-134">[out] A pointer to a pointer to the interface implementation to use to access the open object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="06316-135">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="06316-135">Return value</span></span>

<span data-ttu-id="06316-136">S_OK</span><span class="sxs-lookup"><span data-stu-id="06316-136">S_OK</span></span> 
  
> <span data-ttu-id="06316-137">O objeto foi aberto com êxito.</span><span class="sxs-lookup"><span data-stu-id="06316-137">The object was successfully opened.</span></span>
    
<span data-ttu-id="06316-138">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="06316-138">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="06316-139">O usuário tem permissões insuficientes para abrir o objeto ou foi feita uma tentativa de abrir um objeto somente leitura com permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="06316-139">Either the user has insufficient permissions to open the object or an attempt was made to open a read-only object with read/write permission.</span></span>
    
<span data-ttu-id="06316-140">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="06316-140">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="06316-141">O identificador de entrada especificado por  _lpEntryID_ não representa um objeto.</span><span class="sxs-lookup"><span data-stu-id="06316-141">The entry identifier specified by  _lpEntryID_ does not represent an object.</span></span> 
    
<span data-ttu-id="06316-142">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="06316-142">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="06316-143">O identificador de entrada no  _parâmetro lpEntryID_ não tem um formato reconhecido pelo contêiner.</span><span class="sxs-lookup"><span data-stu-id="06316-143">The entry identifier in the  _lpEntryID_ parameter is not of a format recognized by the container.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="06316-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="06316-144">Remarks</span></span>

<span data-ttu-id="06316-145">O **método IMAPIContainer::OpenEntry** abre um objeto em um contêiner e retorna um ponteiro para uma implementação de interface a ser usada para mais acesso.</span><span class="sxs-lookup"><span data-stu-id="06316-145">The **IMAPIContainer::OpenEntry** method opens an object throughout a container and returns a pointer to an interface implementation to use for further access.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="06316-146">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="06316-146">Notes to callers</span></span>

<span data-ttu-id="06316-147">Como os provedores de serviços não são obrigados a retornar uma implementação de interface do tipo especificado pelo identificador de interface no parâmetro _lpInterface,_ verifique o valor apontado pelo parâmetro _lpulObjType._</span><span class="sxs-lookup"><span data-stu-id="06316-147">Because service providers are not required to return an interface implementation of the type specified by the interface identifier in the  _lpInterface_ parameter, check the value pointed to by the  _lpulObjType_ parameter.</span></span> <span data-ttu-id="06316-148">Se necessário, cast the pointer returned in  _lppUnk_ to a pointer of the appropriate type.</span><span class="sxs-lookup"><span data-stu-id="06316-148">If necessary, cast the pointer returned in  _lppUnk_ to a pointer of the appropriate type.</span></span> 
  
<span data-ttu-id="06316-149">Por padrão, os provedores de serviços abrem objetos com acesso somente leitura, a menos que você de definir o sinalizador MAPI_MODIFY ou MAPI_BEST_ACCESS leitura.</span><span class="sxs-lookup"><span data-stu-id="06316-149">By default, service providers open objects with read-only access unless you set either the MAPI_MODIFY or MAPI_BEST_ACCESS flag.</span></span> <span data-ttu-id="06316-150">Quando um desses sinalizadores é definido, os provedores de serviços tentam retornar um objeto modificável.</span><span class="sxs-lookup"><span data-stu-id="06316-150">When one of these flags is set, service providers attempt to return a modifiable object.</span></span> <span data-ttu-id="06316-151">No entanto, não pressupõe isso porque você solicitou um objeto modificável que o objeto aberto tem permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="06316-151">However, do not assume that because you requested a modifiable object that the opened object has read/write permission.</span></span> <span data-ttu-id="06316-152">Qualquer um dos planos para a chance de uma  modificação subsequente falhar ou recuperar a propriedade PR_ACCESS_LEVEL do objeto para determinar o nível de acesso concedido por **OpenEntry**.</span><span class="sxs-lookup"><span data-stu-id="06316-152">Either plan for the chance of a subsequent modification to fail or retrieve the object's **PR_ACCESS_LEVEL** property to determine the access level granted by **OpenEntry**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="06316-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="06316-153">See also</span></span>



[<span data-ttu-id="06316-154">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="06316-154">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)

