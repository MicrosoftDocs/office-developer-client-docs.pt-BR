---
title: Referência do provedor do Outlook Social Connector
manager: soliver
ms.date: 04/04/2016
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 13661393-adf6-4870-86c4-303262317675
description: O Outlook Social Connector 2013 oferece um hub de comunicação para comunicação pessoal e profissional.
ms.openlocfilehash: e570fe69cbbe0e8d472e712fb3b8592c97fe43c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359833"
---
# <a name="outlook-social-connector-provider-reference"></a><span data-ttu-id="aed0e-103">Referência do provedor do Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="aed0e-103">Outlook Social Connector provider reference</span></span>

<span data-ttu-id="aed0e-104">O Outlook Social Connector 2013 oferece um hub de comunicação para comunicação pessoal e profissional.</span><span class="sxs-lookup"><span data-stu-id="aed0e-104">The Outlook Social Connector 2013 provides a communication hub for personal and professional communications.</span></span> <span data-ttu-id="aed0e-105">O Outlook Social Connector (OSC) funciona com o SharePoint Server, com o SharePoint Workspace, com o cliente do Lync e todos os aplicativos de cliente do Office que oferecem suporte de informações de presença e o cartão de visita suportam a OSC.</span><span class="sxs-lookup"><span data-stu-id="aed0e-105">The Outlook Social Connector (OSC) works with SharePoint Server, SharePoint Workspace, Lync client, and all Office client applications that support presence information and the Contact Card support the OSC.</span></span> 

<span data-ttu-id="aed0e-106">No Outlook em particular, basta selecionar um item do Outlook como um email ou solicitação de reunião e clicar em um remetente ou destinatário no item, sem sair do Outlook para que os usuários possam ver nas atividades do painel de pessoas, fotos e atualizações de status dessa pessoa em sua redes sociais favoritas.</span><span class="sxs-lookup"><span data-stu-id="aed0e-106">In Outlook in particular, just by selecting an Outlook item such as an email or meeting request and clicking the sender or a recipient in that item, without leaving Outlook, users can see in the People Pane activities, photos, and status updates of this person on their favorite social networks.</span></span> <span data-ttu-id="aed0e-107">Os usuários podem ver convenientemente todos o emails do Outlook, anexos e reuniões recebidos dessa pessoa.</span><span class="sxs-lookup"><span data-stu-id="aed0e-107">Users can conveniently see all the Outlook emails, attachments, and meetings received from this person.</span></span> <span data-ttu-id="aed0e-108">Em um ambiente organizacional, os usuários em um site do SharePoint também podem ver as atualizações de documento do painel de pessoas e outras atividades de site dessa pessoa no site do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="aed0e-108">In an organizational environment, users on a SharePoint site can also see in the People Pane document updates and other site activities of this person on the SharePoint site.</span></span>
  
<span data-ttu-id="aed0e-109">Uma rede social pode desenvolver um provedor OSC para sincronizar e exibir as atualizações de rede social no suporte servidores e aplicativos.</span><span class="sxs-lookup"><span data-stu-id="aed0e-109">A social network can develop a provider for the OSC to synchronize and surface social network updates in supporting servers and applications.</span></span> <span data-ttu-id="aed0e-110">Redes sociais como o LinkedIn, Facebook e o Windows Live oferecem provedores para o OSC.</span><span class="sxs-lookup"><span data-stu-id="aed0e-110">Popular social networks such as LinkedIn, Facebook, and Windows Live are offering providers for the OSC.</span></span> 
  
<span data-ttu-id="aed0e-111">A Referência para Provedores do Outlook Social Connector 2013 (OSC) descreve como desenvolver um provedor OSC usando a extensibilidade de provedores OSC.</span><span class="sxs-lookup"><span data-stu-id="aed0e-111">The Outlook Social Connector 2013 Provider Reference describes how to develop an OSC provider using OSC provider extensibility.</span></span> 
  
<span data-ttu-id="aed0e-112">Se você está começando a desenvolver soluções para o Outlook, confira [Selecionando uma API e tecnologia para desenvolver soluções para o Outlook](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md) para identificar as APIs e tecnologias mais adequadas às suas necessidades.</span><span class="sxs-lookup"><span data-stu-id="aed0e-112">If you are new to developing solutions for Outlook, see [Selecting an API or technology for developing solutions for Outlook](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md) to identify the APIs and technologies that are most appropriate for your needs.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="aed0e-113">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="aed0e-113">In this section</span></span>

- <span data-ttu-id="aed0e-114">[Introdução ao desenvolvimento de um provedor do Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md): fornece uma visão geral do OSC, incluindo o seguinte: como um provedor de OSC pode ser útil, passos rápidos para saber desenvolver um provedor, requisitos técnicos, melhores práticas para desenvolver um provedor e quais são as novidades nesta versão.</span><span class="sxs-lookup"><span data-stu-id="aed0e-114">[Getting Started with Developing an Outlook Social Connector Provider](getting-started-with-developing-an-outlook-social-connector-provider.md): Provides an overview of the OSC, including the following: how an OSC provider can be useful, quick steps for learning to develop a provider, technical requirements, best practices for developing a provider, and what's new in this release.</span></span>
    
