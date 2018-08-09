---
title: Desenvolver um provedor com o esquema XML OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0872b1b9-c21f-4bba-8cf1-4b010d8d7fb6
description: O esquema XML de provedor do Outlook Social Connector (OSC) define o formato de uma quantidade significativa de informações que são passadas de uma rede social por meio do provedor do OSC da rede para o OSC.
ms.openlocfilehash: 93df682751146b501a316be62641b8cfd47a74a8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770838"
---
# <a name="developing-a-provider-with-the-osc-xml-schema"></a><span data-ttu-id="d9c96-103">Desenvolver um provedor com o esquema XML OSC</span><span class="sxs-lookup"><span data-stu-id="d9c96-103">Developing a provider with the OSC XML schema</span></span>

<span data-ttu-id="d9c96-104">O esquema XML de provedor do Outlook Social Connector (OSC) define o formato de uma quantidade significativa de informações que são passadas de uma rede social por meio do provedor do OSC da rede para o OSC.</span><span class="sxs-lookup"><span data-stu-id="d9c96-104">The Outlook Social Connector (OSC) provider XML schema defines the format of a significant amount of information that is passed from a social network through the network's OSC provider to the OSC.</span></span> <span data-ttu-id="d9c96-105">O esquema XML permite que um provedor OSC especificar recursos do provedor, amigos e itens de feed na rede social, usando os três elementos principais, **recursos**, **feed de atividades**e **amigos**e seus filhos de atividade elementos.</span><span class="sxs-lookup"><span data-stu-id="d9c96-105">The XML schema allows an OSC provider to specify capabilities of the provider, friends, and activity feed items on the social network, by using the three main elements, **capabilities**, **friends**, and **activityFeed**, and their child elements.</span></span> <span data-ttu-id="d9c96-106">O provedor do OSC implementa interfaces e seus métodos na extensibilidade do provedor do OSC, retornando cadeias de caracteres XML como parâmetros de saída que estão em conformidade com o esquema XML de provedor do OSC.</span><span class="sxs-lookup"><span data-stu-id="d9c96-106">The OSC provider implements interfaces and their methods in the OSC provider extensibility, returning XML strings as output parameters that comply with the OSC provider XML schema.</span></span> <span data-ttu-id="d9c96-107">O OSC chama esses métodos para obter informações que ele pode entender como definido pelo esquema XML.</span><span class="sxs-lookup"><span data-stu-id="d9c96-107">The OSC calls these methods to obtain information that it can understand as defined by the XML schema.</span></span>
  
