---
title: Desenvolver um complemento do Project Online usando o Modelo de Objeto do JavaScript (JSOM)
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4a4b1ad2-de46-421d-a698-53c20c90b93a
description: Este artigo descreve o desenvolvimento do Microsoft Project Online Add-in para aprimorar sua experiência com o Project Online. O projeto de desenvolvimento é implementado como um passo a passo. O complemento usado neste artigo lê e exibe os nomes e as IDs de projeto dos projetos publicados da sua conta do Project Online e permite que você faça buscas em busca de tarefas associadas a projetos individuais.
ms.openlocfilehash: 0a472a6300f18aaa65649f44d944445642a59e1a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322679"
---
# <a name="developing-a-project-online-add-in-using-the-javascript-object-model-jsom"></a><span data-ttu-id="9f5c6-105">Desenvolver um complemento do Project Online usando o Modelo de Objeto do JavaScript (JSOM)</span><span class="sxs-lookup"><span data-stu-id="9f5c6-105">Developing a Project Online add-in using the JavaScript Object Model (JSOM)</span></span>

<span data-ttu-id="9f5c6-106">Este artigo descreve o desenvolvimento do Microsoft Project Online Add-in para aprimorar sua experiência com o Project Online.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-106">This article describes Microsoft Project Online Add-in development to enhance your experience with the Project Online.</span></span> <span data-ttu-id="9f5c6-107">O projeto de desenvolvimento é implementado como um passo a passo.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-107">The development project is implemented as a walkthrough.</span></span> <span data-ttu-id="9f5c6-108">O complemento usado neste artigo lê e exibe os nomes e as IDs de projeto dos projetos publicados da sua conta do Project Online e permite que você faça buscas mais precisas para recuperar tarefas associadas a projetos individuais.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-108">The add-in used for this article reads and displays the project names and IDs of the published projects from your Project Online account and allows you to drill down to retrieve tasks associated with individual projects.</span></span>
  
<span data-ttu-id="9f5c6-109">Em tempo de executar, a listagem do complemento é semelhante à ilustração a seguir:</span><span class="sxs-lookup"><span data-stu-id="9f5c6-109">At run time, the add-in listing looks similar to the following illustration:</span></span>
  
<span data-ttu-id="9f5c6-110">![Screen shot showing a listing of JSOM projects and tasks Screen]shot showing a(media/766e5914-f048-48f4-9282-291f55e6e90d.png "listing of JSOM projects and tasks")</span><span class="sxs-lookup"><span data-stu-id="9f5c6-110">![Screen shot showing a listing of JSOM projects and tasks](media/766e5914-f048-48f4-9282-291f55e6e90d.png "Screen shot showing a listing of JSOM projects and tasks")</span></span>
  
<span data-ttu-id="9f5c6-111">O foco do exemplo é a interação com o Project Online, fazendo consultas e definindo o contexto de cada solicitação do serviço.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-111">The focus of the example is the interaction with the Project Online, making queries and setting the context for each request from the service.</span></span> <span data-ttu-id="9f5c6-112">Os elementos da interface do usuário (UI) recebem atenção mínima.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-112">User interface (UI) elements receive minimal attention.</span></span> <span data-ttu-id="9f5c6-113">Em vez disso, as listagem de origem fornecem comentários sobre a interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-113">Instead, the source listings provide comments regarding the UI.</span></span>
  
> [!NOTE]
> <span data-ttu-id="9f5c6-114">Os arquivos de origem para o exemplo de complemento, um projeto do Visual Studio, estão disponíveis em: https://github.com/OfficeDev/Project-JSOM-List-Projects-Tasks.... .</span><span class="sxs-lookup"><span data-stu-id="9f5c6-114">The source files for the example add-in, a Visual Studio project, are available at: https://github.com/OfficeDev/Project-JSOM-List-Projects-Tasks.....</span></span> <span data-ttu-id="9f5c6-115">Mantenha os arquivos de origem úteis como referência enquanto você lê o artigo, pois cada um complementa o outro.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-115">Keep the source files handy as a reference while you read the article, as each complements the other.</span></span> <span data-ttu-id="9f5c6-116">Os arquivos na com build do projeto do Visual Studio e são executáveis com alterações mínimas substituindo a URL do locatário do Project Online na pasta do PWA.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-116">The files in the Visual Studio project build and are executable with minimal changes—substituting the URL for your Project Online tenant down to the PWA folder.</span></span> 
  
## <a name="background"></a><span data-ttu-id="9f5c6-117">Histórico</span><span class="sxs-lookup"><span data-stu-id="9f5c6-117">Background</span></span>

<span data-ttu-id="9f5c6-118">O Project Online é um serviço do Office 365 que fornece às empresas um PPM (gerenciamento de portfólio de projetos) e uma solução de PMO (escritório de gerenciamento de projetos) para coordenar e gerenciar portfólios, programas e projetos.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-118">Project Online is a Office 365 service that provides companies with a project portfolio management (PPM) and project management office (PMO) solution to coordinate and manage portfolios, programs, and projects.</span></span> <span data-ttu-id="9f5c6-119">O Project Online é uma oferta diferente das edições da área de trabalho do Project; ainda assim, o Project Online ainda contém a funcionalidade para manter e acompanhar detalhes do projeto durante toda a vida de um projeto.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-119">Project Online is a different offering than the Project desktop editions; yet, Project Online still contains the functionality to maintain and track project details throughout the life of a project.</span></span> <span data-ttu-id="9f5c6-120">O Project Online foi criado no SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-120">Project Online is built on SharePoint Online.</span></span>
  
