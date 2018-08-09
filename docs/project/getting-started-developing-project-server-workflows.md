---
title: Introdução ao desenvolvimento de fluxos de trabalho do Project
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 735bbb04-a8c1-46c0-a346-42050f0ac9b1
description: Demanda processos de gerenciamento no Project Server 2013 incluem fluxos de trabalho que o ajudarão a gerenciar propostas de projeto e análises de portfólio. Esta seção inclui artigos que mostram como criar fluxos de trabalho do Project Server.
ms.openlocfilehash: 275f61b7992423a5e10a7ba90b8c76433290343e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771032"
---
# <a name="getting-started-developing-project-server-workflows"></a><span data-ttu-id="bae23-104">Introdução ao desenvolvimento de fluxos de trabalho do Project</span><span class="sxs-lookup"><span data-stu-id="bae23-104">Getting started developing Project Server workflows</span></span>

<span data-ttu-id="bae23-105">Demanda processos de gerenciamento no Project Server 2013 incluem fluxos de trabalho que o ajudarão a gerenciar propostas de projeto e análises de portfólio.</span><span class="sxs-lookup"><span data-stu-id="bae23-105">Demand management processes in Project Server 2013 include workflows that help you manage project proposals and portfolio analyses.</span></span> <span data-ttu-id="bae23-106">Esta seção inclui artigos que mostram como criar fluxos de trabalho do Project Server.</span><span class="sxs-lookup"><span data-stu-id="bae23-106">This section includes articles that show how to create workflows for Project Server.</span></span>
  
<span data-ttu-id="bae23-107">Fluxos de trabalho do Project Server 2013 usam a plataforma de fluxo de trabalho do SharePoint Server 2013, que é baseada na versão 4 do Windows Workflow Foundation (WF4).</span><span class="sxs-lookup"><span data-stu-id="bae23-107">Project Server 2013 workflows use the SharePoint Server 2013 workflow platform, which is built on version 4 of Windows Workflow Foundation (WF4).</span></span> <span data-ttu-id="bae23-108">Fluxos de trabalho baseados em WF4 são declarativos, o que significa que a ferramenta de design de fluxo de trabalho é salva em estágios do fluxo de trabalho, ações, condições e outros elementos em código XAML, que será interpretado em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="bae23-108">WF4-based workflows are declarative, which means that the workflow design tool saves workflow stages, actions, conditions, and other elements to XAML code, which is interpreted at run-time.</span></span> <span data-ttu-id="bae23-109">Você pode usar o SharePoint Designer 2013 ou o Visual Studio 2012 para criar fluxos de trabalho declarativos.</span><span class="sxs-lookup"><span data-stu-id="bae23-109">You can use either SharePoint Designer 2013 or Visual Studio 2012 to create declarative workflows.</span></span> <span data-ttu-id="bae23-110">Um fluxo de trabalho requer o mecanismo de execução de cliente do Gerenciador de fluxo de trabalho 1.0, que pode ser em um servidor local para soluções no local ou em um servidor remoto para soluções do Project Online.</span><span class="sxs-lookup"><span data-stu-id="bae23-110">A workflow requires the Workflow Manager Client 1.0 execution engine, which can be on a local server for on-premises solutions or on a remote server for Project Online solutions.</span></span>
  
