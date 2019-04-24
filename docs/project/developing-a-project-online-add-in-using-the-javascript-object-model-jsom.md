---
title: Desenvolver um suplemento do Project online usando o modelo de objeto do JavaScript (JSOM)
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4a4b1ad2-de46-421d-a698-53c20c90b93a
description: Este artigo descreve o desenvolvimento de suplementos do Microsoft Project online para aprimorar sua experiência com o Project online. O projeto de desenvolvimento é implementado como um passo a passo. O suplemento usado neste artigo lê e exibe os nomes de projeto e as IDs dos projetos publicados da sua conta do Project online e permite que você faça uma busca detalhada para recuperar tarefas associadas a projetos individuais.
ms.openlocfilehash: 0a472a6300f18aaa65649f44d944445642a59e1a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322679"
---
# <a name="developing-a-project-online-add-in-using-the-javascript-object-model-jsom"></a>Desenvolver um suplemento do Project online usando o modelo de objeto do JavaScript (JSOM)

Este artigo descreve o desenvolvimento de suplementos do Microsoft Project online para aprimorar sua experiência com o Project online. O projeto de desenvolvimento é implementado como um passo a passo. O suplemento usado neste artigo lê e exibe os nomes de projeto e as IDs dos projetos publicados da sua conta do Project online e permite que você faça uma busca detalhada para recuperar tarefas associadas a projetos individuais.
  
Em tempo de execução, a lista de suplementos é semelhante à ilustração a seguir:
  
![Captura de tela mostrando uma listagem de projetos e tarefas do JSOM] (media/766e5914-f048-48f4-9282-291f55e6e90d.png "Captura de tela mostrando uma listagem de projetos e tarefas do JSOM")
  
O foco do exemplo é a interação com o Project online, fazendo consultas e Configurando o contexto de cada solicitação do serviço. Os elementos da interface do usuário (UI) recebem o mínimo de atenção. Em vez disso, as listagens de origem fornecem comentários sobre a interface do usuário.
  
> [!NOTE]
> Os arquivos de origem do suplemento de exemplo, um projeto do Visual Studio, estão disponíveis em: https://github.com/OfficeDev/Project-JSOM-List-Projects-Tasks..... Mantenha os arquivos de origem úteis como referência enquanto você lê o artigo, como cada um complementa o outro. Os arquivos na compilação do projeto do Visual Studio e são executáveis com alterações mínimas, substituindo a URL para o locatário do Project online até a pasta do PWA. 
  
## <a name="background"></a>Background

O Project online é um serviço do Office 365 que oferece às empresas uma solução de gerenciamento de portfólio de projetos (PPM) e de gerenciamento de projetos (PMO) para coordenar e gerenciar portfólios, programas e projetos. O Project online é uma oferta diferente da do Project desktop Editions; no entanto, o Project online ainda contém a funcionalidade para manter e acompanhar detalhes do projeto durante toda a vida de um projeto. O Project online é criado no SharePoint Online.
  
Um suplemento hospedado no Project online consiste em arquivos de recurso e JavaScript que interagem com a API de modelo de objeto do lado do cliente. Quando o usuário visita o suplemento, o JavaScript e os recursos são baixados e executados no navegador. O suplemento faz chamadas assíncronas para o Project online para interagir com o serviço, seja criando, recuperando, atualizando ou excluindo dados. 
  
O Project online executa mais uma ação para proteger informações que pertencem a outros locatários do suplemento; especificamente, o Project online cria um site isolado para interagir com as solicitações do suplemento. Nenhum código personalizado é executado no host do Project online. 
  
A configuração de desenvolvimento para suplementos do Project online usa o tipo de projeto de suplemento do Visual Studio SharePoint. O suplemento é escrito em JavaScript e usa o modelo de objeto JavaScript (JSOM) do Project para interagir com o serviço do Project online. O JSOM herda grande parte de sua funcionalidade do JSOM do SharePoint.
  
