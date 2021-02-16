---
title: Desenvolver um provedor com o esquema XML OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0872b1b9-c21f-4bba-8cf1-4b010d8d7fb6
description: O esquema de provedor XML do Outlook Social Connector (OSC)define o formato de uma quantidade significativa de informações que passam de uma rede social através de um provedor do OSC da rede para o OSC.
ms.openlocfilehash: 2346e23beb2de1664ec90263a8f5db5d46c54e6f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539252"
---
# <a name="developing-a-provider-with-the-osc-xml-schema"></a><span data-ttu-id="c73bf-103">Desenvolver um provedor com o esquema XML OSC</span><span class="sxs-lookup"><span data-stu-id="c73bf-103">Developing a provider with the OSC XML schema</span></span>

<span data-ttu-id="c73bf-104">O esquema de provedor XML do Outlook Social Connector (OSC)define o formato de uma quantidade significativa de informações que passam de uma rede social através de um provedor do OSC da rede para o OSC.</span><span class="sxs-lookup"><span data-stu-id="c73bf-104">The Outlook Social Connector (OSC) provider XML schema defines the format of a significant amount of information that is passed from a social network through the network's OSC provider to the OSC.</span></span> <span data-ttu-id="c73bf-105">O esquema XML permite que um provedor de OSC especifique as funcionalidades do provedor, amigos e itens do feed de atividades na rede social, usando os três principais elementos **funcionalidades**, **amigos** e **feed de o atividades** e seus elementos filhos.</span><span class="sxs-lookup"><span data-stu-id="c73bf-105">The XML schema allows an OSC provider to specify capabilities of the provider, friends, and activity feed items on the social network, by using the three main elements, **capabilities**, **friends**, and **activityFeed**, and their child elements.</span></span> <span data-ttu-id="c73bf-106">O provedor OSC implementa interfaces e seus métodos na extensibilidade OSC do provedor, retornando cadeias de caracteres XML como parâmetros de saída que estão em conformidade com o esquema OSC do provedor XML.</span><span class="sxs-lookup"><span data-stu-id="c73bf-106">The OSC provider implements interfaces and their methods in the OSC provider extensibility, returning XML strings as output parameters that comply with the OSC provider XML schema.</span></span> <span data-ttu-id="c73bf-107">O OSC chama esses métodos para obter informações que podem entender como definidas pela esquema XML.</span><span class="sxs-lookup"><span data-stu-id="c73bf-107">The OSC calls these methods to obtain information that it can understand as defined by the XML schema.</span></span>
  