<span data-ttu-id="9f5c6-121">Um complemento hospedado do Project Online consiste em JavaScript e arquivos de recursos que interagem com a API de Modelo de Objeto do Lado do Cliente.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-121">A Project Online hosted add-in consists of JavaScript and resource files that interact with the Client-Side-Object-Model API.</span></span> <span data-ttu-id="9f5c6-122">Quando o usuário visita o complemento, o JavaScript e os recursos são baixados e executados no navegador.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-122">When the user visits the add-in, the JavaScript and resources are downloaded and executed within the browser.</span></span> <span data-ttu-id="9f5c6-123">O complemento faz chamadas assíncronas ao Project Online para interagir com o serviço, seja criando, recuperando, atualizando ou excluindo dados.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-123">The add-In makes asynchronous calls to Project Online to interact with the service, whether creating, retrieving, updating, or deleting data.</span></span> 
  
<span data-ttu-id="9f5c6-124">O Project Online executa mais uma ação para proteger informações que pertencem a outros locatários do complemento; ou seja, o Project Online cria um site isolado para interagir com as solicitações do complemento.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-124">Project Online performs one more action to protect information that belongs to other tenants from the add-in; namely, Project Online creates an isolated site to interact with the requests from the add-in.</span></span> <span data-ttu-id="9f5c6-125">Nenhum código personalizado é executado no host do Project Online.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-125">No custom code runs on the Project Online host.</span></span> 
  
<span data-ttu-id="9f5c6-126">A configuração de desenvolvimento para os complementos do Project Online usa o tipo de projeto do Visual Studio SharePoint Add-in.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-126">The development setup for Project Online add-ins uses the Visual Studio SharePoint Add-in project type.</span></span> <span data-ttu-id="9f5c6-127">O complemento é escrito em JavaScript e usa o modelo de objeto do JavaScript do Project (JSOM) para interagir com o serviço do Project Online.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-127">The add-in is written in JavaScript, and uses the Project JavaScript object model (JSOM) to interact with the Project Online service.</span></span> <span data-ttu-id="9f5c6-128">O JSOM herda grande parte de sua funcionalidade do JSOM do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-128">The JSOM inherits much of its functionality from the SharePoint JSOM.</span></span>
  
> [!NOTE]
> <span data-ttu-id="9f5c6-129">Os complementos podem ser publicados e vendidos na Office Store ou implantados em um catálogo de aplicativos privado no SharePoint.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-129">Add-ins can be published and sold in the Office Store or deployed to a private app catalog on SharePoint.</span></span> <span data-ttu-id="9f5c6-130">Para saber mais, [confira Implantar e publicar o Seu Complemento do Office.](https://docs.microsoft.com/office/dev/add-ins/publish/publish)</span><span class="sxs-lookup"><span data-stu-id="9f5c6-130">For more information, see [Deploy and publish your Office Add-in](https://docs.microsoft.com/office/dev/add-ins/publish/publish).</span></span>
> 
> <span data-ttu-id="9f5c6-131">O complemento usado neste artigo é um exemplo para desenvolvedores; não se destina ao uso em um ambiente de produção.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-131">The add-in used in this article is a sample for developers; it is not intended for use in a production environment.</span></span> <span data-ttu-id="9f5c6-132">O objetivo principal é mostrar um exemplo de desenvolvimento de aplicativos para o Project Online.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-132">The primary purpose is to show an example of app development for Project Online.</span></span> 
  
## <a name="prerequisites"></a><span data-ttu-id="9f5c6-133">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="9f5c6-133">Prerequisites</span></span>

<span data-ttu-id="9f5c6-134">Adicione os seguintes itens a um ambiente do Windows com suporte:</span><span class="sxs-lookup"><span data-stu-id="9f5c6-134">Add the following items to a supported Windows environment:</span></span>
  
- <span data-ttu-id="9f5c6-135">**.NET Framework 4.0 ou posterior:** Versões completas da estrutura da versão 4.0 são compatíveis.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-135">**.NET Framework 4.0 or later**: Complete versions of the framework from version 4.0 are compatible.</span></span> <span data-ttu-id="9f5c6-136">O site de download é https://msdn.microsoft.com/vstudio/aa496123.aspx.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-136">The download site is https://msdn.microsoft.com/vstudio/aa496123.aspx.</span></span>
    
