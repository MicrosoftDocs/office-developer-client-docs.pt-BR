---
title: Introdução ao desenvolvimento de fluxos de trabalho do Project
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 735bbb04-a8c1-46c0-a346-42050f0ac9b1
description: Demanda processos de gerenciamento no Project Server 2013 incluem fluxos de trabalho que o ajudarão a gerenciar propostas de projeto e análises de portfólio. Esta seção inclui artigos que mostram como criar fluxos de trabalho do Project Server.
ms.openlocfilehash: 275f61b7992423a5e10a7ba90b8c76433290343e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771032"
---
# <a name="getting-started-developing-project-server-workflows"></a>Introdução ao desenvolvimento de fluxos de trabalho do Project

Demanda processos de gerenciamento no Project Server 2013 incluem fluxos de trabalho que o ajudarão a gerenciar propostas de projeto e análises de portfólio. Esta seção inclui artigos que mostram como criar fluxos de trabalho do Project Server.
  
Fluxos de trabalho do Project Server 2013 usam a plataforma de fluxo de trabalho do SharePoint Server 2013, que é baseada na versão 4 do Windows Workflow Foundation (WF4). Fluxos de trabalho baseados em WF4 são declarativos, o que significa que a ferramenta de design de fluxo de trabalho é salva em estágios do fluxo de trabalho, ações, condições e outros elementos em código XAML, que será interpretado em tempo de execução. Você pode usar o SharePoint Designer 2013 ou o Visual Studio 2012 para criar fluxos de trabalho declarativos. Um fluxo de trabalho requer o mecanismo de execução de cliente do Gerenciador de fluxo de trabalho 1.0, que pode ser em um servidor local para soluções no local ou em um servidor remoto para soluções do Project Online.
  
Você pode usar o SharePoint Designer 2013 para criar fluxos de trabalho declarativos relativamente simples. Para os fluxos de trabalho complexos e modelos de fluxo de trabalho que podem ser reutilizados, você pode usar o Visual Studio 2012 para desenvolver e depurar fluxos de trabalho para o Project Web App. Para obter mais informações, consulte [Criando fluxos de trabalho do projeto usando o Visual Studio 2012](http://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx).
  
> [!IMPORTANT]
> Use uma instalação de teste do Project Server, não é uma instalação de produção, desenvolver e testar os fluxos de trabalho. Fluxos de trabalho que são desenvolvidos para versões de pré-lançamento do Project Server 2013 devem ser testados para a versão de lançamento e podem precisar ser criado novamente e reimplantados. 
  
## <a name="in-this-section"></a>Nesta seção

[Criar um fluxo de trabalho do Project Server para o Gerenciamento de Propostas](create-a-project-server-workflow-for-demand-management.md)
  
## <a name="see-also"></a>Confira também



[Em massa de campos personalizados de atualização e criar sites de projetos a partir de um fluxo de trabalho do Project Online](bulk-update-custom-fields-and-create-project-sites-from-workflow-in-project.md)


[Desenvolvimento de fluxos de trabalho no SharePoint Designer 2013 e no Visio 2013](http://msdn.microsoft.com/en-us/library/jj163272%28office.15%29.aspx)
  
[O que há de novo nos fluxos de trabalho para o SharePoint 2013](http://msdn.microsoft.com/en-us/library/jj163177.aspx)
  
[Desenvolver fluxos de trabalho do SharePoint 2013 usando o Visual Studio](http://msdn.microsoft.com/en-us/library/jj163199.aspx)
  
[Criando fluxos de trabalho do projeto usando o Visual Studio 2012](http://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx)
  
[Windows Workflow Foundation](http://msdn.microsoft.com/en-us/library/dd489441.aspx)
  
[Introdução do desenvolvedor para o Windows Workflow Foundation (WF) no .NET 4](http://msdn.microsoft.com/en-us/library/ee342461.aspx)
  
[Guia do Mochileiro ao gerenciamento de propostas (white paper)](http://msdn.microsoft.com/en-us/library/ff973112.aspx)

