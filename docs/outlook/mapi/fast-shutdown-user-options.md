---
title: Opções de desligamento rápido do usuário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 220aeab5-20f6-4520-96c9-8aaa0e8ea15b
description: 'Modificado pela última vez: 26 de junho de 2012'
ms.openlocfilehash: a58f8b98ab2f5a5c1028440676a561427272d028
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766523"
---
# <a name="fast-shutdown-user-options"></a><span data-ttu-id="6bf1a-103">Opções de desligamento rápido do usuário</span><span class="sxs-lookup"><span data-stu-id="6bf1a-103">Fast shutdown user options</span></span>

<span data-ttu-id="6bf1a-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6bf1a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6bf1a-105">Este tópico descreve as três Windows configurações do registro que estão disponíveis, iniciando no Microsoft Outlook 2010 e agora, incluindo Microsoft Outlook 2013, para desligamento rápido de clientes MAPI do usuário.</span><span class="sxs-lookup"><span data-stu-id="6bf1a-105">This topic describes the three Windows registry settings that are available, starting in Microsoft Outlook 2010 and now including Microsoft Outlook 2013, for fast shutdown of a user's MAPI clients.</span></span> <span data-ttu-id="6bf1a-106">Os administradores podem usar essas configurações do registro para especificar o comportamento de desligamento do cliente preferencial dependendo suporte dos provedores de MAPI para desligamento rápido do cliente.</span><span class="sxs-lookup"><span data-stu-id="6bf1a-106">Administrators can use these registry settings to specify the preferred client shutdown behavior depending on the MAPI providers' support for client fast shutdown.</span></span> <span data-ttu-id="6bf1a-107">Configuração do administrador, por sua vez, determina como o subsistema de MAPI responde a chamada do cliente MAPI para [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) em termos de suporte de desligamento rápido disponíveis.</span><span class="sxs-lookup"><span data-stu-id="6bf1a-107">The administrator's setting, in turn, determines how the MAPI subsystem responds to the MAPI client's call to [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) in terms of available fast shutdown support.</span></span> 
  
<span data-ttu-id="6bf1a-108">Embora uma configuração de registro reflete a preferência do administrador no nível do usuário para o desligamento rápido para todos os clientes MAPI, um desenvolvedor de cliente MAPI pode decidir se o cliente suporta desligamento rápido independentemente de outros clientes MAPI e o configuração de registro do administrador.</span><span class="sxs-lookup"><span data-stu-id="6bf1a-108">Even though a registry setting reflects the administrator's preference at the user level for fast shutdown for all MAPI clients, a MAPI client developer can decide whether the client supports fast shutdown independently of other MAPI clients and the administrator's registry setting.</span></span> <span data-ttu-id="6bf1a-109">No entanto, para o desligamento rápido ocorrência com êxito, o usuário deve ter a configuração de registro necessárias, um cliente MAPI deve iniciar o desligamento rápido usando o [IMAPIClientShutdown: IUnknown](imapiclientshutdowniunknown.md) interface e os provedores MAPI que funcionam com o cliente deverá implementar o [IMAPIProviderShutdown: IUnknown](imapiprovidershutdowniunknown.md) interface para suportar o desligamento rápido do cliente.</span><span class="sxs-lookup"><span data-stu-id="6bf1a-109">Nonetheless, for fast shutdown to take place successfully, the user must have the necessary registry setting, a MAPI client must initiate the fast shutdown by using the [IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md) interface, and MAPI providers that work with the client should implement the [IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md) interface to support client fast shutdown.</span></span> 
  
<span data-ttu-id="6bf1a-110">A lista a seguir descreve as três opções de nível do usuário.</span><span class="sxs-lookup"><span data-stu-id="6bf1a-110">The following list describes the three user-level options.</span></span>
  
### <a name="option-1-the-mapi-subsystem-enables-fast-shutdown-unless-mapi-providers-explicitly-opt-out"></a><span data-ttu-id="6bf1a-111">Opção 1: O subsistema de MAPI habilita o desligamento rápido, a menos que provedores MAPI explicitamente rejeitar</span><span class="sxs-lookup"><span data-stu-id="6bf1a-111">Option 1: The MAPI subsystem enables fast shutdown, unless MAPI providers explicitly opt out</span></span> 
    
<span data-ttu-id="6bf1a-112">No Outlook 2010, isso é iniciar o comportamento padrão quando o Outlook é o cliente MAPI; não é necessariamente o comportamento padrão de outros clientes MAPI.</span><span class="sxs-lookup"><span data-stu-id="6bf1a-112">Starting in Outlook 2010, this is the default behavior when Outlook is the MAPI client; it is not necessarily the default behavior for other MAPI clients.</span></span> <span data-ttu-id="6bf1a-113">Para especificar explicitamente essa opção para o Outlook, os administradores podem optar definir a seguinte chave do registro e o valor.</span><span class="sxs-lookup"><span data-stu-id="6bf1a-113">To explicitly specify this option for Outlook, administrators can choose to set the following registry key and value.</span></span>
    