> [!NOTE]
> <span data-ttu-id="d9c96-108">Estensibilidade do provedor do OSC oferece suporte a provedores de depuração, definindo o `DebugProviders` valor o `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector` a chave do registro como 1.</span><span class="sxs-lookup"><span data-stu-id="d9c96-108">OSC provider extensibility supports debugging providers by setting the `DebugProviders` value of the  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector` registry key to 1.</span></span> <span data-ttu-id="d9c96-109">Quando você ativa a depuração de provedor, o OSC valida o provedor XML contra a versão do esquema OSC XML especificado no atributo **xmlns** XML.</span><span class="sxs-lookup"><span data-stu-id="d9c96-109">When you turn on provider debugging, the OSC validates the provider XML against the version of the OSC XML schema that you specify in the **xmlns** XML attribute.</span></span> <span data-ttu-id="d9c96-110">Para OSC 1.1 e versões do OSC desde o Outlook Social Connector 2013, especifique o atributo **xmlns** da seguinte maneira:`xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd"`</span><span class="sxs-lookup"><span data-stu-id="d9c96-110">For OSC 1.1 and versions of the OSC since Outlook Social Connector 2013, specify the **xmlns** attribute as follows: `xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd"`</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="d9c96-111">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="d9c96-111">In this section</span></span>

- <span data-ttu-id="d9c96-112">[Sincronizando amigos e atividades](synchronizing-friends-and-activities.md): descreve as várias maneiras em que os provedores OSC podem sincronizar amigos, não-amigos e atividades em uma rede social.</span><span class="sxs-lookup"><span data-stu-id="d9c96-112">[Synchronizing Friends and Activities](synchronizing-friends-and-activities.md): Describes the various ways that OSC providers can synchronize friends, non-friends, and activities on a social network.</span></span> 
    
- <span data-ttu-id="d9c96-113">[Exemplos de XML de provedor do OSC](osc-provider-xml-examples.md): exemplos de XML inclui que mostram como especificar recursos de um provedor OSC, amigos e atividade feed itens em uma rede social usando o esquema OSC XML.</span><span class="sxs-lookup"><span data-stu-id="d9c96-113">[OSC Provider XML Examples](osc-provider-xml-examples.md): Includes XML examples that show how to specify capabilities of an OSC provider, friends, and activity feed items on a social network by using the OSC XML schema.</span></span>
    
- <span data-ttu-id="d9c96-114">[XML de recursos](xml-for-capabilities.md): explica-método [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) que o OSC usa para obter informações sobre recursos, expressado em **recursos de** XML, do provedor do OSC.</span><span class="sxs-lookup"><span data-stu-id="d9c96-114">[XML for Capabilities](xml-for-capabilities.md): Explains the - [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method that the OSC uses to obtain capabilities information, expressed in **capabilities** XML, from the OSC provider.</span></span> <span data-ttu-id="d9c96-115">Esta seção também descreve os elementos XML no esquema XML de provedor do OSC que permitem que um provedor OSC especificar sua funcionalidade, incluindo como ele autentica usuários e sincroniza amigos e atividades.</span><span class="sxs-lookup"><span data-stu-id="d9c96-115">This section also describes the XML elements in the OSC provider XML schema that allow an OSC provider to specify its functionality, including how it authenticates users and synchronizes friends and activities.</span></span> 
    
- <span data-ttu-id="d9c96-116">[XML para amigos](xml-for-friends.md): dá exemplos das APIs que o OSC usa para obter informações dos amigos, expressadas em **amigos** XML, do provedor do OSC.</span><span class="sxs-lookup"><span data-stu-id="d9c96-116">[XML for Friends](xml-for-friends.md): Gives examples of the APIs that the OSC uses to obtain friends' information, expressed in **friends** XML, from the OSC provider.</span></span> <span data-ttu-id="d9c96-117">Esta seção também descreve os elementos no **amigos** XML.</span><span class="sxs-lookup"><span data-stu-id="d9c96-117">This section also describes elements in the **friends** XML.</span></span> 
    
- <span data-ttu-id="d9c96-118">[XML para atividades](xml-for-activities.md): dá exemplos das APIs que o OSC usa para obter informações de atividades, expressadas no **feed de atividades** XML, do provedor do OSC.</span><span class="sxs-lookup"><span data-stu-id="d9c96-118">[XML for Activities](xml-for-activities.md): Gives examples of the APIs that the OSC uses to obtain activities information, expressed in **activityFeed** XML, from the OSC provider.</span></span> <span data-ttu-id="d9c96-119">Esta seção também descreve os elementos XML no esquema XML de provedor do OSC que permitem que um provedor OSC especificar um feed de atividade.</span><span class="sxs-lookup"><span data-stu-id="d9c96-119">This section also describes the XML elements in the OSC provider XML schema that allow an OSC provider to specify an activity feed.</span></span> <span data-ttu-id="d9c96-120">Um feed de atividade inclui da rede onde a atividade feed itens se originou, detalhes de cada item de feed de atividade (como proprietário, digite e data da atividade de publicação) e o modelo para exibir a atividade.</span><span class="sxs-lookup"><span data-stu-id="d9c96-120">An activity feed includes the network where the activity feed items originated, details of each activity feed item (such as owner, type, and publish date of the activity), and the template to display the activity.</span></span> 
    
## <a name="reference"></a><span data-ttu-id="d9c96-121">Referência</span><span class="sxs-lookup"><span data-stu-id="d9c96-121">Reference</span></span>

- [<span data-ttu-id="d9c96-122">Referência do provedor do Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="d9c96-122">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="d9c96-123">Se��es relacionadas</span><span class="sxs-lookup"><span data-stu-id="d9c96-123">Related sections</span></span>

- [<span data-ttu-id="d9c96-124">Introdução ao desenvolvimento de um Outlook Social Connector Provider</span><span class="sxs-lookup"><span data-stu-id="d9c96-124">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [<span data-ttu-id="d9c96-125">Modelos de amostra do OSC</span><span class="sxs-lookup"><span data-stu-id="d9c96-125">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="d9c96-126">Sequências de chamadas comuns do OSC</span><span class="sxs-lookup"><span data-stu-id="d9c96-126">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)
  
- [<span data-ttu-id="d9c96-127">Depurando um provedor</span><span class="sxs-lookup"><span data-stu-id="d9c96-127">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="d9c96-128">Implantando um provedor</span><span class="sxs-lookup"><span data-stu-id="d9c96-128">Deploying a Provider</span></span>](deploying-a-provider.md)
  
- [<span data-ttu-id="d9c96-129">Práticas recomendadas para o desenvolvimento de um provedor</span><span class="sxs-lookup"><span data-stu-id="d9c96-129">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a><span data-ttu-id="d9c96-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="d9c96-130">See also</span></span>

- [<span data-ttu-id="d9c96-131">Depurando um provedor</span><span class="sxs-lookup"><span data-stu-id="d9c96-131">Debugging a Provider</span></span>](debugging-a-provider.md)

