---
title: Programabilidade do Project Server
manager: lindalu
ms.date: 12/03/2019
ms.audience: Developer
f1_keywords:
- events
- PDS
- PDS compatibility
- Project Server databases
- Project Server events
- Project Server Interface
- Project Server workflow
- Project workflow
- PSI
- PSI limitations
- PSI uses
- SharePoint Services
- WF
- workflow
- Workflow Foundation
- WSS
keywords:
- Project 2013, arquitetura e programação, PSI, Projects, capacidade de programação, Project Server, PSI, genérico de compatibilidade, Interface do Project Server, Interface do Project Server, compatibilidade com PDS, Interface do Project Server, genérico, Project Server, versões de projeto, versões, projetos, Project Server, bancos de dados, Project 2013, plataforma, interface do Project Server, cenários de uso, Project Server, eventos, Project Server, compatibilidade de PSI, interface do Project Server
ms.assetid: a93d2153-5132-4289-af51-69350471e248
description: Saiba mais sobre os principais recursos de programação do Project Server 2013. Este artigo contém informações sobre a portabilidade de aplicativos que foram criados para versões anteriores do Project Server.
localization_priority: Priority
ms.openlocfilehash: e6991712b87291e90c6b4f277db84686aab384e7
ms.sourcegitcommit: 31b0a7373ff74fe1d6383c30bc67d7675b73d283
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2020
ms.locfileid: "41773726"
---
# <a name="project-server-programmability"></a>Programabilidade do Project Server

Saiba mais sobre os principais recursos de programação do Project Server 2013. Este artigo contém informações sobre a portabilidade de aplicativos que foram criados para versões anteriores do Project Server.

O Project Server 2013 foi projetado para suportar a maioria dos aplicativos desenvolvidos para o Project Server 2010 e novas soluções para várias plataformas, em que os aplicativos podem acessar as instalações on-line e no local do Project Server. Aplicativos e extensões que foram desenvolvidas para o Project Server 2003 ou anterior devem ser reformuladas para usar o modelo de objeto do lado cliente (CSOM) ou Interface do servidor do projeto. Os aplicativos que foram desenvolvidos para o Project Server 2010 ou Office Project Server 2007 podem exigir algumas alterações e recompilar o uso do PSI; Para usar o CSOM, esses aplicativos exigem um novo design.
  
A plataforma do Project Server permite altos níveis de produtividade do programador criando no SharePoint Server 2013, o .NET Framework 4 e no protocolo OData com o CSOM. Os desenvolvedores podem estender o Project Web App com aplicativos, partes de aplicativos e Web Parts, definir fluxos de trabalho usando o SharePoint Designer 2013 e aplicar regras de negócios usando receptores de eventos remotos para eventos do Project Server.
  
## <a name="project-server-and-sharepoint-server"></a>Project Server e SharePoint Server
<a name="pj15_Programmability_MOSS"> </a>

O Project Web App foi criado a partir do SharePoint Server 2013 e usa Web Parts e páginas mestras para facilitar a criar aplicativos personalizados e soluções do Project Web App. O Project Server 2013 integra-se profundamente ao SharePoint Server 2013 como a plataforma para colaboração de projetos, relatórios, administração de sites, segurança e gerenciamento de fluxo de trabalho.
  
Os sites do projeto incluem mais opções de informações e colaboração para os membros da equipe, onde você pode adicionar aplicativos padrão que incluem um resumo do projeto, listas especializadas do SharePoint para tarefas com cronograma, rastreamento de problemas, riscos, entregas do projeto e o calendário da equipe. biblioteca de documentos e discussões em equipe. Aplicativos personalizados para o Project Server 2013 fornecem extensões e a flexibilidade de colaboração em equipe. Você também pode adicionar partes do aplicativo para personalizar um aplicativo, usando o mesmo mecanismo para adicionar e editar Web Parts, quando você edita uma página. Você pode localizar os sites de projeto em qualquer lugar no farm do SharePoint onde o Project Server está instalado. Para usar outros serviços básicos do SharePoint Server 2013, como os Serviços do Excel e o Enterprise Search, um administrador pode habilitar e configurar os serviços. 
  
Quando você instala o Project Server 2013, você pode configurar o Aplicativo do Serviço do Project é adicionado ao SharePoint Web Services. O aplicativo de serviço do Project inclui serviços locais do Windows Communication Foundation (WCF) e serviços web ASMX para PSI. Outros exemplos de aplicativos de serviço incluem a Pesquisa do SharePoint e o Gerenciamento de documentos do SharePoint. Para saber mais, confira a documentação de desenvolvedor do SharePoint Server 2013.
  
