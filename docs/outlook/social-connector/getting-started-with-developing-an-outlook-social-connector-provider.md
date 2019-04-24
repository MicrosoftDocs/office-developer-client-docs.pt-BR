---
title: Introdução ao desenvolvimento de um provedor do Outlook Social Connector
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1c65d2df-86a3-48d5-9fec-a9040f3b878c
description: A Referência para Provedores do Outlook Social Connector (OSC) descreve como desenvolver um provedor do OSC usando a extensibilidade de provedores do OSC.
ms.openlocfilehash: 24f8eabe33103f53e848f055b72fd402bc5dd89a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327157"
---
# <a name="getting-started-with-developing-an-outlook-social-connector-provider"></a><span data-ttu-id="e2f68-103">Introdução ao desenvolvimento de um provedor do Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="e2f68-103">Getting started with developing an Outlook Social Connector provider</span></span>

<span data-ttu-id="e2f68-104">A Referência para Provedores do Outlook Social Connector (OSC) descreve como desenvolver um provedor do OSC usando a extensibilidade de provedores do OSC.</span><span class="sxs-lookup"><span data-stu-id="e2f68-104">The Outlook Social Connector (OSC) Provider Reference describes how to develop an OSC provider by using OSC provider extensibility.</span></span> <span data-ttu-id="e2f68-105">Se você está começando a desenvolver soluções para o Outlook, confira [Selecionar uma API ou tecnologia para desenvolver soluções para o Outlook](https://msdn.microsoft.com/library/8295da20-e567-4d08-b8e4-5c9b4498edd4%28Office.15%29.aspx) para identificar as APIs e tecnologias mais adequadas às suas necessidades.</span><span class="sxs-lookup"><span data-stu-id="e2f68-105">If you are new to developing solutions for Outlook, see [Selecting an API or Technology for Developing Outlook Solutions](https://msdn.microsoft.com/library/8295da20-e567-4d08-b8e4-5c9b4498edd4%28Office.15%29.aspx) to identify the APIs and technologies that are most appropriate for your needs.</span></span> 

<span data-ttu-id="e2f68-106">Esta seção apresenta uma visão geral do OSC, fala sobre como um provedor de OSC pode ser útil, mostra etapas rápidas para desenvolver um provedor, requisitos técnicos e práticas recomendadas para desenvolver um provedor e informa quais são as novidades nesta versão.</span><span class="sxs-lookup"><span data-stu-id="e2f68-106">This section gives an overview of the OSC, how an OSC provider can be useful, quick steps for learning to develop a provider, technical requirements, best practices for developing a provider, and what's new in this release.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="e2f68-107">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="e2f68-107">In this section</span></span>

- <span data-ttu-id="e2f68-108">[Novidades para provedores](what-s-new-for-providers.md): compara recursos do OSC entre a versão anterior e a atual e descreve os membros da interface e os elementos de esquema XML que foram adicionados, alterados ou preteridos nesta versão.</span><span class="sxs-lookup"><span data-stu-id="e2f68-108">[What's New for Providers](what-s-new-for-providers.md): Compares OSC features in the previous and current release, and describes interface members and XML schema elements that have been added, changed, or deprecated in this release.</span></span> 
    
- <span data-ttu-id="e2f68-109">[Por que desenvolver um provedor do Outlook Social Connector](why-develop-an-outlook-social-connector-provider.md): descreve como um provedor do OSC pode ser útil para sites de redes sociais comuns e outras ferramentas de redes internas.</span><span class="sxs-lookup"><span data-stu-id="e2f68-109">[Why Develop an Outlook Social Connector Provider](why-develop-an-outlook-social-connector-provider.md): Describes how an OSC provider can be useful for common social network sites and other internal networking tools.</span></span>
    
- <span data-ttu-id="e2f68-110">[Relacionar o OSC com o Outlook e redes sociais](relating-the-osc-with-outlook-and-social-networks.md): fornece uma visão arquitetural de como o OSC conecta os usuários do Outlook com redes sociais.</span><span class="sxs-lookup"><span data-stu-id="e2f68-110">[Relating the OSC with Outlook and Social Networks](relating-the-osc-with-outlook-and-social-networks.md): Provides an architectural view of how the OSC connects Outlook users with social networks.</span></span> <span data-ttu-id="e2f68-111">Também define a forma como termos comuns, como "redes sociais", "amigos", "não amigos," e "contatos", são usados no restante dessa referência.</span><span class="sxs-lookup"><span data-stu-id="e2f68-111">Also defines the way that common terms, like "social networks," "friends," "non-friends," and "contacts" are used in the rest of this reference.</span></span>
    
- <span data-ttu-id="e2f68-112">[Etapas rápidas para aprender a desenvolver um provedor](quick-steps-for-learning-to-develop-a-provider.md): fornece um resumo das etapas para aprender a desenvolver um provedor do OSC.</span><span class="sxs-lookup"><span data-stu-id="e2f68-112">[Quick Steps for Learning to Develop a Provider](quick-steps-for-learning-to-develop-a-provider.md): Provides a summary of steps to learn to develop an OSC provider.</span></span>
    
- <span data-ttu-id="e2f68-113">[Requisitos técnicos](technical-requirements.md): descreve as linguagens de programação com suporte, os requisitos de visibilidade COM, os requisitos de tipo de retorno de método e os detalhes da extensibilidade de DLL do provedor do OSC.</span><span class="sxs-lookup"><span data-stu-id="e2f68-113">[Technical Requirements](technical-requirements.md): Describes the supported programming languages, COM visibility requirements, method return type requirements, and details of the OSC provider extensibility DLL.</span></span>
    
- <span data-ttu-id="e2f68-114">[Práticas recomendadas para desenvolver um provedor](best-practices-for-developing-a-provider.md): fornece uma listadas práticas recomendadas a acompanhar ao desenvolver um provedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="e2f68-114">[Best Practices for Developing a Provider](best-practices-for-developing-a-provider.md): Provides a list of best practices to follow while developing an OSC provider.</span></span>
    
## <a name="reference"></a><span data-ttu-id="e2f68-115">Referências</span><span class="sxs-lookup"><span data-stu-id="e2f68-115">Reference</span></span>

- [<span data-ttu-id="e2f68-116">Referência do provedor do Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="e2f68-116">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="e2f68-117">Seções relacionadas</span><span class="sxs-lookup"><span data-stu-id="e2f68-117">Related sections</span></span>

- [<span data-ttu-id="e2f68-118">Modelos de exemplo do OSC</span><span class="sxs-lookup"><span data-stu-id="e2f68-118">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="e2f68-119">Sequências de chamada típicas do OSC</span><span class="sxs-lookup"><span data-stu-id="e2f68-119">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)
  
- [<span data-ttu-id="e2f68-120">Desenvolver um provedor com o esquema XML do OSC</span><span class="sxs-lookup"><span data-stu-id="e2f68-120">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)
  
- [<span data-ttu-id="e2f68-121">Depurar um provedor</span><span class="sxs-lookup"><span data-stu-id="e2f68-121">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="e2f68-122">Implantar um provedor</span><span class="sxs-lookup"><span data-stu-id="e2f68-122">Deploying a Provider</span></span>](deploying-a-provider.md)
  
- [<span data-ttu-id="e2f68-123">Preparando um provedor de OSC para lançamento</span><span class="sxs-lookup"><span data-stu-id="e2f68-123">Getting Ready to Release an OSC Provider</span></span>](getting-ready-to-release-an-osc-provider.md)
  
## <a name="see-also"></a><span data-ttu-id="e2f68-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="e2f68-124">See also</span></span>

- [<span data-ttu-id="e2f68-125">Microsoft Outlook Social Connector 32 bits</span><span class="sxs-lookup"><span data-stu-id="e2f68-125">Microsoft Outlook Social Connector 32-bit</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=b638cc14-11e5-448a-b5a6-4f553ce81b94)
- [<span data-ttu-id="e2f68-126">Atualização para o Outlook Social Connector (KB983403), edição de 32 bits</span><span class="sxs-lookup"><span data-stu-id="e2f68-126">Update for Outlook Social Connector (KB983403), 32-Bit Edition</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=9886faca-f1c5-4579-83e2-c872c7abc61a)
- [<span data-ttu-id="e2f68-127">Atualização para o Outlook Social Connector (KB983403), edição de 64 bits</span><span class="sxs-lookup"><span data-stu-id="e2f68-127">Update for Outlook Social Connector (KB983403), 64-bit Edition</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=72a506a7-8a91-4d56-8b27-bf3b3f58fe9a)
- [<span data-ttu-id="e2f68-128">Outlook Social Connector 2013: modelos de provedor</span><span class="sxs-lookup"><span data-stu-id="e2f68-128">Outlook Social Connector 2013: Provider templates</span></span>](https://code.msdn.microsoft.com/Outlook-Social-Connector-73fd8d2c)

