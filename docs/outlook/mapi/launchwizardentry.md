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
ms.openlocfilehash: c1509918eb587c17deebf95317cf57b4ab19928a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270186"
---
# <a name="launchwizardentry"></a><span data-ttu-id="e8edb-103">LAUNCHWIZARDENTRY</span><span class="sxs-lookup"><span data-stu-id="e8edb-103">LAUNCHWIZARDENTRY</span></span>

  
  
<span data-ttu-id="e8edb-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8edb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8edb-105">Define uma função que inicia o aplicativo assistente de perfil com o objetivo de adicionar um ou mais serviços de mensagem a um perfil.</span><span class="sxs-lookup"><span data-stu-id="e8edb-105">Defines a function that starts the Profile Wizard application for the purpose of adding one or more message services to a profile.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e8edb-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="e8edb-106">Header file:</span></span>  <br/> |<span data-ttu-id="e8edb-107">Mapiwz. h</span><span class="sxs-lookup"><span data-stu-id="e8edb-107">Mapiwz.h</span></span>  <br/> |
|<span data-ttu-id="e8edb-108">Função definida implementada por:</span><span class="sxs-lookup"><span data-stu-id="e8edb-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="e8edb-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e8edb-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e8edb-110">Função definida chamada por:</span><span class="sxs-lookup"><span data-stu-id="e8edb-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="e8edb-111">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="e8edb-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT LAUNCHWIZARDENTRY(
  HWND hParentWnd,
  ULONG ulFlags,
  LPCSTR FAR * lppszServiceNameToAdd,
  ULONG cbBufferMax,
  LPSTR lpszNewProfileName
);
```

## <a name="parameters"></a><span data-ttu-id="e8edb-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e8edb-112">Parameters</span></span>

 <span data-ttu-id="e8edb-113">_hParentWnd_</span><span class="sxs-lookup"><span data-stu-id="e8edb-113">_hParentWnd_</span></span>
  
> <span data-ttu-id="e8edb-114">no Uma alça para a janela pai do chamador.</span><span class="sxs-lookup"><span data-stu-id="e8edb-114">[in] A handle to the caller's parent window.</span></span> <span data-ttu-id="e8edb-115">Se o chamador não tiver uma janela pai, o parâmetro _hParentWnd_ deverá ser nulo.</span><span class="sxs-lookup"><span data-stu-id="e8edb-115">If the caller does not have a parent window, the  _hParentWnd_ parameter should be NULL.</span></span> 
    
 <span data-ttu-id="e8edb-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e8edb-116">_ulFlags_</span></span>
  
> <span data-ttu-id="e8edb-117">no Bitmask de sinalizadores que indicam opções para o assistente de perfil.</span><span class="sxs-lookup"><span data-stu-id="e8edb-117">[in] Bitmask of flags indicating options for the Profile Wizard.</span></span> <span data-ttu-id="e8edb-118">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="e8edb-118">The following flags can be set:</span></span>
    
<span data-ttu-id="e8edb-119">MAPI_PW_ADD_SERVICE_ONLY</span><span class="sxs-lookup"><span data-stu-id="e8edb-119">MAPI_PW_ADD_SERVICE_ONLY</span></span> 
  
> <span data-ttu-id="e8edb-120">O assistente de perfil é adicionar somente os serviços de mensagens listados por meio do parâmetro _lppszServiceNameToAdd_ , e não exibir sua página para selecionar serviços de mensagens.</span><span class="sxs-lookup"><span data-stu-id="e8edb-120">The Profile Wizard is to add only the message services listed through the  _lppszServiceNameToAdd_ parameter, and not display its page for selecting message services.</span></span> 
    
<span data-ttu-id="e8edb-121">MAPI_PW_FIRST_PROFILE</span><span class="sxs-lookup"><span data-stu-id="e8edb-121">MAPI_PW_FIRST_PROFILE</span></span> 
  
> <span data-ttu-id="e8edb-122">O perfil a ser criado é o primeiro para esta estação de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e8edb-122">The profile to be created is the first one for this workstation.</span></span> 
    
<span data-ttu-id="e8edb-123">MAPI_PW_HIDE_SERVICES_LIST</span><span class="sxs-lookup"><span data-stu-id="e8edb-123">MAPI_PW_HIDE_SERVICES_LIST</span></span> 
  
> <span data-ttu-id="e8edb-124">A página do assistente de perfil para selecionar serviços de mensagens não deve ser exibida.</span><span class="sxs-lookup"><span data-stu-id="e8edb-124">The Profile Wizard's page for selecting message services should not be displayed.</span></span> 
    
<span data-ttu-id="e8edb-125">MAPI_PW_LAUNCHED_BY_CONFIG</span><span class="sxs-lookup"><span data-stu-id="e8edb-125">MAPI_PW_LAUNCHED_BY_CONFIG</span></span> 
  
> <span data-ttu-id="e8edb-126">O assistente de perfil foi iniciado pelo aplicativo de configuração do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="e8edb-126">The Profile Wizard was launched by the Control Panel configuration application.</span></span> 
    
<span data-ttu-id="e8edb-127">MAPI_PW_PROVIDER_UI_ONLY</span><span class="sxs-lookup"><span data-stu-id="e8edb-127">MAPI_PW_PROVIDER_UI_ONLY</span></span> 
  
> <span data-ttu-id="e8edb-128">Somente as caixas de diálogo de configuração dos provedores de serviços devem ser exibidas e as páginas do assistente de perfil não devem ser exibidas.</span><span class="sxs-lookup"><span data-stu-id="e8edb-128">Only the service providers's configuration dialog boxes should be displayed and the Profile Wizard's pages should not appear.</span></span> <span data-ttu-id="e8edb-129">Este sinalizador só poderá ser definido se o sinalizador MAPI_PW_ADD_SERVICE_ONLY estiver definido.</span><span class="sxs-lookup"><span data-stu-id="e8edb-129">This flag can only be set if the MAPI_PW_ADD_SERVICE_ONLY flag is set.</span></span> 
    
 <span data-ttu-id="e8edb-130">_lppszServiceNameToAdd_</span><span class="sxs-lookup"><span data-stu-id="e8edb-130">_lppszServiceNameToAdd_</span></span>
  
> <span data-ttu-id="e8edb-131">no Ponteiro para uma matriz de cadeias de caracteres que contém os nomes dos serviços de mensagens a serem adicionados ao perfil.</span><span class="sxs-lookup"><span data-stu-id="e8edb-131">[in] Pointer to an array of strings that contains the names of the message services to be added to the profile.</span></span> <span data-ttu-id="e8edb-132">A matriz deve terminar com um valor nulo.</span><span class="sxs-lookup"><span data-stu-id="e8edb-132">The array must terminate with a NULL value.</span></span> 
    
 <span data-ttu-id="e8edb-133">_cbBufferMax_</span><span class="sxs-lookup"><span data-stu-id="e8edb-133">_cbBufferMax_</span></span>
  
> <span data-ttu-id="e8edb-134">no Tamanho do buffer apontado pelo parâmetro _lpszNewProfileName_ .</span><span class="sxs-lookup"><span data-stu-id="e8edb-134">[in] Size of the buffer pointed to by the  _lpszNewProfileName_ parameter.</span></span> 
    
 <span data-ttu-id="e8edb-135">_lpszNewProfileName_</span><span class="sxs-lookup"><span data-stu-id="e8edb-135">_lpszNewProfileName_</span></span>
  
> <span data-ttu-id="e8edb-136">bota Ponteiro para um buffer de cadeia de caracteres em que a função baseada no **LAUNCHWIZARDENTRY** retorna o nome do perfil criado.</span><span class="sxs-lookup"><span data-stu-id="e8edb-136">[out] Pointer to a string buffer where the function based on **LAUNCHWIZARDENTRY** returns the name of the created profile.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e8edb-137">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e8edb-137">Return value</span></span>

<span data-ttu-id="e8edb-138">S_OK</span><span class="sxs-lookup"><span data-stu-id="e8edb-138">S_OK</span></span> 
  
> <span data-ttu-id="e8edb-139">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="e8edb-139">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="e8edb-140">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="e8edb-140">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="e8edb-141">Um erro de origem inesperada ou desconhecida impediu a conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="e8edb-141">An error of unexpected or unknown origin prevented the operation from completing.</span></span> <span data-ttu-id="e8edb-142">As possibilidades incluem falha ao inicializar o subsistema MAPI para o assistente de perfil, incapacidade de acessar o perfil padrão e um erro retornado da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="e8edb-142">Possibilities include failure to initialize the MAPI subsystem for the Profile Wizard, inability to access the default profile, and an error return from the dialog box.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e8edb-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="e8edb-143">Remarks</span></span>

<span data-ttu-id="e8edb-144">A implementação de MAPI do protótipo da função **LAUNCHWIZARDENTRY** é o ponto de entrada no aplicativo assistente de perfil MAPI.</span><span class="sxs-lookup"><span data-stu-id="e8edb-144">The MAPI implementation of the **LAUNCHWIZARDENTRY** function prototype is the entry point into the MAPI Profile Wizard application.</span></span> <span data-ttu-id="e8edb-145">Nomes de MAPI este ponto de entrada **LaunchWizard**.</span><span class="sxs-lookup"><span data-stu-id="e8edb-145">MAPI names this entry point **LaunchWizard**.</span></span> 
  
<span data-ttu-id="e8edb-146">Quando o sinalizador MAPI_PW_ADD_SERVICE_ONLY é definido no parâmetro _parâmetroulflags_ , as seguintes regras são aplicadas:</span><span class="sxs-lookup"><span data-stu-id="e8edb-146">When the MAPI_PW_ADD_SERVICE_ONLY flag is set in the  _ulFlags_ parameter, the following rules apply:</span></span> 
  
- <span data-ttu-id="e8edb-147">O sinalizador MAPI_PW_LAUNCHED_BY_CONFIG inibe a exibição da página de boas-vindas.</span><span class="sxs-lookup"><span data-stu-id="e8edb-147">The MAPI_PW_LAUNCHED_BY_CONFIG flag inhibits the welcome page from being displayed.</span></span> 
    
- <span data-ttu-id="e8edb-148">Os sinalizadores MAPI_PW_HIDE_SERVICES_LIST e MAPI_PW_PROVIDER_UI_ONLY são úteis somente quando não há um perfil padrão.</span><span class="sxs-lookup"><span data-stu-id="e8edb-148">The MAPI_PW_HIDE_SERVICES_LIST and MAPI_PW_PROVIDER_UI_ONLY flags are useful only when there is no default profile.</span></span> <span data-ttu-id="e8edb-149">Nesse caso, esses sinalizadores determinam qual página do assistente de perfil deve ser exibida.</span><span class="sxs-lookup"><span data-stu-id="e8edb-149">In this case these flags determine which Profile Wizard page is to be displayed.</span></span> 
    
- <span data-ttu-id="e8edb-150">Se houver um perfil padrão, nenhuma das páginas do assistente de perfil será exibida.</span><span class="sxs-lookup"><span data-stu-id="e8edb-150">If a default profile exists, none of the Profile Wizard pages are to be displayed.</span></span> 
    
- <span data-ttu-id="e8edb-151">Se houver um perfil padrão, apenas um serviço de mensagens será listado através do parâmetro _lppszServiceNameToAdd_ e esse serviço de mensagens já estiver no perfil padrão, o assistente de perfil retornará S_OK sem adicionar nada ao perfil.</span><span class="sxs-lookup"><span data-stu-id="e8edb-151">If a default profile exists, only one message service is listed through the  _lppszServiceNameToAdd_ parameter, and that message service is already in the default profile, the Profile Wizard returns S_OK without adding anything to the profile.</span></span> 
    
<span data-ttu-id="e8edb-152">Para cada serviço de mensagens a ser adicionado ao perfil, o assistente de perfil chama a função de ponto de entrada do serviço com base no protótipo [MSGSERVICEENTRY](msgserviceentry.md) .</span><span class="sxs-lookup"><span data-stu-id="e8edb-152">For every message service to be added to the profile, the Profile Wizard calls the service's entry point function based on the [MSGSERVICEENTRY](msgserviceentry.md) prototype.</span></span> <span data-ttu-id="e8edb-153">Para cada provedor de serviços selecionado de um serviço de mensagens a ser adicionado ao perfil, o assistente de perfil chama a função de ponto de entrada do provedor com base no protótipo [WIZARDENTRY](wizardentry.md) .</span><span class="sxs-lookup"><span data-stu-id="e8edb-153">For each service provider selected from a message service to be added to the profile, the Profile Wizard calls the provider's entry point function based on the [WIZARDENTRY](wizardentry.md) prototype.</span></span> <span data-ttu-id="e8edb-154">Durante a configuração interativa, todos os eventos de usuário nas páginas de propriedades fazem com que o assistente de perfil chame a função de retorno de chamada do provedor com base no protótipo [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) .</span><span class="sxs-lookup"><span data-stu-id="e8edb-154">During interactive configuration, every user event in the property pages causes the Profile Wizard to call the provider's callback function based on the [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) prototype.</span></span> 
  
<span data-ttu-id="e8edb-155">Se um provedor de serviços adicionado ao perfil oferecer suporte às páginas do assistente de perfil, ele deverá permitir a configuração programática do perfil.</span><span class="sxs-lookup"><span data-stu-id="e8edb-155">If a service provider being added to the profile supports the Profile Wizard pages, it must allow programmatic configuration of the profile.</span></span>
  