<span data-ttu-id="6bf1a-114">Chave do registro:</span><span class="sxs-lookup"><span data-stu-id="6bf1a-114">Registry key:</span></span>
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
<span data-ttu-id="6bf1a-115">Valor:</span><span class="sxs-lookup"><span data-stu-id="6bf1a-115">Value:</span></span>
  
>  `"FastShutdownBehavior"=dword:00000000`
    
<span data-ttu-id="6bf1a-116">Quando um cliente MAPI inicia um desligamento rápido e chama **IMAPIClientShutdown::QueryFastShutdown** a consulta para suporte de desligamento rápido, o subsistema de MAPI responde à consulta retornando S\_Okey contanto que nenhum provedor MAPI que tenha um ativo MAPI sessão com o cliente MAPI tem explicitamente aceitos sem suporte de desligamento rápido.</span><span class="sxs-lookup"><span data-stu-id="6bf1a-116">When a MAPI client initiates a fast shutdown and calls **IMAPIClientShutdown::QueryFastShutdown** to query for fast shutdown support, the MAPI subsystem responds to the query by returning S\_OK as long as no MAPI provider that has an active MAPI session with the MAPI client has explicitly opted out of fast shutdown support.</span></span> 

<span data-ttu-id="6bf1a-117">Um provedor MAPI recusa sem desligamento rápido Implementando o método [IMAPIProviderShutdown::QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) para retornar um erro (MAPI\_f\_não\_suporte).</span><span class="sxs-lookup"><span data-stu-id="6bf1a-117">A MAPI provider opts out of fast shutdown by implementing the [IMAPIProviderShutdown::QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) method to return an error (MAPI\_E\_NO\_SUPPORT).</span></span> <span data-ttu-id="6bf1a-118">Se um ou mais provedores MAPI retornam um erro em **IMAPIProviderShutdown::QueryFastShutdown**, o subsistema de MAPI retorna MAPI_\E_\NO\_suporte para **IMAPIClientShutdown::QueryFastShutdown**.</span><span class="sxs-lookup"><span data-stu-id="6bf1a-118">If one or more MAPI providers return an error in **IMAPIProviderShutdown::QueryFastShutdown**, the MAPI subsystem returns MAPI_\E_\NO\_SUPPORT to **IMAPIClientShutdown::QueryFastShutdown**.</span></span> 

<span data-ttu-id="6bf1a-119">A menos que um provedor MAPI recusa, o retorna do subsistema MAPI S\_Okey, mesmo se um ou mais provedores não implementou o **IMAPIProviderShutdown: IUnknown** interface.</span><span class="sxs-lookup"><span data-stu-id="6bf1a-119">Unless a MAPI provider opts out, the MAPI subsystem returns S\_OK, even if one or more providers have not implemented the **IMAPIProviderShutdown : IUnknown** interface.</span></span> 
    
### <a name="option-2-the-mapi-subsystem-enables-fast-shutdown-only-if-every-mapi-provider-explicitly-opts-in"></a><span data-ttu-id="6bf1a-120">Opção 2: O subsistema de MAPI habilita o desligamento rápido somente se cada provedor MAPI recusa explicitamente em</span><span class="sxs-lookup"><span data-stu-id="6bf1a-120">Option 2: The MAPI subsystem enables fast shutdown only if every MAPI provider explicitly opts in</span></span> 
    
<span data-ttu-id="6bf1a-121">Os administradores devem definir explicitamente a seguinte chave do registro e o valor para especificar essa preferência para desligamento rápido do cliente.</span><span class="sxs-lookup"><span data-stu-id="6bf1a-121">Administrators must explicitly set the following registry key and value to specify this preference for client fast shutdown.</span></span>
    
<span data-ttu-id="6bf1a-122">Chave do registro:</span><span class="sxs-lookup"><span data-stu-id="6bf1a-122">Registry key:</span></span>
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
<span data-ttu-id="6bf1a-123">Valor:</span><span class="sxs-lookup"><span data-stu-id="6bf1a-123">Value:</span></span>
  
>  `"FastShutdownBehavior"=dword:00000001`
    
