---
title: Desenvolvendo um aplicativo do Project Online usando o modelo de objeto do cliente
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5740d0b2-5d36-40e4-9e83-577cb186359f
description: Este artigo descreve o Microsoft Project Online desenvolvimento de aplicativos para aplicativos de área de trabalho usando o .NET Framework 4.0. O aplicativo descrito neste artigo recupera informações do servidor de hospedagem.
ms.openlocfilehash: a0a2b4042d4db127c56c5ba873ebe25418344571
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771056"
---
# <a name="developing-a-project-online-application-using-the-client-side-object-model"></a><span data-ttu-id="62bd6-104">Desenvolvendo um aplicativo do Project Online usando o modelo de objeto do cliente</span><span class="sxs-lookup"><span data-stu-id="62bd6-104">Developing a Project Online application using the client-side object model</span></span>

<span data-ttu-id="62bd6-105">Este artigo descreve o Microsoft Project Online desenvolvimento de aplicativos para aplicativos de área de trabalho usando o .NET Framework 4.0.</span><span class="sxs-lookup"><span data-stu-id="62bd6-105">This article describes Microsoft Project Online application development for desktop applications using the .NET Framework 4.0.</span></span> <span data-ttu-id="62bd6-106">O aplicativo descrito neste artigo recupera informações do servidor de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="62bd6-106">The application described in this article retrieves information from the hosting server.</span></span> 
  
## <a name="background"></a><span data-ttu-id="62bd6-107">Background</span><span class="sxs-lookup"><span data-stu-id="62bd6-107">Background</span></span>

<span data-ttu-id="62bd6-108">Microsoft Project iniciado como aplicativo da área de trabalho da década de 1990 antecipado.</span><span class="sxs-lookup"><span data-stu-id="62bd6-108">Microsoft Project started as desktop application in the early 1990's.</span></span> <span data-ttu-id="62bd6-109">Atualmente, o projeto é muito mais, como confirmar suas diversas variedades:</span><span class="sxs-lookup"><span data-stu-id="62bd6-109">Today, Project is much more, as its several varieties attest:</span></span>
  
- <span data-ttu-id="62bd6-110">Project standard edition é um aplicativo de área de trabalho que é executado como um aplicativo autônomo.</span><span class="sxs-lookup"><span data-stu-id="62bd6-110">Project standard edition is a desktop application that runs as a stand-alone application.</span></span>
    
- <span data-ttu-id="62bd6-111">Edição de Project professional é um aplicativo de desktop que pode interagir e compartilhar dados com um servidor em uma escala maior, bem como executar a funcionalidade encontrada no Project standard edition.</span><span class="sxs-lookup"><span data-stu-id="62bd6-111">Project professional edition is a desktop application that can interact and share data with a server on a larger scale, as well as perform the functionality found in Project standard edition.</span></span>
    
- <span data-ttu-id="62bd6-112">Project Online é um serviço hospedado pela Microsoft oferece às empresas uma solução no nível PMO para coordenar e gerenciar projetos, programas e portfólios.</span><span class="sxs-lookup"><span data-stu-id="62bd6-112">Project Online is a Microsoft-hosted service that provides companies with a PMO-level solution to coordinate and manage projects, programs, and portfolios.</span></span> <span data-ttu-id="62bd6-113">Uma oferta de diferente que as edições da área de trabalho, o Project Online pode manter e rastrear detalhes do projeto em toda a duração de um projeto.</span><span class="sxs-lookup"><span data-stu-id="62bd6-113">A different offering than the desktop editions, Project Online can maintain and track project details throughout the life of a project.</span></span> 
    
- <span data-ttu-id="62bd6-114">Project Server é um serviço hospedado enterprise no qual a empresa gerencia e protege o servidor que contém o projeto, programa e informações de portfólio.</span><span class="sxs-lookup"><span data-stu-id="62bd6-114">Project Server is an enterprise-hosted service in which the enterprise manages and secures the server containing project, program, and portfolio information.</span></span> <span data-ttu-id="62bd6-115">Project Server, em virtude protegendo o servidor interno, oferece o projeto, programa e recursos de portfólio orientada a do hospedado externamente Project Online com uma maior capacidade de personalização.</span><span class="sxs-lookup"><span data-stu-id="62bd6-115">Project Server, by virtue of securing the server in-house, offers the project, program, and portfolio oriented features of externally-hosted Project Online with a greater capacity for customization.</span></span>
    
<span data-ttu-id="62bd6-116">Project Online tem três conjuntos de APIs online: modelo de objeto do cliente (CSOM), o modelo de objeto JavaScript (JSOM) e transferência de estado representacional (REST).</span><span class="sxs-lookup"><span data-stu-id="62bd6-116">Project Online has three online API sets: Client-side Object Model (CSOM), JavaScript Object Model (JSOM), and Representational State Transfer (REST).</span></span> 
  
- <span data-ttu-id="62bd6-117">A implementação do .NET CSOM é a interface preferida ao desenvolver aplicativos do Windows que interagem com locatários Project Online.</span><span class="sxs-lookup"><span data-stu-id="62bd6-117">The .NET CSOM implementation is the preferred interface when developing Windows applications that interact with Project Online tenants.</span></span> <span data-ttu-id="62bd6-118">Ambientes típicos para aplicativos centrados no usuário incluem áreas de trabalho do Windows e dispositivos Microsoft Surface.</span><span class="sxs-lookup"><span data-stu-id="62bd6-118">Typical environments for user-centric applications include Windows desktops and Microsoft Surface devices.</span></span> <span data-ttu-id="62bd6-119">Aplicativos back-end grafados com .NET CSOM podem se conectar a outros servidores para fontes de dados e lógica corporativos que são externos para o Project Online.</span><span class="sxs-lookup"><span data-stu-id="62bd6-119">Back-end applications written with .NET CSOM can connect to other servers for business logic and data sources that are external to Project Online.</span></span> <span data-ttu-id="62bd6-120">Solicitações de recuperação para o Project Online usam um sistema de consulta do tipo LINQ que oferece vários aprimoramentos em relação de funções de recuperação básica.</span><span class="sxs-lookup"><span data-stu-id="62bd6-120">Retrieval requests to Project Online use a LINQ-like query system that offers several enhancements over basic retrieval functions.</span></span>
    
- <span data-ttu-id="62bd6-121">A interface do modelo de objeto JavaScript (JSOM) oferece suporte a vários navegadores para suplementos Project Online. Um suplemento é um aplicativo web que é armazenado no Project Online inquilino.</span><span class="sxs-lookup"><span data-stu-id="62bd6-121">The JavaScript Object Model (JSOM) interface provides cross-browser support for Project Online Add-ins. An add-in is a web application that is stored in the Project Online tenant.</span></span> <span data-ttu-id="62bd6-122">Quando um usuário quiser executar um add-in, o código para o suplemento baixa e executa no navegador na máquina do usuário.</span><span class="sxs-lookup"><span data-stu-id="62bd6-122">When a user wants to run an add-in, the code for the add-in downloads and runs in the browser on the user machine.</span></span> 
    
