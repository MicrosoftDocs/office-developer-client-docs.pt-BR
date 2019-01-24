---
title: Desenvolvimento de um aplicativo do Project Online usando o modelo de objeto do cliente
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
ms.assetid: 5740d0b2-5d36-40e4-9e83-577cb186359f
description: Este artigo descreve o desenvolvimento de aplicativos do Microsoft Project Online para área de trabalho, usando o .NET Framework 4.0. O aplicativo descrito neste artigo recupera informações do servidor de hospedagem.
localization_priority: Priority
ms.openlocfilehash: 3d3c2dd5b896c10dab9a0494288f38610cbc99e1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712936"
---
# <a name="developing-a-project-online-application-using-the-client-side-object-model"></a><span data-ttu-id="01ce1-104">Desenvolvimento de um aplicativo do Project Online usando o modelo de objeto do cliente</span><span class="sxs-lookup"><span data-stu-id="01ce1-104">Developing a Project Online application using the client-side object model</span></span>

<span data-ttu-id="01ce1-105">Este artigo descreve o desenvolvimento de aplicativos do Microsoft Project Online para área de trabalho, usando o .NET Framework 4.0.</span><span class="sxs-lookup"><span data-stu-id="01ce1-105">This article describes Microsoft Project Online application development for desktop applications using the .NET Framework 4.0.</span></span> <span data-ttu-id="01ce1-106">O aplicativo descrito neste artigo recupera informações do servidor de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="01ce1-106">The application described in this article retrieves information from the hosting server.</span></span> 
  
## <a name="background"></a><span data-ttu-id="01ce1-107">Histórico</span><span class="sxs-lookup"><span data-stu-id="01ce1-107">Background</span></span>

<span data-ttu-id="01ce1-108">O Microsoft Project começou como um aplicativo da área de trabalho no início da década de 1990.</span><span class="sxs-lookup"><span data-stu-id="01ce1-108">Microsoft Project started as desktop application in the early 1990's.</span></span> <span data-ttu-id="01ce1-109">Atualmente o Project é muito mais, o que se comprova por sua variedade:</span><span class="sxs-lookup"><span data-stu-id="01ce1-109">Today, Project is much more, as its several varieties attest:</span></span>
  
- <span data-ttu-id="01ce1-110">O Project Standard Edition é um aplicativo da área de trabalho executado como um aplicativo autônomo.</span><span class="sxs-lookup"><span data-stu-id="01ce1-110">Project standard edition is a desktop application that runs as a stand-alone application.</span></span>
    
- <span data-ttu-id="01ce1-111">O Project Professional Edition é um aplicativo da área de trabalho que pode interagir e compartilhar dados com um servidor em uma escala maior, além de ter as mesmas funcionalidades do Project Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="01ce1-111">Project professional edition is a desktop application that can interact and share data with a server on a larger scale, as well as perform the functionality found in Project standard edition.</span></span>
    
- <span data-ttu-id="01ce1-112">O Project Online é um serviço hospedado da Microsoft que oferece às empresas uma solução no nível de PMO para coordenar e gerenciar projetos, programas e portfólios.</span><span class="sxs-lookup"><span data-stu-id="01ce1-112">Project Online is a Microsoft-hosted service that provides companies with a PMO-level solution to coordinate and manage projects, programs, and portfolios.</span></span> <span data-ttu-id="01ce1-113">Diferente das edições da área de trabalho, o Project Online pode manter e controlar os detalhes do projeto durante a vigência dele.</span><span class="sxs-lookup"><span data-stu-id="01ce1-113">A different offering than the desktop editions, Project Online can maintain and track project details throughout the life of a project.</span></span> 
    
- <span data-ttu-id="01ce1-114">O Project Server é um serviço hospedado pela empresa em que ela gerencia e protege o servidor contendo informações de projetos, programas e portfólios.</span><span class="sxs-lookup"><span data-stu-id="01ce1-114">Project Server is an enterprise-hosted service in which the enterprise manages and secures the server containing project, program, and portfolio information.</span></span> <span data-ttu-id="01ce1-115">O Project Server, por proteger o servidor internamente, oferece os recursos orientados a projetos, programas e portfólios do Project Online hospedado externamente com maior capacidade de personalização.</span><span class="sxs-lookup"><span data-stu-id="01ce1-115">Project Server, by virtue of securing the server in-house, offers the project, program, and portfolio oriented features of externally-hosted Project Online with a greater capacity for customization.</span></span>
    
<span data-ttu-id="01ce1-116">O Project Online tem três conjuntos de API online: CSOM (Modelo de Objeto do Cliente), JSOM (Modelo de Objeto do JavaScript) e REST (Transferência de Estado Representacional).</span><span class="sxs-lookup"><span data-stu-id="01ce1-116">Project Online has three online API sets: Client-side Object Model (CSOM), JavaScript Object Model (JSOM), and Representational State Transfer (REST).</span></span> 
  
- <span data-ttu-id="01ce1-117">A implementação do .NET CSOM é a interface preferencial ao desenvolver aplicativos para Windows que interagem com locatários do Project Online.</span><span class="sxs-lookup"><span data-stu-id="01ce1-117">The .NET CSOM implementation is the preferred interface when developing Windows applications that interact with Project Online tenants.</span></span> <span data-ttu-id="01ce1-118">Entre os ambientes típicos de aplicativos voltados para o usuário estão os computadores Windows e os dispositivos Microsoft Surface.</span><span class="sxs-lookup"><span data-stu-id="01ce1-118">Typical environments for user-centric applications include Windows desktops and Microsoft Surface devices.</span></span> <span data-ttu-id="01ce1-119">Aplicativos de back-end escritos com .NET CSOM podem se conectar a outros servidores como fontes de dados e lógicas corporativas que sejam externas ao Project Online.</span><span class="sxs-lookup"><span data-stu-id="01ce1-119">Back-end applications written with .NET CSOM can connect to other servers for business logic and data sources that are external to Project Online.</span></span> <span data-ttu-id="01ce1-120">Solicitações de recuperação no Project Online usam um sistema de consulta equivalente ao LINQ que oferece diversas melhorias em relação às funções básicas de recuperação.</span><span class="sxs-lookup"><span data-stu-id="01ce1-120">Retrieval requests to Project Online use a LINQ-like query system that offers several enhancements over basic retrieval functions.</span></span>
    
- <span data-ttu-id="01ce1-121">A interface do JSOM (Modelo de Objeto do JavaScript) oferece suporte a navegadores para Suplementos do Project Online. Um suplemento é um aplicativo web que fica armazenado em um locatário do Project Online.</span><span class="sxs-lookup"><span data-stu-id="01ce1-121">The JavaScript Object Model (JSOM) interface provides cross-browser support for Project Online Add-ins. An add-in is a web application that is stored in the Project Online tenant.</span></span> <span data-ttu-id="01ce1-122">Quando um usuário deseja executar um suplemento, o código do suplemento é baixado e executado no navegador do computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="01ce1-122">When a user wants to run an add-in, the code for the add-in downloads and runs in the browser on the user machine.</span></span> 
    
- <span data-ttu-id="01ce1-123">O modelo de REST/Odata proporciona uma comunicação com base em HTTP. Essa interface é recomendável para aplicativos que não estão em ambientes Windows.</span><span class="sxs-lookup"><span data-stu-id="01ce1-123">The REST/Odata model provides HTTP-based communication, This interface is recommended for applications in non-Windows environments.</span></span> <span data-ttu-id="01ce1-124">Pontos de extremidade de comunicações são objetos no site do PWA (Projeto de Aplicativo Web).</span><span class="sxs-lookup"><span data-stu-id="01ce1-124">Communication endpoints are the objects in the Project Web Application (PWA) site.</span></span> <span data-ttu-id="01ce1-125">Os resultados fornecem códigos de status HTTP normal.</span><span class="sxs-lookup"><span data-stu-id="01ce1-125">Results provide normal HTTP status codes.</span></span>
    
<span data-ttu-id="01ce1-126">Este artigo aborda um aplicativo que usa a interface do .NET CSOM.</span><span class="sxs-lookup"><span data-stu-id="01ce1-126">This article focuses on an application that uses the .NET CSOM interface.</span></span>
  
## <a name="prerequisites"></a><span data-ttu-id="01ce1-127">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="01ce1-127">Prerequisites</span></span>

