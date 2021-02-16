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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437382"
---
# <a name="launchwizardentry"></a><span data-ttu-id="525bd-103">LAUNCHWIZARDENTRY</span><span class="sxs-lookup"><span data-stu-id="525bd-103">LAUNCHWIZARDENTRY</span></span>

  
  
<span data-ttu-id="525bd-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="525bd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="525bd-105">Define uma função que inicia o aplicativo Assistente de Perfil com a finalidade de adicionar um ou mais serviços de mensagem a um perfil.</span><span class="sxs-lookup"><span data-stu-id="525bd-105">Defines a function that starts the Profile Wizard application for the purpose of adding one or more message services to a profile.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="525bd-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="525bd-106">Header file:</span></span>  <br/> |<span data-ttu-id="525bd-107">Mapiwz.h</span><span class="sxs-lookup"><span data-stu-id="525bd-107">Mapiwz.h</span></span>  <br/> |
|<span data-ttu-id="525bd-108">Função definida implementada por:</span><span class="sxs-lookup"><span data-stu-id="525bd-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="525bd-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="525bd-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="525bd-110">Função definida chamada por:</span><span class="sxs-lookup"><span data-stu-id="525bd-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="525bd-111">Aplicativos do cliente</span><span class="sxs-lookup"><span data-stu-id="525bd-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT LAUNCHWIZARDENTRY(
  HWND hParentWnd,
  ULONG ulFlags,
  LPCSTR FAR * lppszServiceNameToAdd,
  ULONG cbBufferMax,
  LPSTR lpszNewProfileName
);
```

## <a name="parameters"></a><span data-ttu-id="525bd-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="525bd-112">Parameters</span></span>

 <span data-ttu-id="525bd-113">_hParentWnd_</span><span class="sxs-lookup"><span data-stu-id="525bd-113">_hParentWnd_</span></span>
  
> <span data-ttu-id="525bd-114">[in] Um alça para a janela pai do chamador.</span><span class="sxs-lookup"><span data-stu-id="525bd-114">[in] A handle to the caller's parent window.</span></span> <span data-ttu-id="525bd-115">Se o chamador não tiver uma janela pai, o  _parâmetro hParentWnd_ deverá ser NULL.</span><span class="sxs-lookup"><span data-stu-id="525bd-115">If the caller does not have a parent window, the  _hParentWnd_ parameter should be NULL.</span></span> 
    
 <span data-ttu-id="525bd-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="525bd-116">_ulFlags_</span></span>
  
> <span data-ttu-id="525bd-117">[in] Máscara de bits de sinalizadores indicando opções para o Assistente de Perfil.</span><span class="sxs-lookup"><span data-stu-id="525bd-117">[in] Bitmask of flags indicating options for the Profile Wizard.</span></span> <span data-ttu-id="525bd-118">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="525bd-118">The following flags can be set:</span></span>
    
<span data-ttu-id="525bd-119">MAPI_PW_ADD_SERVICE_ONLY</span><span class="sxs-lookup"><span data-stu-id="525bd-119">MAPI_PW_ADD_SERVICE_ONLY</span></span> 
  
> <span data-ttu-id="525bd-120">O Assistente de Perfil é para adicionar apenas os serviços de mensagem listados por meio do parâmetro  _lppszServiceNameToAdd_ e não exibir sua página para selecionar serviços de mensagem.</span><span class="sxs-lookup"><span data-stu-id="525bd-120">The Profile Wizard is to add only the message services listed through the  _lppszServiceNameToAdd_ parameter, and not display its page for selecting message services.</span></span> 
    
<span data-ttu-id="525bd-121">MAPI_PW_FIRST_PROFILE</span><span class="sxs-lookup"><span data-stu-id="525bd-121">MAPI_PW_FIRST_PROFILE</span></span> 
  
> <span data-ttu-id="525bd-122">O perfil a ser criado é o primeiro para esta estação de trabalho.</span><span class="sxs-lookup"><span data-stu-id="525bd-122">The profile to be created is the first one for this workstation.</span></span> 
    
<span data-ttu-id="525bd-123">MAPI_PW_HIDE_SERVICES_LIST</span><span class="sxs-lookup"><span data-stu-id="525bd-123">MAPI_PW_HIDE_SERVICES_LIST</span></span> 
  
> <span data-ttu-id="525bd-124">A página do Assistente de Perfil para selecionar serviços de mensagem não deve ser exibida.</span><span class="sxs-lookup"><span data-stu-id="525bd-124">The Profile Wizard's page for selecting message services should not be displayed.</span></span> 
    
<span data-ttu-id="525bd-125">MAPI_PW_LAUNCHED_BY_CONFIG</span><span class="sxs-lookup"><span data-stu-id="525bd-125">MAPI_PW_LAUNCHED_BY_CONFIG</span></span> 
  
> <span data-ttu-id="525bd-126">O Assistente de Perfil foi lançado pelo aplicativo de configuração do Painel de Controle.</span><span class="sxs-lookup"><span data-stu-id="525bd-126">The Profile Wizard was launched by the Control Panel configuration application.</span></span> 
    
<span data-ttu-id="525bd-127">MAPI_PW_PROVIDER_UI_ONLY</span><span class="sxs-lookup"><span data-stu-id="525bd-127">MAPI_PW_PROVIDER_UI_ONLY</span></span> 
  
> <span data-ttu-id="525bd-128">Somente as caixas de diálogo de configuração dos provedores de serviços devem ser exibidas e as páginas do Assistente de Perfil não devem aparecer.</span><span class="sxs-lookup"><span data-stu-id="525bd-128">Only the service providers's configuration dialog boxes should be displayed and the Profile Wizard's pages should not appear.</span></span> <span data-ttu-id="525bd-129">Esse sinalizador só poderá ser definido se o sinalizador MAPI_PW_ADD_SERVICE_ONLY estiver definido.</span><span class="sxs-lookup"><span data-stu-id="525bd-129">This flag can only be set if the MAPI_PW_ADD_SERVICE_ONLY flag is set.</span></span> 
    
 <span data-ttu-id="525bd-130">_lppszServiceNameToAdd_</span><span class="sxs-lookup"><span data-stu-id="525bd-130">_lppszServiceNameToAdd_</span></span>
  
> <span data-ttu-id="525bd-131">[in] Ponteiro para uma matriz de cadeias de caracteres que contém os nomes dos serviços de mensagem a serem adicionados ao perfil.</span><span class="sxs-lookup"><span data-stu-id="525bd-131">[in] Pointer to an array of strings that contains the names of the message services to be added to the profile.</span></span> <span data-ttu-id="525bd-132">A matriz deve terminar com um valor NULL.</span><span class="sxs-lookup"><span data-stu-id="525bd-132">The array must terminate with a NULL value.</span></span> 
    
 <span data-ttu-id="525bd-133">_cbBufferMax_</span><span class="sxs-lookup"><span data-stu-id="525bd-133">_cbBufferMax_</span></span>
  
> <span data-ttu-id="525bd-134">[in] Tamanho do buffer apontado pelo parâmetro _lpszNewProfileName._</span><span class="sxs-lookup"><span data-stu-id="525bd-134">[in] Size of the buffer pointed to by the  _lpszNewProfileName_ parameter.</span></span> 
    
 <span data-ttu-id="525bd-135">_lpszNewProfileName_</span><span class="sxs-lookup"><span data-stu-id="525bd-135">_lpszNewProfileName_</span></span>
  
> <span data-ttu-id="525bd-136">[out] Ponteiro para um buffer de cadeia de caracteres em que a função baseada em **LAUNCHWIZARDENTRY** retorna o nome do perfil criado.</span><span class="sxs-lookup"><span data-stu-id="525bd-136">[out] Pointer to a string buffer where the function based on **LAUNCHWIZARDENTRY** returns the name of the created profile.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="525bd-137">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="525bd-137">Return value</span></span>

<span data-ttu-id="525bd-138">S_OK</span><span class="sxs-lookup"><span data-stu-id="525bd-138">S_OK</span></span> 
  
> <span data-ttu-id="525bd-139">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="525bd-139">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="525bd-140">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="525bd-140">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="525bd-141">Um erro de origem inesperada ou desconhecida impedia a conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="525bd-141">An error of unexpected or unknown origin prevented the operation from completing.</span></span> <span data-ttu-id="525bd-142">As possibilidades incluem falha ao inicializar o subsistema MAPI para o Assistente de Perfil, a incapacidade de acessar o perfil padrão e um retorno de erro da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="525bd-142">Possibilities include failure to initialize the MAPI subsystem for the Profile Wizard, inability to access the default profile, and an error return from the dialog box.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="525bd-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="525bd-143">Remarks</span></span>

<span data-ttu-id="525bd-144">A implementação MAPI do protótipo **da função LAUNCHWIZARDENTRY** é o ponto de entrada no aplicativo assistente de perfil MAPI.</span><span class="sxs-lookup"><span data-stu-id="525bd-144">The MAPI implementation of the **LAUNCHWIZARDENTRY** function prototype is the entry point into the MAPI Profile Wizard application.</span></span> <span data-ttu-id="525bd-145">MAPI nomes este ponto de entrada **LaunchWizard**.</span><span class="sxs-lookup"><span data-stu-id="525bd-145">MAPI names this entry point **LaunchWizard**.</span></span> 
  
<span data-ttu-id="525bd-146">Quando o MAPI_PW_ADD_SERVICE_ONLY padrão é definido no  _parâmetro ulFlags,_ as seguintes regras se aplicam:</span><span class="sxs-lookup"><span data-stu-id="525bd-146">When the MAPI_PW_ADD_SERVICE_ONLY flag is set in the  _ulFlags_ parameter, the following rules apply:</span></span> 
  
- <span data-ttu-id="525bd-147">O MAPI_PW_LAUNCHED_BY_CONFIG sinalizador impede que a página de boas-vindas seja exibida.</span><span class="sxs-lookup"><span data-stu-id="525bd-147">The MAPI_PW_LAUNCHED_BY_CONFIG flag inhibits the welcome page from being displayed.</span></span> 
    
- <span data-ttu-id="525bd-148">Os MAPI_PW_HIDE_SERVICES_LIST e MAPI_PW_PROVIDER_UI_ONLY padrão são úteis somente quando não há um perfil padrão.</span><span class="sxs-lookup"><span data-stu-id="525bd-148">The MAPI_PW_HIDE_SERVICES_LIST and MAPI_PW_PROVIDER_UI_ONLY flags are useful only when there is no default profile.</span></span> <span data-ttu-id="525bd-149">Nesse caso, esses sinalizadores determinam qual página do Assistente de Perfil deve ser exibida.</span><span class="sxs-lookup"><span data-stu-id="525bd-149">In this case these flags determine which Profile Wizard page is to be displayed.</span></span> 
    
- <span data-ttu-id="525bd-150">Se existir um perfil padrão, nenhuma das páginas do Assistente de Perfil será exibida.</span><span class="sxs-lookup"><span data-stu-id="525bd-150">If a default profile exists, none of the Profile Wizard pages are to be displayed.</span></span> 
    
- <span data-ttu-id="525bd-151">Se existir um perfil padrão, apenas um serviço de mensagem será listado por meio do parâmetro  _lppszServiceNameToAdd_ e esse serviço de mensagem já estiver no perfil padrão, o Assistente de Perfil retornará S_OK sem adicionar nada ao perfil.</span><span class="sxs-lookup"><span data-stu-id="525bd-151">If a default profile exists, only one message service is listed through the  _lppszServiceNameToAdd_ parameter, and that message service is already in the default profile, the Profile Wizard returns S_OK without adding anything to the profile.</span></span> 
    
<span data-ttu-id="525bd-152">Para cada serviço de mensagem a ser adicionado ao perfil, o Assistente de Perfil chama a função de ponto de entrada do serviço com base no protótipo [MSGSERVICEENTRY.](msgserviceentry.md)</span><span class="sxs-lookup"><span data-stu-id="525bd-152">For every message service to be added to the profile, the Profile Wizard calls the service's entry point function based on the [MSGSERVICEENTRY](msgserviceentry.md) prototype.</span></span> <span data-ttu-id="525bd-153">Para cada provedor de serviços selecionado de um serviço de mensagem a ser adicionado ao perfil, o Assistente de Perfil chama a função de ponto de entrada do provedor com base no protótipo [WIZARDENTRY.](wizardentry.md)</span><span class="sxs-lookup"><span data-stu-id="525bd-153">For each service provider selected from a message service to be added to the profile, the Profile Wizard calls the provider's entry point function based on the [WIZARDENTRY](wizardentry.md) prototype.</span></span> <span data-ttu-id="525bd-154">Durante a configuração interativa, cada evento de usuário nas páginas de propriedades faz com que o Assistente de Perfil chame a função de retorno de chamada do provedor com base no protótipo [SERVICEWIZARDDLGPROC.](servicewizarddlgproc.md)</span><span class="sxs-lookup"><span data-stu-id="525bd-154">During interactive configuration, every user event in the property pages causes the Profile Wizard to call the provider's callback function based on the [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) prototype.</span></span> 
  
<span data-ttu-id="525bd-155">Se um provedor de serviços adicionado ao perfil suportar as páginas do Assistente de Perfil, ele deverá permitir a configuração programática do perfil.</span><span class="sxs-lookup"><span data-stu-id="525bd-155">If a service provider being added to the profile supports the Profile Wizard pages, it must allow programmatic configuration of the profile.</span></span>
  

