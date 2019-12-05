---
title: Atualizações para desenvolvedores no Project
manager: lindalu
ms.date: 12/03/2019
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5b2b22cd-6e28-43a8-9092-b411da8bfb53
description: Os novos recursos incluem um modelo de objeto do lado do cliente (CSOM), interfaces REST, um serviço OData para relatórios, receptores de eventos remotos, fluxos de trabalho declarativos e suplementos de painel de tarefas para clientes do Project.
ms.openlocfilehash: c2bc0b475639a8582422b2091169116428367c60
ms.sourcegitcommit: 37080eb0087261320e24e6f067e5f434a812b2d2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/04/2019
ms.locfileid: "39819277"
---
# <a name="updates-for-developers-in-project"></a>Atualizações para desenvolvedores no Project

Recursos de extensibilidade no Project Server 2013 trabalham com suplementos para o Project online e com instalações locais. Os novos recursos incluem um modelo de objeto do lado do cliente (CSOM), interfaces REST, um serviço OData para relatórios, receptores de eventos remotos, fluxos de trabalho declarativos e suplementos de painel de tarefas para clientes do Project. Saiba também sobre os recursos preteridos que não devem ser usados para o novo desenvolvimento.
  
O Project Server 2013 Builds no Framework introduzido com o Microsoft Office Project Server 2007 e estendido pelo Project Server 2010. O Project Server 2013 adiciona um modelo de objeto do lado do cliente (CSOM) que é refatorado e simplificado da interface do Project Server (PSI) e inclui uma biblioteca JavaScript e bibliotecas do .NET Framework 4 para aplicativos do Windows, Windows Phone 8 e Microsoft Silverlight. O CSOM foi projetado para desenvolvimento para o Project online e também funciona com uma instalação local do Project Server. 

Os bancos de dados do Project Server são combinados em um único banco de dados; Você pode acessar as tabelas e exibições de relatórios online por meio de um serviço OData. O CSOM e o serviço OData incluem uma interface REST (Representational State Transfer). Os fluxos de trabalho do Project Server podem ser criados usando o SharePoint Designer 2013. O Project Professional 2013 pode integrar os dados de relatórios do Project Server, as listas de tarefas do SharePoint e outros conteúdos externos usando o modelo de extensibilidade de suplementos do Office para os painéis de tarefas. O Project Standard 2013 pode usar suplementos de painel de tarefas para integração com conteúdo externo geral.
  
Para obter diagramas e mais informações sobre as principais alterações no Project Server 2013, consulte [Project server 2013 Architecture](project-server-2013-architecture.md).
  