O Aplicativo de Serviço do Project é um provedor de serviços lógico que pode gerenciar várias instâncias do Project Web App. A configuração do Project Server cria um site específico do Project Web App em um aplicativo da web do SharePoint. A  página inicial do Project Web App contém links para a página da Central de projetos, a página da Central de recursos e a página de Central de Business Intelligence para relatórios, além de uma página que contém uma lista de outros aplicativos padrão. A figura 1 mostra o comando **Editar página** na lista suspensa de **configuração**na página inicial do Project Web App, que permite que você adicione ou edite Web Parts. 
  
> [!NOTE]
> Algumas páginas administrativas do Project Web App, como a página de configurações do PWA, não são editáveis e não mostram o comando **Editar página**. O Project Web App não permite editar páginas usando o SharePoint Designer 2013. Você pode editar as páginas do site do projeto com o SharePoint Designer 2013. 
  
**Figura 1. Usando o menu Editar página no Project Web App**

![Editar a Página Inicial no Project Web Access](media/pj15_Programmability_PWAHome.gif "Editar a Página Inicial no Project Web Access")
  
Para acessar a página de configurações do Site no Project Web App, escolha o ícone**configurações** no canto superior direito da página. A página Configurações do Site ( `https://ServerName/ProjectServerName/_layouts/15/settings.aspx`) permite alterar a aparência e o tema do site, adicionar Web Parts personalizadas e modificar ou criar páginas mestras de sites de projetos.
  
A personalização do código em páginas ASPX ou a personalização de páginas mestras do Project Web App com o SharePoint Designer 2013 não são suportadas. A personalização do código nas páginas do Project Web App pode causar problemas com atualizações e service packs do Project Server. 
  
### <a name="customization-of-project-web-app-with-sharepoint-packages"></a>Personalização do Project Web App com pacotes do SharePoint
<a name="pj15_Programmability_CustomizationOfPWA"> </a>

Como o Project Web App é um aplicativo do SharePoint e sites de projeto são sites do SharePoint, você pode adicionar aplicativos personalizados, Web Parts, manipuladores de eventos, campos personalizados e outros recursos usando pacotes do SharePoint (arquivos .wsp) ou aplicativos do SharePoint (arquivos .spapp ). Um pacote do SharePoint ou um pacote de aplicativos pode incluir várias entidades do Project Server, nas quais as definições de entidade são especificadas em um arquivo elements.xml no pacote.
  
No Project Online, você pode adicionar botões à faixa de opções do Project Web App, mas não pode remover ou renomear os botões existentes de produto e não pode criar novas guias da faixa de opções. Para saber mais, confira [Crie ações personalizadas para implantar com aplicativos para o SharePoint](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/create-custom-actions-to-deploy-with-sharepoint-add-ins).
  
> [!CAUTION]
> Ao instalar um pacote do SharePoint ou um pacote de aplicativos, os tipos de entidades do Project Server devem aparecer na ordem que o esquema PSEntityProvision.xsd especifica ou a validação de esquema do pacote falha e a instalação não é concluída. 
  
O arquivo de esquema PSEntityProvision.xsd está disponível no download SDK do Project 2013, na subpasta `Documentation\Schemas\AppProvisioning`. A figura 2 mostra o modo de exibição do Explorer de esquema XML no Visual Studio do esquema **PSEntityProvision**, onde a sequência **LookupTable** é expandida. 
  
**Figura 2. Modo de exibição do Visual Studio do esquema de provisionamento de entidade do Project Server**

![Exibição do esquema de entidade do Project Server](media/pj15_Programmability_EntitySchema.gif "Exibição do esquema de entidade do Project Server")
  
Os pacotes do SharePoint que instalam recursos para o Project Server podem conter um ou mais arquivos elements.xml que seguem o esquema**PSEntityProvision**. As entidades do Project Server em um único arquivo XML devem aparecer na seguinte ordem: 
  
1. Fases do fluxo de trabalho
    
2. Tabelas de pesquisa
    
3. Campos personalizados
    
4. Estágios do fluxo de trabalho
    
5. Tipos de Projeto de Empresa
    
6. Manipuladores de eventos
    
Quando você cria um pacote do SharePoint que contém as entidades do Project Server, é possível colocar as definições de entidade em vários arquivos elements.xml. Cada arquivo XML pode passar na validação de esquema, 
mas as entidades no pacote inteiro podem não estar na ordem correta. Por exemplo, uma entidade de campo personalizado no primeiro arquivo XML pode se referir a uma tabela de pesquisa no segundo arquivo XML. Durante a instalação, o campo personalizado não pode ser criado porque a tabela de pesquisa ainda não foi criada.
  
