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
- VBA, modelo de objeto do Project, projeto, programação, programação, VBA do Project, Visual Basic for Applications, modelo de objeto do Project, VBA, modelo de objeto, VBA, Visual Basic for Applications
localization_priority: Normal
ms.assetid: 0ad49ff6-8dff-4379-a52c-d292c53c2bc0
description: Os aplicativos cliente de desktop do Project 2013, Project Standard 2013 e Project Professional 2013, podem ser personalizados e estendidos usando o VBA para escrever macros. Você pode usar o Visual Studio 2012 para personalizar a interface de usuário da faixa de opções e criar suplementos complexos. os suplementos do Office permitem um novo modelo de extensibilidade para os painéis de tarefas no projeto que são criados em uma plataforma do Office 2013 comum. O Project Standard 2013 e o Project Professional 2013 podem executar suplementos gerais do Office e usar suplementos do painel de tarefas que são desenvolvidos especificamente para o Project para integração com o SharePoint, outros sites e aplicativos Web e dados externos.
ms.openlocfilehash: cc345f0ff91dfb573dd86c256e89df478edd4924
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301509"
---
# <a name="project-client-programming"></a>Programação de cliente do Project

Os aplicativos cliente de desktop do Project 2013, Project Standard 2013 e Project Professional 2013, podem ser personalizados e estendidos usando o VBA para escrever macros. Você pode usar o Visual Studio 2012 para personalizar a interface de usuário da faixa de opções e criar suplementos complexos. os suplementos do Office permitem um novo modelo de extensibilidade para os painéis de tarefas no projeto que são criados em uma plataforma do Office 2013 comum. O Project Standard 2013 e o Project Professional 2013 podem executar suplementos gerais do Office e usar suplementos do painel de tarefas que são desenvolvidos especificamente para o Project para integração com o SharePoint, outros sites e aplicativos Web e dados externos.
  
 **Migrando para o Visual Studio** O VBA é útil para gravar macros e desenvolver soluções de automação relativamente simples. Para desenvolver suplementos de painel de tarefas, suplementos e soluções mais complexas, seguras, escaláveis e facilmente implantadas, recomendamos que você use o Visual Studio 2012. O assembly de interoperabilidade primário do Microsoft .NET Framework 4,0 e do Project 2013 oferece muitas vantagens para o desenvolvimento e a implantação de soluções que automatizam e integram os clientes de área de trabalho do Project 2013. 
  
> [!NOTE]
> Você pode usar o Visual Studio 2010 para desenvolver suplementos do Project. No enTanto, o Visual Studio 2012 inclui modelos e extensões projetados para criar clientes de suplementos do Office. 
  
O modelo de objeto do **MSProject** para VBA no Project 2013 é essencialmente o mesmo que o modelo de objeto **Microsoft. Office. Interop. MSProject** para soluções de código gerenciado com o Office Developer Tools para Visual Studio 2013 (também conhecido como VSTO). O Visual Studio 2012 inclui modelos para o desenvolvimento de suplementos de nível de aplicativo para o Project 2010 e para o Project 2013 (o Project Standard ou versões do Project Professional). O VSTO e o Office Developer Tools para Visual Studio 2012 simplificam o desenvolvimento, o teste e a implantação de soluções de integração avançada que podem usar o cliente de área de trabalho do Project e outros aplicativos do Office 2013 e integrá-los a sites, listas e fluxos. 
  
Suplementos de painel de tarefas e outros suplementos do Office e do SharePoint podem ser vendidos na Office Store (consulte [https://office.microsoft.com/store/](https://office.microsoft.com/en-us/store/)) para uso com o Project online e instalações locais. Macros VBA e suplementos VSTO não podem ser distribuídos na Office Store; Eles são projetados para uso local com o Project Standard e o Project Professional. Você pode distribuir macros do VBA dentro de um projeto. MPP, instale-os no arquivo global. MPT no computador ou distribua-os no modelo global da empresa no Project Server 2013. Os suplementos do VSTO podem ser distribuídos de forma mais segura através da implantação do [ClickOnce](https://msdn.microsoft.com/library/t71a733d.aspx) , que permite atualizações fáceis. 
  
## <a name="reference"></a>Referência

[Referência do desenvolvedor do VBA do Project](https://msdn.microsoft.com/library/ee861523%28office.15%29.aspx) Contém artigos introdutórios e de ajuda do VBA. 
  
## <a name="related-sections"></a>Seções relacionadas

[Arquitetura do Project Server 2013](project-server-2013-architecture.md) Mostra como os clientes do Project interagem com o Project Server. 
  
## <a name="see-also"></a>Confira também

- [Project para desenvolvedores](https://msdn.microsoft.com/office/aa905469)
- [Centro de desenvolvimento do Office](https://dev.office.com)
- [Centro de desenvolvedores do Visual Studio](https://msdn.microsoft.com/vstudio/aa718325.aspx)
- [Segurança e implantação do ClickOnce](https://msdn.microsoft.com/library/t71a733d.aspx)
- [Referência de campos disponíveis](https://support.office.com/en-us/article/available-fields-reference-615a4563-1cc3-40f4-b66f-1b17e793a460)

