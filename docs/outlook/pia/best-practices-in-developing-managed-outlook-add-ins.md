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
# <a name="best-practices-in-developing-managed-outlook-add-ins"></a><span data-ttu-id="b3082-102">Práticas recomendadas para o desenvolvimento de suplementos gerenciados do Outlook</span><span class="sxs-lookup"><span data-stu-id="b3082-102">Best practices in developing managed Outlook add-ins</span></span>

<span data-ttu-id="b3082-103">Embora os assemblies de interoperabilidade do Outlook permitam escrever soluções gerenciadas que interagem com o Outlook, o Outlook precede o .NET Framework e foi desenvolvido para oferecer suporte a programação por meio de linguagens não gerenciadas, como o Visual Basic for Applications (VBA) e o Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b3082-103">Even though the Outlook interop assemblies allow you to write managed solutions that interoperate with Outlook, Outlook predates the .NET Framework and is designed to support programmability through unmanaged languages such as Visual Basic for Applications (VBA) and Visual Basic.</span></span> <span data-ttu-id="b3082-104">Este tópico lista as áreas principais às quais ficar atento ao desenvolver um suplemento gerenciado para o Outlook.</span><span class="sxs-lookup"><span data-stu-id="b3082-104">This topic lists the top areas that you should be aware of when you develop a managed add-in for Outlook.</span></span>

- [<span data-ttu-id="b3082-105">Lançar objetos de modo sistemático</span><span class="sxs-lookup"><span data-stu-id="b3082-105">Systematically releasing objects</span></span>](systematically-releasing-objects.md)
- [<span data-ttu-id="b3082-106">Usar um domínio de aplicativo separado para evitar falhas</span><span class="sxs-lookup"><span data-stu-id="b3082-106">Using a separate application domain to avoid crashing</span></span>](using-a-separate-application-domain-to-avoid-crashing.md)
- [<span data-ttu-id="b3082-107">Usar um objeto de aplicativo confiável fornecido pelas Office Developer Tools para Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b3082-107">Using a trusted application object provided by Office Developer Tools for Visual Studio</span></span>](using-a-trusted-application-object-provided-by-office-developer-tools-for-visual-studio.md)
- [<span data-ttu-id="b3082-108">Escopos adequadamente variáveis em manipuladores de eventos</span><span class="sxs-lookup"><span data-stu-id="b3082-108">Scoping variables appropriately in event handlers</span></span>](scoping-variables-appropriately-in-event-handlers.md)
- [<span data-ttu-id="b3082-109">Evitar tecnologias sem suporte em suplementos gerenciados do Outlook</span><span class="sxs-lookup"><span data-stu-id="b3082-109">Avoiding unsupported technologies in managed Outlook add-ins</span></span>](avoiding-unsupported-technologies-in-managed-outlook-add-ins.md)
- [<span data-ttu-id="b3082-110">Usar associação tardia ao depender de várias versões do Outlook</span><span class="sxs-lookup"><span data-stu-id="b3082-110">Using late binding if depending on multiple versions of Outlook</span></span>](using-late-binding-if-depending-on-multiple-versions-of-outlook.md)