Se uma instalação do pacote falhar, os objetos que foram criados permanecerão no Project Web App, mas o pacote de não instalará completamente. Reinstalar o pacote pode funcionar, mas isso não é uma boa experiência para os clientes. Quando as definições de entidade abrangerem vários arquivos elements.xml, organize as entidades do Project Server em todo o pacote do SharePoint para garantir que a instalação siga a ordem correta. Com o esquema PSEntityProvision.xsd no download do Project 2013 SDK, é possível desenvolver uma ferramenta que verifica a ordem prescrita de entidades nos arquivos XML.
  
## <a name="upgrading-applications-with-the-project-server-apis"></a>Atualizar aplicativos com as APIs do Project Server
<a name="pj15_Programmability_APIs"> </a>

Quando você atualiza um aplicativo que foi desenvolvido para uma versão anterior do Project Server, você pode optar por usar o CSOM ou o PSI para uma interface programática que inclua métodos para criar, ler, atualizar e excluir entidades do projeto (as operações CRUD). Embora o CSOM internamente chame o PSI, ele não substitui totalmente todos os métodos PSI. Para cenários e limitações de PSI e o CSOM, confira [O que o PSI faz e não faz](what-the-psi-does-and-does-not-do.md) e [O que o CSOM faz e não faz](what-the-csom-does-and-does-not-do.md).
  
> [!NOTE]
> Se o CSOM incluir a funcionalidade necessária, recomendamos que você atualize os aplicativos para usar o CSOM. O CSOM permite que os aplicativos sejam usados ​​para instalações locais e on-line do Project Server 2013. 
  
