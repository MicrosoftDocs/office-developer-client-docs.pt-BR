---
title: Extensões do Visual C++ para ADO
TOCTitle: Visual C++ Extensions for ADO
ms:assetid: 38048ae0-1dae-9e5e-c569-04011df8b5aa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249134(v=office.15)
ms:contentKeyID: 48544212
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fc69d3244cf6faf3aa91fe954e4b39323cf13abf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302748"
---
# <a name="visual-c-extensions-for-ado"></a>Extensões do Visual C++ para ADO


**Aplica-se ao:** Access 2013, Office 2013

O método preferencial de programação do ADO **\#** com Visual C++ é usar a diretiva de importação, conforme discutido no [Microsoft Visual C++ ADO Programming.](visual-c-ado-programming.md) Entretanto, as versões anteriores do ADO eram fornecidas com um método alternativo de programação utilizando o C++: as Extensões do Visual C++. Esta seção documenta esse recurso para aqueles que devem manter o código das Extensões do Visual C++, mas o novo código do ADO deve ser escrito usando a \# **importação.**

Um dos trabalhos mais tediosos que os programadores do Visual C++ enfrentam ao recuperar dados com o ADO é a conversão de dados retornados como um tipo de dados VARIANT em um tipo de dados C++ e, em seguida, o repositório dos dados convertidos em uma classe ou estrutura. Além de ser trabalhosa, a recuperação dos dados C++ por meio de tipo de dados VARIANT reduz o desempenho.

O ADO fornece uma interface que oferece suporte à recuperação de dados em tipos de dados C/C++ nativos sem o uso de uma VARIANT, além de fornecer também macros pré-processadoras que simplificam o uso da interface. O resultado é uma ferramenta flexível, mais fácil de usar e com um excelente desempenho.

Um cenário de cliente C/C++ comum é vincular um registro a um [Recordset](recordset-object-ado.md) para uma estrutura ou classe C/C++ contendo tipos nativos de C/C++. O uso de VARIANTs envolve a gravação do código de conversão da VARIANT para os tipos nativos de C/C++. As Extensões do Visual C++ para ADO visam facilitar esse cenário para o programador do Visual C++.

Consulte os tópicos a seguir para saber mais sobre as Extensões do Visual C++ para ADO.

  - [Usando Extensões do Visual C++ para ADO](using-visual-c-extensions.md)

  - [Cabeçalho das Extensões do Visual C++](visual-c-extensions-header.md)

  - [ADO com exemplo de Extensões do Visual C++](visual-c-extensions-example.md)