<span data-ttu-id="6bf1a-124">Quando um cliente MAPI inicia um desligamento rápido e chama **IMAPIClientShutdown::QueryFastShutdown** a consulta para suporte de desligamento rápido, o subsistema de MAPI responde à consulta retornando S\_Okey se todos os provedores MAPI que tiver sessões ativas com desligamento rápido do suporte de cliente MAPI.</span><span class="sxs-lookup"><span data-stu-id="6bf1a-124">When a MAPI client initiates a fast shutdown and calls **IMAPIClientShutdown::QueryFastShutdown** to query for fast shutdown support, the MAPI subsystem responds to the query by returning S\_OK if all MAPI providers that have active sessions with the MAPI client support fast shutdown.</span></span> <span data-ttu-id="6bf1a-125">Um provedor MAPI demonstra seu suporte por meio da implementação **IMAPIProviderShutdown::QueryFastShutdown** para retornar um código de erro não (S\_Okey).</span><span class="sxs-lookup"><span data-stu-id="6bf1a-125">A MAPI provider demonstrates its support by implementing **IMAPIProviderShutdown::QueryFastShutdown** to return a non-error code (S\_OK).</span></span> 

<span data-ttu-id="6bf1a-126">Se um ou mais desses provedores MAPI retornarem MAPI\_f\_não\_suporte, ou não implementar **IMAPIProviderShutdown::QueryFastShutdown**, o subsistema de MAPI retorna um código de erro ao **IMAPIClientShutdown::QueryFastShutdown** .</span><span class="sxs-lookup"><span data-stu-id="6bf1a-126">If one or more such MAPI providers return MAPI\_E\_NO\_SUPPORT, or do not implement **IMAPIProviderShutdown::QueryFastShutdown**, the MAPI subsystem returns an error code to **IMAPIClientShutdown::QueryFastShutdown**.</span></span>
    
### <a name="option-3-an-administrator-disables-support-for-client-fast-shutdown"></a><span data-ttu-id="6bf1a-127">Opção 3: Administrador desabilita o suporte para desligamento rápido do cliente</span><span class="sxs-lookup"><span data-stu-id="6bf1a-127">Option 3: An administrator disables support for client fast shutdown</span></span>
    
<span data-ttu-id="6bf1a-128">Os administradores devem definir explicitamente a seguinte chave do registro e o valor para desabilitar o suporte para desligamento rápido do cliente.</span><span class="sxs-lookup"><span data-stu-id="6bf1a-128">Administrators must explicitly set the following registry key and value to disable support for client fast shutdown.</span></span>
    
<span data-ttu-id="6bf1a-129">Chave do registro:</span><span class="sxs-lookup"><span data-stu-id="6bf1a-129">Registry key:</span></span>
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
<span data-ttu-id="6bf1a-130">Valor:</span><span class="sxs-lookup"><span data-stu-id="6bf1a-130">Value:</span></span>
  
>  `"FastShutdownBehavior"=dword:00000002`
    
<span data-ttu-id="6bf1a-131">Quando um cliente MAPI inicia um desligamento rápido e chama **IMAPIClientShutdown::QueryFastShutdown** a consulta para suporte de desligamento rápido, o subsistema de MAPI responde à consulta, retornando MAPI_E_NO_SUPPORT, independentemente se qualquer provedor MAPI suporta rápida desligamento.</span><span class="sxs-lookup"><span data-stu-id="6bf1a-131">When a MAPI client initiates a fast shutdown and calls **IMAPIClientShutdown::QueryFastShutdown** to query for fast shutdown support, the MAPI subsystem responds to the query by returning MAPI_E_NO_SUPPORT, regardless of whether any MAPI provider supports fast shutdown.</span></span> <span data-ttu-id="6bf1a-132">Sob esta configuração do registro, o subsistema de MAPI nunca chama o método **IMAPIProviderShutdown::QueryFastShutdown** ou [IMAPIProviderShutdown::DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) de qualquer um dos provedores.</span><span class="sxs-lookup"><span data-stu-id="6bf1a-132">Under this registry setting, the MAPI subsystem never calls the **IMAPIProviderShutdown::QueryFastShutdown** or [IMAPIProviderShutdown::DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) method of any of the providers.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="6bf1a-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="6bf1a-133">See also</span></span>

- [<span data-ttu-id="6bf1a-134">Desligamento do cliente em MAPI</span><span class="sxs-lookup"><span data-stu-id="6bf1a-134">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)
- [<span data-ttu-id="6bf1a-135">Visão geral de desligamento rápido</span><span class="sxs-lookup"><span data-stu-id="6bf1a-135">Fast Shutdown Overview</span></span>](fast-shutdown-overview.md)
- [<span data-ttu-id="6bf1a-136">Práticas recomendadas para desligamento rápido</span><span class="sxs-lookup"><span data-stu-id="6bf1a-136">Best Practices for Fast Shutdown</span></span>](best-practices-for-fast-shutdown.md)