- <span data-ttu-id="62bd6-123">O modelo do REST/Odata fornece comunicação baseada em HTTP, esta interface é recomendado para aplicativos em ambientes de não-Windows.</span><span class="sxs-lookup"><span data-stu-id="62bd6-123">The REST/Odata model provides HTTP-based communication, This interface is recommended for applications in non-Windows environments.</span></span> <span data-ttu-id="62bd6-124">Pontos de extremidade de comunicação são os objetos no site do Project Web Application (PWA).</span><span class="sxs-lookup"><span data-stu-id="62bd6-124">Communication endpoints are the objects in the Project Web Application (PWA) site.</span></span> <span data-ttu-id="62bd6-125">Resultados fornecem os códigos de status HTTP normais.</span><span class="sxs-lookup"><span data-stu-id="62bd6-125">Results provide normal HTTP status codes.</span></span>
    
<span data-ttu-id="62bd6-126">Este artigo concentra-se em um aplicativo que usa a interface CSOM do .NET.</span><span class="sxs-lookup"><span data-stu-id="62bd6-126">This article focuses on an application that uses the .NET CSOM interface.</span></span>
  
## <a name="prerequisites"></a><span data-ttu-id="62bd6-127">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="62bd6-127">Prerequisites</span></span>

<span data-ttu-id="62bd6-128">Comece com um sistema de base executando Windows 10 e, em seguida, adicione os seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="62bd6-128">Start with a base system running Windows 10, and add the following items:</span></span>
  
- <span data-ttu-id="62bd6-129">.NET framework 4.0 ou posterior – usam o framework completo.</span><span class="sxs-lookup"><span data-stu-id="62bd6-129">.Net Framework 4.0 or later -- Use the complete framework.</span></span> <span data-ttu-id="62bd6-130">O site de download está https://msdn.microsoft.com/en-us/vstudio/aa496123.aspx.</span><span class="sxs-lookup"><span data-stu-id="62bd6-130">The download site is https://msdn.microsoft.com/en-us/vstudio/aa496123.aspx.</span></span>
    
- <span data-ttu-id="62bd6-131">Visual Studio 2013 ou posterior – qualquer edição é aceitável.</span><span class="sxs-lookup"><span data-stu-id="62bd6-131">Visual Studio 2013 or later -- Any edition is acceptable.</span></span> <span data-ttu-id="62bd6-132">A edição de comunidade do Visual Studio de 2015 foi usada para desenvolver o aplicativo de amostra.</span><span class="sxs-lookup"><span data-stu-id="62bd6-132">The community edition of Visual Studio 2015 was used to develop the sample application.</span></span> <span data-ttu-id="62bd6-133">A edição de comunidade está disponível em https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx.</span><span class="sxs-lookup"><span data-stu-id="62bd6-133">The community edition is available at https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx.</span></span>
    
- <span data-ttu-id="62bd6-134">Componentes de cliente do SharePoint SDK – Project Online e Project Server ficam na parte superior do SharePoint e o SharePoint assemblies.</span><span class="sxs-lookup"><span data-stu-id="62bd6-134">SharePoint Client Components SDK -- Project Online and Project Server sit on top of SharePoint, and SharePoint assemblies.</span></span> <span data-ttu-id="62bd6-135">Os componentes de cliente do SharePoint estão incluídos no Visual Studio Professional e Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="62bd6-135">The SharePoint Client Components are included in Visual Studio Professional and Enterprise editions.</span></span> <span data-ttu-id="62bd6-136">Se você usar a edição da comunidade do Visual Studio, a versão mais recente do Office Developer Tools SDK está disponível no seguinte site: https://www.microsoft.com/en-us/download/details.aspx?id=35585.</span><span class="sxs-lookup"><span data-stu-id="62bd6-136">If you use Visual Studio Community edition, the latest version of the Office Developer Tools SDK is available at the following site: https://www.microsoft.com/en-us/download/details.aspx?id=35585.</span></span>
    
- <span data-ttu-id="62bd6-137">Uma conta de Project Online fornece acesso ao site de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="62bd6-137">A Project Online account -- This provides access to the hosting site.</span></span> <span data-ttu-id="62bd6-138">Para obter mais informações sobre como adquirir uma conta do Project Online, consulte https://products.office.com/en-us/Project/project-online-portfolio-management.</span><span class="sxs-lookup"><span data-stu-id="62bd6-138">For more information about obtaining a Project Online account, see https://products.office.com/en-us/Project/project-online-portfolio-management.</span></span>
    
- <span data-ttu-id="62bd6-139">Projetos no site de hospedagem que são preenchidos com informações</span><span class="sxs-lookup"><span data-stu-id="62bd6-139">Projects on the hosting site that are populated with information</span></span>
    
> [!NOTE]
> <span data-ttu-id="62bd6-140">O padrão (4.0 ou posterior) do .NET Framework é o correto framework usar.</span><span class="sxs-lookup"><span data-stu-id="62bd6-140">The standard .NET Framework (4.0 or later) is the correct framework to use.</span></span> <span data-ttu-id="62bd6-141">Não use o .NET Framework 4 Client Profile.</span><span class="sxs-lookup"><span data-stu-id="62bd6-141">Do not use the .NET Framework 4 Client Profile.</span></span> 
  
## <a name="develop-the-application"></a><span data-ttu-id="62bd6-142">Desenvolver o aplicativo</span><span class="sxs-lookup"><span data-stu-id="62bd6-142">Develop the application</span></span>

<span data-ttu-id="62bd6-143">Desenvolver um aplicativo de área de trabalho para o SharePoint, a interface preferencial é o modelo de objeto do lado do projeto cliente (CSOM).</span><span class="sxs-lookup"><span data-stu-id="62bd6-143">In developing a desktop application for SharePoint, the preferred interface is the Project client side object model (CSOM).</span></span> 
  
<span data-ttu-id="62bd6-144">Você pode baixar o exemplo completo em https://github.com/OfficeDev/Project-CSOM-List-Projects-Tasks.</span><span class="sxs-lookup"><span data-stu-id="62bd6-144">You can download the complete sample at https://github.com/OfficeDev/Project-CSOM-List-Projects-Tasks.</span></span>
  
<span data-ttu-id="62bd6-145">Os dois primeiros tópicos cobrem problemas básicos: Criando um projeto do Visual Studio com namespaces apropriados e assemblies e acessando o servidor de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="62bd6-145">The first two topics cover basic issues: creating a Visual Studio project with appropriate namespaces and assemblies, and accessing the hosting server.</span></span> <span data-ttu-id="62bd6-146">Os tópicos restantes lidam com Recuperando informações por meio de CSOM, de um e muitos objetos.</span><span class="sxs-lookup"><span data-stu-id="62bd6-146">The remaining topics deal with retrieving information through the CSOM, from one and many objects.</span></span> 
  
<span data-ttu-id="62bd6-147">Recuperar informações do host é um processo de ação de dois de aplicativos do cliente.</span><span class="sxs-lookup"><span data-stu-id="62bd6-147">Retrieving information from the host is a two-action process from client applications.</span></span> <span data-ttu-id="62bd6-148">Primeiro, o aplicativo especifica e envia uma ou mais solicitações de recuperação para o servidor.</span><span class="sxs-lookup"><span data-stu-id="62bd6-148">First, the application specifies and sends one or more retrieval requests to the server.</span></span> <span data-ttu-id="62bd6-149">Em segundo lugar, o aplicativo emite uma notificação para o servidor para executar as consultas enviadas.</span><span class="sxs-lookup"><span data-stu-id="62bd6-149">Second, the application issues a notification to the server to execute the submitted queries.</span></span> <span data-ttu-id="62bd6-150">O servidor responde enviando os resultados da consulta para o cliente.</span><span class="sxs-lookup"><span data-stu-id="62bd6-150">The server responds by sending the query results to the client.</span></span>
  