> [!NOTE]
> <span data-ttu-id="c73bf-108">A extensibilidade do provedor OSC dá suporte a provedores de depuração, configurando o`DebugProviders` valor da`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector` chave de registro como 1.</span><span class="sxs-lookup"><span data-stu-id="c73bf-108">OSC provider extensibility supports debugging providers by setting the `DebugProviders` value of the  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector` registry key to 1.</span></span> <span data-ttu-id="c73bf-109">Quando você ativa o provedor de depuração de bugs, a OSC valida o provedor de XML em relação a versão do esquema XML OSC que você especifica no atributo XML **xmlns**.</span><span class="sxs-lookup"><span data-stu-id="c73bf-109">When you turn on provider debugging, the OSC validates the provider XML against the version of the OSC XML schema that you specify in the **xmlns** XML attribute.</span></span> <span data-ttu-id="c73bf-110">Para OSC 1.1 e versões do OSC desde o Outlook Social Connector 2013, especificar o atributo **xmlns** da seguinte maneira: `xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd"`</span><span class="sxs-lookup"><span data-stu-id="c73bf-110">For OSC 1.1 and versions of the OSC since Outlook Social Connector 2013, specify the **xmlns** attribute as follows: `xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd"`</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="c73bf-111">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="c73bf-111">In this section</span></span>

- <span data-ttu-id="c73bf-112">[Sincronização de amigos e atividades](synchronizing-friends-and-activities.md): descreve as várias formas que provedores OSC podem sincronizar amigos, não-amigos e atividades em uma rede social.</span><span class="sxs-lookup"><span data-stu-id="c73bf-112">[Synchronizing Friends and Activities](synchronizing-friends-and-activities.md): Describes the various ways that OSC providers can synchronize friends, non-friends, and activities on a social network.</span></span> 
    
- <span data-ttu-id="c73bf-113">[Exemplos de XML provedor OSC](osc-provider-xml-examples.md): inclui exemplos de que mostram como especificar os recursos de um provedor de OSC, amigos e itens do feed de atividades em uma rede social, usando o esquema XML do OSC.</span><span class="sxs-lookup"><span data-stu-id="c73bf-113">[OSC Provider XML Examples](osc-provider-xml-examples.md): Includes XML examples that show how to specify capabilities of an OSC provider, friends, and activity feed items on a social network by using the OSC XML schema.</span></span>
    
- <span data-ttu-id="c73bf-114">[XML para recursos](xml-for-capabilities.md): explica o método – [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) que o OSC usa para obter informações sobre os recursos, expresso nos **recursos** XML do provedor OSC.</span><span class="sxs-lookup"><span data-stu-id="c73bf-114">[XML for Capabilities](xml-for-capabilities.md): Explains the - [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method that the OSC uses to obtain capabilities information, expressed in **capabilities** XML, from the OSC provider.</span></span> <span data-ttu-id="c73bf-115">Esta seção descreve também os elementos XML no esquema XML do provedor OSC que permite que um provedor OSC especifique sua funcionalidade, incluindo a maneira que autentica usuários e sincroniza atividades e os amigos.</span><span class="sxs-lookup"><span data-stu-id="c73bf-115">This section also describes the XML elements in the OSC provider XML schema that allow an OSC provider to specify its functionality, including how it authenticates users and synchronizes friends and activities.</span></span> 
    
- <span data-ttu-id="c73bf-116">[XML para amigos](xml-for-friends.md): fornece exemplos de APIs que usam o OSC para obter informações de amigos, expressas no XML **amigos** do provedor OSC.</span><span class="sxs-lookup"><span data-stu-id="c73bf-116">[XML for Friends](xml-for-friends.md): Gives examples of the APIs that the OSC uses to obtain friends' information, expressed in **friends** XML, from the OSC provider.</span></span> <span data-ttu-id="c73bf-117">Esta seção também descreve os elementos no XML **amigos**.</span><span class="sxs-lookup"><span data-stu-id="c73bf-117">This section also describes elements in the **friends** XML.</span></span> 
    
- <span data-ttu-id="c73bf-118">[XML de atividades](xml-for-activities.md): fornece exemplos de APIs que usam o OSC para obter informações sobre atividades, expressas no XML **feed de atividades** do provedor OSC.</span><span class="sxs-lookup"><span data-stu-id="c73bf-118">[XML for Activities](xml-for-activities.md): Gives examples of the APIs that the OSC uses to obtain activities information, expressed in **activityFeed** XML, from the OSC provider.</span></span> <span data-ttu-id="c73bf-119">Esta seção descreve também os elementos XML no esquema XML do provedor OSC que permitem que um provedor OSC especifique um feed de atividades.</span><span class="sxs-lookup"><span data-stu-id="c73bf-119">This section also describes the XML elements in the OSC provider XML schema that allow an OSC provider to specify an activity feed.</span></span> <span data-ttu-id="c73bf-120">Um feed de atividades inclui a rede na qual o item do feed de atividades teve origem, detalhes de cada item do feed de atividades (como proprietário, tipo e publicar a data da atividade) e o modelo para exibir a atividade.</span><span class="sxs-lookup"><span data-stu-id="c73bf-120">An activity feed includes the network where the activity feed items originated, details of each activity feed item (such as owner, type, and publish date of the activity), and the template to display the activity.</span></span> 
    
## <a name="reference"></a><span data-ttu-id="c73bf-121">Referências</span><span class="sxs-lookup"><span data-stu-id="c73bf-121">Reference</span></span>

- [<span data-ttu-id="c73bf-122">Referência do provedor do Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="c73bf-122">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="c73bf-123">Seções relacionadas</span><span class="sxs-lookup"><span data-stu-id="c73bf-123">Related sections</span></span>

- [<span data-ttu-id="c73bf-124">Introdução ao desenvolvimento de um provedor de serviços do Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="c73bf-124">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [<span data-ttu-id="c73bf-125">Modelos de exemplo do OSC</span><span class="sxs-lookup"><span data-stu-id="c73bf-125">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="c73bf-126">Sequências de chamadas típicas de OSC</span><span class="sxs-lookup"><span data-stu-id="c73bf-126">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)
  
- [<span data-ttu-id="c73bf-127">Depurar um provedor</span><span class="sxs-lookup"><span data-stu-id="c73bf-127">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="c73bf-128">Implantar um provedor</span><span class="sxs-lookup"><span data-stu-id="c73bf-128">Deploying a Provider</span></span>](deploying-a-provider.md)
  
- [<span data-ttu-id="c73bf-129">Práticas recomendadas para o desenvolvimento de um provedor</span><span class="sxs-lookup"><span data-stu-id="c73bf-129">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a><span data-ttu-id="c73bf-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="c73bf-130">See also</span></span>

- [<span data-ttu-id="c73bf-131">Depurar um provedor</span><span class="sxs-lookup"><span data-stu-id="c73bf-131">Debugging a Provider</span></span>](debugging-a-provider.md)

