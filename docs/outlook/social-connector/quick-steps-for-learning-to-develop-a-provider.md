---
title: Etapas rápidas para aprender a desenvolver um provedor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 13c0ae8c-d268-4bf0-942d-2a6160142f5e
description: Este tópico sugere algumas etapas para aprender sobre como desenvolver um provedor do Outlook Social Connector (OSC).
ms.openlocfilehash: 581997ab257d59062761d97bfef49a88b90bb1e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424214"
---
# <a name="quick-steps-for-learning-to-develop-a-provider"></a><span data-ttu-id="b3091-103">Etapas rápidas para aprender a desenvolver um provedor</span><span class="sxs-lookup"><span data-stu-id="b3091-103">Quick steps for learning to develop a provider</span></span>

<span data-ttu-id="b3091-104">Para desenvolver um provedor OSC, você precisa concluir as seguintes etapas gerais:</span><span class="sxs-lookup"><span data-stu-id="b3091-104">To develop an OSC provider, you need to complete the following general steps:</span></span>
  
- <span data-ttu-id="b3091-105">Implemente as quatro interfaces obrigatórias: [ISocialProvider](isocialprovideriunknown.md), [ISocialSession](isocialsessioniunknown.md), [ISocialProfile](isocialprofileisocialperson.md)e [ISocialPerson](isocialpersoniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="b3091-105">Implement the four mandatory interfaces: [ISocialProvider](isocialprovideriunknown.md), [ISocialSession](isocialsessioniunknown.md), [ISocialProfile](isocialprofileisocialperson.md), and [ISocialPerson](isocialpersoniunknown.md).</span></span> <span data-ttu-id="b3091-106">Dependendo do suporte da rede social para armazenar credenciais de logon em cache, acompanhar uma pessoa na rede social ou sincronizar dinamicamente amigos e suas atividades, talvez você queira implementar a interface [ISocialSession2.](isocialsession2iunknown.md)</span><span class="sxs-lookup"><span data-stu-id="b3091-106">Depending on your social network's support for caching logon credentials, following a person on the social network, or dynamically synchronizing friends and their activities, you might want to implement the [ISocialSession2](isocialsession2iunknown.md) interface.</span></span> 
    
- <span data-ttu-id="b3091-107">Em paralelo com a implementação de interfaces, teste e depure o provedor OSC.</span><span class="sxs-lookup"><span data-stu-id="b3091-107">In parallel with implementing interfaces, test and debug the OSC provider.</span></span> 

- <span data-ttu-id="b3091-108">Implante o provedor OSC.</span><span class="sxs-lookup"><span data-stu-id="b3091-108">Deploy the OSC provider.</span></span>  

- <span data-ttu-id="b3091-109">Faça testes finais antes do lançamento.</span><span class="sxs-lookup"><span data-stu-id="b3091-109">Do final testing before release.</span></span>
    
## <a name="step-a-implementing-interfaces"></a><span data-ttu-id="b3091-110">Etapa A: Implementando interfaces</span><span class="sxs-lookup"><span data-stu-id="b3091-110">Step A: Implementing interfaces</span></span>

<span data-ttu-id="b3091-111">Um provedor OSC implementa interfaces para que o OSC possa usar essas interfaces para obter informações necessárias sobre ou da rede social, por meio do provedor OSC.</span><span class="sxs-lookup"><span data-stu-id="b3091-111">An OSC provider implements interfaces so that the OSC can use these interfaces to obtain necessary information about or from the social network, through the OSC provider.</span></span> <span data-ttu-id="b3091-112">Essas informações incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b3091-112">Such information includes the following:</span></span>
  
- <span data-ttu-id="b3091-113">Como apresentar a caixa de diálogo de logon da conta para um usuário.</span><span class="sxs-lookup"><span data-stu-id="b3091-113">How to present the account logon dialog to a user.</span></span>    
- <span data-ttu-id="b3091-114">Se o provedor oferece suporte à exibição de amigos ou atividades conforme exibido na rede social.</span><span class="sxs-lookup"><span data-stu-id="b3091-114">Whether the provider supports showing friends or activities as displayed on the social network.</span></span>    
- <span data-ttu-id="b3091-115">Como exibir amigos e atividades no Cartão de Visita ou no Painel de Pessoas do Outlook.</span><span class="sxs-lookup"><span data-stu-id="b3091-115">How to display friends and activities in the Contact Card or Outlook People Pane.</span></span>     
- <span data-ttu-id="b3091-116">Quando atualizar as informações de amigos ou atividades no Cartão de Visita ou no Painel de Pessoas.</span><span class="sxs-lookup"><span data-stu-id="b3091-116">When to refresh friends or activities information on the Contact Card or People Pane.</span></span>
    
<span data-ttu-id="b3091-117">As informações são normalmente passadas do provedor para o OSC, na forma de cadeias de caracteres XML como parâmetros de saída dos métodos de interface.</span><span class="sxs-lookup"><span data-stu-id="b3091-117">The information is typically passed from the provider to the OSC, in the form of XML strings as output parameters of interface methods.</span></span> <span data-ttu-id="b3091-118">O OSC e um provedor OSC estão em conformidade com o esquema XML do provedor OSC.</span><span class="sxs-lookup"><span data-stu-id="b3091-118">Both the OSC and an OSC provider comply with the OSC provider XML schema.</span></span> <span data-ttu-id="b3091-119">Portanto, no decorrer da implementação das interfaces, você precisa ter um bom entendimento de como o esquema XML permite especificar informações conforme listado acima.</span><span class="sxs-lookup"><span data-stu-id="b3091-119">Therefore, in the course of implementing the interfaces, you need a good understanding of how the XML schema allows you to specify information as listed above.</span></span> 

<span data-ttu-id="b3091-120">Os recursos a seguir explicam como especificar XML para recursos do provedor, amigos e atividades:</span><span class="sxs-lookup"><span data-stu-id="b3091-120">The following resources explain how to specify XML for provider capabilities, friends, and activities:</span></span>
  
- [<span data-ttu-id="b3091-121">Sequências de chamada típicas do OSC</span><span class="sxs-lookup"><span data-stu-id="b3091-121">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)    
- [<span data-ttu-id="b3091-122">Sincronizar amigos e atividades</span><span class="sxs-lookup"><span data-stu-id="b3091-122">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)    
- [<span data-ttu-id="b3091-123">Exemplo do XML de recursos</span><span class="sxs-lookup"><span data-stu-id="b3091-123">Capabilities XML Example</span></span>](capabilities-xml-example.md)   
- [<span data-ttu-id="b3091-124">XML para recursos</span><span class="sxs-lookup"><span data-stu-id="b3091-124">XML for Capabilities</span></span>](xml-for-capabilities.md)    
- [<span data-ttu-id="b3091-125">Exemplo de XML de amigos</span><span class="sxs-lookup"><span data-stu-id="b3091-125">Friends XML Example</span></span>](friends-xml-example.md)    
- [<span data-ttu-id="b3091-126">XML para amigos</span><span class="sxs-lookup"><span data-stu-id="b3091-126">XML for Friends</span></span>](xml-for-friends.md)   
- [<span data-ttu-id="b3091-127">Exemplo de XML de feed de atividades</span><span class="sxs-lookup"><span data-stu-id="b3091-127">Activity Feed XML Example</span></span>](activity-feed-xml-example.md)   
- [<span data-ttu-id="b3091-128">XML para atividades</span><span class="sxs-lookup"><span data-stu-id="b3091-128">XML for Activities</span></span>](xml-for-activities.md)
    
<span data-ttu-id="b3091-129">Antes de iniciar a implementação, consulte também os tópicos a seguir para economizar tempo posteriormente no processo de depuração:</span><span class="sxs-lookup"><span data-stu-id="b3091-129">Before you start implementation, also consult the following topics to save you time later in the debugging process:</span></span>
  
- [<span data-ttu-id="b3091-130">Requisitos técnicos</span><span class="sxs-lookup"><span data-stu-id="b3091-130">Technical Requirements</span></span>](technical-requirements.md)    
- [<span data-ttu-id="b3091-131">Práticas recomendadas para o desenvolvimento de um provedor</span><span class="sxs-lookup"><span data-stu-id="b3091-131">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)    
- [<span data-ttu-id="b3091-132">Modelos de exemplo do OSC</span><span class="sxs-lookup"><span data-stu-id="b3091-132">OSC Sample Templates</span></span>](osc-sample-templates.md)
    
## <a name="step-b-debugging"></a><span data-ttu-id="b3091-133">Etapa B: depuração</span><span class="sxs-lookup"><span data-stu-id="b3091-133">Step B: Debugging</span></span>

<span data-ttu-id="b3091-134">O tópico [Depurando um Provedor sugere](debugging-a-provider.md) procedimentos de depuração que você pode usar durante o desenvolvimento de um provedor osC.</span><span class="sxs-lookup"><span data-stu-id="b3091-134">The topic [Debugging a Provider](debugging-a-provider.md) suggests debugging procedures you can use while developing an OSC provider.</span></span> 
  
<span data-ttu-id="b3091-135">Enquanto estiver desenvolvendo, você também pode consultar Preparando-se para Lançar um Provedor [OSC](getting-ready-to-release-an-osc-provider.md) para entender melhor o comportamento esperado em determinados cenários (por exemplo, autenticação básica e baseada em formulários).</span><span class="sxs-lookup"><span data-stu-id="b3091-135">While you are developing, you can also refer to [Getting Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md) to gain a better understanding of the expected behavior in certain scenarios (for example, basic and forms-based authentication).</span></span> 
  
## <a name="step-c-deploying"></a><span data-ttu-id="b3091-136">Etapa C: Implantação</span><span class="sxs-lookup"><span data-stu-id="b3091-136">Step C: Deploying</span></span>

<span data-ttu-id="b3091-137">Consulte os tópicos a seguir para saber mais sobre os requisitos de implantação:</span><span class="sxs-lookup"><span data-stu-id="b3091-137">See the following topics to learn about deployment requirements:</span></span>
  
- [<span data-ttu-id="b3091-138">Implantar um provedor</span><span class="sxs-lookup"><span data-stu-id="b3091-138">Deploying a Provider</span></span>](deploying-a-provider.md)    
- [<span data-ttu-id="b3091-139">Registrar um provedor</span><span class="sxs-lookup"><span data-stu-id="b3091-139">Registering a Provider</span></span>](registering-a-provider.md)   
- [<span data-ttu-id="b3091-140">Lista de verificação da instalação</span><span class="sxs-lookup"><span data-stu-id="b3091-140">Installation Checklist</span></span>](installation-checklist.md)
    
## <a name="step-d-final-testing-before-release"></a><span data-ttu-id="b3091-141">Etapa D: Teste final antes do lançamento</span><span class="sxs-lookup"><span data-stu-id="b3091-141">Step D: Final testing before release</span></span>

<span data-ttu-id="b3091-142">Dependendo da sua rede social e do provedor OSC, geralmente há testes específicos do provedor que você deve realizar antes de liberar seu provedor.</span><span class="sxs-lookup"><span data-stu-id="b3091-142">Depending on your social network and the OSC provider, there are usually provider-specific tests you should carry out before you release your provider.</span></span> <span data-ttu-id="b3091-143">Para obter uma lista sugerida de testes, consulte [Getting Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b3091-143">For a suggested list of tests, see [Getting Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b3091-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="b3091-144">See also</span></span>

- [<span data-ttu-id="b3091-145">Introdução ao desenvolvimento de um provedor de serviços do Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="b3091-145">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

