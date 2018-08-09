---
title: Arquitetura do Project Server 2013 e programação
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
- Project 2013, benefícios de programação, programação, Project Server, Project 2013 e a arquitetura para o Project Server, arquitetura e EPM
localization_priority: Normal
ms.assetid: 9ea3b3c1-fb90-454a-b8e6-abc44fca663d
description: Os artigos desta seção descrevem a arquitetura geral da solução Enterprise Project Management (EPM), que combina o Project Professional 2013, o Project Server 2013, o Project Web App e o SharePoint Server 2013.
ms.openlocfilehash: 6b5ab94968dbb996a370e0e5abb89813f5e41ef7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771177"
---
# <a name="project-server-2013-architecture-and-programmability"></a>Arquitetura do Project Server 2013 e programação

Os artigos desta seção descrevem a arquitetura geral da solução Enterprise Project Management (EPM), que combina o Project Professional 2013, o Project Server 2013, o Project Web App e o SharePoint Server 2013.
  
Project Server 2013 foi criado com o .NET Framework 4 e é a terceira versão principal do Project Server para fornecer uma arquitetura de várias camada true. Para o acesso de nuvem, o Project Server 2013 implementa um modelo de objeto do cliente (CSOM) e um serviço OData para geração de relatórios que pode ser usado em aplicativos web, aplicativos móveis e aplicativos do Silverlight. Para aplicativos no local, os clientes podem usar o CSOM ou os serviços do Project Server Interface (PSI). 
  
## <a name="introduction-to-project-server-architecture"></a>Introdução à arquitetura do Project Server

Os tópicos desta seção descrevem a arquitetura geral da solução Enterprise Project Management (EPM), que combina o Project Professional 2013, o Project Server 2013, o Project Web App e o SharePoint Server 2013.
  
Para obter acesso programático para o Project Server, você deve usar o CSOM ou os serviços PSI com a interface do Windows Communication Foundation (WCF). A interface de serviço web ASMX de PSI foi preterido no Project Server 2013, mas ainda funciona. A PSI habilita o acesso eficiente usando conjuntos de dados e você pode criar manipuladores de eventos do servidor. CSOM do próprio usa a PSI para acessar a camada de objeto de negócios do Project Server. Em vez de quatro bancos de dados do Project Server, o Project Server 2013 usa um único banco de dados na camada de acesso de dados.
  
Project Server 2013 integra-se totalmente com o SharePoint Server 2013. O serviço de aplicativo do projeto podem ser associado aos outros conjuntos de sites do SharePoint no farm. Project Server pode operar com e relatar SharePoint listas de tarefas no conjunto de sites e podem também obtêm controle total em que o Project Server importa e gerencia que a tarefa listas como projetos da empresa. Project Server também usa a versão 4 do Windows Workflow Foundation (WF4) e adiciona as atividades de fluxo de trabalho para soluções de gerenciamento de demanda.
  
Para uma discussão dos muitos recursos novos que fornece do Project 2013 para desenvolvedores e dos recursos que são reduzidos, consulte [atualizações para desenvolvedores no Project 2013](updates-for-developers-in-project-2013.md).
  
## <a name="in-this-section"></a>Nesta seção

[Arquitetura do Project Server 2013](project-server-2013-architecture.md) descreve as principais partes da plataforma do Project 2013, incluindo os clientes e servidores. 
  
[Recursos de programação do Project Server](project-server-programmability.md) aborda os recursos de extensibilidade principal do Project Server 2013, personalização do Project Web App e atualizando aplicativos desenvolvidos para versões anteriores do Project Server. 
  
[O que o PSI e não faz](what-the-psi-does-and-does-not-do.md) descreve cenários onde a PSI pode ser usada e lista coisas a PSI não pode fazer. 
  
[O que o CSOM e não faz](what-the-csom-does-and-does-not-do.md) descreve cenários onde o CSOM pode ser usado e lista as tarefas que o CSOM não pode fazer. 
  
### <a name="topics-not-covered"></a>Tópicos não abordados

Os artigos na seção de *arquitetura e programação* do documento não recursos do Project Web App ou clientes de área de trabalho do Project (Project Standard 2013 e Project Professional 2013). 
  
Visual Basic para obter ajuda Applications (VBA) está disponível no editor do Visual Basic dentro do Project Standard e Project Professional.
  
## <a name="see-also"></a>Confira também
<a name="bk_addresources"> </a>

- [Atualizações para desenvolvedores no Project 2013](updates-for-developers-in-project-2013.md)
    
- [Introdução ao desenvolvimento de fluxos de trabalho do Project](getting-started-developing-project-server-workflows.md)
    

