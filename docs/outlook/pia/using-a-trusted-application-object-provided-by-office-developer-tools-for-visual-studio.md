---
title: Usar um objeto de aplicativo confiável fornecido pelas Ferramentas de Desenvolvedor do Office para Visual Studio
TOCTitle: Using a trusted application object provided by Office Developer Tools for Visual Studio
ms:assetid: 3778122f-f60e-48e7-8e72-f3aef168bae2
ms:mtpsurl: https://msdn.microsoft.com/library/Bb622502(v=office.15)
ms:contentKeyID: 55119787
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f86ad294e894b4faea10d033a069638221f1bd78
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285169"
---
# <a name="using-a-trusted-application-object-provided-by-office-developer-tools-for-visual-studio"></a><span data-ttu-id="8e07f-102">Usar um objeto de aplicativo confiável fornecido pelas Ferramentas de Desenvolvedor do Office para Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8e07f-102">Using a trusted Application object provided by Office Developer Tools for Visual Studio</span></span>

<span data-ttu-id="8e07f-103">Se você estiver desenvolvendo um suplemento gerenciado usando as Ferramentas de Desenvolvedor do Office para Visual Studio, use sempre o objeto [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) que é fornecido pelo Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="8e07f-103">If you are developing a managed add-in by using Office Developer Tools for Visual Studio, always use the [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) object that is provided by Visual Studio.</span></span> 

<span data-ttu-id="8e07f-104">A menos que você pretenda automatizar uma nova instância do Outlook, não use Novo ou uma nova palavra-chave para criar uma nova instância do Outlook, já que esta instância do objeto **Application** objeto não é confiável sob a perspectiva do Outlook Object Model Guard.</span><span class="sxs-lookup"><span data-stu-id="8e07f-104">Unless you intend to automate a new instance of Outlook, do not use the New or new keyword to create a new instance of Outlook, as this instance of the **Application** object is not trusted from the perspective of the Outlook Object Model Guard.</span></span> 

<span data-ttu-id="8e07f-105">Se o suplemento usa uma instância não confiável do objeto **Application**, dependendo da versão do Outlook que o cliente esteja executando, o suplemento irá invocar por padrão o Outlook Object Model Guard em um número de membros do modelo de objeto.</span><span class="sxs-lookup"><span data-stu-id="8e07f-105">If your add-in uses an untrusted instance of the **Application** object, depending on the version of Outlook that the client is running, the add-in by default will invoke Outlook's Object Model Guard on a number of members of the object model.</span></span> 

<span data-ttu-id="8e07f-106">Para saber mais sobre o comportamento do Object Model Guard, confira [Alterações de código de segurança no Outlook 2007](https://msdn.microsoft.com/library/bb226709\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="8e07f-106">For more information about the behavior of the Object Model Guard, see [Code Security Changes in Outlook 2007](https://msdn.microsoft.com/library/bb226709\(v=office.15\)).</span></span> <span data-ttu-id="8e07f-107">Observe que, apesar de o artigo "Alterações de código de segurança no Outlook 2007" se referir aos suplementos COM que são confiáveis por padrão, este design se aplica às versões do Outlook desde o Outlook 2007, e a confiabilidade se aplica aos suplementos gerenciados da mesma maneira.</span><span class="sxs-lookup"><span data-stu-id="8e07f-107">Note that even though the "Code Security Changes in Outlook 2007" article refers to COM add-ins that are trusted by default, this design applies to versions of Outlook since Outlook 2007, and the trust applies to managed add-ins the same way.</span></span> <span data-ttu-id="8e07f-108">Independentemente de o suplemento ser gerenciado ou não, a confiabilidade é baseada na suposição de que o suplemento usa um objeto **Application** confiável.</span><span class="sxs-lookup"><span data-stu-id="8e07f-108">Regardless of whether the add-in is managed or not, the trust is based on the assumption that the add-in uses a trusted **Application** object.</span></span>

