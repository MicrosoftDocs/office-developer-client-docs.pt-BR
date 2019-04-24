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
- Project 2013, arquitetura e programação, programação, Project Server, Project 2013, benefícios para o EPM, a arquitetura e o Project Server
localization_priority: Normal
ms.assetid: 9ea3b3c1-fb90-454a-b8e6-abc44fca663d
description: Os artigos desta seção descrevem a arquitetura geral da solução Enterprise Project Management (EPM), que combina o Project Professional 2013, o Project Server 2013, o Project Web App e o SharePoint Server 2013.
ms.openlocfilehash: 44cd5a32b8d3de421ffe3b2d9bf0137146bc4c4e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301467"
---
# <a name="project-server-2013-architecture-and-programmability"></a>Arquitetura e programação do Project Server 2013

Os artigos desta seção descrevem a arquitetura geral da solução Enterprise Project Management (EPM), que combina o Project Professional 2013, o Project Server 2013, o Project Web App e o SharePoint Server 2013.
  
O Project Server 2013 é criado com o .NET Framework 4 e é a terceira versão principal do Project Server para fornecer uma arquitetura de várias camadas real. Para acesso à nuvem, o Project Server 2013 implementa um modelo de objeto do cliente (CSOM) e um serviço OData para relatórios que podem ser usados em aplicativos Web, aplicativos móveis e aplicativos do Silverlight. Para aplicativos locais, os clientes podem usar o CSOM ou os serviços da interface do Project Server (PSI). 
  
## <a name="introduction-to-project-server-architecture"></a>Introdução à arquitetura do Project Server

Os tópicos desta seção descrevem a arquitetura geral da solução Enterprise Project Management (EPM), que combina o Project Professional 2013, o Project Server 2013, o Project Web App e o SharePoint Server 2013.
  
Para acesso programático ao Project Server, você deve usar o CSOM ou os serviços do PSI com a interface do Windows Communication Foundation (WCF). A interface de serviço Web ASMX da PSI foi preterida no Project Server 2013, mas ainda funciona. A PSI permite acesso eficiente usando DataSets e você pode criar manipuladores para eventos no servidor. O próprio CSOM usa o PSI para acessar a camada de objetos comerciais do Project Server. Em vez de quatro bancos de dados do Project Server, o Project Server 2013 usa um único banco de dados na camada de acesso aos dados.
  
O Project Server 2013 se integra profundamente ao SharePoint Server 2013. O serviço de aplicativo do Project pode ser associado a outros conjuntos de sites do SharePoint no farm. O Project Server pode operar com e relatar as listas de tarefas do SharePoint no conjunto de sites e também pode obter controle total onde o Project Server importa e gerencia as listas de tarefas como projetos empresariais. O Project Server também usa a versão 4 do Windows Workflow Foundation (WF4) e adiciona atividades de fluxo de trabalho para soluções de gerenciamento de demanda.
  
Para obter uma discussão dos vários novos recursos que o Project 2013 fornece aos desenvolvedores e dos recursos que foram preteridos, consulte [atualizações para desenvolvedores no Project 2013](updates-for-developers-in-project-2013.md).
  
## <a name="in-this-section"></a>Nesta seção

A [arquitetura do Project Server 2013](project-server-2013-architecture.md) descreve as principais partes da plataforma do Project 2013, incluindo os clientes e os servidores. 
  
A [programação do Project Server](project-server-programmability.md) discute os principais recursos de extensibilidade do project Server 2013, personalização do Project Web App e atualização de aplicativos criados para versões anteriores do Project Server. 
  
O [que o Psi faz e não](what-the-psi-does-and-does-not-do.md) descreve cenários onde o Psi pode ser usado e lista coisas que o Psi não pode fazer. 
  
O [que o CSOM faz e](what-the-csom-does-and-does-not-do.md) não descreve os cenários em que o CSOM pode ser usado e lista coisas que o CSOM não pode fazer. 
  
### <a name="topics-not-covered"></a>Tópicos não cobertos

Os artigos da seção *arquitetura e programação* não documentam recursos dos clientes de desktop do Project (project Standard 2013 e project Professional 2013) ou Project Web App. 
  
A ajuda do Visual Basic for Applications (VBA) está disponível no editor do Visual Basic no Project Standard e no Project Professional.
  
## <a name="see-also"></a>Confira também
<a name="bk_addresources"> </a>

- [Atualizações para desenvolvedores do Project 2013](updates-for-developers-in-project-2013.md)
    
- [Introdução ao desenvolvimento de fluxos de trabalho do Project Server](getting-started-developing-project-server-workflows.md)
    

