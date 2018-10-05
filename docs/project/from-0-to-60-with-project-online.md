---
title: Introdução rápida ao Project Online
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5b48958e-6dab-4121-871f-fb15f58f1b24
description: 'Um desenvolvedor de aplicativos pode personalizar um site Project Online (SharePoint hospedado) usando aplicativos autônomos e/ou complementos do projeto. Uma ampla gama de aplicativos é possível que variam de endereçamento às necessidades das pessoas envolvidas em um projeto para funções de suporte PMO, como um destes procedimentos:'
ms.openlocfilehash: 00f79b05b886bfd2c54c118245e22f10bb5451bf
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392580"
---
# <a name="from-0-to-60-with-project-online"></a><span data-ttu-id="4e6f0-103">Introdução rápida ao Project Online</span><span class="sxs-lookup"><span data-stu-id="4e6f0-103">From 0 to 60 with Project Online</span></span>

<span data-ttu-id="4e6f0-104">Um desenvolvedor de aplicativos pode personalizar um site Project Online (SharePoint hospedado) usando aplicativos autônomos e/ou complementos do projeto. Uma ampla gama de aplicativos é possível que variam de endereçamento às necessidades das pessoas envolvidas em um projeto para funções de suporte PMO, como um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="4e6f0-104">An application developer can customize a Project Online site (SharePoint hosted) using standalone applications and/or Project add-ins. A wealth of applications is possible that range from addressing needs of those involved in a project to PMO support functions, such as any of the following:</span></span>
  
- <span data-ttu-id="4e6f0-105">Entrada de dados de cartão de ponto simplificada para trabalhadores</span><span class="sxs-lookup"><span data-stu-id="4e6f0-105">Streamlined timecard data entry for workers</span></span>
- <span data-ttu-id="4e6f0-106">Aprovação de cartão eficiente para supervisores</span><span class="sxs-lookup"><span data-stu-id="4e6f0-106">Efficient timecard approval for supervisors</span></span>
- <span data-ttu-id="4e6f0-107">Supervisão de autorizações (compras e status) necessário para um projeto</span><span class="sxs-lookup"><span data-stu-id="4e6f0-107">Oversight of permits (procurement and status) needed for a project</span></span>
- <span data-ttu-id="4e6f0-108">Verificação de status/integridade dos projetos ativos</span><span class="sxs-lookup"><span data-stu-id="4e6f0-108">Status/Health check of active projects</span></span>
- <span data-ttu-id="4e6f0-109">Relatório de problemas</span><span class="sxs-lookup"><span data-stu-id="4e6f0-109">Issues report</span></span>
- <span data-ttu-id="4e6f0-110">Alterar o relatório de Status de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="4e6f0-110">Change Management Status report</span></span>
    
<span data-ttu-id="4e6f0-111">Project Online inclui suporte de API para acomodar os cenários a seguintes:</span><span class="sxs-lookup"><span data-stu-id="4e6f0-111">Project Online includes API support to accommodate the following scenarios:</span></span>
  
- <span data-ttu-id="4e6f0-112">Para um suplemento do Project (SharePoint) hospedado:</span><span class="sxs-lookup"><span data-stu-id="4e6f0-112">For a Project (SharePoint) hosted add-in:</span></span>
    
  - <span data-ttu-id="4e6f0-113">Código (JavaScript, HTML, CSS) que está hospedado no SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="4e6f0-113">Code (JavaScript, HTML, CSS) that is hosted in SharePoint Online</span></span>
  - <span data-ttu-id="4e6f0-114">Ativos que são baixados para o navegador e executados no SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="4e6f0-114">Assets that are downloaded to the browser and executed against SharePoint Online.</span></span>  
  - <span data-ttu-id="4e6f0-115">Lógica de negócios que esteja no JavaScript</span><span class="sxs-lookup"><span data-stu-id="4e6f0-115">Business logic that is in JavaScript</span></span>   
  - <span data-ttu-id="4e6f0-116">Acesse os dados são como em/armazenados no Project Online ou do SharePoint (mas não estão limitado a):</span><span class="sxs-lookup"><span data-stu-id="4e6f0-116">Access data that is in/stored in Project Online or SharePoint such as (but is not limited to):</span></span>  
  - <span data-ttu-id="4e6f0-117">Campos personalizados</span><span class="sxs-lookup"><span data-stu-id="4e6f0-117">Custom fields</span></span>  
  - <span data-ttu-id="4e6f0-118">Listas</span><span class="sxs-lookup"><span data-stu-id="4e6f0-118">Lists</span></span>
    
