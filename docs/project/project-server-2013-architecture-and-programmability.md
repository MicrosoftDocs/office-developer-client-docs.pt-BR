---
title: Arquitetura e programação do Project Server 2013
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
f1_keywords:
- architecture
- platform
- Project
- Project architecture
- Project programmability
- Project Server architecture
- Project Server programmability
keywords:
- project 2013, arquitetura e programação, programabilidade, Project Server,Project 2013, benefícios para EPM, arquitetura e Project Server
localization_priority: Normal
ms.assetid: 9ea3b3c1-fb90-454a-b8e6-abc44fca663d
description: Os artigos nesta seção descrevem a arquitetura geral da solução Enterprise Project Management (EPM), que combina o Project Professional 2013, o Project Server 2013, o Project Web App e o SharePoint Server 2013.
ms.openlocfilehash: 44cd5a32b8d3de421ffe3b2d9bf0137146bc4c4e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413784"
---
# <a name="project-server-2013-architecture-and-programmability"></a><span data-ttu-id="41d9d-104">Arquitetura e programação do Project Server 2013</span><span class="sxs-lookup"><span data-stu-id="41d9d-104">Project Server 2013 architecture and programmability</span></span>

<span data-ttu-id="41d9d-105">Os artigos nesta seção descrevem a arquitetura geral da solução Enterprise Project Management (EPM), que combina o Project Professional 2013, o Project Server 2013, o Project Web App e o SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="41d9d-105">The articles in this section describe the overall architecture of the Enterprise Project Management (EPM) solution, which combines Project Professional 2013, Project Server 2013, Project Web App, and SharePoint Server 2013.</span></span>
  
<span data-ttu-id="41d9d-106">O Project Server 2013 foi criado com o .NET Framework 4 e é a terceira grande versão do Project Server a fornecer uma arquitetura de vários mais complexos.</span><span class="sxs-lookup"><span data-stu-id="41d9d-106">Project Server 2013 is built with the .NET Framework 4 and is the third major release of Project Server to provide a true multitier architecture.</span></span> <span data-ttu-id="41d9d-107">Para acesso à nuvem, o Project Server 2013 implementa um modelo de objeto do lado do cliente (CSOM) e um serviço OData para relatórios que podem ser usados em aplicativos Web, aplicativos móveis e aplicativos Silverlight.</span><span class="sxs-lookup"><span data-stu-id="41d9d-107">For cloud access, Project Server 2013 implements a client-side object model (CSOM) and an OData service for reporting that can be used in web applications, mobile applications, and Silverlight applications.</span></span> <span data-ttu-id="41d9d-108">Para aplicativos locais, os clientes podem usar o CSOM ou os serviços do Project Server Interface (PSI).</span><span class="sxs-lookup"><span data-stu-id="41d9d-108">For applications on-premises, clients can use either the CSOM or the Project Server Interface (PSI) services.</span></span> 
  
## <a name="introduction-to-project-server-architecture"></a><span data-ttu-id="41d9d-109">Introdução à arquitetura do Project Server</span><span class="sxs-lookup"><span data-stu-id="41d9d-109">Introduction to Project Server architecture</span></span>

<span data-ttu-id="41d9d-110">Os tópicos nesta seção descrevem a arquitetura geral da solução Enterprise Project Management (EPM), que combina o Project Professional 2013, o Project Server 2013, o Project Web App e o SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="41d9d-110">The topics in this section describe the overall architecture of the Enterprise Project Management (EPM) solution, which combines Project Professional 2013, Project Server 2013, Project Web App, and SharePoint Server 2013.</span></span>
  
<span data-ttu-id="41d9d-111">Para acesso programático ao Project Server, você deve usar o CSOM ou os serviços psi com a interface do Windows Communication Foundation (WCF).</span><span class="sxs-lookup"><span data-stu-id="41d9d-111">For programmatic access to Project Server, you should use either the CSOM or the PSI services with the Windows Communication Foundation (WCF) interface.</span></span> <span data-ttu-id="41d9d-112">A interface do serviço Web ASMX da PSI foi preterida no Project Server 2013, mas ainda funciona.</span><span class="sxs-lookup"><span data-stu-id="41d9d-112">The ASMX web service interface of the PSI is deprecated in Project Server 2013, but still works.</span></span> <span data-ttu-id="41d9d-113">A PSI permite acesso eficiente usando conjuntos de dados e você pode criar manipuladores para eventos do lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="41d9d-113">The PSI enables efficient access by using datasets and you can create handlers for server-side events.</span></span> <span data-ttu-id="41d9d-114">O próprio CSOM usa a PSI para acessar a camada de objeto de negócios do Project Server.</span><span class="sxs-lookup"><span data-stu-id="41d9d-114">The CSOM itself uses the PSI to access the Project Server business object layer.</span></span> <span data-ttu-id="41d9d-115">Em vez de quatro bancos de dados do Project Server, o Project Server 2013 usa um único banco de dados na camada de acesso a dados.</span><span class="sxs-lookup"><span data-stu-id="41d9d-115">Instead of four Project Server databases, Project Server 2013 uses a single database in the data access layer.</span></span>
  
