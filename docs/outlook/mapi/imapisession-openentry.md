---
title: IMAPISessionOpenEntry
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.OpenEntry
api_type:
- COM
ms.assetid: a4df4860-cf4f-4e97-97c4-fcd89b7f1f91
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 10992fdf53c416c473b90b5748b9c5fa4f65cffc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426384"
---
# <a name="imapisessionopenentry"></a><span data-ttu-id="b2931-103">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="b2931-103">IMAPISession::OpenEntry</span></span>

  
  
<span data-ttu-id="b2931-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b2931-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b2931-105">Abre um objeto e retorna um ponteiro de interface para acesso adicional.</span><span class="sxs-lookup"><span data-stu-id="b2931-105">Opens an object and returns an interface pointer for additional access.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="b2931-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b2931-106">Parameters</span></span>

 <span data-ttu-id="b2931-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="b2931-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="b2931-108">no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="b2931-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="b2931-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="b2931-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="b2931-110">no Um ponteiro para o identificador de entrada do objeto a ser aberto.</span><span class="sxs-lookup"><span data-stu-id="b2931-110">[in] A pointer to the entry identifier of the object to open.</span></span>
    
 <span data-ttu-id="b2931-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="b2931-111">_lpInterface_</span></span>
  
> <span data-ttu-id="b2931-112">no Um ponteiro para o identificador de interface (IID) que representa a interface a ser usada para acessar o objeto aberto.</span><span class="sxs-lookup"><span data-stu-id="b2931-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the opened object.</span></span> <span data-ttu-id="b2931-113">Passar NULL retorna a interface padrão do objeto.</span><span class="sxs-lookup"><span data-stu-id="b2931-113">Passing NULL returns the object's standard interface.</span></span> <span data-ttu-id="b2931-114">Por exemplo, se o objeto a ser aberto for uma mensagem, a interface padrão será [IMessage](imessageimapiprop.md); para pastas, é [IMAPIFolder](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="b2931-114">For example, if the object to be opened is a message, the standard interface is [IMessage](imessageimapiprop.md); for folders, it is [IMAPIFolder](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="b2931-115">As interfaces padrão dos objetos do catálogo de endereços são [IDistList](idistlistimapicontainer.md) para uma lista de distribuição e o [IMailUser](imailuserimapiprop.md) para um usuário de mensagens.</span><span class="sxs-lookup"><span data-stu-id="b2931-115">The standard interfaces for address book objects are [IDistList](idistlistimapicontainer.md) for a distribution list and [IMailUser](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="b2931-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b2931-116">_ulFlags_</span></span>
  
> <span data-ttu-id="b2931-117">no Uma bitmask de sinalizadores que controla como o objeto é aberto.</span><span class="sxs-lookup"><span data-stu-id="b2931-117">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="b2931-118">Os seguintes sinalizadores podem ser usados:</span><span class="sxs-lookup"><span data-stu-id="b2931-118">The following flags can be used:</span></span>
    
<span data-ttu-id="b2931-119">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="b2931-119">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="b2931-120">Solicita que o objeto seja aberto usando as permissões de rede máximas permitidas para o usuário e o acesso ao aplicativo cliente máximo.</span><span class="sxs-lookup"><span data-stu-id="b2931-120">Requests that the object be opened by using the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="b2931-121">Por exemplo, se o cliente tiver permissão de leitura/gravação, o objeto deverá ser aberto com permissão de leitura/gravação; Se o cliente tiver permissão somente leitura, o objeto deverá ser aberto com permissão somente leitura.</span><span class="sxs-lookup"><span data-stu-id="b2931-121">For example, if the client has read/write permission, the object should be opened with read/write permission; if the client has read-only permission, the object should be opened with read-only permission.</span></span> 
    
<span data-ttu-id="b2931-122">MAPI_CACHE_OK</span><span class="sxs-lookup"><span data-stu-id="b2931-122">MAPI_CACHE_OK</span></span>
  
> <span data-ttu-id="b2931-123">Use todos os meios, incluindo catálogos de endereços offline, para executar a resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="b2931-123">Use all means, including offline address books, to perform name resolution.</span></span>
    