<span data-ttu-id="01ce1-128">Comece com um sistema de base executando o Windows 10 e adicione os seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="01ce1-128">Start with a base system running Windows 10, and add the following items:</span></span>
  
- <span data-ttu-id="01ce1-129">.NET Framework 4.0 ou posterior – Use a estrutura completa.</span><span class="sxs-lookup"><span data-stu-id="01ce1-129">.Net Framework 4.0 or later -- Use the complete framework.</span></span> <span data-ttu-id="01ce1-130">O site de download é https://msdn.microsoft.com/vstudio/aa496123.aspx.</span><span class="sxs-lookup"><span data-stu-id="01ce1-130">The download site is https://msdn.microsoft.com/vstudio/aa496123.aspx.</span></span>
    
- <span data-ttu-id="01ce1-131">Visual Studio 2013 ou posterior – Qualquer edição é aceitável.</span><span class="sxs-lookup"><span data-stu-id="01ce1-131">Visual Studio 2013 or later -- Any edition is acceptable.</span></span> <span data-ttu-id="01ce1-132">A edição da comunidade do Visual Studio 2015 foi usada para desenvolver o aplicativo de exemplo.</span><span class="sxs-lookup"><span data-stu-id="01ce1-132">The community edition of Visual Studio 2015 was used to develop the sample application.</span></span> <span data-ttu-id="01ce1-133">A edição da comunidade está disponível em https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx.</span><span class="sxs-lookup"><span data-stu-id="01ce1-133">The community edition is available at https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx.</span></span>
    
- <span data-ttu-id="01ce1-134">SDK dos Componentes de Clientes do SharePoint – O Project Online e o Project Server estão acima do SharePoint e dos assemblies do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="01ce1-134">SharePoint Client Components SDK -- Project Online and Project Server sit on top of SharePoint, and SharePoint assemblies.</span></span> <span data-ttu-id="01ce1-135">Os Componentes do Cliente do SharePoint são incluídos nas edições do Visual Studio Professional e Enterprise.</span><span class="sxs-lookup"><span data-stu-id="01ce1-135">The SharePoint Client Components are included in Visual Studio Professional and Enterprise editions.</span></span> <span data-ttu-id="01ce1-136">Se você usar a edição Visual Studio Community, a versão mais recente do SDK de Ferramentas de Desenvolvedor do Office estará disponível no seguinte site: https://www.microsoft.com/en-us/download/details.aspx?id=35585.</span><span class="sxs-lookup"><span data-stu-id="01ce1-136">If you use Visual Studio Community edition, the latest version of the Office Developer Tools SDK is available at the following site: https://www.microsoft.com/en-us/download/details.aspx?id=35585.</span></span>
    
- <span data-ttu-id="01ce1-137">Uma conta do Project Online – Fornece acesso ao site de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="01ce1-137">A Project Online account -- This provides access to the hosting site.</span></span> <span data-ttu-id="01ce1-138">Confira mais informações sobre como obter uma conta do Project Online em https://products.office.com/en-us/Project/project-online-portfolio-management.</span><span class="sxs-lookup"><span data-stu-id="01ce1-138">For more information about obtaining a Project Online account, see https://products.office.com/en-us/Project/project-online-portfolio-management.</span></span>
    
- <span data-ttu-id="01ce1-139">Projetos no site de hospedagem que são preenchidos com informações</span><span class="sxs-lookup"><span data-stu-id="01ce1-139">Projects on the hosting site that are populated with information</span></span>
    
> [!NOTE]
> <span data-ttu-id="01ce1-140">O .NET Framework padrão (4.0 ou posterior) é a estrutura correta a se usar.</span><span class="sxs-lookup"><span data-stu-id="01ce1-140">The standard .NET Framework (4.0 or later) is the correct framework to use.</span></span> <span data-ttu-id="01ce1-141">Não use o .NET Framework 4 Client Profile.</span><span class="sxs-lookup"><span data-stu-id="01ce1-141">Do not use the .NET Framework 4 Client Profile.</span></span> 
  
## <a name="develop-the-application"></a><span data-ttu-id="01ce1-142">Desenvolver o aplicativo</span><span class="sxs-lookup"><span data-stu-id="01ce1-142">Develop the application</span></span>

<span data-ttu-id="01ce1-143">Ao desenvolver um aplicativo de área de trabalho para o SharePoint, a interface preferida é o CSOM (Modelo de Objeto do Cliente) do Project.</span><span class="sxs-lookup"><span data-stu-id="01ce1-143">In developing a desktop application for SharePoint, the preferred interface is the Project client side object model (CSOM).</span></span> 
  
<span data-ttu-id="01ce1-144">É possível baixar a amostra completa em https://github.com/OfficeDev/Project-CSOM-List-Projects-Tasks.</span><span class="sxs-lookup"><span data-stu-id="01ce1-144">You can download the completed sample at https://github.com/OfficeDev/Project-CSOM-List-Projects-Tasks.</span></span>
  
<span data-ttu-id="01ce1-145">Os dois primeiros tópicos abordam as questões básicas: a criação de um projeto do Visual Studio com namespaces apropriados e assemblies, e o acesso ao servidor de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="01ce1-145">The first two topics cover basic issues: creating a Visual Studio project with appropriate namespaces and assemblies, and accessing the hosting server.</span></span> <span data-ttu-id="01ce1-146">Os tópicos restantes lidam com a recuperação de informações por meio do CSOM, de um e de diversos objetos.</span><span class="sxs-lookup"><span data-stu-id="01ce1-146">The remaining topics deal with retrieving information through the CSOM, from one and many objects.</span></span> 
  
<span data-ttu-id="01ce1-147">Recuperar informações do host é um processo de duas ações nos aplicativos cliente.</span><span class="sxs-lookup"><span data-stu-id="01ce1-147">Retrieving information from the host is a two-action process from client applications.</span></span> <span data-ttu-id="01ce1-148">Primeiro o aplicativo especifica e envia uma ou mais solicitações de recuperação para o servidor.</span><span class="sxs-lookup"><span data-stu-id="01ce1-148">First, the application specifies and sends one or more retrieval requests to the server.</span></span> <span data-ttu-id="01ce1-149">Depois o aplicativo emite uma notificação para o servidor executar as consultas enviadas.</span><span class="sxs-lookup"><span data-stu-id="01ce1-149">Second, the application issues a notification to the server to execute the submitted queries.</span></span> <span data-ttu-id="01ce1-150">O servidor responde enviando os resultados da consulta para o cliente.</span><span class="sxs-lookup"><span data-stu-id="01ce1-150">The server responds by sending the query results to the client.</span></span>
  
### <a name="set-up-the-visual-studio-project"></a><span data-ttu-id="01ce1-151">Configurar o projeto do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="01ce1-151">Step 1: Set up the Visual Studio project</span></span>

<span data-ttu-id="01ce1-152">A instalação do aplicativo consiste em criar um novo projeto, vincular os assemblies apropriados e declarar os namespaces necessários.</span><span class="sxs-lookup"><span data-stu-id="01ce1-152">The application setup consists of creating a new project, linking the appropriate assemblies and declaring the needed namespaces.</span></span> <span data-ttu-id="01ce1-153">O Visual Studio apresenta vários tipos de projetos de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="01ce1-153">Visual Studio presents several types of development projects.</span></span> 
  
#### <a name="select-a-visual-studio-project"></a><span data-ttu-id="01ce1-154">Selecionar um projeto do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="01ce1-154">Select a Visual Studio project</span></span>

1. <span data-ttu-id="01ce1-155">Inicie o Visual Studio e selecione **Iniciar um Novo Projeto** na página inicial.</span><span class="sxs-lookup"><span data-stu-id="01ce1-155">Launch Visual Studio and select **Start A New Project** on the Start Page.</span></span> 
    
   <span data-ttu-id="01ce1-156">A caixa de diálogo Novo Projeto exibe modelos de aplicativos disponíveis e os campos de dados de qualquer modelo selecionado.</span><span class="sxs-lookup"><span data-stu-id="01ce1-156">The New Project dialog displays available application templates, and data fields for any selected template.</span></span> 
    
