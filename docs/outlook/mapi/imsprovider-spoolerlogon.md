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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 794674df38266743cac8c947ec93dc1fcfff438b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430571"
---
# <a name="imsproviderspoolerlogon"></a><span data-ttu-id="98d9f-103">IMSProvider::SpoolerLogon</span><span class="sxs-lookup"><span data-stu-id="98d9f-103">IMSProvider::SpoolerLogon</span></span>

  
  
<span data-ttu-id="98d9f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="98d9f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="98d9f-105">Registra o spooler MAPI em um armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="98d9f-105">Logs the MAPI spooler on to a message store.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="98d9f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="98d9f-106">Parameters</span></span>

 <span data-ttu-id="98d9f-107">_lpMAPISup_</span><span class="sxs-lookup"><span data-stu-id="98d9f-107">_lpMAPISup_</span></span>
  
> <span data-ttu-id="98d9f-108">[in] Um ponteiro para o objeto de suporte MAPI para o armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="98d9f-108">[in] A pointer to the MAPI support object for the message store.</span></span>
    
 <span data-ttu-id="98d9f-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="98d9f-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="98d9f-110">[in] Um alça para a janela pai de quaisquer caixas de diálogo ou janelas que esse método exibe.</span><span class="sxs-lookup"><span data-stu-id="98d9f-110">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> 
    
 <span data-ttu-id="98d9f-111">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="98d9f-111">_lpszProfileName_</span></span>
  
> <span data-ttu-id="98d9f-112">[in] Um ponteiro para uma cadeia de caracteres que contém o nome do perfil que está sendo usado para o logon do spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="98d9f-112">[in] A pointer to a string that contains the name of the profile being used for the MAPI spooler logon.</span></span> <span data-ttu-id="98d9f-113">Essa cadeia de caracteres pode ser exibida em caixas de diálogo, escritas em um arquivo de log ou simplesmente ignoradas.</span><span class="sxs-lookup"><span data-stu-id="98d9f-113">This string can be displayed in dialog boxes, written out to a log file, or simply ignored.</span></span> <span data-ttu-id="98d9f-114">Ele deverá estar no formato Unicode se o sinalizador MAPI_UNICODE estiver definido no _parâmetro ulFlags._</span><span class="sxs-lookup"><span data-stu-id="98d9f-114">It must be in Unicode format if the MAPI_UNICODE flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="98d9f-115">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="98d9f-115">_cbEntryID_</span></span>
  
> <span data-ttu-id="98d9f-116">[in] O tamanho, em bytes, do identificador de entrada apontado pelo parâmetro _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="98d9f-116">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="98d9f-117">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="98d9f-117">_lpEntryID_</span></span>
  
> <span data-ttu-id="98d9f-118">[in] Um ponteiro para o identificador de entrada para o armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="98d9f-118">[in] A pointer to the entry identifier for the message store.</span></span> <span data-ttu-id="98d9f-119">Passar NULL no parâmetro  _lpEntryID_ indica que um armazenamento de mensagens ainda não foi selecionado e que caixas de diálogo que permitem ao usuário selecionar um armazenamento de mensagens podem ser apresentadas.</span><span class="sxs-lookup"><span data-stu-id="98d9f-119">Passing NULL in the  _lpEntryID_ parameter indicates that a message store has not yet been selected and that dialog boxes that enable the user to select a message store can be presented.</span></span> 
    
 <span data-ttu-id="98d9f-120">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="98d9f-120">_ulFlags_</span></span>
  
> <span data-ttu-id="98d9f-121">[in] Uma máscara de bits de sinalizadores que controla como o logon é realizado.</span><span class="sxs-lookup"><span data-stu-id="98d9f-121">[in] A bitmask of flags that controls how the logon is performed.</span></span> <span data-ttu-id="98d9f-122">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="98d9f-122">The following flags can be set:</span></span>
    
