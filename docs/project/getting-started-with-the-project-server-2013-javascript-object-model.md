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
# <a name="getting-started-with-the-project-server-2013-javascript-object-model"></a>Introdução ao modelo de objeto do JavaScript do Project Server 2013

No Project Server 2013, o modelo de objeto do JavaScript pode ser usado no Project Online para desenvolvimento móvel e local. Este tópico fornece uma visão geral breve do modelo de objeto JavaScript e descreve como criar uma página de aplicativo que recupera e itera por meio de projetos usando o modelo de objeto do JavaScript.
  
## <a name="using-the-project-server-javascript-object-model"></a>Usar o modelo de objeto do JavaScript do Project Server
<a name="pj15_GetStartedJSOM_UseJSOM"> </a>

Usar o modelo de objeto do JavaScript é uma ótima maneira de criar um aplicativo executado no lado do cliente (ao invés do código de cliente gerenciado, que precisa ser executado remotamente). Os aplicativos podem usar o modelo de objeto do JavaScript para recuperar ou alterar objetos enviando chamadas assíncronas ao servidor. Os aplicativos que usam o modelo de objeto do JavaScript normalmente são implantados como suplementos do SharePoint, páginas de aplicativo e Web Parts personalizadas. Para saber mais, consulte "Tipos de componentes do SharePoint que podem estar em um aplicativo do SharePoint" em [Sites de host, sites de suplemento e componentes do SharePoint no SharePoint 2013](https://msdn.microsoft.com/library/b791cdf5-8aa2-47fa-bc4c-aee437354759%28Office.15%29.aspx).
  
O modelo de objeto do JavaScript implementa a funcionalidade principal do Project Server 2013, mas o modelo de objeto do JavaScript e o modelo de objeto do servidor não têm paridade um para um. O ponto de entrada para o modelo de objeto do JavaScript é o objeto **ProjectContext**, que representa o contexto de cliente do Project Server 2013 e fornece acesso ao conteúdo e à funcionalidade do servidor. O modelo de objeto do JavaScript do Project Server 2013 é definido no arquivo PS.js, localizado no caminho padrão `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS` no servidor de aplicativos. O Project Server 2013 também instala o arquivo PS.Debug.js no mesmo local. O PS.Debug.js é uma versão não reduzida do PS.js que fornece informações do IntelliSense. 
  
O modelo de objeto do JavaScript permite a autenticação de Formulários e todas as solicitações são autenticadas de acordo com o usuário atual. Para saber mais sobre segurança e outras considerações ao criar soluções e aplicativos personalizados, consulte [Autenticação, autorização e segurança no SharePoint 2013](https://msdn.microsoft.com/library/8734790c-eb75-4d78-9604-7cc23b33b693%28Office.15%29.aspx), [Aspectos importantes do cenário de desenvolvimento e arquitetura dos suplementos do SharePoint ](https://msdn.microsoft.com/library/ae96572b-8f06-4fd3-854f-fc312f7f2d88%28Office.15%29.aspx) e [Suplementos do SharePoint em comparação a soluções do SharePoint](https://msdn.microsoft.com/library/0e9efadb-aaf2-4c0d-afd5-d6cf25c4e7a8%28Office.15%29.aspx).
  
> [!NOTE]
> Para acessar remotamente os dados de um site do SharePoint, o SharePoint 2013 oferece uma biblioteca de domínio cruzado que permite fazer chamadas de domínio cruzado no lado do cliente. Para saber mais, consulte [Acessar dados do SharePoint 2013 a partir de suplementos usando a biblioteca de domínio cruzado](https://msdn.microsoft.com/library/bc37ff5c-1285-40af-98ae-01286696242d%28Office.15%29.aspx). 
  
Muitos conceitos e processos para usar o modelo de objeto do JavaScript para o Project Server 2013 se parecem com diferentes modelos de objetos de cliente relacionados. Para saber mais sobre o modelo de objeto de cliente gerenciado do Project Server 2013, consulte **Microsoft.ProjectServer.Client**. Para saber mais sobre o modelo de objeto do JavaScript e o modelo de objeto de cliente gerenciado do SharePoint 2013, consulte [Concluir operações básicas usando código da biblioteca JavaScript no SharePoint 2013](https://msdn.microsoft.com/library/29089af8-dbc0-49b7-a1a0-9e311f49c826%28Office.15%29.aspx), e [Realizar operações básicas usando o código de biblioteca do cliente no SharePoint 2013](https://msdn.microsoft.com/library/5a69c9e3-73bf-4ed5-bc19-182056bdb394%28Office.15%29.aspx).
  
## <a name="walkthrough-creating-an-application-page-that-retrieves-and-iterates-through-projects"></a>Passo a passo: criar uma página de aplicativo que recupera e itera por projetos
<a name="pj15_GetStartedJSOM_UseJSOM"> </a>

Saiba como criar uma página do aplicativo que exibe a ID, o nome e a data de criação de cada projeto publicado em um site.
  
### <a name="prerequisites-for-creating-an-application-page-that-retrieves-and-iterates-through-projects"></a>Pré-requisitos para criar uma página de aplicativo que recupera e itera por projetos
<a name="pj15_GetStartedJSOM_Prereqs"> </a>

Para desenvolver a página de aplicativo descrita neste tópico, instale e configure os seguintes produtos:
  
- SharePoint Server 2013
- Project Server 2013 com pelo menos um projeto publicado
- Visual Studio 2012
- Office Developer Tools para Visual Studio 2012
    
Você também deve ter permissões para implantar a extensão do SharePoint Server 2013 e para recuperar projetos.
  
> [!NOTE]
> Essas instruções pressupõem que você esteja desenvolvendo em um computador que executa o Project Server 2013. 
  
### <a name="creating-the-application-page-in-visual-studio-2012"></a>Criar a página de aplicativo no Visual Studio 2012
<a name="pj15_GetStartedJSOM_CreateVS"> </a>

As etapas a seguir criam um projeto do SharePoint e uma página de aplicativo que contém uma tabela e um rótulo. A tabela exibe informações sobre projetos e o rótulo exibe mensagens de erro.
  
1. No computador que executa o Project Server 2013, execute o Visual Studio 2012 como administrador.
    
2. Crie um projeto vazio do SharePoint 2013 da seguinte maneira:
    
    1. Na caixa de diálogo **Novo Projeto**, escolha **.NET Framework 4.5** na lista suspensa na parte superior da caixa de diálogo. 
        
    2. Na lista de categorias de modelos, escolha a categoria **Office SharePoint** e o modelo **Projeto do SharePoint 2013**. 
        
    3. Nomeie o projeto como GetProjectsJSOM e escolha o botão **OK**. 
        
    4. Na caixa de diálogo **Assistente de Personalização do SharePoint**, selecione **Implantar como uma solução de farm** e, em seguida, escolha o botão **OK**. 
    
3. No Gerenciador de Soluções, edite o valor da propriedade **URL do Site** para que o projeto **ProjectsJSOM** corresponda à URL da instância do Project Web App (por exemplo, `https://ServerName/PWA`).
    
4. Abra o menu de atalho do projeto **GetProjectsJSOM** e, em seguida, adicione a pasta mapeada "Layouts" do SharePoint. 
    
5. Na pasta **Layouts**, abra o menu de atalho da pasta **GetProjectsJSOM** e, em seguida, adicione uma nova página de aplicativo do SharePoint denominada ProjectsList.aspx.
    
   > [!NOTE]
   > Este exemplo não usa o arquivo code-behind que o Visual Studio 2012 cria para a página do aplicativo. 
  
6. Abra o menu de atalho da página **ProjectsList.aspx** e escolha **Definir como item de inicialização**.
    
7. Na marcação da página **ProjectsList.aspx**, defina uma tabela e um espaço reservado de mensagem dentro das marcas "Main" **asp:Content**, como a seguir. 
    
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

### <a name="retrieving-the-projects-collection"></a>Recuperar a coleção de projetos
<a name="pj15_GetStartedJSOM_RetrieveProjs"> </a>

As etapas a seguir recuperam e inicializam a coleção de projetos.
  
1. Após o encerramento da marca **div**, adicione uma marca **SharePoint:ScriptLink** que faz referência ao arquivo PS.js, como a seguir. 
    
   ```HTML
    <SharePoint:ScriptLink name="PS.js" runat="server" ondemand="false" localizable="false" loadafterui="true" />
   ```

2. Abaixo da marca **SharePoint:ScriptLink**, adicione a marca **script**, como a seguir. 
    
   ```HTML
    <script type="text/javascript">
        // Paste the remaining code snippets here, in the order that they are presented.
    </script>
   ```

3. Informe uma variável global para armazenar a coleção de projetos, da maneira a seguir.
    
   ```js
   var projects;
   ```

4. Chame o método **SP.SOD.executeOrDelayUntilScriptLoaded** para garantir que o arquivo PS.js esteja carregado antes de executar o código personalizado. 
    
   ```js
   SP.SOD.executeOrDelayUntilScriptLoaded(GetProjects, "PS.js");
   ```

5. Adicione uma função que conecta-se ao contexto atual e recupera a coleção de projetos, como a seguir.
    
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

   Alguns objetos de clientes, que você recupera pelo contexto, não contêm dados até serem iniciados; ou seja, não é possível acessar valores de propriedades do objeto até que o objeto seja iniciado. Além disso, para as propriedades do tipo **ValueObject**, é necessário solicitar explicitamente a propriedade antes de poder acessar o valor. (Se você tentar acessar uma propriedade antes que seja iniciada, verá a exceção **PropertyOrFieldNotInitializedException**.) 
    
   Para iniciar um objeto, chame o método **load** (ou **loadQuery**) e, depois, o método **executeQueryAsync**. 
    
   - Chamar as funções **load** ou **loadQuery** registra uma solicitação de que você deseja executar no servidor. Passe um parâmetro que representa o objeto que você deseja recuperar. Se você estiver trabalhando com uma propriedade **ValueObject**, então também deve solicitar a propriedade do parâmetro. 
    
   - Chamar a função **executeQueryAsync** envia a solicitação de consulta ao servidor de forma assíncrona. Passe uma função de retorno de chamada bem-sucedida e outra com falha a fim de analisar quando a resposta do servidor é recebida. 
    
   Para reduzir o tráfego de rede, solicite somente as propriedades que você deseja usar chamando a função **load**. Além disso, se estiver trabalhando com vários objetos, agrupe as várias chamadas para a função **load** antes de chamar a função **executeQueryAsync** quando possível. 
    
### <a name="iterating-through-the-projects-collection"></a>Iterar pela coleção de projetos
<a name="pj15_GetStartedJSOM_IterateProjs"> </a>

As etapas a seguir iteram pela coleção de projetos (se a chamada do servidor for bem-sucedida) ou renderizam uma mensagem de erro (se a chamada falhar).
  
1. Adicione uma função de retorno de chamada bem-sucedida que itera pela coleção de projetos, como a seguir.
    
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

2. Adicione uma função de retorno de chamada com falha que processa uma mensagem de erro, como a seguir.
    
    ```js
    function onQueryFailed(sender, args) {
        $get("spanMessage").innerText = 'Request failed: ' + args.get_message();
    }
    ```

3. Para testar a página de aplicativo, na barra de menus, escolha **Depurar**, **Iniciar Depuração**. Se for solicitado a modificar as configurações, escolha **OK**.

<a name="pj15_GetStartedJSOM_CompleteExample"> </a>

## <a name="complete-code-example"></a>Exemplo de código completo

A seguir apresentamos o código completo do arquivo ProjectsList.aspx.
  
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

<a name="pj15_GetStartedJSOM_AR"> </a>

## <a name="see-also"></a>Confira também

- [Criar, recuperar, atualizar e excluir projetos usando o modelo de objeto do JavaScript do Project Server ](create-retrieve-update-delete-projects-using-project-server-javascript.md)  
- [Modelo de objeto no lado do cliente (CSOM) para o Project 2013](client-side-object-model-csom-for-project-2013.md)
- [Introdução ao Project Server CSOM e .NET](getting-started-with-the-project-server-csom-and-net.md)
    

