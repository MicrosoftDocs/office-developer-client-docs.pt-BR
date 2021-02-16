---
title: Evitar tecnologias sem suporte em suplementos gerenciados do Outlook
TOCTitle: Avoiding unsupported technologies in managed Outlook add-ins
ms:assetid: 365fd319-725f-4c4b-b6e7-575f78ed8bda
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb610014(v=office.15)
ms:contentKeyID: 55119789
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 99cdfc2447e6bf63078eb87bb9546d8b07ee83e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359052"
---
# <a name="avoiding-unsupported-technologies-in-managed-outlook-add-ins"></a><span data-ttu-id="1f574-102">Evitar tecnologias sem suporte em suplementos gerenciados do Outlook</span><span class="sxs-lookup"><span data-stu-id="1f574-102">Avoiding unsupported technologies in managed Outlook add-ins</span></span>

<span data-ttu-id="1f574-103">Determinadas tecnologias que antecedem o .NET Framework não são compatíveis com a programação de código gerenciado.</span><span class="sxs-lookup"><span data-stu-id="1f574-103">Certain technologies that predate the .NET Framework are not supported in managed code programming.</span></span> <span data-ttu-id="1f574-104">Essas tecnologias incluem CDO (Collaboration Data Objects), MAPI (Messaging Application Programming Interface), conhecido como MAPI estendido, e Simple MAPI.</span><span class="sxs-lookup"><span data-stu-id="1f574-104">These technologies include Collaboration Data Objects (CDO), Messaging Application Programming Interface (MAPI, often known as Extended MAPI), and Simple MAPI.</span></span> <span data-ttu-id="1f574-105">Essas tecnologias foram projetadas e desenvolvidas com código não gerenciado e a Microsoft não fornece wrappers gerenciados oficiais para suportar seu uso em aplicativos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="1f574-105">These technologies were designed and developed with unmanaged code, and Microsoft does not provide official managed wrappers to support their use in managed applications.</span></span> 

<span data-ttu-id="1f574-106">Para saber mais, confira a seção "APIs que têm suporte no código gerenciado" no artigo [KB 266353: as diretrizes de suporte para desenvolvimento de mensagens do lado do cliente](https://go.microsoft.com/fwlink/?linkid=89209).</span><span class="sxs-lookup"><span data-stu-id="1f574-106">For more information, see the section "APIs that are supported in managed code" in the article [KB 266353: The support guidelines for client-side messaging development](https://go.microsoft.com/fwlink/?linkid=89209).</span></span>

<span data-ttu-id="1f574-107">No entanto, o Microsoft Outlook oferece muitos recursos de modelo de objeto que realizam o que, anteriormente, apenas o ECO e o ECE (Exchange Client Extensions) resolviam para os desenvolvedores.</span><span class="sxs-lookup"><span data-stu-id="1f574-107">Nonetheless, Microsoft Outlook offers many object model features that achieve what previously only CDO and Exchange Client Extensions (ECE) solved for developers.</span></span> <span data-ttu-id="1f574-108">Se você usa o CDO em um aplicativo do Outlook não gerenciado existente e a falta de suporte para CDO em soluções gerenciadas tiver impedido a migração do aplicativo para código gerenciado, considere atualizar sua solução para código gerenciado usando apenas o modelo de objeto do Outlook e o Assembly de Interoperabilidade Primário (PIA), sem ter que recorrer ao CDO.</span><span class="sxs-lookup"><span data-stu-id="1f574-108">If you use CDO in an existing unmanaged Outlook application and the lack of support for CDO in managed solutions has hindered you from migrating the application to managed code, you can now consider updating your solution to managed code, using only the Outlook object model and the Primary Interop Assembly (PIA), without having to resort to CDO.</span></span> 

<span data-ttu-id="1f574-109">Para ver mais informações sobre uma plataforma do Outlook mais abrangente introduzida no Outlook 2007 para reduzir a dependência do CDO e do ECE, confira [Novidades para desenvolvedores no Outlook 2007 (Parte 1 de 2)](https://msdn.microsoft.com/library/bb226711\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="1f574-109">For more information about a more comprehensive Outlook platform introduced in Outlook 2007 to reduce reliance on CDO and ECE, see [What's New for Developers in Outlook 2007 (Part 1 of 2)](https://msdn.microsoft.com/library/bb226711\(v=office.15\)).</span></span>

