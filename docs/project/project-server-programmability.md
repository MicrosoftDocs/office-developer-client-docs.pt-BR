---
title: Programabilidade do Project Server
manager: soliver
ms.date: 09/17/2015
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
- Project 2013, versões de arquitetura e os recursos de programação, PSI, projetos, recursos de programação, Project Server, PSI, limitações, Interface do Project Server, sem suporte genérico de compatibilidade, a Interface do Project Server, PDS recursos, Interface do Project Server, Project Server, project projetos de versões, versões, Project Server, bancos de dados, Project 2013, plataforma, Interface do Project Server, utilize os eventos de cenários, Project Server, Project Server, o serviço de dados do Project, compatibilidade com PSI, Project Server Interface
localization_priority: Normal
ms.assetid: a93d2153-5132-4289-af51-69350471e248
description: Saiba mais sobre os recursos de programação principais no Project Server 2013. Este artigo inclui informações sobre portando aplicativos que foram desenvolvidos para versões anteriores do Project Server.
ms.openlocfilehash: f3901fe97f1c8291d0b35709f2350fc4358044b4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592980"
---
# <a name="project-server-programmability"></a>Programabilidade do Project Server

Saiba mais sobre os recursos de programação principais no Project Server 2013. Este artigo inclui informações sobre portando aplicativos que foram desenvolvidos para versões anteriores do Project Server.

Project Server 2013 foi projetado para atender a maioria dos aplicativos que foram desenvolvidos para o Project Server 2010 e novas soluções para várias plataformas, onde aplicativos podem acessar ambos online e instalações do Project Server no local. Aplicativos e extensões que foram desenvolvidas para o Project Server 2003 ou anterior devem ser reprojetadas para usar o modelo de objeto do cliente (CSOM) ou o Project Server Interface (PSI). Aplicativos que foram desenvolvidos para o Office Project Server 2007 ou do Project Server 2010 podem exigir algumas alterações e recompilar para usar a PSI; Para usar o CSOM, esses aplicativos requerem uma reformulação.
  
A plataforma do Project Server habilita altos níveis de produtividade do programador com base no SharePoint Server 2013, o protocolo OData com o CSOM e .NET Framework 4. Os desenvolvedores podem estender o Project Web App com aplicativos e partes do app Web Parts, definir fluxos de trabalho usando o SharePoint Designer 2013 e impor regras comerciais usando os receptores de evento remoto para eventos do Project Server.
  
## <a name="project-server-and-sharepoint-server"></a>Project Server e SharePoint Server
<a name="pj15_Programmability_MOSS"> </a>

Project Web App baseia-se o SharePoint Server 2013 e usa páginas mestras e Web Parts para facilitar a criar aplicativos personalizados e soluções de Project Web App. Project Server 2013 integra-se totalmente com o SharePoint Server 2013 como plataforma para colaboração em projetos, relatórios, administração do site, segurança e gerenciamento de fluxo de trabalho.
  
Os sites de projeto incluem mais informações e opções de colaboração para os membros da equipe, onde você pode adicionar aplicativos padrão que incluem um projeto de listas do SharePoint de resumo, especializado para tarefas com um cronograma, acompanhamento de problemas, riscos, produtos, do project e o calendário de equipe, juntamente com as discussões de biblioteca e equipe do documento. Aplicativos personalizados do Project Server 2013 fornecem extensões e flexibilidade para colaboração de equipe. Você também pode adicionar parts app para personalizar um aplicativo, usando o mesmo mecanismo para adicionar e editar Web Parts quando você edita uma página. Você pode localizar os sites de projeto em qualquer lugar no farm do SharePoint onde o Project Server está instalado. Para usar outros serviços principais do SharePoint Server 2013, serviços do Excel e de pesquisa corporativa, um administrador pode habilitar e configurar os serviços. 
  
Quando você instala o Project Server 2013, você pode provisionar o aplicativo de serviço do Project no site do SharePoint Web Services. O aplicativo de serviço do projeto inclui os serviços locais do Windows Communication Foundation (WCF) e ASMX web services para a PSI. Outros aplicativos de serviço exemplos de pesquisa do SharePoint e o gerenciamento de documentos do SharePoint. Para obter mais informações, consulte a documentação do desenvolvedor do SharePoint Server 2013.
  
O aplicativo de serviço do projeto é um provedor de serviço lógico que pode gerenciar várias instâncias do Project Web App. Configuração do Project Server cria um site específico do Project Web App em um aplicativo da web do SharePoint. Home page do Project Web App contém links para a página Central de projetos, página Central de recursos e a página da Central de Business Intelligence para relatórios, além de uma página que contém uma lista de aplicativos padrão adicionais. A Figura 1 mostra o comando **Editar página** na lista suspensa **configurações** na Home page do Project Web App, que permite que você adicionar ou editar Web Parts. 
  
