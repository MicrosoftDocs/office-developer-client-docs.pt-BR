---
title: Arquitetura do Project Server
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2cfa5a6e-2f5c-440c-b35a-bc7a34648f9c
description: Project Server 2013 se integra a funcionalidade de gerenciamento de projeto em todo um farm do SharePoint e habilita o uso do Project Online com um modelo de objeto do cliente (CSOM) e uma interface de OData para os dados de relatórios.
ms.openlocfilehash: 992fae3790b8bdb6ab55f41d42ef0229a75e255c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771187"
---
# <a name="project-server-architecture"></a>Arquitetura do Project Server

Project Server 2013 se integra a funcionalidade de gerenciamento de projeto em todo um farm do SharePoint e habilita o uso do Project Online com um modelo de objeto do cliente (CSOM) e uma interface de OData para os dados de relatórios.
   
Project Server 2013 é um sistema de várias camadas que amplia a arquitetura introduzida no Office Project Server 2007. Mudanças de arquitetura incluem a associação entre o serviço de aplicativo do Project e conjuntos de sites do SharePoint, a adição de alguns objetos corporativos na web front-end (WFE), o modelo de objeto do cliente (CSOM) para acesso remoto, um único banco de dados de projeto, um Interface de OData para relatórios de tabelas e modos de exibição, a integração do Windows Workflow Foundation versão 4 (WF4) por meio do cliente de Gerenciador de fluxo de trabalho 1.0 na nuvem ou em um servidor local e receptores de evento remoto que estão acessíveis por vários Project Server instalações. Além das soluções personalizadas do local, você pode criar aplicativos que incluem os receptores de evento remoto e componentes que acessam as interfaces CSOM e OData.
  
A camada de front-end inclui o Project Professional 2013, Project Web App e os aplicativos de terceiros. Aplicativos cliente se comunicar com a camada intermediária por meio do Project Server Interface (PSI) ou por meio de pontos de extremidade do CSOM, que por sua vez, se comunicam com a PSI e a camada de objetos comerciais. Acesso de banco de dados está integrado nos objetos de negócios. O sistema de eventos do Project Server pode acessar os manipuladores de evento local e receptores de evento remoto. O serviço de cálculo do projeto implementa o mecanismo de agendamento do Project Professional dentro do Project Server. Aplicativos cliente não (ou não deveriam) acessar diretamente o banco de dados do projeto; Project Server oculta os objetos de negócios de clientes.
  
> [!NOTE]
> Project Server é baseado na arquitetura do SharePoint. Para obter informações sobre a arquitetura do SharePoint Server 2013 e o modelo de aplicativo do SharePoint, consulte a seção *guia de Introdução ao desenvolvimento no SharePoint* na documentação do desenvolvedor do Office 2013. 

<a name="pj15_Architecture_SharePoint"> </a>

## <a name="integrating-with-sharepoint-site-collections"></a>Integrando com conjuntos de sites do SharePoint

O serviço de aplicativo do projeto no Project Server 2013 pode ser associado um conjunto de sites do SharePoint para uso com listas de tarefas do SharePoint, o serviço de aplicativo do Project também pode importar uma lista de tarefas do SharePoint como um projeto da empresa para o Project Server completo controle. Com uma lista de tarefas do SharePoint, o SharePoint mantém o site de projeto em um conjunto de sites; Project Professional pode sincronizar com e atualizar a lista de tarefas. Um site de projeto pode ser uma lista de tarefas do SharePoint independente ou uma lista de tarefas que está sincronizada com um arquivo. mpp; o arquivo. mpp pode ser armazenado localmente ou em uma biblioteca do SharePoint. 
  
Project Server mantém os projetos quando ele tem controle total; Project Professional salva os dados diretamente para o Project Server. Tabela 1 compara o comportamento de uma lista de tarefas, a web part de agenda e outras funcionalidades para SharePoint controle das listas de tarefas e projetos importados ao Project Server tem controle total. A web part de agenda contém a grade na página do Project Web App, onde você pode editar uma agenda de projeto. O modo de associado é onde os dados de status são inseridos uma vez para tarefas e quadros de horários; no modo de entrada única, os dados de status de tarefa são inseridos separadamente dos quadros de horários.
  
**Tabela 1. Comparação de listas de tarefas do SharePoint e controle total**

