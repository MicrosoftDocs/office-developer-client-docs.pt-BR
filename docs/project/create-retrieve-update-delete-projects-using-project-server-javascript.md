---
title: Criar, recuperar, atualizar e excluir projetos usando o Project Server JavaScript
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6b690938-05bc-46a3-a40e-30f081403767
description: Obter a instância ProjectContext atual; recuperar e iterar sobre o conjunto de projetos publicados no servidor. criar, recuperar, conferir e excluir um projeto usando o modelo de objeto do JavaScript do Project Server; e alterar as propriedades do projeto.
ms.openlocfilehash: 10dac7edfa3e84cebfd0585bc8c4bff1ea22ea44
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382908"
---
# <a name="create-retrieve-update-and-delete-projects-using-project-server-javascript"></a><span data-ttu-id="86619-103">Criar, recuperar, atualizar e excluir projetos usando o Project Server JavaScript</span><span class="sxs-lookup"><span data-stu-id="86619-103">Create, retrieve, update, and delete projects using Project Server JavaScript</span></span>

<span data-ttu-id="86619-104">Cenários neste artigo mostram como obter a instância **ProjectContext** atual; recuperar e iterar sobre o conjunto de projetos publicados no servidor. criar, recuperar, conferir e excluir um projeto usando o modelo de objeto do JavaScript do Project Server; e alterar as propriedades do projeto.</span><span class="sxs-lookup"><span data-stu-id="86619-104">The scenarios in this article show how to get the current **ProjectContext** instance; retrieve and iterate through the collection of published projects on the server; create, retrieve, check out, and delete a project by using the Project Server JavaScript object model; and change a project's properties.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="86619-105">Esses cenários definem o código personalizado na marcação de uma página do aplicativo do SharePoint, mas não usam o arquivo de code-behind que o Visual Studio 2012 cria na página.</span><span class="sxs-lookup"><span data-stu-id="86619-105">These scenarios define custom code in the markup of a SharePoint application page but do not use the code-behind file that Visual Studio 2012 creates for the page.</span></span> 
  
## <a name="prerequisites-for-working-with-project-server-2013-projects-in-the-javascript-object-model"></a><span data-ttu-id="86619-106">Pré-requisitos para trabalhar com projetos do Project Server 2013 no modelo de objeto do JavaScript</span><span class="sxs-lookup"><span data-stu-id="86619-106">Prerequisites for working with Project Server 2013 projects in the JavaScript object model</span></span>

<span data-ttu-id="86619-107">Para executar os cenários descritos neste artigo, instale e configure os seguintes produtos:</span><span class="sxs-lookup"><span data-stu-id="86619-107">To perform the scenarios that are described in this article, you must install and configure the following products:</span></span>
  
- <span data-ttu-id="86619-108">SharePoint Server 2013</span><span class="sxs-lookup"><span data-stu-id="86619-108">SharePoint Server 2013</span></span>
- <span data-ttu-id="86619-109">Project Server 2013</span><span class="sxs-lookup"><span data-stu-id="86619-109">Project Server 2013</span></span>
- <span data-ttu-id="86619-110">Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="86619-110">Visual Studio 2012</span></span>
- <span data-ttu-id="86619-111">Office Developer Tools para Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="86619-111">Office Developer Tools for Visual Studio 2012</span></span>
    
<span data-ttu-id="86619-112">Você também deve ter permissões para implantar a extensão do SharePoint Server 2013 e para colaborar com projetos.</span><span class="sxs-lookup"><span data-stu-id="86619-112">You must also have permissions to deploy the extension to SharePoint Server 2013 and to contribute to projects.</span></span>
  
> [!NOTE]
> <span data-ttu-id="86619-113">Essas instruções pressupõem que você esteja desenvolvendo em um computador que executa o Project Server 2013.</span><span class="sxs-lookup"><span data-stu-id="86619-113">These instructions assume that you are developing on the computer that is running Project Server 2013.</span></span> 
  
## <a name="create-the-visual-studio-solution"></a><span data-ttu-id="86619-114">Criar a solução do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="86619-114">Create the Visual Studio solution</span></span>
<span data-ttu-id="86619-115"><a name="pj15_CRUDProjectsJSOM_Setup"> </a></span><span class="sxs-lookup"><span data-stu-id="86619-115"></span></span>

