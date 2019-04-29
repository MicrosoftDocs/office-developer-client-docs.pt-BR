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
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 19d3df004676a71e2bf6243d9288efd824d99c33
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418019"
---
# <a name="imapisessionopenmsgstore"></a><span data-ttu-id="065ea-103">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="065ea-103">IMAPISession::OpenMsgStore</span></span>

<span data-ttu-id="065ea-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="065ea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="065ea-105">Abre um repositório de mensagens e retorna um ponteiro [IMsgStore](imsgstoreimapiprop.md) para obter mais acesso.</span><span class="sxs-lookup"><span data-stu-id="065ea-105">Opens a message store and returns an [IMsgStore](imsgstoreimapiprop.md) pointer for further access.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="065ea-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="065ea-106">Parameters</span></span>

<span data-ttu-id="065ea-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="065ea-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="065ea-108">no Uma alça para a janela pai da caixa de diálogo endereço comum e outros vídeos relacionados.</span><span class="sxs-lookup"><span data-stu-id="065ea-108">[in] A handle to the parent window of the common address dialog box and other related displays.</span></span>
    
<span data-ttu-id="065ea-109">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="065ea-109">_cbEntryID_</span></span>
  
> <span data-ttu-id="065ea-110">no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="065ea-110">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="065ea-111">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="065ea-111">_lpEntryID_</span></span>
  
> <span data-ttu-id="065ea-112">no Um ponteiro para o identificador de entrada do repositório de mensagens a ser aberto.</span><span class="sxs-lookup"><span data-stu-id="065ea-112">[in] A pointer to the entry identifier of the message store to be opened.</span></span> <span data-ttu-id="065ea-113">O parâmetro _lpEntryID_ não deve ser nulo.</span><span class="sxs-lookup"><span data-stu-id="065ea-113">The  _lpEntryID_ parameter must not be NULL.</span></span> 
    
<span data-ttu-id="065ea-114">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="065ea-114">_lpInterface_</span></span>
  
> <span data-ttu-id="065ea-115">no Um ponteiro para o identificador de interface (IID) que representa a interface a ser usada para acessar o repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="065ea-115">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the message store.</span></span> <span data-ttu-id="065ea-116">Passar NULL faz com que o parâmetro _lppMDB_ retorne um ponteiro para a interface padrão de um repositório de mensagens (**IMsgStore**).</span><span class="sxs-lookup"><span data-stu-id="065ea-116">Passing NULL causes the  _lppMDB_ parameter to return a pointer to the standard interface for a message store (**IMsgStore**).</span></span>
    
<span data-ttu-id="065ea-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="065ea-117">_ulFlags_</span></span>
  
