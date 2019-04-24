---
title: Opções do usuário para desligamento rápido
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
api_type:
- COM
ms.assetid: 220aeab5-20f6-4520-96c9-8aaa0e8ea15b
description: 'Última modificação: 26 de junho de 2012'
localization_priority: Priority
ms.openlocfilehash: 3c60862733c6b38e60650ae9daba9bba578fcd58
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341073"
---
# <a name="fast-shutdown-user-options"></a><span data-ttu-id="3dbd8-103">Opções do usuário para desligamento rápido</span><span class="sxs-lookup"><span data-stu-id="3dbd8-103">Fast shutdown user options</span></span>

<span data-ttu-id="3dbd8-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3dbd8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3dbd8-105">Este tópico descreve as três configurações de registro do Windows disponíveis, iniciando com o Microsoft Outlook 2010 e agora incluindo o Microsoft Outlook 2013, para o desligamento rápido de clientes de MAPI de um usuário.</span><span class="sxs-lookup"><span data-stu-id="3dbd8-105">This topic describes the three Windows registry settings that are available, starting in Microsoft Outlook 2010 and now including Microsoft Outlook 2013, for fast shutdown of a user's MAPI clients.</span></span> <span data-ttu-id="3dbd8-106">Os administradores podem usar essas configurações de registro para especificar o comportamento de desligamento preferencial do cliente, dependendo do suporte dos provedores de MAPI para o desligamento rápido do cliente.</span><span class="sxs-lookup"><span data-stu-id="3dbd8-106">Administrators can use these registry settings to specify the preferred client shutdown behavior depending on the MAPI providers' support for client fast shutdown.</span></span> <span data-ttu-id="3dbd8-107">A configuração do administrador, por sua vez, determina como o subsistema de MAPI responde à chamada do cliente de MAPI para [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) em termos de suporte de desligamento rápido disponível.</span><span class="sxs-lookup"><span data-stu-id="3dbd8-107">The administrator's setting, in turn, determines how the MAPI subsystem responds to the MAPI client's call to [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) in terms of available fast shutdown support.</span></span> 
  
<span data-ttu-id="3dbd8-108">Mesmo que uma configuração do registro reflita a preferência do administrador no nível do usuário pelo desligamento rápido de todos os clientes de MAPI, um desenvolvedor de cliente de MAPI poderá decidir se o cliente dará suporte ao desligamento rápido independentemente de outros clientes de MAPI e da configuração do registro do administrador.</span><span class="sxs-lookup"><span data-stu-id="3dbd8-108">Even though a registry setting reflects the administrator's preference at the user level for fast shutdown for all MAPI clients, a MAPI client developer can decide whether the client supports fast shutdown independently of other MAPI clients and the administrator's registry setting.</span></span> <span data-ttu-id="3dbd8-109">No entanto, para que o desligamento rápido ocorra com êxito, o usuário deverá ter a configuração do registro necessária, um cliente de MAPI deverá iniciar o desligamento rápido usando a interface [IMAPIClientShutdown: IUnknown](imapiclientshutdowniunknown.md), e os provedores de MAPI que trabalham com o cliente deverão implementar a interface [IMAPIProviderShutdown: IUnknown](imapiprovidershutdowniunknown.md) para dar suporte ao desligamento rápido do cliente.</span><span class="sxs-lookup"><span data-stu-id="3dbd8-109">Nonetheless, for fast shutdown to take place successfully, the user must have the necessary registry setting, a MAPI client must initiate the fast shutdown by using the [IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md) interface, and MAPI providers that work with the client should implement the [IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md) interface to support client fast shutdown.</span></span> 
  
<span data-ttu-id="3dbd8-110">A lista a seguir descreve as três opções de nível do usuário.</span><span class="sxs-lookup"><span data-stu-id="3dbd8-110">The following list describes the three user-level options.</span></span>
  
### <a name="option-1-the-mapi-subsystem-enables-fast-shutdown-unless-mapi-providers-explicitly-opt-out"></a><span data-ttu-id="3dbd8-111">Opção 1: o subsistema de MAPI permite o desligamento rápido, a menos que os provedores de MAPI recusem explicitamente</span><span class="sxs-lookup"><span data-stu-id="3dbd8-111">Option 1: The MAPI subsystem enables fast shutdown, unless MAPI providers explicitly opt out</span></span> 
    
<span data-ttu-id="3dbd8-112">Começando com o Outlook 2010, esse é o comportamento padrão quando o Outlook é o cliente de MAPI; não é necessariamente o comportamento padrão para outros clientes de MAPI.</span><span class="sxs-lookup"><span data-stu-id="3dbd8-112">Starting in Outlook 2010, this is the default behavior when Outlook is the MAPI client; it is not necessarily the default behavior for other MAPI clients.</span></span> <span data-ttu-id="3dbd8-113">Para especificar explicitamente essa opção para o Outlook, os administradores podem optar por definir o seguinte valor e chave do Registro.</span><span class="sxs-lookup"><span data-stu-id="3dbd8-113">To explicitly specify this option for Outlook, administrators can choose to set the following registry key and value.</span></span>
    