<span data-ttu-id="b2931-124">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="b2931-124">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="b2931-125">Use apenas o catálogo de endereços offline para executar a resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="b2931-125">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="b2931-126">Por exemplo, você pode usar esse sinalizador para permitir que um aplicativo cliente Abra a lista de endereços global (GAL) no modo cache do Exchange e acesse uma entrada desse catálogo de endereços do cache sem criar tráfego entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="b2931-126">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="b2931-127">Esse sinalizador é suportado apenas pelo provedor de catálogo de endereços do Exchange.</span><span class="sxs-lookup"><span data-stu-id="b2931-127">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="b2931-128">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="b2931-128">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="b2931-129">Permite que o **OpenEntry** seja retornado com êxito, possivelmente antes que o objeto esteja totalmente disponível para o cliente de chamada.</span><span class="sxs-lookup"><span data-stu-id="b2931-129">Allows **OpenEntry** to return successfully, possibly before the object is fully available to the calling client.</span></span> <span data-ttu-id="b2931-130">Se o objeto não estiver disponível, fazer uma chamada de objeto subsequente pode causar um erro.</span><span class="sxs-lookup"><span data-stu-id="b2931-130">If the object is not available, making a subsequent object call can cause an error.</span></span> 
    
<span data-ttu-id="b2931-131">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="b2931-131">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="b2931-132">Solicita permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="b2931-132">Requests read/write permission.</span></span> <span data-ttu-id="b2931-133">Por padrão, os objetos são abertos com permissão somente leitura e os clientes não devem funcionar na pressuposição de que a permissão de leitura/gravação é concedida.</span><span class="sxs-lookup"><span data-stu-id="b2931-133">By default, objects are opened with read-only permission, and clients should not work on the assumption that read/write permission is granted.</span></span> 
    
<span data-ttu-id="b2931-134">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="b2931-134">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="b2931-135">Não use o catálogo de endereços offline para executar a resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="b2931-135">Do not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="b2931-136">Esse sinalizador é suportado apenas pelo provedor de catálogo de endereços do Exchange.</span><span class="sxs-lookup"><span data-stu-id="b2931-136">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="b2931-137">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="b2931-137">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="b2931-138">Mostrar os itens atualmente marcados como excluídos de forma reversível (ou seja, eles estão na fase de tempo de retenção de itens excluídos).</span><span class="sxs-lookup"><span data-stu-id="b2931-138">Show items that are currently marked as soft deleted (that is, they are in the deleted item retention time phase).</span></span>
    
 <span data-ttu-id="b2931-139">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="b2931-139">_lpulObjType_</span></span>
  
> <span data-ttu-id="b2931-140">bota Um ponteiro para o tipo do objeto aberto.</span><span class="sxs-lookup"><span data-stu-id="b2931-140">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="b2931-141">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="b2931-141">_lppUnk_</span></span>
  
> <span data-ttu-id="b2931-142">bota Um ponteiro para um ponteiro para o objeto aberto.</span><span class="sxs-lookup"><span data-stu-id="b2931-142">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b2931-143">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b2931-143">Return value</span></span>

<span data-ttu-id="b2931-144">S_OK</span><span class="sxs-lookup"><span data-stu-id="b2931-144">S_OK</span></span> 
  
> <span data-ttu-id="b2931-145">O objeto foi aberto com êxito.</span><span class="sxs-lookup"><span data-stu-id="b2931-145">The object was opened successfully.</span></span>
    
