---
title: Criar, recuperar, atualizar e excluir projetos usando o Project Server JavaScript
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6b690938-05bc-46a3-a40e-30f081403767
description: Obter a instância atual do ProjectContext; recuperar e percorrer a coleção de projetos publicados no servidor. criar, recuperar, fazer check-out e excluir um projeto usando o modelo de objeto do Project Server JavaScript; e alterar propriedades de um projeto.
ms.openlocfilehash: 966c1298d210cb608001e4ce2b390611a75bdb24
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771037"
---
# <a name="create-retrieve-update-and-delete-projects-using-project-server-javascript"></a><span data-ttu-id="429eb-103">Criar, recuperar, atualizar e excluir projetos usando o Project Server JavaScript</span><span class="sxs-lookup"><span data-stu-id="429eb-103">Create, retrieve, update, and delete projects using Project Server JavaScript</span></span>

<span data-ttu-id="429eb-104">Os cenários deste artigo mostram como obter a instância atual do **ProjectContext** ; recuperar e percorrer a coleção de projetos publicados no servidor. criar, recuperar, fazer check-out e excluir um projeto usando o modelo de objeto do Project Server JavaScript; e alterar propriedades de um projeto.</span><span class="sxs-lookup"><span data-stu-id="429eb-104">The scenarios in this article show how to get the current **ProjectContext** instance; retrieve and iterate through the collection of published projects on the server; create, retrieve, check out, and delete a project by using the Project Server JavaScript object model; and change a project's properties.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="429eb-105">Esses cenários definem código personalizado na marcação de uma página de aplicativo do SharePoint, mas não utilizarem o arquivo de code-behind que cria do Visual Studio 2012 para a página.</span><span class="sxs-lookup"><span data-stu-id="429eb-105">These scenarios define custom code in the markup of a SharePoint application page but do not use the code-behind file that Visual Studio 2012 creates for the page.</span></span> 
  
## <a name="prerequisites-for-working-with-project-server-2013-projects-in-the-javascript-object-model"></a><span data-ttu-id="429eb-106">Pré-requisitos para trabalhar com projetos do Project Server 2013 no modelo de objeto JavaScript</span><span class="sxs-lookup"><span data-stu-id="429eb-106">Prerequisites for working with Project Server 2013 projects in the JavaScript object model</span></span>

<span data-ttu-id="429eb-107">Para executar os cenários descritos neste artigo, instale e configure os seguintes produtos:</span><span class="sxs-lookup"><span data-stu-id="429eb-107">To perform the scenarios that are described in this article, you must install and configure the following products:</span></span>
  
- <span data-ttu-id="429eb-108">SharePoint Server 2013</span><span class="sxs-lookup"><span data-stu-id="429eb-108">SharePoint Server 2013</span></span>
- <span data-ttu-id="429eb-109">Project Server 2013</span><span class="sxs-lookup"><span data-stu-id="429eb-109">Project Server 2013</span></span>
- <span data-ttu-id="429eb-110">Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="429eb-110">Visual Studio 2012</span></span>
- <span data-ttu-id="429eb-111">Office Developer Tools para Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="429eb-111">Office Developer Tools for Visual Studio 2012</span></span>
    
<span data-ttu-id="429eb-112">Você também deve ter permissões para implantar a extensão para o SharePoint Server 2013 e contribuir para projetos.</span><span class="sxs-lookup"><span data-stu-id="429eb-112">You must also have permissions to deploy the extension to SharePoint Server 2013 and to contribute to projects.</span></span>
  
> [!NOTE]
> <span data-ttu-id="429eb-113">Estas instruções pressupõem que você estiver desenvolvendo no computador que está executando o Project Server 2013.</span><span class="sxs-lookup"><span data-stu-id="429eb-113">These instructions assume that you are developing on the computer that is running Project Server 2013.</span></span> 
  
## <a name="create-the-visual-studio-solution"></a><span data-ttu-id="429eb-114">Criar a solução do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="429eb-114">Create the Visual Studio solution</span></span>
<span data-ttu-id="429eb-115"><a name="pj15_CRUDProjectsJSOM_Setup"> </a></span><span class="sxs-lookup"><span data-stu-id="429eb-115"></span></span>

