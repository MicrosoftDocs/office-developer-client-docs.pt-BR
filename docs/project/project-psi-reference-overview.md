---
title: Visão geral da referência da PSI do Project
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
- serviço web,serviços web,calendário,autenticação,serviço Web,serviços Web,ResourcePlan,Web service,StatusReports,web service,PSI, namespaces,manipuladores de eventos, Project Server,manipulador de eventos,notificações,QueueSystem,Project 2013, plataforma,LoginWindows,status,recurso,recursos,WinProj,WssInterop,LookupTable,PWA,segurança,TimeSheet,eventos,programação,versão,versões,CustomFields,ResourcePlan,regra,regras,referência de código gerenciado,URL,para a PSI,administrador,administração,admin,CubeAdmin,exibir,LoginForms,URLs,ObjectLinkProvider,arquivo morto,evento,projeto,projetos,Project,Project Server Interface,interface do servidor do projeto,interface do Project Server,métodos Web
localization_priority: Normal
ms.assetid: d3c33089-0cbe-48c3-bfc0-0be819ca4d73
description: A Interface do Project Server (PSI) é a API usada para desenvolver aplicativos que se integram ao Project Server 2013 no local.
ms.openlocfilehash: 58235e16afd208d0d4415e28ad200cc7ff62ac8b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390118"
---
# <a name="project-psi-reference-overview"></a>Visão geral da referência da PSI do Project

A Interface do Project Server (PSI) é a API usada para desenvolver aplicativos que se integram ao Project Server 2013 no local.
  
Este artigo é uma visão geral dos assemblies, namespaces e serviços documentados na PSI. A [Referência do serviço Web e da biblioteca de classe do Project Server 2013](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) no SDK contém toda a documentação de código gerenciado para a PSI e o namespace [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) no Project Server 2013. Para desenvolver aplicativos para o Project Online, você deve usar o namespace **Microsoft.ProjectServer.Client** ao invés da PSI. 

