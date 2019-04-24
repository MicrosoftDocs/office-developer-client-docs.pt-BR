---
title: Práticas recomendadas para o desenvolvimento de suplementos gerenciados do Outlook
TOCTitle: Best practices in developing managed Outlook add-ins
ms:assetid: a03246f6-2ca5-4fcb-8e63-a11cfbc8d9a0
ms:mtpsurl: https://msdn.microsoft.com/library/Bb611563(v=office.15)
ms:contentKeyID: 55119784
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 474a43c17360979b4b25ccb55c0ed48b2c9d2ef7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359077"
---
# <a name="best-practices-in-developing-managed-outlook-add-ins"></a>Práticas recomendadas para o desenvolvimento de suplementos gerenciados do Outlook

Embora os assemblies de interoperabilidade do Outlook permitam escrever soluções gerenciadas que interagem com o Outlook, o Outlook precede o .NET Framework e foi desenvolvido para oferecer suporte a programação por meio de linguagens não gerenciadas, como o Visual Basic for Applications (VBA) e o Visual Basic. Este tópico lista as áreas principais às quais ficar atento ao desenvolver um suplemento gerenciado para o Outlook.

- [Lançar objetos de modo sistemático](systematically-releasing-objects.md)
- [Usar um domínio de aplicativo separado para evitar falhas](using-a-separate-application-domain-to-avoid-crashing.md)
- [Usar um objeto de aplicativo confiável fornecido pelas Office Developer Tools para Visual Studio](using-a-trusted-application-object-provided-by-office-developer-tools-for-visual-studio.md)
- [Escopos adequadamente variáveis em manipuladores de eventos](scoping-variables-appropriately-in-event-handlers.md)
- [Evitar tecnologias sem suporte em suplementos gerenciados do Outlook](avoiding-unsupported-technologies-in-managed-outlook-add-ins.md)
- [Usar associação tardia ao depender de várias versões do Outlook](using-late-binding-if-depending-on-multiple-versions-of-outlook.md)

