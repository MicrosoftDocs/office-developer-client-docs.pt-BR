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
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 07667558a21a9110d684164d2e6c143d6a519368
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309692"
---
# <a name="imsgstoreopenentry"></a><span data-ttu-id="895d9-103">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="895d9-103">IMsgStore::OpenEntry</span></span>

  
  
<span data-ttu-id="895d9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="895d9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="895d9-105">Abre uma pasta ou mensagem e retorna um ponteiro de interface para acesso adicional.</span><span class="sxs-lookup"><span data-stu-id="895d9-105">Opens a folder or message and returns an interface pointer for further access.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="895d9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="895d9-106">Parameters</span></span>

 <span data-ttu-id="895d9-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="895d9-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="895d9-108">no A contagem de bytes no identificador de entrada apontado pelo __ parâmetro lpEntryID _._</span><span class="sxs-lookup"><span data-stu-id="895d9-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter  _._</span></span>
    
 <span data-ttu-id="895d9-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="895d9-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="895d9-110">no Um ponteiro para o identificador de entrada do objeto a ser aberto ou nulo.</span><span class="sxs-lookup"><span data-stu-id="895d9-110">[in] A pointer to the entry identifier of the object to open, or NULL.</span></span> <span data-ttu-id="895d9-111">Se _lpEntryID_ estiver definido como nulo, **OpenEntry** abrirá a pasta raiz do repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="895d9-111">If  _lpEntryID_ is set to NULL, **OpenEntry** opens the root folder for the message store.</span></span> 
    
 <span data-ttu-id="895d9-112">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="895d9-112">_lpInterface_</span></span>
  
> <span data-ttu-id="895d9-113">no Um ponteiro para o identificador de interface (IID) que representa a interface a ser usada para acessar o objeto aberto.</span><span class="sxs-lookup"><span data-stu-id="895d9-113">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the opened object.</span></span> <span data-ttu-id="895d9-114">Passar resultados nulos na interface padrão do objeto ([IMAPIFolder](imapifolderimapicontainer.md) para pastas e [IMessage](imessageimapiprop.md) para mensagens) que está sendo retornada.</span><span class="sxs-lookup"><span data-stu-id="895d9-114">Passing NULL results in the object's standard interface ([IMAPIFolder](imapifolderimapicontainer.md) for folders and [IMessage](imessageimapiprop.md) for messages) being returned.</span></span> 
    
 <span data-ttu-id="895d9-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="895d9-115">_ulFlags_</span></span>
  
> <span data-ttu-id="895d9-116">no Uma bitmask de sinalizadores que controla como o objeto é aberto.</span><span class="sxs-lookup"><span data-stu-id="895d9-116">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="895d9-117">Os seguintes sinalizadores podem ser usados:</span><span class="sxs-lookup"><span data-stu-id="895d9-117">The following flags can be used:</span></span>
    
<span data-ttu-id="895d9-118">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="895d9-118">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="895d9-119">Solicita que o objeto seja aberto usando as permissões de rede máximas permitidas para o usuário e o acesso ao aplicativo cliente máximo.</span><span class="sxs-lookup"><span data-stu-id="895d9-119">Requests that the object be opened by using the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="895d9-120">Por exemplo, se o cliente tiver permissão de leitura/gravação, o objeto deverá ser aberto usando permissão de leitura/gravação; Se o cliente tiver permissão somente leitura, o objeto deverá ser aberto usando a permissão somente leitura.</span><span class="sxs-lookup"><span data-stu-id="895d9-120">For example, if the client has read/write permission, the object should be opened by using read/write permission; if the client has read-only permission, the object should be opened by using read-only permission.</span></span> 
    
