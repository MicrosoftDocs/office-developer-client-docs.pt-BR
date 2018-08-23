---
title: IMSProviderSpoolerLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider.SpoolerLogon
api_type:
- COM
ms.assetid: 79d5af23-efad-4013-a330-56babfb2bb0f
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 56c025713b0cc2b41a4bf4463f48f8d7c3d2124b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586414"
---
# <a name="imsproviderspoolerlogon"></a><span data-ttu-id="1714e-103">IMSProvider::SpoolerLogon</span><span class="sxs-lookup"><span data-stu-id="1714e-103">IMSProvider::SpoolerLogon</span></span>

  
  
<span data-ttu-id="1714e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1714e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1714e-105">Registra o MAPI spooler em um armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="1714e-105">Logs the MAPI spooler on to a message store.</span></span>
  
```cpp
HRESULT SpoolerLogon(
  LPMAPISUP lpMAPISup,
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags,
  LPCIID lpInterface,
  ULONG cbSpoolSecurity,
  LPBYTE lpbSpoolSecurity,
  LPMAPIERROR FAR * lppMAPIError,
  LPMSLOGON FAR * lppMSLogon,
  LPMDB FAR * lppMDB     
);
```

## <a name="parameters"></a><span data-ttu-id="1714e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1714e-106">Parameters</span></span>

 <span data-ttu-id="1714e-107">_lpMAPISup_</span><span class="sxs-lookup"><span data-stu-id="1714e-107">_lpMAPISup_</span></span>
  
> <span data-ttu-id="1714e-108">[in] Um ponteiro para MAPI suporte ao objeto para o armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="1714e-108">[in] A pointer to the MAPI support object for the message store.</span></span>
    
 <span data-ttu-id="1714e-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="1714e-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="1714e-110">[in] Um identificador para a janela do pai de quaisquer caixas de diálogo ou windows esse método exibe.</span><span class="sxs-lookup"><span data-stu-id="1714e-110">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> 
    
 <span data-ttu-id="1714e-111">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="1714e-111">_lpszProfileName_</span></span>
  
> <span data-ttu-id="1714e-112">[in] Um ponteiro para uma cadeia de caracteres que contém o nome do perfil que está sendo usado para o logon de spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="1714e-112">[in] A pointer to a string that contains the name of the profile being used for the MAPI spooler logon.</span></span> <span data-ttu-id="1714e-113">Esta cadeia de caracteres pode ser exibida nas caixas de diálogo, gravada em um arquivo de log ou simplesmente ignorada.</span><span class="sxs-lookup"><span data-stu-id="1714e-113">This string can be displayed in dialog boxes, written out to a log file, or simply ignored.</span></span> <span data-ttu-id="1714e-114">Ele deve estar no formato Unicode, se o sinalizador MAPI_UNICODE é definido no parâmetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="1714e-114">It must be in Unicode format if the MAPI_UNICODE flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="1714e-115">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="1714e-115">_cbEntryID_</span></span>
  
> <span data-ttu-id="1714e-116">[in] O tamanho, em bytes, do identificador de entrada apontado pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="1714e-116">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="1714e-117">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="1714e-117">_lpEntryID_</span></span>
  
> <span data-ttu-id="1714e-118">[in] Um ponteiro para o identificador de entrada para o armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="1714e-118">[in] A pointer to the entry identifier for the message store.</span></span> <span data-ttu-id="1714e-119">Passar NULL no parâmetro _lpEntryID_ indica que um armazenamento de mensagens ainda não foi selecionado e que as caixas de diálogo que permitem que o usuário selecione um armazenamento de mensagens podem ser apresentadas.</span><span class="sxs-lookup"><span data-stu-id="1714e-119">Passing NULL in the  _lpEntryID_ parameter indicates that a message store has not yet been selected and that dialog boxes that enable the user to select a message store can be presented.</span></span> 
    
 <span data-ttu-id="1714e-120">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1714e-120">_ulFlags_</span></span>
  