### <a name="set-up-the-visual-studio-project"></a><span data-ttu-id="62bd6-151">Configurar o projeto do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="62bd6-151">Set up the Visual Studio project</span></span>

<span data-ttu-id="62bd6-152">A instalação do aplicativo consiste em criar um novo projeto, vinculando os assemblies apropriados e declarando os namespaces necessários.</span><span class="sxs-lookup"><span data-stu-id="62bd6-152">The application setup consists of creating a new project, linking the appropriate assemblies and declaring the needed namespaces.</span></span> <span data-ttu-id="62bd6-153">O Visual Studio apresenta vários tipos de projetos de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="62bd6-153">Visual Studio presents several types of development projects.</span></span> 
  
#### <a name="select-a-visual-studio-project"></a><span data-ttu-id="62bd6-154">Selecione um projeto do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="62bd6-154">Select a Visual Studio project</span></span>

1. <span data-ttu-id="62bd6-155">Inicie o Visual Studio e selecione **Iniciar um novo projeto** , na página inicial.</span><span class="sxs-lookup"><span data-stu-id="62bd6-155">Launch Visual Studio and select **Start A New Project** on the Start Page.</span></span> 
    
   <span data-ttu-id="62bd6-156">A caixa de diálogo Novo projeto exibe modelos de aplicativos disponíveis e campos de dados para qualquer modelo selecionado.</span><span class="sxs-lookup"><span data-stu-id="62bd6-156">The New Project dialog displays available application templates, and data fields for any selected template.</span></span> 
    
2. <span data-ttu-id="62bd6-157">Para este aplicativo, especifique os seguintes itens.</span><span class="sxs-lookup"><span data-stu-id="62bd6-157">For this application, specify the following items.</span></span> <span data-ttu-id="62bd6-158">Palavras-chave, encontradas na tela tem um atributo negrito:</span><span class="sxs-lookup"><span data-stu-id="62bd6-158">Keywords encountered on the screen have a bold attribute:</span></span>
    
   1. <span data-ttu-id="62bd6-159">A partir de modelos de Installed no painel esquerdo, selecione **c#** => **Windows** => **desktop clássico**.</span><span class="sxs-lookup"><span data-stu-id="62bd6-159">From the Installed templates in the left pane, select **C#** => **Windows** => **Classic desktop**.</span></span> 
    
   2. <span data-ttu-id="62bd6-160">Na parte superior do painel central, selecione o **.NET Framework 4**.</span><span class="sxs-lookup"><span data-stu-id="62bd6-160">At the top of the central pane, select **.NET Framework 4**.</span></span> 
    
   3. <span data-ttu-id="62bd6-161">A partir de tipos de aplicativos, no painel central, escolha o **Aplicativo de Console**.</span><span class="sxs-lookup"><span data-stu-id="62bd6-161">From the application types in the central pane, choose **Console Application**.</span></span> 
    
   4. <span data-ttu-id="62bd6-162">Na seção inferior, especifique um nome e local para o projeto e o nome da solução.</span><span class="sxs-lookup"><span data-stu-id="62bd6-162">In the bottom section, specify a name and location for the project, and a solution name.</span></span> 
    
   5. <span data-ttu-id="62bd6-163">Também na seção inferior, marque a caixa de **criar diretório para a solução** .</span><span class="sxs-lookup"><span data-stu-id="62bd6-163">Also in the bottom section, check the **Create directory for solution** box.</span></span> 
    
3. <span data-ttu-id="62bd6-164">Clique em **Okey** para criar o projeto inicial.</span><span class="sxs-lookup"><span data-stu-id="62bd6-164">Click **OK** to create the initial project.</span></span> 
    
#### <a name="add-assemblies"></a><span data-ttu-id="62bd6-165">Adicionar assemblies</span><span class="sxs-lookup"><span data-stu-id="62bd6-165">Add assemblies</span></span>

<span data-ttu-id="62bd6-166">A solução VERSUS precisa o assembly ProjectServerClient do projeto 2103 SDK, algumas de assemblies do SDK do SharePoint e o assembly System. Security do .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="62bd6-166">The VS solution needs the ProjectServerClient assembly from the Project 2103 SDK, a couple of assemblies from the SharePoint SDK, and the .NET Framework System.Security assembly.</span></span>
  
1. <span data-ttu-id="62bd6-167">No Solution Explorer VERSUS, com o botão direito na entrada referências e selecione **Adicionar referência...**</span><span class="sxs-lookup"><span data-stu-id="62bd6-167">In the VS Solution Explorer, right-click the References entry, and select **Add Reference…**</span></span> <span data-ttu-id="62bd6-168">no menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="62bd6-168">from the shortcut menu.</span></span> 
    
2. <span data-ttu-id="62bd6-169">Verifique o **Microsoft.ProjectServer.Client.dll**.</span><span class="sxs-lookup"><span data-stu-id="62bd6-169">Check the **Microsoft.ProjectServer.Client.dll**.</span></span> 
    
   <span data-ttu-id="62bd6-170">Se necessário, clique no que **Procurar...**</span><span class="sxs-lookup"><span data-stu-id="62bd6-170">If needed, click the **Browse…**</span></span> <span data-ttu-id="62bd6-171">botão na parte inferior da caixa de diálogo e navegue até o diretório de instalação do SDK do Project 2013 para localizar o assembly.</span><span class="sxs-lookup"><span data-stu-id="62bd6-171">button at the bottom of the dialog and navigate to the Project 2013 SDK installation directory to locate the assembly.</span></span> 
    
3. <span data-ttu-id="62bd6-172">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="62bd6-172">Click **OK**.</span></span> 
    
4. <span data-ttu-id="62bd6-173">Adicione o namespace do cliente PrjoctServer ao arquivo. cs.</span><span class="sxs-lookup"><span data-stu-id="62bd6-173">Add the PrjoctServer Client namespace to the .cs file.</span></span>
    
   ```cs
    using Microsoft.ProjectServer.Client;
   ```

<span data-ttu-id="62bd6-174">Adicione os assemblies do SDK do SharePoint 2013 usando o Console do Gerenciador de pacotes do NuGet.</span><span class="sxs-lookup"><span data-stu-id="62bd6-174">Add the SharePoint 2013 SDK assemblies using the NuGet Package Manager Console.</span></span> 
  
1. <span data-ttu-id="62bd6-175">No menu Ferramentas do VS, clique nos seguintes menus: **ferramentas =\> NuGet Package Manager =\> Package Manager Console**.</span><span class="sxs-lookup"><span data-stu-id="62bd6-175">From the VS Tools menu, click the following menus: **Tools =\> NuGet Package Manager =\> Package Manager Console**.</span></span> 
    
2. <span data-ttu-id="62bd6-176">No Console do Gerenciador de pacotes, digite o seguinte comando e pressione \<ENTER\>:</span><span class="sxs-lookup"><span data-stu-id="62bd6-176">In the Package Manager Console, enter the following command and press \<ENTER\>:</span></span>
    
   ```cs
    Install-Package Microsoft.SharePointOnline.CSOM
   ```

   <span data-ttu-id="62bd6-177">O **Console do Gerenciador de pacote** fornece uma descrição dos resultados do comando; e, então, VERSUS Solution Explorer exibe os assemblies do SharePoint nas referências de projeto.</span><span class="sxs-lookup"><span data-stu-id="62bd6-177">The **Package Manager Console** provides a description of the command results; and, the VS Solution Explorer displays the SharePoint assemblies in the project references.</span></span> 
    