<span data-ttu-id="895d9-121">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="895d9-121">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="895d9-122">Permite que o **OpenEntry** seja retornado com êxito, possivelmente antes que o objeto esteja totalmente disponível para o cliente de chamada.</span><span class="sxs-lookup"><span data-stu-id="895d9-122">Allows **OpenEntry** to return successfully, possibly before the object is fully available to the calling client.</span></span> <span data-ttu-id="895d9-123">Se o objeto não estiver disponível, fazer uma chamada de objeto subsequente poderá gerar um erro.</span><span class="sxs-lookup"><span data-stu-id="895d9-123">If the object is not available, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="895d9-124">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="895d9-124">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="895d9-125">Solicita permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="895d9-125">Requests read/write permission.</span></span> <span data-ttu-id="895d9-126">Por padrão, os objetos são abertos com permissão somente leitura e os clientes não devem funcionar na pressuposição de que a permissão de leitura/gravação é concedida.</span><span class="sxs-lookup"><span data-stu-id="895d9-126">By default, objects are opened with read-only permission, and clients should not work on the assumption that read/write permission is granted.</span></span> 
    
 <span data-ttu-id="895d9-127">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="895d9-127">_lpulObjType_</span></span>
  
> <span data-ttu-id="895d9-128">bota Um ponteiro para o tipo do objeto aberto.</span><span class="sxs-lookup"><span data-stu-id="895d9-128">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="895d9-129">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="895d9-129">_lppUnk_</span></span>
  
> <span data-ttu-id="895d9-130">bota Um ponteiro para um ponteiro para o objeto aberto.</span><span class="sxs-lookup"><span data-stu-id="895d9-130">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="895d9-131">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="895d9-131">Return value</span></span>

<span data-ttu-id="895d9-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="895d9-132">S_OK</span></span> 
  
> <span data-ttu-id="895d9-133">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="895d9-133">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="895d9-134">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="895d9-134">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="895d9-135">Foi feita uma tentativa de modificar um objeto somente leitura ou para acessar um objeto para o qual o usuário tem permissões insuficientes.</span><span class="sxs-lookup"><span data-stu-id="895d9-135">An attempt was made to modify a read-only object or to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="895d9-136">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="895d9-136">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="895d9-137">Quando um repositório é aberto no modo cache, um cliente ou um provedor de serviços pode chamar **IMsgStore:: OpenEntry**, definindo o sinalizador MAPI_NO_CACHE para abrir um item ou uma pasta no repositório remoto.</span><span class="sxs-lookup"><span data-stu-id="895d9-137">When a store is opened in cached mode, a client or service provider can call **IMsgStore::OpenEntry**, setting the MAPI_NO_CACHE flag to open an item or a folder on the remote store.</span></span> <span data-ttu-id="895d9-138">Se você abrir o repositório de mensagens com o sinalizador MDB_ONLINE no servidor remoto, não será necessário usar o sinalizador MAPI_NO_CACHE.</span><span class="sxs-lookup"><span data-stu-id="895d9-138">If you open the message store with the MDB_ONLINE flag on the remote server, you do not have to use the MAPI_NO_CACHE flag.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="895d9-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="895d9-139">Remarks</span></span>