| Recurso | Lista de tarefas | Controle total |
|:-----|:-----|:-----|
|**Lista de tarefas no SharePoint** <br/> |Leitura/gravação  <br/> |Somente leitura  <br/> |
|**Web part de agendamento** <br/> |Somente leitura  <br/> |Leitura/gravação  <br/> |
|**Emissão de relatórios** <br/> |Relatórios valiosos por meio do Project Server  <br/> |Relatórios valiosos por meio do Project Server  <br/> |
|**Outra funcionalidade do Project Server** <br/> | Funcionalidade bloqueada:  <br/>-Edições de projeto server-side, com o Project Web App ou os aplicativos cliente personalizados  <br/>-Status  <br/>-Tarefas não são visíveis no modo associado  <br/> |A funcionalidade completa está habilitada  <br/> |
   
### <a name="managing-projects-as-sharepoint-task-lists"></a>Gerenciando projetos como listas de tarefas do SharePoint
<a name="pj15_Architecture_VisibilityMode"> </a>

Quando o Project Server é associado a um conjunto de sites do SharePoint onde SharePoint mantém o controle, listas de tarefas e o Project Professional 2013 (. mpp) arquivos em bibliotecas de documentos são visíveis para o serviço de aplicativo do Project, mas mantém o SharePoint o mestre de dados de sincronização (consulte a Figura 1). Agendamento no servidor com a web part de agendamento não pode ser feito. Você pode usar o Project Professional para sincronizar com e edite a lista de tarefa em um site de projeto. Iniciando com listas de tarefas do SharePoint, as organizações podem evoluir gradualmente para usar a funcionalidade completa do Project Server.
  
A Figura 1 mostrará os processos a seguir quando projetos forem mantidos em listas de tarefas do SharePoint: 
  
- (A) O Project Professional pode sincronizar com listas de tarefas e criar novos sites do projeto no conjunto de sites antes ou depois da associação ao Serviço do Aplicativo do Project.
    
- (B) O Project Server sincroniza com dados do site do projeto para fins de relatórios, mas o SharePoint mantém os dados mestres; as listas de tarefas permanecem de leitura/gravação.
    
- (C) Após a associação, o Project Professional pode criar novos projetos e salvá-lo ou publicá-lo no Project Server. O Cache Ativo no Project Professional mantém a sincronização de dados com o Project Server.
    
- (D) quando um novo projeto é publicado no Project Professional, o usuário tem a opção de criar um site de projeto para o projeto. Um projeto também pode ser criado no Project Web App como um tipo de projeto de lista de tarefas do SharePoint ou como um tipo de projeto da empresa de controle total (EPT). Etapa (D) mostra o EPT de controle total.
    
**Figura 1. Usando sites do projeto como listas de tarefas do SharePoint**

![Usando sites de projeto no modo de visibilidade] (media/pj15_Architecture_VisibilityMode.gif "Usando sites de projeto no modo de visibilidade")

<br/>

### <a name="managing-projects-with-full-control"></a>Gerenciando projetos com controle total
<a name="pj15_Architecture_ManagedMode"> </a>

Quando o Project Server está associado um conjunto de sites e tem controle total, Project Server importa como projetos da empresa de listas de tarefas do SharePoint e podem excluir quaisquer arquivos. mpp relacionados. Project Server mantém os dados mestres para sincronização de lista de tarefas; listas de tarefas no conjunto de sites se tornam somente leitura (consulte a Figura 2). Projetos importados podem ser editados usando o Project Professional, ou usando o Project Web App.
  
> [!NOTE]
> Depois que o Project Server importar um projeto, o usuário escolherá excluir o projeto do site ou interromper a conexão antes da edição do projeto. Você pode fazer a escolha no Project Professional. 
  
A Figura 2 mostra os processos a seguir quando o Project Server mantém projetos corporativos com controle total:
  
- (A) O usuário pode escolher quais sites do projeto serão importados. O Project Server importa os sites do projeto e, opcionalmente, exclui os arquivos .mpp associados. A lista de tarefas do SharePoint de um projeto importado se torna somente leitura.
    
- (B) após a associação, o Project Professional cria novos projetos e salva ou publica ao Project Server. O Cache ativo no Project Professional mantém a sincronização de dados com o Project Server. A web part de agendamento no Project Web App pode fazer o agendamento no servidor.
    
- (C) quando um novo projeto é publicado no Project Professional, o usuário tem a opção de criar um site de projeto para o projeto. Um projeto também pode ser criado no Project Web App com um EPT de controle total e publicado com uma lista de tarefas de somente leitura para um site de projeto no conjunto de sites.
    
**Figura 2. Usando sites do projeto com controle total**

![Usando sites de projeto no modo gerenciado] (media/pj15_Architecture_ManagedMode.gif "Usando sites de projeto no modo gerenciado")
  
