---
title: Introdução rápida ao Project Online
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5b48958e-6dab-4121-871f-fb15f58f1b24
description: 'Um desenvolvedor de aplicativos pode personalizar um site do Project online (hospedado no SharePoint) usando aplicativos autônomos e/ou suplementos do Project. É possível que O alcance de vários aplicativos seja de acordo com as necessidades de endereçamento dos envolvidos em um projeto para as funções de suporte de PMO, como qualquer um dos seguintes:'
ms.openlocfilehash: 00f79b05b886bfd2c54c118245e22f10bb5451bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344405"
---
# <a name="from-0-to-60-with-project-online"></a><span data-ttu-id="f2ff9-103">Introdução rápida ao Project Online</span><span class="sxs-lookup"><span data-stu-id="f2ff9-103">From 0 to 60 with Project Online</span></span>

<span data-ttu-id="f2ff9-104">Um desenvolvedor de aplicativos pode personalizar um site do Project online (hospedado no SharePoint) usando aplicativos autônomos e/ou suplementos do Project. É possível que O alcance de vários aplicativos seja de acordo com as necessidades de endereçamento dos envolvidos em um projeto para as funções de suporte de PMO, como qualquer um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="f2ff9-104">An application developer can customize a Project Online site (SharePoint hosted) using standalone applications and/or Project add-ins. A wealth of applications is possible that range from addressing needs of those involved in a project to PMO support functions, such as any of the following:</span></span>
  
- <span data-ttu-id="f2ff9-105">Entrada de dados de cartão de timeSimplificada para trabalhadores</span><span class="sxs-lookup"><span data-stu-id="f2ff9-105">Streamlined timecard data entry for workers</span></span>
- <span data-ttu-id="f2ff9-106">Aprovação de cartão de visita eficiente para supervisores</span><span class="sxs-lookup"><span data-stu-id="f2ff9-106">Efficient timecard approval for supervisors</span></span>
- <span data-ttu-id="f2ff9-107">Supervisão de permissões (aquisição e status) necessárias para um projeto</span><span class="sxs-lookup"><span data-stu-id="f2ff9-107">Oversight of permits (procurement and status) needed for a project</span></span>
- <span data-ttu-id="f2ff9-108">Verificação de status/integridade dos projetos ativos</span><span class="sxs-lookup"><span data-stu-id="f2ff9-108">Status/Health check of active projects</span></span>
- <span data-ttu-id="f2ff9-109">Relatório de problemas</span><span class="sxs-lookup"><span data-stu-id="f2ff9-109">Issues report</span></span>
- <span data-ttu-id="f2ff9-110">Relatório de status de gerenciamento de alterações</span><span class="sxs-lookup"><span data-stu-id="f2ff9-110">Change Management Status report</span></span>
    
<span data-ttu-id="f2ff9-111">O Project online inclui suporte à API para acomodar os seguintes cenários:</span><span class="sxs-lookup"><span data-stu-id="f2ff9-111">Project Online includes API support to accommodate the following scenarios:</span></span>
  
- <span data-ttu-id="f2ff9-112">Para um suplemento hospedado do projeto (SharePoint):</span><span class="sxs-lookup"><span data-stu-id="f2ff9-112">For a Project (SharePoint) hosted add-in:</span></span>
    
  - <span data-ttu-id="f2ff9-113">Código (JavaScript, HTML, CSS) hospedado no SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="f2ff9-113">Code (JavaScript, HTML, CSS) that is hosted in SharePoint Online</span></span>
  - <span data-ttu-id="f2ff9-114">Ativos que são baixados para o navegador e executados no SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="f2ff9-114">Assets that are downloaded to the browser and executed against SharePoint Online.</span></span>  
  - <span data-ttu-id="f2ff9-115">Lógica de negócios que está em JavaScript</span><span class="sxs-lookup"><span data-stu-id="f2ff9-115">Business logic that is in JavaScript</span></span>   
  - <span data-ttu-id="f2ff9-116">Acessar dados que estão armazenados no Project online ou no SharePoint, como (mas não está limitado a):</span><span class="sxs-lookup"><span data-stu-id="f2ff9-116">Access data that is in/stored in Project Online or SharePoint such as (but is not limited to):</span></span>  
  - <span data-ttu-id="f2ff9-117">Custom fields (campos personalizados)</span><span class="sxs-lookup"><span data-stu-id="f2ff9-117">Custom fields</span></span>  
  - <span data-ttu-id="f2ff9-118">Listas</span><span class="sxs-lookup"><span data-stu-id="f2ff9-118">Lists</span></span>
    