- <span data-ttu-id="4e6f0-119">Para um projeto (SharePoint) hospedado em provedor suplemento:</span><span class="sxs-lookup"><span data-stu-id="4e6f0-119">For a Project (SharePoint) provider-hosted add-in:</span></span>
    
  - <span data-ttu-id="4e6f0-120">Código que existe em um site externo para o site do Project Online</span><span class="sxs-lookup"><span data-stu-id="4e6f0-120">Code that exists on a site external to the Project Online site</span></span> 
  - <span data-ttu-id="4e6f0-121">Um site externo, que pode ser (mas não está limitado a):</span><span class="sxs-lookup"><span data-stu-id="4e6f0-121">An external site, which can be (but is not limited to):</span></span>  
  - <span data-ttu-id="4e6f0-122">Outro site do SharePoint</span><span class="sxs-lookup"><span data-stu-id="4e6f0-122">Another SharePoint site</span></span>  
  - <span data-ttu-id="4e6f0-123">Serviço/aplicativo Web baseado em qualquer plataforma</span><span class="sxs-lookup"><span data-stu-id="4e6f0-123">Web App/Service built on any platform</span></span>  
  - <span data-ttu-id="4e6f0-124">O site externo contém a lógica de negócios</span><span class="sxs-lookup"><span data-stu-id="4e6f0-124">The external site contains business logic</span></span>  
  - <span data-ttu-id="4e6f0-125">O navegador é redirecionado do Project Online site externo com tokens de acesso ao Project Online</span><span class="sxs-lookup"><span data-stu-id="4e6f0-125">The browser is redirected from Project Online to external site with access tokens to Project Online</span></span>  
  - <span data-ttu-id="4e6f0-126">O site externo pode fazer chamadas para o SharePoint e o Project Online</span><span class="sxs-lookup"><span data-stu-id="4e6f0-126">The external site can make calls to SharePoint and Project Online</span></span>
    
- <span data-ttu-id="4e6f0-127">Para um suplemento externo/autônomo:</span><span class="sxs-lookup"><span data-stu-id="4e6f0-127">For an external/standalone add-in:</span></span>
    
  - <span data-ttu-id="4e6f0-128">Usuário executa um aplicativo no seu dispositivo</span><span class="sxs-lookup"><span data-stu-id="4e6f0-128">User executes an application on their device</span></span>
  - <span data-ttu-id="4e6f0-129">Aplicativo autentica e chama APIs do Project Online diretamente</span><span class="sxs-lookup"><span data-stu-id="4e6f0-129">Application authenticates and calls Project Online APIs directly</span></span>
    