2. <span data-ttu-id="01ce1-157">Para esse aplicativo, especifique os itens a seguir.</span><span class="sxs-lookup"><span data-stu-id="01ce1-157">For this application, specify the following items.</span></span> <span data-ttu-id="01ce1-158">As palavras-chave da tela têm um atributo em negrito:</span><span class="sxs-lookup"><span data-stu-id="01ce1-158">Keywords encountered on the screen have a bold attribute:</span></span>
    
   1. <span data-ttu-id="01ce1-159">nos modelos Instalados no painel esquerdo, selecione \*\* C#\*\* => **Windows** => **Área de trabalho Clássica**.</span><span class="sxs-lookup"><span data-stu-id="01ce1-159">From the Installed templates in the left pane, select **C#** => **Windows** => **Classic desktop**.</span></span> 
    
   2. <span data-ttu-id="01ce1-160">Na parte superior do painel central, selecione **.NET Framework 4**.</span><span class="sxs-lookup"><span data-stu-id="01ce1-160">At the top of the central pane, select **.NET Framework 4**.</span></span> 
    
   3. <span data-ttu-id="01ce1-161">Nos tipos de aplicativo no painel central, escolha **Aplicativo do Console**.</span><span class="sxs-lookup"><span data-stu-id="01ce1-161">From the application types in the central pane, choose **Console Application**.</span></span> 
    
   4. <span data-ttu-id="01ce1-162">Na seção inferior, especifique o nome e o local do projeto e o nome da solução.</span><span class="sxs-lookup"><span data-stu-id="01ce1-162">In the bottom section, specify a name and location for the project, and a solution name.</span></span> 
    
   5. <span data-ttu-id="01ce1-163">Também na seção inferior, marque a caixa **Criar diretório para a solução**.</span><span class="sxs-lookup"><span data-stu-id="01ce1-163">Also in the bottom section, check the **Create directory for solution** box.</span></span> 
    
3. <span data-ttu-id="01ce1-164">Clique em **OK** para criar o projeto inicial.</span><span class="sxs-lookup"><span data-stu-id="01ce1-164">Click **OK** to create the workflow.</span></span> 
    
#### <a name="add-assemblies"></a><span data-ttu-id="01ce1-165">Adicionar assemblies</span><span class="sxs-lookup"><span data-stu-id="01ce1-165">Add assemblies</span></span>

<span data-ttu-id="01ce1-166">A solução VS precisa do assembly ProjectServerClient do SDK do Project 2013, de um conjunto de assemblies do SDK do SharePoint e do assembly .NET Framework System.Security.</span><span class="sxs-lookup"><span data-stu-id="01ce1-166">The VS solution needs the ProjectServerClient assembly from the Project 2103 SDK, a couple of assemblies from the SharePoint SDK, and the .NET Framework System.Security assembly.</span></span>
  
1. <span data-ttu-id="01ce1-167">No Explorador de Soluções do VS, clique na entrada Referências e selecione **Adicionar Referência...**</span><span class="sxs-lookup"><span data-stu-id="01ce1-167">In the VS Solution Explorer, right-click the References entry, and select **Add Reference…**</span></span> <span data-ttu-id="01ce1-168">no menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="01ce1-168">from the shortcut menu.</span></span> 
    
2. <span data-ttu-id="01ce1-169">Verifique a **Microsoft.ProjectServer.Client.dll**.</span><span class="sxs-lookup"><span data-stu-id="01ce1-169">Check the **Microsoft.ProjectServer.Client.dll**.</span></span> 
    
   <span data-ttu-id="01ce1-170">Se necessário, clique no botão **Procurar...**</span><span class="sxs-lookup"><span data-stu-id="01ce1-170">If needed, click the **Browse…**</span></span> <span data-ttu-id="01ce1-171">na parte inferior da caixa de diálogo e navegue até o diretório de instalação do SDK do Project 2013 para localizar o assembly.</span><span class="sxs-lookup"><span data-stu-id="01ce1-171">button at the bottom of the dialog and navigate to the Project 2013 SDK installation directory to locate the assembly.</span></span> 
    
3. <span data-ttu-id="01ce1-172">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="01ce1-172">Click **OK**.</span></span> 
    
4. <span data-ttu-id="01ce1-173">Adicione o namespace ProjectServerClient ao arquivo .cs.</span><span class="sxs-lookup"><span data-stu-id="01ce1-173">Add the PrjoctServer Client namespace to the .cs file.</span></span>
    
   ```cs
    using Microsoft.ProjectServer.Client;
   ```

<span data-ttu-id="01ce1-174">Adicione os assemblies de SDK do SharePoint 2013 usando o Console do Gerenciador de Pacotes NuGet.</span><span class="sxs-lookup"><span data-stu-id="01ce1-174">Add the SharePoint 2013 SDK assemblies using the NuGet Package Manager Console.</span></span> 
  
1. <span data-ttu-id="01ce1-175">No menu Ferramentas do VS, clique nos seguintes menus: **Ferramentas =\> Gerenciador de Pacotes NuGet =\> Console do Gerenciador de Pacotes**.</span><span class="sxs-lookup"><span data-stu-id="01ce1-175">From the VS Tools menu, click the following menus: **Tools =\> NuGet Package Manager =\> Package Manager Console**.</span></span> 
    
2. <span data-ttu-id="01ce1-176">No Console do Gerenciador de Pacotes, insira o comando a seguir e pressione \<Enter\>:</span><span class="sxs-lookup"><span data-stu-id="01ce1-176">In the Package Manager Console, enter the following command and press \<ENTER\>:</span></span>
    
   ```cs
    Install-Package Microsoft.SharePointOnline.CSOM
   ```

   <span data-ttu-id="01ce1-177">O **Console do Gerenciador de Pacotes** fornece uma descrição de resultados de comandos, e o Explorador de soluções do VS exibe assemblies do SharePoint nas referências do projeto.</span><span class="sxs-lookup"><span data-stu-id="01ce1-177">The **Package Manager Console** provides a description of the command results; and, the VS Solution Explorer displays the SharePoint assemblies in the project references.</span></span> 
    
3. <span data-ttu-id="01ce1-178">Adicione os namespaces ao arquivo .cs:</span><span class="sxs-lookup"><span data-stu-id="01ce1-178">Add the namespaces to the .cs file:</span></span>
    
   ```cs
    using Microsoft.SharePoint.Client;
   ```

<span data-ttu-id="01ce1-179">O assembly System.Security faz parte do .NET Framework e foi instalado com a estrutura.</span><span class="sxs-lookup"><span data-stu-id="01ce1-179">The System.Security assembly is part of .NET Framework and was installed with the framework.</span></span> <span data-ttu-id="01ce1-180">O aplicativo de exemplo precisa de mais um namespace que forneça uma cadeia de caracteres criptografada ao sistema de hospedagem para efetuar a autenticação.</span><span class="sxs-lookup"><span data-stu-id="01ce1-180">The sample application needs one more namespace that provides an encrypted string to the hosting system for authentication.</span></span> <span data-ttu-id="01ce1-181">Depois de autenticado, o aplicativo pode acessar projetos no sistema de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="01ce1-181">Once authenticated, the application can access projects on the hosting system.</span></span> <span data-ttu-id="01ce1-182">Adicione o namespace System.Security ao arquivo .cs desta maneira:</span><span class="sxs-lookup"><span data-stu-id="01ce1-182">Add the System.Security namespace to the .cs file in this way:</span></span>
  
1. <span data-ttu-id="01ce1-183">No Explorador de Soluções do VS, clique na entrada Referências e selecione **Adicionar Referência...**</span><span class="sxs-lookup"><span data-stu-id="01ce1-183">In the VS Solution Explorer, right-click the References entry, and select **Add Reference…**</span></span> <span data-ttu-id="01ce1-184">no menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="01ce1-184">from the shortcut menu.</span></span> 
    
2. <span data-ttu-id="01ce1-185">Selecione **Assemblies =\> Framework** no painel esquerdo da caixa de diálogo Gerenciador de Referências, depois marque **System.Security**.</span><span class="sxs-lookup"><span data-stu-id="01ce1-185">Select **Assemblies =\> Framework** in the left pane of the References Manager dialog, then check **System.Security**.</span></span> 
    
3. <span data-ttu-id="01ce1-186">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="01ce1-186">Click **OK**.</span></span> 
    
4. <span data-ttu-id="01ce1-187">Adicione o namespace System.Security ao arquivo .cs:</span><span class="sxs-lookup"><span data-stu-id="01ce1-187">Add the System.Security namespace to the .cs file:</span></span>
    
   ```cs
    using System.Security;
   ```