> <span data-ttu-id="1714e-121">[in] Uma bitmask dos sinalizadores que controla como o logon é executado.</span><span class="sxs-lookup"><span data-stu-id="1714e-121">[in] A bitmask of flags that controls how the logon is performed.</span></span> <span data-ttu-id="1714e-122">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="1714e-122">The following flags can be set:</span></span>
    
<span data-ttu-id="1714e-123">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="1714e-123">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="1714e-124">A chamada será autorizada tenha êxito, mesmo se o objeto subjacente não está disponível para a implementação de chamada.</span><span class="sxs-lookup"><span data-stu-id="1714e-124">The call is allowed to succeed even if the underlying object is not available to the calling implementation.</span></span> <span data-ttu-id="1714e-125">Se o objeto não estiver disponível, uma chamada subsequente ao objeto pode gerar um erro.</span><span class="sxs-lookup"><span data-stu-id="1714e-125">If the object is not available, a subsequent call to the object might raise an error.</span></span>
    
<span data-ttu-id="1714e-126">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1714e-126">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="1714e-127">As cadeias de caracteres passada na estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="1714e-127">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="1714e-128">Se MAPI_UNICODE não estiver definida, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="1714e-128">If MAPI_UNICODE is not set, the strings are in ANSI format.</span></span>
    
<span data-ttu-id="1714e-129">MDB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="1714e-129">MDB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="1714e-130">Impede a exibição das caixas de diálogo de logon.</span><span class="sxs-lookup"><span data-stu-id="1714e-130">Prevents the display of logon dialog boxes.</span></span> <span data-ttu-id="1714e-131">Se esse sinalizador estiver definido, o valor de erro MAPI_E_LOGON_FAILED retornado se o logon for bem sucedido.</span><span class="sxs-lookup"><span data-stu-id="1714e-131">If this flag is set, the error value MAPI_E_LOGON_FAILED is returned if the logon is unsuccessful.</span></span> <span data-ttu-id="1714e-132">Se esse sinalizador não estiver definido, o provedor de armazenamento de mensagens pode solicita ao usuário para corrigir um nome ou a senha, insira um disco ou para executar outras ações necessárias para estabelecer a conexão para o repositório.</span><span class="sxs-lookup"><span data-stu-id="1714e-132">If this flag is not set, the message store provider can prompt the user to correct a name or password, to insert a disk, or to perform other actions necessary to establish connection to the store.</span></span>
    
<span data-ttu-id="1714e-133">MDB_WRITE</span><span class="sxs-lookup"><span data-stu-id="1714e-133">MDB_WRITE</span></span> 
  
> <span data-ttu-id="1714e-134">Permissão de leitura/gravação solicitações.</span><span class="sxs-lookup"><span data-stu-id="1714e-134">Requests read/write permission.</span></span>
    
 <span data-ttu-id="1714e-135">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="1714e-135">_lpInterface_</span></span>
  
> <span data-ttu-id="1714e-136">[in] Um ponteiro para o identificador de interface (IID) para o armazenamento de mensagens fazer logon.</span><span class="sxs-lookup"><span data-stu-id="1714e-136">[in] A pointer to the interface identifier (IID) for the message store to log on to.</span></span> <span data-ttu-id="1714e-137">Passar NULL indica que a interface MAPI para o armazenamento de mensagens ([IMsgStore](imsgstoreimapiprop.md)) é retornada.</span><span class="sxs-lookup"><span data-stu-id="1714e-137">Passing NULL indicates the MAPI interface for the message store ([IMsgStore](imsgstoreimapiprop.md)) is returned.</span></span> <span data-ttu-id="1714e-138">O parâmetro _lpInterface_ também pode ser definido como um identificador para uma interface apropriado para o armazenamento de mensagens (por exemplo, IID_IUnknown ou IID_IMAPIProp).</span><span class="sxs-lookup"><span data-stu-id="1714e-138">The  _lpInterface_ parameter can also be set to an identifier for an appropriate interface for the message store (for example IID_IUnknown or IID_IMAPIProp).</span></span> 
    
 <span data-ttu-id="1714e-139">_cbSpoolSecurity_</span><span class="sxs-lookup"><span data-stu-id="1714e-139">_cbSpoolSecurity_</span></span>
  