Se o seu aplicativo ler principalmente dados do Project Server, você poderá usar as tabelas e exibições de relatórios no banco de dados do Project Server para um cenário local. Se você pretende usar o aplicativo com o Project Online, você pode usar o protocolo OData para o serviço **ProjectData**, que fornece acesso local e on-line aos dados de relatório. Para obter mais informações, confira [ProjectData ‒  referência do serviço Project OData](https://docs.microsoft.com/previous-versions/office/project-odata/jj163015(v=office.15)).
  
### <a name="using-the-psi"></a>Usando o PSI
<a name="pj15_Programmability_PSI"> </a>

O PSI permite que aplicativos de confiança total do cliente, incluindo os aplicativos Project Professional 2013, Project Web App e LOB, acessem dados do Project Server em um farm do SharePoint. O PSI é criado e usado com o .NET Framework 4 e oferece vantagens, como um ambiente de desenvolvimento conhecido, com segurança interna, tratamento de erros e coleta de lixo.
  
O PSI é acessado por meio de serviços WCF ou serviços da web ASMX. A interface ASMX se baseia no WCF. Cada serviço PSI normalmente contém uma classe base com métodos CRUD para itens dentro dessa classe. Os itens são especificados pelas classes relacionadas **Dataset**. Por exemplo, o serviço **CustomFields** serviço contém a classe **CustomFields** com métodos, como [CreateCustomFields2](https://docs.microsoft.com/previous-versions/office/ee767959(v=office.14)) . Os dados de um ou mais campos personalizados da empresa são especificados em **CustomFieldDataSet**.
  
> [!NOTE]
> A interface de serviço Web ASMX da PSI foi preterida no Project Server 2013. Embora a interface ASMX ainda esteja disponível, novos aplicativos que usam o PSI devem usar a interface do WCF ou, se possível, novos aplicativos devem usar o CSOM em vez do PSI. Versões futuras do Project Server exigirão uma atualização dos aplicativos baseados em ASMX existentes para usar a interface WCF do PSI ou para usar o CSOM. 
  
Existem 22 serviços PSI documentados e públicos, que são duplicados na interface do WCF e na interface do ASMX. O PSI também inclui oito serviços privados não documentados. O Project Web App e o Project Professional usam os serviços PSI públicos e os serviços PSI privados. O PSI geralmente é acrescentado para corresponder aos objetos de negócios. Ou seja, cada método PSI está associado a um objeto comercial, como **Calendário** ou **Recurso**. A PSI é a interface principal de objetos comerciais. Como a camada de negócios fornece componentes de lógica de negócios reutilizáveis, diferentes aplicativos que interagem com os dados do Project Server usam a mesma lógica de negócios.
  
Os métodos PSI que interagem assincronamente com o Project Server têm nomes que começam com **Queue**. Cada método PSI é implementado com uma interface separada que usa dados fortemente digitados. Por exemplo, o método **QueueCreateProject** no serviço **projeto**aceita o parâmetro _dataset_ tipo **ProjectDataSet**. A classe**ProjectDataSet**deriva o tipo **DataSet**. A verificação de tipo no .NET Framework e a conclusão do IntelliSense no Visual Studio ajudam a reduzir erros no desenvolvimento com o PSI. Para obter uma introdução à referência detalhada para namespaces, classes, métodos, propriedades, eventos e assemblies relacionados do PSI, consulte [Visão geral da referência da PSI do Project](project-psi-reference-overview.md).
  
O Project Server 2013 usa o tratamento de exceções do .NET Framework. Todos os erros são registrados no servidor, na parte superior da pilha PSI. Alguns erros enviam um relatório simples para o cliente, como um objeto **SoapException** para a interface ASMX ou um objeto **FaultException** para a interface WCF. As exceções podem ser registradas no log de eventos do aplicativo e alguns erros também registram um relatório detalhado no servidor nos logs de rastreamento do ULS (Unified Logging Service). 
  
Para aplicativos locais de confiança total, o PSI também é extensível. Você pode adicionar um assembly .NET a um serviço que forneça novas funcionalidades, usa a mesma infraestrutura de segurança do Project Server e chama outros métodos PSI ou herda classes PSI. Uma extensão PSI também pode fornecer a lógica de negócios e o acesso ao banco de dados necessários para a nova funcionalidade.
  
### <a name="using-the-csom"></a>Usando o CSOM
<a name="pj15_Programmability_CSOM"> </a>

Com o CSOM, você pode desenvolver aplicativos que acessam o Project Online ou uma instalação do Project Server 2013 no local. Os aplicativos podem ser distribuídos em uma loja pública do Office ou em um catálogo de aplicativos particulares. O CSOM foi projetado para ser uma API fácil de usar que consome diretamente ou fornece dados por nome com consultas LINQ, em vez de transmitir conjuntos de dados e construir parâmetros _changeXml_ ou parâmetros de _filtro_ XML. O CSOM implementa a funcionalidade principal da interface do servidor do projeto (PSI) para as principais entidades, como**Projeto**, **Tarefa**, **EnterpriseResource**e **Atribuição**. O CSOM inclui várias entidades adicionais, como **CustomField**, **LookupTable**, **WorkflowActivities**, **EventHandler**, e **QueueJob**, que oferecem suporte a outras funcionalidades comuns do Project Server.
  
O CSOM pode ser usado copiando os seguintes recursos para o seu computador de desenvolvimento local:
  
- Para o desenvolvimento do .NET Framework 4, copie a assembly `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\ISAPI\Microsoft.ProjectServer.Client.dll`. 
    
  Para documentação de classes CSOM e membros, confira a namespace [Microsoft.ProjectServer.Client](https://docs.microsoft.com/previous-versions/office/dn529530(v=office.15)). Para um exemplo de aplicativo, confira [Introdução ao CSOM e .NET](getting-started-with-the-project-server-csom-and-net.md).
    
- Para o desenvolvimento do Microsoft Silverlight, copie a assembly `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\ClientBin\Microsoft.ProjectServer.Client.Silverlight.dll`. 
    
- Para esenvolver aplicativos para Windows Phone 8, copie a assembly `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\ClientBin\Microsoft.ProjectServer.Client.Phone.dll`. 
    
- Para usar o JavaScript para desenvolver aplicativos para outros dispositivos e aplicativos da web, copie o arquivo `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\PS.js` e o arquivo `PS.debug.js`. Para um exemplo de web app, confira [Introdução ao modelo de objeto do JavaScript do Project Server 2013](getting-started-with-the-project-server-2013-javascript-object-model.md).
    
O CSOM chama internamente o PSI; portanto, se o PSI não puder fazer um trabalho, o CSOM também não poderá. Para limitações do CSOM, confira [O que o CSOM faz e não faz](what-the-csom-does-and-does-not-do.md) e [O que o PSI faz e não faz](what-the-psi-does-and-does-not-do.md). Confira mais informações sobre o desenvolvimento do CSOM em [Atualizações para desenvolvedores no Project 2013](updates-for-developers-in-project-2013.md) e [Modelo de objeto do cliente (CSOM) para o Project 2013](client-side-object-model-csom-for-project-2013.md).
  
### <a name="porting-applications-built-for-project-server-2003"></a>Portabilidade de aplicativos criados do Project Server 2003
<a name="pj15_Programmability_Porting2003"> </a>

No Project Server 2003, muitos dados e funcionalidades estão disponíveis somente com o Project Professional 2003 ou pelo acesso direto ao banco de dados. O PSI introduzido no Project Server 2007 remove muito essa restrição. Ao contrário do Project Data Service (PDS) no Project Server 2003, o PSI e o CSOM fornecem interfaces abrangentes para objetos comerciais no Project Server.
  
Os aplicativos desenvolvidos para o PDS não são compatíveis com versões mais recentes do Project Server. O CSOM e o PSI fornecem paridade funcional para o PDS, mas são incompatíveis com métodos ou parâmetros PDS.
  
> [!NOTE]
> Como os aplicativos do PDS devem ser completamente reprojetados para o Project Server 2013, recomendamos que você use o CSOM. 
  
Confira mais informações sobre compatibilidade PDS e  diretrizes de portabilidade de extensões PDS para o PSI em [Paridade PDS em serviços Web de PSI](https://docs.microsoft.com/previous-versions/office/developer/office-2007/ms197081(v=office.12)).
  
### <a name="porting-applications-built-for-project-server-2007-and-project-server-2010"></a>Aplicativos de portabilidade criados do Project Server 2007 e no Project Server 2010
<a name="pj15_Programmability_Porting2007"> </a>

O PSI no Project Server 2013 é um superconjunto do modelo de objeto PSI no Office Project Server 2007 e no Project Server 2010. Muitos aplicativos criados para as duas versões anteriores do Project Server continuam a funcionar em instalações locais de confiança total do Project Server 2013. No entanto, os seguintes tipos de aplicativos exigem atualizações ou reformulação:
  
- Use o CSOM para aplicativos que são adaptados para uso com o Project Online.
    
- Use o CSOM para aplicativos que são adaptados para uso em dispositivos móveis e computadores tablet.
    
- Use o CSOM para aplicativos que estão disponíveis como aplicativos na Office Store ou em um catálogo de aplicativos particulares.
    
- Para aplicativos que modificam o agendamento do projeto, use o CSOM ou altere o aplicativo para usar o método PSI o[QueueUpdateProject2](https://docs.microsoft.com/previous-versions/office/project-class/jj236245(v=office.15)). 
    
- Aplicativos locais ou da web que fazem logon em usuários em diferentes instâncias do Project Web App devem usar configurações programáticas para pontos de extremidade do WCF do CSOM ou do PSI. Os métodos foram substituídos. Os aplicativos devem usar a autenticação OAuth no lugar da autenticação Formas e para uso com o Project Online. Para saber mais, confira [Autorização e autenticação para os aplicativos no SharePoint 2013](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/authorization-and-authentication-of-sharepoint-add-ins).
    
- Aplicativos que dependem ou modificam configurações de segurança específicas do Project Server.
    
  > [!NOTE]
  > Uma instalação local padrão do Project Server 2013 usa o modo de permissão do SharePoint, no qual as configurações de segurança do Project Server não são acessíveis por meio do PSI. Para alterar o modo de permissão do Project, confira a seção *Modo de permissão do SharePoint* em [Novidades para profissionais de TI no Project Server 2013](https://docs.microsoft.com/project/what-s-new-for-it-pros-in-project-server-2016). 
  
- Para muitos fluxos de trabalho personalizados do Project Server, você pode usar o SharePoint Designer 2013 para criar fluxos de trabalho declarativos. Para fluxos de trabalho personalizados que exigem mais programação, você *não* deve usar diretamente classes ou membros na namespace **Microsoft.Office.Project.Server.Workflow**. Nesse caso, use a classe [Microsoft.ProjectServer.Client.WorkflowActivities](https://docs.microsoft.com/previous-versions/office/mt780562(v=office.15)) no CSOM. 
    
- Em geral, aplicativos que usam representação devem ser reescritos para usar a interface do WCF do PSI. Aplicativos que fazem atualizações de status simples para outros usuários não requerem representação. Eles podem usar o método [StatusAssignment.SubmitStatusUpdates](https://docs.microsoft.com/previous-versions/office/project-class/jj235883(v=office.15)) no CSOM ou o método[Statusing.SubmitStatusForResource](https://docs.microsoft.com/previous-versions/office/ee755393(v=office.14)) no PSI. 
    
- Os componentes de middleware executados no computador do Project Server podem ser instalados apenas para uso local e devem usar a interface do WCF do PSI. Por exemplo, um componente de middleware que usa a interface ASMX para trocar dados entre o Project Web App no ​​local e um aplicativo de quadro de horários externo precisaria ser reescrito para usar a interface WCF do PSI. Para trabalhar com o Project Online, o componente teria que ser reprojetado como um aplicativo e usar o CSOM.
    
### <a name="migration-and-compatibility-of-custom-solutions"></a>Migração e compatibilidade de soluções personalizadas
<a name="pj15_Programmability_CustomSolutions"> </a>

Classes e membros nas interfaces públicas ASMX e WCF do PSI são idênticos. No entanto, o número de colunas e o tamanho das tabelas de dados usadas ou retornadas pelos métodos PSI podem ser diferentes entre o Project Server 2013 e as duas versões anteriores do Project Server. Também existem diferenças nas tabelas e exibições de relatórios, em comparação com o banco de dados de relatórios nas versões anteriores.
  
> [!IMPORTANT]
> É altamente recomendável testar completamente as soluções em uma instalação de não produção do Project Server 2013 antes de implantá-las em um servidor de produção. 
  
Quando você migrar uma solução para o Project Server 2013, ou se uma solução não funcionar conforme o esperado, você deve, pelo menos, fazer o seguinte:
  
- Atualizar a solução, abrindo-a no Visual Studio 2012. Algumas soluções também podem usar o Visual Studio 2010.
    
- Alterar o destino para .NET Framework 4.
    
- Alterar a montagem de referências para usar conjuntos do Project Server 2013, como Microsoft.Office.Project.Server.Library.dll e Microsoft.Office.Project.Server.Events.Receivers.dll.
    
- Fazer uma lista das referências da Web do ASMX ou referências de serviço do WCF e nomes de espaço para nome e, em seguida, excluir as referências do Project Server.
    
- Adicionar a montagem de proxy ProjectServerServices.dll que você pode criar a partir dos arquivos de origem do proxy WCF no download do SDK do Project 2013 ou adicionar os arquivos de origem do proxy para os serviços WCF necessários. Para serviços ASMX, inclua as referências de serviço da web do ASMX front-end novamente, usando os mesmos nomes de namespace; ou adicione o assembly de proxy ProjectServerServices.dll que você pode criar a partir das origens WSDL no download do Project 2013 SDK.
    
  > [!NOTE]
  > No download do SDK do Project 2013, os namespaces nos arquivos de origem do proxy começam todos com*Svc* . Por exemplo, a namespace **Recurso**do serviço no arquivo de proxy WCF e no arquivo de proxy ASMX é **SvcResource**. > Se o seu aplicativo usar nomes de namespaces diferentes, você poderá recompilar o assembly do proxy para usar seus namespaces ou alterar os namespaces do PSI no seu aplicativo. Por exemplo, você pode modificar o script CompileWCFProxyAssembly.cmd e recompilar ProjectServerServices.dll dos arquivos de origem do proxy no download do SDK. 
  
- Se você mudar de usar a interface ASMX do PSI para a interface do WCF, poderá inicializar as classes de cliente de forma programática ou usando os pontos de extremidade do WCF no app.config. Use a inicialização programática quando você precisar alternar rapidamente para instâncias diferentes do Project Web App ou quando estiver desenvolvendo uma web part que use o PSI.
    
- Existem vários novos métodos e conjuntos de dados nos serviços PSI no Project Server 2013 e algumas classes **DataRow** contêm novas propriedades. Por exemplo, o método [QueueUpdateProject2](https://docs.microsoft.com/previous-versions/office/project-class/jj236245(v=office.15)) no PSI usa o mecanismo de agendamento do Project Server para reprogramar um projeto atualizado sem a necessidade de abrir o projeto no Project Professional 2013 e também permite adicionar ou excluir entidades do projeto na mesma chamada. 
    
- Compilar e testar a solução.
    
## <a name="project-scheduling-on-the-server"></a>Agendamento do Project no servidor
<a name="pj15_Programmability_Scheduling"> </a>

O Project Server 2013 tem dois mecanismos de agendamento. O mecanismo de agendamento mais recente é o mesmo mecanismo de agendamento no Project Professional 2013. Quando você faz alterações no agendamento e publica as alterações usando a web part Scheduling (página Detalhes do Projeto) no Project Web App ou em um site de projeto ou usando o CSOM, o cálculo de datas, custos, duração, trabalho restante, linhas de base e outras alterações relacionadas ao agendamento são as mesmas caso você fizesse as alterações e publicasse o projeto usando o Project Professional 2013. No entanto, exceto para o [QueueUpdateProject2](https://docs.microsoft.com/previous-versions/office/project-class/jj236245(v=office.15)) os métodos PSI usam o mecanismo de agendamento anterior migrado do Project Server 2010. O motivo é garantir que os aplicativos herdados se comportem da mesma maneira no Project Server 2013 como faziam anteriormente. 
  
> [!NOTE]
> Para usar o mecanismo de agendamento atualizado no Project Server 2013, os aplicativos podem usar o CSOM. 
  
Os mecanismos de planejamento mais antigos e mais recentes têm as seguintes limitações:
  
- **Somente agendamento de projeto único ** O agendamento afeta apenas o projeto atual, quando as alterações são feitas por meio de atualizações de status da tarefa com o PSI ou o CSOM ou com o Project Web App. Se o projeto atual tem links para outros projetos, subprojetos ou projetos mestres, os projetos vinculados não são alterados. 
    
- **Resumo de tarefas** Os resumos de tarefas geralmente são somente leitura no Project Server. Por exemplo, as atribuições para tarefas de resumo não podem ser criadas e a conclusão percentual não pode ser modificada. No entanto, o Project Server suporta a edição de datas e duração de tarefas de resumo agendadas manualmente. 
    
    Os dados efetivos no Project Server não são adicionados automaticamente a uma atribuição de tarefa de resumo, porque isso ignoraria o processo de aprovação no Project Server. No Project Professional, quando você adiciona efetivos a uma sub tarefa, os efetivos também são adicionados para uma atribuição na tarefa de resumo. A diferença de comportamento pode ser confusa para o usuário.
    
    O Project Server exclui os efetivos em uma atribuição de tarefa de resumo se a duração da sub tarefa diminuir ou a data de término for alterada.
    
    > [!CAUTION]
    > Embora o Project Professional possa fazê-lo, recomendamos que você não faça atribuições em tarefas de resumo. 
  
A seguir estão os problemas e as limitações da programação PSI com o mecanismo de agendamento mais antigo do Project Server:
  
- **Alterando o status ativo de uma tarefa** O mecanismo de agendamento mais antigo do Project Server pode mostrar horários de início ou término inconsistentes quando você usa o método [QueueUpdateProject](https://docs.microsoft.com/previous-versions/office/ms471014(v=office.14)) para alterar o status ativo de uma tarefa, se houver várias alterações no objeto **ProjectDataSet** para o parâmetro _dataset_. Se a propriedade **TASK_IS_ACTIVE** é a única alteração no parâmetro _conjunto de dados_ da **QueueUpdateProject**, você pode atualizar o projeto.
    
    Para obter mais informações sobre tarefas inativas e o mecanismo de agendamento mais antigo, consulte os artigos do blog [Introduzindo tarefas inativas no Project 2010](https://blogs.msdn.com/b/project/archive/2010/06/10/introducing-inactive-tasks-in-project-2010.aspx) e [Project Server 2010: Agendando na Web, PSI e Project Professional](https://blogs.msdn.com/b/brismith/archive/2010/09/10/project-server-2010-scheduling-on-the-web-the-psi-and-project-professional.aspx?wa=wsignin1.0). Para obter uma comparação de agendamento no Project Professional 2010 e no Project Web App no ​​Project Server 2010, confira [Comparação de gerenciamento de cronograma baseado na Web](https://blogs.msdn.microsoft.com/brismith/2010/09/10/project-server-2010-scheduling-on-the-web-the-psi-and-project-professional/).
    
- **Valor acumulado não calculado** O mecanismo de programação mais antigo não calcula os campos de valor agregado: ACWP, BAC, BCWP, BCWS, CPI, CV, CV%, EAC, SPI, SV,% SV, TCPI, VAC, Variação de Duração, Variação Inicial, Concluir Variação, Desvio de Custos e Variação de Trabalho. Se um projeto tiver valores para esses campos e o projeto for atualizado usando o método **QueueUpdateProject**, os valores do campo não serão alterados. Para evitar o problema, use o método **QueueUpdateProject2**. 
    
Você pode lidar com as limitações de agendamento PSI das seguintes maneiras:
  
- Se o CSOM tiver os métodos requeridos pelo aplicativo, use o CSOM em vez do PSI.
    
- Abra projetos no Project Professional e salve-os para o Project Server.
    
- Nos relatórios, não inclua campos que o PSI não atualiza.
    
- Adicione uma anotação nos relatórios sobre dados que podem estar obsoletos.
    
Há sinalizadores nas tabelas de relatórios e nos cubos que ajudam a detectar quando alguns dados do projeto não são atualizados. Os dados de relatório na tabela MSP_EpmProject e em MSP_EpmProject_UserView incluem os seguintes campos: 
  
-  _ProjectWbsIsStale_ &ndash; Indica se a estrutura de divisão de trabalho (hierarquia de estrutura de tópicos de tarefa) é obsoleta. 
    
-  _ProjectEarnedValueIsStale_ &ndash;Indica que os campos de valor acumulado são obsoletos. 
    
-  _ProjectRollupsAreStale_ &ndash; Indica que um subprojeto está atualizado no banco de dados de rascunho, mas o projeto mestre não está atualizado. Os valores acumulados do subprojeto são obsoletos. 
    
-  _ProjectHierarchyNotSynchronized_ &ndash; O projeto mestre não está sincronizado com seus filhos. Isso acontece quando os projetos filho são publicados explicitamente, não como parte da publicação do projeto principal. 
    
-  _ProjectCalculationsAreStale_ &ndash;O Project Professional salvou um projeto sem calcular o agendamento (ou seja, o modo de cálculo está definido como **Manual** na guia **Agendamento** na caixa de diálogo **Opções do Projeto**). 
    
-  _ProjectGhostTaskAreStale_ &ndash;é  semelhante ao _ProjectHierarchyNotSynchronized_, mas avisa sobre dados de vínculos entre projetos. É possível que nenhum projeto mestre exista, mas os dados do projeto em um lado do link são mais recentes do que no outro lado.
    
## <a name="about-accessing-the-project-server-database"></a>Como acessar o banco de dados do Project Server
<a name="pj15_Programmability_Databases"> </a>

Se você tiver permissões no Microsoft SQL Server para acessar o banco de dados do Project Server, você pode ler as tabelas de relatórios e exibições. Se você tiver as permissões necessárias do Project Server, você também pode ler dados de tabelas de relatórios usando as consultas OData. Os desenvolvedores são fortemente desencorajados a acessar diretamente as tabelas de rascunho, publicadas ou arquivadas por meio de consultas do SQL Server no banco de dados do Project Server. Fazer alterações diretas em qualquer uma das tabelas no banco de dados do Project Server pode danificar a integridade referencial e interferir no acesso ao banco de dados por meio do serviço de enfileiramento do Project Server.
  
> [!IMPORTANT]
> Não há nada que o impeça ativamente de usar o acesso direto ao banco de dados programático para atualizar os dados. Você deve estar ciente de que o cache do Project Professional, as tabelas publicadas e as tabelas de relatórios dependem de um protocolo de sincronização de cache que pode ser interrompido pela edição direta de dados. Se você danificar o banco de dados do Project Server ou corromper os caches do lado do cliente do Project Professional usando o acesso direto a dados alterados, saiba que o suporte ao produto não poderá ajudar! 
  
Os aplicativos que acessam diretamente as tabelas e exibições de rascunho, publicadas ou arquivadas também dependem dos esquemas do banco de dados, que podem ser alterados nos pacotes de serviços ou nas versões posteriores do Project Server 2013. Os aplicativos que acessam diretamente os bancos de dados também perdem a segurança integrada do Project Server, a lógica de negócios comum, o rastreamento, as auditorias, a verificação de erros, os relatórios, o fluxo de trabalho e outros recursos. Você provavelmente teria que reescrever tal aplicativo após as atualizações do Project Server 2013. 
  
Por todas essas razões, o Project Professional e o Project Web App não fazem chamadas diretas para as tabelas de rascunho, publicadas ou arquivadas; nem para qualquer outro aplicativo que se integre ao Project Server.
  
Os esquemas para as tabelas de rascunhos, publicados e arquivados não são documentados. Você pode usar as tabelas de relatórios para ajudar a gerar relatórios, e o esquema para as tabelas e exibições de relatórios está documentado no download do SDK do Project 2013. Para esquema OData de dados de relatórios, confira [ProjectData - referência do serviço OData do Project](https://docs.microsoft.com/previous-versions/office/project-odata/jj163015(v=office.15)).
  
## <a name="see-also"></a>Confira também

- [Atualizações para desenvolvedores do Project 2013](updates-for-developers-in-project-2013.md)    
- [Arquitetura do Project Server 2013](project-server-2013-architecture.md)    
- [O que a PSI faz e não faz](what-the-psi-does-and-does-not-do.md)   
- [O que o CSOM faz e não faz](what-the-csom-does-and-does-not-do.md)    
- [Modelo de objeto do cliente (CSOM) para o Project 2013](client-side-object-model-csom-for-project-2013.md)    
- [Introdução ao desenvolvimento de fluxos de trabalho do Project Server](getting-started-developing-project-server-workflows.md)    
- [Referências de programação do Project 2013](project-2013-programming-references.md)    
- [Visão geral da referência da PSI do Project](project-psi-reference-overview.md)    
- [Criar ações personalizadas para implantação com aplicativos do SharePoint](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/create-custom-actions-to-deploy-with-sharepoint-add-ins)    
- [Apresentamos as tarefas inativas no Project 2010](https://blogs.msdn.com/b/project/archive/2010/06/10/introducing-inactive-tasks-in-project-2010.aspx)    
- [Project Server 2010: Agendamento na Web, PSI e Project Professional](https://blogs.msdn.microsoft.com/brismith/2010/09/10/project-server-2010-scheduling-on-the-web-the-psi-and-project-professional/)

