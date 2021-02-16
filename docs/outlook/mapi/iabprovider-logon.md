---
title: IABProviderLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABProvider.Logon
api_type:
- COM
ms.assetid: f9468715-1674-4d14-81c8-2f24dbaa0453
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 59c6d4a05c91511ad8c481fd4ddbe42396442190
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348780"
---
# <a name="iabproviderlogon"></a><span data-ttu-id="422af-103">IABProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="422af-103">IABProvider::Logon</span></span>

  
  
<span data-ttu-id="422af-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="422af-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="422af-105">Estabelece uma conexão com uma sessão ativa.</span><span class="sxs-lookup"><span data-stu-id="422af-105">Establishes a connection to an active session.</span></span>
  
```cpp
HRESULT Logon(
  LPMAPISUP lpMAPISup,
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  ULONG ulFlags,
  ULONG FAR * lpulcbSecurity,
  LPBYTE FAR * lppbSecurity,
  LPMAPIERROR FAR * lppMAPIError,
  LPABLOGON FAR * lppABLogon
);
```

## <a name="parameters"></a><span data-ttu-id="422af-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="422af-106">Parameters</span></span>

 <span data-ttu-id="422af-107">_lpMAPISup_</span><span class="sxs-lookup"><span data-stu-id="422af-107">_lpMAPISup_</span></span>
  
> <span data-ttu-id="422af-108">[in] Um ponteiro para o objeto de suporte do provedor de agendas de endereços.</span><span class="sxs-lookup"><span data-stu-id="422af-108">[in] A pointer to the address book provider's support object.</span></span>
    
 <span data-ttu-id="422af-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="422af-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="422af-110">[in] Um alça para a janela pai da caixa de diálogo de logon que o método **logon** exibe, se permitido.</span><span class="sxs-lookup"><span data-stu-id="422af-110">[in] A handle to the parent window for the logon dialog box that the **Logon** method displays, if permitted.</span></span> <span data-ttu-id="422af-111">O _parâmetro ulUIParam_ contém o valor do parâmetro do mesmo nome passado para MAPI na chamada anterior para a [função MAPILogonEx.](mapilogonex.md)</span><span class="sxs-lookup"><span data-stu-id="422af-111">The  _ulUIParam_ parameter contains the value of the parameter of the same name passed to MAPI in the previous call to the [MAPILogonEx](mapilogonex.md) function.</span></span> 
    
 <span data-ttu-id="422af-112">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="422af-112">_lpszProfileName_</span></span>
  
> <span data-ttu-id="422af-113">[in] Um ponteiro para o nome do perfil da sessão.</span><span class="sxs-lookup"><span data-stu-id="422af-113">[in] A pointer to the name of the session profile.</span></span>
    
 <span data-ttu-id="422af-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="422af-114">_ulFlags_</span></span>
  
> <span data-ttu-id="422af-115">[in] Uma máscara de bits de sinalizadores que controla como o logon é realizado.</span><span class="sxs-lookup"><span data-stu-id="422af-115">[in] A bitmask of flags that controls how the logon is performed.</span></span> <span data-ttu-id="422af-116">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="422af-116">The following flags can be set:</span></span>
    
<span data-ttu-id="422af-117">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="422af-117">AB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="422af-118">O provedor não deve exibir uma caixa de diálogo durante o logon.</span><span class="sxs-lookup"><span data-stu-id="422af-118">The provider should not display a dialog box during logon.</span></span> <span data-ttu-id="422af-119">Se esse sinalizador não estiver definido, o provedor poderá exibir uma caixa de diálogo para solicitar ao usuário informações de configuração ausentes.</span><span class="sxs-lookup"><span data-stu-id="422af-119">If this flag is not set, the provider can display a dialog box to prompt the user for missing configuration information.</span></span>
    
<span data-ttu-id="422af-120">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="422af-120">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="422af-121">Permite que **o logon** retorne com êxito, possivelmente antes da finalização do processo de logon.</span><span class="sxs-lookup"><span data-stu-id="422af-121">Enables **Logon** to return successfully, possibly before the logon process is finished.</span></span> 
    
<span data-ttu-id="422af-122">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="422af-122">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="422af-123">Todas as cadeias de caracteres devem estar no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="422af-123">All strings should be in Unicode format.</span></span> <span data-ttu-id="422af-124">Se o MAPI_UNICODE sinalizador não estiver definido, as cadeias de caracteres deverão estar no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="422af-124">If the MAPI_UNICODE flag is not set, the strings should be in ANSI format.</span></span>
    
 <span data-ttu-id="422af-125">_lpulcbSecurity_</span><span class="sxs-lookup"><span data-stu-id="422af-125">_lpulcbSecurity_</span></span>
  
