---
title: Arquitetura do Project Server
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 2cfa5a6e-2f5c-440c-b35a-bc7a34648f9c
description: O Project Server 2013 integra funcionalidade de gerenciamento de projetos em um farm do SharePoint e habilita o uso do Project Online com um modelo de objeto do lado cliente (CSOM) e uma interface OData para os dados de Relatórios.
localization_priority: Priority
ms.openlocfilehash: db4dd0eed9c043021f586041fa0e28708fdbd243
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301583"
---
# <a name="project-server-architecture"></a>Arquitetura do Project Server

O Project Server 2013 integra funcionalidade de gerenciamento de projetos em um farm do SharePoint e habilita o uso do Project Online com um modelo de objeto do lado cliente (CSOM) e uma interface OData para os dados de Relatórios.
   
O Project Server 2013 é um sistema multicamadas que estende a arquitetura introduzida no Office Project Server 2007. As alterações de arquitetura incluem a associação do Serviço do Aplicativo do Project com conjuntos de sites do SharePoint, a adição de alguns objetos comerciais ao front-end da Web (WFE), o modelo do objeto do lado cliente (CSOM) para acesso remoto, um único banco de dados do Project, uma interface OData para as tabelas e exibições de Relatórios, integração do Windows Workflow Foundation versão 4 (WF4) por meio do Workflow Manager Client 1.0 na nuvem ou em um servidor local e receptores de eventos remotos acessíveis por várias instalações do Project Server. Além de soluções personalizadas locais, você pode criar aplicativos que incluam receptores de eventos remotos e componentes que acessem as interfaces do CSOM e OData.
  
A camada de front-end inclui o Project Professional 2013, o Project Web App e aplicativos de terceiros. Os aplicativos clientes podem se comunicar com a camada do meio através da Project Server Interface (PSI) ou através dos pontos de extremidade do CSOM que, por sua vez, se comunicam com o PSI e a camada do objeto de negócios. O acesso ao banco de dados é integrado nos objetos de negócios. O Project Server Eventing System pode acessar os manipuladores de eventos locais e os receptores de eventos remotos. O Serviço de Cálculo do Project implementa o mecanismo de agendamento do Project Professional no Project Server. Os aplicativos clientes não têm (ou não devem ter) acesso direto ao banco de dados do Project. O Project Server oculta objetos de negócios dos clientes.
  
> [!NOTE]
> O Project Server é criado na arquitetura do SharePoint. Para saber mais sobre a arquitetura do SharePoint Server 2013 e o modelo do aplicativo do SharePoint, confira a seção *Introdução ao desenvolvimento do SharePoint* na documentação do desenvolvedor do Office 2013. 

<a name="pj15_Architecture_SharePoint"> </a>

## <a name="integrating-with-sharepoint-site-collections"></a>Integrando com conjuntos de sites do SharePoint

O Serviço do Aplicativo do Project no Project Server 2013 pode ser associado a um conjunto de sites do SharePoint para ser usado com listas de tarefas do SharePoint. O Serviço do Aplicativo do Project também pode importar uma lista de tarefas do SharePoint como um projeto corporativo para controle total do Project Server. Através de uma lista de tarefas do SharePoint, o SharePoint mantém o site do projeto em um conjunto de sites. O Project Professional pode sincronizar e atualizar a lista de tarefas. Um site de projeto pode ser uma lista de tarefas do SharePoint independente sincronizada com um arquivo .mpp. Esse arquivo pode ser armazenado localmente ou em uma biblioteca do SharePoint. 
  
O Project Server mantém os projetos quando tem controle total. O Project Professional salva dados diretamente no Project Server. A Tabela 1 compara o comportamento de uma lista de tarefas, o Schedule Web Part e outras funcionalidades para o controle de listas de tarefas do SharePoint e para projetos importados quando o Project Server tem controle total. O Schedule Web Part contém a grade na página do Project Web App onde é possível editar uma programação de projeto. O modo associado é onde os dados de status são inseridos uma vez para as tarefas e quadros de horários. No modo de entrada única, os dados de status das tarefas são inseridos separadamente dos quadros de horários.
  
**Tabela 1. Comparação de listas de tarefas do SharePoint e controle total**