## <a name="general-architecture"></a>Arquitetura geral
<a name="pj15_Architecture_General"> </a>

A Figura 3 mostra um modo de exibição generalizado da arquitetura do Project Server 2013, incluindo o aplicativo de serviço do projeto, uma instância do Project Web App em um WFE e vários outros aplicativos de cliente, incluindo o Project Professional 2013.
  
Pode haver várias instâncias do Project Web App que se comunicam com o aplicativo de serviço do projeto de back-end. Para uma instalação local, o WFE pode ser em um servidor separado em um farm do SharePoint, ou pode ser no mesmo servidor do SharePoint com o aplicativo de serviço do projeto. Project Online inclui um WFE, o aplicativo de serviço do projeto e um servidor local ou remoto do cliente do Gerenciador de fluxo de trabalho 1.0. 
  
**Figura 3. Arquitetura geral do Project Server 2013**

![Arquitetura do Project Server] (media/pj15_Architecture_ProjectServiceApp_WFE.gif "Arquitetura do Project Server")

<br/>

Os comentários gerais a seguir se aplicam à Figura 3:
  
- **Project Online:** Você pode criar aplicativos que usam as interfaces CSOM, REST e OData. Um pacote de aplicativos também poderá instalar receptores de evento remoto em um serviço web personalizado em um servidor local, em um servidor do Windows Azure ou no Microsoft Azure. Project Online não oferece suporte a soluções de terceiros no local, a interface WCF, a interface ASMX ou manipuladores de eventos local. 
    
- **Receptores de evento:** Receptores de evento também podem ser chamados manipuladores de eventos. Project Online suporta o registro de receptores de eventos do Project Server remotos, que pode ser usado por uma instância do Project Web App na nuvem ou por uma instalação do Project Server no local. Uma instalação do Project Server no local suporta receptores de evento remoto e manipuladores de evento de confiança total local. 
    
- **Navegadores:** Não há nenhuma limitação de vários navegadores na exibição de algumas páginas do Project Web App, que hajam no Project Server 2010. Os seguintes navegadores são compatíveis para uso completo ao Project Web App: 
    
  - Internet Explorer 8. x (no Windows 7 e versões anteriores do Microsoft Windows), Internet Explorer 9. x e o Internet Explorer 10. x 
  - Firefox 4.x (no Windows, no Mac OS-X e no Linux/Unix)
  - Safari 5.x (no Windows e no Mac OS-X)
  - Chrome
    
- **Interfaces programáticas:** Para aplicativos de terceiros, Project Online expõe a interface HTTP/HTTPS (incluindo REST), a interface CSOM, um serviço OData para o CSOM e um serviço OData para geração de relatórios. Para aplicativos de cliente de terceiros que estão no local (na Intranet), você pode usar a interface WCF para a PSI ou você pode usar as interfaces CSOM, OData e REST via HTTP. Os clientes do Project Web App e do Project Professional 2013 usam a interface WCF. Em uma instalação de servidor único, o front-end ASMX serviços web CSOM e REST internamente chame os serviços do WCF back-end. 
    
    > [!NOTE]
    > A interface ASMX baseados em SOAP para serviços web na PSI ainda está disponível no Project Server 2013, mas foi preterida. 
  
    O serviço OData para geração de relatórios é implementado pelo serviço WCF OData.svc interno. Você pode obter o documento de metadados do serviço para os dados de relatórios usando `http://ServerName/ProjectServerName/_api/ProjectData/$metadata`. 
    
    O serviço OData para o CSOM destina-se a plataformas como Windows RT, iOS e Android, onde você pode usar a interface REST com JavaScript em páginas HTML. 
    
    > [!NOTE]
    > Embora o `$metadata` opção para **ProjectData** reporting service é válida, o `$metadata` opção para o serviço de **ProjectServer** do CSOM do é removido na versão lançada do Project Server 2013. Para obter mais informações sobre consultas REST para o CSOM, consulte [o modelo de objeto do lado do cliente (CSOM) para o Project Server](client-side-object-model-csom-for-project-2013.md). 
  
- **PSI encaminhador:** Acesso programático para o PSI feitas em um WFE separado passa o encaminhador PSI, que inclui um encaminhador do WCF e um encaminhador de serviço Web. Clientes que usam a interface ASMX acessam a PSI através do encaminhador do serviço Web. Clientes que usam a interface WCF acessam a PSI por meio de encaminhador WCF. Acesso programático através do CSOM, OData e REST é direcionado por meio de encaminhador WCF. 
    