> <span data-ttu-id="065ea-118">no Uma bitmask de sinalizadores que controla como o objeto é aberto.</span><span class="sxs-lookup"><span data-stu-id="065ea-118">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="065ea-119">Os seguintes sinalizadores podem ser usados:</span><span class="sxs-lookup"><span data-stu-id="065ea-119">The following flags can be used:</span></span>
    
  - <span data-ttu-id="065ea-120">MAPI_BEST_ACCESS: solicita que o repositório de mensagens seja aberto com as permissões de rede máximas permitidas para o usuário e as permissões máximas do aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="065ea-120">MAPI_BEST_ACCESS: Requests that the message store be opened with the maximum network permissions allowed for the user and the maximum client application permissions.</span></span> <span data-ttu-id="065ea-121">Por exemplo, se o cliente tiver permissão de leitura/gravação, o repositório de mensagens deverá ser aberto com permissão de leitura/gravação; Se o cliente tiver permissão somente leitura, o repositório de mensagens deverá ser aberto com permissão somente leitura.</span><span class="sxs-lookup"><span data-stu-id="065ea-121">For example, if the client has read/write permission, the message store should be opened with read/write permission; if the client has read-only permission, the message store should be opened with read-only permission.</span></span> 
      
  - <span data-ttu-id="065ea-122">MAPI_DEFERRED_ERRORS: permite que o **OpenMsgStore** seja retornado com êxito, possivelmente antes que o repositório de mensagens esteja totalmente disponível para o cliente de chamada.</span><span class="sxs-lookup"><span data-stu-id="065ea-122">MAPI_DEFERRED_ERRORS: Allows **OpenMsgStore** to return successfully, possibly before the message store is fully available to the calling client.</span></span> <span data-ttu-id="065ea-123">Se o repositório de mensagens não estiver disponível, fazer uma chamada de objeto subsequente poderá gerar um erro.</span><span class="sxs-lookup"><span data-stu-id="065ea-123">If the message store is not available, making a subsequent object call can raise an error.</span></span> 
      
  - <span data-ttu-id="065ea-124">MDB\_NO_DIALOG: impede a exibição de caixas de diálogo de logon.</span><span class="sxs-lookup"><span data-stu-id="065ea-124">MDB\_NO_DIALOG: Prevents the display of logon dialog boxes.</span></span> <span data-ttu-id="065ea-125">Se esse sinalizador estiver definido, e **OpenMsgStore** tiver informações de configuração insuficientes para abrir o repositório de mensagens sem a ajuda do usuário, ele retornará MAPI_E_LOGON_FAILED.</span><span class="sxs-lookup"><span data-stu-id="065ea-125">If this flag is set, and **OpenMsgStore** has insufficient configuration information to open the message store without the user's help, it returns MAPI_E_LOGON_FAILED.</span></span> <span data-ttu-id="065ea-126">Se esse sinalizador não for definido, o provedor do repositório de mensagens poderá solicitar que o usuário corrija um nome ou senha ou execute outras ações necessárias para estabelecer uma conexão com o repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="065ea-126">If this flag is not set, the message store provider can prompt the user to correct a name or password or to perform other actions that are needed to establish a connection to the message store.</span></span> 
      
  - <span data-ttu-id="065ea-127">MDB\_NO_MAIL: o repositório de mensagens não deve ser usado para enviar ou receber emails.</span><span class="sxs-lookup"><span data-stu-id="065ea-127">MDB\_NO_MAIL: The message store should not be used for sending or receiving mail.</span></span> <span data-ttu-id="065ea-128">Quando esse sinalizador é definido, o MAPI não notifica o spooler MAPI que este repositório de mensagens está sendo aberto.</span><span class="sxs-lookup"><span data-stu-id="065ea-128">When this flag is set, MAPI does not notify the MAPI spooler that this message store is being opened.</span></span>
      
  - <span data-ttu-id="065ea-129">MDB\_online: no modo cache do Exchange, um cliente ou provedor de serviços pode chamar esse método com MDB_ONLINE para substituir a conexão ao repositório de mensagens local e abrir o repositório no servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="065ea-129">MDB\_ONLINE: In Cached Exchange Mode, a client or service provider can call this method with MDB_ONLINE to override the connection to the local message store and open the store on the remote server.</span></span> <span data-ttu-id="065ea-130">Não é possível abrir um repositório do Exchange no modo de cache e no modo não armazenado em cache ao mesmo tempo na mesma sessão MAPI.</span><span class="sxs-lookup"><span data-stu-id="065ea-130">You cannot open an Exchange store in cached mode and in non-cached mode at the same time in the same MAPI session.</span></span> <span data-ttu-id="065ea-131">Se você já tiver aberto o arquivo de cache mensagens, você deve fechar o repositório antes de abri-lo com esse sinalizador ou abrir uma nova sessão MAPI onde você pode abrir o armazenamento do Exchange no servidor remoto usando esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="065ea-131">If you have already opened the cached message store, you must either close the store before you open it with this flag, or open a new MAPI session where you can open the Exchange store on the remote server by using this flag.</span></span>
      
  - <span data-ttu-id="065ea-132">MDB_TEMPORARY: instrui o MAPI de que o repositório de mensagens não é permanente e não deve ser adicionado à tabela do repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="065ea-132">MDB_TEMPORARY: Instructs MAPI that the message store is not permanent and should not be added to the message store table.</span></span> <span data-ttu-id="065ea-133">Esse sinalizador é usado para fazer logon no repositório de mensagens para que as informações possam ser recuperadas programaticamente da seção perfil.</span><span class="sxs-lookup"><span data-stu-id="065ea-133">This flag is used to log on to the message store so information can be retrieved programmatically from the profile section.</span></span> 
      
  - <span data-ttu-id="065ea-134">MDB_WRITE: solicita permissão de leitura/gravação para o repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="065ea-134">MDB_WRITE: Requests read/write permission to the message store.</span></span>
    
<span data-ttu-id="065ea-135">_lppMDB_</span><span class="sxs-lookup"><span data-stu-id="065ea-135">_lppMDB_</span></span>
  
> <span data-ttu-id="065ea-136">bota Ponteiro para um ponteiro do repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="065ea-136">[out] Pointer to a pointer of the message store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="065ea-137">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="065ea-137">Return value</span></span>

<span data-ttu-id="065ea-138">S_OK</span><span class="sxs-lookup"><span data-stu-id="065ea-138">S_OK</span></span> 
  
> <span data-ttu-id="065ea-139">O repositório de mensagens foi aberto com êxito.</span><span class="sxs-lookup"><span data-stu-id="065ea-139">The message store was successfully opened.</span></span>
    
