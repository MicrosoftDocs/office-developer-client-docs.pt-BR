---
title: MAPILogonEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPILogonEx
api_type:
- HeaderDef
ms.assetid: 98091e5b-1abd-4814-9c7a-583b420ee11d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9f2ec8f0ec00f7314982e9b112415f69901c358c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424116"
---
# <a name="mapilogonex"></a><span data-ttu-id="ea902-103">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="ea902-103">MAPILogonEx</span></span>

  
  
<span data-ttu-id="ea902-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ea902-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ea902-105">Registra um aplicativo cliente em uma sessão com o sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="ea902-105">Logs a client application on to a session with the messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ea902-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="ea902-106">Header file:</span></span>  <br/> |<span data-ttu-id="ea902-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="ea902-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="ea902-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="ea902-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ea902-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ea902-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ea902-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="ea902-110">Called by:</span></span>  <br/> |<span data-ttu-id="ea902-111">Aplicativos do cliente</span><span class="sxs-lookup"><span data-stu-id="ea902-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT MAPILogonEx(
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  FLAGS flFlags,
  LPMAPISESSION FAR * lppSession
);
```

## <a name="parameters"></a><span data-ttu-id="ea902-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ea902-112">Parameters</span></span>

 <span data-ttu-id="ea902-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="ea902-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="ea902-114">[in] Alça para a janela para a qual a caixa de diálogo de logon é modal.</span><span class="sxs-lookup"><span data-stu-id="ea902-114">[in] Handle to the window to which the logon dialog box is modal.</span></span> <span data-ttu-id="ea902-115">Se nenhuma caixa de diálogo aparecer durante a chamada, o  _parâmetro ulUIParam_ será ignorado.</span><span class="sxs-lookup"><span data-stu-id="ea902-115">If no dialog box appears during the call, the  _ulUIParam_ parameter is ignored.</span></span> <span data-ttu-id="ea902-116">Esse parâmetro pode ser zero.</span><span class="sxs-lookup"><span data-stu-id="ea902-116">This parameter can be zero.</span></span> 
    
 <span data-ttu-id="ea902-117">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="ea902-117">_lpszProfileName_</span></span>
  
> <span data-ttu-id="ea902-118">[in] Ponteiro para uma cadeia de caracteres que contém o nome do perfil a ser usado quando o usuário faz o login.</span><span class="sxs-lookup"><span data-stu-id="ea902-118">[in] Pointer to a string that contains the name of the profile to use when the user logs on.</span></span> <span data-ttu-id="ea902-119">Esta cadeia de caracteres é limitada a 64 caracteres.</span><span class="sxs-lookup"><span data-stu-id="ea902-119">This string is limited to 64 characters.</span></span>
    
 <span data-ttu-id="ea902-120">_lpszPassword_</span><span class="sxs-lookup"><span data-stu-id="ea902-120">_lpszPassword_</span></span>
  
> <span data-ttu-id="ea902-121">[in] Ponteiro para uma cadeia de caracteres que contém a senha do perfil.</span><span class="sxs-lookup"><span data-stu-id="ea902-121">[in] Pointer to a string that contains the password of the profile.</span></span> <span data-ttu-id="ea902-122">O  _parâmetro lpszPassword_ deve ser NULL.</span><span class="sxs-lookup"><span data-stu-id="ea902-122">The  _lpszPassword_ parameter must be NULL.</span></span> 
    
 <span data-ttu-id="ea902-123">_flFlags_</span><span class="sxs-lookup"><span data-stu-id="ea902-123">_flFlags_</span></span>
  
> <span data-ttu-id="ea902-124">[in] Bitmask de sinalizadores usados para controlar como o logon é realizado.</span><span class="sxs-lookup"><span data-stu-id="ea902-124">[in] Bitmask of flags used to control how logon is performed.</span></span> <span data-ttu-id="ea902-125">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="ea902-125">The following flags can be set:</span></span>
    
<span data-ttu-id="ea902-126">MAPI_ALLOW_OTHERS</span><span class="sxs-lookup"><span data-stu-id="ea902-126">MAPI_ALLOW_OTHERS</span></span> 
  
> <span data-ttu-id="ea902-127">A sessão compartilhada deve ser retornada, o que permite que clientes posteriores obtenham a sessão sem fornecer nenhuma credencial de usuário.</span><span class="sxs-lookup"><span data-stu-id="ea902-127">The shared session should be returned, which allows later clients to obtain the session without providing any user credentials.</span></span> 
    
<span data-ttu-id="ea902-128">MAPI_BG_SESSION</span><span class="sxs-lookup"><span data-stu-id="ea902-128">MAPI_BG_SESSION</span></span>
  
> <span data-ttu-id="ea902-129">Faça logon em uma sessão e execute qualquer operação em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="ea902-129">Log on to a session and run any operations in the background.</span></span> <span data-ttu-id="ea902-130">Em geral, se um cliente pretende fazer o processamento em um thread em segundo plano ou em um processo separado de uma maneira que seja discreta para o thread em primeiro plano, ele deverá chamar com o sinalizador MAPI_BG_SESSION pesquisa.</span><span class="sxs-lookup"><span data-stu-id="ea902-130">In general, if a client intends to do processing on a background thread or in a separate process in a manner that is unobtrusive to the foreground thread, it should call with the MAPI_BG_SESSION flag.</span></span> <span data-ttu-id="ea902-131">Um aplicativo cliente como um mecanismo de indexação ou a abertura de um Arquivo de Pastas Particulares (PST) para acesso de tipo em segundo plano são alguns exemplos de onde usar MAPI_BG_SESSION. MAPILogonEx.</span><span class="sxs-lookup"><span data-stu-id="ea902-131">A client application such as an indexing engine or opening a Personal Folders File (PST) for background type access are some examples of where to use MAPI_BG_SESSION.MAPILogonEx.</span></span>
    
<span data-ttu-id="ea902-132">MAPI_EXPLICIT_PROFILE</span><span class="sxs-lookup"><span data-stu-id="ea902-132">MAPI_EXPLICIT_PROFILE</span></span> 
  
> <span data-ttu-id="ea902-133">O perfil padrão não deve ser usado e o usuário deve ser obrigado a fornecer um perfil.</span><span class="sxs-lookup"><span data-stu-id="ea902-133">The default profile should not be used and the user should be required to supply a profile.</span></span> 
    
<span data-ttu-id="ea902-134">MAPI_EXTENDED</span><span class="sxs-lookup"><span data-stu-id="ea902-134">MAPI_EXTENDED</span></span> 
  
> <span data-ttu-id="ea902-135">Faça logoff com recursos estendidos.</span><span class="sxs-lookup"><span data-stu-id="ea902-135">Log on with extended capabilities.</span></span> <span data-ttu-id="ea902-136">Esse sinalizador sempre deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="ea902-136">This flag should always be set.</span></span>
    
<span data-ttu-id="ea902-137">MAPI_FORCE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="ea902-137">MAPI_FORCE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="ea902-138">Uma tentativa deve ser feita para baixar todas as mensagens do usuário antes de retornar.</span><span class="sxs-lookup"><span data-stu-id="ea902-138">An attempt should be made to download all of the user's messages before returning.</span></span> <span data-ttu-id="ea902-139">Se o MAPI_FORCE_DOWNLOAD sinalizador não estiver definido, as mensagens poderão ser baixadas em segundo plano depois que a chamada para MAPILogonEx retornar.</span><span class="sxs-lookup"><span data-stu-id="ea902-139">If the MAPI_FORCE_DOWNLOAD flag is not set, messages can be downloaded in the background after the call to MAPILogonEx returns.</span></span> 
    
<span data-ttu-id="ea902-140">MAPI_LOGON_UI</span><span class="sxs-lookup"><span data-stu-id="ea902-140">MAPI_LOGON_UI</span></span> 
  
> <span data-ttu-id="ea902-141">Uma caixa de diálogo deve ser exibida para solicitar ao usuário informações de logon, se necessário.</span><span class="sxs-lookup"><span data-stu-id="ea902-141">A dialog box should be displayed to prompt the user for logon information if required.</span></span> <span data-ttu-id="ea902-142">Quando o MAPI_LOGON_UI não estiver definido, o cliente de chamada não exibirá uma caixa de diálogo de logon e retornará um valor de erro se o usuário não estiver conectado.</span><span class="sxs-lookup"><span data-stu-id="ea902-142">When the MAPI_LOGON_UI flag is not set, the calling client does not display a logon dialog box and returns an error value if the user is not logged on.</span></span>
    
<span data-ttu-id="ea902-143">MAPI_NEW_SESSION</span><span class="sxs-lookup"><span data-stu-id="ea902-143">MAPI_NEW_SESSION</span></span> 
  
> <span data-ttu-id="ea902-144">Deve ser feita uma tentativa de criar uma nova sessão MAPI em vez de adquirir a sessão compartilhada.</span><span class="sxs-lookup"><span data-stu-id="ea902-144">An attempt should be made to create a new MAPI session instead of acquiring the shared session.</span></span> <span data-ttu-id="ea902-145">Se o MAPI_NEW_SESSION sinalizador não estiver definido, MAPILogonEx usará uma sessão compartilhada existente, mesmo se o parâmetro  _lpszprofileName_ não for NULL.</span><span class="sxs-lookup"><span data-stu-id="ea902-145">If the MAPI_NEW_SESSION flag is not set, MAPILogonEx uses an existing shared session even if the  _lpszprofileName_ parameter is not NULL.</span></span> 
    
<span data-ttu-id="ea902-146">MAPI_NO_MAIL</span><span class="sxs-lookup"><span data-stu-id="ea902-146">MAPI_NO_MAIL</span></span> 
  
> <span data-ttu-id="ea902-147">O MAPI não deve informar o spooler MAPI sobre a existência da sessão.</span><span class="sxs-lookup"><span data-stu-id="ea902-147">MAPI should not inform the MAPI spooler of the session's existence.</span></span> <span data-ttu-id="ea902-148">O resultado é que nenhuma mensagem pode ser enviada ou recebida na sessão, exceto por meio de um par de armazenamento e transporte fortemente emparelhados.</span><span class="sxs-lookup"><span data-stu-id="ea902-148">The result is that no messages can be sent or received in the session except through a tightly coupled store and transport pair.</span></span> <span data-ttu-id="ea902-149">Um cliente de chamada define esse sinalizador se estiver agindo como um agente, se o trabalho de configuração tiver que ser feito ou se o cliente estiver navegando nos armazenamentos de mensagens disponíveis.</span><span class="sxs-lookup"><span data-stu-id="ea902-149">A calling client sets this flag if it is acting as an agent, if configuration work must be done, or if the client is browsing the available message stores.</span></span> 
    
<span data-ttu-id="ea902-150">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="ea902-150">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="ea902-151">O chamador está sendo executado como um serviço do Windows.</span><span class="sxs-lookup"><span data-stu-id="ea902-151">The caller is running as a Windows service.</span></span> <span data-ttu-id="ea902-152">Os chamadores que não estão sendo executados como um serviço do Windows não devem definir esse sinalizador; os chamadores que estão sendo executados como um serviço devem definir esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="ea902-152">Callers that are not running as a Windows service should not set this flag; callers that are running as a service must set this flag.</span></span> 
    
<span data-ttu-id="ea902-153">MAPI_SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="ea902-153">MAPI_SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="ea902-154">MAPILogonEx deve exibir uma caixa de diálogo de configuração para cada serviço de mensagem no perfil.</span><span class="sxs-lookup"><span data-stu-id="ea902-154">MAPILogonEx should display a configuration dialog box for each message service in the profile.</span></span> <span data-ttu-id="ea902-155">As caixas de diálogo são exibidas após o perfil ter sido escolhido, mas antes de qualquer serviço de mensagens estar conectado.</span><span class="sxs-lookup"><span data-stu-id="ea902-155">The dialog boxes are displayed after the profile has been chosen but before any message service is logged on.</span></span> <span data-ttu-id="ea902-156">A caixa de diálogo comum MAPI para logon também contém uma caixa de seleção que solicita a mesma operação.</span><span class="sxs-lookup"><span data-stu-id="ea902-156">The MAPI common dialog box for logon also contains a check box that requests the same operation.</span></span> 
    
<span data-ttu-id="ea902-157">MAPI_TIMEOUT_SHORT</span><span class="sxs-lookup"><span data-stu-id="ea902-157">MAPI_TIMEOUT_SHORT</span></span> 
  
> <span data-ttu-id="ea902-158">O logon deve falhar se for bloqueado por mais de alguns segundos.</span><span class="sxs-lookup"><span data-stu-id="ea902-158">The logon should fail if blocked for more than a few seconds.</span></span> 
    
<span data-ttu-id="ea902-159">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ea902-159">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ea902-160">As cadeias de caracteres passadas estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="ea902-160">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="ea902-161">Se o MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="ea902-161">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
<span data-ttu-id="ea902-162">MAPI_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="ea902-162">MAPI_USE_DEFAULT</span></span> 
  
> <span data-ttu-id="ea902-163">O subsistema de mensagens deve substituir o nome de perfil do perfil padrão pelo _parâmetro lpszProfileName._</span><span class="sxs-lookup"><span data-stu-id="ea902-163">The messaging subsystem should substitute the profile name of the default profile for the  _lpszProfileName_ parameter.</span></span> <span data-ttu-id="ea902-164">O MAPI_EXPLICIT_PROFILE sinalizador é ignorado, a menos que  _lpszProfileName_ seja NULL ou vazio.</span><span class="sxs-lookup"><span data-stu-id="ea902-164">The MAPI_EXPLICIT_PROFILE flag is ignored unless  _lpszProfileName_ is NULL or empty.</span></span> 
    
 <span data-ttu-id="ea902-165">_lppSession_</span><span class="sxs-lookup"><span data-stu-id="ea902-165">_lppSession_</span></span>
  
> <span data-ttu-id="ea902-166">[out] Ponteiro para um ponteiro para a interface de sessão MAPI.</span><span class="sxs-lookup"><span data-stu-id="ea902-166">[out] Pointer to a pointer to the MAPI session interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ea902-167">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ea902-167">Return value</span></span>

<span data-ttu-id="ea902-168">S_OK</span><span class="sxs-lookup"><span data-stu-id="ea902-168">S_OK</span></span> 
  
> <span data-ttu-id="ea902-169">O logon foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="ea902-169">The logon succeeded.</span></span>
    
<span data-ttu-id="ea902-170">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="ea902-170">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="ea902-171">O logon não foi bem-sucedido, porque um ou mais parâmetros para MAPILogonEx eram inválidos ou porque já havia muitas sessões abertas.</span><span class="sxs-lookup"><span data-stu-id="ea902-171">The logon was unsuccessful, either because one or more of the parameters to MAPILogonEx were invalid or because there were too many sessions open already.</span></span>
    
<span data-ttu-id="ea902-172">MAPI_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="ea902-172">MAPI_E_TIMEOUT</span></span> 
  
> <span data-ttu-id="ea902-173">O MAPI serializa todos os logons por meio de um mutex.</span><span class="sxs-lookup"><span data-stu-id="ea902-173">MAPI serializes all logons through a mutex.</span></span> <span data-ttu-id="ea902-174">Isso será retornado se o MAPI_TIMEOUT_SHORT sinalizador tiver sido definido e outro thread tiver mantido o mutex.</span><span class="sxs-lookup"><span data-stu-id="ea902-174">This is returned if the MAPI_TIMEOUT_SHORT flag was set and another thread held the mutex.</span></span> 
    
<span data-ttu-id="ea902-175">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="ea902-175">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="ea902-176">O usuário cancelou a operação, normalmente clicando no botão Cancelar **em** uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="ea902-176">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ea902-177">Comentários</span><span class="sxs-lookup"><span data-stu-id="ea902-177">Remarks</span></span>

<span data-ttu-id="ea902-178">Os aplicativos cliente MAPI chamam a função MAPILogonEx para fazer logon em uma sessão com o sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="ea902-178">MAPI client applications call the MAPILogonEx function to log on to a session with the messaging system.</span></span> <span data-ttu-id="ea902-179">Todas as cadeias de caracteres que são passadas e retornadas de e para chamadas MAPI são terminadas por caractere nulo e devem ser especificadas no conjunto de caracteres atual ou na página de código do cliente ou do sistema operacional do provedor de chamada.</span><span class="sxs-lookup"><span data-stu-id="ea902-179">All strings that are passed in and returned to and from MAPI calls are null-terminated and must be specified in the current character set or code page of the calling client or provider's operating system.</span></span>
  
<span data-ttu-id="ea902-180">O  _parâmetro lpszProfileName_ será ignorado se houver uma sessão anterior chamada MapiLogonEx com o sinalizador MAPI_ALLOW_OTHERS definido e se o sinalizador MAPI_NEW_SESSION não estiver definido.</span><span class="sxs-lookup"><span data-stu-id="ea902-180">The  _lpszProfileName_ parameter is ignored if there is an existing previous session that called MapiLogonEx with the MAPI_ALLOW_OTHERS flag set and if the flag MAPI_NEW_SESSION is not set.</span></span> <span data-ttu-id="ea902-181">Se o parâmetro  _lpszProfileName_ for NULL ou aponta para uma cadeia de caracteres vazia e o parâmetro  _flFlags_ incluir o sinalizador MAPI_LOGON_UI, a função MAPILogonEx gerará uma caixa de diálogo de logon com um campo vazio para o nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="ea902-181">If the  _lpszProfileName_ parameter is NULL or points to an empty string, and the  _flFlags_ parameter includes the MAPI_LOGON_UI flag, the MAPILogonEx function generates a logon dialog box that has an empty field for the profile name.</span></span> 
  
<span data-ttu-id="ea902-182">Ao fazer logor em um perfil específico, um cliente deve passar o sinalizador MAPI_NEW_SESSION para MAPILogonEx, além do nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="ea902-182">When logging on to a specific profile, a client should pass the MAPI_NEW_SESSION flag into MAPILogonEx in addition to the profile name.</span></span> <span data-ttu-id="ea902-183">Caso contrário, se outro cliente tiver estabelecido uma sessão compartilhada fazendo logon com o MAPI_ALLOW_OTHERS, o cliente será conectado à sessão compartilhada em vez de ao perfil solicitado.</span><span class="sxs-lookup"><span data-stu-id="ea902-183">Otherwise, if another client has established a shared session by logging on with MAPI_ALLOW_OTHERS, the client will be logged on to the shared session instead of to the profile requested.</span></span> 
  
<span data-ttu-id="ea902-184">O MAPI_EXPLICIT_PROFILE sinalizador não faz com que o nome de perfil padrão seja usado quando  _lpszProfileName_ for NULL ou vazio, a menos que o sinalizador MAPI_USE_DEFAULT também esteja presente.</span><span class="sxs-lookup"><span data-stu-id="ea902-184">The MAPI_EXPLICIT_PROFILE flag does not cause the default profile name to be used when  _lpszProfileName_ is NULL or empty unless the MAPI_USE_DEFAULT flag is also present.</span></span> 
  
<span data-ttu-id="ea902-185">O MAPI_NO_MAIL sinalizador tem vários efeitos que causam o seguinte ao não usar o spooler MAPI:</span><span class="sxs-lookup"><span data-stu-id="ea902-185">The MAPI_NO_MAIL flag has several effects that cause the following when not using the MAPI spooler:</span></span>
  
- <span data-ttu-id="ea902-186">Nenhuma mensagem pode ser enviada ou entregue pelo spooler MAPI durante esta sessão.</span><span class="sxs-lookup"><span data-stu-id="ea902-186">No messages can be sent or delivered by the MAPI spooler during this session.</span></span> <span data-ttu-id="ea902-187">Somente provedores de transporte e armazenamento fortemente próximos podem enviar e entregar mensagens.</span><span class="sxs-lookup"><span data-stu-id="ea902-187">Only tightly coupled store and transport providers can send and deliver messages.</span></span> 
    
- <span data-ttu-id="ea902-188">Os armazenamentos baseados em servidor ainda podem enviar ou entregar mensagens.</span><span class="sxs-lookup"><span data-stu-id="ea902-188">Server based stores might still send or deliver messages.</span></span> 
    
- <span data-ttu-id="ea902-189">As mensagens enviadas ou entregues por armazenamentos baseados em servidor não são processadas por provedores de ganchos.</span><span class="sxs-lookup"><span data-stu-id="ea902-189">Messages sent or delivered by server based stores are not processed by any hook providers.</span></span> 
    
- <span data-ttu-id="ea902-190">Opções por mensagem e por destinatário para transporte não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="ea902-190">Per-message and per-recipient options for transports are not available.</span></span> 
    
- <span data-ttu-id="ea902-191">A tabela de status não contém entradas para provedores de transporte, e nenhuma funcionalidade de transporte dependente de objetos de status (como configuração) está disponível.</span><span class="sxs-lookup"><span data-stu-id="ea902-191">The status table does not contain entries for transport providers, and any transport functionality dependent on status objects (such as configuration) is not available.</span></span> 
    
- <span data-ttu-id="ea902-192">A linha do spooler de mensagem na tabela de status contém o valor STATUS_FAILURE mensagem.</span><span class="sxs-lookup"><span data-stu-id="ea902-192">The message spooler row in the status table contains the STATUS_FAILURE value.</span></span> 
    
- <span data-ttu-id="ea902-193">Logons sem retorno são permitidos, mas esses logons não fazem com que o logon anterior receba atualizações de objeto de status.</span><span class="sxs-lookup"><span data-stu-id="ea902-193">Piggybacked logons are allowed, but those logons do not cause the previous logon to receive status object updates.</span></span> 
    
<span data-ttu-id="ea902-194">Um serviço deve sempre fazer logoff usando o sinalizador MAPI_NO_MAIL linha.</span><span class="sxs-lookup"><span data-stu-id="ea902-194">A service should always log on using the MAPI_NO_MAIL flag.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ea902-195">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ea902-195">MFCMAPI reference</span></span>

<span data-ttu-id="ea902-196">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ea902-196">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ea902-197">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="ea902-197">**File**</span></span>|<span data-ttu-id="ea902-198">**Função**</span><span class="sxs-lookup"><span data-stu-id="ea902-198">**Function**</span></span>|<span data-ttu-id="ea902-199">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="ea902-199">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ea902-200">MAPIObjects.cpp</span><span class="sxs-lookup"><span data-stu-id="ea902-200">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="ea902-201">CMapiObjects::MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="ea902-201">CMapiObjects::MAPILogonEx</span></span>  <br/> |<span data-ttu-id="ea902-202">MFCMAPI usa o método MAPILogonEx para fazer logoff no MAPI.</span><span class="sxs-lookup"><span data-stu-id="ea902-202">MFCMAPI uses the MAPILogonEx method to log on to MAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ea902-203">Confira também</span><span class="sxs-lookup"><span data-stu-id="ea902-203">See also</span></span>



[<span data-ttu-id="ea902-204">IMAPISession::GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="ea902-204">IMAPISession::GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md)
  
[<span data-ttu-id="ea902-205">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="ea902-205">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)


[<span data-ttu-id="ea902-206">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="ea902-206">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