- **Fluxos de trabalho:** Fluxos de trabalho declarativos (fluxos de trabalho que são definidos no SharePoint Designer 2013) são liberados para o cliente do Gerenciador de fluxo de trabalho 1.0 para processamento. Cliente do Gerenciador de fluxo de trabalho 1.0 pode ser executado em um servidor separado no farm do SharePoint, no Microsoft Azure na nuvem ou em um único computador do Project Server para testes ou demonstrações. Fluxos de trabalho codificados que são desenvolvidos com o Visual Studio 2012 são processados no tempo de execução do fluxo de trabalho no SharePoint, como no Project Server 2010. Para obter mais informações, consulte [Introdução ao desenvolvimento de fluxos de trabalho do Project Server](getting-started-developing-project-server-workflows.md).
    
- **a rede de perímetro (DMZ):** Figura 3 não mostrar que um servidor WFE no local pode ser isolado por um firewall adicional em uma rede de perímetro (também conhecido como uma "zona desmilitarizada" ou DMZ). Uma rede de perímetro pode permitir que os clientes da Internet acessar o SharePoint e do Project Server em um firewall. 
    
- **Serviços Web do SharePoint:** Figura 3 não mostra a infraestrutura do SharePoint, como o aplicativo de serviços Web do SharePoint de back-end, que é parte do SharePoint Server 2013. Quando você instala o Project Server, o aplicativo de serviço do projeto é adicionado aos serviços Web do SharePoint. 
    
A camada de front-end inclui aplicativos de terceiros, Project Professional e do Project Web App. Um navegador exibe páginas ASP.NET 4.0 (páginas. aspx) no Project Web App. As páginas do Project Web App usam o Project Server Web Parts que se comunicar com a PSI e também usar Web Parts padrão do SharePoint. 
  
A camada intermediária inclui a PSI e a camada de objeto de negócios, que consiste em objetos lógicos que representam as entidades de negócios do Project Server. Entidades de negócios incluem projeto, recurso, tarefa, atribuição e assim por diante. A PSI e a camada de objeto de negócios estão intimamente ligadas e estão localizados no mesmo servidor. Um aplicativo cliente chama a PSI por meio de uma das interfaces disponíveis e a PSI invoca objetos comerciais. Para melhorar o desempenho do WFE do Project Server 2013 inclui alguns objetos comerciais de solicitações que não usam o sistema de enfileiramento do Project Server ou exigem o serviço de cálculo do projeto. Os objetos de negócios WFE se comunicar diretamente com o banco de dados do projeto.
  
Os componentes do Project Web App do Project Server, usam o banco de dados de configuração do SharePoint 2013 para configuração de site de projeto e o banco de dados de conteúdo para conteúdo de site de projeto, como listas de tarefas, as páginas personalizadas, fluxos de trabalho, as configurações de gerenciamento, documentos e listas de problemas, riscos e comprometimentos. A configuração do SharePoint e recursos adicionais de suporte de bancos de dados de conteúdo para gerenciamento de projetos, modelos de projeto e espaços de trabalho, listas personalizadas para colaboração de equipe e relatórios.
  
### <a name="project-web-app-and-the-wfe"></a>Project Web App e o WFE
<a name="pj15_Architecture_PWAServer"> </a>

Você pode configurar várias instâncias do Project Web App em um WFE e vários servidores WFE dentro de uma intranet corporativa para habilitar a distribuição de carga para clientes de intranet. Quando um aplicativo cliente usa uma instância do Project Web App em um servidor WFE separado, chamadas PSI são roteadas através do encaminhador PSI. O encaminhador PSI (o encaminhador WCF ou o encaminhador de serviço Web) executa as seguintes funções:
  
- Otimiza chamadas à PSI de clientes remotos.
    
- Distingue entre chamadas PSI que exigem o Serviço de Fila do Project Server e aquelas que não. Os nomes de método de PSI assíncrona começam com Queue, como **QueueCreateProject**.
    
- Identifica chamadas à PSI que invocam manipuladores de evento locais.
    
- Identifica chamadas à PSI que exigem o Serviço de Cálculo do Project.
    
- Usa um cache baseado em servidor que funciona com o Cache Ativo no lado cliente no Project Professional para reduzir chamadas de viagens de ida e volta para o Project Server.
    
Depois que o SharePoint Server autentica um usuário do Project Server, o encaminhador PSI transparente envia solicitações que usam o serviços de back-end para os serviços PSI no computador executando o Project Server. Solicitações que não exigem serviços back-end são enviadas para os objetos de negócios na instância do Project Web App local. O encaminhador PSI melhora a escalabilidade, desempenho e confiabilidade para o Project Server processamento através da LAN, uma WAN e no Project Online.
  
