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
- vba, modelo de objeto do projeto,Project, programabilidade,Programação, Project VBA,Visual Basic for Applications, modelo de objeto do Project, VBA, modelo de objeto,VBA,Visual Basic for Applications
localization_priority: Normal
ms.assetid: 0ad49ff6-8dff-4379-a52c-d292c53c2bc0
description: Os aplicativos clientes da área de trabalho do Project 2013 — Project Standard 2013 e Project Professional 2013 — podem ser personalizados e estendidos usando o VBA para gravar macros. Você pode usar o Visual Studio 2012 para personalizar a interface do usuário da faixa de opções e criar complementos complexos. Os Complementos do Office permitem um novo modelo de extensibilidade para painéis de tarefas no Project que são construídos em uma plataforma comum do Office 2013. O Project Standard 2013 e o Project Professional 2013 podem executar Os Complementos gerais do Office e usar os complementos do painel de tarefas desenvolvidos especificamente para o Project se integrarem ao SharePoint, a outros sites e aplicativos Web e dados externos.
ms.openlocfilehash: cc345f0ff91dfb573dd86c256e89df478edd4924
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301509"
---
# <a name="project-client-programming"></a>Programação de cliente do Project

Os aplicativos clientes da área de trabalho do Project 2013 — Project Standard 2013 e Project Professional 2013 — podem ser personalizados e estendidos usando o VBA para gravar macros. Você pode usar o Visual Studio 2012 para personalizar a interface do usuário da faixa de opções e criar complementos complexos. Os Complementos do Office permitem um novo modelo de extensibilidade para painéis de tarefas no Project que são construídos em uma plataforma comum do Office 2013. O Project Standard 2013 e o Project Professional 2013 podem executar Os Complementos gerais do Office e usar os complementos do painel de tarefas desenvolvidos especificamente para o Project se integrarem ao SharePoint, outros sites e aplicativos Web e dados externos.
  
 **Mudando para o Visual Studio** O VBA é útil para gravar macros e desenvolver soluções de automação relativamente simples. Para desenvolver complementos de painel de tarefas, complementos e soluções mais complexas, seguras, escalonáveis e facilmente implantadas, recomendamos que você use o Visual Studio 2012. O Microsoft .NET Framework 4.0 e o assembly de interop primário do Project 2013 oferecem muitas vantagens para desenvolver e implantar soluções que automatizam e integram os clientes de área de trabalho do Project 2013. 
  
> [!NOTE]
> Você pode usar o Visual Studio 2010 para desenvolver os complementos do Project. No entanto, o Visual Studio 2012 inclui modelos e extensões projetados para criar clientes de Complementos do Office. 
  
O modelo de objeto **MSProject** para VBA no Project 2013 é essencialmente o mesmo que o modelo de objeto **Microsoft.Office.Interop.MSProject** para soluções de código gerenciado com Office Developer Tools para Visual Studio 2013 (também conhecido como VSTO). O Visual Studio 2012 inclui modelos para o desenvolvimento de complementos no nível do aplicativo para o Project 2010 e para o Project 2013 (as versões do Project Standard ou do Project Professional). O VSTO e o Office Developer Tools para Visual Studio 2012 simplificam o desenvolvimento, o teste e a implantação de soluções avançadas de integração que podem usar o cliente de área de trabalho do Project e outros aplicativos do Office 2013 e integrar com sites, listas e fluxos de trabalho do SharePoint. 
  
Os complementos do painel de tarefas e outros para o Office e o SharePoint podem ser vendidos na Office Store (veja ) para uso com o Project Online e instalações [https://office.microsoft.com/store/](https://office.microsoft.com/en-us/store/) locais. Macros VBA e complementos VSTO não podem ser distribuídos na Office Store; eles foram projetados para uso local com o Project Standard e o Project Professional. Você pode distribuir macros VBA dentro de um projeto. Arquivo MPP, instale-os no arquivo Global.MPT no computador ou distribua-os no modelo global da empresa no Project Server 2013. Os complementos VSTO podem ser distribuídos com mais segurança por meio da implantação [do ClickOnce,](https://msdn.microsoft.com/library/t71a733d.aspx) que permite atualizações fáceis. 
  
## <a name="reference"></a>Referência

[Referência do desenvolvedor do VBA do Project](https://msdn.microsoft.com/library/ee861523%28office.15%29.aspx) Contém artigos introdutórios e da Ajuda do VBA. 
  
## <a name="related-sections"></a>Seções relacionadas

[Arquitetura do Project Server 2013](project-server-2013-architecture.md) Mostra como os clientes do Project interagem com o Project Server. 
  
## <a name="see-also"></a>Confira também

- [Project para desenvolvedores](https://msdn.microsoft.com/office/aa905469)
- [Central de desenvolvedores do Office](https://dev.office.com)
- [Central de desenvolvedores do Visual Studio](https://msdn.microsoft.com/vstudio/aa718325.aspx)
- [Segurança e implantação do ClickOnce](https://msdn.microsoft.com/library/t71a733d.aspx)
- [Referência de campos disponíveis](https://support.office.com/en-us/article/available-fields-reference-615a4563-1cc3-40f4-b66f-1b17e793a460)