| Recurso | Lista de tarefas | Controle total |
|:-----|:-----|:-----|
|**Lista de tarefas no SharePoint** <br/> |Leitura/gravação  <br/> |Somente leitura  <br/> |
|**Schedule Web Part** <br/> |Somente leitura  <br/> |Leitura/gravação  <br/> |
|**Relatórios** <br/> |Relatórios avançados pelo Project Server  <br/> |Relatórios avançados pelo Project Server  <br/> |
|**Outra funcionalidade do Project Server** <br/> | Funcionalidade bloqueada:  <br/>- Edições do projeto no lado do servidor, com o Project Web App ou aplicativos cliente personalizados  <br/>- Status  <br/>- As tarefas não ficam visíveis no modo de ligação  <br/> |A funcionalidade completa está habilitada  <br/> |
   
### <a name="managing-projects-as-sharepoint-task-lists"></a>Como gerenciar projetos como listas de tarefas do SharePoint
<a name="pj15_Architecture_VisibilityMode"> </a>

Quando o Project Server está associado a um conjunto de sites do SharePoint do qual o SharePoint mantém o controle, as listas de tarefas e arquivos do Project Professional 2013 (.mpp) em bibliotecas de documentos ficam visíveis para o Serviço do Aplicativo do Project. No entanto, o SharePoint mantém os dados mestres para sincronização (veja a Figura 1). Não é possível realizar o agendamento do lado do servidor com o Schedule Web Part. Você pode usar o Project Professional para sincronizar e editar a lista de tarefas em um site de projeto. Tendo as listas de tarefas do SharePoint como ponto de partida, as organizações podem evoluir gradualmente para usar a funcionalidade completa do Project Server.
  
A Figura 1 mostra os seguintes processos quando os projetos são mantidos nas listas de tarefas do SharePoint: 
  
- (A) O Project Professional pode sincronizar com listas de tarefas e criar novos sites do projeto no conjunto de sites antes ou depois da associação ao Serviço do Aplicativo do Project.
    
- (B) O Project Server sincroniza com dados do site do projeto para fins de relatórios, mas o SharePoint mantém os dados mestres; as listas de tarefas permanecem de leitura/gravação.
    
- (C) Após a associação, o Project Professional pode criar novos projetos e salvá-lo ou publicá-lo no Project Server. O Cache Ativo no Project Professional mantém a sincronização de dados com o Project Server.
    
- (D) Quando um novo projeto é publicado no Project Professional, o usuário tem a opção de criar um site de projeto para o projeto. Um projeto também pode ser criado no Project Web App como um tipo de projeto de lista de tarefas do SharePoint ou como um tipo de projeto corporativo (EPT) de controle total. A Etapa (D) mostra o EPT de controle total.
    
**Figura 1. Como usar sites do projeto como listas de tarefas do SharePoint**

![Como usar sites do projeto no modo de visibilidade](media/pj15_Architecture_VisibilityMode.gif "Como usar sites do projeto no modo de visibilidade")

<br/>

### <a name="managing-projects-with-full-control"></a>Como gerenciar projetos com controle total
<a name="pj15_Architecture_ManagedMode"> </a>

Quando o Project Server está associado a um conjunto de sites e tem controle total, ele importa as listas de tarefas do SharePoint como projetos corporativos e pode excluir todos os arquivos .mpp relacionados. O Project Server mantém os dados mestres para a sincronização da lista de tarefas. As listas de tarefas no conjunto de sites tornam-se somente leitura (veja a Figura 2). Os projetos importados podem ser editados usando o Project Professional ou o Project Web App.
  
> [!NOTE]
> Depois que o Project Server importar um projeto, o usuário escolherá excluir o projeto do site ou interromper a conexão antes da edição do projeto. Você pode fazer a escolha no Project Professional. 
  
A Figura 2 mostra os processos a seguir quando o Project Server mantém projetos corporativos com controle total:
  
- (A) O usuário pode escolher quais sites do projeto serão importados. O Project Server importa os sites do projeto e, opcionalmente, exclui os arquivos .mpp associados. A lista de tarefas do SharePoint de um projeto importado se torna somente leitura.
    
- (B) Após a associação, o Project Professional cria novos projetos e salva ou publica no Project Server. O Cache Ativo no Project Professional mantém a sincronização de dados com o Project Server. A Schedule Web Part no Project Web App pode fazer o agendamento no lado do servidor.
    
- (C) Quando um novo projeto é publicado no Project Professional, o usuário tem a opção de criar um site de projeto para o projeto. Também é possível criar um projeto no Project Web App com o EPT de controle total e publicá-lo com uma lista de tarefas somente leitura em um site do projeto no conjunto de sites.
    
**Figura 2. Como usar sites do projeto com controle total**

![Como usar sites do projeto no modo gerenciado](media/pj15_Architecture_ManagedMode.gif "Como usar sites do projeto no modo gerenciado")
  