Project Web App foi desenvolvido com ASP.NET 4.0. Os elementos visuais nos arquivos. aspx (HTML, controles de servidor e texto estático) são separados da lógica de programação em classes code-behind que estão em assemblies compilados (arquivos. dll). Páginas de site no Project Web App, como a página de nível superior, Central de projetos e Central de relatórios podem ser personalizadas usando Web Parts. Páginas de aplicativo que não tenham uma opção de **Editar página** no menu **Ações** do Site não podem ser editadas, como a página Configurações do servidor e a página de quadro de horários de revisão. 
  
### <a name="the-csom-and-the-project-server-interface"></a>O CSOM e a Interface do Project Server
<a name="pj15_Architecture_PSI"> </a>

A PSI é acrescentada em 22 de serviços públicos, como o **projeto**, **recurso**, **CustomField**e **status**. A PSI também contém sete serviços privados para uso interno. A PSI é fundamental API do Project Server; ele expõe a funcionalidade do Project Server para o CSOM e aplicativos externos. O CSOM inclui classes que acessam as classes PSI e os membros que são usados para aplicativos de terceiros a mais comumente usadas. No Project Server 2013, algumas funcionalidades do Project Server não estão disponível no CSOM, como os serviços de **Administração**, **calendário**, **PortfolioAnalyses**e **segurança** . 
  
Project Professional 2013 e o uso do Project Web App a PSI para acessar dados do Project Server no rascunho, publicado e arquivar tabelas e modos de exibição do banco de dados do projeto. Você pode acessar um serviço PSI por meio de um arquivo de proxy ou um assembly de proxy, para os serviços WCF ou serviços da web ASMX.
  
> [!NOTE]
> O CSOM é a interface preferida para desenvolvedores do Project Server de terceiros; ele pode ser usado para aplicativos que acessam a uma instalação do local do Project Server e Project Online. Recomendamos que você use o CSOM para o desenvolvimento de novos aplicativos, se o CSOM inclui a funcionalidade que requer o seu aplicativo. 
  
Alguns aplicativos de linha de negócios (LOB) e outros aplicativos de terceiros que foram desenvolvidos para o Project Server 2010 exigem serviços PSI que ainda não são representados no CSOM. Se eles alvo apenas uma instalação local do Project Server, aplicativos podem continuar a usar a interface WCF ou a interface ASMX de PSI.
  
Os aplicativos de cliente chamar a PSI por meio de proxies de serviço. Os clientes que usam a interface WCF acessar todos os serviços PSI por meio de `http://ServerName/ProjectServerName/_vti_bin/psi/ProjectServer.svc`. Clientes que usam uma interface de serviço web ASMX usam a URL do Project Web App para o serviço específico. Por exemplo, o serviço de **recursos** está em `http://ServerName/ProjectServerName/_vti_bin/psi/resource.asmx?wsdl`. Se aplicativos não têm acesso à intranet para o Project Server, eles podem usar um servidor do Project Web App em uma rede de perímetro (não é mostrada na Figura 3).
  
Figura 4 mostra o painel de **conexões** no **Gerenciador de serviços de informações da Internet (IIS)** para uma instalação de servidor único do SharePoint Server 2013, Project Server 2013 e um site de gerenciamento de fluxo de trabalho local para o cliente do Gerenciador de fluxo de trabalho 1.0. O conjunto de sites do SharePoint (A) inclui os serviços PSI front-end no `_vti_bin\PSI` subdiretório virtual. O aplicativo de serviços Web do SharePoint (B) inclui o aplicativo de serviço do Project, com os serviços PSI back-end do `508c23fb7dfd4c83a8919fae24bc68c5/PSI` subdiretório virtual. O GUID é o nome da instância do aplicativo de serviço do projeto para essa instalação do Project Server. 
  
**Figura 4. Gerenciador do IIS mostrando a PSI de front-end (A) e a PSI de back-end (B)**

![A PSI front-end e back-end PSI] (media/pj15_Architecture_PSI_IIS.gif "A PSI front-end e back-end PSI")
  
Aplicativos cliente não podem acessar diretamente os serviços WCF para a PSI no aplicativo de serviço de projeto de back-end. Se eles não exigem acesso ao Project Online, os aplicativos cliente e componentes de aplicativos LOB usam proxies para a PSI. Uma URL de back-end para a interface WCF do **recurso** serviço na Figura 4, por exemplo, seria `http://ServerName:32843/508c23fb7dfd4c83a8919fae24bc68c5/psi/resource.svc`. Porta 32843 é a porta HTTP padrão para o aplicativo de serviços Web do SharePoint (32844 é a porta de comunicações HTTPS). No entanto, o arquivo Web. config para blocos do Project Web App acesso direto aos serviços PSI back-end.
  