- <span data-ttu-id="f2ff9-119">Para um suplemento hospedado pelo provedor do projeto (SharePoint):</span><span class="sxs-lookup"><span data-stu-id="f2ff9-119">For a Project (SharePoint) provider-hosted add-in:</span></span>
    
  - <span data-ttu-id="f2ff9-120">Código existente em um site externo para o site do Project online</span><span class="sxs-lookup"><span data-stu-id="f2ff9-120">Code that exists on a site external to the Project Online site</span></span> 
  - <span data-ttu-id="f2ff9-121">Um site externo, que pode ser (mas não está limitado a):</span><span class="sxs-lookup"><span data-stu-id="f2ff9-121">An external site, which can be (but is not limited to):</span></span>  
  - <span data-ttu-id="f2ff9-122">Outro site do SharePoint</span><span class="sxs-lookup"><span data-stu-id="f2ff9-122">Another SharePoint site</span></span>  
  - <span data-ttu-id="f2ff9-123">Aplicativo Web/serviço criado em qualquer plataforma</span><span class="sxs-lookup"><span data-stu-id="f2ff9-123">Web App/Service built on any platform</span></span>  
  - <span data-ttu-id="f2ff9-124">O site externo contém lógica comercial</span><span class="sxs-lookup"><span data-stu-id="f2ff9-124">The external site contains business logic</span></span>  
  - <span data-ttu-id="f2ff9-125">O navegador é redirecionado do Project online para o site externo com tokens de acesso para o Project online</span><span class="sxs-lookup"><span data-stu-id="f2ff9-125">The browser is redirected from Project Online to external site with access tokens to Project Online</span></span>  
  - <span data-ttu-id="f2ff9-126">O site externo pode fazer chamadas para o SharePoint e o Project online</span><span class="sxs-lookup"><span data-stu-id="f2ff9-126">The external site can make calls to SharePoint and Project Online</span></span>
    
- <span data-ttu-id="f2ff9-127">Para um suplemento externo/autônomo:</span><span class="sxs-lookup"><span data-stu-id="f2ff9-127">For an external/standalone add-in:</span></span>
    
  - <span data-ttu-id="f2ff9-128">O usuário executa um aplicativo no dispositivo</span><span class="sxs-lookup"><span data-stu-id="f2ff9-128">User executes an application on their device</span></span>
  - <span data-ttu-id="f2ff9-129">O aplicativo autentica e chama as APIs do Project online diretamente</span><span class="sxs-lookup"><span data-stu-id="f2ff9-129">Application authenticates and calls Project Online APIs directly</span></span>
    

