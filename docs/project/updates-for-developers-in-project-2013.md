---
title: Atualizações para desenvolvedores no Project
manager: soliver
ms.date: 09/29/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5b2b22cd-6e28-43a8-9092-b411da8bfb53
description: Novos recursos incluem um modelo de objeto do cliente (CSOM), interfaces do REST, um serviço OData para relatórios, receptores de evento remoto, fluxos de trabalho declarativos e suplementos de painel de tarefas para clientes do Project.
ms.openlocfilehash: facd52c5ba2473de41f2a6bede431af0f55ba4ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771184"
---
# <a name="updates-for-developers-in-project"></a>Atualizações para desenvolvedores no Project

Recursos de extensibilidade do Project Server 2013 funcionam com suplementos para o Project Online e com instalações de local. Novos recursos incluem um modelo de objeto do cliente (CSOM), interfaces do REST, um serviço OData para relatórios, receptores de evento remoto, fluxos de trabalho declarativos e suplementos de painel de tarefas para clientes do Project. Saiba também recursos preteridos e não devem ser usados para o desenvolvimento de novos.
  
Project Server 2013 amplia a estrutura introduzido com o Microsoft Office Project Server 2007 e estendida pelo Project Server 2010. Project Server 2013 adiciona um modelo de objeto do cliente (CSOM) que é refatorado simplificado do Project Server Interface (PSI) e inclui uma biblioteca de JavaScript e .NET Framework 4 bibliotecas para aplicativos do Windows, Windows Phone 8 e Microsoft Silverlight. O CSOM foi projetado para desenvolvimento do Project Online e também opera com uma instalação do Project Server no local. 

Os bancos de dados do Project Server são combinados em um único banco de dados; Você pode acessar as exibições e tabelas de relatórios online por meio de um serviço OData. O CSOM e o serviço OData incluem uma interface de transferência de estado representacional (REST). Fluxos de trabalho do Project Server podem ser criados usando o SharePoint Designer 2013. Project Professional 2013 pode integrar com o relatório de dados, listas de tarefas do SharePoint e outro conteúdo externo usando o modelo de extensibilidade de suplementos do Office para painéis de tarefas do Project Server. Project Standard 2013 pode usar suplementos de painel de tarefas para integrar com conteúdo externo geral.
  
Para obter mais informações sobre as principais alterações no Project Server 2013 e diagramas, consulte [arquitetura do Project Server 2013](project-server-2013-architecture.md).
  