3. <span data-ttu-id="62bd6-178">Adicione os espaços para nome para o arquivo. cs:</span><span class="sxs-lookup"><span data-stu-id="62bd6-178">Add the namespaces to the .cs file:</span></span>
    
   ```cs
    using Microsoft.SharePoint.Client;
   ```

<span data-ttu-id="62bd6-179">O assembly System. Security faz parte do .NET Framework e foi instalado com o framework.</span><span class="sxs-lookup"><span data-stu-id="62bd6-179">The System.Security assembly is part of .NET Framework and was installed with the framework.</span></span> <span data-ttu-id="62bd6-180">O aplicativo de amostra precisa mais um namespace que fornece uma cadeia de caracteres criptografada para o sistema de hospedagem para autenticação.</span><span class="sxs-lookup"><span data-stu-id="62bd6-180">The sample application needs one more namespace that provides an encrypted string to the hosting system for authentication.</span></span> <span data-ttu-id="62bd6-181">Uma vez autenticado, o aplicativo pode acessar os projetos no sistema de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="62bd6-181">Once authenticated, the application can access projects on the hosting system.</span></span> <span data-ttu-id="62bd6-182">Adicione o namespace System. Security ao arquivo. cs desta forma:</span><span class="sxs-lookup"><span data-stu-id="62bd6-182">Add the System.Security namespace to the .cs file in this way:</span></span>
  
1. <span data-ttu-id="62bd6-183">No Solution Explorer VERSUS, com o botão direito na entrada referências e selecione **Adicionar referência...**</span><span class="sxs-lookup"><span data-stu-id="62bd6-183">In the VS Solution Explorer, right-click the References entry, and select **Add Reference…**</span></span> <span data-ttu-id="62bd6-184">no menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="62bd6-184">from the shortcut menu.</span></span> 
    
2. <span data-ttu-id="62bd6-185">Selecione **Assemblies =\> Framework** no painel à esquerda da caixa de diálogo Gerenciador de referências, verifique se **System. Security**.</span><span class="sxs-lookup"><span data-stu-id="62bd6-185">Select **Assemblies =\> Framework** in the left pane of the References Manager dialog, then check **System.Security**.</span></span> 
    
3. <span data-ttu-id="62bd6-186">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="62bd6-186">Click **OK**.</span></span> 
    
4. <span data-ttu-id="62bd6-187">Adicione o namespace System. Security ao arquivo. cs:</span><span class="sxs-lookup"><span data-stu-id="62bd6-187">Add the System.Security namespace to the .cs file:</span></span>
    
   ```cs
    using System.Security;
   ```

<span data-ttu-id="62bd6-188">O início do arquivo. cs deve conter os seguintes namespaces:</span><span class="sxs-lookup"><span data-stu-id="62bd6-188">The start of the .cs file should contain the following namespaces:</span></span>
  
- <span data-ttu-id="62bd6-189">System</span><span class="sxs-lookup"><span data-stu-id="62bd6-189">System</span></span>
    
- <span data-ttu-id="62bd6-190">System.Collections.Generic</span><span class="sxs-lookup"><span data-stu-id="62bd6-190">System.Collections.Generic</span></span>
    
- <span data-ttu-id="62bd6-191">System. Linq</span><span class="sxs-lookup"><span data-stu-id="62bd6-191">System.Linq</span></span>
    
- <span data-ttu-id="62bd6-192">System.Test</span><span class="sxs-lookup"><span data-stu-id="62bd6-192">System.Test</span></span>
    
- <span data-ttu-id="62bd6-193">Microsoft.ProjectServer.Client</span><span class="sxs-lookup"><span data-stu-id="62bd6-193">Microsoft.ProjectServer.Client</span></span>
    
- <span data-ttu-id="62bd6-194">Microsoft.SharePoint.Client</span><span class="sxs-lookup"><span data-stu-id="62bd6-194">Microsoft.SharePoint.Client</span></span>
    
- <span data-ttu-id="62bd6-195">System. Security</span><span class="sxs-lookup"><span data-stu-id="62bd6-195">System.Security</span></span>
    
### <a name="connect-to-the-host-system"></a><span data-ttu-id="62bd6-196">Conectar ao sistema de host</span><span class="sxs-lookup"><span data-stu-id="62bd6-196">Connect to the host system</span></span>

<span data-ttu-id="62bd6-197">Project Online é um aplicativo do SharePoint, portanto, usando a autenticação do SharePoint é a abordagem correta.</span><span class="sxs-lookup"><span data-stu-id="62bd6-197">Project Online is a SharePoint application, so using SharePoint authentication is the correct approach.</span></span> <span data-ttu-id="62bd6-198">O fragmento de código a seguir se prepara para acessar o ambiente hospedado.</span><span class="sxs-lookup"><span data-stu-id="62bd6-198">The following code fragment prepares to access the hosted environment.</span></span>
  
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

<span data-ttu-id="62bd6-199">Preparações para acessar o ambiente hospedado incluem os seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="62bd6-199">Preparations to access the hosted environment include the following items:</span></span>
  
1. <span data-ttu-id="62bd6-200">Crie um objeto de contexto para os projetos – isso está contido no código a seguir do fragmento de código anterior.</span><span class="sxs-lookup"><span data-stu-id="62bd6-200">Create a context object for the projects -- this is contained in the following code of the preceding code fragment.</span></span> 
    
   ```cs
    private static ProjectContext projContext;
    
   ```

   <span data-ttu-id="62bd6-201">O contexto é herdado por outros componentes, permitindo que o sistema gerenciar o contexto do modelo de objeto do projeto.</span><span class="sxs-lookup"><span data-stu-id="62bd6-201">The context is inherited by other components, allowing the system to manage the context of the Project object model.</span></span>
    
2. <span data-ttu-id="62bd6-202">Identificar o site do host--isso é feito no código a seguir no fragmento de código anterior.</span><span class="sxs-lookup"><span data-stu-id="62bd6-202">Identify the host site -- this is done in the following code from the preceding code fragment.</span></span>
    
   ```cs
    using (ProjectContext projContext = new ProjectContext("https://Contoso.sharepoint.com/sites/pwa"))
   ```

   <span data-ttu-id="62bd6-203">Ao instanciar o contexto de projetos, o aplicativo precisa fornecer a raiz do conjunto de sites de projetos.</span><span class="sxs-lookup"><span data-stu-id="62bd6-203">When instantiating the projects context, the application needs to provide the root of the Projects site collection.</span></span> <span data-ttu-id="62bd6-204">O aplicativo usa uma subcadeia de caracteres da URL da raiz dos projetos.</span><span class="sxs-lookup"><span data-stu-id="62bd6-204">The application uses a substring of the URL of the root of the Projects.</span></span> <span data-ttu-id="62bd6-205">Um instantâneo deste local é realçado com um retângulo vermelho na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="62bd6-205">A snapshot of this location is highlighted with a red rectangle in the following illustration.</span></span> <span data-ttu-id="62bd6-206">A autenticação precisa a cadeia de caracteres de seu início por meio de subcadeia de caracteres "pwa".</span><span class="sxs-lookup"><span data-stu-id="62bd6-206">The authentication needs the string from its start through the substring "pwa".</span></span> <span data-ttu-id="62bd6-207">Na listagem de código, o aplicativo usa a cadeia de caracteres "https://XXXXXXXX.sharepoint.com/sites/pwa".</span><span class="sxs-lookup"><span data-stu-id="62bd6-207">In the code listing, the application uses the string "https://XXXXXXXX.sharepoint.com/sites/pwa".</span></span>
        
   <span data-ttu-id="62bd6-208">![Captura de tela da URL do conjunto de sites de projetos dentro de uma borda vermelha.] (media/d48c4894-5dba-46b6-886a-3c59bfb83c4d.png "Conjunto dentro de uma borda vermelha de sites de captura de tela da URL dos projetos")</span><span class="sxs-lookup"><span data-stu-id="62bd6-208">![Screen shot of the URL of the Projects site collection within a red border.](media/d48c4894-5dba-46b6-886a-3c59bfb83c4d.png "Screen shot of the URL of the Projects site collection within a red border")</span></span>
  