- <span data-ttu-id="9f5c6-137">**Visual Studio 2013 ou posterior:**</span><span class="sxs-lookup"><span data-stu-id="9f5c6-137">**Visual Studio 2013 or later**:</span></span>  
    
   - <span data-ttu-id="9f5c6-138">A edição profissional do Visual Studio 2015 está pronta para ser pronta para uso e está disponível em https://www.visualstudio.com/en-us/products/visual-studio-professional-with-msdn-vs.aspx .</span><span class="sxs-lookup"><span data-stu-id="9f5c6-138">The professional edition of Visual Studio 2015 is ready to go out-of-the box and is available at https://www.visualstudio.com/en-us/products/visual-studio-professional-with-msdn-vs.aspx.</span></span>
    
   - <span data-ttu-id="9f5c6-139">A edição da comunidade do Visual Studio 2015 está disponível em https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx .</span><span class="sxs-lookup"><span data-stu-id="9f5c6-139">The community edition of Visual Studio 2015 is available at https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx.</span></span> <span data-ttu-id="9f5c6-140">Esta edição requer a instalação manual do Microsoft Office Developer Tools para Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-140">This edition requires manual installation of the Microsoft Office Developer Tools for Visual Studio.</span></span>
    
   <span data-ttu-id="9f5c6-141">As Ferramentas de Desenvolvedor do Microsoft Office para Visual Studio estão disponíveis em https://www.visualstudio.com/en-us/features/office-tools-vs.aspx .</span><span class="sxs-lookup"><span data-stu-id="9f5c6-141">The Microsoft Office Developer Tools for Visual Studio are available at https://www.visualstudio.com/en-us/features/office-tools-vs.aspx.</span></span>
    
- <span data-ttu-id="9f5c6-142">**Uma conta do Project Online:** fornece acesso ao serviço de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-142">**A Project Online account**: This provides access to the hosting service.</span></span> <span data-ttu-id="9f5c6-143">Confira mais informações sobre como obter uma conta do Project Online em https://products.office.com/en-us/Project/project-online-portfolio-management.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-143">For more information about obtaining a Project Online account, see https://products.office.com/en-us/Project/project-online-portfolio-management.</span></span>
    
   <span data-ttu-id="9f5c6-144">Verifique se o usuário do complemento tem autorização suficiente para acessar alguns projetos no locatário do Project Online.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-144">Ensure that the add-in user has sufficient authorization to access some projects in the Project Online tenant.</span></span> 
    
- <span data-ttu-id="9f5c6-145">**Projetos no site de hospedagem** preenchidos com informações.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-145">**Projects on the hosting site** that are populated with information.</span></span>
    
> [!NOTE]
> <span data-ttu-id="9f5c6-146">O .NET Framework padrão é a estrutura correta a ser usada.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-146">The standard .NET Framework is the correct framework to use.</span></span> <span data-ttu-id="9f5c6-147">Não use o "Perfil de Cliente do .NET Framework 4".</span><span class="sxs-lookup"><span data-stu-id="9f5c6-147">Do not use the ".NET Framework 4 Client Profile".</span></span> 
  
### <a name="set-up-the-visual-studio-project"></a><span data-ttu-id="9f5c6-148">Configurar o projeto do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9f5c6-148">Set up the Visual Studio project</span></span>

<span data-ttu-id="9f5c6-149">A configuração do aplicativo consiste em criar um novo projeto, vincular as bibliotecas apropriadas e declarar os namespaces necessários.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-149">The application setup consists of creating a new project, linking the appropriate libraries and declaring the needed namespaces.</span></span> <span data-ttu-id="9f5c6-150">O Visual Studio apresenta vários tipos de projetos de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-150">Visual Studio presents several types of development projects.</span></span> <span data-ttu-id="9f5c6-151">A seção é breve e muito básica.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-151">The section is brief and very basic.</span></span> <span data-ttu-id="9f5c6-152">O valor que tem as informações é agregado em um só lugar.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-152">The value is having the information is coalesced in one place.</span></span>
  
#### <a name="select-a-visual-studio-project"></a><span data-ttu-id="9f5c6-153">Selecionar um projeto do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9f5c6-153">Select a Visual Studio project</span></span>

<span data-ttu-id="9f5c6-154">Para criar um projeto do tipo apropriado para o complemento, você deve seguir as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-154">To create a project of the appropriate type for the add-in, you must do the following steps.</span></span> <span data-ttu-id="9f5c6-155">As palavras-chave encontradas na tela têm um **atributo em** negrito:</span><span class="sxs-lookup"><span data-stu-id="9f5c6-155">Keywords encountered on the screen have a **bold** attribute:</span></span> 
  
1. <span data-ttu-id="9f5c6-156">No menu Arquivo, escolha **Arquivo**  >  **Novo**  >  **Projeto.**</span><span class="sxs-lookup"><span data-stu-id="9f5c6-156">From the File menu, choose **File** > **New** > **Project**.</span></span> 
    
2. <span data-ttu-id="9f5c6-157">Nos modelos instalados no painel esquerdo, selecione **C#**  >  **Office/SharePoint**  >  **Web Add-ins**.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-157">From the Installed templates in the left pane, select **C#** > **Office/SharePoint** > **Web Add-ins**.</span></span> 
    
3. <span data-ttu-id="9f5c6-158">Na parte superior do painel central, selecione **.NET Framework 4** ou posterior; a versão atual é 4.6.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-158">At the top of the central pane, select **.NET Framework 4** or later; the current version is 4.6.</span></span> 
    
4. <span data-ttu-id="9f5c6-159">Nos tipos de aplicativos no painel central, escolha **o SharePoint Add-in.**</span><span class="sxs-lookup"><span data-stu-id="9f5c6-159">From the application types in the central pane, choose **SharePoint Add-in**.</span></span> 
    
5. <span data-ttu-id="9f5c6-160">Na seção inferior, especifique o nome e o local do projeto e o nome da solução.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-160">In the bottom section, specify a name and location for the project, and a solution name.</span></span> 
    