<span data-ttu-id="01ce1-188">O início do arquivo .cs deve conter os seguintes namespaces:</span><span class="sxs-lookup"><span data-stu-id="01ce1-188">The start of the .cs file should contain the following namespaces:</span></span>
  
- <span data-ttu-id="01ce1-189">System</span><span class="sxs-lookup"><span data-stu-id="01ce1-189">System</span></span>
    
- <span data-ttu-id="01ce1-190">System.Collections.Generic</span><span class="sxs-lookup"><span data-stu-id="01ce1-190">System.Collections.Generic</span></span>
    
- <span data-ttu-id="01ce1-191">System.Linq</span><span class="sxs-lookup"><span data-stu-id="01ce1-191">System.Linq</span></span>
    
- <span data-ttu-id="01ce1-192">System.Test</span><span class="sxs-lookup"><span data-stu-id="01ce1-192">System.Test</span></span>
    
- <span data-ttu-id="01ce1-193">Microsoft.ProjectServer.Client</span><span class="sxs-lookup"><span data-stu-id="01ce1-193">Microsoft.ProjectServer.Client</span></span>
    
- <span data-ttu-id="01ce1-194">Microsoft.SharePoint.Client</span><span class="sxs-lookup"><span data-stu-id="01ce1-194">Microsoft.SharePoint.Client</span></span>
    
- <span data-ttu-id="01ce1-195">System.Security</span><span class="sxs-lookup"><span data-stu-id="01ce1-195">System.Security</span></span>
    
### <a name="connect-to-the-host-system"></a><span data-ttu-id="01ce1-196">Conecte-se ao sistema de host</span><span class="sxs-lookup"><span data-stu-id="01ce1-196">Connect to the host system</span></span>

<span data-ttu-id="01ce1-197">O Project Online é um aplicativo do SharePoint, assim, usar a autenticação do SharePoint é a abordagem correta.</span><span class="sxs-lookup"><span data-stu-id="01ce1-197">Project Online is a SharePoint application, so using SharePoint authentication is the correct approach.</span></span> <span data-ttu-id="01ce1-198">O fragmento de código a seguir prepara para acessar o ambiente hospedado.</span><span class="sxs-lookup"><span data-stu-id="01ce1-198">The following code fragment prepares to access the hosted environment.</span></span>
  
```cs
    class Program
    {
        private static ProjectContext projContext;
        static void Main (string[] args)
        {
            using (ProjectContext projContext = new ProjectContext("https://Contoso.sharepoint.com/sites/pwa"))
            {
                SecureString password - new SecureString();
                foreach (char c in "password".ToCharArray()) password.AppendChar(c);
                //Using SharePoint method to load Credentials
                projContext.Credentials = new SharePointOnlineCredentials("sarad@Contoso.onmicrosoft.com", password);

```

<span data-ttu-id="01ce1-199">Entre os preparativos para acessar o ambiente hospedado estão os seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="01ce1-199">Preparations to access the hosted environment include the following items:</span></span>
  
1. <span data-ttu-id="01ce1-200">Criar um objeto de contexto para projetos – ele está contido no código a seguir ao fragmento de código anterior.</span><span class="sxs-lookup"><span data-stu-id="01ce1-200">Create a context object for the projects -- this is contained in the following code of the preceding code fragment.</span></span> 
    
   ```cs
    private static ProjectContext projContext;
    
   ```

   <span data-ttu-id="01ce1-201">O contexto é herdado pelos outros componentes, permitindo que o sistema gerencie o contexto do modelo de objeto do Project.</span><span class="sxs-lookup"><span data-stu-id="01ce1-201">The context is inherited by other components, allowing the system to manage the context of the Project object model.</span></span>
    
2. <span data-ttu-id="01ce1-202">Identificar o site do host – isso é feito no código a seguir ao fragmento de código anterior.</span><span class="sxs-lookup"><span data-stu-id="01ce1-202">Identify the host site -- this is done in the following code from the preceding code fragment.</span></span>
    
   ```cs
    using (ProjectContext projContext = new ProjectContext("https://Contoso.sharepoint.com/sites/pwa"))
   ```

   <span data-ttu-id="01ce1-203">Ao instanciar o contexto dos projetos, o aplicativo deve fornecer a raiz do conjunto de sites dos Projects.</span><span class="sxs-lookup"><span data-stu-id="01ce1-203">When instantiating the projects context, the application needs to provide the root of the Projects site collection.</span></span> <span data-ttu-id="01ce1-204">O aplicativo usa uma subcadeia de caracteres da URL da raiz dos Projects.</span><span class="sxs-lookup"><span data-stu-id="01ce1-204">The application uses a substring of the URL of the root of the Projects.</span></span> <span data-ttu-id="01ce1-205">Um instantâneo desse local é realçado com um retângulo vermelho na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="01ce1-205">A snapshot of this location is highlighted with a red rectangle in the following illustration.</span></span> <span data-ttu-id="01ce1-206">A autenticação precisa da cadeia de caracteres desde o início pela subcadeia de caracteres "pwa".</span><span class="sxs-lookup"><span data-stu-id="01ce1-206">The authentication needs the string from its start through the substring "pwa".</span></span> <span data-ttu-id="01ce1-207">Na lista de códigos, o aplicativo usa a cadeia "https://XXXXXXXX.sharepoint.com/sites/pwa".</span><span class="sxs-lookup"><span data-stu-id="01ce1-207">In the code listing, the application uses the string "https://XXXXXXXX.sharepoint.com/sites/pwa".</span></span>
        
   <span data-ttu-id="01ce1-208">![Captura de tela da URL do conjunto de sites dos Projects dentro de uma borda vermelha. ] (media/d48c4894-5dba-46b6-886a-3c59bfb83c4d.png "Captura de tela da URL do conjunto de sites dos Projects dentro de uma borda vermelha")</span><span class="sxs-lookup"><span data-stu-id="01ce1-208">![Screen shot of the URL of the Projects site collection within a red border.](media/d48c4894-5dba-46b6-886a-3c59bfb83c4d.png "Screen shot of the URL of the Projects site collection within a red border")</span></span>
  
3. <span data-ttu-id="01ce1-209">Definir a senha em uma cadeia de caracteres segura – isso é feito no código a seguir ao fragmento de código anterior.</span><span class="sxs-lookup"><span data-stu-id="01ce1-209">Place the password in a secure string -- this is done in the following code from the preceding code fragment.</span></span>
    
   ```cs
    SecureString password - new SecureString();
    foreach (char c in "password".ToCharArray()) password.AppendChar(c);
    
   ```

   <span data-ttu-id="01ce1-210">A conta de usuário e a senha são as credenciais para acessar o site do host.</span><span class="sxs-lookup"><span data-stu-id="01ce1-210">The password and user account are the credentials to access the host site.</span></span> 
    
4. <span data-ttu-id="01ce1-211">Adicionar a conta de usuário e senha na parte de credenciais do objeto de contexto – isso é feito no código a seguir ao fragmento de código anterior.</span><span class="sxs-lookup"><span data-stu-id="01ce1-211">Add the user account and password to the credentials portion of the context object -- this is done in the following code from the preceding code fragment.</span></span>
    
   ```cs
    projContext.Credentials = new SharePointOnlineCredentials("sarad@Contoso.onmicrosoft.com", password);
   ```

<span data-ttu-id="01ce1-212">O contexto de instâncias do projeto está pronto para uso.</span><span class="sxs-lookup"><span data-stu-id="01ce1-212">The instantiated project context is ready to use.</span></span>
  
### <a name="list-all-published-projects"></a><span data-ttu-id="01ce1-213">Listar todos os projetos publicados</span><span class="sxs-lookup"><span data-stu-id="01ce1-213">List all published projects</span></span>

<span data-ttu-id="01ce1-214">O Project Online e o Project Server usam proxies para se comunicar com o servidor para criar, relatar, atualizar e excluir operações (CRUD).</span><span class="sxs-lookup"><span data-stu-id="01ce1-214">Project Online and ProjectServer use proxies to communicate with the server for create, report, update, and delete (CRUD) operations.</span></span> <span data-ttu-id="01ce1-215">O host/servidor manipula as solicitações de maneira eficiente e faz o cliente executar as seguintes ações ao se comunicar com o servidor:</span><span class="sxs-lookup"><span data-stu-id="01ce1-215">The host/server handles requests in an efficient manner and has the client perform the following actions in communicating with the server:</span></span>
  
