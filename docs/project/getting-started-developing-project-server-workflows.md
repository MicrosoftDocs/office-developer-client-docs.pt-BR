---
title: Introdução ao desenvolvimento de fluxos de trabalho do Project
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 735bbb04-a8c1-46c0-a346-42050f0ac9b1
description: Os processos de gerenciamento de demanda no Project Server 2013 incluem fluxos de trabalho que o ajudarão a gerenciar propostas de projetos e análises de portfólios. Esta seção inclui artigos que mostram como criar fluxos de trabalho do Project Server.
ms.openlocfilehash: 0a09022e63528f50ee4f0c8bd69bd6c34c5d8753
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384091"
---
# <a name="getting-started-developing-project-server-workflows"></a><span data-ttu-id="fa3b6-104">Introdução ao desenvolvimento de fluxos de trabalho do Project</span><span class="sxs-lookup"><span data-stu-id="fa3b6-104">Getting started developing Project Server workflows</span></span>

<span data-ttu-id="fa3b6-105">Os processos de gerenciamento de demanda no Project Server 2013 incluem fluxos de trabalho que o ajudarão a gerenciar propostas de projetos e análises de portfólios.</span><span class="sxs-lookup"><span data-stu-id="fa3b6-105">Demand management processes in Project Server 2013 include workflows that help you manage project proposals and portfolio analyses.</span></span> <span data-ttu-id="fa3b6-106">Esta seção inclui artigos que mostram como criar fluxos de trabalho do Project Server.</span><span class="sxs-lookup"><span data-stu-id="fa3b6-106">This section includes articles that show how to create workflows for Project Server.</span></span>
  
<span data-ttu-id="fa3b6-107">Os fluxos de trabalho do Project Server 2013 usam a plataforma de fluxod de trabalho do SharePoint Server 2013, criada na versão 4 do Windows Workflow Foundation (WF4).</span><span class="sxs-lookup"><span data-stu-id="fa3b6-107">Project Server 2013 workflows use the SharePoint Server 2013 workflow platform, which is built on version 4 of Windows Workflow Foundation (WF4).</span></span> <span data-ttu-id="fa3b6-108">Os fluxos de trabalho com base em WF4 são declarativos, o que significa que a ferramenta de design de fluxo de trabalho salva estágios, ações, condições e outros elementos do fluxo de trabalho em código XAML, que é interpretado no tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="fa3b6-108">WF4-based workflows are declarative, which means that the workflow design tool saves workflow stages, actions, conditions, and other elements to XAML code, which is interpreted at run-time.</span></span> <span data-ttu-id="fa3b6-109">Você pode usar o SharePoint Designer 2013 ou o Visual Studio 2012 para criar fluxos de trabalho declarativos.</span><span class="sxs-lookup"><span data-stu-id="fa3b6-109">You can use either SharePoint Designer 2013 or Visual Studio 2012 to create declarative workflows.</span></span> <span data-ttu-id="fa3b6-110">Um fluxo de trabalho requer o mecanismo de execução do Workflow Manager Client 1.0, que pode ser em um servidor local para soluções locais ou em um servidor remoto para soluções do Project Online.</span><span class="sxs-lookup"><span data-stu-id="fa3b6-110">A workflow requires the Workflow Manager Client 1.0 execution engine, which can be on a local server for on-premises solutions or on a remote server for Project Online solutions.</span></span>
  
