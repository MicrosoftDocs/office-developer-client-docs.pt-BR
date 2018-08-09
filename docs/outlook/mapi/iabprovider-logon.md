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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 21a6907f7511779d7e8ec6825ac68d109d2f48eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766852"
---
# <a name="iabproviderlogon"></a><span data-ttu-id="d19ec-103">IABProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="d19ec-103">IABProvider::Logon</span></span>

  
  
<span data-ttu-id="d19ec-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d19ec-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d19ec-105">Estabelece uma conexão para uma sessão ativa.</span><span class="sxs-lookup"><span data-stu-id="d19ec-105">Establishes a connection to an active session.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="d19ec-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d19ec-106">Parameters</span></span>

 <span data-ttu-id="d19ec-107">_lpMAPISup_</span><span class="sxs-lookup"><span data-stu-id="d19ec-107">_lpMAPISup_</span></span>
  
> <span data-ttu-id="d19ec-108">[in] Um ponteiro para o objeto de suporte do provedor de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="d19ec-108">[in] A pointer to the address book provider's support object.</span></span>
    
 <span data-ttu-id="d19ec-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="d19ec-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="d19ec-110">[in] Uma alça para a janela pai para a caixa de diálogo de logon que exibe o método de **Logon** , se permitido.</span><span class="sxs-lookup"><span data-stu-id="d19ec-110">[in] A handle to the parent window for the logon dialog box that the **Logon** method displays, if permitted.</span></span> <span data-ttu-id="d19ec-111">O parâmetro _ulUIParam_ contém o valor do parâmetro do mesmo nome passado para MAPI na chamada para a função [MAPILogonEx](mapilogonex.md) anterior.</span><span class="sxs-lookup"><span data-stu-id="d19ec-111">The  _ulUIParam_ parameter contains the value of the parameter of the same name passed to MAPI in the previous call to the [MAPILogonEx](mapilogonex.md) function.</span></span> 
    
 <span data-ttu-id="d19ec-112">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="d19ec-112">_lpszProfileName_</span></span>
  
> <span data-ttu-id="d19ec-113">[in] Um ponteiro para o nome do perfil da sessão.</span><span class="sxs-lookup"><span data-stu-id="d19ec-113">[in] A pointer to the name of the session profile.</span></span>
    
 <span data-ttu-id="d19ec-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d19ec-114">_ulFlags_</span></span>
  
> <span data-ttu-id="d19ec-115">[in] Uma bitmask dos sinalizadores que controla como o logon é executado.</span><span class="sxs-lookup"><span data-stu-id="d19ec-115">[in] A bitmask of flags that controls how the logon is performed.</span></span> <span data-ttu-id="d19ec-116">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="d19ec-116">The following flags can be set:</span></span>
    
<span data-ttu-id="d19ec-117">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="d19ec-117">AB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="d19ec-118">O provedor não deve exibir uma caixa de diálogo durante o logon.</span><span class="sxs-lookup"><span data-stu-id="d19ec-118">The provider should not display a dialog box during logon.</span></span> <span data-ttu-id="d19ec-119">Se esse sinalizador não estiver definido, o provedor pode exibir uma caixa de diálogo para solicitar ao usuário para faltando informações de configuração.</span><span class="sxs-lookup"><span data-stu-id="d19ec-119">If this flag is not set, the provider can display a dialog box to prompt the user for missing configuration information.</span></span>
    
<span data-ttu-id="d19ec-120">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="d19ec-120">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="d19ec-121">Permite o **Logon** retornar com êxito, possivelmente antes do processo de logon for concluído.</span><span class="sxs-lookup"><span data-stu-id="d19ec-121">Enables **Logon** to return successfully, possibly before the logon process is finished.</span></span> 
    
<span data-ttu-id="d19ec-122">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d19ec-122">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="d19ec-123">Todas as cadeias de caracteres devem estar no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="d19ec-123">All strings should be in Unicode format.</span></span> <span data-ttu-id="d19ec-124">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres devem estar no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="d19ec-124">If the MAPI_UNICODE flag is not set, the strings should be in ANSI format.</span></span>
    
 <span data-ttu-id="d19ec-125">_lpulcbSecurity_</span><span class="sxs-lookup"><span data-stu-id="d19ec-125">_lpulcbSecurity_</span></span>
  