<span data-ttu-id="3dbd8-114">Chave do Registro:</span><span class="sxs-lookup"><span data-stu-id="3dbd8-114">Registry key:</span></span>
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
<span data-ttu-id="3dbd8-115">Valor:</span><span class="sxs-lookup"><span data-stu-id="3dbd8-115">Value:</span></span>
  
>  `"FastShutdownBehavior"=dword:00000000`
    
<span data-ttu-id="3dbd8-116">Quando um cliente de MAPI inicia um desligamento rápido e chama **IMAPIClientShutdown::QueryFastShutdown** para consultar o suporte do desligamento rápido, o subsistema de MAPI responde à consulta retornando S\_OK, desde que nenhum provedor de MAPI que tenha uma sessão de MAPI ativa com o cliente de MAPI tenha recusado explicitamente o suporte do desligamento rápido.</span><span class="sxs-lookup"><span data-stu-id="3dbd8-116">When a MAPI client initiates a fast shutdown and calls **IMAPIClientShutdown::QueryFastShutdown** to query for fast shutdown support, the MAPI subsystem responds to the query by returning S\_OK as long as no MAPI provider that has an active MAPI session with the MAPI client has explicitly opted out of fast shutdown support.</span></span> 

<span data-ttu-id="3dbd8-117">Um provedor de MAPI recusa o desligamento rápido implementando o método [IMAPIProviderShutdown::QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) para retornar um erro (MAPI\_E\_NO\_SUPPORT).</span><span class="sxs-lookup"><span data-stu-id="3dbd8-117">A MAPI provider opts out of fast shutdown by implementing the [IMAPIProviderShutdown::QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) method to return an error (MAPI\_E\_NO\_SUPPORT).</span></span> <span data-ttu-id="3dbd8-118">Se um ou mais provedores de MAPI retornarem um erro em **IMAPIProviderShutdown::QueryFastShutdown**, o subsistema de MAPI retorná MAPI_\E_\NO\_SUPPORT para **IMAPIClientShutdown::QueryFastShutdown**.</span><span class="sxs-lookup"><span data-stu-id="3dbd8-118">If one or more MAPI providers return an error in **IMAPIProviderShutdown::QueryFastShutdown**, the MAPI subsystem returns MAPI_\E_\NO\_SUPPORT to **IMAPIClientShutdown::QueryFastShutdown**.</span></span> 

<span data-ttu-id="3dbd8-119">Se um provedor de MAPI recusar, o subsistema de MAPI retornará S\_OK, mesmo que um ou mais provedores não tenham implementado a interface **IMAPIProviderShutdown: IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="3dbd8-119">Unless a MAPI provider opts out, the MAPI subsystem returns S\_OK, even if one or more providers have not implemented the **IMAPIProviderShutdown : IUnknown** interface.</span></span> 
    
### <a name="option-2-the-mapi-subsystem-enables-fast-shutdown-only-if-every-mapi-provider-explicitly-opts-in"></a><span data-ttu-id="3dbd8-120">Opção 2: o subsistema de MAPI habilita o desligamento rápido somente se cada provedor de MAPI aceitar explicitamente</span><span class="sxs-lookup"><span data-stu-id="3dbd8-120">Option 2: The MAPI subsystem enables fast shutdown only if every MAPI provider explicitly opts in</span></span> 
    
<span data-ttu-id="3dbd8-121">Os administradores devem definir explicitamente o seguinte valor e chave do Registro para especificar essa preferência para o desligamento rápido do cliente.</span><span class="sxs-lookup"><span data-stu-id="3dbd8-121">Administrators must explicitly set the following registry key and value to specify this preference for client fast shutdown.</span></span>
    
<span data-ttu-id="3dbd8-122">Chave do Registro:</span><span class="sxs-lookup"><span data-stu-id="3dbd8-122">Registry key:</span></span>
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
<span data-ttu-id="3dbd8-123">Valor:</span><span class="sxs-lookup"><span data-stu-id="3dbd8-123">Value:</span></span>
  
>  `"FastShutdownBehavior"=dword:00000001`
    
