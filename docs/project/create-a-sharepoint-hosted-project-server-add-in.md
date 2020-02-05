---
title: Criar um suplemento do Project Server hospedado pelo SharePoint
manager: lindalu
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: bb9c3c00-7121-41e1-9db3-75550d040ba8
description: Dos três tipos de aplicativo que você pode criar para o Project Online (hospedado automaticamente, hospedado pelo provedor e hospedado pelo SharePoint), o aplicativo hospedado pelo SharePoint é o mais simples de criar e implantar.
ms.openlocfilehash: 9b3b41eda40a8419ad72f11bb474acf7acaf81e9
ms.sourcegitcommit: 31b0a7373ff74fe1d6383c30bc67d7675b73d283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2020
ms.locfileid: "41773754"
---
# <a name="create-a-sharepoint-hosted-project-server-add-in"></a>Criar um suplemento do Project Server hospedado pelo SharePoint

Dos três tipos de aplicativo que você pode criar para o Project Online (hospedado automaticamente, hospedado pelo provedor e hospedado pelo SharePoint), o aplicativo hospedado pelo SharePoint é o mais simples de criar e implantar. Um aplicativo hospedado pelo SharePoint não requer autenticação OAuth, não usa o Azure nem exige a manutenção de um site local para os recursos hospedados pelo provedor. O modelo **Aplicativo do SharePoint 2013** no Visual Studio é uma estrutura prática para o desenvolvimento de aplicativos que podem ser publicados e vendidos na Office Store ou implantados em um catálogo de aplicativos privado no SharePoint. 
  
No Project, o status é um processo em que um membro da equipe pode usar a página Tarefas no Project Web App para enviar o status de uma tarefa atribuída, como o número de horas trabalhadas diariamente na tarefa. O proprietário da atribuição (geralmente o gerente de projeto) pode aprovar ou rejeitar o status. Quando o status é aprovado, o Project recalcula o cronograma. O aplicativo **QuickStatus** exibe tarefas atribuídas, em que o usuário pode atualizar rapidamente a porcentagem concluída e enviar o status das atribuições selecionadas para aprovação. Embora a página Tarefas no Project Web App tenha muito mais funcionalidade, o aplicativo **QuickStatus** é um exemplo que fornece uma interface simplificada. 
  
