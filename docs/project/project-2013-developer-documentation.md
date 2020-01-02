---
title: Documentação do desenvolvedor do Project 2013
manager: lindalu
ms.date: 12/19/2019
ms.audience: Developer
f1_keywords:
- Project
- Project 2013
- Project 2013 SDK
- Project programmability
- Project SDK
- SDK
- SDK Project
keywords:
- SDK, visão geral do project 2013, o Project 2013 SDK
ms.assetid: f66adbf1-5cb5-4dd0-be08-45e1c88c010c
description: Localize documentação, exemplos de código, artigos de instruções e referências de programação para ajudar a criar aplicativos para o Office ou um catálogo de aplicativos privados; e para personalizar e integrar clientes do Project Server e do Project a uma ampla variedade de outros aplicativos da área de trabalho e de negócios para o gerenciamento de projeto corporativo.
localization_priority: Priority
ms.openlocfilehash: 1b6227bb25810be04bc87abb418f9966b593bf1c
ms.sourcegitcommit: 55205b4ec1376713d31e75d195e031798fb2c6ad
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/20/2019
ms.locfileid: "40825755"
---
# <a name="project-2013-developer-documentation"></a>Documentação do desenvolvedor do Project 2013

Localize documentação, exemplos de código, artigos de instruções e referências de programação para ajudar a criar aplicativos para a AppSource. Saiba como personalizar e integrar clientes do Project Server e do Project a uma ampla variedade de outros aplicativos da área de trabalho e de negócios para o gerenciamento de projeto corporativo (EPM).
   