## <a name="general-architecture"></a>Arquitetura geral
<a name="pj15_Architecture_General"> </a>

A Figura 3 mostra uma exibição generalizada da arquitetura do Project Server 2013, incluindo o Aplicativo do Serviço do Project, uma instância do Project Web App em um WFE e vários outros aplicativos clientes, incluindo o Project Professional 2013.
  
Pode haver várias instâncias do Project Web App que se comunicam com o Aplicativo do Serviço do Project de back-end. Para uma instalação local, o WFE pode estar em um servidor separado em um farm do SharePoint ou pode estar no mesmo servidor do SharePoint com o Aplicativo do Serviço do Project. O Project Online inclui um WFE, o Aplicativo do Serviço do Project e um servidor local ou remoto do Workflow Manager Client 1.0. 
  
**Figura 3. Arquitetura geral do Project Server 2013**

![Arquitetura do Project Server](media/pj15_Architecture_ProjectServiceApp_WFE.gif "Arquitetura do Project Server")

<br/>

Os comentários gerais à seguir aplicam-se à Figura 3:
  
- **Project Online:** você pode criar aplicativos que usam as interfaces CSOM, REST e OData. Um pacote de aplicativos também pode instalar receptores de eventos remotos em um serviço da Web personalizado em um servidor local, em um servidor do Azure ou no Microsoft Azure. O Project Online não oferece suporte a soluções locais de terceiros, à interface do WCF, à interface ASMX ou a manipuladores de eventos locais. 
    
- **Receptores de eventos:** os receptores de evento também podem ser chamados de manipuladores de eventos. O Project Online oferece suporte ao registro de receptores de eventos remotos do Project Server que podem ser usados por uma instância do Project Web App na nuvem ou por uma instalação do Project Server no local. Uma instalação do Project Server local oferece suporte a receptores de eventos remotos e manipuladores de eventos de confiança total locais. 
    
- **Navegadores:** não há limitações entre navegadores para visualizar algumas páginas do Project Web App como há no Project Server 2010. Os navegadores da Web a seguir têm suporte para uso completo com o Project Web App: 
    
  - Internet Explorer 8.x (no Windows 7 e em versões anteriores do Microsoft Windows), Internet Explorer 9.x e Internet Explorer 10.x 
  - Firefox 4.x (no Windows, Mac OS-X e Linux/Unix)
  - Safari 5.x (no Windows e no Mac OS-X)
  - Chrome
    
- **Interfaces programáticas:** para aplicativos de terceiros, o Project Online expõe a interface HTTP/HTTPS (incluindo REST), a interface CSOM, um serviço OData para o CSOM e um serviço OData para relatórios. Para aplicativos cliente de terceiros que estão no local (na Intranet), você pode usar a interface do WCF para PSI ou usar as interfaces CSOM, OData e REST por meio de HTTP. Os clientes do Project Web App e do Project Professional 2013 usam a interface do WCF. Em uma instalação de servidor único, os serviços Web de front-end ASMX, CSOM e REST chamam internamente os serviços do WCF de back-end. 
    
    > [!NOTE]
    > A interface do ASMX baseada em SOAP para serviços Web na PSI ainda está disponível no Project Server 2013, mas foi preterida. 
  
    O serviço OData para relatórios é implementado pelo serviço interno OData.svc do WCF. Você pode obter o Documento de metadados do serviço dos dados de relatório usando `https://ServerName/ProjectServerName/_api/ProjectData/$metadata`. 
    
    O serviço OData para o CSOM destina-se a plataformas como o Windows RT, o iOS e o Android, onde você pode usar a interface REST com o JavaScript em páginas HTML. 
    
    > [!NOTE]
    > Embora a opção `$metadata` para o serviço de relatório **ProjectData** seja válido, a opção`$metadata` para o serviço **ProjectServer** do CSOM é removida na versão do Project Server 2013. Para saber mais sobre as consultas REST, confira [Modelo de objeto do cliente (CSOM) para o Project Server](client-side-object-model-csom-for-project-2013.md). 
  
- **Encaminhador PSI:** o acesso programático à PSI em um WFE separado passa pelo Encaminhador PSI, que inclui um Encaminhador WCF e um Encaminhador Serviço Web. Clientes que usam a interface ASMX acessam a PSI pelo Encaminhador Serviço Web. Clientes que usam a interface WCF acessam a PSI pelo Encaminhador WCF. O acesso programático pelo CSOM, OData e REST é canalizado pelo Encaminhador WCF. 
    
