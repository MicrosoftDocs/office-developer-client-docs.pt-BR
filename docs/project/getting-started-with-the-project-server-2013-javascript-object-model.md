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
# <a name="getting-started-with-the-project-server-2013-javascript-object-model"></a>Introdução ao modelo de objeto JavaScript do Project Server 2013

No Project Server 2013, o modelo de objeto JavaScript pode ser usado no Project Online, desenvolvimento de dispositivos móvel e no local. Este tópico fornece uma breve visão geral do modelo de objeto JavaScript e, em seguida, descreve como criar uma página de aplicativo que recupera e itera projetos usando o modelo de objeto JavaScript.
  
## <a name="using-the-project-server-javascript-object-model"></a>Usando o modelo de objeto JavaScript do Project Server
<a name="pj15_GetStartedJSOM_UseJSOM"> </a>

Usando o modelo de objeto JavaScript é uma ótima maneira de criar um aplicativo que executa o lado do cliente (em oposição ao código do cliente gerenciado que precisa ser executado remotamente). Aplicativos podem usar o modelo de objeto JavaScript para recuperar ou alterar objetos enviando chamadas assíncronas para o servidor. Normalmente, os aplicativos que usam o modelo de objeto JavaScript são implantados como personalizado suplementos do SharePoint, Web Parts e páginas de aplicativo. Para obter mais informações, consulte "Tipos de componentes do SharePoint que podem estar em um aplicativo para SharePoint" em [webs de Host, suplemento webs e os componentes do SharePoint no SharePoint 2013](http://msdn.microsoft.com/library/b791cdf5-8aa2-47fa-bc4c-aee437354759%28Office.15%29.aspx).
  
O modelo de objeto JavaScript implementa a funcionalidade principal do Project Server 2013, mas o modelo de objeto JavaScript e o modelo de objeto de servidor não têm um-para-paridade. O ponto de entrada para o modelo de objeto JavaScript é o objeto **ProjectContext** , que representa o contexto de cliente do Project Server 2013 e fornece acesso ao conteúdo do servidor e a funcionalidade. O modelo de objeto JavaScript para o Project Server 2013 é definido no arquivo PS.js, que está localizado no caminho padrão `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS` no servidor de aplicativos. Project Server 2013 também instala o PS. Arquivo Debug no mesmo local. PS. Debug é uma versão unminified do PS.js que fornece informações de IntelliSense. 
  
O modelo de objeto JavaScript permite a autenticação de formulários e todas as solicitações sejam autenticadas como o usuário atual. Para obter mais informações sobre segurança e outras considerações para aplicativos personalizados de criação e soluções, consulte [autenticação, autorização e segurança no SharePoint 2013](http://msdn.microsoft.com/library/8734790c-eb75-4d78-9604-7cc23b33b693%28Office.15%29.aspx), [de aspectos importantes da arquitetura do SharePoint Add-in e desenvolvimento Paisagem](http://msdn.microsoft.com/library/ae96572b-8f06-4fd3-854f-fc312f7f2d88%28Office.15%29.aspx)e [suplementos do SharePoint em comparação com soluções do SharePoint](http://msdn.microsoft.com/library/0e9efadb-aaf2-4c0d-afd5-d6cf25c4e7a8%28Office.15%29.aspx).
  
> [!NOTE]
> Para acessar os dados de um site do SharePoint remotamente, o SharePoint 2013 fornece uma biblioteca de entre domínios que permite que você faça chamadas do lado do cliente entre domínios. Para obter mais informações, consulte [data de acesso do SharePoint 2013 de suplementos usando a biblioteca de domínio cruzado](http://msdn.microsoft.com/library/bc37ff5c-1285-40af-98ae-01286696242d%28Office.15%29.aspx). 
  
Muitos conceitos e processos para usar o modelo de objeto JavaScript para o Project Server 2013 se parecem com aqueles nos modelos de objeto do cliente relacionados. Para obter mais informações sobre o modelo de objeto do cliente gerenciado do Project Server 2013, consulte **Microsoft.ProjectServer.Client**. Para obter mais informações sobre o modelo de objeto do SharePoint 2013JavaScript e o modelo de objeto do cliente gerenciado, consulte [concluir operações básicas usando o código JavaScript da biblioteca no SharePoint 2013](http://msdn.microsoft.com/library/29089af8-dbc0-49b7-a1a0-9e311f49c826%28Office.15%29.aspx) e [completa operações básicas usando o cliente do SharePoint 2013 código de biblioteca](http://msdn.microsoft.com/library/5a69c9e3-73bf-4ed5-bc19-182056bdb394%28Office.15%29.aspx).
  
## <a name="walkthrough-creating-an-application-page-that-retrieves-and-iterates-through-projects"></a>Passo a passo: Criando uma página do aplicativo que recupera e itera através de projetos
<a name="pj15_GetStartedJSOM_UseJSOM"> </a>

Saiba como criar uma página que exibe o ID, o nome e a data de criação de cada projeto publicado em um site do aplicativo.
  
### <a name="prerequisites-for-creating-an-application-page-that-retrieves-and-iterates-through-projects"></a>Pré-requisitos para a criação de página de um aplicativo que recupera e itera através de projetos
<a name="pj15_GetStartedJSOM_Prereqs"> </a>

Para desenvolver a página do aplicativo que está descrita neste tópico, instale e configure os seguintes produtos:
  
- SharePoint Server 2013
- Project Server 2013 com pelo menos um projeto publicado
- Visual Studio 2012
- Office Developer Tools para Visual Studio 2012
    
Você também deve ter permissões para implantar a extensão para o SharePoint Server 2013 e para recuperar os projetos.
  
> [!NOTE]
> Estas instruções pressupõem que você estiver desenvolvendo no computador que está executando o Project Server 2013. 
  
### <a name="creating-the-application-page-in-visual-studio-2012"></a>Criando a página de aplicativo no Visual Studio 2012
<a name="pj15_GetStartedJSOM_CreateVS"> </a>

As etapas a seguir criam um projeto do SharePoint e a página de um aplicativo que contém uma tabela e rótulo. A tabela exibe informações sobre os projetos e o rótulo exibe mensagens de erro.
  
1. No computador que está executando o Project Server 2013, execute o Visual Studio 2012 como administrador.
    
2. Crie um projeto vazio do SharePoint 2013, da seguinte maneira:
    
    1. Na caixa de diálogo **Novo projeto**, escolha o **.NET Framework 4.5** da lista suspensa na parte superior da caixa de diálogo. 
        
    2. Na lista de categorias de modelo, escolha a categoria **SharePoint do Office** e, em seguida, escolha o modelo de **Projeto do SharePoint 2013** . 
        
    3. Nome do projeto GetProjectsJSOM e escolha o botão **Okey** . 
        
    4. Na caixa de diálogo **Assistente de personalização do SharePoint** , selecione **implantar como uma solução de farm**e escolha o botão **Okey** . 
    
3. No Solution Explorer, edite o valor da propriedade **URL do Site** para o projeto **ProjectsJSOM** coincidir com a URL da instância do Project Web App (por exemplo, `http://ServerName/PWA`).
    
4. Abra o menu de atalho para o projeto **GetProjectsJSOM** e, em seguida, adicionar uma lista do SharePoint "Layouts" mapeado a pasta. 
    
5. Na pasta **Layouts** , abra o menu de atalho para a pasta **GetProjectsJSOM** e, em seguida, adicione uma nova página de aplicativos do SharePoint denominada ProjectsList.aspx.
    
   > [!NOTE]
   > Este exemplo não usa o arquivo de code-behind que cria do Visual Studio 2012 para a página do aplicativo. 
  
6. Abra o menu de atalho para a página **ProjectsList.aspx** e escolha **definida como Item de inicialização**.
    
7. Na marcação para a página **ProjectsList.aspx** , defina uma tabela e um espaço reservado de mensagem dentro das marcas de **asp: Content** "Main", da seguinte maneira. 
    
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

### <a name="retrieving-the-projects-collection"></a>Recuperando a coleção projects
<a name="pj15_GetStartedJSOM_RetrieveProjs"> </a>

As etapas a seguir recuperar e inicializar a coleção projects.
  
1. Após o fechamento **div** marca, adicione uma marca de **SharePoint:ScriptLink** que referencia o arquivo de PS.js, da seguinte maneira. 
    
   ```HTML
    <SharePoint:ScriptLink name="PS.js" runat="server" ondemand="false" localizable="false" loadafterui="true" />
   ```

2. Abaixo da tag **SharePoint:ScriptLink** , adicione marcas de **script** , da seguinte maneira. 
    
   ```HTML
    <script type="text/javascript">
        // Paste the remaining code snippets here, in the order that they are presented.
    </script>
   ```

3. Declare uma variável global para armazenar o conjunto de projetos, da seguinte maneira.
    
   ```js
   var projects;
   ```

4. Chamar o **SP. SOD.executeOrDelayUntilScriptLoaded** método para garantir que o arquivo PS.js seja carregado antes de seu código personalizado é executado. 
    
   ```js
   SP.SOD.executeOrDelayUntilScriptLoaded(GetProjects, "PS.js");
   ```

5. Adicione uma função que se conecta ao contexto atual e recupera a coleção projects, da seguinte maneira.
    
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

   Alguns objetos de cliente que você recuperar por meio do contexto não contêm nenhum dado até que eles são inicializados; ou seja, você não pode acessar os valores de propriedade do objeto até que o objeto é inicializado. Além disso, para propriedades do tipo **ValueObject**, você deve solicitar explicitamente a propriedade antes de poder acessar seu valor. (Se você tentar acessar uma propriedade antes de ele é inicializado, você receberá uma exceção **PropertyOrFieldNotInitializedException** .) 
    
   Para inicializar um objeto, você chamar o método **load** (ou o método **loadQuery** ) e, em seguida, o método **executeQueryAsync** . 
    
   - Chamar a função **de carga** ou a função **loadQuery** registra uma solicitação que você deseja executar no servidor. Você passar um parâmetro que representa o objeto que você deseja recuperar. Se você estiver trabalhando com uma propriedade **ValueObject** , em seguida, você também solicitar a propriedade no parâmetro. 
    
   - Chamar a função **executeQueryAsync** envia a solicitação de consulta para o servidor de forma assíncrona. Você passar uma função de retorno de chamada de sucesso e uma função de retorno de chamada de falha para invocar quando a resposta do servidor é recebida. 
    
   Para reduzir o tráfego de rede, solicite apenas as propriedades que você deseja trabalhar com quando se chama a função **de carga** . Além disso, se você estiver trabalhando com vários objetos, agrupe várias chamadas para a função **de carga** antes de chamar a função **executeQueryAsync** quando possível. 
    
### <a name="iterating-through-the-projects-collection"></a>A iteração através da coleção de projetos
<a name="pj15_GetStartedJSOM_IterateProjs"> </a>

As etapas a seguir percorrer a coleção projects (se a chamada do servidor é bem-sucedida) ou uma mensagem de erro de renderização (se a chamada falhar).
  
1. Adicione uma função de retorno de chamada de sucesso que itera através da coleção de projetos, da seguinte maneira.
    
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

2. Adicione uma função de retorno de chamada falha que renderiza a uma mensagem de erro, da seguinte maneira.
    
    ```js
    function onQueryFailed(sender, args) {
        $get("spanMessage").innerText = 'Request failed: ' + args.get_message();
    }
    ```

3. Para testar a página de aplicativo, na barra de menus, escolha **Depurar**, **Iniciar depuração**. Se você for solicitado para modificar o arquivo Web. config, escolha **Okey**.

<a name="pj15_GetStartedJSOM_CompleteExample"> </a>

## <a name="complete-code-example"></a>Exemplo de código completo

A seguir é o código completo do arquivo ProjectsList.aspx exe.
  
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

- [Criar, recuperar, atualizar e excluir projetos usando o modelo de objeto JavaScript do Project Server](create-retrieve-update-delete-projects-using-project-server-javascript.md)  
- [Modelo de objeto do cliente (CSOM) para o Project 2013](client-side-object-model-csom-for-project-2013.md)
- [Introdução ao Project Server CSOM e .NET](getting-started-with-the-project-server-csom-and-net.md)
    