> <span data-ttu-id="1714e-140">[in] Um ponteiro para o tamanho, em bytes, de dados de validação no parâmetro _lppbSpoolSecurity_ .</span><span class="sxs-lookup"><span data-stu-id="1714e-140">[in] A pointer to the size, in bytes, of validation data in the  _lppbSpoolSecurity_ parameter.</span></span> 
    
 <span data-ttu-id="1714e-141">_lpbSpoolSecurity_</span><span class="sxs-lookup"><span data-stu-id="1714e-141">_lpbSpoolSecurity_</span></span>
  
> <span data-ttu-id="1714e-142">[in] Um ponteiro para um ponteiro para validação de dados.</span><span class="sxs-lookup"><span data-stu-id="1714e-142">[in] A pointer to a pointer to validation data.</span></span> <span data-ttu-id="1714e-143">O método **SpoolerLogon** usa esses dados para efetuar o MAPI spooler no mesmo armazenamento como o provedor de armazenamento de mensagem anteriormente logon usando o método [IMSProvider::Logon](imsprovider-logon.md) .</span><span class="sxs-lookup"><span data-stu-id="1714e-143">The **SpoolerLogon** method uses this data to log the MAPI spooler on to the same store as the message store provider previously logged on to by using the [IMSProvider::Logon](imsprovider-logon.md) method.</span></span> 
    
 <span data-ttu-id="1714e-144">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="1714e-144">_lppMAPIError_</span></span>
  
> <span data-ttu-id="1714e-145">[out] Um ponteiro para um ponteiro para a retornado [MAPIERROR](mapierror.md) estrutura, se houver, que contém informações de versão, componente e contexto para um erro.</span><span class="sxs-lookup"><span data-stu-id="1714e-145">[out] A pointer to a pointer to the returned [MAPIERROR](mapierror.md) structure, if any, that contains version, component, and context information for an error.</span></span> <span data-ttu-id="1714e-146">O parâmetro _lppMAPIError_ pode ser definido como NULL se não houver nenhuma estrutura **MAPIERROR** para retornar.</span><span class="sxs-lookup"><span data-stu-id="1714e-146">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
 <span data-ttu-id="1714e-147">_lppMSLogon_</span><span class="sxs-lookup"><span data-stu-id="1714e-147">_lppMSLogon_</span></span>
  
> <span data-ttu-id="1714e-148">[out] Um ponteiro para o ponteiro para a mensagem armazenar o objeto de logon de MAPI fazer logon.</span><span class="sxs-lookup"><span data-stu-id="1714e-148">[out] A pointer to the pointer to the message store logon object for MAPI to log on to.</span></span>
    
 <span data-ttu-id="1714e-149">_lppMDB_</span><span class="sxs-lookup"><span data-stu-id="1714e-149">_lppMDB_</span></span>
  
> <span data-ttu-id="1714e-150">[out] Um ponteiro para o ponteiro para a mensagem armazenar o objeto para o spooler MAPI e os aplicativos de cliente para fazer logon.</span><span class="sxs-lookup"><span data-stu-id="1714e-150">[out] A pointer to the pointer to the message store object for the MAPI spooler and client applications to log on to.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1714e-151">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="1714e-151">Return value</span></span>

<span data-ttu-id="1714e-152">S_OK</span><span class="sxs-lookup"><span data-stu-id="1714e-152">S_OK</span></span> 
  
> <span data-ttu-id="1714e-153">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="1714e-153">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="1714e-154">MAPI_E_UNCONFIGURED</span><span class="sxs-lookup"><span data-stu-id="1714e-154">MAPI_E_UNCONFIGURED</span></span> 
  
> <span data-ttu-id="1714e-155">O perfil não conter informações suficientes para que o logon concluir.</span><span class="sxs-lookup"><span data-stu-id="1714e-155">The profile does not contain enough information for the logon to complete.</span></span> <span data-ttu-id="1714e-156">Quando este valor é retornado, MAPI chama a função de ponto entrada do serviço de mensagem do provedor de repositório a mensagem.</span><span class="sxs-lookup"><span data-stu-id="1714e-156">When this value is returned, MAPI calls the message store provider's message service entry point function.</span></span>
    
