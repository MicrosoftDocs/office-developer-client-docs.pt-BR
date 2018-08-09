---
title: Arquitetura do Project Server 2013 e programação
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
- Project 2013, benefícios de programação, programação, Project Server, Project 2013 e a arquitetura para o Project Server, arquitetura e EPM
localization_priority: Normal
ms.assetid: 9ea3b3c1-fb90-454a-b8e6-abc44fca663d
description: Os artigos desta seção descrevem a arquitetura geral da solução Enterprise Project Management (EPM), que combina o Project Professional 2013, o Project Server 2013, o Project Web App e o SharePoint Server 2013.
ms.openlocfilehash: 6b5ab94968dbb996a370e0e5abb89813f5e41ef7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771177"
---
# <a name="project-server-2013-architecture-and-programmability"></a><span data-ttu-id="71a15-104">Arquitetura do Project Server 2013 e programação</span><span class="sxs-lookup"><span data-stu-id="71a15-104">Project Server 2013 architecture and programmability</span></span>

<span data-ttu-id="71a15-105">Os artigos desta seção descrevem a arquitetura geral da solução Enterprise Project Management (EPM), que combina o Project Professional 2013, o Project Server 2013, o Project Web App e o SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="71a15-105">The articles in this section describe the overall architecture of the Enterprise Project Management (EPM) solution, which combines Project Professional 2013, Project Server 2013, Project Web App, and SharePoint Server 2013.</span></span>
  
<span data-ttu-id="71a15-106">Project Server 2013 foi criado com o .NET Framework 4 e é a terceira versão principal do Project Server para fornecer uma arquitetura de várias camada true.</span><span class="sxs-lookup"><span data-stu-id="71a15-106">Project Server 2013 is built with the .NET Framework 4 and is the third major release of Project Server to provide a true multitier architecture.</span></span> <span data-ttu-id="71a15-107">Para o acesso de nuvem, o Project Server 2013 implementa um modelo de objeto do cliente (CSOM) e um serviço OData para geração de relatórios que pode ser usado em aplicativos web, aplicativos móveis e aplicativos do Silverlight.</span><span class="sxs-lookup"><span data-stu-id="71a15-107">For cloud access, Project Server 2013 implements a client-side object model (CSOM) and an OData service for reporting that can be used in web applications, mobile applications, and Silverlight applications.</span></span> <span data-ttu-id="71a15-108">Para aplicativos no local, os clientes podem usar o CSOM ou os serviços do Project Server Interface (PSI).</span><span class="sxs-lookup"><span data-stu-id="71a15-108">For applications on-premises, clients can use either the CSOM or the Project Server Interface (PSI) services.</span></span> 
  
## <a name="introduction-to-project-server-architecture"></a><span data-ttu-id="71a15-109">Introdução à arquitetura do Project Server</span><span class="sxs-lookup"><span data-stu-id="71a15-109">Introduction to Project Server architecture</span></span>

<span data-ttu-id="71a15-110">Os tópicos desta seção descrevem a arquitetura geral da solução Enterprise Project Management (EPM), que combina o Project Professional 2013, o Project Server 2013, o Project Web App e o SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="71a15-110">The topics in this section describe the overall architecture of the Enterprise Project Management (EPM) solution, which combines Project Professional 2013, Project Server 2013, Project Web App, and SharePoint Server 2013.</span></span>
  
<span data-ttu-id="71a15-111">Para obter acesso programático para o Project Server, você deve usar o CSOM ou os serviços PSI com a interface do Windows Communication Foundation (WCF).</span><span class="sxs-lookup"><span data-stu-id="71a15-111">For programmatic access to Project Server, you should use either the CSOM or the PSI services with the Windows Communication Foundation (WCF) interface.</span></span> <span data-ttu-id="71a15-112">A interface de serviço web ASMX de PSI foi preterido no Project Server 2013, mas ainda funciona.</span><span class="sxs-lookup"><span data-stu-id="71a15-112">The ASMX web service interface of the PSI is deprecated in Project Server 2013, but still works.</span></span> <span data-ttu-id="71a15-113">A PSI habilita o acesso eficiente usando conjuntos de dados e você pode criar manipuladores de eventos do servidor.</span><span class="sxs-lookup"><span data-stu-id="71a15-113">The PSI enables efficient access by using datasets and you can create handlers for server-side events.</span></span> <span data-ttu-id="71a15-114">CSOM do próprio usa a PSI para acessar a camada de objeto de negócios do Project Server.</span><span class="sxs-lookup"><span data-stu-id="71a15-114">The CSOM itself uses the PSI to access the Project Server business object layer.</span></span> <span data-ttu-id="71a15-115">Em vez de quatro bancos de dados do Project Server, o Project Server 2013 usa um único banco de dados na camada de acesso de dados.</span><span class="sxs-lookup"><span data-stu-id="71a15-115">Instead of four Project Server databases, Project Server 2013 uses a single database in the data access layer.</span></span>
  
