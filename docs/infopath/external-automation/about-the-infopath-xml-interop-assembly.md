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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386821"
---
# <a name="about-the-infopath-xml-interop-assembly"></a>Sobre o assembly de interoperabilidade do InfoPath XML

O assembly de interoperabilidade XML do InfoPath é fornecido a fim de permitir suporte para interoperabilidade entre o código gerenciado e o servidor de COM expostos pelo Microsoft XML Core Services (MSXML) em aplicativos externos que automatizam o InfoPath.

A opção **Suporte à Programação .NET** no programa de configuração do InfoPath instala três assemblies de interoperabilidade. Os assemblies de interoperabilidade são assemblies .NET que atuam como uma ponte entre código gerenciado e não gerenciado, mapeando membros de objeto COM para membros gerenciados .NET equivalentes. Um desses assemblies, Microsoft.Office.Interop.InfoPath.Xml.dll, fornece os membros do namespace [ Microsoft.Office.Interop.InfoPath.Xml ](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.infopath.xml?view=infopath-external), que é usado para trabalhar com membros expostos pelo servidor de COM para Microsoft XML Core Services (MSXML) a partir de aplicativos externos que automatizam o InfoPath usando código gerenciado. 
  
> [!NOTE]
> As referências para os assemblies de interoperabilidade Microsoft.Office.Interop.InfoPath.dll e Microsoft.Office.Interop.InfoPath.Xml.dll que são necessárias para projetos de automação externa do InfoPath devem ser estabelecidas manualmente. Para saber mais sobre automação externa, confira [Cenários e exemplos de automação externa](external-automation-scenarios-and-examples.md). 
  
## <a name="see-also"></a>Confira também

- [Trabalhar com MSXML e System.Xml usando o modelo de objeto do InfoPath 2003](https://msdn.microsoft.com/library/f7a0cac5-26f9-49ed-b52c-0240ef0c9d38%28Office.15%29.aspx)