> [!NOTE]
> O download do SDK do Project 2013 inclui arquivos de PSI de proxy para os serviços do WCF e os serviços ASMX e obter instruções sobre como compilá-los em assemblies de proxy. > Para criar arquivos atualizados do proxy PSI que usam a interface WCF, você precisará usar o utilitário de svcutil.exe ou o Visual Studio diretamente no computador do Project Server. 
  
Normalmente, os membros dos serviços PSI produzem ou consumam tipos de objetos de **conjunto de dados** como os meios para trocar informações com os objetos de negócios. Há também vários modelos para desenvolvimento de PSI. Por exemplo, os serviços PSI **LookupTable** , **CustomFields**e **recursos**usam objetos de filtro XML para manipulação do **conjunto de dados** , e outros serviços não; alguns métodos no serviço de **status** usam um parâmetro _changeXml_ , enquanto outros métodos e os serviços não. O CSOM não usa conjuntos de dados. Embora o CSOM tem um modelo de programação diferente que a PSI, e você pode usar os assemblies .NET ou JavaScript, desenvolvimento com o CSOM é geralmente mais simples e mais consistente do que o desenvolvimento com a PSI. 
  
Para obter mais informações sobre a PSI, consulte [Visão geral da referência do Project PSI](project-psi-reference-overview.md). Para obter mais informações sobre o CSOM, consulte [o modelo de objeto do lado do cliente (CSOM) para o Project 2013](client-side-object-model-csom-for-project-2013.md).
  
### <a name="business-objects-in-the-wfe-and-the-project-service-application"></a>Objetos de negócios no WFE e o Aplicativo do Serviço do Project
<a name="pj15_Architecture_BusinessObjects"> </a>

O modelo de objeto interno do Project Server inclui os objetos de negócios, que representam entidades lógicas, como Projeto e Recurso. Os aplicativos cliente só acessam objetos de negócios por meio do CSOM ou da PSI. Os objetos de negócios, por sua vez, acessam as tabelas e as exibições de rascunho, de publicação e de arquivo morto do banco de dados do Project.
  
Os objetos de negócios não são expostos a desenvolvedores terceirizados. A PSI manipula o mapeamento da API para objetos de negócios, e o CSOM mapeia sua API para o PSI. As entidades lógicas dos objetos de negócios podem ser classificadas em três tipos:
  
- **Entidades fundamentais** são objetos como projetos, tarefas, atribuições, recursos e calendários. As entidades fundamentais incluem lógica comercial básica, como permissões e nomenclatura. 
    
- **Entidades comerciais** são objetos como quadros de horários, portfólios de projeto e modelos. As entidades comerciais incluem lógica comercial adicional e normalmente são criadas de uma combinação das entidades fundamentais. 
    
- **Entidades de suporte** são objetos como segurança e validação. 
    
No Project Server 2010, todos os objetos de negócios são implementados no aplicativo de serviço do projeto. No Project Server 2013, o WFE hospeda muitos dos objetos corporativos que processam métodos síncronos e não exigem o serviço de cálculo do projeto. Métodos PSI síncronos como **DeleteProject** e **ReadAssignments** não use o serviço de fila do Project Server. Os métodos assíncronos na PSI têm nomes que começam com `Queue`, como **QueueCreateProject** e **QueueUpdateTimesheet**. Um método assíncrono envia uma mensagem para o serviço de fila do Project Server, que agenda o processamento do método enquanto o controle é retornado para o usuário.
  
O Encaminhador PSI determina quais solicitações são encaminhadas para o Aplicativo do Serviço do Project e quais podem ser processadas pelos objetos de negócios no WFE. Os objetos de negócios no WFE ignoram o Aplicativo do Serviço do Project e têm acesso direto ao banco de dados do Project, semelhante à maneira que outros processos do SharePoint em um WFE acessam diretamente os bancos de dados de Configuração e de Conteúdo. A execução de vários dos objetos de negócios no WFE aumenta a eficiência do Project Server, reduz a carga na camada do aplicativo e permite que o Project Server seja melhor dimensionado para cargas de trabalho maiores.
  
> [!NOTE]
> No Project Server 2013, manipuladores de evento local devem ser implantados para o WFE e o computador do Project Server de back-end. 
  
### <a name="project-server-database"></a>Banco de dados do Project Server
<a name="pj15_Architecture_DAL"> </a>