<span data-ttu-id="429eb-116">As etapas a seguir criam uma solução do Visual Studio 2012 que contém um projeto do SharePoint e uma página do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="429eb-116">The following steps create a Visual Studio 2012 solution that contains a SharePoint project and an application page.</span></span> <span data-ttu-id="429eb-117">A página contém a lógica para trabalhar com projetos.</span><span class="sxs-lookup"><span data-stu-id="429eb-117">The page contains the logic for working with projects.</span></span>
  
### <a name="to-create-the-sharepoint-project-in-visual-studio"></a><span data-ttu-id="429eb-118">Para criar o projeto do SharePoint no Visual Studio</span><span class="sxs-lookup"><span data-stu-id="429eb-118">To create the SharePoint project in Visual Studio</span></span>

1. <span data-ttu-id="429eb-119">No computador que está executando o Project Server 2013, execute o Visual Studio 2012 como administrador.</span><span class="sxs-lookup"><span data-stu-id="429eb-119">On the computer that is running Project Server 2013, run Visual Studio 2012 as an administrator.</span></span>
    
2. <span data-ttu-id="429eb-120">Na barra de menus, escolha **arquivo**, **novo** **projeto**.</span><span class="sxs-lookup"><span data-stu-id="429eb-120">On the menu bar, choose **File**, **New**, **Project**.</span></span>
    
3. <span data-ttu-id="429eb-121">Na caixa de diálogo **Novo projeto**, escolha o **.NET Framework 4.5** da lista suspensa na parte superior da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="429eb-121">In the **New Project** dialog box, choose **.NET Framework 4.5** from the drop-down list at the top of the dialog box.</span></span> 
    
4. <span data-ttu-id="429eb-122">Na categoria de modelo do **Office/SharePoint** , selecione **Soluções do SharePoint**e, em seguida, escolha o modelo de **Projeto do SharePoint 2013** .</span><span class="sxs-lookup"><span data-stu-id="429eb-122">In the **Office/SharePoint** template category, choose **SharePoint Solutions**, and then choose the **SharePoint 2013 Project** template.</span></span> 
    
5. <span data-ttu-id="429eb-123">Nome do projeto ProjectsJSOM e escolha o botão **Okey** .</span><span class="sxs-lookup"><span data-stu-id="429eb-123">Name the project ProjectsJSOM, and then choose the **OK** button.</span></span> 
    
6. <span data-ttu-id="429eb-124">Na caixa de diálogo **Assistente de personalização do SharePoint**, selecione **implantar como uma solução de farm** e, em seguida, escolha o botão **Concluir**.</span><span class="sxs-lookup"><span data-stu-id="429eb-124">In the **SharePoint Customization Wizard** dialog box, choose **Deploy as a farm solution**, and then choose the **Finish** button.</span></span> 
    
7. <span data-ttu-id="429eb-125">Edite o valor da propriedade **URL do Site** para o projeto **ProjectsJSOM** coincidir com a URL da instância do Project Web App (por exemplo, `http://ServerName/PWA`).</span><span class="sxs-lookup"><span data-stu-id="429eb-125">Edit the value of the **Site URL** property for the **ProjectsJSOM** project to match the URL of the Project Web App instance (for example,  `http://ServerName/PWA`).</span></span>
    
### <a name="to-create-the-application-page-in-visual-studio"></a><span data-ttu-id="429eb-126">Para criar a página de aplicativo no Visual Studio</span><span class="sxs-lookup"><span data-stu-id="429eb-126">To create the application page in Visual Studio</span></span>

1. <span data-ttu-id="429eb-127">No **Solution Explorer**, abra o menu de atalho para o projeto **ProjectsJSOM** e, em seguida, adicione uma lista do SharePoint "Layouts" mapeado a pasta.</span><span class="sxs-lookup"><span data-stu-id="429eb-127">In **Solution Explorer**, open the shortcut menu for the **ProjectsJSOM** project, and then add a SharePoint "Layouts" mapped folder.</span></span> 
    
2. <span data-ttu-id="429eb-128">Na pasta **Layouts** , abra o menu de atalho para a pasta **ProjectsJSOM** e, em seguida, adicione uma nova página de aplicativos do SharePoint denominada ProjectsList.aspx.</span><span class="sxs-lookup"><span data-stu-id="429eb-128">In the **Layouts** folder, open the shortcut menu for the **ProjectsJSOM** folder, and then add a new SharePoint application page named ProjectsList.aspx.</span></span>
    
