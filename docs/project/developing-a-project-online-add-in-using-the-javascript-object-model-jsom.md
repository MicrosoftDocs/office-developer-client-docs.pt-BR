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
# <a name="developing-a-project-online-add-in-using-the-javascript-object-model-jsom"></a>Desenvolver um complemento do Project Online usando o Modelo de Objeto do JavaScript (JSOM)

Este artigo descreve o desenvolvimento do Microsoft Project Online Add-in para aprimorar sua experiência com o Project Online. O projeto de desenvolvimento é implementado como um passo a passo. O complemento usado neste artigo lê e exibe os nomes e as IDs de projeto dos projetos publicados da sua conta do Project Online e permite que você faça buscas mais precisas para recuperar tarefas associadas a projetos individuais.
  
Em tempo de executar, a listagem do complemento é semelhante à ilustração a seguir:
  
![Screen shot showing a listing of JSOM projects and tasks Screen]shot showing a(media/766e5914-f048-48f4-9282-291f55e6e90d.png "listing of JSOM projects and tasks")
  
O foco do exemplo é a interação com o Project Online, fazendo consultas e definindo o contexto de cada solicitação do serviço. Os elementos da interface do usuário (UI) recebem atenção mínima. Em vez disso, as listagem de origem fornecem comentários sobre a interface do usuário.
  
> [!NOTE]
> Os arquivos de origem para o exemplo de complemento, um projeto do Visual Studio, estão disponíveis em: https://github.com/OfficeDev/Project-JSOM-List-Projects-Tasks.... . Mantenha os arquivos de origem úteis como referência enquanto você lê o artigo, pois cada um complementa o outro. Os arquivos na com build do projeto do Visual Studio e são executáveis com alterações mínimas substituindo a URL do locatário do Project Online na pasta do PWA. 
  
## <a name="background"></a>Histórico

O Project Online é um serviço do Office 365 que fornece às empresas um PPM (gerenciamento de portfólio de projetos) e uma solução de PMO (escritório de gerenciamento de projetos) para coordenar e gerenciar portfólios, programas e projetos. O Project Online é uma oferta diferente das edições da área de trabalho do Project; ainda assim, o Project Online ainda contém a funcionalidade para manter e acompanhar detalhes do projeto durante toda a vida de um projeto. O Project Online foi criado no SharePoint Online.
  
Um complemento hospedado do Project Online consiste em JavaScript e arquivos de recursos que interagem com a API de Modelo de Objeto do Lado do Cliente. Quando o usuário visita o complemento, o JavaScript e os recursos são baixados e executados no navegador. O complemento faz chamadas assíncronas ao Project Online para interagir com o serviço, seja criando, recuperando, atualizando ou excluindo dados. 
  
O Project Online executa mais uma ação para proteger informações que pertencem a outros locatários do complemento; ou seja, o Project Online cria um site isolado para interagir com as solicitações do complemento. Nenhum código personalizado é executado no host do Project Online. 
  
A configuração de desenvolvimento para os complementos do Project Online usa o tipo de projeto do Visual Studio SharePoint Add-in. O complemento é escrito em JavaScript e usa o modelo de objeto do JavaScript do Project (JSOM) para interagir com o serviço do Project Online. O JSOM herda grande parte de sua funcionalidade do JSOM do SharePoint.
  