1. <span data-ttu-id="01ce1-216">Estabelecer um contexto de comunicação.</span><span class="sxs-lookup"><span data-stu-id="01ce1-216">Establish a context for communication.</span></span> 
    
   <span data-ttu-id="01ce1-217">O contexto é usado por conjunto de projetos, bem como outros objetos e coleções por herança, incluindo o conjunto de tarefas, conjunto de atribuições, o objeto estágio e os campos personalizados.</span><span class="sxs-lookup"><span data-stu-id="01ce1-217">The context is used by the projects collection, as well as other objects and collections through inheritance, including the tasks collection, assignments collection, the stage object, and custom fields.</span></span> 
    
2. <span data-ttu-id="01ce1-218">Use o modelo de objeto para especificar um objeto, conjunto ou dados a recuperar.</span><span class="sxs-lookup"><span data-stu-id="01ce1-218">Use the object model to specify an object, collection, or data to retrieve.</span></span>
    
   <span data-ttu-id="01ce1-219">Esta etapa usa LINQ como uma consulta ou método.</span><span class="sxs-lookup"><span data-stu-id="01ce1-219">This step uses LINQ as a query or as a method.</span></span> <span data-ttu-id="01ce1-220">A especificação controla o que você recebe.</span><span class="sxs-lookup"><span data-stu-id="01ce1-220">The specification controls what you receive.</span></span> <span data-ttu-id="01ce1-221">Geralmente essa etapa é inserida no corpo do método de Carregamento (etapa 3).</span><span class="sxs-lookup"><span data-stu-id="01ce1-221">Often, this step is embedded as the body of the Load method (step 3).</span></span> 
    
3. <span data-ttu-id="01ce1-222">Carregue a especificação de recuperação da etapa anterior usando os métodos Load() ou LoadQuery().</span><span class="sxs-lookup"><span data-stu-id="01ce1-222">Load the retrieval specification from the previous step using the Load() or LoadQuery() method.</span></span>
    
   <span data-ttu-id="01ce1-223">Para o carregamento de conjuntos e objetos, use Load().</span><span class="sxs-lookup"><span data-stu-id="01ce1-223">For loading collections and objects, use Load().</span></span> <span data-ttu-id="01ce1-224">Para consultas com cláusulas como "where" e "group", use LoadQuery().</span><span class="sxs-lookup"><span data-stu-id="01ce1-224">For queries with clauses such as "where" and "group", use LoadQuery().</span></span> 
    
4. <span data-ttu-id="01ce1-225">Execute a solicitação usando o método de ExecuteQuery().</span><span class="sxs-lookup"><span data-stu-id="01ce1-225">Execute the request using the ExecuteQuery() method.</span></span>
    
   <span data-ttu-id="01ce1-226">O método ExecuteQuery() notifica o host de que a consulta ou consultas estão prontas para executar.</span><span class="sxs-lookup"><span data-stu-id="01ce1-226">The ExecuteQuery() method notifies the host that the query or queries are ready to execute.</span></span> <span data-ttu-id="01ce1-227">Quando o host recebe a notificações, executa as consultas e envia os resultados ao cliente.</span><span class="sxs-lookup"><span data-stu-id="01ce1-227">Once the host receives notification, it executes the queries and sends the results to the client.</span></span> 
    
<span data-ttu-id="01ce1-228">Com as informações no cliente, o aplicativo pode usá-la.</span><span class="sxs-lookup"><span data-stu-id="01ce1-228">With the information at the client, the application can use it.</span></span> <span data-ttu-id="01ce1-229">O fragmento de código a seguir percorre projetos publicados e marca o Id e o Nome de cada projeto publicado no host.</span><span class="sxs-lookup"><span data-stu-id="01ce1-229">The following code fragment cycles through the published projects and prints the Id and Name for each published project on the host.</span></span>
  
```cs
// Get the list of projects in Project Web App.
var projects = projContext.Projects;
projContext.Load(projects);
projcontext.ExecuteQuery();
foreach (PublishedProject pubProj in projContext.Projects)
{
    Console.WriteLine("\n{0}. {1}   {2} \t{3} \n", j++, pubProj.Id, pubProj.Name, pubProj.CreatedDate);
}

```

<span data-ttu-id="01ce1-230">Saída:</span><span class="sxs-lookup"><span data-stu-id="01ce1-230">Output</span></span>
  
```cs
Published Project count:2
1. be80a848-b2ef-e511-80f4-00155dc84e01   A second Project     3/21/2016 10:14:40 PM
2. 9d730a1a-60ed-e511-80f6-00155dc87d01   Ent_Proj_1   3/18/2016 11:21:14 PM

```

### <a name="make-a-request"></a><span data-ttu-id="01ce1-231">fazer uma solicitação</span><span class="sxs-lookup"><span data-stu-id="01ce1-231">Make a second GET request.</span></span>

<span data-ttu-id="01ce1-232">Usando as ações do fragmento de código anterior, o aplicativo recupera a lista de projetos na conta especificada do site de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="01ce1-232">Using the actions from the previous code fragment, the application retrieves the list of projects in the specified account on the hosting site.</span></span> 
  
1. <span data-ttu-id="01ce1-233">ProjectContext está especificado nos projetos a listar.</span><span class="sxs-lookup"><span data-stu-id="01ce1-233">The ProjectContext is specified for the projects to list.</span></span> 
    
   ```cs
    var projects = projContext.Projects;
   ```

2. <span data-ttu-id="01ce1-234">Especifique o item a recuperar.</span><span class="sxs-lookup"><span data-stu-id="01ce1-234">Specify the item to retrieve.</span></span> 
    
   ```cs
    projContext.Load(projects);
   ```

   <span data-ttu-id="01ce1-235">Ao simplesmente informar o conjunto, o servidor recupera o conjunto de projetos, preenchendo cada projeto com valores do conjunto padrão de propriedades.</span><span class="sxs-lookup"><span data-stu-id="01ce1-235">By only stating the collection, the server retrieves the project collection, populating each project with values for the default set of properties.</span></span> <span data-ttu-id="01ce1-236">Acessar as propriedades que fazem parte do conjunto de propriedades padrão fornece resultados bem-sucedidos.</span><span class="sxs-lookup"><span data-stu-id="01ce1-236">Accessing properties that are part of the default property set gives successful results.</span></span> <span data-ttu-id="01ce1-237">Acessar as propriedades que não fazem parte do conjunto padrão resulta na exceção "Não inicializado".</span><span class="sxs-lookup"><span data-stu-id="01ce1-237">Accessing properties that are not part of the default set results in a "Not initialized" exception.</span></span>
    
3. <span data-ttu-id="01ce1-238">Carregue a solicitação (projContext.Load).</span><span class="sxs-lookup"><span data-stu-id="01ce1-238">Load the request (projContext.Load).</span></span>
    
   <span data-ttu-id="01ce1-239">Isso faz parte da etapa anterior.</span><span class="sxs-lookup"><span data-stu-id="01ce1-239">This is part of the previous step.</span></span>
    
4. <span data-ttu-id="01ce1-240">Execute a consulta (ExecuteQuery).</span><span class="sxs-lookup"><span data-stu-id="01ce1-240">Execute the SQL query.</span></span> 
    
   ```cs
    projContext.ExecuteQuery();
   ```

### <a name="retrieve-high-level-project-information"></a><span data-ttu-id="01ce1-241">Recuperar informações de projeto de alto nível</span><span class="sxs-lookup"><span data-stu-id="01ce1-241">Retrieve high-level project information</span></span>

<span data-ttu-id="01ce1-242">Propriedades que não sejam propriedades padrão devem ser especificadas na solicitação para o servidor.</span><span class="sxs-lookup"><span data-stu-id="01ce1-242">Properties that are not default properties must be specified in the request to the server.</span></span> <span data-ttu-id="01ce1-243">O próximo fragmento de código carrega o contexto do conjunto de projetos, como no exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="01ce1-243">The next code fragment loads the projects collection context as in the previous example.</span></span> <span data-ttu-id="01ce1-244">Em seguida, a especificação solicita propriedades adicionais não padrão a incluir no resultado.</span><span class="sxs-lookup"><span data-stu-id="01ce1-244">Then, the specification requests additional non-default properties to include in the result.</span></span> 
  