<span data-ttu-id="98d9f-123">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="98d9f-123">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="98d9f-124">A chamada tem permissão para ser bem-sucedida, mesmo se o objeto subjacente não estiver disponível para a implementação da chamada.</span><span class="sxs-lookup"><span data-stu-id="98d9f-124">The call is allowed to succeed even if the underlying object is not available to the calling implementation.</span></span> <span data-ttu-id="98d9f-125">Se o objeto não estiver disponível, uma chamada subsequente para o objeto poderá criar um erro.</span><span class="sxs-lookup"><span data-stu-id="98d9f-125">If the object is not available, a subsequent call to the object might raise an error.</span></span>
    
<span data-ttu-id="98d9f-126">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="98d9f-126">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="98d9f-127">As cadeias de caracteres passadas estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="98d9f-127">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="98d9f-128">Se MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="98d9f-128">If MAPI_UNICODE is not set, the strings are in ANSI format.</span></span>
    
<span data-ttu-id="98d9f-129">MDB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="98d9f-129">MDB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="98d9f-130">Impede a exibição de caixas de diálogo de logon.</span><span class="sxs-lookup"><span data-stu-id="98d9f-130">Prevents the display of logon dialog boxes.</span></span> <span data-ttu-id="98d9f-131">Se esse sinalizador estiver definido, o valor de erro MAPI_E_LOGON_FAILED será retornado se o logon não for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="98d9f-131">If this flag is set, the error value MAPI_E_LOGON_FAILED is returned if the logon is unsuccessful.</span></span> <span data-ttu-id="98d9f-132">Se esse sinalizador não estiver definido, o provedor do armazenamento de mensagens poderá solicitar que o usuário corrija um nome ou senha, insira um disco ou execute outras ações necessárias para estabelecer conexão com o armazenamento.</span><span class="sxs-lookup"><span data-stu-id="98d9f-132">If this flag is not set, the message store provider can prompt the user to correct a name or password, to insert a disk, or to perform other actions necessary to establish connection to the store.</span></span>
    
<span data-ttu-id="98d9f-133">MDB_WRITE</span><span class="sxs-lookup"><span data-stu-id="98d9f-133">MDB_WRITE</span></span> 
  
> <span data-ttu-id="98d9f-134">Solicita permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="98d9f-134">Requests read/write permission.</span></span>
    
 <span data-ttu-id="98d9f-135">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="98d9f-135">_lpInterface_</span></span>
  
> <span data-ttu-id="98d9f-136">[in] Um ponteiro para o IID (identificador da interface) para o armazenamento de mensagens fazer logon.</span><span class="sxs-lookup"><span data-stu-id="98d9f-136">[in] A pointer to the interface identifier (IID) for the message store to log on to.</span></span> <span data-ttu-id="98d9f-137">Passar NULL indica que a interface MAPI do repositório de mensagens ([IMsgStore](imsgstoreimapiprop.md)) é retornada.</span><span class="sxs-lookup"><span data-stu-id="98d9f-137">Passing NULL indicates the MAPI interface for the message store ([IMsgStore](imsgstoreimapiprop.md)) is returned.</span></span> <span data-ttu-id="98d9f-138">O  _parâmetro lpInterface_ também pode ser definido como um identificador para uma interface apropriada para o armazenamento de mensagens (por exemplo, IID_IUnknown ou IID_IMAPIProp).</span><span class="sxs-lookup"><span data-stu-id="98d9f-138">The  _lpInterface_ parameter can also be set to an identifier for an appropriate interface for the message store (for example IID_IUnknown or IID_IMAPIProp).</span></span> 
    
 <span data-ttu-id="98d9f-139">_cbSpoolSecurity_</span><span class="sxs-lookup"><span data-stu-id="98d9f-139">_cbSpoolSecurity_</span></span>
  
> <span data-ttu-id="98d9f-140">[in] Um ponteiro para o tamanho, em bytes, dos dados de validação no _parâmetro lppbSpoolSecurity._</span><span class="sxs-lookup"><span data-stu-id="98d9f-140">[in] A pointer to the size, in bytes, of validation data in the  _lppbSpoolSecurity_ parameter.</span></span> 
    
 <span data-ttu-id="98d9f-141">_lpbSpoolSecurity_</span><span class="sxs-lookup"><span data-stu-id="98d9f-141">_lpbSpoolSecurity_</span></span>
  