- **Fluxos de trabalho:** fluxos de trabalho declarativos (fluxos de trabalho definidos no SharePoint Designer 2013) são descarregados para o Workflow Manager Client 1.0 para processamento. O Workflow Manager Client 1.0 pode ser executado em um servidor separado no farm do SharePoint, no Microsoft Azure em nuvem ou em um computador exclusivo do Project Server para teste e demonstrações. Os fluxos de trabalho codificados desenvolvidos com o Visual Studio 2012 são processados no tempo de execução do fluxo de trabalho dentro do SharePoint Server, como no Project Server 2010. Para saber mais confira [Introdução ao desenvolvimento de fluxos de trabalho do Project Server](getting-started-developing-project-server-workflows.md).
    
- **Rede de perímetro (DMZ):**  a Figura 3 não mostra que um servidor WFE local pode ser isolado por um firewall adicional em uma rede de perímetro (também conhecida como "zona desmilitarizada" ou DMZ). Uma rede de perímetro pode permitir que clientes da Internet acessem o SharePoint e o Project Server passando por um firewall. 
    
- **SharePoint Web Services:**  a Figura 3 não mostra a infraestrutura do SharePoint, como o aplicativo de back-end SharePoint Web Services, que faz parte do SharePoint Server 2013. Quando você instala o Project Server, o Aplicativo do Serviço do Project é adicionado ao SharePoint Web Services. 
    
A camada de front-end inclui aplicativos de terceiros, o Project Professional e o Project Web App. O navegador exibe páginas do ASP.NET 4.0 (páginas .aspx) no Project Web App. As páginas do Project Web App usam Web Parts do Project Server que se comunicam com a PSI e também usam Web Parts do SharePoint padrão. 
  
A camada intermediária inclui a PSI e a camada de objeto de negócios, que consiste em objetos lógicos que representam entidades comerciais do Project Server. As entidades de negócios incluem Projeto, Tarefa, Recurso, Atribuição e assim por diante. A PSI e o nível do objeto de negócios estão fortemente acoplados e estão localizados no mesmo servidor. Um aplicativo cliente chama a PSI por meio de uma das interfaces disponíveis e a PSI invoca objetos de negócios. Para melhorar o desempenho, o WFE do Project Server 2013 inclui alguns objetos de negócios para solicitações que não usam o Sistema de Enfileiramento do Project Server ou exigem o Serviço de Cálculo do Project. Os objetos de negócios do WFE se comunicam diretamente com o banco de dados do Project.
  
Os componentes Project Web App do Project Server usam o banco de dados de configuração do SharePoint 2013 para configuração do site do projeto e o banco de dados de conteúdo para conteúdo do site do projeto, como listas de tarefas, páginas personalizadas, fluxos de trabalho, configurações de gerenciamento, documentos e listas de problemas, riscos e compromissos. Os bancos de dados de configuração e de conteúdo do SharePoint dão suporte a recursos adicionais para gerenciamento de projetos, como modelos e espaços de trabalho de projeto, listas personalizadas para colaboração em equipe e relatórios.
  
### <a name="project-web-app-and-the-wfe"></a>Project Web App e o WFE
<a name="pj15_Architecture_PWAServer"> </a>

Você pode configurar várias instâncias do Project Web App em um WFE e vários servidores WFE em uma intranet corporativa para permitir a distribuição de carga para clientes de intranet. Quando um aplicativo cliente usa uma instância do Project Web App em um servidor WFE separado, as chamadas PSI são roteadas pelo Encaminhador PSI. O Encaminhador PSI (o Encaminhador WCF ou o Encaminhador Serviço Web) executa as seguintes funções:
  
- Otimiza as chamadas de clientes remotos para a PSI.
    
- Distingue entre chamadas PSI que exigem o Serviço de Fila do Project Server e aquelas que não. Os nomes de método de PSI assíncrona começam com Queue, como **QueueCreateProject**.
    
- Identifica chamadas PSI que invocam manipuladores de eventos locais registrados.
    
- Identifica chamadas à PSI que exigem o Serviço de Cálculo do Project.
    
- Usa um cache baseado em servidor que funciona com o Cache Ativo do lado do cliente no Project Professional para reduzir as chamadas de ida e volta para o Project Server.
    
Depois que o SharePoint Server autentica um usuário do Project Server, o Encaminhador PSI envia, de forma transparente, solicitações que usam serviços de back-end para os serviços PSI no computador que executa o Project Server. As solicitações que não exigem serviços de back-end são enviadas para os objetos de negócios na instância local do Project Web App. O Encaminhador PSI melhora a escalabilidade, o desempenho e a confiabilidade do processamento do Project Server na LAN, em uma WAN e no Project Online.
  
