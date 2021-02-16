---
title: Criar, recuperar, atualizar e excluir projetos usando o Project Server JavaScript
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6b690938-05bc-46a3-a40e-30f081403767
description: Obter a instância ProjectContext atual; recuperar e iterar sobre o conjunto de projetos publicados no servidor. criar, recuperar, conferir e excluir um projeto usando o modelo de objeto do JavaScript do Project Server; e alterar as propriedades do projeto.
ms.openlocfilehash: 10dac7edfa3e84cebfd0585bc8c4bff1ea22ea44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322663"
---
# <a name="create-retrieve-update-and-delete-projects-using-project-server-javascript"></a>Criar, recuperar, atualizar e excluir projetos usando o Project Server JavaScript

Cenários neste artigo mostram como obter a instância **ProjectContext** atual; recuperar e iterar sobre o conjunto de projetos publicados no servidor. criar, recuperar, conferir e excluir um projeto usando o modelo de objeto do JavaScript do Project Server; e alterar as propriedades do projeto. 
  
> [!NOTE]
> Esses cenários definem o código personalizado na marcação de uma página do aplicativo do SharePoint, mas não usam o arquivo de code-behind que o Visual Studio 2012 cria na página. 
  
## <a name="prerequisites-for-working-with-project-server-2013-projects-in-the-javascript-object-model"></a>Pré-requisitos para trabalhar com projetos do Project Server 2013 no modelo de objeto do JavaScript

Para executar os cenários descritos neste artigo, instale e configure os seguintes produtos:
  
- SharePoint Server 2013
- Project Server 2013
- Visual Studio 2012
- Office Developer Tools para Visual Studio 2012
    
Você também deve ter permissões para implantar a extensão do SharePoint Server 2013 e para colaborar com projetos.
  
> [!NOTE]
> Essas instruções pressupõem que você esteja desenvolvendo em um computador que executa o Project Server 2013. 
  
## <a name="create-the-visual-studio-solution"></a>Criar a solução do Visual Studio
<a name="pj15_CRUDProjectsJSOM_Setup"> </a>

As etapas a seguir criam uma solução do Visual Studio 2012 com um projeto do SharePoint e uma página de aplicativo. A página contém a lógica para trabalhar com projetos.
  
### <a name="to-create-the-sharepoint-project-in-visual-studio"></a>Para criar um projeto do SharePoint no Visual Studio

1. No computador que executa o Project Server 2013, execute o Visual Studio 2012 como administrador.
    
2. Na barra de menus, selecione **Arquivo**, **Novo**, **Projeto**.
    
3. Na caixa de diálogo **Novo Projeto**, escolha **.NET Framework 4.5** na lista suspensa na parte superior da caixa de diálogo. 
    
4. Na categoria de modelos **Office/SharePoint**, escolha **Soluções do SharePoint** e, em seguida, escolha o modelo **Projeto do SharePoint 2013**. 
    
5. Nomeie o projeto como ProjectsJSOM e depois selecione o botão **OK**. 
    
6. Na caixa de diálogo **Assistente de Personalização do SharePoint**, selecione **Implantar como uma solução de farm** e, em seguida, escolha o botão **Concluir**. 
    
7. Edite o valor da propriedade **URL do Site** para que o projeto **ProjectsJSOM** corresponda à URL da instância do Project Web App (por exemplo, `https://ServerName/PWA`).
    
### <a name="to-create-the-application-page-in-visual-studio"></a>Criar a página de aplicativo em Visual Studio

1. No **Solution Explorer**, abra o menu de atalho do projeto **ProjectsJSOM** e, em seguida, adicione uma pasta mapeada "Layouts" do SharePoint. 
    
2. Na pasta **Layouts**, abra o menu de atalho da pasta **ProjectsJSOM** e, em seguida, adicione uma nova página de aplicativo do SharePoint denominada ProjectList.aspx.
    
3. Abra o menu de atalho da página **ProjectsList.aspx** e escolha **Set as Startup Item**.
    
4. Na marcação da página **ProjectsList.aspx**, defina os controles de interface de usuário dentro das marcas "Main" **asp:Content**, da forma seguinte. 
    
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
   > Esses controles não podem ser usados em todos os cenários. Por exemplo, o cenário "Criar projetos" não usa os controles de **área de texto** e **botão**. 
  
5. Depois de fechar a marca **span**, adicione uma marca **SharePoint:ScriptLink**, uma marca **SharePoint:FormDigest** e marcas de **script**, da forma seguinte. 
    
   ```HTML
    <SharePoint:ScriptLink id="ScriptLink" name="PS.js" runat="server" ondemand="false" localizable="false" loadafterui="true" />
    <SharePoint:FormDigest id="FormDigest" runat="server" />
    <script type="text/javascript">
        // Replace this comment with the code for your scenario.
    </script>
   ```

   A marca **SharePoint:ScriptLink** faz referência ao arquivo PS.js, que define o modelo de objeto do JavaScript do Project Server 2013. A marca **SharePoint:FormDigest** gerará uma compilação de mensagem para validação de segurança, quando isso for solicitado pelas operações que atualizam o conteúdo do servidor. 
    