> <span data-ttu-id="98d9f-142">[in] Um ponteiro para um ponteiro para dados de validação.</span><span class="sxs-lookup"><span data-stu-id="98d9f-142">[in] A pointer to a pointer to validation data.</span></span> <span data-ttu-id="98d9f-143">O **método SpoolerLogon** usa esses dados para fazer logon do spooler MAPI no mesmo armazenamento que o provedor de armazenamento de mensagens conectado anteriormente usando o método [IMSProvider::Logon.](imsprovider-logon.md)</span><span class="sxs-lookup"><span data-stu-id="98d9f-143">The **SpoolerLogon** method uses this data to log the MAPI spooler on to the same store as the message store provider previously logged on to by using the [IMSProvider::Logon](imsprovider-logon.md) method.</span></span> 
    
 <span data-ttu-id="98d9f-144">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="98d9f-144">_lppMAPIError_</span></span>
  
> <span data-ttu-id="98d9f-145">[out] Um ponteiro para um ponteiro para a estrutura [MAPIERROR](mapierror.md) retornada, se alguma, que contenha informações de versão, componente e contexto para um erro.</span><span class="sxs-lookup"><span data-stu-id="98d9f-145">[out] A pointer to a pointer to the returned [MAPIERROR](mapierror.md) structure, if any, that contains version, component, and context information for an error.</span></span> <span data-ttu-id="98d9f-146">O  _parâmetro lppMAPIError_ pode ser definido como NULL se não houver **estrutura MAPIERROR** a ser retornada.</span><span class="sxs-lookup"><span data-stu-id="98d9f-146">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
 <span data-ttu-id="98d9f-147">_lppMSLogon_</span><span class="sxs-lookup"><span data-stu-id="98d9f-147">_lppMSLogon_</span></span>
  
> <span data-ttu-id="98d9f-148">[out] Um ponteiro para o ponteiro para o objeto de logon do armazenamento de mensagens para MAPI fazer logon.</span><span class="sxs-lookup"><span data-stu-id="98d9f-148">[out] A pointer to the pointer to the message store logon object for MAPI to log on to.</span></span>
    
 <span data-ttu-id="98d9f-149">_lppMDB_</span><span class="sxs-lookup"><span data-stu-id="98d9f-149">_lppMDB_</span></span>
  
> <span data-ttu-id="98d9f-150">[out] Um ponteiro para o ponteiro para o objeto de armazenamento de mensagens para o spooler MAPI e aplicativos cliente para fazer logoff.</span><span class="sxs-lookup"><span data-stu-id="98d9f-150">[out] A pointer to the pointer to the message store object for the MAPI spooler and client applications to log on to.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="98d9f-151">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="98d9f-151">Return value</span></span>

<span data-ttu-id="98d9f-152">S_OK</span><span class="sxs-lookup"><span data-stu-id="98d9f-152">S_OK</span></span> 
  
> <span data-ttu-id="98d9f-153">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="98d9f-153">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="98d9f-154">MAPI_E_UNCONFIGURED</span><span class="sxs-lookup"><span data-stu-id="98d9f-154">MAPI_E_UNCONFIGURED</span></span> 
  
> <span data-ttu-id="98d9f-155">O perfil não contém informações suficientes para que o logon seja concluído.</span><span class="sxs-lookup"><span data-stu-id="98d9f-155">The profile does not contain enough information for the logon to complete.</span></span> <span data-ttu-id="98d9f-156">Quando esse valor é retornado, o MAPI chama a função de ponto de entrada do serviço de mensagens do provedor de armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="98d9f-156">When this value is returned, MAPI calls the message store provider's message service entry point function.</span></span>
    
