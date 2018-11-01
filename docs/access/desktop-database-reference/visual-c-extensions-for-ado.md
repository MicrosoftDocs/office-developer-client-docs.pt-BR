---
title: Extensões do Visual C++ para ADO
TOCTitle: Visual C++ Extensions for ADO
ms:assetid: 38048ae0-1dae-9e5e-c569-04011df8b5aa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249134(v=office.15)
ms:contentKeyID: 48544212
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f4e0d9e9f5db8741cb04fd4d576ea67408285aac
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881759"
---
# <a name="visual-c-extensions-for-ado"></a>Extensões do Visual C++ para ADO


**Aplica-se a**: Access 2013, o Office 2013

O método preferencial de programação ADO com o Visual C++ está usando o ** \#importar** diretiva, conforme discutido no [Microsoft Visual C++ ADO Programming](visual-c-ado-programming.md). Entretanto, as versões anteriores do ADO eram fornecidas com um método alternativo de programação utilizando o C++: as Extensões do Visual C++. Esta seção documenta esse recurso para aqueles que deve manter o código de extensões do Visual C++, mas o novo código ADO deve ser escrito usando \# **Importar**.

Um dos trabalhos mais tediosos que os programadores do Visual C++ enfrentam ao recuperar dados com o ADO é a conversão de dados retornados como um tipo de dados VARIANT em um tipo de dados C++ e, em seguida, o repositório dos dados convertidos em uma classe ou estrutura. Além de ser trabalhosa, a recuperação dos dados C++ por meio de tipo de dados VARIANT reduz o desempenho.

O ADO fornece uma interface que oferece suporte à recuperação de dados em tipos de dados C/C++ nativos sem o uso de uma VARIANT, além de fornecer também macros pré-processadoras que simplificam o uso da interface. O resultado é uma ferramenta flexível, mais fácil de usar e com um excelente desempenho.

Um cenário de cliente C/C++ comum é vincular um registro a um [Recordset](recordset-object-ado.md) para uma estrutura ou classe C/C++ contendo tipos nativos de C/C++. O uso de VARIANTs envolve a gravação do código de conversão da VARIANT para os tipos nativos de C/C++. As Extensões do Visual C++ para ADO visam facilitar esse cenário para o programador do Visual C++.

Consulte os tópicos a seguir para saber mais sobre as Extensões do Visual C++ para ADO.

  - [Usando Extensões do Visual C++ para ADO](using-visual-c-extensions.md)

  - [Cabeçalho das Extensões do Visual C++](visual-c-extensions-header.md)

  - [ADO com exemplo de Extensões do Visual C++](visual-c-extensions-example.md)