|<span data-ttu-id="f2ff9-130">Tipo de aplicativo</span><span class="sxs-lookup"><span data-stu-id="f2ff9-130">Type of application</span></span>|<span data-ttu-id="f2ff9-131">Implementação da API</span><span class="sxs-lookup"><span data-stu-id="f2ff9-131">API implementation</span></span>|<span data-ttu-id="f2ff9-132">Ambiente de destino</span><span class="sxs-lookup"><span data-stu-id="f2ff9-132">Target environment</span></span>|<span data-ttu-id="f2ff9-133">Exemplos de aplicativos</span><span class="sxs-lookup"><span data-stu-id="f2ff9-133">Application examples</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f2ff9-134">Projeto hospedado</span><span class="sxs-lookup"><span data-stu-id="f2ff9-134">Project hosted</span></span>  <br/> |<span data-ttu-id="f2ff9-135">JSOM (modelo de objeto java script)</span><span class="sxs-lookup"><span data-stu-id="f2ff9-135">JSOM (Java Script Object Model)</span></span>  <br/> <span data-ttu-id="f2ff9-136">REST</span><span class="sxs-lookup"><span data-stu-id="f2ff9-136">REST</span></span>  <br/> |<span data-ttu-id="f2ff9-137">Navegador</span><span class="sxs-lookup"><span data-stu-id="f2ff9-137">Browser</span></span>  <br/> |<span data-ttu-id="f2ff9-138">Entrada do cartão de um</span><span class="sxs-lookup"><span data-stu-id="f2ff9-138">Timecard entry</span></span>  <br/> <span data-ttu-id="f2ff9-139">Aprovação de cartão de visita</span><span class="sxs-lookup"><span data-stu-id="f2ff9-139">Timecard approval</span></span>  <br/> <span data-ttu-id="f2ff9-140">Status do projeto</span><span class="sxs-lookup"><span data-stu-id="f2ff9-140">Project Status</span></span>  <br/> <span data-ttu-id="f2ff9-141">Relatório de problemas</span><span class="sxs-lookup"><span data-stu-id="f2ff9-141">Issues Report</span></span>  <br/> |
|<span data-ttu-id="f2ff9-142">Provedor de projeto hospedado</span><span class="sxs-lookup"><span data-stu-id="f2ff9-142">Project Provider Hosted</span></span>  <br/> |<span data-ttu-id="f2ff9-143">Biblioteca de cliente do CSOM</span><span class="sxs-lookup"><span data-stu-id="f2ff9-143">CSOM client library</span></span>  <br/> |<span data-ttu-id="f2ff9-144">Site/aplicativo do Azure</span><span class="sxs-lookup"><span data-stu-id="f2ff9-144">Azure Website/App</span></span>  <br/> <span data-ttu-id="f2ff9-145">Ambiente não Windows (lâmpada etc.)</span><span class="sxs-lookup"><span data-stu-id="f2ff9-145">Non-Windows environment (LAMP, etc.)</span></span>  <br/> |<span data-ttu-id="f2ff9-146">Validador de quadro de horários externo</span><span class="sxs-lookup"><span data-stu-id="f2ff9-146">External timesheet validator</span></span>  <br/> <span data-ttu-id="f2ff9-147">Importador de projeto</span><span class="sxs-lookup"><span data-stu-id="f2ff9-147">Project Importer</span></span>  <br/> |
|<span data-ttu-id="f2ff9-148">Externo/autônomo</span><span class="sxs-lookup"><span data-stu-id="f2ff9-148">External/Standalone</span></span>  <br/> |<span data-ttu-id="f2ff9-149">REST</span><span class="sxs-lookup"><span data-stu-id="f2ff9-149">REST</span></span>  <br/> <span data-ttu-id="f2ff9-150">CSOM</span><span class="sxs-lookup"><span data-stu-id="f2ff9-150">CSOM</span></span>  <br/> |<span data-ttu-id="f2ff9-151">RESTANTE-qualquer plataforma</span><span class="sxs-lookup"><span data-stu-id="f2ff9-151">REST - any platform</span></span>  <br/> <span data-ttu-id="f2ff9-152">CSOM-qualquer plataforma com suporte do .NET</span><span class="sxs-lookup"><span data-stu-id="f2ff9-152">CSOM - any .NET supported platform</span></span>  <br/> |<span data-ttu-id="f2ff9-153">Entrada do cartão de um</span><span class="sxs-lookup"><span data-stu-id="f2ff9-153">Timecard entry</span></span>  <br/> <span data-ttu-id="f2ff9-154">Migração de projetos para um novo site</span><span class="sxs-lookup"><span data-stu-id="f2ff9-154">Migration of projects to a new site</span></span>  <br/> <span data-ttu-id="f2ff9-155">Status de gerenciamento de alterações.</span><span class="sxs-lookup"><span data-stu-id="f2ff9-155">Change Management Status.</span></span>  <br/> |
   
## <a name="what-does-it-take-to-start-developing-applications-for-project-online"></a><span data-ttu-id="f2ff9-156">O que é necessário para começar a desenvolver aplicativos para o Project online?</span><span class="sxs-lookup"><span data-stu-id="f2ff9-156">What does it take to start developing applications for Project Online?</span></span>

<span data-ttu-id="f2ff9-157">Os itens comuns necessários para o desenvolvimento de aplicativos do Project online são uma conta do Project online e dados de teste, projetos e informações relacionadas ao projeto que incluem atribuições, tarefas, recursos e campos personalizados.</span><span class="sxs-lookup"><span data-stu-id="f2ff9-157">The common items needed for developing Project Online applications are a Project Online account and test data--projects and project-related information that include assignments, tasks, resources, and custom fields.</span></span> <span data-ttu-id="f2ff9-158">Um ambiente de desenvolvimento também é necessário, mas as especificações do ambiente de desenvolvimento dependem do tipo de aplicativo e da interface de API necessárias para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f2ff9-158">A development environment is needed as well, but specifics of the development environment depend on the type of application and the API interface needed for the application.</span></span> <span data-ttu-id="f2ff9-159">As próximas seções descrevem as necessidades de desenvolvimento para as três interfaces de API.</span><span class="sxs-lookup"><span data-stu-id="f2ff9-159">The next few sections describe development needs for the three API interfaces.</span></span>
  