6. <span data-ttu-id="9f5c6-161">Também na seção inferior, marque a caixa **Criar diretório para a solução**.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-161">Also in the bottom section, check the **Create directory for solution** box.</span></span> 
    
7. <span data-ttu-id="9f5c6-162">Clique em **OK** para criar o projeto inicial.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-162">Click **OK** to create the initial project.</span></span> 
    
<span data-ttu-id="9f5c6-163">O Assistente do Visual Studio faz algumas perguntas de acompanhamento sobre o site de configurações do Project Online (chamado de configurações do SharePoint nas caixas de diálogo) em algumas caixas de diálogo a seguir.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-163">The Visual Studio Wizard asks a few follow-up questions about the Project Online settings site (called SharePoint settings in the dialogs) in a couple of dialogs that follow.</span></span> <span data-ttu-id="9f5c6-164">Aqui estão as perguntas:</span><span class="sxs-lookup"><span data-stu-id="9f5c6-164">Here are the questions:</span></span>
  
1. <span data-ttu-id="9f5c6-165">Qual site do SharePoint você deseja usar para depurar seu complemento?</span><span class="sxs-lookup"><span data-stu-id="9f5c6-165">What SharePoint site do you want to use for debugging your add-in?</span></span> <span data-ttu-id="9f5c6-166">Especifique a URL para seu site do PWA, como https://contoso.sharepoint.com/sites/pwa .</span><span class="sxs-lookup"><span data-stu-id="9f5c6-166">Specify the URL to your PWA site, such as https://contoso.sharepoint.com/sites/pwa.</span></span>
    
2. <span data-ttu-id="9f5c6-167">Como você deseja hospedar seu Add-in do SharePoint?</span><span class="sxs-lookup"><span data-stu-id="9f5c6-167">How do you want to host your SharePoint Add-in?</span></span> <span data-ttu-id="9f5c6-168">Escolha [X] **Hospedado pelo SharePoint.**</span><span class="sxs-lookup"><span data-stu-id="9f5c6-168">Choose [X] **SharePoint-hosted**.</span></span>
    
   <span data-ttu-id="9f5c6-169">Para saber mais sobre os Complementos do SharePoint, incluindo opções de hospedagem, confira [Os Complementos do SharePoint.](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins)</span><span class="sxs-lookup"><span data-stu-id="9f5c6-169">For more information about SharePoint Add-ins, including hosting options, see [SharePoint Add-ins](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins).</span></span>
    
3. <span data-ttu-id="9f5c6-170">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-170">Click **Next**.</span></span> 
    
<span data-ttu-id="9f5c6-171">A segunda caixa de diálogo adicional solicita que você especifique a versão do SharePoint Online para o complemento:</span><span class="sxs-lookup"><span data-stu-id="9f5c6-171">The second additional dialog asks you to specify the SharePoint Online version for the add-in:</span></span> 
  
1. <span data-ttu-id="9f5c6-172">Qual é a versão mais antiga do SharePoint para a qual você deseja direcionar o seu complemento?</span><span class="sxs-lookup"><span data-stu-id="9f5c6-172">What's the earliest version of SharePoint that you want your add-in to target?</span></span> <span data-ttu-id="9f5c6-173">Escolha [X] S **harePoint-Online**.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-173">Choose [X] S **harePoint-Online**.</span></span> 
    
2. <span data-ttu-id="9f5c6-174">Clique em **Concluir**.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-174">Click **Finish**.</span></span> 
    
<span data-ttu-id="9f5c6-175">O Visual Studio cria o projeto e acessa o site do Project Online.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-175">Visual Studio creates the project and accesses the Project Online site.</span></span> 
  
### <a name="enable-sideloading-on-the-project-online-site"></a><span data-ttu-id="9f5c6-176">Habilitar sideload no site do Project Online</span><span class="sxs-lookup"><span data-stu-id="9f5c6-176">Enable sideloading on the Project Online site</span></span>

<span data-ttu-id="9f5c6-177">Sideload é o mecanismo para testar e depurar os complementos do Project Online. Você precisa de dois scripts para sideload: um para habilitar o sideload em seu site do Project Online e outro para desabilitar o sideload depois de concluir o teste e a depuração do complemento.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-177">Sideloading is the mechanism for testing and debugging Project Online add-ins. You need two scripts for sideloading: one to enable sideloading on your Project Online site and another to disable sideloading once you finish testing and debugging the add-in.</span></span>
  