```cs
var projects = projContext.Projects;
projContext.Load(projects,
    ps => ps.IncludeWithDefaultProperties(
        p => p.StartDate, p => p.Phase, p => p.Stage));
projContext.ExecuteQuery();

```

<span data-ttu-id="01ce1-245">A instrução de carregamento especifica o contexto de conjuntos de projetos e adiciona DataDeInício, Estágio e Fase ao resultado da consulta.</span><span class="sxs-lookup"><span data-stu-id="01ce1-245">The load statement specifies the projects collection context, and adds the StartDate, Phase, and Stage to the query result.</span></span> <span data-ttu-id="01ce1-246">As propriedades adicionais podem ser escalares, objetos ou conjuntos.</span><span class="sxs-lookup"><span data-stu-id="01ce1-246">The additional properties can be scalar, objects, or collections.</span></span> <span data-ttu-id="01ce1-247">Itens escalares podem ser acessados diretamente.</span><span class="sxs-lookup"><span data-stu-id="01ce1-247">Scalar items can be accessed directly.</span></span> <span data-ttu-id="01ce1-248">Objetos e conjuntos exigem processamento adicional, como no próximo fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="01ce1-248">Objects and collections require additional processing, as in the following code fragment.</span></span>
  
```cs
// Using the previous definition and Load statement …
projContext.ExecuteQuery();
foreach (PublishedProject pubProj in projContext.Projects)
{
Console.WriteLine("\n\t{0}. \t{1} \n\t{2} \n\t{3} \n", j++, pubProj.Id, pubProj.Name,
    pubProj.CreatedDate);
             // The following statement generates an exception about the object 
             // reference not being set to an instance on the server. 
             // Console.WriteLine("\tCurrent Phase:\t{0}", pubProj.Phase.Name);
             // Phase and Stage are not published with the rest of the data. Need to pull these objects from the server.
             Phase oPhase = pubProj.Phase;
             projContext.Load(oPhase);
             projContext.ExecuteQuery();
             //if-else fails because the else case fails with "Microsoft.SharePoint.Client.ServerObjectNullReferenceException".
             //if (oPhase.ServerObjectIsNull != null)
             //Using try-catch instead
             try
             {
                  Console.WriteLine("\tCurrent Phase:\t{0}", oPhase.Name);
             }
             
             catch
             {
                  Console.WriteLine("\tCurrent Phase:\t Not available");
             }
             
             Stage oStage = pubProj.Stage;
             projContext.Load(oStage);
             projContext.ExecuteQuery();
             //Again, not using if-else combination for the same reason as above.
             try
             {
                  Console.WriteLine("\tCurrent Stage:\t{0}", oStage.Name);
             }
             
             catch
             {
                  Console.WriteLine("\tCurrent Stage:\t Not available");
    }

```

<span data-ttu-id="01ce1-249">Saída dos três primeiros projetos:</span><span class="sxs-lookup"><span data-stu-id="01ce1-249">Output of the first three projects:</span></span>
  
```cs
Project counts:31
1. Project ID:  957d5fcd-5cbf-e111-9f1e-00155d022681
        Name:           Acquisition Target Analysis
        CreatedDate:            3/22/2016 5:14:34 PM
        Current Phase:  3. Plan
        Current Stage:  6. Plan
2. Project ID:  16905202-5fbf-e111-9f1e-00155d022681
        Name:           Apparel ERP Upgrade
        CreatedDate:            3/22/2016 5:36:40 PM
        Current Phase:  3. Plan
        Current Stage:  6. Plan
3. Project ID:  dce23152-63bf-e111-9f1e-00155d022681
        Name:           Audit Tracking Solution
        CreatedDate:            3/22/2016 5:02:24 PM
        Current Phase:  2. Select
        Current Stage:  4. Select Gate

```

### <a name="retrieve-all-tasks-in-a-project"></a><span data-ttu-id="01ce1-250">recuperar todas as tarefas em um projeto</span><span class="sxs-lookup"><span data-stu-id="01ce1-250">Retrieve all tasks in a project</span></span>

<span data-ttu-id="01ce1-251">Cada projeto tem diversas tarefas.</span><span class="sxs-lookup"><span data-stu-id="01ce1-251">Each project has many tasks.</span></span> <span data-ttu-id="01ce1-252">Portanto, extrair as tarefas de um projeto único consiste em:</span><span class="sxs-lookup"><span data-stu-id="01ce1-252">So, pulling the tasks for a single project consists of the following:</span></span>
  
1. <span data-ttu-id="01ce1-253">estabelecer o contexto do conjunto de projetos.</span><span class="sxs-lookup"><span data-stu-id="01ce1-253">Establish the context of the projects collection.</span></span>
    
   ```cs
    var projects = projContext.Projects;
   ```

2. <span data-ttu-id="01ce1-254">Recupere informações de projeto, incluindo as propriedades da Tarefa.</span><span class="sxs-lookup"><span data-stu-id="01ce1-254">Retrieve the project information, including the Task properties.</span></span>
    
   ```cs
    projContext.Load(projects);
    ProjContext.ExecuteQuery();
    foreach (PublishedProject pubProj in projContext.Projects){
    
   ```

    <span data-ttu-id="01ce1-255">Observe que o aplicativo está voltado a projetos publicados.</span><span class="sxs-lookup"><span data-stu-id="01ce1-255">Note that the application is addressing published projects.</span></span> <span data-ttu-id="01ce1-256">O contexto do projeto atual publicado é pubProj.</span><span class="sxs-lookup"><span data-stu-id="01ce1-256">The context for the current published project is pubProj.</span></span> 
    
3. <span data-ttu-id="01ce1-257">Estabeleça contexto para o conjunto de tarefas.</span><span class="sxs-lookup"><span data-stu-id="01ce1-257">Establish the context for the Tasks collection.</span></span>
    
   ```cs
    PublishedTaskCollection collTask = pubProj.Tasks;
   ```

   <span data-ttu-id="01ce1-258">A propriedade `pubProj.Tasks` referencia as tarefas do projeto publicado atual.</span><span class="sxs-lookup"><span data-stu-id="01ce1-258">The `pubProj.Tasks` property references the tasks of the current published project.</span></span> 
    
4. <span data-ttu-id="01ce1-259">Carregue a especificação para recuperar o conjunto de Tarefas, incluindo as propriedades não padrão apropriadas.</span><span class="sxs-lookup"><span data-stu-id="01ce1-259">Load the specification to retrieve Task collection, including the appropriate non-default properties.</span></span>
    
   ```cs
    projContext.Load(collTask,
        tsk => tsk.IncludeWithDefaultProperties(
            t => t.Id, t => t.Name, t => t.Start,
            t => t.ScheduledStart, t => t.Completion));
    
   ```

5. <span data-ttu-id="01ce1-260">Execute a consulta para recuperar o conjunto de tarefas com as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="01ce1-260">Execute the query to retrieve the Task collection with the appropriate properties.</span></span>
    
   ```cs
    projContext.ExecuteQuery();
   ```

<span data-ttu-id="01ce1-261">As informações agora são locais.</span><span class="sxs-lookup"><span data-stu-id="01ce1-261">The information is now local.</span></span> <span data-ttu-id="01ce1-262">O fragmento de código a seguir processa o conjunto de tarefas publicadas gravando as informações no console.</span><span class="sxs-lookup"><span data-stu-id="01ce1-262">The following code fragment processes the published tasks collection by writing the information to the console.</span></span>
  
```cs
    Console.WriteLine("Task collection count: {0}", collTask.Count.ToString());
    if (collTask.Count > 0)
    {
        int k = 1;    //Task counter.
        foreach (PublishedTask t in collTask)
        {
            Console.WriteLine("{0}. Id:{1} \tName:{2}", k++, t.Id, t.Name);
            Console.WriteLine("\t ScheduledStart:{0} \tStart:{1} \tCompletion:{2}", k, t.ScheduledStart, t.Start, t.Completion);
        }
    }

```

<span data-ttu-id="01ce1-263">Saída de tarefas para um projeto:</span><span class="sxs-lookup"><span data-stu-id="01ce1-263">Output of tasks for one project:</span></span>
  