> [!NOTE]
> O Project Server 2013 foi criado na plataforma SharePoint Server 2013 e o Project 2013 inclui grande parte da mesma infraestrutura que os outros aplicativos do Office 2013. Para obter a documentação do modelo para suplementos do SharePoint, fluxos de trabalho baseados no SharePoint, Web Parts, desenvolvimento com outros recursos do SharePoint e documentação de suplementos do Office, confira [suplementos do SharePoint](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins), [suplementos do Office](https://docs.microsoft.com/office/dev/add-ins/overview/office-add-ins)e [visão geral do desenvolvimento do SharePoint 2013](https://msdn.microsoft.com/library/jj164084%28office.15%29.aspx). 
  
## <a name="major-new-features-in-project-2013"></a>Principais recursos novos no Project 2013
<a name="pj15_WhatsNew_MajorNewFeatures"> </a>

Os novos recursos do Project Standard 2013 e do Project Professional 2013 incluem uma interface de usuário aprimorada que corresponde a outros aplicativos do Office 2013 e dá suporte à interface de usuário de estilo moderno no Windows 8, integração com objetos de arte do Office para relatórios, burndown relatórios e novos recursos de programação para relatórios. O Project Professional 2013 permite o compartilhamento mais abrangente e a sincronização de projetos no SharePoint Server 2013, juntamente com os suplementos do painel de tarefas que também são implementados em outros aplicativos do Office 2013, como Word, Excel e Outlook.
  
Há muitos recursos novos no Project Server 2013. Alguns não têm uma história de programação principal, como a nova linha do tempo no Project Web App. Esses recursos serão documentados na ajuda do produto e na documentação do usuário final no Microsoft Office Online e nos tópicos direcionados a administradores e profissionais de ti no Microsoft TechNet. Outros novos recursos, como quadros de horários aprimorados, facilitam a interação dos desenvolvedores de terceiros com quadros de horários e status por meio da interface do Project Server (PSI).
  
A adição do Project online e da Office Store (https://office.microsoft.com/store) para suplementos do Project são alterações muito distantes, onde o Project Server pode ser acessado por meio do Microsoft Azure. O acesso baseado em nuvem ao Project Server usa um modelo de objeto do lado do cliente (CSOM) para o desenvolvimento de suplementos com o Microsoft .NET Framework, o Microsoft Silverlight, o Windows Phone e aplicativos Web que usam JavaScript. Um requisito do Project online é que os quatro bancos de dados do Project Server de versões anteriores são mesclados em um banco de dados.
  
O desempenho e a escalabilidade do Project Server 2013 são aprimorados em várias áreas, como status da tarefa, quadros de horários e gerenciamento de projetos. Os fluxos de trabalho do Project Server são reprojetados com a versão 4 do Windows Workflow Foundation (WF4). O uso do .NET Framework 4 e do Windows Communication Foundation (WCF) com o PSI melhora a segurança, o desempenho e a escalabilidade. Por exemplo, você pode alterar o protocolo de transporte de aplicativos baseados no WCF usando arquivos de configuração, sem alterar o código do aplicativo ou recompilar. O Project Web App armazena em cache muitas das chamadas PSI em que os dados não são alterados de forma significativa.
  
> [!NOTE]
> Para desenvolvimento com o Project Server 2013, você pode usar o Visual Studio com as extensões de ferramentas do Office e do SharePoint, que podem criar suplementos de forma nativa para os produtos do Office 2013. O Project Server 2013 requer que o Visual Studio habilite totalmente o desenvolvimento de recursos, como páginas de detalhes do projeto e aplicativos baseados em WCF. As extensões de ferramentas do SharePoint no Visual Studio podem implantar Web Parts e outros recursos do SharePoint diretamente no Project Web App e outros sites do SharePoint. 
>
> O Visual Studio não é mais necessário para desenvolver fluxos de trabalho do Project Server que usam campos personalizados, estágios, fases e tipos de projeto corporativos que podem ser gerenciados no Project Web App. Embora você possa usar o Visual Studio para desenvolver fluxos de trabalho, eles são geralmente mais fáceis e rápidos de criar usando o SharePoint Designer. O Visual Studio pode ser usado para fluxos de trabalho que exigem acesso ao CSOM ou outras APIs externas. 
  
### <a name="project-add-ins"></a>Suplementos do Project
<a name="pj15_WhatsNew_Apps"> </a>

A distribuição e o marketing do software foram revolucionados com o conceito de um suplemento. Para o Project 2013, os suplementos podem ser disponibilizados para compra e download na Office Store pública ou distribuídos dentro de um catálogo privado no SharePoint. Um suplemento normalmente é um programa interativo e autônomo que executa um pequeno número de tarefas relacionadas. Um suplemento do Project pode ser um suplemento do painel de tarefas para os clientes do Project Standard 2013 ou do Project Standard 2013, ou um suplemento para o Project Server 2013 ou o Project online.
  
Para obter informações sobre os suplementos para os clientes de desktop do Project, consulte [suplementos do painel de tarefas no Project](#pj15_WhatsNew_Agave). Para um exemplo do Project Server 2013, confira [criar um suplemento do Project Server hospedado no SharePoint](create-a-sharepoint-hosted-project-server-add-in.md). Além dos artigos do SDK de [suplementos do Office e do SharePoint](https://msdn.microsoft.com/library/fp161507.aspx), o [blog do Office](https://blogs.office.com/dev/) tem várias postagens que também são relevantes para o Project 2013 e o Project online. 
  
Um suplemento para o Project Server 2013 pode funcionar com uma instalação local e com o Project online. Os suplementos do Project Server podem incluir Web Parts, receptores de eventos remotos e lógica de negócios. O acesso ao modelo de objeto do Project Server em um suplemento é através do CSOM, e não do PSI. O armazenamento de dados pode ser baseado em nuvem, como o SQL Azure, externo, como por meio do Microsoft Business Connectivity Services (BCS), interno com um banco de dados local ou misto.
  
#### <a name="add-in-security"></a>Segurança de suplementos

Em geral, as ações que um suplemento utiliza são realizadas em nome do usuário que executa o suplemento; Não use explicitamente a representação ou especifique quem pode executar o suplemento. As ações não podem exceder o nível de permissão do usuário que executa o suplemento. 
  
No Office Developer Tools para Visual Studio 2012, o arquivo AppManifext. XML tem um editor gráfico onde você pode definir o escopo da solicitação de permissão. Por exemplo, para criar um suplemento que permite aos gerentes de projeto atualizar seus projetos, na guia **permissões** do painel **arquivo AppManifest. xml** designer, selecione **vários projetos** para o escopo e **escreva** para a permissão. Se o usuário do suplemento tiver permissões do gerente de projeto, poderá executar o suplemento para projetos que ele gerencia. O código no arquivo arquivo AppManifest. xml incluiria o seguinte: 
  
```XML
  <AppPermissionRequests>
    <AppPermissionRequest Scope="https://sharepoint/projectserver/projects" Right="Write" />
  </AppPermissionRequests>
```

**Tabela 1. Escopos de solicitação de permissão para suplementos do Project Server**

|Escopo|Permissões|
|:-----|:-----|
|**Project Server** <br/> |**Gerenciar** (exige permissões de administrador do Project Server.)  <br/> |
|**Vários projetos** <br/> |**Read**, **Write** (requer permissões do gerente de projeto para algumas operações; permissões de membros da equipe do projeto para operações básicas de leitura, como atribuições de tarefas.)  <br/> |
|**Único projeto** <br/> |**Read**, **Write** (requer pelo menos permissões de membro da equipe do projeto; o acesso a alguns dados em um projeto depende de outros níveis de permissão).  <br/> |
|**Recursos da empresa** <br/> |**Read**, **Write** (requer permissões do Gerenciador de recursos.)  <br/> |
|**Statusing** <br/> |**SubmitStatus** (requer permissão para enviar o status de seus projetos.)  <br/> |
|**Relatórios** <br/> |**Read** (requer permissão para fazer logon no Project Server).  <br/> |
|**Fluxo de Trabalho** <br/> |**Elevate** (requer permissão para executar fluxos de trabalho. O suplemento é executado com permissões elevadas, para permitir transições de estágio para estágio em um fluxo de trabalho. A lógica de negócios no suplemento controla as transições de estágio.)  <br/> |
   
> [!NOTE]
> O Project Server 2013 e o Project online não usam o modelo de autenticação somente aplicativo no SharePoint 2013 (Confira [tipos de política de autorização de suplemento no sharepoint 2013](https://msdn.microsoft.com/library/124879c7-a746-4c10-96a7-da76ad5327f0%28Office.15%29.aspx)). 
  
Para obter informações sobre o desenvolvimento, distribuição, hospedagem e gerenciamento de suplementos, confira suplementos [do SharePoint](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins) e [suplementos do Office](https://docs.microsoft.com/office/dev/add-ins/overview/office-add-ins)e tópicos relacionados na documentação do desenvolvedor do SharePoint Server 2013 e do Office 2013. Para obter informações sobre o escopo de solicitação de permissão para outros suplementos do SharePoint, consulte [permissões de suplemento no SharePoint 2013](https://msdn.microsoft.com/library/5f7a8440-3c09-4cf8-83ec-c236bfa2d6c4%28Office.15%29.aspx).
  
### <a name="integrating-with-sharepoint-server"></a>Integração com o SharePoint Server
<a name="pj15_WhatsNew_IntegrationWSS"> </a>

Muitos recursos do Project Web App requerem a nova infraestrutura no SharePoint Server 2013, como a autenticação OAuth e baseada em declarações, autorização e permissões do Project Server por meio de grupos do SharePoint, sincronização de projetos com a tarefa do SharePoint listas e fluxos de trabalho declarativos do Project Server. O aplicativo de serviço do Project pode ser associado a qualquer conjunto de sites em um farm do SharePoint. A sincronização do projeto pode ser com uma lista de tarefas do SharePoint, onde o SharePoint mantém o projeto. Um projeto corporativo também pode ser sincronizado com uma lista de tarefas do SharePoint, onde o Project Server mantém controle total. Para diagramas arquitetônicos e uma explicação sobre a sincronização de projetos, consulte [Project Server 2013 Architecture](project-server-2013-architecture.md).
  
Há muitos recursos novos no SharePoint Server 2013. Para obter mais informações, consulte [SharePoint for Developers](https://msdn.microsoft.com/sharepoint).
  
### <a name="integrating-with-workflows"></a>Integração com fluxos de trabalho
<a name="pj15_WhatsNew_Workflow"> </a>

Fluxos de trabalho são um recurso principal do gerenciamento de portfólio de projetos. Um ciclo de vida do projeto pode incluir processos de longa duração que abrangem muitas fases. As fases de governança incluem propostas de projeto, análises de impacto nos negócios e seleção, criação, planejamento, gerenciamento e acompanhamento de projetos.
  
Os fluxos de trabalho do Project Server 2013 são criados na plataforma de fluxo de trabalho do SharePoint 2013, que usa WF4. Diferentemente das versões anteriores, é possível criar fluxos de trabalho declarativos para o Project Server 2013 usando o SharePoint Designer 2013 e acessíveis para uso local e online. Os fluxos de trabalho do Project Server usam o modelo de segurança de fluxo de trabalho do SharePoint com OAuth e podem ser instalados em um site do Project Web App. A Figura 1 mostra que o SharePoint Designer 2013 pode adicionar estágios a um fluxo de trabalho de site para gerenciamento de demanda, onde os estágios são definidos no Project Web App.
  
**Figura 1. Usando o SharePoint Designer para adicionar um estágio a um fluxo de trabalho para o Project Web App**

![Adicionar um estágio a um fluxo de trabalho no SPD](media/pj15_CreateWorkflowSPD_AddStageInSPD.gif "Adicionar um estágio a um fluxo de trabalho no SPD")

<br/>

Você cria um fluxo de trabalho declarativo adicionando estágios de fluxo de trabalho, ações, condições e outros elementos em uma ferramenta de design, que pode ser o SharePoint Designer 2013 ou o Visual Studio 2012. A ferramenta de design salva o fluxo de trabalho como código XAML, que é interpretado no tempo de execução. Os fluxos de trabalho declarativos podem ser executados no Project Server 2013 no local ou no Project online. Usando o Visual Studio 2012, você também pode criar ações e formulários personalizados para controle adicional e salvar modelos de fluxo de trabalho para reutilização com várias instâncias do Project Web App. O SharePoint Designer 2013 pode consumir ações personalizadas criadas no Visual Studio 2012.
  
Um fluxo de trabalho do Project Server 2013 atua como um aplicativo, onde um administrador, que tem permissões de design para o Project Web App, pode publicar um fluxo de trabalho declarativo e associá-lo a um tipo de projeto da empresa (EPT). O EPT deve ser para um projeto corporativo, onde o Project Server mantém controle total. Uma lista de tarefas do SharePoint não pode usar um fluxo de trabalho do Project Server. 
  
O OAuth permite que os gerentes de projeto com permissões de criação de projeto invoquem o fluxo de trabalho sem usar representação. Chamadas de fluxo de trabalho para o Project Server, por exemplo, para ler um valor de campo personalizado para decidir qual ramificação seguir, são feitas em nome do gerente de projeto. Para impedir que o gerente de projeto crie um fluxo de trabalho que avança automaticamente para o próximo estágio, a chamada para mover para o próximo estágio de fluxo de trabalho é executada como o autor do fluxo de trabalho (o administrador). Por outro lado, os usuários de fluxos de trabalho herdados do Project Server 2010 fazem chamadas representadas por meio da conta de usuário proxy de fluxo de trabalho para obter acesso de administrador em todo o fluxo de trabalho.
  
Embora o Project Server 2013 local possa usar fluxos de trabalho compilados baseados no WF 3.5, recomendamos que você atualize os fluxos de trabalho herdados para fluxos de trabalho declarativos com base no WF4. A tecnologia mais recente é mais escalonável e robusta. Analistas de negócios e equipe de PMO podem criar ou atualizar designs de fluxo de trabalho usando o Visio 2013 e implementar fluxos de trabalho do Project Server sem codificação usando o SharePoint Designer 2013.
  
Para obter informações sobre como criar um fluxo de trabalho declarativo para o Project Web App, confira [introdução ao desenvolvimento de fluxos de trabalho do Project Server](getting-started-developing-project-server-workflows.md). Para obter uma comparação entre os recursos do SharePoint Designer e do Visual Studio para fluxos de trabalho, consulte [desenvolvimento de fluxos de trabalho do sharepoint 2013 usando o Visual Studio](https://msdn.microsoft.com/library/office/jj163199.aspx).
  
### <a name="client-side-object-model"></a>Modelo de objeto do lado do cliente
<a name="pj15_WhatsNew_CSOM"> </a>

O acesso programático ao Project online requer um CSOM criado no CSOM do SharePoint. A autenticação do Project online será com o OAuth usando um Windows Live ID, não a autenticação de formulários do Project Server ou a autenticação do Windows.
  
Veja a seguir os princípios e recursos do CSOM no Project Server 2013:
  
- O CSOM foi projetado para facilitar o uso. Por exemplo, métodos e propriedades diretamente usam ou fornecem dados por nome, em vez de exigir muitos GUIDs, parâmetros _changeXml_ ou transmitir em torno de conjuntos de dados. 
    
- O Project Server CSOM implementa um subconjunto da funcionalidade PSI, com base nos requisitos mais comuns para soluções de terceiros.
    
- O CSOM chama internamente a PSI, mas é fatorado de forma diferente. Por exemplo, as atualizações para todas as alterações de status são feitas por meio do método **StatusAssignmentCollection. SubmitAllStatusUpdates** , não pelo método psi **Statusing. SubmitStatus** para o usuário ou o método **SubmitStatusForResource** para outros recursos. 
    
- O CSOM pode ser acessado por meio de um serviço WCF (Client. svc), e não por meio dos 22 serviços públicos da PSI.
    
- A inicialização do Project Server CSOM é diretamente através da classe [ProjectContext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx) com a URL do Project Web App, não usando uma referência do WCF ou um assembly de proxy. 
    
- O CSOM implementa várias bibliotecas de clientes e interfaces, que são compatíveis com a infraestrutura interna do CSOM do SharePoint. As bibliotecas e as interfaces do cliente incluem o seguinte:
    
  - Biblioteca de cliente do Microsoft .NET no assembly Microsoft. ProjectServer. Client. dll
    
  - Biblioteca do Silverlight no assembly Microsoft. ProjectServer. Client. Silverlight. dll
    
  - Biblioteca do Windows Phone 8 no assembly Microsoft. ProjectServer. Client. Phone. dll
    
  - Biblioteca JavaScript para aplicativos Web no arquivo PS. js ou PS. Debug. js
    
  - Pontos de extremidade REST, para acesso com o protocolo OData
    
  - Suporte nativo para consultas LINQ com filtragem, para limitar a quantidade de dados retornados
    
- O CSOM pode ser usado para soluções do Project online e para soluções locais, independentemente do PSI e de outros assemblies do Project Server, como Microsoft. Office. Project. Server. library. dll.
    
- Funcionalidades adicionais do Project Server 2013 CSOM podem ser consideradas para atualizações cumulativas e service packs, com base nas solicitações por parceiros do Project Server e na Comunidade de desenvolvedores.
    
> [!NOTE]
> O CSOM é a interface preferencial para desenvolvedores do Project Server de terceiros. Recomendamos que você use o CSOM para o desenvolvimento de novos aplicativos, caso o CSOM inclua a funcionalidade exigida por seu aplicativo. 
  
Para obter informações sobre o desenvolvimento com o CSOM, consulte o [modelo de objeto do cliente (CSOM) para o Project 2013](client-side-object-model-csom-for-project-2013.md). Para obter informações sobre a interface REST em aplicativos do SharePoint, consulte *Programming using the SharePoint REST Service* na documentação do desenvolvedor do SharePoint 2013. 
  
### <a name="changes-in-the-reporting-database"></a>Alterações no banco de dados de relatórios
<a name="pj15_WhatsNew_RDBChanges"> </a>

Os quatro bancos de dados no Project Server 2010 são combinados em um único banco de dados de projeto no Project Server 2013. O nome padrão do banco de dados de projeto é ProjectService. As tabelas e exibições de relatórios mantêm seus nomes anteriores, e as tabelas e exibições dos bancos de dados rascunho, publicado e arquivo morto `draft`têm `pub`os prefixos, e `ver` no banco de dados ProjectService. Por exemplo, a tabela projetos publicados é pub. MSP_PROJECTS. 
  
> [!IMPORTANT]
> O acesso direto não é suportado para as tabelas`draft` e exibições de rascunho`pub`(prefixo), publicado`ver`() e arquivo (). Os relatórios devem usar apenas as tabelas e exibições de relatórios, `dbo` que têm o prefixo. Por exemplo, o dbo. MSP_EpmProject tabela inclui a lista de projetos na instância do Project Web App. 
>
> Não há nada que impeça você de usar o acesso direto ao banco de dados programático para atualizar os dados em qualquer uma das tabelas e modos de exibição no banco de dados do Project. Você deve estar ciente de que o cache do Project Professional, as tabelas para dados de rascunho e publicados e as tabelas de relatórios contam com um protocolo de sincronização de cache que pode ser interrompido pela edição direta de dados. Se você danificar os bancos de dados do Project Server ou os caches do lado do cliente corrompidos do Project Professional usando o acesso direto a alterações de dados, seja avisado de que o suporte ao produto não poderá ajudar! 
  
O Project Server 2013 introduz um serviço OData para acesso local e online. As tabelas e exibições de relatórios online são expostas apenas pela interface OData; para uso local, você pode usar a interface OData ou acessar diretamente as tabelas e exibições de relatórios no banco de dados do ProjectService no farm do SharePoint. O Project online não oferece suporte a um banco de dados multilocatário. Ou seja, várias instâncias do Project Web App têm seu próprio banco de dados de projeto. O serviço OData executa internamente consultas SQL nas tabelas e exibições de relatórios e fornece uma carga XML ou JSON. Para obter uma introdução ao serviço OData para relatórios no Project Server 2013 e para a referência de esquema **ProjectData** , consulte [ProjectData-Project OData Service Reference](https://msdn.microsoft.com/library/office/jj163015.aspx).
  
Para obter informações gerais sobre consultas OData, consulte [OData: convenções URI](https://www.odata.org/documentation/). Por exemplo, você pode ver todos os projetos em uma instância local do Project Web App, onde o nome do projeto começa com "Test" usando a seguinte consulta em um navegador. Clique com o botão direito do mouse na página do navegador e clique em **Exibir fonte**.
  
```html
https://ServerName /ProjectServerName /_api/ProjectData/Projects?$filter=startswith(ProjectName, 'Test') eq true
```

Para importar dados do projeto para o PowerPivot no Excel 2013, na faixa de opções de dados, selecione **do feed de dados OData** no menu suspenso **de outras fontes** . Na caixa de diálogo **Assistente de conexão** de dados https://ServerName/ProjectServerName/_api/ProjectData/ , digite o local do feed de dados, escolha **Avançar**e, em seguida, selecione a tabela **projetos** na página **selecionar tabelas** do assistente. Nomeie e salve o arquivo. odc e, em seguida, escolha **concluir**. Na caixa de diálogo **importar dados** , escolha **relatório de tabela dinâmica**. Na planilha do Excel, escolha campos para as linhas e colunas da tabela dinâmica que você deseja exibir.
  
Os usuários do Project Server no local, que têm as permissões corretas, podem acessar diretamente as tabelas e exibições de relatórios por meio do Microsoft SQL Server para criar relatórios, como no Project Server 2010. No Project Server 2013, os usuários também podem acessar as tabelas de relatórios no local por meio da interface OData. Você pode recuperar dados do Project Server online ou no local por meio de pontos de extremidade REST para o serviço OData. Por exemplo, a tabela dbo.MSP_PROJECT e a exibição dbo.MSP_EpmProject_UserView pode ser usada para relatórios. Qualquer tabela ou modo de exibição que `draft`possua um `ver` , ou prefixo, `pub`é para uso interno apenas pelo Project Server e não é para o uso de relatórios. Por exemplo, o rascunho. MSP_TASKS tabela e o pub. MSP_PROJECTS_WORKING_VIEW modo de exibição não estão documentados e são apenas para uso interno. 
  
> [!NOTE]
> Você pode estender relatórios no local adicionando tabelas, exibições, campos e procedimentos armazenados em um banco de dados separado. Você não deve modificar as tabelas e exibições de relatórios existentes no banco de dados do Project Server. 
  
As tabelas, os modos de exibição e os campos de relatório no banco de dados do projeto serão documentados em um arquivo de ajuda HTML em uma atualização posterior do download do SDK do Project 2013. Para obter a documentação do esquema XML OData para o serviço **ProjectData** , consulte [ProjectData-Project OData Service Reference](https://msdn.microsoft.com/library/office/jj163015.aspx). As consultas das tabelas e exibições de relatórios que foram criadas para o Project Server 2010 serão, na maioria dos casos, trabalhar com o banco de dados de projeto no Project Server 2013. Os usuários locais podem acessar os cubos OLAP do Project Server no SQL Server Analysis Services, como fazem no momento. No Project Online, os cubos OLAP não estão disponíveis.
  
### <a name="task-pane-add-ins-in-project"></a>Suplementos do painel de tarefas no Project
<a name="pj15_WhatsNew_Agave"> </a>

Os suplementos do painel de tarefas do Project Standard 2013 e do Project Professional 2013 dão suporte, que podem ser usados para integração e exibição de conteúdo externo em uma página da Web. O painel de tarefas mostra o conteúdo da página da Web que tem acesso por meio de JavaScript a tarefas, recursos, modos de exibição e dados gerais do projeto. O modelo de objeto do JavaScript para o Project pode obter informações sobre uma tarefa ou recurso selecionado e pode obter dados em uma célula selecionada na grade para modos de exibição como o gráfico de Gantt. Os suplementos do painel de tarefas do Project também podem implementar manipuladores de eventos para eventos de seleção de tarefa, recurso ou modo de exibição. 
  
A Figura 2 mostra o suplemento do painel de tarefas **Hello ProjectData** que consulta o serviço **ProjectData** e, em seguida, compara dados no projeto atual com as médias de todos os projetos. O download do SDK do Project 2013 inclui o código-fonte completo do suplemento. 
  
**Figura 2. Um suplemento de painel de tarefas no Project Professional pode acessar dados no Project Server**

![Comparing the current project with all projects](media/pj15_RestQueryApp_CompareProject.gif "Comparing the current project with all projects")
  
> [!NOTE]
> O Project Standard 2013 não pode integrar diretamente com o Project Server 2013 por meio de suplementos do painel de tarefas. 
  
Os suplementos do painel de tarefas no Project Professional podem oferecer suporte a Web Parts criadas para o Project Server 2013, de modo que os desenvolvedores possam criar uma extensão uma vez que seja executada com o Project Web App e o Project Professional. Os suplementos gerais do painel de tarefas que são desenvolvidos para outros produtos do Office 2013 também podem ser usados com o Project Standard 2013 e o Project Professional 2013. Para saber mais, confira [suplementos do painel de tarefas para o Project](task-pane-add-ins-for-project.md).
  
### <a name="project-server-event-receivers"></a>Receptores de eventos do Project Server
<a name="pj15_WhatsNew_Events"> </a>

Pode haver vários servidores do Project Web App (também chamados de servidores Web front-end ou WFEs) em um farm do SharePoint que inclui o aplicativo de serviço back-end do Project. Os receptores de evento também podem ser chamados de manipuladores de eventos. Manipuladores de eventos locais podem ser implementados com código de confiança total e implantados em todos os WFEs para uma instalação local do Project Server. Receptores de eventos remotos podem ser implementados em serviços Web em servidores locais ou remotos e acessados por várias instalações do Project Server e do WFEs. O Project online pode usar somente receptores de eventos remotos.
  
Os manipuladores de eventos do Project Server são gerenciados pelo SharePoint para cada instância do Project Web App, e não por uma página específica de configurações do Project Web App. No aplicativo da administração central do SharePoint, escolha **configurações gerais de aplicativos**, escolha **gerenciar** em **configurações do PWA**e, em seguida, escolha a instância na lista suspensa **instância do Project Web App** na página Configurações do PWA. Para adicionar um manipulador de eventos local ou um receptor de eventos remoto, escolha os **manipuladores de eventos no servidor**.
  
Para uma instalação local do Project Server, você pode criar um receptor de eventos remotos como um recurso do SharePoint que usa a classe [Microsoft. ProjectServer. Client. EventHandlerCreationInformation](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.EventHandlerCreationInformation.aspx) no CSOM e, em seguida, gerenciar programaticamente o receptor de evento usando métodos na classe [eventhandlercollection](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.EventHandlerCollection.aspx) . Para receptores de eventos remotos, pré-eventos são síncronos, os eventos post são assíncronos e há um tempo limite para casos em que o receptor de eventos remotos não retorna. 
  
> [!NOTE]
> A administração central do SharePoint está disponível somente para instalações locais. Para o Project online e o SharePoint Online, você pode adicionar ou remover receptores de eventos remotos usando um pacote de aplicativo baseado em CSOM. 
  
Na página manipuladores de eventos no servidor, o processo para adicionar um manipulador de eventos local para uma instalação local do Project Server é praticamente igual ao processo descrito no tópico [criar um manipulador de eventos do Project Server e registrar um evento](https://msdn.microsoft.com/library/gg615466.aspx) para o Project Server 2010. A diferença é que a página novo manipulador de eventos tem opções adicionais. Por exemplo, escolha **projeto criando** na lista **eventos** e, em seguida, escolha **novo manipulador de eventos**. Na página novo manipulador de eventos, os únicos dois campos obrigatórios são **Name** e **Order** (veja a Figura 3). Se você estiver adicionando um manipulador de eventos de confiança total local, adicione o campo **nome do assembly** e o campo **nome da classe** ; sair da **URL de ponto de extremidade** vazia. Se você estiver adicionando um receptor de evento remoto, adicione a **URL do ponto de extremidade**e deixe o nome do **assembly** e o **nome da classe** vazios. 
  
> [!CAUTION]
> Se você especificar o nome do assembly/ *nome da classe* e a URL do ponto de extremidade, o Project Server chamará apenas o manipulador de eventos local (local). O receptor de eventos remotos é ignorado. 
> 
> Se você criar dois manipuladores de eventos para o mesmo evento, onde um manipulador de eventos é local e um é um receptor de eventos remotos e o valor da **ordem** é o mesmo para ambos, o Project Server ignora o receptor de evento remoto. 
  
**Figura 3. Adicionar um manipulador de eventos local ou um receptor de eventos remoto**

![Configuring an event handler or event receiver](media/pj15_EventHandlers_NewEventHandler.gif "Configuring an event handler or event receiver")
    
Se você precisar acessar os conjuntos de databases PSI para um manipulador de eventos local, poderá copiar o assembly Microsoft. Office. Project. Schema. dll do diretório [\_Windows] \Microsoft.NET\assembly\GAC msil\microsoft.Office.Project.schema\v4.0_15.0.0.0__71e9bce111e9429c. 

Em vez da PSI, recomendamos que você use as classes de evento no namespace **Microsoft. ProjectServer. Client** ; o desenvolvimento com o CSOM não requer a manipulação de DataSets. Para desenvolver receptores de eventos remotos para o Project online, você deve usar a classe [Event](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.Event.aspx) e a classe [EventHandlerCreationInformation](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.EventHandlerCreationInformation.aspx) no CSOM. 
  
Antes de implantar um manipulador de eventos do Project Server, instale e teste o manipulador de eventos completamente em uma instalação de teste do Project Server. Para uma instalação do Project Server no local, se o manipulador de eventos local que você adicionar se tornar inoperante, o serviço de eventos do Project Server 2013 falhará ao carregar os outros manipuladores de eventos personalizados válidos. Nesse caso, você deve remover o manipulador de eventos com problema e reiniciar o serviço de eventos.
  
> [!NOTE]
> Para uma instalação local do Project Server, recomendamos que você migre para receptores de eventos remotos usando o CSOM para desenvolver receptores de eventos. Como os receptores de eventos remotos não têm código de terceiros sendo executado dentro do serviço de eventos do Project Server, os receptores de eventos remotos são mais estáveis. Os administradores locais são aliviados da responsabilidade de manter o serviço de eventos do Project Server. 
  
Para obter informações gerais sobre eventos, consulte [tratamento de eventos em aplicativos para SharePoint](https://msdn.microsoft.com/library/jj220048%28office.15%29.aspx). 
  
## <a name="deprecated-features"></a>Recursos preteridos
<a name="pj15_WhatsNew_Deprecated"> </a>

> [!NOTE]
> Para obter informações sobre os recursos e APIs que foram preteridos ou removidos no Project Server 2016 Preview, confira [o que foi preterido ou removido no Project server 2016 Preview](https://docs.microsoft.com/project/what-s-deprecated-or-removed-in-project-server-2016). 
  
Os recursos preteridos ainda estão disponíveis no Project 2013 para algumas soluções, mas não devem ser usados para o novo desenvolvimento. A maioria dos seguintes recursos e práticas não funcionam com o Project online ou com a instalação local padrão do Project Server 2013 no modo de permissão do SharePoint. As soluções existentes que usam esses recursos podem não funcionar para uma atualização do Project Server 2010 para o Project Server 2013. Embora as soluções que usam recursos preteridos possam continuar a funcionar em alguns casos, elas não são totalmente suportadas para todas as instalações do Project 2013.
  
Se suas soluções usarem recursos preteridos, eles deverão ser testados exaustivamente antes da implantação e você deverá modificá-los para usar os recursos suportados assim que for prático. Para obter informações sobre como configurar a segurança do Project Server 2013 local para o modo de permissão do Project, consulte a seção *modo de permissão do SharePoint* em What ' [s New for it prós in Project Server 2013](https://docs.microsoft.com/project/what-s-new-for-it-pros-in-project-server-2016).
  
- Os [cenários de extensão psi](https://docs.microsoft.com/previous-versions/office/developer/office-2010/ff843378(v=office.14)) de **extensões** são preteridos e não terão suporte em versões futuras. Estes cenários do Project Server 2013 no local estão habilitados para integração usando serviços personalizados do Windows Communication Foundation (WCF). 
  
- **Projeto psi** A [classe de projeto](https://docs.microsoft.com/office/client-developer/project/project-psi-reference-overview) do Psi foi preterida. Para todos os novos desenvolvimentos, use o [projeto CSOM](client-side-object-model-csom-for-project-2013.md). Os aplicativos do Project Server 2013 que usam o projeto PSI continuarão funcionando, mas os aplicativos do Project online precisarão substituir qualquer método PSI de classe de projeto com seus métodos CSOM equivalentes.
  
- **PSI do plano de recursos** O [plano de recursos psi](https://docs.microsoft.com/previous-versions/office/project-class/gg240019(v=office.15)) é preterido. Ele continuará a ter suporte para o desenvolvimento do Project 2013, mas não terá suporte em versões futuras. 
  
- **Interface asmx para o Psi** O PSI inclui interfaces duplicadas para o desenvolvimento de extensões do Project Server no local. A interface de serviços Web ASMX foi introduzida com a primeira implementação do PSI no Office Project Server 2007. O Project Server 2010 adicionou a interface de serviços do WCF, onde o modelo de objeto basicamente duplica os serviços Web ASMX. Embora o Project Server 2013 continue a oferecer suporte a ASMX e WCF, as novas soluções que exigem o PSI devem usar os serviços do WCF. Se possível, novas soluções devem ser gravadas usando o CSOM. 
  
  Os serviços Web ASMX do PSI são preteridos no Project Server 2013. Para trabalhar em versões futuras do Project Server, as soluções que usam os serviços Web ASMX devem ser reconfiguradas para usar os serviços do WCF ou o CSOM. Para obter mais informações, consulte a seção *Atualizando aplicativos com as APIs do Project Server* na [programação do Project Server](project-server-programmability.md).
  
- **Provedor de link de objeto (OLP)** Nas versões anteriores do Project Server, o serviço **Objectlinkprovider** na psi (consulte [WebSvcObjectLinkProvider](https://docs.microsoft.com/previous-versions/office/ms481347(v=office.14)) oferece uma maneira de gerenciar links de objeto da Web entre as tarefas do projeto da empresa e listas especializadas do SharePoint no site do projeto para problemas, riscos, resultados finais e documentos. No Project Server 2013, o OLP foi preterido. 
  
  Você pode usar a classe **[RelatedItemManager](https://docs.microsoft.com/previous-versions/office/sharepoint-server/jj168020(v=office.15))** no CSOM do SharePoint para criar, ler e excluir links de objeto da Web entre itens na lista tarefas e outras listas em um site de projeto. Por exemplo, para adicionar um link de um item de tarefa a um problema, você pode usar o método **[AddSingleLink](https://docs.microsoft.com/previous-versions/office/sharepoint-server/jj166451(v=office.15))** ou qualquer um dos dois métodos similares, **AddSingleLinkFromUrl** ou **AddSingleLinkToUrl**. A classe **RelatedItemManager** também inclui métodos para excluir um link de objeto da Web e ler itens relacionados. Para a classe equivalente no JSOM (o modelo de objeto do JavaScript), consulte [SP. Objeto RelatedItemManager (SP. js)](https://docs.microsoft.com/previous-versions/office/sharepoint-visio/jj838582(v=office.15)).
  
  Recomendamos que você use o CSOM do SharePoint para criar aplicativos do tipo OLP para uma instalação local do Project Server 2013 e do Project online. O namespace [Microsoft. SharePoint](https://docs.microsoft.com/previous-versions/office/sharepoint-server/ms464984(v=office.15)) não inclui uma classe **RelatedItemManager** * * * *. 
  
- **Permissões personalizadas** As permissões de segurança personalizadas para acessar os recursos ou extensões específicos do Project Server têm suporte no Office Project Server 2007, onde um artigo do SDK explicou como criá-los modificando diretamente o banco de dados publicado. No Project Server 2010, as permissões personalizadas ainda funcionam, mas são preteridas. No Project Server 2013, as permissões personalizadas não funcionam com o modo de permissão padrão do SharePoint para instalações locais. Para o modo de permissão do Project, as permissões personalizadas são suportadas. Com o Project online, o acesso direto ao banco de dados não é possível. 
  
- **Representação** Representação em aplicativos baseados em PSI, onde o usuário de um aplicativo pode assumir as permissões de segurança de um usuário diferente do Project Server, é preterido no Project Server 2013. Como indicado anteriormente, uma instalação local padrão do Project Server 2013 usa o modo de permissão do SharePoint, que não permite a representação nos grupos de segurança do Project Server. Para obter mais informações, consulte [autenticação, autorização e segurança no SharePoint 2013](https://docs.microsoft.com/sharepoint/dev/general-development/authentication-authorization-and-security-in-sharepoint).
  
  Status os aplicativos são extensões típicas que podem ter usado a representação em versões anteriores do Project Server. O Project Server 2010 introduziu o método **ReadStatusForResource** e o método **SubmitStatusForResource** no PSI, juntamente com a permissão global **StatusBrokerPermission** , que eliminou a necessidade de representação para ler e atualizar o status em nome de outro usuário. O CSOM no Project Server 2013 usa o PSI subjacente para habilitar de forma transparente as extensões de status e pode ser usado para o Project online ou para instalações locais. 
  
- **Extensões de banco de dados de relatórios** Adicionar tabelas e exibições personalizadas para o banco de dados de relatórios é uma prática comum com versões anteriores do Project Server. Como o Project Server 2013 combina os quatro bancos de dados de versões anteriores em um banco de dados, as atualizações não transferem tabelas personalizadas, modos de exibição ou SPROCs para as tabelas de relatório no banco de dados do Project Server 2013. 
  
  É recomendável usar o SQL Azure ou um banco de dados separado do SQL Server para exibir tabelas e exibições de relatórios personalizados, onde você pode gerenciar backups e atualizações de banco de dados. Para o Project online, isso é necessário.
  
- **Relatórios** As tabelas e exibições de relatórios locais no banco de dados do Project Server e os cubos OLAP *não* são preteridas e permanecem totalmente suportadas. No entanto, as tabelas e exibições de relatórios (o banco de dados de relatórios nas versões anteriores do Project Server) não estão acessíveis no Project online. Da mesma forma, os cubos OLAP estão disponíveis somente em instalações locais do Project Server 2013. Para reportar aplicativos com o Project online, você pode usar o serviço **ProjectData** , através de consultas REST com o protocolo OData. 
  
- **Guia do projeto** O guia do projeto é um recurso padrão nos aplicativos de área de trabalho do Office Project 2007, onde o conteúdo HTML e JavaScript em um painel de tarefas fornece orientações interativas para a criação e o gerenciamento de projetos. No Project 2010, o guia do projeto não está disponível em uma instalação padrão, mas pode ser habilitado por meio do VBA ou de um suplemento VSTO. O download do SDK do Project 2010 inclui os arquivos modificados do guia do projeto. 
  
  O modelo de objeto do VBA e o modelo de objeto **Microsoft. Office. Interop. MSProject** no Project 2013 ainda incluem os 22 membros da classe **Application** e a classe de **projeto** que pode gerenciar o guia do projeto. No entanto, os aplicativos do painel de tarefas do Project 2013 podem entrar em conflito com ações em um painel de projeto e o conteúdo do guia do projeto não pode ser facilmente distribuído ou vendido na Office Store. Recomendamos enfaticamente que você desenvolva soluções do painel de tarefas do Project com suplementos do Office, não como conteúdo do guia do projeto personalizado. Para obter mais informações sobre o guia do projeto, consulte a [documentação do SDK do project 2010](https://msdn.microsoft.com/library/ms512767.aspx).
  
## <a name="comparing-project-server-on-premises-with-project-online"></a>Comparando o Project Server no local com o Project online
<a name="pj15_WhatsNew_Comparing"> </a>

Para ajudá-lo a decidir se deseja usar o Project Server local ou o Project online e quais tipos de extensões você pode desenvolver em ambos os casos, a tabela 2 compara os recursos extensíveis de uma instalação local do Project Server 2013 com o Project online. A tabela 2 não inclui diferenças na implantação, administração ou uso. Para obter mais informações sobre o Project online e o Project Server 2013, confira o [project 2013 para desenvolvedores](https://developer.microsoft.com/project/docs) e o [Project online](https://developer.microsoft.com/project).
  
**Tabela 2. Extensibilidade do Project Server local e do Project online**

| Recurso |Project Server local | Project Online |
|:-----|:-----|:-----|
|**Programação** <br/> |Aplicativos baseados em CSOM; modelo de programação consistente  <br/>– Bibliotecas de clientes .NET, Silverlight e Windows Phone  <br/>– Biblioteca JavaScript para páginas personalizadas, Web Parts e extensões de faixa de opções  <br/>-Protocolos OData e REST<br/><br/> Aplicativos baseados em PSI; modelo de programação complexo, também pode criar aplicativos para administração, análise de portfólio, notificações, segurança de modo de projeto, sistema de fila e outras áreas<br/><br/>Extensões PSI  <br/><br/>Permissões personalizadas com segurança de modo de projeto (preterido)  <br/><br/>Representação com o PSI (preterido)  <br/><br/>Código de confiança total; instalar extensões no farm do SharePoint  <br/> |Aplicativos baseados em CSOM; modelo de programação consistente  <br/>– Bibliotecas de clientes .NET, Silverlight e Windows Phone<br/>– Biblioteca JavaScript para páginas personalizadas, Web Parts e extensões de faixa de opções<br/>-Protocolos OData e REST<br/><br/>Pode usar o PSI, mas não tem suporte: nenhuma conexão OAuth e sem serviço para serviço<br/><br/>Nenhuma extensão da API CSOM<br/><br/>Nenhuma permissão personalizada<br/><br/>Sem representação<br/><br/>Nenhum código de confiança total  <br/> |
|**Bancos de dados personalizados** <br/> |– SQL Azure  <br/>– Não há suporte para o SQL Server (modificação de tabelas e exibições de relatórios no banco de dados do Project Server)  <br/> |– SQL Azure  <br/>– Não há suporte para o SQL Server (modificação de tabelas e exibições de relatórios no banco de dados do Project Server)  <br/> |
|**Relatórios** <br/> |- Serviço **ProjectData** ; Protocolos OData e REST  <br/>– Tabelas e exibições de relatórios no banco de dados do Project Server<br/>-Banco de dados OLAP  <br/> |- Serviço **ProjectData** ; Protocolos OData e REST  <br/> |
|**Manipuladores de eventos** <br/> |– Receptores de eventos remotos, acessíveis por meio de pontos de extremidade do WCF<br/>– Manipuladores de eventos de confiança total, instalados no farm do SharePoint  <br/> | – Receptores de eventos remotos, acessíveis por meio de pontos de extremidade do WCF  <br/> |
|**Fluxos de trabalho** <br/> |Fluxos de trabalho declarativos criados com o SharePoint Designer 2013<br/>– Use somente em uma instância específica do Project Web App<br/>– Pode importar um design de fluxo de trabalho do Visio 2013<br/>-Pode importar e usar ações personalizadas<br/><br/> Fluxos de trabalho declarativos criados com o Visual Studio 2012<br/>– Criar um aplicativo que pode incluir fluxos de trabalho<br/>-Criar um pacote de solução do SharePoint (. wsp) que pode incluir fluxos de trabalho<br/>– Criar modelos de fluxo de trabalho para reutilização<br/>– Criar e usar ações personalizadas  <br/><br/>Pode usar fluxos de trabalho compilados herdados, criados com o WF 3.5 (recomendar atualização para o fluxo de trabalho declarativo WF4)  <br/> |Fluxos de trabalho declarativos criados com o SharePoint Designer 2013<br/>– Use somente em uma instância específica do Project Web App<br/>– Pode importar um design de fluxo de trabalho do Visio 2013<br/>-Pode importar e usar ações personalizadas  <br/><br/>Fluxos de trabalho declarativos criados com o Visual Studio 2012<br/>– Criar um aplicativo que pode incluir fluxos de trabalho  <br/>-Criar um pacote de solução do SharePoint (. wsp) que pode incluir fluxos de trabalho<br/>– Criar modelos de fluxo de trabalho para reutilização <br/>– Criar e usar ações personalizadas  <br/> |
|**Distribuição** <br/> |– Office Store (para aplicativos baseados em CSOM)<br/>– Catálogo de aplicativos privado no SharePoint<br/>-Compartilhamento de arquivos da intranet  <br/> |-Office Store<br/>– Catálogo de aplicativos privado no SharePoint  <br/> |

   
## <a name="conclusion"></a>Conclusão
<a name="pj15_WhatsNew_Conclusion"> </a>

O Project Server 2013 fornece uma infinidade de novos cenários e recursos de desenvolvimento que os parceiros e clientes podem usar para adaptar e estender os recursos e a utilidade do Project Server em grandes empresas e em pequenas organizações. Você pode usar a infraestrutura para o Office 2013 e o SharePoint 2013 para ajudar a criar e distribuir aplicativos para o Project 2013, que podem estender imensamente o uso de aplicativos personalizados. Alguns recursos de extensibilidade e práticas de versões anteriores são preteridos no Project 2013, particularmente os serviços Web ASMX da PSI e dos recursos que envolvem representação ou alterações diretas do banco de dados, que não podem ser usados com o Project online.
  
A introdução do CSOM permite o acesso programático ao Project online para uma ampla variedade de dispositivos e usando JavaScript em aplicativos Web. O CSOM fornece um modelo de programação mais consistente em comparação com o PSI. Os dados do Project Server podem ser acessados de várias outras maneiras do que nas versões anteriores, incluindo através do serviço OData online e por pontos de extremidade REST para relatórios de dados no banco de dados do projeto. Os relatórios existentes ainda funcionam da mesma forma para uso local; novos relatórios têm mais flexibilidade.
  
Os suplementos do Office oferecem uma nova avenida para a venda de soluções e a integração do Project Standard 2013 com conteúdo da Web e outros produtos do Office 2013. Você também pode criar novas maneiras de integrar o Project Professional 2013 com dados do Project Server e listas do SharePoint por meio de suplementos do Office no painel de tarefas.
  
Para obter mais informações sobre como desenvolver aplicativos e usar os recursos de programação e o CSOM do SharePoint Server 2013, consulte [SharePoint for Developers](https://docs.microsoft.com/sharepoint/dev/) and [Office for Developers](https://developer.microsoft.com/office/docs).
  
## <a name="see-also"></a>Confira também

- [Arquitetura do Project Server 2013](project-server-2013-architecture.md)  
- [Tarefas de programação do Project](project-programming-tasks.md) 
- [Modelo de objeto do cliente (CSOM) para o Project 2013](client-side-object-model-csom-for-project-2013.md) 
- [ProjectData - referência do serviço OData do Project](https://msdn.microsoft.com/library/office/jj163015.aspx)  
- [Suplementos do painel de tarefas para Project](task-pane-add-ins-for-project.md)   
- [OData: convenções de URI](https://www.odata.org/documentation/uri-conventions#FilterSystemQueryOption)    
- [SharePoint para desenvolvedores](https://msdn.microsoft.com/sharepoint)    
- [Office para desenvolvedores](https://msdn.microsoft.com/office)   
- [Tratamento de eventos em aplicativos para SharePoint](https://msdn.microsoft.com/library/jj220048%28office.15%29.aspx)   
- [AppSource](https://appsource.microsoft.com/marketplace/apps?product=office)   
- [Project Online](https://developer.microsoft.com/project)
    

