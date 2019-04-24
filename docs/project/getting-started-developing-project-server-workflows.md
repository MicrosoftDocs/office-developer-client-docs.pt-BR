---
title: Introdução ao desenvolvimento de fluxos de trabalho do Project
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 735bbb04-a8c1-46c0-a346-42050f0ac9b1
description: Os processos de gerenciamento de demanda no Project Server 2013 incluem fluxos de trabalho que o ajudarão a gerenciar propostas de projetos e análises de portfólios. Esta seção inclui artigos que mostram como criar fluxos de trabalho do Project Server.
ms.openlocfilehash: 0a09022e63528f50ee4f0c8bd69bd6c34c5d8753
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344468"
---
# <a name="getting-started-developing-project-server-workflows"></a>Introdução ao desenvolvimento de fluxos de trabalho do Project

Os processos de gerenciamento de demanda no Project Server 2013 incluem fluxos de trabalho que o ajudarão a gerenciar propostas de projetos e análises de portfólios. Esta seção inclui artigos que mostram como criar fluxos de trabalho do Project Server.
  
Os fluxos de trabalho do Project Server 2013 usam a plataforma de fluxod de trabalho do SharePoint Server 2013, criada na versão 4 do Windows Workflow Foundation (WF4). Os fluxos de trabalho com base em WF4 são declarativos, o que significa que a ferramenta de design de fluxo de trabalho salva estágios, ações, condições e outros elementos do fluxo de trabalho em código XAML, que é interpretado no tempo de execução. Você pode usar o SharePoint Designer 2013 ou o Visual Studio 2012 para criar fluxos de trabalho declarativos. Um fluxo de trabalho requer o mecanismo de execução do Workflow Manager Client 1.0, que pode ser em um servidor local para soluções locais ou em um servidor remoto para soluções do Project Online.
  
Você pode usar o SharePoint Designer 2013 para criar fluxos de trabalho declarativos relativamente simples. Para fluxos de trabalho complexos e modelos de fluxo de trabalho que podem ser reutilizados, você pode usar o Visual Studio 2012 para desenvolver e depurar fluxos de trabalho do Project Web App. Para saber mais, confira [Criar fluxos de trabalho do Project usando o Visual Studio 2012](https://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx).
  
> [!IMPORTANT]
> Use uma instalação de teste do Project Server, e não uma instalação de produção, para desenvolver e testar fluxos de trabalho. Fluxos de trabalho desenvolvidos para versões de pré-lançamento do Project Server 2013 devem ser testados para a versão de lançamento, e podem precisar ser criados e implantados novamente. 
  
## <a name="in-this-section"></a>Nesta seção

[Criar um fluxo de trabalho do Project Server para o Gerenciamento de Propostas](create-a-project-server-workflow-for-demand-management.md)
  
## <a name="see-also"></a>Confira também



[Atualizar campos personalizados em massa e criar sites de projeto a partir de um fluxo de trabalho do Project Online](bulk-update-custom-fields-and-create-project-sites-from-workflow-in-project.md)


[Desenvolvimento de fluxos de trabalho no SharePoint Designer 2013 e no Visio 2013](https://msdn.microsoft.com/library/jj163272%28office.15%29.aspx)
  
[Novidades nos fluxos de trabalho do SharePoint 2013](https://msdn.microsoft.com/library/jj163177.aspx)
  
[Desenvolver fluxos de trabalho do SharePoint 2013 usando o Visual Studio](https://msdn.microsoft.com/library/jj163199.aspx)
  
[Criar fluxos de trabalho do Project usando o Visual Studio 2012](https://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx)
  
[Windows Workflow Foundation](https://msdn.microsoft.com/library/dd489441.aspx)
  
[Introdução de um desenvolvedor ao Windows Workflow Foundation (WF) no .NET 4](https://msdn.microsoft.com/library/ee342461.aspx)
  
[Guia de gerenciamento de propostas para iniciantes (white paper)](https://msdn.microsoft.com/library/ff973112.aspx)