3. <span data-ttu-id="429eb-129">Abra o menu de atalho para a página **ProjectsList.aspx** e escolha **definida como Item de inicialização**.</span><span class="sxs-lookup"><span data-stu-id="429eb-129">Open the shortcut menu for the **ProjectsList.aspx** page and choose **Set as Startup Item**.</span></span>
    
4. <span data-ttu-id="429eb-130">Na marcação para a página **ProjectsList.aspx** , definem os controles de interface de usuário dentro das marcas de **asp: Content** "Main", da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="429eb-130">In the markup for the **ProjectsList.aspx** page, define user interface controls inside the "Main" **asp:Content** tags, as follows.</span></span> 
    
   ```HTML
    <table width="100%" id="tblProjects">
        <tr id="headerRow">
            <th width="25%" align="left">Name</th>
            <th width="25%" align="left">Description</th>
            <th width="25%" align="left">Start Date</th>
            <th width="25%" align="left">ID</th>
        </tr>
    </table>
    <textarea id="txtGuid" rows="1" cols="35">Paste the project GUID here.</textarea>
    <button id="btnSend" type="button"></button><br />
    <span id="spanMessage" style="color: #FF0000;"></span>
   ```

   > [!NOTE]
   > <span data-ttu-id="429eb-131">Esses controles não podem ser usados em todos os cenários.</span><span class="sxs-lookup"><span data-stu-id="429eb-131">These controls may not be used in every scenario.</span></span> <span data-ttu-id="429eb-132">Por exemplo, o cenário "Criar projetos" não usa os controles da **área de texto** e **botão** .</span><span class="sxs-lookup"><span data-stu-id="429eb-132">For example, the "Create projects" scenario does not use the **textarea** and **button** controls.</span></span> 
  
5. <span data-ttu-id="429eb-133">Após o fechamento **span** marca, adicione uma marca de **SharePoint:ScriptLink** , uma marca de **SharePoint:FormDigest** e marcas de **script** , da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="429eb-133">After the closing **span** tag, add a **SharePoint:ScriptLink** tag, a **SharePoint:FormDigest** tag, and **script** tags, as follows.</span></span> 
    
   ```HTML
    <SharePoint:ScriptLink id="ScriptLink" name="PS.js" runat="server" ondemand="false" localizable="false" loadafterui="true" />
    <SharePoint:FormDigest id="FormDigest" runat="server" />
    <script type="text/javascript">
        // Replace this comment with the code for your scenario.
    </script>
   ```

   <span data-ttu-id="429eb-134">A marca **SharePoint:ScriptLink** referencia o arquivo de PS.js, que define o modelo de objeto JavaScript para o Project Server 2013.</span><span class="sxs-lookup"><span data-stu-id="429eb-134">The **SharePoint:ScriptLink** tag references the PS.js file, which defines the JavaScript object model for Project Server 2013.</span></span> <span data-ttu-id="429eb-135">A marca **SharePoint:FormDigest** gera um resumo da mensagem para a validação de segurança quando exigido pela operações que atualizem o conteúdo do servidor.</span><span class="sxs-lookup"><span data-stu-id="429eb-135">The **SharePoint:FormDigest** tag generates a message digest for security validation when required by operations that update server content.</span></span> 
    