<span data-ttu-id="f2ff9-160">A documentação de referência descreve o modelo de objeto que é comum para todas as três interfaces, bem como um mapa de entidade que mostra as relações entre os componentes do modelo de objeto.</span><span class="sxs-lookup"><span data-stu-id="f2ff9-160">The reference documentation describes the object model that is common for all three interfaces, as well as an entity map that shows relations among the object model components.</span></span>
  
## <a name="project-hosted-add-in-development-environment"></a><span data-ttu-id="f2ff9-161">Ambiente de desenvolvimento de suplementos hospedados do Project</span><span class="sxs-lookup"><span data-stu-id="f2ff9-161">Project hosted add-in development environment</span></span>

<span data-ttu-id="f2ff9-162">Um suplemento hospedado é um suplemento que reside no servidor e é baixado para um navegador para execução em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="f2ff9-162">A hosted add-in is an add-in that resides on the server and is downloaded to a browser for runtime execution.</span></span> <span data-ttu-id="f2ff9-163">Os suplementos hospedados podem usar as interfaces JSOM ou REST e são escritos em JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f2ff9-163">Hosted add-ins can use the JSOM or REST interfaces and are written in JavaScript.</span></span> <span data-ttu-id="f2ff9-164">O Project online fornece referências à biblioteca JSOM para execução em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="f2ff9-164">Project Online provides references to the JSOM library for runtime execution.</span></span> <span data-ttu-id="f2ff9-165">Supondo que o desenvolvimento esteja em uma plataforma do Windows, os recursos necessários são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="f2ff9-165">Assuming development is on a Windows platform, the needed resources follow:</span></span>
  
- <span data-ttu-id="f2ff9-166">Visual Studio 2015 (preferencial) ou Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="f2ff9-166">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span>
    
- <span data-ttu-id="f2ff9-167">Ferramentas de desenvolvimento do Office para Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f2ff9-167">Office development tools for Visual Studio</span></span>
    
- <span data-ttu-id="f2ff9-168">Linguagem JavaScript</span><span class="sxs-lookup"><span data-stu-id="f2ff9-168">JavaScript language</span></span>
    
<span data-ttu-id="f2ff9-169">Visite https://github.com/OfficeDev/Project-JSOM-Copy-Work-Packages para obter um exemplo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f2ff9-169">Visit https://github.com/OfficeDev/Project-JSOM-Copy-Work-Packages for a sample application.</span></span> 
  
<span data-ttu-id="f2ff9-170">Você pode baixar e executar o exemplo em algumas etapas simples:</span><span class="sxs-lookup"><span data-stu-id="f2ff9-170">You can download and run the sample in a few easy steps:</span></span>
  
1. <span data-ttu-id="f2ff9-171">Baixe e abra o aplicativo de exemplo</span><span class="sxs-lookup"><span data-stu-id="f2ff9-171">Download and open the sample application</span></span>
    
2. <span data-ttu-id="f2ff9-172">Atualizar o SiteURL na janela de propriedades</span><span class="sxs-lookup"><span data-stu-id="f2ff9-172">Update the SiteURL in the Properties window</span></span>
    
   <span data-ttu-id="f2ff9-173">O Project online examina o escopo do aplicativo do suplemento e as permissões de usuário para controlar o acesso às informações no host do Project online.</span><span class="sxs-lookup"><span data-stu-id="f2ff9-173">Project Online examines both the application scope of the add-in and the user permissions to govern access to information on the Project Online host.</span></span> <span data-ttu-id="f2ff9-174">Se o acesso for explicitamente negado em uma ou ambas as configurações, o Project online negará o acesso às informações.</span><span class="sxs-lookup"><span data-stu-id="f2ff9-174">If access is explicitly denied in either or both settings, Project Online denies access to the information.</span></span> <span data-ttu-id="f2ff9-175">Caso contrário, o acesso é concedido.</span><span class="sxs-lookup"><span data-stu-id="f2ff9-175">Otherwise, access is granted.</span></span>
    