<span data-ttu-id="71a15-116">Project Server 2013 integra-se totalmente com o SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="71a15-116">Project Server 2013 integrates deeply with SharePoint Server 2013.</span></span> <span data-ttu-id="71a15-117">O serviço de aplicativo do projeto podem ser associado aos outros conjuntos de sites do SharePoint no farm.</span><span class="sxs-lookup"><span data-stu-id="71a15-117">The Project Application Service can be associated with other SharePoint site collections in the farm.</span></span> <span data-ttu-id="71a15-118">Project Server pode operar com e relatar SharePoint listas de tarefas no conjunto de sites e podem também obtêm controle total em que o Project Server importa e gerencia que a tarefa listas como projetos da empresa.</span><span class="sxs-lookup"><span data-stu-id="71a15-118">Project Server can operate with and report on SharePoint task lists in the site collection, and can also get full control where Project Server imports and manages the task lists as enterprise projects.</span></span> <span data-ttu-id="71a15-119">Project Server também usa a versão 4 do Windows Workflow Foundation (WF4) e adiciona as atividades de fluxo de trabalho para soluções de gerenciamento de demanda.</span><span class="sxs-lookup"><span data-stu-id="71a15-119">Project Server also uses version 4 of the Windows Workflow Foundation (WF4) and adds workflow activities for Demand Management solutions.</span></span>
  
<span data-ttu-id="71a15-120">Para uma discussão dos muitos recursos novos que fornece do Project 2013 para desenvolvedores e dos recursos que são reduzidos, consulte [atualizações para desenvolvedores no Project 2013](updates-for-developers-in-project-2013.md).</span><span class="sxs-lookup"><span data-stu-id="71a15-120">For a discussion of the many new features that Project 2013 provides for developers, and of the features that are deprecated, see [Updates for developers in Project 2013](updates-for-developers-in-project-2013.md).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="71a15-121">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="71a15-121">In this section</span></span>

<span data-ttu-id="71a15-122">[Arquitetura do Project Server 2013](project-server-2013-architecture.md) descreve as principais partes da plataforma do Project 2013, incluindo os clientes e servidores.</span><span class="sxs-lookup"><span data-stu-id="71a15-122">[Project Server 2013 architecture](project-server-2013-architecture.md) describes the major parts of the Project 2013 platform, including the clients and servers.</span></span> 
  
<span data-ttu-id="71a15-123">[Recursos de programação do Project Server](project-server-programmability.md) aborda os recursos de extensibilidade principal do Project Server 2013, personalização do Project Web App e atualizando aplicativos desenvolvidos para versões anteriores do Project Server.</span><span class="sxs-lookup"><span data-stu-id="71a15-123">[Project Server programmability](project-server-programmability.md) discusses the main extensibility features of Project Server 2013, customization of Project Web App, and upgrading applications that are built for previous Project Server versions.</span></span> 
  
<span data-ttu-id="71a15-124">[O que o PSI e não faz](what-the-psi-does-and-does-not-do.md) descreve cenários onde a PSI pode ser usada e lista coisas a PSI não pode fazer.</span><span class="sxs-lookup"><span data-stu-id="71a15-124">[What the PSI does and does not do](what-the-psi-does-and-does-not-do.md) describes scenarios where the PSI can be used and lists things that the PSI cannot do.</span></span> 
  
<span data-ttu-id="71a15-125">[O que o CSOM e não faz](what-the-csom-does-and-does-not-do.md) descreve cenários onde o CSOM pode ser usado e lista as tarefas que o CSOM não pode fazer.</span><span class="sxs-lookup"><span data-stu-id="71a15-125">[What the CSOM does and does not do](what-the-csom-does-and-does-not-do.md) describes scenarios where the CSOM can be used and lists things that the CSOM cannot do.</span></span> 
  
### <a name="topics-not-covered"></a><span data-ttu-id="71a15-126">Tópicos não abordados</span><span class="sxs-lookup"><span data-stu-id="71a15-126">Topics not covered</span></span>

<span data-ttu-id="71a15-127">Os artigos na seção de *arquitetura e programação* do documento não recursos do Project Web App ou clientes de área de trabalho do Project (Project Standard 2013 e Project Professional 2013).</span><span class="sxs-lookup"><span data-stu-id="71a15-127">The articles in the  *Architecture and programmability*  section do not document features of the Project desktop clients (Project Standard 2013 and Project Professional 2013) or Project Web App.</span></span> 
  
<span data-ttu-id="71a15-128">Visual Basic para obter ajuda Applications (VBA) está disponível no editor do Visual Basic dentro do Project Standard e Project Professional.</span><span class="sxs-lookup"><span data-stu-id="71a15-128">Visual Basic for Applications (VBA) help is available in the Visual Basic editor within Project Standard and Project Professional.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="71a15-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="71a15-129">See also</span></span>
<span data-ttu-id="71a15-130"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="71a15-130"></span></span>

- [<span data-ttu-id="71a15-131">Atualizações para desenvolvedores no Project 2013</span><span class="sxs-lookup"><span data-stu-id="71a15-131">Updates for developers in Project 2013</span></span>](updates-for-developers-in-project-2013.md)
    
- [<span data-ttu-id="71a15-132">Introdução ao desenvolvimento de fluxos de trabalho do Project</span><span class="sxs-lookup"><span data-stu-id="71a15-132">Getting started developing Project Server workflows</span></span>](getting-started-developing-project-server-workflows.md)
    