|<span data-ttu-id="4e6f0-130">Tipo de aplicativo</span><span class="sxs-lookup"><span data-stu-id="4e6f0-130">Type of application</span></span>|<span data-ttu-id="4e6f0-131">Implementação da API</span><span class="sxs-lookup"><span data-stu-id="4e6f0-131">API implementation</span></span>|<span data-ttu-id="4e6f0-132">Ambiente de destino</span><span class="sxs-lookup"><span data-stu-id="4e6f0-132">Target environment</span></span>|<span data-ttu-id="4e6f0-133">Exemplos de aplicativos</span><span class="sxs-lookup"><span data-stu-id="4e6f0-133">Application examples</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4e6f0-134">Projeto hospedado</span><span class="sxs-lookup"><span data-stu-id="4e6f0-134">Project hosted</span></span>  <br/> |<span data-ttu-id="4e6f0-135">JSOM (modelo de objeto do Java Script)</span><span class="sxs-lookup"><span data-stu-id="4e6f0-135">JSOM (Java Script Object Model)</span></span>  <br/> <span data-ttu-id="4e6f0-136">REST</span><span class="sxs-lookup"><span data-stu-id="4e6f0-136">REST</span></span>  <br/> |<span data-ttu-id="4e6f0-137">Browser</span><span class="sxs-lookup"><span data-stu-id="4e6f0-137">Browser</span></span>  <br/> |<span data-ttu-id="4e6f0-138">Entrada de cartão de ponto</span><span class="sxs-lookup"><span data-stu-id="4e6f0-138">Timecard entry</span></span>  <br/> <span data-ttu-id="4e6f0-139">Aprovação de cartão de ponto</span><span class="sxs-lookup"><span data-stu-id="4e6f0-139">Timecard approval</span></span>  <br/> <span data-ttu-id="4e6f0-140">Status do projeto</span><span class="sxs-lookup"><span data-stu-id="4e6f0-140">Project Status</span></span>  <br/> <span data-ttu-id="4e6f0-141">Relatório de problemas</span><span class="sxs-lookup"><span data-stu-id="4e6f0-141">Issues Report</span></span>  <br/> |
|<span data-ttu-id="4e6f0-142">Provedor de projeto hospedado</span><span class="sxs-lookup"><span data-stu-id="4e6f0-142">Project Provider Hosted</span></span>  <br/> |<span data-ttu-id="4e6f0-143">Biblioteca do cliente CSOM</span><span class="sxs-lookup"><span data-stu-id="4e6f0-143">CSOM client library</span></span>  <br/> |<span data-ttu-id="4e6f0-144">Site do Windows Azure/App</span><span class="sxs-lookup"><span data-stu-id="4e6f0-144">Azure Website/App</span></span>  <br/> <span data-ttu-id="4e6f0-145">Ambiente de não-Windows (LÂMPADA, etc.)</span><span class="sxs-lookup"><span data-stu-id="4e6f0-145">Non-Windows environment (LAMP, etc.)</span></span>  <br/> |<span data-ttu-id="4e6f0-146">Validador de quadro de horários externo</span><span class="sxs-lookup"><span data-stu-id="4e6f0-146">External timesheet validator</span></span>  <br/> <span data-ttu-id="4e6f0-147">Importador de projeto</span><span class="sxs-lookup"><span data-stu-id="4e6f0-147">Project Importer</span></span>  <br/> |
|<span data-ttu-id="4e6f0-148">Externa/autônomo</span><span class="sxs-lookup"><span data-stu-id="4e6f0-148">External/Standalone</span></span>  <br/> |<span data-ttu-id="4e6f0-149">REST</span><span class="sxs-lookup"><span data-stu-id="4e6f0-149">REST</span></span>  <br/> <span data-ttu-id="4e6f0-150">CSOM</span><span class="sxs-lookup"><span data-stu-id="4e6f0-150">CSOM</span></span>  <br/> |<span data-ttu-id="4e6f0-151">REST - qualquer plataforma</span><span class="sxs-lookup"><span data-stu-id="4e6f0-151">REST - any platform</span></span>  <br/> <span data-ttu-id="4e6f0-152">CSOM - todas as plataformas com suporte do .NET</span><span class="sxs-lookup"><span data-stu-id="4e6f0-152">CSOM - any .NET supported platform</span></span>  <br/> |<span data-ttu-id="4e6f0-153">Entrada de cartão de ponto</span><span class="sxs-lookup"><span data-stu-id="4e6f0-153">Timecard entry</span></span>  <br/> <span data-ttu-id="4e6f0-154">Migração de projetos para um novo site</span><span class="sxs-lookup"><span data-stu-id="4e6f0-154">Migration of projects to a new site</span></span>  <br/> <span data-ttu-id="4e6f0-155">Alterar o Status de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="4e6f0-155">Change Management Status.</span></span>  <br/> |
   
## <a name="what-does-it-take-to-start-developing-applications-for-project-online"></a><span data-ttu-id="4e6f0-156">O que leva para começar a desenvolver aplicativos para o Project Online?</span><span class="sxs-lookup"><span data-stu-id="4e6f0-156">What does it take to start developing applications for Project Online?</span></span>

<span data-ttu-id="4e6f0-157">Os itens comuns necessários para o desenvolvimento de aplicativos do Project Online são uma conta do Project Online e testam dados--projetos e informações relacionados ao projeto que incluem atribuições, tarefas, recursos e campos personalizados.</span><span class="sxs-lookup"><span data-stu-id="4e6f0-157">The common items needed for developing Project Online applications are a Project Online account and test data--projects and project-related information that include assignments, tasks, resources, and custom fields.</span></span> <span data-ttu-id="4e6f0-158">Um ambiente de desenvolvimento necessário também, mas as especificações do ambiente de desenvolvimento dependem do tipo de aplicativo e a interface de API necessária para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4e6f0-158">A development environment is needed as well, but specifics of the development environment depend on the type of application and the API interface needed for the application.</span></span> <span data-ttu-id="4e6f0-159">As próximas seções descrevem as necessidades de desenvolvimento para as interfaces de API três.</span><span class="sxs-lookup"><span data-stu-id="4e6f0-159">The next few sections describe development needs for the three API interfaces.</span></span>
  
