---
title: Introdução ao modelo de objeto do JavaScript do Project Server 2013
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 30dc3194-7480-4e7c-b731-4a171d652ee0
description: No Project Server 2013, o modelo de objeto do JavaScript pode ser usado no Project Online para desenvolvimento móvel e local. Este tópico fornece uma visão geral breve do modelo de objeto JavaScript e descreve como criar uma página de aplicativo que recupera e itera por meio de projetos usando o modelo de objeto do JavaScript.
ms.openlocfilehash: ec8a10e987276807dc4648bd8948b2285f76fd37
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360470"
---
# <a name="getting-started-with-the-project-server-2013-javascript-object-model"></a><span data-ttu-id="09a6e-104">Introdução ao modelo de objeto do JavaScript do Project Server 2013</span><span class="sxs-lookup"><span data-stu-id="09a6e-104">Getting started with the Project Server 2013 JavaScript object model</span></span>

<span data-ttu-id="09a6e-105">No Project Server 2013, o modelo de objeto do JavaScript pode ser usado no Project Online para desenvolvimento móvel e local.</span><span class="sxs-lookup"><span data-stu-id="09a6e-105">In Project Server 2013, the JavaScript object model can be used in Project Online, mobile, and on-premise development.</span></span> <span data-ttu-id="09a6e-106">Este tópico fornece uma visão geral breve do modelo de objeto JavaScript e descreve como criar uma página de aplicativo que recupera e itera por meio de projetos usando o modelo de objeto do JavaScript.</span><span class="sxs-lookup"><span data-stu-id="09a6e-106">This topic provides a brief overview of the JavaScript object model and then describes how to create an application page that retrieves and iterates through projects by using the JavaScript object model.</span></span>
  
## <a name="using-the-project-server-javascript-object-model"></a><span data-ttu-id="09a6e-107">Usar o modelo de objeto do JavaScript do Project Server</span><span class="sxs-lookup"><span data-stu-id="09a6e-107">Using the Project Server JavaScript object model</span></span>
<span data-ttu-id="09a6e-108"><a name="pj15_GetStartedJSOM_UseJSOM"> </a></span><span class="sxs-lookup"><span data-stu-id="09a6e-108"><a name="pj15_GetStartedJSOM_UseJSOM"> </a></span></span>