<span data-ttu-id="065ea-140">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="065ea-140">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="065ea-141">Foi feita uma tentativa de acessar um repositório de mensagens para o qual o usuário tem permissões insuficientes.</span><span class="sxs-lookup"><span data-stu-id="065ea-141">An attempt was made to access a message store for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="065ea-142">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="065ea-142">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="065ea-143">O repositório de mensagens indicado pelo _lpEntryID_ não existe.</span><span class="sxs-lookup"><span data-stu-id="065ea-143">The message store indicated by  _lpEntryID_ does not exist.</span></span> 
    
<span data-ttu-id="065ea-144">MAPI_E_UNKNOWN_CPID</span><span class="sxs-lookup"><span data-stu-id="065ea-144">MAPI_E_UNKNOWN_CPID</span></span> 
  
> <span data-ttu-id="065ea-145">O servidor não está configurado para dar suporte à página de código do cliente.</span><span class="sxs-lookup"><span data-stu-id="065ea-145">The server is not configured to support the client's code page.</span></span>
    
<span data-ttu-id="065ea-146">MAPI_E_UNKNOWN_LCID</span><span class="sxs-lookup"><span data-stu-id="065ea-146">MAPI_E_UNKNOWN_LCID</span></span> 
  
> <span data-ttu-id="065ea-147">O servidor não está configurado para dar suporte às informações de localidade do cliente.</span><span class="sxs-lookup"><span data-stu-id="065ea-147">The server is not configured to support the client's locale information.</span></span>
    
<span data-ttu-id="065ea-148">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="065ea-148">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="065ea-149">A chamada teve êxito, mas o provedor do repositório de mensagens tem informações de erro disponíveis.</span><span class="sxs-lookup"><span data-stu-id="065ea-149">The call succeeded, but the message store provider has error information available.</span></span> <span data-ttu-id="065ea-150">Quando esse aviso é retornado, a chamada deve ser tratada como bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="065ea-150">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="065ea-151">Para obter as informações de erro do provedor, chame o método [IMAPISession:: GetLastError](imapisession-getlasterror.md) .</span><span class="sxs-lookup"><span data-stu-id="065ea-151">To get the error information from the provider, call the [IMAPISession::GetLastError](imapisession-getlasterror.md) method.</span></span> <span data-ttu-id="065ea-152">Para testar esse aviso, use a macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="065ea-152">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="065ea-153">Para obter mais informações, consulte [usando macros para tratamento de erros](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="065ea-153">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="065ea-154">Comentários</span><span class="sxs-lookup"><span data-stu-id="065ea-154">Remarks</span></span>

<span data-ttu-id="065ea-155">O método **IMAPISession:: OpenMsgStore** abre um repositório de mensagens específico.</span><span class="sxs-lookup"><span data-stu-id="065ea-155">The **IMAPISession::OpenMsgStore** method opens a particular message store.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="065ea-156">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="065ea-156">Notes to callers</span></span>

<span data-ttu-id="065ea-157">O nível de permissão padrão para repositórios de mensagens é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="065ea-157">The default permission level for message stores is read-only.</span></span> <span data-ttu-id="065ea-158">Se você definir o sinalizador MDB_WRITE, ainda poderá não receber permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="065ea-158">If you set the MDB_WRITE flag, you still might not be granted read/write permission.</span></span> <span data-ttu-id="065ea-159">O nível final de acesso que o MAPI atribui ao repositório de mensagens depende do seu nível de permissão, do próprio repositório de mensagens e do provedor de armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="065ea-159">The final level of access that MAPI assigns to the message store depends on your permission level, the message store itself, and the message store provider.</span></span> 
  
<span data-ttu-id="065ea-160">Se você chamar **OpenMsgStore** para abrir um repositório de mensagens com permissão somente leitura, ocorrerá o seguinte:</span><span class="sxs-lookup"><span data-stu-id="065ea-160">If you call **OpenMsgStore** to open a message store with read-only permission, the following will occur:</span></span> 
  
- <span data-ttu-id="065ea-161">A propriedade **PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) da loja não terá seus bits de\_armazenamento MODIFY_OK e\_Store CREATE_OK definidos.</span><span class="sxs-lookup"><span data-stu-id="065ea-161">The store's **PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property will not have its STORE\_MODIFY_OK and STORE\_CREATE_OK bits set.</span></span> 
    
- <span data-ttu-id="065ea-162">As chamadas para abrir uma das mensagens ou pastas do repositório de mensagens usando o [IMAPISession:: OpenEntry](imapisession-openentry.md) com o sinalizador de MAPI_MODIFY falharão.</span><span class="sxs-lookup"><span data-stu-id="065ea-162">Calls to open one of the message store's messages or folders by using [IMAPISession::OpenEntry](imapisession-openentry.md) with the MAPI_MODIFY flag set will fail.</span></span> 
    