> [!NOTE]
> Os complementos podem ser publicados e vendidos na Office Store ou implantados em um catálogo de aplicativos privado no SharePoint. Para saber mais, [confira Implantar e publicar o Seu Complemento do Office.](https://docs.microsoft.com/office/dev/add-ins/publish/publish)
> 
> O complemento usado neste artigo é um exemplo para desenvolvedores; não se destina ao uso em um ambiente de produção. O objetivo principal é mostrar um exemplo de desenvolvimento de aplicativos para o Project Online. 
  
## <a name="prerequisites"></a>Pré-requisitos

Adicione os seguintes itens a um ambiente do Windows com suporte:
  
- **.NET Framework 4.0 ou posterior:** Versões completas da estrutura da versão 4.0 são compatíveis. O site de download é https://msdn.microsoft.com/vstudio/aa496123.aspx.
    
- **Visual Studio 2013 ou posterior:**  
    
   - A edição profissional do Visual Studio 2015 está pronta para ser pronta para uso e está disponível em https://www.visualstudio.com/en-us/products/visual-studio-professional-with-msdn-vs.aspx .
    
   - A edição da comunidade do Visual Studio 2015 está disponível em https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx . Esta edição requer a instalação manual do Microsoft Office Developer Tools para Visual Studio.
    
   As Ferramentas de Desenvolvedor do Microsoft Office para Visual Studio estão disponíveis em https://www.visualstudio.com/en-us/features/office-tools-vs.aspx .
    
- **Uma conta do Project Online:** fornece acesso ao serviço de hospedagem. Confira mais informações sobre como obter uma conta do Project Online em https://products.office.com/en-us/Project/project-online-portfolio-management.
    
   Verifique se o usuário do complemento tem autorização suficiente para acessar alguns projetos no locatário do Project Online. 
    
- **Projetos no site de hospedagem** preenchidos com informações.
    
> [!NOTE]
> O .NET Framework padrão é a estrutura correta a ser usada. Não use o "Perfil de Cliente do .NET Framework 4". 
  
### <a name="set-up-the-visual-studio-project"></a>Configurar o projeto do Visual Studio

A configuração do aplicativo consiste em criar um novo projeto, vincular as bibliotecas apropriadas e declarar os namespaces necessários. O Visual Studio apresenta vários tipos de projetos de desenvolvimento. A seção é breve e muito básica. O valor que tem as informações é agregado em um só lugar.
  
#### <a name="select-a-visual-studio-project"></a>Selecionar um projeto do Visual Studio

Para criar um projeto do tipo apropriado para o complemento, você deve seguir as etapas a seguir. As palavras-chave encontradas na tela têm um **atributo em** negrito: 
  
1. No menu Arquivo, escolha **Arquivo**  >  **Novo**  >  **Projeto.** 
    
2. Nos modelos instalados no painel esquerdo, selecione **C#**  >  **Office/SharePoint**  >  **Web Add-ins**. 
    
3. Na parte superior do painel central, selecione **.NET Framework 4** ou posterior; a versão atual é 4.6. 
    
4. Nos tipos de aplicativos no painel central, escolha **o SharePoint Add-in.** 
    
5. Na seção inferior, especifique o nome e o local do projeto e o nome da solução. 
    
6. Também na seção inferior, marque a caixa **Criar diretório para a solução**. 
    
7. Clique em **OK** para criar o projeto inicial. 
    
O Assistente do Visual Studio faz algumas perguntas de acompanhamento sobre o site de configurações do Project Online (chamado de configurações do SharePoint nas caixas de diálogo) em algumas caixas de diálogo a seguir. Aqui estão as perguntas:
  
1. Qual site do SharePoint você deseja usar para depurar seu complemento? Especifique a URL para seu site do PWA, como https://contoso.sharepoint.com/sites/pwa .
    
2. Como você deseja hospedar seu Add-in do SharePoint? Escolha [X] **Hospedado pelo SharePoint.**
    
   Para saber mais sobre os Complementos do SharePoint, incluindo opções de hospedagem, confira [Os Complementos do SharePoint.](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins)
    
3. Clique em **Avançar**. 
    
A segunda caixa de diálogo adicional solicita que você especifique a versão do SharePoint Online para o complemento: 
  
1. Qual é a versão mais antiga do SharePoint para a qual você deseja direcionar o seu complemento? Escolha [X] S **harePoint-Online**. 
    
2. Clique em **Concluir**. 
    
O Visual Studio cria o projeto e acessa o site do Project Online. 
  
### <a name="enable-sideloading-on-the-project-online-site"></a>Habilitar sideload no site do Project Online

Sideload é o mecanismo para testar e depurar os complementos do Project Online. Você precisa de dois scripts para sideload: um para habilitar o sideload em seu site do Project Online e outro para desabilitar o sideload depois de concluir o teste e a depuração do complemento.
  
Para obter mais informações sobre como configurar o sideload, consulte [Habilitar SideLoading](https://blogs.msdn.microsoft.com/officeapps/2013/12/10/enable-app-sideloading-in-your-non-developer-site-collection/)do aplicativo em seu conjunto de sites não desenvolvedor.
  
> [!NOTE]
> O sideload de aplicativos é um recurso de desenvolvedor/teste. Ele não **se destina ao uso de produção.** Não faça sideload de aplicativos regularmente ou mantenha o sideload de aplicativo habilitado por mais tempo do que você está usando ativamente o recurso. 
  
## <a name="add-content-to-the-add-in-project"></a>Adicionar conteúdo ao projeto do complemento

Depois de criar um projeto e configurar o mecanismo de depuração, adicionar conteúdo ao aplicativo inclui as seguintes tarefas:
  
- Definindo o escopo do aplicativo
    
- Vinculando a biblioteca JSOM
    
- Adicionando elementos de interface do usuário ao add-in
    
- Inicializando e conectando-se ao serviço do Project Online
    
- Recuperar projetos e detalhes/propriedades
    
- Exibindo projetos
    
- Exibindo tarefas para um projeto
    
O projeto do complemento consiste em muitos arquivos. Neste exemplo, você precisará editar os seguintes arquivos: 
  
- AppManifest.xml
    
- Default.aspx
    
- App.js
    
- App.css - opcional; contém definições de estilo desenvolvidas para o complemento
    
Se o locatário do Project Online mudar, como mudar de uma avaliação para um site de assinatura, você poderá atualizar as propriedades do projeto, incluindo a Conexão do Servidor e a URL do Site, usando a Janela Propriedades disponível por meio do comando Exibir Janela  >   Propriedades. 
  
Você também pode adicionar arquivos ao projeto. Nesse caso, você precisará atualizar o arquivo Elements.xml localizado no mesmo grupo (Conteúdo, Imagens, Páginas ou Scripts) para incluir os novos arquivos. Para saber mais sobre os arquivos de projeto, confira Explorar a estrutura do manifesto do aplicativo e [o pacote de um SharePoint Add-in.](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/explore-the-app-manifest-structure-and-the-package-of-a-sharepoint-add-in)
  
### <a name="set-application-scope"></a>Definir escopo do aplicativo

O complemento precisa de níveis de escopo ou permissão definidos antes que o serviço retorne informações nos resultados da consulta. Para este complemento, use o escopo a seguir para o projeto do Visual Studio. Essa alteração é feita no AppManifest.xml na guia Permissões:

|Escopo|Permissão|
|:-----|:-----|
|Vários Projetos (Project Server)  <br/> |Ler  <br/> |
   
Salve o arquivo depois de definir o escopo do aplicativo. Caso contrário, nenhum dado será retornado do serviço. 
  
### <a name="link-the-jsom-library"></a>Vincular a biblioteca JSOM

As bibliotecas do Project Online em tempo de execução, PS.js e PS.debug.js, são fornecidas pelo Project Online e são sempre a versão mais recente. Os complementos JavaScript que usam O JSOM devem se vincular a uma dessas bibliotecas. As definições de vinculação são adicionadas ao arquivo Default.aspx. Os comandos para usar o PS.js e/ou PS.debug.js são parte do código localizado no arquivo App.js arquivo.
  
Adicione o seguinte comando para PS.js ou PS.debug.js no elemento após  `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` o "SharePoint:ScriptLink" para sp.js. 
  
```js
<SharePoint:ScriptLink name="PS.js" runat="server" OnDemand="false" LoadAfterUI="true" Localizable="false" />
```

> [!NOTE]
> O **atributo OnDemand** para PS.js ou PS.debug.js definido como **falso**. 
  
### <a name="add-ui-elements-to-the-add-in"></a>Adicionar elementos de interface do usuário ao add-in

O exemplo de um complemento consiste em alguns componentes. As descrições de elementos estáticos estão localizadas no arquivo Default.aspx. As descrições de elementos dinâmicos e o código para todos os componentes estão localizados App.js arquivo. Para comentários sobre os componentes, consulte as listagem do código-fonte. Aqui está uma lista dos componentes da interface do usuário no complemento:
  
- Título
    
- Verbiage introdutório
    
- Botão para remover tarefas da tabela
    
- Tabela que lista a ID e o nome do projeto e as informações da tarefa.
    
- Botão Tarefas (clonado uma vez para cada projeto) que importa dados de tarefa para a tabela.
    
Para obter detalhes da interface do usuário, como o título e a parte de título da tabela do projeto, consulte o arquivo de projeto Default.aspx.
  
### <a name="initialize-and-connect-to-the-host-system"></a>Inicializar e conectar-se ao sistema host

O App.js arquivo contém o código JavaScript. O complemento é carregado PS.js no navegador e chama a função initializePage. InitializePage recupera um contexto para o ponto de extremidade do Project Online e inicia a função loadProjects.
  
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

### <a name="retrieve-the-projects"></a>Recuperar os projetos

A função loadProjects consulta o serviço para os nomes e IDs do projeto. 
  
O aplicativo recupera o nome do projeto e a ID do projeto. Outras informações sobre o projeto estão disponíveis e podem ser acessadas modificando o método de carregamento para identificar explicitamente as propriedades a serem recuperadas. Um exemplo é fornecido no código como um comentário. 
  
Se a consulta for bem-sucedida, o complemento continuará chamando displayProjects. 
  
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

### <a name="display-the-projects"></a>Exibir os projetos

A função displayProjects cria uma tabela, uma linha por projeto e um botão para mostrar as tarefas do projeto específico. 
  
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
> O loop while acessa as propriedades de ID e nome. Isso é um pouco diferente do projeto do código-fonte que chama uma função que, por sua vez, acessa as mesmas propriedades. 
  
### <a name="display-the-tasks-for-a-project"></a>Exibir as tarefas de um projeto

As tarefas, enquanto fazem parte do complemento, não fazem parte do carregamento inicial. Se o usuário estiver interessado nas tarefas associadas a um projeto, clicar no botão "Mostrar Tarefas" faz com que as tarefas sejam exibidas na lista usando o manipulador de eventos btnLoadTasks. 
  
O manipulador de eventos btnLoadTasks, com a ID de projeto apropriada, solicita as tarefas para o projeto especificado do servidor. Depois de recuperado, btnLoadTasks passa a lista de tarefas para displayTasks para apresentar as tarefas na tela.
  
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

A função displayTasks exibe as tarefas associadas a um projeto especificado imediatamente abaixo da entrada do projeto.
  
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
> O loop while acessa a ID da tarefa e as propriedades do nome. Isso é um pouco diferente do projeto do código-fonte que chama uma função que, por sua vez, acessa as mesmas propriedades. 
  
Exemplo de saída para as tarefas de um único projeto a seguir.
  
![Captura de tela mostrando a saída de uma captura de tela de tarefa]do projeto mostrando a saída de uma tarefa do(media/f6500a3f-000b-4f3e-9be6-9a74d0bea15e.png "projeto")
  
## <a name="see-also"></a>Confira também

Confira a documentação e exemplos relacionados ao desenvolvimento de aplicativos usando o CSOM e Project Online no [Portal de Desenvolvimento do Project](https://developer.microsoft.com/en-us/project).
    