<span data-ttu-id="98d9f-157">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="98d9f-157">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="98d9f-158">A chamada foi bem-sucedida, mas o provedor do armazenamento de mensagens tem informações de erro disponíveis.</span><span class="sxs-lookup"><span data-stu-id="98d9f-158">The call succeeded, but the message store provider has error information available.</span></span> <span data-ttu-id="98d9f-159">Quando esse aviso é retornado, a chamada deve ser tratada como bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="98d9f-159">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="98d9f-160">Para testar esse aviso, use a **HR_FAILED** macro.</span><span class="sxs-lookup"><span data-stu-id="98d9f-160">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="98d9f-161">Para obter mais informações, consulte [Usando macros para tratamento de erros.](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="98d9f-161">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span> <span data-ttu-id="98d9f-162">Para obter as informações de erro do provedor, chame o [método IMAPISession::GetLastError.](imapisession-getlasterror.md)</span><span class="sxs-lookup"><span data-stu-id="98d9f-162">To get the error information from the provider, call the [IMAPISession::GetLastError](imapisession-getlasterror.md) method.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="98d9f-163">Comentários</span><span class="sxs-lookup"><span data-stu-id="98d9f-163">Remarks</span></span>

<span data-ttu-id="98d9f-164">O spooler MAPI chama o **método IMSProvider::SpoolerLogon** para fazer logoff em um armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="98d9f-164">The MAPI spooler calls the **IMSProvider::SpoolerLogon** method to log on to a message store.</span></span> <span data-ttu-id="98d9f-165">O spooler MAPI deve usar o objeto de armazenamento de mensagens retornado pelo provedor de armazenamento de mensagens no parâmetro  _lppMDB_ durante e após o logon.</span><span class="sxs-lookup"><span data-stu-id="98d9f-165">The MAPI spooler should use the message store object returned by the message store provider in the  _lppMDB_ parameter during and after logon.</span></span> 
  
<span data-ttu-id="98d9f-166">Para consistência com o [método IMSProvider::Logon,](imsprovider-logon.md) o provedor também retorna um objeto de logon do armazenamento de mensagens no parâmetro _lppMSLogon._</span><span class="sxs-lookup"><span data-stu-id="98d9f-166">For consistency with the [IMSProvider::Logon](imsprovider-logon.md) method, the provider also returns a message store logon object in the  _lppMSLogon_ parameter.</span></span> <span data-ttu-id="98d9f-167">O uso do objeto de armazenamento e do objeto de logon são idênticos para logon de armazenamento normal; deve haver uma correspondência um-para-um entre o objeto de logon e o objeto de armazenamento de forma que os objetos agem como se fosse um objeto que expõe duas interfaces.</span><span class="sxs-lookup"><span data-stu-id="98d9f-167">The use of the store object and the logon object are identical for usual store logon; there should be a one-to-one correspondence between the logon object and the store object such that the objects act as if they are one object that exposes two interfaces.</span></span> <span data-ttu-id="98d9f-168">Os dois objetos são criados juntos e liberados juntos.</span><span class="sxs-lookup"><span data-stu-id="98d9f-168">The two objects are created together and freed together.</span></span> 
  
<span data-ttu-id="98d9f-169">O provedor de armazenamento deve marcar internamente o objeto de armazenamento de mensagens retornado para indicar que o armazenamento está sendo usado pelo spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="98d9f-169">The store provider should internally mark the returned message store object to indicate that the store is being used by the MAPI spooler.</span></span> <span data-ttu-id="98d9f-170">Alguns dos métodos para esse objeto de armazenamento se comportam de maneira diferente do objeto de armazenamento de mensagens fornecido aos aplicativos cliente.</span><span class="sxs-lookup"><span data-stu-id="98d9f-170">Some of the methods for this store object behave differently than for the message store object provided to client applications.</span></span> <span data-ttu-id="98d9f-171">Manter essa marca interna é a maneira mais comum de disparar o comportamento específico para o spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="98d9f-171">Keeping this internal mark is the most common way of triggering the behavior specific to the MAPI spooler.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="98d9f-172">Confira também</span><span class="sxs-lookup"><span data-stu-id="98d9f-172">See also</span></span>



[<span data-ttu-id="98d9f-173">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="98d9f-173">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="98d9f-174">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="98d9f-174">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="98d9f-175">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="98d9f-175">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)

