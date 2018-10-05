---
title: Documentação do desenvolvedor do Project 2013
manager: soliver
ms.date: 04/04/2016
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
- SDK, visão geral do project 2013, Project 2013, SDK
localization_priority: Normal
ms.assetid: f66adbf1-5cb5-4dd0-be08-45e1c88c010c
description: Encontre documentação, amostras de código, artigos de instruções e referências de programação para ajudar a construir aplicativos para o Office Store ou um catálogo de aplicativos privado para personalizar e integrar o Project Server e os clientes do Project com uma ampla variedade de outros desktop e corporativos aplicativos para gerenciamento de projetos empresariais.
ms.openlocfilehash: 887b5964d6fa0e4845156e13c7f49a399543c133
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398224"
---
# <a name="project-2013-developer-documentation"></a>Documentação do desenvolvedor do Project 2013

Encontre documentação, amostras de código, artigos de instruções e referências de programação para ajudar a construir aplicativos para o Office Store ou um catálogo de aplicativos privado para personalizar e integrar o Project Server e os clientes do Project com uma ampla variedade de outros desktop e corporativos aplicativos para gerenciamento de projetos empresariais.
  
Bem-vindo ao Microsoft Project 2013 Software Development Kit (SDK). O SDK contém documentação, amostras de código, artigos de instruções e referências de programação para ajudar a construir aplicativos para um repositório público ou o catálogo de aplicativos privado para personalizar e integrar o Project Server e os clientes do Project com uma ampla variedade de outra área de trabalho e aplicativos de negócios para enterprise project management.
  