<span data-ttu-id="bae23-111">Você pode usar o SharePoint Designer 2013 para criar fluxos de trabalho declarativos relativamente simples.</span><span class="sxs-lookup"><span data-stu-id="bae23-111">You can use SharePoint Designer 2013 to create relatively simple declarative workflows.</span></span> <span data-ttu-id="bae23-112">Para os fluxos de trabalho complexos e modelos de fluxo de trabalho que podem ser reutilizados, você pode usar o Visual Studio 2012 para desenvolver e depurar fluxos de trabalho para o Project Web App.</span><span class="sxs-lookup"><span data-stu-id="bae23-112">For complex workflows, and workflow templates that can be reused, you can use Visual Studio 2012 to develop and debug workflows for Project Web App.</span></span> <span data-ttu-id="bae23-113">Para obter mais informações, consulte [Criando fluxos de trabalho do projeto usando o Visual Studio 2012](http://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx).</span><span class="sxs-lookup"><span data-stu-id="bae23-113">For more information, see [Creating Project Workflows using Visual Studio 2012](http://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx).</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="bae23-114">Use uma instalação de teste do Project Server, não é uma instalação de produção, desenvolver e testar os fluxos de trabalho.</span><span class="sxs-lookup"><span data-stu-id="bae23-114">Use a test installation of Project Server, not a production installation, to develop and test workflows.</span></span> <span data-ttu-id="bae23-115">Fluxos de trabalho que são desenvolvidos para versões de pré-lançamento do Project Server 2013 devem ser testados para a versão de lançamento e podem precisar ser criado novamente e reimplantados.</span><span class="sxs-lookup"><span data-stu-id="bae23-115">Workflows that are developed for pre-release versions of Project Server 2013 must be tested for the release version, and may have to be created again and redeployed.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="bae23-116">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="bae23-116">In this section</span></span>

[<span data-ttu-id="bae23-117">Criar um fluxo de trabalho do Project Server para o Gerenciamento de Propostas</span><span class="sxs-lookup"><span data-stu-id="bae23-117">Create a Project Server workflow for Demand Management</span></span>](create-a-project-server-workflow-for-demand-management.md)
  
## <a name="see-also"></a><span data-ttu-id="bae23-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="bae23-118">See also</span></span>



[<span data-ttu-id="bae23-119">Em massa de campos personalizados de atualização e criar sites de projetos a partir de um fluxo de trabalho do Project Online</span><span class="sxs-lookup"><span data-stu-id="bae23-119">Bulk update custom fields and create project sites from a Project Online workflow</span></span>](bulk-update-custom-fields-and-create-project-sites-from-workflow-in-project.md)


[<span data-ttu-id="bae23-120">Desenvolvimento de fluxos de trabalho no SharePoint Designer 2013 e no Visio 2013</span><span class="sxs-lookup"><span data-stu-id="bae23-120">Workflow development in SharePoint Designer 2013 and Visio 2013</span></span>](http://msdn.microsoft.com/en-us/library/jj163272%28office.15%29.aspx)
  
[<span data-ttu-id="bae23-121">O que há de novo nos fluxos de trabalho para o SharePoint 2013</span><span class="sxs-lookup"><span data-stu-id="bae23-121">What's new in workflows for SharePoint 2013</span></span>](http://msdn.microsoft.com/en-us/library/jj163177.aspx)
  
[<span data-ttu-id="bae23-122">Desenvolver fluxos de trabalho do SharePoint 2013 usando o Visual Studio</span><span class="sxs-lookup"><span data-stu-id="bae23-122">Develop SharePoint 2013 workflows using Visual Studio</span></span>](http://msdn.microsoft.com/en-us/library/jj163199.aspx)
  
[<span data-ttu-id="bae23-123">Criando fluxos de trabalho do projeto usando o Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="bae23-123">Creating Project Workflows using Visual Studio 2012</span></span>](http://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx)
  
[<span data-ttu-id="bae23-124">Windows Workflow Foundation</span><span class="sxs-lookup"><span data-stu-id="bae23-124">Windows Workflow Foundation</span></span>](http://msdn.microsoft.com/en-us/library/dd489441.aspx)
  
[<span data-ttu-id="bae23-125">Introdução do desenvolvedor para o Windows Workflow Foundation (WF) no .NET 4</span><span class="sxs-lookup"><span data-stu-id="bae23-125">A developer's introduction to Windows Workflow Foundation (WF) in .NET 4</span></span>](http://msdn.microsoft.com/en-us/library/ee342461.aspx)
  
[<span data-ttu-id="bae23-126">Guia do Mochileiro ao gerenciamento de propostas (white paper)</span><span class="sxs-lookup"><span data-stu-id="bae23-126">Hitchhiker's guide to demand management (white paper)</span></span>](http://msdn.microsoft.com/en-us/library/ff973112.aspx)