<span data-ttu-id="4e6f0-160">A documentação de referência descreve o modelo de objeto que é comum para todas as interfaces de três, bem como um mapa de entidade que mostra as relações entre os componentes do modelo de objeto.</span><span class="sxs-lookup"><span data-stu-id="4e6f0-160">The reference documentation describes the object model that is common for all three interfaces, as well as an entity map that shows relations among the object model components.</span></span>
  
## <a name="project-hosted-add-in-development-environment"></a><span data-ttu-id="4e6f0-161">Ambiente de desenvolvimento de suplemento do Project hospedado</span><span class="sxs-lookup"><span data-stu-id="4e6f0-161">Project hosted add-in development environment</span></span>

<span data-ttu-id="4e6f0-162">Um suplemento hospedado é um suplemento que reside no servidor e é baixado para um navegador para execução de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="4e6f0-162">A hosted add-in is an add-in that resides on the server and is downloaded to a browser for runtime execution.</span></span> <span data-ttu-id="4e6f0-163">Suplementos hospedados podem usar as interfaces JSOM ou REST e escritos em JavaScript.</span><span class="sxs-lookup"><span data-stu-id="4e6f0-163">Hosted add-ins can use the JSOM or REST interfaces and are written in JavaScript.</span></span> <span data-ttu-id="4e6f0-164">Project Online fornece referências à biblioteca JSOM para execução de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="4e6f0-164">Project Online provides references to the JSOM library for runtime execution.</span></span> <span data-ttu-id="4e6f0-165">Desenvolvimento considerando está em uma plataforma Windows, o acompanhamento de recursos necessários:</span><span class="sxs-lookup"><span data-stu-id="4e6f0-165">Assuming development is on a Windows platform, the needed resources follow:</span></span>
  
- <span data-ttu-id="4e6f0-166">O Visual Studio (preferencial) de 2015 ou Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="4e6f0-166">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span>
    
- <span data-ttu-id="4e6f0-167">Ferramentas de desenvolvimento do Office para Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4e6f0-167">Office development tools for Visual Studio</span></span>
    
- <span data-ttu-id="4e6f0-168">Idioma do JavaScript</span><span class="sxs-lookup"><span data-stu-id="4e6f0-168">JavaScript language</span></span>
    
<span data-ttu-id="4e6f0-169">Visite https://github.com/OfficeDev/Project-JSOM-Copy-Work-Packages para um aplicativo de amostra.</span><span class="sxs-lookup"><span data-stu-id="4e6f0-169">Visit https://github.com/OfficeDev/Project-JSOM-Copy-Work-Packages for a sample application.</span></span> 
  
<span data-ttu-id="4e6f0-170">Você pode baixar e executar a amostra em algumas etapas simples:</span><span class="sxs-lookup"><span data-stu-id="4e6f0-170">You can download and run the sample in a few easy steps:</span></span>
  
1. <span data-ttu-id="4e6f0-171">Baixe e abra o aplicativo de amostra</span><span class="sxs-lookup"><span data-stu-id="4e6f0-171">Download and open the sample application</span></span>
    
2. <span data-ttu-id="4e6f0-172">Atualizar o SiteURL na janela Propriedades</span><span class="sxs-lookup"><span data-stu-id="4e6f0-172">Update the SiteURL in the Properties window</span></span>
    
   <span data-ttu-id="4e6f0-173">Project Online examina o escopo de aplicativo do suplemento e as permissões de usuário para controlar o acesso às informações no host do Project Online.</span><span class="sxs-lookup"><span data-stu-id="4e6f0-173">Project Online examines both the application scope of the add-in and the user permissions to govern access to information on the Project Online host.</span></span> <span data-ttu-id="4e6f0-174">Se o acesso negado explicitamente em uma ou ambas as configurações, Project Online nega acesso às informações.</span><span class="sxs-lookup"><span data-stu-id="4e6f0-174">If access is explicitly denied in either or both settings, Project Online denies access to the information.</span></span> <span data-ttu-id="4e6f0-175">Caso contrário, o acesso é concedido.</span><span class="sxs-lookup"><span data-stu-id="4e6f0-175">Otherwise, access is granted.</span></span>
    
