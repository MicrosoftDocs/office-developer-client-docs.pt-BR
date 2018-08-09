---
title: Introdução ao modelo de objeto JavaScript do Project Server 2013
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 30dc3194-7480-4e7c-b731-4a171d652ee0
description: No Project Server 2013, o modelo de objeto JavaScript pode ser usado no Project Online, desenvolvimento de dispositivos móvel e no local. Este tópico fornece uma breve visão geral do modelo de objeto JavaScript e, em seguida, descreve como criar uma página de aplicativo que recupera e itera projetos usando o modelo de objeto JavaScript.
ms.openlocfilehash: 94c882249474e22328031d55233cfba654dcff83
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771046"
---
# <a name="getting-started-with-the-project-server-2013-javascript-object-model"></a><span data-ttu-id="8585f-104">Introdução ao modelo de objeto JavaScript do Project Server 2013</span><span class="sxs-lookup"><span data-stu-id="8585f-104">Getting started with the Project Server 2013 JavaScript object model</span></span>

<span data-ttu-id="8585f-105">No Project Server 2013, o modelo de objeto JavaScript pode ser usado no Project Online, desenvolvimento de dispositivos móvel e no local.</span><span class="sxs-lookup"><span data-stu-id="8585f-105">In Project Server 2013, the JavaScript object model can be used in Project Online, mobile, and on-premise development.</span></span> <span data-ttu-id="8585f-106">Este tópico fornece uma breve visão geral do modelo de objeto JavaScript e, em seguida, descreve como criar uma página de aplicativo que recupera e itera projetos usando o modelo de objeto JavaScript.</span><span class="sxs-lookup"><span data-stu-id="8585f-106">This topic provides a brief overview of the JavaScript object model and then describes how to create an application page that retrieves and iterates through projects by using the JavaScript object model.</span></span>
  
## <a name="using-the-project-server-javascript-object-model"></a><span data-ttu-id="8585f-107">Usando o modelo de objeto JavaScript do Project Server</span><span class="sxs-lookup"><span data-stu-id="8585f-107">Using the Project Server JavaScript object model</span></span>
<span data-ttu-id="8585f-108"><a name="pj15_GetStartedJSOM_UseJSOM"> </a></span><span class="sxs-lookup"><span data-stu-id="8585f-108"></span></span>

<span data-ttu-id="8585f-109">Usando o modelo de objeto JavaScript é uma ótima maneira de criar um aplicativo que executa o lado do cliente (em oposição ao código do cliente gerenciado que precisa ser executado remotamente).</span><span class="sxs-lookup"><span data-stu-id="8585f-109">Using the JavaScript object model is a great way to create an app that runs client-side (as opposed to managed client code which needs to run remotely).</span></span> <span data-ttu-id="8585f-110">Aplicativos podem usar o modelo de objeto JavaScript para recuperar ou alterar objetos enviando chamadas assíncronas para o servidor.</span><span class="sxs-lookup"><span data-stu-id="8585f-110">Apps can use the JavaScript object model to retrieve or change objects by sending asynchronous calls to the server.</span></span> <span data-ttu-id="8585f-111">Normalmente, os aplicativos que usam o modelo de objeto JavaScript são implantados como personalizado suplementos do SharePoint, Web Parts e páginas de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8585f-111">Apps that use the JavaScript object model are typically deployed as custom SharePoint Add-ins, application pages, and Web Parts.</span></span> <span data-ttu-id="8585f-112">Para obter mais informações, consulte "Tipos de componentes do SharePoint que podem estar em um aplicativo para SharePoint" em [webs de Host, suplemento webs e os componentes do SharePoint no SharePoint 2013](http://msdn.microsoft.com/library/b791cdf5-8aa2-47fa-bc4c-aee437354759%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="8585f-112">For more information, see "Types of SharePoint components that can be in an app for SharePoint" in [Host webs, add-in webs, and SharePoint components in SharePoint 2013](http://msdn.microsoft.com/library/b791cdf5-8aa2-47fa-bc4c-aee437354759%28Office.15%29.aspx).</span></span>
  
