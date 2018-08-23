---
title: Desenvolvendo um suplemento Project Online usando o modelo de objeto JavaScript (JSOM)
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4a4b1ad2-de46-421d-a698-53c20c90b93a
description: Este artigo descreve o desenvolvimento de suplemento Microsoft Project Online para aperfeiçoar sua experiência ao Project Online. O projeto de desenvolvimento é implementado como um passo a passo. O suplemento usado para este artigo lê e exibe os nomes de projeto e as identificações dos projetos publicados de sua conta do Project Online e permite fazer drill para baixo até tarefas recuperar associadas aos projetos individuais.
ms.openlocfilehash: ea5c7e3f3d20aa6bf5b6bb77a18eb87d06f549e1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572540"
---
# <a name="developing-a-project-online-add-in-using-the-javascript-object-model-jsom"></a>Desenvolvendo um suplemento Project Online usando o modelo de objeto JavaScript (JSOM)

Este artigo descreve o desenvolvimento de suplemento Microsoft Project Online para aperfeiçoar sua experiência com o Project Online. O projeto de desenvolvimento é implementado como um passo a passo. O suplemento usado para este artigo lê e exibe os nomes de projeto e as identificações dos projetos publicados de sua conta do Project Online e permite fazer drill para baixo até tarefas recuperar associadas aos projetos individuais.
  
Em tempo de execução, a listagem de suplemento parece com a ilustração a seguir:
  
![Captura de tela mostrando uma listagem de JSOM projetos e tarefas] (media/766e5914-f048-48f4-9282-291f55e6e90d.png "Captura de tela mostrando uma listagem de JSOM projetos e tarefas")
  
O foco do exemplo é a interação com o Project Online, fazendo consultas e definindo o contexto de cada solicitação do serviço. Elementos de interface do usuário recebem atenção mínima. Em vez disso, as listagens de origem fornecem comentários sobre a interface do usuário.
  
> [!NOTE]
> Os arquivos de origem para o exemplo suplemento, um projeto do Visual Studio, estão disponíveis em: https://github.com/OfficeDev/Project-JSOM-List-Projects-Tasks..... Manter os arquivos de origem úteis como uma referência enquanto você leia o artigo, como cada complementa o outro. Os arquivos no Visual Studio compilação do projeto e são executáveis com alterações mínimas — substituindo a URL para seu locatário do Project Online para baixo até a pasta do PWA. 
  
## <a name="background"></a>Background

Project Online é um serviço do Office 365 que fornece as empresas com um gerenciamento de portfólio de projeto (PPM) e a solução do project management office (PMO) para coordenar e gerenciar portfólios, programas e projetos. Project Online é uma oferta de diferente que as edições da área de trabalho do projeto; ainda assim, Project Online ainda contém a funcionalidade para manter e rastrear detalhes do projeto em toda a duração de um projeto. Project Online é baseado no SharePoint Online.
  
Um suplemento Project Online hospedado consiste em arquivos JavaScript e recursos que interagem com a API de cliente-lado-modelo de objeto. Quando o usuário visita o suplemento, o JavaScript e os recursos são baixados e executados dentro do navegador. O suplemento faz chamadas assíncronas com o Project Online para interagir com o serviço, se a criação, recuperação, atualizem ou excluam dados. 
  
Project Online realiza uma ação de mais para proteger as informações que pertence a outros locatários add-in do; Isto é, Project Online cria um site isolado para interagir com as solicitações do suplemento. Nenhum código personalizado é executado no host do Project Online. 
  
A configuração de desenvolvimento para Project Online suplementos usa o tipo de projeto Visual Studio SharePoint Add-in. O suplemento é gravado em JavaScript e usa o modelo de objeto JavaScript do projeto (JSOM) para interagir com o serviço do Project Online. O JSOM herda grande parte da sua funcionalidade JSOM do SharePoint.
  
