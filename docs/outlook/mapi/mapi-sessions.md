---
title: Sessões MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c5a7c137-393e-40ff-a2b9-afe02da2435a
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 45dc993c337249ed7d4dffbd5324267de82981d0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767951"
---
# <a name="mapi-sessions"></a><span data-ttu-id="a7e51-103">Sessões MAPI</span><span class="sxs-lookup"><span data-stu-id="a7e51-103">MAPI sessions</span></span>

<span data-ttu-id="a7e51-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a7e51-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a7e51-105">Antes do aplicativo cliente pode chamar um sistema de mensagens subjacente, ele precisa estabelecer uma sessão ou conexão, com o subsistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="a7e51-105">Before the client application can call an underlying messaging system, it must establish a session, or connection, with the MAPI subsystem.</span></span>
  
<span data-ttu-id="a7e51-106">Sessões são iniciadas quando um usuário faz logon, um processo que acessa um perfil válido e valida o sistema de mensagens e as credenciais do serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="a7e51-106">Sessions are initiated when a user logs on, a process that accesses a valid profile and validates the messaging system and the message service credentials.</span></span> <span data-ttu-id="a7e51-107">Em seguida, o processo garante que todos os serviços de mensagem do perfil estão configurados corretamente.</span><span class="sxs-lookup"><span data-stu-id="a7e51-107">Then, the process ensures that all of the profile's message services are correctly configured.</span></span> <span data-ttu-id="a7e51-108">A interface de cliente que você usa determina a chamada de logon.</span><span class="sxs-lookup"><span data-stu-id="a7e51-108">The client interface you use determines the logon call.</span></span> <span data-ttu-id="a7e51-109">Clientes MAPI chamar a função de [MAPILogonEx](mapilogonex.md) .</span><span class="sxs-lookup"><span data-stu-id="a7e51-109">MAPI clients call the [MAPILogonEx](mapilogonex.md) function.</span></span> 
  
<span data-ttu-id="a7e51-110">Configuração do serviço de mensagens é uma das partes mais importantes do processo de logon.</span><span class="sxs-lookup"><span data-stu-id="a7e51-110">Message service configuration is one of the most important parts of the logon process.</span></span> <span data-ttu-id="a7e51-111">O perfil é a origem inicial das informações de configuração.</span><span class="sxs-lookup"><span data-stu-id="a7e51-111">The profile is the initial source for configuration information.</span></span> <span data-ttu-id="a7e51-112">Se informações sobre um serviço de mensagem específica estiverem ausentes, o processo de logon tenta solicitar ao usuário para fornecer a ele.</span><span class="sxs-lookup"><span data-stu-id="a7e51-112">If information for a particular message service is missing, the logon process tries to prompt the user to supply it.</span></span> <span data-ttu-id="a7e51-113">Isso nem sempre é bem-sucedida por dois motivos: primeiro, solicitando que o usuário requer a exibição de uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="a7e51-113">This is not always successful for two reasons: First, prompting the user requires the display of a dialog box.</span></span> <span data-ttu-id="a7e51-114">É possível para que os clientes não permitir a exibição de uma interface do usuário, passando um sinalizador na chamada de logon.</span><span class="sxs-lookup"><span data-stu-id="a7e51-114">It is possible for clients to disallow the display of a user interface by passing a flag into the logon call.</span></span> <span data-ttu-id="a7e51-115">Em segundo lugar, o usuário pode cancelar a caixa de diálogo antes que as informações necessárias podem ser adicionadas.</span><span class="sxs-lookup"><span data-stu-id="a7e51-115">Second, the user could cancel the dialog box before the needed information can be added.</span></span>
  