<span data-ttu-id="9f5c6-178">Para obter mais informações sobre como configurar o sideload, consulte [Habilitar SideLoading](https://blogs.msdn.microsoft.com/officeapps/2013/12/10/enable-app-sideloading-in-your-non-developer-site-collection/)do aplicativo em seu conjunto de sites não desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-178">For more information about setting up sideloading, see [Enable app SideLoading in your non-developer site collection](https://blogs.msdn.microsoft.com/officeapps/2013/12/10/enable-app-sideloading-in-your-non-developer-site-collection/).</span></span>
  
> [!NOTE]
> <span data-ttu-id="9f5c6-179">O sideload de aplicativos é um recurso de desenvolvedor/teste.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-179">Sideloading apps is a developer/test feature.</span></span> <span data-ttu-id="9f5c6-180">Ele não **se destina ao uso de produção.**</span><span class="sxs-lookup"><span data-stu-id="9f5c6-180">It is **not intended for production use**.</span></span> <span data-ttu-id="9f5c6-181">Não faça sideload de aplicativos regularmente ou mantenha o sideload de aplicativo habilitado por mais tempo do que você está usando ativamente o recurso.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-181">Do not sideload apps regularly, or keep app sideloading enabled for longer than you are actively using the feature.</span></span> 
  
## <a name="add-content-to-the-add-in-project"></a><span data-ttu-id="9f5c6-182">Adicionar conteúdo ao projeto do complemento</span><span class="sxs-lookup"><span data-stu-id="9f5c6-182">Add content to the add-in project</span></span>

<span data-ttu-id="9f5c6-183">Depois de criar um projeto e configurar o mecanismo de depuração, adicionar conteúdo ao aplicativo inclui as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="9f5c6-183">After creating a project and setting up the debugging mechanism, adding content to the app includes the following tasks:</span></span>
  
- <span data-ttu-id="9f5c6-184">Definindo o escopo do aplicativo</span><span class="sxs-lookup"><span data-stu-id="9f5c6-184">Setting the application scope</span></span>
    
- <span data-ttu-id="9f5c6-185">Vinculando a biblioteca JSOM</span><span class="sxs-lookup"><span data-stu-id="9f5c6-185">Linking the JSOM library</span></span>
    
- <span data-ttu-id="9f5c6-186">Adicionando elementos de interface do usuário ao add-in</span><span class="sxs-lookup"><span data-stu-id="9f5c6-186">Adding UI Elements to the add-in</span></span>
    
- <span data-ttu-id="9f5c6-187">Inicializando e conectando-se ao serviço do Project Online</span><span class="sxs-lookup"><span data-stu-id="9f5c6-187">Initializing and connecting to the Project Online service</span></span>
    
- <span data-ttu-id="9f5c6-188">Recuperar projetos e detalhes/propriedades</span><span class="sxs-lookup"><span data-stu-id="9f5c6-188">Retrieving projects and details/properties</span></span>
    
- <span data-ttu-id="9f5c6-189">Exibindo projetos</span><span class="sxs-lookup"><span data-stu-id="9f5c6-189">Displaying projects</span></span>
    
- <span data-ttu-id="9f5c6-190">Exibindo tarefas para um projeto</span><span class="sxs-lookup"><span data-stu-id="9f5c6-190">Displaying tasks for a Project</span></span>
    
<span data-ttu-id="9f5c6-191">O projeto do complemento consiste em muitos arquivos.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-191">The add-in project consists of many files.</span></span> <span data-ttu-id="9f5c6-192">Neste exemplo, você precisará editar os seguintes arquivos:</span><span class="sxs-lookup"><span data-stu-id="9f5c6-192">In this example, you'll need to edit the following files:</span></span> 
  
- <span data-ttu-id="9f5c6-193">AppManifest.xml</span><span class="sxs-lookup"><span data-stu-id="9f5c6-193">AppManifest.xml</span></span>
    
- <span data-ttu-id="9f5c6-194">Default.aspx</span><span class="sxs-lookup"><span data-stu-id="9f5c6-194">Default.aspx</span></span>
    
- <span data-ttu-id="9f5c6-195">App.js</span><span class="sxs-lookup"><span data-stu-id="9f5c6-195">App.js</span></span>
    
- <span data-ttu-id="9f5c6-196">App.css - opcional; contém definições de estilo desenvolvidas para o complemento</span><span class="sxs-lookup"><span data-stu-id="9f5c6-196">App.css - optional; contains style definitions developed for the add-in</span></span>
    
<span data-ttu-id="9f5c6-197">Se o locatário do Project Online mudar, como mudar de uma avaliação para um site de assinatura, você poderá atualizar as propriedades do projeto, incluindo a Conexão do Servidor e a URL do Site, usando a Janela Propriedades disponível por meio do comando Exibir Janela  >   Propriedades.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-197">If the Project Online tenant changes, such as moving from a trial to a subscription site, you can update the project properties, including the Server Connection and Site URL, using the Properties Window available through the **View** > **Properties Window** command.</span></span> 
  
<span data-ttu-id="9f5c6-198">Você também pode adicionar arquivos ao projeto.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-198">You can also add files to the project.</span></span> <span data-ttu-id="9f5c6-199">Nesse caso, você precisará atualizar o arquivo Elements.xml localizado no mesmo grupo (Conteúdo, Imagens, Páginas ou Scripts) para incluir os novos arquivos.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-199">If so, you'll need to update the Elements.xml file located in the same group (Content, Images, Pages, or Scripts) to include the new files.</span></span> <span data-ttu-id="9f5c6-200">Para saber mais sobre os arquivos de projeto, confira Explorar a estrutura do manifesto do aplicativo e [o pacote de um SharePoint Add-in.](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/explore-the-app-manifest-structure-and-the-package-of-a-sharepoint-add-in)</span><span class="sxs-lookup"><span data-stu-id="9f5c6-200">For more information about the project files, see [Explore the app manifest structure and the package of a SharePoint Add-in](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/explore-the-app-manifest-structure-and-the-package-of-a-sharepoint-add-in).</span></span>
  
### <a name="set-application-scope"></a><span data-ttu-id="9f5c6-201">Definir escopo do aplicativo</span><span class="sxs-lookup"><span data-stu-id="9f5c6-201">Set application scope</span></span>

<span data-ttu-id="9f5c6-202">O complemento precisa de níveis de escopo ou permissão definidos antes que o serviço retorne informações nos resultados da consulta.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-202">The add-in needs scope or permission levels defined before the service returns information in query results.</span></span> <span data-ttu-id="9f5c6-203">Para este complemento, use o escopo a seguir para o projeto do Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-203">For this add-in, use the following scope to the Visual Studio project.</span></span> <span data-ttu-id="9f5c6-204">Essa alteração é feita no AppManifest.xml na guia Permissões:</span><span class="sxs-lookup"><span data-stu-id="9f5c6-204">This change is made to the AppManifest.xml file in the Permissions tab:</span></span>

|<span data-ttu-id="9f5c6-205">Escopo</span><span class="sxs-lookup"><span data-stu-id="9f5c6-205">Scope</span></span>|<span data-ttu-id="9f5c6-206">Permissão</span><span class="sxs-lookup"><span data-stu-id="9f5c6-206">Permission</span></span>|
|:-----|:-----|
|<span data-ttu-id="9f5c6-207">Vários Projetos (Project Server)</span><span class="sxs-lookup"><span data-stu-id="9f5c6-207">Multiple Projects (Project Server)</span></span>  <br/> |<span data-ttu-id="9f5c6-208">Ler</span><span class="sxs-lookup"><span data-stu-id="9f5c6-208">Read</span></span>  <br/> |
   
<span data-ttu-id="9f5c6-209">Salve o arquivo depois de definir o escopo do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-209">Save the file after setting the application scope.</span></span> <span data-ttu-id="9f5c6-210">Caso contrário, nenhum dado será retornado do serviço.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-210">Otherwise, no data will be returned from the service.</span></span> 
  
### <a name="link-the-jsom-library"></a><span data-ttu-id="9f5c6-211">Vincular a biblioteca JSOM</span><span class="sxs-lookup"><span data-stu-id="9f5c6-211">Link the JSOM library</span></span>

<span data-ttu-id="9f5c6-212">As bibliotecas do Project Online em tempo de execução, PS.js e PS.debug.js, são fornecidas pelo Project Online e são sempre a versão mais recente.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-212">The runtime Project Online libraries, PS.js and PS.debug.js, are provided by Project Online and are always the most recent version.</span></span> <span data-ttu-id="9f5c6-213">Os complementos JavaScript que usam O JSOM devem se vincular a uma dessas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-213">JavaScript add-ins that use JSOM must link with one of these libraries.</span></span> <span data-ttu-id="9f5c6-214">As definições de vinculação são adicionadas ao arquivo Default.aspx.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-214">The linking definitions are added in the Default.aspx file.</span></span> <span data-ttu-id="9f5c6-215">Os comandos para usar o PS.js e/ou PS.debug.js são parte do código localizado no arquivo App.js arquivo.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-215">The commands to use the PS.js and/or PS.debug.js are part of the code located in the App.js file.</span></span>
  
<span data-ttu-id="9f5c6-216">Adicione o seguinte comando para PS.js ou PS.debug.js no elemento após  `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` o "SharePoint:ScriptLink" para sp.js.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-216">Add the following command for PS.js or PS.debug.js definition in the  `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` element following the "SharePoint:ScriptLink" for sp.js.</span></span> 
  
```js
<SharePoint:ScriptLink name="PS.js" runat="server" OnDemand="false" LoadAfterUI="true" Localizable="false" />
```

> [!NOTE]
> <span data-ttu-id="9f5c6-217">O **atributo OnDemand** para PS.js ou PS.debug.js definido como **falso**.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-217">The **OnDemand** attribute for PS.js or PS.debug.js set to **false**.</span></span> 
  
### <a name="add-ui-elements-to-the-add-in"></a><span data-ttu-id="9f5c6-218">Adicionar elementos de interface do usuário ao add-in</span><span class="sxs-lookup"><span data-stu-id="9f5c6-218">Add UI elements to the add-in</span></span>

<span data-ttu-id="9f5c6-219">O exemplo de um complemento consiste em alguns componentes.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-219">The example add-in consists of a few components.</span></span> <span data-ttu-id="9f5c6-220">As descrições de elementos estáticos estão localizadas no arquivo Default.aspx.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-220">Static element descriptions are located in the Default.aspx file.</span></span> <span data-ttu-id="9f5c6-221">As descrições de elementos dinâmicos e o código para todos os componentes estão localizados App.js arquivo.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-221">Dynamic element descriptions and code for all components are located in the App.js file.</span></span> <span data-ttu-id="9f5c6-222">Para comentários sobre os componentes, consulte as listagem do código-fonte.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-222">For comments regarding the components, refer to the source code listings.</span></span> <span data-ttu-id="9f5c6-223">Aqui está uma lista dos componentes da interface do usuário no complemento:</span><span class="sxs-lookup"><span data-stu-id="9f5c6-223">Here is a list of the UI components in the add-in:</span></span>
  
- <span data-ttu-id="9f5c6-224">Título</span><span class="sxs-lookup"><span data-stu-id="9f5c6-224">Title</span></span>
    
- <span data-ttu-id="9f5c6-225">Verbiage introdutório</span><span class="sxs-lookup"><span data-stu-id="9f5c6-225">Introductory verbiage</span></span>
    
- <span data-ttu-id="9f5c6-226">Botão para remover tarefas da tabela</span><span class="sxs-lookup"><span data-stu-id="9f5c6-226">Button to remove tasks from the table</span></span>
    
- <span data-ttu-id="9f5c6-227">Tabela que lista a ID e o nome do projeto e as informações da tarefa.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-227">Table that lists the project ID and name, and the task information.</span></span>
    
- <span data-ttu-id="9f5c6-228">Botão Tarefas (clonado uma vez para cada projeto) que importa dados de tarefa para a tabela.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-228">Tasks Button (cloned once for each project) that imports task data into the table.</span></span>
    
<span data-ttu-id="9f5c6-229">Para obter detalhes da interface do usuário, como o título e a parte de título da tabela do projeto, consulte o arquivo de projeto Default.aspx.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-229">For details of the user interface, such as the title and the header portion of the project table, see the Default.aspx project file.</span></span>
  
### <a name="initialize-and-connect-to-the-host-system"></a><span data-ttu-id="9f5c6-230">Inicializar e conectar-se ao sistema host</span><span class="sxs-lookup"><span data-stu-id="9f5c6-230">Initialize and connect to the host system</span></span>

<span data-ttu-id="9f5c6-231">O App.js arquivo contém o código JavaScript.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-231">The App.js file contains the JavaScript code.</span></span> <span data-ttu-id="9f5c6-232">O complemento é carregado PS.js no navegador e chama a função initializePage.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-232">The add-in loads PS.js in the browser, and then calls the initializePage function.</span></span> <span data-ttu-id="9f5c6-233">InitializePage recupera um contexto para o ponto de extremidade do Project Online e inicia a função loadProjects.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-233">InitializePage retrieves a context to the Project Online endpoint and starts the loadProjects function.</span></span>
  
```js
    'use strict';
    SP.SOD.executeOrDelayUntilScriptLoaded(initializePage, "PS.js");
    //Project PWA Context and published projects in PWA
    var projContext;
    var projects;
    function initializePage() {
        //Get the Project context for this web
        projContext = PS.ProjectContext.get_current();
        loadProjects();
    }
    //General CSOM failure event handler
    //Invoked when ExecuteQueryAsync returns unsuccessfully
    function onRequestFailed(sender, args) {
        alert("Failed to execute: " + args.get_message());
        return;
    };

```

### <a name="retrieve-the-projects"></a><span data-ttu-id="9f5c6-234">Recuperar os projetos</span><span class="sxs-lookup"><span data-stu-id="9f5c6-234">Retrieve the projects</span></span>

<span data-ttu-id="9f5c6-235">A função loadProjects consulta o serviço para os nomes e IDs do projeto.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-235">The loadProjects function queries the service for the project names and IDs.</span></span> 
  
<span data-ttu-id="9f5c6-236">O aplicativo recupera o nome do projeto e a ID do projeto. Outras informações sobre o projeto estão disponíveis e podem ser acessadas modificando o método de carregamento para identificar explicitamente as propriedades a serem recuperadas.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-236">The application retrieves the project name and project Id. Other information about the project is available and can be accessed by modifying the load method to identify explicitly the properties to retrieve.</span></span> <span data-ttu-id="9f5c6-237">Um exemplo é fornecido no código como um comentário.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-237">An example is provided in the code as a comment.</span></span> 
  
<span data-ttu-id="9f5c6-238">Se a consulta for bem-sucedida, o complemento continuará chamando displayProjects.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-238">If the query succeeds, the add-in continues by calling displayProjects.</span></span> 
  
```js
    //Query CSOM and get the list of projects in PWA
    function loadProjects() {
        projects = projContext.get_projects();
    //Request to server - identifies what to retrieve
        projContext.load(projects, 'Include(Name, Id)');
        //Notice to server to execute query
        projContext.executeQueryAsync(displayProjects, onRequestFailed);
        // Syntax for requesting more fields to pull down from server
        // projContext.load(projects, 'Include(Name, Description, StartDate, 
        // Id, IsCheckedOut)');
    }

```

### <a name="display-the-projects"></a><span data-ttu-id="9f5c6-239">Exibir os projetos</span><span class="sxs-lookup"><span data-stu-id="9f5c6-239">Display the projects</span></span>

<span data-ttu-id="9f5c6-240">A função displayProjects cria uma tabela, uma linha por projeto e um botão para mostrar as tarefas do projeto específico.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-240">The displayProjects function creates a table, one row per project, and a button to show the tasks for the specific project.</span></span> 
  
```js
    //Display the projects with names and ids in a table
    function displayProjects() {
        //Current published project and ID
        var p, projId;
        //Project table rows to publish collectively
        var pTable = []; 
        var pEnum = projects.getEnumerator();
        //Build a 3-column table, with one project per row.
        while (pEnum.moveNext()) {
            p = pEnum.get_current();
        
            //Items used in getting information for table rows:
            //Current published project object, and ID and name
            // var project = p;
            // var projId = p.get_id();
            // var projName = p.get_name();
        
            //Continue processing/working with project object as needed.
        }
    }

```

> [!NOTE]
> <span data-ttu-id="9f5c6-241">O loop while acessa as propriedades de ID e nome.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-241">The while loop accesses the ID and name properties.</span></span> <span data-ttu-id="9f5c6-242">Isso é um pouco diferente do projeto do código-fonte que chama uma função que, por sua vez, acessa as mesmas propriedades.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-242">This is slightly different than the source code project that calls a function that, in turn, accesses the same properties.</span></span> 
  
### <a name="display-the-tasks-for-a-project"></a><span data-ttu-id="9f5c6-243">Exibir as tarefas de um projeto</span><span class="sxs-lookup"><span data-stu-id="9f5c6-243">Display the tasks for a project</span></span>

<span data-ttu-id="9f5c6-244">As tarefas, enquanto fazem parte do complemento, não fazem parte do carregamento inicial.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-244">The tasks, while part of the add-in, are not part of the initial loading.</span></span> <span data-ttu-id="9f5c6-245">Se o usuário estiver interessado nas tarefas associadas a um projeto, clicar no botão "Mostrar Tarefas" faz com que as tarefas sejam exibidas na lista usando o manipulador de eventos btnLoadTasks.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-245">If the user is interested in the tasks associated with a project, clicking the "Show Tasks" button causes the tasks to display in the list using the btnLoadTasks event handler.</span></span> 
  
<span data-ttu-id="9f5c6-246">O manipulador de eventos btnLoadTasks, com a ID de projeto apropriada, solicita as tarefas para o projeto especificado do servidor.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-246">The btnLoadTasks event handler, with the appropriate project ID, requests the tasks for the specified project from the server.</span></span> <span data-ttu-id="9f5c6-247">Depois de recuperado, btnLoadTasks passa a lista de tarefas para displayTasks para apresentar as tarefas na tela.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-247">Once retrieved, btnLoadTasks passes the task list to displayTasks to present the tasks onscreen.</span></span>
  
```js
    //Query CSOM and get the list of tasks for a specific project
    function btnLoadTasks(pid) {
        //Event handler for the "Show tasks" buttons. 
        //
        //The project ID is the sole argument and is used to get the appropriate task 
        //info from the service.
        //The project ID is also the button name, and is used to identify where to place
        //the task information in the table.
        //
        //Project ID to pass to the event handler
        var projId = pid;
        //
        //Get the project reference
        var pProj = projects.getById(projId);
        //
        //Get the tasks collection reference associated with the project.
        var tasks = pProj.get_tasks();
        //
        projContext.load(tasks, 'Include(Id, Name, Start, ScheduledStart, Completion)');
        //
        //If the query succeeds, displayTasks presents the tasks to the user.
        projContext.executeQueryAsync(function () { displayTasks(tasks, projId) }, onRequestFailed);
    }

```

<span data-ttu-id="9f5c6-248">A função displayTasks exibe as tarefas associadas a um projeto especificado imediatamente abaixo da entrada do projeto.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-248">The displayTasks function displays the tasks associated with a specified project immediately beneath the project entry.</span></span>
  
```js
    //Insert tasks for the specified project immediately underneath the project entry 
    //in the table.
    function displayTasks(tasks, projId) {
        //selected project ID
        var pId = projId;
        //individual task
        var t;
        //Task table rows to publish collectively
        var tTable = [];
        var tEnum = tasks.getEnumerator();
        //Build table one task per row.
        while (tEnum.moveNext()) {
            t = tEnum.get_current();
            //
            //Items used in getting information for table rows:
            //Current task object, and ID and name
            // var task = t;
            // var taskId = t.get_id();
            // var taskName = t.get_name();
            
            //Continue processing/working with task object as needed.
        }
    }

```

> [!NOTE]
> <span data-ttu-id="9f5c6-249">O loop while acessa a ID da tarefa e as propriedades do nome.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-249">The while loop accesses the task ID and name properties.</span></span> <span data-ttu-id="9f5c6-250">Isso é um pouco diferente do projeto do código-fonte que chama uma função que, por sua vez, acessa as mesmas propriedades.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-250">This is slightly different than the source code project that calls a function that, in turn, accesses the same properties.</span></span> 
  
<span data-ttu-id="9f5c6-251">Exemplo de saída para as tarefas de um único projeto a seguir.</span><span class="sxs-lookup"><span data-stu-id="9f5c6-251">Sample output for the tasks of a single project follows.</span></span>
  
<span data-ttu-id="9f5c6-252">![Captura de tela mostrando a saída de uma captura de tela de tarefa]do projeto mostrando a saída de uma tarefa do(media/f6500a3f-000b-4f3e-9be6-9a74d0bea15e.png "projeto")</span><span class="sxs-lookup"><span data-stu-id="9f5c6-252">![Screen shot showing the output for a project task](media/f6500a3f-000b-4f3e-9be6-9a74d0bea15e.png "Screen shot showing the output for a project task")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9f5c6-253">Confira também</span><span class="sxs-lookup"><span data-stu-id="9f5c6-253">See also</span></span>

<span data-ttu-id="9f5c6-254">Confira a documentação e exemplos relacionados ao desenvolvimento de aplicativos usando o CSOM e Project Online no [Portal de Desenvolvimento do Project](https://developer.microsoft.com/en-us/project).</span><span class="sxs-lookup"><span data-stu-id="9f5c6-254">For documentation and samples related to Project Online and application development using CSOM, see the [Project Development Portal](https://developer.microsoft.com/en-us/project).</span></span>
    


