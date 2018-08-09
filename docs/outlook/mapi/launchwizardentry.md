---
title: LAUNCHWIZARDENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.LAUNCHWIZARDENTRY
api_type:
- COM
ms.assetid: 5778dffa-f01b-46b3-9c19-862793740918
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d80671331c2760c574ab32d79115a352ee4bcf25
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767780"
---
# <a name="launchwizardentry"></a><span data-ttu-id="36469-103">LAUNCHWIZARDENTRY</span><span class="sxs-lookup"><span data-stu-id="36469-103">LAUNCHWIZARDENTRY</span></span>

  
  
<span data-ttu-id="36469-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="36469-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="36469-105">Define uma função que inicia o aplicativo Assistente de perfil para fins de adição de um ou mais serviços de mensagem a um perfil.</span><span class="sxs-lookup"><span data-stu-id="36469-105">Defines a function that starts the Profile Wizard application for the purpose of adding one or more message services to a profile.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="36469-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="36469-106">Header file:</span></span>  <br/> |<span data-ttu-id="36469-107">Mapiwz.h</span><span class="sxs-lookup"><span data-stu-id="36469-107">Mapiwz.h</span></span>  <br/> |
|<span data-ttu-id="36469-108">Função definido implementada por:</span><span class="sxs-lookup"><span data-stu-id="36469-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="36469-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="36469-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="36469-110">Função definido chamada pelo:</span><span class="sxs-lookup"><span data-stu-id="36469-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="36469-111">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="36469-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT LAUNCHWIZARDENTRY(
  HWND hParentWnd,
  ULONG ulFlags,
  LPCSTR FAR * lppszServiceNameToAdd,
  ULONG cbBufferMax,
  LPSTR lpszNewProfileName
);
```

## <a name="parameters"></a><span data-ttu-id="36469-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="36469-112">Parameters</span></span>

 <span data-ttu-id="36469-113">_hParentWnd_</span><span class="sxs-lookup"><span data-stu-id="36469-113">_hParentWnd_</span></span>
  
> <span data-ttu-id="36469-114">[in] Um identificador para a janela do pai do chamador.</span><span class="sxs-lookup"><span data-stu-id="36469-114">[in] A handle to the caller's parent window.</span></span> <span data-ttu-id="36469-115">Se o chamador não tiver uma janela pai, o parâmetro _hParentWnd_ deve ser NULL.</span><span class="sxs-lookup"><span data-stu-id="36469-115">If the caller does not have a parent window, the  _hParentWnd_ parameter should be NULL.</span></span> 
    
 <span data-ttu-id="36469-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="36469-116">_ulFlags_</span></span>
  
> <span data-ttu-id="36469-117">[in] Bitmask dos sinalizadores indicando opções para o Assistente de perfil.</span><span class="sxs-lookup"><span data-stu-id="36469-117">[in] Bitmask of flags indicating options for the Profile Wizard.</span></span> <span data-ttu-id="36469-118">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="36469-118">The following flags can be set:</span></span>
    
<span data-ttu-id="36469-119">MAPI_PW_ADD_SERVICE_ONLY</span><span class="sxs-lookup"><span data-stu-id="36469-119">MAPI_PW_ADD_SERVICE_ONLY</span></span> 
  
> <span data-ttu-id="36469-120">O Assistente de perfil é adicionar apenas os serviços de mensagem listados através do parâmetro _lppszServiceNameToAdd_ e não exibir sua página para selecionar serviços de mensagens.</span><span class="sxs-lookup"><span data-stu-id="36469-120">The Profile Wizard is to add only the message services listed through the  _lppszServiceNameToAdd_ parameter, and not display its page for selecting message services.</span></span> 
    
<span data-ttu-id="36469-121">MAPI_PW_FIRST_PROFILE</span><span class="sxs-lookup"><span data-stu-id="36469-121">MAPI_PW_FIRST_PROFILE</span></span> 
  
> <span data-ttu-id="36469-122">O perfil a ser criado é o primeiro para esta estação de trabalho.</span><span class="sxs-lookup"><span data-stu-id="36469-122">The profile to be created is the first one for this workstation.</span></span> 
    
<span data-ttu-id="36469-123">MAPI_PW_HIDE_SERVICES_LIST</span><span class="sxs-lookup"><span data-stu-id="36469-123">MAPI_PW_HIDE_SERVICES_LIST</span></span> 
  
> <span data-ttu-id="36469-124">Página de perfil do Assistente para selecionar serviços de mensagem não deve ser exibida.</span><span class="sxs-lookup"><span data-stu-id="36469-124">The Profile Wizard's page for selecting message services should not be displayed.</span></span> 
    
<span data-ttu-id="36469-125">MAPI_PW_LAUNCHED_BY_CONFIG</span><span class="sxs-lookup"><span data-stu-id="36469-125">MAPI_PW_LAUNCHED_BY_CONFIG</span></span> 
  
> <span data-ttu-id="36469-126">O Assistente de perfil foi iniciado pelo aplicativo de configuração do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="36469-126">The Profile Wizard was launched by the Control Panel configuration application.</span></span> 
    
<span data-ttu-id="36469-127">MAPI_PW_PROVIDER_UI_ONLY</span><span class="sxs-lookup"><span data-stu-id="36469-127">MAPI_PW_PROVIDER_UI_ONLY</span></span> 
  
> <span data-ttu-id="36469-128">Somente dos provedores de serviços configuração caixas de diálogo devem ser exibidas e páginas de perfil do assistente não devem ser exibidos.</span><span class="sxs-lookup"><span data-stu-id="36469-128">Only the service providers's configuration dialog boxes should be displayed and the Profile Wizard's pages should not appear.</span></span> <span data-ttu-id="36469-129">Esse sinalizador só pode ser definida se o sinalizador MAPI_PW_ADD_SERVICE_ONLY está definido.</span><span class="sxs-lookup"><span data-stu-id="36469-129">This flag can only be set if the MAPI_PW_ADD_SERVICE_ONLY flag is set.</span></span> 
    
 <span data-ttu-id="36469-130">_lppszServiceNameToAdd_</span><span class="sxs-lookup"><span data-stu-id="36469-130">_lppszServiceNameToAdd_</span></span>
  
> <span data-ttu-id="36469-131">[in] Ponteiro para uma matriz de cadeias de caracteres que contém os nomes dos serviços de mensagem a ser adicionada ao perfil.</span><span class="sxs-lookup"><span data-stu-id="36469-131">[in] Pointer to an array of strings that contains the names of the message services to be added to the profile.</span></span> <span data-ttu-id="36469-132">A matriz deve terminar com um valor NULL.</span><span class="sxs-lookup"><span data-stu-id="36469-132">The array must terminate with a NULL value.</span></span> 
    
 <span data-ttu-id="36469-133">_cbBufferMax_</span><span class="sxs-lookup"><span data-stu-id="36469-133">_cbBufferMax_</span></span>
  
> <span data-ttu-id="36469-134">[in] Tamanho do buffer apontado pelo parâmetro _lpszNewProfileName_ .</span><span class="sxs-lookup"><span data-stu-id="36469-134">[in] Size of the buffer pointed to by the  _lpszNewProfileName_ parameter.</span></span> 
    
 <span data-ttu-id="36469-135">_lpszNewProfileName_</span><span class="sxs-lookup"><span data-stu-id="36469-135">_lpszNewProfileName_</span></span>
  
> <span data-ttu-id="36469-136">[out] Ponteiro para um buffer de sequência em que a função com base em **LAUNCHWIZARDENTRY** retorna o nome do perfil criado.</span><span class="sxs-lookup"><span data-stu-id="36469-136">[out] Pointer to a string buffer where the function based on **LAUNCHWIZARDENTRY** returns the name of the created profile.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="36469-137">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="36469-137">Return value</span></span>

<span data-ttu-id="36469-138">S_OK</span><span class="sxs-lookup"><span data-stu-id="36469-138">S_OK</span></span> 
  
> <span data-ttu-id="36469-139">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="36469-139">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="36469-140">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="36469-140">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="36469-141">Um erro de origem inesperado ou desconhecido impediu a conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="36469-141">An error of unexpected or unknown origin prevented the operation from completing.</span></span> <span data-ttu-id="36469-142">Incapacidade de acessar o perfil padrão e um erro possibilidades incluem falha ao inicializar o subsistema MAPI para o Assistente de perfil, retornar da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="36469-142">Possibilities include failure to initialize the MAPI subsystem for the Profile Wizard, inability to access the default profile, and an error return from the dialog box.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="36469-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="36469-143">Remarks</span></span>

<span data-ttu-id="36469-144">A implementação de MAPI do protótipo de função **LAUNCHWIZARDENTRY** é o ponto de entrada para o aplicativo Assistente de perfil de MAPI.</span><span class="sxs-lookup"><span data-stu-id="36469-144">The MAPI implementation of the **LAUNCHWIZARDENTRY** function prototype is the entry point into the MAPI Profile Wizard application.</span></span> <span data-ttu-id="36469-145">Esse ponto de entrada **LaunchWizard**os nomes de MAPI.</span><span class="sxs-lookup"><span data-stu-id="36469-145">MAPI names this entry point **LaunchWizard**.</span></span> 
  
<span data-ttu-id="36469-146">Quando o sinalizador MAPI_PW_ADD_SERVICE_ONLY é definido no parâmetro _ulFlags_ , as seguintes regras se aplicam:</span><span class="sxs-lookup"><span data-stu-id="36469-146">When the MAPI_PW_ADD_SERVICE_ONLY flag is set in the  _ulFlags_ parameter, the following rules apply:</span></span> 
  
- <span data-ttu-id="36469-147">O sinalizador MAPI_PW_LAUNCHED_BY_CONFIG inibe a página de boas-vindas seja exibida.</span><span class="sxs-lookup"><span data-stu-id="36469-147">The MAPI_PW_LAUNCHED_BY_CONFIG flag inhibits the welcome page from being displayed.</span></span> 
    
- <span data-ttu-id="36469-148">Os sinalizadores MAPI_PW_HIDE_SERVICES_LIST e MAPI_PW_PROVIDER_UI_ONLY são úteis somente quando não houver nenhum perfil padrão.</span><span class="sxs-lookup"><span data-stu-id="36469-148">The MAPI_PW_HIDE_SERVICES_LIST and MAPI_PW_PROVIDER_UI_ONLY flags are useful only when there is no default profile.</span></span> <span data-ttu-id="36469-149">Nesse caso, esses sinalizadores determinam qual página deve ser exibida do Assistente de perfil.</span><span class="sxs-lookup"><span data-stu-id="36469-149">In this case these flags determine which Profile Wizard page is to be displayed.</span></span> 
    
- <span data-ttu-id="36469-150">Se existir um perfil padrão, nenhuma das páginas do Assistente de perfil devem ser exibidas.</span><span class="sxs-lookup"><span data-stu-id="36469-150">If a default profile exists, none of the Profile Wizard pages are to be displayed.</span></span> 
    
- <span data-ttu-id="36469-151">Se existir um perfil padrão, o serviço de apenas uma mensagem está listado por meio do parâmetro _lppszServiceNameToAdd_ e que o serviço de mensagem já está no perfil padrão, o Assistente de perfil Retorna S_OK sem adicionar qualquer coisa ao perfil.</span><span class="sxs-lookup"><span data-stu-id="36469-151">If a default profile exists, only one message service is listed through the  _lppszServiceNameToAdd_ parameter, and that message service is already in the default profile, the Profile Wizard returns S_OK without adding anything to the profile.</span></span> 
    
<span data-ttu-id="36469-152">Para cada serviço de mensagem a ser adicionada ao perfil, o Assistente de perfil chama a função de ponto de entrada do serviço com base em protótipo [MSGSERVICEENTRY](msgserviceentry.md) .</span><span class="sxs-lookup"><span data-stu-id="36469-152">For every message service to be added to the profile, the Profile Wizard calls the service's entry point function based on the [MSGSERVICEENTRY](msgserviceentry.md) prototype.</span></span> <span data-ttu-id="36469-153">Para cada provedor de serviço selecionado de um serviço de mensagem a ser adicionada ao perfil, o Assistente de perfil chama a função de ponto de entrada do provedor com base em protótipo [WIZARDENTRY](wizardentry.md) .</span><span class="sxs-lookup"><span data-stu-id="36469-153">For each service provider selected from a message service to be added to the profile, the Profile Wizard calls the provider's entry point function based on the [WIZARDENTRY](wizardentry.md) prototype.</span></span> <span data-ttu-id="36469-154">Durante a configuração interativa, todos os eventos do usuário nas páginas de propriedade faz com que o Assistente de perfil chamar a função de retorno de chamada do provedor com base em protótipo [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) .</span><span class="sxs-lookup"><span data-stu-id="36469-154">During interactive configuration, every user event in the property pages causes the Profile Wizard to call the provider's callback function based on the [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) prototype.</span></span> 
  
<span data-ttu-id="36469-155">Se um provedor de serviço que está sendo adicionado ao perfil do suporta as páginas do Assistente de perfil, ela deve permitir programática configuração do perfil.</span><span class="sxs-lookup"><span data-stu-id="36469-155">If a service provider being added to the profile supports the Profile Wizard pages, it must allow programmatic configuration of the profile.</span></span>
  