3. <span data-ttu-id="4e6f0-176">Habilite [sideloading](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) em seu site.</span><span class="sxs-lookup"><span data-stu-id="4e6f0-176">Enable [sideloading](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) on your site.</span></span>  
    
4. <span data-ttu-id="4e6f0-177">Compile o projeto.</span><span class="sxs-lookup"><span data-stu-id="4e6f0-177">Build the project.</span></span>
    
5. <span data-ttu-id="4e6f0-178">Execute o projeto.</span><span class="sxs-lookup"><span data-stu-id="4e6f0-178">Run the project.</span></span>
    
## <a name="project-provider-hosted-add-in-development-environment"></a><span data-ttu-id="4e6f0-179">Ambiente de desenvolvimento hospedado em provedor suplemento do Project</span><span class="sxs-lookup"><span data-stu-id="4e6f0-179">Project provider-hosted add-in development environment</span></span>

<span data-ttu-id="4e6f0-180">Suplementos do provedor hospedado são aplicativos escritos e que residem em qualquer plataforma da web.</span><span class="sxs-lookup"><span data-stu-id="4e6f0-180">Provider hosted add-ins are applications written and residing on any web platform.</span></span> <span data-ttu-id="4e6f0-181">Eles podem se conectar e executar operações de dados usando o REST (ou CSOM para plataformas de Microsoft) API.</span><span class="sxs-lookup"><span data-stu-id="4e6f0-181">They can connect and perform data operations using the REST (or CSOM for Microsoft platforms) API.</span></span> <span data-ttu-id="4e6f0-182">Qualquer idioma e um ambiente com suporte para a interface REST podem ser usados para desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="4e6f0-182">Any language and environment that supports the REST interface can be used for development.</span></span> 
  
<span data-ttu-id="4e6f0-183">Um exemplo do ambiente de desenvolvimento do Windows para esse tipo de aplicativo inclui os seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="4e6f0-183">An example of the Windows development environment for this type of application includes the following items:</span></span>
  
-  <span data-ttu-id="4e6f0-184">O Visual Studio (preferencial) de 2015 ou Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="4e6f0-184">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span> 
    
- <span data-ttu-id="4e6f0-185">Ferramentas de desenvolvimento do Microsoft Office para Visual Studio (fornecidos com o Visual Studio 2015 Professional e Enterprise Edition)</span><span class="sxs-lookup"><span data-stu-id="4e6f0-185">Microsoft Office Development Tools for Visual Studio (supplied with Visual Studio 2015 Professional and Enterprise editions)</span></span>
    
- <span data-ttu-id="4e6f0-186">.NET framework 4.0 ou mais recente</span><span class="sxs-lookup"><span data-stu-id="4e6f0-186">.NET Framework 4.0 or newer</span></span>
    