O Project Web App é desenvolvido com o ASP.NET 4.0. Os elementos visuais em arquivos .aspx (HTML, controles de servidor e texto estático) são separados da lógica de programação em classes de código subjacente que estão em assemblies compilados (arquivos .dll). As páginas do site no Project Web App, como a página de nível superior, o Centro de Projeto e a Central de Relatórios, podem ser personalizadas com Web Parts. As páginas do aplicativo que não têm uma opção **Editar Página** no menu **Ações do Site** não podem ser editadas, como a página Configurações do Servidor e a página Revisar Quadro de Horários. 
  
### <a name="the-csom-and-the-project-server-interface"></a>O CSOM e a Interface do Project Server
<a name="pj15_Architecture_PSI"> </a>

A PSI é fatorada em 22 serviços públicos, como **Project**, **Resource**, **CustomField** e **Statusing**. A PSI também contém sete serviços particulares para uso interno. A PSI é a API fundamental do Project Server. Ela expõe a funcionalidade do Project Server ao CSOM e a aplicativos externos. O CSOM inclui classes que acessam as classes e os membros da PSI mais usados, utilizados para aplicativos de terceiros. No Project Server 2013, algumas funcionalidades do Project Server não estão disponíveis no CSOM, como os serviços **Admin**, **Calendar**, **PortfolioAnalyses** e **Security**. 
  
O Project Professional 2013 e o Project Web App usam o PSI para acessar os dados do Project Server nas tabelas e exibições de rascunho, publicadas e arquivadas do banco de dados do Project. Você pode acessar um serviço do PSI através de um arquivo de proxy ou de um assembly de proxy, tanto para os serviços do WCF ou para os serviços Web do ASMX.
  
> [!NOTE]
> O CSOM é a interface preferencial para desenvolvedores do Project Server terceirizados; pode ser usado para aplicativos que acessam uma instalação local do Project Server e o Project Online. Recomendamos que você use o CSOM para o desenvolvimento de novos aplicativos, caso o CSOM inclua a funcionalidade exigida por seu aplicativo. 
  
Alguns aplicativos de linha de negócios (LOB) e outros aplicativos de terceiros desenvolvidos para o Project Server 2010 exigem serviços do PSI que ainda estejam representados no CSOM. Se eles se destinarem somente a uma instalação local do Project Server, os aplicativos poderão continuar a usar a interface do WCF ou a interface do ASMX da PSI.
  
Os aplicativos cliente chamam o PSI por meio de proxies de serviço. Os clientes que usam a interface do WCF acessam todos os serviços do PSI pelo `https://ServerName/ProjectServerName/_vti_bin/psi/ProjectServer.svc`. Os clientes que usam uma interface de serviço Web ASMX usam a URL do Project Web App para o serviço específico. Por exemplo, o serviço **Resource** está em `https://ServerName/ProjectServerName/_vti_bin/psi/resource.asmx?wsdl`. Se os aplicativos não tiverem acesso à intranet no Project Server, eles poderão usar um servidor do Project Web App em uma rede de perímetro (não mostrada na Figura 3).
  
A Figura 4 exibe o painel **Conexões** no **Gerenciador dos Serviços de Informações da Internet (IIS)** para uma instalação de servidor único do SharePoint Server 2013, Project Server 2013 e um site local de Gerenciamento de Fluxo de Trabalho para o Workflow Manager Client 1.0. O conjunto de sites do SharePoint (A) inclui os serviços do PSI de front-end no subdiretório virtual `_vti_bin\PSI`. O aplicativo SharePoint Web Services (B) inclui o Aplicativo do Serviço do Project, com os serviços de back-end do PSI no subdiretório virtual `508c23fb7dfd4c83a8919fae24bc68c5/PSI`. O GUID é o nome da instância do Aplicativo do Serviço do Project para essa instalação do Project Server. 
  
**Figura 4. Gerenciador do IIS mostrando o PSI de front-end (A) e o PSI de back-end (B)**

![O PSI de front-end e o PSI de back-end](media/pj15_Architecture_PSI_IIS.gif "O PSI de front-end e o PSI de back-end")
  
Os aplicativos cliente não podem acessar diretamente os serviços do WCF para o PSI no Aplicativo do Serviço do Project de back-end. Se eles não exigirem acesso ao Project Online, os aplicativos cliente e os componentes dos aplicativos LOB usarão proxies para o PSI. Uma URL de back-end para a interface do WCF do serviço **Resource** na Figura 4, por exemplo, seria `https://ServerName:32843/508c23fb7dfd4c83a8919fae24bc68c5/psi/resource.svc`. A porta 32843 é a porta HTTP padrão para o aplicativo SharePoint Web Services (32844 é a porta para comunicações HTTPS). No entanto, o arquivo web.config do Project Web App bloqueia o acesso direto aos serviços de back-end do PSI.
  