> <span data-ttu-id="d19ec-126">[além, out] Um ponteiro para o tamanho, em bytes, da estrutura de credenciais de segurança apontado pelo parâmetro _lppbSecurity_ .</span><span class="sxs-lookup"><span data-stu-id="d19ec-126">[in, out] A pointer to the size, in bytes, of the security credentials structure pointed to by the  _lppbSecurity_ parameter.</span></span> <span data-ttu-id="d19ec-127">Na entrada, o valor deve ser diferente de zero; na saída, o valor deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="d19ec-127">On input, the value must be nonzero; on output, the value must be zero.</span></span> <span data-ttu-id="d19ec-128">Em ambos os casos, os ponteiros devem ser válidos.</span><span class="sxs-lookup"><span data-stu-id="d19ec-128">In both cases, the pointers must be valid.</span></span> 
    
 <span data-ttu-id="d19ec-129">_lppbSecurity_</span><span class="sxs-lookup"><span data-stu-id="d19ec-129">_lppbSecurity_</span></span>
  
> <span data-ttu-id="d19ec-130">[além, out] Um ponteiro para um ponteiro para as credenciais de segurança.</span><span class="sxs-lookup"><span data-stu-id="d19ec-130">[in, out] A pointer to a pointer to security credentials.</span></span> <span data-ttu-id="d19ec-131">Na entrada, o valor deve ser diferente de zero; na saída, o valor deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="d19ec-131">On input, the value must be nonzero; on output, the value must be zero.</span></span> <span data-ttu-id="d19ec-132">Em ambos os casos, o ponteiro deve ser válido.</span><span class="sxs-lookup"><span data-stu-id="d19ec-132">In both cases the pointer must be valid.</span></span>
    
 <span data-ttu-id="d19ec-133">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="d19ec-133">_lppMAPIError_</span></span>
  
> <span data-ttu-id="d19ec-134">[out] Um ponteiro para um ponteiro para uma estrutura [MAPIERROR](mapierror.md) .</span><span class="sxs-lookup"><span data-stu-id="d19ec-134">[out] A pointer to a pointer to a [MAPIERROR](mapierror.md) structure.</span></span> <span data-ttu-id="d19ec-135">O parâmetro _lppMAPIError_ pode ser definido como NULL se não houver nenhuma estrutura **MAPIERROR** para retornar.</span><span class="sxs-lookup"><span data-stu-id="d19ec-135">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
 <span data-ttu-id="d19ec-136">_lppABLogon_</span><span class="sxs-lookup"><span data-stu-id="d19ec-136">_lppABLogon_</span></span>
  
> <span data-ttu-id="d19ec-137">[out] Um ponteiro para um ponteiro para o objeto de logon do provedor.</span><span class="sxs-lookup"><span data-stu-id="d19ec-137">[out] A pointer to a pointer to the provider's logon object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d19ec-138">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="d19ec-138">Return value</span></span>

<span data-ttu-id="d19ec-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="d19ec-139">S_OK</span></span> 
  
> <span data-ttu-id="d19ec-140">Uma conexão para uma sessão ativa foi estabelecida com êxito.</span><span class="sxs-lookup"><span data-stu-id="d19ec-140">A connection to an active session was successfully established.</span></span>
    
<span data-ttu-id="d19ec-141">MAPI_E_FAILONEPROVIDER</span><span class="sxs-lookup"><span data-stu-id="d19ec-141">MAPI_E_FAILONEPROVIDER</span></span> 
  
> <span data-ttu-id="d19ec-142">O provedor não pode fazer logon, mas MAPI pode continuar a fazer logon com os outros provedores no serviço de mensagem ao qual o provedor pertence.</span><span class="sxs-lookup"><span data-stu-id="d19ec-142">The provider cannot log on, but MAPI can continue to log on the other providers in the message service to which the provider belongs.</span></span> 
    
<span data-ttu-id="d19ec-143">MAPI_E_UNCONFIGURED</span><span class="sxs-lookup"><span data-stu-id="d19ec-143">MAPI_E_UNCONFIGURED</span></span> 
  
> <span data-ttu-id="d19ec-144">O provedor tem informações suficientes para concluir o logon.</span><span class="sxs-lookup"><span data-stu-id="d19ec-144">The provider has insufficient information to complete the logon.</span></span> <span data-ttu-id="d19ec-145">Função de entrada de serviço de mensagem do provedor a chamadas de MAPI.</span><span class="sxs-lookup"><span data-stu-id="d19ec-145">MAPI calls the provider's message service entry function.</span></span>
    
<span data-ttu-id="d19ec-146">MAPI_E_UNKNOWN_CPID</span><span class="sxs-lookup"><span data-stu-id="d19ec-146">MAPI_E_UNKNOWN_CPID</span></span> 
  
> <span data-ttu-id="d19ec-147">O servidor não está configurado para oferecer suporte à página de código do cliente.</span><span class="sxs-lookup"><span data-stu-id="d19ec-147">The server is not configured to support the client's code page.</span></span>
    