> [!NOTE]
> Algumas páginas administrativas no Project Web App — como a página Configurações do PWA — não são editáveis e não mostrar o comando **Editar página** . Project Web App não permite a edição de páginas usando o SharePoint Designer 2013. Você pode editar páginas de site de projeto com o SharePoint Designer 2013. 
  
**Figura 1. Usando o menu Editar página no Project Web App**

![Editando a Home page do Project Web Access] (media/pj15_Programmability_PWAHome.gif "Editando a Home page do Project Web Access")
  
Para acessar a página Configurações do Site no Project Web App, escolha o ícone de **configurações** no canto superior direito da página. Página Configurações do Site ( `http://ServerName/ProjectServerName/_layouts/15/settings.aspx`) permite alterar a aparência e o tema do site, adicionando Web Parts personalizadas e modificando ou criando páginas para sites de projeto mestre.
  
Personalização do código em páginas ASPX ou personalização de páginas mestras do Project Web App com o SharePoint Designer 2013, não é suportada. Personalização do código nas páginas do Project Web App pode causar problemas com os service packs e atualizações do Project Server. 
  
### <a name="customization-of-project-web-app-with-sharepoint-packages"></a>Personalização do Project Web App com os pacotes do SharePoint
<a name="pj15_Programmability_CustomizationOfPWA"> </a>

Como o Project Web App é um aplicativo do SharePoint e sites de projetos são sites do SharePoint, você pode adicionar aplicativos personalizados, Web Parts, manipuladores de eventos, campos personalizados e outros recursos usando pacotes (arquivos. wsp) do SharePoint ou aplicativos do SharePoint (.spapp arquivos). Um pacote do SharePoint ou um pacote de aplicativos pode incluir várias entidades do Project Server, onde as definições de entidade são especificadas em um arquivo Elements. XML dentro do pacote.
  