> <span data-ttu-id="422af-126">[in, out] Um ponteiro para o tamanho, em bytes, da estrutura de credenciais de segurança apontada pelo _parâmetro lppbSecurity._</span><span class="sxs-lookup"><span data-stu-id="422af-126">[in, out] A pointer to the size, in bytes, of the security credentials structure pointed to by the  _lppbSecurity_ parameter.</span></span> <span data-ttu-id="422af-127">Na entrada, o valor deve ser não zero; na saída, o valor deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="422af-127">On input, the value must be nonzero; on output, the value must be zero.</span></span> <span data-ttu-id="422af-128">Em ambos os casos, os ponteiros devem ser válidos.</span><span class="sxs-lookup"><span data-stu-id="422af-128">In both cases, the pointers must be valid.</span></span> 
    
 <span data-ttu-id="422af-129">_lppbSecurity_</span><span class="sxs-lookup"><span data-stu-id="422af-129">_lppbSecurity_</span></span>
  
> <span data-ttu-id="422af-130">[in, out] Um ponteiro para um ponteiro para credenciais de segurança.</span><span class="sxs-lookup"><span data-stu-id="422af-130">[in, out] A pointer to a pointer to security credentials.</span></span> <span data-ttu-id="422af-131">Na entrada, o valor deve ser não zero; na saída, o valor deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="422af-131">On input, the value must be nonzero; on output, the value must be zero.</span></span> <span data-ttu-id="422af-132">Em ambos os casos, o ponteiro deve ser válido.</span><span class="sxs-lookup"><span data-stu-id="422af-132">In both cases the pointer must be valid.</span></span>
    
 <span data-ttu-id="422af-133">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="422af-133">_lppMAPIError_</span></span>
  
> <span data-ttu-id="422af-134">[out] Um ponteiro para um ponteiro para uma [estrutura MAPIERROR.](mapierror.md)</span><span class="sxs-lookup"><span data-stu-id="422af-134">[out] A pointer to a pointer to a [MAPIERROR](mapierror.md) structure.</span></span> <span data-ttu-id="422af-135">O  _parâmetro lppMAPIError_ pode ser definido como NULL se não houver **estrutura MAPIERROR** a ser retornada.</span><span class="sxs-lookup"><span data-stu-id="422af-135">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
 <span data-ttu-id="422af-136">_lppABLogon_</span><span class="sxs-lookup"><span data-stu-id="422af-136">_lppABLogon_</span></span>
  
> <span data-ttu-id="422af-137">[out] Um ponteiro para um ponteiro para o objeto de logon do provedor.</span><span class="sxs-lookup"><span data-stu-id="422af-137">[out] A pointer to a pointer to the provider's logon object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="422af-138">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="422af-138">Return value</span></span>

<span data-ttu-id="422af-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="422af-139">S_OK</span></span> 
  
> <span data-ttu-id="422af-140">Uma conexão com uma sessão ativa foi estabelecida com êxito.</span><span class="sxs-lookup"><span data-stu-id="422af-140">A connection to an active session was successfully established.</span></span>
    
<span data-ttu-id="422af-141">MAPI_E_FAILONEPROVIDER</span><span class="sxs-lookup"><span data-stu-id="422af-141">MAPI_E_FAILONEPROVIDER</span></span> 
  
> <span data-ttu-id="422af-142">O provedor não pode fazer logoff, mas o MAPI pode continuar a fazer logoff nos outros provedores no serviço de mensagens ao qual o provedor pertence.</span><span class="sxs-lookup"><span data-stu-id="422af-142">The provider cannot log on, but MAPI can continue to log on the other providers in the message service to which the provider belongs.</span></span> 
    
<span data-ttu-id="422af-143">MAPI_E_UNCONFIGURED</span><span class="sxs-lookup"><span data-stu-id="422af-143">MAPI_E_UNCONFIGURED</span></span> 
  
> <span data-ttu-id="422af-144">O provedor tem informações insuficientes para concluir o logon.</span><span class="sxs-lookup"><span data-stu-id="422af-144">The provider has insufficient information to complete the logon.</span></span> <span data-ttu-id="422af-145">MAPI calls the provider's message service entry function.</span><span class="sxs-lookup"><span data-stu-id="422af-145">MAPI calls the provider's message service entry function.</span></span>
    
<span data-ttu-id="422af-146">MAPI_E_UNKNOWN_CPID</span><span class="sxs-lookup"><span data-stu-id="422af-146">MAPI_E_UNKNOWN_CPID</span></span> 
  
