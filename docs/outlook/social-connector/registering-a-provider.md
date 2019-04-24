---
title: Registrar um provedor
manager: soliver
ms.date: 03/05/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b60b3634-4c8b-4273-97a0-0a8a5a8a5342
description: Este tópico descreve os locais do registro do Windows que são usados quando você instala um provedor do Outlook Social Connector (OSC).
ms.openlocfilehash: a5f76850f9bebcba3c2bff31e799a3b012d6b91a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329208"
---
# <a name="registering-a-provider"></a><span data-ttu-id="0592d-103">Registrar um provedor</span><span class="sxs-lookup"><span data-stu-id="0592d-103">Registering a provider</span></span>

<span data-ttu-id="0592d-104">Este tópico descreve os locais do registro do Windows que são usados quando você instala um provedor do Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="0592d-104">This topic describes the Windows registry locations that are used when you install an Outlook Social Connector (OSC) provider.</span></span>
  
## <a name="com-registration"></a><span data-ttu-id="0592d-105">Registro COM</span><span class="sxs-lookup"><span data-stu-id="0592d-105">COM registration</span></span>

<span data-ttu-id="0592d-106">Você deve configurar a DLL do provedor OSC para se registrar usando o auto-registro de COM ou regsvr32 durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="0592d-106">You must configure the OSC provider DLL to register using COM self-registration or regsvr32 during installation.</span></span> <span data-ttu-id="0592d-107">O registro COM da DLL do provedor registra o provedor OSC no `HKEY_CLASSES_ROOT` hive do registro.</span><span class="sxs-lookup"><span data-stu-id="0592d-107">COM registration of the provider DLL registers the OSC provider under the `HKEY_CLASSES_ROOT` registry hive.</span></span> 
  
<span data-ttu-id="0592d-108">Um provedor OSC desenvolvido em código gerenciado tem um assembly de provedor visível COM.</span><span class="sxs-lookup"><span data-stu-id="0592d-108">An OSC provider developed in managed code has a COM-visible provider assembly.</span></span> <span data-ttu-id="0592d-109">Você deve usar um domínio de aplicativo separado para o componente do provedor.</span><span class="sxs-lookup"><span data-stu-id="0592d-109">You should use a separate application domain for the provider component.</span></span> <span data-ttu-id="0592d-110">Caso contrário, o provedor OSC usa o domínio de aplicativo compartilhado padrão usado por outros componentes, e o provedor pode não funcionar conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="0592d-110">Otherwise, the OSC provider uses the default shared application domain that is used by other components, and the provider may not operate as expected.</span></span>
  
## <a name="registering-provider-progid"></a><span data-ttu-id="0592d-111">Registrando ProgID do provedor</span><span class="sxs-lookup"><span data-stu-id="0592d-111">Registering provider ProgID</span></span>

<span data-ttu-id="0592d-112">Cada provedor do OSC deve registrar um identificador de`ProgID`programação ().</span><span class="sxs-lookup"><span data-stu-id="0592d-112">Each OSC provider must register a programmatic identifier (`ProgID`).</span></span> <span data-ttu-id="0592d-113">O instalador do provedor pode escolher um dos seguintes locais para adicionar ou remover `ProgID`:</span><span class="sxs-lookup"><span data-stu-id="0592d-113">The provider installer can choose one of the following locations to add or remove the `ProgID`:</span></span>
  
- <span data-ttu-id="0592d-114">`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash; Seu instalador de provedor deve usar esse local se o provedor estiver instalado apenas para o usuário conectado no momento.</span><span class="sxs-lookup"><span data-stu-id="0592d-114">`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` &ndash; Your provider installer should use this location if the provider is installed for only the currently logged-on user.</span></span>
    
- <span data-ttu-id="0592d-115">`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash; Seu instalador de provedor deve usar esse local se o provedor estiver instalado para todos os usuários no computador.</span><span class="sxs-lookup"><span data-stu-id="0592d-115">`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` &ndash; Your provider installer should use this location if the provider is installed for all users on the computer.</span></span>
    
<span data-ttu-id="0592d-116">O OSC procura o provedor `ProgID` nos locais acima, a menos que o computador cliente tenha o Outlook de 32 bits em execução em um sistema operacional Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="0592d-116">The OSC looks for the provider  `ProgID` in the above locations, unless the client computer has 32-bit Outlook running on a 64-bit Windows operating system.</span></span> <span data-ttu-id="0592d-117">Nesse caso, o instalador do provedor deve escolher um dos seguintes locais no `HKEY_CURRENT_USER` ou `HKEY_LOCAL_MACHINE` Hive:</span><span class="sxs-lookup"><span data-stu-id="0592d-117">In such a case, your provider installer should choose one of the following locations in the  `HKEY_CURRENT_USER` or  `HKEY_LOCAL_MACHINE` hive:</span></span> 
  
- `HKEY_CURRENT_USER\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
<span data-ttu-id="0592d-118">Para uma versão de clique para executar do Office, seu instalador de provedor deve escolher um dos seguintes locais no hive HKEY_CURRENT_USER ou HKEY_LOCAL_MACHINE:</span><span class="sxs-lookup"><span data-stu-id="0592d-118">For a Click-to-Run version of Office, your provider installer should choose one of the following locations in the HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE hive:</span></span>
  
- `HKEY_CURRENT_USER\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Outlook\SocialConnector\SocialProviders`
    
## <a name="see-also"></a><span data-ttu-id="0592d-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="0592d-119">See also</span></span>

- [<span data-ttu-id="0592d-120">Lista de verificação da instalação</span><span class="sxs-lookup"><span data-stu-id="0592d-120">Installation Checklist</span></span>](installation-checklist.md)
- [<span data-ttu-id="0592d-121">Etapas rápidas para aprender a desenvolver um provedor</span><span class="sxs-lookup"><span data-stu-id="0592d-121">Quick Steps for Learning to Develop a Provider</span></span>](quick-steps-for-learning-to-develop-a-provider.md)
- [<span data-ttu-id="0592d-122">Implantar um provedor</span><span class="sxs-lookup"><span data-stu-id="0592d-122">Deploying a Provider</span></span>](deploying-a-provider.md)

