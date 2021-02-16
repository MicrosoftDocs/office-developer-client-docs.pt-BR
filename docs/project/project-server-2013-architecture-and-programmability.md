---
title: Arquitetura e programação do Project Server 2013
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
f1_keywords:
- architecture
- platform
- Project
- Project architecture
- Project programmability
- Project Server architecture
- Project Server programmability
keywords:
- project 2013, arquitetura e programação, programabilidade, Project Server,Project 2013, benefícios para EPM, arquitetura e Project Server
localization_priority: Normal
ms.assetid: 9ea3b3c1-fb90-454a-b8e6-abc44fca663d
description: Os artigos nesta seção descrevem a arquitetura geral da solução Enterprise Project Management (EPM), que combina o Project Professional 2013, o Project Server 2013, o Project Web App e o SharePoint Server 2013.
ms.openlocfilehash: 44cd5a32b8d3de421ffe3b2d9bf0137146bc4c4e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413784"
---
# <a name="project-server-2013-architecture-and-programmability"></a>Arquitetura e programação do Project Server 2013

Os artigos nesta seção descrevem a arquitetura geral da solução Enterprise Project Management (EPM), que combina o Project Professional 2013, o Project Server 2013, o Project Web App e o SharePoint Server 2013.
  
O Project Server 2013 foi criado com o .NET Framework 4 e é a terceira grande versão do Project Server a fornecer uma arquitetura de vários mais complexos. Para acesso à nuvem, o Project Server 2013 implementa um modelo de objeto do lado do cliente (CSOM) e um serviço OData para relatórios que podem ser usados em aplicativos Web, aplicativos móveis e aplicativos Silverlight. Para aplicativos locais, os clientes podem usar o CSOM ou os serviços do Project Server Interface (PSI). 
  
## <a name="introduction-to-project-server-architecture"></a>Introdução à arquitetura do Project Server

Os tópicos nesta seção descrevem a arquitetura geral da solução Enterprise Project Management (EPM), que combina o Project Professional 2013, o Project Server 2013, o Project Web App e o SharePoint Server 2013.
  
Para acesso programático ao Project Server, você deve usar o CSOM ou os serviços psi com a interface do Windows Communication Foundation (WCF). A interface do serviço Web ASMX da PSI foi preterida no Project Server 2013, mas ainda funciona. A PSI permite acesso eficiente usando conjuntos de dados e você pode criar manipuladores para eventos do lado do servidor. O próprio CSOM usa a PSI para acessar a camada de objeto de negócios do Project Server. Em vez de quatro bancos de dados do Project Server, o Project Server 2013 usa um único banco de dados na camada de acesso a dados.
  
O Project Server 2013 integra-se profundamente ao SharePoint Server 2013. O Serviço de Aplicativo do Project pode ser associado a outros conjunto de sites do SharePoint no farm. O Project Server pode operar e relatar listas de tarefas do SharePoint no conjunto de sites e também pode obter controle total de onde o Project Server importa e gerencia as listas de tarefas como projetos da empresa. O Project Server também usa a versão 4 do Windows Workflow Foundation (WF4) e adiciona atividades de fluxo de trabalho para soluções de Gerenciamento de Propostas.
  
For a discussion of the many new features that Project 2013 provides for developers, and of the features that are deprecated, see [Updates for developers in Project 2013](updates-for-developers-in-project-2013.md).
  
## <a name="in-this-section"></a>Nesta seção

[A arquitetura do Project Server 2013](project-server-2013-architecture.md) descreve as principais partes da plataforma do Project 2013, incluindo os clientes e servidores. 
  
A programação do [Project Server](project-server-programmability.md) discute os principais recursos de extensibilidade do Project Server 2013, a personalização do Project Web App e a atualização de aplicativos que foram projetados para versões anteriores do Project Server. 
  
[O que o PSI faz e](what-the-psi-does-and-does-not-do.md) não descreve cenários em que o PSI pode ser usado e lista coisas que o PSI não pode fazer. 
  
[O que o CSOM](what-the-csom-does-and-does-not-do.md) faz e não descreve cenários em que o CSOM pode ser usado e lista coisas que o CSOM não pode fazer. 
  
### <a name="topics-not-covered"></a>Tópicos não abordados

Os artigos  da seção Arquitetura e programação não documentam recursos dos clientes da área de trabalho do Project (Project Standard 2013 e Project Professional 2013) ou do Project Web App. 
  
A ajuda do Visual Basic for Applications (VBA) está disponível no editor do Visual Basic no Project Standard e no Project Professional.
  
## <a name="see-also"></a>Confira também
<a name="bk_addresources"> </a>

- [Atualizações para desenvolvedores do Project 2013](updates-for-developers-in-project-2013.md)
    
- [Introdução ao desenvolvimento de fluxos de trabalho do Project Server](getting-started-developing-project-server-workflows.md)
    