> [!NOTE]
> Os suplementos podem ser publicados e vendidos na Office Store ou implantados em um catálogo de aplicativos particulares no SharePoint. Para obter mais informações, consulte [implantar e publicar seu suplemento do Office](https://docs.microsoft.com/office/dev/add-ins/publish/publish).
> 
> O suplemento usado neste artigo é um exemplo para desenvolvedores; Ele não se destina ao uso em um ambiente de produção. O principal objetivo é mostrar um exemplo de desenvolvimento de aplicativos para o Project online. 
  
## <a name="prerequisites"></a>Pré-requisitos

Adicione os seguintes itens a um ambiente do Windows compatível:
  
- **.NET Framework 4,0 ou posterior**: as versões completas da estrutura da versão 4,0 são compatíveis. O site de download é https://msdn.microsoft.com/vstudio/aa496123.aspx.
    
- **Visual Studio 2013 ou posterior**:  
    
   - A edição profissional do Visual Studio 2015 está pronta para ser acessada e está disponível em https://www.visualstudio.com/en-us/products/visual-studio-professional-with-msdn-vs.aspx.
    
   - A edição da Comunidade do Visual Studio 2015 está disponível https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspxem. Esta edição requer a instalação manual do Microsoft Office Developer Tools para Visual Studio.
    
   As ferramentas de desenvolvedor do Microsoft Office para Visual Studio estão https://www.visualstudio.com/en-us/features/office-tools-vs.aspxdisponíveis em.
    
- **Uma conta do Project online**: fornece acesso ao serviço de hospedagem. Confira mais informações sobre como obter uma conta do Project Online em https://products.office.com/en-us/Project/project-online-portfolio-management.
    
   Certifique-se de que o usuário do suplemento tenha autorização suficiente para acessar alguns projetos no locatário do Project online. 
    
- **Projetos no site de hospedagem** que são preenchidos com informações.
    
> [!NOTE]
> O .NET Framework padrão é a estrutura correta a ser usada. Não use o ".NET Framework 4 Client Profile". 
  
### <a name="set-up-the-visual-studio-project"></a>Configurar o projeto do Visual Studio

A instalação do aplicativo consiste em criar um novo projeto, vincular as bibliotecas apropriadas e declarar os namespaces necessários. O Visual Studio apresenta vários tipos de projetos de desenvolvimento. A seção é breve e muito básica. O valor tem as informações são agrupadas em um só lugar.
  
#### <a name="select-a-visual-studio-project"></a>Selecionar um projeto do Visual Studio

Para criar um projeto do tipo apropriado para o suplemento, você deve executar as etapas a seguir. Palavras-chave encontradas na tela têm um atributo **negrito** : 
  
1. No menu arquivo, escolha **arquivo** > **novo** > **projeto**. 
    
2. Nos modelos instalados no painel esquerdo, selecione**suplementos da Web****do Office/SharePoint do** >  **C#** > . 
    
3. Na parte superior do painel central, selecione **.NET Framework 4** ou posterior; a versão atual é 4,6. 
    
4. Nos tipos de aplicativos no painel central, escolha **suplemento do SharePoint**. 
    
5. Na seção inferior, especifique o nome e o local do projeto e o nome da solução. 
    
6. Também na seção inferior, marque a caixa **Criar diretório para a solução**. 
    
7. Clique em **OK** para criar o projeto inicial. 
    
O assistente do Visual Studio faz algumas perguntas de acompanhamento sobre o site de configurações do Project online (chamado de configurações do SharePoint nas caixas de diálogo) em algumas caixas de diálogo que se seguem. Aqui estão as perguntas:
  
1. Qual site do SharePoint você deseja usar para depurar seu suplemento? Especifique a URL para o site do PWA, como https://contoso.sharepoint.com/sites/pwa.
    
2. Como você deseja hospedar seu suplemento do SharePoint? Escolha [X] **hospedado pelo SharePoint**.
    
   Para obter mais informações sobre os suplementos do SharePoint, incluindo opções de hospedagem, confira [suplementos do SharePoint](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins).
    
3. Clique em **Avançar**. 
    
A segunda caixa de diálogo adicional solicita que você especifique a versão do SharePoint Online para o suplemento: 
  
1. Qual é a versão mais antiga do SharePoint para a qual você deseja que o suplemento direcione? Escolha [X] S **harePoint-online**. 
    
2. Clique em **Concluir**. 
    
O Visual Studio cria o projeto e acessa o site do Project online. 
  
### <a name="enable-sideloading-on-the-project-online-site"></a>Habilitar o Sideload no site do Project online

O Sideload é o mecanismo para testar e depurar os suplementos do Project online. Você precisa de dois scripts para o Sideload: um para habilitar o Sideload no site do Project online e outro para desabilitar o Sideload depois que você terminar de testar e depurar o suplemento.
  
Para obter mais informações sobre como configurar o Sideload, consulte [habilitar o aplicativo Sideload em seu conjunto de sites não desenvolvedor](https://blogs.msdn.microsoft.com/officeapps/2013/12/10/enable-app-sideloading-in-your-non-developer-site-collection/).
  
> [!NOTE]
> Aplicativos de Sideload é um recurso de desenvolvedor/teste. Não se **destina ao uso de produção**. Não Sideload aplicativos regularmente ou mantenha o aplicativo Sideload habilitado por mais tempo do que você está usando ativamente o recurso. 
  
## <a name="add-content-to-the-add-in-project"></a>Adicionar conteúdo ao projeto do suplemento

Após criar um projeto e configurar o mecanismo de depuração, adicionar conteúdo ao aplicativo inclui as seguintes tarefas:
  
- Definindo o escopo do aplicativo
    
- Vinculando a biblioteca JSOM
    
- Adicionando elementos de interface do usuário ao suplemento
    
- Inicializando e conectando-se ao serviço do Project online
    
- Recuperando projetos e detalhes/Propriedades
    
- Exibindo projetos
    
- Exibindo tarefas para um projeto
    
O projeto do suplemento consiste em vários arquivos. Neste exemplo, você precisará editar os seguintes arquivos: 
  
- Arquivo AppManifest. xml
    
- Default. aspx
    
- App. js
    
- App. css-opcional; contém definições de estilo desenvolvidas para o suplemento
    
Se o locatário do Project online for alterado, como mover de uma versão de avaliação para um site de assinatura, você poderá atualizar as propriedades do projeto, incluindo a conexão do servidor e a URL do site, usando a janela Propriedades disponível através das propriedades do **modo de exibição** > ** Comando Window** . 
  
Você também pode adicionar arquivos ao projeto. Em caso afirmativo, você precisará atualizar o arquivo elements. xml localizado no mesmo grupo (conteúdo, imagens, páginas ou scripts) para incluir os novos arquivos. Para obter mais informações sobre os arquivos de projeto, consulte [explorar a estrutura do manifesto do aplicativo e o pacote de um suplemento do SharePoint](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/explore-the-app-manifest-structure-and-the-package-of-a-sharepoint-add-in).
  
### <a name="set-application-scope"></a>Definir o escopo do aplicativo

O suplemento precisa de níveis de escopo ou permissão definidos antes que o serviço retorne informações nos resultados da consulta. Para este suplemento, use o escopo a seguir para o projeto do Visual Studio. Essa alteração é feita no arquivo arquivo AppManifest. xml na guia permissões:

|Escopo|Permissão|
|:-----|:-----|
|Vários projetos (Project Server)  <br/> |Leitura  <br/> |
   
Salve o arquivo após definir o escopo do aplicativo. Caso contrário, nenhum dado será retornado do serviço. 
  
### <a name="link-the-jsom-library"></a>Vincular a biblioteca JSOM

As bibliotecas do Project online de tempo de execução, PS. js e PS. Debug. js, são fornecidas pelo Project online e são sempre a versão mais recente. Suplementos JavaScript que usam JSOM devem ser vinculados a uma dessas bibliotecas. As definições de vínculo são adicionadas ao arquivo default. aspx. Os comandos para usar o PS. js e/ou PS. Debug. js fazem parte do código localizado no arquivo app. js.
  
Adicione o seguinte comando à definição PS. js ou PS. Debug. js no `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` elemento após o "SharePoint: ScriptLink" para SP. js. 
  
```js
<SharePoint:ScriptLink name="PS.js" runat="server" OnDemand="false" LoadAfterUI="true" Localizable="false" />
```

> [!NOTE]
> O **** atributo OnDemand para PS. js ou PS. Debug. js definido como **false**. 
  
### <a name="add-ui-elements-to-the-add-in"></a>Adicionar elementos de interface do usuário ao suplemento

O suplemento de exemplo consiste em alguns componentes. As descrições de elementos estáticos estão localizadas no arquivo default. aspx. As descrições de elemento dinâmico e o código para todos os componentes estão localizados no arquivo app. js. Para obter comentários sobre os componentes, consulte as listagens de código-fonte. Veja a seguir uma lista de componentes da interface do usuário no suplemento:
  
- Título
    
- Introdução argumentação
    
- Botão para remover tarefas da tabela
    
- Tabela que lista o nome e a ID do projeto e as informações sobre a tarefa.
    
- Botão tarefas (clonado uma vez para cada projeto) que importa dados de tarefa para a tabela.
    
Para obter detalhes sobre a interface do usuário, como o título e a parte do cabeçalho da tabela do projeto, consulte o arquivo de projeto default. aspx.
  
### <a name="initialize-and-connect-to-the-host-system"></a>Inicializar e conectar-se ao sistema host

O arquivo app. js contém o código JavaScript. O suplemento carrega PS. js no navegador e, em seguida, chama a função initializePage. InitializePage recupera um contexto para o ponto de extremidade do Project online e inicia a função loadProjects.
  
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

A função loadProjects consulta o serviço para os nomes de projeto e IDs. 
  
O aplicativo recupera o nome do projeto e a ID do projeto. Outras informações sobre o projeto estão disponíveis e podem ser acessadas modificando o método Load para identificar explicitamente as propriedades a serem recuperadas. Um exemplo é fornecido no código como um comentário. 
  
Se a consulta for bem-sucedida, o suplemento continuará chamando displayProjects. 
  
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
> O loop while acessa as propriedades ID e Name. Isso é um pouco diferente do projeto de código-fonte que chama uma função que, por sua vez, acessa as mesmas propriedades. 
  
### <a name="display-the-tasks-for-a-project"></a>Exibir as tarefas de um projeto

As tarefas, enquanto fazem parte do suplemento, não fazem parte do carregamento inicial. Se o usuário estiver interessado nas tarefas associadas a um projeto, clicar no botão "Mostrar tarefas" fará com que as tarefas sejam exibidas na lista usando o manipulador de eventos btnLoadTasks. 
  
O manipulador de eventos btnLoadTasks, com a ID de projeto apropriada, solicita as tarefas para o projeto especificado do servidor. Após a recuperação, o btnLoadTasks passa a lista de tarefas para o displayTasks para apresentar as tarefas na tela.
  
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

A função displayTasks exibe as tarefas associadas a um projeto específico imediatamente abaixo da entrada do projeto.
  
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
> O loop while acessa as propriedades ID da tarefa e nome. Isso é um pouco diferente do projeto de código-fonte que chama uma função que, por sua vez, acessa as mesmas propriedades. 
  
Segue um exemplo de saída das tarefas de um projeto único.
  
![Captura de tela mostrando o resultado de uma tarefa de projeto] (media/f6500a3f-000b-4f3e-9be6-9a74d0bea15e.png "Captura de tela mostrando o resultado de uma tarefa de projeto")
  
## <a name="see-also"></a>Confira também

Confira a documentação e exemplos relacionados ao desenvolvimento de aplicativos usando o CSOM e Project Online no [Portal de Desenvolvimento do Project](https://developer.microsoft.com/en-us/project).
    


