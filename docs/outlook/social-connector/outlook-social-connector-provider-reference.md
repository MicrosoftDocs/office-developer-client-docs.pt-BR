---
title: Referência do provedor do Outlook Social Connector
manager: soliver
ms.date: 04/04/2016
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 13661393-adf6-4870-86c4-303262317675
description: O Outlook Social Connector 2013 fornece um hub de comunicação para comunicações de pessoais e profissionais.
ms.openlocfilehash: 32a9eb88b7724f8735d0eb8623bb3716ad836a7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770946"
---
# <a name="outlook-social-connector-provider-reference"></a><span data-ttu-id="5e522-103">Referência do provedor do Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="5e522-103">Outlook Social Connector provider reference</span></span>

<span data-ttu-id="5e522-104">O Outlook Social Connector 2013 fornece um hub de comunicação para comunicações de pessoais e profissionais.</span><span class="sxs-lookup"><span data-stu-id="5e522-104">The Outlook Social Connector 2013 provides a communication hub for personal and professional communications.</span></span> <span data-ttu-id="5e522-105">Outlook Social Connector (OSC) funciona com o SharePoint Server, SharePoint Workspace, cliente do Lync, e o OSC de suporte de todos os aplicativos cliente do Office que oferecem suporte a informações de presença e o cartão de visita.</span><span class="sxs-lookup"><span data-stu-id="5e522-105">The Outlook Social Connector (OSC) works with SharePoint Server, SharePoint Workspace, Lync client, and all Office client applications that support presence information and the Contact Card support the OSC.</span></span> 

<span data-ttu-id="5e522-106">No Outlook em particular, basta selecionar um item do Outlook, como um email ou solicitação de reunião e clicando no remetente ou destinatário no que o item, sem sair do Outlook, os usuários podem ver nas atividades de painel pessoas, fotos e atualizações de status dessa pessoa em seus redes sociais favoritas.</span><span class="sxs-lookup"><span data-stu-id="5e522-106">In Outlook in particular, just by selecting an Outlook item such as an email or meeting request and clicking the sender or a recipient in that item, without leaving Outlook, users can see in the People Pane activities, photos, and status updates of this person on their favorite social networks.</span></span> <span data-ttu-id="5e522-107">Usuários podem ver convenientemente todos o Outlook emails, anexos e reuniões recebidas dessa pessoa.</span><span class="sxs-lookup"><span data-stu-id="5e522-107">Users can conveniently see all the Outlook emails, attachments, and meetings received from this person.</span></span> <span data-ttu-id="5e522-108">Em um ambiente organizacional, os usuários em um site do SharePoint também podem ver nas atualizações de documento do painel de pessoas e outras atividades de site desta pessoa no site do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="5e522-108">In an organizational environment, users on a SharePoint site can also see in the People Pane document updates and other site activities of this person on the SharePoint site.</span></span>
  
<span data-ttu-id="5e522-109">Uma rede social pode desenvolver um provedor para que o OSC sincronize e mostre atualizações de redes sociais em aplicativos e servidores com suporte.</span><span class="sxs-lookup"><span data-stu-id="5e522-109">A social network can develop a provider for the OSC to synchronize and surface social network updates in supporting servers and applications.</span></span> <span data-ttu-id="5e522-110">Populares redes sociais, como Windows Live, Facebook e LinkedIn estão oferecendo provedores para que o OSC.</span><span class="sxs-lookup"><span data-stu-id="5e522-110">Popular social networks such as LinkedIn, Facebook, and Windows Live are offering providers for the OSC.</span></span> 
  
<span data-ttu-id="5e522-111">Referência do provedor do Outlook Social Connector 2013 descreve como desenvolver um provedor OSC usando estensibilidade do provedor do OSC.</span><span class="sxs-lookup"><span data-stu-id="5e522-111">The Outlook Social Connector 2013 Provider Reference describes how to develop an OSC provider using OSC provider extensibility.</span></span> 
  
<span data-ttu-id="5e522-112">Se você é novo no desenvolvimento de soluções para o Outlook, consulte [selecionando um API ou tecnologia para desenvolver soluções do Outlook](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md) para identificar as APIs e tecnologias que são mais apropriadas para suas necessidades.</span><span class="sxs-lookup"><span data-stu-id="5e522-112">If you are new to developing solutions for Outlook, see [Selecting an API or technology for developing solutions for Outlook](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md) to identify the APIs and technologies that are most appropriate for your needs.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="5e522-113">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="5e522-113">In this section</span></span>

- <span data-ttu-id="5e522-114">[Introdução ao desenvolvimento de um Outlook Social Connector Provider](getting-started-with-developing-an-outlook-social-connector-provider.md): fornece uma visão geral do OSC, incluindo o seguinte: como um provedor OSC pode ser útil, etapas rápidas de aprendizado para desenvolver um provedor, requisitos técnicos, as práticas recomendadas de desenvolvendo um provedor, e o que há de novo nesta versão.</span><span class="sxs-lookup"><span data-stu-id="5e522-114">[Getting Started with Developing an Outlook Social Connector Provider](getting-started-with-developing-an-outlook-social-connector-provider.md): Provides an overview of the OSC, including the following: how an OSC provider can be useful, quick steps for learning to develop a provider, technical requirements, best practices for developing a provider, and what's new in this release.</span></span>
    
