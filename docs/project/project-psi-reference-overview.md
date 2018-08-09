---
title: Visão geral da referência PSI do Project
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
f1_keywords:
- Admin
- Archive
- Authentication
- Calendar
- CubeAdmin
- CustomFields
- Events
- LoginForms
- LoginWindows
- LookupTable
- Notifications
- ObjectLinkProvider
- Project
- Project Server Interface
- Project Server Web services
- PSI
- PSI reference
- PSI Web services
- PWA
- QueueSystem
- Resource
- ResourcePlan
- Rules
- Security
- Statusing
- StatusReports
- TimeSheet
- Version
- View
- Web service
- Web services
- WinProj
- WssInterop
keywords:
- Web service, calendário, autenticação, Web service, ResourcePlan, Web service, StatusReports, Web service, PSI, namespaces, manipuladores de eventos, Project Server, o serviço da Web, notificações, QueueSystem, Web plataforma de serviço, Project 2013, LoginWindows, Web serviço, o serviço Web, status, serviço da Web, recurso, WinProj, serviço do Web service, WssInterop, Web, o serviço de Web do serviço, Winproj, evento manipuladores, LookupTable, Web service, PWA, da Web, Web service, segurança, notificações, serviço da Web, o serviço Web, Quadro de horários, o Web service, QueueSystem, PSI, serviços Web, o serviço Web, eventos, PSI, programação, o serviço Web, LookupTable, versão, serviço da Web, CustomFields, serviço da Web, o serviço Web, PWA, PSI, recurso, serviço da Web, o serviço Web, ResourcePlan, quadro de horários, Web pessoal, o serviço Web, regras, PSI, gerenciado serviço da Web de referência, segurança, de código, Web service, CustomFields, URL, para a PSI, Web service, WssInterop, Web service, Admin, Web referência, PSI, Web service, CubeAdmin, View, serviço da Web service, calendário, Web, Web serviço de exibição, administração, serviço Web, LoginForms, Web service, serviço da Web, LoginForms, PSI, URLs, ObjectLinkProvider, o serviço da Web service, arquivamento, Web service, CubeAdmin, Web service, regras, Web, Web service, autenticação, serviços Web, PSI, Project Server , eventos, eventos, serviço da Web, o serviço Web, projeto, status, Web pessoal, serviço, ObjectLinkProvider, Project Server Interface Web, o serviço da Web métodos, PSI, Web service, StatusReports, Web, arquivo morto, Project, Web service, serviço Web, LoginWindows
localization_priority: Normal
ms.assetid: d3c33089-0cbe-48c3-bfc0-0be819ca4d73
description: O Project Server Interface (PSI) é a API para usar para o desenvolvimento de aplicativos que integram com o Project Server 2013 local.
ms.openlocfilehash: 14ab540fd8a66cf18c576572fc0eff4df7c7d61c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771180"
---
# <a name="project-psi-reference-overview"></a>Visão geral da referência PSI do Project

O Project Server Interface (PSI) é a API para usar para o desenvolvimento de aplicativos que integram com o Project Server 2013 local.
  