A PSI no Project Server 2013 tem uma interface dupla. A interface ASMX para serviços Web é definida por arquivos de descoberta e linguagem WSDL (disco e WSDL) no diretório virtual `https://ServerName/ProjectServerName/_vti_bin/psi/` (por exemplo, Projectdisco.aspx e Projectwsdl.aspx). Você pode acessar a interface ASMX apenas pela URL de uma instalação local do Project Web App (por exemplo, `https://ServerName/ProjectServerName/_vti_bin/psi/project.asmx?wsdl)`. Para mostrar o serviço Web em um navegador, você deve incluir a opção de URL `?wsdl`. Como a interface ASMX foi criada usando a infraestrutura do Windows Communication Foundation (WCF), os arquivos .asmx para os serviços Web do Project Server não existem de fato no diretório virtual da PSI. 
  
A interface de serviços do WCF é definida por arquivos .svc no diretório virtual `https://ServerName:32843/GUID/PSI/` do back-end no aplicativo de serviços Web do SharePoint. A URL dos serviços da PSI no diretório virtual do aplicativo de serviço do Project (por exemplo, `https://ServerName:32843/GUID/PSI/project.svc`) inclui os arquivos .svc. Porém, não é possível usar diretamente a URL de back-end para definir uma referência ao serviço do WCF. Para desenvolver um aplicativo ou componente que usa os serviços do WCF da PSI, você pode usar um assembly de proxy ou um arquivo de proxy. O download do SDK do Project 2013 inclui arquivos de proxy para os serviços do WCF no Project Server 2013 e os scripts para acessar arquivos de proxy do WCF atualizados e compilar os arquivos em um assembly de proxy para as builds mais recentes do Project Server.
  
O nome de diretório do aplicativo de serviço do Project é um valor GUID, que é o mesmo GUID da instância do Project Web App local. Na janela **Gerenciador dos Serviços de Informações da Internet (IIS)**, expanda o nó **Serviços Web do SharePoint**, escolha o nome do diretório GUID e escolha **Configurações Avançadas** para copiar o valor de **Caminho Virtual**. 
  
> [!IMPORTANT]
> A interface de serviço Web ASMX da PSI foi preterida no Project Server 2013, mas ainda é compatível. Novos aplicativos devem usar a interface WCF da PSI ou CSOM. Para saber mais sobre recursos preteridos, consulte [Atualizações para desenvolvedores no Project 2013](updates-for-developers-in-project-2013.md)
> 
> Novos aplicativos e componentes middleware que são executados apenas em uma instalação local do Project Server devem usar a interface do WCF, que é a tecnologia recomendável para comunicações de rede. Os aplicativos herdados que usam a interface ASMX devem usar a URL pelo Project Web App, que verifica as permissões do Project Server. 
> 
> Para saber mais sobre a interface ASMX e como usar a interface do WCF, consulte [Pré-requisitos para exemplos de código baseados em ASMX no Project](prerequisites-for-asmx-based-code-samples-in-project.md) e [Pré-requisitos para exemplos de código baseados em WCF no Project](prerequisites-for-wcf-based-code-samples-in-project.md). 
  
Para desenvolver aplicativos que usam a interface do WCF, você pode usar o Visual Studio 2010 ou Visual Studio 2012. Para criar fluxos de trabalho declarativos do Project Server, você pode usar o SharePoint Designer 2013. Os fluxos de trabalho do Project Server que exigem acesso à PSI ou ao CSOM podem ser desenvolvidos com o Visual Studio 2012.
  
### <a name="using-the-psi-reference"></a>Usar a referência da PSI
<a name="pj15_PSIRefOverview_Using"> </a>

O modelo de objeto da PSI é grande e várias classes e membros são somente para uso interno. Como resultado, pode ser confuso encontrar os tópicos que você deseja na [Referência do serviço Web e da biblioteca de classes do Project Server 2013](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx). A maioria dos tópicos de referência que você usará para desenvolvimento está nos seguintes grupos:
  
- **Métodos de classe primária**: cada serviço na PSI inclui uma classe primária que tem o nome do serviço. Por exemplo, o serviço **Resource** contém a classe [Resource](https://msdn.microsoft.com/library/WebSvcResource.Resource.aspx), que está no namespace [WebSvcResource](https://msdn.microsoft.com/library/WebSvcResource.aspx). Para ver uma lista dos métodos disponíveis na classe **Resource**, expanda o nó de classe no painel de conteúdo e, em seguida, escolha o tópico **Métodos de Resource**. 
    
- **Propriedades DataRow:** Muitos dos métodos de classe primária usam ou retornam um **DataSet**. Cada objeto **DataTable** em um **DataSet** contém dados em um ou mais objetos **DataRow**. Na maioria dos casos você precisa ver apenas as propriedades de linha, não todos os outros membros das classes **DataSet**, **DataTable** ou **DataRow**. Por exemplo, a classe **ResourceAssignmentDataSet** inclui subclasses para as classes **ResourceAssignmentDataTable** e [ResourceAssignmentDataSet.ResourceAssignmentRow](https://msdn.microsoft.com/library/WebSvcResource.ResourceAssignmentDataSet.ResourceAssignmentRow.aspx). Para ver uma lista das propriedades que estão na classe **ResourceAssignmentRow**, expanda o nó da classe no painel de conteúdo e, em seguida, escolha o tópico **Propriedades de ResourceAssignmentDataSet.ResourceAssignmentRow**. 
    
Além dos namespaces de serviço, o tópico [Referência do serviço Web e da biblioteca de classes do Project Server 2013](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) fornece links para os três assemblies do Project Server usados no desenvolvimento de soluções de terceiros para instalações locais. Fornecemos apenas a documentação mínima para esses assemblies. A referência da PSI documenta as classes e os membros principais nos 23 serviços públicos. Seis serviços da PSI destinam-se apenas para uso interno e não estão documentados. 
  
> [!NOTE]
> As classes no modelo de objeto do lado do cliente (CSOM) podem ser usadas independentemente de outros assemblies e serviços do Project Server. Você pode usar o namespace **Microsoft.ProjectServer.Client** em um ambiente de desenvolvimento remoto no computador do Project Server e desenvolver aplicativos que se integram ao Project Online ou a uma instalação local do Project Server. Mas o CSOM contém um subconjunto de recursos da PSI completa. O CSOM permite o desenvolvimento dos cenários mais comuns para integração com o Project Server. Para saber mais, consulte [O que o CSOM faz e não faz](what-the-csom-does-and-does-not-do.md) e [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx). 
  
Para o desenvolvimento da maioria dos aplicativos que usa a PSI, você não precisa desenvolver em um computador do Project Server ou definir as referências a conjuntos do Project Server no cache de assembly global. Você pode copiar os assemblies necessários do Project Server para seu computador de desenvolvimento. O Project Server 2013 instala os seguintes assemblies em _[Arquivos de Programa]_ `\Microsoft Office Servers\15.0\Bin`: 
  
- Microsoft.Office.Project.Server.Events.Receivers.dll 
- Microsoft.Office.Project.Server.Library.dll
- Microsoft.Office.Project.Server.Workflow.dll
    
Os namespaces para os serviços da PSI têm nomes arbitrários criados para um assembly de proxy da PSI, ProjectServerServices.dll, que é gerado para fins de documentação. Na referência da PSI, o namespace de cada serviço tem um nome de espaço reservado (como _[serviço Web do Project]_) e uma referência Web (como `https://ServerName/ProjectServerName/_vti_bin/psi/Project.asmx?wsdl`). 
  
## <a name="project-server-assemblies-and-namespaces"></a>Namespaces e assemblies do Project Server
<a name="pj15_PSIRefOverview_Assemblies"> </a>

Muitos assemblies são instalados junto com o Project Server; apenas quatro assemblies do Project Server são documentados. Os desenvolvedores terceirizados geralmente usam apenas algumas classes e membros nesses assemblies. Os assemblies não-documentados do Project Server incluem namespaces e classes que o Project Server usa internamente, como classes para o Project Web App, entidades comerciais e a camada de acesso a dados (DAL). Quando você define uma referência no Visual Studio para um dos assemblies documentados do Project Server, pode ver todos os namespaces, as classes e os membros no Pesquisador de Objetos do Visual Studio.
  
> [!NOTE]
> Vários membros dos namespaces documentados do Project Server são usados apenas internamente e têm uma quantidade mínima de documentação. 
  
Ao desenvolver para o Project Online, você pode usar somente o CSOM para acessar a funcionalidade do Project Server. Você não tem acesso aos serviços da PSI ou outros assemblies do Project Server.
  
A [Referência do serviço Web e da biblioteca de classe do Project Server 2013](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) para a PSI inclui os seguintes namespaces de assemblies: 
  
- **Microsoft.Office.Project.Server.Library.dll** Este assembly contém um namespace documentado e três namespaces não-documentados, da seguinte maneira: 
    
  - O namespace [Microsoft.Office.Project.Server.Library](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.aspx) inclui muitas enumerações, campos de classe e propriedades que são usados em aplicativos locais para o Project Server. Por exemplo, os desenvolvedores normalmente usam enumerações como **CustomField.Type**, e as classes **PSClientError**, **PSErrorInfo** e **Filter**. 
    
    O namespace **Microsoft.Office.Project.Server.Library** também inclui as seguintes sete classes de propriedade que incluem mais de 3.200 subclasses: 
    
      - **AssignmentProperties**  
      - **CalendarProperties**
      - **ConstraintProperties**
      - **LookupTableProperties**
      - **ProjectProperties**
      - **ResourceProperties**
      - **TaskProperties**
    
    As classes de propriedades são usadas internamente e não estão documentadas. As classes de propriedades são usadas para serialização entre o Project Professional 2013 e o Project Server. Quando você trabalha com o namespace **Microsoft.Office.Project.Server.Library** no Visual Studio, o Pesquisador de Objetos mostra todas as classes de propriedade, o que dificulta encontrar as classes que são úteis para desenvolvimento de terceiros. Como os desenvolvedores de terceiros não têm que usar as classes de propriedades, o SDK não os documenta. 
    
  - **Microsoft.Office.Project.Server.DataServices** As classes e os membros desse namespace são usados internamente pelo serviço **OData** no Project Online para acessar as tabelas de relatórios no banco de dados do Project. As classes **DataServices** não estão documentadas. 
    
  - **Microsoft.Office.Project.Server.Administration** A classe e os membros desse namespace são usados internamente para log de diagnóstico e não estão documentados. 
    
  - **Microsoft.Office.Project.Server.Base** As classes e os membros desse namespace são usados internamente como classes base e não são documentados. 
    
  - **Microsoft.Office.Project.Server.Library.FilterSchema** Esse namespace é usado internamente para gerar esquemas de filtro e não é documentado. 
    
- **Microsoft.Office.Project.Server.Workflow.dll** Este assembly é usado para fluxos de trabalho herdados do Project Server 2010 que ainda funcionam no Project Server 2013. Para criar novos fluxos de trabalho, você deve usar o SharePoint Designer 2013 ou o Visual Studio 2012 com a classe [Microsoft.ProjectServer.Client.WorkflowActivities](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.WorkflowActivities.aspx). O assembly Microsoft.Office.Project.Server.Workflow.dll inclui os três namespaces a seguir: 
    
  - [Microsoft.Office.Project.Server.Workflow](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Workflow.aspx) Este namespace inclui classes que são usadas para atividades de fluxo de trabalho do Project Server. As atividades incluem leitura, comparação e atualização das propriedades do projeto. Outras classes gerenciam fluxos de trabalho e incluem retornos de chamadas de fluxo de trabalho quando os projetos são alterados. 
    
  - **Microsoft.Office.Project.PWA** Este namespace inclui um proxy interno para a PSI, para ser usado com o Project Web App e atividades de fluxo de trabalho personalizadas; não está documentado. 
    
    Uma atividade de fluxo de trabalho personalizado exige uma referência a **Microsoft.Office.Project.PWA** para acessar todas as classes de serviços da PSI. Por exemplo, a classe **Microsoft.Office.Project.PWA.PSI** inclui a propriedade **ProjectWebService**, que recebe um proxy para o namespace [WebSvcProject](https://msdn.microsoft.com/library/WebSvcProject.aspx). 
    
  - **Microsoft.Office.Project.Server.WebServiceProxy** Esse namespace inclui classes internas de proxy para a classe primária em cada serviço da PSI. Ao usar as permissões elevadas do usuário de fluxo de trabalho, o fluxo de trabalho pode chamar métodos da PSI por meio de classes de proxy. As classes de proxy não são documentadas. 
    
- **Microsoft.Office.Project.Server.Events.Receivers.dll**[Microsoft.Office.Project.Server.Events](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.aspx) é o único namespace neste assembly. Ele inclui as classes de argumentos de evento e de receptor de evento para os serviços da PSI e outras classes internas. 
    
  Os desenvolvedores escrevem manipuladores de eventos que derivam de classes de receptores de eventos. A maioria das classes primárias nos serviços da PSI tem uma classe de receptor de evento correspondente. Por exemplo, a classe **ProjectEventReceiver** contém métodos de receptor antes do evento e após o evento que correspondem a métodos na classe **Project** na PSI. Os métodos **OnCreating** e **OnCreated** são os métodos receptores antes do evento e após o evento para o método **QueueCreateProject**. 
    
  Normalmente, os desenvolvedores usam as seguintes classes de receptores de eventos:
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
    
  As classes **RulesEventReceiver** e **StatusReportsEventReceiver** são usadas internamente no Project Web App. 
    
- **Microsoft.ProjectServer.Client.dll** Este assembly contém o CSOM para desenvolvimento com .NET Framework 4. O assembly está localizado em `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\ISAPI\Microsoft.ProjectServer.Client.dll`. O desenvolvimento de aplicativos com o namespace **Microsoft.ProjectServer.Client** é independente das APIs e dos serviços do Project Server locais, embora os aplicativos possam funcionar em instalações locais ou online do Project Server. Para assemblies CSOM relacionados que podem ser usados para Windows Phone 8, Microsoft Silverlight ou JavaScript com aplicativos Web, consulte [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx). 
    
- **Microsoft.Office.Project.Server.Schema.dll** O SDK do Project 2013 não documenta o namespace **Microsoft.Office.Project.Server.Schema** que está no assembly `[Windows]\Microsoft.NET\assembly\GAC_MSIL\Microsoft.Office.Project.Schema\v4.0_15.0.0.0__71e9bce111e9429c\Microsoft.Office.Project.Schema.dll`. O namespace contém as definições de todas as classes **DataSet**, **DataTable** e **DataRow** usadas na PSI e muitas outras classes semelhantes que o Project Server usa internamente. As classes públicas em cada serviço da PSI são documentadas na referência de serviços específicos. Por exemplo, a classe **DriverDataSet.DriverRow** é documentada no namespace [WebSvcDriver](https://msdn.microsoft.com/library/WebSvcDriver.aspx). 
    
  > [!NOTE]
  > Os aplicativos que usam o CSOM, usam manipuladores de eventos remotos ou acessam o Project Online não usam o namespace **Microsoft.Office.Project.Server.Schema**. 
  
  Em alguns aplicativos que usam manipuladores de eventos de confiança total, em que os manipuladores de eventos estão instalados no computador do Project Server, é necessário definir uma referência para o assembly Microsoft.Office.Project.Schema.dll. Veja dois exemplos:
    
  - Em um manipulador após o evento **OnCreated** de confiança total para campos personalizados, é possível usar o argumento de eventos **e.CustomFieldInformation** com uma referência para o namespace ** Microsoft.Office.Project.Server.Schema** para as definições **CustomFieldDataSet** e **CustomFieldsRow**. 
   
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

  - Uma atividade de fluxo de trabalho personalizado pode exigir uma referência a **Microsoft.Office.Project.Server.Schema** para definições **DataSet**. 
    
## <a name="psi-services"></a>Serviços da PSI
<a name="pj15_PSIRefOverview_PSI"> </a>

A PSI é um conjunto de serviços do WCF e serviços Web ASMX idênticos para Project Server 2013. Para usar um serviço em um projeto do Visual Studio, você pode definir uma referência para a URL do arquivo `.svc` ou serviço `.asmx?wsdl` usando um nome arbitrário para o nameservice. Os utilitários wsdl.exe ou svcutil.exe em seguida geram o código-fonte de proxy para esse namespace e o compilador cria um assembly de serviços de proxy para incluir em seu aplicativo. 
  
> [!NOTE]
> A referência da PSI inclui nomes de nameservice como espaço reservado para os serviços da PSI, tais como _[serviço Web do administrador]_, _[serviço Web do driver]_ e _[serviço Web do Project]_. Cada nameservice da PSI inclui uma classe primária que contém os métodos Web para esse serviço. Por exemplo, se você definir uma referência ao serviço **Admin** e chamá-lo de **WebSvcAdmin**, em seu aplicativo o nameservice **WebSvcAdmin** inclui a classe primária **Admin** que tem os métodos Web **GetServerCurrency**, **ListInstalledLanguages**, **ReadServerVersion** e assim por diante. Consulte [Atualizações para desenvolvedores no Project 2013](updates-for-developers-in-project-2013.md) para obter uma lista de serviços obsoletos da PSI. 
  
Do total de 30 serviços da PSI, **authentication**, **ExchangeSync**, **OData**, **P12Upgrade**, **psiserviceapp**, **PWA**, **View** e **WinProj** são para uso interno pelo Project Web App e o Project Professional e não são documentados. Embora você possa criar arquivos de proxy ou um assembly de proxy que inclua os serviços internos da PSI, os serviços internos não são para uso de terceiros; a referência da PSI não documenta esses serviços. A figura a seguir mostra a localização dos serviços da PSI de back-end no Gerenciador dos Serviços de Informações da Internet. 
  
**Localizar os serviços da PSI no IIS**

![Serviços da PSI no Gerenciador de IIS](media/pj15_PSIReference_IIS.gif "Serviços da PSI no Gerenciador de IIS")
  
Veja a seguir todas as classes que contêm métodos Web nos serviços da PSI:
  
1. [Admin](https://msdn.microsoft.com/library/WebSvcAdmin.Admin.aspx) inclui métodos que são usados nas páginas de **Administração do Project Server** no Project Web App. Define anos fiscais, gerencia as configurações de moeda e status, períodos de relatórios, o log de auditoria e as configurações para o Active Directory. 
    
2. [Archive](https://msdn.microsoft.com/library/WebSvcArchive.Archive.aspx) inclui métodos para gerenciamento de backup e restauração de projetos, categorias de segurança, campos personalizados, recursos, configurações do sistema, modos de exibição e o projeto global da empresa. Lê e atualiza o cronograma de arquivo morto. Arquiva todos os projetos ou exclui projetos arquivados especificados. Salva objetos de backup em tabelas de banco de dados de arquivo morto e restaura objetos de backup das tabelas de banco de dados publicadas. 
    
3. **authentication** Inclui métodos apenas para uso interno pelo Project Professional e Project Web App. 
    
4. [Calendar](https://msdn.microsoft.com/library/WebSvcCalendar.Calendar.aspx) Gerencia exceções do calendário empresarial. Faz check-out e check-in em calendários de recursos. Cria, exclui, lista tudo, atualiza ou retorna exceções do calendário. 
    
5. [CubeAdmin](https://msdn.microsoft.com/library/WebSvcCubeAdmin.CubeAdmin.aspx) Gerencia as configurações de cubo OLAP. Obtém o Analysis Server, o status do banco de dados e a lista de cubos. Coloca na fila uma solicitação de serviço de criação de cubo. Lê e atualiza as definições de membro calculado e as configurações de campo para dimensões e medidas no cubo. 
    
6. [CustomFields](https://msdn.microsoft.com/library/WebSvcCustomFields.CustomFields.aspx) Gerencia os campos personalizados da empresa. Inclui os métodos de check-out e check-in e os métodos para criar, ler, atualizar e excluir (CRUD) para campos personalizados da empresa. 
    
7. [Driver](https://msdn.microsoft.com/library/WebSvcDriver.Driver.aspx) Gerencia drivers de análise de portfólio e priorização de drivers para a criação de projetos e Gerenciamento de Propostas. Inclui os métodos CRUD para drivers de projeto. 
    
8. [Events](https://msdn.microsoft.com/library/WebSvcEvents.Events.aspx) Gerencia associações do manipulador de eventos do Project Server. Inclui os métodos CRUD para as associações do manipulador de eventos do Project Server para um evento específico ou para todas as associações do manipulador de eventos. 
    
9. **ExchangeSync** Este é um serviço interno do Project Server que lida com os eventos do Exchange Server. O Project Web App usa o **ExchangeSync** para sincronizar as atribuições entre o Project Server e o Exchange Server, ao invés de sincronizar diretamente com o cliente do Outlook no Office Project Server 2007. 
    
    O acesso ao serviço **ExchangeSync** está disponível somente pela URL do **ProjectServiceApplication**. As classes e os membros do **ExchangeSync** não têm suporte para desenvolvimento de terceiros. 
    
10. [LoginForms](https://msdn.microsoft.com/library/WebSvcLoginForms.LoginForms.aspx) fornece os métodos **Logon** e **Logoff** com autenticação baseada em formulários. O acesso ao serviço **LoginForms** está disponível somente em um site de front-end do Project Web App. 
    
11. [LoginWindows](https://msdn.microsoft.com/library/WebSvcLoginWindows.LoginWindows.aspx) fornece os métodos **Logon** e **Logoff**, que são usados para autenticação do Windows com aplicativos baseados em ASMX para instalações do Project Server 2013 com autenticação múltipla (baseada em declarações e em formulários). O acesso ao serviço **LoginWindows** está disponível somente em um site de front-end do Project Web App. 
    
    > [!CAUTION]
    > O serviço **LoginWindows** não é usado em aplicativos baseados em WCF ou para aplicativos que executam instalações no Project Server que usam apenas autenticação de declarações ou **OAuth**; nesses casos, o método **Logon** sempre retorna **false**. A autenticação por declarações manipula a autenticação integrada do Windows. 
  
12. [LookupTable](https://msdn.microsoft.com/library/WebSvcLookupTable.LookupTable.aspx) Gerencia as tabelas de pesquisa, as tabelas de pesquisa multilíngue e as máscaras de código correspondentes. Faz check-out, faz check-in, lê, cria, exclui e atualiza. 
    
13. [Notifications](https://msdn.microsoft.com/library/WebSvcNotifications.Notifications.aspx) Gerencia alertas e lembretes. Inclui métodos que obtêm, definem, registram e cancelam o registro de resultados de alerta. 
    
14. [ObjectLinkProvider](https://msdn.microsoft.com/library/WebSvcObjectLinkProvider.ObjectLinkProvider.aspx) Gerencia objetos e links da Web para documentos e itens de lista em sites do SharePoint. Cria, exclui ou lê objetos Web de projeto, vinculados a projetos, de tarefas ou vinculados a tarefas. 
    
    > [!NOTE]
    > O serviço **ObjectLinkProvider** foi preterido no Project Server 2013. Para saber mais, consulte a seção *Recursos preteridos* em [Atualizações para desenvolvedores no Project 2013](updates-for-developers-in-project-2013.md). 
  
15. **OData** Fornece a interface interna de **OData** para as tabelas e os modos de exibição de relatório. O acesso ao serviço **OData** está disponível somente pela URL do **ProjectServiceApplication** de back-end. O serviço **OData** privado na PSI fornece um método, **ODataClient.ProcessOdataMessage**, que o Project Server usa internamente para processar solicitações para dados de relatórios. As solicitações HTTP passam pelo serviço **ProjectData** de front-end. 
    
    Para saber mais sobre o serviço **ProjectData** e o protocolo OData para ler dados de relatório, consulte [ProjectData: referência do serviço OData do Project](https://msdn.microsoft.com/library/office/jj163015.aspx).
    
16. **P12Upgrade** Fornece métodos internos para o instalador do Project Server 2013 atualizar uma instalação do Office Project Server 2007. O acesso ao serviço **P12Upgrade** está disponível somente pela URL do **ProjectServiceApplication**. Os métodos **P12Upgrade** não têm suporte para desenvolvimento de terceiros. 
    
17. [PortfolioAnalyses](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.aspx) Inclui os métodos CRUD para dependências do projeto e para soluções de otimizador, planejador e análise. 
    
18. [Project](https://msdn.microsoft.com/library/WebSvcProject.Project.aspx) Gerencia projetos. Faz check-out, faz check-in, cria, exclui, lê ou atualiza projetos em tabelas publicadas ou tabelas de rascunho do banco de dados do Project. Coloca uma mensagem na fila para publicação. 
    
    Cria ou exclui entidades em projetos (tarefas, recursos, atribuições, etc.). Obtém informações sobre ou atualiza a equipe de projeto ou o endereço do site do projeto. Obtém o status do projeto, uma lista de projetos em tabelas de rascunho, todas as tarefas resumidas, tarefas que estão disponíveis para atribuição a um recurso específico ou todos os projetos em que um recurso tem atribuições.
    
    Cria e gerencia compromissos, cria propostas de projetos e projetos a partir de listas de tarefas do SharePoint e encontra relações entre projeto e projeto mestre.
    
19. **psiserviceapp** Usado internamente pelo Project Online. As classes e os membros do **psiserviceapp** não têm suporte para desenvolvimento de terceiros. 
    
20. **PWA** Contém vários métodos que são otimizados para o Project Web App, incluindo os métodos para regras de aprovação de atualização de tarefas e para gerenciar relatórios de status. Os métodos **PWA** são geralmente especializados e um pouco redundantes em comparação com métodos equivalentes em outros serviços da PSI. Os métodos **PWA** usam ou retornam muitos dos mesmos conjuntos de dados que os outros métodos da PSI. 
    
    O acesso ao serviço **PWA** está disponível somente pela URL do **ProjectServiceApplication**. As classes e os membros do **PWA** não têm suporte para desenvolvimento de terceiros. 
    
21. [QueueSystem](https://msdn.microsoft.com/library/WebSvcQueueSystem.QueueSystem.aspx) Gerencia a fila do Project Server. Obtém a contagem de trabalhos, o tempo de espera do grupo de trabalho e do trabalho, o status de todos os trabalhos, trabalhos especificados, trabalhos que pertencem ao chamador ou trabalhos para projetos especificados. Gerencia a correlação de trabalho e configura a fila. 
    
22. [Resource](https://msdn.microsoft.com/library/WebSvcResource.Resource.aspx) Gerencia os recursos da empresa. Faz check-out, faz check-in, atualiza ou cria recursos ou usuários do Project Server e suas configurações de autorização; encontra recursos por nome ou GUID; lê recursos ou dados de usuário e a estrutura de divisão de recursos (EDR) e as informações de segurança relacionadas; obtém todas as atribuições de um recurso; e redefine as senhas de usuários. A classe **Resource** inclui os métodos CRUD para delegações do usuário. 
    
23. [ResourcePlan](https://msdn.microsoft.com/library/WebSvcResourcePlan.ResourcePlan.aspx) Gerencia planos de recursos. Faz check-out, faz check-in, publica e inclui os métodos CRUD para planos de recursos. 
    
24. [Security](https://msdn.microsoft.com/library/WebSvcSecurity.Security.aspx) Inclui os métodos CRUD para modelos de segurança, categorias de segurança, permissões globais e organizacionais e permissões de grupo. A classe **Security** inclui métodos para categorias de projeto. 
    
25. [Statusing](https://msdn.microsoft.com/library/WebSvcStatusing.Statusing.aspx) Gerencia atualizações de status e atribuições. Aplica atualizações ou aprovações de status, envia atualizações de status, define informações de resumo para atualizações enviadas, exclui o histórico de aprovação ou as atualizações de status de aprovação para um usuário específico ou exclui todas as informações de status para um conjunto de projetos. Cria, obtém ou delega atribuições; define a duração da atribuição. Obtém novas atribuições para o usuário atual; obtém o histórico de transação da atribuição ou tarefa, os valores reais divididos ao longo do tempo ou a hierarquia das tarefas resumidas. 
    
    Visualiza ou importa dados de quadro de horários ou lê o cronograma de trabalho ou folga de um usuário. Localiza atualizações de status pendentes, informações para atualizações enviadas ou um registro de transações de alterações em uma atualização enviada. Lê o status da equipe.
    
26. [TimeSheet](https://msdn.microsoft.com/library/WebSvcTimeSheet.TimeSheet.aspx) Gerencia quadros de horários. Inclui métodos CRUD para quadros de horários e envia ou faz o cancelamento de quadros de horários. Localiza os quadros de horários que estão atrasados ou aguardando aprovação; localiza quadros de horários por período ou data. Obtém a lista de aprovadores de quadro de horários. Pré-carrega os valores reais de quadros de horários e valida uma linha do quadro de horários. A classe **TimeSheet** inclui os métodos **ReadProjectTimesheetLines** e **SubmitTimesheetLines** para ler e enviar quadros de horários para outro recurso sem a necessidade de representação. 
    
27. **View** O serviço **View** foi projetado para ser usado somente no Project Web App. Os métodos na classe **View** gerenciam modos de exibição e relatórios de exibição e leem campos nos modos de exibição. 
    
    O acesso ao serviço **View** está disponível somente pela URL do **ProjectServiceApplication**. Os métodos de **View** não têm suporte para desenvolvimento de terceiros. 
    
28. **WinProj** O serviço **WinProj** foi projetado para uso apenas pelo Project Professional. Os desenvolvedores terceirizados não devem usar métodos **WinProj** para programação com o Project Server. 
    
    Alguns métodos **WinProj** usam conjuntos de dados, como **ProjectRelationsDataSet** e **ResourceDataSet**, que os serviços **Project** e **Resource** também usam, mas exigem propriedades específicas e funções no Project Professional. 
    
    O acesso ao serviço **WinProj** está disponível somente pela URL do **ProjectServiceApplication**. Os métodos **WinProj** não têm suporte para desenvolvimento de terceiros. 
    
29. [Workflow](https://msdn.microsoft.com/library/WebSvcWorkflow.Workflow.aspx) Inclui os métodos CRUD para tipos de projeto corporativo e para gerenciar fases e estágios do fluxo de trabalho. Executa fluxos de trabalho, define informações de status e gerencia estágios da página de detalhes de projeto (PDP) em fluxos de trabalho de gerenciamento de propostas. Para desenvolver fluxos de trabalho do Project Server, os desenvolvedores podem usar o SharePoint Designer 2013 para fluxos de trabalho declarativos ou as Office Developer Tools para Visual Studio 2012 para desenvolvimento com o .NET Framework 4 e a classe [ Microsoft.ProjectServer.Client.WorkflowActivities](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.WorkflowActivities.aspx) no CSOM. 
    
30. [WssInterop](https://msdn.microsoft.com/library/WebSvcWssInterop.WssInterop.aspx) Gerencia sites de projeto. Cria e exclui sites de projeto. Obtém informações sobre e atualiza as configurações do SharePoint e os sites de administração. Sincroniza e atualiza as associações e os grupos do site de projeto. 
    
Cada namespace de serviço inclui todas as classes do manipulador de evento e do esquema **DataSet** que o serviço usa. Por exemplo, `Calendar.svc` (ou `Calendar.asmx?wsdl` para o serviço Web ASMX) descreve o serviço **Calendar**. Se você atribuir a referência **WebSvcCalendar**, o namespace do proxy conterá a classe **Calendar** primária com os métodos **CheckInCalendars**, ** CheckOutCalendars** e assim por diante. O namespace de proxy **WebSvcCalendar** também inclui a classe **CalendarDataSet** e todas as suas subclasses. 
  
Alguns dos serviços da PSI contêm classes **DataSet** duplicadas. Por exemplo, os serviços **Project** e **Statusing** incluem a classe **ProjectDataSet**. Isso ocorre porque os dois métodos nos serviços **Project** e **Statusing** incluem referências ao **ProjectDataSet**, e os assemblies de proxy que você cria ao definir referências e compilar um aplicativo incluem os conjuntos de dados relacionados. Os serviços **Project** e **Statusing** podem exigir valores para campos diferentes na classe **ProjectDataSet.ProjectRow**. 
  
Quando você estiver navegando pelos namespaces e pelas classes de referência da PSI, por exemplo para ver os métodos Web para o serviço **Project**, expanda o namespace **[serviço Web do Project]** na lista **Conteúdo** e, em seguida, expanda a classe **Project**. 
  
## <a name="see-also"></a>Confira também

- [Arquitetura do Project Server 2013](project-server-2013-architecture.md)
- [Programabilidade do Project Server](project-server-programmability.md)   
- [O que a PSI faz e não faz](what-the-psi-does-and-does-not-do.md)   
- [Pré-requisitos para exemplos de código baseados em ASMX no Project](prerequisites-for-asmx-based-code-samples-in-project.md)   
- [Pré-requisitos para exemplos de código baseados em WCF no Project](prerequisites-for-wcf-based-code-samples-in-project.md)   
- [Central de desenvolvedores do .NET Framework](https://msdn.microsoft.com/netframework/aa496123.aspx)
    