<span data-ttu-id="a7e51-116">Quando um processo de logon falha uma vez, o usuário é informado sobre a falha e tem a chance de repetição ou corrigir a condição de erro.</span><span class="sxs-lookup"><span data-stu-id="a7e51-116">When a logon process fails one time, the user is informed of the failure and given the chance to retry or correct the error condition.</span></span> <span data-ttu-id="a7e51-117">Mais uma vez, uma interface de usuário será exibida, se o cliente permite e o usuário será solicitado a inserir quaisquer dados estão faltando.</span><span class="sxs-lookup"><span data-stu-id="a7e51-117">Once again, a user interface will be displayed, if the client allows it, and the user will be prompted to enter whatever data is missing.</span></span> <span data-ttu-id="a7e51-118">Se esse segundo try for bem sucedida, MAPI desabilita todos os provedores de serviço no serviço de mensagem para a duração da sessão.</span><span class="sxs-lookup"><span data-stu-id="a7e51-118">If this second try is unsuccessful, MAPI disables all service providers in the message service for the duration of the session.</span></span> <span data-ttu-id="a7e51-119">Na verdade, o serviço de mensagem inteira está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="a7e51-119">In effect, the whole message service is disabled.</span></span> <span data-ttu-id="a7e51-120">Isso significa que nenhum dos provedores de serviço no serviço de mensagem pode trabalhar.</span><span class="sxs-lookup"><span data-stu-id="a7e51-120">This means that none of the service providers in the message service can work.</span></span> <span data-ttu-id="a7e51-121">Isso é feito porque se um provedor de falha de logon, os outros provedores geralmente também falharem.</span><span class="sxs-lookup"><span data-stu-id="a7e51-121">This is done because if one provider fails logon, the other providers usually also fail.</span></span> <span data-ttu-id="a7e51-122">O processo de logon pode falhar devido a um caminho inválido para um recurso necessário, uma versão incompatível do MAPI, um servidor de mensagens não está disponível ou corrupção de dados.</span><span class="sxs-lookup"><span data-stu-id="a7e51-122">The logon process can fail due to an invalid path for a necessary resource, an incompatible version of MAPI, an unavailable messaging server, or data corruption.</span></span> 
  
<span data-ttu-id="a7e51-123">Os clientes podem especificar um dos dois tipos de sessões seja estabelecida na chamada logon: uma sessão individual ou uma sessão compartilhada.</span><span class="sxs-lookup"><span data-stu-id="a7e51-123">Clients can specify one of two types of sessions to be established in the logon call: an individual session or a shared session.</span></span> <span data-ttu-id="a7e51-124">Sessões individuais são conexões particulares; Há um relacionamento individual entre um aplicativo cliente e a sessão está usando.</span><span class="sxs-lookup"><span data-stu-id="a7e51-124">Individual sessions are private connections; there is a one-to-one relationship between a client application and the session it is using.</span></span> <span data-ttu-id="a7e51-125">Como consequência, aplicativos de cliente que compartilham uma sessão também compartilham um perfil.</span><span class="sxs-lookup"><span data-stu-id="a7e51-125">As a consequence, client applications that share a session also share a profile.</span></span> <span data-ttu-id="a7e51-126">Sessões compartilhadas são estabelecidas uma vez, mas podem ser usadas por outros aplicativos cliente que precisam usá-los.</span><span class="sxs-lookup"><span data-stu-id="a7e51-126">Shared sessions are established once but can be used by other client applications that need to use them.</span></span> <span data-ttu-id="a7e51-127">O perfil e as credenciais são especificadas somente com o logon inicial.</span><span class="sxs-lookup"><span data-stu-id="a7e51-127">The profile and credentials are specified only with the initial logon.</span></span> 
  
<span data-ttu-id="a7e51-128">Os clientes podem fazer logon várias vezes como o mesmo usuário ou vários usuários.</span><span class="sxs-lookup"><span data-stu-id="a7e51-128">Clients can log on multiple times as the same user or as multiple users.</span></span> <span data-ttu-id="a7e51-129">MAPI não impede a isso.</span><span class="sxs-lookup"><span data-stu-id="a7e51-129">MAPI does not prevent this.</span></span> <span data-ttu-id="a7e51-130">Alguns provedores de serviços, no entanto, podem não ser tão flexíveis, retornando o valor de erro MAPI_E_SESSION_LIMIT em tentativas de logon subsequentes.</span><span class="sxs-lookup"><span data-stu-id="a7e51-130">Some service providers, however, might not be as flexible, returning the error value MAPI_E_SESSION_LIMIT on subsequent logon attempts.</span></span> <span data-ttu-id="a7e51-131">Provedores de serviços com limitações de hardware subjacente podem ser necessária para impor um limite de sessão.</span><span class="sxs-lookup"><span data-stu-id="a7e51-131">Service providers with underlying hardware limitations can be required to enforce a session limit.</span></span>
  