6. <span data-ttu-id="429eb-136">Substitua o comentário de espaço reservado com o código de um dos seguintes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="429eb-136">Replace the placeholder comment with the code from one of the following procedures:</span></span>
    
   - [<span data-ttu-id="429eb-137">Criar projetos do Project Server 2013 usando o modelo de objeto JavaScript</span><span class="sxs-lookup"><span data-stu-id="429eb-137">Create Project Server 2013 projects by using the JavaScript object model</span></span>](#pj15_CRUDProjectsJSOM_CreateProjects)
    
   - [<span data-ttu-id="429eb-138">Atualizar projetos do Project Server 2013 usando o modelo de objeto JavaScript</span><span class="sxs-lookup"><span data-stu-id="429eb-138">Update Project Server 2013 projects by using the JavaScript object model</span></span>](#pj15_CRUDProjectsJSOM_UpdateProjects)
    
   - [<span data-ttu-id="429eb-139">Excluir projetos do Project Server 2013 usando o modelo de objeto JavaScript</span><span class="sxs-lookup"><span data-stu-id="429eb-139">Delete Project Server 2013 projects by using the JavaScript object model</span></span>](#pj15_CRUDProjectsJSOM_DeleteProjects)
    
7. <span data-ttu-id="429eb-140">Para testar a página de aplicativo, na barra de menus, escolha **Depurar**, **Iniciar depuração**.</span><span class="sxs-lookup"><span data-stu-id="429eb-140">To test the application page, on the menu bar, choose **Debug**, **Start Debugging**.</span></span> <span data-ttu-id="429eb-141">Se você for solicitado para modificar o arquivo Web. config, escolha **Okey**.</span><span class="sxs-lookup"><span data-stu-id="429eb-141">If you are prompted to modify the web.config file, choose **OK**.</span></span>
    
## <a name="create-project-server-2013-projects-by-using-the-javascript-object-model"></a><span data-ttu-id="429eb-142">Criar projetos do Project Server 2013 usando o modelo de objeto JavaScript</span><span class="sxs-lookup"><span data-stu-id="429eb-142">Create Project Server 2013 projects by using the JavaScript object model</span></span>
<span data-ttu-id="429eb-143"><a name="pj15_CRUDProjectsJSOM_CreateProjects"> </a></span><span class="sxs-lookup"><span data-stu-id="429eb-143"></span></span>

<span data-ttu-id="429eb-144">O procedimento nesta seção cria projetos usando o modelo de objeto JavaScript.</span><span class="sxs-lookup"><span data-stu-id="429eb-144">The procedure in this section creates projects by using the JavaScript object model.</span></span> <span data-ttu-id="429eb-145">O procedimento inclui as seguintes etapas de alto nível:</span><span class="sxs-lookup"><span data-stu-id="429eb-145">The procedure includes the following high-level steps:</span></span>
  
1. <span data-ttu-id="429eb-146">Obter a instância de **ProjectContext** atual.</span><span class="sxs-lookup"><span data-stu-id="429eb-146">Get the current **ProjectContext** instance.</span></span> 
    
2. <span data-ttu-id="429eb-147">Crie um objeto **ProjectCreationInformation** para especificar propriedades iniciais para o seu projeto.</span><span class="sxs-lookup"><span data-stu-id="429eb-147">Create a **ProjectCreationInformation** object to specify initial properties for your project.</span></span> <span data-ttu-id="429eb-148">Especifique a propriedade necessários **nome** usando a função **ProjectCreationInformation.set_name** .</span><span class="sxs-lookup"><span data-stu-id="429eb-148">Specify the required **name** property by using the **ProjectCreationInformation.set_name** function.</span></span> 
    
3. <span data-ttu-id="429eb-149">Recupere os projetos publicados do servidor usando a função **ProjectContext.get_projects** .</span><span class="sxs-lookup"><span data-stu-id="429eb-149">Retrieve the published projects from the server by using the **ProjectContext.get_projects** function.</span></span> <span data-ttu-id="429eb-150">A função **get_projects** retorna um objeto **ProjectCollection** .</span><span class="sxs-lookup"><span data-stu-id="429eb-150">The **get_projects** function returns a **ProjectCollection** object.</span></span> 
    
4. <span data-ttu-id="429eb-151">Adicione o novo projeto à coleção usando a função **ProjectCollection.add** e passando no objeto **ProjectCreationInformation** .</span><span class="sxs-lookup"><span data-stu-id="429eb-151">Add the new project to the collection by using the **ProjectCollection.add** function and passing in the **ProjectCreationInformation** object.</span></span> 
    
5. <span data-ttu-id="429eb-152">Atualize a coleção usando a função **ProjectCollection.update** e a função **ProjectContext.waitForQueueAsync** .</span><span class="sxs-lookup"><span data-stu-id="429eb-152">Update the collection by using the **ProjectCollection.update** function and the **ProjectContext.waitForQueueAsync** function.</span></span> <span data-ttu-id="429eb-153">A função **Atualizar** retorna um objeto de **QueueJob** que você passa para **waitForQueueAsync**.</span><span class="sxs-lookup"><span data-stu-id="429eb-153">The **update** function returns a **QueueJob** object that you pass to **waitForQueueAsync**.</span></span> <span data-ttu-id="429eb-154">Essa chamada também publica o projeto.</span><span class="sxs-lookup"><span data-stu-id="429eb-154">This call also publishes the project.</span></span>
    
<span data-ttu-id="429eb-155">Cole o seguinte código entre as marcas de **script** que você adicionou no procedimento **para criar a página de aplicativo no Visual Studio** .</span><span class="sxs-lookup"><span data-stu-id="429eb-155">Paste the following code between the **script** tags that you added in the **To create the application page in Visual Studio** procedure.</span></span> 
  
```js
    // Declare a global variable to store the project collection.
    var projects;
    // Ensure that the PS.js file is loaded before your custom code runs.
    SP.SOD.executeOrDelayUntilScriptLoaded(CreateProject, "PS.js");
    // Add a project the projects collection.
    function CreateProject() {
        
        // Initialize the current client context.
        var projContext = PS.ProjectContext.get_current();
        // Initialize a ProjectCreationInformation object and specify properties
        // for the new project.
        // The Name property is required and must be unique.
        var creationInfo = new PS.ProjectCreationInformation();
        creationInfo.set_name("Test Project 1");
        // Specify optional properties for the new project.
        // If not specified, the Start property uses the current date and the
        // EnterpriseProjectTypeId property uses the default EPT.
        creationInfo.set_description("Created through the JSOM.");
        creationInfo.set_start("2013-10-01 09:00:00.000");
        // Get the projects collection.
        projects = projContext.get_projects();
        // Add the new project to the projects collection.
        projects.add(creationInfo);
        // Add a second project to use in the deleting projects procedure.
        creationInfo.set_name("Test Project 2");
        projects.add(creationInfo);
        // Submit the request to update the collection on the server
        var updateJob = projects.update();
        projContext.waitForQueueAsync(updateJob, 10, GetProjects);
    }
    // Get the projects collection.
    function GetProjects(response) {
        // This call demonstrates that you can get the context from the 
        // ProjectCollection object.
        var projContext = projects.get_context();
        // Register the request for information that you want to run on the server.
        // This call includes an optional "Include" parameter to request only the Name, Description,
        // StartDate, and Id properties of the projects in the collection.
        projContext.load(projects, 'Include(Name, Description, StartDate, Id)');
        // Run the request on the server.
        projContext.executeQueryAsync(IterateThroughProjects, QueryFailed);
    }
    // Iterate through the projects collection.
    function IterateThroughProjects(response) {
        // Get the enumerator and iterate through the collection.
        var enumerator = projects.getEnumerator();
        while (enumerator.moveNext()) {
            var project = enumerator.get_current();
            // Create and populate a row with the values for the project's Name, Description,
            // StartDate, and Id properties.
            var row = tblProjects.insertRow();
            row.insertCell().innerText = project.get_name();
            row.insertCell().innerText = project.get_description();
            row.insertCell().innerText = project.get_startDate();
            row.insertCell().innerText = project.get_id();
        }
        // This scenario does not use the textarea or button controls.
        $get("txtGuid").disabled = true;
        $get("btnSend").disabled = true;
    }
    function QueryFailed(sender, args) {
        $get("spanMessage").innerText = 'Request failed: ' + args.get_message();
    }
```

## <a name="update-project-server-2013-projects-by-using-the-javascript-object-model"></a><span data-ttu-id="429eb-156">Atualizar projetos do Project Server 2013 usando o modelo de objeto JavaScript</span><span class="sxs-lookup"><span data-stu-id="429eb-156">Update Project Server 2013 projects by using the JavaScript object model</span></span>
<span data-ttu-id="429eb-157"><a name="pj15_CRUDProjectsJSOM_UpdateProjects"> </a></span><span class="sxs-lookup"><span data-stu-id="429eb-157"></span></span>

<span data-ttu-id="429eb-158">O procedimento nesta seção atualiza a propriedade **startDate** de um projeto usando o modelo de objeto JavaScript.</span><span class="sxs-lookup"><span data-stu-id="429eb-158">The procedure in this section updates the **startDate** property of a project by using the JavaScript object model.</span></span> <span data-ttu-id="429eb-159">O procedimento inclui as seguintes etapas de alto nível:</span><span class="sxs-lookup"><span data-stu-id="429eb-159">The procedure includes the following high-level steps:</span></span> 
  
1. <span data-ttu-id="429eb-160">Obter a instância de **ProjectContext** atual.</span><span class="sxs-lookup"><span data-stu-id="429eb-160">Get the current **ProjectContext** instance.</span></span> 
    
2. <span data-ttu-id="429eb-161">Recupere os projetos publicados do servidor usando a função **ProjectContext.get_projects** .</span><span class="sxs-lookup"><span data-stu-id="429eb-161">Retrieve the published projects from the server by using the **ProjectContext.get_projects** function.</span></span> <span data-ttu-id="429eb-162">A função **get_projects** retorna um objeto **ProjectCollection** .</span><span class="sxs-lookup"><span data-stu-id="429eb-162">The **get_projects** function returns a **ProjectCollection** object.</span></span> 
    
3. <span data-ttu-id="429eb-163">Execute a solicitação no servidor usando a função **ProjectContext.load** e a função **ProjectContext.executeQueryAsync** .</span><span class="sxs-lookup"><span data-stu-id="429eb-163">Run the request on the server by using the **ProjectContext.load** function and the **ProjectContext.executeQueryAsync** function.</span></span> 
    
4. <span data-ttu-id="429eb-164">Recupere um objeto **PublishedProject** usando a função **ProjectContext.getById** .</span><span class="sxs-lookup"><span data-stu-id="429eb-164">Retrieve a **PublishedProject** object by using the **ProjectContext.getById** function.</span></span> 
    
5. <span data-ttu-id="429eb-165">Confira o projeto de destino usando a função **Project.checkOut** .</span><span class="sxs-lookup"><span data-stu-id="429eb-165">Check out the target project by using the **Project.checkOut** function.</span></span> <span data-ttu-id="429eb-166">A função de **check-out** retornará a versão de rascunho do projeto publicado.</span><span class="sxs-lookup"><span data-stu-id="429eb-166">The **checkOut** function returns the draft version of the published project.</span></span> 
    
6. <span data-ttu-id="429eb-167">Altere a data de início do projeto usando a função **DraftProject.set_startDate** .</span><span class="sxs-lookup"><span data-stu-id="429eb-167">Change the project's start date by using the **DraftProject.set_startDate** function.</span></span> 
    
7. <span data-ttu-id="429eb-168">Publica o projeto usando a função **DraftProject.publish** e a função **ProjectContext.waitForQueueAsync** .</span><span class="sxs-lookup"><span data-stu-id="429eb-168">Publish the project by using the **DraftProject.publish** function and the **ProjectContext.waitForQueueAsync** function.</span></span> <span data-ttu-id="429eb-169">A função de **Publicar** retorna um objeto **QueueJob** que você passa para **waitForQueueAsync**.</span><span class="sxs-lookup"><span data-stu-id="429eb-169">The **publish** function returns a **QueueJob** object that you pass to **waitForQueueAsync**.</span></span>
    
<span data-ttu-id="429eb-170">Cole o seguinte código entre as marcas de **script** que você adicionou no procedimento **para criar a página de aplicativo no Visual Studio** .</span><span class="sxs-lookup"><span data-stu-id="429eb-170">Paste the following code between the **script** tags that you added in the **To create the application page in Visual Studio** procedure.</span></span> 
  
```js
    // Declare global variables.
    var projContext;
    var projects;
    // Ensure that the PS.js file is loaded before your custom code runs.
    SP.SOD.executeOrDelayUntilScriptLoaded(GetProjects, "PS.js");
    // Get the projects collection.
    function GetProjects() {
        // Initialize the current client context.
        projContext = PS.ProjectContext.get_current();
        // Get the projects collection.
        projects = projContext.get_projects();
        // Register the request for information that you want to run on the server.
        // This call includes an optional "Include" parameter to request only the Name, Description,
        // StartDate, and Id properties of the projects in the collection.
        projContext.load(projects, 'Include(Name, Description, StartDate, Id)');
        // Run the request on the server.
        projContext.executeQueryAsync(IterateThroughProjects, QueryFailed);
    }
    // Iterate through the projects collection.
    function IterateThroughProjects(response) {
        // Get the enumerator and iterate through the collection.
        var enumerator = projects.getEnumerator();
        while (enumerator.moveNext()) {
            var project = enumerator.get_current();
            // Create and populate a row with the values for the project's Name, Description,
            // StartDate, and Id properties.
            var row = tblProjects.insertRow();
            row.insertCell().innerText = project.get_name();
            row.insertCell().innerText = project.get_description();
            row.insertCell().innerText = project.get_startDate();
            row.insertCell().innerText = project.get_id();
        }
        // Initialize button properties.
        $get("btnSend").onclick = function () { ChangeProject(); };
        $get("btnSend").innerText = "Update";
    }
    // Change the project's start date.
    function ChangeProject() {
        // Get the identifier of the target project.
        var targetGuid = $get("txtGuid").innerText;
        // Get the target project and then check it out. The checkOut function
        // returns the draft version of the project.
        var project = projects.getById(targetGuid);
        var draftProject = project.checkOut();
        // Set the new property value and then publish the project.
        // Specify "true" to also check the project in.
        draftProject.set_startDate("2013-12-31 09:00:00.000");
        var publishJob = draftProject.publish(true);
        // Register the job that you want to run on the server and specify the
        // timeout duration and callback function.
        projContext.waitForQueueAsync(publishJob, 10, QueueJobSent);
    }
    // Print the JobState return code, which gives the status of the queue job.
    function QueueJobSent(response) {
        $get("spanMessage").innerText = 'JobState = ' + response + '. Wait a few seconds, then refresh the page to see your changes.';
    }
    function QueryFailed(sender, args) {
        $get("spanMessage").innerText = 'Request failed: ' + args.get_message();
    }
```

## <a name="delete-project-server-2013-projects-by-using-the-javascript-object-model"></a><span data-ttu-id="429eb-171">Excluir projetos do Project Server 2013 usando o modelo de objeto JavaScript</span><span class="sxs-lookup"><span data-stu-id="429eb-171">Delete Project Server 2013 projects by using the JavaScript object model</span></span>
<span data-ttu-id="429eb-172"><a name="pj15_CRUDProjectsJSOM_DeleteProjects"> </a></span><span class="sxs-lookup"><span data-stu-id="429eb-172"></span></span>

<span data-ttu-id="429eb-173">O procedimento nesta seção exclui um projeto usando o modelo de objeto JavaScript.</span><span class="sxs-lookup"><span data-stu-id="429eb-173">The procedure in this section deletes a project by using the JavaScript object model.</span></span> <span data-ttu-id="429eb-174">O procedimento inclui as seguintes etapas de alto nível:</span><span class="sxs-lookup"><span data-stu-id="429eb-174">The procedure includes the following high-level steps:</span></span>
  
1. <span data-ttu-id="429eb-175">Obter a instância de **ProjectContext** atual.</span><span class="sxs-lookup"><span data-stu-id="429eb-175">Get the current **ProjectContext** instance.</span></span> 
    
2. <span data-ttu-id="429eb-176">Recupere os projetos publicados do servidor usando a função **ProjectContext.get_projects** .</span><span class="sxs-lookup"><span data-stu-id="429eb-176">Retrieve the published projects from the server by using the **ProjectContext.get_projects** function.</span></span> <span data-ttu-id="429eb-177">A função **get_projects** retorna um objeto **ProjectCollection** .</span><span class="sxs-lookup"><span data-stu-id="429eb-177">The **get_projects** function returns a **ProjectCollection** object.</span></span> 
    
3. <span data-ttu-id="429eb-178">Execute a solicitação no servidor usando a função **ProjectContext.load** e a função **ProjectContext.executeQueryAsync** .</span><span class="sxs-lookup"><span data-stu-id="429eb-178">Run the request on the server by using the **ProjectContext.load** function and the **ProjectContext.executeQueryAsync** function.</span></span> 
    
4. <span data-ttu-id="429eb-179">Recupere um objeto **PublishedProject** usando a função **ProjectCollection.getById** .</span><span class="sxs-lookup"><span data-stu-id="429eb-179">Retrieve a **PublishedProject** object by using the **ProjectCollection.getById** function.</span></span> 
    
5. <span data-ttu-id="429eb-180">Exclua o projeto, passando para a função **ProjectCollection.remove** .</span><span class="sxs-lookup"><span data-stu-id="429eb-180">Delete the project by passing it to the **ProjectCollection.remove** function.</span></span> 
    
6. <span data-ttu-id="429eb-181">Atualize a coleção usando a função **ProjectCollection.update** e a função **ProjectContext.waitForQueueAsync** .</span><span class="sxs-lookup"><span data-stu-id="429eb-181">Update the collection by using the **ProjectCollection.update** function and the **ProjectContext.waitForQueueAsync** function.</span></span> <span data-ttu-id="429eb-182">A função **Atualizar** retorna um objeto de **QueueJob** que você passa para **waitForQueueAsync**.</span><span class="sxs-lookup"><span data-stu-id="429eb-182">The **update** function returns a **QueueJob** object that you pass to **waitForQueueAsync**.</span></span>
    
<span data-ttu-id="429eb-183">Cole o seguinte código entre as marcas de **script** que você adicionou no procedimento **para criar a página de aplicativo no Visual Studio** .</span><span class="sxs-lookup"><span data-stu-id="429eb-183">Paste the following code between the **script** tags that you added in the **To create the application page in Visual Studio** procedure.</span></span> 
  
```js
    // Declare global variables.
    var projContext;
    var projects;
    // Ensure that the PS.js file is loaded before your custom code runs.
    SP.SOD.executeOrDelayUntilScriptLoaded(GetProjects, "PS.js");
    // Get the projects collection.
    function GetProjects() {
        // Initialize the current client context.
        projContext = PS.ProjectContext.get_current();
        // Get the projects collection.
        projects = projContext.get_projects();
        // Register the request for information that you want to run on the server.
        // This call includes an optional "Include" parameter to request only the Name, Description,
        // StartDate, and Id properties of the projects in the collection.
        projContext.load(projects, 'Include(Name, Description, StartDate, Id)');
        // Run the request on the server.
        projContext.executeQueryAsync(IterateThroughProjects, QueryFailed);
    }
    // Iterate through the projects collection.
    function IterateThroughProjects(response) {
        // Get the enumerator and iterate through the collection.
        var enumerator = projects.getEnumerator();
        while (enumerator.moveNext()) {
            var project = enumerator.get_current();
            // Create and populate a row with the values for the project's Name, Description,
            // StartDate, and Id properties.
            var row = tblProjects.insertRow();
            row.insertCell().innerText = project.get_name();
            row.insertCell().innerText = project.get_description();
            row.insertCell().innerText = project.get_startDate();
            row.insertCell().innerText = project.get_id();
        }
        // Initialize button properties.
        $get("btnSend").onclick = function () { DeleteProject(); };
        $get("btnSend").innerText = "Delete";
    }
    // Delete the project.
    function DeleteProject() {
        // Get the identifier of the target project.
        var targetGuid = $get("txtGuid").innerText;
        // Get the target project and then remove it from the collection.
        var project = projects.getById(targetGuid);
        projects.remove(project);
        var removeJob = projects.update();
        // Register the job that you want to run on the server and specify the
        // timeout duration and callback function.
        projContext.waitForQueueAsync(removeJob, 10, QueueJobSent);
    }
    // Print the JobState return code, which gives the status of the queue job.
    function QueueJobSent(response) {
        $get("spanMessage").innerText = 'JobState = ' + response + '. Wait a few seconds, then refresh the page to see your changes.';
    }
    function QueryFailed(sender, args) {
        $get("spanMessage").innerText = 'Request failed: ' + args.get_message();
    }
```

<span data-ttu-id="429eb-184"><a name="pj15_CRUDProjectsJSOM_AR"> </a></span><span class="sxs-lookup"><span data-stu-id="429eb-184"></span></span>

## <a name="see-also"></a><span data-ttu-id="429eb-185">Confira também</span><span class="sxs-lookup"><span data-stu-id="429eb-185">See also</span></span>

- [<span data-ttu-id="429eb-186">Tarefas de programação do Project</span><span class="sxs-lookup"><span data-stu-id="429eb-186">Project programming tasks</span></span>](project-programming-tasks.md)
- [<span data-ttu-id="429eb-187">Modelo de objeto do cliente (CSOM) para o Project 2013</span><span class="sxs-lookup"><span data-stu-id="429eb-187">Client-side object model (CSOM) for Project 2013</span></span>](client-side-object-model-csom-for-project-2013.md)
    