> <span data-ttu-id="422af-147">O servidor não está configurado para dar suporte à página de código do cliente.</span><span class="sxs-lookup"><span data-stu-id="422af-147">The server is not configured to support the client's code page.</span></span>
    
<span data-ttu-id="422af-148">MAPI_E_UNKNOWN_LCID</span><span class="sxs-lookup"><span data-stu-id="422af-148">MAPI_E_UNKNOWN_LCID</span></span> 
  
> <span data-ttu-id="422af-149">O servidor não está configurado para dar suporte às informações de localidade do cliente.</span><span class="sxs-lookup"><span data-stu-id="422af-149">The server is not configured to support the client's locale information.</span></span>
    
<span data-ttu-id="422af-150">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="422af-150">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="422af-151">O usuário cancelou a operação, normalmente clicando no botão **Cancelar** na caixa de diálogo de logon.</span><span class="sxs-lookup"><span data-stu-id="422af-151">The user canceled the operation, typically by clicking the **Cancel** button in the logon dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="422af-152">Comentários</span><span class="sxs-lookup"><span data-stu-id="422af-152">Remarks</span></span>

<span data-ttu-id="422af-153">As conexões são estabelecidas com cada provedor de agendas no perfil de sessão quando um cliente chama o método [IMAPISession::OpenAddressBook.](imapisession-openaddressbook.md)</span><span class="sxs-lookup"><span data-stu-id="422af-153">Connections are established with each address book provider in the session profile when a client calls the [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) method.</span></span> <span data-ttu-id="422af-154">**OpenAddressBook** chama o método de **Logon** de cada provedor.</span><span class="sxs-lookup"><span data-stu-id="422af-154">**OpenAddressBook** then calls each provider's **Logon** method.</span></span> 
  
<span data-ttu-id="422af-155">O nome de perfil apontado pelo parâmetro _lpszProfileName_ é exibido no conjunto de caracteres do cliente do usuário, conforme indicado pela presença ou ausência do sinalizador MAPI_UNICODE no parâmetro _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="422af-155">The profile name pointed to by the  _lpszProfileName_ parameter is displayed in the character set of the user's client as indicated by the presence or absence of the MAPI_UNICODE flag in the  _ulFlags_ parameter.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="422af-156">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="422af-156">Notes to implementers</span></span>

<span data-ttu-id="422af-157">Na implementação do método **Logon,** chame o método [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) para registrar um identificador exclusivo ou estrutura [MAPIUID.](mapiuid.md)</span><span class="sxs-lookup"><span data-stu-id="422af-157">In your implementation of the **Logon** method, call the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method to register a unique identifier, or [MAPIUID](mapiuid.md) structure.</span></span> <span data-ttu-id="422af-158">Cada um dos seus objetos terá um identificador de entrada que inclui este **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="422af-158">Each of your objects will have an entry identifier that includes this **MAPIUID**.</span></span> <span data-ttu-id="422af-159">MAPI uses the **MAPIUID** to match an object with its provider.</span><span class="sxs-lookup"><span data-stu-id="422af-159">MAPI uses the **MAPIUID** to match an object with its provider.</span></span> <span data-ttu-id="422af-160">Por exemplo, quando um cliente chama o método [IMAPISession::OpenEntry](imapisession-openentry.md) para abrir um usuário de mensagens, **OpenEntry** examina a parte **MAPIUID** do identificador de entrada que foi passado e corresponde a ela com um **MAPIUID** registrado por um provedor de agendamento de endereços.</span><span class="sxs-lookup"><span data-stu-id="422af-160">For example, when a client calls the [IMAPISession::OpenEntry](imapisession-openentry.md) method to open a messaging user, **OpenEntry** examines the **MAPIUID** portion of the entry identifier that was passed in and matches it with a **MAPIUID** registered by an address book provider.</span></span> 
  