> [!NOTE]
> Project Server 2013 é criado na plataforma do SharePoint Server 2013 e Project 2013 inclui muito da infraestrutura de mesmo como os outros aplicativos do Office 2013. Para obter a documentação do modelo para o SharePoint Add-ins, fluxos de trabalho baseados no SharePoint, Web Parts, desenvolvimento com outros recursos do SharePoint e documentação de suplementos do Office, consulte o [Office e SharePoint Add-ins](http://msdn.microsoft.com/library/fp161507%28office.15%29.aspx) e [desenvolvimento do SharePoint 2013 Visão geral do](http://msdn.microsoft.com/library/jj164084%28office.15%29.aspx). 
  
## <a name="major-new-features-in-project-2013"></a>Principais novos recursos no Project 2013
<a name="pj15_WhatsNew_MajorNewFeatures"> </a>

Novos recursos no Project Standard 2013 e Project Professional 2013 incluem uma interface de usuário aprimorada que corresponde a outros aplicativos do Office 2013 e oferece suporte à interface de usuário de estilo moderno no Windows 8, integração com objetos de arte do Office para relatórios de progresso relatórios e novos recursos de programação para relatórios. Habilita o Project Professional 2013 mais abrangentes compartilhando e sincronizando projetos no SharePoint Server 2013, juntamente com os tarefa painel complementos que também são implementados em outros aplicativos do Office 2013, como Word, Excel e Outlook.
  
Há vários novos recursos no Project Server 2013. Alguns não possuem uma história principais recursos de programação, como a nova linha do tempo no Project Web App. Esses recursos serão documentados na documentação de Ajuda e do usuário final do produto no Microsoft Office Online e nos tópicos destinados a administradores e profissionais de TI no Microsoft TechNet. Outros novos recursos, como quadros de horários aprimorados, tornam mais fácil para desenvolvedores de terceiros interagir com os quadros de horários e status através do Project Server Interface (PSI).
  
A adição do Project Online e Office Store (http://office.microsoft.com/store) para suplementos de projeto são alterações grandes, onde o Project Server é acessível através do Microsoft Azure. Acesso baseado em nuvem ao Project Server usa um modelo de objeto do cliente (CSOM) para o desenvolvimento de suplementos com o Microsoft .NET Framework, Microsoft Silverlight, Windows Phone e aplicativos web que usam o JavaScript. Um requisito do Project Online é que os quatro bancos de dados do Project Server de versões anteriores são mesclados em um banco de dados.
  
Escalabilidade e desempenho do project Server 2013 é melhorado em muitas áreas como gerenciamento de projetos, quadros de horários e status da tarefa. Fluxos de trabalho do Project Server são reprojetados com a versão 4 do Windows Workflow Foundation (WF4). O uso do .NET Framework 4 e Windows Communication Foundation (WCF) com a PSI melhora a segurança, desempenho e escalabilidade. Por exemplo, você pode alterar o protocolo de transporte de aplicativos baseados em WCF usando arquivos de configuração, sem alterar o código do aplicativo ou recompilação. Muitas das chamadas PSI onde dados não alteram significativamente caches de Project Web App.
  
> [!NOTE]
> Para o desenvolvimento com o Project Server 2013, você pode usar o Visual Studio com as extensões de ferramentas Office e SharePoint, que nativamente podem criar suplementos para os produtos do Office 2013. Project Server 2013 requer o Visual Studio para totalmente permitem o desenvolvimento de recursos, como páginas de detalhes do projeto e aplicativos baseados no WCF. As extensões de ferramentas do SharePoint no Visual Studio podem implantar Web Parts e outros recursos do SharePoint diretamente para o Project Web App e outros sites do SharePoint. 
>
> Visual Studio não for mais necessária para desenvolver fluxos de trabalho do Project Server que usam os campos personalizados, estágios, fases e tipos de projeto corporativo que podem ser gerenciados no Project Web App. Embora você possa usar o Visual Studio para desenvolver fluxos de trabalho, eles são geralmente mais fácil e rápido criar usando o SharePoint Designer. Visual Studio pode ser usado para fluxos de trabalho que precisam acessar o CSOM ou outros APIs externas. 
  
### <a name="project-add-ins"></a>Suplementos do projeto
<a name="pj15_WhatsNew_Apps"> </a>

Distribuição e marketing do software foi revolucionou com o conceito de um suplemento. Para o Project 2013, suplementos podem ser disponibilizados para compra e o download da Office Store pública ou distribuídos dentro de um catálogo particular no SharePoint. Um suplemento é normalmente um programa interativo, independente, que executa um pequeno número de tarefas relacionadas. Um suplemento do Project pode ser um add-in de painel de tarefas para o Project Standard 2013 ou Project Standard 2013 clientes ou um suplemento para o Project Server 2013 ou Project Online.
  
Para obter informações sobre suplementos para os clientes de área de trabalho do projeto, consulte [tarefa painel complementos no projeto](#pj15_WhatsNew_Agave). Para obter um exemplo do Project Server 2013, consulte o [suplemento do Project Server de criar um hospedado no SharePoint](create-a-sharepoint-hosted-project-server-add-in.md). Além dos artigos no [Office e SharePoint suplementos SDK](http://msdn.microsoft.com/library/fp161507.aspx), o [Blog do Office](https://blogs.office.com/dev/) tem muitas postagens que também são relevantes para o Project 2013 e Project Online. 
  
Um suplemento do Project Server 2013 pode trabalhar com uma instalação local e Project Online. Suplementos de servidor de projeto podem incluir Web Parts, receptores de evento remoto e a lógica de negócios. Acesso ao modelo de objeto do Project Server em um suplemento é por meio de CSOM, não a PSI. Armazenamento de dados pode ser baseado em nuvem, como com o SQL Azure, externos, como a Microsoft Business Connectivity Services (BCS), interno com um banco de dados local, ou mista.
  
#### <a name="add-in-security"></a>Segurança de suplementos

Em geral, as ações que um suplemento leva são realizadas em nome do usuário que executa o suplemento; Você não explicitamente utilizam a representação ou especificar quem pode executar o suplemento. Ações não podem exceder o nível de permissão do usuário que executa o suplemento. 
  
No Office Developer Tools para Visual Studio 2012, o arquivo AppManifext.xml tem um editor de gráfico, onde você pode definir o escopo de solicitação de permissão. Por exemplo, para criar um suplemento que permite que os gerentes de projeto atualizar seus projetos, na guia **permissões** do painel designer **AppManifest.xml** , selecione **Vários projetos** para o escopo e a **gravação** para que a permissão. Se o usuário suplemento tem permissões de gerente de projeto, ela pode executar o add-in para projetos que gerencia a ela. O código no arquivo AppManifest.xml seria incluem o seguinte: 
  
```XML
  <AppPermissionRequests>
    <AppPermissionRequest Scope="http://sharepoint/projectserver/projects" Right="Write" />
  </AppPermissionRequests>
```

**Tabela 1. Escopos de solicitação de permissão para suplementos do Project Server**

|Escopo|Permissions|
|:-----|:-----|
|**Project Server** <br/> |**Gerenciar** (Exige permissões de administrador do Project Server).  <br/> |
|**Vários projetos** <br/> |**Leitura**, **gravação** (exige permissões de gerente de projeto para algumas operações; permissões de membro da equipe de projeto para basic leia operações, como atribuições de tarefa.)  <br/> |
|**Único projeto** <br/> |**Leitura**, **gravação** (requer ao menos permissões de membro da equipe de projeto; o acesso a alguns dados em um projeto depende de outros níveis de permissão.)  <br/> |
|**Recursos da empresa** <br/> |**Leitura**, **gravação** (requer permissões de gerente de recursos).  <br/> |
|**Status** <br/> |**SubmitStatus** (Requer a permissão para enviar o status dos seus projetos.)  <br/> |
|**Emissão de relatórios** <br/> |**Leitura** (Requer a permissão para fazer logon no Project Server).  <br/> |
|**Fluxo de trabalho** <br/> |**Elevar** (Requer a permissão para executar fluxos de trabalho. O suplemento é executado com permissões elevadas, para habilitar o estágio a outro transições em um fluxo de trabalho. A lógica de negócios do add-in controla transições estágio).  <br/> |
   
> [!NOTE]
> Project Server 2013 e Project Online não use o modelo de autenticação do aplicativo somente no SharePoint 2013 (consulte o [suplemento de tipos de diretiva de autorização no SharePoint 2013](http://msdn.microsoft.com/library/124879c7-a746-4c10-96a7-da76ad5327f0%28Office.15%29.aspx)). 
  
Para obter informações sobre como desenvolver, distribuir, hospedar e gerenciar suplementos, consulte Tópicos relacionados na documentação de desenvolvedor do SharePoint Server 2013 e Office 2013 e [suplementos do Office](http://msdn.microsoft.com/library/1e123201-6e70-45c1-a48c-d5b955896ddb%28Office.15%29.aspx)e [SharePoint suplementos](http://msdn.microsoft.com/library/cd1eda9e-8e54-4223-93a9-a6ea0d18df70%28Office.15%29.aspx) . Para obter informações sobre o escopo de solicitação de permissão para outros suplementos do SharePoint, consulte [Add-in permissões no SharePoint 2013](http://msdn.microsoft.com/library/5f7a8440-3c09-4cf8-83ec-c236bfa2d6c4%28Office.15%29.aspx).
  
### <a name="integrating-with-sharepoint-server"></a>Integrando com o SharePoint Server
<a name="pj15_WhatsNew_IntegrationWSS"> </a>

Muitos recursos no Project Web App exigem a infraestrutura de nova no SharePoint Server 2013 como OAuth e a autenticação baseada em declarações, autorização do Project Server e permissões por meio de grupos do SharePoint, sincronização de projetos com tarefas do SharePoint listas e fluxos de trabalho declarativos do Project Server. O aplicativo de serviço Project pode ser associado a qualquer conjunto de sites em um farm do SharePoint. Sincronização de projeto pode ser com uma lista de tarefas do SharePoint, onde o SharePoint mantém o projeto. Um projeto da empresa também pode ser sincronizado com uma lista de tarefas do SharePoint, onde o Project Server mantém controle total. Para obter uma explicação da sincronização do projeto e diagramas de arquitetura, consulte [arquitetura do Project Server 2013](project-server-2013-architecture.md).
  
Há vários novos recursos no SharePoint Server 2013. Para obter mais informações, consulte [SharePoint para desenvolvedores](http://msdn.microsoft.com/en-US/sharepoint).
  
### <a name="integrating-with-workflows"></a>Integrando com fluxos de trabalho
<a name="pj15_WhatsNew_Workflow"> </a>

Fluxos de trabalho são dos principais recursos de gerenciamento de portfólio de projetos. Um ciclo de vida de projeto pode incluir os processos de execução longa que abrangem várias fases. Fases de governança incluem propostas de projeto, análise do impacto nos negócios e selecionando, criando, planejamento, gerenciamento e acompanhamento de projetos.
  
Fluxos de trabalho do Project Server 2013 são compilados em plataforma de fluxo de trabalho do SharePoint 2013, que utilizará WF4. Ao contrário nas versões anteriores, fluxos de trabalho declarativos do Project Server 2013 podem ser criados usando o SharePoint Designer 2013 em estão acessíveis para o local e o uso online. Usam o modelo de segurança do fluxo de trabalho do SharePoint com OAuth fluxos de trabalho do Project Server e podem ser instalados em um site do Project Web App. A Figura 1 mostra que o SharePoint Designer 2013 pode adicionar estágios para um fluxo de trabalho de site para o gerenciamento de demanda, onde os estágios são definidos no Project Web App.
  
**Figura 1. Usando o SharePoint Designer para adicionar um estágio a um fluxo de trabalho do Project Web App**

![Adicionando um estágio para um fluxo de trabalho no SPD] (media/pj15_CreateWorkflowSPD_AddStageInSPD.gif "Adicionando um estágio para um fluxo de trabalho no SPD")

<br/>

Você pode criar um fluxo de trabalho declarativo por meio da adição de outros elementos, ações, condições e estágios do fluxo de trabalho em uma ferramenta de design, que pode ser o SharePoint Designer 2013 ou o Visual Studio 2012. A ferramenta de design, em seguida, salva o fluxo de trabalho como código XAML, que será interpretado em tempo de execução. Fluxos de trabalho declarativos podem executar no Project Server 2013 no local ou no Project Online. Usando o Visual Studio 2012, você também pode criar ações personalizadas e formulários para o controle adicional e salvar modelos de fluxo de trabalho para reutilização com várias instâncias do Project Web App. SharePoint Designer 2013 podem consumir ações personalizadas que são criadas no Visual Studio 2012.
  
Um fluxo de trabalho do Project Server 2013 atua como um aplicativo, onde um administrador — quem possui permissões de design para o Project Web App — pode publicar um fluxo de trabalho declarativo e associá-lo a um tipo de projeto corporativo (EPT). O EPT deve ser para um projeto da empresa, onde o Project Server mantém controle total. Uma lista de tarefas do SharePoint não pode usar um fluxo de trabalho do Project Server. 
  
OAuth permite que os gerentes de projeto que possuem permissões de criação de projeto para chamar o fluxo de trabalho sem usar representação. Chamadas de fluxo de trabalho no Project Server, por exemplo ler um valor de campo personalizado para decidir qual ramificação a serem seguidas, são feitas em nome do gerente de projeto. Para impedir que o gerente de projeto criando um fluxo de trabalho que avança automaticamente para a próxima etapa, a chamada para mover para o próximo estágio de fluxo de trabalho é executado como o autor do fluxo de trabalho (o administrador). Por outro lado, os usuários de legado fluxos de trabalho do Project Server 2010 fazer chamadas de representada por meio da conta de usuário Proxy de fluxo de trabalho para ter acesso de administrador em todo o fluxo de trabalho inteiro.
  
Embora possa usar o Project Server 2013 local compilados fluxos de trabalho baseados em WF3.5, é recomendável atualizar fluxos de trabalho herdados para fluxos de trabalho declarativos com base em WF4. A tecnologia mais recente é mais escalonável e robusto. Analistas de negócios e equipe PMO pode criar ou atualizar designs do fluxo de trabalho usando o Visio 2013 e implementar fluxos de trabalho do Project Server sem codificação usando o SharePoint Designer 2013.
  
Para obter informações sobre como criar um fluxo de trabalho declarativo para o Project Web App, consulte [Introdução ao desenvolvimento de fluxos de trabalho do Project Server](getting-started-developing-project-server-workflows.md). Para obter uma comparação do SharePoint Designer e recursos do Visual Studio para fluxos de trabalho, consulte [fluxos de trabalho de desenvolvimento do SharePoint 2013 usando o Visual Studio](http://msdn.microsoft.com/en-us/library/office/jj163199.aspx).
  
### <a name="client-side-object-model"></a>Modelo de objeto do cliente
<a name="pj15_WhatsNew_CSOM"> </a>

Acesso programático ao Project Online requer um CSOM que se baseia em CSOM do SharePoint. Autenticação do Project Online será com OAuth usando um Windows Live ID, não a autenticação de formulários do Project Server ou a autenticação do Windows.
  
A seguir estão os princípios e os recursos do CSOM no Project Server 2013:
  
- O CSOM se destina a facilidade de uso. Por exemplo, métodos e propriedades diretamente usam ou fornecem dados pelo nome, em vez de exigir que os GUIDs de muitas, _changeXml_ parâmetros ou passando em torno de conjuntos de dados. 
    
- O Project Server CSOM implementa um subconjunto da funcionalidade PSI, com base nos requisitos mais comuns para soluções de terceiros.
    
- O CSOM internamente chama a PSI, mas é acrescentado de forma diferente. Por exemplo, as atualizações para todas as alterações de status são feitas por meio do método **StatusAssignmentCollection.SubmitAllStatusUpdates** , não pelo método PSI **Statusing.SubmitStatus** para o usuário ou o método **SubmitStatusForResource** para outros recursos. 
    
- O CSOM pode ser acessada por meio de um serviço WCF (Client.svc), em vez de 22 serviços públicos de PSI.
    
- Inicialização do Project Server CSOM diretamente através da classe [ProjectContext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx) com a URL do Project Web App, não está usando um assembly de referência ou proxy WCF. 
    
- O CSOM implementa várias bibliotecas de cliente e interfaces, que são compatíveis com a infraestrutura interna do SharePoint CSOM. As bibliotecas de cliente e interfaces incluem o seguinte:
    
  - Biblioteca do cliente do Microsoft .NET no assembly Microsoft.ProjectServer.Client.dll
    
  - Biblioteca do Silverlight no assembly Microsoft.ProjectServer.Client.Silverlight.dll
    
  - Biblioteca do Windows Phone 8 no assembly Microsoft.ProjectServer.Client.Phone.dll
    
  - Biblioteca de JavaScript para aplicativos web no arquivo PS.js ou PS.debug.js
    
  - Pontos de extremidade do REST para acesso com o protocolo OData
    
  - Suporte nativo para consultas LINQ com a filtragem, para limitar a quantidade de dados que são retornados
    
- O CSOM pode ser usado tanto para soluções do Project Online para soluções locais, independentemente da PSI e outros assemblies do Project Server, como Microsoft.Office.Project.Server.Library.dll.
    
- Funcionalidade adicional para o Project Server 2013 CSOM poderá ser considerada para atualizações cumulativas e service packs, com base em solicitações por parceiros do Project Server e da comunidade do desenvolvedor.
    
> [!NOTE]
> O CSOM é a interface preferida para desenvolvedores do Project Server de terceiros. Recomendamos que você use o CSOM para o desenvolvimento de novos aplicativos, se o CSOM inclui a funcionalidade que requer o seu aplicativo. 
  
Para obter informações sobre desenvolvimento com o CSOM, consulte [o modelo de objeto do lado do cliente (CSOM) para o Project 2013](client-side-object-model-csom-for-project-2013.md). Para obter informações sobre a interface REST em aplicativos do SharePoint, consulte *usando o serviço REST do SharePoint de programação* na documentação do desenvolvedor do SharePoint 2013. 
  
### <a name="changes-in-the-reporting-database"></a>Alterações no banco de dados de relatórios
<a name="pj15_WhatsNew_RDBChanges"> </a>

Os quatro bancos de dados no Project Server 2010 são combinados em um único banco de dados de projeto no Project Server 2013. O nome padrão do banco de dados de projeto é ProjectService. Relatórios de tabelas e exibições mantêm seus nomes anteriores e tabelas e modos de exibição dos bancos de dados de rascunho, publicado e arquivamento tem os prefixos `draft`, `pub`, e `ver` no banco de dados ProjectService. Por exemplo, a tabela de projetos publicados é pub. MSP_PROJECTS. 
  
> [!IMPORTANT]
> Direcionar o access não é suportado para o rascunho (`draft` prefixo), publicados (`pub`) e o arquivo morto (`ver`) tabelas e exibições. Relatórios devem usar somente as tabelas e modos de exibição, que possuem relatórios a `dbo` prefixo. Por exemplo, o dbo. Tabela de MSP_EpmProject inclui a lista de projetos na instância do Project Web App. 
>
> Não há nada a ativamente impedir o uso de acesso direto programático banco de dados para atualizar dados em qualquer uma das tabelas e modos de exibição no banco de dados do projeto. Você deve estar ciente de que o cache do Project Professional, as tabelas de dados publicados e de rascunho e as tabelas de relatório todos contam com um protocolo de sincronização do cache que pode ser interrompido por direcionam a edição de dados. Se você danificar seus bancos de dados do Project Server ou corromper o Project Professional do cliente armazena em cache usando o acesso direto para alterar os dados, ser avisado que suporte ao produto não poderão ajudar! 
  
Project Server 2013 introduz um serviço OData para online e acesso local. As tabelas de relatórios online e visualizações são expostas apenas pela interface OData; para uso no local, pode usar a interface do OData ou acessar diretamente o relatório tabelas e modos de exibição no banco de dados ProjectService no farm do SharePoint. Project Online não oferece suporte a um banco de dados multilocatário. Ou seja, várias instâncias do Project Web App cada tem seu próprio banco de dados do Project. O serviço OData internamente executa consultas SQL nas tabelas e modos de exibição de relatórios e fornece uma carga XML ou JSON. Para obter uma introdução ao serviço OData para relatórios no Project Server 2013 e para a referência do esquema **ProjectData** , consulte [ProjectData - Referência de serviço OData do projeto](https://msdn.microsoft.com/en-us/library/office/jj163015.aspx).
  
Para obter informações gerais sobre consultas de OData, consulte [OData: convenções URI](http://www.odata.org/developers/protocols/uri-conventions#FilterSystemQueryOption). Por exemplo, você pode ver todos os projetos em uma instância local do Project Web App, onde o nome do projeto começa com "Test" usando a seguinte consulta em um navegador. Com o botão direito na página do navegador e, em seguida, clique em **Exibir código-fonte**.
  
```html
http://ServerName /ProjectServerName /_api/ProjectData/Projects?$filter=startswith(ProjectName, 'Test') eq true
```

Para importar dados do projeto para o PowerPivot no Excel 2013, na faixa de opções dados, selecione o **feed do OData de dados** no menu suspenso **De outras fontes** . Na caixa de diálogo **Assistente para Conexão de dados** , digite http://ServerName/ProjectServerName/_api/ProjectData/ nos dados de local de feed, escolha **Avançar**e, em seguida, selecione a tabela de **projetos** na página **Selecione tabelas** do assistente. Nome e salve o arquivo. odc e, em seguida, escolha **Concluir**. Na caixa de diálogo **Importar dados** , escolha o **Relatório de tabela dinâmica**. Na planilha do Excel, escolha campos para as linhas de tabela dinâmica e colunas que você deseja mostrar.
  
Os usuários do Project Server no local, que tem as permissões corretas, podem acessar diretamente as tabelas e modos de exibição de relatórios por meio do Microsoft SQL Server para criar relatórios, como faziam no Project Server 2010. No Project Server 2013, os usuários também podem tabelas de relatório do local de acesso por meio da interface de OData. É possível recuperar dados do Project Server online ou local por meio de pontos de extremidade do REST para o serviço OData. Por exemplo, o dbo. Tabela MSP_PROJECT e o dbo. Modo de exibição MSP_EpmProject_UserView pode ser usado para relatórios. Qualquer tabelas ou modos de exibição que têm um `draft`, `pub`, ou `ver` prefixo são apenas para uso interno pelo Project Server e não são para relatórios de uso. Por exemplo, o rascunho. Tabela MSP_TASKS e a publicação. Modo de exibição MSP_PROJECTS_WORKING_VIEW não estão documentadas e são somente para uso interno. 
  
> [!NOTE]
> Você pode estender a emissão de relatórios por meio da adição de tabelas, exibições, campos e procedimentos armazenados em um banco de dados separado no local. Você não deve modificar o relatório de tabelas existentes e modos de exibição no banco de dados do Project Server. 
  
O relatório tabelas, exibições e campos no banco de dados de projeto serão documentados em um arquivo de Ajuda em HTML em uma atualização mais recente do download do SDK do Project 2013. Para obter a documentação do esquema XML de OData para o serviço **ProjectData** , consulte [ProjectData - Referência de serviço OData do projeto](https://msdn.microsoft.com/en-us/library/office/jj163015.aspx). Consultas de relatórios tabelas e modos de exibição que foram criados para o Project Server 2010, na maioria dos casos, funcionará com o banco de dados de projeto no Project Server 2013. Usuários locais podem acessar os cubos OLAP do Project Server no SQL Server Analysis Services, como faziam no momento. Cubos OLAP no Project Online, não estão disponíveis.
  
### <a name="task-pane-add-ins-in-project"></a>Suplementos do tarefa painel no Project
<a name="pj15_WhatsNew_Agave"> </a>

Project Standard 2013 e o Project Professional 2013 suportam a tarefa painel suplementos, que podem ser usados para integrar com e exibir o conteúdo externo em uma página da Web. O painel de tarefas mostra o conteúdo de página da Web que tenha acesso por meio do JavaScript para tarefas, recursos, modos de exibição e dados gerais do projeto. O modelo de objeto JavaScript para o Project pode obter informações sobre um recurso ou tarefa selecionada e obter dados em uma célula selecionada na grade para modos de exibição, como gráfico de Gantt. Tarefa painel suplementos para o Project também podem implementar manipuladores de eventos para a tarefa, recurso ou exibir eventos de seleção alterado. 
  
A Figura 2 mostra o **Olá ProjectData** tarefa painel suplemento que consulta o serviço **ProjectData** e então compara os dados do projeto atual com as médias para todos os projetos. O download do SDK do Project 2013 inclui o código fonte completo para o suplemento. 
  
**Figura 2. Um tarefa painel suplemento no Project Professional pode acessar os dados no Project Server**

![Comparando o projeto atual com todos os projetos] (media/pj15_RestQueryApp_CompareProject.gif "Comparando o projeto atual com todos os projetos")
  
> [!NOTE]
> Project Standard 2013 não é possível integrar diretamente com o Project Server 2013 por meio de suplementos de painel de tarefas. 
  
Suplementos do tarefa painel no Project Professional podem oferecer suporte a Web Parts que são compiladas do Project Server 2013, portanto, os desenvolvedores podem criar uma extensão, uma vez que é executado com o Project Web App e o Project Professional. Tarefas gerais painel suplementos que são desenvolvidos para outros produtos do Office 2013 também podem ser usados com o Project Standard 2013 e Project Professional 2013. Para obter mais informações, consulte [tarefa painel suplementos para o Project](task-pane-add-ins-for-project.md).
  
### <a name="project-server-event-receivers"></a>Receptores de eventos do Project Server
<a name="pj15_WhatsNew_Events"> </a>

Pode haver vários servidores do Project Web App (também chamados de servidores de front-end da web ou WFEs) em um farm do SharePoint que inclui o aplicativo de serviço do projeto de back-end. Receptores de evento também podem ser chamados manipuladores de eventos. Manipuladores de evento local podem ser implementados com o código de confiança total e implantados em todos os WFEs para uma instalação local do Project Server. Receptores de evento remoto podem ser implementados nos serviços da web em servidores locais ou remotos e podem ser acessados por vários WFEs e várias instalações do Project Server. Project Online pode usar somente os receptores de evento remoto.
  
Manipuladores de eventos do Project Server são gerenciados pelo SharePoint para cada instância do Project Web App, em vez de uma página específica de configurações do Project Web App. No aplicativo Administração Central do SharePoint, escolha **Configurações gerais de aplicativos**, escolha **Gerenciar** em **Configurações do PWA**e, em seguida, escolha a instância na lista suspensa **A instância do Project Web App** nas configurações do PWA página. Para adicionar um manipulador de eventos local ou um receptor de evento remoto, escolha **Manipuladores de eventos no servidor**.
  
Para uma instalação local do Project Server, você pode criar um receptor de evento remoto como um recurso do SharePoint que usa a classe [Microsoft.ProjectServer.Client.EventHandlerCreationInformation](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.EventHandlerCreationInformation.aspx) no CSOM do e gerenciar programaticamente a receptor de evento usando os métodos da classe [EventHandlerCollection](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.EventHandlerCollection.aspx) . Para receptores de evento remoto, pré-eventos são síncronas, pós-eventos são assíncronas e há um tempo limite para casos onde o receptor de evento remoto não retorna. 
  
> [!NOTE]
> Administração Central do SharePoint está disponível somente para instalações locais. Para o Project Online e SharePoint Online, você pode adicionar ou remover os receptores de evento remoto usando um pacote de aplicativos baseados em CSOM. 
  
Na página manipuladores de eventos no servidor, o processo para adicionar um manipulador de evento local para uma instalação do Project Server no local é quase o mesmo que o processo descrito no tópico [criar um manipulador de eventos do Project Server e registrar um evento](http://msdn.microsoft.com/en-us/library/gg615466.aspx) do Project Server 2010. A diferença é que a página novo manipulador de eventos possui opções adicionais. Por exemplo, escolha a **Criação do projeto** na lista de **eventos** e, em seguida, escolha **Novo MANIPULADOR de eventos**. Na página de manipulador de evento New, os únicos dois necessário campos são **nome** e a **ordem** (consulte a Figura 3). Se você estiver adicionando um manipulador de eventos de confiança total local, adicione os campos **Nome do Assembly** e o **Nome de classe** ; Deixe a **Url do ponto de extremidade** vazio. Se você estiver adicionando um receptor de evento remoto, adicione a **Url de ponto de extremidade**e deixar vazio o **Nome do Assembly** e o **Nome de classe** . 
  
> [!CAUTION]
> Se você especificar *tanto* o nome de classe de nome/assembly e a URL do ponto de extremidade, Project Server chama somente o local (no local) manipulador de eventos. O receptor de evento remoto será ignorado. 
> 
> Se você criar dois manipuladores de eventos para o mesmo evento, onde um manipulador de eventos é local e um é um receptor de evento remoto e o valor da **ordem** é o mesmo para ambos, o Project Server ignora o receptor de evento remoto. 
  
**Figura 3. Adicionando um manipulador de evento local ou um receptor de evento remoto**

![Configurando um manipulador de eventos ou o receptor de evento] (media/pj15_EventHandlers_NewEventHandler.gif "Configurando um manipulador de eventos ou o receptor de evento")
    
Se precisar de acesso ao PSI conjuntos de dados para um manipulador de eventos de local, você pode copiar o assembly Microsoft.Office.Project.Schema.dll a partir do [Windows]\Microsoft.NET\assembly\GAC\_MSIL\Microsoft.Office.Project.Schema\v4.0_15.0.0.0__ diretório de 71e9bce111e9429c. 

Em vez da PSI, recomendamos que você use as classes de evento no namespace **Microsoft.ProjectServer.Client** ; desenvolvimento com o CSOM não exige a manipulação de conjuntos de dados. Para desenvolver receptores de evento remoto para o Project Online, você deve usar a classe de [evento](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.Event.aspx) e a classe [EventHandlerCreationInformation](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.EventHandlerCreationInformation.aspx) o CSOM. 
  
Antes de implantar um manipulador de eventos do Project Server, instalar e testar o manipulador de eventos completamente em uma instalação de teste do Project Server. Para uma instalação do Project Server no local, se o manipulador de eventos de local que você adicionar ficar inoperante, o serviço de eventos do Project Server 2013 Falha ao carregar os outros manipuladores de evento personalizado válido. Nesse caso, você deve remover o manipulador de eventos do problema e reiniciar o serviço de eventos.
  
> [!NOTE]
> Para uma instalação do Project Server no local, é recomendável que você migre para receptores de evento remoto usando o CSOM para desenvolver receptores de evento. Porque os receptores de evento remoto não tiver código de terceiros em execução dentro do serviço de eventos do Project Server, os receptores de evento remoto são mais estáveis. Administradores locais são aliviados da responsabilidade para manter o serviço de eventos do Project Server. 
  
Para obter informações gerais sobre eventos, consulte [manipulação de eventos de aplicativos do SharePoint](http://msdn.microsoft.com/en-us/library/jj220048%28office.15%29.aspx). 
  
## <a name="deprecated-features"></a>Recursos preteridos
<a name="pj15_WhatsNew_Deprecated"> </a>

> [!NOTE]
> Para obter informações sobre recursos e APIs que são substituídos ou removidos no Project Server 2016 Preview, consulte [o que foi preterido ou removidos no Project Server 2016 Preview](https://technet.microsoft.com/library/mt422816%28v=office.16%29.aspx). 
  
Recursos preteridos ainda estão disponíveis no Project 2013 para algumas soluções, mas não devem ser usados para o desenvolvimento de novos. A maioria das seguintes práticas recomendadas e recursos não funcionam com o Project Online ou com a instalação do local padrão do Project Server 2013 no modo de permissão do SharePoint. As soluções existentes que usam esses recursos podem não funcionar para uma atualização do Project Server 2010 para o Project Server 2013. Embora não preterido soluções que usam recursos podem continuar a funcionar em alguns casos, eles não são suportados totalmente para todas as instalações do Project 2013.
  
Se suas soluções usam recursos preteridos, deve ser testadas amplamente antes da implantação, e você deve modificá-los para suporte de usar recursos tão logo que for possível. Para obter informações sobre como configurar a segurança do Project Server 2013 local para o modo de permissão do Project, consulte a seção de *Modo de permissão do SharePoint* no [que há de novo para profissionais de TI no Project Server 2013](http://technet.microsoft.com/en-us/library/ff631142%28office.15%29.aspx).
  
- **Extensões** [Cenários de extensão do PSI](https://msdn.microsoft.com/library/office/ff843378%28v=office.14%29.aspx) são preteridos e não será suportada em versões futuras. Esses cenários do Project Server 2013 local habilitado integração usando serviços personalizados do Windows Communication Foundation (WCF). 
  
- **Project PSI** A [classe do projeto](https://msdn.microsoft.com/library/office/websvcproject.project_di_pj14mref.aspx%28Office.15%29.aspx) do PSI foi preterida. Para todo o desenvolvimento de novo, use o [CSOM do projeto](https://msdn.microsoft.com/library/office/microsoft.projectserver.client_di_pj14mref.aspx%28Office.15%29.aspx). Project Server 2013 aplicativos que usam o Project PSI continuarão a funcionar, mas o Project Online aplicativos precisará Substitua quaisquer métodos da classe do projeto PSI seus métodos CSOM equivalentes.
  
- **Planejamento de recursos PSI** O [Recurso planejar PSI](https://msdn.microsoft.com/library/office/websvcresourceplan_di_pj14mref.aspx) foi preterida. Ele continuará a ter suporte para o desenvolvimento do Project 2013, mas não será suportado em versões futuras. 
  
- **Interface ASMX para a PSI** A PSI inclui interfaces duplicados para o desenvolvimento de extensões do Project Server no local. A interface de serviços web ASMX foi introduzida com a primeira implementação da PSI no Office Project Server 2007. Project Server 2010 adicionada a interface de serviços WCF, onde o modelo de objeto essencialmente duplica os serviços da web ASMX. Embora o Project Server 2013 continua a suportar ASMX e WCF, novas soluções que exigem a PSI devem usar os serviços WCF. Se possível, devem ser escritas novas soluções usando o CSOM. 
  
  Os serviços da web ASMX da PSI são reduzidos no Project Server 2013. Para trabalhar em futuras versões do Project Server, soluções que usam os serviços da web ASMX devem ser reescritas para usar os serviços WCF ou o CSOM. Para obter mais informações, consulte a seção de *Atualizando aplicativos com as APIs do Project Server* na [programação do Project Server](project-server-programmability.md).
  
- **Provedor de vínculo de objeto (OLP)** Nas versões anteriores do Project Server, o serviço **ObjectLinkProvider** a PSI (consulte [WebSvcObjectLinkProvider](https://msdn.microsoft.com/library/WebSvcObjectLinkProvider.aspx) ) fornece uma maneira de gerenciar links de objeto da web entre tarefas de projetos da empresa e especializadas listas do SharePoint no site do projeto para problemas, riscos, produtos e documentos. No Project Server 2013, o OLP foi preterido. 
  
  Você pode usar a classe de **[RelatedItemManager](http://msdn.microsoft.com/en-us/library/microsoft.sharepoint.client.relateditemmanager.aspx)** em CSOM do SharePoint para criar, ler e excluir links de objeto da web entre itens da lista de tarefas e as outras listas em um site de projeto. Por exemplo, para adicionar um link de um item de tarefa para um problema, você pode usar o método **[AddSingleLink](http://msdn.microsoft.com/en-us/library/office/microsoft.sharepoint.client.relateditemmanager.addsinglelink.aspx)** ou um dos dois métodos semelhantes, **AddSingleLinkFromUrl** ou **AddSingleLinkToUrl**. A classe **RelatedItemManager** também inclui métodos para excluir um link de objeto da web e ler itens relacionados. Para a classe equivalente a JSOM (modelo de objeto JavaScript), consulte [SP. Objeto RelatedItemManager (sp.js)](http://msdn.microsoft.com/en-us/library/jj838582.aspx).
  
  Recomendamos que você use o CSOM do SharePoint para criar aplicativos de tipo de OLP para uma instalação local do Project Server 2013 e Project Online. O namespace [Microsoft. SharePoint](http://msdn.microsoft.com/en-us/library/microsoft.sharepoint.aspx) não inclui um **RelatedItemManager** * * * classe. 
  
- **Permissões personalizadas** Permissões de segurança personalizada para acessar recursos específicos do Project Server ou extensões eram suportadas no Office Project Server 2007, onde um artigo SDK explicado como criá-las modificando diretamente o banco de dados publicado. No Project Server 2010, permissões personalizadas ainda funcionam mas são reduzidas. No Project Server 2013, permissões personalizadas não funcionam com o modo de permissão do SharePoint padrão para instalações locais. Para o modo de permissão do Project, permissões personalizadas são aceitos. Com o Project Online, o acesso direto do banco de dados não é possível. 
  
- **Representação** Representação em aplicativos baseados no PSI, onde o usuário de um aplicativo pode assumir as permissões de segurança de um usuário diferente do Project Server, foi preterida no Project Server 2013. Como anteriormente indicado, um padrão local instalação do Project Server 2013 usa o modo de permissão do SharePoint, que não permitem a representação em grupos de segurança do Project Server. Para obter mais informações, consulte [autenticação, autorização e segurança no SharePoint 2013](http://msdn.microsoft.com/en-us/library/ms457529%28office.15%29.aspx).
  
  Os aplicativos de status são extensões típicas que possam ter usado representação nas versões anteriores do Project Server. Project Server 2010 introduziu o método **ReadStatusForResource** e o método **SubmitStatusForResource** a PSI, juntamente com a permissão global **StatusBrokerPermission** , eliminava a necessidade de representação ler e atualizar o status em nome de outro usuário. O CSOM no Project Server 2013 usa a PSI subjacente transparente habilitar extensões de status e pode ser usada para instalações locais ou Project Online. 
  
- **Extensões do banco de dados de relatório** Adicionar tabelas personalizadas e modos de exibição no banco de dados de relatórios é uma prática comum com versões anteriores do Project Server. Porque o Project Server 2013 combina os quatro bancos de dados de versões anteriores em um banco de dados, upgrades não transferir personalizadas tabelas, exibições ou SPROCs para as tabelas de relatório no banco de dados do Project Server 2013. 
  
  Recomendamos que você use o SQL Azure ou um banco de dados do SQL Server separado para tabelas de relatório personalizadas e modos de exibição, onde é possível gerenciar backups de banco de dados e atualizações. Para o Project Online, isso é necessário.
  
- **Emissão de relatórios** O relatório de tabelas locais e modos de exibição no banco de dados do Project Server e os cubos OLAP, são *não* preterido e permanecem totalmente suportado. No entanto, as tabelas e modos de exibição (o banco de dados relatórios nas versões anteriores do Project Server) os relatórios não são acessíveis no Project Online. Da mesma forma, os cubos OLAP estão disponíveis apenas com as instalações do local do Project Server 2013. Para relatórios de aplicativos com o Project Online, você pode usar o serviço **ProjectData** , por meio de consultas do REST com o protocolo OData. 
  
- **Guia do projeto** Guia do projeto é um recurso padrão em aplicativos de desktop Office Project 2007, onde o conteúdo HTML e JavaScript em um painel de tarefas fornece orientação interativa para Criando e gerenciando projetos. No Project 2010, o guia do projeto não está disponível em uma instalação padrão, mas pode ser habilitado por meio de VBA ou um suplemento do VSTO. O download do SDK do Project 2010 inclui os arquivos modificados do guia do projeto. 
  
  O modelo de objeto do VBA e o modelo de objeto **Microsoft.Office.Interop.MSProject** no Project 2013 ainda incluem os 22 membros da classe **Application** e a classe do **projeto** que pode gerenciar o guia do projeto. No entanto, Project 2013, aplicativos de painel de tarefas podem entrar em conflito com as ações em um painel de tarefas do guia do projeto e o conteúdo do guia do projeto não pode ser distribuído facilmente ou vendidos no Office Store. É altamente recomendável que você desenvolva soluções do painel de tarefa de projeto com suplementos do Office, o conteúdo não personalizado do guia do projeto. Para obter mais informações sobre o guia do projeto, consulte a [Documentação do SDK do Project 2010](http://msdn.microsoft.com/en-us/library/ms512767.aspx).
  
## <a name="comparing-project-server-on-premises-with-project-online"></a>Comparando o Project Server local com o Project Online
<a name="pj15_WhatsNew_Comparing"> </a>

Para ajudá-lo a decidir se deseja usar o Project Server no local ou Project Online e quais tipos de extensões, você pode desenvolver em ambos os casos, a tabela 2 compara os recursos extensíveis de uma instalação local do Project Server 2013 com o Project Online. Tabela 2 não inclui diferenças na implantação, administração e uso. Para obter mais informações sobre o Project Online e Project Server 2013, consulte [Project 2013 para desenvolvedores](http://msdn.microsoft.com/en-US/office/fp161502) e [Project Online](http://www.microsoft.com/project/).
  
**Tabela 2. Local de extensibilidade do Project Server e Project Online**

| Recurso |Project Server no local | Project Online |
|:-----|:-----|:-----|
|**Recursos de programação** <br/> |Aplicativos baseados no CSOM; modelo de programação consistente  <br/>-.NET, Silverlight, bibliotecas de cliente do Windows Phone  <br/>-Biblioteca de JavaScript para extensões da faixa de opções, Web Parts e páginas personalizadas  <br/>-Protocolos OData e REST<br/><br/> Aplicativos baseados no PSI; modelo de programação complexo, também pode criar aplicativos para administração, análise de portfólio, notificações, modo de segurança do Project, o sistema de fila e outras áreas<br/><br/>Extensões PSI  <br/><br/>Permissões personalizadas com segurança em modo Project (obsoleto)  <br/><br/>Representação com a PSI (obsoleto)  <br/><br/>Código de confiança total; instalar extensões no farm do SharePoint  <br/> |Aplicativos baseados no CSOM; modelo de programação consistente  <br/>-.NET, Silverlight, bibliotecas de cliente do Windows Phone<br/>-Biblioteca de JavaScript para extensões da faixa de opções, Web Parts e páginas personalizadas<br/>-Protocolos OData e REST<br/><br/>Pode usar a PSI, mas não suportado: nenhuma OAuth e nenhuma conexão de serviço para<br/><br/>Não há extensões da API do CSOM<br/><br/>Não há permissões personalizadas<br/><br/>Sem representação<br/><br/>Nenhum código de confiança total  <br/> |
|**Bancos de dados personalizados** <br/> |-SQL Azure  <br/>-SQL Server (modificação de tabelas e modos de exibição no Project Server não há suporte para o banco de dados de relatório)  <br/> |-SQL Azure  <br/>-SQL Server (modificação de tabelas e modos de exibição no Project Server não há suporte para o banco de dados de relatório)  <br/> |
|**Emissão de relatórios** <br/> |- Serviço **ProjectData** ; Protocolos OData e REST  <br/>-Relatório de tabelas e modos de exibição no banco de dados do Project Server<br/>-Banco de dados OLAP  <br/> |- Serviço **ProjectData** ; Protocolos OData e REST  <br/> |
|**Manipuladores de eventos** <br/> |-Receptores de evento remoto, acessíveis através de pontos de extremidade do WCF<br/>-Manipuladores de eventos confiança total, instalados no farm do SharePoint  <br/> | -Receptores de evento remoto, acessíveis através de pontos de extremidade do WCF  <br/> |
|**Fluxos de trabalho** <br/> |Fluxos de trabalho declarativos, criados com o SharePoint Designer 2013<br/>-Use apenas em uma instância específica do Project Web App<br/>-Pode importar um design de fluxo de trabalho do Visio 2013<br/>-Pode importar e usar de ações personalizadas<br/><br/> Fluxos de trabalho declarativos, criados com o Visual Studio 2012<br/>-Criar um aplicativo que pode incluir fluxos de trabalho<br/>-Criar um pacote de solução do SharePoint (. wsp) que pode incluir fluxos de trabalho<br/>-Criar modelos de fluxo de trabalho para reutilização<br/>-Criar e usar de ações personalizadas  <br/><br/>Pode usar herdados fluxos de trabalho compilados, criados com WF3.5 (recomendável atualizar para o declarativos WF4 fluxo de trabalho)  <br/> |Fluxos de trabalho declarativos, criados com o SharePoint Designer 2013<br/>-Use apenas em uma instância específica do Project Web App<br/>-Pode importar um design de fluxo de trabalho do Visio 2013<br/>-Pode importar e usar de ações personalizadas  <br/><br/>Fluxos de trabalho declarativos, criados com o Visual Studio 2012<br/>-Criar um aplicativo que pode incluir fluxos de trabalho  <br/>-Criar um pacote de solução do SharePoint (. wsp) que pode incluir fluxos de trabalho<br/>-Criar modelos de fluxo de trabalho para reutilização <br/>-Criar e usar de ações personalizadas  <br/> |
|**Distribuição** <br/> |-Office Store (para aplicativos baseados em CSOM)<br/>-Catálogo de aplicativos privado no SharePoint<br/>-Compartilhamento de arquivo intranet  <br/> |-Office Store<br/>-Catálogo de aplicativos privado no SharePoint  <br/> |

   
## <a name="conclusion"></a>Conclusão
<a name="pj15_WhatsNew_Conclusion"> </a>

Project Server 2013 fornece uma ampla gama de novos recursos de desenvolvimento e cenários em que os parceiros e clientes podem usar para se adaptar e estender os recursos e a eficácia do Project Server em empresas de grandes porte e em organizações de pequenas porte. Você pode usar a infraestrutura para Office 2013 e SharePoint 2013 para ajudar a criar e distribuir aplicativos para o Project 2013 que pode estender significativamente a COMERCIABILIDADE e o uso de aplicativos personalizados. Alguns recursos de extensibilidade e práticas de versões anteriores foram eliminadas no Project 2013, particularmente os serviços de web ASMX do PSI e recursos que envolvem representação ou alterações de banco de dados direta, que não podem ser usadas com o Project Online.
  
A introdução das CSOM do permite acesso programático ao Project Online para uma ampla variedade de dispositivos e usando o JavaScript nos aplicativos da web. O CSOM fornece um modelo de programação mais consistente em comparação com a PSI. Dados do Project Server podem ser acessados de várias maneiras que nas versões anteriores, incluindo através do serviço OData online e pontos de extremidade do REST para relatórios de dados do banco de dados do projeto. Relatórios existentes ainda funcionam da mesma maneira para uso local; novos relatórios tem mais flexibilidade.
  
Suplementos do Office fornecem um novo canal para venda de soluções e integrar o Project Standard 2013 com o conteúdo da web e outros produtos do Office 2013. Também é possível criar novas maneiras de integrar o Project Professional 2013 com dados do Project Server e listas do SharePoint por meio do painel de tarefas suplementos do Office.
  
Para obter mais informações sobre como desenvolver aplicativos e usar os recursos de programação e o CSOM do SharePoint Server 2013, consulte [SharePoint para desenvolvedores](http://msdn.microsoft.com/en-US/sharepoint) e do [Office para desenvolvedores](http://msdn.microsoft.com/en-US/office).
  
## <a name="see-also"></a>Confira também

- [Arquitetura do Project Server 2013](project-server-2013-architecture.md)  
- [Tarefas de programação do Project](project-programming-tasks.md) 
- [Modelo de objeto do cliente (CSOM) para o Project 2013](client-side-object-model-csom-for-project-2013.md) 
- [ProjectData - referência do serviço OData do Project](https://msdn.microsoft.com/en-us/library/office/jj163015.aspx)  
- [Suplementos do painel de tarefas para Project](task-pane-add-ins-for-project.md)   
- [OData: Convenções URI](http://www.odata.org/documentation/uri-conventions#FilterSystemQueryOption)    
- [SharePoint para desenvolvedores](http://msdn.microsoft.com/en-US/sharepoint)    
- [Office para desenvolvedores](http://msdn.microsoft.com/en-US/office)   
- [Manipulação de eventos em aplicativos do SharePoint](http://msdn.microsoft.com/en-us/library/jj220048%28office.15%29.aspx)   
- [Office Store](http://office.microsoft.com/en-us/store/)   
- [Project Online](http://www.microsoft.com/project/)
    