No Project Server 2013, os quatro bancos de dados do Project Server de versões anteriores são combinados em um banco de dados de projeto no SQL Server. O nome do banco de dados de projeto padrão é ProjectService. As tabelas e modos de exibição de relatórios continuarão com seus nomes anteriores com o `dbo` prefixo, como dbo. MSP_EpmProject e dbo. MSP_EpmProject_UserView. Tabelas e modos de exibição que estavam anteriormente no banco de dados de rascunho têm o `draft` prefixo. Tabelas e modos de exibição do banco de dados publicado têm o `pub` prefixo. Tabelas e modos de exibição do banco de dados de arquivo morto tem o `ver` prefixo. 
  
> [!IMPORTANT]
> Direcionar o access não é suportado para o rascunho ( `draft` prefixo), publicados ( `pub` prefixo) e o arquivo morto ( `ver` prefixo) tabelas e exibições. Relatórios devem usar somente as tabelas e modos de exibição, que possuem relatórios a `dbo` prefixo. 
  
Os dados do Project Server são particionados no banco de dados do Project desta forma:
  
- As tabelas de rascunho e visualizações contêm dados de projetos que foram criados pelo Project Professional e outros aplicativos não publicados. Não exibe dados de projetos de rascunho tabelas e modos de exibição do Project Web App.
    
- As exibições e tabelas publicadas contenham todos os projetos publicados e recursos da empresa, dados globais para tipos de projeto corporativo (EPTs) e outros modelos de projeto. Projetos publicados são visíveis no Project Web App. Os dados publicados também incluem tabelas que são específicas para o Project Web App (quadros de horários, modelos, modos de exibição e assim por diante) e tabelas de dados globais (campos personalizados, tabelas de pesquisa, permissões de autorização do Project Server e metadados).
    
- Os dados de arquivo morto salvam versões de backup de projetos, de recursos, de campos personalizados e de outros dados.
    
- Os dados de relatórios podem ser usados para acesso somente leitura em aplicativos de terceiros e para relatórios. Cubos do Project Server OLAP usam os modos de exibição de relatórios que têm o `_OlapView` sufixo. Cubos OLAP estão disponíveis em uma instalação do Project Server no local, mas não estão disponíveis no Project Online. 
    
    Os dados de relatórios são abrangentes e são atualizados quase em tempo real. As tabelas e exibições de relatórios são otimizadas para geração de relatório somente leitura; por exemplo, as tabelas de relatórios são desordenados para oferecerem dados redundantes e reduzirem o número de tabelas relacionais.
    
As entidades lógicas, como Recurso ou Projeto, podem se estender por várias tabelas, e todas as tabelas para uma entidade em particular têm a mesma chave primária. A chave primária é o GUID em uma única coluna que identifica exclusivamente uma instância de uma entidade em particular.
  
Dados do Project Server para cada instância do Project Web App são armazenados em um banco de dados separado do projeto com um nome diferente. Aplicativos cliente que têm acesso direto ao Project Server diretamente podem ler as tabelas e modos de exibição de relatórios. Para acesso remoto, os aplicativos cliente podem usar a interface de OData e a interface REST para obter dados para relatórios. Os clientes devem usar somente o CSOM ou a PSI para acessar o rascunho, publicado e arquivar tabelas e exibições. O serviço de dados de relatório (RDS, que não é mostrado na Figura 3) atualiza os dados de relatórios de dados publicados em praticamente em tempo real. O banco de dados de projeto pode estar localizado em um servidor separado.
  
Esquemas são documentadas apenas para as tabelas e modos de exibição de relatórios. Para uma instalação do Project Server no local, você pode adicionar o relatório de tabelas e modos de exibição para entidades que não são definidos no esquema de banco de dados do Project. Você também pode criar bancos de dados separados para aplicativos personalizados no local. Modificação não é suportada para o rascunho, publicado e arquiva tabelas e exibições. Como o banco de dados do projeto não está acessível diretamente no Project Online, relatórios de tabelas e modos de exibição não podem ser modificado. No entanto, se você tiver uma conta do SQL Azure, você pode criar bancos de dados separados para uso personalizado ao Project Online.
  
### <a name="event-receivers"></a>Receptores de eventos
<a name="pj15_Architecture_EventHandlers"> </a>