<span data-ttu-id="09a6e-109">Usar o modelo de objeto do JavaScript é uma ótima maneira de criar um aplicativo executado no lado do cliente (ao invés do código de cliente gerenciado, que precisa ser executado remotamente).</span><span class="sxs-lookup"><span data-stu-id="09a6e-109">Using the JavaScript object model is a great way to create an app that runs client-side (as opposed to managed client code which needs to run remotely).</span></span> <span data-ttu-id="09a6e-110">Os aplicativos podem usar o modelo de objeto do JavaScript para recuperar ou alterar objetos enviando chamadas assíncronas ao servidor.</span><span class="sxs-lookup"><span data-stu-id="09a6e-110">Apps can use the JavaScript object model to retrieve or change objects by sending asynchronous calls to the server.</span></span> <span data-ttu-id="09a6e-111">Os aplicativos que usam o modelo de objeto do JavaScript normalmente são implantados como suplementos do SharePoint, páginas de aplicativo e Web Parts personalizadas.</span><span class="sxs-lookup"><span data-stu-id="09a6e-111">Apps that use the JavaScript object model are typically deployed as custom SharePoint Add-ins, application pages, and Web Parts.</span></span> <span data-ttu-id="09a6e-112">Para saber mais, consulte "Tipos de componentes do SharePoint que podem estar em um aplicativo do SharePoint" em [Sites de host, sites de suplemento e componentes do SharePoint no SharePoint 2013](https://msdn.microsoft.com/library/b791cdf5-8aa2-47fa-bc4c-aee437354759%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="09a6e-112">For more information, see "Types of SharePoint components that can be in an app for SharePoint" in [Host webs, add-in webs, and SharePoint components in SharePoint 2013](https://msdn.microsoft.com/library/b791cdf5-8aa2-47fa-bc4c-aee437354759%28Office.15%29.aspx).</span></span>
  
<span data-ttu-id="09a6e-113">O modelo de objeto do JavaScript implementa a funcionalidade principal do Project Server 2013, mas o modelo de objeto do JavaScript e o modelo de objeto do servidor não têm paridade um para um.</span><span class="sxs-lookup"><span data-stu-id="09a6e-113">The JavaScript object model implements the main functionality of Project Server 2013, but the JavaScript object model and the server object model do not have one-to-one parity.</span></span> <span data-ttu-id="09a6e-114">O ponto de entrada para o modelo de objeto do JavaScript é o objeto **ProjectContext**, que representa o contexto de cliente do Project Server 2013 e fornece acesso ao conteúdo e à funcionalidade do servidor.</span><span class="sxs-lookup"><span data-stu-id="09a6e-114">The entry point to the JavaScript object model is the **ProjectContext** object, which represents the client context for Project Server 2013 and provides access to server content and functionality.</span></span> <span data-ttu-id="09a6e-115">O modelo de objeto do JavaScript do Project Server 2013 é definido no arquivo PS.js, localizado no caminho padrão `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS` no servidor de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="09a6e-115">The JavaScript object model for Project Server 2013 is defined in the PS.js file, which is located in the default path  `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS` on the application server.</span></span> <span data-ttu-id="09a6e-116">O Project Server 2013 também instala o arquivo PS.Debug.js no mesmo local.</span><span class="sxs-lookup"><span data-stu-id="09a6e-116">Project Server 2013 also installs the PS.Debug.js file in the same location.</span></span> <span data-ttu-id="09a6e-117">O PS.Debug.js é uma versão não reduzida do PS.js que fornece informações do IntelliSense.</span><span class="sxs-lookup"><span data-stu-id="09a6e-117">PS.Debug.js is an unminified version of PS.js that provides IntelliSense information.</span></span> 
  
<span data-ttu-id="09a6e-118">O modelo de objeto do JavaScript permite a autenticação de Formulários e todas as solicitações são autenticadas de acordo com o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="09a6e-118">The JavaScript object model allows Forms authentication, and all requests are authenticated as the current user.</span></span> <span data-ttu-id="09a6e-119">Para saber mais sobre segurança e outras considerações ao criar soluções e aplicativos personalizados, consulte [Autenticação, autorização e segurança no SharePoint 2013](https://msdn.microsoft.com/library/8734790c-eb75-4d78-9604-7cc23b33b693%28Office.15%29.aspx), [Aspectos importantes do cenário de desenvolvimento e arquitetura dos suplementos do SharePoint ](https://msdn.microsoft.com/library/ae96572b-8f06-4fd3-854f-fc312f7f2d88%28Office.15%29.aspx) e [Suplementos do SharePoint em comparação a soluções do SharePoint](https://msdn.microsoft.com/library/0e9efadb-aaf2-4c0d-afd5-d6cf25c4e7a8%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="09a6e-119">For more information about security and other considerations for designing custom apps and solutions, see [Authentication, authorization, and security in SharePoint 2013](https://msdn.microsoft.com/library/8734790c-eb75-4d78-9604-7cc23b33b693%28Office.15%29.aspx), [Important aspects of the SharePoint Add-in architecture and development landscape](https://msdn.microsoft.com/library/ae96572b-8f06-4fd3-854f-fc312f7f2d88%28Office.15%29.aspx), and [SharePoint Add-ins compared with SharePoint solutions](https://msdn.microsoft.com/library/0e9efadb-aaf2-4c0d-afd5-d6cf25c4e7a8%28Office.15%29.aspx).</span></span>
  
> [!NOTE]
> <span data-ttu-id="09a6e-120">Para acessar remotamente os dados de um site do SharePoint, o SharePoint 2013 oferece uma biblioteca de domínio cruzado que permite fazer chamadas de domínio cruzado no lado do cliente.</span><span class="sxs-lookup"><span data-stu-id="09a6e-120">To access data from a SharePoint site remotely, SharePoint 2013 provides a cross-domain library that enables you to make client-side cross-domain calls.</span></span> <span data-ttu-id="09a6e-121">Para saber mais, consulte [Acessar dados do SharePoint 2013 a partir de suplementos usando a biblioteca de domínio cruzado](https://msdn.microsoft.com/library/bc37ff5c-1285-40af-98ae-01286696242d%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="09a6e-121">For more information, see [Access SharePoint 2013 data from add-ins using the cross-domain library](https://msdn.microsoft.com/library/bc37ff5c-1285-40af-98ae-01286696242d%28Office.15%29.aspx).</span></span> 
  
<span data-ttu-id="09a6e-122">Muitos conceitos e processos para usar o modelo de objeto do JavaScript para o Project Server 2013 se parecem com diferentes modelos de objetos de cliente relacionados.</span><span class="sxs-lookup"><span data-stu-id="09a6e-122">Many concepts and processes for using the JavaScript object model for Project Server 2013 resemble those in related client object models.</span></span> <span data-ttu-id="09a6e-123">Para saber mais sobre o modelo de objeto de cliente gerenciado do Project Server 2013, consulte **Microsoft.ProjectServer.Client**.</span><span class="sxs-lookup"><span data-stu-id="09a6e-123">For more information about the Project Server 2013 managed client object model, see **Microsoft.ProjectServer.Client**.</span></span> <span data-ttu-id="09a6e-124">Para saber mais sobre o modelo de objeto do JavaScript e o modelo de objeto de cliente gerenciado do SharePoint 2013, consulte [Concluir operações básicas usando código da biblioteca JavaScript no SharePoint 2013](https://msdn.microsoft.com/library/29089af8-dbc0-49b7-a1a0-9e311f49c826%28Office.15%29.aspx), e [Realizar operações básicas usando o código de biblioteca do cliente no SharePoint 2013](https://msdn.microsoft.com/library/5a69c9e3-73bf-4ed5-bc19-182056bdb394%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="09a6e-124">For more information about the SharePoint 2013JavaScript object model and managed client object model, see [Complete basic operations using JavaScript library code in SharePoint 2013](https://msdn.microsoft.com/library/29089af8-dbc0-49b7-a1a0-9e311f49c826%28Office.15%29.aspx) and [Complete basic operations using SharePoint 2013 client library code](https://msdn.microsoft.com/library/5a69c9e3-73bf-4ed5-bc19-182056bdb394%28Office.15%29.aspx).</span></span>
  
## <a name="walkthrough-creating-an-application-page-that-retrieves-and-iterates-through-projects"></a><span data-ttu-id="09a6e-125">Passo a passo: criar uma página de aplicativo que recupera e itera por projetos</span><span class="sxs-lookup"><span data-stu-id="09a6e-125">Walkthrough: Creating an application page that retrieves and iterates through projects</span></span>
<span data-ttu-id="09a6e-126"><a name="pj15_GetStartedJSOM_UseJSOM"> </a></span><span class="sxs-lookup"><span data-stu-id="09a6e-126"><a name="pj15_GetStartedJSOM_UseJSOM"> </a></span></span>

<span data-ttu-id="09a6e-127">Saiba como criar uma página do aplicativo que exibe a ID, o nome e a data de criação de cada projeto publicado em um site.</span><span class="sxs-lookup"><span data-stu-id="09a6e-127">Learn how to create an application page that displays the ID, name, and created date of each published project in a site.</span></span>
  
### <a name="prerequisites-for-creating-an-application-page-that-retrieves-and-iterates-through-projects"></a><span data-ttu-id="09a6e-128">Pré-requisitos para criar uma página de aplicativo que recupera e itera por projetos</span><span class="sxs-lookup"><span data-stu-id="09a6e-128">Prerequisites for creating an application page that retrieves and iterates through projects</span></span>
<span data-ttu-id="09a6e-129"><a name="pj15_GetStartedJSOM_Prereqs"> </a></span><span class="sxs-lookup"><span data-stu-id="09a6e-129"><a name="pj15_GetStartedJSOM_Prereqs"> </a></span></span>

<span data-ttu-id="09a6e-130">Para desenvolver a página de aplicativo descrita neste tópico, instale e configure os seguintes produtos:</span><span class="sxs-lookup"><span data-stu-id="09a6e-130">To develop the application page that is described in this topic, you must install and configure the following products:</span></span>
  
- <span data-ttu-id="09a6e-131">SharePoint Server 2013</span><span class="sxs-lookup"><span data-stu-id="09a6e-131">SharePoint Server 2013</span></span>
- <span data-ttu-id="09a6e-132">Project Server 2013 com pelo menos um projeto publicado</span><span class="sxs-lookup"><span data-stu-id="09a6e-132">Project Server 2013 with at least one published project</span></span>
- <span data-ttu-id="09a6e-133">Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="09a6e-133">Visual Studio 2012</span></span>
- <span data-ttu-id="09a6e-134">Office Developer Tools para Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="09a6e-134">Office Developer Tools for Visual Studio 2012</span></span>
    
<span data-ttu-id="09a6e-135">Você também deve ter permissões para implantar a extensão do SharePoint Server 2013 e para recuperar projetos.</span><span class="sxs-lookup"><span data-stu-id="09a6e-135">You must also have permissions to deploy the extension to SharePoint Server 2013 and to retrieve projects.</span></span>
  
> [!NOTE]
> <span data-ttu-id="09a6e-136">Essas instruções pressupõem que você esteja desenvolvendo em um computador que executa o Project Server 2013.</span><span class="sxs-lookup"><span data-stu-id="09a6e-136">These instructions assume that you are developing on the computer that is running Project Server 2013.</span></span> 
  
### <a name="creating-the-application-page-in-visual-studio-2012"></a><span data-ttu-id="09a6e-137">Criar a página de aplicativo no Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="09a6e-137">Creating the application page in Visual Studio 2012</span></span>
<span data-ttu-id="09a6e-138"><a name="pj15_GetStartedJSOM_CreateVS"> </a></span><span class="sxs-lookup"><span data-stu-id="09a6e-138"><a name="pj15_GetStartedJSOM_CreateVS"> </a></span></span>

<span data-ttu-id="09a6e-139">As etapas a seguir criam um projeto do SharePoint e uma página de aplicativo que contém uma tabela e um rótulo.</span><span class="sxs-lookup"><span data-stu-id="09a6e-139">The following steps create a SharePoint project and an application page that contains a table and label.</span></span> <span data-ttu-id="09a6e-140">A tabela exibe informações sobre projetos e o rótulo exibe mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="09a6e-140">The table displays information about the projects and the label displays error messages.</span></span>
  
1. <span data-ttu-id="09a6e-141">No computador que executa o Project Server 2013, execute o Visual Studio 2012 como administrador.</span><span class="sxs-lookup"><span data-stu-id="09a6e-141">On the computer that is running Project Server 2013, run Visual Studio 2012 as an administrator.</span></span>
    
2. <span data-ttu-id="09a6e-142">Crie um projeto vazio do SharePoint 2013 da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="09a6e-142">Create an empty SharePoint 2013 project, as follows:</span></span>
    
    1. <span data-ttu-id="09a6e-143">Na caixa de diálogo **Novo Projeto**, escolha **.NET Framework 4.5** na lista suspensa na parte superior da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="09a6e-143">In the **New Project** dialog box, choose **.NET Framework 4.5** from the drop-down list at the top of the dialog box.</span></span> 
        
    2. <span data-ttu-id="09a6e-144">Na lista de categorias de modelos, escolha a categoria **Office SharePoint** e o modelo **Projeto do SharePoint 2013**.</span><span class="sxs-lookup"><span data-stu-id="09a6e-144">In the list of template categories, choose the **Office SharePoint** category, and then choose the **SharePoint 2013 Project** template.</span></span> 
        
    3. <span data-ttu-id="09a6e-145">Nomeie o projeto como GetProjectsJSOM e escolha o botão **OK**.</span><span class="sxs-lookup"><span data-stu-id="09a6e-145">Name the project GetProjectsJSOM, and then choose the **OK** button.</span></span> 
        
    4. <span data-ttu-id="09a6e-146">Na caixa de diálogo **Assistente de Personalização do SharePoint**, selecione **Implantar como uma solução de farm** e, em seguida, escolha o botão **OK**.</span><span class="sxs-lookup"><span data-stu-id="09a6e-146">In the **SharePoint Customization Wizard** dialog box, choose **Deploy as a farm solution**, and then choose the **OK** button.</span></span> 
    
3. <span data-ttu-id="09a6e-147">No Gerenciador de Soluções, edite o valor da propriedade **URL do Site** para que o projeto **ProjectsJSOM** corresponda à URL da instância do Project Web App (por exemplo, `https://ServerName/PWA`).</span><span class="sxs-lookup"><span data-stu-id="09a6e-147">In Solution Explorer, edit the value of the **Site URL** property for the **ProjectsJSOM** project to match the URL of the Project Web App instance (for example,  `https://ServerName/PWA`).</span></span>
    
4. <span data-ttu-id="09a6e-148">Abra o menu de atalho do projeto **GetProjectsJSOM** e, em seguida, adicione a pasta mapeada "Layouts" do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="09a6e-148">Open the shortcut menu for the **GetProjectsJSOM** project, and then add a SharePoint "Layouts" mapped folder.</span></span> 
    
5. <span data-ttu-id="09a6e-149">Na pasta **Layouts**, abra o menu de atalho da pasta **GetProjectsJSOM** e, em seguida, adicione uma nova página de aplicativo do SharePoint denominada ProjectsList.aspx.</span><span class="sxs-lookup"><span data-stu-id="09a6e-149">In the **Layouts** folder, open the shortcut menu for the **GetProjectsJSOM** folder, and then add a new SharePoint application page named ProjectsList.aspx.</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="09a6e-150">Este exemplo não usa o arquivo code-behind que o Visual Studio 2012 cria para a página do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="09a6e-150">This example does not use the code-behind file that Visual Studio 2012 creates for the application page.</span></span> 
  
6. <span data-ttu-id="09a6e-151">Abra o menu de atalho da página **ProjectsList.aspx** e escolha **Definir como item de inicialização**.</span><span class="sxs-lookup"><span data-stu-id="09a6e-151">Open the shortcut menu for the **ProjectsList.aspx** page and choose **Set as Startup Item**.</span></span>
    
7. <span data-ttu-id="09a6e-152">Na marcação da página **ProjectsList.aspx**, defina uma tabela e um espaço reservado de mensagem dentro das marcas "Main" **asp:Content**, como a seguir.</span><span class="sxs-lookup"><span data-stu-id="09a6e-152">In the markup for the **ProjectsList.aspx** page, define a table and a message placeholder inside the "Main" **asp:Content** tags, as follows.</span></span> 
    
    ```HTML
    <table width="100%" id="tblProjects">
        <tr id="headerRow">
            <th width="25%" align="left">Project name</th>
            <th width="25%" align="left">Created date</th>
            <th width="50%" align="left">Project ID</th>
        </tr>
    </table>
    <div id="divMessage">
        <br/>
        <span id="spanMessage" style="color: #FF0000;"></span>
    </div>
    ```

### <a name="retrieving-the-projects-collection"></a><span data-ttu-id="09a6e-153">Recuperar a coleção de projetos</span><span class="sxs-lookup"><span data-stu-id="09a6e-153">Retrieving the projects collection</span></span>
<span data-ttu-id="09a6e-154"><a name="pj15_GetStartedJSOM_RetrieveProjs"> </a></span><span class="sxs-lookup"><span data-stu-id="09a6e-154"><a name="pj15_GetStartedJSOM_RetrieveProjs"> </a></span></span>

<span data-ttu-id="09a6e-155">As etapas a seguir recuperam e inicializam a coleção de projetos.</span><span class="sxs-lookup"><span data-stu-id="09a6e-155">The following steps retrieve and initialize the projects collection.</span></span>
  
1. <span data-ttu-id="09a6e-156">Após o encerramento da marca **div**, adicione uma marca **SharePoint:ScriptLink** que faz referência ao arquivo PS.js, como a seguir.</span><span class="sxs-lookup"><span data-stu-id="09a6e-156">After the closing **div** tag, add a **SharePoint:ScriptLink** tag that references the PS.js file, as follows.</span></span> 
    
   ```HTML
    <SharePoint:ScriptLink name="PS.js" runat="server" ondemand="false" localizable="false" loadafterui="true" />
   ```

2. <span data-ttu-id="09a6e-157">Abaixo da marca **SharePoint:ScriptLink**, adicione a marca **script**, como a seguir.</span><span class="sxs-lookup"><span data-stu-id="09a6e-157">Below the **SharePoint:ScriptLink** tag, add **script** tags, as follows.</span></span> 
    
   ```HTML
    <script type="text/javascript">
        // Paste the remaining code snippets here, in the order that they are presented.
    </script>
   ```

3. <span data-ttu-id="09a6e-158">Informe uma variável global para armazenar a coleção de projetos, da maneira a seguir.</span><span class="sxs-lookup"><span data-stu-id="09a6e-158">Declare a global variable to store the projects collection, as follows.</span></span>
    
   ```js
   var projects;
   ```

4. <span data-ttu-id="09a6e-159">Chame o método **SP.SOD.executeOrDelayUntilScriptLoaded** para garantir que o arquivo PS.js esteja carregado antes de executar o código personalizado.</span><span class="sxs-lookup"><span data-stu-id="09a6e-159">Call the **SP.SOD.executeOrDelayUntilScriptLoaded** method to ensure that the PS.js file is loaded before your custom code runs.</span></span> 
    
   ```js
   SP.SOD.executeOrDelayUntilScriptLoaded(GetProjects, "PS.js");
   ```

5. <span data-ttu-id="09a6e-160">Adicione uma função que conecta-se ao contexto atual e recupera a coleção de projetos, como a seguir.</span><span class="sxs-lookup"><span data-stu-id="09a6e-160">Add a function that connects to the current context and retrieves the projects collection, as follows.</span></span>
    
   ```js
    function GetProjects() {
        // Initialize the current client context.
        var projContext = PS.ProjectContext.get_current();
        // Get the projects collection.
        projects = projContext.get_projects();
        // Register the request that you want to run on the server.
        // This call includes an optional "Include" parameter to request only the
        // Name, CreatedDate, and Id properties of the projects in the collection.
        projContext.load(projects, 'Include(Name, CreatedDate, Id)');
        // Run the request on the server.
        projContext.executeQueryAsync(onQuerySucceeded, onQueryFailed);
    }
   ```

   <span data-ttu-id="09a6e-161">Alguns objetos de clientes, que você recupera pelo contexto, não contêm dados até serem iniciados; ou seja, não é possível acessar valores de propriedades do objeto até que o objeto seja iniciado.</span><span class="sxs-lookup"><span data-stu-id="09a6e-161">Some client objects that you retrieve through the context contain no data until they are initialized; that is, you cannot access the property values of the object until the object is initialized.</span></span> <span data-ttu-id="09a6e-162">Além disso, para as propriedades do tipo **ValueObject**, é necessário solicitar explicitamente a propriedade antes de poder acessar o valor.</span><span class="sxs-lookup"><span data-stu-id="09a6e-162">Moreover, for properties of type **ValueObject**, you must explicitly request the property before you can access its value.</span></span> <span data-ttu-id="09a6e-163">(Se você tentar acessar uma propriedade antes que seja iniciada, verá a exceção **PropertyOrFieldNotInitializedException**.)</span><span class="sxs-lookup"><span data-stu-id="09a6e-163">(If you try to access a property before it is initialized, you receive a **PropertyOrFieldNotInitializedException** exception.)</span></span> 
    
   <span data-ttu-id="09a6e-164">Para iniciar um objeto, chame o método **load** (ou **loadQuery**) e, depois, o método **executeQueryAsync**.</span><span class="sxs-lookup"><span data-stu-id="09a6e-164">To initialize an object, you call the **load** method (or the **loadQuery** method) and then the **executeQueryAsync** method.</span></span> 
    
   - <span data-ttu-id="09a6e-165">Chamar as funções **load** ou **loadQuery** registra uma solicitação de que você deseja executar no servidor.</span><span class="sxs-lookup"><span data-stu-id="09a6e-165">Calling the **load** function or the **loadQuery** function registers a request that you want to run on the server.</span></span> <span data-ttu-id="09a6e-166">Passe um parâmetro que representa o objeto que você deseja recuperar.</span><span class="sxs-lookup"><span data-stu-id="09a6e-166">You pass in a parameter that represents the object that you want to retrieve.</span></span> <span data-ttu-id="09a6e-167">Se você estiver trabalhando com uma propriedade **ValueObject**, então também deve solicitar a propriedade do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="09a6e-167">If you are working with a **ValueObject** property, then you also request the property in the parameter.</span></span> 
    
   - <span data-ttu-id="09a6e-168">Chamar a função **executeQueryAsync** envia a solicitação de consulta ao servidor de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="09a6e-168">Calling the **executeQueryAsync** function sends the query request to the server asynchronously.</span></span> <span data-ttu-id="09a6e-169">Passe uma função de retorno de chamada bem-sucedida e outra com falha a fim de analisar quando a resposta do servidor é recebida.</span><span class="sxs-lookup"><span data-stu-id="09a6e-169">You pass in a success callback function and a failure callback function to invoke when the server response is received.</span></span> 
    
   <span data-ttu-id="09a6e-170">Para reduzir o tráfego de rede, solicite somente as propriedades que você deseja usar chamando a função **load**.</span><span class="sxs-lookup"><span data-stu-id="09a6e-170">To reduce network traffic, request only the properties that you want to work with when you call the **load** function.</span></span> <span data-ttu-id="09a6e-171">Além disso, se estiver trabalhando com vários objetos, agrupe as várias chamadas para a função **load** antes de chamar a função **executeQueryAsync** quando possível.</span><span class="sxs-lookup"><span data-stu-id="09a6e-171">In addition, if you are working with multiple objects, group multiple calls to the **load** function before you call the **executeQueryAsync** function when it is possible.</span></span> 
    
### <a name="iterating-through-the-projects-collection"></a><span data-ttu-id="09a6e-172">Iterar pela coleção de projetos</span><span class="sxs-lookup"><span data-stu-id="09a6e-172">Iterating through the projects collection</span></span>
<span data-ttu-id="09a6e-173"><a name="pj15_GetStartedJSOM_IterateProjs"> </a></span><span class="sxs-lookup"><span data-stu-id="09a6e-173"><a name="pj15_GetStartedJSOM_IterateProjs"> </a></span></span>

<span data-ttu-id="09a6e-174">As etapas a seguir iteram pela coleção de projetos (se a chamada do servidor for bem-sucedida) ou renderizam uma mensagem de erro (se a chamada falhar).</span><span class="sxs-lookup"><span data-stu-id="09a6e-174">The following steps iterate through the projects collection (if the server call is successful) or render an error message (if the call fails).</span></span>
  
1. <span data-ttu-id="09a6e-175">Adicione uma função de retorno de chamada bem-sucedida que itera pela coleção de projetos, como a seguir.</span><span class="sxs-lookup"><span data-stu-id="09a6e-175">Add a success callback function that iterates through the projects collection, as follows.</span></span>
    
   ```js
    function onQuerySucceeded(sender, args) {
        // Get the enumerator and iterate through the collection.
        var projectEnumerator = projects.getEnumerator();
        while (projectEnumerator.moveNext()) {
            var project = projectEnumerator.get_current();
            // Create the row for the project's information.
            var row = tblProjects.insertRow();
            // Insert cells for the Id, Name, and CreatedDate properties.
            row.insertCell().innerText = project.get_name();
            row.insertCell().innerText = project.get_createdDate();
            row.insertCell().innerText = project.get_id();
        }
    }
   ```

2. <span data-ttu-id="09a6e-176">Adicione uma função de retorno de chamada com falha que processa uma mensagem de erro, como a seguir.</span><span class="sxs-lookup"><span data-stu-id="09a6e-176">Add a failure callback function that renders an error message, as follows.</span></span>
    
    ```js
    function onQueryFailed(sender, args) {
        $get("spanMessage").innerText = 'Request failed: ' + args.get_message();
    }
    ```

3. <span data-ttu-id="09a6e-177">Para testar a página de aplicativo, na barra de menus, escolha **Depurar**, **Iniciar Depuração**.</span><span class="sxs-lookup"><span data-stu-id="09a6e-177">To test the application page, on the menu bar, choose **Debug**, **Start Debugging**.</span></span> <span data-ttu-id="09a6e-178">Se for solicitado a modificar as configurações, escolha **OK**.</span><span class="sxs-lookup"><span data-stu-id="09a6e-178">If you are prompted to modify the web.config file, choose **OK**.</span></span>

<span data-ttu-id="09a6e-179"><a name="pj15_GetStartedJSOM_CompleteExample"> </a></span><span class="sxs-lookup"><span data-stu-id="09a6e-179"><a name="pj15_GetStartedJSOM_CompleteExample"> </a></span></span>

## <a name="complete-code-example"></a><span data-ttu-id="09a6e-180">Exemplo de código completo</span><span class="sxs-lookup"><span data-stu-id="09a6e-180">Complete code example</span></span>

<span data-ttu-id="09a6e-181">A seguir apresentamos o código completo do arquivo ProjectsList.aspx.</span><span class="sxs-lookup"><span data-stu-id="09a6e-181">Following is the complete code from the ProjectsList.aspx file.</span></span>
  
```js
<%@ Assembly Name="$SharePoint.Project.AssemblyFullName$" %>
<%@ Import Namespace="Microsoft.SharePoint.ApplicationPages" %>
<%@ Register Tagprefix="SharePoint" Namespace="Microsoft.SharePoint.WebControls" Assembly="Microsoft.SharePoint, Version=15.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
<%@ Register Tagprefix="Utilities" Namespace="Microsoft.SharePoint.Utilities" Assembly="Microsoft.SharePoint, Version=15.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
<%@ Register Tagprefix="asp" Namespace="System.Web.UI" Assembly="System.Web.Extensions, Version=3.5.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35" %>
<%@ Import Namespace="Microsoft.SharePoint" %>
<%@ Assembly Name="Microsoft.Web.CommandUI, Version=15.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="ProjectsList.aspx.cs" Inherits="GetProjectsJSOM.Layouts.GetProjectsJSOM.ProjectsList" DynamicMasterPageFile="~masterurl/default.master" %>
<asp:Content ID="PageHead" ContentPlaceHolderID="PlaceHolderAdditionalPageHead" runat="server">
</asp:Content>
<asp:Content ID="Main" ContentPlaceHolderID="PlaceHolderMain" runat="server">
    <table width="100%" id="tblProjects">
    <tr id="headerRow">
        <th width="25%" align="left">Project name</th>
        <th width="25%" align="left">Created date</th>
        <th width="50%" align="left">Project ID</th>
    </tr>
</table>
<div id="divMessage">
    <br/>
    <span id="spanMessage" style="color: #FF0000;"></span>
</div>
<SharePoint:ScriptLink name="PS.js" runat="server" ondemand="false" localizable="false" loadafterui="true" />
<script type="text/javascript">
    // Declare a variable to store the published projects that exist
    // in the current context.
    var projects;
    // Ensure that the PS.js file is loaded before your custom code runs.
    SP.SOD.executeOrDelayUntilScriptLoaded(GetProjects, "PS.js");
    // Get the projects collection.
    function GetProjects() {
        // Initialize the current client context.
        var projContext = PS.ProjectContext.get_current();
        // Get the projects collection.
        projects = projContext.get_projects();
        // Register the request that you want to run on the server.
        // This call includes an optional "Include" parameter to request only the
        // Name, CreatedDate, and Id properties of the projects in the collection.
        projContext.load(projects, 'Include(Name, CreatedDate, Id)');
        // Run the request on the server.
        projContext.executeQueryAsync(onQuerySucceeded, onQueryFailed);
    }
    function onQuerySucceeded(sender, args) {
        // Get the enumerator and iterate through the collection.
        var projectEnumerator = projects.getEnumerator();
        while (projectEnumerator.moveNext()) {
            var project = projectEnumerator.get_current();
            // Create the row for the project's information.
            var row = tblProjects.insertRow();
            // Insert cells for the Id, Name, and CreatedDate properties.
            row.insertCell().innerText = project.get_name();
            row.insertCell().innerText = project.get_createdDate();
            row.insertCell().innerText = project.get_id();
        }
    }
    function onQueryFailed(sender, args) {
        $get("spanMessage").innerText = 'Request failed: ' + args.get_message();
    }
</script>
</asp:Content>
<asp:Content ID="PageTitle" ContentPlaceHolderID="PlaceHolderPageTitle" runat="server">
Application Page
</asp:Content>
<asp:Content ID="PageTitleInTitleArea" ContentPlaceHolderID="PlaceHolderPageTitleInTitleArea" runat="server" >
My Application Page
</asp:Content>

```

<span data-ttu-id="09a6e-182"><a name="pj15_GetStartedJSOM_AR"> </a></span><span class="sxs-lookup"><span data-stu-id="09a6e-182"><a name="pj15_GetStartedJSOM_AR"> </a></span></span>

## <a name="see-also"></a><span data-ttu-id="09a6e-183">Confira também</span><span class="sxs-lookup"><span data-stu-id="09a6e-183">See also</span></span>

- [<span data-ttu-id="09a6e-184">Criar, recuperar, atualizar e excluir projetos usando o modelo de objeto do JavaScript do Project Server </span><span class="sxs-lookup"><span data-stu-id="09a6e-184">Create, retrieve, update, and delete projects by using the Project Server JavaScript object model</span></span>](create-retrieve-update-delete-projects-using-project-server-javascript.md)  
- [<span data-ttu-id="09a6e-185">Modelo de objeto no lado do cliente (CSOM) para o Project 2013</span><span class="sxs-lookup"><span data-stu-id="09a6e-185">Client-side object model (CSOM) for Project 2013</span></span>](client-side-object-model-csom-for-project-2013.md)
- [<span data-ttu-id="09a6e-186">Introdução ao Project Server CSOM e .NET</span><span class="sxs-lookup"><span data-stu-id="09a6e-186">Getting started with the Project Server CSOM and .NET</span></span>](getting-started-with-the-project-server-csom-and-net.md)
    