<span data-ttu-id="86619-116">As etapas a seguir criam uma solução do Visual Studio 2012 com um projeto do SharePoint e uma página de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="86619-116">The following steps create a Visual Studio 2012 solution that contains a SharePoint project and an application page.</span></span> <span data-ttu-id="86619-117">A página contém a lógica para trabalhar com projetos.</span><span class="sxs-lookup"><span data-stu-id="86619-117">The page contains the logic for working with projects.</span></span>
  
### <a name="to-create-the-sharepoint-project-in-visual-studio"></a><span data-ttu-id="86619-118">Para criar um projeto do SharePoint no Visual Studio</span><span class="sxs-lookup"><span data-stu-id="86619-118">To configure the SharePoint Add-in project in Visual Studio</span></span>

1. <span data-ttu-id="86619-119">No computador que executa o Project Server 2013, execute o Visual Studio 2012 como administrador.</span><span class="sxs-lookup"><span data-stu-id="86619-119">On the computer that is running Project Server 2013, run Visual Studio 2012 as an administrator.</span></span>
    
2. <span data-ttu-id="86619-120">Na barra de menus, selecione **Arquivo**, **Novo**, **Projeto**.</span><span class="sxs-lookup"><span data-stu-id="86619-120">On the menu bar, choose **File**, **New**, **Project**.</span></span>
    
3. <span data-ttu-id="86619-121">Na caixa de diálogo **Novo Projeto**, escolha **.NET Framework 4.5** na lista suspensa na parte superior da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="86619-121">In the **New Project** dialog box, choose **.NET Framework 4.5** from the drop-down list at the top of the dialog box.</span></span> 
    
4. <span data-ttu-id="86619-122">Na categoria de modelos **Office/SharePoint**, escolha **Soluções do SharePoint** e, em seguida, escolha o modelo **Projeto do SharePoint 2013**.</span><span class="sxs-lookup"><span data-stu-id="86619-122">In the Templates list, expand Office/SharePoint, choose the SharePoint Solutions category, and then choose the SharePoint 2013 Project template.</span></span> 
    
5. <span data-ttu-id="86619-123">Nomeie o projeto como ProjectsJSOM e depois selecione o botão **OK**.</span><span class="sxs-lookup"><span data-stu-id="86619-123">Name the project HelloWorld, and then choose the OK button.</span></span> 
    
6. <span data-ttu-id="86619-124">Na caixa de diálogo **Assistente de Personalização do SharePoint**, selecione **Implantar como uma solução de farm** e, em seguida, escolha o botão **Concluir**.</span><span class="sxs-lookup"><span data-stu-id="86619-124">In the **SharePoint Customization Wizard** dialog box, choose **Deploy as a farm solution**, and then choose the **Finish** button.</span></span> 
    
7. <span data-ttu-id="86619-125">Edite o valor da propriedade **URL do Site** para que o projeto **ProjectsJSOM** corresponda à URL da instância do Project Web App (por exemplo, `https://ServerName/PWA`).</span><span class="sxs-lookup"><span data-stu-id="86619-125">Edit the value of the **Site URL** property for the **ProjectsJSOM** project to match the URL of the Project Web App instance (for example,  `https://ServerName/PWA`).</span></span>
    
### <a name="to-create-the-application-page-in-visual-studio"></a><span data-ttu-id="86619-126">Criar a página de aplicativo em Visual Studio</span><span class="sxs-lookup"><span data-stu-id="86619-126">Create the application page in Visual Studio 2012</span></span>

1. <span data-ttu-id="86619-127">No **Solution Explorer**, abra o menu de atalho do projeto **ProjectsJSOM** e, em seguida, adicione uma pasta mapeada "Layouts" do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="86619-127">In **Solution Explorer**, open the shortcut menu for the **FollowPeopleJSOM** project, and then add a SharePoint "Layouts" mapped folder.</span></span> 
    
2. <span data-ttu-id="86619-128">Na pasta **Layouts**, abra o menu de atalho da pasta **ProjectsJSOM** e, em seguida, adicione uma nova página de aplicativo do SharePoint denominada ProjectList.aspx.</span><span class="sxs-lookup"><span data-stu-id="86619-128">In the **Layouts** folder, open the shortcut menu for the **FollowPeopleJSOM** folder, and then add a new SharePoint application page namedFollowPeople.aspx.</span></span>
    
