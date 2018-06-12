---
title: Sobre o assembly de interoperabilidade do InfoPath XML
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- interoperabilidade do MSXML [infopath 2007], InfoPath 2007, o assembly de interoperabilidade primário do XML, o assembly de interoperabilidade do InfoPath XML
localization_priority: Normal
ms.assetid: fb28659b-8a71-4f43-9121-2c748fb2c5e1
description: O assembly de interoperabilidade do InfoPath XML é fornecido para permitir que o suporte para a interoperabilidade entre o servidor COM expostos pelo Microsoft XML Core Services (MSXML) a partir dos aplicativos externos que automatizam o InfoPath e o código gerenciado.
ms.openlocfilehash: 8d3fb1c1de141fe23c655e82b77d83a8e2b11abd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765483"
---
# <a name="about-the-infopath-xml-interop-assembly"></a>Sobre o assembly de interoperabilidade do InfoPath XML

O assembly de interoperabilidade do InfoPath XML é fornecido para permitir que o suporte para a interoperabilidade entre o servidor COM expostos pelo Microsoft XML Core Services (MSXML) a partir dos aplicativos externos que automatizam o InfoPath e o código gerenciado.

A opção de **Suporte à programação do .NET** no programa de instalação do InfoPath instala os assemblies de interoperabilidade três. Os assemblies de interoperabilidade são assemblies .NET que agem como uma ponte entre código gerenciado e, mapeamento de membros do objeto COM ao equivalente .NET gerenciado membros. Um desses assemblies, Microsoft.Office.Interop.InfoPath.Xml.dll, fornece os membros do namespace [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/en-us/library/microsoft.office.interop.infopath.xml) , que são utilizados para trabalhar com os membros expostos pelo servidor COM para o Microsoft XML Core Services (MSXML) dos aplicativos externos que automatizam o InfoPath usando código gerenciado. 
  
> [!NOTE]
> As referências a assemblies de interoperabilidade a Microsoft.Office.Interop.InfoPath.dll e Microsoft.Office.Interop.InfoPath.Xml.dll que são necessários para projetos de automação externa do InfoPath devem ser estabelecidas manualmente. Para obter mais informações sobre automação externa, consulte [os cenários de automação externa e exemplos](external-automation-scenarios-and-examples.md). 
  
## <a name="see-also"></a>Confira também

- [Trabalhando com MSXML e System. XML usando o modelo de objeto do InfoPath 2003](http://msdn.microsoft.com/library/f7a0cac5-26f9-49ed-b52c-0240ef0c9d38%28Office.15%29.aspx)

