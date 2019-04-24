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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346645"
---
# <a name="mapilogonex"></a><span data-ttu-id="5f28d-103">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="5f28d-103">MAPILogonEx</span></span>

  
  
<span data-ttu-id="5f28d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5f28d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5f28d-105">Registra um aplicativo cliente em uma sessão com o sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="5f28d-105">Logs a client application on to a session with the messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5f28d-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="5f28d-106">Header file:</span></span>  <br/> |<span data-ttu-id="5f28d-107">Mapix. h</span><span class="sxs-lookup"><span data-stu-id="5f28d-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="5f28d-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="5f28d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="5f28d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="5f28d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="5f28d-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="5f28d-110">Called by:</span></span>  <br/> |<span data-ttu-id="5f28d-111">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="5f28d-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT MAPILogonEx(
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  FLAGS flFlags,
  LPMAPISESSION FAR * lppSession
);
```

## <a name="parameters"></a><span data-ttu-id="5f28d-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5f28d-112">Parameters</span></span>

 <span data-ttu-id="5f28d-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="5f28d-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="5f28d-114">no Manipulador para a janela à qual a caixa de diálogo de logon é modal.</span><span class="sxs-lookup"><span data-stu-id="5f28d-114">[in] Handle to the window to which the logon dialog box is modal.</span></span> <span data-ttu-id="5f28d-115">Se nenhuma caixa de diálogo for exibida durante a chamada, o parâmetro _ulUIParam_ será ignorado.</span><span class="sxs-lookup"><span data-stu-id="5f28d-115">If no dialog box appears during the call, the  _ulUIParam_ parameter is ignored.</span></span> <span data-ttu-id="5f28d-116">Esse parâmetro pode ser zero.</span><span class="sxs-lookup"><span data-stu-id="5f28d-116">This parameter can be zero.</span></span> 
    
 <span data-ttu-id="5f28d-117">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="5f28d-117">_lpszProfileName_</span></span>
  
> <span data-ttu-id="5f28d-118">no Ponteiro para uma cadeia de caracteres que contém o nome do perfil a ser usado quando o usuário faz logon.</span><span class="sxs-lookup"><span data-stu-id="5f28d-118">[in] Pointer to a string that contains the name of the profile to use when the user logs on.</span></span> <span data-ttu-id="5f28d-119">Esta cadeia de caracteres é limitada a 64 caracteres.</span><span class="sxs-lookup"><span data-stu-id="5f28d-119">This string is limited to 64 characters.</span></span>
    
 <span data-ttu-id="5f28d-120">_lpszPassword_</span><span class="sxs-lookup"><span data-stu-id="5f28d-120">_lpszPassword_</span></span>
  
> <span data-ttu-id="5f28d-121">no Ponteiro para uma cadeia de caracteres que contém a senha do perfil.</span><span class="sxs-lookup"><span data-stu-id="5f28d-121">[in] Pointer to a string that contains the password of the profile.</span></span> <span data-ttu-id="5f28d-122">O parâmetro _lpszPassword_ deve ser nulo.</span><span class="sxs-lookup"><span data-stu-id="5f28d-122">The  _lpszPassword_ parameter must be NULL.</span></span> 
    
 <span data-ttu-id="5f28d-123">_Parâmetroflflags_</span><span class="sxs-lookup"><span data-stu-id="5f28d-123">_flFlags_</span></span>
  
> <span data-ttu-id="5f28d-124">no Bitmask dos sinalizadores usados para controlar como o logon é executado.</span><span class="sxs-lookup"><span data-stu-id="5f28d-124">[in] Bitmask of flags used to control how logon is performed.</span></span> <span data-ttu-id="5f28d-125">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="5f28d-125">The following flags can be set:</span></span>
    
<span data-ttu-id="5f28d-126">MAPI_ALLOW_OTHERS</span><span class="sxs-lookup"><span data-stu-id="5f28d-126">MAPI_ALLOW_OTHERS</span></span> 
  
> <span data-ttu-id="5f28d-127">A sessão compartilhada deve ser retornada, permitindo que os clientes posteriores obtenham a sessão sem fornecer nenhuma credencial de usuário.</span><span class="sxs-lookup"><span data-stu-id="5f28d-127">The shared session should be returned, which allows later clients to obtain the session without providing any user credentials.</span></span> 
    
<span data-ttu-id="5f28d-128">MAPI_BG_SESSION</span><span class="sxs-lookup"><span data-stu-id="5f28d-128">MAPI_BG_SESSION</span></span>
  
> <span data-ttu-id="5f28d-129">Faça logon em uma sessão e execute qualquer operação em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="5f28d-129">Log on to a session and run any operations in the background.</span></span> <span data-ttu-id="5f28d-130">Em geral, se um cliente pretende fazer o processamento em um thread de segundo plano ou em um processo separado de uma maneira que não é invasiva para o thread de primeiro plano, ele deve chamar com o sinalizador MAPI_BG_SESSION.</span><span class="sxs-lookup"><span data-stu-id="5f28d-130">In general, if a client intends to do processing on a background thread or in a separate process in a manner that is unobtrusive to the foreground thread, it should call with the MAPI_BG_SESSION flag.</span></span> <span data-ttu-id="5f28d-131">Um aplicativo cliente, como um mecanismo de indexação ou a abertura de um arquivo de pastas particulares (PST) para acesso de tipo de plano de fundo, são alguns exemplos de onde usar o MAPI_BG_SESSION. Funçãomapilogonex.</span><span class="sxs-lookup"><span data-stu-id="5f28d-131">A client application such as an indexing engine or opening a Personal Folders File (PST) for background type access are some examples of where to use MAPI_BG_SESSION.MAPILogonEx.</span></span>
    
<span data-ttu-id="5f28d-132">MAPI_EXPLICIT_PROFILE</span><span class="sxs-lookup"><span data-stu-id="5f28d-132">MAPI_EXPLICIT_PROFILE</span></span> 
  
> <span data-ttu-id="5f28d-133">O perfil padrão não deve ser usado e o usuário deve ser solicitado a fornecer um perfil.</span><span class="sxs-lookup"><span data-stu-id="5f28d-133">The default profile should not be used and the user should be required to supply a profile.</span></span> 
    
<span data-ttu-id="5f28d-134">MAPI_EXTENDED</span><span class="sxs-lookup"><span data-stu-id="5f28d-134">MAPI_EXTENDED</span></span> 
  
> <span data-ttu-id="5f28d-135">Faça logon com recursos estendidos.</span><span class="sxs-lookup"><span data-stu-id="5f28d-135">Log on with extended capabilities.</span></span> <span data-ttu-id="5f28d-136">Esse sinalizador deve sempre ser definido.</span><span class="sxs-lookup"><span data-stu-id="5f28d-136">This flag should always be set.</span></span>
    
<span data-ttu-id="5f28d-137">MAPI_FORCE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="5f28d-137">MAPI_FORCE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="5f28d-138">Uma tentativa deve ser feita para baixar todas as mensagens do usuário antes de retornar.</span><span class="sxs-lookup"><span data-stu-id="5f28d-138">An attempt should be made to download all of the user's messages before returning.</span></span> <span data-ttu-id="5f28d-139">Se o sinalizador MAPI_FORCE_DOWNLOAD não estiver definido, as mensagens poderão ser baixadas em segundo plano depois que a chamada para Funçãomapilogonex retornar.</span><span class="sxs-lookup"><span data-stu-id="5f28d-139">If the MAPI_FORCE_DOWNLOAD flag is not set, messages can be downloaded in the background after the call to MAPILogonEx returns.</span></span> 
    
<span data-ttu-id="5f28d-140">MAPI_LOGON_UI</span><span class="sxs-lookup"><span data-stu-id="5f28d-140">MAPI_LOGON_UI</span></span> 
  
> <span data-ttu-id="5f28d-141">Uma caixa de diálogo deve ser exibida para solicitar ao usuário as informações de logon, se necessário.</span><span class="sxs-lookup"><span data-stu-id="5f28d-141">A dialog box should be displayed to prompt the user for logon information if required.</span></span> <span data-ttu-id="5f28d-142">Quando o sinalizador MAPI_LOGON_UI não estiver definido, o cliente de chamada não exibirá uma caixa de diálogo de logon e retornará um valor de erro se o usuário não estiver conectado.</span><span class="sxs-lookup"><span data-stu-id="5f28d-142">When the MAPI_LOGON_UI flag is not set, the calling client does not display a logon dialog box and returns an error value if the user is not logged on.</span></span>
    
<span data-ttu-id="5f28d-143">MAPI_NEW_SESSION</span><span class="sxs-lookup"><span data-stu-id="5f28d-143">MAPI_NEW_SESSION</span></span> 
  
> <span data-ttu-id="5f28d-144">Uma tentativa deve ser feita para criar uma nova sessão MAPI em vez de adquirir a sessão compartilhada.</span><span class="sxs-lookup"><span data-stu-id="5f28d-144">An attempt should be made to create a new MAPI session instead of acquiring the shared session.</span></span> <span data-ttu-id="5f28d-145">Se o sinalizador MAPI_NEW_SESSION não estiver definido, o Funçãomapilogonex usará uma sessão compartilhada existente, mesmo que o parâmetro _lpszprofileName_ não seja nulo.</span><span class="sxs-lookup"><span data-stu-id="5f28d-145">If the MAPI_NEW_SESSION flag is not set, MAPILogonEx uses an existing shared session even if the  _lpszprofileName_ parameter is not NULL.</span></span> 
    
<span data-ttu-id="5f28d-146">MAPI_NO_MAIL</span><span class="sxs-lookup"><span data-stu-id="5f28d-146">MAPI_NO_MAIL</span></span> 
  
> <span data-ttu-id="5f28d-147">O MAPI não deve informar o spooler MAPI da existência da sessão.</span><span class="sxs-lookup"><span data-stu-id="5f28d-147">MAPI should not inform the MAPI spooler of the session's existence.</span></span> <span data-ttu-id="5f28d-148">O resultado é que nenhuma mensagem pode ser enviada ou recebida na sessão, exceto por meio de um par de transporte e transporte rigidamente acoplado.</span><span class="sxs-lookup"><span data-stu-id="5f28d-148">The result is that no messages can be sent or received in the session except through a tightly coupled store and transport pair.</span></span> <span data-ttu-id="5f28d-149">Um cliente de chamada define esse sinalizador se ele estiver atuando como um agente, se o trabalho de configuração tiver de ser feito ou se o cliente estiver pesquisando os repositórios de mensagens disponíveis.</span><span class="sxs-lookup"><span data-stu-id="5f28d-149">A calling client sets this flag if it is acting as an agent, if configuration work must be done, or if the client is browsing the available message stores.</span></span> 
    
<span data-ttu-id="5f28d-150">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="5f28d-150">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="5f28d-151">O chamador está sendo executado como um serviço do Windows.</span><span class="sxs-lookup"><span data-stu-id="5f28d-151">The caller is running as a Windows service.</span></span> <span data-ttu-id="5f28d-152">Os chamadores que não estão sendo executados como um serviço do Windows não devem definir esse sinalizador; os chamadores que estão executando como um serviço devem definir esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="5f28d-152">Callers that are not running as a Windows service should not set this flag; callers that are running as a service must set this flag.</span></span> 
    
<span data-ttu-id="5f28d-153">MAPI_SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="5f28d-153">MAPI_SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="5f28d-154">Funçãomapilogonex deve exibir uma caixa de diálogo de configuração para cada serviço de mensagens no perfil.</span><span class="sxs-lookup"><span data-stu-id="5f28d-154">MAPILogonEx should display a configuration dialog box for each message service in the profile.</span></span> <span data-ttu-id="5f28d-155">As caixas de diálogo são exibidas após o perfil ter sido escolhido, mas antes de qualquer serviço de mensagem estar conectado.</span><span class="sxs-lookup"><span data-stu-id="5f28d-155">The dialog boxes are displayed after the profile has been chosen but before any message service is logged on.</span></span> <span data-ttu-id="5f28d-156">A caixa de diálogo comum de MAPI para logon também contém uma caixa de seleção que solicita a mesma operação.</span><span class="sxs-lookup"><span data-stu-id="5f28d-156">The MAPI common dialog box for logon also contains a check box that requests the same operation.</span></span> 
    
<span data-ttu-id="5f28d-157">MAPI_TIMEOUT_SHORT</span><span class="sxs-lookup"><span data-stu-id="5f28d-157">MAPI_TIMEOUT_SHORT</span></span> 
  
> <span data-ttu-id="5f28d-158">O logon deve falhar se bloqueado por mais de alguns segundos.</span><span class="sxs-lookup"><span data-stu-id="5f28d-158">The logon should fail if blocked for more than a few seconds.</span></span> 
    
<span data-ttu-id="5f28d-159">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5f28d-159">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="5f28d-160">As cadeias de caracteres passadas estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="5f28d-160">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="5f28d-161">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="5f28d-161">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
<span data-ttu-id="5f28d-162">MAPI_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="5f28d-162">MAPI_USE_DEFAULT</span></span> 
  
> <span data-ttu-id="5f28d-163">O subsistema de mensagens deve substituir o nome do perfil do perfil padrão para o parâmetro _lpszProfileName_ .</span><span class="sxs-lookup"><span data-stu-id="5f28d-163">The messaging subsystem should substitute the profile name of the default profile for the  _lpszProfileName_ parameter.</span></span> <span data-ttu-id="5f28d-164">O sinalizador MAPI_EXPLICIT_PROFILE é ignorado, a menos que _lpszProfileName_ seja nulo ou vazio.</span><span class="sxs-lookup"><span data-stu-id="5f28d-164">The MAPI_EXPLICIT_PROFILE flag is ignored unless  _lpszProfileName_ is NULL or empty.</span></span> 
    
 <span data-ttu-id="5f28d-165">_lppSession_</span><span class="sxs-lookup"><span data-stu-id="5f28d-165">_lppSession_</span></span>
  
> <span data-ttu-id="5f28d-166">bota Ponteiro para um ponteiro para a interface de sessão MAPI.</span><span class="sxs-lookup"><span data-stu-id="5f28d-166">[out] Pointer to a pointer to the MAPI session interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5f28d-167">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="5f28d-167">Return value</span></span>

<span data-ttu-id="5f28d-168">S_OK</span><span class="sxs-lookup"><span data-stu-id="5f28d-168">S_OK</span></span> 
  
> <span data-ttu-id="5f28d-169">O logon foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="5f28d-169">The logon succeeded.</span></span>
    
<span data-ttu-id="5f28d-170">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="5f28d-170">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="5f28d-171">O logon não foi bem-sucedido, porque um ou mais parâmetros para Funçãomapilogonex eram inválidos ou porque já havia muitas sessões abertas.</span><span class="sxs-lookup"><span data-stu-id="5f28d-171">The logon was unsuccessful, either because one or more of the parameters to MAPILogonEx were invalid or because there were too many sessions open already.</span></span>
    
<span data-ttu-id="5f28d-172">MAPI_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="5f28d-172">MAPI_E_TIMEOUT</span></span> 
  
> <span data-ttu-id="5f28d-173">O MAPI serializa todos os logons por meio de um mutex.</span><span class="sxs-lookup"><span data-stu-id="5f28d-173">MAPI serializes all logons through a mutex.</span></span> <span data-ttu-id="5f28d-174">Isso será retornado se o sinalizador MAPI_TIMEOUT_SHORT tiver sido definido e outro thread tiver mantido o mutex.</span><span class="sxs-lookup"><span data-stu-id="5f28d-174">This is returned if the MAPI_TIMEOUT_SHORT flag was set and another thread held the mutex.</span></span> 
    
<span data-ttu-id="5f28d-175">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="5f28d-175">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="5f28d-176">O usuário cancelou a operação, geralmente clicando no botão **Cancelar** em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="5f28d-176">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5f28d-177">Comentários</span><span class="sxs-lookup"><span data-stu-id="5f28d-177">Remarks</span></span>

<span data-ttu-id="5f28d-178">Os aplicativos cliente MAPI chamam a função Funçãomapilogonex para fazer logon em uma sessão com o sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="5f28d-178">MAPI client applications call the MAPILogonEx function to log on to a session with the messaging system.</span></span> <span data-ttu-id="5f28d-179">Todas as cadeias de caracteres que são passadas e retornadas para e de chamadas MAPI são terminadas em nulo e devem ser especificadas no conjunto de caracteres atual ou na página de códigos do sistema operacional do cliente ou provedor de chamadas.</span><span class="sxs-lookup"><span data-stu-id="5f28d-179">All strings that are passed in and returned to and from MAPI calls are null-terminated and must be specified in the current character set or code page of the calling client or provider's operating system.</span></span>
  
<span data-ttu-id="5f28d-180">O parâmetro _lpszProfileName_ será ignorado se houver uma sessão anterior existente que chamou funçãomapilogonex com o sinalizador MAPI_ALLOW_OTHERS definido e se o sinalizador MAPI_NEW_SESSION não estiver definido.</span><span class="sxs-lookup"><span data-stu-id="5f28d-180">The  _lpszProfileName_ parameter is ignored if there is an existing previous session that called MapiLogonEx with the MAPI_ALLOW_OTHERS flag set and if the flag MAPI_NEW_SESSION is not set.</span></span> <span data-ttu-id="5f28d-181">Se o parâmetro _lpszProfileName_ for NULL ou apontar para uma cadeia de caracteres vazia, e o parâmetro _parâmetroflflags_ incluir o sinalizador MAPI_LOGON_UI, a função funçãomapilogonex gerará uma caixa de diálogo de logon que tem um campo vazio para o nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="5f28d-181">If the  _lpszProfileName_ parameter is NULL or points to an empty string, and the  _flFlags_ parameter includes the MAPI_LOGON_UI flag, the MAPILogonEx function generates a logon dialog box that has an empty field for the profile name.</span></span> 
  
<span data-ttu-id="5f28d-182">Ao fazer logon em um perfil específico, um cliente deve passar o sinalizador MAPI_NEW_SESSION para o Funçãomapilogonex, além do nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="5f28d-182">When logging on to a specific profile, a client should pass the MAPI_NEW_SESSION flag into MAPILogonEx in addition to the profile name.</span></span> <span data-ttu-id="5f28d-183">Caso contrário, se outro cliente tiver estabelecido uma sessão compartilhada fazendo logon com o MAPI_ALLOW_OTHERS, o cliente será conectado à sessão compartilhada em vez de ao perfil solicitado.</span><span class="sxs-lookup"><span data-stu-id="5f28d-183">Otherwise, if another client has established a shared session by logging on with MAPI_ALLOW_OTHERS, the client will be logged on to the shared session instead of to the profile requested.</span></span> 
  
<span data-ttu-id="5f28d-184">O sinalizador MAPI_EXPLICIT_PROFILE não faz com que o nome do perfil padrão seja usado quando _lpszProfileName_ é nulo ou vazio, a menos que o sinalizador MAPI_USE_DEFAULT também esteja presente.</span><span class="sxs-lookup"><span data-stu-id="5f28d-184">The MAPI_EXPLICIT_PROFILE flag does not cause the default profile name to be used when  _lpszProfileName_ is NULL or empty unless the MAPI_USE_DEFAULT flag is also present.</span></span> 
  
<span data-ttu-id="5f28d-185">O sinalizador MAPI_NO_MAIL tem vários efeitos que causam o seguinte quando não usam o MAPI spooler:</span><span class="sxs-lookup"><span data-stu-id="5f28d-185">The MAPI_NO_MAIL flag has several effects that cause the following when not using the MAPI spooler:</span></span>
  
- <span data-ttu-id="5f28d-186">Nenhuma mensagem pode ser enviada ou entregue pelo spooler MAPI durante esta sessão.</span><span class="sxs-lookup"><span data-stu-id="5f28d-186">No messages can be sent or delivered by the MAPI spooler during this session.</span></span> <span data-ttu-id="5f28d-187">Somente provedores de armazenamento e transporte rigidamente acoplados podem enviar e entregar mensagens.</span><span class="sxs-lookup"><span data-stu-id="5f28d-187">Only tightly coupled store and transport providers can send and deliver messages.</span></span> 
    
- <span data-ttu-id="5f28d-188">Os repositórios baseados em servidor ainda podem enviar ou entregar mensagens.</span><span class="sxs-lookup"><span data-stu-id="5f28d-188">Server based stores might still send or deliver messages.</span></span> 
    
- <span data-ttu-id="5f28d-189">As mensagens enviadas ou entregues por repositórios baseados em servidor não são processadas por provedores de conexão.</span><span class="sxs-lookup"><span data-stu-id="5f28d-189">Messages sent or delivered by server based stores are not processed by any hook providers.</span></span> 
    
- <span data-ttu-id="5f28d-190">As opções por mensagem e por destinatário para transportes não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="5f28d-190">Per-message and per-recipient options for transports are not available.</span></span> 
    
- <span data-ttu-id="5f28d-191">A tabela de status não contém entradas para provedores de transporte e qualquer funcionalidade de transporte dependente de objetos de status (como configuração) não está disponível.</span><span class="sxs-lookup"><span data-stu-id="5f28d-191">The status table does not contain entries for transport providers, and any transport functionality dependent on status objects (such as configuration) is not available.</span></span> 
    
- <span data-ttu-id="5f28d-192">A linha de spooler de mensagem na tabela status contém o valor STATUS_FAILURE.</span><span class="sxs-lookup"><span data-stu-id="5f28d-192">The message spooler row in the status table contains the STATUS_FAILURE value.</span></span> 
    
- <span data-ttu-id="5f28d-193">Os logons acumulados são permitidos, mas esses logons não fazem o logon anterior receber atualizações de objetos de status.</span><span class="sxs-lookup"><span data-stu-id="5f28d-193">Piggybacked logons are allowed, but those logons do not cause the previous logon to receive status object updates.</span></span> 
    
<span data-ttu-id="5f28d-194">Um serviço deve sempre fazer logon usando o sinalizador MAPI_NO_MAIL.</span><span class="sxs-lookup"><span data-stu-id="5f28d-194">A service should always log on using the MAPI_NO_MAIL flag.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5f28d-195">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="5f28d-195">MFCMAPI reference</span></span>

<span data-ttu-id="5f28d-196">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="5f28d-196">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5f28d-197">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="5f28d-197">**File**</span></span>|<span data-ttu-id="5f28d-198">**Função**</span><span class="sxs-lookup"><span data-stu-id="5f28d-198">**Function**</span></span>|<span data-ttu-id="5f28d-199">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="5f28d-199">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5f28d-200">MAPIObjects. cpp</span><span class="sxs-lookup"><span data-stu-id="5f28d-200">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="5f28d-201">CMapiObjects:: Funçãomapilogonex</span><span class="sxs-lookup"><span data-stu-id="5f28d-201">CMapiObjects::MAPILogonEx</span></span>  <br/> |<span data-ttu-id="5f28d-202">MFCMAPI usa o método Funçãomapilogonex para fazer logon no MAPI.</span><span class="sxs-lookup"><span data-stu-id="5f28d-202">MFCMAPI uses the MAPILogonEx method to log on to MAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5f28d-203">Confira também</span><span class="sxs-lookup"><span data-stu-id="5f28d-203">See also</span></span>



[<span data-ttu-id="5f28d-204">IMAPISession::GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="5f28d-204">IMAPISession::GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md)
  
[<span data-ttu-id="5f28d-205">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="5f28d-205">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)


[<span data-ttu-id="5f28d-206">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="5f28d-206">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

