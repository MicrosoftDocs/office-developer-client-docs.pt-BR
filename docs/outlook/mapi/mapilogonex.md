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
ms.openlocfilehash: db76dfec27100a22785082580da70ecc2c10fc45
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579981"
---
# <a name="mapilogonex"></a><span data-ttu-id="f5823-103">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="f5823-103">MAPILogonEx</span></span>

  
  
<span data-ttu-id="f5823-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f5823-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f5823-105">Logs de um aplicativo cliente em uma sessão com o sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="f5823-105">Logs a client application on to a session with the messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f5823-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="f5823-106">Header file:</span></span>  <br/> |<span data-ttu-id="f5823-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="f5823-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="f5823-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="f5823-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f5823-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f5823-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f5823-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="f5823-110">Called by:</span></span>  <br/> |<span data-ttu-id="f5823-111">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="f5823-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT MAPILogonEx(
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  FLAGS flFlags,
  LPMAPISESSION FAR * lppSession
);
```

## <a name="parameters"></a><span data-ttu-id="f5823-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f5823-112">Parameters</span></span>

 <span data-ttu-id="f5823-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="f5823-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="f5823-114">[in] Identificador para a janela para o qual a caixa de diálogo de logon é modal.</span><span class="sxs-lookup"><span data-stu-id="f5823-114">[in] Handle to the window to which the logon dialog box is modal.</span></span> <span data-ttu-id="f5823-115">Se nenhuma caixa de diálogo aparece durante a chamada, o parâmetro _ulUIParam_ será ignorado.</span><span class="sxs-lookup"><span data-stu-id="f5823-115">If no dialog box appears during the call, the  _ulUIParam_ parameter is ignored.</span></span> <span data-ttu-id="f5823-116">Esse parâmetro pode ser zero.</span><span class="sxs-lookup"><span data-stu-id="f5823-116">This parameter can be zero.</span></span> 
    
 <span data-ttu-id="f5823-117">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="f5823-117">_lpszProfileName_</span></span>
  
> <span data-ttu-id="f5823-118">[in] Ponteiro para uma cadeia de caracteres que contém o nome do perfil para usar quando o usuário fizer logon.</span><span class="sxs-lookup"><span data-stu-id="f5823-118">[in] Pointer to a string that contains the name of the profile to use when the user logs on.</span></span> <span data-ttu-id="f5823-119">Esta cadeia de caracteres é limitada a 64 caracteres.</span><span class="sxs-lookup"><span data-stu-id="f5823-119">This string is limited to 64 characters.</span></span>
    
 <span data-ttu-id="f5823-120">_lpszPassword_</span><span class="sxs-lookup"><span data-stu-id="f5823-120">_lpszPassword_</span></span>
  
> <span data-ttu-id="f5823-121">[in] Ponteiro para uma cadeia de caracteres que contém a senha do perfil.</span><span class="sxs-lookup"><span data-stu-id="f5823-121">[in] Pointer to a string that contains the password of the profile.</span></span> <span data-ttu-id="f5823-122">O parâmetro _lpszPassword_ deve ser NULL.</span><span class="sxs-lookup"><span data-stu-id="f5823-122">The  _lpszPassword_ parameter must be NULL.</span></span> 
    
 <span data-ttu-id="f5823-123">_flFlags_</span><span class="sxs-lookup"><span data-stu-id="f5823-123">_flFlags_</span></span>
  
> <span data-ttu-id="f5823-124">[in] Bitmask dos sinalizadores usadas para controlar como o logon é executada.</span><span class="sxs-lookup"><span data-stu-id="f5823-124">[in] Bitmask of flags used to control how logon is performed.</span></span> <span data-ttu-id="f5823-125">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="f5823-125">The following flags can be set:</span></span>
    
<span data-ttu-id="f5823-126">MAPI_ALLOW_OTHERS</span><span class="sxs-lookup"><span data-stu-id="f5823-126">MAPI_ALLOW_OTHERS</span></span> 
  
> <span data-ttu-id="f5823-127">A sessão compartilhada deve ser retornada, que permite que os clientes posteriores obtenham a sessão sem fornecer as credenciais de usuário.</span><span class="sxs-lookup"><span data-stu-id="f5823-127">The shared session should be returned, which allows later clients to obtain the session without providing any user credentials.</span></span> 
    
<span data-ttu-id="f5823-128">MAPI_BG_SESSION</span><span class="sxs-lookup"><span data-stu-id="f5823-128">MAPI_BG_SESSION</span></span>
  
> <span data-ttu-id="f5823-129">Fazer logon em uma sessão e executar todas as operações em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="f5823-129">Log on to a session and run any operations in the background.</span></span> <span data-ttu-id="f5823-130">Em geral, se um cliente pretende fazer processamento em um segmento de plano de fundo ou em um processo separado no modo não invasiva para o segmento de primeiro plano, ele deve chamar com o sinalizador MAPI_BG_SESSION.</span><span class="sxs-lookup"><span data-stu-id="f5823-130">In general, if a client intends to do processing on a background thread or in a separate process in a manner that is unobtrusive to the foreground thread, it should call with the MAPI_BG_SESSION flag.</span></span> <span data-ttu-id="f5823-131">Um aplicativo cliente como um mecanismo de indexação ou abrir um arquivo de pastas particulares (PST) para acesso de tipo de plano de fundo são alguns exemplos de onde usar MAPI_BG_SESSION. MAPILogonEx.</span><span class="sxs-lookup"><span data-stu-id="f5823-131">A client application such as an indexing engine or opening a Personal Folders File (PST) for background type access are some examples of where to use MAPI_BG_SESSION.MAPILogonEx.</span></span>
    
<span data-ttu-id="f5823-132">MAPI_EXPLICIT_PROFILE</span><span class="sxs-lookup"><span data-stu-id="f5823-132">MAPI_EXPLICIT_PROFILE</span></span> 
  
> <span data-ttu-id="f5823-133">O perfil padrão não deve ser usado e o usuário deve ser solicitado a fornecer um perfil.</span><span class="sxs-lookup"><span data-stu-id="f5823-133">The default profile should not be used and the user should be required to supply a profile.</span></span> 
    
<span data-ttu-id="f5823-134">MAPI_EXTENDED</span><span class="sxs-lookup"><span data-stu-id="f5823-134">MAPI_EXTENDED</span></span> 
  
> <span data-ttu-id="f5823-135">Faça logon com recursos estendidos.</span><span class="sxs-lookup"><span data-stu-id="f5823-135">Log on with extended capabilities.</span></span> <span data-ttu-id="f5823-136">Esse sinalizador deve sempre ser definido.</span><span class="sxs-lookup"><span data-stu-id="f5823-136">This flag should always be set.</span></span>
    
<span data-ttu-id="f5823-137">MAPI_FORCE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="f5823-137">MAPI_FORCE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="f5823-138">Deve ser feita uma tentativa para baixar todas as mensagens do usuário antes de retornar.</span><span class="sxs-lookup"><span data-stu-id="f5823-138">An attempt should be made to download all of the user's messages before returning.</span></span> <span data-ttu-id="f5823-139">Se o sinalizador MAPI_FORCE_DOWNLOAD não estiver definido, as mensagens podem ser baixadas em segundo plano após a chamada para MAPILogonEx retorna.</span><span class="sxs-lookup"><span data-stu-id="f5823-139">If the MAPI_FORCE_DOWNLOAD flag is not set, messages can be downloaded in the background after the call to MAPILogonEx returns.</span></span> 
    
<span data-ttu-id="f5823-140">MAPI_LOGON_UI</span><span class="sxs-lookup"><span data-stu-id="f5823-140">MAPI_LOGON_UI</span></span> 
  
> <span data-ttu-id="f5823-141">Uma caixa de diálogo deve ser exibida para solicitar informações de logon do usuário, se necessário.</span><span class="sxs-lookup"><span data-stu-id="f5823-141">A dialog box should be displayed to prompt the user for logon information if required.</span></span> <span data-ttu-id="f5823-142">Quando o sinalizador MAPI_LOGON_UI não estiver definido, o cliente da chamada não exibe uma caixa de diálogo de logon e retorna um valor de erro se o usuário não está conectado.</span><span class="sxs-lookup"><span data-stu-id="f5823-142">When the MAPI_LOGON_UI flag is not set, the calling client does not display a logon dialog box and returns an error value if the user is not logged on.</span></span>
    
<span data-ttu-id="f5823-143">MAPI_NEW_SESSION</span><span class="sxs-lookup"><span data-stu-id="f5823-143">MAPI_NEW_SESSION</span></span> 
  
> <span data-ttu-id="f5823-144">Deve ser feita uma tentativa para criar uma nova sessão MAPI, em vez de adquirir a sessão compartilhada.</span><span class="sxs-lookup"><span data-stu-id="f5823-144">An attempt should be made to create a new MAPI session instead of acquiring the shared session.</span></span> <span data-ttu-id="f5823-145">Se o sinalizador MAPI_NEW_SESSION não estiver definido, MAPILogonEx usa uma sessão compartilhada existente, mesmo se o parâmetro _lpszprofileName_ não for nulo.</span><span class="sxs-lookup"><span data-stu-id="f5823-145">If the MAPI_NEW_SESSION flag is not set, MAPILogonEx uses an existing shared session even if the  _lpszprofileName_ parameter is not NULL.</span></span> 
    
<span data-ttu-id="f5823-146">MAPI_NO_MAIL</span><span class="sxs-lookup"><span data-stu-id="f5823-146">MAPI_NO_MAIL</span></span> 
  
> <span data-ttu-id="f5823-147">MAPI não deve informar o spooler de MAPI de existência da sessão.</span><span class="sxs-lookup"><span data-stu-id="f5823-147">MAPI should not inform the MAPI spooler of the session's existence.</span></span> <span data-ttu-id="f5823-148">O resultado é que nenhuma mensagem pode ser enviada ou recebida na sessão, exceto por meio de uma ligação estreita armazenar e par de transporte.</span><span class="sxs-lookup"><span data-stu-id="f5823-148">The result is that no messages can be sent or received in the session except through a tightly coupled store and transport pair.</span></span> <span data-ttu-id="f5823-149">Um cliente da chamada define esse sinalizador se ele está agindo como um operador, se o trabalho de configuração deve ser feito, ou se o cliente estiver navegando os repositórios de mensagem disponíveis.</span><span class="sxs-lookup"><span data-stu-id="f5823-149">A calling client sets this flag if it is acting as an agent, if configuration work must be done, or if the client is browsing the available message stores.</span></span> 
    
<span data-ttu-id="f5823-150">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="f5823-150">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="f5823-151">O chamador está sendo executado como um serviço do Windows.</span><span class="sxs-lookup"><span data-stu-id="f5823-151">The caller is running as a Windows service.</span></span> <span data-ttu-id="f5823-152">Chamadores que não estejam executando um serviço do Windows não deve definir esse sinalizador; os chamadores que estão sendo executados como um serviço devem definir esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="f5823-152">Callers that are not running as a Windows service should not set this flag; callers that are running as a service must set this flag.</span></span> 
    
<span data-ttu-id="f5823-153">MAPI_SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="f5823-153">MAPI_SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="f5823-154">MAPILogonEx deve exibir uma caixa de diálogo de configuração para cada serviço de mensagem no perfil.</span><span class="sxs-lookup"><span data-stu-id="f5823-154">MAPILogonEx should display a configuration dialog box for each message service in the profile.</span></span> <span data-ttu-id="f5823-155">As caixas de diálogo são exibidas depois que o perfil foi escolhido, mas antes de qualquer mensagem de serviço está conectado.</span><span class="sxs-lookup"><span data-stu-id="f5823-155">The dialog boxes are displayed after the profile has been chosen but before any message service is logged on.</span></span> <span data-ttu-id="f5823-156">A caixa de diálogo comuns de MAPI para logon também contém uma caixa de seleção que solicita a mesma operação.</span><span class="sxs-lookup"><span data-stu-id="f5823-156">The MAPI common dialog box for logon also contains a check box that requests the same operation.</span></span> 
    
<span data-ttu-id="f5823-157">MAPI_TIMEOUT_SHORT</span><span class="sxs-lookup"><span data-stu-id="f5823-157">MAPI_TIMEOUT_SHORT</span></span> 
  
> <span data-ttu-id="f5823-158">Fazer logon deve falhar se bloqueado por mais de alguns segundos.</span><span class="sxs-lookup"><span data-stu-id="f5823-158">The logon should fail if blocked for more than a few seconds.</span></span> 
    
<span data-ttu-id="f5823-159">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f5823-159">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="f5823-160">As cadeias de caracteres passada na estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="f5823-160">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="f5823-161">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="f5823-161">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
<span data-ttu-id="f5823-162">MAPI_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="f5823-162">MAPI_USE_DEFAULT</span></span> 
  
> <span data-ttu-id="f5823-163">O subsistema de mensagens deve substituir o nome do perfil do perfil padrão para o parâmetro _lpszProfileName_ .</span><span class="sxs-lookup"><span data-stu-id="f5823-163">The messaging subsystem should substitute the profile name of the default profile for the  _lpszProfileName_ parameter.</span></span> <span data-ttu-id="f5823-164">O sinalizador MAPI_EXPLICIT_PROFILE será ignorado, a menos que _lpszProfileName_ é nulo ou vazio.</span><span class="sxs-lookup"><span data-stu-id="f5823-164">The MAPI_EXPLICIT_PROFILE flag is ignored unless  _lpszProfileName_ is NULL or empty.</span></span> 
    
 <span data-ttu-id="f5823-165">_lppSession_</span><span class="sxs-lookup"><span data-stu-id="f5823-165">_lppSession_</span></span>
  
> <span data-ttu-id="f5823-166">[out] Ponteiro para um ponteiro para a interface de sessão MAPI.</span><span class="sxs-lookup"><span data-stu-id="f5823-166">[out] Pointer to a pointer to the MAPI session interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f5823-167">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="f5823-167">Return value</span></span>

<span data-ttu-id="f5823-168">S_OK</span><span class="sxs-lookup"><span data-stu-id="f5823-168">S_OK</span></span> 
  
> <span data-ttu-id="f5823-169">O logon bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="f5823-169">The logon succeeded.</span></span>
    
<span data-ttu-id="f5823-170">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="f5823-170">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="f5823-171">O logon foi bem sucedido, porque um ou mais dos parâmetros para MAPILogonEx eram inválidos ou porque havia muitas sessões abertas já.</span><span class="sxs-lookup"><span data-stu-id="f5823-171">The logon was unsuccessful, either because one or more of the parameters to MAPILogonEx were invalid or because there were too many sessions open already.</span></span>
    
<span data-ttu-id="f5823-172">MAPI_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="f5823-172">MAPI_E_TIMEOUT</span></span> 
  
> <span data-ttu-id="f5823-173">MAPI serializa todos os logons por meio de um mutex.</span><span class="sxs-lookup"><span data-stu-id="f5823-173">MAPI serializes all logons through a mutex.</span></span> <span data-ttu-id="f5823-174">Isso será retornado se o sinalizador MAPI_TIMEOUT_SHORT foi definido e outro thread conduzidas a exclusão mútua.</span><span class="sxs-lookup"><span data-stu-id="f5823-174">This is returned if the MAPI_TIMEOUT_SHORT flag was set and another thread held the mutex.</span></span> 
    
<span data-ttu-id="f5823-175">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="f5823-175">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="f5823-176">O usuário cancelou a operação, geralmente clicando no botão **Cancelar** em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f5823-176">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f5823-177">Comentários</span><span class="sxs-lookup"><span data-stu-id="f5823-177">Remarks</span></span>

<span data-ttu-id="f5823-178">Aplicativos de cliente MAPI chamam a função de MAPILogonEx para fazer logon em uma sessão com o sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="f5823-178">MAPI client applications call the MAPILogonEx function to log on to a session with the messaging system.</span></span> <span data-ttu-id="f5823-179">Todas as cadeias de caracteres que são passadas e retornadas de e para chamadas MAPI são terminada em nulo e devem ser especificadas no conjunto de caracteres atual ou código de página do chamada cliente ou do provedor de sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="f5823-179">All strings that are passed in and returned to and from MAPI calls are null-terminated and must be specified in the current character set or code page of the calling client or provider's operating system.</span></span>
  
<span data-ttu-id="f5823-180">O parâmetro _lpszProfileName_ é ignorado se não houver uma sessão anterior existente que chamado MapiLogonEx com o sinalizador MAPI_ALLOW_OTHERS definido e se o sinalizador MAPI_NEW_SESSION não estiver definida.</span><span class="sxs-lookup"><span data-stu-id="f5823-180">The  _lpszProfileName_ parameter is ignored if there is an existing previous session that called MapiLogonEx with the MAPI_ALLOW_OTHERS flag set and if the flag MAPI_NEW_SESSION is not set.</span></span> <span data-ttu-id="f5823-181">Se o parâmetro _lpszProfileName_ é NULL ou aponta para uma sequência vazia e o parâmetro _flFlags_ inclui o sinalizador MAPI_LOGON_UI, a função MAPILogonEx gerará uma caixa de diálogo de logon que possui um campo vazio para o nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="f5823-181">If the  _lpszProfileName_ parameter is NULL or points to an empty string, and the  _flFlags_ parameter includes the MAPI_LOGON_UI flag, the MAPILogonEx function generates a logon dialog box that has an empty field for the profile name.</span></span> 
  
<span data-ttu-id="f5823-182">Ao fazer logon em um perfil específico, um cliente deve passar o sinalizador MAPI_NEW_SESSION em MAPILogonEx além do nome de perfil.</span><span class="sxs-lookup"><span data-stu-id="f5823-182">When logging on to a specific profile, a client should pass the MAPI_NEW_SESSION flag into MAPILogonEx in addition to the profile name.</span></span> <span data-ttu-id="f5823-183">Caso contrário, se outro cliente tenha estabelecido uma sessão compartilhada fazendo logon com MAPI_ALLOW_OTHERS, o cliente será estar conectado à sessão compartilhada em vez de no perfil solicitada.</span><span class="sxs-lookup"><span data-stu-id="f5823-183">Otherwise, if another client has established a shared session by logging on with MAPI_ALLOW_OTHERS, the client will be logged on to the shared session instead of to the profile requested.</span></span> 
  
<span data-ttu-id="f5823-184">O sinalizador MAPI_EXPLICIT_PROFILE não fará o nome de perfil padrão a ser usado ao _lpszProfileName_ é nulo ou vazio, a menos que o sinalizador MAPI_USE_DEFAULT também está presente.</span><span class="sxs-lookup"><span data-stu-id="f5823-184">The MAPI_EXPLICIT_PROFILE flag does not cause the default profile name to be used when  _lpszProfileName_ is NULL or empty unless the MAPI_USE_DEFAULT flag is also present.</span></span> 
  
<span data-ttu-id="f5823-185">O sinalizador MAPI_NO_MAIL tem vários efeitos que causam o seguinte quando não usando o MAPI spooler:</span><span class="sxs-lookup"><span data-stu-id="f5823-185">The MAPI_NO_MAIL flag has several effects that cause the following when not using the MAPI spooler:</span></span>
  
- <span data-ttu-id="f5823-186">Nenhuma mensagem pode ser enviada ou entregue pelo spooler MAPI durante a sessão.</span><span class="sxs-lookup"><span data-stu-id="f5823-186">No messages can be sent or delivered by the MAPI spooler during this session.</span></span> <span data-ttu-id="f5823-187">Únicos provedores de armazenamento e transporte de ligação estreita podem enviar e entregar mensagens.</span><span class="sxs-lookup"><span data-stu-id="f5823-187">Only tightly coupled store and transport providers can send and deliver messages.</span></span> 
    
- <span data-ttu-id="f5823-188">Repositórios de baseado em servidor ainda podem enviar ou entregar mensagens.</span><span class="sxs-lookup"><span data-stu-id="f5823-188">Server based stores might still send or deliver messages.</span></span> 
    
- <span data-ttu-id="f5823-189">Mensagens enviadas ou viabilizadas pela repositórios com base em servidor não são processadas por quaisquer provedores de fora do gancho.</span><span class="sxs-lookup"><span data-stu-id="f5823-189">Messages sent or delivered by server based stores are not processed by any hook providers.</span></span> 
    
- <span data-ttu-id="f5823-190">Opções-message e por destinatário para transportes não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="f5823-190">Per-message and per-recipient options for transports are not available.</span></span> 
    
- <span data-ttu-id="f5823-191">A tabela de status não contiver entradas para provedores de transporte e qualquer funcionalidade de transporte dependentes de objetos de status (por exemplo, a configuração) não está disponível.</span><span class="sxs-lookup"><span data-stu-id="f5823-191">The status table does not contain entries for transport providers, and any transport functionality dependent on status objects (such as configuration) is not available.</span></span> 
    
- <span data-ttu-id="f5823-192">Linha da tabela de status spooler mensagem contém o valor STATUS_FAILURE.</span><span class="sxs-lookup"><span data-stu-id="f5823-192">The message spooler row in the status table contains the STATUS_FAILURE value.</span></span> 
    
- <span data-ttu-id="f5823-193">Logons acumuladas são permitidas, mas os logons não farão com que o logon anterior receber atualizações de status de objeto.</span><span class="sxs-lookup"><span data-stu-id="f5823-193">Piggybacked logons are allowed, but those logons do not cause the previous logon to receive status object updates.</span></span> 
    
<span data-ttu-id="f5823-194">Um serviço sempre deve fazer logon usando o sinalizador MAPI_NO_MAIL.</span><span class="sxs-lookup"><span data-stu-id="f5823-194">A service should always log on using the MAPI_NO_MAIL flag.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f5823-195">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f5823-195">MFCMAPI reference</span></span>

<span data-ttu-id="f5823-196">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f5823-196">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f5823-197">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="f5823-197">**File**</span></span>|<span data-ttu-id="f5823-198">**Function**</span><span class="sxs-lookup"><span data-stu-id="f5823-198">**Function**</span></span>|<span data-ttu-id="f5823-199">**Comment**</span><span class="sxs-lookup"><span data-stu-id="f5823-199">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f5823-200">MAPIObjects.cpp</span><span class="sxs-lookup"><span data-stu-id="f5823-200">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="f5823-201">CMapiObjects::MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="f5823-201">CMapiObjects::MAPILogonEx</span></span>  <br/> |<span data-ttu-id="f5823-202">MFCMAPI usa o método MAPILogonEx para fazer logon no MAPI.</span><span class="sxs-lookup"><span data-stu-id="f5823-202">MFCMAPI uses the MAPILogonEx method to log on to MAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f5823-203">Confira também</span><span class="sxs-lookup"><span data-stu-id="f5823-203">See also</span></span>



[<span data-ttu-id="f5823-204">IMAPISession::GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="f5823-204">IMAPISession::GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md)
  
[<span data-ttu-id="f5823-205">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="f5823-205">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)


[<span data-ttu-id="f5823-206">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="f5823-206">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