- <span data-ttu-id="065ea-163">Chamadas para abrir uma das propriedades das mensagens ou pastas do repositório de mensagens usando [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) com o sinalizador MAPI_MODIFY falharão.</span><span class="sxs-lookup"><span data-stu-id="065ea-163">Calls to open one of the properties of the message store's messages or folders by using [IMAPIProp::OpenProperty](imapiprop-openproperty.md) with the MAPI_MODIFY flag will fail.</span></span> 
    
- <span data-ttu-id="065ea-164">As chamadas para qualquer um dos seguintes métodos falharão:</span><span class="sxs-lookup"><span data-stu-id="065ea-164">Calls to any of the following methods will fail:</span></span> 
    
  - [<span data-ttu-id="065ea-165">IMAPIFolder::CreateMessage</span><span class="sxs-lookup"><span data-stu-id="065ea-165">IMAPIFolder::CreateMessage</span></span>](imapifolder-createmessage.md)
    
  - [<span data-ttu-id="065ea-166">IMAPIFolder::DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="065ea-166">IMAPIFolder::DeleteMessages</span></span>](imapifolder-deletemessages.md)
    
  - [<span data-ttu-id="065ea-167">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="065ea-167">IMAPIFolder::CreateFolder</span></span>](imapifolder-createfolder.md)
    
  - [<span data-ttu-id="065ea-168">IMAPIFolder::DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="065ea-168">IMAPIFolder::DeleteFolder</span></span>](imapifolder-deletefolder.md)
    
  - [<span data-ttu-id="065ea-169">IMAPIFolder::SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="065ea-169">IMAPIFolder::SetMessageStatus</span></span>](imapifolder-setmessagestatus.md)
    
  - [<span data-ttu-id="065ea-170">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="065ea-170">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
    
  - [<span data-ttu-id="065ea-171">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="065ea-171">IMAPIProp::DeleteProps</span></span>](imapiprop-deleteprops.md)
  
- <span data-ttu-id="065ea-172">As chamadas para os seguintes métodos falharão se o destino da mensagem copiada for somente leitura, se o destino for o mesmo que o repositório de mensagens de origem ou se for outro repositório somente leitura.</span><span class="sxs-lookup"><span data-stu-id="065ea-172">Calls to the following methods will fail if the destination for the copied message is read-only, whether the destination is the same as the source message store or is another read-only store.</span></span>
    
  - [<span data-ttu-id="065ea-173">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="065ea-173">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
    
  - [<span data-ttu-id="065ea-174">IMAPIFolder::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="065ea-174">IMAPIFolder::CopyFolder</span></span>](imapifolder-copyfolder.md)
    
  - [<span data-ttu-id="065ea-175">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="065ea-175">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="065ea-176">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="065ea-176">MFCMAPI reference</span></span>

<span data-ttu-id="065ea-177">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="065ea-177">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="065ea-178">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="065ea-178">**File**</span></span>|<span data-ttu-id="065ea-179">**Função**</span><span class="sxs-lookup"><span data-stu-id="065ea-179">**Function**</span></span>|<span data-ttu-id="065ea-180">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="065ea-180">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="065ea-181">MAPIStoreFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="065ea-181">MAPIStoreFunctions.cpp</span></span>  <br/> |<span data-ttu-id="065ea-182">CallOpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="065ea-182">CallOpenMsgStore</span></span>  <br/> |<span data-ttu-id="065ea-183">MFCMAPI usa o método **IMAPISession:: OpenMsgStore** para abrir um repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="065ea-183">MFCMAPI uses the **IMAPISession::OpenMsgStore** method to open a message store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="065ea-184">Confira também</span><span class="sxs-lookup"><span data-stu-id="065ea-184">See also</span></span>

- [<span data-ttu-id="065ea-185">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="065ea-185">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)
- [<span data-ttu-id="065ea-186">IMAPISession::GetLastError</span><span class="sxs-lookup"><span data-stu-id="065ea-186">IMAPISession::GetLastError</span></span>](imapisession-getlasterror.md)
- [<span data-ttu-id="065ea-187">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="065ea-187">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)
- [<span data-ttu-id="065ea-188">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="065ea-188">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
- [<span data-ttu-id="065ea-189">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="065ea-189">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)
- [<span data-ttu-id="065ea-190">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="065ea-190">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
- [<span data-ttu-id="065ea-191">Usando macros para tratamento de erros</span><span class="sxs-lookup"><span data-stu-id="065ea-191">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