<span data-ttu-id="b2931-146">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="b2931-146">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="b2931-147">Foi feita uma tentativa de modificar um objeto somente leitura ou uma tentativa de acessar um objeto para o qual o usuário tem permissões insuficientes.</span><span class="sxs-lookup"><span data-stu-id="b2931-147">An attempt was made to modify a read-only object or an attempt was made to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="b2931-148">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="b2931-148">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="b2931-149">Não há um objeto associado ao identificador de entrada passado no parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="b2931-149">There is not an object associated with the entry identifier passed in the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="b2931-150">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="b2931-150">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="b2931-151">O identificador de entrada passado no parâmetro _lpEntryID_ está em um formato irreconhecível.</span><span class="sxs-lookup"><span data-stu-id="b2931-151">The entry identifier passed in the  _lpEntryID_ parameter is in an unrecognizable format.</span></span> <span data-ttu-id="b2931-152">Esse valor normalmente é retornado se o provedor de serviço que contém o objeto não estiver aberto.</span><span class="sxs-lookup"><span data-stu-id="b2931-152">This value is typically returned if the service provider that contains the object is not open.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b2931-153">Comentários</span><span class="sxs-lookup"><span data-stu-id="b2931-153">Remarks</span></span>

<span data-ttu-id="b2931-154">O método **IMAPISession:: OpenEntry** abre um objeto de repositório de mensagens ou de catálogo de endereços, retornando um ponteiro para uma interface que pode ser usada para acessar o objeto.</span><span class="sxs-lookup"><span data-stu-id="b2931-154">The **IMAPISession::OpenEntry** method opens a message store or address book object, returning a pointer to an interface that can be used to access the object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b2931-155">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="b2931-155">Notes to callers</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b2931-156">Ao abrir entradas de pasta em um armazenamento público, como pastas e mensagens, use [IMsgStore:: OpenEntry](imsgstore-openentry.md) em vez de **IMAPISession:: OpenEntry**.</span><span class="sxs-lookup"><span data-stu-id="b2931-156">When opening folder entries on a public store, such as folders and messages, use [IMsgStore::OpenEntry](imsgstore-openentry.md) instead of **IMAPISession::OpenEntry**.</span></span> <span data-ttu-id="b2931-157">Isso garante que as pastas públicas funcionem corretamente quando várias contas do Exchange são definidas em um perfil.</span><span class="sxs-lookup"><span data-stu-id="b2931-157">This ensures that public folders function correctly when multiple Exchange accounts are defined in a profile.</span></span> 
  