<span data-ttu-id="8585f-113">O modelo de objeto JavaScript implementa a funcionalidade principal do Project Server 2013, mas o modelo de objeto JavaScript e o modelo de objeto de servidor não têm um-para-paridade.</span><span class="sxs-lookup"><span data-stu-id="8585f-113">The JavaScript object model implements the main functionality of Project Server 2013, but the JavaScript object model and the server object model do not have one-to-one parity.</span></span> <span data-ttu-id="8585f-114">O ponto de entrada para o modelo de objeto JavaScript é o objeto **ProjectContext** , que representa o contexto de cliente do Project Server 2013 e fornece acesso ao conteúdo do servidor e a funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="8585f-114">The entry point to the JavaScript object model is the **ProjectContext** object, which represents the client context for Project Server 2013 and provides access to server content and functionality.</span></span> <span data-ttu-id="8585f-115">O modelo de objeto JavaScript para o Project Server 2013 é definido no arquivo PS.js, que está localizado no caminho padrão `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS` no servidor de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="8585f-115">The JavaScript object model for Project Server 2013 is defined in the PS.js file, which is located in the default path  `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS` on the application server.</span></span> <span data-ttu-id="8585f-116">Project Server 2013 também instala o PS. Arquivo Debug no mesmo local.</span><span class="sxs-lookup"><span data-stu-id="8585f-116">Project Server 2013 also installs the PS.Debug.js file in the same location.</span></span> <span data-ttu-id="8585f-117">PS. Debug é uma versão unminified do PS.js que fornece informações de IntelliSense.</span><span class="sxs-lookup"><span data-stu-id="8585f-117">PS.Debug.js is an unminified version of PS.js that provides IntelliSense information.</span></span> 
  