> [!NOTE]
> O Project Server 2013 foi criado na plataforma SharePoint Server 2013 e o Project 2013 inclui grande parte da mesma infraestrutura que os outros aplicativos do Office 2013. Para obter documentação do modelo para suplementos do SharePoint, fluxos de trabalho baseados no SharePoint, Web Parts, desenvolvimento com outros recursos do SharePoint e documentação de suplementos do Office, confira[Suplementos do SharePoint](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins) e [ Suplementos do Office](https://docs.microsoft.com/office/dev/add-ins/overview/office-add-ins). 
  
## <a name="introduction-to-the-project-software-development-kit-sdk"></a>Introdução ao SDK (Kit de Desenvolvimento de Software) do Project
<a name="pj15_Welcome_IntroToSDK"> </a>

O Project Server 2013 é uma plataforma para criar soluções de gerenciamento de projetos corporativos no local ou na nuvem, e para criar aplicativos que os usuários finais podem descobrir e adquirir por meio da AppSource (antigo Office Store). A arquitetura do Project Server 2013 é baseada na plataforma apresentada no Microsoft Office Project Server 2007, com muitos acréscimos e melhorias. Os novos recursos incluem um modelo de objeto do lado do cliente (CSOM) para habilitar o acesso ao Project Online, um serviço OData para acesso online aos dados de relatório do Project Server, receptores remotos de eventos e arquitetura de fluxo de trabalho baseado na versão 4 do Windows Workflow Foundation. (WF4) e Suplementos do Office, que é uma arquitetura comum para extensões do painel de tarefas em aplicativos de clientes do Microsoft Office 2013.
  
Uma alteração importante no Project Server 2013 é o uso de um único banco de dados no lugar dos bancos de dados Rascunho, Publicado, Arquivo e Relatórios no Project Server 2010. Para saber mais sobre novos recursos e recursos preteridos, consulte [Atualizações para desenvolvedores no Project 2013](updates-for-developers-in-project-2013.md). Confira informações sobre as alterações de plataformas do Project Server em [Arquitetura do Project Server 2013](project-server-2013-architecture.md). Para obter uma visão geral da plataforma de desenvolvimento que existe no Project Server 2010 e na qual o Project Server 2013 se baseia, consulte[Introdução ao desenvolvimento no Project 2010](https://msdn.microsoft.com/library/gg607685.aspx) no MSDN. 
  
O Project Server 2013 foi criado no Microsoft .NET Framework 4 e Microsoft SharePoint Server 2013. Os artigos e exemplos neste SDK oferecem um ponto de partida para o desenvolvimento de soluções personalizadas e de aplicativos; eles não tratam de todos os recursos de programabilidade do Project Server ou do Project Professional. A [Central de desenvolvedores do Project](https://msdn.microsoft.com/library/4e5245c3-4891-455b-b321-1819cdd77247.aspx) inclui links para artigos de projetos, blogs, vídeos, webcasts, artigos com instruções visuais e outros recursos. 
  
O SDK do Project 2013 inclui informações de desenvolvedor do Project Server 2013, do Project Web App, do Project Professional 2013 e do Project Standard 2013. Os artigos do SDK foram projetados para ajudar desenvolvedores e administradores a avaliarem o Project e o Project Server em relação à extensibilidade e ao planejamento de soluções personalizadas.
  
### <a name="feedback"></a>Comentários
<a name="pj15_Welcome_Feedback"> </a>

Gostaríamos de saber sua opinião. Nos tópicos on-line do MSDN, você pode adicionar comentários, exemplos de código ou sinalizar o conteúdo como um bug na seção **Conteúdo da Comunidade**, na parte inferior de cada página. Quando você instala o download SDK do Project 2013, os artigos de documentação local tem um link *Enviar Feedback* localizado abaixo do título. A qualquer momento, ao ler o SDK, escolha o link para enviar um e-mail para a equipe do SDK. Você pode enviar correções, uma solicitação para esclarecimentos ou uma amostra de código ou outros comentários e nos ajudar a fortalecer o conteúdo. 
  
### <a name="download"></a>Baixar
<a name="pj15_Welcome_Download"> </a>

O download do SDK do Project 2013 está disponível na [Central de Download da Microsoft ](https://www.microsoft.com/en-us/download/details.aspx?id=30435%20) (`https://www.microsoft.com/en-us/download/details.aspx?id=30435%20`). O download inclui o Project2013SDK.HxS (o arquivo que inclui este artigo), amostras de código relacionadas, assemblies redistribuíveis e outros recursos. O Project 2013 SDK ainda não inclui a referência de tabelas de dados de relatórios.
  
### <a name="whats-new-in-the-project-sdk"></a>Novidades no SDK do Project
<a name="pj15_Welcome_WhatsNew"> </a>

O principal objetivo do SDK do Project 2013 é fornecer uma visão geral da capacidade de programação e documentação do CSOM e dos recursos relacionados para a criação de aplicativos, os serviços PSI (Interface do Servidor do Projecto) e aplicativos do painel de tarefas do Project Professional 2013. O SDK do Project 2013 inclui exemplos passo a passo das principais áreas para personalização do Project Server 2013 e dos clientes do Project (Project Standard 2013, Project Professional 2013 e Project Web App). A documentação está incompleta. mais conteúdo será adicionado em versões posteriores. 
  
A tecnologia subjacente para comunicação de rede é o Windows Communication Foundation (WCF) no Project Server 2013, incluindo cenários de nuvem que usam o CSOM do Project Server e o desenvolvimento local usando o PSI. As referências de serviço da web herdadas do ASMX também são baseadas na arquitetura do WCF. Configurar uma referência a um serviço web do PSI (arquivo ASMX) no Project Server 2013 requer acrescentar a opção  de URL `?wsdl` para o caminho. Por exemplo, `https://ServerName/ProjectServerName/_vti_bin/PSI/Resource.asmx?wsdl`.
  
> [!NOTE]
> Embora ele aborde apenas os recursos mais usados ​​do Project Server, recomendamos usar o CSOM sempre que possível para aplicativos no local e na nuvem. Embora ainda esteja disponível no Project Server 2013, a interface do ASMX para o PSI foi descontinuada. Para aplicativos locais que exigem acesso total ao PSI, você deve usar a interface do WCF para o PSI, em vez da interface do ASMX. 
  
O desenvolvimento em um computador Windows 7 é suportado pela cópia dos assemblies CSOM do Project Server 2013 e do SharePoint Server 2013 para o computador de desenvolvimento. O download SDK inclui assemblies CSOM para Project Server e uma licença para redistribuição. Para obter assemblies do CSOM do SharePoint, consulte [do SharePoint Server 2013 cliente componentes SDK](https://www.microsoft.com/en-us/download/details.aspx?id=35585).
  
Para desenvolvimento com os serviços WCF, você pode definir uma referência para um assembly de proxy do PSI ou adicione arquivos de proxy do PSI à solução. Você pode definir referências diretas aos serviços Web ASMX do Project Server de front-end de um computador remoto no mesmo domínio ou usar um assembly de proxy ou de arquivos de proxy. O download do SDK inclui arquivos de proxy para os serviços WCF e os serviços Web do ASMX, além de scripts para a criação dos assemblies de proxy e para a geração de arquivos de proxy atualizados.
  
No Project Server 2013, você pode criar fluxos de trabalho declarativos do Project Server usando o Microsoft SharePoint Designer 2013, tanto para uso local quanto on-line. O SharePoint Designer 2013 usa as propriedades e métodos da atividade do fluxo de trabalho no CSOM. O desenvolvimento e a implantação de soluções do Visual Studio 2012 que incluem Web Parts do Project Server, ou personalizações do Project Web App, são suportados apenas em um computador do Project Server.
  
Confira uma visão geral de recursos preteridos no Project Server 2013 e novos recursos de programação em [atualizações para desenvolvedores no Project 2013](updates-for-developers-in-project-2013.md). Outra das principais alterações feitas no Project Server 2013 é o uso de fluxos de trabalho baseados em WF-4 para o gerenciamento da criação e da aprovação de propostas de projeto baseadas em modelos de projeto corporativo. 
  
Os novos tópicos incluem o seguinte:
  
- [Criar um suplemento do SharePoint hospedado no Project Server](create-a-sharepoint-hosted-project-server-add-in.md) mostra como usar o Visual Studio para desenvolvimento remoto de um aplicativo que possa ser usado com o Project Server 2013 e com o Project Online. 
    
- [Arquitetura do Project Server 2013](project-server-2013-architecture.md) explica os principais recursos novos da plataforma do Project Server. 
    
- [Introdução ao modelo de objeto do JavaScript do Project Server 2013](getting-started-with-the-project-server-2013-javascript-object-model.md) mostra como desenvolver aplicativos Web que podem acessar o Project Server. 
    
- [Introdução a CSOM e .NET do Project Server ](getting-started-with-the-project-server-csom-and-net.md) mostra como usar o modelo de objeto do lado cliente para desenvolver aplicativos em vez de usar os serviços PSI. 
    
- [Aplicativos de painel de tarefas do Project Professional](task-pane-add-ins-for-project.md) apresenta suplementos do Office, conforme aplicados ao Project 2013. O Office 2013 SDK inclui artigos que mostram como desenvolver aplicativos do painel de tarefas para o Project e os outros clientes do Office 2013. 
    
- [Criar um fluxo de trabalho do Project Server para o Gerenciamento de Propostas](create-a-project-server-workflow-for-demand-management.md) mostra como o SharePoint Designer 2013 pode ser usado para criar fluxos de trabalho do Project Server. 
    
- [ProjectData - referência do serviço OData do Project](https://msdn.microsoft.com/library/office/jj163015.aspx) inclui uma visão geral da interface OData para relatórios do Project Server, além de tópicos de referência de XML para o serviço **ProjectData**. 
    
Tópicos na namespace **Microsoft.ProjectServer.Client** e novos métodos nos serviços PSI têm apenas uma documentação mínima. A maioria dos tópicos de referência para os serviços PSI permanece inalterada em relação à versão de julho de 2011 do SDK do Project 2010. 
  
### <a name="future-sdk-releases"></a>Futuras versões do SDK
<a name="pj15_Welcome_FutureReleases"> </a>

O SDK do Project 2013 será atualizado com novos artigos e conteúdo de referência para a versão de disponibilidade geral.
  
## <a name="sections-in-the-project-sdk"></a>Seções do SDK do Project
<a name="pj15_Welcome_SectionsInTheSDK"> </a>

Há duas seções de nível superior no SDK do Project 2013:
  
- A seção [Artigos conceituais e de orientação](project-conceptual-and-how-to-articles.md) contém visões gerais dos principais recursos e artigos com procedimentos passo a passo para o desenvolvimento. 
    
- A seção [Project Server 2013 class library and web service reference](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) documenta o modelo de objeto dos assemblies públicos, o assembly Microsoft.ProjectServer.Client.dll para o CSOM e os serviços PSI. 
    
A seção **Artigos conceituais e de instruções** inclui o seguinte: 
  
- [Novidades e o que há para desenvolvedores](updates-for-developers-in-project-2013.md) descreve os principais recursos de programabilidade novos e os recursos preteridos no Project 2013. 
    
- [Visão geral do Project para desenvolvedores](https://msdn.microsoft.com/library/8da91ab0-af4f-429f-8241-490600e3f7bd%28Office.15%29.aspx) inclui artigos sobre a arquitetura do Project Server, artigos que mostram como iniciar o desenvolvimento com CSOM, informações sobre novos recursos no VBA para Project e uma referência ao SDK do Office 2013, que contém tópicos sobre aplicativos do painel de tarefas para o Project Professional 2013. 
    
- [Project programming tasks ](project-programming-tasks.md)inclui artigos de instruções sobre a criação de aplicativos para o Project Server usando o JavaScript com o CSOM, além da criação de propostas e fluxos de trabalho de projetos para gerenciamento de propostas. 
    
- [Project 2013 programming references](project-2013-programming-references.md) inclui uma introdução à referência de PSI para o Project Server 2013, informações sobre códigos de erro do Project Server e referência ao esquema OData para o serviço **ProjectData**. 
    
> [!NOTE]
>  Seguem os requisitos para desenvolver e implantar soluções e aplicativos de EPM da AppSource que se integra ao Project Server 2013:> Você deve instalar o .NET Framework 4 ou o .NET Framework 4.5 no computador de desenvolvimento e nos computadores de implantação. Para determinar se a versão correta está instalada, abra **Programas e Recursos** no painel de controle do Windows. > O Visual Studio 2012 instala e usa o .NET Framework 4.5. Quando você cria um projeto do Visual Studio, você pode selecionar **.NET Framework 4.0** ou **NET Framework 4.5** na lista suspensa da caixa de diálogo **Novo Projeto**. Você também pode selecionar as **Estrutura de Destino** na guia**Aplicativo** do projeto da janela **Propriedades**. > Você pode usar o Visual Studio 2010 para aplicativos que usam o CSOM ou o PSI e para os aplicativos do painel de tarefas do Project. No entanto, o Visual Studio 2010 não contém modelos de suplementos do Office, ferramentas de desenvolvimento do Office ou ferramentas de desenvolvimento do SharePoint para o Office 2013. Para baixar o Visual Studio 2012 e o Web Platform Installer (WebPI) que inclui as ferramentas de desenvolvimento do Office e do SharePoint, confira [Downloads para aplicativos do Office e SharePoint](https://msdn.microsoft.com/office/apps/fp123627). > Recomendamos que você desenvolva soluções personalizadas em um ambiente de teste. Se você desenvolver soluções para as versões atuais do Project Server 2013 e do Project 2013, elas deverão ser recompiladas com referências atualizadas e podem precisar de alterações adicionais para trabalhar com versões posteriores. Soluções desenvolvidas para qualquer versão de pré-lançamento podem não funcionar com a versão de lançamento. 
  
## <a name="see-also"></a>Confira também
<a name="pj15_Welcome_AR"> </a>

- [Atualizações para desenvolvedores do Project 2013](updates-for-developers-in-project-2013.md)
    
- [Arquitetura do Project Server 2013](project-server-2013-architecture.md)
    
- [Download do SDK do Project 2013](https://www.microsoft.com/en-us/download/details.aspx?id=30435%20)
    
- [SDK de componentes de cliente do SharePoint 2013](https://www.microsoft.com/en-us/download/details.aspx?id=35585)
    
- [Project para desenvolvedores](https://msdn.microsoft.com/project)
    
- [Documentação de desenvolvedor do Office](https://msdn.microsoft.com/office)
    
- [Introdução ao desenvolvimento no Project 2010](https://msdn.microsoft.com/library/gg607685.aspx)
    
- [Convenções de Documentos](https://msdn.microsoft.com/library/6b38829f-1a9d-4fb6-ad3b-01182628080a.aspx)
    
- [Acessibilidade no SharePoint 2013](https://msdn.microsoft.com/library/jj841103.aspx)
    
- [Acessibilidade no Microsoft Office 365](https://www.microsoft.com/enable/products/office365/)
    
- [Aviso de Privacidade do Microsoft Online](https://privacy.microsoft.com/pt-BR/privacystatement)
    