<span data-ttu-id="895d9-140">O método **IMsgStore:: OpenEntry** abre uma pasta ou mensagem e retorna um ponteiro para uma interface que pode ser usada para acesso adicional.</span><span class="sxs-lookup"><span data-stu-id="895d9-140">The **IMsgStore::OpenEntry** method opens a folder or message and returns a pointer to an interface that can be used for further access.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="895d9-141">Ao abrir entradas de pasta em um armazenamento público, como pastas e mensagens, use **IMsgStore:: OpenEntry** em vez de [IMAPISession:: OpenEntry](imapisession-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="895d9-141">When opening folder entries on a public store, such as folders and messages, use **IMsgStore::OpenEntry** instead of [IMAPISession::OpenEntry](imapisession-openentry.md).</span></span> <span data-ttu-id="895d9-142">Isso garante que as pastas públicas funcionem corretamente quando várias contas do Exchange são definidas em um perfil.</span><span class="sxs-lookup"><span data-stu-id="895d9-142">This ensures that public folders function correctly when multiple Exchange accounts are defined in a profile.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="895d9-143">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="895d9-143">Notes to callers</span></span>

<span data-ttu-id="895d9-144">Pastas e mensagens são automaticamente abertas com permissão somente leitura, a menos que você defina o sinalizador MAPI_MODIFY ou MAPI_BEST_ACCESS no parâmetro _parâmetroulflags_ .</span><span class="sxs-lookup"><span data-stu-id="895d9-144">Folders and messages are automatically opened with read-only permission, unless you set the MAPI_MODIFY or MAPI_BEST_ACCESS flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="895d9-145">A definição de um desses sinalizadores não garante um tipo específico de permissão; as permissões que você recebe dependem do provedor de armazenamento de mensagens, seu nível de acesso e o objeto.</span><span class="sxs-lookup"><span data-stu-id="895d9-145">Setting one of these flags does not guarantee a particular type of permission; the permissions that you are granted depend on the message store provider, your access level, and the object.</span></span> <span data-ttu-id="895d9-146">Para determinar o nível de acesso do objeto aberto, recupere sua propriedade **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="895d9-146">To determine the access level of the opened object, retrieve its **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="895d9-147">Embora **IMsgStore:: OpenEntry** possa ser usado para abrir qualquer pasta ou mensagem, geralmente é mais rápido usar o método [IMAPIContainer:: OpenEntry](imapicontainer-openentry.md) se você tiver acesso à pasta pai da pasta ou da mensagem a ser aberta.</span><span class="sxs-lookup"><span data-stu-id="895d9-147">Although **IMsgStore::OpenEntry** can be used to open any folder or message, it is usually faster to use the [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) method if you have access to the parent folder of the folder or message to be opened.</span></span> 
  
<span data-ttu-id="895d9-148">Verifique o valor retornado no parâmetro _lpulObjType_ para determinar se o tipo de objeto retornado é o que você esperava.</span><span class="sxs-lookup"><span data-stu-id="895d9-148">Check the value returned in the  _lpulObjType_ parameter to determine whether the returned object type is what you expected.</span></span> <span data-ttu-id="895d9-149">Se o tipo de objeto não for do tipo esperado, converta o ponteiro do parâmetro _lppUnk_ para um ponteiro do tipo apropriado.</span><span class="sxs-lookup"><span data-stu-id="895d9-149">If the object type is not the expected type, cast the pointer from the  _lppUnk_ parameter to a pointer of the appropriate type.</span></span> <span data-ttu-id="895d9-150">Por exemplo, se você estiver abrindo uma pasta, converta _lppUnk_ para um ponteiro do tipo **LPMAPIFOLDER**.</span><span class="sxs-lookup"><span data-stu-id="895d9-150">For example, if you are opening a folder, cast  _lppUnk_ to a pointer of type **LPMAPIFOLDER**.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="895d9-151">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="895d9-151">MFCMAPI reference</span></span>

<span data-ttu-id="895d9-152">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="895d9-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="895d9-153">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="895d9-153">**File**</span></span>|<span data-ttu-id="895d9-154">**Função**</span><span class="sxs-lookup"><span data-stu-id="895d9-154">**Function**</span></span>|<span data-ttu-id="895d9-155">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="895d9-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="895d9-156">MAPIFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="895d9-156">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="895d9-157">CallOpenEntry</span><span class="sxs-lookup"><span data-stu-id="895d9-157">CallOpenEntry</span></span>  <br/> |<span data-ttu-id="895d9-158">MFCMAPI usa o método **IMsgStore:: OpenEntry** para abrir o objeto associado a uma ID de entrada.</span><span class="sxs-lookup"><span data-stu-id="895d9-158">MFCMAPI uses the **IMsgStore::OpenEntry** method to open the object associated with an entry ID.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="895d9-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="895d9-159">See also</span></span>



[<span data-ttu-id="895d9-160">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="895d9-160">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)
  
[<span data-ttu-id="895d9-161">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="895d9-161">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="895d9-162">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="895d9-162">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

