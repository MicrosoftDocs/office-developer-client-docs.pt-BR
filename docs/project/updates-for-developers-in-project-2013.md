---
title: Atualizações para desenvolvedores no Project
manager: lindalu
ms.date: 12/03/2019
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5b2b22cd-6e28-43a8-9092-b411da8bfb53
description: Os novos recursos incluem um modelo de objeto do lado do cliente (CSOM), interfaces REST, um serviço OData para relatórios, receptores de eventos remotos, fluxos de trabalho declarativos e complementos de painel de tarefas para clientes do Project.
ms.openlocfilehash: c2bc0b475639a8582422b2091169116428367c60
ms.sourcegitcommit: 37080eb0087261320e24e6f067e5f434a812b2d2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/04/2019
ms.locfileid: "39819277"
---
# <a name="updates-for-developers-in-project"></a>Atualizações para desenvolvedores no Project

Os recursos de extensibilidade no Project Server 2013 funcionam com os complementos do Project Online e com instalações locais. Os novos recursos incluem um modelo de objeto do lado do cliente (CSOM), interfaces REST, um serviço OData para relatórios, receptores de eventos remotos, fluxos de trabalho declarativos e complementos de painel de tarefas para clientes do Project. Saiba também sobre os recursos preterido que não devem ser usados para o desenvolvimento de novos.
  
O Project Server 2013 se baseia na estrutura introduzida com o Microsoft Office Project Server 2007 e estendida pelo Project Server 2010. O Project Server 2013 adiciona um modelo de objeto do lado do cliente (CSOM) que é refactorado e simplificado da PSI (Project Server Interface) e inclui uma biblioteca JavaScript e bibliotecas do .NET Framework 4 para aplicativos do Windows, Windows Phone 8 e Microsoft Silverlight. O CSOM foi projetado para desenvolvimento para o Project Online e também funciona com uma instalação local do Project Server. 

Os bancos de dados do Project Server são combinados em um único banco de dados; você pode acessar as tabelas e exibições de relatórios online por meio de um serviço OData. O CSOM e o serviço OData incluem uma interface REST (Representational State Transfer). Fluxos de trabalho do Project Server podem ser criados usando o SharePoint Designer 2013. O Project Professional 2013 pode se integrar aos dados de relatório do Project Server, listas de tarefas do SharePoint e outros conteúdos externos usando o modelo de extensibilidade de Complementos do Office para painéis de tarefas. O Project Standard 2013 pode usar os complementos do painel de tarefas para integrar com conteúdo externo geral.
  
Para obter diagramas e mais informações sobre as principais alterações no Project Server 2013, consulte a arquitetura do [Project Server 2013.](project-server-2013-architecture.md)
  