<span data-ttu-id="fa3b6-111">Você pode usar o SharePoint Designer 2013 para criar fluxos de trabalho declarativos relativamente simples.</span><span class="sxs-lookup"><span data-stu-id="fa3b6-111">You can use SharePoint Designer 2013 to create relatively simple declarative workflows.</span></span> <span data-ttu-id="fa3b6-112">Para fluxos de trabalho complexos e modelos de fluxo de trabalho que podem ser reutilizados, você pode usar o Visual Studio 2012 para desenvolver e depurar fluxos de trabalho do Project Web App.</span><span class="sxs-lookup"><span data-stu-id="fa3b6-112">For complex workflows, and workflow templates that can be reused, you can use Visual Studio 2012 to develop and debug workflows for Project Web App.</span></span> <span data-ttu-id="fa3b6-113">Para saber mais, confira [Criar fluxos de trabalho do Project usando o Visual Studio 2012](https://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx).</span><span class="sxs-lookup"><span data-stu-id="fa3b6-113">For more information, see [Creating Project Workflows using Visual Studio 2012](https://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx).</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="fa3b6-114">Use uma instalação de teste do Project Server, e não uma instalação de produção, para desenvolver e testar fluxos de trabalho.</span><span class="sxs-lookup"><span data-stu-id="fa3b6-114">Use a test installation of Project Server, not a production installation, to develop and test workflows.</span></span> <span data-ttu-id="fa3b6-115">Fluxos de trabalho desenvolvidos para versões de pré-lançamento do Project Server 2013 devem ser testados para a versão de lançamento, e podem precisar ser criados e implantados novamente.</span><span class="sxs-lookup"><span data-stu-id="fa3b6-115">Workflows that are developed for pre-release versions of Project Server 2013 must be tested for the release version, and may have to be created again and redeployed.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="fa3b6-116">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="fa3b6-116">In this section</span></span>

[<span data-ttu-id="fa3b6-117">Criar um fluxo de trabalho do Project Server para o Gerenciamento de Propostas</span><span class="sxs-lookup"><span data-stu-id="fa3b6-117">Create a Project Server workflow for Demand Management</span></span>](create-a-project-server-workflow-for-demand-management.md)
  
## <a name="see-also"></a><span data-ttu-id="fa3b6-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="fa3b6-118">See also</span></span>



[<span data-ttu-id="fa3b6-119">Atualizar campos personalizados em massa e criar sites de projeto a partir de um fluxo de trabalho do Project Online</span><span class="sxs-lookup"><span data-stu-id="fa3b6-119">Bulk update custom fields and create project sites from a workflow in Project Online</span></span>](bulk-update-custom-fields-and-create-project-sites-from-workflow-in-project.md)


[<span data-ttu-id="fa3b6-120">Desenvolvimento de fluxos de trabalho no SharePoint Designer 2013 e no Visio 2013</span><span class="sxs-lookup"><span data-stu-id="fa3b6-120">Workflow development in SharePoint Designer 2013 and Visio 2013</span></span>](https://msdn.microsoft.com/library/jj163272%28office.15%29.aspx)
  
[<span data-ttu-id="fa3b6-121">Novidades nos fluxos de trabalho do SharePoint 2013</span><span class="sxs-lookup"><span data-stu-id="fa3b6-121">What's new in workflows for SharePoint 2013</span></span>](https://msdn.microsoft.com/library/jj163177.aspx)
  
[<span data-ttu-id="fa3b6-122">Desenvolver fluxos de trabalho do SharePoint 2013 usando o Visual Studio</span><span class="sxs-lookup"><span data-stu-id="fa3b6-122">Develop SharePoint 2013 workflows using Visual Studio</span></span>](https://msdn.microsoft.com/library/jj163199.aspx)
  
[<span data-ttu-id="fa3b6-123">Criar fluxos de trabalho do Project usando o Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="fa3b6-123">Creating Project Workflows using Visual Studio 2012</span></span>](https://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx)
  
[<span data-ttu-id="fa3b6-124">Windows Workflow Foundation</span><span class="sxs-lookup"><span data-stu-id="fa3b6-124">Windows Workflow Foundation</span></span>](https://msdn.microsoft.com/library/dd489441.aspx)
  
[<span data-ttu-id="fa3b6-125">Introdução de um desenvolvedor ao Windows Workflow Foundation (WF) no .NET 4</span><span class="sxs-lookup"><span data-stu-id="fa3b6-125">A Developer's Introduction to Windows Workflow Foundation (WF) in .NET 4</span></span>](https://msdn.microsoft.com/library/ee342461.aspx)
  
[<span data-ttu-id="fa3b6-126">Guia de gerenciamento de propostas para iniciantes (white paper)</span><span class="sxs-lookup"><span data-stu-id="fa3b6-126">Hitchhiker's guide to demand management (white paper)</span></span>](https://msdn.microsoft.com/library/ff973112.aspx)

