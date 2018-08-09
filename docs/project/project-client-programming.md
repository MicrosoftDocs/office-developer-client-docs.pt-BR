---
title: Programação de cliente do Project
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
f1_keywords:
- object model
- Project object model
- Project VBA
- VBA
keywords:
- VBA, project programação do modelo, Project, objeto, programação, projeto VBA, Visual Basic for Applications, modelo, VBA, objeto modelo de objeto Project, VBA, Visual Basic for Applications
localization_priority: Normal
ms.assetid: 0ad49ff6-8dff-4379-a52c-d292c53c2bc0
description: Os aplicativos de cliente de desktop Project 2013 — Project Standard 2013 e Project Professional 2013 — podem ser personalizados e estendido usando o VBA para gravação de macros. Você pode usar o Visual Studio 2012 para personalizar a interface do usuário da faixa de opções e criar suplementos complexos habilita de suplementos do Office, uma nova extensibilidade do modelo para painéis de tarefas no projeto que são compilados em uma plataforma comum do Office 2013. Project Standard 2013 e Project Professional 2013 podem executar gerais suplementos do Office e use tarefa painel suplementos que são desenvolvidos especificamente para o projeto de integrar com o SharePoint, outros sites e aplicativos da web e dados externos.
ms.openlocfilehash: e8604b4d479d0c64f8d45ad2363d7391d57408ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771171"
---
# <a name="project-client-programming"></a><span data-ttu-id="960c8-106">Programação de cliente do Project</span><span class="sxs-lookup"><span data-stu-id="960c8-106">Project client programming</span></span>

<span data-ttu-id="960c8-107">Os aplicativos de cliente de desktop Project 2013 — Project Standard 2013 e Project Professional 2013 — podem ser personalizados e estendido usando o VBA para gravação de macros.</span><span class="sxs-lookup"><span data-stu-id="960c8-107">The Project 2013 desktop client applications—Project Standard 2013 and Project Professional 2013—can be customized and extended by using VBA to write macros.</span></span> <span data-ttu-id="960c8-108">Você pode usar o Visual Studio 2012 para personalizar a interface do usuário da faixa de opções e criar suplementos complexos habilita de suplementos do Office, uma nova extensibilidade do modelo para painéis de tarefas no projeto que são compilados em uma plataforma comum do Office 2013.</span><span class="sxs-lookup"><span data-stu-id="960c8-108">You can use Visual Studio 2012 to customize the ribbon user interface and create complex add-ins. Office Add-ins enables a new extensibility model for task panes in Project that are built on a common Office 2013 platform.</span></span> <span data-ttu-id="960c8-109">Project Standard 2013 e Project Professional 2013 podem executar gerais suplementos do Office e use tarefa painel suplementos que são desenvolvidos especificamente para o projeto de integrar com o SharePoint, outros sites e aplicativos da web e dados externos.</span><span class="sxs-lookup"><span data-stu-id="960c8-109">Project Standard 2013 and Project Professional 2013 can run general Office Add-ins and use task pane add-ins that are developed specifically for Project to integrate with SharePoint, other websites and web applications, and external data.</span></span>
  
 <span data-ttu-id="960c8-110">**Mover para o Visual Studio** VBA é útil para gravação de macros e desenvolver soluções de automação relativamente simples.</span><span class="sxs-lookup"><span data-stu-id="960c8-110">**Moving to Visual Studio** VBA is useful for recording macros and developing relatively simple automation solutions.</span></span> <span data-ttu-id="960c8-111">Para desenvolver suplementos de painel de tarefas, suplementos e mais complexos, seguros, escalonáveis e soluções facilmente implantadas, recomendamos que você use o Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="960c8-111">To develop task pane add-ins, add-ins, and more complex, secure, scalable, and easily deployed solutions, we recommend that you use Visual Studio 2012.</span></span> <span data-ttu-id="960c8-112">O Microsoft .NET Framework 4.0 e o assembly de interoperabilidade primário do Project 2013 oferecem diversas vantagens para desenvolvimento e implantação de soluções que automatizam e integram os clientes de área de trabalho do Project 2013.</span><span class="sxs-lookup"><span data-stu-id="960c8-112">The Microsoft .NET Framework 4.0 and the Project 2013 primary interop assembly provide many advantages for developing and deploying solutions that automate and integrate the Project 2013 desktop clients.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="960c8-113">Você pode usar o Visual Studio 2010 para desenvolver suplementos do projeto. No entanto, o Visual Studio 2012 inclui modelos e extensões que são projetadas para criar clientes de suplementos do Office.</span><span class="sxs-lookup"><span data-stu-id="960c8-113">You can use Visual Studio 2010 to develop Project add-ins. However, Visual Studio 2012 includes templates and extensions that are designed to create Office Add-ins clients.</span></span> 
  