3. <span data-ttu-id="86619-129">Abra o menu de atalho da página **ProjectsList.aspx** e escolha **Set as Startup Item**.</span><span class="sxs-lookup"><span data-stu-id="86619-129">Open the shortcut menu for the FollowPeople.aspx page, and then choose Set as Startup Item.</span></span>
    
4. <span data-ttu-id="86619-130">Na marcação da página**ProjectsList.aspx**, defina os controles de interface de usuário dentro das marcas "Main" **asp:Content**, da forma seguinte.</span><span class="sxs-lookup"><span data-stu-id="86619-130">In the markup for the SocialFeed.aspx page, define controls inside the "Main" asp:Content tags, as shown in the following code.</span></span> 
    
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
   > <span data-ttu-id="86619-131">Esses controles não podem ser usados em todos os cenários.</span><span class="sxs-lookup"><span data-stu-id="86619-131">These controls may not be used in every scenario.</span></span> <span data-ttu-id="86619-132">Por exemplo, o cenário "Criar projetos" não usa os controles de **área de texto** e **botão**.</span><span class="sxs-lookup"><span data-stu-id="86619-132">For example, the "Create projects" scenario does not use the **textarea** and **button** controls.</span></span> 
  
5. <span data-ttu-id="86619-133">Depois de fechar a marca **span**, adicione uma marca **SharePoint:ScriptLink**, uma marca **SharePoint:FormDigest** e marcas de **script**, da forma seguinte.</span><span class="sxs-lookup"><span data-stu-id="86619-133">After the closing **span** tag, add a **SharePoint:ScriptLink** tag, a **SharePoint:FormDigest** tag, and **script** tags, as follows.</span></span> 
    
   ```HTML
    <SharePoint:ScriptLink id="ScriptLink" name="PS.js" runat="server" ondemand="false" localizable="false" loadafterui="true" />
    <SharePoint:FormDigest id="FormDigest" runat="server" />
    <script type="text/javascript">
        // Replace this comment with the code for your scenario.
    </script>
   ```

   <span data-ttu-id="86619-134">A marca**SharePoint:ScriptLink** faz referência ao arquivo PS.js, que define o modelo de objeto do JavaScript do Project Server 2013.</span><span class="sxs-lookup"><span data-stu-id="86619-134">The **SharePoint:ScriptLink** tag references the PS.js file, which defines the JavaScript object model for Project Server 2013.</span></span> <span data-ttu-id="86619-135">A marca **SharePoint:FormDigest** gerará uma compilação de mensagem para validação de segurança, quando isso for solicitado pelas operações que atualizam o conteúdo do servidor.</span><span class="sxs-lookup"><span data-stu-id="86619-135">The **SharePoint:FormDigest** tag generates a message digest for security validation when required by operations that update server content.</span></span> 
    