<span data-ttu-id="41d9d-116">O Project Server 2013 integra-se profundamente ao SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="41d9d-116">Project Server 2013 integrates deeply with SharePoint Server 2013.</span></span> <span data-ttu-id="41d9d-117">O Serviço de Aplicativo do Project pode ser associado a outros conjunto de sites do SharePoint no farm.</span><span class="sxs-lookup"><span data-stu-id="41d9d-117">The Project Application Service can be associated with other SharePoint site collections in the farm.</span></span> <span data-ttu-id="41d9d-118">O Project Server pode operar e relatar listas de tarefas do SharePoint no conjunto de sites e também pode obter controle total de onde o Project Server importa e gerencia as listas de tarefas como projetos da empresa.</span><span class="sxs-lookup"><span data-stu-id="41d9d-118">Project Server can operate with and report on SharePoint task lists in the site collection, and can also get full control where Project Server imports and manages the task lists as enterprise projects.</span></span> <span data-ttu-id="41d9d-119">O Project Server também usa a versão 4 do Windows Workflow Foundation (WF4) e adiciona atividades de fluxo de trabalho para soluções de Gerenciamento de Propostas.</span><span class="sxs-lookup"><span data-stu-id="41d9d-119">Project Server also uses version 4 of the Windows Workflow Foundation (WF4) and adds workflow activities for Demand Management solutions.</span></span>
  
<span data-ttu-id="41d9d-120">For a discussion of the many new features that Project 2013 provides for developers, and of the features that are deprecated, see [Updates for developers in Project 2013](updates-for-developers-in-project-2013.md).</span><span class="sxs-lookup"><span data-stu-id="41d9d-120">For a discussion of the many new features that Project 2013 provides for developers, and of the features that are deprecated, see [Updates for developers in Project 2013](updates-for-developers-in-project-2013.md).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="41d9d-121">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="41d9d-121">In this section</span></span>

<span data-ttu-id="41d9d-122">[A arquitetura do Project Server 2013](project-server-2013-architecture.md) descreve as principais partes da plataforma do Project 2013, incluindo os clientes e servidores.</span><span class="sxs-lookup"><span data-stu-id="41d9d-122">[Project Server 2013 architecture](project-server-2013-architecture.md) describes the major parts of the Project 2013 platform, including the clients and servers.</span></span> 
  
<span data-ttu-id="41d9d-123">A programação do [Project Server](project-server-programmability.md) discute os principais recursos de extensibilidade do Project Server 2013, a personalização do Project Web App e a atualização de aplicativos que foram projetados para versões anteriores do Project Server.</span><span class="sxs-lookup"><span data-stu-id="41d9d-123">[Project Server programmability](project-server-programmability.md) discusses the main extensibility features of Project Server 2013, customization of Project Web App, and upgrading applications that are built for previous Project Server versions.</span></span> 
  
<span data-ttu-id="41d9d-124">[O que o PSI faz e](what-the-psi-does-and-does-not-do.md) não descreve cenários em que o PSI pode ser usado e lista coisas que o PSI não pode fazer.</span><span class="sxs-lookup"><span data-stu-id="41d9d-124">[What the PSI does and does not do](what-the-psi-does-and-does-not-do.md) describes scenarios where the PSI can be used and lists things that the PSI cannot do.</span></span> 
  
<span data-ttu-id="41d9d-125">[O que o CSOM](what-the-csom-does-and-does-not-do.md) faz e não descreve cenários em que o CSOM pode ser usado e lista coisas que o CSOM não pode fazer.</span><span class="sxs-lookup"><span data-stu-id="41d9d-125">[What the CSOM does and does not do](what-the-csom-does-and-does-not-do.md) describes scenarios where the CSOM can be used and lists things that the CSOM cannot do.</span></span> 
  
### <a name="topics-not-covered"></a><span data-ttu-id="41d9d-126">Tópicos não abordados</span><span class="sxs-lookup"><span data-stu-id="41d9d-126">Topics not covered</span></span>

<span data-ttu-id="41d9d-127">Os artigos  da seção Arquitetura e programação não documentam recursos dos clientes da área de trabalho do Project (Project Standard 2013 e Project Professional 2013) ou do Project Web App.</span><span class="sxs-lookup"><span data-stu-id="41d9d-127">The articles in the  *Architecture and programmability*  section do not document features of the Project desktop clients (Project Standard 2013 and Project Professional 2013) or Project Web App.</span></span> 
  
<span data-ttu-id="41d9d-128">A ajuda do Visual Basic for Applications (VBA) está disponível no editor do Visual Basic no Project Standard e no Project Professional.</span><span class="sxs-lookup"><span data-stu-id="41d9d-128">Visual Basic for Applications (VBA) help is available in the Visual Basic editor within Project Standard and Project Professional.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="41d9d-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="41d9d-129">See also</span></span>
<span data-ttu-id="41d9d-130"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="41d9d-130"><a name="bk_addresources"> </a></span></span>

- [<span data-ttu-id="41d9d-131">Atualizações para desenvolvedores do Project 2013</span><span class="sxs-lookup"><span data-stu-id="41d9d-131">Updates for developers in Project 2013</span></span>](updates-for-developers-in-project-2013.md)
    
- [<span data-ttu-id="41d9d-132">Introdução ao desenvolvimento de fluxos de trabalho do Project Server</span><span class="sxs-lookup"><span data-stu-id="41d9d-132">Getting started developing Project Server workflows</span></span>](getting-started-developing-project-server-workflows.md)
    