> [!NOTE]
> Project Server 2013 é criado na plataforma do SharePoint Server 2013 e Project 2013 inclui muito da infraestrutura de mesmo como os outros aplicativos do Office 2013. Para obter a documentação do modelo para o SharePoint Add-ins, fluxos de trabalho baseados no SharePoint, Web Parts, desenvolvimento com outros recursos do SharePoint e documentação de suplementos do Office, consulte [Add-ins do SharePoint](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins) e [suplementos do Office](https://docs.microsoft.com/office/dev/add-ins/overview/office-add-ins). 
  
## <a name="introduction-to-the-project-sdk"></a>Introdução ao SDK do Project
<a name="pj15_Welcome_IntroToSDK"> </a>

Project Server 2013 é uma plataforma para criar o local ou baseado em nuvem empresarial soluções de gerenciamento de projeto e para criar aplicativos que os usuários finais capaz de descobrir e adquirir por meio de um armazenamento público ou de um catálogo de aplicativos privado. A arquitetura do Project Server 2013 baseia-se na plataforma introduzida no Microsoft Office Project Server 2007, com muitas adições e melhorias. Os novos recursos incluem um modelo de objeto do cliente (CSOM) para habilitar o acesso ao Project Online, um serviço OData para acesso online ao Project Server, relatórios de dados, receptores de evento remoto, arquitetura de fluxo de trabalho que se baseia em versão 4 do fluxo de trabalho do Windows Foundation (WF4) e suplementos do Office, que é uma arquitetura comum para extensões do painel de tarefas em aplicativos cliente do Microsoft Office 2013.
  
Uma alteração importante no Project Server 2013 é o uso de um único banco de dados no lugar os bancos de dados de rascunho, publicado, arquivo morto e relatórios no Project Server 2010. Para obter mais informações sobre novos recursos e recursos preteridos, consulte [atualizações para desenvolvedores no Project 2013](updates-for-developers-in-project-2013.md). Para obter informações sobre alterações na plataforma do Project Server, consulte [arquitetura do Project Server 2013](project-server-2013-architecture.md). Para obter uma visão geral da plataforma de desenvolvimento que existe no Project Server 2010 e Project Server 2013 baseado no, consulte [Introdução ao desenvolvimento para Project 2010](https://msdn.microsoft.com/library/gg607685.aspx) no MSDN. 
  
Project Server 2013 foi criado com o Microsoft .NET Framework 4 e Microsoft SharePoint Server 2013. Os artigos e os exemplos neste SDK fornecem um ponto de partida para o desenvolvimento de soluções personalizadas e aplicativos; eles não atendem todos os recursos de programação do Project Server ou Project Professional. O [Project Developer Center](https://msdn.microsoft.com/library/4e5245c3-4891-455b-b321-1819cdd77247.aspx) inclui links para artigos, blogs, vídeos, webcasts, artigos com instruções visuais e outros recursos de projeto. 
  
O SDK do Project 2013 inclui informações do desenvolvedor para o Project Server 2013, Project Web App, Project Professional 2013 e Project Standard 2013. Os artigos SDK projetados para ajudar a avaliar o Project e do Project Server para planejamento de soluções personalizadas e extensibilidade de administradores e desenvolvedores.
  
### <a name="feedback"></a>Comentários
<a name="pj15_Welcome_Feedback"> </a>

Gostaríamos de saber a sua opinião. Nos tópicos online no MSDN, você pode adicionar comentários, amostras de código, ou sinalizar o conteúdo como um bug na seção de **Conteúdo da comunidade** na parte inferior de cada página. Quando você instala o download do SDK do Project 2013, os artigos documentação local tem um link de *Enviar comentários* que está localizado abaixo do título. A qualquer momento no modo de leitura do SDK, escolha o link para enviar um email para a equipe do SDK. Você pode enviar uma solicitação de esclarecimento, correções ou um exemplo de código ou outros comentários e nos ajudar a tornar o conteúdo mais forte. 
  
### <a name="download"></a>Baixar
<a name="pj15_Welcome_Download"> </a>

O download do SDK do Project 2013 está disponível no [Centro de Download da Microsoft](https://www.microsoft.com/en-us/download/details.aspx?id=30435%20) ( `https://www.microsoft.com/en-us/download/details.aspx?id=30435%20`). O download inclui Project2013SDK.HxS (o arquivo que inclua este artigo), amostras de código, assemblies redistribuíveis e outros recursos relacionados. O SDK do Project 2013 ainda não inclui a referência de tabelas de dados de relatórios.
  
### <a name="whats-new-in-the-project-sdk"></a>Novidades no SDK do Project
<a name="pj15_Welcome_WhatsNew"> </a>

O principal objetivo do Project 2013 SDK é fornecer uma visão geral dos recursos de programação e documentação do CSOM e recursos relacionados para a criação de aplicativos, serviços do Project Server Interface (PSI) e aplicativos do painel de tarefas do Project Professional 2013. O SDK do Project 2013 inclui exemplos passo a passo das principais áreas de personalização do Project Server 2013 e os clientes de projeto (Project Standard 2013, Project Professional 2013 e Project Web App). A documentação está incompleta. mais conteúdo será adicionado em versões posteriores. 
  
A tecnologia subjacente para comunicação de rede é Windows Communication Foundation (WCF) no Project Server 2013, incluindo cenários de nuvem que usam o Project Server CSOM e desenvolvimento de local usando a PSI. As referências de serviços web ASMX herdadas também se baseiam na arquitetura WCF. Definindo uma referência a um serviço web PSI (arquivo ASMX) no Project Server 2013 requer anexando o `?wsdl` opção de URL para o caminho. Por exemplo, `https://ServerName/ProjectServerName/_vti_bin/PSI/Resource.asmx?wsdl`.
  
> [!NOTE]
> Embora ele aborda somente a mais comumente usada recursos do Project Server, recomendamos que você use o CSOM onde for possível para aplicativos tanto no local e na nuvem. Embora seja ainda ficam disponível no Project Server 2013, a interface ASMX para a PSI foi preterida. Para aplicativos de local que exigem acesso total para o PSI feitas, você deve usar a interface WCF para a PSI, em vez da interface ASMX. 
  
Há suporte para o desenvolvimento em um computador Windows 7, copiando os assemblies CSOM do Project Server 2013 e do SharePoint Server 2013 para o computador de desenvolvimento. O download do SDK inclui os assemblies CSOM para o Project Server e uma licença de redistribuição. Para obter os assemblies de CSOM do SharePoint, consulte o [SDK de componentes de cliente do SharePoint Server 2013](https://www.microsoft.com/en-us/download/details.aspx?id=35585).
  
Para desenvolvimento com os serviços WCF, você pode definir uma referência para um assembly de proxy do PSI ou adicione arquivos de proxy do PSI à solução. Você pode definir referências diretas aos serviços Web ASMX do Project Server de front-end de um computador remoto no mesmo domínio ou usar um assembly de proxy ou de arquivos de proxy. O download do SDK inclui arquivos de proxy para os serviços WCF e os serviços Web do ASMX, além de scripts para a criação dos assemblies de proxy e para a geração de arquivos de proxy atualizados.
  
No Project Server 2013, você pode criar fluxos de trabalho declarativos do Project Server usando o Microsoft SharePoint Designer 2013, tanto no local e online usar. SharePoint Designer 2013 usa os métodos e propriedades de atividade de fluxo de trabalho no CSOM. Desenvolvimento e implantação de soluções do Visual Studio 2012 que inclui Web Parts do Project Server ou personalizações do Project Web App, é suportado somente em um computador do Project Server.
  
Para obter uma visão geral dos novos recursos de programação e recursos preteridos no Project Server 2013, consulte [atualizações para desenvolvedores no Project 2013](updates-for-developers-in-project-2013.md). Outra alteração importante no Project Server 2013 é o uso de fluxos de trabalho baseados em WF4 para gerenciar a criação e aprovação de propostas de projeto que se baseiam em modelos de projeto corporativo. 
  
Os novos tópicos incluem o seguinte:
  
- [Suplemento de criar um Project Server hospedado no SharePoint](create-a-sharepoint-hosted-project-server-add-in.md) mostra como usar o Visual Studio para o desenvolvimento remoto de um aplicativo que pode ser usado com o Project Server 2013 e Project Online. 
    
- [Project Server 2013 architecture](project-server-2013-architecture.md) explica os principais recursos novos da plataforma do Project Server. 
    
- [Introdução ao modelo de objeto do Project Server 2013 JavaScript](getting-started-with-the-project-server-2013-javascript-object-model.md) mostra como desenvolver aplicativos da web que podem acessar o Project Server. 
    
- [Introdução ao Project Server CSOM e .NET](getting-started-with-the-project-server-csom-and-net.md) mostra como usar o modelo de objeto do cliente para desenvolver aplicativos, em vez de usar os serviços PSI. 
    
- [Aplicativos do painel de tarefas para Project Professional](task-pane-add-ins-for-project.md) introduz os suplementos do Office, conforme aplicadas ao Project 2013. O Office 2013 SDK inclui artigos que mostram como desenvolver aplicativos do painel de tarefas para projetos e outros clientes do Office 2013. 
    
- [Criar um fluxo de trabalho do Project Server para gerenciamento de demanda](create-a-project-server-workflow-for-demand-management.md) mostra como o SharePoint Designer 2013 podem ser usados para criar fluxos de trabalho do Project Server. 
    
- [ProjectData - Referência de serviço OData de projeto](https://msdn.microsoft.com/library/office/jj163015.aspx) inclui uma visão geral da interface do OData para geração de relatórios do Project Server, além de tópicos de referência XML para o serviço **ProjectData** . 
    
Tópicos no namespace **Microsoft.ProjectServer.Client** e novos métodos nos serviços de PSI têm apenas documentação mínima. A maioria dos tópicos de referência para os serviços PSI são inalterada desde o lançamento de julho de 2011 do SDK do Project 2010. 
  
### <a name="future-sdk-releases"></a>Futuras versões do SDK
<a name="pj15_Welcome_FutureReleases"> </a>

O SDK do Project 2013 será atualizado com artigos novos e conteúdo de referência para a versão de disponibilidade geral.
  
## <a name="sections-in-the-project-sdk"></a>Seções do SDK do Project
<a name="pj15_Welcome_SectionsInTheSDK"> </a>

Há duas seções de nível superior no Project 2013 SDK:
  
- A seção de [artigos conceituais e instruções do Project](project-conceptual-and-how-to-articles.md) contém uma visão geral dos principais recursos e artigos com procedimentos passo a passo para desenvolvimento. 
    
- A seção de [referência do serviço Project Server 2013 classe web e de biblioteca de](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) documentos o modelo de objeto dos assemblies do públicos, o assembly Microsoft.ProjectServer.Client.dll para o CSOM e os serviços PSI. 
    
A seção **Artigos conceituais e de instruções** inclui o seguinte: 
  
- [O que há de novo e o que está para desenvolvedores](updates-for-developers-in-project-2013.md) descreve os principais novos recursos de programação e recursos no Project 2013 preteridos. 
    
- [Visão geral do Project para desenvolvedores](https://msdn.microsoft.com/library/8da91ab0-af4f-429f-8241-490600e3f7bd%28Office.15%29.aspx) inclui artigos sobre a arquitetura do Project Server, que mostram como começar a desenvolver com o CSOM, informações sobre novos recursos no VBA para o projeto e uma referência para o SDK do Office 2013, que contém artigos tópicos sobre desenvolvimento de aplicativos do painel de tarefas para o Project Professional 2013. 
    
- [Tarefas de programação de projeto](project-programming-tasks.md) inclui artigos de instruções sobre como criar aplicativos para o Project Server, usando o JavaScript com o CSOM e criando propostas de projeto e fluxos de trabalho para gerenciamento de demanda. 
    
- [Referências de programação do Project 2013](project-2013-programming-references.md) inclui uma introdução à referência PSI para a referência de esquema de OData para o serviço **ProjectData** , informações sobre códigos de erro do Project Server e Project Server 2013. 
    
> [!NOTE]
>  Estes são os requisitos para desenvolver e implantar aplicativos da Office Store pública que integram com o Project Server 2013 e soluções EPM: > você deve instalar o .NET Framework 4 ou o .NET Framework 4.5 no computador de desenvolvimento e sobre a implantação computadores. Para determinar se a versão correta está instalada, abra **programas e recursos** no painel de controle do Windows. > Visual Studio 2012 instala e usa o .NET Framework 4.5. Quando você cria um projeto do Visual Studio, você pode selecionar o **.NET Framework 4.0** ou **4.5 do NET Framework** na lista suspensa da caixa de diálogo **Novo projeto** . Você também pode selecionar a **Estrutura de destino** na guia **aplicativo** da janela de **Propriedades** do projeto. > Você pode usar o Visual Studio 2010 para aplicativos que usam o CSOM ou a PSI e para aplicativos de painel de tarefas do projeto. No entanto, o Visual Studio 2010 não contém os modelos de suplementos do Office, ferramentas de desenvolvimento do Office ou as ferramentas de desenvolvimento do SharePoint para o Office 2013. Para baixar o Visual Studio 2012 e o Web Platform Installer (WebPI) que inclui as ferramentas de desenvolvimento do Office e SharePoint, consulte os [Downloads de aplicativos para Office e SharePoint](https://msdn.microsoft.com/office/apps/fp123627). > É recomendável que você desenvolva soluções personalizadas em um ambiente de teste. Se você desenvolve soluções para as atuais versões do Project Server 2013 e Project 2013, eles devem ser recompilados com referências atualizadas e talvez precise alterações adicionais, para funcionar com versões posteriores. Soluções desenvolvidas para qualquer versão de pré-lançamento podem não funcionar com a versão de lançamento. 
  
## <a name="see-also"></a>Confira também
<a name="pj15_Welcome_AR"> </a>

- [Atualizações para desenvolvedores no Project 2013](updates-for-developers-in-project-2013.md)
    
- [Arquitetura do Project Server 2013](project-server-2013-architecture.md)
    
- [Download do SDK do Project 2013](https://www.microsoft.com/en-us/download/details.aspx?id=30435%20)
    
- [SDK de componentes de cliente do SharePoint Server 2013](https://www.microsoft.com/en-us/download/details.aspx?id=35585)
    
- [Project para desenvolvedores](https://msdn.microsoft.com/project)
    
- [Documentação do desenvolvedor do Office](https://msdn.microsoft.com/office)
    
- [Introdução ao desenvolvimento para Project 2010](https://msdn.microsoft.com/library/gg607685.aspx)
    
- [Convenções de documentos](https://msdn.microsoft.com/library/6b38829f-1a9d-4fb6-ad3b-01182628080a.aspx)
    
- [Acessibilidade no SharePoint 2013](https://msdn.microsoft.com/library/jj841103.aspx)
    
- [Acessibilidade no Microsoft Office 365](https://www.microsoft.com/enable/products/office365/)
    
- [Aviso de privacidade online da Microsoft](https://privacy.microsoft.com/en-us/privacystatement)
    

