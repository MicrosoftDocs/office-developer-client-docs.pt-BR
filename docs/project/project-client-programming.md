---
title: Programação de cliente do Project
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
f1_keywords:
- object model
- Project object model
- Project VBA
- VBA
keywords:
- VBA, project programação do modelo, Project, objeto, programação, projeto VBA, Visual Basic for Applications, modelo, VBA, objeto modelo de objeto Project, VBA, Visual Basic for Applications
localization_priority: Normal
ms.assetid: 0ad49ff6-8dff-4379-a52c-d292c53c2bc0
description: Os aplicativos de cliente de desktop Project 2013 — Project Standard 2013 e Project Professional 2013 — podem ser personalizados e estendido usando o VBA para gravação de macros. Você pode usar o Visual Studio 2012 para personalizar a interface do usuário da faixa de opções e criar suplementos complexos habilita de suplementos do Office, uma nova extensibilidade do modelo para painéis de tarefas no projeto que são compilados em uma plataforma comum do Office 2013. Project Standard 2013 e Project Professional 2013 podem executar gerais suplementos do Office e use tarefa painel suplementos que são desenvolvidos especificamente para o projeto de integrar com o SharePoint, outros sites e aplicativos da web e dados externos.
ms.openlocfilehash: cc345f0ff91dfb573dd86c256e89df478edd4924
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394822"
---
# <a name="project-client-programming"></a>Programação de cliente do Project

Os aplicativos de cliente de desktop Project 2013 — Project Standard 2013 e Project Professional 2013 — podem ser personalizados e estendido usando o VBA para gravação de macros. Você pode usar o Visual Studio 2012 para personalizar a interface do usuário da faixa de opções e criar suplementos complexos habilita de suplementos do Office, uma nova extensibilidade do modelo para painéis de tarefas no projeto que são compilados em uma plataforma comum do Office 2013. Project Standard 2013 e Project Professional 2013 podem executar gerais suplementos do Office e use tarefa painel suplementos que são desenvolvidos especificamente para o projeto de integrar com o SharePoint, outros sites e aplicativos da web e dados externos.
  
 **Mover para o Visual Studio** VBA é útil para gravação de macros e desenvolver soluções de automação relativamente simples. Para desenvolver suplementos de painel de tarefas, suplementos e mais complexos, seguros, escalonáveis e soluções facilmente implantadas, recomendamos que você use o Visual Studio 2012. O Microsoft .NET Framework 4.0 e o assembly de interoperabilidade primário do Project 2013 oferecem diversas vantagens para desenvolvimento e implantação de soluções que automatizam e integram os clientes de área de trabalho do Project 2013. 
  
> [!NOTE]
> Você pode usar o Visual Studio 2010 para desenvolver suplementos do projeto. No entanto, o Visual Studio 2012 inclui modelos e extensões que são projetadas para criar clientes de suplementos do Office. 
  
O modelo de objeto do VBA no Project 2013 **MSProject** é essencialmente o mesmo que o modelo de objeto **Microsoft.Office.Interop.MSProject** para soluções de código gerenciado com Office Developer Tools para Visual Studio 2013 (também conhecido como VSTO). Visual Studio 2012 inclui modelos para o desenvolvimento de suplementos de nível de aplicativo para o Project 2010 e do Project 2013 (versões do Project Standard ou Project Professional). VSTO e o Office Developer Tools para Visual Studio 2012 simplificam o desenvolvimento, teste e implantação de soluções de integração avançada que podem usar o cliente de desktop Project e outros aplicativos do Office 2013 e integrar com sites do SharePoint, listas, e fluxos de trabalho. 
  
Suplementos de painel de tarefas e outros suplementos do Office e SharePoint podem ser vendidos no Office Store (consulte [https://office.microsoft.com/store/](https://office.microsoft.com/en-us/store/)) para uso com instalações do Project Online e no local. Macros VBA e suplementos do VSTO não podem ser distribuídos no Office Store; eles foram projetados para uso local com o Project Standard e Project Professional. Você pode distribuir as macros VBA em um projeto. Arquivo MPP, instalá-los no arquivo global. mpt em seu computador ou distribuí-las no modelo global da empresa no Project Server 2013. Suplementos do VSTO podem ser distribuídos com mais segurança por meio da implantação do [ClickOnce](https://msdn.microsoft.com/library/t71a733d.aspx) , que permite que atualizações fácil. 
  
## <a name="reference"></a>Referência

[Referência para desenvolvedores VBA do Project](https://msdn.microsoft.com/library/ee861523%28office.15%29.aspx) Contém introdutório e artigos de Ajuda do VBA. 
  
## <a name="related-sections"></a>Se��es relacionadas

[Arquitetura do Project Server 2013](project-server-2013-architecture.md) Mostra como os clientes do Project interagem com o Project Server. 
  
## <a name="see-also"></a>Confira também

- [Project para desenvolvedores](https://msdn.microsoft.com/office/aa905469)
- [Central de desenvolvedores do Office](https://dev.office.com)
- [Central de desenvolvedores do Visual Studio](https://msdn.microsoft.com/vstudio/aa718325.aspx)
- [Implantação e segurança do ClickOnce](https://msdn.microsoft.com/library/t71a733d.aspx)
- [Referência de campos disponíveis](https://support.office.com/en-us/article/available-fields-reference-615a4563-1cc3-40f4-b66f-1b17e793a460)