> [!NOTE]
> O download do SDK do Project 2013 inclui arquivos de proxy do PSI para os serviços do WCF e para os serviços do ASMX, além de instruções sobre como compilá-los para assemblies de proxy. > Para criar arquivos de proxy da PSI atualizados que usam o interface do WCF, você terá de usar o utilitário svcutil.exe ou o Visual Studio diretamente no computador do Project Server. 
  
Membros dos serviços PSI normalmente produzir ou consumir objetos **conjunto de dados** tipados como meio de troca de informações de objetos comerciais. Existem também vários modelos diferentes para o desenvolvimento da PSI. Por exemplo, os serviços PSI **Resource**, **CustomFields** e **LookupTable** PSI usam objetos de filtro XML para manipulação **DataSet** e outros serviços não. Alguns métodos no serviço **Statusing** usam um parâmetro _changeXml_, enquanto outros métodos e serviços não. O CSOM não utiliza conjuntos de dados. Embora o CSOM tenha um modelo de programação diferente da PSI, e você possa usar assemblies do .NET ou JavaScript, o desenvolvimento com o CSOM é geralmente mais simples e mais consistente se comparado com o desenvolvimento com a PSI. 
  
Para obter mais informações sobre a PSI, confira [Visão geral da referência de PSI do Project](project-psi-reference-overview.md). Para saber mais sobre o CSOM, confira [Modelo de objeto do cliente (CSOM) para o Project 2013](client-side-object-model-csom-for-project-2013.md).
  
### <a name="business-objects-in-the-wfe-and-the-project-service-application"></a>Objetos de negócios no WFE e no Aplicativo do Serviço do Project
<a name="pj15_Architecture_BusinessObjects"> </a>

O modelo de objeto interno do Project Server inclui os objetos de negócios, que representam entidades lógicas, como Projeto e Recurso. Os aplicativos cliente só acessam objetos de negócios por meio do CSOM ou da PSI. Os objetos de negócios, por sua vez, acessam as tabelas e as exibições de rascunho, de publicação e de arquivo morto do banco de dados do Project.
  
Os objetos de negócios não são expostos a desenvolvedores terceirizados. A PSI manipula o mapeamento da API para objetos de negócios, e o CSOM mapeia sua API para o PSI. As entidades lógicas dos objetos de negócios podem ser classificadas em três tipos:
  
- **Entidades fundamentais** são objetos como projetos, tarefas, atribuições, recursos e calendários. As entidades fundamentais incluem lógica comercial básica, como permissões e nomenclatura. 
    
- **Entidades comerciais** são objetos como quadros de horários, portfólios de projeto e modelos. As entidades comerciais incluem lógica comercial adicional e normalmente são criadas de uma combinação das entidades fundamentais. 
    
- As **entidades de suporte** são objetos como segurança e validação. 
    
No Project Server 2010, todos os objetos de negócios são implementados no Aplicativo do Serviço do Project. No Project Server 2013, o WFE hospeda muitos dos objetos de negócios que processam métodos síncronos e não exigem o Serviço de Cálculo do Project. Os métodos de PSI síncrona, como **DeleteProject** e **ReadAssignments**, não usam o Serviço de Fila do Project Server. Os métodos assíncronos na PSI têm nomes que começam com `Queue`, como **QueueCreateProject** e **QueueUpdateTimesheet**. Um método assíncrono envia uma mensagem ao Serviço de Fila do Project Server que agenda o processamento do método enquanto o controle é retornado ao usuário.
  
O Encaminhador PSI determina quais solicitações são encaminhadas para o Aplicativo do Serviço do Project e quais podem ser processadas pelos objetos de negócios no WFE. Os objetos de negócios no WFE ignoram o Aplicativo do Serviço do Project e têm acesso direto ao banco de dados do Project, semelhante à maneira que outros processos do SharePoint em um WFE acessam diretamente os bancos de dados de Configuração e de Conteúdo. A execução de vários dos objetos de negócios no WFE aumenta a eficiência do Project Server, reduz a carga na camada do aplicativo e permite que o Project Server seja melhor dimensionado para cargas de trabalho maiores.
  
> [!NOTE]
> No Project Server 2013, os manipuladores de eventos locais devem ser implantados no WFE e no computador de back-end do Project Server. 
  