6. Substitua o comentário de espaço reservado pelo código de um dos seguintes procedimentos:
    
   - [Criar projetos do Project Server 2013 usando o modelo de objeto do JavaScript](#pj15_CRUDProjectsJSOM_CreateProjects)
    
   - [Atualizar projetos do Project Server 2013 usando o modelo de objeto do JavaScript](#pj15_CRUDProjectsJSOM_UpdateProjects)
    
   - [Excluir projetos do Project Server 2013 usando o modelo de objeto do JavaScript](#pj15_CRUDProjectsJSOM_DeleteProjects)
    
7. Para testar a página de aplicativo, na barra de menus, escolha **Depurar**, **Iniciar Depuração**. Se você for solicitado a modificar as configurações, escolha **OK**.
    
## <a name="create-project-server-2013-projects-by-using-the-javascript-object-model"></a>Criar projetos do Project Server 2013 usando o modelo de objeto do JavaScript
<a name="pj15_CRUDProjectsJSOM_CreateProjects"> </a>

O procedimento nesta seção cria projetos usando o modelo de objeto JavaScript. O procedimento inclui as seguintes etapas de alto nível:
  
1. Obter a instância atual **ProjectContext**. 
    
2. Criar um objeto **ProjectCreationInformation** para especificar propriedades iniciais para o seu projeto. Especificar a propriedade **nome** necessária usando a função **ProjectCreationInformation.set_name**. 
    
3. Recuperar projetos publicados pelo servidor usando a função **ProjectContext.get_projects**. A função **get_projects** retorna um objeto **ProjectCollection**. 
    
4. Adicionar o novo projeto ao conjunto, usando a função **ProjectCollection.add** e passando o objeto **ProjectCreationInformation**. 
    
5. Atualizar o conjunto usando a função **ProjectCollection.update** e a função **ProjectContext.waitForQueueAsync**. A função **atualizar** retorna um objeto **QueueJob** que passará para **waitForQueueAsync**. Essa chamada também publica o projeto.
    
Cole o seguinte código entre as marcas de **script** que você adicionou no procedimento **Criar a página de aplicativo em Visual Studio**. 
  
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

## <a name="update-project-server-2013-projects-by-using-the-javascript-object-model"></a>Atualizar projetos do Project Server 2013 usando o modelo de objeto do JavaScript
<a name="pj15_CRUDProjectsJSOM_UpdateProjects"> </a>

O procedimento nesta seção atualiza a propriedade **startDate** de um projeto, usando o modelo de objeto JavaScript. O procedimento inclui as seguintes etapas de alto nível: 
  
1. Obter a instância atual **ProjectContext**. 
    
2. Recuperar projetos publicados pelo servidor usando a função **ProjectContext.get_projects**. A função **get_projects** retorna um objeto **ProjectCollection**. 
    
3. Executar a solicitação no servidor usando a função **ProjectContext.load** e a função **ProjectContext.executeQueryAsync**. 
    
4. Recuperar o objeto **PublishedProject** usando a função **ProjectContext.getById**. 
    
5. Confira o projeto de destino, usando a função **Project.checkOut**. A função **check-out** retornará a versão de rascunho do projeto publicado. 
    
6. Alterar a data de início do projeto usando a função **DraftProject.set_startDate**. 
    
7. Publicar o projeto usando a função **DraftProject.publish** e a função **ProjectContext.waitForQueueAsync**. A função **publicar** retorna um objeto **QueueJob** que passará para o **waitForQueueAsync**.
    
Cole o seguinte código entre as marcas de **script** que você adicionou no procedimento **Criar a página de aplicativo em Visual Studio**. 
  
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

## <a name="delete-project-server-2013-projects-by-using-the-javascript-object-model"></a>Excluir projetos do Project Server 2013 usando o modelo de objeto do JavaScript
<a name="pj15_CRUDProjectsJSOM_DeleteProjects"> </a>

O procedimento nesta seção exclui um projeto usando o modelo de objeto JavaScript. O procedimento inclui as seguintes etapas de alto nível:
  
1. Obter a instância atual **ProjectContext**. 
    
2. Recuperar projetos publicados pelo servidor usando a função **ProjectContext.get_projects**. A função **get_projects** retorna um objeto **ProjectCollection**. 
    
3. Executar a solicitação no servidor usando a função **ProjectContext.load** e a função **ProjectContext.executeQueryAsync**. 
    
4. Recuperar um objeto **PublishedProject** usando a função **ProjectCollection.getById**. 
    
5. Excluir o projeto, passando-o para a função **ProjectCollection.remove**. 
    
6. Atualizar o conjunto usando a função **ProjectCollection.update** e a função **ProjectContext.waitForQueueAsync**. A função **atualizar** retorna um objeto **QueueJob** que passará para **waitForQueueAsync**.
    
Cole o seguinte código entre as marcas de **script** que você adicionou no procedimento **Criar a página de aplicativo em Visual Studio**. 
  
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

<a name="pj15_CRUDProjectsJSOM_AR"> </a>

## <a name="see-also"></a>Confira também

- [Tarefas de programação do Project](project-programming-tasks.md)
- [Modelo de objeto do cliente (CSOM) para o Project 2013](client-side-object-model-csom-for-project-2013.md)
    