3. <span data-ttu-id="62bd6-209">Colocar a senha em uma cadeia de caracteres segura--isso é feito no código a seguir no fragmento de código anterior.</span><span class="sxs-lookup"><span data-stu-id="62bd6-209">Place the password in a secure string -- this is done in the following code from the preceding code fragment.</span></span>
    
   ```cs
    SecureString password - new SecureString();
    foreach (char c in "password".ToCharArray()) password.AppendChar(c);
    
   ```

   <span data-ttu-id="62bd6-210">A conta de usuário e senha são as credenciais para acessar o site do host.</span><span class="sxs-lookup"><span data-stu-id="62bd6-210">The password and user account are the credentials to access the host site.</span></span> 
    
4. <span data-ttu-id="62bd6-211">Adicionar a conta de usuário e senha para a parte de credenciais do objeto contexto – isso é feito no código a seguir no fragmento de código anterior.</span><span class="sxs-lookup"><span data-stu-id="62bd6-211">Add the user account and password to the credentials portion of the context object -- this is done in the following code from the preceding code fragment.</span></span>
    
   ```cs
    projContext.Credentials = new SharePointOnlineCredentials("sarad@Contoso.onmicrosoft.com", password);
   ```

<span data-ttu-id="62bd6-212">O contexto de projeto instanciadas está pronto para uso.</span><span class="sxs-lookup"><span data-stu-id="62bd6-212">The instantiated project context is ready to use.</span></span>
  
### <a name="list-all-published-projects"></a><span data-ttu-id="62bd6-213">Listar projetos publicados tudo</span><span class="sxs-lookup"><span data-stu-id="62bd6-213">List all published projects</span></span>

<span data-ttu-id="62bd6-214">Project Online e ProjectServer usam proxies para se comunicar com o servidor para criar, relatório, atualizar e excluir operações (CRUD).</span><span class="sxs-lookup"><span data-stu-id="62bd6-214">Project Online and ProjectServer use proxies to communicate with the server for create, report, update, and delete (CRUD) operations.</span></span> <span data-ttu-id="62bd6-215">Servidor/host processa solicitações de maneira eficiente e tem o cliente a executar as seguintes ações na comunicação com o servidor:</span><span class="sxs-lookup"><span data-stu-id="62bd6-215">The host/server handles requests in an efficient manner and has the client perform the following actions in communicating with the server:</span></span>
  
1. <span data-ttu-id="62bd6-216">Estabelece um contexto para comunicação.</span><span class="sxs-lookup"><span data-stu-id="62bd6-216">Establish a context for communication.</span></span> 
    
   <span data-ttu-id="62bd6-217">O contexto é usado pelo conjunto de projetos, bem como outros objetos e coleções por meio de herança, incluindo a coleção tasks, coleção assignments, o objeto stage e campos personalizados.</span><span class="sxs-lookup"><span data-stu-id="62bd6-217">The context is used by the projects collection, as well as other objects and collections through inheritance, including the tasks collection, assignments collection, the stage object, and custom fields.</span></span> 
    
2. <span data-ttu-id="62bd6-218">Use o modelo de objeto para especificar um objeto, coleção ou dados a serem recuperados.</span><span class="sxs-lookup"><span data-stu-id="62bd6-218">Use the object model to specify an object, collection, or data to retrieve.</span></span>
    
   <span data-ttu-id="62bd6-219">Esta etapa usa LINQ como uma consulta ou como um método.</span><span class="sxs-lookup"><span data-stu-id="62bd6-219">This step uses LINQ as a query or as a method.</span></span> <span data-ttu-id="62bd6-220">A especificação controla o que você recebe.</span><span class="sxs-lookup"><span data-stu-id="62bd6-220">The specification controls what you receive.</span></span> <span data-ttu-id="62bd6-221">Muitas vezes, esta etapa é incorporada como o corpo do método Load (etapa 3).</span><span class="sxs-lookup"><span data-stu-id="62bd6-221">Often, this step is embedded as the body of the Load method (step 3).</span></span> 
    
3. <span data-ttu-id="62bd6-222">Carregar a especificação de recuperação da etapa anterior usando o método Load () ou LoadQuery().</span><span class="sxs-lookup"><span data-stu-id="62bd6-222">Load the retrieval specification from the previous step using the Load() or LoadQuery() method.</span></span>
    
   <span data-ttu-id="62bd6-223">Para carregar os objetos e coleções, use Load ().</span><span class="sxs-lookup"><span data-stu-id="62bd6-223">For loading collections and objects, use Load().</span></span> <span data-ttu-id="62bd6-224">Para consultas com cláusulas como "where" e "grupo", use LoadQuery().</span><span class="sxs-lookup"><span data-stu-id="62bd6-224">For queries with clauses such as "where" and "group", use LoadQuery().</span></span> 
    
4. <span data-ttu-id="62bd6-225">Execute a solicitação usando o método ExecuteQuery ().</span><span class="sxs-lookup"><span data-stu-id="62bd6-225">Execute the request using the ExecuteQuery() method.</span></span>
    
   <span data-ttu-id="62bd6-226">O método ExecuteQuery () notifica o host que estão prontas para execução da consulta ou consultas.</span><span class="sxs-lookup"><span data-stu-id="62bd6-226">The ExecuteQuery() method notifies the host that the query or queries are ready to execute.</span></span> <span data-ttu-id="62bd6-227">Depois que o host recebe uma notificação, ela executa as consultas e envia os resultados para o cliente.</span><span class="sxs-lookup"><span data-stu-id="62bd6-227">Once the host receives notification, it executes the queries and sends the results to the client.</span></span> 
    
<span data-ttu-id="62bd6-228">Com as informações no cliente, o aplicativo pode usá-lo.</span><span class="sxs-lookup"><span data-stu-id="62bd6-228">With the information at the client, the application can use it.</span></span> <span data-ttu-id="62bd6-229">O fragmento de código a seguir percorre os projetos publicados e imprime a Id e o nome para cada projeto publicado no host.</span><span class="sxs-lookup"><span data-stu-id="62bd6-229">The following code fragment cycles through the published projects and prints the Id and Name for each published project on the host.</span></span>
  
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