```cs
Task collection count: 5
1. Id:256fa850-b2ef-e511-80f6-00155dc87d01      Name:Load software onto computer
         ScheduledStart:2       Start:4/4/2016 8:00:00 AM       Completion:4/4/2016 8:00:00 AM
2. Id:266fa850-b2ef-e511-80f6-00155dc87d01      Name:Locate and load Project Online SDK
         ScheduledStart:3       Start:4/5/2016 8:00:00 AM       Completion:4/5/2016 8:00:00 AM
3. Id:276fa850-b2ef-e511-80f6-00155dc87d01      Name:Locate and load SP SDK
         ScheduledStart:4       Start:4/5/2016 1:00:00 PM       Completion:4/5/2016 1:00:00 PM
4. Id:286fa850-b2ef-e511-80f6-00155dc87d01      Name:Build app that accesses Proj Online
         ScheduledStart:5       Start:4/6/2016 8:00:00 AM       Completion:4/6/2016 8:00:00 AM
5. Id:296fa850-b2ef-e511-80f6-00155dc87d01      Name:Build app that accesses task assignments
         ScheduledStart:6       Start:4/7/2016 8:00:00 AM       Completion:4/7/2016 8:00:00 AM

```

### <a name="access-information-at-multiple-levels"></a><span data-ttu-id="01ce1-264">acesse as informações em vários níveis</span><span class="sxs-lookup"><span data-stu-id="01ce1-264">Access information at multiple levels</span></span>

<span data-ttu-id="01ce1-265">Cada tarefa pode ter uma ou mais pessoas (ou seja,</span><span class="sxs-lookup"><span data-stu-id="01ce1-265">Each task can have one or more persons (a.k.a.</span></span> <span data-ttu-id="01ce1-266">recursos) contribuindo até sua conclusão.</span><span class="sxs-lookup"><span data-stu-id="01ce1-266">resource) contributing toward its completion.</span></span> <span data-ttu-id="01ce1-267">Os conjuntos de Tarefas e Recursos contêm essas informações para cada tarefa.</span><span class="sxs-lookup"><span data-stu-id="01ce1-267">The Assignments and Resources collections contain this information for each task.</span></span> 
  
<span data-ttu-id="01ce1-268">O processamento consiste em:</span><span class="sxs-lookup"><span data-stu-id="01ce1-268">The crawl and content processing architecture consists of the following:</span></span>
  
1. <span data-ttu-id="01ce1-269">obter um contexto para a tarefa do projeto.</span><span class="sxs-lookup"><span data-stu-id="01ce1-269">Obtaining a context for the project task.</span></span>
    
2. <span data-ttu-id="01ce1-270">Criar e carregar uma solicitação para as tarefas vinculadas à tarefa.</span><span class="sxs-lookup"><span data-stu-id="01ce1-270">Build a request and load the request for the assignments tied to the task.</span></span> 
    
3. <span data-ttu-id="01ce1-271">Executar a consulta para as tarefas.</span><span class="sxs-lookup"><span data-stu-id="01ce1-271">Execute the query for the assignments.</span></span>
    
4. <span data-ttu-id="01ce1-272">Criar e carregar a solicitação do recurso associado a uma tarefa individual.</span><span class="sxs-lookup"><span data-stu-id="01ce1-272">Build a request and load the request for the resource associated with an individual assignment.</span></span> 
    
5. <span data-ttu-id="01ce1-273">Executar a consulta para o recurso.</span><span class="sxs-lookup"><span data-stu-id="01ce1-273">Execute the query for the resource.</span></span>
    
> [!NOTE] 
> - <span data-ttu-id="01ce1-274">O conjunto de Atribuições é solicitado explicitamente nas informações do servidor porque não é uma propriedade padrão do conjunto de Tarefas.</span><span class="sxs-lookup"><span data-stu-id="01ce1-274">The Assignments collection is explicitly requested in the information from the server because it is not a default property of the Tasks collection.</span></span> <span data-ttu-id="01ce1-275">Como um conjunto, é feita uma consulta subsequente para obter o conjunto do servidor.</span><span class="sxs-lookup"><span data-stu-id="01ce1-275">As a collection, a subsequent query is made to pull the collection from the server.</span></span> 
> - <span data-ttu-id="01ce1-276">O Recurso é um objeto.</span><span class="sxs-lookup"><span data-stu-id="01ce1-276">The Resource is an object.</span></span> <span data-ttu-id="01ce1-277">A consulta de uma atribuição inclui o nome do recurso associado à tarefa.</span><span class="sxs-lookup"><span data-stu-id="01ce1-277">The query for an assignment includes the resource name associated with the assignment.</span></span>
    
```cs
PublishedTaskCollection collTask = pubProj.Tasks;
    projContext.Load(collTask,
        tsk => tsk.IncludeWithDefaultProperties(
            t => t.Id, t => t.Name, 
            t => t.Assignments));
    projContext.Load(collTask);
    projContext.ExecuteQuery();
    Console.WriteLine("Task collection count: {0}", collTask.Count.ToString());
    if (collTask.Count > 0)
    {
        int k = 1;    //Task counter.
        //Processing task list for current project
        foreach (PublishedTask t in collTask)
        {
            Console.WriteLine("{0}. Id:{1} \tName:{2}", k, t.Id, t.Name);
            k++;
            //Define and retrieve Assignments for current task
            PublishedAssignmentCollection collAssgns = t.Assignments;
            projContext.Load(collAssgns);
            projContext.ExecuteQuery();
            Console.WriteLine("    Assignment collection count: {0}", collAssgns.Count);
            if (collAssgns.Count > 0)
            {
                //Output string for resources assigned to task
                StringBuilder output = new StringBuilder();
                output.AppendFormat("\t Assignments: ");
                foreach (PublishedAssignment a in collAssgns)
                {
                    //Define and retrieve resource name for current assignment 
                    //(an object)
                    projContext.Load(a,
                        b => b.Resource.Name);
                    projContext.ExecuteQuery();
                    output.AppendFormat("{0}, ", a.Resource.Name);
                }
                Console.WriteLine(output);
            }
            else
            {
                Console.WriteLine("\t Assignments: None");
            }
        }
    }   // endif

```

<span data-ttu-id="01ce1-278">Saída das tarefas 52, 75 e 76 de um projeto:</span><span class="sxs-lookup"><span data-stu-id="01ce1-278">Output for tasks 52, 75, and 76 of a project:</span></span>
  
```cs
52. Id:2c729e96-54f0-e511-80c6-000d3a33235f     Name:Develop training materials
    Assignment collection count: 1
         Assignments: Robert Lyon,
75. Id:43729e96-54f0-e511-80c6-000d3a33235f     Name:Determine final deployment strategy
    Assignment collection count: 0
         Assignments: None
76. Id:44729e96-54f0-e511-80c6-000d3a33235f     Name:Develop deployment methodology
    Assignment collection count: 4
         Assignments: Molly Dempsey, Sara Davis, Shammi Mohamed, Zainal Arifin, 

```

### <a name="access-custom-enterprise-level-fields"></a><span data-ttu-id="01ce1-279">acessar campos personalizados de nível empresarial</span><span class="sxs-lookup"><span data-stu-id="01ce1-279">Access custom enterprise-level fields</span></span>

<span data-ttu-id="01ce1-280">Existem campos personalizados no Project Online.</span><span class="sxs-lookup"><span data-stu-id="01ce1-280">Custom fields exist for Project Online.</span></span> <span data-ttu-id="01ce1-281">São os campos de nível empresarial que podem ser associados ao projeto individual.</span><span class="sxs-lookup"><span data-stu-id="01ce1-281">These are enterprise-level fields that can be associated with individual project.</span></span> <span data-ttu-id="01ce1-282">Esta seção descreve como acessar esses campos.</span><span class="sxs-lookup"><span data-stu-id="01ce1-282">This section describes how to access these fields.</span></span> 
  
<span data-ttu-id="01ce1-283">Campos personalizados não estão incluídos no conjunto padrão de propriedades associadas a um projeto.</span><span class="sxs-lookup"><span data-stu-id="01ce1-283">Custom fields are not included in the default set of properties associated with a project.</span></span> <span data-ttu-id="01ce1-284">Portanto, eles precisam de identificação explícita na especificação da recuperação.</span><span class="sxs-lookup"><span data-stu-id="01ce1-284">So, they need explicit identification in the retrieval specification.</span></span> <span data-ttu-id="01ce1-285">A visão de alto nível do processo consiste nos seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="01ce1-285">The high-level view of the process consists of the following items:</span></span>
  