Para o Project Online, você pode adicionar botões à faixa de opções do Project Web App, mas não é possível remover ou renomear botões existentes do produto, e não é possível criar novas guias da faixa de opções. Para obter mais informações, consulte [criar ações personalizadas para implantação com aplicativos do SharePoint](http://msdn.microsoft.com/en-us/library/office/apps/jj163954%28v=office.15%29.aspx).
  
> [!CAUTION]
> Ao instalar um pacote do SharePoint ou um pacote de aplicativos, os tipos de entidades do Project Server devem aparecer na ordem que especifica o esquema de PSEntityProvision.xsd ou falha de validação de esquema do pacote e a instalação não for concluída. 
  
O arquivo de esquema PSEntityProvision.xsd está disponível no download do SDK do Project 2013, no `Documentation\Schemas\AppProvisioning` subdiretório. A Figura 2 mostra o modo de exibição do Gerenciador de esquema XML no Visual Studio do esquema de **PSEntityProvision** , onde a sequência de **LookupTable** é expandida. 
  
**Figura 2. Modo de exibição Visual Studio da entidade do Project Server no esquema de provisionamento**

![Modo de exibição do esquema de entidade do Project Server] (media/pj15_Programmability_EntitySchema.gif "Modo de exibição do esquema de entidade do Project Server")
  
Pacotes do SharePoint que instalar recursos para o Project Server podem conter um ou mais arquivos Elements. XML que seguem o esquema de **PSEntityProvision** . As entidades do Project Server em um único arquivo XML devem aparecer na seguinte ordem: 
  
1. Fases do fluxo de trabalho
    
2. Tabelas de pesquisa
    
3. Campos personalizados
    
4. Estágios do fluxo de trabalho
    
5. Tipos de projeto corporativo
    
6. Manipuladores de eventos
    
Quando você cria um pacote do SharePoint que contém as entidades do Project Server, é possível colocar as definições de entidade em vários arquivos de Elements. XML. Cada arquivo XML poderia passar a validação de esquema, mas as entidades no pacote completo podem não ser na ordem correta. Por exemplo, uma entidade de campo personalizado no arquivo XML primeiro poderia se referir a uma tabela de pesquisa no segundo arquivo XML. Durante a instalação, o campo personalizado não pode ser criado porque a tabela de pesquisa ainda não tiver sido criada.
  
Se um pacote de instalação falhar, os objetos que foram criados permanecem no Project Web App, mas o pacote não foi instalado completamente. Reinstalar o pacote pode funcionar, mas isso não é uma boa experiência para os clientes. Quando as definições de entidade abrangem vários arquivos Elements. XML, organize as entidades do Project Server em todo o pacote do SharePoint para garantir que a instalação segue a ordem correta. Com o esquema de PSEntityProvision.xsd no download do SDK do Project 2013, é possível desenvolver uma ferramenta que verifica a ordem indicada das entidades nos arquivos XML.
  
## <a name="upgrading-applications-with-the-project-server-apis"></a>Atualizando aplicativos com as APIs do Project Server
<a name="pj15_Programmability_APIs"> </a>

Quando você atualiza um aplicativo que foi desenvolvido para uma versão anterior do Project Server, você pode optar por usar o CSOM ou a PSI para uma interface de programação que inclui métodos para criar, ler, atualizar e excluir entidades de projeto (as operações CRUD). Embora o CSOM internamente chama a PSI, ele não substitui totalmente todos os métodos PSI. Para cenários e limitações do PSI e do CSOM do, consulte [o que o PSI e não faz](what-the-psi-does-and-does-not-do.md) e [o que o CSOM faz e não faz](what-the-csom-does-and-does-not-do.md).
  
> [!NOTE]
> Se o CSOM inclui a funcionalidade que necessária, é recomendável que você atualize aplicativos para usar o CSOM. O CSOM permite que os aplicativos a serem usados para locais e online instalações do Project Server 2013. 
  
Se seu aplicativo principalmente lê os dados do Project Server, você pode usar as tabelas e modos de exibição de relatórios no banco de dados do Project Server para um cenário no local. Se você pretende usar o aplicativo com o Project Online, você pode usar o protocolo OData para o serviço **ProjectData** , que fornece o local e online acesso aos dados de relatórios. Para obter mais informações, consulte [ProjectData - Referência de serviço OData de projeto](https://msdn.microsoft.com/en-us/library/office/jj163015.aspx)
  
### <a name="using-the-psi"></a>Usando a PSI
<a name="pj15_Programmability_PSI"> </a>

A PSI permite que os aplicativos de cliente de confiança total, incluindo aplicativos LOB, Project Web App e Project Professional 2013, para acessar dados do Project Server em um farm do SharePoint. A PSI é criada e usada com o .NET Framework 4 e oferece vantagens como um ambiente de desenvolvimento conhecido com segurança integrada, coleta de lixo e tratamento de erros.
  
A PSI é acessada por meio de serviços WCF ou serviços web ASMX. A interface ASMX baseia-se no WCF. Cada serviço PSI normalmente contém uma classe de base com métodos CRUD para itens dentro dessa classe. Itens são especificados pelas classes de **conjunto de dados** relacionados. Por exemplo, o serviço de **CustomFields** contém a classe **CustomFields** com métodos como [CreateCustomFields2](https://msdn.microsoft.com/library/WebSvcCustomFields.CustomFields.CreateCustomFields2.aspx) . Dados para um ou mais campos personalizados da empresa são especificados no **CustomFieldDataSet**.
  
> [!NOTE]
> A interface de serviços web ASMX do PSI foi preterida no Project Server 2013. Embora a interface ASMX ainda esteja disponível, novos aplicativos que usam a PSI devem usar a interface WCF ou, se possível, novos aplicativos devem usar o CSOM em vez da PSI. Futuras versões do Project Server exigirá uma atualização dos aplicativos de baseados em ASMX existentes para usar a interface WCF de PSI ou para usar o CSOM. 
  
Existem 22 público, documentados serviços PSI, que são duplicados na interface do WCF e a interface ASMX. A PSI também inclui oito particulares, não documentados os serviços. Project Web App e do Project Professional usam os serviços públicos de PSI e os serviços PSI privados. A PSI geralmente é acrescentada para coincidir com os objetos de negócios. Ou seja, cada método PSI é associado um objeto de negócios, como **recursos**ou **calendário** . A PSI é a interface principal para os objetos de negócios. Como a camada de negócios fornece os componentes de lógica de negócios reutilizável, diferentes aplicativos que interagem com dados do Project Server usam a mesma lógica de negócios.
  
Métodos PSI que assincronamente interagem com o Project Server têm nomes que começam com a **fila**. Cada método PSI é implementado com uma interface separada que usa fortemente tipadas dados. Por exemplo, o método **QueueCreateProject** no serviço do **projeto** aceita o parâmetro do _conjunto de dados_ do tipo **ProjectDataSet**. A classe **ProjectDataSet** deriva o tipo de **conjunto de dados** . Digite o check-in a conclusão do .NET Framework e IntelliSense na Ajuda do Visual Studio para reduzir os erros de desenvolvimento com a PSI. Para obter uma introdução à referência detalhada para PSI namespaces, classes, propriedades, métodos, eventos e assemblies relacionados, consulte [Visão geral da referência do Project PSI](project-psi-reference-overview.md).
  
Project Server 2013 usa o tratamento de exceção do .NET Framework. Todos os erros são registrados no servidor, na parte superior da pilha PSI. Alguns erros envia um relatório simple para o cliente, como um objeto **SoapException** para a interface ASMX ou um objeto **FaultException** para a interface WCF. Exceções poderão ser registradas no log de eventos de aplicativo e alguns erros também registram um relatório detalhado no servidor nos logs de rastreamento Unified Logging Service (ULS). 
  
Para aplicativos de confiança total do locais, a PSI também é extensível. Você pode adicionar um assembly do .NET com um serviço que fornece a nova funcionalidade, usa a mesma infraestrutura de segurança do Project Server e chama outros métodos PSI ou herda das classes PSI. Uma extensão PSI também pode fornecer o acesso de banco de dados e lógica de negócios necessário para a nova funcionalidade.
  
### <a name="using-the-csom"></a>Usando o CSOM
<a name="pj15_Programmability_CSOM"> </a>

Com o CSOM, você pode desenvolver aplicativos que acessam o Project Online ou uma instalação do Project Server 2013 local. Aplicativos podem ser distribuídos em um Office Store pública ou um catálogo de aplicativos privado. O CSOM foi projetado para ser uma API de fácil utilização que consome diretamente ou fornece dados pelo nome com consultas LINQ, em vez de passagem de conjuntos de dados e construção de parâmetros _changeXml_ ou os parâmetros de _filtro_ XML. O CSOM implementa a funcionalidade principal do Project Server Interface (PSI) para as entidades principais, como o **projeto**, **tarefa**, **atribuição**e **EnterpriseResource**. O CSOM inclui muitas entidades adicionais, como **CustomField**, **LookupTable**, **WorkflowActivities**, **EventHandler**e **QueueJob**, que oferece suporte a outras funcionalidades comuns do Project Server.
  
O CSOM pode ser usado, copiando os seguintes recursos para o seu computador de desenvolvimento local:
  
- Para o desenvolvimento do .NET Framework 4, copie o `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\ISAPI\Microsoft.ProjectServer.Client.dll` assembly. 
    
  Para a documentação das classes CSOM e membros, consulte o namespace [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) . Para um aplicativo de exemplo, consulte o [guia de Introdução ao CSOM e .NET](getting-started-with-the-project-server-csom-and-net.md).
    
- Para o desenvolvimento do Microsoft Silverlight, copie o `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\ClientBin\Microsoft.ProjectServer.Client.Silverlight.dll` assembly. 
    
- Para desenvolver aplicativos para Windows Phone 8, copie o `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\ClientBin\Microsoft.ProjectServer.Client.Phone.dll` assembly. 
    
- Para usar o JavaScript para o desenvolvimento de aplicativos web e aplicativos para outros dispositivos, copie o `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\PS.js` arquivo e o `PS.debug.js` arquivo. Para um aplicativo web de exemplo, consulte o [guia de Introdução do modelo de objeto JavaScript do Project Server 2013](getting-started-with-the-project-server-2013-javascript-object-model.md).
    
O CSOM internamente chama a PSI; Portanto, se a PSI não pode fazer um trabalho, nem podem o CSOM. Para limitações do CSOM do, consulte [o que o CSOM e não faz](what-the-csom-does-and-does-not-do.md) e [o que o PSI faz e não faz](what-the-psi-does-and-does-not-do.md). Para obter mais informações sobre o desenvolvimento com o CSOM, consulte [atualizações para desenvolvedores no Project 2013](updates-for-developers-in-project-2013.md) e [o modelo de objeto do lado do cliente (CSOM) para o Project 2013](client-side-object-model-csom-for-project-2013.md).
  
### <a name="porting-applications-built-for-project-server-2003"></a>Portando aplicativos integrados para Project Server 2003
<a name="pj15_Programmability_Porting2003"> </a>

No Project Server 2003, quantidade dados e a funcionalidade está disponível somente com o Project Professional 2003 ou pelo acesso direto do banco de dados. A PSI, introduzida no Project Server 2007, remove grande parte dessa restrição. Ao contrário do Project Data Service (PDS) no Project Server 2003, a PSI e CSOM do fornecem interfaces abrangentes aos objetos de negócios no Project Server.
  
Os aplicativos desenvolvidos para o PDS não são compatíveis com versões anteriores do Project Server. O CSOM e a PSI fornecem paridade funcional para o PDS, mas não coincidem com os métodos PDS ou parâmetros.
  
> [!NOTE]
> Porque aplicativos PDS devem ser completamente reprojetados para Project Server 2013, recomendamos que você use o CSOM. 
  
Para obter mais informações sobre a compatibilidade PDS e diretrizes para portando extensões PDS para o PSI feitas, consulte [PDS paridade em serviços da Web de PSI](http://msdn.microsoft.com/library/61a0b0c7-9b74-46d1-87ed-66ffdd8017f8%28Office.15%29.aspx).
  
### <a name="porting-applications-built-for-project-server-2007-and-project-server-2010"></a>Portando aplicativos integrados do Project Server 2007 e Project Server 2010
<a name="pj15_Programmability_Porting2007"> </a>

A PSI no Project Server 2013 é um subconjunto do modelo de objeto PSI no Office Project Server 2007 e Project Server 2010. Muitos aplicativos desenvolvidos para as duas versões anteriores do Project Server continuam a trabalhar em instalações de local de confiança total, local do Project Server 2013. No entanto, os seguintes tipos de aplicativos requerem atualizações ou reformulação:
  
- Use o CSOM para aplicativos que são adaptados para uso com o Project Online.
    
- Use o CSOM para aplicativos que são adaptados para uso em dispositivos móveis e tablet PCs.
    
- Use o CSOM para aplicativos que estão disponíveis como aplicativos na Office Store ou um catálogo de aplicativos privado.
    
- Para aplicativos que modificam o agendamento do projeto, use o CSOM ou altere o aplicativo para usar o método PSI [QueueUpdateProject2](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject2.aspx) . 
    
- Local ou aplicativos da web que o logon de usuários diferentes instâncias do Project Web App devem usar as configurações programáticas para pontos de extremidade do WCF do CSOM do ou a PSI. Os métodos foram eliminados. Aplicativos devem usar a autenticação OAuth no lugar de autenticação de formulários e para uso com o Project Online. Para obter mais informações, consulte [autorização e autenticação para aplicativos no SharePoint 2013](http://msdn.microsoft.com/en-us/library/fp142384%28office.15%29.aspx#FileName_uniquekeyword1).
    
- Aplicativos que dependem ou modificar as configurações de segurança do Project Server específicas.
    
  > [!NOTE]
  > Uma instalação do local padrão do Project Server 2013 usa o modo de permissão do SharePoint, onde as configurações de segurança do Project Server não são acessíveis através do PSI. Para alterar o modo de permissão do Project, consulte a seção de *Modo de permissão do SharePoint* no [que há de novo para profissionais de TI no Project Server 2013](http://technet.microsoft.com/en-us/library/ff631142%28office.15%29.aspx#section13). 
  
- Para muitos personalizados do Project Server fluxos de trabalho, você pode usar o SharePoint Designer 2013 para criar fluxos de trabalho declarativos. Para fluxos de trabalho personalizados que exigem programação adicional, você deve diretamente usar *não* membros ou classes no namespace **Microsoft.Office.Project.Server.Workflow** . Em vez disso, use a classe de [Microsoft.ProjectServer.Client.WorkflowActivities](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.WorkflowActivities.aspx) no CSOM. 
    
- Em geral, os aplicativos que utilizam a representação devem ser reconfigurados para usar a interface WCF de PSI. Aplicativos que fazem atualizações de status simples para outros usuários não necessitam de representação. Eles podem usar o método [StatusAssignment.SubmitStatusUpdates](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.StatusAssignment.SubmitStatusUpdates.aspx) o CSOM ou o método [Statusing.SubmitStatusForResource](https://msdn.microsoft.com/library/WebSvcStatusing.Statusing.SubmitStatusForResource.aspx) a PSI. 
    
- Componentes de middleware que são executados no computador do Project Server podem ser instalados somente para uso no local e devem usar a interface WCF de PSI. Por exemplo, um componente de middleware que usa o ASMX interface para trocar dados entre o Project Web App no local e um aplicativo de quadro de horários externo teria a ser reconfigurado para usar a interface WCF de PSI. Para trabalhar com o Project Online, o componente teria que ser reprojetada como um aplicativo e usar o CSOM.
    
### <a name="migration-and-compatibility-of-custom-solutions"></a>Migração e compatibilidade de soluções personalizadas
<a name="pj15_Programmability_CustomSolutions"> </a>

Classes e os membros das interfaces ASMX e WCF públicas da PSI são idênticos. Mas, o número de colunas e o tamanho de tabelas de dados usados ou retornados por métodos PSI podem ser diferentes entre as duas versões anteriores do Project Server e o Project Server 2013. Também há diferenças nas tabelas e modos de exibição, em comparação com o banco de dados de relatórios nas versões anteriores a geração de relatórios.
  
> [!IMPORTANT]
> É altamente recomendável que você teste exaustivamente soluções em uma instalação de não-produção do Project Server 2013 antes de implantá-las para um servidor de produção. 
  
Quando você migrar uma solução para o Project Server 2013, ou se uma solução não funcionar conforme o esperado, você deve no mínimo, faça o seguinte:
  
- Atualize a solução abrindo-o no Visual Studio 2012. Algumas soluções também podem usar o Visual Studio 2010.
    
- Altere o destino para o .NET Framework 4.
    
- Referências de assembly de alteração para usar os assemblies do Project Server 2013, como Microsoft.Office.Project.Server.Library.dll e Microsoft.Office.Project.Server.Events.Receivers.dll.
    
- Faça uma lista das referências de web ASMX ou as referências de serviços do WCF e nomes de namespace e, em seguida, exclua as referências do Project Server.
    
- Adicione o assembly de proxy ProjectServerServices.dll que você pode construir os WCF proxy dos arquivos de origem no download do SDK do Project 2013, ou adicionar os arquivos de origem de proxy para os serviços WCF necessários. Para os serviços ASMX, adicione as referências de serviço de web front-end do ASMX novamente, usando os mesmos nomes de namespace; ou adicione o assembly de proxy ProjectServerServices.dll que você pode construir das fontes WSDL no download do SDK do Project 2013.
    
  > [!NOTE]
  > No download do SDK do Project 2013, os espaços para nome da fonte de proxy arquivos todas iniciadas pela *Svc* . Por exemplo, o namespace de serviço do **recurso** no arquivo de proxy de WCF e no arquivo ASMX proxy é **SvcResource**. > Se o aplicativo usa os nomes de namespace diferente, você pode recompilar o assembly de proxy para usar seu namespaces ou alterar os namespaces PSI em seu aplicativo. Por exemplo, você pode modificar o script CompileWCFProxyAssembly.cmd e recompilar ProjectServerServices.dll os proxy dos arquivos de origem no download do SDK. 
  
- Se você alterar usem a interface ASMX de PSI para a interface WCF, você pode inicializar as classes de cliente programaticamente ou por meio de pontos de extremidade do WCF em App. config. Use programática inicialização quando você precisar alternar rapidamente para diferentes instâncias do Project Web App, ou quando você estiver desenvolvendo uma web part que usa a PSI.
    
- Há vários métodos de novos e conjuntos de dados nos serviços de PSI no Project Server 2013 e algumas classes **DataRow** contêm novas propriedades. Por exemplo, o método [QueueUpdateProject2](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject2.aspx) a PSI usa o Project Server mecanismo de agendamento para reagendar um projeto atualizado sem que seja necessário abrir o projeto no Project Professional 2013 e também permite a adição ou exclusão de entidades de projeto no a mesma chamada. 
    
- Compilar e testar a solução.
    
## <a name="project-scheduling-on-the-server"></a>Agendamento no servidor do projeto
<a name="pj15_Programmability_Scheduling"> </a>

Project Server 2013 tem dois mecanismos de agendamento. O mecanismo de agendamento mais recente é o mesmo que o mecanismo de agendamento no Project Professional 2013. Quando você fizer alterações de agendamento e publica as alterações usando a web part de agendamento (página de detalhes do projeto) no Project Web App ou um site de projeto, ou usando o CSOM, o cálculo de datas, custos, duração, restante do trabalho, as linhas de base e outras alterações relacionadas para agendar são os mesmos como se você fez as alterações e publicado do projeto usando o Project Professional 2013. Contudo, exceto para o método [QueueUpdateProject2](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject2.aspx) , os métodos da PSI usam o mecanismo de agendamento mais antigo que foram migrado do Project Server 2010. O motivo é garantir que aplicativos herdados se comportam da mesma no Project Server 2013 como faziam anteriormente. 
  
> [!NOTE]
> Para usar o mecanismo de agendamento atualizado no Project Server 2013, aplicativos podem usar o CSOM. 
  
O mais antigos e os mecanismos de agendamento mais recentes têm as seguintes limitações:
  
- **Único projeto somente de agendamento** Agendamento afeta apenas o projeto atual, quando as alterações são feitas por meio de atualizações de status da tarefa com a PSI ou CSOM do ou com o Project Web App. Se o projeto atual tiver links para outros projetos, subprojetos ou projetos mestres, os projetos vinculados não são alterados. 
    
- **Tarefas de resumo** Tarefas de resumo são geralmente somente leitura no Project Server. Por exemplo, atribuições, tarefas de resumo não podem ser criadas e conclusão percentual não pode ser modificado. No entanto, Project Server oferece suporte a edição as datas e a duração das tarefas de resumida agendadas manualmente. 
    
    Dados efetivos no Project Server não são adicionados automaticamente a uma atribuição de tarefa de resumo, pois que seria ignorar o processo de aprovação no Project Server. No Project Professional, quando você adiciona dados efetivos para uma subtarefa, os dados efetivos também são adicionados para uma atribuição na tarefa de resumo. A diferença no comportamento poderá ser confusa para um usuário.
    
    Project Server exclui dados efetivos em uma atribuição de tarefa de resumo, se a duração de subtarefa abrevia ou a data de término for alterada.
    
    > [!CAUTION]
    > Embora o Project Professional pode executá-la, é recomendável que você não faça atribuições nas tarefas de resumo. 
  
Estes são os problemas e limitações de programação de PSI com o Project Server mais antigos agendamento no mecanismo:
  
- **Alterando o status ativo de uma tarefa** O mecanismo de agendamento mais antigo do Project Server pode mostrar inconsistente iniciar ou terminar vezes quando você usar o método [QueueUpdateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject.aspx) para alterar o status ativo de uma tarefa, se houver várias alterações no objeto **ProjectDataSet** para o _ DataSet_ parâmetro. Se a propriedade **TASK_IS_ACTIVE** for a única alteração no parâmetro _dataset_ do **QueueUpdateProject**, você poderá atualizar o projeto.
    
    Para obter mais informações sobre tarefas inativas e o mecanismo de agendamento mais antigo, consulte o blog articles [Introducing de tarefas inativas no Project 2010](http://blogs.msdn.com/b/project/archive/2010/06/10/introducing-inactive-tasks-in-project-2010.aspx) e [Project Server 2010: agendamento na web, o Project Professional e PSI](http://blogs.msdn.com/b/brismith/archive/2010/09/10/project-server-2010-scheduling-on-the-web-the-psi-and-project-professional.aspx?wa=wsignin1.0). Para obter uma comparação de agendamento no Project Professional 2010 e do Project Web App no Project Server 2010, consulte [comparação de gerenciamento de agenda baseado na Web](https://blogs.msdn.microsoft.com/brismith/2010/09/10/project-server-2010-scheduling-on-the-web-the-psi-and-project-professional/).
    
- **Valor acumulado não calculada** O mecanismo de agendamento mais antigo não calculam os campos de valor acumulado: CRTR, OAT, COTR, cota, IDC, VC, VC %, EAT, EDA, VA, VA %, IDAC, VAT, variação da duração, variação inicial, variação do término, variação de custo e variação do trabalho. Se um projeto tem valores para esses campos e o projeto é atualizado, usando o método **QueueUpdateProject** , não alteram os valores do campo. Para evitar o problema, use o método **QueueUpdateProject2** . 
    
Você pode manipular a PSI agendamento limitações das seguintes maneiras:
  
- Se o CSOM tiver os métodos que requer que o aplicativo, use o CSOM em vez da PSI.
    
- Abrir projetos no Project Professional e salvá-los para o Project Server.
    
- Em relatórios, não inclua os campos que não atualiza a PSI.
    
- Adicione uma nota nos relatórios sobre os dados que podem ser atualizados.
    
Há sinalizadores nas tabelas de relatórios e os cubos que ajudarão-lo a detectam quando alguns dados do projeto não são atualizados. Os dados de relatórios na tabela MSP_EpmProject e em MSP_EpmProject_UserView incluem os seguintes campos: 
  
-  _ProjectWbsIsStale_ &ndash; Indica se a estrutura de divisão de trabalho (hierarquia da estrutura de tópicos de tarefas) é obsoleta. 
    
-  _ProjectEarnedValueIsStale_ &ndash; Indica que os campos de valor acumulado estão obsoletos. 
    
-  _ProjectRollupsAreStale_ &ndash; Indica que um subprojeto é atualizado no banco de dados de rascunho, mas o projeto mestre não é atualizado. Os valores acumulados do subprojeto estão obsoletos. 
    
-  _ProjectHierarchyNotSynchronized_ &ndash; o projeto mestre não está sincronizado com os seus filhos. Isso acontece quando os projetos de filhos são publicados explicitamente, e não como parte de publicação do projeto mestre. 
    
-  _ProjectCalculationsAreStale_ &ndash; Project Professional salva um projeto sem calcular o cronograma (ou seja, o modo de cálculo está definido como **Manual** na guia **agenda** na caixa de diálogo **Opções do projeto** ). 
    
-  _ProjectGhostTaskAreStale_ &ndash; Semelhante ao _ProjectHierarchyNotSynchronized_, mas avisa nos dados de link entre projetos. É possível que não existe nenhum projeto mestre, mas os dados de projeto em um lado do link fiquem mais recentes do que no outro lado.
    
## <a name="about-accessing-the-project-server-database"></a>Sobre como acessar o banco de dados do Project Server
<a name="pj15_Programmability_Databases"> </a>

Se você tiver permissões no Microsoft SQL Server para acessar o banco de dados do Project Server, você pode ler as tabelas e modos de exibição de relatórios. Se você tiver as permissões necessárias do Project Server, você também pode ler dados das tabelas de relatórios usando consultas OData. Os desenvolvedores Desencorajamos acessem diretamente o rascunho, publicado, ou arquivar tabelas através de consultas do SQL Server no banco de dados do Project Server. Fazendo alterações diretas em qualquer uma das tabelas do banco de dados do Project Server pode danificar a integridade referencial e interferir no acesso do banco de dados por meio do serviço de enfileiramento do Project Server.
  
> [!IMPORTANT]
> Não há nada a ativamente impedir o uso de acesso direto programático banco de dados para atualizar dados. Você deve estar ciente de que o cache do Project Professional, as tabelas publicadas e as tabelas de relatório se baseiam em um protocolo de sincronização do cache que pode ser interrompido por meio da edição diretos dados. Se você danificar seu banco de dados do Project Server ou corromper o Project Professional do cliente armazena em cache usando o acesso direto para alterar os dados, ser avisado que suporte ao produto não poderão ajudar! 
  
Aplicativos que acessam diretamente o rascunho, publicado ou arquivar tabelas e modos de exibição também são dependentes de esquemas de banco de dados, que podem ser alterada no service packs ou versões posteriores do Project Server 2013. Aplicativos que acessem diretamente os bancos de dados também perdem a segurança integrada do Project Server, a lógica de negócios comuns, rastreamento, auditorias, verificação de erros, relatórios, fluxo de trabalho e outros recursos. Provavelmente você teria reescrever esse aplicativo depois de atualizações do Project Server 2013. 
  
Para todos esses motivos, Project Professional e do Project Web App não fazer chamadas diretas para o rascunho, publicado, ou arquivar tabelas; deve nem qualquer outro aplicativo que se integra com o Project Server.
  
Os esquemas para o rascunho, publicado, e tabelas de arquivo morto não estão documentadas. Você pode usar as tabelas de relatório para ajudar a gerar relatórios e o esquema para as tabelas e modos de exibição de relatórios está documentado no download do SDK do Project 2013. Para o esquema de OData de dados de relatórios, consulte [ProjectData - Referência de serviço OData do projeto](https://msdn.microsoft.com/en-us/library/office/jj163015.aspx).
  
## <a name="see-also"></a>Confira também

- [Atualizações para desenvolvedores no Project 2013](updates-for-developers-in-project-2013.md)    
- [Arquitetura do Project Server 2013](project-server-2013-architecture.md)    
- [O que o PSI faz e não faz](what-the-psi-does-and-does-not-do.md)   
- [O que o CSOM faz e não faz](what-the-csom-does-and-does-not-do.md)    
- [Modelo de objeto do cliente (CSOM) para o Project 2013](client-side-object-model-csom-for-project-2013.md)    
- [Introdução ao desenvolvimento de fluxos de trabalho do Project](getting-started-developing-project-server-workflows.md)    
- [Referências de programação do Project 2013](project-2013-programming-references.md)    
- [Visão geral da referência PSI do Project](project-psi-reference-overview.md)    
- [Criar ações personalizadas implante com aplicativos para SharePoint](http://msdn.microsoft.com/en-us/library/office/apps/jj163954%28v=office.15%29.aspx)    
- [Apresentando tarefas inativas no Project 2010](http://blogs.msdn.com/b/project/archive/2010/06/10/introducing-inactive-tasks-in-project-2010.aspx)    
- [Project Server 2010: Agendamento na Web, a PSI e o Project Professional](https://blogs.msdn.microsoft.com/brismith/2010/09/10/project-server-2010-scheduling-on-the-web-the-psi-and-project-professional/)