<span data-ttu-id="62bd6-230">Saída:</span><span class="sxs-lookup"><span data-stu-id="62bd6-230">Output:</span></span>
  
```cs
Published Project count:2
1. be80a848-b2ef-e511-80f4-00155dc84e01   A second Project     3/21/2016 10:14:40 PM
2. 9d730a1a-60ed-e511-80f6-00155dc87d01   Ent_Proj_1   3/18/2016 11:21:14 PM

```

### <a name="make-a-request"></a><span data-ttu-id="62bd6-231">Fazer uma solicitação</span><span class="sxs-lookup"><span data-stu-id="62bd6-231">Make a request</span></span>

<span data-ttu-id="62bd6-232">Usando as ações de fragmento de código anterior, o aplicativo recupera a lista de projetos na conta especificada no site de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="62bd6-232">Using the actions from the previous code fragment, the application retrieves the list of projects in the specified account on the hosting site.</span></span> 
  
1. <span data-ttu-id="62bd6-233">O ProjectContext for especificado para listar os projetos.</span><span class="sxs-lookup"><span data-stu-id="62bd6-233">The ProjectContext is specified for the projects to list.</span></span> 
    
   ```cs
    var projects = projContext.Projects;
   ```

2. <span data-ttu-id="62bd6-234">Especifique o item a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="62bd6-234">Specify the item to retrieve.</span></span> 
    
   ```cs
    projContext.Load(projects);
   ```

   <span data-ttu-id="62bd6-235">Por informando apenas a coleção, o servidor recupera a coleção de projetos, preenchendo a cada projeto com valores para o conjunto de propriedades padrão.</span><span class="sxs-lookup"><span data-stu-id="62bd6-235">By only stating the collection, the server retrieves the project collection, populating each project with values for the default set of properties.</span></span> <span data-ttu-id="62bd6-236">Acesso às propriedades que fazem parte do conjunto de propriedades padrão concede resultados bem-sucedidos.</span><span class="sxs-lookup"><span data-stu-id="62bd6-236">Accessing properties that are part of the default property set gives successful results.</span></span> <span data-ttu-id="62bd6-237">Acesso às propriedades que não fazem parte do padrão definir resultados em uma exceção "Não inicializado".</span><span class="sxs-lookup"><span data-stu-id="62bd6-237">Accessing properties that are not part of the default set results in a "Not initialized" exception.</span></span>
    
3. <span data-ttu-id="62bd6-238">Carregar a solicitação (projContext.Load).</span><span class="sxs-lookup"><span data-stu-id="62bd6-238">Load the request (projContext.Load).</span></span>
    
   <span data-ttu-id="62bd6-239">Isso é parte da etapa anterior.</span><span class="sxs-lookup"><span data-stu-id="62bd6-239">This is part of the previous step.</span></span>
    
4. <span data-ttu-id="62bd6-240">Executa a consulta (ExecuteQuery).</span><span class="sxs-lookup"><span data-stu-id="62bd6-240">Execute the query (ExecuteQuery).</span></span> 
    
   ```cs
    projContext.ExecuteQuery();
   ```

### <a name="retrieve-high-level-project-information"></a><span data-ttu-id="62bd6-241">Recuperar informações de projeto de alto nível</span><span class="sxs-lookup"><span data-stu-id="62bd6-241">Retrieve high-level project information</span></span>

<span data-ttu-id="62bd6-242">Propriedades que não são propriedades padrão devem ser especificadas na solicitação ao servidor.</span><span class="sxs-lookup"><span data-stu-id="62bd6-242">Properties that are not default properties must be specified in the request to the server.</span></span> <span data-ttu-id="62bd6-243">O próximo fragmento de código carrega o contexto do conjunto de projetos do exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="62bd6-243">The next code fragment loads the projects collection context as in the previous example.</span></span> <span data-ttu-id="62bd6-244">Em seguida, a especificação solicita propriedades adicionais de não-padrão para incluir no resultado.</span><span class="sxs-lookup"><span data-stu-id="62bd6-244">Then, the specification requests additional non-default properties to include in the result.</span></span> 
  
```cs
var projects = projContext.Projects;
projContext.Load(projects,
    ps => ps.IncludeWithDefaultProperties(
        p => p.StartDate, p => p.Phase, p => p.Stage));
projContext.ExecuteQuery();

```

<span data-ttu-id="62bd6-245">A instrução de carga Especifica o contexto do conjunto de projetos e adiciona o StartDate, fase e estágio para o resultado da consulta.</span><span class="sxs-lookup"><span data-stu-id="62bd6-245">The load statement specifies the projects collection context, and adds the StartDate, Phase, and Stage to the query result.</span></span> <span data-ttu-id="62bd6-246">As propriedades adicionais podem ser escalares, objetos ou coleções.</span><span class="sxs-lookup"><span data-stu-id="62bd6-246">The additional properties can be scalar, objects, or collections.</span></span> <span data-ttu-id="62bd6-247">Escalares itens podem ser acessados diretamente.</span><span class="sxs-lookup"><span data-stu-id="62bd6-247">Scalar items can be accessed directly.</span></span> <span data-ttu-id="62bd6-248">Objetos e coleções exigem processamento adicional, como o fragmento de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="62bd6-248">Objects and collections require additional processing, as in the following code fragment.</span></span>
  
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

<span data-ttu-id="62bd6-249">Saída dos três primeiros projetos:</span><span class="sxs-lookup"><span data-stu-id="62bd6-249">Output of the first three projects:</span></span>
  
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

### <a name="retrieve-all-tasks-in-a-project"></a><span data-ttu-id="62bd6-250">Recuperar todas as tarefas em um projeto</span><span class="sxs-lookup"><span data-stu-id="62bd6-250">Retrieve all tasks in a project</span></span>

<span data-ttu-id="62bd6-251">Cada projeto tem muitas tarefas.</span><span class="sxs-lookup"><span data-stu-id="62bd6-251">Each project has many tasks.</span></span> <span data-ttu-id="62bd6-252">Portanto, desligar as tarefas para um único projeto consiste das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="62bd6-252">So, pulling the tasks for a single project consists of the following:</span></span>
  
1. <span data-ttu-id="62bd6-253">Estabelece o contexto do conjunto de projetos.</span><span class="sxs-lookup"><span data-stu-id="62bd6-253">Establish the context of the projects collection.</span></span>
    
   ```cs
    var projects = projContext.Projects;
   ```

2. <span data-ttu-id="62bd6-254">Recupere as informações de projeto, incluindo as propriedades da tarefa.</span><span class="sxs-lookup"><span data-stu-id="62bd6-254">Retrieve the project information, including the Task properties.</span></span>
    
   ```cs
    projContext.Load(projects);
    ProjContext.ExecuteQuery();
    foreach (PublishedProject pubProj in projContext.Projects){
    
   ```

    <span data-ttu-id="62bd6-255">Observe que o aplicativo está lidando com projetos publicados.</span><span class="sxs-lookup"><span data-stu-id="62bd6-255">Note that the application is addressing published projects.</span></span> <span data-ttu-id="62bd6-256">O contexto para o projeto publicado atual é pubProj.</span><span class="sxs-lookup"><span data-stu-id="62bd6-256">The context for the current published project is pubProj.</span></span> 
    