<span data-ttu-id="422af-161">Se um cliente faz logon no provedor mais de uma vez, talvez você queira registrar um **MAPIUID** diferente para cada logon.</span><span class="sxs-lookup"><span data-stu-id="422af-161">If a client logs on to your provider more than once, you may want to register a different **MAPIUID** for each logon.</span></span> <span data-ttu-id="422af-162">O registro de estruturas **MAPIUID** exclusivas permite que o MAPI roteie corretamente as solicitações para a instância de provedor apropriada.</span><span class="sxs-lookup"><span data-stu-id="422af-162">Registering unique **MAPIUID** structures enables MAPI to correctly route requests to the appropriate provider instance.</span></span> <span data-ttu-id="422af-163">No entanto, talvez você queira que cada objeto de logon compartilhe um **MAPIUID.**</span><span class="sxs-lookup"><span data-stu-id="422af-163">However, you may want to have every logon object share one **MAPIUID**.</span></span> <span data-ttu-id="422af-164">Nesse caso, você deve ser capaz de lidar com o roteamento por conta própria em vez de depender de MAPI.</span><span class="sxs-lookup"><span data-stu-id="422af-164">In this case, you must be able to handle the routing yourself instead of relying on MAPI.</span></span> <span data-ttu-id="422af-165">Para obter mais informações sobre como criar um **MAPIUID,** consulte [Registrando identificadores](registering-service-provider-unique-identifiers.md)exclusivos do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="422af-165">For more information about how to create a **MAPIUID**, see [Registering Service Provider Unique Identifiers](registering-service-provider-unique-identifiers.md).</span></span>
  