### <a name="project-server-database"></a>Banco de dados do Project Server
<a name="pj15_Architecture_DAL"> </a>

No Project Server 2013, os quatro bancos de dados do Project Server de versões anteriores são combinados em um banco de dados do Project no SQL Server. O nome do banco de dados padrão do Project é ProjectService. As tabelas e exibições de relatório mantêm seus nomes anteriores com o prefixo `dbo`, como dbo.MSP_EpmProject e dbo.MSP_EpmProject_UserView. As tabelas e as exibições que anteriormente estavam no banco de dados Rascunho têm o prefixo `draft`. As tabelas e as exibições do banco de dados Publicado têm o prefixo `pub`. As tabelas e as exibições do banco de dados Arquivo morto têm o prefixo `ver`. 
  
> [!IMPORTANT]
> O acesso direto não é suportado pelas tabelas e visualizações de rascunho (prefixo `draft`), publicado (prefixo `pub`) e arquivo (prefixo `ver`). Os relatórios devem usar apenas as tabelas e exibições de relatório que têm o prefixo `dbo`. 
  
Os dados do Project Server são particionados no banco de dados do Project da seguinte maneira:
  
- As tabelas e exibições de rascunho contêm dados de projetos não publicados criados pelo Project Professional e outros aplicativos. O Project Web App não exibe dados de projeto das tabelas e exibições de rascunho.
    
- As tabelas e exibições publicadas contêm todos os projetos e recursos publicados da empresa, dados globais para tipos de projeto corporativo (EPTs) e outros modelos de projeto. Projetos publicados são visíveis no Project Web App. Os dados publicados também incluem tabelas específicas do Project Web App (quadros de horários, modelos, visualizações e assim por diante) e tabelas de dados globais (campos personalizados, tabelas de consulta, permissões de autorização do Project Server e metadados).
    
- Os dados de arquivamento salvam versões de backup de projetos, recursos, campos personalizados e outros dados.
    
- Os dados de relatório podem ser usados para acesso somente leitura em aplicativos de terceiros e para relatórios. Os cubos OLAP do Project Server usam as exibições de relatório que possuem o sufixo `_OlapView`. Os cubos OLAP estão disponíveis em uma instalação local do Project Server, mas não estão disponíveis no Project Online. 
    
    Os dados de relatórios são abrangentes e são atualizados quase em tempo real. As tabelas e exibições de relatórios são otimizadas para geração de relatório somente leitura; por exemplo, as tabelas de relatórios são desordenados para oferecerem dados redundantes e reduzirem o número de tabelas relacionais.
    
As entidades lógicas, como Recurso ou Projeto, podem se estender por várias tabelas, e todas as tabelas para uma entidade em particular têm a mesma chave primária. A chave primária é o GUID em uma única coluna que identifica exclusivamente uma instância de uma entidade em particular.
  
Os dados do Project Server para cada instância do Project Web App são armazenados em um banco de dados separado do Project com um nome diferente. Aplicativos cliente que possuem acesso direto ao Project Server podem ler diretamente as tabelas e exibições de relatórios. Para acesso remoto, os aplicativos cliente podem usar a interface OData e a interface REST para obter dados para relatórios. Os clientes devem usar apenas o CSOM ou a PSI para acessar as tabelas e exibições de rascunho, publicadas e arquivadas. O serviço de dados de relatório (RDS, que não é mostrado na Figura 3) atualiza os dados de relatório de dados publicados praticamente em tempo real. O banco de dados do Project pode estar localizado em um servidor separado.
  
Os esquemas são documentados apenas para as tabelas e exibições de relatórios. Para uma instalação local do Project Server, você pode adicionar tabelas e exibições de relatórios para entidades que não estão definidas no esquema de banco de dados do Project. Você também pode criar bancos de dados separados para aplicativos locais personalizados. A modificação não é suportada pelas tabelas e exibições Rascunho, Publicado e Arquivo. Como o banco de dados do Project não está diretamente acessível no Project Online, as tabelas e exibições de relatório não podem ser modificadas. No entanto, se você tiver uma conta do SQL Azure, poderá criar bancos de dados separados para uso personalizado com o Project Online.
  
### <a name="event-receivers"></a>Receptores de eventos
<a name="pj15_Architecture_EventHandlers"> </a>