<span data-ttu-id="960c8-114">O modelo de objeto do VBA no Project 2013 **MSProject** é essencialmente o mesmo que o modelo de objeto **Microsoft.Office.Interop.MSProject** para soluções de código gerenciado com Office Developer Tools para Visual Studio 2013 (também conhecido como VSTO).</span><span class="sxs-lookup"><span data-stu-id="960c8-114">The **MSProject** object model for VBA in Project 2013 is essentially the same as the **Microsoft.Office.Interop.MSProject** object model for managed-code solutions with Office Developer Tools for Visual Studio 2013 (also known as VSTO).</span></span> <span data-ttu-id="960c8-115">Visual Studio 2012 inclui modelos para o desenvolvimento de suplementos de nível de aplicativo para o Project 2010 e do Project 2013 (versões do Project Standard ou Project Professional).</span><span class="sxs-lookup"><span data-stu-id="960c8-115">Visual Studio 2012 includes templates for developing application-level add-ins for Project 2010 and for Project 2013 (either the Project Standard or Project Professional versions).</span></span> <span data-ttu-id="960c8-116">VSTO e o Office Developer Tools para Visual Studio 2012 simplificam o desenvolvimento, teste e implantação de soluções de integração avançada que podem usar o cliente de desktop Project e outros aplicativos do Office 2013 e integrar com sites do SharePoint, listas, e fluxos de trabalho.</span><span class="sxs-lookup"><span data-stu-id="960c8-116">VSTO and Office Developer Tools for Visual Studio 2012 simplify developing, testing, and deploying advanced integration solutions that can use the Project desktop client and other Office 2013 applications, and integrate with SharePoint sites, lists, and workflows.</span></span> 
  
<span data-ttu-id="960c8-117">Suplementos de painel de tarefas e outros suplementos do Office e SharePoint podem ser vendidos no Office Store (consulte [http://office.microsoft.com/store/](http://office.microsoft.com/en-us/store/)) para uso com instalações do Project Online e no local.</span><span class="sxs-lookup"><span data-stu-id="960c8-117">Task pane add-ins and other add-ins for Office and SharePoint can be sold in the Office Store (see [http://office.microsoft.com/store/](http://office.microsoft.com/en-us/store/)) for use with both Project Online and on-premises installations.</span></span> <span data-ttu-id="960c8-118">Macros VBA e suplementos do VSTO não podem ser distribuídos no Office Store; eles foram projetados para uso local com o Project Standard e Project Professional.</span><span class="sxs-lookup"><span data-stu-id="960c8-118">VBA macros and VSTO add-ins cannot be distributed in the Office Store; they are designed for local use with Project Standard and Project Professional.</span></span> <span data-ttu-id="960c8-119">Você pode distribuir as macros VBA em um projeto. Arquivo MPP, instalá-los no arquivo global. mpt em seu computador ou distribuí-las no modelo global da empresa no Project Server 2013.</span><span class="sxs-lookup"><span data-stu-id="960c8-119">You can distribute VBA macros within a project .MPP file, install them in the Global.MPT file on your computer, or distribute them in the enterprise global template in Project Server 2013.</span></span> <span data-ttu-id="960c8-120">Suplementos do VSTO podem ser distribuídos com mais segurança por meio da implantação do [ClickOnce](http://msdn.microsoft.com/en-us/library/t71a733d.aspx) , que permite que atualizações fácil.</span><span class="sxs-lookup"><span data-stu-id="960c8-120">VSTO add-ins can be distributed more securely through [ClickOnce](http://msdn.microsoft.com/en-us/library/t71a733d.aspx) deployment, which enables easy updates.</span></span> 
  
## <a name="reference"></a><span data-ttu-id="960c8-121">Referência</span><span class="sxs-lookup"><span data-stu-id="960c8-121">Reference</span></span>

<span data-ttu-id="960c8-122">[Referência para desenvolvedores VBA do Project](http://msdn.microsoft.com/en-us/library/ee861523%28office.15%29.aspx) Contém introdutório e artigos de Ajuda do VBA.</span><span class="sxs-lookup"><span data-stu-id="960c8-122">[Project VBA developer reference](http://msdn.microsoft.com/en-us/library/ee861523%28office.15%29.aspx) Contains introductory and VBA Help articles.</span></span> 
  
## <a name="related-sections"></a><span data-ttu-id="960c8-123">Se��es relacionadas</span><span class="sxs-lookup"><span data-stu-id="960c8-123">Related sections</span></span>

<span data-ttu-id="960c8-124">[Arquitetura do Project Server 2013](project-server-2013-architecture.md) Mostra como os clientes do Project interagem com o Project Server.</span><span class="sxs-lookup"><span data-stu-id="960c8-124">[Project Server 2013 architecture](project-server-2013-architecture.md) Shows how the Project clients interact with Project Server.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="960c8-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="960c8-125">See also</span></span>



[<span data-ttu-id="960c8-126">Project para desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="960c8-126">Project for developers</span></span>](http://msdn.microsoft.com/en-us/office/aa905469)
  
[<span data-ttu-id="960c8-127">Central de desenvolvedores do Office</span><span class="sxs-lookup"><span data-stu-id="960c8-127">Office developer center</span></span>](https://dev.office.com)
  
[<span data-ttu-id="960c8-128">Central de desenvolvedores do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="960c8-128">Visual Studio developer center</span></span>](http://msdn.microsoft.com/en-us/vstudio/aa718325.aspx)
  
[<span data-ttu-id="960c8-129">Implantação e segurança do ClickOnce</span><span class="sxs-lookup"><span data-stu-id="960c8-129">ClickOnce Security and Deployment</span></span>](http://msdn.microsoft.com/en-us/library/t71a733d.aspx)
  
[<span data-ttu-id="960c8-130">Referência de campos disponíveis</span><span class="sxs-lookup"><span data-stu-id="960c8-130">Available fields reference</span></span>](http://office.microsoft.com/en-us/project-help/available-fields-reference-HA102749299.aspx?CTT=1)