1. <span data-ttu-id="01ce1-286">direcionar para o campo personalizado usando seu nome comum.</span><span class="sxs-lookup"><span data-stu-id="01ce1-286">Tunnel to the custom field using its common name.</span></span>
    
2. <span data-ttu-id="01ce1-287">Recuperar o nome do campo personalizado interno.</span><span class="sxs-lookup"><span data-stu-id="01ce1-287">Retrieve the internal name of the custom field.</span></span>
    
3. <span data-ttu-id="01ce1-288">Retornar ao contexto global e consultar o sistema usando o nome interno do campo personalizado.</span><span class="sxs-lookup"><span data-stu-id="01ce1-288">Return to the global context and query the system using the internal name of the custom field.</span></span>
    
#### <a name="tunnel-to-the-custom-field-retrieve-its-internal-name-and-used-it-to-query-the-system"></a><span data-ttu-id="01ce1-289">Direcionar para o campo personalizado, recuperar o nome interno e usá-lo para consultar o sistema</span><span class="sxs-lookup"><span data-stu-id="01ce1-289">Tunnel to the custom field, retrieve its internal name, and used it to query the system</span></span>

<span data-ttu-id="01ce1-290">Essa tarefa especifica uma recuperação que usa uma propriedade não padrão com um detalhe adicional.</span><span class="sxs-lookup"><span data-stu-id="01ce1-290">This task specifies a retrieval that uses a non-default property with one added detail.</span></span>
  
1. <span data-ttu-id="01ce1-291">Inicie usando o contexto de projetos, como descrito no início deste artigo.</span><span class="sxs-lookup"><span data-stu-id="01ce1-291">Begin by using the projects context, as described at the beginning of this article.</span></span>
    
   ```cs
    // Get the list of published projects in Project Web App.
    var projects = projContext.Projects;
    
   ```

2. <span data-ttu-id="01ce1-292">Adicione dois itens na solicitação de recuperação de conjunto de projetos além de quaisquer outras propriedades não padrão a recuperar:</span><span class="sxs-lookup"><span data-stu-id="01ce1-292">Add two items to the projects collection retrieval request in addition to any other non-default properties to retrieve:</span></span>
    
   ```cs
    projContext.Load(projects,
        ps => ps.IncludeWithDefaultProperties(
            p => p.Phase, p => p.Stage,                  // Other nondefault properties
            p => p.IncludeCustomFields,                  // Gets PublishedProject object 
                                                        // that contains custom fields
            p => p.IncludeCustomFields.CustomFields));   // Populates the custom fields
                    projContext.ExecuteQuery();
    
   ```

   <span data-ttu-id="01ce1-293">A cláusula `p => p.IncludeCustomFields` identifica a necessidade de usar um objeto do projeto que ofereça suporte a campos personalizados.</span><span class="sxs-lookup"><span data-stu-id="01ce1-293">The  `p => p.IncludeCustomFields` clause identifies the need to use a project object that supports custom fields.</span></span> 
    
   <span data-ttu-id="01ce1-294">A cláusula `p => p.IncludeCustomFields.CustomFields` solicita a inclusão de dados do campo personalizado no resultado da consulta.</span><span class="sxs-lookup"><span data-stu-id="01ce1-294">The  `p => p.IncludeCustomFields.CustomFields` clause requests the inclusion of custom field data in the query result.</span></span> <span data-ttu-id="01ce1-295">Essas informações são usadas depois que o nome do campo personalizado interno é recuperado.</span><span class="sxs-lookup"><span data-stu-id="01ce1-295">This information is used after the custom field internal name is retrieved.</span></span> 
    
3. <span data-ttu-id="01ce1-296">Carregue a solicitação.</span><span class="sxs-lookup"><span data-stu-id="01ce1-296">Load the request.</span></span>
    
   <span data-ttu-id="01ce1-297">Isso faz parte da etapa anterior.</span><span class="sxs-lookup"><span data-stu-id="01ce1-297">This is part of the previous step.</span></span>
    
4. <span data-ttu-id="01ce1-298">Execute a consulta.</span><span class="sxs-lookup"><span data-stu-id="01ce1-298">Execute the Query.</span></span>
    
   ```cs
    projContext.ExecuteQuery()
   ```

5. <span data-ttu-id="01ce1-299">Com essas informações no cliente, crie uma solicitação para recuperar campos personalizados associados ao projeto atual.</span><span class="sxs-lookup"><span data-stu-id="01ce1-299">With this information on the client, build a request to retrieve the custom fields associated with the current project.</span></span>
    
   ```cs
    foreach (PublishedProject pubProj in projContext.Projects)
    {
        //Console.WriteLine("\n\t{0}. \t{1} \n\t\t{2} \n\t\t{3} \n", 
                j++, pubProj.Id, pubProj.Name, pubProj.CreatedDate);
        CustomFieldCollection collCustF = pubProj.CustomFields;
                        
        projContext.Load(collCustF);
        projContext.ExecuteQuery();
    
   ```

6. <span data-ttu-id="01ce1-300">Localize o campo personalizado apropriado e recupere o nome do campo interno.</span><span class="sxs-lookup"><span data-stu-id="01ce1-300">Locate the appropriate custom field and retrieve the internal name of the field.</span></span> 
    
   ```cs
        foreach (CustomField oCF in collCustF)
        {
            if (oCF.Name == "Project Health")
            {
                Console.WriteLine("Name: {0}", oCF.Name);
                Console.WriteLine("InternalName: {0}", oCF.InternalName);
    
   ```

   <span data-ttu-id="01ce1-301">O nome interno do campo personalizado é recuperado.</span><span class="sxs-lookup"><span data-stu-id="01ce1-301">The internal name of the custom field is retrieved.</span></span> <span data-ttu-id="01ce1-302">Agora os itens de alto nível 1 e 2 estão concluídos.</span><span class="sxs-lookup"><span data-stu-id="01ce1-302">High-level items 1 and 2 are now complete.</span></span>
    
7. <span data-ttu-id="01ce1-303">Retorne ao contexto do projeto e recupere o valor do campo personalizado.</span><span class="sxs-lookup"><span data-stu-id="01ce1-303">Return to the project context and retrieve the value of the custom field.</span></span>
    
   ```cs
    Console.WriteLine("Value: {0}", 
        pubProj.IncludeCustomFields.FieldValues[oCF.InternalName]);
    
   ```

   > [!NOTE]
   > <span data-ttu-id="01ce1-304">O valor de campo personalizado é recuperado usando o nome interno como índice.</span><span class="sxs-lookup"><span data-stu-id="01ce1-304">The value of the custom field is retrieved using the internal name as an index.</span></span> 
  
<span data-ttu-id="01ce1-305">A saída de três projetos que consistem em ID do projeto, Nome do projeto, nome do campo personalizado, nome interno do campo personalizado e valor do campo personalizado.</span><span class="sxs-lookup"><span data-stu-id="01ce1-305">Output of three projects consisting of project ID, project Name, custom field name, custom field internal name, and custom field value.</span></span>
  
```cs
Project counts:31
1. Project ID:  957d5fcd-5cbf-e111-9f1e-00155d022681
        Name:           Acquisition Target Analysis
Name: Project Health
InternalName: Custom_745de6dfcfb4e11195dc00155d02c97f
Value: Green
2. Project ID:  16905202-5fbf-e111-9f1e-00155d022681
        Name:           Apparel ERP Upgrade
Name: Project Health
InternalName: Custom_745de6dfcfb4e11195dc00155d02c97f
Value: Green
3. Project ID:  dce23152-63bf-e111-9f1e-00155d022681
        Name:           Audit Tracking Solution
Name: Project Health
InternalName: Custom_745de6dfcfb4e11195dc00155d02c97f
Value: Red

```

## <a name="see-also"></a><span data-ttu-id="01ce1-306">Confira também</span><span class="sxs-lookup"><span data-stu-id="01ce1-306">See also</span></span>

<span data-ttu-id="01ce1-307">Confira a documentação e exemplos relacionados ao desenvolvimento de aplicativos usando o CSOM e Project Online no [Portal de Desenvolvimento do Project](https://developer.microsoft.com/pt-BR/project).</span><span class="sxs-lookup"><span data-stu-id="01ce1-307">For documentation and samples related to Project Online and application development using CSOM, see the [Project Development Portal](https://developer.microsoft.com/pt-BR/project).</span></span>
    