6. <span data-ttu-id="86619-136">Substitua o comentário de espaço reservado pelo código de um dos seguintes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="86619-136">Replace the comment between the script tags with the code example from one of the following scenarios:</span></span>
    
   - [<span data-ttu-id="86619-137">Criar projetos do Project Server 2013 usando o modelo de objeto do JavaScript</span><span class="sxs-lookup"><span data-stu-id="86619-137">Create Project Server 2013 projects by using the JavaScript object model</span></span>](#pj15_CRUDProjectsJSOM_CreateProjects)
    
   - [<span data-ttu-id="86619-138">Atualizar projetos do Project Server 2013 usando o modelo de objeto do JavaScript</span><span class="sxs-lookup"><span data-stu-id="86619-138">Update Project Server 2013 projects by using the JavaScript object model</span></span>](#pj15_CRUDProjectsJSOM_UpdateProjects)
    
   - [<span data-ttu-id="86619-139">Excluir projetos do Project Server 2013 usando o modelo de objeto do JavaScript</span><span class="sxs-lookup"><span data-stu-id="86619-139">Delete Project Server 2013 projects by using the JavaScript object model</span></span>](#pj15_CRUDProjectsJSOM_DeleteProjects)
    
7. <span data-ttu-id="86619-140">Para testar a página de aplicativo, na barra de menus, escolha **Depurar**, **Iniciar Depuração**.</span><span class="sxs-lookup"><span data-stu-id="86619-140">To test the console application, on the menu bar, choose **Debug**, **Start Debugging**.</span></span> <span data-ttu-id="86619-141">Se você for solicitado a modificar as configurações, escolha **OK**.</span><span class="sxs-lookup"><span data-stu-id="86619-141">To test the application page, on the menu bar, choose Debug, Start Debugging. If you are prompted to modify the web.config file, choose the OK button.</span></span>
    
## <a name="create-project-server-2013-projects-by-using-the-javascript-object-model"></a><span data-ttu-id="86619-142">Criar projetos do Project Server 2013 usando o modelo de objeto do JavaScript</span><span class="sxs-lookup"><span data-stu-id="86619-142">Create Project Server 2013 projects by using the JavaScript object model</span></span>
<span data-ttu-id="86619-143"><a name="pj15_CRUDProjectsJSOM_CreateProjects"> </a></span><span class="sxs-lookup"><span data-stu-id="86619-143"></span></span>

<span data-ttu-id="86619-144">O procedimento nesta seção cria projetos usando o modelo de objeto JavaScript.</span><span class="sxs-lookup"><span data-stu-id="86619-144">The procedure in this section creates projects by using the JavaScript object model.</span></span> <span data-ttu-id="86619-145">O procedimento inclui as seguintes etapas de alto nível:</span><span class="sxs-lookup"><span data-stu-id="86619-145">The procedure includes the following high-level steps:</span></span>
  
1. <span data-ttu-id="86619-146">Obter a instância atual **ProjectContext**.</span><span class="sxs-lookup"><span data-stu-id="86619-146">Get the current **ProjectContext** instance.</span></span> 
    
2. <span data-ttu-id="86619-147">Criar um objeto **ProjectCreationInformation** para especificar propriedades iniciais para o seu projeto.</span><span class="sxs-lookup"><span data-stu-id="86619-147">Create a **ProjectCreationInformation** object to specify initial properties for your project.</span></span> <span data-ttu-id="86619-148">Especificar a propriedade **nome** necessária usando a função **ProjectCreationInformation.set_name**.</span><span class="sxs-lookup"><span data-stu-id="86619-148">Specify the required **name** property by using the **ProjectCreationInformation.set_name** function.</span></span> 
    
3. <span data-ttu-id="86619-149">Recuperar projetos publicados pelo servidor usando a função **ProjectContext.get_projects**.</span><span class="sxs-lookup"><span data-stu-id="86619-149">Retrieve the published projects from the server by using the **ProjectContext.get_projects** function.</span></span> <span data-ttu-id="86619-150">A função **get_projects** retorna um objeto **ProjectCollection**.</span><span class="sxs-lookup"><span data-stu-id="86619-150">The **get_projects** function returns a **ProjectCollection** object.</span></span> 
    
4. <span data-ttu-id="86619-151">Adicionar o novo projeto ao conjunto, usando a função **ProjectCollection.add** e passando o objeto **ProjectCreationInformation**.</span><span class="sxs-lookup"><span data-stu-id="86619-151">Add the new project to the collection by using the **ProjectCollection.add** function and passing in the **ProjectCreationInformation** object.</span></span> 
    
5. <span data-ttu-id="86619-152">Atualizar o conjunto usando a função **ProjectCollection.update** e a função **ProjectContext.waitForQueueAsync**.</span><span class="sxs-lookup"><span data-stu-id="86619-152">Update the collection by using the **ProjectCollection.update** function and the **ProjectContext.waitForQueueAsync** function.</span></span> <span data-ttu-id="86619-153">A função **atualizar** retorna um objeto **QueueJob** que passará para **waitForQueueAsync**.</span><span class="sxs-lookup"><span data-stu-id="86619-153">The **update** function returns a **QueueJob** object that you pass to **waitForQueueAsync**.</span></span> <span data-ttu-id="86619-154">Essa chamada também publica o projeto.</span><span class="sxs-lookup"><span data-stu-id="86619-154">This call also publishes the project.</span></span>
    
<span data-ttu-id="86619-155">Cole o seguinte código entre as marcas de **script** que você adicionou no procedimento **Criar a página de aplicativo em Visual Studio**.</span><span class="sxs-lookup"><span data-stu-id="86619-155">Paste the following code between the **script** tags that you added in the **Create the application page** procedure.</span></span> 
  
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

## <a name="update-project-server-2013-projects-by-using-the-javascript-object-model"></a><span data-ttu-id="86619-156">Atualizar projetos do Project Server 2013 usando o modelo de objeto do JavaScript</span><span class="sxs-lookup"><span data-stu-id="86619-156">Update Project Server 2013 projects by using the JavaScript object model</span></span>
<span data-ttu-id="86619-157"><a name="pj15_CRUDProjectsJSOM_UpdateProjects"> </a></span><span class="sxs-lookup"><span data-stu-id="86619-157"></span></span>

<span data-ttu-id="86619-158">O procedimento nesta seção atualiza a propriedade **startDate** de um projeto, usando o modelo de objeto JavaScript.</span><span class="sxs-lookup"><span data-stu-id="86619-158">The procedure in this section updates the **startDate** property of a project by using the JavaScript object model.</span></span> <span data-ttu-id="86619-159">O procedimento inclui as seguintes etapas de alto nível:</span><span class="sxs-lookup"><span data-stu-id="86619-159">The procedure includes the following high-level steps:</span></span> 
  
1. <span data-ttu-id="86619-160">Obter a instância atual **ProjectContext**.</span><span class="sxs-lookup"><span data-stu-id="86619-160">Get the current **ProjectContext** instance.</span></span> 
    
2. <span data-ttu-id="86619-161">Recuperar projetos publicados pelo servidor usando a função **ProjectContext.get_projects**.</span><span class="sxs-lookup"><span data-stu-id="86619-161">Retrieve the published projects from the server by using the **ProjectContext.get_projects** function.</span></span> <span data-ttu-id="86619-162">A função **get_projects** retorna um objeto **ProjectCollection**.</span><span class="sxs-lookup"><span data-stu-id="86619-162">The **get_projects** function returns a **ProjectCollection** object.</span></span> 
    
3. <span data-ttu-id="86619-163">Executar a solicitação no servidor usando a função **ProjectContext.load** e a função **ProjectContext.executeQueryAsync**.</span><span class="sxs-lookup"><span data-stu-id="86619-163">Run the request on the server by using the **ProjectContext.load** function and the **ProjectContext.executeQueryAsync** function.</span></span> 
    
4. <span data-ttu-id="86619-164">Recuperar o objeto **PublishedProject** usando a função **ProjectContext.getById**.</span><span class="sxs-lookup"><span data-stu-id="86619-164">Retrieve a **PublishedProject** object by using the **ProjectContext.getById** function.</span></span> 
    
5. <span data-ttu-id="86619-165">Confira o projeto de destino, usando a função **Project.checkOut**.</span><span class="sxs-lookup"><span data-stu-id="86619-165">Check out the target project by using the **Project.checkOut** function.</span></span> <span data-ttu-id="86619-166">A função **check-out** retornará a versão de rascunho do projeto publicado.</span><span class="sxs-lookup"><span data-stu-id="86619-166">The **checkOut** function returns the draft version of the published project.</span></span> 
    
6. <span data-ttu-id="86619-167">Alterar a data de início do projeto usando a função **DraftProject.set_startDate**.</span><span class="sxs-lookup"><span data-stu-id="86619-167">Change the project's start date by using the **DraftProject.set_startDate** function.</span></span> 
    
7. <span data-ttu-id="86619-168">Publicar o projeto usando a função **DraftProject.publish** e a função **ProjectContext.waitForQueueAsync**.</span><span class="sxs-lookup"><span data-stu-id="86619-168">Publish the project by using the **DraftProject.publish** function and the **ProjectContext.waitForQueueAsync** function.</span></span> <span data-ttu-id="86619-169">A função **publicar** retorna um objeto **QueueJob** que passará para o **waitForQueueAsync**.</span><span class="sxs-lookup"><span data-stu-id="86619-169">The **publish** function returns a **QueueJob** object that you pass to **waitForQueueAsync**.</span></span>
    
<span data-ttu-id="86619-170">Cole o seguinte código entre as marcas de **script** que você adicionou no procedimento **Criar a página de aplicativo em Visual Studio**.</span><span class="sxs-lookup"><span data-stu-id="86619-170">Paste the following code between the **script** tags that you added in the **Create the application page** procedure.</span></span> 
  
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

## <a name="delete-project-server-2013-projects-by-using-the-javascript-object-model"></a><span data-ttu-id="86619-171">Excluir projetos do Project Server 2013 usando o modelo de objeto do JavaScript</span><span class="sxs-lookup"><span data-stu-id="86619-171">Delete Project Server 2013 projects by using the JavaScript object model</span></span>
<span data-ttu-id="86619-172"><a name="pj15_CRUDProjectsJSOM_DeleteProjects"> </a></span><span class="sxs-lookup"><span data-stu-id="86619-172"></span></span>

<span data-ttu-id="86619-173">O procedimento nesta seção exclui um projeto usando o modelo de objeto JavaScript.</span><span class="sxs-lookup"><span data-stu-id="86619-173">The procedure in this section deletes a project by using the JavaScript object model.</span></span> <span data-ttu-id="86619-174">O procedimento inclui as seguintes etapas de alto nível:</span><span class="sxs-lookup"><span data-stu-id="86619-174">The procedure includes the following high-level steps:</span></span>
  
1. <span data-ttu-id="86619-175">Obter a instância atual **ProjectContext**.</span><span class="sxs-lookup"><span data-stu-id="86619-175">Get the current **ProjectContext** instance.</span></span> 
    
2. <span data-ttu-id="86619-176">Recuperar projetos publicados pelo servidor usando a função **ProjectContext.get_projects**.</span><span class="sxs-lookup"><span data-stu-id="86619-176">Retrieve the published projects from the server by using the **ProjectContext.get_projects** function.</span></span> <span data-ttu-id="86619-177">A função **get_projects** retorna um objeto **ProjectCollection**.</span><span class="sxs-lookup"><span data-stu-id="86619-177">The **get_projects** function returns a **ProjectCollection** object.</span></span> 
    
3. <span data-ttu-id="86619-178">Executar a solicitação no servidor usando a função **ProjectContext.load** e a função **ProjectContext.executeQueryAsync**.</span><span class="sxs-lookup"><span data-stu-id="86619-178">Run the request on the server by using the **ProjectContext.load** function and the **ProjectContext.executeQueryAsync** function.</span></span> 
    
4. <span data-ttu-id="86619-179">Recuperar um objeto **PublishedProject** usando a função **ProjectCollection.getById**.</span><span class="sxs-lookup"><span data-stu-id="86619-179">Retrieve a **PublishedProject** object by using the **ProjectCollection.getById** function.</span></span> 
    
5. <span data-ttu-id="86619-180">Excluir o projeto, passando-o para a função **ProjectCollection.remove**.</span><span class="sxs-lookup"><span data-stu-id="86619-180">Delete the project by passing it to the **ProjectCollection.remove** function.</span></span> 
    
6. <span data-ttu-id="86619-181">Atualizar o conjunto usando a função **ProjectCollection.update** e a função **ProjectContext.waitForQueueAsync**.</span><span class="sxs-lookup"><span data-stu-id="86619-181">Update the collection by using the **ProjectCollection.update** function and the **ProjectContext.waitForQueueAsync** function.</span></span> <span data-ttu-id="86619-182">A função **atualizar** retorna um objeto **QueueJob** que passará para **waitForQueueAsync**.</span><span class="sxs-lookup"><span data-stu-id="86619-182">The **update** function returns a **QueueJob** object that you pass to **waitForQueueAsync**.</span></span>
    
<span data-ttu-id="86619-183">Cole o seguinte código entre as marcas de **script** que você adicionou no procedimento **Criar a página de aplicativo em Visual Studio**.</span><span class="sxs-lookup"><span data-stu-id="86619-183">Paste the following code between the **script** tags that you added in the **Create the application page** procedure.</span></span> 
  
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

<span data-ttu-id="86619-184"><a name="pj15_CRUDProjectsJSOM_AR"> </a></span><span class="sxs-lookup"><span data-stu-id="86619-184"></span></span>

## <a name="see-also"></a><span data-ttu-id="86619-185">Confira também</span><span class="sxs-lookup"><span data-stu-id="86619-185">See also</span></span>

- [<span data-ttu-id="86619-186">Tarefas de programação do Project</span><span class="sxs-lookup"><span data-stu-id="86619-186">Project programming tasks</span></span>](project-programming-tasks.md)
- [<span data-ttu-id="86619-187">Modelo de objeto do cliente (CSOM) para o Project 2013</span><span class="sxs-lookup"><span data-stu-id="86619-187">Client-side object model (CSOM) for Project</span></span>](client-side-object-model-csom-for-project-2013.md)
    

