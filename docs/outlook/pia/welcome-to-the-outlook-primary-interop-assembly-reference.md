---
title: Referência de assembly de interoperabilidade primário do Outlook
TOCTitle: '@NoTitle'
ms:assetid: 54bdde85-8dc9-4498-a1ac-f72eaf8f0cd3
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb652780(v=office.15)
ms:contentKeyID: 55119771
ms.date: 09/15/2015
mtps_version: v=office.15
f1_keywords:
- Outlook 2010, programming
- Outlook 2010, object model
- Outlook 2010, PIA
- Outlook code samples
- Outlook 2010, primary interop assembly
- primary interop assembly [Outlook 2010]
- PIA [Outlook 2010]
- reference [Outlook 2010], primary interop assembly
localization_priority: Normal
ms.openlocfilehash: 53c50c447c6f132c562a1a22934df646347a51bc
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701449"
---
# <a name="outlook-primary-interop-assembly-reference"></a><span data-ttu-id="ede18-102">Referência de assembly de interoperabilidade primário do Outlook</span><span class="sxs-lookup"><span data-stu-id="ede18-102">Outlook Primary Interop Assembly reference</span></span>

<span data-ttu-id="ede18-103">A referência de PIA (assembly de interoperabilidade primária) do Outlook 2013 fornece ajuda para o desenvolvimento de aplicativos gerenciados para o Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="ede18-103">The Outlook 2013 Primary Interop Assembly (PIA) reference provides help for developing managed applications for Outlook 2013.</span></span> <span data-ttu-id="ede18-104">Ela estende a Referência do desenvolvedor do[Outlook 2013](https://docs.microsoft.com/office/vba/api/overview/outlook) do ambiente COM para o ambiente gerenciado e se concentra em como usar o PIA.</span><span class="sxs-lookup"><span data-stu-id="ede18-104">It extends the [Outlook 2013 Developer Reference](https://docs.microsoft.com/office/vba/api/overview/outlook) from the COM environment to the managed environment and focuses on how to use the PIA.</span></span> <span data-ttu-id="ede18-105">Inclui todas as adições e alterações no modelo de objeto no Outlook 2013 e fornece vários exemplos de código no C\# e do Visual Basic para mostrar como realizar tarefas comuns no Outlook.</span><span class="sxs-lookup"><span data-stu-id="ede18-105">It includes all the additions and changes to the object model in Outlook 2013, and provides many code samples in C\# and Visual Basic to show how to perform common tasks in Outlook.</span></span>

<span data-ttu-id="ede18-106">Se você está começando a desenvolver soluções para o Outlook, confira [Selecionando uma API e tecnologia para desenvolver soluções para o Outlook](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md) para identificar as APIs e tecnologias mais adequadas às suas necessidades.</span><span class="sxs-lookup"><span data-stu-id="ede18-106">If you are new to developing solutions for Outlook, see [Selecting an API or technology for developing solutions for Outlook](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md) to identify the APIs and technologies that are most appropriate for your needs.</span></span>

## <a name="purpose-of-the-outlook-pia-reference"></a><span data-ttu-id="ede18-107">Finalidade de referência ao Outlook PIA</span><span class="sxs-lookup"><span data-stu-id="ede18-107">Purpose of the Outlook PIA reference</span></span>

<span data-ttu-id="ede18-108">Se você estiver começando a escrever suplementos do Outlook, primeiro deve consultar o conteúdo conceitual na referência do desenvolvedor do Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="ede18-108">If you are just beginning to write add-ins for Outlook, you should first refer to the conceptual content in the Outlook 2013 Developer Reference.</span></span> <span data-ttu-id="ede18-109">Embora o ambiente de programação, de acesso a alguns métodos e de conexão com eventos sejam diferentes no COM e no desenvolvimento gerenciados, os recursos no modelo de objeto do Outlook se comportam da mesma forma no desenvolvimento gerenciado e no COM.</span><span class="sxs-lookup"><span data-stu-id="ede18-109">Even though the programming environment and accessing certain methods and connecting to events are different in COM and in managed development, features in the Outlook object model behave the same way in both COM and managed development.</span></span> <span data-ttu-id="ede18-110">Você pode consultar o conteúdo conceitual de referência do desenvolvedor do Outlook 2013 para entender como usar diferentes recursos do modelo de objeto.</span><span class="sxs-lookup"><span data-stu-id="ede18-110">You can refer to the conceptual content in the Outlook 2013 Developer Reference to understand how to use the different features of the object model.</span></span>

<span data-ttu-id="ede18-111">Se você tiver um conhecimento básico de modelo de objeto do Outlook e está aprendendo a desenvolver suplementos gerenciados do Outlook, confira [configurar uso do Outlook PIA](setting-up-to-use-the-outlook-pia.md).</span><span class="sxs-lookup"><span data-stu-id="ede18-111">If you have a basic understanding of the Outlook object model and are learning to develop managed Outlook add-ins, see [Setting up to use the Outlook PIA](setting-up-to-use-the-outlook-pia.md).</span></span> 

<span data-ttu-id="ede18-112">Para saber mais sobre o desenvolvimento gerenciado de soluções Office usando ferramentas de desenvolvedor do Office para o Visual Studio 2013, confira [Office para desenvolvimento no Visual Studio](https://docs.microsoft.com/visualstudio/vsto/office-and-sharepoint-development-in-visual-studio?view=vs-2017).</span><span class="sxs-lookup"><span data-stu-id="ede18-112">For information about developing managed Office solutions by using Office Developer Tools for Visual Studio 2013, see [Office Development in Visual Studio](https://docs.microsoft.com/visualstudio/vsto/office-and-sharepoint-development-in-visual-studio?view=vs-2017).</span></span> 

<span data-ttu-id="ede18-113">Para saber mais sobre como programar algumas tarefas básicas do Outlook no Visual Basic e C\#, confira [soluções Outlook](https://docs.microsoft.com/visualstudio/vsto/outlook-solutions?view=vs-2017).</span><span class="sxs-lookup"><span data-stu-id="ede18-113">For information about how to program some basic Outlook tasks in both Visual Basic and C\#, see [Outlook solutions](https://docs.microsoft.com/visualstudio/vsto/outlook-solutions?view=vs-2017).</span></span> 

<span data-ttu-id="ede18-114">Para exemplos de códigos mais avançados, confira [como faço para... (Outlook 2013 PIA referência) ](how-do-i-outlook-2013-pia-reference.md) nesta referência.</span><span class="sxs-lookup"><span data-stu-id="ede18-114">For more advanced code examples, see [How do I... (Outlook 2013 PIA Reference)](how-do-i-outlook-2013-pia-reference.md) in this reference.</span></span>

<span data-ttu-id="ede18-115">Se você já estiver familiarizado com o modelo de objeto do Outlook, tiver alguma experiência com aplicativos gerenciados e estiver usando o Outlook PIA pela primeira vez, comece por [instalação e a referência PIA Outlook](installing-and-referencing-the-outlook-pia.md) e[ A arquitetura do Outlook PIA](architecture-of-the-outlook-pia.md).</span><span class="sxs-lookup"><span data-stu-id="ede18-115">If you are already familiar with the Outlook object model, you have some experience writing managed applications, and you are using the Outlook PIA for the first time, start with [Installing and referencing the Outlook PIA](installing-and-referencing-the-outlook-pia.md) and [Architecture of the Outlook PIA](architecture-of-the-outlook-pia.md).</span></span>

## <a name="accessing-the-outlook-pia-reference-in-design-time"></a><span data-ttu-id="ede18-116">Acessar a referência Outlook PIA em tempo de design</span><span class="sxs-lookup"><span data-stu-id="ede18-116">Accessing the Outlook PIA reference in design time</span></span>

<span data-ttu-id="ede18-117">Se você usar ferramentas de desenvolvedor do Office para o Visual Studio 2013 e estiver conectado à Internet, você pode acessar a Ajuda contextual pressionando F1 no ambiente de desenvolvimento integrado do Visual Studio (interface IDE).</span><span class="sxs-lookup"><span data-stu-id="ede18-117">If you use Office Developer Tools for Visual Studio 2013 and you are connected to the Internet, you can access context-sensitive Help when you press F1 in the Visual Studio integrated development environment (IDE).</span></span> <span data-ttu-id="ede18-118">Esse conteúdo da Ajuda é a referência PIA do Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="ede18-118">This Help content is the Outlook 2013 PIA reference.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ede18-119">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="ede18-119">In this section</span></span>

- [<span data-ttu-id="ede18-120">Quais são as novidades na referência ao Outlook PIA</span><span class="sxs-lookup"><span data-stu-id="ede18-120">What's new in the Outlook PIA reference</span></span>](what-s-new-in-the-outlook-pia-reference.md)
- [<span data-ttu-id="ede18-121">Como realizar a configuração para usar o PIA do Outlook</span><span class="sxs-lookup"><span data-stu-id="ede18-121">Setting up to use the Outlook PIA</span></span>](setting-up-to-use-the-outlook-pia.md)
- [<span data-ttu-id="ede18-122">Arquitetura do PIA do Outlook</span><span class="sxs-lookup"><span data-stu-id="ede18-122">Architecture of the Outlook PIA</span></span>](architecture-of-the-outlook-pia.md)
- [<span data-ttu-id="ede18-123">Desenvolvimento de suplementos gerenciados do Outlook usando o Outlook PIA</span><span class="sxs-lookup"><span data-stu-id="ede18-123">Developing managed Outlook add-ins using the Outlook PIA</span></span>](developing-managed-outlook-add-ins-using-the-outlook-pia.md)
- [<span data-ttu-id="ede18-124">Como faço para... (Referência do PIA do Outlook 2013)</span><span class="sxs-lookup"><span data-stu-id="ede18-124">How do I... (Outlook 2013 PIA Reference)</span></span>](how-do-i-outlook-2013-pia-reference.md)
- [<span data-ttu-id="ede18-125">Biblioteca de Classes</span><span class="sxs-lookup"><span data-stu-id="ede18-125">Class library</span></span>](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook?view=outlook-pia)

## <a name="see-also"></a><span data-ttu-id="ede18-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="ede18-126">See also</span></span>

- [<span data-ttu-id="ede18-127">Central de desenvolvimento do Outlook</span><span class="sxs-lookup"><span data-stu-id="ede18-127">Outlook Developer Center</span></span>](../outlook-home.md)
- [<span data-ttu-id="ede18-128">COM e interoperabilidade .NET</span><span class="sxs-lookup"><span data-stu-id="ede18-128">COM and .NET Interoperability</span></span>](https://www.apress.com/us/book/9781590590119)
- [<span data-ttu-id="ede18-129">Office para desenvolvimento no Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ede18-129">Office Development in Visual Studio</span></span>](https://docs.microsoft.com/visualstudio/vsto/office-and-sharepoint-development-in-visual-studio?view=vs-2017)
- [<span data-ttu-id="ede18-130">Acessibilidade em produtos Microsoft</span><span class="sxs-lookup"><span data-stu-id="ede18-130">Accessibility in Microsoft Products</span></span>](https://www.microsoft.com/en-us/accessibility/)