<span data-ttu-id="3dbd8-124">Quando um cliente de MAPI inicia um desligamento rápido e chama \*\*IMAPIClientShutdown::QueryFastShutdown \*\* para consultar o suporte do desligamento rápido, o subsistema de MAPI responde à consulta retornando S\_OK se todos os provedores de MAPI que possuem sessões ativas com o cliente de MAPI derem suporte ao desligamento rápido.</span><span class="sxs-lookup"><span data-stu-id="3dbd8-124">When a MAPI client initiates a fast shutdown and calls **IMAPIClientShutdown::QueryFastShutdown** to query for fast shutdown support, the MAPI subsystem responds to the query by returning S\_OK if all MAPI providers that have active sessions with the MAPI client support fast shutdown.</span></span> <span data-ttu-id="3dbd8-125">Um provedor de MAPI demonstra o suporte implementando **IMAPIProviderShutdown::QueryFastShutdown** para retornar um código de não erro (S\_OK).</span><span class="sxs-lookup"><span data-stu-id="3dbd8-125">A MAPI provider demonstrates its support by implementing **IMAPIProviderShutdown::QueryFastShutdown** to return a non-error code (S\_OK).</span></span> 

<span data-ttu-id="3dbd8-126">Se um ou mais desses provedores de MAPI retornarem MAPI\_E\_NO\_SUPPORT ou não implementarem **IMAPIProviderShutdown::QueryFastShutdown**, o subsistema de MAPI retornará um código de erro para **IMAPIClientShutdown::QueryFastShutdown**.</span><span class="sxs-lookup"><span data-stu-id="3dbd8-126">If one or more such MAPI providers return MAPI\_E\_NO\_SUPPORT, or do not implement **IMAPIProviderShutdown::QueryFastShutdown**, the MAPI subsystem returns an error code to **IMAPIClientShutdown::QueryFastShutdown**.</span></span>
    
### <a name="option-3-an-administrator-disables-support-for-client-fast-shutdown"></a><span data-ttu-id="3dbd8-127">Opção 3: um administrador desabilita o suporte para o desligamento rápido do cliente</span><span class="sxs-lookup"><span data-stu-id="3dbd8-127">Option 3: An administrator disables support for client fast shutdown</span></span>
    
<span data-ttu-id="3dbd8-128">Os administradores devem definir explicitamente o seguinte valor e a chave do Registro para desabilitar o suporte para o desligamento rápido do cliente.</span><span class="sxs-lookup"><span data-stu-id="3dbd8-128">Administrators must explicitly set the following registry key and value to disable support for client fast shutdown.</span></span>
    
<span data-ttu-id="3dbd8-129">Chave do Registro:</span><span class="sxs-lookup"><span data-stu-id="3dbd8-129">Registry key:</span></span>
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
<span data-ttu-id="3dbd8-130">Valor:</span><span class="sxs-lookup"><span data-stu-id="3dbd8-130">Value:</span></span>
  
>  `"FastShutdownBehavior"=dword:00000002`
    
<span data-ttu-id="3dbd8-131">Quando um cliente de MAPI inicia um desligamento rápido e chama **IMAPIClientShutdown::QueryFastShutdown** para consultar o suporte do desligamento rápido, o subsistema de MAPI responde à consulta retornando MAPI_E_NO_SUPPORT, independentemente de se algum provedor de MAPI oferece suporte ao desligamento rápido.</span><span class="sxs-lookup"><span data-stu-id="3dbd8-131">When a MAPI client initiates a fast shutdown and calls **IMAPIClientShutdown::QueryFastShutdown** to query for fast shutdown support, the MAPI subsystem responds to the query by returning MAPI_E_NO_SUPPORT, regardless of whether any MAPI provider supports fast shutdown.</span></span> <span data-ttu-id="3dbd8-132">Nesta configuração de registro, o subsistema de MAPI nunca chama o método **IMAPIProviderShutdown::QueryFastShutdown** ou [IMAPIProviderShutdown::DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) de qualquer dos provedores.</span><span class="sxs-lookup"><span data-stu-id="3dbd8-132">Under this registry setting, the MAPI subsystem never calls the **IMAPIProviderShutdown::QueryFastShutdown** or [IMAPIProviderShutdown::DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) method of any of the providers.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="3dbd8-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="3dbd8-133">See also</span></span>

- [<span data-ttu-id="3dbd8-134">Desligamento do cliente em MAPI</span><span class="sxs-lookup"><span data-stu-id="3dbd8-134">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)
- [<span data-ttu-id="3dbd8-135">Visão geral do desligamento rápido</span><span class="sxs-lookup"><span data-stu-id="3dbd8-135">Fast Shutdown Overview</span></span>](fast-shutdown-overview.md)
- [<span data-ttu-id="3dbd8-136">Práticas recomendadas para o desligamento rápido</span><span class="sxs-lookup"><span data-stu-id="3dbd8-136">Best Practices for Fast Shutdown</span></span>](best-practices-for-fast-shutdown.md)