O aplicativo **QuickStatus** é uma amostra para desenvolvedores, ele não se destina ao uso em um ambiente de produção. O objetivo principal é mostrar um exemplo de desenvolvimento de aplicativo para o Project Online, não criar um aplicativo de status totalmente funcional. Para uma melhor abordagem ao status, confira a recomendação em [Próximas etapas](#pj15_StatusingApp_NextSteps).
  
Para informações gerais sobre o status, confira [Progresso da tarefa](https://support.office.com/article/Find-information-about-Project-Server-2013-8b08a414-15a7-4076-b2db-c90d0214ea7f?ui=en-US&rs=en-US&ad=US#BKMK_TaskProgress). Confira mais informações sobre o desenvolvimento de suplementos para o SharePoint e o Project Server em [Suplementos do SharePoint](https://msdn.microsoft.com/library/jj163230.aspx).

<a name="pj15_StatusingApp_Prerequisites"> </a>

## <a name="prerequisites-for-creating-an-app-for-project-server-2013"></a>Pré-requisitos para a criação de um aplicativo para o Project Server 2013

Para desenvolver aplicativos relativamente simples que possam ser implantados no Project Online ou em uma instalação local do Project Server 2013, você pode usar o Napa, que fornece um ambiente de desenvolvimento online. Para aplicativos mais complexos, modificar a faixa de opções do Project Web App e uma depuração mais fácil durante o desenvolvimento, você pode usar o Visual Studio 2012 ou o Visual Studio 2013. Por exemplo, com uma instalação local, você pode verificar manualmente as tabelas de dados de Rascunhos em busca de alterações no banco de dados do Project Server. Este artigo mostra como fazer o desenvolvimento de aplicativos com o Visual Studio.
  
O desenvolvimento de aplicativos do Project Server com o Visual Studio exige o seguinte:
  
- Verifique se você instalou os service packs e as atualizações mais recentes do Windows em seu computador de desenvolvimento local. O sistema operacional pode ser Windows 7, Windows 8, Windows Server 2008 ou Windows Server 2012.
    
- É preciso ter um computador com o SharePoint Server 2013 e o Project Server 2013 instalados, configurado para o isolamento de aplicativos e o sideloading de aplicativos. O sideloading permite que o Visual Studio instale temporariamente o aplicativo para depuração. Você pode usar uma instalação local do SharePoint e do Project Server. Confira mais informações em [Configurar um ambiente de desenvolvimento local para aplicativos do SharePoint ](https://msdn.microsoft.com/library/fp179923%28Office.15%29.aspx).
    
   > [!NOTE]
   > Para uma instalação local, configure um domínio de aplicativos isolado *antes* de criar um catálogo de aplicativos corporativos. 
  
- O computador de desenvolvimento pode ser um computador remoto com o Office Developer Tools para Visual Studio 2012 instalado. Verifique se você instalou a versão mais recente. Confira a seção *Ferramentas* de [Download de aplicativos do Office e do SharePoint](https://msdn.microsoft.com/office/apps/fp123627.aspx).
    
- Verifique se a instância do Project Web App usada para desenvolvimento e testes pode ser acessada no navegador.
    
Confira informações sobre como usar as ferramentas online em [Configurar um ambiente para desenvolver aplicativos para o SharePoint no Office 365](https://msdn.microsoft.com/library/fp161179.aspx). Para um passo a passo da criação de um aplicativo simples para o Project Server que usa as ferramentas online, confira a série de blog do EPMSource, [Como criar seu primeiro aplicativo do Project Server](https://epmsource.com/2012/11/20/building-your-first-project-server-app-part-zerothe-introduction/).

<a name="pj15_StatusingApp_UsingVisualStudio"> </a>

## <a name="using-visual-studio-to-create-a-project-server-app"></a>Usar o Visual Studio para criar um aplicativo do Project Server

O Office Developer Tools para Visual Studio 2012 inclui um modelo para aplicativos do SharePoint que podem ser usados ​​com o Project Server 2013. Quando você criar uma solução de aplicativo, a solução incluirá os arquivos a seguir para seu código personalizado:
  
- **AppManifest.xml** inclui configurações para o título do aplicativo, o escopo da solicitação de permissão e outras propriedades. O Procedimento 1 inclui etapas para a definição das propriedades usando o Designer de Manifesto. 
    
- **Default.aspx** na pasta Páginas é a página principal do aplicativo. O Procedimento 2 mostra como adicionar conteúdo HTML5 para o aplicativo **QuickStatus**. 
    
- **App.js** na pasta Scripts é o arquivo principal do código JavaScript personalizado. O Procedimento 3 explica o código JavaScript para o aplicativo **QuickStatus**. 
    
   Se você adicionar controles comerciais como uma grade baseada em jQuery ou o seletor de datas, poderá adicionar referências a arquivos JavaScript adicionais no arquivo Default.aspx.
    
- **App.css** na pasta Conteúdo é o arquivo principal para estilos CSS3 personalizados. O Procedimento 2 e o Procedimento 3 incluem informações sobre CSS (folhas de estilo em cascata) para o aplicativo **QuickStatus**. Você pode adicionar referências a arquivos CSS adicionais no arquivo Default.aspx. 
    
- **AppIcon.png** na pasta Imagens é o ícone 96 x 96 que o aplicativo exibe na Office Store ou no catálogo de aplicativos. 
    
Para modificar a faixa de opções do Project Web App, você pode adicionar uma ação personalizada da faixa de opções. A seção [Código de exemplo para o aplicativo QuickStatus](#pj15_StatusingApp_Example) inclui o código completo para os arquivos modificados Default.aspx, App.js, App.css, Elements.xml e AppManifest.xml. 
  
### <a name="procedure-1-to-create-an-app-project-in-visual-studio"></a>Procedimento 1. Para criar um projeto de aplicativo no Visual Studio

1. Execute o Visual Studio 2012 como administrador e selecione **Novo Projeto** na página Iniciar. 
    
2. Na caixa de diálogo **Novo Projeto**, expanda os nós **Modelos**, **Visual C#** e **Office/SharePoint** e então selecione **Aplicativos**. Use o **.NET Framework 4.5** padrão na lista suspensa da estrutura de destino na parte superior do painel central e então selecione **Aplicativo para o SharePoint 2013** (consulte a Figura 1). 
    
3. No campo **Nome**, digite QuickStatus, navegue até o local onde deseja salvar o aplicativo e então escolha **OK**.
    
   **Figura 1. Criar um aplicativo do Project Server no Visual Studio**

   ![Creating a Project Server app in Visual Studio](media/pj15_CreateStatusingApp_NewProject.gif "Creating a Project Server app in Visual Studio")
  
4. Na caixa de diálogo **Novo aplicativo para o SharePoint**, preencha estes três campos: 
    
   - Na caixa de texto superior, digite o nome que você deseja que o aplicativo exiba no Project Web App. Por exemplo, digite Atualização do QuickStatus.
    
   - Para o site usar para depuração, digite a URL da instância do Project Web App. Por exemplo, digite `https://ServerName/ProjectServerName` (substituindo o _ServerName_ e o _ProjectServerName_ por seus próprios valores) e, em seguida, escolha **Validar**. Se tudo correr bem, o Visual Studio mostrará **Conexão bem-sucedida**. Se você receber uma mensagem de erro, verifique se a URL do Project Web App está correta e se o computador do Project Server está configurado para isolamento de aplicativos e sideloading de aplicativos. Confira mais informações na seção [Pré-requisitos para a criação de um aplicativo para o Project Server 2013](#pj15_StatusingApp_Prerequisites). 
    
   - Na lista suspensa **Como você deseja hospedar seu aplicativo do SharePoint**, escolha **Hospedado pelo SharePoint**.
    
   > [!CAUTION]
   > Se você escolher o tipo de projeto **Hospedado pelo provedor** padrão por engano, o Visual Studio criará dois projetos na solução: um projeto **QuickStatus** e um projeto **QuickStatusWeb**. Se forem exibidos dois projetos, exclua essa solução e comece novamente. 
  
5. Escolha **OK** para criar a solução **QuickStatus**, o projeto **QuickStatus** e arquivos padrão. 
    
6. Abra o modo Designer de Manifesto (por exemplo, clique duas vezes no arquivo AppManifest.xml). Na guia **Geral**, a caixa de texto **Título** deve mostrar o nome do aplicativo que você digitou na etapa 4. Escolha a guia **Permissões** para adicionar as seguintes solicitações de permissão para o aplicativo (consulte a Figura 2): 
    
   - Na primeira linha da lista **Solicitações de permissão**, na coluna **Escopo**, escolha **Status** na lista suspensa. Na coluna **Permissão**, escolha **SubmitStatus**.
    
   - Adicione uma linha onde o **Escopo** é **Vários Projetos** e a **Permissão** é **Leitura**.
    
   **Figura 2. Configurar o escopo da permissão para um aplicativo de status**

   ![Setting the permission scope for a statusing app](media/pj15_CreateStatusingApp_PermissionScope.gif "Setting the permission scope for a statusing app")
  
O aplicativo **QuickStatus** permite que um usuário do Project Web App leia atribuições para esse usuário de vários projetos, altere a porcentagem concluída de atribuição e envie a atualização. Os outros escopos de solicitação de permissão mostrados na lista suspensa da Figura 2 não são necessários para este aplicativo. Os escopos de solicitação de permissão são as permissões que o aplicativo solicita em nome do usuário. Se o usuário não tiver essas permissões no Project Web App, o aplicativo não será executado. Um aplicativo pode ter vários escopos de solicitação de permissão, incluindo aqueles para outras permissões do SharePoint, mas deve ter apenas o mínimo necessário para a funcionalidade do aplicativo. A seguir estão os escopos de solicitação de permissão relacionados ao Project Server: 

- **Recursos da Empresa**: permissões do gerente de recursos para ler ou escrever informações sobre outros usuários do Project Web App.
    
- **Vários Projetos**: leitura ou gravação para mais de um projeto, onde o usuário tem as permissões exigidas.
    
- **Project Server**: exige o usuário do aplicativo para ter permissões do administrador para o Project Web App.
    
- **Relatório**: leitura do serviço OData do **ProjectData** para o Project Web App (requer apenas permissão de logon para o Project Web App). 
    
- **Projeto Único**: leitura ou gravação para um projeto onde o usuário tem as permissões exigidas.
    
- **Status**: envie atualizações para status de atribuições, como as horas trabalhadas, a porcentagem concluída e as novas atribuições.
    
- **Fluxo de Trabalho**: se o usuário tiver permissão para executar fluxos de trabalho do Project Server, o aplicativo então será executado com permissões elevadas para o fluxo de trabalho.
    
Confira mais informações sobre os escopos da solicitação de permissão do Project Server 2013 na seção *Aplicativos do Project* em [Atualizações para desenvolvedores no Project 2013](updates-for-developers-in-project-2013.md) e [Permissões de aplicativo no SharePoint 2013](https://msdn.microsoft.com/library/fp142383.aspx).


<a name="pj15_StatusingApp_HTML"> </a>

### <a name="creating-the-html-content-for-the-quickstatus-app"></a>Criar o conteúdo HTML para o aplicativo QuickStatus

Antes de começar a codificar o conteúdo HTML, projete a interface do usuário e a experiência do usuário para o aplicativo QuickStatus (a Figura 3 mostra um exemplo da página concluída). Um design também pode incluir uma estrutura de tópico das funções JavaScript que interagem com o código HTML. Confira informações gerais em [Design de experiência do usuário para aplicativos no SharePoint 2013](https://msdn.microsoft.com/library/fp179934.aspx).
  
**Figura 3. Página Design do aplicativo QuickStatus**

![Design of the QuickStatus app page](media/pj15_CreateStatusingApp_AfterRefresh.gif "Design of the QuickStatus app page")
  
O aplicativo mostra o nome de exibição na parte superior, que é o valor do elemento **Title** no AppManifest.xml. 
  
Por padrão, a página usa HTML5. A seguir, os elementos HTML padrão para os objetos da interface do usuário principal que o aplicativo **QuickStatus** contém no corpo da página: 
  
- Um elemento **form** contém todos os outros elementos da interface do usuário. 
    
- Um elemento **fieldset** cria um contêiner e uma borda para a tabela de atribuições; o elemento **legend** secundário oferece um rótulo para o contêiner. 
    
- Um elemento **table** inclui uma legenda e apenas um cabeçalho de tabela. As funções JavaScript alteram a legenda da tabela e adicionam linhas para as atribuições. 
    
   > [!NOTE]
   > Para adicionar paginação e classificação com facilidade, um aplicativo de produção provavelmente usaria um controle de grade baseado em jQuery comercial em vez de uma tabela. 
  
   A tabela inclui colunas para o nome do projeto, o nome da tarefa com uma caixa de seleção, o trabalho real, a porcentagem concluída, o trabalho restante e a data de término da atribuição. As funções JavaScript criam a caixa de seleção e o campo de entrada de texto para a porcentagem concluída de cada tarefa.
    
- Um elemento **input** para uma caixa de texto define a porcentagem concluída para todas as atribuições selecionadas. 
    
- Um elemento **button** envia as alterações de status. 
    
- Um elemento **button** atualiza a página. 
    
- Um elemento **button** sai do aplicativo e retorna para a página Tarefas no Project Web App. 
    
A caixa de texto inferior e os elementos button estão dentro dos elementos **div**, para que o CSS possa gerenciar facilmente a posição e a aparência dos objetos da interface do usuário. Uma função JavaScript adiciona um parágrafo na parte inferior da página que contém os resultados para o sucesso ou fracasso da atualização de status. 
  
### <a name="procedure-2-to-create-the-html-content"></a>Procedimento 2. Para criar o conteúdo HTML

1. No Visual Studio, abra o arquivo Default.aspx.
    
   O arquivo inclui dois elementos **asp:Content**: o elemento com o atributo `ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` é adicionado ao cabeçalho da página, e o elemento com o atributo `ContentPlaceHolderID="PlaceHolderMain"` é posicionado no elemento **body** da página. 
    
2. No controle `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead" runat="server">` para o cabeçalho da página, adicione uma referência ao arquivo PS.js no computador do Project Server. Para testar e depurar, você pode usar o PS.debug.js. 
    
   ```HTML
     <script type="text/javascript" src="/_layouts/15/ps.debug.js"></script>
   ```

   A infraestrutura do aplicativo usa o diretório virtual `/_layouts/15/` para o site do SharePoint no IIS. O arquivo físico é `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\PS.debug.js`.
    
   > [!NOTE]
   > Antes de implantar o aplicativo para uso em produção, remova `.debug` das referências do script para melhorar o desempenho. 
  
3. No controle `<asp:Content ContentPlaceHolderID="PlaceHolderMain" runat="server">` para o corpo da página, exclua o elemento **div** gerado e, em seguida, adicione o código HTML para os objetos da interface de usuário. O elemento **table** contém apenas uma linha de cabeçalho. A coluna **Task name** inclui um controle de entrada da caixa de seleção. O texto do elemento **caption** é substituído pelo retorno de chamada **onGetUserNameSuccess** para a função **getUserInfo** no arquivo App.js. 
    
    ```HTML
    <form>
        <fieldset>
        <legend>Select assigned tasks</legend>
        <table id="assignmentsTable">
            <caption id="tableCaption">Replace caption</caption>
            <thead>
            <tr id="headerRow">
                <th>Project name</th>
                <th><input type="checkbox" id="headercheckbox" checked="checked" />Task name</th>
                <th>Actual work</th>
                <th>% complete</th>
                <th>Remaining work</th>
                <th>Due date</th>
            </tr>
            </thead>
        </table>
        </fieldset>
        <div id="inputPercentComplete" >
        Set percent complete for all selected assignments, or leave this
        <br /> field blank and set percent complete for individual assignments: 
        <input type="text" name="percentComplete" id="pctComplete" size="4"  maxlength="4" />
        </div>
        <div id="submitResult">
        <p><button id="btnSubmitUpdate" type="button" class="bottomButtons" ></button></p>
        <p id="message"></p>
        </div>
        <div id="refreshPage">
        <p><button id="btnRefresh" type="button" class="bottomButtons" >Refresh</button></p>
        </div>
        <div id="exitPage">
        <p><button id="btnExit" type="button" class="bottomButtons" >Exit</button></p>
        </div>
    </form>
    ```

4. No arquivo App.css, adicione código CSS para a posição e a aparência dos elementos da interface do usuário. Para obter o código CSS completo do aplicativo **QuickStatus**, consulte a seção [Código de exemplo para o aplicativo QuickStatus](#pj15_StatusingApp_Example). 
    
O Procedimento 3 inclui as funções JavaScript para ler as atribuições e criar as linhas da tabela, e para alterar e atualizar a porcentagem concluída da atribuição. As etapas reais são mais interativas no desenvolvimento de um aplicativo, em que você cria, alternadamente, parte do código HTML, adiciona e testa estilos relacionados e funções JavaScript, modifica ou adiciona mais código HTML e, em seguida, repete o processo.

<a name="pj15_StatusingApp_JavaScript"> </a>

### <a name="creating-the-javascript-functions-for-the-quickstatus-app"></a>Criar as funções JavaScript para o aplicativo QuickStatus

O modelo do Visual Studio para um aplicativo do SharePoint inclui o arquivo App.js, que contém o código de inicialização padrão que obtém o contexto do cliente do SharePoint e demonstra as ações básicas de get e set para a página do aplicativo. O namespace JavaScript para a biblioteca SP.js do lado do cliente do SharePoint é **SP**. Como um aplicativo do Project Server usa a biblioteca PS.js, o aplicativo usa o namespace **PS** para obter o contexto do cliente e acessar o JSOM para o Project Server. 
  
As funções JavaScript do aplicativo **QuickStatus** incluem o seguinte: 
  
- O manipulador de eventos **ready** do documento é executado quando o modelo de objeto do documento (DOM) é instanciado. O manipulador de eventos **ready** executa estas quatro etapas: 
    
    1. Inicializa a variável global **projContext** com o contexto de cliente para o JSOM do Project Server e a variável global **pwaWeb**. 
        
    2. Chama a função **getUserInfo** para inicializar a variável global **projUser**. 
        
    3. Chama a função **getAssignments**, que obtém os dados de atribuição especificados para o usuário. 
        
    4. Associa manipuladores de eventos de clique a uma caixa de seleção de cabeçalho de tabela e a caixas de seleção em cada linha da tabela. Os manipuladores de eventos de clique gerenciam o atributo **checked** das caixas de seleção quando o usuário marca ou desmarca qualquer caixa de seleção na tabela. 
    
- Se a função **getAssignments** obtiver êxito, chama a função **onGetAssignmentsSuccess**. Essa função insere uma linha na tabela para cada atribuição, inicializa os controles HTML em cada linha e então inicializa as propriedades do botão na parte inferior. 
    
- O manipulador de eventos **onClick** para o botão **Atualizar** chama a função **updateAssignments**. Essa função obtém o valor da porcentagem concluída que é aplicado a cada atribuição selecionada ou se a caixa de texto de porcentagem concluída estiver vazia, a função obterá a porcentagem concluída de cada atribuição selecionada na tabela. O valor completo aplicado a cada atribuição selecionada na tabela. A função **updateAssignments** então salva e envia as atualizações de status e grava uma mensagem sobre os resultados na parte inferior da página. 
    
### <a name="procedure-3-to-create-the-javascript-functions"></a>Procedimento 3. Para criar as funções JavaScript

1. No Visual Studio, abra o arquivo App.js e então exclua todo o conteúdo do arquivo.
    
2. Adicione as variáveis globais e o manipulador de eventos **ready** do documento. O objeto **document** é acessado usando uma função jQuery. 
    
   O manipulador de eventos de clique para a caixa de seleção de cabeçalho de tabela define o estado marcado das caixas de seleção de linha. Se todas as caixas de seleção de linha estiverem marcadas ou se todas estiverem desmarcadas, o manipulador de eventos de clique para as caixas de seleção de linha define o estado marcado da caixa de seleção de cabeçalho. Os manipuladores de eventos de clique também definem a mensagem de resultados na parte inferior da página como uma cadeia de caracteres vazia.
    
   ```js
    var projContext;
    var pwaWeb;
    var projUser;
    // This code runs when the DOM is ready and creates a ProjectContext object.
    // The ProjectContext object is required to use the JSOM for Project Server.
    $(document).ready(function () {
        projContext = PS.ProjectContext.get_current();
        pwaWeb = projContext.get_web();
        getUserInfo();
        getAssignments();
        // Bind a click event handler to the table header check box, which sets the row check boxes
        // to the checked state of the header check box, and sets the results message to an empty string.
        $('#headercheckbox').live('click', function (event) {
            $('input:checkbox:not(#headercheckbox)').attr('checked', this.checked);
            $get("message").innerText = "";
        });
        // Bind a click event handler to the row check boxes. If any row check box is cleared, clear
        // the header check box. If all of the row check boxes are selected, select the header check box.
        $('input:checkbox:not(#headercheckbox)').live('click', function (event) {
            var isChecked = true;
            $('input:checkbox:not(#headercheckbox)').each(function () {
                if (this.checked == false) isChecked = false;
                $get("message").innerText = "";
            });
            $("#headercheckbox").attr('checked', isChecked);
        });
    });
   ```

3. Adicione a função **getUserInfo**, que chama **onGetUserNameSuccess** caso a consulta obtenha êxito. A função **onGetUserNameSuccess** substitui o conteúdo do parágrafo **caption** por uma legenda de tabela que inclui o nome do usuário. 
    
   ```js
        // Get information about the current user.
        function getUserInfo() {
            projUser = pwaWeb.get_currentUser();
            projContext.load(projUser);
            projContext.executeQueryAsync(onGetUserNameSuccess,
                // Anonymous function to execute if getUserInfo fails.
                function (sender, args) {
                    alert('Failed to get user name. Error: ' + args.get_message());
            });
        } 
        // This function is executed if the getUserInfo call is successful.
        function onGetUserNameSuccess() {
            var prefaceInfo = 'Assignments for ' + projUser.get_title();
            $('#tableCaption').text(prefaceInfo);
        }
   ```

4. Adicione a função **getAssignments**, que chama **onGetAssignmentsSuccess** (consulte a etapa 5) caso a consulta de atribuição não obtenha êxito. A opção **Include** limita a consulta para retornar somente os campos especificados. 
    
   ```js
    // Get the collection of assignments for the current user.
    function getAssignments() {
        assignments = PS.EnterpriseResource.getSelf(projContext).get_assignments();
        // Register the request that you want to run on the server. The optional "Include" parameter 
        // requests only the specified properties for each assignment in the collection.
        projContext.load(assignments,
            'Include(Project, Name, ActualWork, ActualWorkMilliseconds, PercentComplete, RemainingWork, Finish, Task)');
        // Run the request on the server.
        projContext.executeQueryAsync(onGetAssignmentsSuccess,
            // Anonymous function to execute if getAssignments fails.
            function (sender, args) {
                alert('Failed to get assignments. Error: ' + args.get_message());
            });
    }
   ```

5. Adicione a função **onGetAssignmentsSuccess**, que adiciona uma linha para cada atribuição à tabela. A variável **prevProjName** é usada para determinar se uma linha é para um projeto diferente. Nesse caso, o nome do projeto é mostrado em uma fonte em negrito; caso contrário, o nome do projeto é definido como uma cadeia de caracteres vazia. 
    
   > [!NOTE]
   > O JSOM não inclui as propriedades **TimeSpan** que o CSOM inclui, como **ActualWorkTimeSpan**. Em vez disso, o JSOM usa propriedades para o número de milissegundos, como a propriedade [PS.StatusAssignment.actualWorkMilliseconds](https://msdn.microsoft.com/library/736bce1e-f734-0efe-6c5f-e0e891ab00ef%28Office.15%29.aspx). O método para obter essa propriedade é **get\_actualWorkMilliseconds**, que retorna um valor inteiro. > O método **get_actualWork** retorna uma cadeia de caracteres como "3h". Você pode usar qualquer valor no aplicativo **QuickStatus**, mas exibi-lo de forma diferente. A consulta de atribuições inclui ambas as propriedades, para que você possa testar o valor durante a depuração. Se você remover a variável **actualWork**, também poderá remover a propriedade **ActualWork** na consulta de atribuições. 
  
   Por fim, a função **onGetAssignmentsSuccess** inicializa o botão **Atualização** e o botão **Atualizar** com manipuladores de eventos de clique. O valor do texto do botão **Atualização** também poderia ser definido no código HTML. 
    
   ```js
        // Get the enumerator, iterate through the assignment collection, 
        // and add each assignment to the table.
        function onGetAssignmentsSuccess(sender, args) {
            if (assignments.get_count() > 0) {
                var assignmentsEnumerator = assignments.getEnumerator();
                var projName = "";
                var prevProjName = "3D2A8045-4920-4B31-B3E7-9D0C5195FC70"; // Any unique name.
                var taskNum = 0;
                var chkTask = "";
                var txtPctComplete = "";
                // Constants for creating input controls in the table.
                var INPUTCHK = '<input type="checkbox" class="chkTask" checked="checked" id="chk';
                var LBLCHK = '<label for="chk';
                var INPUTTXT = '<input type="text" size="4"  maxlength="4" class="txtPctComplete" id="txt';
                while (assignmentsEnumerator.moveNext()) {
                    var statusAssignment = assignmentsEnumerator.get_current();
                    projName = statusAssignment.get_project().get_name();
                    // Get an integer, such as 3600000.
                    var actualWorkMilliseconds = statusAssignment.get_actualWorkMilliseconds(); 
                    // Get a string, such as "1h". Not used here.
                    var actualWork = statusAssignment.get_actualWork();
                    if (projName === prevProjName) {
                        projName = "";
                    }
                    prevProjName = statusAssignment.get_project().get_name();
                    // Create a row for the assignment information.
                    var row = assignmentsTable.insertRow();
                    taskNum++;
                    // Create an HTML string with a check box and task name label, for example:
                    // <input type="checkbox" class="chkTask" checked="checked" id="chk1" /> <label for="chk1">Task 1</label>
                    chkTask = INPUTCHK + taskNum + '" /> ' + LBLCHK + taskNum + '">' 
                        + statusAssignment.get_name() + '</label>';
                    txtPctComplete = INPUTTXT + taskNum + '" />';
                    // Insert cells for the assignment properties.
                    row.insertCell().innerHTML = '<strong>' + projName + '</strong>';
                    row.insertCell().innerHTML = chkTask;
                    row.insertCell().innerText = actualWorkMilliseconds / 3600000 + 'h';
                    row.insertCell().innerHTML = txtPctComplete;
                    row.insertCell().innerText = statusAssignment.get_remainingWork();
                    row.insertCell().innerText = statusAssignment.get_finish();
                    // Initialize the percent complete cell.
                    $get("txt" + taskNum).innerText = statusAssignment.get_percentComplete() + '%'
                }
            }
            else {
                $('p#message').attr('style', 'color: #0f3fdb');     // Blue text.
                $get("message").innerText = projUser.get_title() + ' has no assignments'
            }
            // Initialize the button properties.
            $get("btnSubmitUpdate").onclick = function() { updateAssignments(); };
            $get("btnSubmitUpdate").innerText = 'Update';
            $get('btnRefresh').onclick = function () { window.location.reload(true); };
            $get('btnExit').onclick = function () { exitToPwa(); };
        }
   ```

6. Adicione o manipulador de eventos de clique **updateAssignments** para o botão **Atualização**. Quando o usuário altera um valor para a porcentagem concluída de uma tarefa ou adiciona um valor à caixa de texto **percentComplete**, o valor poderia ser inserido em diversos formatos, como "60", "60%" ou "60 %". O método **getNumericValue** retorna o valor numérico do texto de entrada. 
    
   > [!NOTE]
   > Em um aplicativo projetado para o uso em produção, os valores de entrada para informações numéricas devem incluir validação de campo e verificação de erros adicional. 
  
   O exemplo **updateAssignments** inclui alguma verificação básica de erro e exiba informações no parágrafo **message** na parte inferior da página — verde se a consulta de atualização obtiver êxito e vermelho se houver um erro de entrada ou se a consulta de atualização não obtiver êxito. 
    
   Antes de usar o método **submitAllStatusUpdates**, o aplicativo deve salvar as atualizações no servidor usando o método **PS.StatusAssignmentCollection.update**. 
    
   ```js
        // Update all checked assignments. If the bottom percent complete field is blank,
        // use the value in the % complete field of each selected row in the table.
        function updateAssignments() {
            // Get percent complete from the bottom text box.
            var pctCompleteMain = getNumericValue($('#pctComplete').val()).trim();
            var pctComplete = pctCompleteMain;
            var assignmentsEnumerator = assignments.getEnumerator();
            var taskNum = 0;
            var taskRow = "";
            var indexPercent = "";
            var doSubmit = true;
            while (assignmentsEnumerator.moveNext()) {
                var pctCompleteRow = "";
                taskRow = "chk" + ++taskNum;
                if ($get(taskRow).checked) {
                    var statusAssignment = assignmentsEnumerator.get_current();
                    if (pctCompleteMain === "") {
                        // Get percent complete from the text box field in the table row.
                        pctCompleteRow = getNumericValue($('#txt' + taskNum).val());
                        pctComplete = pctCompleteRow;
                    }
                    // If both percent complete fields are empty, show an error.
                    if (pctCompleteMain === "" && pctCompleteRow === "") {
                        $('p#message').attr('style', 'color: #e11500');     // Red text.
                        $get("message").innerHTML =
                            '<b>Error:</b> Both <i>Percent complete</i> fields are empty, in row '
                            + taskNum
                            + ' and in the bottom textbox.<br/>One of those fields must have a valid percent.'
                            + '<p>Please refresh the page and try again.</p>';
                        doSubmit = false;
                        taskNum = 0;
                        break;
                    }
                    if (doSubmit) statusAssignment.set_percentComplete(pctComplete);
                }
            } 
            // Save and submit the assignment updates.
            if (doSubmit) {
                assignments.update();
                assignments.submitAllStatusUpdates();
                projContext.executeQueryAsync(function (source, args) {
                    $('p#message').attr('style', 'color: #0faa0d');     // Green text.
                    $get("message").innerText = 'Assignments have been updated.';
                }, function (source, args) {
                    $('p#message').attr('style', 'color: #e11500');     // Red text.
                    $get("message").innerText = 'Error updating assignments: ' + args.get_message();
                });
            }
        }
        // Get the numeric part for percent complete, from a string. For example, with "20 %", return "20".
        function getNumericValue(pctComplete) {
            pctComplete = pctComplete.trim();
            pctComplete = pctComplete.replace(/ /g, "");    // Remove interior spaces.
            indexPercent = pctComplete.indexOf('%', 0);
            if (indexPercent > -1) pctComplete = pctComplete.substring(0, indexPercent);
            return pctComplete;
        }
   ```

7. Adicione a função **exitToPwa**, que usa o parâmetro de cadeia de caracteres de consulta **SPHostUrl ** para a URL do site do Project Web App host. Para navegar de volta para a página Tarefas, acrescente `"/Tasks.aspx"` à URL. Por exemplo, a variável **spHostUrl** seria definida como `https://ServerName/ProjectServerName/Tasks.aspx`.
    
   A função  **getQueryStringParameter** divide a URL da página **QuickStatus** para extrair e retornar o parâmetro especificado nas opções da URL. A seguir, um exemplo do valor **document.URL** para o documento **QuickStatus** (tudo em uma linha): 
    
   ```HTML
    https://app-ef98082fa37e3c.servername.officeapps.selfhost.corp.microsoft.com/pwa/
        QuickStatus/Pages/Default.aspx
        ?SPHostUrl=https%3A%2F%2Fsphvm%2D85178%2Fpwa
        &SPLanguage=en%2DUS
        &SPClientTag=1
        &SPProductNumber=15%2E0%2E4420%2E1022
        &SPAppWebUrl=https%3A%2F%2Fapp%2Def98082fa37e3c%2Eservername
            %2Eofficeapps%2Eselfhost%2Ecorp%2Emicrosoft%2Ecom%2Fpwa%2FQuickStatus
   ```

   Para a URL anterior, a função **getQueryStringParameter** retorna o valor de cadeia de caracteres de consulta **SPHostUrl**, `https://ServerName/pwa`. 
    
   ```js
        // Exit the QuickStatus page and go back to the Tasks page in Project Web App.
        function exitToPwa() {
            // Get the SharePoint host URL, which is the top page of PWA, and add the Tasks page.
            var spHostUrl = decodeURIComponent(getQueryStringParameter('SPHostUrl'))
                            + "/Tasks.aspx";
            // Set the top window for the QuickStatus IFrame to the Tasks page.
            window.top.location.href = spHostUrl;
        }
        // Get a specified query string parameter from the {StandardTokens} URL option string.
        function getQueryStringParameter(urlParameterKey) {
            var docUrl = document.URL;
            var params = docUrl.split('?')[1].split('&');
            for (var i = 0; i < params.length; i++) {
                var theParam = params[i].split('=');
                if (theParam[0] == urlParameterKey)
                    return decodeURIComponent(theParam[1]);
            }
        }
   ```

Se você publicar o aplicativo **QuickStatus** neste ponto e adicioná-lo ao Project Web App, o aplicativo poderá ser executado na página Conteúdo do Site, mas não estará facilmente disponível para os usuários. Para ajudar os usuários a encontrar e executar o aplicativo, você pode adicionar um botão para ele na faixa de opções na página Tarefas. O Procedimento 4 mostra como adicionar uma ação personalizada da faixa de opções. 

<a name="pj15_StatusingApp_ribbon"> </a>

### <a name="adding-a-ribbon-custom-action"></a>Adicionar uma ação personalizada da faixa de opções

Guias, grupos e controles da faixa de opções do Project Web App são especificados no arquivo pwaribbon.xml, que é instalado no diretório `[Program Files]\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\FEATURES\PWARibbon\listtemplates` no computador que está executando o Project Server. Para ajudar a criar ações personalizadas para a faixa de opções do Project Web App, o download do SDK do Project 2013 inclui uma cópia do pwaribbon.xml. 
  
O Project Web App usa diferentes definições de faixa de opções para a página Tarefas, dependendo se a instância do Project Web App usa o modo de entrada única que permite aos usuários inserir valores para o quadro de horários e o status da tarefa. Se você tiver permissões administrativas para o Project Web App, para determinar o modo de entrada, escolha **Configurações do PWA** no menu de configurações suspensas, no canto superior direito da página. Na página Configurações do PWA, escolha **Configurações e Padrões do Quadro de Horários** e, em seguida, examine a caixa de seleção **Modo de Entrada Única** na parte inferior da página. 
  
Quando o modo de entrada única estiver desativado, a faixa de opções na página Tarefas será definida pela região Meu Trabalho em pwaribbon.xml: 
  
```XML
   <!-- REGION My Work Ribbon-->
   <CustomAction
      Id="Ribbon.ContextualTabs.MyWork"
      . . .
```

Quando o modo de entrada única estiver ativado, a faixa de opções da página Tarefas será definida pela região Modo Vinculado em pwaribbon.xml: 
  
```XML
   <!-- REGION Tied Mode Ribbon-->
   <CustomAction
      Id="Ribbon.ContextualTabs.TiedMode"
      . . .
```

Embora os grupos e controles em cada região pareçam semelhantes, um controle para o modo vinculado pode chamar uma função diferente do mesmo controle para o modo não vinculado. O Procedimento 4 mostra como adicionar um controle de botão para o aplicativo **QuickStatus** quando o modo de entrada única estiver desativado (a caixa de seleção **Modo de Entrada Única** está desmarcada). 
  
> [!NOTE]
> Confira informações gerais sobre a adição de ações personalizadas a uma faixa de opções ou a um menu em um aplicativo do SharePoint em [Criar ações personalizadas para implantação com aplicativos do SharePoint](https://msdn.microsoft.com/library/jj163954.aspx). 
  
### <a name="procedure-4-to-add-a-ribbon-custom-action-to-the-tasks-page"></a>Procedimento 4. Para adicionar uma ação personalizada da faixa de opções à página Tarefas

1. Examine a faixa de opções na página Tarefas no Project Web App. Selecione a guia **TAREFAS** na faixa de opções e planeje como modificá-la. Existem sete grupos, como **Enviar**, **Tarefas** e **Período**. O grupo **Enviar** tem dois controles, um botão **Salvar** e um menu suspenso **Enviar Status**. Você pode adicionar um controle em qualquer local de um grupo, adicionar um grupo com um novo controle em qualquer local na guia **TAREFAS** ou adicionar outra guia da faixa de opções com grupos e controles personalizados. Neste exemplo, adicionamos um terceiro botão ao grupo **Enviar**, em que o botão invoca o URL do aplicativo **QuickStatus**. 
    
2. No painel **Gerenciador de Soluções ** do Visual Studio, clique com o botão direito do mouse no projeto **QuickStatus** e adicione um novo item. Na caixa de diálogo **Adicionar Novo Item**, escolha **Ação Personalizada da Faixa de Opções** (confira a Figura 4). Por exemplo, nomeie a ação personalizada RibbonQuickStatusAction e escolha **Adicionar**.
    
   **Figura 4. Adicionar uma ação personalizada da faixa de opções**

   ![Adding a ribbon custom action](media/pj15_CreateStatusingApp_AddRibbonCustomAction.gif "Adding a ribbon custom action")
  
3. Na primeira página do assistente **Criar Ação Personalizada para a Faixa de Opções**, deixe a opção **Host da Web** selecionada, escolha **Nenhum** na lista suspensa para o escopo da ação personalizada e então escolha **Avançar** (consulte a Figura 5). Os itens das listas suspensas são relevantes para o SharePoint e não para o Project Server. Substituiremos a maioria dos XMLs gerados para a ação personalizada e, portanto, ela se aplicará ao Project Server. 
    
   **Figura 5. Especificar propriedades para a ação personalizada da faixa de opções**

   ![Specifying properties for the ribbon custom action](media/pj15_CreateStatusingApp_RibbonCustomAction2.gif "Specifying properties for the ribbon custom action")
  
4. Na próxima página do assistente **Criar Ação Personalizada para a Faixa de Opções**, deixe todos os valores padrão para as configurações e então escolha **Concluir** (consulte a Figura 6). O Visual Studio cria a pasta **RibbonQuickStatusAction**, que contém um arquivo Elements.xml. 
    
   **Figura 6. Especificar as configurações para um controle de botão**

   ![Specifying the settings for a button control](media/pj15_CreateStatusingApp_RibbonCustomAction3.gif "Specifying the settings for a button control")
  
5. Modifique o código padrão gerado no arquivo Elements.xml para a ação personalizada da faixa de opções. A seguir, o código XML padrão:
    
   ```XML
    <?xml version="1.0" encoding="utf-8"?>
    <Elements xmlns="http://schemas.microsoft.com/sharepoint/">
        <CustomAction Id="21ea3aaf-79e5-4aac-9479-8eef14b4d9df.RibbonQuickStatusAction"
                    Location="CommandUI.Ribbon"
                    Sequence="10001"
                    Title="Invoke &apos;RibbonQuickStatusAction&apos; action">
        <CommandUIExtension>
            <!-- 
            Update the UI definitions below with the controls and the command actions
            that you want to enable for the custom action.
            -->
            <CommandUIDefinitions>
            <CommandUIDefinition Location="Ribbon.ListItem.Actions.Controls._children">
                <Button Id="Ribbon.ListItem.Actions.RibbonQuickStatusActionButton"
                        Alt="Request RibbonQuickStatusAction"
                        Sequence="100"
                        Command="Invoke_RibbonQuickStatusActionButtonRequest"
                        LabelText="Request RibbonQuickStatusAction"
                        TemplateAlias="o1"
                        Image32by32="_layouts/15/images/placeholder32x32.png"
                        Image16by16="_layouts/15/images/placeholder16x16.png" />
            </CommandUIDefinition>
            </CommandUIDefinitions>
            <CommandUIHandlers>
            <CommandUIHandler Command="Invoke_RibbonQuickStatusActionButtonRequest"
                                CommandAction="~appWebUrl/Pages/Default.aspx"/>
            </CommandUIHandlers>
        </CommandUIExtension >
        </CustomAction>
    </Elements>
   ```

   1. No elemento **CustomAction**, exclua o atributo **Sequence** e o atributo **Title**. 
    
   2. Para adicionar um controle ao grupo **Enviar**, encontre o primeiro grupo na coleção `Ribbon.ContextualTabs.MyWork.Home.Groups` no arquivo pwaribbon.xml, que é o elemento que inicia, `<Group Id="Ribbon.ContextualTabs.MyWork.Home.Page" Command="PageGroup" Sequence="10" Title="$Resources:pwafeatures,PAGE_PDP_CM_SUBMIT"`. Para adicionar um controle filho ao grupo **Enviar**, o código a seguir mostra o atributo **Location** correto do elemento **CommandUIDefinition** no arquivo Elements.xml: 
    
      ```XML
        <CommandUIDefinitions>
          <CommandUIDefinition Location="Ribbon.ContextualTabs.MyWork.Home.Page.Controls._children">
             . . .
          </CommandUIDefinition>
        </CommandUIDefinitions>
      ```

   3. Altere os valores de atributo do elemento **Button** secundário desta forma: 
    
       ```XML
            <Button Id="Ribbon.ContextualTabs.MyWork.Home.Page.QuickStatus"
                    Alt="Quick Status app"
                    Sequence="30"
                    Command="Invoke_QuickStatus"
                    LabelText="Quick Status"
                    TemplateAlias="o1"
                    Image16by16="_layouts/15/1033/images/ps16x16.png" 
                    Image16by16Left="-80"
                    Image16by16Top="-144"
                    Image32by32="_layouts/15/1033/images/ps32x32.png" 
                    Image32by32Left="-32"
                    Image32by32Top="-288" 
                    ToolTipTitle="QuickStatus"
                    ToolTipDescription="Run the QuickStatus app" />
       ```

       - Para tornar o botão o terceiro controle no grupo, o atributo **Sequence** pode ser qualquer número maior que o valor `Sequence="20"` do controle **Send Status** existente (que é um elemento **FlyoutAnchor** de pwaribbon.xml). Por convenção, os números de sequência dos grupos e controles são `10, 20, 30, …`, o que permite que os elementos sejam inseridos em posições intermediárias.
    
       - O atributo **Command** especifica o comando a ser executado no elemento **CommandUIHandler** (confira a seguinte etapa 5.d). Você pode simplificar o nome do comando para tornar mais fácil para o próximo desenvolvedor. Por exemplo, `Command="Invoke_QuickStatus"` é mais fácil de ler que `Command="Invoke_RibbonQuickStatusActionButtonRequest"`.
    
       - Os atributos de imagem especificam o ícone de 16 x 16 pixels e o ícone de 32 x 32 pixels para o controle de botão. No arquivo padrão Elements.xml, `Image32by32="_layouts/15/images/placeholder32x32.png"` especifica um ponto laranja. Você pode extrair ícones dos arquivos de mapa de imagem (ps16x16.png e ps32x32.png) que estão instalados no diretório `[Program Files]\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\1033\IMAGES` no computador que está executando o Project Server. Por exemplo, o ícone de 32 x 32 pixels está na segunda coluna de ícones da esquerda e na décima linha abaixo da parte superior do mapa de imagem ps32x32.png (a parte superior do ícone é após o final da nona linha; 9 linhas x 32 pixels/linha = 288 pixels). 
    
       - Para mostrar uma dica de ferramenta para o controle de botão, adicione o atributo **ToolTipTitle** e o atributo **ToolTipDescription**. 
    
    4. Altere os atributos do elemento **CommandUIHandler**. Por exemplo, assegure-se de que o atributo **Command** corresponda ao valor do atributo **Command** para o elemento **Button**. Para o atributo **CommandAction**, `~appWebUrl` é um espaço reservado para a URL da página da Web do **QuickStatus**. Quando o botão da faixa de opções invoca o aplicativo **QuickStatus**, o token **{StandardTokens}** é substituído por opções de URL que incluem **SPHostUrl**, **SPLanguage**, **SPClientTag**, **SPProductNumber** e **SPAppWebUrl**.
    
        ```XML
            <CommandUIHandlers>
                <CommandUIHandler Command="Invoke_QuickStatus"
                                  CommandAction="~appWebUrl/Pages/Default.aspx?{StandardTokens}"/>
            </CommandUIHandlers>
        ```

6. No **Gerenciador de Soluções**, abra o designer **Feature1.feature** e mova o item **RibbonQuickStatusAction** do painel **Itens na Solução** para o painel **Itens no Recurso**. Então, se você abrir o designer **Package.package**, o item **RibbonQuickStatusAction** estará no painel **Itens no Pacote**. 
    
Conforme você desenvolve o aplicativo e adiciona um botão da faixa de opções, normalmente testa o aplicativo e define pontos de interrupção no código JavaScript para depuração. Quando você pressiona **F5** para iniciar a depuração, o Visual Studio compila o aplicativo, implanta-o no site especificado na propriedade **URL do site** do projeto **QuickStatus** e exibe uma página que pergunta se você confia no aplicativo. Quando você prossegue e sai do aplicativo **QuickStatus**, ele retorna à página Tarefas no Project Web App. 

> [!NOTE]
> A Figura 7 mostra que o botão **Quick Status** na guia **TAREFAS** da faixa de opções está desativado. Depois de muitas implantações de depuração com o Visual Studio, os controles de faixa de opções personalizados podem ser bloqueados quando você continua a depurar ou implantar o aplicativo publicado no mesmo servidor de teste. Para habilitar o botão, exclua o item **RibbonQuickStatusAction** no Visual Studio e crie uma nova ação de faixa de opções que tenha um nome e uma ID diferente. Se isso não resolver o problema, tente remover o aplicativo da instância de teste do Project Web App e recrie o aplicativo com uma ID de aplicativo diferente. 
  
**Figura 7. Visualizar a dica de ferramenta do botão QuickStatus desabilitado**

![Viewing the tooltip of the disabled button](media/pj15_CreateStatusingApp_ButtonToolTipDisabled.gif "Viewing the tooltip of the disabled button")
  
O Procedimento 5 mostra como implantar e instalar o aplicativo **QuickStatus**. O Procedimento 6 mostra algumas etapas adicionais para testar o aplicativo depois de instalá-lo. 

<a name="pj15_StatusingApp_Deploying"> </a>

## <a name="deploying-the-quickstatus-app"></a>Implantar o aplicativo QuickStatus

Há várias maneiras de implantar um aplicativo para um aplicativo da Web do SharePoint, como o Project Web App. Qual implantação você usará dependerá se você deseja publicar o aplicativo em um catálogo particular do SharePoint ou no Public Office Store e se o SharePoint está instalado no local ou é uma locação online. O procedimento 5 mostra como implantar o aplicativo **QuickStatus** em uma instalação local em um catálogo particular de aplicativos. Confira mais informações em [Instalar e gerenciar aplicativos do SharePoint 2013](https://technet.microsoft.com/library/fp161232.aspx) e [Publicar aplicativos para do SharePoint](https://msdn.microsoft.com/library/jj164070.aspx).
  
> [!NOTE]
> A adição de um aplicativo em um catálogo do SharePoint exige permissões de administrador do SharePoint. 
  
### <a name="procedure-5-to-deploy-the-quickstatus-app"></a>Procedimento 5. Para implantar o aplicativo QuickStatus

1. No Visual Studio, salve todos os arquivos e então clique com o botão direito do mouse no projeto **QuickStatus** no **Gerenciador de Soluções** e escolha **Publicar**.
    
2. Como o aplicativo **QuickStatus** é hospedado pelo SharePoint, existem algumas poucas opções para publicação (consulte a Figura 8). Na caixa de diálogo **Publicar aplicativos para o Office e o SharePoint**, escolha **Concluir**.
    
   **Figura 8. Publicar o aplicativo QuickStatus**

   ![Using the Publish Wizard](media/pj15_CreateStatusingApp_PublishWizard.gif "Using the Publish Wizard")
  
3. Copie o arquivo QuickStatus.app do diretório `~\QuickStatus\bin\Debug\app.publish\1.0.0.0` para um diretório conveniente no computador local (ou para o computador do SharePoint para uma instalação local). 
    
4. Na Administração Central do SharePoint, escolha **Aplicativos** no Início Rápido e então escolha **Gerenciar o Catálogo de Aplicativos**.
    
5. Se o catálogo de aplicativos não existir, crie um conjunto de sites para o catálogo de aplicativos seguindo a seção *Configurar o site Catálogo de Aplicativos para um aplicativo Web* em [Gerenciar o Catálogo de Aplicativos no SharePoint 2013](https://technet.microsoft.com/library/fp161234.aspx).
    
   Se houver um catálogo de aplicativos, navegue até a URL do site na página Gerenciar Catálogo de Aplicativos. Por exemplo, nas etapas a seguir, o site do catálogo de aplicativos é  `https://ServerName/sites/TestApps`.
    
6. Na página do catálogo de aplicativos, escolha **Aplicativos para o SharePoint** no Início Rápido. Na página Aplicativos para o SharePoint, na guia **ARQUIVOS** da faixa de opções, escolha **Carregar Documento**.
    
7. Na caixa de diálogo **Adicionar um documento**, procure o arquivo QuickStatus.app, adicione comentários à versão e então escolha **OK**.
    
8. Ao adicionar um aplicativo, você também pode adicionar informações locais para a descrição, o ícone e outras informações do aplicativo. Na caixa de diálogo **Aplicativos para SharePoint – QuickStatus.app**, adicione as informações que você deseja mostrar para o aplicativo no conjunto de sites do SharePoint. Por exemplo, adicione as seguintes informações: 
    
   1. Campo **Descrição Curta**: digite Aplicativo de Teste de QuickStatus.
    
   2. Campo **Descrição**: digite Testar aplicativo para atualizar porcentagem concluída para tarefas em vários projetos.
    
   3. Campos **URL do Ícone**: adicione uma imagem de 96 x 96 pixels para o ícone do aplicativo aos recursos do site para o catálogo de aplicativos. Por exemplo, navegue para `https://ServerName/sites/TestApps`, escolha **Conteúdo do Site** no menu suspenso **Configurações**, escolha **Ativos do Site** e, em seguida, adicione a imagem quickStatusApp. Clique com o botão direito no item **quickStatusApp**, escolha **Propriedades** e copie o valor **Endereço (URL)** na caixa de diálogo **Propriedades**. Por exemplo, copie `https://ServerName/sites/TestApps/SiteAssets/QuickStatusApp.png` e cole o valor no campo de endereço da Web **URL do Ícone**. Digite uma descrição para o ícone, por exemplo (como na Figura 9), digite o ícone do aplicativo QuickStatus. Teste se a URL é válida.
    
      **Figura 9. Adicionar uma URL de ícone para o aplicativo QuickStatus**

      ![Setting properties in SharePoint for the app](media/pj15_CreateStatusingApp_AddAppToSharePointSettings.gif "Setting properties in SharePoint for the app")
  
   4. Campo **Categoria**: escolha uma categoria existente ou especifique seu próprio valor. Por exemplo, digite Status.
    
      > [!NOTE]
      > Uma categoria chamada **Status** destina-se apenas para fins de teste. Uma categoria típica para aplicativos do Project Server é **Gerenciamento de Projetos**. 
  
   5. Campo **Nome do editor**: digite o nome do editor. Neste exemplo, digite SDK do Project.
    
   6. **Campo Habilitado**: para tornar o aplicativo visível para os administradores de site do Project Web App para instalação, selecione a caixa de seleção **Habilitado**. 
    
   7. Os campos adicionais são opcionais. Por exemplo, você pode adicionar uma URL de suporte e várias imagens de ajuda à página de detalhes do aplicativo. Na Figura 9, os campos **URL da Imagem 1** incluem a URL para uma captura de tela do aplicativo e uma descrição da captura de tela. 
    
   8. Na caixa de diálogo **Aplicativos para SharePoint - QuickStatus.app**, escolha **Salvar**. Na Figura 9, o item **Atualização do QuickStatus** na biblioteca Aplicativos do SharePoint está marcado para edição e, portanto, na guia **EDITAR** da faixa de opções da caixa de diálogo, você deveria escolher **Check-in** para concluir o processo (confira a Figura 10). 
    
      **Figura 10. O aplicativo QuickStatus é adicionado à biblioteca Aplicativos do SharePoint.**

      ![The QuickStatus app is added to SharePoint](media/pj15_CreateStatusingApp_AddAppToSharePoint.gif "The QuickStatus app is added to SharePoint")
  
9. No Project Web App, no menu suspenso **Configurações**, escolha **Adicionar um aplicativo**. Na página Seus aplicativos, no Início Rápido, escolha **Da sua organização** e, em seguida, escolha **Detalhes do Aplicativo** para o aplicativo **Atualização do QuickStatus**. A Figura 11 mostra a página de detalhes com o ícone do aplicativo, captura de tela e outras informações adicionadas na etapa anterior. 
    
   **Figura 11. Usar a página de detalhes de Atualização do QuickStatus no Project Web App**

   ![Adding the QuickStatus app to Project Web App](media/pj15_CreateStatusingApp_AddAppToPWA.gif "Adding the QuickStatus app to Project Web App")
  
10. Na página de detalhes da Atualização do QuickStatus, escolha **ADICIONAR**. O Project Web App exibe uma caixa de diálogo que lista as operações que o aplicativo QuickStatus pode executar (confira a Figura 12). A lista de operações é derivada dos elementos **AppPermissionRequest** no arquivo AppManifest.xml. 
    
    **Figura 12. Verificar se você confia no aplicativo QuickStatus**

    ![Verifying trust for the QuickStatus app](media/pj15_CreateStatusingApp_AddAppToPWA2Trust.gif "Verifying trust for the QuickStatus app")
  
11. Na caixa de diálogo **Você confia na Atualização do QuickStatus**, escolha **Confiar**. O aplicativo é adicionado à página Conteúdo do Site do Project Web App (confira a Figura 13).
    
    **Figura 13. Exibir o aplicativo QuickStatus na página Conteúdo do Site**

    ![Viewing the QuickStatus app in Site Contents](media/pj15_CreateStatusingApp_AddAppToPWA3.gif "Viewing the QuickStatus app in Site Contents")
  
Na página Conteúdo do Site, você pode selecionar o ícone **Atualização do QuickStatus** para executar o aplicativo.

> [!NOTE]
> Para comandos adicionais que oferecem informações sobre o aplicativo, na página Conteúdo do Site, escolha a região que contém o nome **Atualização do QuickStatus** e as reticências (...). Você pode examinar a página Sobre para o aplicativo, exiba a página Detalhes do Aplicativo que contém informações sobre erros do aplicativo, examine a página de permissões do aplicativo ou remova o aplicativo do Project Web App. 
  
Na página Tarefas no Project Web App (confira a Figura 14), o botão **QuickStatus** deve estar ativado na faixa de opções. Se o botão **QuickStatus** estiver desativado, tente as ações descritas na observação da Figura 7. 

**Figura 14. Iniciar o aplicativo QuickStatus na guia TAREFAS**

![Starting the QuickStatus app from the TASKS tab](media/pj15_CreateStatusingApp_TasksRibbon.gif "Starting the QuickStatus app from the TASKS tab")
  
O Procedimento 6 mostra alguns testes a serem feitos com o aplicativo QuickStatus.

<a name="pj15_StatusingApp_Testing"> </a>

## <a name="testing-the-quickstatus-app"></a>Testar o aplicativo QuickStatus

Todas as operações que um usuário pode tentar no aplicativo **QuickStatus** devem ser testadas em uma instalação de teste do Project Server antes de implantar o aplicativo em um servidor de produção ou em um locatário de produção do Project Online. Uma instalação de teste permite alterar e excluir atribuições para usuários sem afetar projetos reais. O teste também deve envolver vários usuários com diferentes conjuntos de permissões, como administrador, gerente de projeto e membro da equipe. Testes completos podem revelar alterações que devem ser feitas no aplicativo, que não eram aparentes nos testes durante o desenvolvimento. O Procedimento 6 lista vários testes para o aplicativo **QuickStatus**, mas não inclui uma série exaustiva de testes. 
  
### <a name="procedure-6-to-test-the-quickstatus-app"></a>Procedimento 6. Para testar o aplicativo QuickStatus

1. Execute o aplicativo **QuickStatus** onde o usuário não tem atribuições. O aplicativo deve mostrar uma mensagem azul na parte inferior da página, por exemplo, **Nome de Usuário não tem atribuições**.
    
   Escolha **Atualização**, e a mensagem muda para **As atribuições foram atualizadas** em verde.
    
   > [!NOTE]
   > O comportamento do aplicativo deve ser alterado para que o botão **Atualização** seja desativado quando não houver atribuições. 
  
2. Execute o aplicativo onde o usuário tiver várias atribuições em diversos projetos diferentes e algumas atribuições não estejam concluídas. Observe a aparência do aplicativo e execute as ações como a seguir (consulte a Figura 15):
    
   1. A função **onGetAssignmentsSuccess** cria uma linha na tabela para cada atribuição para o usuário atual. O nome do projeto é mostrado somente uma vez, em negrito, para a primeira atribuição em cada projeto. 
    
   2. Desmarque a caixa de seleção no cabeçalho da coluna **Nome da tarefa**. O manipulador de eventos de clique do cabeçalho da tela desmarca todas as outras caixas de seleção nas linhas da tarefa. 
    
   3. Selecione todas as tarefas. O manipulador de eventos de clique para cada linha determina se todas as linhas estão selecionadas e, nesse caso, selecione o cabeçalho da coluna **Nome da tarefa**. 
    
   4. Desmarque todas as caixas de seleção novamente e então selecione uma atribuição com algum trabalho restante. Por exemplo, a Figura 15 mostra a principal tarefa T1 tem 20% de trabalho restantes para concluir.
    
   5. Na caixa de texto **Definir Porcentagem Concluída**, digite 80 e escolha **Atualizar**. A parte inferior da página deve exibir uma mensagem em verde, **As atribuições foram atualizadas**.
    
      **Figura 15. Atualizar uma atribuição no aplicativo QuickStatus**

      ![Updating an assignment in the QuickStatus app](media/pj15_CreateStatusingApp_Testing1Update.gif "Updating an assignment in the QuickStatus app")
  
3. Escolha **Atualizar** (confira a Figura 16). Todas as tarefas são selecionadas novamente e a tarefa principal mostra uma porcentagem de conclusão de 80%. 
    
      **Figura 16. Atualizar a página Atualização do QuickStatus**

      ![Refreshing the QuickStatus page](media/pj15_CreateStatusingApp_Testing2Refresh.gif "Refreshing the QuickStatus page")
  
4. Desmarque todas as caixas de seleção e então selecione outra tarefa. Por exemplo, selecione **Nova tarefa do PWA**. Deixe a caixa de texto **Definir porcentagem concluída** vazia, exclua todo o texto da coluna **% concluídos** para a tarefa selecionada e então escolha **Atualização**. Como ambas as caixas de texto estão vazias, o aplicativo mostra uma mensagem de erro vermelha (consulte a Figura 17).
    
      **Figura 17. Testar a mensagem de erro**

      ![Testing the error message](media/pj15_CreateStatusingApp_Testing3Error.gif "Testing the error message")
  
5. Atualize a tarefa anterior para 80% concluída e, em seguida, escolha **Sair**. A função **exitToPwa** altera o local da janela do navegador para a página Tarefas no aplicativo host do SharePoint (ou seja, a URL é alterada para https://ServerName/pwa/Tasks.aspx)). A Figura 18 mostra que a tarefa **T1** e a tarefa **Nova tarefa do PWA**, cada uma, mostram 80% de conclusão. 
    
      **Figura 18. Verificar se as tarefas estão atualizadas no Project Web App**

      ![Verifying the updated tasks in Project Web App](media/pj15_CreateStatusingApp_TasksUpdatedInPWA.gif "Verifying the updated tasks in Project Web App")
  
6. Antes que o status atualizado seja mostrado no Project Professional 2013, as alterações deverão ser enviadas para aprovação e então aprovadas pelo gerente de projetos.
    
Os testes revelam outras alterações que devem ser feitas no aplicativo **QuickStatus** para usabilidade aprimorada. Por exemplo:

- Deve haver verificações de erro adicionais e validação de valores de caixa de texto. Atualmente, um usuário pode inserir um valor não numérico ou um valor negativo para porcentagem concluída, que resulta em uma mensagem de erro não amigável. Por exemplo, com um valor negativo, a mensagem de erro é **Erro ao atualizar atribuições: PJClientCallableException: StatusingSetDataValueInvalid**.
    
- A mensagem de erro para caixas de texto em branco pode listar o projeto e a tarefa, além do número da linha.
    
- A mensagem de êxito pode incluir uma lista das tarefas atualizadas ou, se a função **updateAssignments** obtiver êxito, pode executar uma atualização de página automática e mostrar tarefas atualizadas ou porcentagens em uma cor diferente e em fonte em negrito. 
    
- Para evitar uma tabela muito grande, a tabela de atribuições deverá estar limitada a tarefas com menos de 100% concluídos. Ou adicione uma opção para mostrar todas as tarefas. Esse problema também pode ser resolvido usando uma grade baseada em jQuery em vez de uma tabela, onde você pode implementar filtragem e paginação de grade com facilidade.
    
- Como o aplicativo **QuickStatus** não envia status, o ícone **Status Rápido** na guia **TAREFAS** da faixa de opções logicamente seria o primeiro ícone do grupo **Tarefas**, em vez do último ícone do grupo **Enviar**. 
    
- Como a função **onGetAssignmentsSuccess** inicializa o texto do botão **btnSubmitUpdate**, mas os outros valores de texto do botão são inicializados em HTML, a página é deixada em um estado parcialmente inicializado enquanto a função **getAssignments** é executada. Os botões da página apareceriam mais consistentes caso os valores de texto fossem todos inicializados em HTML. 
    
Mais importante, a abordagem que o aplicativo **QuickStatus** usa, em que ele altera porcentagem concluída para atribuições, deve ser revisada em um aplicativo de produção. Para saber mais, consulte a seção [Próximas etapas](#pj15_StatusingApp_NextSteps). 

<a name="pj15_StatusingApp_Example"> </a>

## <a name="example-code-for-the-quickstatus-app"></a>Código de exemplo para o aplicativo QuickStatus

### <a name="defaultaspx-file"></a>Arquivo Default.aspx

O código a seguir está no arquivo `Pages\Default.aspx` do projeto **QuickStatus**: 
  
```HTML
    <%-- The following lines are ASP.NET directives needed when using SharePoint components --%>
    <%@ Page Inherits="Microsoft.SharePoint.WebPartPages.WebPartPage, Microsoft.SharePoint, Version=15.0.0.0, 
    Culture=neutral, PublicKeyToken=71e9bce111e9429c" MasterPageFile="~masterurl/default.master" Language="C#" %>
    <%@ Register TagPrefix="Utilities" Namespace="Microsoft.SharePoint.Utilities" Assembly="Microsoft.SharePoint, Version=15.0.0.0, 
    Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
    <%@ Register TagPrefix="WebPartPages" Namespace="Microsoft.SharePoint.WebPartPages" Assembly="Microsoft.SharePoint, Version=15.0.0.0, 
    Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
    <%@ Register TagPrefix="SharePoint" Namespace="Microsoft.SharePoint.WebControls" Assembly="Microsoft.SharePoint, Version=15.0.0.0, 
    Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
    <%-- The markup and script in the following Content element will be placed in the <head> of the page.
        For production deployment, change the .debug.js JavaScript references to .js. --%>
    <asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead" runat="server">
    <script type="text/javascript" src="../Scripts/jquery-1.7.1.min.js"></script>
    <script type="text/javascript" src="/_layouts/15/sp.runtime.debug.js"></script>
    <script type="text/javascript" src="/_layouts/15/sp.debug.js"></script>
    <script type="text/javascript" src="/_layouts/15/ps.debug.js"></script>
    <!-- CSS styles -->
    <link rel="Stylesheet" type="text/css" href="../Content/App.css" />
    <!-- Add your JavaScript to the following file -->
    <script type="text/javascript" src="../Scripts/App.js"></script>
    </asp:Content>
    <%-- The markup and script in the following Content element will be placed in the <body> of the page --%>
    <asp:Content ContentPlaceHolderID="PlaceHolderMain" runat="server">
    <form>
        <fieldset>
        <legend>Select assigned tasks</legend>
        <table id="assignmentsTable">
            <caption id="tableCaption">Replace caption</caption>
            <thead>
            <tr id="headerRow">
                <th>Project name</th>
                <th><input type="checkbox" id="headercheckbox" checked="checked" />Task name</th>
                <th>Actual work</th>
                <th>% complete</th>
                <th>Remaining work</th>
                <th>Due date</th>
            </tr>
            </thead>
        </table>
        </fieldset>
        <div id="inputPercentComplete" >
        Set percent complete for all selected assignments, or leave this
        <br /> field blank and set percent complete for individual assignments: 
        <input type="text" name="percentComplete" id="pctComplete" size="4"  maxlength="4" />
        </div>
        <div id="submitResult">
        <p><button id="btnSubmitUpdate" type="button" class="bottomButtons" ></button></p>
        <p id="message"></p>
        </div>
        <div id="refreshPage">
        <p><button id="btnRefresh" type="button" class="bottomButtons" >Refresh</button></p>
        </div>
    <div id="exitPage">
        <p><button id="btnExit" type="button" class="bottomButtons" >Exit</button></p>
    </div>
    </form>
    </asp:Content>
```

<br/>

### <a name="appjs-file"></a>Arquivo App.js

O código a seguir está no arquivo `Scripts\App.js` do projeto **QuickStatus**: 
  
```js
    var projContext;
    var pwaWeb;
    var projUser;
    // This code runs when the DOM is ready and creates a ProjectContext object.
    // The ProjectContext object is required to use the JSOM for Project Server.
    $(document).ready(function () {
        projContext = PS.ProjectContext.get_current();
        pwaWeb = projContext.get_web();
        getUserInfo();
        getAssignments();
        // Bind a click event handler to the table header check box, which sets the row check boxes
        // to the selected state of the header check box, and sets the results message to an empty string.
        $('#headercheckbox').live('click', function (event) {
            $('input:checkbox:not(#headercheckbox)').attr('checked', this.checked);
            $get("message").innerText = "";
        });
        // Bind a click event handler to the row check boxes. If any row check box is cleared, clear
        // the header check box. If all of the row check boxes are selected, select the header check box.
        $('input:checkbox:not(#headercheckbox)').live('click', function (event) {
            var isChecked = true;
            $('input:checkbox:not(#headercheckbox)').each(function () {
                if (this.checked == false) isChecked = false;
                $get("message").innerText = "";
            });
            $("#headercheckbox").attr('checked', isChecked);
        });
    });
    // Get information about the current user.
    function getUserInfo() {
        projUser = pwaWeb.get_currentUser();
        projContext.load(projUser);
        projContext.executeQueryAsync(onGetUserNameSuccess,
            // Anonymous function to execute if getUserInfo fails.
            function (sender, args) {
                alert('Failed to get user name. Error: ' + args.get_message());
        });
    }
    // This function is executed if the getUserInfo call is successful.
    // Replace the contents of the 'caption' paragraph with the project user name.
    function onGetUserNameSuccess() {
        var prefaceInfo = 'Assignments for ' + projUser.get_title();
        $('#tableCaption').text(prefaceInfo);
    }
    // Get the collection of assignments for the current user.
    function getAssignments() {
        assignments = PS.EnterpriseResource.getSelf(projContext).get_assignments();
        // Register the request that you want to run on the server. The optional "Include" parameter 
        // requests only the specified properties for each assignment in the collection.
        projContext.load(assignments,
            'Include(Project, Name, ActualWork, ActualWorkMilliseconds, PercentComplete, RemainingWork, Finish, Task)');
        // Run the request on the server.
        projContext.executeQueryAsync(onGetAssignmentsSuccess,
            // Anonymous function to execute if getAssignments fails.
            function (sender, args) {
                alert('Failed to get assignments. Error: ' + args.get_message());
            });
    }
    // Get the enumerator, iterate through the assignment collection, 
    // and add each assignment to the table.
    function onGetAssignmentsSuccess(sender, args) {
        if (assignments.get_count() > 0) {
            var assignmentsEnumerator = assignments.getEnumerator();
            var projName = "";
            var prevProjName = "3D2A8045-4920-4B31-B3E7-9D0C5195FC70"; // Any unique name.
            var taskNum = 0;
            var chkTask = "";
            var txtPctComplete = "";
            // Constants for creating input controls in the table.
            var INPUTCHK = '<input type="checkbox" class="chkTask" checked="checked" id="chk';
            var LBLCHK = '<label for="chk';
            var INPUTTXT = '<input type="text" size="4"  maxlength="4" class="txtPctComplete" id="txt';
            while (assignmentsEnumerator.moveNext()) {
                var statusAssignment = assignmentsEnumerator.get_current();
                projName = statusAssignment.get_project().get_name();
                // Get an integer value for the number of milliseconds of actual work, such as 3600000.
                var actualWorkMilliseconds = statusAssignment.get_actualWorkMilliseconds();
                // Get a string value for the assignment actual work, such as "1h". Not used here.
                var actualWork = statusAssignment.get_actualWork();                         
                if (projName === prevProjName) {
                    projName = "";
                }
                prevProjName = statusAssignment.get_project().get_name();
                // Create a row for the assignment information.
                var row = assignmentsTable.insertRow();
                taskNum++;
                // Create an HTML string with a check box and task name label, for example:
                //     <input type="checkbox" class="chkTask" checked="checked" id="chk1" /> 
                //     <label for="chk1">Task 1</label>
                chkTask = INPUTCHK + taskNum + '" /> ' + LBLCHK + taskNum + '">'
                    + statusAssignment.get_name() + '</label>';
                txtPctComplete = INPUTTXT + taskNum + '" />';
                // Insert cells for the assignment properties.
                row.insertCell().innerHTML = '<strong>' + projName + '</strong>';
                row.insertCell().innerHTML = chkTask;
                row.insertCell().innerText = actualWorkMilliseconds / 3600000 + 'h';
                row.insertCell().innerHTML = txtPctComplete;
                row.insertCell().innerText = statusAssignment.get_remainingWork();
                row.insertCell().innerText = statusAssignment.get_finish();
                // Initialize the percent complete cell.
                $get("txt" + taskNum).innerText = statusAssignment.get_percentComplete() + '%'
            }
        }
        else {
            $('p#message').attr('style', 'color: #0f3fdb');     // Blue text.
            $get("message").innerText = projUser.get_title() + ' has no assignments'
        }
        // Initialize the button properties.
        $get("btnSubmitUpdate").onclick = function() { updateAssignments(); };
        $get("btnSubmitUpdate").innerText = 'Update';
        $get('btnRefresh').onclick = function () { window.location.reload(true); };
        $get('btnExit').onclick = function () { exitToPwa(); };
    }
    // Update all selected assignments. If the bottom percent complete field is blank,
    // use the value in the % complete field of each selected row in the table.
    function updateAssignments() {
        // Get percent complete from the bottom text box.
        var pctCompleteMain = getNumericValue($('#pctComplete').val()).trim();
        var pctComplete = pctCompleteMain;
        var assignmentsEnumerator = assignments.getEnumerator();
        var taskNum = 0;
        var taskRow = "";
        var indexPercent = "";
        var doSubmit = true;
        while (assignmentsEnumerator.moveNext()) {
            var pctCompleteRow = "";
            taskRow = "chk" + ++taskNum;
            if ($get(taskRow).checked) {
                var statusAssignment = assignmentsEnumerator.get_current();
                if (pctCompleteMain === "") {
                    // Get percent complete from the text box field in the table row.
                    pctCompleteRow = getNumericValue($('#txt' + taskNum).val());
                    pctComplete = pctCompleteRow;
                }
                // If both percent complete fields are empty, show an error.
                if (pctCompleteMain === "" && pctCompleteRow === "") {
                    $('p#message').attr('style', 'color: #e11500');     // Red text.
                    $get("message").innerHTML =
                        '<b>Error:</b> Both <i>Percent complete</i> fields are empty, in row '
                        + taskNum
                        + ' and in the bottom textbox.<br/>One of those fields must have a valid percent.'
                        + '<p>Please refresh the page and try again.</p>';
                    doSubmit = false;
                    taskNum = 0;
                    break;
                }
                if (doSubmit) statusAssignment.set_percentComplete(pctComplete);
            }
        } 
        // Save and submit the assignment updates.
        if (doSubmit) {
            assignments.update();
            assignments.submitAllStatusUpdates();
            projContext.executeQueryAsync(function (source, args) {
                $('p#message').attr('style', 'color: #0faa0d');     // Green text.
                $get("message").innerText = 'Assignments have been updated.';
            }, function (source, args) {
                $('p#message').attr('style', 'color: #e11500');     // Red text.
                $get("message").innerText = 'Error updating assignments: ' + args.get_message();
            });
        }
    }
    // Get the numeric part for percent complete, from a string. 
    // For example, with "20 %", return "20".
    function getNumericValue(pctComplete) {
        pctComplete = pctComplete.trim();
        pctComplete = pctComplete.replace(/ /g, "");    // Remove interior spaces.
        indexPercent = pctComplete.indexOf('%', 0);
        if (indexPercent > -1) pctComplete = pctComplete.substring(0, indexPercent);
        return pctComplete;
    }
    // Exit the QuickStatus page and go back to the Tasks page in Project Web App.
    function exitToPwa() {
        // Get the SharePoint host URL, which is the top page of PWA, and add the Tasks page.
        var spHostUrl = decodeURIComponent(getQueryStringParameter('SPHostUrl'))
                        + "/Tasks.aspx";
        // Set the top window for the QuickStatus IFrame to the Tasks page.
        window.top.location.href = spHostUrl;
    }
    // Get a specified query string parameter from the {StandardTokens} URL option string.
    function getQueryStringParameter(urlParameterKey) {
        var docUrl = document.URL;
        var params = docUrl.split('?')[1].split('&');
        for (var i = 0; i < params.length; i++) {
            var theParam = params[i].split('=');
            if (theParam[0] == urlParameterKey)
                return decodeURIComponent(theParam[1]);
        }
    }
```

<br/>

### <a name="appcss-file"></a>Arquivo App.css

O código CSS a seguir está no arquivo `Content\App.css` do projeto **QuickStatus**: 
  
```css
    /* Custom styles for the QuickStatus app. */
    /*============= Table elements ========================================*/
    table {
        width: 90%;
    }
    caption {
        font-size: 16px;
        padding-bottom: 5px;
        font-weight: bold;
        color: gray;
    }
    table th {
        background-color: gray;
        color: white;
    }
    table td, th {
        width: auto;
        text-align: left;
        padding: 2px;
        border: solid 1px whitesmoke;
        color: gray;
    }
    /*=== Class for check boxes added to rows 
    */
    .chkTask {
        width: 12px;
        height: 12px;
        color: gray;
    }
    /*========== DIV id for the Percent Complete text box ================*/
    #inputPercentComplete {
        position: fixed;
        top: auto;
        height: auto;
        padding-top: 20px;
        margin-left: 30px;
    }
    /*========== DIV id for the Submit Result button ====================*/
    #submitResult {
        position: fixed;
        top: auto;
        height: auto;
        padding-top: 60px;
    }
    /*========== DIV id for the Refresh Page button ====================*/
    #refreshPage {
        position: fixed;
        top: auto;
        height: auto;
        padding-top: 60px;
        margin-left: 120px;
    }
    /*========== DIV id for the Exit Page button ====================*/
    #exitPage {
        position: fixed;
        top: auto;
        height: auto;
        padding-top: 60px;
        margin-left: 240px;
    }
    /*========== Class for the buttons at the bottom of the page =======*/
    .bottomButtons {
        color: gray;
        font-weight: bold; 
        font-size: 12px; 
        border-color: darkgreen;
        border-width: thin;
    }
```

<br/>

### <a name="elementsxml-file-for-the-ribbon"></a>Arquivo Elements.xml para a faixa de opções

A definição XML a seguir, para o botão adicionado à guia **TAREFAS** na faixa de opções, está no arquivo `RibbonQuickStatusAction\Elements.xml` do projeto **QuickStatus**: 
  
```XML
    <?xml version="1.0" encoding="utf-8"?>
    <Elements xmlns="http://schemas.microsoft.com/sharepoint/">
    <CustomAction Id="21ea3aaf-79e5-4aac-9479-8eef14b4d9df.RibbonQuickStatusAction"
                    Location="CommandUI.Ribbon">
        <CommandUIExtension>
        <!-- 
        Add a button that invokes the QuickStatus app. The Quick Status button is displayed as  
        the third control in the Page group (the group title is "Submit").
        -->
        <CommandUIDefinitions>
            <CommandUIDefinition Location="Ribbon.ContextualTabs.MyWork.Home.Page.Controls._children">
            <Button Id="Ribbon.ContextualTabs.MyWork.Home.Page.QuickStatus"
                    Alt="Quick Status app"
                    Sequence="30"
                    Command="Invokae_QuickStatus"
                    LabelText="Quick Status"
                    TemplateAlias="o1"
                    Image16by16="_layouts/15/1033/images/ps16x16.png" 
                    Image16by16Left="-80"
                    Image16by16Top="-144"
                    Image32by32="_layouts/15/1033/images/ps32x32.png" 
                    Image32by32Left="-32"
                    Image32by32Top="-288" 
                    ToolTipTitle="Quick Status"
                    ToolTipDescription="Run the QuickStatus app" />
            </CommandUIDefinition>
        </CommandUIDefinitions>
        <CommandUIHandlers>
            <CommandUIHandler Command="Invoke_QuickStatus"
                            CommandAction="~appWebUrl/Pages/Default.aspx?{StandardTokens}"/>
        </CommandUIHandlers>
        </CommandUIExtension >
    </CustomAction>
    </Elements>
```

<br/>

### <a name="appmanifestxml-file"></a>Arquivo AppManifest.xml

A seguir, o XML para o manifesto do aplicativo do projeto **QuickStatus**, que inclui os dois escopos de solicitação de permissão necessários para a atualização do status de atribuição do usuário do aplicativo em vários projetos: 
  
```XML
    <?xml version="1.0" encoding="utf-8" ?>
    <!--Created:cb85b80c-f585-40ff-8bfc-12ff4d0e34a9-->
    <App xmlns="http://schemas.microsoft.com/sharepoint/2012/app/manifest"
        Name="QuickStatus"
        ProductID="{bbc497e7-1221-4d7b-a0ae-141a99546008}"
        Version="1.0.0.0"
        SharePointMinVersion="15.0.0.0"
    >
    <Properties>
        <Title>Quick Status Update</Title>
        <StartPage>~appWebUrl/Pages/Default.aspx?{StandardTokens}</StartPage>
    </Properties>
    <AppPrincipal>
        <Internal />
    </AppPrincipal>
    <AppPermissionRequests>
        <AppPermissionRequest Scope="https://sharepoint/projectserver/statusing" Right="SubmitStatus" />
        <AppPermissionRequest Scope="https://sharepoint/projectserver/projects" Right="Read" />
    </AppPermissionRequests>
    </App>
```

<br/>

### <a name="appiconpng-file"></a>Arquivo AppIcon.png

A solução completa do Visual Studio para o aplicativo **QuickStatus** inclui um arquivo AppIcon.png personalizado. A solução será incluída no download do SDK do Project 2013. 

<a name="pj15_StatusingApp_NextSteps"> </a>

## <a name="next-steps"></a>Próximas etapas

O aplicativo **QuickStatus** é um exemplo relativamente simples de como gravar aplicativos que podem ser instalados no Project Server 2013 e no Project Online. A seção [Testar o aplicativo QuickStatus](#pj15_StatusingApp_Testing) lista várias melhorias que podem ser feitas para melhor usabilidade. O aplicativo **QuickStatus** usa funções JavaScript para atualizar o status da atribuição do Project Web App. Porém, alterar a porcentagem concluída da atribuição não é uma prática recomendada de gerenciamento de projetos. Outra abordagem seria atualizar a data de início real e a duração restante das tarefas atribuídas. Para uma discussão dos problemas, confira [Atualizar Melhor](https://www.mpug.com/articles/update-better) no boletim informativo MPUG. 

<a name="pj15_StatusingApp_AdditionalResources"> </a>

## <a name="see-also"></a>Confira também

- [Tarefas de programação do Project Server](project-programming-tasks.md)
- [Suplementos do SharePoint](https://msdn.microsoft.com/library/jj163230.aspx)
- [Gerenciar atualizações de tarefas no Project Web App](https://technet.microsoft.com/library/hh767481%28v=office.14%29.aspx)
- [Criar ações personalizadas para implantação com Suplementos do SharePoint](https://msdn.microsoft.com/library/jj163954.aspx)
    