<span data-ttu-id="422af-166">O objeto de suporte que MAPI passa para o método **Logon** no parâmetro _lpMAPISup_ fornece acesso a muitos dos métodos incluídos na interface [IMAPISupport : IUnknown.](imapisupportiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="422af-166">The support object that MAPI passes to your **Logon** method in the  _lpMAPISup_ parameter provides access to many of the methods included in the [IMAPISupport : IUnknown](imapisupportiunknown.md) interface.</span></span> <span data-ttu-id="422af-167">MAPI creates a support object that is customized to your type of provider.</span><span class="sxs-lookup"><span data-stu-id="422af-167">MAPI creates a support object that is customized to your type of provider.</span></span> <span data-ttu-id="422af-168">Por exemplo, se você precisar fazer logon em um sistema de mensagens ou serviço de diretório subjacente ao estabelecer sua conexão, poderá chamar o método [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) para recuperar credenciais de segurança para esta sessão de logon específica.</span><span class="sxs-lookup"><span data-stu-id="422af-168">For example, if you need to log on to an underlying messaging system or directory service when you establish your connection, you can call the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to retrieve security credentials for this particular logon session.</span></span> 
  
<span data-ttu-id="422af-169">Se **Logon** for bem-sucedido, chame o método [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) do objeto de suporte para incrementar sua contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="422af-169">If **Logon** is successful, be sure that you call the support object's [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) method to increment its reference count.</span></span> <span data-ttu-id="422af-170">Isso permite que seu provedor mantenha o ponteiro do objeto de suporte para o restante da sessão.</span><span class="sxs-lookup"><span data-stu-id="422af-170">This enables your provider to hold onto the support object pointer for the rest of the session.</span></span> <span data-ttu-id="422af-171">Se você não chamar esse **método AddRef,** o MAPI descarregará seu provedor.</span><span class="sxs-lookup"><span data-stu-id="422af-171">If you do not call this **AddRef** method, MAPI will unload your provider.</span></span> 
  
<span data-ttu-id="422af-172">Você pode incluir o nome do perfil passado no parâmetro  _lpszProfileName_ em caixas de diálogo de erro, telas de logon ou outras interfaces do usuário.</span><span class="sxs-lookup"><span data-stu-id="422af-172">You can include the profile name passed in the  _lpszProfileName_ parameter in error dialog boxes, logon screens, or other user interfaces.</span></span> <span data-ttu-id="422af-173">Para usar o nome do perfil, copie-o para o armazenamento que você alocou.</span><span class="sxs-lookup"><span data-stu-id="422af-173">To use the profile name, copy it to storage that you have allocated.</span></span> 
  
<span data-ttu-id="422af-174">Crie um objeto de logon e retorne um ponteiro para ele no _parâmetro lppABLogon._</span><span class="sxs-lookup"><span data-stu-id="422af-174">Create a logon object and return a pointer to it in the  _lppABLogon_ parameter.</span></span> <span data-ttu-id="422af-175">MAPI uses this logon object to make calls to the methods in your [IABLogon](iablogoniunknown.md) implementation.</span><span class="sxs-lookup"><span data-stu-id="422af-175">MAPI uses this logon object to make calls to the methods in your [IABLogon](iablogoniunknown.md) implementation.</span></span> 
  
<span data-ttu-id="422af-176">Se você precisar de uma senha durante o logon, exibirá uma caixa de diálogo de logon somente se o sinalizador AB_NO_DIALOG não estiver definido.</span><span class="sxs-lookup"><span data-stu-id="422af-176">If you require a password during logon, display a logon dialog box only if the AB_NO_DIALOG flag is not set.</span></span> <span data-ttu-id="422af-177">Se o usuário cancelar o processo de **logon,** normalmente clicando no botão Cancelar na caixa de diálogo, retorne MAPI_E_USER_CANCEL logon . </span><span class="sxs-lookup"><span data-stu-id="422af-177">If the user cancels the logon process, typically by clicking the **Cancel** button in the dialog box, return MAPI_E_USER_CANCEL from **Logon**.</span></span>
  
<span data-ttu-id="422af-178">Normalmente, quando um provedor de agendas não consegue fazer logon, o MAPI desabilita o serviço de mensagens ao qual pertence o provedor com falha— ou seja, o MAPI não tentará estabelecer conexões para nenhum dos outros provedores que pertencem ao serviço pelo resto do tempo de vida da sessão.</span><span class="sxs-lookup"><span data-stu-id="422af-178">Typically, when an address book provider cannot log on, MAPI disables the message service to which the failing provider belongs—that is, MAPI will not try to establish connections for any of the other providers that belong to the service for the rest of the session's lifetime.</span></span> <span data-ttu-id="422af-179">No entanto, se o provedor não puder estabelecer uma conexão e você quiser não desabilitar todo o serviço, retorne MAPI_E_FAILONEPROVIDER ou MAPI_E_UNCONFIGURED.</span><span class="sxs-lookup"><span data-stu-id="422af-179">However, if your provider cannot establish a connection and you want not to disable the entire service, return either MAPI_E_FAILONEPROVIDER or MAPI_E_UNCONFIGURED.</span></span> <span data-ttu-id="422af-180">O MAPI não desabilitará o serviço de mensagens ao qual o provedor pertence.</span><span class="sxs-lookup"><span data-stu-id="422af-180">MAPI will not disable the message service to which the provider belongs.</span></span> 
  
<span data-ttu-id="422af-181">Retorne MAPI_E_FAILONEPROVIDER se ocorrer um erro que não seja sério o suficiente para impedir que os outros provedores no serviço de mensagens estabeleem conexões.</span><span class="sxs-lookup"><span data-stu-id="422af-181">Return MAPI_E_FAILONEPROVIDER if an error occurs that is not serious enough to prevent the other providers in the message service from establishing connections.</span></span> <span data-ttu-id="422af-182">Retorne MAPI_E_UNCONFIGURED se as informações de configuração necessárias não puderem ser exibidas no perfil e você não puder exibir uma caixa de diálogo para solicitar ao usuário.</span><span class="sxs-lookup"><span data-stu-id="422af-182">Return MAPI_E_UNCONFIGURED if the necessary configuration information is missing from the profile and you cannot display a dialog box to prompt the user.</span></span> <span data-ttu-id="422af-183">O MAPI responderá chamando a função de ponto de entrada do serviço de mensagens do provedor com o MSG_SERVICE_CONFIGURE definido como o parâmetro  _ulContext_ para dar ao serviço a chance de se configurar, programaticamente ou usando uma folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="422af-183">MAPI will respond by calling your provider's message service entry point function with MSG_SERVICE_CONFIGURE set as the  _ulContext_ parameter to give the service a chance to configure itself, either programmatically or using a property sheet.</span></span> <span data-ttu-id="422af-184">Quando a função de ponto de entrada do serviço de mensagens tiver sido concluída, o MAPI recuperará o logon.</span><span class="sxs-lookup"><span data-stu-id="422af-184">When the message service entry point function has finished, MAPI retries the logon.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="422af-185">Confira também</span><span class="sxs-lookup"><span data-stu-id="422af-185">See also</span></span>



[<span data-ttu-id="422af-186">IABLogon::Logoff</span><span class="sxs-lookup"><span data-stu-id="422af-186">IABLogon::Logoff</span></span>](iablogon-logoff.md)
  
[<span data-ttu-id="422af-187">IABLogon::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="422af-187">IABLogon::OpenEntry</span></span>](iablogon-openentry.md)
  
[<span data-ttu-id="422af-188">IMAPISupport::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="422af-188">IMAPISupport::OpenProfileSection</span></span>](imapisupport-openprofilesection.md)
  
[<span data-ttu-id="422af-189">IMAPISupport::SetProviderUID</span><span class="sxs-lookup"><span data-stu-id="422af-189">IMAPISupport::SetProviderUID</span></span>](imapisupport-setprovideruid.md)
  
[<span data-ttu-id="422af-190">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="422af-190">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="422af-191">IABProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="422af-191">IABProvider : IUnknown</span></span>](iabprovideriunknown.md)

