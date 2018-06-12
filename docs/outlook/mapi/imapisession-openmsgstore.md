---
title: IMAPISessionOpenMsgStore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.OpenMsgStore
api_type:
- COM
ms.assetid: 7f73b5cf-7093-42e9-8acc-63d73df77cf5
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 983c22772acfea7837e85d409b7928a35aed91ce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767191"
---
# <a name="imapisessionopenmsgstore"></a><span data-ttu-id="251ff-103">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="251ff-103">IMAPISession::OpenMsgStore</span></span>

<span data-ttu-id="251ff-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="251ff-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="251ff-105">Abre um armazenamento de mensagens e retorna um ponteiro de [IMsgStore](imsgstoreimapiprop.md) para obter mais acesso.</span><span class="sxs-lookup"><span data-stu-id="251ff-105">Opens a message store and returns an [IMsgStore](imsgstoreimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenMsgStore(
  ULONG_PTR ulUIParam,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPMDB FAR * lppMDB
);
```

## <a name="parameters"></a><span data-ttu-id="251ff-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="251ff-106">Parameters</span></span>

<span data-ttu-id="251ff-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="251ff-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="251ff-108">[in] Um identificador para a janela do pai da caixa de diálogo endereço comuns e outros relacionados a exibe.</span><span class="sxs-lookup"><span data-stu-id="251ff-108">[in] A handle to the parent window of the common address dialog box and other related displays.</span></span>
    
<span data-ttu-id="251ff-109">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="251ff-109">_cbEntryID_</span></span>
  
> <span data-ttu-id="251ff-110">[in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="251ff-110">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="251ff-111">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="251ff-111">_lpEntryID_</span></span>
  
> <span data-ttu-id="251ff-112">[in] Um ponteiro para o identificador de entrada do repositório de mensagem a ser aberto.</span><span class="sxs-lookup"><span data-stu-id="251ff-112">[in] A pointer to the entry identifier of the message store to be opened.</span></span> <span data-ttu-id="251ff-113">O parâmetro _lpEntryID_ não deve ser NULL.</span><span class="sxs-lookup"><span data-stu-id="251ff-113">The  _lpEntryID_ parameter must not be NULL.</span></span> 
    
<span data-ttu-id="251ff-114">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="251ff-114">_lpInterface_</span></span>
  
> <span data-ttu-id="251ff-115">[in] Um ponteiro para o identificador de interface (IID) que representa a interface a ser usado para acessar o repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="251ff-115">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the message store.</span></span> <span data-ttu-id="251ff-116">Passar NULL faz com que o parâmetro _lppMDB_ retornar um ponteiro para a interface padrão para um armazenamento de mensagens (**IMsgStore**).</span><span class="sxs-lookup"><span data-stu-id="251ff-116">Passing NULL causes the  _lppMDB_ parameter to return a pointer to the standard interface for a message store (**IMsgStore**).</span></span>
    
<span data-ttu-id="251ff-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="251ff-117">_ulFlags_</span></span>
  
> <span data-ttu-id="251ff-118">[in] Uma bitmask dos sinalizadores que controla como o objeto é aberto.</span><span class="sxs-lookup"><span data-stu-id="251ff-118">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="251ff-119">Sinalizadores a seguir podem ser usados:</span><span class="sxs-lookup"><span data-stu-id="251ff-119">The following flags can be used:</span></span>
    
  - <span data-ttu-id="251ff-120">MAPI_BEST_ACCESS: Solicitações que o armazenamento de mensagens seja aberto com as permissões de rede máximo permitido para o usuário e o cliente máximo permissões do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="251ff-120">MAPI_BEST_ACCESS: Requests that the message store be opened with the maximum network permissions allowed for the user and the maximum client application permissions.</span></span> <span data-ttu-id="251ff-121">Por exemplo, se o cliente tem a permissão de leitura/gravação, o armazenamento de mensagens deve ser aberto com permissão de leitura/gravação; Se o cliente tem a permissão somente leitura, o armazenamento de mensagens deve ser aberto com permissão somente leitura.</span><span class="sxs-lookup"><span data-stu-id="251ff-121">For example, if the client has read/write permission, the message store should be opened with read/write permission; if the client has read-only permission, the message store should be opened with read-only permission.</span></span> 
      
  - <span data-ttu-id="251ff-122">MAPI_DEFERRED_ERRORS: Permite **OpenMsgStore** retornar com êxito, possivelmente antes da mensagem repositório é totalmente disponível para o cliente da chamada.</span><span class="sxs-lookup"><span data-stu-id="251ff-122">MAPI_DEFERRED_ERRORS: Allows **OpenMsgStore** to return successfully, possibly before the message store is fully available to the calling client.</span></span> <span data-ttu-id="251ff-123">Se o armazenamento de mensagens não estiver disponível, fazendo uma chamada do objeto subsequente pode gerar um erro.</span><span class="sxs-lookup"><span data-stu-id="251ff-123">If the message store is not available, making a subsequent object call can raise an error.</span></span> 
      
  - <span data-ttu-id="251ff-124">MDB\_NO_DIALOG: impede a exibição das caixas de diálogo de logon.</span><span class="sxs-lookup"><span data-stu-id="251ff-124">MDB\_NO_DIALOG: Prevents the display of logon dialog boxes.</span></span> <span data-ttu-id="251ff-125">Se esse sinalizador estiver definido e **OpenMsgStore** tem informações de configuração insuficiente para abrir o armazenamento de mensagens sem a Ajuda do usuário, ele retornará MAPI_E_LOGON_FAILED.</span><span class="sxs-lookup"><span data-stu-id="251ff-125">If this flag is set, and **OpenMsgStore** has insufficient configuration information to open the message store without the user's help, it returns MAPI_E_LOGON_FAILED.</span></span> <span data-ttu-id="251ff-126">Se esse sinalizador não estiver definido, o provedor de armazenamento de mensagens pode solicitar o usuário para corrigir um nome ou a senha ou para executar outras ações necessárias para estabelecer uma conexão para o armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="251ff-126">If this flag is not set, the message store provider can prompt the user to correct a name or password or to perform other actions that are needed to establish a connection to the message store.</span></span> 
      
  - <span data-ttu-id="251ff-127">MDB\_NO_MAIL: O armazenamento de mensagens não deve ser usado para envio ou recebimento de email.</span><span class="sxs-lookup"><span data-stu-id="251ff-127">MDB\_NO_MAIL: The message store should not be used for sending or receiving mail.</span></span> <span data-ttu-id="251ff-128">Quando esse sinalizador estiver definido, MAPI não notificar o spooler MAPI que este armazenamento de mensagens está sendo aberto.</span><span class="sxs-lookup"><span data-stu-id="251ff-128">When this flag is set, MAPI does not notify the MAPI spooler that this message store is being opened.</span></span>
      
  - <span data-ttu-id="251ff-129">MDB\_ONLINE: no modo cache do Exchange, um provedor de cliente ou serviço pode chamar esse método com MDB_ONLINE para substituir a conexão ao repositório de mensagem local e abrir o repositório de servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="251ff-129">MDB\_ONLINE: In Cached Exchange Mode, a client or service provider can call this method with MDB_ONLINE to override the connection to the local message store and open the store on the remote server.</span></span> <span data-ttu-id="251ff-130">Você não pode abrir um repositório do Exchange no modo de cache e no modo em cache não ao mesmo tempo na mesma sessão MAPI.</span><span class="sxs-lookup"><span data-stu-id="251ff-130">You cannot open an Exchange store in cached mode and in non-cached mode at the same time in the same MAPI session.</span></span> <span data-ttu-id="251ff-131">Se você já abriu o armazenamento de mensagens em cache, você deve fechar ou o repositório antes de abri-lo com esse sinalizador ou abra uma nova sessão MAPI, onde você pode abrir o armazenamento do Exchange no servidor remoto usando esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="251ff-131">If you have already opened the cached message store, you must either close the store before you open it with this flag, or open a new MAPI session where you can open the Exchange store on the remote server by using this flag.</span></span>
      
  - <span data-ttu-id="251ff-132">MDB_TEMPORARY: Instrui MAPI que o armazenamento de mensagens não é permanente e não deve ser adicionado à tabela de repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="251ff-132">MDB_TEMPORARY: Instructs MAPI that the message store is not permanent and should not be added to the message store table.</span></span> <span data-ttu-id="251ff-133">Esse sinalizador é usado para fazer o logon no repositório de mensagem para que informações podem ser recuperadas por meio de programação da seção perfil.</span><span class="sxs-lookup"><span data-stu-id="251ff-133">This flag is used to log on to the message store so information can be retrieved programmatically from the profile section.</span></span> 
      
  - <span data-ttu-id="251ff-134">MDB_WRITE: Solicitações de leitura/gravação permissão para o armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="251ff-134">MDB_WRITE: Requests read/write permission to the message store.</span></span>
    
<span data-ttu-id="251ff-135">_lppMDB_</span><span class="sxs-lookup"><span data-stu-id="251ff-135">_lppMDB_</span></span>
  
> <span data-ttu-id="251ff-136">[out] Ponteiro para um ponteiro para o armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="251ff-136">[out] Pointer to a pointer of the message store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="251ff-137">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="251ff-137">Return value</span></span>

<span data-ttu-id="251ff-138">S_OK</span><span class="sxs-lookup"><span data-stu-id="251ff-138">S_OK</span></span> 
  
> <span data-ttu-id="251ff-139">O armazenamento de mensagens foi aberto com êxito.</span><span class="sxs-lookup"><span data-stu-id="251ff-139">The message store was successfully opened.</span></span>
    
<span data-ttu-id="251ff-140">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="251ff-140">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="251ff-141">Foi feita uma tentativa de acessar um armazenamento de mensagens para o qual o usuário tem permissões insuficientes.</span><span class="sxs-lookup"><span data-stu-id="251ff-141">An attempt was made to access a message store for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="251ff-142">E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="251ff-142">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="251ff-143">O armazenamento de mensagens indicado pelo _lpEntryID_ não existe.</span><span class="sxs-lookup"><span data-stu-id="251ff-143">The message store indicated by  _lpEntryID_ does not exist.</span></span> 
    
<span data-ttu-id="251ff-144">MAPI_E_UNKNOWN_CPID</span><span class="sxs-lookup"><span data-stu-id="251ff-144">MAPI_E_UNKNOWN_CPID</span></span> 
  
> <span data-ttu-id="251ff-145">O servidor não está configurado para oferecer suporte à página de código do cliente.</span><span class="sxs-lookup"><span data-stu-id="251ff-145">The server is not configured to support the client's code page.</span></span>
    
<span data-ttu-id="251ff-146">MAPI_E_UNKNOWN_LCID</span><span class="sxs-lookup"><span data-stu-id="251ff-146">MAPI_E_UNKNOWN_LCID</span></span> 
  
> <span data-ttu-id="251ff-147">O servidor não está configurado para oferecer suporte a informações de localidade do cliente.</span><span class="sxs-lookup"><span data-stu-id="251ff-147">The server is not configured to support the client's locale information.</span></span>
    
<span data-ttu-id="251ff-148">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="251ff-148">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="251ff-149">A chamada foi bem-sucedida, mas o provedor de armazenamento de mensagem tem informações de erro disponíveis.</span><span class="sxs-lookup"><span data-stu-id="251ff-149">The call succeeded, but the message store provider has error information available.</span></span> <span data-ttu-id="251ff-150">Quando esse aviso é retornado, a chamada deve ser manipulada com êxito.</span><span class="sxs-lookup"><span data-stu-id="251ff-150">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="251ff-151">Para obter as informações de erro do provedor, chame o método [IMAPISession::GetLastError](imapisession-getlasterror.md) .</span><span class="sxs-lookup"><span data-stu-id="251ff-151">To get the error information from the provider, call the [IMAPISession::GetLastError](imapisession-getlasterror.md) method.</span></span> <span data-ttu-id="251ff-152">Para testar esse aviso, use a macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="251ff-152">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="251ff-153">Para obter mais informações, consulte [Usando Macros para tratamento de erros](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="251ff-153">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="251ff-154">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="251ff-154">Remarks</span></span>

<span data-ttu-id="251ff-155">O método **IMAPISession::OpenMsgStore** abre um armazenamento de mensagens específico.</span><span class="sxs-lookup"><span data-stu-id="251ff-155">The **IMAPISession::OpenMsgStore** method opens a particular message store.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="251ff-156">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="251ff-156">Notes to callers</span></span>

<span data-ttu-id="251ff-157">O nível de permissão padrão para repositórios de mensagem é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="251ff-157">The default permission level for message stores is read-only.</span></span> <span data-ttu-id="251ff-158">Se você definir o sinalizador MDB_WRITE, você ainda pode não ser concedida permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="251ff-158">If you set the MDB_WRITE flag, you still might not be granted read/write permission.</span></span> <span data-ttu-id="251ff-159">Nível de acesso que atribui MAPI para o armazenamento de mensagens depende de seu nível de permissão do final, a mensagem armazenar propriamente dito e o provedor de armazenamento de mensagem.</span><span class="sxs-lookup"><span data-stu-id="251ff-159">The final level of access that MAPI assigns to the message store depends on your permission level, the message store itself, and the message store provider.</span></span> 
  
<span data-ttu-id="251ff-160">Se você chamar **OpenMsgStore** para abrir um armazenamento de mensagens com permissão somente leitura, ocorrerá o seguinte:</span><span class="sxs-lookup"><span data-stu-id="251ff-160">If you call **OpenMsgStore** to open a message store with read-only permission, the following will occur:</span></span> 
  
- <span data-ttu-id="251ff-161">O repositório **PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) propriedade não terá seu armazenamento\_MODIFY_OK e repositório\_CREATE_OK o conjunto de bits.</span><span class="sxs-lookup"><span data-stu-id="251ff-161">The store's **PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property will not have its STORE\_MODIFY_OK and STORE\_CREATE_OK bits set.</span></span> 
    
- <span data-ttu-id="251ff-162">Chamadas para abrir uma das mensagens ou pastas do armazenamento de mensagens usando [IMAPISession::OpenEntry](imapisession-openentry.md) com o sinalizador definido MAPI_MODIFY falhará.</span><span class="sxs-lookup"><span data-stu-id="251ff-162">Calls to open one of the message store's messages or folders by using [IMAPISession::OpenEntry](imapisession-openentry.md) with the MAPI_MODIFY flag set will fail.</span></span> 
    
- <span data-ttu-id="251ff-163">Chamadas para abrir uma das propriedades de mensagens ou pastas do armazenamento de mensagens usando [IMAPIProp::OpenProperty](imapiprop-openproperty.md) com o sinalizador MAPI_MODIFY falhará.</span><span class="sxs-lookup"><span data-stu-id="251ff-163">Calls to open one of the properties of the message store's messages or folders by using [IMAPIProp::OpenProperty](imapiprop-openproperty.md) with the MAPI_MODIFY flag will fail.</span></span> 
    
- <span data-ttu-id="251ff-164">Falharão chamadas para qualquer um dos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="251ff-164">Calls to any of the following methods will fail:</span></span> 
    
  - [<span data-ttu-id="251ff-165">IMAPIFolder::CreateMessage</span><span class="sxs-lookup"><span data-stu-id="251ff-165">IMAPIFolder::CreateMessage</span></span>](imapifolder-createmessage.md)
    
  - [<span data-ttu-id="251ff-166">IMAPIFolder::DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="251ff-166">IMAPIFolder::DeleteMessages</span></span>](imapifolder-deletemessages.md)
    
  - [<span data-ttu-id="251ff-167">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="251ff-167">IMAPIFolder::CreateFolder</span></span>](imapifolder-createfolder.md)
    
  - [<span data-ttu-id="251ff-168">IMAPIFolder::DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="251ff-168">IMAPIFolder::DeleteFolder</span></span>](imapifolder-deletefolder.md)
    
  - [<span data-ttu-id="251ff-169">IMAPIFolder::SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="251ff-169">IMAPIFolder::SetMessageStatus</span></span>](imapifolder-setmessagestatus.md)
    
  - [<span data-ttu-id="251ff-170">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="251ff-170">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
    
  - [<span data-ttu-id="251ff-171">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="251ff-171">IMAPIProp::DeleteProps</span></span>](imapiprop-deleteprops.md)
  
- <span data-ttu-id="251ff-172">Chamadas para os métodos a seguintes irá falhar se o destino da mensagem copiada é somente leitura, se o destino for o mesmo que o armazenamento de mensagens do código-fonte ou outro repositório de somente leitura.</span><span class="sxs-lookup"><span data-stu-id="251ff-172">Calls to the following methods will fail if the destination for the copied message is read-only, whether the destination is the same as the source message store or is another read-only store.</span></span>
    
  - [<span data-ttu-id="251ff-173">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="251ff-173">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
    
  - [<span data-ttu-id="251ff-174">IMAPIFolder::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="251ff-174">IMAPIFolder::CopyFolder</span></span>](imapifolder-copyfolder.md)
    
  - [<span data-ttu-id="251ff-175">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="251ff-175">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="251ff-176">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="251ff-176">MFCMAPI reference</span></span>

<span data-ttu-id="251ff-177">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="251ff-177">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="251ff-178">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="251ff-178">**File**</span></span>|<span data-ttu-id="251ff-179">**Function**</span><span class="sxs-lookup"><span data-stu-id="251ff-179">**Function**</span></span>|<span data-ttu-id="251ff-180">**Comment**</span><span class="sxs-lookup"><span data-stu-id="251ff-180">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="251ff-181">MAPIStoreFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="251ff-181">MAPIStoreFunctions.cpp</span></span>  <br/> |<span data-ttu-id="251ff-182">CallOpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="251ff-182">CallOpenMsgStore</span></span>  <br/> |<span data-ttu-id="251ff-183">MFCMAPI usa o método **IMAPISession::OpenMsgStore** para abrir um armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="251ff-183">MFCMAPI uses the **IMAPISession::OpenMsgStore** method to open a message store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="251ff-184">Confira também</span><span class="sxs-lookup"><span data-stu-id="251ff-184">See also</span></span>

- [<span data-ttu-id="251ff-185">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="251ff-185">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)
- [<span data-ttu-id="251ff-186">IMAPISession::GetLastError</span><span class="sxs-lookup"><span data-stu-id="251ff-186">IMAPISession::GetLastError</span></span>](imapisession-getlasterror.md)
- [<span data-ttu-id="251ff-187">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="251ff-187">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)
- [<span data-ttu-id="251ff-188">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="251ff-188">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
- [<span data-ttu-id="251ff-189">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="251ff-189">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)
- [<span data-ttu-id="251ff-190">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="251ff-190">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
- [<span data-ttu-id="251ff-191">Usando Macros para tratamento de erros</span><span class="sxs-lookup"><span data-stu-id="251ff-191">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

