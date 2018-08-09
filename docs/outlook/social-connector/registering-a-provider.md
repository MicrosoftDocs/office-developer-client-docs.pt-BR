---
title: Registrar um provedor
manager: soliver
ms.date: 03/05/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b60b3634-4c8b-4273-97a0-0a8a5a8a5342
description: Este tópico descreve os locais de registro do Windows que são usados quando você instala um provedor do Outlook Social Connector (OSC).
ms.openlocfilehash: 3ec594ec94b045d2ceb583144781a5746b945b5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770944"
---
# <a name="registering-a-provider"></a><span data-ttu-id="20375-103">Registrar um provedor</span><span class="sxs-lookup"><span data-stu-id="20375-103">Registering a provider</span></span>

<span data-ttu-id="20375-104">Este tópico descreve os locais de registro do Windows que são usados quando você instala um provedor do Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="20375-104">This topic describes the Windows registry locations that are used when you install an Outlook Social Connector (OSC) provider.</span></span>
  
## <a name="com-registration"></a><span data-ttu-id="20375-105">Registro COM</span><span class="sxs-lookup"><span data-stu-id="20375-105">COM registration</span></span>

<span data-ttu-id="20375-106">Você deve configurar o provedor OSC DLL para registrar usando o registro de autoatendimento COM ou regsvr32 durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="20375-106">You must configure the OSC provider DLL to register using COM self-registration or regsvr32 during installation.</span></span> <span data-ttu-id="20375-107">Registro de COM do provedor DLL registra o provedor de OSC sob o `HKEY_CLASSES_ROOT` hive do registro.</span><span class="sxs-lookup"><span data-stu-id="20375-107">COM registration of the provider DLL registers the OSC provider under the `HKEY_CLASSES_ROOT` registry hive.</span></span> 
  
<span data-ttu-id="20375-108">Um provedor OSC desenvolvido em código gerenciado tem um assembly do provedor COM visíveis.</span><span class="sxs-lookup"><span data-stu-id="20375-108">An OSC provider developed in managed code has a COM-visible provider assembly.</span></span> <span data-ttu-id="20375-109">Você deve usar um domínio de aplicativo separado para o componente do provedor.</span><span class="sxs-lookup"><span data-stu-id="20375-109">You should use a separate application domain for the provider component.</span></span> <span data-ttu-id="20375-110">Caso contrário, o provedor do OSC usa o domínio de aplicativo compartilhado padrão que é usado por outros componentes e o provedor pode não funcionar conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="20375-110">Otherwise, the OSC provider uses the default shared application domain that is used by other components, and the provider may not operate as expected.</span></span>
  
## <a name="registering-provider-progid"></a><span data-ttu-id="20375-111">Registrando provedor ProgID</span><span class="sxs-lookup"><span data-stu-id="20375-111">Registering provider ProgID</span></span>

<span data-ttu-id="20375-112">Cada provedor OSC deve registrar um identificador de programação (`ProgID`).</span><span class="sxs-lookup"><span data-stu-id="20375-112">Each OSC provider must register a programmatic identifier (`ProgID`).</span></span> <span data-ttu-id="20375-113">O instalador do provedor pode escolher um dos seguintes locais para adicionar ou remover o `ProgID`:</span><span class="sxs-lookup"><span data-stu-id="20375-113">The provider installer can choose one of the following locations to add or remove the `ProgID`:</span></span>
  
- <span data-ttu-id="20375-114">`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash; o instalador do seu provedor deve usar este local, se o provedor está instalado para que apenas o usuário conectado no momento.</span><span class="sxs-lookup"><span data-stu-id="20375-114">`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` &ndash; Your provider installer should use this location if the provider is installed for only the currently logged-on user.</span></span>
    
- <span data-ttu-id="20375-115">`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash; o instalador do seu provedor deve usar este local, se o provedor está instalado para todos os usuários no computador.</span><span class="sxs-lookup"><span data-stu-id="20375-115">`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` &ndash; Your provider installer should use this location if the provider is installed for all users on the computer.</span></span>
    
<span data-ttu-id="20375-116">O OSC procura o provedor `ProgID` nos locais acima, a menos que o computador cliente tem o Outlook de 32 bits em execução em um sistema de operacional do Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="20375-116">The OSC looks for the provider  `ProgID` in the above locations, unless the client computer has 32-bit Outlook running on a 64-bit Windows operating system.</span></span> <span data-ttu-id="20375-117">Nesse caso, o instalador do seu provedor deve escolher um dos seguintes locais, no `HKEY_CURRENT_USER` ou `HKEY_LOCAL_MACHINE` hive:</span><span class="sxs-lookup"><span data-stu-id="20375-117">In such a case, your provider installer should choose one of the following locations in the  `HKEY_CURRENT_USER` or  `HKEY_LOCAL_MACHINE` hive:</span></span> 
  
- `HKEY_CURRENT_USER\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
<span data-ttu-id="20375-118">Para obter uma versão Click-to-Run do Office, o instalador do seu provedor deve escolher um dos seguintes locais no hive HKEY_CURRENT_USER ou HKEY_LOCAL_MACHINE:</span><span class="sxs-lookup"><span data-stu-id="20375-118">For a Click-to-Run version of Office, your provider installer should choose one of the following locations in the HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE hive:</span></span>
  
- `HKEY_CURRENT_USER\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Outlook\SocialConnector\SocialProviders`
    
## <a name="see-also"></a><span data-ttu-id="20375-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="20375-119">See also</span></span>

- [<span data-ttu-id="20375-120">Lista de verificação de instalação</span><span class="sxs-lookup"><span data-stu-id="20375-120">Installation Checklist</span></span>](installation-checklist.md)
- [<span data-ttu-id="20375-121">Etapas rápidas de aprendizado para desenvolver um provedor</span><span class="sxs-lookup"><span data-stu-id="20375-121">Quick Steps for Learning to Develop a Provider</span></span>](quick-steps-for-learning-to-develop-a-provider.md)
- [<span data-ttu-id="20375-122">Implantando um provedor</span><span class="sxs-lookup"><span data-stu-id="20375-122">Deploying a Provider</span></span>](deploying-a-provider.md)