3. <span data-ttu-id="f2ff9-176">Habilite o [Sideload](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) no site.</span><span class="sxs-lookup"><span data-stu-id="f2ff9-176">Enable [sideloading](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) on your site.</span></span>  
    
4. <span data-ttu-id="f2ff9-177">Compile o projeto.</span><span class="sxs-lookup"><span data-stu-id="f2ff9-177">Build the project.</span></span>
    
5. <span data-ttu-id="f2ff9-178">Execute o projeto.</span><span class="sxs-lookup"><span data-stu-id="f2ff9-178">Run the project.</span></span>
    
## <a name="project-provider-hosted-add-in-development-environment"></a><span data-ttu-id="f2ff9-179">Ambiente de desenvolvimento de suplementos hospedados pelo provedor de projeto</span><span class="sxs-lookup"><span data-stu-id="f2ff9-179">Project provider-hosted add-in development environment</span></span>

<span data-ttu-id="f2ff9-180">Os suplementos hospedados pelo provedor são aplicativos escritos e residentes em qualquer plataforma Web.</span><span class="sxs-lookup"><span data-stu-id="f2ff9-180">Provider hosted add-ins are applications written and residing on any web platform.</span></span> <span data-ttu-id="f2ff9-181">Eles podem conectar e realizar operações de dados usando a API REST (ou CSOM para plataformas Microsoft).</span><span class="sxs-lookup"><span data-stu-id="f2ff9-181">They can connect and perform data operations using the REST (or CSOM for Microsoft platforms) API.</span></span> <span data-ttu-id="f2ff9-182">Todos os idiomas e ambientes que dão suporte à interface REST podem ser usados para desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="f2ff9-182">Any language and environment that supports the REST interface can be used for development.</span></span> 
  
<span data-ttu-id="f2ff9-183">Um exemplo de ambiente de desenvolvimento do Windows para esse tipo de aplicativo inclui os seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="f2ff9-183">An example of the Windows development environment for this type of application includes the following items:</span></span>
  
-  <span data-ttu-id="f2ff9-184">Visual Studio 2015 (preferencial) ou Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="f2ff9-184">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span> 
    
- <span data-ttu-id="f2ff9-185">Ferramentas de desenvolvimento do Microsoft Office para Visual Studio (fornecido com o Visual Studio 2015 Professional e Enterprise Editions)</span><span class="sxs-lookup"><span data-stu-id="f2ff9-185">Microsoft Office Development Tools for Visual Studio (supplied with Visual Studio 2015 Professional and Enterprise editions)</span></span>
    
- <span data-ttu-id="f2ff9-186">.NET Framework 4,0 ou mais recente</span><span class="sxs-lookup"><span data-stu-id="f2ff9-186">.NET Framework 4.0 or newer</span></span>
    