- <span data-ttu-id="5e522-115">[Modelos de amostra OSC](osc-sample-templates.md): descreve vários modelos do Visual Studio para o desenvolvimento de um provedor.</span><span class="sxs-lookup"><span data-stu-id="5e522-115">[OSC Sample Templates](osc-sample-templates.md): Describes several Visual Studio templates for developing a provider.</span></span>
    
- <span data-ttu-id="5e522-116">[Sequências de chamar típica OSC](osc-typical-calling-sequences.md): descreve alguns típicas sequências de chamada pelo OSC de membros nas interfaces de extensibilidade do provedor OSC.</span><span class="sxs-lookup"><span data-stu-id="5e522-116">[OSC Typical Calling Sequences](osc-typical-calling-sequences.md): Describes a few typical calling sequences by the OSC of members in the OSC provider extensibility interfaces.</span></span> <span data-ttu-id="5e522-117">Isso deve habilitar compreender melhor como implementar as interfaces.</span><span class="sxs-lookup"><span data-stu-id="5e522-117">This should enable you to better understand how to implement these interfaces.</span></span>
    
- <span data-ttu-id="5e522-118">[Desenvolvendo um provedor com o esquema OSC XML](developing-a-provider-with-the-osc-xml-schema.md): descreve como o esquema OSC XML e interfaces de extensibilidade do provedor OSC foram projetados para oferecer suporte a um provedor OSC.</span><span class="sxs-lookup"><span data-stu-id="5e522-118">[Developing a Provider with the OSC XML Schema](developing-a-provider-with-the-osc-xml-schema.md): Describes how the OSC provider extensibility interfaces and OSC XML schema are designed to support an OSC provider.</span></span>
    
- <span data-ttu-id="5e522-119">[Depurando um provedor](debugging-a-provider.md): sugere algumas maneiras para ajudar a depurar um provedor OSC.</span><span class="sxs-lookup"><span data-stu-id="5e522-119">[Debugging a Provider](debugging-a-provider.md): Suggests a few ways to help debug an OSC provider.</span></span>
    
- <span data-ttu-id="5e522-120">[Implantando um provedor](deploying-a-provider.md): descreve os requisitos de registro para um provedor OSC e fornece uma lista de verificação para instalar um provedor.</span><span class="sxs-lookup"><span data-stu-id="5e522-120">[Deploying a Provider](deploying-a-provider.md): Describes registration requirements for an OSC provider, and provides a checklist for installing a provider.</span></span>
    
- <span data-ttu-id="5e522-121">[Obtendo pronto para lançamento de um provedor OSC](getting-ready-to-release-an-osc-provider.md): sugere os testes, você pode fazer antes de liberar um provedor OSC.</span><span class="sxs-lookup"><span data-stu-id="5e522-121">[Getting Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md): Suggests tests you can do before releasing an OSC provider.</span></span>
    
- <span data-ttu-id="5e522-122">[Referência do provedor do Outlook Social Connector](outlook-social-connector-provider-reference-0.md): referência de fornece informações para as interfaces de extensibilidade do provedor OSC e esquema OSC XML e códigos de erro possíveis de listas.</span><span class="sxs-lookup"><span data-stu-id="5e522-122">[Outlook Social Connector Provider Reference](outlook-social-connector-provider-reference-0.md): Provides reference information for the OSC provider extensibility interfaces and OSC XML schema, and lists possible error codes.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5e522-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="5e522-123">See also</span></span>

- [<span data-ttu-id="5e522-124">Aviso de direitos autoral da referência Outlook 2013 do conector Social provedor</span><span class="sxs-lookup"><span data-stu-id="5e522-124">Outlook Social Connector 2013 provider reference copyright notice</span></span>](outlook-social-connector-2013-provider-reference-copyright-notice.md) 
- [<span data-ttu-id="5e522-125">Convenções de Documentos</span><span class="sxs-lookup"><span data-stu-id="5e522-125">Document Conventions</span></span>](http://msdn.microsoft.com/en-us/office/aa905365.aspx)   
- [<span data-ttu-id="5e522-126">Accessibility in Microsoft Products</span><span class="sxs-lookup"><span data-stu-id="5e522-126">Accessibility in Microsoft Products</span></span>](http://www.microsoft.com/enable/products/default.aspx)  
- [<span data-ttu-id="5e522-127">Aviso de Privacidade do Microsoft Online</span><span class="sxs-lookup"><span data-stu-id="5e522-127">Microsoft Online Privacy Notice</span></span>](https://privacy.microsoft.com/en-us/privacystatement)
    