<span data-ttu-id="b2931-158">Call **IMAPISession:: OpenEntry** somente quando você não sabe qual tipo de objeto você está abrindo.</span><span class="sxs-lookup"><span data-stu-id="b2931-158">Call **IMAPISession::OpenEntry** only when you do not know what kind of object that you are opening.</span></span> <span data-ttu-id="b2931-159">Se você tiver certeza de que está abrindo uma pasta ou uma mensagem, chame [IMsgStore:: OpenEntry](imsgstore-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="b2931-159">If you know that you are opening a folder or a message, call [IMsgStore::OpenEntry](imsgstore-openentry.md).</span></span> <span data-ttu-id="b2931-160">Se você tiver certeza de que está abrindo um contêiner de catálogo de endereços, um usuário de mensagens ou uma lista de distribuição, chame [IAddrBook:: OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="b2931-160">If you know that you are opening an address book container, a messaging user, or a distribution list, call [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> <span data-ttu-id="b2931-161">Esses métodos mais específicos são mais rápidos do que **IMAPISession:: OpenEntry**.</span><span class="sxs-lookup"><span data-stu-id="b2931-161">These more specific methods are faster than **IMAPISession::OpenEntry**.</span></span> 
  
<span data-ttu-id="b2931-162">MAPI abre todos os objetos com permissão somente leitura, a menos que você defina o sinalizador MAPI_MODIFY ou MAPI_BEST_ACCESS no parâmetro _parâmetroulflags_ .</span><span class="sxs-lookup"><span data-stu-id="b2931-162">MAPI opens all objects with read-only permission, unless you set the MAPI_MODIFY or MAPI_BEST_ACCESS flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="b2931-163">A definição de um desses sinalizadores não garante um tipo de acesso específico; as permissões concedidas dependem do provedor de serviços, o nível de acesso e o objeto.</span><span class="sxs-lookup"><span data-stu-id="b2931-163">Setting one of these flags does not guarantee a particular type of access; the permissions that are granted depend on the service provider, the access level, and the object.</span></span> <span data-ttu-id="b2931-164">Para determinar o nível de acesso do objeto aberto, recupere sua propriedade **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b2931-164">To determine the access level of the opened object, retrieve its **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="b2931-165">Chamar **IMAPISession:: OpenEntry** e setting _lpEntryID_ para apontar para o identificador de entrada de um repositório de mensagens é o mesmo que chamar o método [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md) com o sinalizador MDB_NO_DIALOG definido.</span><span class="sxs-lookup"><span data-stu-id="b2931-165">Calling **IMAPISession::OpenEntry** and setting  _lpEntryID_ to point to the entry identifier of a message store is the same as calling the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method with the MDB_NO_DIALOG flag set.</span></span> <span data-ttu-id="b2931-166">As configurações de sinalizador também são equivalentes, exceto para solicitar permissão de leitura/gravação com o **OpenMsgStore**, você deve definir o sinalizador MDB_WRITE em vez de MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="b2931-166">The flag settings are also equivalent, except that to request read/write permission with **OpenMsgStore**, you must set the MDB_WRITE flag instead of MAPI_MODIFY.</span></span> 
  
<span data-ttu-id="b2931-167">Verifique o valor retornado no parâmetro _lpulObjType_ para determinar se o tipo de objeto retornado é o esperado.</span><span class="sxs-lookup"><span data-stu-id="b2931-167">Check the value returned in the  _lpulObjType_ parameter to determine whether the object type returned is what you expected.</span></span> <span data-ttu-id="b2931-168">Se o tipo de objeto não for o tipo que você esperava, converta o ponteiro do parâmetro _lppUnk_ para um ponteiro do tipo apropriado.</span><span class="sxs-lookup"><span data-stu-id="b2931-168">If the object type is not the type that you expected, cast the pointer from the  _lppUnk_ parameter to a pointer of the appropriate type.</span></span> <span data-ttu-id="b2931-169">Por exemplo, se você estiver abrindo uma pasta, converta _lppUnk_ para um ponteiro do tipo LPMAPIFOLDER.</span><span class="sxs-lookup"><span data-stu-id="b2931-169">For example, if you are opening a folder, cast  _lppUnk_ to a pointer of type LPMAPIFOLDER.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b2931-170">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="b2931-170">MFCMAPI reference</span></span>

<span data-ttu-id="b2931-171">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b2931-171">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b2931-172">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="b2931-172">**File**</span></span>|<span data-ttu-id="b2931-173">**Função**</span><span class="sxs-lookup"><span data-stu-id="b2931-173">**Function**</span></span>|<span data-ttu-id="b2931-174">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="b2931-174">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b2931-175">MAPIFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="b2931-175">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="b2931-176">CallOpenEntry</span><span class="sxs-lookup"><span data-stu-id="b2931-176">CallOpenEntry</span></span>  <br/> |<span data-ttu-id="b2931-177">MFCMAPI usa o método **IMAPISession:: OpenEntry** para abrir um objeto.</span><span class="sxs-lookup"><span data-stu-id="b2931-177">MFCMAPI uses the **IMAPISession::OpenEntry** method to open an object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b2931-178">Confira também</span><span class="sxs-lookup"><span data-stu-id="b2931-178">See also</span></span>



[<span data-ttu-id="b2931-179">IAddrBook::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="b2931-179">IAddrBook::OpenEntry</span></span>](iaddrbook-openentry.md)
  
[<span data-ttu-id="b2931-180">IDistList : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="b2931-180">IDistList : IMAPIContainer</span></span>](idistlistimapicontainer.md)
  
[<span data-ttu-id="b2931-181">IMailUser : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b2931-181">IMailUser : IMAPIProp</span></span>](imailuserimapiprop.md)
  
[<span data-ttu-id="b2931-182">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="b2931-182">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
  
[<span data-ttu-id="b2931-183">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="b2931-183">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)
  
[<span data-ttu-id="b2931-184">IMessage : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b2931-184">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)
  
[<span data-ttu-id="b2931-185">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="b2931-185">IMsgStore::OpenEntry</span></span>](imsgstore-openentry.md)
  
[<span data-ttu-id="b2931-186">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b2931-186">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="b2931-187">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="b2931-187">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