> [!NOTE]
> Suplementos podem ser publicados e vendidos no Office Store ou implantados em um catálogo de aplicativos privado no SharePoint. Para obter mais informações, consulte [Deploy e publicar o Add-in Office](https://docs.microsoft.com/en-us/office/dev/add-ins/publish/publish).
> 
> O suplemento usado neste artigo é uma amostra para desenvolvedores; ele não é projetado para uso em um ambiente de produção. O objetivo principal é mostrar um exemplo de desenvolvimento de aplicativos para o Project Online. 
  
## <a name="prerequisites"></a>Pré-requisitos

Adicione os seguintes itens em um ambiente do Windows com suporte:
  
- **.NET framework 4.0 ou posterior**: as versões completas do framework da versão 4.0 são compatíveis. O site de download está https://msdn.microsoft.com/en-us/vstudio/aa496123.aspx.
    
- **Visual Studio 2013 ou posterior**:  
    
   - A professional edition do Visual Studio de 2015 está pronto para ir fora da caixa e está disponível em https://www.visualstudio.com/en-us/products/visual-studio-professional-with-msdn-vs.aspx.
    
   - A edição de comunidade do 2015 do Visual Studio está disponível em https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx. Nesta edição requer instalação manual das ferramentas de desenvolvedor do Microsoft Office para Visual Studio.
    
   O Microsoft Office Developer Tools para o Visual Studio estão disponível em https://www.visualstudio.com/en-us/features/office-tools-vs.aspx.
    
- **Conta uma Project Online**: Isso oferece acesso ao serviço de hospedagem. Para obter mais informações sobre como adquirir uma conta do Project Online, consulte https://products.office.com/en-us/Project/project-online-portfolio-management.
    
   Certifique-se de que o usuário de suplemento tenha autorização suficiente para acessar alguns projetos no Project Online inquilino. 
    
- **Projetos no site de hospedagem** que são preenchidas com informações.
    
> [!NOTE]
> O padrão do .NET Framework é uma estrutura para usar correta. Não use o ".NET Framework 4 Client Profile". 
  
### <a name="set-up-the-visual-studio-project"></a>Configurar o projeto do Visual Studio

A instalação do aplicativo consiste em criar um novo projeto, vinculando nas bibliotecas apropriadas e declarando os namespaces necessários. O Visual Studio apresenta vários tipos de projetos de desenvolvimento. A seção é breve e muito básico. O valor está tendo a informação é unidas em um único local.
  
#### <a name="select-a-visual-studio-project"></a>Selecione um projeto do Visual Studio

Para criar um projeto do tipo apropriado para o suplemento, você deve fazer as seguintes etapas. Palavras-chave, encontradas na tela tem um atributo **negrito** : 
  
1. No menu Arquivo, escolha **arquivo** > **New** > **Project**. 
    
2. A partir de modelos de Installed no painel esquerdo, selecione **c#** > **Office/SharePoint** > **Web suplementos**. 
    
3. Na parte superior do painel central, selecione o **.NET Framework 4** ou posterior; a versão atual é 4.6. 
    
4. A partir de tipos de aplicativos, no painel central, escolha **do suplemento do SharePoint**. 
    
5. Na seção inferior, especifique um nome e local para o projeto e o nome da solução. 
    
6. Também na seção inferior, marque a caixa de **criar diretório para a solução** . 
    
7. Clique em **Okey** para criar o projeto inicial. 
    
O Assistente do Visual Studio pergunta algumas perguntas de acompanhamento sobre o site de configurações (configurações do SharePoint chamados nas caixas de diálogo) Project Online de duas caixas de diálogo que seguem. Aqui estão as perguntas:
  
1. Qual site do SharePoint você deseja usar para depuração seu suplemento? Especificar a URL para seu site do PWA, tais como https://contoso.sharepoint.com/sites/pwa.
    
2. Como você deseja hospedar o Add-in do SharePoint? Escolha [X] **hospedado no SharePoint**.
    
   Para obter mais informações sobre o SharePoint Add-ins, incluindo opções de hospedagem, consulte [Add-ins do SharePoint](https://docs.microsoft.com/en-us/sharepoint/dev/sp-add-ins/sharepoint-add-ins).
    
3. Clique em **Avançar**. 
    
A segunda caixa de diálogo adicional solicita que você especificar a versão do SharePoint Online para o suplemento: 
  
1. Qual é a versão mais antiga do SharePoint que você deseja que seu suplemento para o destino? Escolha [X] S **HarePoint on-line**. 
    
2. Click **Finish**. 
    
Visual Studio cria o projeto e acessa o site do Project Online. 
  
### <a name="enable-sideloading-on-the-project-online-site"></a>Habilitar sideloading no site do Project Online

Sideloading é o mecanismo para testar e depurar suplementos Project Online. Você precisa de dois scripts para sideloading: um para habilitar sideloading em seu site do Project Online e outro para desabilitar sideloading depois que terminar de teste e depuração o add-in.
  
Para obter mais informações sobre como configurar sideloading, consulte [Habilitar app SideLoading em seu conjunto de sites não desenvolvedores](https://blogs.msdn.microsoft.com/officeapps/2013/12/10/enable-app-sideloading-in-your-non-developer-site-collection/).
  
> [!NOTE]
> Aplicativos sideloading é um recurso de desenvolvedor/teste. É **não pretendido para uso em produção**. Execute aplicativos de sideload não regularmente ou mantenha sideloading aplicativo habilitado para mais do que você estiver usando ativamente o recurso. 
  
## <a name="add-content-to-the-add-in-project"></a>Adicionar conteúdo ao projeto de suplemento

Após criar um projeto e configurando o mecanismo de depuração, a adição de conteúdo para o aplicativo inclui as seguintes tarefas:
  
- Configurando o escopo de aplicativo
    
- Vinculando a biblioteca JSOM
    
- Adicionando elementos de interface do usuário para o suplemento
    
- Inicializando e conectando-se ao serviço Project Online
    
- Recuperando detalhes/propriedades e projetos
    
- Exibindo projetos
    
- A exibição de tarefas para um projeto
    
O projeto de suplemento consiste em vários arquivos. Neste exemplo, você precisará editar os arquivos a seguir: 
  
- AppManifest.xml
    
- Default. aspx
    
- App.js
    
- App.CSS - opcional; contém as definições de estilo desenvolvidas para o suplemento
    
Se o Project Online inquilino muda, como mover de uma versão de avaliação para um site de inscrição, você pode atualizar as propriedades do projeto, incluindo a Conexão do servidor e a URL do Site, usando a janela de propriedades disponíveis por meio do **modo de exibição** > **Propriedades Janela** comando. 
  
Você também pode adicionar arquivos ao projeto. Nesse caso, você precisará atualizar o arquivo Elements XML localizado no mesmo grupo (conteúdo, imagens, páginas ou Scripts) para incluir os novos arquivos. Para obter mais informações sobre os arquivos do projeto, consulte [Explore a estrutura de manifesto de aplicativo e o pacote de um suplemento do SharePoint](https://docs.microsoft.com/en-us/sharepoint/dev/sp-add-ins/explore-the-app-manifest-structure-and-the-package-of-a-sharepoint-add-in).
  
### <a name="set-application-scope"></a>Definir o escopo do aplicativo

O suplemento precisa de níveis de permissão ou escopo definidos antes que o serviço retorna informações nos resultados da consulta. Para este suplemento, use o seguinte escopo para o projeto do Visual Studio. Esta alteração é feita no arquivo AppManifest.xml na guia permissões:

|Escopo|Permissão|
|:-----|:-----|
|Vários projetos (Project Server)  <br/> |Read  <br/> |
   
Salve o arquivo após a configuração do escopo do aplicativo. Caso contrário, nenhum dado será retornado do serviço. 
  
### <a name="link-the-jsom-library"></a>Vincular a biblioteca JSOM

As bibliotecas de Project Online runtime, PS.js e PS.debug.js, são fornecidas pelo Project Online e são sempre a versão mais recente. Suplementos JavaScript usam JSOM devem link com uma dessas bibliotecas. As definições de vinculação são adicionadas no arquivo default. aspx. Os comandos para usar o PS.js e/ou PS.debug.js fazem parte do código localizado no arquivo App.js.
  
Adicione o seguinte comando para definição de PS.js ou PS.debug.js no `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` elemento seguindo o "SharePoint:ScriptLink" sp.js. 
  
```js
<SharePoint:ScriptLink name="PS.js" runat="server" OnDemand="false" LoadAfterUI="true" Localizable="false" />
```

> [!NOTE]
> O atributo **OnDemand** para PS.js ou PS.debug.js é definida como **false**. 
  
### <a name="add-ui-elements-to-the-add-in"></a>Adicionar elementos de interface do usuário para o suplemento

O suplemento de exemplo consiste em alguns componentes. Descrições de elemento estático estão localizadas no arquivo default. aspx. Descrições de elemento dinâmico e código para todos os componentes estão localizados no arquivo App.js. Para comentários sobre os componentes, consulte as listagens de código fonte. Aqui está uma lista dos componentes de UI do add-in:
  
- Title
    
- Verbosidade introdutória
    
- Botão para remover as tarefas da tabela
    
- Tabela que lista a ID do projeto e o nome e as informações de tarefa.
    
- Botão (clonada uma vez para cada projeto) que importa dados de tarefa para a tabela de tarefas.
    
Para obter detalhes da interface do usuário, como o título e a parte do cabeçalho da tabela project, consulte o arquivo de projeto default. aspx.
  
### <a name="initialize-and-connect-to-the-host-system"></a>Inicializar e conecte-se para o sistema host

O arquivo de App.js contém o código JavaScript. O suplemento carrega PS.js no navegador e, em seguida, chama a função initializePage. InitializePage recupera um contexto para o ponto de extremidade do Project Online e inicia a função loadProjects.
  
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

A função loadProjects consulta o serviço de nomes de projeto e IDs. 
  
O aplicativo recupera o nome do projeto e o project ID. Outras informações sobre o projeto está disponíveis e podem ser acessadas por modificar o método load para identificar explicitamente propriedades a serem recuperadas. Um exemplo é fornecido no código como um comentário. 
  
Se a consulta for bem sucedido, o suplemento continua chamando displayProjects. 
  
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
> O loop while acessos a ID e propriedades de nome. Isso é ligeiramente diferente projeto código-fonte que chama uma função que, por sua vez, acessa as mesmas propriedades. 
  
### <a name="display-the-tasks-for-a-project"></a>Exibir as tarefas de um projeto

As tarefas, enquanto a parte do add-in, não fazem parte do carregamento inicial. Se o usuário está interessado nas tarefas associadas a um projeto, clicando no botão "Mostrar tarefas" faz com que as tarefas a ser exibido na lista usando o manipulador de eventos btnLoadTasks. 
  
O manipulador de eventos btnLoadTasks, com a ID de projeto apropriado, solicita as tarefas do projeto especificado do servidor. Depois que recuperados, o btnLoadTasks passa a lista de tarefas para displayTasks para apresentar as tarefas na tela.
  
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

A função displayTasks exibe as tarefas associadas a um projeto especificado imediatamente abaixo da entrada de projeto.
  
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
> O loop while acessos a identificação da tarefa e propriedades de nome. Isso é ligeiramente diferente projeto código-fonte que chama uma função que, por sua vez, acessa as mesmas propriedades. 
  
Saída de exemplo para as tarefas de um único projeto segue.
  
![Captura de tela mostrando a saída para uma tarefa de projeto] (media/f6500a3f-000b-4f3e-9be6-9a74d0bea15e.png "Captura de tela mostrando a saída para uma tarefa de projeto")
  
## <a name="see-also"></a>Confira também

Para documentação e exemplos relacionados ao Project Online e desenvolvimento de aplicativos usando CSOM, consulte o [Portal de desenvolvimento do Project](https://developer.microsoft.com/en-us/project).
    