Manipuladores de evento local e receptores de evento remoto para o Project Server permitem extensibilidade de terceiros em resposta a eventos do Project Server, como criar ou publicação de um projeto. No Project Server 2010, todos os manipuladores de eventos são locais em são gravados no código de confiança total, implantado diretamente no computador que executa o Project Server e para os WFEs e executados dentro do sistema de eventos do Project Server. Porque o Project Online não é possível usar manipuladores de eventos de confiança total, o Project Server 2013 implementa receptores de evento remoto que são semelhantes aos receptores de evento remoto no SharePoint Server 2013. Uma instalação local do Project Server 2013 pode usar os manipuladores de evento tradicionais de confiança total e receptores de evento remoto.
  
Um receptor de evento remoto do Project Server pode ser implementado em um serviço web personalizado com um ponto de extremidade SOAP que executa o Microsoft Azure ou em outros ambientes que oferecem suporte a serviços web SOAP. Um pacote de aplicativos do Project Server pode incluir os receptores de evento remoto que são instalados com o aplicativo.
  
Receptores de evento remoto podem ligar novamente para o Project Server usando os pontos de extremidade do CSOM (não é mostrados na Figura 3). A chamada para um receptor de evento remoto inclui informações do sistema de eventos do Project Server e a instância do Project Web App (ou Locatário do Project Web App no Project Online) que emite a chamada. Receptores de evento remoto permitem que você crie e hospede um serviço web único que pode ser usado por várias instalações do Project Server. Por outro lado, os manipuladores de evento de confiança total local devem ser implantados em cada instalação do Project Server.
  
### <a name="publishing-and-server-side-scheduling"></a>Publicação e agendamento no lado do servidor
<a name="pj15_Architecture_PublishingScheduling"> </a>

Project Server 2013 suporta ambas as atualizações de agenda de projeto manuais e automatizadas. O processo de padrão é uma atualização de agendamento manual. Ou seja, o gerente de projeto faz check-out e abre um projeto no Project Professional ou no Project Web App, aplica as alterações e, em seguida, salva e publica o projeto para disponibilizar as alterações para todos. Project Professional tem um mecanismo de agendamento que calcula as alterações e, em seguida, salva as alterações no Project Server. No Project Server 2010, o mecanismo de agendamento do lado do servidor é uma implementação diferente do mecanismo de agendamento no Project Professional.
  
No Project Server 2013, o serviço de cálculo do projeto implementa o mesmo mecanismo de agendamento que esteja no Project Professional 2013. O serviço de cálculo do projeto é executado em um serviço do Windows chamado de **Serviço de cálculo do Microsoft Project Server**. Editando uma agenda de projeto no Project Web App ou com aplicativos de terceiros que usam os resultados CSOM em exatamente as mesmas alterações de agendamento que tornaria Project Professional.
  
> [!NOTE]
> Aplicativos de terceiros que usam a PSI podem mostrar algumas diferenças de agendamento de uma agenda que calcula do Project Web App. Para compatibilidade, os métodos PSI públicos que faça ainda de agendamento do lado servidor usam o mecanismo de agendamento que foi introduzido no Project Server 2010. Uma exceção é **QueueUpdateProject2**, que é um novo método de PSI no Project Server 2013. Por exemplo, o mecanismo de agendamento mais antigo não agendar subprojetos ou links para outros projetos e não calcula campos de valor acumulado. Para evitar possíveis de agendamento diferenças entre os aplicativos de terceiros e Project Professional ou no Project Web App, você deve desenvolver aplicativos com o CSOM onde for possível. 
  
O Project Server permite que a versão publicada de um projeto seja atualizada enquanto um gerente de projeto estiver usando a versão de rascunho, por meio destas etapas:
  
1. O Project Server aplica atualizações e reagenda a versão publicada.
    
2. O Project Server salva a atualização para aplicar à versão de rascunho quando um destes eventos ocorrer:
    
   - O Project Professional abre o projeto.
    
   - O Project Professional tenta publicar o projeto.
    
3. Se houver um conflito, o gerente do projeto será notificado e deverá resolver o conflito antes da publicação da versão de rascunho.
    
## <a name="see-also"></a>Confira também

- [Visão geral do Project 2013 para desenvolvedores](http://msdn.microsoft.com/library/8da91ab0-af4f-429f-8241-490600e3f7bd%28Office.15%29.aspx)
- [Programabilidade do Project Server](project-server-programmability.md)  
- [Modelo de objeto do cliente (CSOM) para o Project 2013](client-side-object-model-csom-for-project-2013.md)  
- [O que o PSI faz e não faz](what-the-psi-does-and-does-not-do.md)  
- [Introdução ao desenvolvimento de fluxos de trabalho do Project](getting-started-developing-project-server-workflows.md)   
- [Visão geral da referência PSI do Project](project-psi-reference-overview.md)   
- [Protocolo do Open Data](http://www.odata.org/)
    