<span data-ttu-id="8585f-118">O modelo de objeto JavaScript permite a autenticação de formulários e todas as solicitações sejam autenticadas como o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="8585f-118">The JavaScript object model allows Forms authentication, and all requests are authenticated as the current user.</span></span> <span data-ttu-id="8585f-119">Para obter mais informações sobre segurança e outras considerações para aplicativos personalizados de criação e soluções, consulte [autenticação, autorização e segurança no SharePoint 2013](http://msdn.microsoft.com/library/8734790c-eb75-4d78-9604-7cc23b33b693%28Office.15%29.aspx), [de aspectos importantes da arquitetura do SharePoint Add-in e desenvolvimento Paisagem](http://msdn.microsoft.com/library/ae96572b-8f06-4fd3-854f-fc312f7f2d88%28Office.15%29.aspx)e [suplementos do SharePoint em comparação com soluções do SharePoint](http://msdn.microsoft.com/library/0e9efadb-aaf2-4c0d-afd5-d6cf25c4e7a8%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="8585f-119">For more information about security and other considerations for designing custom apps and solutions, see [Authentication, authorization, and security in SharePoint 2013](http://msdn.microsoft.com/library/8734790c-eb75-4d78-9604-7cc23b33b693%28Office.15%29.aspx), [Important aspects of the SharePoint Add-in architecture and development landscape](http://msdn.microsoft.com/library/ae96572b-8f06-4fd3-854f-fc312f7f2d88%28Office.15%29.aspx), and [SharePoint Add-ins compared with SharePoint solutions](http://msdn.microsoft.com/library/0e9efadb-aaf2-4c0d-afd5-d6cf25c4e7a8%28Office.15%29.aspx).</span></span>
  
> [!NOTE]
> <span data-ttu-id="8585f-120">Para acessar os dados de um site do SharePoint remotamente, o SharePoint 2013 fornece uma biblioteca de entre domínios que permite que você faça chamadas do lado do cliente entre domínios.</span><span class="sxs-lookup"><span data-stu-id="8585f-120">To access data from a SharePoint site remotely, SharePoint 2013 provides a cross-domain library that enables you to make client-side cross-domain calls.</span></span> <span data-ttu-id="8585f-121">Para obter mais informações, consulte [data de acesso do SharePoint 2013 de suplementos usando a biblioteca de domínio cruzado](http://msdn.microsoft.com/library/bc37ff5c-1285-40af-98ae-01286696242d%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="8585f-121">For more information, see [Access SharePoint 2013 data from add-ins using the cross-domain library](http://msdn.microsoft.com/library/bc37ff5c-1285-40af-98ae-01286696242d%28Office.15%29.aspx).</span></span> 
  
<span data-ttu-id="8585f-122">Muitos conceitos e processos para usar o modelo de objeto JavaScript para o Project Server 2013 se parecem com aqueles nos modelos de objeto do cliente relacionados.</span><span class="sxs-lookup"><span data-stu-id="8585f-122">Many concepts and processes for using the JavaScript object model for Project Server 2013 resemble those in related client object models.</span></span> <span data-ttu-id="8585f-123">Para obter mais informações sobre o modelo de objeto do cliente gerenciado do Project Server 2013, consulte **Microsoft.ProjectServer.Client**.</span><span class="sxs-lookup"><span data-stu-id="8585f-123">For more information about the Project Server 2013 managed client object model, see **Microsoft.ProjectServer.Client**.</span></span> <span data-ttu-id="8585f-124">Para obter mais informações sobre o modelo de objeto do SharePoint 2013JavaScript e o modelo de objeto do cliente gerenciado, consulte [concluir operações básicas usando o código JavaScript da biblioteca no SharePoint 2013](http://msdn.microsoft.com/library/29089af8-dbc0-49b7-a1a0-9e311f49c826%28Office.15%29.aspx) e [completa operações básicas usando o cliente do SharePoint 2013 código de biblioteca](http://msdn.microsoft.com/library/5a69c9e3-73bf-4ed5-bc19-182056bdb394%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="8585f-124">For more information about the SharePoint 2013JavaScript object model and managed client object model, see [Complete basic operations using JavaScript library code in SharePoint 2013](http://msdn.microsoft.com/library/29089af8-dbc0-49b7-a1a0-9e311f49c826%28Office.15%29.aspx) and [Complete basic operations using SharePoint 2013 client library code](http://msdn.microsoft.com/library/5a69c9e3-73bf-4ed5-bc19-182056bdb394%28Office.15%29.aspx).</span></span>
  
## <a name="walkthrough-creating-an-application-page-that-retrieves-and-iterates-through-projects"></a><span data-ttu-id="8585f-125">Passo a passo: Criando uma página do aplicativo que recupera e itera através de projetos</span><span class="sxs-lookup"><span data-stu-id="8585f-125">Walkthrough: Creating an application page that retrieves and iterates through projects</span></span>
<span data-ttu-id="8585f-126"><a name="pj15_GetStartedJSOM_UseJSOM"> </a></span><span class="sxs-lookup"><span data-stu-id="8585f-126"></span></span>

<span data-ttu-id="8585f-127">Saiba como criar uma página que exibe o ID, o nome e a data de criação de cada projeto publicado em um site do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8585f-127">Learn how to create an application page that displays the ID, name, and created date of each published project in a site.</span></span>
  
### <a name="prerequisites-for-creating-an-application-page-that-retrieves-and-iterates-through-projects"></a><span data-ttu-id="8585f-128">Pré-requisitos para a criação de página de um aplicativo que recupera e itera através de projetos</span><span class="sxs-lookup"><span data-stu-id="8585f-128">Prerequisites for creating an application page that retrieves and iterates through projects</span></span>
<span data-ttu-id="8585f-129"><a name="pj15_GetStartedJSOM_Prereqs"> </a></span><span class="sxs-lookup"><span data-stu-id="8585f-129"></span></span>

<span data-ttu-id="8585f-130">Para desenvolver a página do aplicativo que está descrita neste tópico, instale e configure os seguintes produtos:</span><span class="sxs-lookup"><span data-stu-id="8585f-130">To develop the application page that is described in this topic, you must install and configure the following products:</span></span>
  
- <span data-ttu-id="8585f-131">SharePoint Server 2013</span><span class="sxs-lookup"><span data-stu-id="8585f-131">SharePoint Server 2013</span></span>
- <span data-ttu-id="8585f-132">Project Server 2013 com pelo menos um projeto publicado</span><span class="sxs-lookup"><span data-stu-id="8585f-132">Project Server 2013 with at least one published project</span></span>
- <span data-ttu-id="8585f-133">Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="8585f-133">Visual Studio 2012</span></span>
- <span data-ttu-id="8585f-134">Office Developer Tools para Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="8585f-134">Office Developer Tools for Visual Studio 2012</span></span>
    
<span data-ttu-id="8585f-135">Você também deve ter permissões para implantar a extensão para o SharePoint Server 2013 e para recuperar os projetos.</span><span class="sxs-lookup"><span data-stu-id="8585f-135">You must also have permissions to deploy the extension to SharePoint Server 2013 and to retrieve projects.</span></span>
  
> [!NOTE]
> <span data-ttu-id="8585f-136">Estas instruções pressupõem que você estiver desenvolvendo no computador que está executando o Project Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8585f-136">These instructions assume that you are developing on the computer that is running Project Server 2013.</span></span> 
  
### <a name="creating-the-application-page-in-visual-studio-2012"></a><span data-ttu-id="8585f-137">Criando a página de aplicativo no Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="8585f-137">Creating the application page in Visual Studio 2012</span></span>
<span data-ttu-id="8585f-138"><a name="pj15_GetStartedJSOM_CreateVS"> </a></span><span class="sxs-lookup"><span data-stu-id="8585f-138"></span></span>

<span data-ttu-id="8585f-139">As etapas a seguir criam um projeto do SharePoint e a página de um aplicativo que contém uma tabela e rótulo.</span><span class="sxs-lookup"><span data-stu-id="8585f-139">The following steps create a SharePoint project and an application page that contains a table and label.</span></span> <span data-ttu-id="8585f-140">A tabela exibe informações sobre os projetos e o rótulo exibe mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="8585f-140">The table displays information about the projects and the label displays error messages.</span></span>
  
1. <span data-ttu-id="8585f-141">No computador que está executando o Project Server 2013, execute o Visual Studio 2012 como administrador.</span><span class="sxs-lookup"><span data-stu-id="8585f-141">On the computer that is running Project Server 2013, run Visual Studio 2012 as an administrator.</span></span>
    
2. <span data-ttu-id="8585f-142">Crie um projeto vazio do SharePoint 2013, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="8585f-142">Create an empty SharePoint 2013 project, as follows:</span></span>
    
    1. <span data-ttu-id="8585f-143">Na caixa de diálogo **Novo projeto**, escolha o **.NET Framework 4.5** da lista suspensa na parte superior da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="8585f-143">In the **New Project** dialog box, choose **.NET Framework 4.5** from the drop-down list at the top of the dialog box.</span></span> 
        
    2. <span data-ttu-id="8585f-144">Na lista de categorias de modelo, escolha a categoria **SharePoint do Office** e, em seguida, escolha o modelo de **Projeto do SharePoint 2013** .</span><span class="sxs-lookup"><span data-stu-id="8585f-144">In the list of template categories, choose the **Office SharePoint** category, and then choose the **SharePoint 2013 Project** template.</span></span> 
        
    3. <span data-ttu-id="8585f-145">Nome do projeto GetProjectsJSOM e escolha o botão **Okey** .</span><span class="sxs-lookup"><span data-stu-id="8585f-145">Name the project GetProjectsJSOM, and then choose the **OK** button.</span></span> 
        
    4. <span data-ttu-id="8585f-146">Na caixa de diálogo **Assistente de personalização do SharePoint** , selecione **implantar como uma solução de farm**e escolha o botão **Okey** .</span><span class="sxs-lookup"><span data-stu-id="8585f-146">In the **SharePoint Customization Wizard** dialog box, choose **Deploy as a farm solution**, and then choose the **OK** button.</span></span> 
    
3. <span data-ttu-id="8585f-147">No Solution Explorer, edite o valor da propriedade **URL do Site** para o projeto **ProjectsJSOM** coincidir com a URL da instância do Project Web App (por exemplo, `http://ServerName/PWA`).</span><span class="sxs-lookup"><span data-stu-id="8585f-147">In Solution Explorer, edit the value of the **Site URL** property for the **ProjectsJSOM** project to match the URL of the Project Web App instance (for example,  `http://ServerName/PWA`).</span></span>
    
4. <span data-ttu-id="8585f-148">Abra o menu de atalho para o projeto **GetProjectsJSOM** e, em seguida, adicionar uma lista do SharePoint "Layouts" mapeado a pasta.</span><span class="sxs-lookup"><span data-stu-id="8585f-148">Open the shortcut menu for the **GetProjectsJSOM** project, and then add a SharePoint "Layouts" mapped folder.</span></span> 
    
5. <span data-ttu-id="8585f-149">Na pasta **Layouts** , abra o menu de atalho para a pasta **GetProjectsJSOM** e, em seguida, adicione uma nova página de aplicativos do SharePoint denominada ProjectsList.aspx.</span><span class="sxs-lookup"><span data-stu-id="8585f-149">In the **Layouts** folder, open the shortcut menu for the **GetProjectsJSOM** folder, and then add a new SharePoint application page named ProjectsList.aspx.</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="8585f-150">Este exemplo não usa o arquivo de code-behind que cria do Visual Studio 2012 para a página do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8585f-150">This example does not use the code-behind file that Visual Studio 2012 creates for the application page.</span></span> 
  
6. <span data-ttu-id="8585f-151">Abra o menu de atalho para a página **ProjectsList.aspx** e escolha **definida como Item de inicialização**.</span><span class="sxs-lookup"><span data-stu-id="8585f-151">Open the shortcut menu for the **ProjectsList.aspx** page and choose **Set as Startup Item**.</span></span>
    
7. <span data-ttu-id="8585f-152">Na marcação para a página **ProjectsList.aspx** , defina uma tabela e um espaço reservado de mensagem dentro das marcas de **asp: Content** "Main", da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="8585f-152">In the markup for the **ProjectsList.aspx** page, define a table and a message placeholder inside the "Main" **asp:Content** tags, as follows.</span></span> 
    
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

### <a name="retrieving-the-projects-collection"></a><span data-ttu-id="8585f-153">Recuperando a coleção projects</span><span class="sxs-lookup"><span data-stu-id="8585f-153">Retrieving the projects collection</span></span>
<span data-ttu-id="8585f-154"><a name="pj15_GetStartedJSOM_RetrieveProjs"> </a></span><span class="sxs-lookup"><span data-stu-id="8585f-154"></span></span>

<span data-ttu-id="8585f-155">As etapas a seguir recuperar e inicializar a coleção projects.</span><span class="sxs-lookup"><span data-stu-id="8585f-155">The following steps retrieve and initialize the projects collection.</span></span>
  
1. <span data-ttu-id="8585f-156">Após o fechamento **div** marca, adicione uma marca de **SharePoint:ScriptLink** que referencia o arquivo de PS.js, da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="8585f-156">After the closing **div** tag, add a **SharePoint:ScriptLink** tag that references the PS.js file, as follows.</span></span> 
    
   ```HTML
    <SharePoint:ScriptLink name="PS.js" runat="server" ondemand="false" localizable="false" loadafterui="true" />
   ```

2. <span data-ttu-id="8585f-157">Abaixo da tag **SharePoint:ScriptLink** , adicione marcas de **script** , da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="8585f-157">Below the **SharePoint:ScriptLink** tag, add **script** tags, as follows.</span></span> 
    
   ```HTML
    <script type="text/javascript">
        // Paste the remaining code snippets here, in the order that they are presented.
    </script>
   ```

3. <span data-ttu-id="8585f-158">Declare uma variável global para armazenar o conjunto de projetos, da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="8585f-158">Declare a global variable to store the projects collection, as follows.</span></span>
    
   ```js
   var projects;
   ```

4. <span data-ttu-id="8585f-159">Chamar o **SP. SOD.executeOrDelayUntilScriptLoaded** método para garantir que o arquivo PS.js seja carregado antes de seu código personalizado é executado.</span><span class="sxs-lookup"><span data-stu-id="8585f-159">Call the **SP.SOD.executeOrDelayUntilScriptLoaded** method to ensure that the PS.js file is loaded before your custom code runs.</span></span> 
    
   ```js
   SP.SOD.executeOrDelayUntilScriptLoaded(GetProjects, "PS.js");
   ```

5. <span data-ttu-id="8585f-160">Adicione uma função que se conecta ao contexto atual e recupera a coleção projects, da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="8585f-160">Add a function that connects to the current context and retrieves the projects collection, as follows.</span></span>
    
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

   <span data-ttu-id="8585f-161">Alguns objetos de cliente que você recuperar por meio do contexto não contêm nenhum dado até que eles são inicializados; ou seja, você não pode acessar os valores de propriedade do objeto até que o objeto é inicializado.</span><span class="sxs-lookup"><span data-stu-id="8585f-161">Some client objects that you retrieve through the context contain no data until they are initialized; that is, you cannot access the property values of the object until the object is initialized.</span></span> <span data-ttu-id="8585f-162">Além disso, para propriedades do tipo **ValueObject**, você deve solicitar explicitamente a propriedade antes de poder acessar seu valor.</span><span class="sxs-lookup"><span data-stu-id="8585f-162">Moreover, for properties of type **ValueObject**, you must explicitly request the property before you can access its value.</span></span> <span data-ttu-id="8585f-163">(Se você tentar acessar uma propriedade antes de ele é inicializado, você receberá uma exceção **PropertyOrFieldNotInitializedException** .)</span><span class="sxs-lookup"><span data-stu-id="8585f-163">(If you try to access a property before it is initialized, you receive a **PropertyOrFieldNotInitializedException** exception.)</span></span> 
    
   <span data-ttu-id="8585f-164">Para inicializar um objeto, você chamar o método **load** (ou o método **loadQuery** ) e, em seguida, o método **executeQueryAsync** .</span><span class="sxs-lookup"><span data-stu-id="8585f-164">To initialize an object, you call the **load** method (or the **loadQuery** method) and then the **executeQueryAsync** method.</span></span> 
    
   - <span data-ttu-id="8585f-165">Chamar a função **de carga** ou a função **loadQuery** registra uma solicitação que você deseja executar no servidor.</span><span class="sxs-lookup"><span data-stu-id="8585f-165">Calling the **load** function or the **loadQuery** function registers a request that you want to run on the server.</span></span> <span data-ttu-id="8585f-166">Você passar um parâmetro que representa o objeto que você deseja recuperar.</span><span class="sxs-lookup"><span data-stu-id="8585f-166">You pass in a parameter that represents the object that you want to retrieve.</span></span> <span data-ttu-id="8585f-167">Se você estiver trabalhando com uma propriedade **ValueObject** , em seguida, você também solicitar a propriedade no parâmetro.</span><span class="sxs-lookup"><span data-stu-id="8585f-167">If you are working with a **ValueObject** property, then you also request the property in the parameter.</span></span> 
    
   - <span data-ttu-id="8585f-168">Chamar a função **executeQueryAsync** envia a solicitação de consulta para o servidor de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="8585f-168">Calling the **executeQueryAsync** function sends the query request to the server asynchronously.</span></span> <span data-ttu-id="8585f-169">Você passar uma função de retorno de chamada de sucesso e uma função de retorno de chamada de falha para invocar quando a resposta do servidor é recebida.</span><span class="sxs-lookup"><span data-stu-id="8585f-169">You pass in a success callback function and a failure callback function to invoke when the server response is received.</span></span> 
    
   <span data-ttu-id="8585f-170">Para reduzir o tráfego de rede, solicite apenas as propriedades que você deseja trabalhar com quando se chama a função **de carga** .</span><span class="sxs-lookup"><span data-stu-id="8585f-170">To reduce network traffic, request only the properties that you want to work with when you call the **load** function.</span></span> <span data-ttu-id="8585f-171">Além disso, se você estiver trabalhando com vários objetos, agrupe várias chamadas para a função **de carga** antes de chamar a função **executeQueryAsync** quando possível.</span><span class="sxs-lookup"><span data-stu-id="8585f-171">In addition, if you are working with multiple objects, group multiple calls to the **load** function before you call the **executeQueryAsync** function when it is possible.</span></span> 
    
### <a name="iterating-through-the-projects-collection"></a><span data-ttu-id="8585f-172">A iteração através da coleção de projetos</span><span class="sxs-lookup"><span data-stu-id="8585f-172">Iterating through the projects collection</span></span>
<span data-ttu-id="8585f-173"><a name="pj15_GetStartedJSOM_IterateProjs"> </a></span><span class="sxs-lookup"><span data-stu-id="8585f-173"></span></span>

<span data-ttu-id="8585f-174">As etapas a seguir percorrer a coleção projects (se a chamada do servidor é bem-sucedida) ou uma mensagem de erro de renderização (se a chamada falhar).</span><span class="sxs-lookup"><span data-stu-id="8585f-174">The following steps iterate through the projects collection (if the server call is successful) or render an error message (if the call fails).</span></span>
  
1. <span data-ttu-id="8585f-175">Adicione uma função de retorno de chamada de sucesso que itera através da coleção de projetos, da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="8585f-175">Add a success callback function that iterates through the projects collection, as follows.</span></span>
    
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

2. <span data-ttu-id="8585f-176">Adicione uma função de retorno de chamada falha que renderiza a uma mensagem de erro, da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="8585f-176">Add a failure callback function that renders an error message, as follows.</span></span>
    
    ```js
    function onQueryFailed(sender, args) {
        $get("spanMessage").innerText = 'Request failed: ' + args.get_message();
    }
    ```

3. <span data-ttu-id="8585f-177">Para testar a página de aplicativo, na barra de menus, escolha **Depurar**, **Iniciar depuração**.</span><span class="sxs-lookup"><span data-stu-id="8585f-177">To test the application page, on the menu bar, choose **Debug**, **Start Debugging**.</span></span> <span data-ttu-id="8585f-178">Se você for solicitado para modificar o arquivo Web. config, escolha **Okey**.</span><span class="sxs-lookup"><span data-stu-id="8585f-178">If you are prompted to modify the web.config file, choose **OK**.</span></span>

<span data-ttu-id="8585f-179"><a name="pj15_GetStartedJSOM_CompleteExample"> </a></span><span class="sxs-lookup"><span data-stu-id="8585f-179"></span></span>

## <a name="complete-code-example"></a><span data-ttu-id="8585f-180">Exemplo de código completo</span><span class="sxs-lookup"><span data-stu-id="8585f-180">Complete code example</span></span>

<span data-ttu-id="8585f-181">A seguir é o código completo do arquivo ProjectsList.aspx exe.</span><span class="sxs-lookup"><span data-stu-id="8585f-181">Following is the complete code from the ProjectsList.aspx file.</span></span>
  
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

<span data-ttu-id="8585f-182"><a name="pj15_GetStartedJSOM_AR"> </a></span><span class="sxs-lookup"><span data-stu-id="8585f-182"></span></span>

## <a name="see-also"></a><span data-ttu-id="8585f-183">Confira também</span><span class="sxs-lookup"><span data-stu-id="8585f-183">See also</span></span>

- [<span data-ttu-id="8585f-184">Criar, recuperar, atualizar e excluir projetos usando o modelo de objeto JavaScript do Project Server</span><span class="sxs-lookup"><span data-stu-id="8585f-184">Create, retrieve, update, and delete projects by using the Project Server JavaScript object model</span></span>](create-retrieve-update-delete-projects-using-project-server-javascript.md)  
- [<span data-ttu-id="8585f-185">Modelo de objeto do cliente (CSOM) para o Project 2013</span><span class="sxs-lookup"><span data-stu-id="8585f-185">Client-side object model (CSOM) for Project 2013</span></span>](client-side-object-model-csom-for-project-2013.md)
- [<span data-ttu-id="8585f-186">Introdução ao Project Server CSOM e .NET</span><span class="sxs-lookup"><span data-stu-id="8585f-186">Getting started with the Project Server CSOM and .NET</span></span>](getting-started-with-the-project-server-csom-and-net.md)
    