Os manipuladores de eventos locais e receptores de eventos remotos do Project Server permitem extensibilidade de terceiros em resposta a eventos do Project Server, como criar ou publicar um projeto. No Project Server 2010, todos os manipuladores de eventos são locais e são gravados em código de confiança total, implantados diretamente no computador que está executando o Project Server e nos WFEs e executados dentro do Project Server Eventing System. Como o Project Online não pode usar manipuladores de eventos de confiança total, o Project Server 2013 implementa receptores de eventos remotos que são semelhantes aos receptores de eventos remotos no SharePoint Server 2013. Uma instalação local do Project Server 2013 pode usar manipuladores de eventos de confiança total tradicionais e receptores de eventos remotos.
  
Um receptor de eventos remotos do Project Server pode ser implementado em um serviço Web personalizado com um ponto de extremidade SOAP executado no Microsoft Azure ou em outros ambientes que deem suporte a serviços Web SOAP. Um pacote de aplicativos do Project Server pode incluir receptores de eventos remotos instalados com o aplicativo.
  
Os receptores de eventos remotos podem retornar a chamada para o Project Server usando os terminais CSOM (não mostrados na Figura 3). A chamada para um receptor de eventos remoto inclui informações do Project Server Eventing System e da instância do Project Web App (ou o locatário do Project Web App no Project Online) que emite a chamada. Os receptores de eventos remotos permitem criar e hospedar um único serviço Web que pode ser usado por várias instalações do Project Server. Por outro lado, os manipuladores de eventos de confiança total locais devem ser implantados para cada instalação do Project Server.
  
### <a name="publishing-and-server-side-scheduling"></a>Publicação e agendamento do servidor
<a name="pj15_Architecture_PublishingScheduling"> </a>

O Project Server 2013 suporta atualizações manuais e automatizadas do cronograma do projeto. O processo padrão é uma atualização de programação manual. Ou seja, o gerente de projeto faz check-out e abre um projeto no Project Professional ou no Project Web App, aplica as alterações e, em seguida, salva e publica o projeto para disponibilizar as alterações para todas as pessoas. O Project Professional possui um mecanismo de agendamento que calcula as alterações e salva as alterações no Project Server. No Project Server 2010, o mecanismo de agendamento do lado do servidor é uma implementação diferente do mecanismo de agendamento no Project Professional.
  
No Project Server 2013, o Serviço de Cálculo do Project implementa o mecanismo de agendamento do Project Professional 2013. O Serviço de Cálculo do Project é executado em um serviço do Windows chamado **Serviço de Cálculo do Microsoft Project Server**. A edição de um agendamento de projeto no Project Web App ou com aplicativos de terceiros que usam o CSOM resulta exatamente nas mesmas alterações de agendamento que o Project Professional faria.
  
> [!NOTE]
> Os aplicativos de terceiros que usam a PSI podem apresentar algumas diferenças de agendamento de um agendamento calculado pelo Project Web App. Para compatibilidade com versões anteriores, os métodos PSI públicos que fazem o agendamento no servidor ainda usam o mecanismo de agendamento que foi introduzido no Project Server 2010. **QueueUpdateProject2** é uma exceção já que é um novo método PSI no Project Server 2013. Por exemplo, o mecanismo de agendamento mais antigo não agenda subprojetos ou links para outros projetos e não calcula campos de valor agregado. Para evitar possíveis diferenças de agendamento entre aplicativos de terceiros e o Project Professional ou o Project Web App, você deve desenvolver aplicativos com o CSOM sempre que possível. 
  
O Project Server permite que a versão publicada de um projeto seja atualizada enquanto um gerente de projeto estiver usando a versão de rascunho, por meio destas etapas:
  
1. O Project Server aplica atualizações e reagenda a versão publicada.
    
2. O Project Server salva a atualização para aplicar à versão de rascunho quando um destes eventos ocorrer:
    
   - O Project Professional abre o projeto.
    
   - O Project Professional tenta publicar o projeto.
    
3. Se houver um conflito, o gerente de projeto será notificado e deverá resolver o conflito antes que a versão de rascunho seja publicada.
    
## <a name="see-also"></a>Confira também

- [Visão geral do Project 2013 para desenvolvedores](https://msdn.microsoft.com/library/8da91ab0-af4f-429f-8241-490600e3f7bd%28Office.15%29.aspx)
- [Programabilidade do Project Server](project-server-programmability.md)  
- [Modelo de objeto do cliente (CSOM) para o Project 2013](client-side-object-model-csom-for-project-2013.md)  
- [O que a PSI faz e não faz](what-the-psi-does-and-does-not-do.md)  
- [Introdução ao desenvolvimento de fluxos de trabalho do Project Server](getting-started-developing-project-server-workflows.md)   
- [Visão geral da referência da PSI do Project](project-psi-reference-overview.md)   
- [Protocolo Open Data](https://www.odata.org/)
    