- <span data-ttu-id="aed0e-115">[Modelos de exemplo OSC](osc-sample-templates.md): descreve vários modelos do Visual Studio para desenvolver um provedor.</span><span class="sxs-lookup"><span data-stu-id="aed0e-115">[OSC Sample Templates](osc-sample-templates.md): Describes several Visual Studio templates for developing a provider.</span></span>
    
- <span data-ttu-id="aed0e-116">[Sequências de chamadas típicas do OSC](osc-typical-calling-sequences.md): descreve algumas sequências de chamadas típicas para o OSC dos membros nas interfaces de extensibilidade do provedor OSC.</span><span class="sxs-lookup"><span data-stu-id="aed0e-116">[OSC Typical Calling Sequences](osc-typical-calling-sequences.md): Describes a few typical calling sequences by the OSC of members in the OSC provider extensibility interfaces.</span></span> <span data-ttu-id="aed0e-117">Isso deve permitir que você entenda melhor como implementar esses interfaces.</span><span class="sxs-lookup"><span data-stu-id="aed0e-117">This should enable you to better understand how to implement these interfaces.</span></span>
    
- <span data-ttu-id="aed0e-118">[Desenvolvimento de um provedor de esquema XML OSC](developing-a-provider-with-the-osc-xml-schema.md):descreve como a interface de extensibilidade do provedor OSC e o esquema XML OSC são projetados para dar suporte a um provedor do OSC.</span><span class="sxs-lookup"><span data-stu-id="aed0e-118">[Developing a Provider with the OSC XML Schema](developing-a-provider-with-the-osc-xml-schema.md): Describes how the OSC provider extensibility interfaces and OSC XML schema are designed to support an OSC provider.</span></span>
    
- <span data-ttu-id="aed0e-119">[Depuração de provedor](debugging-a-provider.md): sugere várias maneiras de ajudar a depurar um provedor do OSC.</span><span class="sxs-lookup"><span data-stu-id="aed0e-119">[Debugging a Provider](debugging-a-provider.md): Suggests a few ways to help debug an OSC provider.</span></span>
    
- <span data-ttu-id="aed0e-120">[Implantação de provedor](deploying-a-provider.md): descreve os requisitos de registro para um provedor de OSC e fornece uma lista de verificação para instalar um provedor.</span><span class="sxs-lookup"><span data-stu-id="aed0e-120">[Deploying a Provider](deploying-a-provider.md): Describes registration requirements for an OSC provider, and provides a checklist for installing a provider.</span></span>
    
- <span data-ttu-id="aed0e-121">[Preparando-se para lançar um provedor de OSC](getting-ready-to-release-an-osc-provider.md): sugere teste que você pode fazer antes de lançar um provedor do OSC.</span><span class="sxs-lookup"><span data-stu-id="aed0e-121">[Getting Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md): Suggests tests you can do before releasing an OSC provider.</span></span>
    
- <span data-ttu-id="aed0e-122">[Referência de provedor do Outlook Social Connector](outlook-social-connector-provider-reference-0.md): fornece informações de referência para as interfaces de extensibilidade do provedor OSC, para o esquema XML OSC e lista os possíveis códigos de erro.</span><span class="sxs-lookup"><span data-stu-id="aed0e-122">[Outlook Social Connector Provider Reference](outlook-social-connector-provider-reference-0.md): Provides reference information for the OSC provider extensibility interfaces and OSC XML schema, and lists possible error codes.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="aed0e-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="aed0e-123">See also</span></span>

- [<span data-ttu-id="aed0e-124">Aviso de direitos autorais da referência do provedor do Outlook Social Connector 2013</span><span class="sxs-lookup"><span data-stu-id="aed0e-124">Outlook Social Connector 2013 provider reference copyright notice</span></span>](outlook-social-connector-2013-provider-reference-copyright-notice.md) 
- [<span data-ttu-id="aed0e-125">Convenções de Documentos</span><span class="sxs-lookup"><span data-stu-id="aed0e-125">Document Conventions</span></span>](https://msdn.microsoft.com/office/aa905365.aspx)   
- [<span data-ttu-id="aed0e-126">Acessibilidade em produtos Microsoft</span><span class="sxs-lookup"><span data-stu-id="aed0e-126">Accessibility in Microsoft Products</span></span>](https://www.microsoft.com/enable/products/default.aspx)  
- [<span data-ttu-id="aed0e-127">Aviso de Privacidade do Microsoft Online</span><span class="sxs-lookup"><span data-stu-id="aed0e-127">Microsoft Online Privacy Notice</span></span>](https://privacy.microsoft.com/pt-BR/privacystatement)
    