<span data-ttu-id="d19ec-148">MAPI_E_UNKNOWN_LCID</span><span class="sxs-lookup"><span data-stu-id="d19ec-148">MAPI_E_UNKNOWN_LCID</span></span> 
  
> <span data-ttu-id="d19ec-149">O servidor não está configurado para oferecer suporte a informações de localidade do cliente.</span><span class="sxs-lookup"><span data-stu-id="d19ec-149">The server is not configured to support the client's locale information.</span></span>
    
<span data-ttu-id="d19ec-150">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="d19ec-150">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="d19ec-151">O usuário cancelou a operação, geralmente clicando no botão **Cancelar** na caixa de diálogo de logon.</span><span class="sxs-lookup"><span data-stu-id="d19ec-151">The user canceled the operation, typically by clicking the **Cancel** button in the logon dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d19ec-152">Comentários</span><span class="sxs-lookup"><span data-stu-id="d19ec-152">Remarks</span></span>

<span data-ttu-id="d19ec-153">Conexões estabelecidas com cada provedor de catálogo de endereços no perfil da sessão quando um cliente chama o método [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) .</span><span class="sxs-lookup"><span data-stu-id="d19ec-153">Connections are established with each address book provider in the session profile when a client calls the [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) method.</span></span> <span data-ttu-id="d19ec-154">**OpenAddressBook** chama o método de **Logon** do cada provedor.</span><span class="sxs-lookup"><span data-stu-id="d19ec-154">**OpenAddressBook** then calls each provider's **Logon** method.</span></span> 
  
<span data-ttu-id="d19ec-155">O nome do perfil apontado pelo parâmetro _lpszProfileName_ é exibido no conjunto de caracteres do cliente do usuário conforme indicado pela presença ou ausência do sinalizador MAPI_UNICODE no parâmetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="d19ec-155">The profile name pointed to by the  _lpszProfileName_ parameter is displayed in the character set of the user's client as indicated by the presence or absence of the MAPI_UNICODE flag in the  _ulFlags_ parameter.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="d19ec-156">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="d19ec-156">Notes to implementers</span></span>

<span data-ttu-id="d19ec-157">Em sua implementação do método **Logon** , chame o método de [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) para registrar um identificador exclusivo, ou uma estrutura [MAPIUID](mapiuid.md) .</span><span class="sxs-lookup"><span data-stu-id="d19ec-157">In your implementation of the **Logon** method, call the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method to register a unique identifier, or [MAPIUID](mapiuid.md) structure.</span></span> <span data-ttu-id="d19ec-158">Cada um dos seus objetos terão um identificador de entrada que inclua este **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="d19ec-158">Each of your objects will have an entry identifier that includes this **MAPIUID**.</span></span> <span data-ttu-id="d19ec-159">O MAPI usa o **MAPIUID** para corresponder a um objeto com seu provedor.</span><span class="sxs-lookup"><span data-stu-id="d19ec-159">MAPI uses the **MAPIUID** to match an object with its provider.</span></span> <span data-ttu-id="d19ec-160">Por exemplo, quando um cliente chama o método [IMAPISession::OpenEntry](imapisession-openentry.md) para abrir um usuário de mensagens, **OpenEntry** examina a parte **MAPIUID** do identificador de entrada que foi passado e faz a correspondência com um **MAPIUID** registrados por um provedor de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="d19ec-160">For example, when a client calls the [IMAPISession::OpenEntry](imapisession-openentry.md) method to open a messaging user, **OpenEntry** examines the **MAPIUID** portion of the entry identifier that was passed in and matches it with a **MAPIUID** registered by an address book provider.</span></span> 
  