- <span data-ttu-id="4e6f0-187">[Pacote de CSOM do SharePoint Online](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (para chamadas do CSOM)</span><span class="sxs-lookup"><span data-stu-id="4e6f0-187">[SharePointOnline CSOM package](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (for CSOM calls)</span></span> 
    
- <span data-ttu-id="4e6f0-188">Uma linguagem de programação, como c#</span><span class="sxs-lookup"><span data-stu-id="4e6f0-188">A programming language, such as C#</span></span> 
    
<span data-ttu-id="4e6f0-189">Visite https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations para trabalhar scripts de amostra.</span><span class="sxs-lookup"><span data-stu-id="4e6f0-189">Visit https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations for working sample scripts.</span></span> 
  
<span data-ttu-id="4e6f0-190">Você pode executar o exemplo em algumas etapas:</span><span class="sxs-lookup"><span data-stu-id="4e6f0-190">You can run the sample in a few steps:</span></span>
  
1. <span data-ttu-id="4e6f0-191">Baixe e abra o aplicativo de amostra</span><span class="sxs-lookup"><span data-stu-id="4e6f0-191">Download and open the sample application</span></span>
    
2. <span data-ttu-id="4e6f0-192">Atualizar o SiteURL na janela Propriedades</span><span class="sxs-lookup"><span data-stu-id="4e6f0-192">Update the SiteURL in the Properties window</span></span>
    
   <span data-ttu-id="4e6f0-193">Project Online examina o escopo de aplicativo do suplemento e as permissões de usuário para controlar o acesso às informações no host do Project Online.</span><span class="sxs-lookup"><span data-stu-id="4e6f0-193">Project Online examines both the application scope of the add-in and the user permissions to govern access to information on the Project Online host.</span></span> <span data-ttu-id="4e6f0-194">Se o acesso negado explicitamente em uma ou ambas as configurações, Project Online nega acesso às informações.</span><span class="sxs-lookup"><span data-stu-id="4e6f0-194">If access is explicitly denied in either or both settings, Project Online denies access to the information.</span></span> <span data-ttu-id="4e6f0-195">Caso contrário, o acesso é concedido.</span><span class="sxs-lookup"><span data-stu-id="4e6f0-195">Otherwise, access is granted.</span></span>
    
3. <span data-ttu-id="4e6f0-196">Habilite [sideloading](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) em seu site.</span><span class="sxs-lookup"><span data-stu-id="4e6f0-196">Enable [sideloading](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) on your site.</span></span> 
    
4. <span data-ttu-id="4e6f0-197">Compile o projeto.</span><span class="sxs-lookup"><span data-stu-id="4e6f0-197">Build the project.</span></span>
    
5. <span data-ttu-id="4e6f0-198">Execute o projeto.</span><span class="sxs-lookup"><span data-stu-id="4e6f0-198">Run the project.</span></span>
    
## <a name="externalstandalone-application-development-environment"></a><span data-ttu-id="4e6f0-199">Ambiente de desenvolvimento de aplicativo externo/autônomo</span><span class="sxs-lookup"><span data-stu-id="4e6f0-199">External/standalone application development environment</span></span>

<span data-ttu-id="4e6f0-200">Um aplicativo autônomo pode chamar Project Online usando o modelo de objeto de lado do cliente (CSOM) ou o REST para se comunicar com o Project Online para criar, recuperar, atualizar e excluir informações residentes no servidor.</span><span class="sxs-lookup"><span data-stu-id="4e6f0-200">A standalone application can call Project Online using the Client Side Object Model (CSOM) or REST to communicate with Project Online to create, retrieve, update, and delete information residing on the server.</span></span> <span data-ttu-id="4e6f0-201">Este é um aplicativo cliente autônomo que depende do nível de acesso de usuário para executar.</span><span class="sxs-lookup"><span data-stu-id="4e6f0-201">This is a standalone client application that depends on the user access level to run.</span></span> 
  
<span data-ttu-id="4e6f0-202">Um exemplo do ambiente de desenvolvimento do Windows para esse tipo de aplicativo inclui os seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="4e6f0-202">An example of the Windows development environment for this type of application includes the following items:</span></span>
  
- <span data-ttu-id="4e6f0-203">O Visual Studio (preferencial) de 2015 ou Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="4e6f0-203">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span> 
    
- <span data-ttu-id="4e6f0-204">Ferramentas de desenvolvimento do Microsoft Office para Visual Studio (fornecidos com o Visual Studio 2015 Professional e Enterprise Edition)</span><span class="sxs-lookup"><span data-stu-id="4e6f0-204">Microsoft Office Development Tools for Visual Studio (supplied with Visual Studio 2015 Professional and Enterprise editions)</span></span>
    
- <span data-ttu-id="4e6f0-205">.NET framework 4.0 ou mais recente</span><span class="sxs-lookup"><span data-stu-id="4e6f0-205">.NET Framework 4.0 or newer</span></span>
    
- <span data-ttu-id="4e6f0-206">[Pacote de CSOM do SharePoint Online](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (para chamadas do CSOM)</span><span class="sxs-lookup"><span data-stu-id="4e6f0-206">[SharePointOnline CSOM package](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (for CSOM calls)</span></span> 
    
- <span data-ttu-id="4e6f0-207">Uma linguagem de programação, como c#</span><span class="sxs-lookup"><span data-stu-id="4e6f0-207">A programming language, such as C#</span></span> 
    
<span data-ttu-id="4e6f0-208">Visite https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields para um aplicativo de amostra.</span><span class="sxs-lookup"><span data-stu-id="4e6f0-208">Visit https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields for a sample application.</span></span> 
  
<span data-ttu-id="4e6f0-209">Você pode executar o exemplo em algumas etapas:</span><span class="sxs-lookup"><span data-stu-id="4e6f0-209">You can run the sample in a few steps:</span></span>
  
1. <span data-ttu-id="4e6f0-210">Baixar o aplicativo de amostra</span><span class="sxs-lookup"><span data-stu-id="4e6f0-210">Download the sample application</span></span>
    
2. <span data-ttu-id="4e6f0-211">Fazer algumas alterações de acessar o site do Project Online — o nome do site, a conta de usuário e senha.</span><span class="sxs-lookup"><span data-stu-id="4e6f0-211">Make a couple of changes to access your Project Online site—the site name, user account, and password.</span></span>
    
   <span data-ttu-id="4e6f0-212">Certifique-se de que o usuário tem acesso a todos os projetos.</span><span class="sxs-lookup"><span data-stu-id="4e6f0-212">Ensure the user has access to all projects.</span></span> <span data-ttu-id="4e6f0-213">Project Online usa as permissões de usuário para controlar o acesso às informações no repositório de dados.</span><span class="sxs-lookup"><span data-stu-id="4e6f0-213">Project Online uses user permissions to govern access to information in the data store.</span></span>
    
3. <span data-ttu-id="4e6f0-214">Adicione o assembly do SharePoint as referências usando o Console do Gerenciador de pacotes do Nuget, disponível no menu Ferramentas, digitando o seguinte no console do Nuget:</span><span class="sxs-lookup"><span data-stu-id="4e6f0-214">Add the SharePoint assembly to the references using the Nuget Package Manager Console, available from the Tools menu by typing the following in the Nuget console:</span></span> 
    
   `Install-Package Microsoft.SharePointOnline.CSOM`

4. <span data-ttu-id="4e6f0-215">Compile o projeto.</span><span class="sxs-lookup"><span data-stu-id="4e6f0-215">Build the project.</span></span>
    
5. <span data-ttu-id="4e6f0-216">Execute o projeto.</span><span class="sxs-lookup"><span data-stu-id="4e6f0-216">Run the project.</span></span>
    
## <a name="next-steps"></a><span data-ttu-id="4e6f0-217">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="4e6f0-217">Next steps</span></span>

<span data-ttu-id="4e6f0-218">Cada aplicativo de amostra possui um artigo para explicar os destaques dos trabalhando com a API de projeto individuais.</span><span class="sxs-lookup"><span data-stu-id="4e6f0-218">Each sample application has an article to explain the highlights of working with the individual Project API.</span></span> <span data-ttu-id="4e6f0-219">Os artigos aparecem na lista a seguir, juntamente com alguns artigos que descrevem as relações de entidade, informações sobre o sistema de consulta e acessar os campos personalizados.</span><span class="sxs-lookup"><span data-stu-id="4e6f0-219">The articles appear in the following list, along with a few articles that describe the entity relationships, information on the query system, and accessing Custom Fields.</span></span> 
  
- [<span data-ttu-id="4e6f0-220">Desenvolvendo um aplicativo do Project Online usando o modelo de objeto do cliente</span><span class="sxs-lookup"><span data-stu-id="4e6f0-220">Developing a Project Online Application Using the Client-side Object Model</span></span>](developing-a-project-online-application-using-the-client-side-object-model.md)
    
- [<span data-ttu-id="4e6f0-221">Desenvolvendo um suplemento Project Online usando o modelo de objeto JavaScript (JSOM)</span><span class="sxs-lookup"><span data-stu-id="4e6f0-221">Developing a Project Online add-in using the JavaScript Object Model (JSOM)</span></span>](developing-a-project-online-add-in-using-the-javascript-object-model-jsom.md)
    
- [<span data-ttu-id="4e6f0-222">Acessar campos personalizados da empresa no Project Online</span><span class="sxs-lookup"><span data-stu-id="4e6f0-222">Accessing Project Online enterprise custom fields</span></span>](accessing-project-online-enterprise-custom-fields.md)
    
## <a name="see-also"></a><span data-ttu-id="4e6f0-223">Confira também</span><span class="sxs-lookup"><span data-stu-id="4e6f0-223">See also</span></span>

<span data-ttu-id="4e6f0-224">Para documentação e exemplos relacionados ao Project Online e desenvolvimento de aplicativos usando CSOM, consulte o [Portal de desenvolvimento do Project](https://developer.microsoft.com/en-us/project).</span><span class="sxs-lookup"><span data-stu-id="4e6f0-224">For documentation and samples related to Project Online and application development using CSOM, see the [Project Development Portal](https://developer.microsoft.com/en-us/project).</span></span>
    