3. <span data-ttu-id="62bd6-257">Estabelece o contexto de coleção Tasks.</span><span class="sxs-lookup"><span data-stu-id="62bd6-257">Establish the context for the Tasks collection.</span></span>
    
   ```cs
    PublishedTaskCollection collTask = pubProj.Tasks;
   ```

   <span data-ttu-id="62bd6-258">O `pubProj.Tasks` propriedade referencia as tarefas do projeto atual publicado.</span><span class="sxs-lookup"><span data-stu-id="62bd6-258">The `pubProj.Tasks` property references the tasks of the current published project.</span></span> 
    
4. <span data-ttu-id="62bd6-259">Carregar a especificação para recuperar o conjunto de tarefa, incluindo as propriedades adequadas de não-padrão.</span><span class="sxs-lookup"><span data-stu-id="62bd6-259">Load the specification to retrieve Task collection, including the appropriate non-default properties.</span></span>
    
   ```cs
    projContext.Load(collTask,
        tsk => tsk.IncludeWithDefaultProperties(
            t => t.Id, t => t.Name, t => t.Start,
            t => t.ScheduledStart, t => t.Completion));
    
   ```

5. <span data-ttu-id="62bd6-260">Executa a consulta para recuperar a coleção de tarefa com as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="62bd6-260">Execute the query to retrieve the Task collection with the appropriate properties.</span></span>
    
   ```cs
    projContext.ExecuteQuery();
   ```

<span data-ttu-id="62bd6-261">Agora, a informação é local.</span><span class="sxs-lookup"><span data-stu-id="62bd6-261">The information is now local.</span></span> <span data-ttu-id="62bd6-262">O fragmento de código a seguir processa a coleção tasks publicado escrevendo as informações no console.</span><span class="sxs-lookup"><span data-stu-id="62bd6-262">The following code fragment processes the published tasks collection by writing the information to the console.</span></span>
  
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

<span data-ttu-id="62bd6-263">Saída de tarefas para um projeto:</span><span class="sxs-lookup"><span data-stu-id="62bd6-263">Output of tasks for one project:</span></span>
  
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

### <a name="access-information-at-multiple-levels"></a><span data-ttu-id="62bd6-264">Informações de acesso em vários níveis</span><span class="sxs-lookup"><span data-stu-id="62bd6-264">Access information at multiple levels</span></span>

<span data-ttu-id="62bd6-265">Cada tarefa pode ter uma ou mais pessoas (também conhecido como</span><span class="sxs-lookup"><span data-stu-id="62bd6-265">Each task can have one or more persons (a.k.a.</span></span> <span data-ttu-id="62bd6-266">recurso) contribuindo rumo à sua conclusão.</span><span class="sxs-lookup"><span data-stu-id="62bd6-266">resource) contributing toward its completion.</span></span> <span data-ttu-id="62bd6-267">Os conjuntos de recursos e atribuições contenham essas informações para cada tarefa.</span><span class="sxs-lookup"><span data-stu-id="62bd6-267">The Assignments and Resources collections contain this information for each task.</span></span> 
  
<span data-ttu-id="62bd6-268">O processamento consiste no seguinte:</span><span class="sxs-lookup"><span data-stu-id="62bd6-268">The processing consists of the following:</span></span>
  
1. <span data-ttu-id="62bd6-269">Obtendo um contexto para a tarefa do projeto.</span><span class="sxs-lookup"><span data-stu-id="62bd6-269">Obtaining a context for the project task.</span></span>
    
2. <span data-ttu-id="62bd6-270">Crie uma solicitação e carregar a solicitação para as atribuições vinculadas à tarefa.</span><span class="sxs-lookup"><span data-stu-id="62bd6-270">Build a request and load the request for the assignments tied to the task.</span></span> 
    
3. <span data-ttu-id="62bd6-271">Executa a consulta para as atribuições.</span><span class="sxs-lookup"><span data-stu-id="62bd6-271">Execute the query for the assignments.</span></span>
    
4. <span data-ttu-id="62bd6-272">Crie uma solicitação e carregar a solicitação para o recurso associado a uma atribuição individual.</span><span class="sxs-lookup"><span data-stu-id="62bd6-272">Build a request and load the request for the resource associated with an individual assignment.</span></span> 
    
5. <span data-ttu-id="62bd6-273">Executa a consulta para o recurso.</span><span class="sxs-lookup"><span data-stu-id="62bd6-273">Execute the query for the resource.</span></span>
    
> [!NOTE] 
> - <span data-ttu-id="62bd6-274">A coleção Assignments é solicitada explicitamente as informações do servidor porque ele não é uma propriedade padrão da coleção Tasks.</span><span class="sxs-lookup"><span data-stu-id="62bd6-274">The Assignments collection is explicitly requested in the information from the server because it is not a default property of the Tasks collection.</span></span> <span data-ttu-id="62bd6-275">Como um conjunto, será feita uma consulta subsequente retire o conjunto do servidor.</span><span class="sxs-lookup"><span data-stu-id="62bd6-275">As a collection, a subsequent query is made to pull the collection from the server.</span></span> 
> - <span data-ttu-id="62bd6-276">O recurso é um objeto.</span><span class="sxs-lookup"><span data-stu-id="62bd6-276">The Resource is an object.</span></span> <span data-ttu-id="62bd6-277">A consulta para uma atribuição inclui o nome do recurso associado à atribuição.</span><span class="sxs-lookup"><span data-stu-id="62bd6-277">The query for an assignment includes the resource name associated with the assignment.</span></span>
    
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

<span data-ttu-id="62bd6-278">Saída para tarefas 52, 75 e 76 de um projeto:</span><span class="sxs-lookup"><span data-stu-id="62bd6-278">Output for tasks 52, 75, and 76 of a project:</span></span>
  
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

### <a name="access-custom-enterprise-level-fields"></a><span data-ttu-id="62bd6-279">Campos personalizados de nível empresarial acesso</span><span class="sxs-lookup"><span data-stu-id="62bd6-279">Access custom enterprise-level fields</span></span>

<span data-ttu-id="62bd6-280">Campos personalizados existirem para o Project Online.</span><span class="sxs-lookup"><span data-stu-id="62bd6-280">Custom fields exist for Project Online.</span></span> <span data-ttu-id="62bd6-281">Esses são os campos de nível empresarial que podem ser associados ao projeto individual.</span><span class="sxs-lookup"><span data-stu-id="62bd6-281">These are enterprise-level fields that can be associated with individual project.</span></span> <span data-ttu-id="62bd6-282">Esta seção descreve como acessar esses campos.</span><span class="sxs-lookup"><span data-stu-id="62bd6-282">This section describes how to access these fields.</span></span> 
  
<span data-ttu-id="62bd6-283">Campos personalizados não são incluídos no conjunto padrão das propriedades associadas a um projeto.</span><span class="sxs-lookup"><span data-stu-id="62bd6-283">Custom fields are not included in the default set of properties associated with a project.</span></span> <span data-ttu-id="62bd6-284">Portanto, elas precisam identificação explícita na especificação da recuperação.</span><span class="sxs-lookup"><span data-stu-id="62bd6-284">So, they need explicit identification in the retrieval specification.</span></span> <span data-ttu-id="62bd6-285">O modo de exibição de alto nível do processo consiste dos seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="62bd6-285">The high-level view of the process consists of the following items:</span></span>
  
1. <span data-ttu-id="62bd6-286">Túnel para o campo personalizado usando seu nome comum.</span><span class="sxs-lookup"><span data-stu-id="62bd6-286">Tunnel to the custom field using its common name.</span></span>
    
