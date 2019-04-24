---
title: Sobre o assembly de interoperabilidade do InfoPath XML
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- interoperabilidade de msxml [infopath 2007], InfoPath 2007, assembly de interoperabilidade principal XML, assembly de interoperabilidade XML do InfoPath
localization_priority: Normal
ms.assetid: fb28659b-8a71-4f43-9121-2c748fb2c5e1
description: O assembly de interoperabilidade XML do InfoPath é fornecido a fim de permitir suporte para interoperabilidade entre o código gerenciado e o servidor de COM expostos pelo Microsoft XML Core Services (MSXML) em aplicativos externos que automatizam o InfoPath.
ms.openlocfilehash: 8d47fb58c5133fa14ac78aa8fb29278b70c26abb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303777"
---
# <a name="about-the-infopath-xml-interop-assembly"></a><span data-ttu-id="a73f7-104">Sobre o assembly de interoperabilidade do InfoPath XML</span><span class="sxs-lookup"><span data-stu-id="a73f7-104">About the InfoPath XML interop assembly</span></span>

<span data-ttu-id="a73f7-105">O assembly de interoperabilidade XML do InfoPath é fornecido a fim de permitir suporte para interoperabilidade entre o código gerenciado e o servidor de COM expostos pelo Microsoft XML Core Services (MSXML) em aplicativos externos que automatizam o InfoPath.</span><span class="sxs-lookup"><span data-stu-id="a73f7-105">The InfoPath XML interop assembly is provided to allow support for interoperability between managed code and the COM server exposed by Microsoft XML Core Services (MSXML) from external applications that automate InfoPath.</span></span>

<span data-ttu-id="a73f7-106">A opção **Suporte à Programação .NET** no programa de configuração do InfoPath instala três assemblies de interoperabilidade.</span><span class="sxs-lookup"><span data-stu-id="a73f7-106">The **.NET Programmability Support** option in the InfoPath setup program installs three interop assemblies.</span></span> <span data-ttu-id="a73f7-107">Os assemblies de interoperabilidade são assemblies .NET que atuam como uma ponte entre código gerenciado e não gerenciado, mapeando membros de objeto COM para membros gerenciados .NET equivalentes.</span><span class="sxs-lookup"><span data-stu-id="a73f7-107">Interop assemblies are .NET assemblies that act as a bridge between managed and unmanaged code, mapping COM object members to equivalent .NET managed members.</span></span> <span data-ttu-id="a73f7-108">Um desses assemblies, Microsoft.Office.Interop.InfoPath.Xml.dll, fornece os membros do namespace [ Microsoft.Office.Interop.InfoPath.Xml ](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.infopath.xml?view=infopath-external), que é usado para trabalhar com membros expostos pelo servidor de COM para Microsoft XML Core Services (MSXML) a partir de aplicativos externos que automatizam o InfoPath usando código gerenciado.</span><span class="sxs-lookup"><span data-stu-id="a73f7-108">One of those assemblies, Microsoft.Office.Interop.InfoPath.Xml.dll, provides the members of the [Microsoft.Office.Interop.InfoPath.Xml](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.infopath.xml?view=infopath-external) namespace, which is used to work with members exposed by the COM server for Microsoft XML Core Services (MSXML) from external applications that automate InfoPath using managed code.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a73f7-109">As referências para os assemblies de interoperabilidade Microsoft.Office.Interop.InfoPath.dll e Microsoft.Office.Interop.InfoPath.Xml.dll que são necessárias para projetos de automação externa do InfoPath devem ser estabelecidas manualmente.</span><span class="sxs-lookup"><span data-stu-id="a73f7-109">The references to the Microsoft.Office.Interop.InfoPath.dll and Microsoft.Office.Interop.InfoPath.Xml.dll interop assemblies that are required for InfoPath external automation projects must be established manually.</span></span> <span data-ttu-id="a73f7-110">Para saber mais sobre automação externa, confira [Cenários e exemplos de automação externa](external-automation-scenarios-and-examples.md).</span><span class="sxs-lookup"><span data-stu-id="a73f7-110">For more information on external automation, see [External Automation Scenarios and Examples](external-automation-scenarios-and-examples.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a73f7-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="a73f7-111">See also</span></span>

- [<span data-ttu-id="a73f7-112">Trabalhar com MSXML e System.Xml usando o modelo de objeto do InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="a73f7-112">Working with MSXML and System.Xml Using the InfoPath 2003 Object Model</span></span>](https://msdn.microsoft.com/library/f7a0cac5-26f9-49ed-b52c-0240ef0c9d38%28Office.15%29.aspx)