Este artigo é uma visão geral do serviços na PSI, namespaces e assemblies documentados. A [referência do serviço de web e de biblioteca de classe do Project Server 2013](http://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) no SDK contém toda a documentação de código gerenciado para a PSI e o namespace [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) no Project Server 2013. Para desenvolver aplicativos para o Project Online, você deve usar o namespace **Microsoft.ProjectServer.Client** em vez da PSI. 

A PSI no Project Server 2013 tem uma interface dupla. A interface ASMX para serviços da web é definida por descoberta e arquivos de Web Service Description Language (disco e WSDL) no `http://ServerName/ProjectServerName/_vti_bin/psi/` diretório virtual (por exemplo, Projectdisco.aspx e Projectwsdl.aspx). Você pode acessar a interface ASMX somente através da URL de uma instalação local do Project Web App (por exemplo, `http://ServerName/ProjectServerName/_vti_bin/psi/project.asmx?wsdl)`. Para mostrar o serviço web em um navegador, você deve incluir o `?wsdl` opção URL. Porque a interface ASMX é criada usando a infra-estrutura do Windows Communication Foundation (WCF), os arquivos. asmx para serviços web do Project Server não existir no diretório virtual de PSI. 
  
A interface de serviços do WCF é definida pelos arquivos. svc no back-end `http://ServerName:32843/GUID/PSI/` diretório virtual do aplicativo de serviços Web do SharePoint. Os serviços de URL de PSI no diretório virtual do aplicativo de serviço do projeto (por exemplo, `http://ServerName:32843/GUID/PSI/project.svc`) inclui os arquivos. svc. Mas, diretamente você não pode usar a URL de back-end para definir uma referência de serviço WCF. Para desenvolver um aplicativo ou componente que usa os serviços do WCF a PSI, você pode usar um assembly de proxy ou um arquivo de proxy. O download do SDK do Project 2013 inclui arquivos de proxy para os serviços WCF no Project Server 2013 e compilações de scripts para obter os arquivos atualizados de proxy WCF e compilar os arquivos em um assembly de proxy para o mais recente do Project Server.
  
O nome do diretório de aplicativo de serviço do projeto é um valor GUID, que é o mesmo que o GUID da instância do Project Web App no local. Na janela do **Gerenciador de serviços de informações da Internet (IIS)** , expanda o nó **Serviços Web do SharePoint** , escolha o nome do diretório GUID e escolha **Configurações avançadas** para copiar o valor de **Caminho Virtual** . 
  
> [!IMPORTANT]
> A interface de serviço web ASMX de PSI foi preterido no Project Server 2013, mas ainda é suportado. Novos aplicativos devem usar a interface WCF de PSI ou CSOM do. Para obter mais informações sobre recursos preteridos, consulte [atualizações para desenvolvedores no Project 2013](updates-for-developers-in-project-2013.md)
> 
> Novos aplicativos e componentes middleware executada somente em uma instalação local do Project Server, devem usar a interface WCF, que é a tecnologia que a Microsoft recomenda para comunicações de rede. Aplicativos que usam a interface ASMX herdados devem usar a URL por meio do Project Web App, que verifica as permissões do Project Server. 
> 
> Para obter mais informações sobre a interface ASMX e como usar a interface WCF, consulte [pré-requisitos para amostras de código com base em ASMX no projeto](prerequisites-for-asmx-based-code-samples-in-project.md) e [pré-requisitos para amostras de código com base em WCF no projeto](prerequisites-for-wcf-based-code-samples-in-project.md). 
  
Para desenvolver aplicativos que usam a interface WCF, você pode usar o Visual Studio 2010 ou Visual Studio 2012. Para criar fluxos de trabalho declarativos do Project Server, você pode usar o SharePoint Designer 2013. Fluxos de trabalho de servidor de projeto que precisam acessar a PSI ou CSOM do podem ser desenvolvidos com o Visual Studio 2012.
  
### <a name="using-the-psi-reference"></a>Usando a referência PSI
<a name="pj15_PSIRefOverview_Using"> </a>

O modelo de objeto PSI é grande e muitas classes e membros são apenas para uso interno. Como resultado, pode ser confusa localizar os tópicos que você deseja na [referência do serviço Project Server 2013 classe biblioteca e web](http://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx). A maioria dos tópicos de referência que você usará para desenvolvimento está em grupos a seguir:
  
- **Métodos da classe principal:** Cada serviço na PSI inclui uma classe principal que é chamada para o nome do serviço. Por exemplo, o serviço de **recursos** contém a classe de [recurso](https://msdn.microsoft.com/library/WebSvcResource.Resource.aspx) , que está no namespace [WebSvcResource](https://msdn.microsoft.com/library/WebSvcResource.aspx) . Para ver uma lista dos métodos que estão disponíveis na classe do **recurso** , expanda o nó de classe no painel conteúdo e escolha o tópico de **Métodos de recurso** . 
    
- **Propriedades DataRow:** Muitos dos métodos da classe principal usam ou retornam um **conjunto de dados**. Cada objeto **DataTable** em um **conjunto de dados** contém dados em um ou mais objetos **DataRow** . Na maioria dos casos, você precisará ver apenas as propriedades de linha, nem todos os outros membros das classes **DataSet**, **DataTable**ou **DataRow** . Por exemplo, a classe de **ResourceAssignmentDataSet** inclui subclasses para o **ResourceAssignmentDataTable** e a classe de [ResourceAssignmentDataSet.ResourceAssignmentRow](https://msdn.microsoft.com/library/WebSvcResource.ResourceAssignmentDataSet.ResourceAssignmentRow.aspx) . Para ver uma lista de propriedades que estão na classe **ResourceAssignmentRow** , expanda o nó de classe no painel conteúdo e escolha o tópico **ResourceAssignmentDataSet.ResourceAssignmentRow propriedades** . 
    
Além dos namespaces de serviço, os links de tópico de [referência do serviço de web e de biblioteca de classe do Project Server 2013](http://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) para os três assemblies do Project Server que são usadas no desenvolvimento de soluções de terceiros para local instalações. Fornecemos apenas a documentação mínima para esses assemblies. A referência PSI documenta as principais classes e membros nos serviços públicos de 23. Serviços de seis PSI são apenas para uso interno e não estão documentados. 
  
> [!NOTE]
> Classes no modelo de objeto do cliente (CSOM) podem ser usados independentemente de outros assemblies do Project Server e serviços. Você pode usar o namespace **Microsoft.ProjectServer.Client** em um ambiente de desenvolvimento remoto do computador do Project Server e como desenvolver aplicativos que integram com o Project Online ou com uma instalação local do Project Server. No entanto, o CSOM contém um subconjunto da funcionalidade da PSI completa. O CSOM permite o desenvolvimento dos cenários mais comuns de integração do Project Server. Para obter mais informações, consulte [o que o CSOM e não faz](what-the-csom-does-and-does-not-do.md) e [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) . 
  
Para o desenvolvimento da maioria dos aplicativos que usam a PSI, você não precisará desenvolver em um computador do Project Server ou definir referências a assemblies do Project Server no cache de assembly global. Você pode copiar os assemblies do Project Server necessários para seu computador de desenvolvimento. Project Server 2013 instala os seguintes assemblies em _[Arquivos de programa]_ `\Microsoft Office Servers\15.0\Bin`: 
  
- Microsoft.Office.Project.Server.Events.Receivers.dll 
- Microsoft.Office.Project.Server.Library.dll
- Microsoft.Office.Project.Server.Workflow.dll
    
Namespaces para os serviços PSI têm nomes arbitrários, criados para um assembly de proxy PSI, ProjectServerServices.dll, que é gerado para fins de documentação. Na referência do PSI, cada namespace de serviço tem um nome de espaço reservado (por exemplo, _[serviço web do projeto]_) e uma referência da web (como `http://ServerName/ProjectServerName/_vti_bin/psi/Project.asmx?wsdl`). 
  
## <a name="project-server-assemblies-and-namespaces"></a>Namespaces e assemblies do project Server
<a name="pj15_PSIRefOverview_Assemblies"> </a>

Muitos conjuntos são instalados quando você instala o Project Server; apenas quatro os assemblies do Project Server está documentados. Desenvolvedores de terceiros geralmente usam apenas algumas classes e membros nesses conjuntos. Os assemblies do Project Server não documentados incluem namespaces e classes que Project Server usa internamente, tais como de classes para o Project Web App, as entidades de negócios, e o acesso a dados camada (DAL). Quando você define uma referência no Visual Studio para um dos documentadas assemblies do Project Server, você pode ver todos os namespaces, classes e membros no Pesquisador de objetos Visual Studio.
  
> [!NOTE]
> Muitos membros dos documentadas namespaces do Project Server são usados apenas internamente e tem a documentação mínima. 
  
Ao desenvolver para o Project Online, você pode usar somente o CSOM para acessar a funcionalidade do Project Server. Você não tem acesso a serviços PSI ou os assemblies do Project Server.
  
A [referência do serviço de web e de biblioteca de classe do Project Server 2013](http://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) para a PSI inclui namespaces dos seguintes módulos: 
  
- **Microsoft.Office.Project.Server.Library.dll** desse assembly contém um namespace documentado e namespaces não documentados três, da seguinte maneira: 
    
  - O namespace [Microsoft.Office.Project.Server.Library](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.aspx) inclui muitos enumerações e os campos de classe e propriedades que são frequentemente utilizadas em aplicativos de local para o Project Server. Por exemplo, os desenvolvedores geralmente usar enumerações como **CustomField.Type**e as classes de **filtro** , **PSErrorInfo**e **PSClientError**. 
    
    O namespace **Microsoft.Office.Project.Server.Library** também inclui as seguintes classes de sete propriedade, que incluem 3.200 acima subclasses: 
    
      - **AssignmentProperties**  
      - **CalendarProperties**
      - **ConstraintProperties**
      - **LookupTableProperties**
      - **Propriedades do projeto**
      - **ResourceProperties**
      - **TaskProperties**
    
    As classes de propriedade são usadas internamente e não estão documentadas. As classes de propriedade são usadas para serialização entre o Project Server e o Project Professional 2013. Quando você trabalha com o namespace **Microsoft.Office.Project.Server.Library** no Visual Studio, o Pesquisador de objetos mostra todas as classes de propriedade, o que torna mais difícil localizar classes que são úteis para o desenvolvimento de terceiros. Porque os desenvolvedores de terceiros não é necessário usar as classes de propriedade, o SDK não documenta-los. 
    
  - **Microsoft.Office.Project.Server.DataServices** as classes e os membros deste namespace são usados internamente pelo serviço **OData** no Project Online para acessar as tabelas de relatório no banco de dados do projeto. As classes **DataServices** não estão documentadas. 
    
  - **Microsoft.Office.Project.Server.Administration** as classes e os membros deste namespace usados internamente para o log de diagnóstico e não estão documentados. 
    
  - **Microsoft.Office.Project.Server.Base** as classes e os membros deste namespace são usados internamente como classes base e não estão documentados. 
    
  - **Microsoft.Office.Project.Server.Library.FilterSchema** esse namespace é usado internamente para gerar esquemas de filtro e não está documentado. 
    
- **Microsoft.Office.Project.Server.Workflow.dll** desse assembly é usado para herdado fluxos de trabalho do Project Server 2010 que ainda podem trabalhar no Project Server 2013. Para criar novos fluxos de trabalho, você deve usar o SharePoint Designer 2013 ou, você também pode usar o Visual Studio 2012 com a classe [Microsoft.ProjectServer.Client.WorkflowActivities](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.WorkflowActivities.aspx) . O assembly Microsoft.Office.Project.Server.Workflow.dll inclui os seguintes três namespaces: 
    
  - [Microsoft.Office.Project.Server.Workflow](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Workflow.aspx) esse namespace inclui classes que são usadas para atividades de fluxo de trabalho do Project Server. As atividades são de leitura, comparando e atualizando as propriedades do projeto. Outras classes gerenciar fluxos de trabalho e incluem retornos de chamada de fluxo de trabalho quando projetos são alterados. 
    
  - **Microsoft.Office.Project.PWA** esse namespace inclui um proxy interno para a PSI, para uso com o Project Web App e atividades de fluxo de trabalho personalizado; não está documentado. 
    
    Uma atividade de fluxo de trabalho personalizado requer uma referência à **Microsoft.Office.Project.PWA** para acessar todas as classes nos serviços de PSI. Por exemplo, a classe de **Microsoft.Office.Project.PWA.PSI** inclui a propriedade **ProjectWebService** , que obtém um proxy para o namespace [WebSvcProject](https://msdn.microsoft.com/library/WebSvcProject.aspx) . 
    
  - **Microsoft.Office.Project.Server.WebServiceProxy** este namespace inclui as classes de proxy interno para a classe principal em cada serviço PSI. Usando as permissões elevadas do usuário de fluxo de trabalho, o fluxo de trabalho pode chamar métodos PSI por meio de classes de proxy. As classes de proxy não estão documentadas. 
    
- **Microsoft.Office.Project.Server.Events.Receivers.dll** [Microsoft.Office.Project.Server.Events](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.aspx) é o namespace somente nesse assembly. Ela inclui o receptor de evento e classes de argumento de evento para os serviços PSI e outras classes internos. 
    
  Os desenvolvedores escrever manipuladores de eventos que derivam de classes do receptor de evento. A maioria das classes primárias nos serviços de PSI tem uma classe de receptor de evento correspondente. Por exemplo, a classe **ProjectEventReceiver** contém os métodos pré-evento e pós-evento receptor que correspondem aos métodos na classe **Project** na PSI. O método **OnCreating** e o método **OnCreated** são os métodos de pré-evento e pós-evento receptor para o método **QueueCreateProject** . 
    
  Os desenvolvedores geralmente usam as seguintes classes do receptor de evento:
  <br/>  
  - [AdminEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.AdminEventReceiver.aspx)
  - [CalendarEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.CalendarEventReceiver.aspx)
  - [CubeAdminEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.CubeAdminEventReceiver.aspx)
  - [CustomFieldsEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.CustomFieldsEventReceiver.aspx)
  - [LookupTableEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.LookupTableEventReceiver.aspx)
  - [ProjectEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.ProjectEventReceiver.aspx)
  - [OptimizerEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.OptimizerEventReceiver.aspx)
  - [ReportingEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.ReportingEventReceiver.aspx)
  - [ResourceEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.ResourceEventReceiver.aspx)
  - [SecurityEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.SecurityEventReceiver.aspx)
  - [StatusingEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.StatusingEventReceiver.aspx)
  - [TimesheetEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.TimesheetEventReceiver.aspx)
  - [UserDelegationEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.UserDelegationEventReceiver.aspx)
  - [WorkflowEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.WorkflowEventReceiver.aspx)
  - [WssInteropEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.WssInteropEventReceiver.aspx)
    
  A classe **RulesEventReceiver** e a classe de **StatusReportsEventReceiver** são usados internamente no Project Web App. 
    
- **Microsoft.ProjectServer.Client.dll** desse assembly contém o CSOM para desenvolvimento com o .NET Framework 4. O assembly está localizado em `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\ISAPI\Microsoft.ProjectServer.Client.dll`. Desenvolvimento de aplicativos com o namespace **Microsoft.ProjectServer.Client** é independente do local APIs do Project Server e serviços, embora os aplicativos podem trabalhar com qualquer um um local ou online instalação do Project Server. Para assemblies CSOM relacionados que podem ser usados para o Windows Phone 8, o Microsoft Silverlight ou JavaScript com aplicativos da web, consulte [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) . 
    
- **Microsoft.Office.Project.Server.Schema.dll** o SDK do Project 2013 não documenta o namespace **Microsoft.Office.Project.Server.Schema** , que está no `[Windows]\Microsoft.NET\assembly\GAC_MSIL\Microsoft.Office.Project.Schema\v4.0_15.0.0.0__71e9bce111e9429c\Microsoft.Office.Project.Schema.dll` assembly. O namespace contém as definições de todas as classes **DataSet**, **DataTable**e **DataRow** usadas na PSI, além de muitas outras classes semelhantes que usa o Project Server internamente. As classes públicas em cada serviço PSI são documentadas na referência do serviço específico. Por exemplo, a classe **DriverDataSet.DriverRow** está documentada no namespace [WebSvcDriver](https://msdn.microsoft.com/library/WebSvcDriver.aspx) . 
    
  > [!NOTE]
  > Aplicativos que usam o CSOM, usam manipuladores de evento remoto ou acessar o Project Online não use o namespace **Microsoft.Office.Project.Server.Schema** . 
  
  Em alguns aplicativos que usam os manipuladores de eventos de confiança total, onde os manipuladores de eventos estão instalados no computador do Project Server, é necessário definir uma referência para o assembly Microsoft.Office.Project.Schema.dll. A seguir estão dois exemplos:
    
  - Em um manipulador de pós-evento **OnCreated** de confiança total para campos personalizados, você pode usar o argumento de evento **e.CustomFieldInformation** com uma referência ao namespace **Microsoft.Office.Project.Server.Schema** para o **CustomFieldDataSet **e definições de **CustomFieldsRow** . 
   
     ```cs
        using PSLibrary = Microsoft.Office.Project.Server.Library;
        using Microsoft.Office.Project.Server.Schema;
        . . .
        // Event handler for the OnCreated event of a custom field.
        public override void OnCreated(
            PSLibrary.PSContextInfo contextInfo, 
            CustomFieldsPostEventArgs e)
        {
            // Get information from the event arguments. 
            string userName = contextInfo.UserName.ToString();
            CustomFieldDataSet customFieldDs = e.CustomFieldInformation;
            CustomFieldsRow customFieldRow = customFieldDs.CustomFields.Rows[0];
            string customFieldName = customFieldRow["MD_PROP_NAME"].ToString();
            byte customFieldType = (byte)customFieldRow["MD_PROP_TYPE_ENUM"];
            Guid customFieldUid = (Guid)customFieldRow["MD_PROP_UID"];
            . . .
        }
     ```

  - Uma atividade de fluxo de trabalho personalizado pode exigir uma referência ao **Microsoft.Office.Project.Server.Schema** para definições do **conjunto de dados** . 
    
## <a name="psi-services"></a>Serviços PSI
<a name="pj15_PSIRefOverview_PSI"> </a>

A PSI é um conjunto de serviços do WCF e idênticos ASMX web services para o Project Server 2013. Para usar um serviço em um projeto do Visual Studio, você definir uma referência para a URL do `.svc` arquivo ou o `.asmx?wsdl` service usando um nome arbitrário para o nameservice. O utilitário de wsdl.exe ou o svcutil.exe, em seguida, gera o código-fonte proxy daquele namespace e o compilador cria um assembly de serviço de proxy para incluir em seu aplicativo. 
  
> [!NOTE]
> A referência PSI inclui os nomes de nameservice de espaço reservado para os serviços PSI como _[serviço da web Admin]_, _[serviço web de Driver]_ e _[serviço web do projeto]_. Cada nameservice PSI inclui uma classe principal que contém os métodos web para o serviço. Por exemplo, se você definir uma referência para o serviço de **Administração** e nomeie-o **WebSvcAdmin**, em seguida, em seu aplicativo o **WebSvcAdmin** nameservice inclui a classe **Admin** principal que tem os métodos web **GetServerCurrency**, **ListInstalledLanguages**, **ReadServerVersion**e assim por diante. Consulte [atualizações para desenvolvedores no Project 2013](updates-for-developers-in-project-2013.md) para obter uma lista dos serviços PSI preteridos. 
  
Os serviços de PSI total 30, **autenticação**, **ExchangeSync**, **OData**, **P12Upgrade**, **psiserviceapp**, **PWA**, **modo de exibição**e **WinProj** são para uso interno pelo Project Web App e do Project Professional e são não documentado. Embora você possa criar arquivos de proxy ou um assembly de proxy que inclui os serviços internos da PSI, os serviços internos não estão para uso de terceiros; a referência PSI não documenta esses serviços. A figura a seguir mostra o local dos serviços PSI do back-end em Gerenciador de serviços de informações da Internet. 
  
**Localizar os serviços PSI no IIS**

![Serviços PSI no Gerenciador do IIS] (media/pj15_PSIReference_IIS.gif "Serviços PSI no Gerenciador do IIS")
  
A seguir estão todas as classes que contêm os métodos web nos serviços de PSI:
  
1. [Admin](https://msdn.microsoft.com/library/WebSvcAdmin.Admin.aspx) Inclui os métodos que são usados nas páginas de **Administração do Project Server** no Project Web App. Define anos fiscais, gerencia as configurações de status e moeda, relatórios de períodos, o log de auditoria e configurações do Active Directory. 
    
2. [Arquivo morto](https://msdn.microsoft.com/library/WebSvcArchive.Archive.aspx) Inclui os métodos de gerenciamento de backup e restauração de projetos, categorias de segurança, campos personalizados, recursos, configurações do sistema, exibições e projeto global da empresa. Lê e atualiza o agendamento de arquivo morto. Arquiva todos os projetos ou exclui projetos arquivados especificados. Salva os objetos de backup para as tabelas de banco de dados de arquivamento e restaura o backup objetos nas tabelas de banco de dados publicado. 
    
3. **autenticação** Inclui métodos para uso interno apenas pelo Project Professional e do Project Web App. 
    
4. [Calendário](https://msdn.microsoft.com/library/WebSvcCalendar.Calendar.aspx) Gerencia as exceções de calendário da empresa. Faz check-out e faz check-in de calendários de recursos. Cria, exclui, lista todos os, atualiza ou retorna exceções de calendário. 
    
5. [CubeAdmin](https://msdn.microsoft.com/library/WebSvcCubeAdmin.CubeAdmin.aspx) Gerencia as configurações de cubo OLAP. Obtém a lista de cubos, status do banco de dados e servidor de análise. Coloca uma solicitação de Cube Build Service na fila. Lê e atualiza as configurações de campo para dimensões e medidas no cubo e definições de membro calculado. 
    
6. [CustomFields](https://msdn.microsoft.com/library/WebSvcCustomFields.CustomFields.aspx) Gerencia os campos personalizados da empresa. Inclui o check-out e check-in métodos e a criar, ler, atualização e métodos delete (CRUD) para campos personalizados da empresa. 
    
7. [Driver](https://msdn.microsoft.com/library/WebSvcDriver.Driver.aspx) Gerencia drivers de análise de portfólio e priorização de fatores para criação do projeto e o gerenciamento de propostas. Inclui os métodos CRUD para drivers de projeto. 
    
8. [Eventos](https://msdn.microsoft.com/library/WebSvcEvents.Events.aspx) Gerencia as associações de manipulador de evento do Project Server. Inclui os métodos CRUD para as associações de manipulador de eventos do Project Server para um evento específico, ou para todas as associações de manipulador de eventos. 
    
9. **ExchangeSync** Este é um serviço interno do Project Server que trata os eventos do Exchange Server. Project Web App usa **ExchangeSync** para sincronizar atribuições entre o Project Server e o Exchange Server, em vez de sincronização direta com o cliente do Outlook, como no Office Project Server 2007. 
    
    Acesso ao serviço de **ExchangeSync** está disponível somente através da URL de **ProjectServiceApplication** . As classes **ExchangeSync** e membros não são suportados para o desenvolvimento de terceiros. 
    
10. [LoginForms](https://msdn.microsoft.com/library/WebSvcLoginForms.LoginForms.aspx) Fornece os métodos de **logon** e o **Logoff** com autenticação baseada em formulários. Acesso ao serviço de **LoginForms** está disponível somente em um site do Project Web App front-end. 
    
11. [LoginWindows](https://msdn.microsoft.com/library/WebSvcLoginWindows.LoginWindows.aspx) Fornece os métodos de **logon** e o **Logoff** que são usados para autenticação do Windows com aplicativos baseados em ASMX para autenticação de vários (declarações e baseada em formulários) instalações do Project Server 2013. Acesso ao serviço de **LoginWindows** está disponível somente em um site do Project Web App front-end. 
    
    > [!CAUTION]
    > O serviço de **LoginWindows** não é usado em aplicativos baseados em WCF, ou para aplicativos que são executados em instalações do Project Server que usam apenas a autenticação de declarações ou **OAuth**; Nesses casos, o método **Login** sempre retorna **false**. Autenticação de declarações lida com a autenticação integrada do Windows. 
  
12. [LookupTable](https://msdn.microsoft.com/library/WebSvcLookupTable.LookupTable.aspx) Gerencia as tabelas de pesquisa, tabelas de pesquisa multilíngues e suas máscaras de código correspondente. Faz check-out, faz check-in, lê, cria, exclui e atualizações. 
    
13. [Notificações](https://msdn.microsoft.com/library/WebSvcNotifications.Notifications.aspx) Gerencia alertas e lembretes. Inclui métodos que obtém, definir, registrar e cancelar o registro de resultados de alerta. 
    
14. [ObjectLinkProvider](https://msdn.microsoft.com/library/WebSvcObjectLinkProvider.ObjectLinkProvider.aspx) Gerencia objetos da web e links para documentos e itens de lista em sites do SharePoint. Cria, exclui ou lê o projeto, vinculados ao projeto, tarefa ou objetos web tarefa vinculada. 
    
    > [!NOTE]
    > O serviço de **ObjectLinkProvider** foi preterido no Project Server 2013. Para obter mais informações, consulte a seção de *recursos obsoleto* no [atualizações para os desenvolvedores no Project 2013](updates-for-developers-in-project-2013.md). 
  
15. **OData** Fornece a interface interna do **OData** para as tabelas e modos de exibição de relatórios. Acesso ao serviço **OData** está disponível somente através da URL de **ProjectServiceApplication** de back-end. O serviço **OData** privado na PSI fornece um método, **ODataClient.ProcessOdataMessage**, que usa o Project Server internamente para processar solicitações de relatórios de dados. As solicitações HTTP passam o serviço **ProjectData** front-end. 
    
    Para obter informações sobre o serviço **ProjectData** e o protocolo OData para ler dados de relatórios, consulte [ProjectData - Referência de serviço OData do projeto](https://msdn.microsoft.com/en-us/library/office/jj163015.aspx).
    
16. **P12Upgrade** Fornece métodos internos para o instalador do Project Server 2013 atualizar uma instalação do Office Project Server 2007. Acesso ao serviço de **P12Upgrade** está disponível somente através da URL de **ProjectServiceApplication** . Os métodos **P12Upgrade** não são suportados para o desenvolvimento de terceiros. 
    
17. [PortfolioAnalyses](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.aspx) Inclui os métodos CRUD para dependências do projeto e para soluções otimizador, planejador e análise. 
    
18. [Project](https://msdn.microsoft.com/library/WebSvcProject.Project.aspx) Gerencia a projetos. Faz check-out, faz check-in, cria, exclui, lê ou atualiza projetos nas tabelas de rascunho de banco de dados de Project ou tabelas publicadas. Coloca uma mensagem na fila para publicação. 
    
    Cria ou exclui entidades dentro de projetos (tarefas, recursos, atribuições e assim por diante). Obtém informações sobre ou atualiza a equipe de projeto ou o endereço do site de projeto. Obtém o status do projeto, uma lista de projetos em todos os projetos, tarefas que estão disponíveis para atribuição de um recurso especificado, todas as tarefas de resumo ou as tabelas de rascunho onde um recurso tem atribuições.
    
    Cria e gerencia os compromissos, cria propostas de projeto e projetos de listas de tarefas do SharePoint e localiza relacionamentos do projeto mestre do projeto.
    
19. **psiserviceapp** Usada internamente pelo Project Online. As classes **psiserviceapp** e membros não são suportados para o desenvolvimento de terceiros. 
    
20. **PWA** Contém muitos métodos otimizados para o Project Web App, incluindo os métodos para regras de aprovação de atualização de tarefa e gerenciar relatórios de status. Os métodos de **PWA** frequentemente são especializados e comparado relativamente redundantes métodos equivalente da outros serviços PSI. Métodos de **PWA** usam ou retornam muitos dos mesmos conjuntos de dados como os outros métodos PSI. 
    
    Acesso ao serviço de **PWA** está disponível somente através da URL de **ProjectServiceApplication** . As classes do **PWA** e membros não são suportados para o desenvolvimento de terceiros. 
    
21. [QueueSystem](https://msdn.microsoft.com/library/WebSvcQueueSystem.QueueSystem.aspx) Gerencia a fila do Project Server. Obtém a contagem de trabalhos, o trabalho e o tempo de espera do grupo de trabalho, o status de todos os trabalhos, trabalhos especificados, trabalhos que pertence ao chamador ou trabalhos para projetos especificados. Gerencia correlação de trabalho e configura a fila. 
    
22. [Recurso](https://msdn.microsoft.com/library/WebSvcResource.Resource.aspx) Gerencia os recursos da empresa. Faz check-out, faz check-in, atualiza ou cria recursos ou usuários do Project Server e suas configurações de autorização; Localiza recursos por nome ou GUID; lê o recurso ou dados do usuário e a estrutura de divisão de recursos (EDR) e informações relacionadas à segurança; obtém todas as atribuições para um recurso; e redefine as senhas de usuário. A classe de **recurso** inclui métodos CRUD para representações de usuário. 
    
23. [ResourcePlan](https://msdn.microsoft.com/library/WebSvcResourcePlan.ResourcePlan.aspx) Gerencia planos de recurso. Faz check-out, faz check-in, publica e inclui os métodos CRUD para planos de recurso. 
    
24. [Segurança](https://msdn.microsoft.com/library/WebSvcSecurity.Security.aspx) Inclui os métodos de CRUD para modelos de segurança, categorias de segurança, as permissões globais e organizacionais e permissões de grupo. A classe de **segurança** inclui métodos para categorias de projeto. 
    
25. [Status](https://msdn.microsoft.com/library/WebSvcStatusing.Statusing.aspx) Gerencia as atualizações de status e atribuições. Aplica atualizações de status ou aprovações, envia o status atualiza, define informações de resumo para atualizações enviadas, exclui o histórico de aprovação para um usuário específico ou atualizações de status de aprovado ou exclui todas as informações de status para um conjunto de projetos. Cria, obtém ou delega atribuições; Define a duração do trabalho de atribuição. Obtém as novas atribuições para o usuário atual; Obtém o histórico de transação de atribuição ou tarefa, os dados efetivos de divisão em fases ou a hierarquia de tarefa de resumo. 
    
    Permite a visualização ou importa dados do quadro de horários ou lê o trabalho de um usuário e a agenda de folga. Localiza pendentes atualizações de status, informações para atualizações enviadas ou um registro de transação das alterações em uma atualização enviada. Status da equipe de leituras.
    
26. [Quadro de horários](https://msdn.microsoft.com/library/WebSvcTimeSheet.TimeSheet.aspx) Gerencia os quadros de horários. Inclui os métodos de CRUD para quadros de horários e envia ou repete os quadros de horários. Localiza quadros de horários são atrasado ou aguardando aprovação; Localiza quadros de horários por data ou período. Obtém a lista de aprovadores de quadro de horários. Pré-carrega dados efetivos de quadro de horários e valida uma linha de quadro de horários. A classe de **quadro de horários** que inclui o método **ReadProjectTimesheetLines** e o método **SubmitTimesheetLines** para leitura e enviando quadros de horários para outro recurso sem exigir a representação. 
    
27. **Modo de exibição** O serviço de **exibição** foi projetado para uso somente no Project Web App. Métodos da classe do **modo de exibição** gerenciar modos de exibição e exibir relatórios e campos nos modos de exibição de leitura. 
    
    Acesso ao serviço de **exibição** está disponível somente através da URL de **ProjectServiceApplication** . Os métodos de **modo de exibição** não são suportados para o desenvolvimento de terceiros. 
    
28. **WinProj** O serviço do **WinProj** foi projetado para ser usado apenas pelo Project Professional. Desenvolvedores de terceiros não devem usar os métodos **WinProj** para programação com o Project Server. 
    
    Alguns métodos **WinProj** usam conjuntos de dados, como **ProjectRelationsDataSet** e **ResourceDataSet** que os serviços de **recursos** e **projetos** também usam, mas exigem propriedades específicas e funções no Project Professional. 
    
    Acesso ao serviço **WinProj** está disponível somente através da URL de **ProjectServiceApplication** . Não há suporte para os métodos **WinProj** para desenvolvimento de terceiros. 
    
29. [Fluxo de trabalho](https://msdn.microsoft.com/library/WebSvcWorkflow.Workflow.aspx) Inclui os métodos CRUD para tipos de projeto corporativo e gerenciar etapas e fases do fluxo de trabalho. Executa os fluxos de trabalho, define informações de status e gerencia os estágios de página (PDP) de detalhes do projeto em fluxos de trabalho de gerenciamento de demanda. Para desenvolver fluxos de trabalho do Project Server, os desenvolvedores podem usar o SharePoint Designer 2013 para fluxos de trabalho declarativos ou usar as ferramentas de desenvolvedor do Office para Visual Studio 2012 para o desenvolvimento com o .NET Framework 4 e a [ Microsoft.ProjectServer.Client.WorkflowActivities](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.WorkflowActivities.aspx) classe o CSOM. 
    
30. [WssInterop](https://msdn.microsoft.com/library/WebSvcWssInterop.WssInterop.aspx) Gerencia os sites de projeto. Cria e exclui sites de projetos. Obtém informações sobre e atualiza as definições do SharePoint e sites de administração. Sincroniza e atualiza as associações de site de projeto e os grupos. 
    
O namespace de cada serviço inclui todas as classes de manipulador com **DataSet** esquema e o evento que usa o serviço. Por exemplo, `Calendar.svc` (ou `Calendar.asmx?wsdl` para o ASMX serviço web) descreve o serviço de **calendário** . Se você nomear a referência **WebSvcCalendar**, o namespace de proxy contém principal **calendário** classe com os métodos **CheckInCalendars**, **CheckOutCalendars**e assim por diante. O namespace do proxy **WebSvcCalendar** também inclui a classe de **CalendarDataSet** e todas as suas subclasses. 
  
Alguns dos serviços PSI contêm duplicados classes de **conjunto de dados** . Por exemplo, o serviço de **projeto** e o serviço de **status** ambos incluem a classe **ProjectDataSet** . Isso ocorre porque os métodos no serviço **Project** e o serviço de **status** incluem referências para o **ProjectDataSet**e os assemblies de proxy que você cria quando você definir referências e compila um aplicativo incluem o relacionados conjuntos de dados. O serviço do **Project** e o serviço de **status** podem exigir valores para campos diferentes na classe **ProjectDataSet.ProjectRow** . 
  
Quando você está navegando namespaces e classes de referência do PSI, por exemplo, consulte os métodos web para o serviço de **projeto** , expanda o namespace **[serviço web do Project]** na lista de **conteúdo** e, em seguida, expanda o **projeto** classe. 
  
## <a name="see-also"></a>Confira também

- [Arquitetura do Project Server 2013](project-server-2013-architecture.md)
- [Programabilidade do Project Server](project-server-programmability.md)   
- [O que o PSI faz e não faz](what-the-psi-does-and-does-not-do.md)   
- [Pré-requisitos para amostras de código com base em ASMX no projeto](prerequisites-for-asmx-based-code-samples-in-project.md)   
- [Pré-requisitos para amostras de código com base em WCF no projeto](prerequisites-for-wcf-based-code-samples-in-project.md)   
- [Centro do desenvolvedor do .NET framework](http://msdn.microsoft.com/en-us/netframework/aa496123.aspx)
    