- <span data-ttu-id="f2ff9-187">[Pacote SHAREPOINTONLINE CSOM](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (para chamadas CSOM)</span><span class="sxs-lookup"><span data-stu-id="f2ff9-187">[SharePointOnline CSOM package](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (for CSOM calls)</span></span> 
    
- <span data-ttu-id="f2ff9-188">Uma linguagem de programação, como C#</span><span class="sxs-lookup"><span data-stu-id="f2ff9-188">A programming language, such as C#</span></span> 
    
<span data-ttu-id="f2ff9-189">Visite https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations exemplos de scripts de amostra.</span><span class="sxs-lookup"><span data-stu-id="f2ff9-189">Visit https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations for working sample scripts.</span></span> 
  
<span data-ttu-id="f2ff9-190">Você pode executar o exemplo em algumas etapas:</span><span class="sxs-lookup"><span data-stu-id="f2ff9-190">You can run the sample in a few steps:</span></span>
  
1. <span data-ttu-id="f2ff9-191">Baixe e abra o aplicativo de exemplo</span><span class="sxs-lookup"><span data-stu-id="f2ff9-191">Download and open the sample application</span></span>
    
2. <span data-ttu-id="f2ff9-192">Atualizar o SiteURL na janela de propriedades</span><span class="sxs-lookup"><span data-stu-id="f2ff9-192">Update the SiteURL in the Properties window</span></span>
    
   <span data-ttu-id="f2ff9-193">O Project online examina o escopo do aplicativo do suplemento e as permissões de usuário para controlar o acesso às informações no host do Project online.</span><span class="sxs-lookup"><span data-stu-id="f2ff9-193">Project Online examines both the application scope of the add-in and the user permissions to govern access to information on the Project Online host.</span></span> <span data-ttu-id="f2ff9-194">Se o acesso for explicitamente negado em uma ou ambas as configurações, o Project online negará o acesso às informações.</span><span class="sxs-lookup"><span data-stu-id="f2ff9-194">If access is explicitly denied in either or both settings, Project Online denies access to the information.</span></span> <span data-ttu-id="f2ff9-195">Caso contrário, o acesso é concedido.</span><span class="sxs-lookup"><span data-stu-id="f2ff9-195">Otherwise, access is granted.</span></span>
    
3. <span data-ttu-id="f2ff9-196">Habilite o [Sideload](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) no site.</span><span class="sxs-lookup"><span data-stu-id="f2ff9-196">Enable [sideloading](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) on your site.</span></span> 
    
4. <span data-ttu-id="f2ff9-197">Compile o projeto.</span><span class="sxs-lookup"><span data-stu-id="f2ff9-197">Build the project.</span></span>
    
5. <span data-ttu-id="f2ff9-198">Execute o projeto.</span><span class="sxs-lookup"><span data-stu-id="f2ff9-198">Run the project.</span></span>
    
## <a name="externalstandalone-application-development-environment"></a><span data-ttu-id="f2ff9-199">Ambiente de desenvolvimento de aplicativos externos/autônomos</span><span class="sxs-lookup"><span data-stu-id="f2ff9-199">External/standalone application development environment</span></span>

<span data-ttu-id="f2ff9-200">Um aplicativo autônomo pode chamar o Project online usando o modelo de objeto do lado do cliente (CSOM) ou o REST para se comunicar com o Project online para criar, recuperar, atualizar e excluir informações residentes no servidor.</span><span class="sxs-lookup"><span data-stu-id="f2ff9-200">A standalone application can call Project Online using the Client Side Object Model (CSOM) or REST to communicate with Project Online to create, retrieve, update, and delete information residing on the server.</span></span> <span data-ttu-id="f2ff9-201">Este é um aplicativo cliente autônomo que depende do nível de acesso do usuário a ser executado.</span><span class="sxs-lookup"><span data-stu-id="f2ff9-201">This is a standalone client application that depends on the user access level to run.</span></span> 
  
<span data-ttu-id="f2ff9-202">Um exemplo de ambiente de desenvolvimento do Windows para esse tipo de aplicativo inclui os seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="f2ff9-202">An example of the Windows development environment for this type of application includes the following items:</span></span>
  
- <span data-ttu-id="f2ff9-203">Visual Studio 2015 (preferencial) ou Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="f2ff9-203">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span> 
    
- <span data-ttu-id="f2ff9-204">Ferramentas de desenvolvimento do Microsoft Office para Visual Studio (fornecido com o Visual Studio 2015 Professional e Enterprise Editions)</span><span class="sxs-lookup"><span data-stu-id="f2ff9-204">Microsoft Office Development Tools for Visual Studio (supplied with Visual Studio 2015 Professional and Enterprise editions)</span></span>
    
- <span data-ttu-id="f2ff9-205">.NET Framework 4,0 ou mais recente</span><span class="sxs-lookup"><span data-stu-id="f2ff9-205">.NET Framework 4.0 or newer</span></span>
    
- <span data-ttu-id="f2ff9-206">[Pacote SHAREPOINTONLINE CSOM](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (para chamadas CSOM)</span><span class="sxs-lookup"><span data-stu-id="f2ff9-206">[SharePointOnline CSOM package](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (for CSOM calls)</span></span> 
    
- <span data-ttu-id="f2ff9-207">Uma linguagem de programação, como C#</span><span class="sxs-lookup"><span data-stu-id="f2ff9-207">A programming language, such as C#</span></span> 
    
<span data-ttu-id="f2ff9-208">Visite https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields para obter um exemplo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f2ff9-208">Visit https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields for a sample application.</span></span> 
  
<span data-ttu-id="f2ff9-209">Você pode executar o exemplo em algumas etapas:</span><span class="sxs-lookup"><span data-stu-id="f2ff9-209">You can run the sample in a few steps:</span></span>
  
1. <span data-ttu-id="f2ff9-210">Baixar o aplicativo de exemplo</span><span class="sxs-lookup"><span data-stu-id="f2ff9-210">Download the sample application</span></span>
    
2. <span data-ttu-id="f2ff9-211">Faça algumas alterações para acessar seu site do Project online, o nome do site, a conta do usuário e a senha.</span><span class="sxs-lookup"><span data-stu-id="f2ff9-211">Make a couple of changes to access your Project Online site—the site name, user account, and password.</span></span>
    
   <span data-ttu-id="f2ff9-212">Verifique se o usuário tem acesso a todos os projetos.</span><span class="sxs-lookup"><span data-stu-id="f2ff9-212">Ensure the user has access to all projects.</span></span> <span data-ttu-id="f2ff9-213">O Project online usa permissões de usuário para controlar o acesso a informações no repositório de dados.</span><span class="sxs-lookup"><span data-stu-id="f2ff9-213">Project Online uses user permissions to govern access to information in the data store.</span></span>
    
3. <span data-ttu-id="f2ff9-214">Adicione o assembly do SharePoint às referências usando o console do Gerenciador de pacotes do NuGet, disponível no menu ferramentas, digitando o seguinte no console do NuGet:</span><span class="sxs-lookup"><span data-stu-id="f2ff9-214">Add the SharePoint assembly to the references using the Nuget Package Manager Console, available from the Tools menu by typing the following in the Nuget console:</span></span> 
    
   `Install-Package Microsoft.SharePointOnline.CSOM`

4. <span data-ttu-id="f2ff9-215">Compile o projeto.</span><span class="sxs-lookup"><span data-stu-id="f2ff9-215">Build the project.</span></span>
    
5. <span data-ttu-id="f2ff9-216">Execute o projeto.</span><span class="sxs-lookup"><span data-stu-id="f2ff9-216">Run the project.</span></span>
    
## <a name="next-steps"></a><span data-ttu-id="f2ff9-217">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="f2ff9-217">Next steps</span></span>

<span data-ttu-id="f2ff9-218">Cada aplicativo de exemplo tem um artigo para explicar os destaques do trabalho com a API de projeto individual.</span><span class="sxs-lookup"><span data-stu-id="f2ff9-218">Each sample application has an article to explain the highlights of working with the individual Project API.</span></span> <span data-ttu-id="f2ff9-219">Os artigos aparecem na lista a seguir, juntamente com alguns artigos que descrevem as relações de entidade, as informações no sistema de consulta e o acesso a campos personalizados.</span><span class="sxs-lookup"><span data-stu-id="f2ff9-219">The articles appear in the following list, along with a few articles that describe the entity relationships, information on the query system, and accessing Custom Fields.</span></span> 
  
- [<span data-ttu-id="f2ff9-220">Desenvolver um aplicativo do Project online usando o modelo de objeto do lado do cliente</span><span class="sxs-lookup"><span data-stu-id="f2ff9-220">Developing a Project Online Application Using the Client-side Object Model</span></span>](developing-a-project-online-application-using-the-client-side-object-model.md)
    
- [<span data-ttu-id="f2ff9-221">Desenvolver um suplemento do Project online usando o modelo de objeto do JavaScript (JSOM)</span><span class="sxs-lookup"><span data-stu-id="f2ff9-221">Developing a Project Online add-in using the JavaScript Object Model (JSOM)</span></span>](developing-a-project-online-add-in-using-the-javascript-object-model-jsom.md)
    
- [<span data-ttu-id="f2ff9-222">Acessar campos personalizados da empresa no Project Online</span><span class="sxs-lookup"><span data-stu-id="f2ff9-222">Accessing Project Online enterprise custom fields</span></span>](accessing-project-online-enterprise-custom-fields.md)
    
## <a name="see-also"></a><span data-ttu-id="f2ff9-223">Confira também</span><span class="sxs-lookup"><span data-stu-id="f2ff9-223">See also</span></span>

<span data-ttu-id="f2ff9-224">Confira a documentação e exemplos relacionados ao desenvolvimento de aplicativos usando o CSOM e Project Online no [Portal de Desenvolvimento do Project](https://developer.microsoft.com/en-us/project).</span><span class="sxs-lookup"><span data-stu-id="f2ff9-224">For documentation and samples related to Project Online and application development using CSOM, see the [Project Development Portal](https://developer.microsoft.com/en-us/project).</span></span>
    

