---
title: IMsgStoreOpenEntry
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.OpenEntry
api_type:
- COM
ms.assetid: a63c42cf-36af-466b-b41e-d6b53ce1c9fb
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 124208a3f5c6bb300aca3699a04b15e842c46cd1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767515"
---
# <a name="imsgstoreopenentry"></a><span data-ttu-id="d7b5f-103">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="d7b5f-103">IMsgStore::OpenEntry</span></span>

  
  
<span data-ttu-id="d7b5f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d7b5f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d7b5f-105">Abre uma pasta ou uma mensagem e retorna um ponteiro de interface para obter mais acesso.</span><span class="sxs-lookup"><span data-stu-id="d7b5f-105">Opens a folder or message and returns an interface pointer for further access.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="d7b5f-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="d7b5f-106">Parameters</span></span>

 <span data-ttu-id="d7b5f-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="d7b5f-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="d7b5f-108">[in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ _._</span><span class="sxs-lookup"><span data-stu-id="d7b5f-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter  _._</span></span>
    
 <span data-ttu-id="d7b5f-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="d7b5f-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="d7b5f-110">[in] Um ponteiro para o identificador de entrada do objeto a ser aberto ou nulo.</span><span class="sxs-lookup"><span data-stu-id="d7b5f-110">[in] A pointer to the entry identifier of the object to open, or NULL.</span></span> <span data-ttu-id="d7b5f-111">Se _lpEntryID_ for definido como NULL, **OpenEntry** abre a pasta raiz para o armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="d7b5f-111">If  _lpEntryID_ is set to NULL, **OpenEntry** opens the root folder for the message store.</span></span> 
    
 <span data-ttu-id="d7b5f-112">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="d7b5f-112">_lpInterface_</span></span>
  
> <span data-ttu-id="d7b5f-113">[in] Um ponteiro para o identificador de interface (IID) que representa a interface para ser usado para acessar o objeto aberto.</span><span class="sxs-lookup"><span data-stu-id="d7b5f-113">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the opened object.</span></span> <span data-ttu-id="d7b5f-114">Passagem nula resulta no objeto da interface padrão ([IMAPIFolder](imapifolderimapicontainer.md) para pastas) e [IMessage](imessageimapiprop.md) para mensagens que está sendo retornado.</span><span class="sxs-lookup"><span data-stu-id="d7b5f-114">Passing NULL results in the object's standard interface ([IMAPIFolder](imapifolderimapicontainer.md) for folders and [IMessage](imessageimapiprop.md) for messages) being returned.</span></span> 
    
 <span data-ttu-id="d7b5f-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d7b5f-115">_ulFlags_</span></span>
  
> <span data-ttu-id="d7b5f-116">[in] Uma bitmask dos sinalizadores que controla como o objeto é aberto.</span><span class="sxs-lookup"><span data-stu-id="d7b5f-116">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="d7b5f-117">Sinalizadores a seguir podem ser usados:</span><span class="sxs-lookup"><span data-stu-id="d7b5f-117">The following flags can be used:</span></span>
    
<span data-ttu-id="d7b5f-118">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="d7b5f-118">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="d7b5f-119">Solicita que o objeto seja aberto usando as permissões de rede máximo permitidas para o usuário e o acesso do aplicativo de cliente máximo.</span><span class="sxs-lookup"><span data-stu-id="d7b5f-119">Requests that the object be opened by using the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="d7b5f-120">Por exemplo, se o cliente tem a permissão de leitura/gravação, o objeto deve ser aberto usando a permissão de leitura/gravação; Se o cliente tem a permissão somente leitura, o objeto deve ser aberto usando permissão somente leitura.</span><span class="sxs-lookup"><span data-stu-id="d7b5f-120">For example, if the client has read/write permission, the object should be opened by using read/write permission; if the client has read-only permission, the object should be opened by using read-only permission.</span></span> 
    
<span data-ttu-id="d7b5f-121">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="d7b5f-121">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="d7b5f-122">Permite **OpenEntry** retornar com êxito, possivelmente antes do objeto é totalmente disponível para o cliente da chamada.</span><span class="sxs-lookup"><span data-stu-id="d7b5f-122">Allows **OpenEntry** to return successfully, possibly before the object is fully available to the calling client.</span></span> <span data-ttu-id="d7b5f-123">Se o objeto não estiver disponível, fazendo uma chamada do objeto subsequente pode gerar um erro.</span><span class="sxs-lookup"><span data-stu-id="d7b5f-123">If the object is not available, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="d7b5f-124">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="d7b5f-124">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="d7b5f-125">Permissão de leitura/gravação solicitações.</span><span class="sxs-lookup"><span data-stu-id="d7b5f-125">Requests read/write permission.</span></span> <span data-ttu-id="d7b5f-126">Por padrão, os objetos são abertos com permissão somente leitura e os clientes não devem funcionar no pressuposto que tem permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="d7b5f-126">By default, objects are opened with read-only permission, and clients should not work on the assumption that read/write permission is granted.</span></span> 
    
 <span data-ttu-id="d7b5f-127">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="d7b5f-127">_lpulObjType_</span></span>
  
> <span data-ttu-id="d7b5f-128">[out] Um ponteiro para o tipo de objeto aberto.</span><span class="sxs-lookup"><span data-stu-id="d7b5f-128">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="d7b5f-129">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="d7b5f-129">_lppUnk_</span></span>
  
> <span data-ttu-id="d7b5f-130">[out] Um ponteiro para um ponteiro para o objeto aberto.</span><span class="sxs-lookup"><span data-stu-id="d7b5f-130">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d7b5f-131">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="d7b5f-131">Return value</span></span>

<span data-ttu-id="d7b5f-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="d7b5f-132">S_OK</span></span> 
  
> <span data-ttu-id="d7b5f-133">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="d7b5f-133">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="d7b5f-134">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="d7b5f-134">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="d7b5f-135">Foi feita uma tentativa para modificar um objeto somente leitura ou para acessar um objeto para o qual o usuário tem permissões insuficientes.</span><span class="sxs-lookup"><span data-stu-id="d7b5f-135">An attempt was made to modify a read-only object or to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="d7b5f-136">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="d7b5f-136">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="d7b5f-137">Quando um repositório é aberto no modo de cache, um provedor de cliente ou serviço pode chamar **IMsgStore::OpenEntry**, definindo o sinalizador MAPI_NO_CACHE para abrir um item ou uma pasta no repositório remoto.</span><span class="sxs-lookup"><span data-stu-id="d7b5f-137">When a store is opened in cached mode, a client or service provider can call **IMsgStore::OpenEntry**, setting the MAPI_NO_CACHE flag to open an item or a folder on the remote store.</span></span> <span data-ttu-id="d7b5f-138">Se você abrir o armazenamento de mensagens com o sinalizador MDB_ONLINE no servidor remoto, você não precisará usar o sinalizador MAPI_NO_CACHE.</span><span class="sxs-lookup"><span data-stu-id="d7b5f-138">If you open the message store with the MDB_ONLINE flag on the remote server, you do not have to use the MAPI_NO_CACHE flag.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d7b5f-139">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="d7b5f-139">Remarks</span></span>

<span data-ttu-id="d7b5f-140">O método **IMsgStore::OpenEntry** abre uma pasta ou uma mensagem e retorna um ponteiro para uma interface que pode ser usada para obter mais acesso.</span><span class="sxs-lookup"><span data-stu-id="d7b5f-140">The **IMsgStore::OpenEntry** method opens a folder or message and returns a pointer to an interface that can be used for further access.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="d7b5f-141">Ao abrir entradas da pasta em um repositório público, como pastas e mensagens, use **IMsgStore::OpenEntry** em vez de [IMAPISession::OpenEntry](imapisession-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="d7b5f-141">When opening folder entries on a public store, such as folders and messages, use **IMsgStore::OpenEntry** instead of [IMAPISession::OpenEntry](imapisession-openentry.md).</span></span> <span data-ttu-id="d7b5f-142">Isso garante que funcionam de pastas públicas corretamente quando várias contas do Exchange são definidas em um perfil.</span><span class="sxs-lookup"><span data-stu-id="d7b5f-142">This ensures that public folders function correctly when multiple Exchange accounts are defined in a profile.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d7b5f-143">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="d7b5f-143">Notes to callers</span></span>

<span data-ttu-id="d7b5f-144">Pastas e mensagens são abertas automaticamente com permissão somente leitura, a menos que você defina o sinalizador MAPI_MODIFY ou MAPI_BEST_ACCESS no parâmetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="d7b5f-144">Folders and messages are automatically opened with read-only permission, unless you set the MAPI_MODIFY or MAPI_BEST_ACCESS flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="d7b5f-145">A definição de uma desses sinalizadores não garante a um determinado tipo de permissão; as permissões são concedidas dependem do provedor de armazenamento de mensagem, seu nível de acesso e o objeto.</span><span class="sxs-lookup"><span data-stu-id="d7b5f-145">Setting one of these flags does not guarantee a particular type of permission; the permissions that you are granted depend on the message store provider, your access level, and the object.</span></span> <span data-ttu-id="d7b5f-146">Para determinar o nível de acesso do objeto aberto, recupere sua propriedade **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d7b5f-146">To determine the access level of the opened object, retrieve its **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="d7b5f-147">Embora **IMsgStore::OpenEntry** pode ser usado para abrir qualquer pasta ou mensagem, é geralmente mais rápido usar o método [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) se você tiver acesso à pasta pai da pasta ou mensagem a ser aberto.</span><span class="sxs-lookup"><span data-stu-id="d7b5f-147">Although **IMsgStore::OpenEntry** can be used to open any folder or message, it is usually faster to use the [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) method if you have access to the parent folder of the folder or message to be opened.</span></span> 
  
<span data-ttu-id="d7b5f-148">Verifica o valor retornado no parâmetro _lpulObjType_ para determinar se o tipo de objeto retornado é esperado.</span><span class="sxs-lookup"><span data-stu-id="d7b5f-148">Check the value returned in the  _lpulObjType_ parameter to determine whether the returned object type is what you expected.</span></span> <span data-ttu-id="d7b5f-149">Se o tipo de objeto não é do tipo esperado, converta o ponteiro do parâmetro _lppUnk_ para um ponteiro do tipo apropriado.</span><span class="sxs-lookup"><span data-stu-id="d7b5f-149">If the object type is not the expected type, cast the pointer from the  _lppUnk_ parameter to a pointer of the appropriate type.</span></span> <span data-ttu-id="d7b5f-150">Por exemplo, se você está abrindo uma pasta, converta os _lppUnk_ para um ponteiro do tipo **LPMAPIFOLDER**.</span><span class="sxs-lookup"><span data-stu-id="d7b5f-150">For example, if you are opening a folder, cast  _lppUnk_ to a pointer of type **LPMAPIFOLDER**.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d7b5f-151">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="d7b5f-151">MFCMAPI reference</span></span>

<span data-ttu-id="d7b5f-152">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d7b5f-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d7b5f-153">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="d7b5f-153">**File**</span></span>|<span data-ttu-id="d7b5f-154">**Function**</span><span class="sxs-lookup"><span data-stu-id="d7b5f-154">**Function**</span></span>|<span data-ttu-id="d7b5f-155">**Comment**</span><span class="sxs-lookup"><span data-stu-id="d7b5f-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d7b5f-156">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="d7b5f-156">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="d7b5f-157">CallOpenEntry</span><span class="sxs-lookup"><span data-stu-id="d7b5f-157">CallOpenEntry</span></span>  <br/> |<span data-ttu-id="d7b5f-158">MFCMAPI usa o método **IMsgStore::OpenEntry** para abrir o objeto associado com uma ID de entrada.</span><span class="sxs-lookup"><span data-stu-id="d7b5f-158">MFCMAPI uses the **IMsgStore::OpenEntry** method to open the object associated with an entry ID.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d7b5f-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7b5f-159">See also</span></span>



[<span data-ttu-id="d7b5f-160">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="d7b5f-160">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)
  
[<span data-ttu-id="d7b5f-161">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="d7b5f-161">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="d7b5f-162">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="d7b5f-162">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