> [!NOTE]
> O Project Server 2013 foi criado na plataforma SharePoint Server 2013 e o Project 2013 inclui grande parte da mesma infraestrutura que os outros aplicativos do Office 2013. For documentation of the model for SharePoint Add-ins, SharePoint-based workflows, Web Parts, development with other SharePoint features, and documentation of Office Add-ins, see [SharePoint Add-ins](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins), [Office Add-ins,](https://docs.microsoft.com/office/dev/add-ins/overview/office-add-ins)and [SharePoint 2013 development overview](https://msdn.microsoft.com/library/jj164084%28office.15%29.aspx). 
  
## <a name="major-new-features-in-project-2013"></a>Principais recursos novos no Project 2013
<a name="pj15_WhatsNew_MajorNewFeatures"> </a>

Os novos recursos do Project Standard 2013 e do Project Professional 2013 incluem uma interface de usuário aprimorada que corresponde a outros aplicativos do Office 2013 e dá suporte à interface do usuário de estilo moderno no Windows 8, integração com objetos De Arte do Office para relatórios, relatórios de lista baixa e novos recursos de programação para relatórios. O Project Professional 2013 permite compartilhamento e sincronização de projetos mais extensos no SharePoint Server 2013, juntamente com os complementos do painel de tarefas que também são implementados em outros aplicativos do Office 2013, como Word, Excel e Outlook.
  
Há muitos recursos novos no Project Server 2013. Alguns não têm uma história importante de programação, como a nova linha do tempo no Project Web App. Esses recursos serão documentados na ajuda do produto e na documentação do usuário final no Microsoft Office Online e em tópicos direcionados a administradores e profissionais de TI no Microsoft TechNet. Outros novos recursos, como planilhas aprimoradas, facilitam a interação de terceiros com planilhas e status por meio da PSI (Project Server Interface).
  
A adição do Project Online e da Office Store ( para os complementos do Project são alterações abrangentes, onde o Project Server pode ser acessado por meio do https://office.microsoft.com/store) Microsoft Azure. O acesso baseado em nuvem ao Project Server usa um modelo de objeto do lado do cliente (CSOM) para desenvolvimento de complementos com o Microsoft .NET Framework, Microsoft Silverlight, Windows Phone e aplicativos Web que usam JavaScript. Um requisito do Project Online é que os quatro bancos de dados do Project Server de versões anteriores sejam mesclados em um banco de dados.
  
O desempenho e a escalabilidade do Project Server 2013 são aprimorados em muitas áreas, como status da tarefa, quadro de horários e gerenciamento de projetos. Os fluxos de trabalho do Project Server são reprojetados com a versão 4 do Windows Workflow Foundation (WF4). O uso do .NET Framework 4 e do Windows Communication Foundation (WCF) com a PSI melhora a segurança, o desempenho e a escalabilidade. Por exemplo, você pode alterar o protocolo de transporte de aplicativos baseados em WCF usando arquivos de configuração, sem alterar o código do aplicativo ou recompilar. O Project Web App armazena em cache muitas das chamadas PSI nas quais os dados não mudam significativamente.
  
> [!NOTE]
> Para o desenvolvimento com o Project Server 2013, você pode usar o Visual Studio com as extensões de ferramentas do Office e do SharePoint, que podem criar na verdade os complementos para os produtos do Office 2013. O Project Server 2013 requer que o Visual Studio habilita totalmente o desenvolvimento de recursos, como páginas de detalhes do projeto e aplicativos baseados em WCF. As extensões de ferramentas do SharePoint no Visual Studio podem implantar Web Parts e outros recursos do SharePoint diretamente no Project Web App e em outros sites do SharePoint. 
>
> O Visual Studio não é mais necessário para desenvolver fluxos de trabalho do Project Server que usam campos, estágios, fases e tipos de projeto corporativo personalizados que podem ser gerenciados no Project Web App. Embora você possa usar o Visual Studio para desenvolver fluxos de trabalho, eles geralmente são mais fáceis e rápidos de criar usando o SharePoint Designer. O Visual Studio pode ser usado para fluxos de trabalho que exigem acesso ao CSOM ou outras APIs externas. 
  
### <a name="project-add-ins"></a>Suplementos do Project
<a name="pj15_WhatsNew_Apps"> </a>

A distribuição e o marketing de software foram reorganizados com o conceito de um complemento. Para o Project 2013, os complementos podem ser disponibilizados para compra e download da Office Store pública ou distribuídos em um catálogo privado no SharePoint. Um complemento geralmente é um programa interativo independente que executa um pequeno número de tarefas relacionadas. Um complemento do Project pode ser um complemento do painel de tarefas para os clientes do Project Standard 2013 ou do Project Standard 2013, ou um complemento para o Project Server 2013 ou o Project Online.
  
Para obter informações sobre os complementos para os clientes da área de trabalho do Project, consulte Os complementos do painel [de tarefas no Project.](#pj15_WhatsNew_Agave) Para um exemplo do Project Server 2013, confira Criar um complemento do Project Server hospedado [pelo SharePoint.](create-a-sharepoint-hosted-project-server-add-in.md) Além de artigos no SDK de Complementos do Office e do [SharePoint,](https://msdn.microsoft.com/library/fp161507.aspx)o Blog do [Office](https://blogs.office.com/dev/) tem muitas postagens que também são relevantes para o Project 2013 e o Project Online. 
  
Um complemento para o Project Server 2013 pode funcionar com uma instalação local e com o Project Online. Os complementos do Project Server podem incluir Web Parts, receptores de eventos remotos e lógica de negócios. O acesso ao modelo de objeto do Project Server em um complemento é por meio do CSOM, não da PSI. O armazenamento de dados pode ser baseado em nuvem, como com o SQL Azure, externo por meio do Microsoft Business Connectivity Services (BCS), interno com um banco de dados local ou misto.
  
#### <a name="add-in-security"></a>Segurança do add-in

Em geral, as ações realizadas por um complemento são realizadas em nome do usuário que executa o complemento; você não usa explicitamente a representação ou especifica quem pode executar o complemento. As ações não podem exceder o nível de permissão do usuário que executa o complemento. 
  
No Office Developer Tools para Visual Studio 2012, o arquivo AppManifext.xml tem um editor gráfico onde você pode definir o escopo da solicitação de permissão. Por exemplo, para criar um complemento que permita que gerentes  de projeto atualizem seus projetos,  na guia Permissões  do painel designer **AppManifest.xml,** selecione Vários Projetos para o escopo e Gravar para a permissão. Se o usuário do complemento tiver permissões de gerente de projeto, ele poderá executar o complemento para projetos que gerencia. O código no AppManifest.xml arquivo incluiria o seguinte: 
  
```XML
  <AppPermissionRequests>
    <AppPermissionRequest Scope="https://sharepoint/projectserver/projects" Right="Write" />
  </AppPermissionRequests>
```

**Tabela 1. Escopos de solicitação de permissão para os complementos do Project Server**

|Escopo|Permissions|
|:-----|:-----|
|**Project Server** <br/> |**Gerenciar** (requer permissões de administrador do Project Server.)  <br/> |
|**Vários Projetos** <br/> |**Leitura**, **Gravação** (Requer permissões de gerente de projeto para algumas operações; permissões de membro da equipe de projeto para operações de leitura básicas, como atribuições de tarefas.)  <br/> |
|**Projeto único** <br/> |**Leitura**, **Gravação** (requer pelo menos permissões de membro da equipe do projeto; o acesso a alguns dados em um projeto depende de outros níveis de permissão.)  <br/> |
|**Recursos da Empresa** <br/> |**Leitura,** **Gravação** (Requer permissões do gerenciador de recursos.)  <br/> |
|**Statusing** <br/> |**SubmitStatus** (Requer permissão para enviar o status de seus projetos.)  <br/> |
|**Relatórios** <br/> |**Leitura** (Requer permissão para fazer logoff no Project Server.)  <br/> |
|**Fluxo de trabalho** <br/> |**Elevar (Requer** permissão para executar fluxos de trabalho. O complemento é executado com permissões elevadas para habilitar transições de estágio para estágio em um fluxo de trabalho. Lógica de negócios nas transições do estágio de controles do complemento.)  <br/> |
   
> [!NOTE]
> O Project Server 2013 e o Project Online não usam o modelo de autenticação somente aplicativo no SharePoint 2013 (consulte Tipos de política de autorização de complemento no [SharePoint 2013).](https://msdn.microsoft.com/library/124879c7-a746-4c10-96a7-da76ad5327f0%28Office.15%29.aspx) 
  
Para obter informações sobre como desenvolver, distribuir, hospedar e gerenciar os complementos, consulte Os Complementos do [SharePoint](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins) e os [Complementos](https://docs.microsoft.com/office/dev/add-ins/overview/office-add-ins)do Office e tópicos relacionados na documentação de desenvolvedor do SharePoint Server 2013 e do Office 2013. For information about permission request scope for other SharePoint Add-ins, see [Add-in permissions in SharePoint 2013](https://msdn.microsoft.com/library/5f7a8440-3c09-4cf8-83ec-c236bfa2d6c4%28Office.15%29.aspx).
  
### <a name="integrating-with-sharepoint-server"></a>Integração com o SharePoint Server
<a name="pj15_WhatsNew_IntegrationWSS"> </a>

Muitos recursos no Project Web App exigem a nova infraestrutura no SharePoint Server 2013, como OAuth e autenticação baseada em declarações, autorização e permissões do Project Server por meio de grupos do SharePoint, sincronização de projetos com listas de tarefas do SharePoint e fluxos de trabalho declarativos do Project Server. O Aplicativo de Serviço do Project pode ser associado a qualquer conjunto de sites em um farm do SharePoint. A sincronização do projeto pode ser com uma lista de tarefas do SharePoint, onde o SharePoint mantém o projeto. Um projeto corporativo também pode ser sincronizado com uma lista de tarefas do SharePoint, onde o Project Server mantém controle total. Para diagramas de arquitetura e uma explicação da sincronização do projeto, consulte a arquitetura do [Project Server 2013.](project-server-2013-architecture.md)
  
Há muitos recursos novos no SharePoint Server 2013. Para saber mais, confira [SharePoint para desenvolvedores.](https://msdn.microsoft.com/sharepoint)
  
### <a name="integrating-with-workflows"></a>Integração com fluxos de trabalho
<a name="pj15_WhatsNew_Workflow"> </a>

Os fluxos de trabalho são um recurso fundamental do gerenciamento de portfólio de projetos. Um ciclo de vida do projeto pode incluir processos de execução longa que abrangem muitas fases. As fases de governança incluem propostas de projeto, análises de impacto nos negócios e seleção, criação, planejamento, gerenciamento e acompanhamento de projetos.
  
Fluxos de trabalho do Project Server 2013 são construídos na plataforma de fluxo de trabalho SharePoint 2013, que usa WF4. Ao contrário das versões anteriores, fluxos de trabalho declarativos para o Project Server 2013 podem ser criados usando o SharePoint Designer 2013 e são acessíveis para uso local e online. Os fluxos de trabalho do Project Server usam o modelo de segurança de fluxo de trabalho do SharePoint com o OAuth e podem ser instalados em um site do Project Web App. A Figura 1 mostra que o SharePoint Designer 2013 pode adicionar estágios a um fluxo de trabalho de site para Gerenciamento de Demanda, onde os estágios são definidos no Project Web App.
  
**Figura 1. Usando o SharePoint Designer para adicionar um estágio a um fluxo de trabalho para o Project Web App**

![Adicionar um estágio a um fluxo de trabalho no SPD](media/pj15_CreateWorkflowSPD_AddStageInSPD.gif "Adicionar um estágio a um fluxo de trabalho no SPD")

<br/>

Você cria um fluxo de trabalho declarativo adicionando estágios de fluxo de trabalho, ações, condições e outros elementos em uma ferramenta de design, que pode ser SharePoint Designer 2013 ou Visual Studio 2012. Em seguida, a ferramenta de design salva o fluxo de trabalho como código XAML, que é interpretado no tempo de execução. Fluxos de trabalho declarativos podem ser executados no Project Server 2013 local ou no Project Online. Usando o Visual Studio 2012, você também pode criar formulários e ações personalizadas para controle adicional e salvar modelos de fluxo de trabalho para reutilização com várias instâncias do Project Web App. O SharePoint Designer 2013 pode consumir ações personalizadas criadas no Visual Studio 2012.
  
Um fluxo de trabalho do Project Server 2013 atua como um aplicativo, onde um administrador que tem permissões de design para o Project Web App pode publicar um fluxo de trabalho declarativo e associá-lo a um tipo de projeto corporativo (EPT). O EPT deve ser para um projeto corporativo, onde o Project Server mantém controle total. Uma lista de tarefas do SharePoint não pode usar um fluxo de trabalho do Project Server. 
  
O OAuth permite que gerentes de projeto com permissões de criação de projeto invoquem o fluxo de trabalho sem usar a representação. Chamadas de fluxo de trabalho para o Project Server, por exemplo, para ler um valor de campo personalizado para decidir qual ramificação seguir, são feitas em nome do gerente de projeto. Para impedir que o gerente de projeto de criar um fluxo de trabalho que avança automaticamente para o próximo estágio, a chamada para mover para o próximo estágio do fluxo de trabalho é executado como o autor do fluxo de trabalho (o administrador). Por outro lado, os usuários de fluxos de trabalho herdados do Project Server 2010 fazem chamadas personificados por meio da conta de Usuário do Proxy de Fluxo de Trabalho para obter acesso de administrador em todo o fluxo de trabalho.
  
Embora o Project Server 2013 local possa usar fluxos de trabalho compilados baseados em WF3.5, recomendamos que você atualize fluxos de trabalho herdados para fluxos de trabalho declarativos com base em WF4. A tecnologia mais nova é mais escalonável e robusta. Analistas de negócios e a equipe de PMO podem criar ou atualizar designs de fluxo de trabalho usando o Visio 2013 e implementar fluxos de trabalho do Project Server sem codificação usando o SharePoint Designer 2013.
  
Para obter informações sobre como criar um fluxo de trabalho declarativo para o Project Web App, consulte [Getting started developing Project Server workflows](getting-started-developing-project-server-workflows.md). For a comparison of SharePoint Designer and Visual Studio capabilities for workflows, see [Develop SharePoint 2013 workflows using Visual Studio](https://msdn.microsoft.com/library/office/jj163199.aspx).
  
### <a name="client-side-object-model"></a>Modelo de objeto do lado do cliente
<a name="pj15_WhatsNew_CSOM"> </a>

O acesso programático ao Project Online requer um CSOM criado no CSOM do SharePoint. A autenticação do Project Online será com o OAuth usando uma ID do Windows Live, não a autenticação do Project Server Forms ou a autenticação do Windows.
  
A seguir estão os princípios e recursos do CSOM no Project Server 2013:
  
- O CSOM foi projetado para facilitar o uso. Por exemplo, métodos e propriedades usam ou fornecem dados diretamente por nome, em vez de exigir muitos GUIDs,  _parâmetros changeXml_ ou passar conjuntos de dados. 
    
- O CSOM do Project Server implementa um subconjunto da funcionalidade psi, com base nos requisitos mais comuns para soluções de terceiros.
    
- O CSOM chama internamente a PSI, mas é fatorado de forma diferente. Por exemplo, as atualizações de todas as alterações de status são feitas por meio do método **StatusAssignmentCollection.SubmitAllStatusUpdates,** não pelo método **PSI Statusing.SubmitStatus** do usuário ou pelo **método SubmitStatusForResource** para outros recursos. 
    
- O CSOM é acessível por meio de um serviço WCF (Client.svc), e não por meio dos 22 serviços públicos da PSI.
    
- A inicialização do CSOM do Project Server é feita diretamente por meio da classe [ProjectContext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx) com a URL do Project Web App, não usando uma referência do WCF ou assembly de proxy. 
    
- O CSOM implementa várias bibliotecas de cliente e interfaces, que são suportadas pela infraestrutura interna do CSOM do SharePoint. As interfaces e bibliotecas do cliente incluem o seguinte:
    
  - Biblioteca de cliente do Microsoft .NET no assembly Microsoft.ProjectServer.Client.dll linha
    
  - Biblioteca Silverlight no assembly Microsoft.ProjectServer.Client.Silverlight.dll conjunto
    
  - Biblioteca do Windows Phone 8 no assembly Microsoft.ProjectServer.Client.Phone.dll linha
    
  - Biblioteca JavaScript para aplicativos Web no arquivo PS.js ou arquivo PS.debug.js arquivo
    
  - Pontos de extremidade REST, para acesso com o protocolo OData
    
  - Suporte nativo para consultas LINQ com filtragem, para limitar a quantidade de dados retornados
    
- O CSOM pode ser usado para soluções do Project Online e para soluções locais, independentemente da PSI e de outros assemblies do Project Server, como Microsoft.Office.Project.Server.Library.dll.
    
- A funcionalidade adicional do CSOM do Project Server 2013 pode ser considerada para atualizações cumulativas e service packs, com base em solicitações de parceiros do Project Server e da comunidade de desenvolvedores.
    
> [!NOTE]
> O CSOM é a interface preferida para desenvolvedores do Project Server de terceiros. Recomendamos que você use o CSOM para o desenvolvimento de novos aplicativos, caso o CSOM inclua a funcionalidade exigida por seu aplicativo. 
  
For information about developing with the CSOM, see [Client-side object model (CSOM) for Project 2013](client-side-object-model-csom-for-project-2013.md). For information about the REST interface in SharePoint applications,  *see Programming using the SharePoint REST service*  in the SharePoint 2013 developer documentation. 
  
### <a name="changes-in-the-reporting-database"></a>Alterações no banco de dados relatórios
<a name="pj15_WhatsNew_RDBChanges"> </a>

Os quatro bancos de dados no Project Server 2010 são combinados em um único banco de dados do Project no Project Server 2013. O nome padrão do banco de dados do Project é ProjectService. As tabelas e exibições de relatório mantêm seus nomes anteriores, e as tabelas e exibições dos bancos de dados Rascunho, Publicado e Arquivo têm os prefixos e no banco de dados  `draft`  `pub`  `ver` ProjectService. Por exemplo, a tabela de projetos publicados é pub. MSP_PROJECTS. 
  
> [!IMPORTANT]
> O acesso direto não tem suporte para tabelas e exibições de rascunho `draft` (prefixo), publicados ( ) e de `pub` arquivo morto `ver` (). Os relatórios devem usar apenas as tabelas e exibições de relatórios, que têm o `dbo` prefixo. Por exemplo, o dbo. MSP_EpmProject tabela inclui a lista de projetos na instância do Project Web App. 
>
> Não há nada que o impeça ativamente de usar o acesso direto programático ao banco de dados para atualizar dados em qualquer uma das tabelas e exibições no banco de dados do Project. Você deve estar ciente de que o cache do Project Professional, as tabelas de rascunho e de dados publicados e as tabelas de relatórios dependem de um protocolo de sincronização de cache que pode ser interrompido pela edição direta de dados. Se você danificar seus bancos de dados do Project Server ou corromper caches do lado do cliente do Project Professional usando o acesso direto para alterar dados, seja avisado de que o suporte ao produto não poderá ajudar! 
  
O Project Server 2013 introduz um serviço OData para acesso online e local. As tabelas e exibições de relatórios online são expostas apenas pela interface OData; para uso local, você pode usar a interface OData ou acessar diretamente as tabelas e exibições de relatórios no banco de dados ProjectService no farm do SharePoint. O Project Online não dá suporte a um banco de dados multi-intencional. Ou seja, várias instâncias do Project Web App têm seu próprio banco de dados do Project. O serviço OData executa internamente consultas SQL nas tabelas e exibições de relatórios e fornece uma carga XML ou JSON. For an introduction to the OData service for reporting in Project Server 2013, and for the **ProjectData** schema reference, see [ProjectData - Project OData service reference](https://msdn.microsoft.com/library/office/jj163015.aspx).
  
Para obter informações gerais sobre consultas OData, consulte [OData: convenções de URI](https://www.odata.org/documentation/). Por exemplo, você pode ver todos os projetos em uma instância local do Project Web App onde o nome do projeto começa com "Test" usando a seguinte consulta em um navegador. Clique com o botão direito do mouse na página do navegador e clique em **Exibir origem.**
  
```html
https://ServerName /ProjectServerName /_api/ProjectData/Projects?$filter=startswith(ProjectName, 'Test') eq true
```

Para importar dados de projeto para o PowerPivot no Excel 2013,  na faixa de opções DE DADOS, selecione Do feed de dados **OData** no menu suspenso De Outras Fontes. Na caixa **de diálogo** Assistente para Conexão de Dados, digite o local do feed de dados, escolha Próximo e selecione a tabela Projetos na página Selecionar Tabelas https://ServerName/ProjectServerName/_api/ProjectData/ do assistente.    Nome e salve o arquivo .odc e escolha **Concluir.** Na caixa **de diálogo Importar Dados,** escolha **Relatório de Tabela Dinâmica.** Na planilha do Excel, escolha campos para as linhas e colunas da tabela dinâmica que você deseja mostrar.
  
Os usuários locais do Project Server, que têm as permissões corretas, podem acessar diretamente as tabelas e exibições de relatórios por meio do Microsoft SQL Server para criar relatórios, como no Project Server 2010. No Project Server 2013, os usuários também podem acessar as tabelas de relatórios locais por meio da interface OData. Você pode recuperar dados online ou locais do Project Server por meio de pontos de extremidade REST para o serviço OData. Por exemplo, a tabela dbo.MSP_PROJECT e a exibição dbo.MSP_EpmProject_UserView pode ser usada para relatórios. Quaisquer tabelas ou exibições que tenham um prefixo , ou sejam apenas para uso interno pelo Project Server e não são para uso  `draft`  `pub` de  `ver` relatórios. Por exemplo, o rascunho. MSP_TASKS a tabela e o pub. MSP_PROJECTS_WORKING_VIEW de exibição não estão documentados e são apenas para uso interno. 
  
> [!NOTE]
> Você pode estender os relatórios locais adicionando tabelas, exibições, campos e procedimentos armazenados em um banco de dados separado. Você não deve modificar as tabelas e exibições de relatórios existentes no banco de dados do Project Server. 
  
As tabelas, exibições e campos de relatório no banco de dados do Project serão documentados em um arquivo de Ajuda HTML em uma atualização posterior do download do SDK do Project 2013. Para documentação do esquema XML OData para o **serviço ProjectData,** consulte [ProjectData - referência de serviço OData do Project.](https://msdn.microsoft.com/library/office/jj163015.aspx) Consultas das tabelas e exibições de relatórios que foram criadas para o Project Server 2010 irão, na maioria dos casos, trabalhar com o banco de dados do Project no Project Server 2013. Os usuários locais podem acessar os cubos OLAP do Project Server no SQL Server Analysis Services, como fazem atualmente. No Project Online, os cubos OLAP não estão disponíveis.
  
### <a name="task-pane-add-ins-in-project"></a>Task pane add-ins in Project
<a name="pj15_WhatsNew_Agave"> </a>

O Project Standard 2013 e o Project Professional 2013 suportam os complementos do painel de tarefas, que podem ser usados para integrar e exibir conteúdo externo em uma página da Web. O painel de tarefas mostra o conteúdo da página da Web que tem acesso por meio do JavaScript a tarefas, recursos, exibições e dados gerais do projeto. O modelo de objeto JavaScript para Project pode obter informações sobre uma tarefa ou recurso selecionado e pode obter dados em uma célula selecionada na grade para exibições como o gráfico de Gantt. Os complementos do painel de tarefas do Project também podem implementar manipuladores de eventos para eventos alterados de tarefa, recurso ou exibição de seleção. 
  
A Figura 2 mostra o complemento do painel de tarefas **Hello ProjectData** que consulta o serviço **ProjectData** e compara os dados no projeto atual com as médias de todos os projetos. O download do SDK do Project 2013 inclui o código-fonte completo do complemento. 
  
**Figura 2. Um complemento do painel de tarefas no Project Professional pode acessar dados no Project Server**

![Comparing the current project with all projects](media/pj15_RestQueryApp_CompareProject.gif "Comparing the current project with all projects")
  
> [!NOTE]
> O Project Standard 2013 não pode se integrar diretamente ao Project Server 2013 por meio de complementos de painel de tarefas. 
  
Os complementos do painel de tarefas no Project Professional podem dar suporte a Web Parts criadas para o Project Server 2013, para que os desenvolvedores possam criar uma extensão uma vez que seja executado com o Project Web App e o Project Professional. Os complementos gerais do painel de tarefas desenvolvidos para outros produtos do Office 2013 também podem ser usados com o Project Standard 2013 e o Project Professional 2013. Para obter mais informações, [consulte Os complementos do painel de tarefas do Project.](task-pane-add-ins-for-project.md)
  
### <a name="project-server-event-receivers"></a>Receptores de eventos do Project Server
<a name="pj15_WhatsNew_Events"> </a>

Pode haver vários servidores do Project Web App (também chamados de servidores web front-end ou WFEs) em um farm do SharePoint que inclui o Aplicativo de Serviço do Project back-end. Receptores de eventos também podem ser chamados de manipuladores de eventos. Os manipuladores de eventos locais podem ser implementados com código de confiança total e implantados em todos os WFEs para uma instalação local do Project Server. Os receptores de eventos remotos podem ser implementados em serviços Web em servidores locais ou remotos e acessados por vários WFEs e várias instalações do Project Server. O Project Online só pode usar receptores de eventos remotos.
  
Os manipuladores de eventos do Project Server são gerenciados pelo SharePoint para cada instância do Project Web App, e não por uma página específica de Configurações do Project Web App. No aplicativo da Administração Central do SharePoint,  escolha Configurações Gerais de Aplicativos, escolha Gerenciar em Configurações do **PWA** e, em seguida, escolha a instância na lista drop-down da Instância do Project Web **App** na página Configurações do PWA. Para adicionar um manipulador de eventos local ou um receptor de eventos remotos, escolha **Manipuladores de Eventos** do Lado do Servidor.
  
Para uma instalação local do Project Server, você pode criar um receptor de eventos remotos como um recurso do SharePoint que usa a classe [Microsoft.ProjectServer.Client.EventHandlerCreationInformation](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.EventHandlerCreationInformation.aspx) no CSOM e, em seguida, gerenciar programaticamente o receptor de evento usando métodos na classe [EventHandlerCollection.](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.EventHandlerCollection.aspx) Para receptores de eventos remotos, os pré-eventos são síncronos, pós-eventos são assíncronos e há um tempo para casos em que o receptor de eventos remotos não retorna. 
  
> [!NOTE]
> A Administração Central do SharePoint está disponível apenas para instalações locais. Para o Project Online e o SharePoint Online, você pode adicionar ou remover receptores de eventos remotos usando um pacote de aplicativo baseado em CSOM. 
  
Na página Manipuladores de Eventos do Lado do Servidor, o processo para adicionar um manipulador de eventos local para uma instalação local do Project Server é quase o mesmo que o processo descrito em Criar um manipulador de eventos do [Project Server](https://msdn.microsoft.com/library/gg615466.aspx) e registrar um tópico de evento para o Project Server 2010. A diferença é que a página Novo Manipulador de Eventos tem opções adicionais. For example, choose **Project Creating** in the **Events** list, and then choose NEW **EVENT HANDLER**. Na página Novo Manipulador de Eventos, os dois únicos campos obrigatórios são **Nome** e Ordem **(consulte** a Figura 3). Se você estiver adicionando um manipulador de eventos de confiança total local, adicione o campo Nome do **Assembly** e o **campo Nome da** Classe; deixe **a URL do ponto de extremidade** vazia. Se você estiver adicionando um receptor de eventos remoto, adicione **a URL do ponto** de extremidade e deixe o Nome do Assembly **e** o Nome da **Classe vazios.** 
  
> [!CAUTION]
> Se você especificar  *o*  nome/nome da classe do assembly e a URL do ponto de extremidade, o Project Server chamará somente o manipulador de eventos local (local). O receptor de eventos remoto é ignorado. 
> 
> Se você criar dois manipuladores de eventos para o mesmo evento, onde um manipulador de eventos é local e um é um receptor de eventos remoto, e o valor **order** é o mesmo para ambos, o Project Server ignora o receptor de eventos remoto. 
  
**Figura 3. Adicionando um manipulador de eventos local ou um receptor de eventos remoto**

![Configuring an event handler or event receiver](media/pj15_EventHandlers_NewEventHandler.gif "Configuring an event handler or event receiver")
    
Se você precisar acessar conjuntos de dados da PSI para um manipulador de eventos local, poderá copiar o assembly Microsoft.Office.Project.Schema.dll do diretório [Windows]\Microsoft.NET\assembly\GAC \_ MSIL\Microsoft.Office.Project.Schema\v4.0_15.0.0.0__71e9bce111e9429c. 

Em vez da PSI, recomendamos que você use as classes de evento no namespace **Microsoft.ProjectServer.Client;** o desenvolvimento com o CSOM não exige manipulação de conjuntos de dados. Para desenvolver receptores de eventos remotos para o Project Online, você deve usar a classe [Event](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.Event.aspx) e a classe [EventHandlerCreationInformation](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.EventHandlerCreationInformation.aspx) no CSOM. 
  
Antes de implantar um manipulador de eventos do Project Server, instale e teste completamente o manipulador de eventos em uma instalação de teste do Project Server. Para uma instalação local do Project Server, se o manipulador de eventos local que você adicionar ficar inoperante, o Serviço de Eventos do Project Server 2013 não carregará os outros manipuladores de eventos personalizados válidos. Nesse caso, você deve remover o manipulador de eventos do problema e reiniciar o serviço de Eventos.
  
> [!NOTE]
> Para uma instalação local do Project Server, recomendamos migrar para receptores de eventos remotos usando o CSOM para desenvolver receptores de eventos. Como os receptores de eventos remotos não têm código de terceiros em execução no Serviço de Eventos do Project Server, os receptores de eventos remotos são mais estáveis. Os administradores locais são responsáveis pela manutenção do Serviço de Eventos do Project Server. 
  
Para obter informações gerais sobre eventos, consulte [Manipulando eventos em aplicativos para SharePoint](https://msdn.microsoft.com/library/jj220048%28office.15%29.aspx). 
  
## <a name="deprecated-features"></a>Recursos preteridos
<a name="pj15_WhatsNew_Deprecated"> </a>

> [!NOTE]
> Para obter informações sobre recursos e APIs que foram preterido ou removidos no Project Server 2016 Preview, consulte O que foi preterido ou removido no [Project Server 2016 Preview.](https://docs.microsoft.com/project/what-s-deprecated-or-removed-in-project-server-2016) 
  
Os recursos preterido ainda estão disponíveis no Project 2013 para algumas soluções, mas não devem ser usados para o desenvolvimento de novos. A maioria dos seguintes recursos e práticas não funciona com o Project Online ou com a instalação local padrão do Project Server 2013 no modo de permissão do SharePoint. Soluções existentes que usam esses recursos podem não funcionar para uma atualização do Project Server 2010 para o Project Server 2013. Embora as soluções que usam recursos preterido possam continuar a funcionar em alguns casos, elas não têm suporte total para todas as instalações do Project 2013.
  
Se suas soluções usam recursos preterido, elas devem ser testadas completamente antes da implantação, e você deve modificá-las para usar os recursos com suporte assim que for prático. For information about configuring on-premises Project Server 2013 security for Project permission mode, see the *SharePoint Permission Mode* section in [What's new for IT pros in Project Server 2013.](https://docs.microsoft.com/project/what-s-new-for-it-pros-in-project-server-2016)
  
- **Os cenários** de extensão da [PSI](https://docs.microsoft.com/previous-versions/office/developer/office-2010/ff843378(v=office.14)) de extensões foram preterido e não terão suporte em versões futuras. Esses cenários locais do Project Server 2013 habilitaram a integração usando serviços personalizados do Windows Communication Foundation (WCF). 
  
- **PSI do Project** A [classe Project](https://docs.microsoft.com/office/client-developer/project/project-psi-reference-overview) da PSI foi preterida. Para todos os novos desenvolvimentos, use [o CSOM do Project.](client-side-object-model-csom-for-project-2013.md) Os aplicativos do Project Server 2013 que usam o Psi do Project continuarão a funcionar, mas os aplicativos do Project Online precisarão substituir quaisquer métodos PSI da classe Project por seus métodos CSOM equivalentes.
  
- **PSI do Plano de Recursos** A [PSI do Plano](https://docs.microsoft.com/previous-versions/office/project-class/gg240019(v=office.15)) de Recursos foi preterida. Ele continuará a ter suporte para o desenvolvimento do Project 2013, mas não terá suporte em versões futuras. 
  
- **Interface ASMX para PSI** A PSI inclui interfaces duplicadas para o desenvolvimento de extensões locais do Project Server. A interface de serviços Web ASMX foi introduzida com a primeira implementação da PSI no Office Project Server 2007. O Project Server 2010 adicionou a interface de serviços do WCF, onde o modelo de objeto duplica essencialmente os serviços Web ASMX. Embora o Project Server 2013 continue a dar suporte ao ASMX e ao WCF, novas soluções que exigem o PSI devem usar os serviços do WCF. Se possível, novas soluções devem ser escritas usando o CSOM. 
  
  Os serviços Web ASMX da PSI foram preterido no Project Server 2013. Para funcionar em versões futuras do Project Server, as soluções que usam os serviços Web ASMX devem ser reescritas para usar os serviços WCF ou o CSOM. Para obter mais informações, consulte a *seção Atualizando aplicativos* com as APIs do Project Server na [programação do Project Server.](project-server-programmability.md)
  
- **Object Link Provider (OLP)** Em versões anteriores do Project Server, o serviço **ObjectLinkProvider** no PSI (consulte [WebSvcObjectLinkProvider](https://docs.microsoft.com/previous-versions/office/ms481347(v=office.14)) fornece uma maneira de gerenciar links de objeto da Web entre tarefas de projeto corporativo e listas especializadas do SharePoint no site do projeto para problemas, riscos, entregas e documentos. No Project Server 2013, a OLP foi preterida. 
  
  Você pode usar a classe **[RelatedItemManager](https://docs.microsoft.com/previous-versions/office/sharepoint-server/jj168020(v=office.15))** no SharePoint CSOM para criar, ler e excluir links de objeto da Web entre itens na lista de tarefas e as outras listas em um site de projeto. Por exemplo, para adicionar um link de um item de tarefa a um problema, você pode usar o método **[AddSingleLink](https://docs.microsoft.com/previous-versions/office/sharepoint-server/jj166451(v=office.15))** ou um dos dois métodos semelhantes, **AddSingleLinkFromUrl** ou **AddSingleLinkToUrl**. A **classe RelatedItemManager** também inclui métodos para excluir um link de objeto da Web e ler itens relacionados. Para a classe equivalente no JSOM (o modelo de objeto do JavaScript), consulte [SP. Objeto RelatedItemManager (sp.js)](https://docs.microsoft.com/previous-versions/office/sharepoint-visio/jj838582(v=office.15)).
  
  Recomendamos que você use o CSOM do SharePoint para criar aplicativos do tipo OLP para uma instalação local do Project Server 2013 e para o Project Online. O namespace [Microsoft.SharePoint](https://docs.microsoft.com/previous-versions/office/sharepoint-server/ms464984(v=office.15)) não inclui uma **classe RelatedItemManager** *****. 
  
- **Permissões personalizadas** Permissões de segurança personalizadas para acessar recursos ou extensões específicos do Project Server eram suportadas no Office Project Server 2007, onde um artigo do SDK explicava como criar essas extensões modificando diretamente o banco de dados Publicado. No Project Server 2010, as permissões personalizadas ainda funcionam, mas foram preteridas. No Project Server 2013, as permissões personalizadas não funcionam com o modo de permissão padrão do SharePoint para instalações locais. Para o modo de permissão do Project, há suporte para permissões personalizadas. Com o Project Online, o acesso direto ao banco de dados não é possível. 
  
- **Representação** A representação em aplicativos baseados em PSI, onde o usuário de um aplicativo pode assumir as permissões de segurança de um usuário diferente do Project Server, foi preterida no Project Server 2013. Como indicado anteriormente, uma instalação local padrão do Project Server 2013 usa o modo de permissão do SharePoint, que não permite a representação nos grupos de segurança do Project Server. Para obter mais informações, consulte [Autenticação, autorização e segurança no SharePoint 2013.](https://docs.microsoft.com/sharepoint/dev/general-development/authentication-authorization-and-security-in-sharepoint)
  
  Aplicativos de status são extensões típicas que podem ter usado a representação em versões anteriores do Project Server. O Project Server 2010 introduziu o método **ReadStatusForResource** e o método **SubmitStatusForResource** na PSI, juntamente com a permissão global **StatusBrokerPermission,** que eliminou a necessidade de representação ler e atualizar o status em nome de outro usuário. O CSOM no Project Server 2013 usa o PSI subjacente para habilitar de forma transparente extensões de status e pode ser usado para instalações locais ou do Project Online. 
  
- **Relatórios de extensões de banco de dados** Adicionar tabelas e exibições personalizadas ao banco de dados relatórios é uma prática comum com versões anteriores do Project Server. Como o Project Server 2013 combina os quatro bancos de dados de versões anteriores em um banco de dados, as atualizações não transferem tabelas, exibições ou SPROCs personalizados para as tabelas de relatórios no banco de dados do Project Server 2013. 
  
  Recomendamos que você use o SQL Azure ou um banco de dados do SQL Server separado para tabelas e exibições de relatórios personalizadas, onde você pode gerenciar backups e atualizações de banco de dados. Para o Project Online, isso é necessário.
  
- **Relatórios** As tabelas e exibições de relatórios locais no banco  de dados do Project Server e os cubos OLAP não foram preterido e permanecem totalmente suportados. No entanto, as tabelas e exibições de relatórios (o banco de dados de relatórios em versões anteriores do Project Server) não estão acessíveis no Project Online. Da mesma forma, os cubos OLAP estão disponíveis apenas com instalações locais do Project Server 2013. Para aplicativos de relatório com o Project Online, você pode usar o **serviço ProjectData,** por meio de consultas REST com o protocolo OData. 
  
- **Guia do projeto** O Guia do Projeto é um recurso padrão nos aplicativos da área de trabalho do Office Project 2007, onde o conteúdo HTML e JavaScript em um painel de tarefas fornece orientações interativas para criar e gerenciar projetos. No Project 2010, o Guia do Projeto não está disponível em uma instalação padrão, mas pode ser habilitado por meio do VBA ou de um complemento VSTO. O download do SDK do Project 2010 inclui os arquivos modificados do Guia do Projeto. 
  
  O modelo de objeto do VBA e o modelo de objeto **Microsoft.Office.Interop.MSProject** no Project 2013 ainda incluem os 22 membros da classe **Application** e a classe **Project** que podem gerenciar o Guia do Projeto. No entanto, os aplicativos do painel de tarefas do Project 2013 podem entrar em conflito com as ações em um painel de tarefas do Guia do Projeto e o conteúdo do Guia do Projeto não pode ser facilmente distribuído ou vendido na Office Store. Recomendamos que você desenvolva soluções do painel de tarefas do Project com os Complementos do Office, não com o conteúdo personalizado do Guia do Projeto. Para obter mais informações sobre o Guia do Projeto, consulte a Documentação do [SDK do Project 2010.](https://msdn.microsoft.com/library/ms512767.aspx)
  
## <a name="comparing-project-server-on-premises-with-project-online"></a>Comparando o Project Server local com o Project Online
<a name="pj15_WhatsNew_Comparing"> </a>

Para ajudá-lo a decidir se vai usar o Project Server local ou o Project Online e quais tipos de extensões você pode desenvolver em ambos os casos, a Tabela 2 compara os recursos extensíveis de uma instalação local do Project Server 2013 com o Project Online. A Tabela 2 não inclui diferenças na implantação, administração ou uso. Para obter mais informações sobre o Project Online e o Project Server 2013, consulte [o Project 2013](https://developer.microsoft.com/project/docs) para desenvolvedores e [o Project Online.](https://developer.microsoft.com/project)
  
**Tabela 2. Extensibilidade do Project Server local e do Project Online**

| Recurso |Project Server local | Project Online |
|:-----|:-----|:-----|
|**Programabilidade** <br/> |Aplicativos baseados em CSOM; modelo de programação consistente  <br/>- Bibliotecas de cliente .NET, Silverlight, Windows Phone  <br/>- Biblioteca JavaScript para páginas personalizadas, Web Parts e extensões da faixa de opções  <br/>- Protocolos OData e REST<br/><br/> Aplicativos baseados em PSI; complex programming model, can also create apps for administration, portfolio analysis, notifications, Project mode security, queue system, and other areas<br/><br/>Extensões psi  <br/><br/>Permissões personalizadas com segurança do modo project (preterido)  <br/><br/>Representação com a PSI (preterida)  <br/><br/>Código de confiança total; instalar extensões no farm do SharePoint  <br/> |Aplicativos baseados em CSOM; modelo de programação consistente  <br/>- Bibliotecas de cliente .NET, Silverlight, Windows Phone<br/>- Biblioteca JavaScript para páginas personalizadas, Web Parts e extensões da faixa de opções<br/>- Protocolos OData e REST<br/><br/>Pode usar a PSI, mas não tem suporte: nenhum OAuth e nenhuma conexão de serviço a serviço<br/><br/>Nenhuma extensão da API do CSOM<br/><br/>Sem permissões personalizadas<br/><br/>Nenhuma representação<br/><br/>Nenhum código de confiança total  <br/> |
|**Bancos de dados personalizados** <br/> |- SQL Azure  <br/>- SQL Server (não há suporte para modificação de tabelas e exibições de relatórios no banco de dados do Project Server)  <br/> |- SQL Azure  <br/>- SQL Server (não há suporte para modificação de tabelas e exibições de relatórios no banco de dados do Project Server)  <br/> |
|**Relatórios** <br/> |- **Serviço ProjectData;** Protocolos OData e REST  <br/>- Relatórios de tabelas e exibições no banco de dados do Project Server<br/>- Banco de dados OLAP  <br/> |- **Serviço ProjectData;** Protocolos OData e REST  <br/> |
|**Manipuladores de eventos** <br/> |- Receptores de eventos remotos, acessíveis por meio de pontos de extremidade do WCF<br/>– Manipuladores de eventos de confiança total, instalados no farm do SharePoint  <br/> | - Receptores de eventos remotos, acessíveis por meio de pontos de extremidade do WCF  <br/> |
|**Fluxos de trabalho** <br/> |Fluxos de trabalho declarativos, criados com o SharePoint Designer 2013<br/>- Usar somente em uma instância específica do Project Web App<br/>- Pode importar um design de fluxo de trabalho do Visio 2013<br/>- Pode importar e usar ações personalizadas<br/><br/> Fluxos de trabalho declarativos, criados com o Visual Studio 2012<br/>- Criar um aplicativo que pode incluir fluxos de trabalho<br/>- Criar um pacote de solução do SharePoint (.wsp) que pode incluir fluxos de trabalho<br/>- Criar modelos de fluxo de trabalho para reutilização<br/>- Criar e usar ações personalizadas  <br/><br/>Pode usar fluxos de trabalho compilados herdados, criados com o WF3.5 (recomendamos a atualização para o fluxo de trabalho declarativo do WF4)  <br/> |Fluxos de trabalho declarativos, criados com o SharePoint Designer 2013<br/>- Usar somente em uma instância específica do Project Web App<br/>- Pode importar um design de fluxo de trabalho do Visio 2013<br/>- Pode importar e usar ações personalizadas  <br/><br/>Fluxos de trabalho declarativos, criados com o Visual Studio 2012<br/>- Criar um aplicativo que pode incluir fluxos de trabalho  <br/>- Criar um pacote de solução do SharePoint (.wsp) que pode incluir fluxos de trabalho<br/>- Criar modelos de fluxo de trabalho para reutilização <br/>- Criar e usar ações personalizadas  <br/> |
|**Distribuição** <br/> |- Office Store (para aplicativos baseados em CSOM)<br/>- Catálogo de aplicativos particulares no SharePoint<br/>- Compartilhamento de arquivos da intranet  <br/> |- Office Store<br/>- Catálogo de aplicativos particulares no SharePoint  <br/> |

   
## <a name="conclusion"></a>Conclusão
<a name="pj15_WhatsNew_Conclusion"> </a>

O Project Server 2013 fornece uma grande quantidade de novos recursos e cenários de desenvolvimento que parceiros e clientes podem usar para adaptar e estender os recursos e a utilidade do Project Server em grandes empresas e em pequenas organizações. Você pode usar a infraestrutura para o Office 2013 e o SharePoint 2013 para ajudar a criar e distribuir aplicativos para o Project 2013 que podem estender muito a comercialização e o uso de aplicativos personalizados. Alguns recursos de extensibilidade e práticas de versões anteriores foram preterido no Project 2013, especialmente os serviços Web ASMX da PSI e os recursos que envolvem a representação ou alterações diretas no banco de dados, que não podem ser usados com o Project Online.
  
A introdução do CSOM permite acesso programático ao Project Online para uma ampla variedade de dispositivos e usando JavaScript em aplicativos Web. O CSOM fornece um modelo de programação mais consistente em comparação com a PSI. Os dados do Project Server podem ser acessados de muitas maneiras além das versões anteriores, incluindo por meio do serviço OData online e por meio de pontos de extremidade REST para relatar dados no banco de dados do Project. Os relatórios existentes ainda funcionam da mesma maneira para uso local; novos relatórios têm mais flexibilidade.
  
Os Complementos do Office fornecem uma nova forma de vender soluções e integrar o Project Standard 2013 com conteúdo da Web e outros produtos do Office 2013. Você também pode criar novas maneiras de integrar o Project Professional 2013 com dados do Project Server e listas do SharePoint por meio de Complementos do Office do painel de tarefas.
  
For more information about developing apps, and using the programmability features and the CSOM of SharePoint Server 2013, see [SharePoint for developers](https://docs.microsoft.com/sharepoint/dev/) and [Office for developers](https://developer.microsoft.com/office/docs).
  
## <a name="see-also"></a>Confira também

- [Arquitetura do Project Server 2013](project-server-2013-architecture.md)  
- [Tarefas de programação do Project](project-programming-tasks.md) 
- [Modelo de objeto do cliente (CSOM) para o Project 2013](client-side-object-model-csom-for-project-2013.md) 
- [ProjectData - referência do serviço OData do Project](https://msdn.microsoft.com/library/office/jj163015.aspx)  
- [Suplementos do painel de tarefas para Project](task-pane-add-ins-for-project.md)   
- [OData: convenções de URI](https://www.odata.org/documentation/uri-conventions#FilterSystemQueryOption)    
- [SharePoint para desenvolvedores](https://msdn.microsoft.com/sharepoint)    
- [Office para desenvolvedores](https://msdn.microsoft.com/office)   
- [Manipulando eventos em aplicativos para SharePoint](https://msdn.microsoft.com/library/jj220048%28office.15%29.aspx)   
- [AppSource](https://appsource.microsoft.com/marketplace/apps?product=office)   
- [Project Online](https://developer.microsoft.com/project)
    