<span data-ttu-id="1714e-157">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="1714e-157">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="1714e-158">A chamada foi bem-sucedida, mas o provedor de armazenamento de mensagem tem informações de erro disponíveis.</span><span class="sxs-lookup"><span data-stu-id="1714e-158">The call succeeded, but the message store provider has error information available.</span></span> <span data-ttu-id="1714e-159">Quando esse aviso é retornado, a chamada deve ser manipulada com êxito.</span><span class="sxs-lookup"><span data-stu-id="1714e-159">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="1714e-160">Para testar esse aviso, use a macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="1714e-160">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="1714e-161">Para obter mais informações, consulte [Usando Macros para tratamento de erros](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="1714e-161">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span> <span data-ttu-id="1714e-162">Para obter as informações de erro do provedor, chame o método [IMAPISession::GetLastError](imapisession-getlasterror.md) .</span><span class="sxs-lookup"><span data-stu-id="1714e-162">To get the error information from the provider, call the [IMAPISession::GetLastError](imapisession-getlasterror.md) method.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="1714e-163">Comentários</span><span class="sxs-lookup"><span data-stu-id="1714e-163">Remarks</span></span>

<span data-ttu-id="1714e-164">O MAPI spooler chama o método de **IMSProvider::SpoolerLogon** para fazer logon um armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="1714e-164">The MAPI spooler calls the **IMSProvider::SpoolerLogon** method to log on to a message store.</span></span> <span data-ttu-id="1714e-165">O MAPI spooler deve usar o objeto de repositório de mensagem retornado pelo provedor de repositório de mensagem no parâmetro _lppMDB_ durante e após o logon.</span><span class="sxs-lookup"><span data-stu-id="1714e-165">The MAPI spooler should use the message store object returned by the message store provider in the  _lppMDB_ parameter during and after logon.</span></span> 
  
<span data-ttu-id="1714e-166">Para obter consistência com o método [IMSProvider::Logon](imsprovider-logon.md) , o provedor também retorna um objeto de logon do repositório de mensagem no parâmetro _lppMSLogon_ .</span><span class="sxs-lookup"><span data-stu-id="1714e-166">For consistency with the [IMSProvider::Logon](imsprovider-logon.md) method, the provider also returns a message store logon object in the  _lppMSLogon_ parameter.</span></span> <span data-ttu-id="1714e-167">O uso do objeto store e o objeto de logon são idênticas para logon repositório usual; deve haver uma correspondência direta entre o objeto de logon e o objeto de armazenamento, de forma que os objetos agir como se fossem um objeto que expõe duas interfaces.</span><span class="sxs-lookup"><span data-stu-id="1714e-167">The use of the store object and the logon object are identical for usual store logon; there should be a one-to-one correspondence between the logon object and the store object such that the objects act as if they are one object that exposes two interfaces.</span></span> <span data-ttu-id="1714e-168">Os dois objetos são criados juntos e liberação juntos.</span><span class="sxs-lookup"><span data-stu-id="1714e-168">The two objects are created together and freed together.</span></span> 
  
<span data-ttu-id="1714e-169">O provedor de armazenamento internamente marcará o objeto de repositório de mensagem retornada para indicar que o repositório está sendo usado pelo spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="1714e-169">The store provider should internally mark the returned message store object to indicate that the store is being used by the MAPI spooler.</span></span> <span data-ttu-id="1714e-170">Alguns métodos para este objeto de repositório de forma diferente da mensagem armazenar objeto fornecido aos aplicativos cliente se comportam.</span><span class="sxs-lookup"><span data-stu-id="1714e-170">Some of the methods for this store object behave differently than for the message store object provided to client applications.</span></span> <span data-ttu-id="1714e-171">Manter este marca interna é a maneira mais comum de disparo o comportamento específico para o spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="1714e-171">Keeping this internal mark is the most common way of triggering the behavior specific to the MAPI spooler.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1714e-172">Confira também</span><span class="sxs-lookup"><span data-stu-id="1714e-172">See also</span></span>



[<span data-ttu-id="1714e-173">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="1714e-173">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="1714e-174">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="1714e-174">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="1714e-175">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1714e-175">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)