<span data-ttu-id="d19ec-161">Se um cliente fizer logon ao seu provedor de mais de uma vez, convém registrar um **MAPIUID** de diferentes para cada logon.</span><span class="sxs-lookup"><span data-stu-id="d19ec-161">If a client logs on to your provider more than once, you may want to register a different **MAPIUID** for each logon.</span></span> <span data-ttu-id="d19ec-162">Registrar as estruturas **MAPIUID** exclusivas permite MAPI corretamente rotear solicitações para a instância do provedor apropriado.</span><span class="sxs-lookup"><span data-stu-id="d19ec-162">Registering unique **MAPIUID** structures enables MAPI to correctly route requests to the appropriate provider instance.</span></span> <span data-ttu-id="d19ec-163">No entanto, convém ter cada objeto de logon compartilhar um **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="d19ec-163">However, you may want to have every logon object share one **MAPIUID**.</span></span> <span data-ttu-id="d19ec-164">Nesse caso, você deve ser capaz de lidar com o roteamento sozinho, em vez de depender de MAPI.</span><span class="sxs-lookup"><span data-stu-id="d19ec-164">In this case, you must be able to handle the routing yourself instead of relying on MAPI.</span></span> <span data-ttu-id="d19ec-165">Para obter mais informações sobre como criar um **MAPIUID**, consulte [Registrando serviço provedor exclusivo identificadores](registering-service-provider-unique-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="d19ec-165">For more information about how to create a **MAPIUID**, see [Registering Service Provider Unique Identifiers](registering-service-provider-unique-identifiers.md).</span></span>
  
<span data-ttu-id="d19ec-166">O objeto de suporte a MAPI passa para seu método de **Logon** no parâmetro _lpMAPISup_ fornece acesso a muitos dos métodos incluídos no [IMAPISupport: IUnknown](imapisupportiunknown.md) interface.</span><span class="sxs-lookup"><span data-stu-id="d19ec-166">The support object that MAPI passes to your **Logon** method in the  _lpMAPISup_ parameter provides access to many of the methods included in the [IMAPISupport : IUnknown](imapisupportiunknown.md) interface.</span></span> <span data-ttu-id="d19ec-167">MAPI cria um objeto de suporte que é personalizado para seu tipo de provedor.</span><span class="sxs-lookup"><span data-stu-id="d19ec-167">MAPI creates a support object that is customized to your type of provider.</span></span> <span data-ttu-id="d19ec-168">Por exemplo, se você precisa fazer logon um sistema de mensagens subjacente ou o serviço de diretório ao estabelecer sua conexão, você pode chamar o método [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) para recuperar as credenciais de segurança para esta sessão de logon específica.</span><span class="sxs-lookup"><span data-stu-id="d19ec-168">For example, if you need to log on to an underlying messaging system or directory service when you establish your connection, you can call the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to retrieve security credentials for this particular logon session.</span></span> 
  
<span data-ttu-id="d19ec-169">Se o **Logon** for bem-sucedido, certifique-se de que você chamar o suporte ao método do objeto [AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) para incrementar sua contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="d19ec-169">If **Logon** is successful, be sure that you call the support object's [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) method to increment its reference count.</span></span> <span data-ttu-id="d19ec-170">Isso permite que o seu provedor mantenha o ponteiro de objeto de suporte para o restante da sessão.</span><span class="sxs-lookup"><span data-stu-id="d19ec-170">This enables your provider to hold onto the support object pointer for the rest of the session.</span></span> <span data-ttu-id="d19ec-171">Se você não chamar esse método **AddRef** , MAPI descarregará o seu provedor.</span><span class="sxs-lookup"><span data-stu-id="d19ec-171">If you do not call this **AddRef** method, MAPI will unload your provider.</span></span> 
  
<span data-ttu-id="d19ec-172">Você pode incluir o nome do perfil passado no parâmetro _lpszProfileName_ em caixas de diálogo de erro, telas de logon ou outras interfaces de usuário.</span><span class="sxs-lookup"><span data-stu-id="d19ec-172">You can include the profile name passed in the  _lpszProfileName_ parameter in error dialog boxes, logon screens, or other user interfaces.</span></span> <span data-ttu-id="d19ec-173">Para usar o nome do perfil, copie-o para armazenamento que você tiver alocado.</span><span class="sxs-lookup"><span data-stu-id="d19ec-173">To use the profile name, copy it to storage that you have allocated.</span></span> 
  
<span data-ttu-id="d19ec-174">Criar um objeto de logon e retornar um ponteiro para ele no parâmetro _lppABLogon_ .</span><span class="sxs-lookup"><span data-stu-id="d19ec-174">Create a logon object and return a pointer to it in the  _lppABLogon_ parameter.</span></span> <span data-ttu-id="d19ec-175">MAPI usa esse objeto de logon para fazer chamadas para os métodos na sua implementação [IABLogon](iablogoniunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="d19ec-175">MAPI uses this logon object to make calls to the methods in your [IABLogon](iablogoniunknown.md) implementation.</span></span> 
  
<span data-ttu-id="d19ec-176">Se você precisar de uma senha durante o logon, exibe uma caixa de diálogo logon apenas se o sinalizador AB_NO_DIALOG não estiver definido.</span><span class="sxs-lookup"><span data-stu-id="d19ec-176">If you require a password during logon, display a logon dialog box only if the AB_NO_DIALOG flag is not set.</span></span> <span data-ttu-id="d19ec-177">Se o usuário cancelar o processo de logon, geralmente clicando no botão **Cancelar** na caixa de diálogo retorne MAPI_E_USER_CANCEL de **Logon**.</span><span class="sxs-lookup"><span data-stu-id="d19ec-177">If the user cancels the logon process, typically by clicking the **Cancel** button in the dialog box, return MAPI_E_USER_CANCEL from **Logon**.</span></span>
  
<span data-ttu-id="d19ec-178">Normalmente, quando um provedor de catálogo de endereços não pode fazer logon, MAPI desabilita o serviço de mensagem ao qual pertence o provedor está falhando — ou seja, MAPI não tentará estabelecer conexões por qualquer um dos outros provedores que pertencem ao serviço para o restante da sessão tempo de vida.</span><span class="sxs-lookup"><span data-stu-id="d19ec-178">Typically, when an address book provider cannot log on, MAPI disables the message service to which the failing provider belongs—that is, MAPI will not try to establish connections for any of the other providers that belong to the service for the rest of the session's lifetime.</span></span> <span data-ttu-id="d19ec-179">No entanto, se o seu provedor não é possível estabelecer uma conexão e você não deseja desabilitar todo o serviço, retorne MAPI_E_FAILONEPROVIDER ou MAPI_E_UNCONFIGURED.</span><span class="sxs-lookup"><span data-stu-id="d19ec-179">However, if your provider cannot establish a connection and you want not to disable the entire service, return either MAPI_E_FAILONEPROVIDER or MAPI_E_UNCONFIGURED.</span></span> <span data-ttu-id="d19ec-180">MAPI não desabilitará o serviço de mensagem ao qual o provedor pertence.</span><span class="sxs-lookup"><span data-stu-id="d19ec-180">MAPI will not disable the message service to which the provider belongs.</span></span> 
  
<span data-ttu-id="d19ec-181">Retorno MAPI_E_FAILONEPROVIDER se ocorrer um erro que não é grave o suficiente para impedir que os outros provedores no serviço de mensagem estabelecer conexões.</span><span class="sxs-lookup"><span data-stu-id="d19ec-181">Return MAPI_E_FAILONEPROVIDER if an error occurs that is not serious enough to prevent the other providers in the message service from establishing connections.</span></span> <span data-ttu-id="d19ec-182">Retorne MAPI_E_UNCONFIGURED se as informações de configuração necessárias estão ausentes do perfil e você não pode exibir uma caixa de diálogo para solicitar ao usuário.</span><span class="sxs-lookup"><span data-stu-id="d19ec-182">Return MAPI_E_UNCONFIGURED if the necessary configuration information is missing from the profile and you cannot display a dialog box to prompt the user.</span></span> <span data-ttu-id="d19ec-183">MAPI responderá ao chamar a função de ponto de entrada do seu provedor mensagem serviço com MSG_SERVICE_CONFIGURE definido como o parâmetro _ulContext_ para fornecer o serviço a oportunidade de se configurar propriamente dito, seja programaticamente ou usar uma folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="d19ec-183">MAPI will respond by calling your provider's message service entry point function with MSG_SERVICE_CONFIGURE set as the  _ulContext_ parameter to give the service a chance to configure itself, either programmatically or using a property sheet.</span></span> <span data-ttu-id="d19ec-184">Quando a entrada de serviço de mensagem aponte concluiu a função, MAPI repete o logon.</span><span class="sxs-lookup"><span data-stu-id="d19ec-184">When the message service entry point function has finished, MAPI retries the logon.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d19ec-185">Confira também</span><span class="sxs-lookup"><span data-stu-id="d19ec-185">See also</span></span>



[<span data-ttu-id="d19ec-186">IABLogon::Logoff</span><span class="sxs-lookup"><span data-stu-id="d19ec-186">IABLogon::Logoff</span></span>](iablogon-logoff.md)
  
[<span data-ttu-id="d19ec-187">IABLogon::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="d19ec-187">IABLogon::OpenEntry</span></span>](iablogon-openentry.md)
  
[<span data-ttu-id="d19ec-188">IMAPISupport::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="d19ec-188">IMAPISupport::OpenProfileSection</span></span>](imapisupport-openprofilesection.md)
  
[<span data-ttu-id="d19ec-189">IMAPISupport::SetProviderUID</span><span class="sxs-lookup"><span data-stu-id="d19ec-189">IMAPISupport::SetProviderUID</span></span>](imapisupport-setprovideruid.md)
  
[<span data-ttu-id="d19ec-190">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="d19ec-190">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="d19ec-191">IABProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d19ec-191">IABProvider : IUnknown</span></span>](iabprovideriunknown.md)

