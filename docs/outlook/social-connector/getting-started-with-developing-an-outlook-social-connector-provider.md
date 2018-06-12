---
title: Introdução ao desenvolvimento de um Outlook Social Connector provider
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1c65d2df-86a3-48d5-9fec-a9040f3b878c
description: Referência do provedor do Outlook Social Connector (OSC) descreve como desenvolver um provedor OSC usando estensibilidade do provedor do OSC.
ms.openlocfilehash: 19f5ffe8987d0b19017692ddb8f7888be2140033
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770817"
---
# <a name="getting-started-with-developing-an-outlook-social-connector-provider"></a><span data-ttu-id="d9e4a-103">Introdução ao desenvolvimento de um Outlook Social Connector provider</span><span class="sxs-lookup"><span data-stu-id="d9e4a-103">Getting started with developing an Outlook Social Connector provider</span></span>

<span data-ttu-id="d9e4a-104">Referência do provedor do Outlook Social Connector (OSC) descreve como desenvolver um provedor OSC usando estensibilidade do provedor do OSC.</span><span class="sxs-lookup"><span data-stu-id="d9e4a-104">The Outlook Social Connector (OSC) Provider Reference describes how to develop an OSC provider by using OSC provider extensibility.</span></span> <span data-ttu-id="d9e4a-105">Se você é novo no desenvolvimento de soluções para o Outlook, consulte [selecionando um API ou tecnologia para desenvolver soluções do Outlook](http://msdn.microsoft.com/library/8295da20-e567-4d08-b8e4-5c9b4498edd4%28Office.15%29.aspx) para identificar as APIs e tecnologias que são mais apropriadas para suas necessidades.</span><span class="sxs-lookup"><span data-stu-id="d9e4a-105">If you are new to developing solutions for Outlook, see [Selecting an API or Technology for Developing Outlook Solutions](http://msdn.microsoft.com/library/8295da20-e567-4d08-b8e4-5c9b4498edd4%28Office.15%29.aspx) to identify the APIs and technologies that are most appropriate for your needs.</span></span> 

<span data-ttu-id="d9e4a-106">Esta seção fornece uma visão geral do OSC, como um provedor OSC pode ser útil, rápidas etapas de aprendizado para desenvolver um provedor, requisitos técnicos, práticas recomendadas para o desenvolvimento de um provedor e o que há de novo nesta versão.</span><span class="sxs-lookup"><span data-stu-id="d9e4a-106">This section gives an overview of the OSC, how an OSC provider can be useful, quick steps for learning to develop a provider, technical requirements, best practices for developing a provider, and what's new in this release.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="d9e4a-107">Nesta se��o</span><span class="sxs-lookup"><span data-stu-id="d9e4a-107">In this section</span></span>

- <span data-ttu-id="d9e4a-108">[What's New for Providers](what-s-new-for-providers.md): OSC compara recursos na versão anterior e atual e descreve os membros de interface e os elementos de esquema XML que foram adicionados, alterados ou preteridos nesta versão.</span><span class="sxs-lookup"><span data-stu-id="d9e4a-108">[What's New for Providers](what-s-new-for-providers.md): Compares OSC features in the previous and current release, and describes interface members and XML schema elements that have been added, changed, or deprecated in this release.</span></span> 
    
- <span data-ttu-id="d9e4a-109">[Por que desenvolver um Outlook Social Connector Provider](why-develop-an-outlook-social-connector-provider.md): descreve como um provedor OSC pode ser útil para sites de rede social comuns e outras ferramentas de redes internas.</span><span class="sxs-lookup"><span data-stu-id="d9e4a-109">[Why Develop an Outlook Social Connector Provider](why-develop-an-outlook-social-connector-provider.md): Describes how an OSC provider can be useful for common social network sites and other internal networking tools.</span></span>
    
- <span data-ttu-id="d9e4a-110">[Relacionando o OSC com o Outlook e redes sociais](relating-the-osc-with-outlook-and-social-networks.md): fornece uma visão de arquitetura de como o OSC se conecta usuários do Outlook com redes sociais.</span><span class="sxs-lookup"><span data-stu-id="d9e4a-110">[Relating the OSC with Outlook and Social Networks](relating-the-osc-with-outlook-and-social-networks.md): Provides an architectural view of how the OSC connects Outlook users with social networks.</span></span> <span data-ttu-id="d9e4a-111">Também define a forma como esse termos comuns, como "redes sociais", "amigos", "não-amigos," e "contacts" são usados no restante desta referência.</span><span class="sxs-lookup"><span data-stu-id="d9e4a-111">Also defines the way that common terms, like "social networks," "friends," "non-friends," and "contacts" are used in the rest of this reference.</span></span>
    
- <span data-ttu-id="d9e4a-112">[Etapas rápidas de aprendizado para desenvolver um provedor](quick-steps-for-learning-to-develop-a-provider.md): fornece um resumo das etapas para aprender a desenvolver um provedor OSC.</span><span class="sxs-lookup"><span data-stu-id="d9e4a-112">[Quick Steps for Learning to Develop a Provider](quick-steps-for-learning-to-develop-a-provider.md): Provides a summary of steps to learn to develop an OSC provider.</span></span>
    
- <span data-ttu-id="d9e4a-113">[Requisitos técnicos](technical-requirements.md): descreve as linguagens de programação suportadas, requisitos de visibilidade de COM, requisitos de tipo de retorno do método e detalhes de extensibilidade do provedor do OSC DLL.</span><span class="sxs-lookup"><span data-stu-id="d9e4a-113">[Technical Requirements](technical-requirements.md): Describes the supported programming languages, COM visibility requirements, method return type requirements, and details of the OSC provider extensibility DLL.</span></span>
    
- <span data-ttu-id="d9e4a-114">[Práticas recomendadas para o desenvolvimento de um provedor](best-practices-for-developing-a-provider.md): fornece uma lista de práticas recomendadas a seguir ao desenvolver um provedor OSC.</span><span class="sxs-lookup"><span data-stu-id="d9e4a-114">[Best Practices for Developing a Provider](best-practices-for-developing-a-provider.md): Provides a list of best practices to follow while developing an OSC provider.</span></span>
    
## <a name="reference"></a><span data-ttu-id="d9e4a-115">Refer�ncia</span><span class="sxs-lookup"><span data-stu-id="d9e4a-115">Reference</span></span>

- [<span data-ttu-id="d9e4a-116">Referência do provedor do Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="d9e4a-116">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="d9e4a-117">Se��es relacionadas</span><span class="sxs-lookup"><span data-stu-id="d9e4a-117">Related sections</span></span>

- [<span data-ttu-id="d9e4a-118">Modelos de amostra do OSC</span><span class="sxs-lookup"><span data-stu-id="d9e4a-118">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="d9e4a-119">Sequências de chamadas comuns do OSC</span><span class="sxs-lookup"><span data-stu-id="d9e4a-119">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)
  
- [<span data-ttu-id="d9e4a-120">Desenvolvendo um provedor com o esquema OSC XML</span><span class="sxs-lookup"><span data-stu-id="d9e4a-120">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)
  
- [<span data-ttu-id="d9e4a-121">Depurando um provedor</span><span class="sxs-lookup"><span data-stu-id="d9e4a-121">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="d9e4a-122">Implantando um provedor</span><span class="sxs-lookup"><span data-stu-id="d9e4a-122">Deploying a Provider</span></span>](deploying-a-provider.md)
  
- [<span data-ttu-id="d9e4a-123">Preparando-se para o lançamento de um provedor OSC</span><span class="sxs-lookup"><span data-stu-id="d9e4a-123">Getting Ready to Release an OSC Provider</span></span>](getting-ready-to-release-an-osc-provider.md)
  
## <a name="see-also"></a><span data-ttu-id="d9e4a-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="d9e4a-124">See also</span></span>

- [<span data-ttu-id="d9e4a-125">32 bits do Microsoft Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="d9e4a-125">Microsoft Outlook Social Connector 32-bit</span></span>](http://www.microsoft.com/downloads/details.aspx?FamilyID=b638cc14-11e5-448a-b5a6-4f553ce81b94)
- [<span data-ttu-id="d9e4a-126">Atualização para o Outlook Social Connector (KB983403), edição de 32 bits</span><span class="sxs-lookup"><span data-stu-id="d9e4a-126">Update for Outlook Social Connector (KB983403), 32-Bit Edition</span></span>](http://www.microsoft.com/downloads/details.aspx?FamilyID=9886faca-f1c5-4579-83e2-c872c7abc61a)
- [<span data-ttu-id="d9e4a-127">Atualização para o Outlook Social Connector (KB983403), edição de 64 bits</span><span class="sxs-lookup"><span data-stu-id="d9e4a-127">Update for Outlook Social Connector (KB983403), 64-bit Edition</span></span>](http://www.microsoft.com/downloads/details.aspx?FamilyID=72a506a7-8a91-4d56-8b27-bf3b3f58fe9a)
- [<span data-ttu-id="d9e4a-128">Conector Social do Outlook 2013: Modelos de provedor</span><span class="sxs-lookup"><span data-stu-id="d9e4a-128">Outlook Social Connector 2013: Provider templates</span></span>](http://code.msdn.microsoft.com/Outlook-Social-Connector-73fd8d2c)