<span data-ttu-id="a7e51-132">As chamadas de função para o estabelecimento de uma sessão tem uma coleção de parâmetros e os sinalizadores que controlam como a sessão é criada.</span><span class="sxs-lookup"><span data-stu-id="a7e51-132">The function calls for establishing a session have a collection of flags and parameters that control how the session is created.</span></span> <span data-ttu-id="a7e51-133">O cliente especifica um nome de perfil opcional e um identificador de janela que atua como a janela pai para as caixas de diálogo que são exibidos.</span><span class="sxs-lookup"><span data-stu-id="a7e51-133">The client specifies an optional profile name and a window handle that acts as the parent window for any dialog boxes that are displayed.</span></span> <span data-ttu-id="a7e51-134">Os sinalizadores incluem MAPI_NEW_SESSION, que solicita que uma nova sessão individual (em vez de uma sessão compartilhada) ser estabelecida, e o sinalizador de interface do usuário MAPI_LOGON_UI.</span><span class="sxs-lookup"><span data-stu-id="a7e51-134">The flags include MAPI_NEW_SESSION, which requests that a new, individual session (rather than a shared session) be established, and the MAPI_LOGON_UI user interface flag.</span></span> <span data-ttu-id="a7e51-135">O sinalizador de interface do usuário é definido como solicitar uma caixa de diálogo de logon.</span><span class="sxs-lookup"><span data-stu-id="a7e51-135">The user interface flag is set to request a logon dialog box.</span></span>
  
<span data-ttu-id="a7e51-136">A ilustração a seguir mostra como esses parâmetros e os sinalizadores vários estabelecem uma sessão MAPI.</span><span class="sxs-lookup"><span data-stu-id="a7e51-136">The following illustration shows how these various parameters and flags establish a MAPI session.</span></span>
  
<span data-ttu-id="a7e51-137">**MAPI session flowchart**</span><span class="sxs-lookup"><span data-stu-id="a7e51-137">**MAPI session flowchart**</span></span>
  
<span data-ttu-id="a7e51-138">![Fluxograma de sessão MAPI] (media/amapi_47.gif "Fluxograma de sessão MAPI")</span><span class="sxs-lookup"><span data-stu-id="a7e51-138">![MAPI session flowchart](media/amapi_47.gif "MAPI session flowchart")</span></span>
  
<span data-ttu-id="a7e51-139">Para obter informações sobre como lidar com sessões de dentro de um aplicativo cliente, consulte [Manipulação de sessão MAPI](mapi-session-handling.md)</span><span class="sxs-lookup"><span data-stu-id="a7e51-139">For information about handling sessions from within a client application, see [MAPI Session Handling](mapi-session-handling.md)</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a7e51-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="a7e51-140">See also</span></span>

- [<span data-ttu-id="a7e51-141">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="a7e51-141">MAPILogonEx</span></span>](mapilogonex.md)  
- [<span data-ttu-id="a7e51-142">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a7e51-142">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)
- [<span data-ttu-id="a7e51-143">Tratamento de sessão MAPI</span><span class="sxs-lookup"><span data-stu-id="a7e51-143">MAPI Session Handling</span></span>](mapi-session-handling.md)  
- [<span data-ttu-id="a7e51-144">Vis�o geral da programa��o MAPI</span><span class="sxs-lookup"><span data-stu-id="a7e51-144">MAPI Programming Overview</span></span>](mapi-programming-overview.md)