2. <span data-ttu-id="62bd6-287">Recupere o nome interno do campo personalizado.</span><span class="sxs-lookup"><span data-stu-id="62bd6-287">Retrieve the internal name of the custom field.</span></span>
    
3. <span data-ttu-id="62bd6-288">Volte para o contexto global e o sistema utilizando o nome interno do campo personalizado de consulta.</span><span class="sxs-lookup"><span data-stu-id="62bd6-288">Return to the global context and query the system using the internal name of the custom field.</span></span>
    
#### <a name="tunnel-to-the-custom-field-retrieve-its-internal-name-and-used-it-to-query-the-system"></a><span data-ttu-id="62bd6-289">Campo personalizado de túnel, recuperar seu nome interno e utilizou para o sistema de consulta</span><span class="sxs-lookup"><span data-stu-id="62bd6-289">Tunnel to the custom field, retrieve its internal name, and used it to query the system</span></span>

<span data-ttu-id="62bd6-290">Essa tarefa especifica uma recuperação que usa uma propriedade de não-padrão com um detalhe adicionado.</span><span class="sxs-lookup"><span data-stu-id="62bd6-290">This task specifies a retrieval that uses a non-default property with one added detail.</span></span>
  
1. <span data-ttu-id="62bd6-291">Comece usando o contexto de projetos, conforme descrito no início deste artigo.</span><span class="sxs-lookup"><span data-stu-id="62bd6-291">Begin by using the projects context, as described at the beginning of this article.</span></span>
    
   ```cs
    // Get the list of published projects in Project Web App.
    var projects = projContext.Projects;
    
   ```

2. <span data-ttu-id="62bd6-292">Adicione dois itens para a solicitação de recuperação de conjunto de projetos além de quaisquer outras propriedades de não-padrão para recuperar:</span><span class="sxs-lookup"><span data-stu-id="62bd6-292">Add two items to the projects collection retrieval request in addition to any other non-default properties to retrieve:</span></span>
    
   ```cs
    projContext.Load(projects,
        ps => ps.IncludeWithDefaultProperties(
            p => p.Phase, p => p.Stage,                  // Other nondefault properties
            p => p.IncludeCustomFields,                  // Gets PublishedProject object 
                                                        // that contains custom fields
            p => p.IncludeCustomFields.CustomFields));   // Populates the custom fields
                    projContext.ExecuteQuery();
    
   ```

   <span data-ttu-id="62bd6-293">O `p => p.IncludeCustomFields` cláusula identifica a necessidade de usar um objeto de projeto que ofereça suporte a campos personalizados.</span><span class="sxs-lookup"><span data-stu-id="62bd6-293">The  `p => p.IncludeCustomFields` clause identifies the need to use a project object that supports custom fields.</span></span> 
    
   <span data-ttu-id="62bd6-294">O `p => p.IncludeCustomFields.CustomFields` cláusula solicita a inclusão de dados de campo personalizado no resultado da consulta.</span><span class="sxs-lookup"><span data-stu-id="62bd6-294">The  `p => p.IncludeCustomFields.CustomFields` clause requests the inclusion of custom field data in the query result.</span></span> <span data-ttu-id="62bd6-295">Essa informação é usada após o nome interno de campo personalizado é recuperado.</span><span class="sxs-lookup"><span data-stu-id="62bd6-295">This information is used after the custom field internal name is retrieved.</span></span> 
    
3. <span data-ttu-id="62bd6-296">Carregar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="62bd6-296">Load the request.</span></span>
    
   <span data-ttu-id="62bd6-297">Isso é parte da etapa anterior.</span><span class="sxs-lookup"><span data-stu-id="62bd6-297">This is part of the previous step.</span></span>
    
4. <span data-ttu-id="62bd6-298">Execute a consulta.</span><span class="sxs-lookup"><span data-stu-id="62bd6-298">Execute the Query.</span></span>
    
   ```cs
    projContext.ExecuteQuery()
   ```

5. <span data-ttu-id="62bd6-299">Com essas informações no cliente, crie uma solicitação para recuperar os campos personalizados associados ao projeto atual.</span><span class="sxs-lookup"><span data-stu-id="62bd6-299">With this information on the client, build a request to retrieve the custom fields associated with the current project.</span></span>
    
   ```cs
    foreach (PublishedProject pubProj in projContext.Projects)
    {
        //Console.WriteLine("\n\t{0}. \t{1} \n\t\t{2} \n\t\t{3} \n", 
                j++, pubProj.Id, pubProj.Name, pubProj.CreatedDate);
        CustomFieldCollection collCustF = pubProj.CustomFields;
                        
        projContext.Load(collCustF);
        projContext.ExecuteQuery();
    
   ```

6. <span data-ttu-id="62bd6-300">Localize o campo personalizado apropriado e recuperar o nome interno do campo.</span><span class="sxs-lookup"><span data-stu-id="62bd6-300">Locate the appropriate custom field and retrieve the internal name of the field.</span></span> 
    
   ```cs
        foreach (CustomField oCF in collCustF)
        {
            if (oCF.Name == "Project Health")
            {
                Console.WriteLine("Name: {0}", oCF.Name);
                Console.WriteLine("InternalName: {0}", oCF.InternalName);
    
   ```

   <span data-ttu-id="62bd6-301">O nome interno do campo personalizado é recuperado.</span><span class="sxs-lookup"><span data-stu-id="62bd6-301">The internal name of the custom field is retrieved.</span></span> <span data-ttu-id="62bd6-302">Itens de alto nível 1 e 2 agora estão concluídas.</span><span class="sxs-lookup"><span data-stu-id="62bd6-302">High-level items 1 and 2 are now complete.</span></span>
    
7. <span data-ttu-id="62bd6-303">Volte para o contexto de projeto e recuperar o valor do campo personalizado.</span><span class="sxs-lookup"><span data-stu-id="62bd6-303">Return to the project context and retrieve the value of the custom field.</span></span>
    
   ```cs
    Console.WriteLine("Value: {0}", 
        pubProj.IncludeCustomFields.FieldValues[oCF.InternalName]);
    
   ```

   > [!NOTE]
   > <span data-ttu-id="62bd6-304">O valor do campo personalizado é recuperado usando o nome interno como um índice.</span><span class="sxs-lookup"><span data-stu-id="62bd6-304">The value of the custom field is retrieved using the internal name as an index.</span></span> 
  
<span data-ttu-id="62bd6-305">Saída de três projetos, consistindo em ID do projeto, nome do projeto, nome do campo personalizado, nome interno de campo personalizado e valor do campo personalizado.</span><span class="sxs-lookup"><span data-stu-id="62bd6-305">Output of three projects consisting of project ID, project Name, custom field name, custom field internal name, and custom field value.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="62bd6-306">Confira também</span><span class="sxs-lookup"><span data-stu-id="62bd6-306">See also</span></span>

<span data-ttu-id="62bd6-307">Para documentação e exemplos relacionados ao Project Online e desenvolvimento de aplicativos usando CSOM, consulte o [Portal de desenvolvimento do Project](http://dev.office.com/project.aspx).</span><span class="sxs-lookup"><span data-stu-id="62bd6-307">For documentation and samples related to Project Online and application development using CSOM, see the [Project Development Portal](http://dev.office.com/project.aspx).</span></span>
    

