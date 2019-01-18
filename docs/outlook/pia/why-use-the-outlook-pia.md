---
title: Por que usar o Outlook PIA
TOCTitle: Why use the Outlook PIA
ms:assetid: 5cc9085e-7c97-4698-8cb9-e33e427c02e7
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb645534(v=office.15)
ms:contentKeyID: 55119773
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: dc882eba5f4e6c7729b81626d7324f89b724a244
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709163"
---
# <a name="why-use-the-outlook-pia"></a>Por que usar o Outlook PIA

A partir do Outlook 98, o Outlook fornece um modelo de objeto para desenvolvedores integrarem as funcionalidade do Outlook em um aplicativo, estender o Outlook ou automatizar o Outlook. O modelo de objeto foi projetado para funcionar com a tecnologia de modelo COM (Component Object). Historicamente, os desenvolvedores de aplicativos do Outlook desenvolveram soluções COM usando o Visual Basic for Applications (VBA) e Visual Basic. No entanto, as soluções Outlook desenvolvidas com o VBA tem limitações de implantação, principalmente em ambientes corporativos, e são difíceis de atualizar após sua implantação.

O .NET Framework fornece um conjunto avançado de suporte de tecnologias que aborda muitas das limitações do VBA e COM os suplementos e bibliotecas de classe. No entanto, um aplicativo gerenciado precisa de uma ponte entre os ambientes .NET e COM para programar em relação a um modelo de objeto COM do programa. Um conjunto interop é um COM wrapper que atua como uma ligação. Consequentemente, mais soluções do Outlook são desenvolvidas agora como aplicativos gerenciados que dependem um assembly de interoperabilidade. Para saber mais sobre como o assembly de interoperabilidade facilita a interoperabilidade entre o .NET, COM, confira [Introdução a interoperabilidade entre COM e .NET](introduction-to-interoperability-between-com-and-net.md).

Um módulo de interoperabilidade descreve os tipos COM e permite ao código gerenciado interagir com um modelo de objeto COM. Pode existir qualquer número de assemblies de interoperabilidade para descrever um determinado tipo COM. Como publicador da biblioteca de tipos, o Outlook fornece um Assembly de interoperabilidade principal (PIA) que contém a descrição oficial do modelo de objeto do Outlook baseado no COM. Em geral, é melhor usar o Outlook PIA ao invés de confiar em um módulo de interoperabilidade de outra fonte.

## <a name="using-visual-studio-and-office-developer-tools-for-visual-studio"></a>Usar o Visual Studio e o Office Developer Tools para Visual Studio

É possível que os desenvolvedores criem soluções Outlook gerenciadas fora do Visual Studio, mas usando o Visual Studio os recursos do Outlook integrados ao código gerenciado torna tudo muito simples. A conveniência e a maior facilidade para desenvolvimento torna mais favorável para desenvolvedores de suplemento migrarem de COM para o desenvolvimento do .NET. No momento do design, os desenvolvedores podem usar ferramentas de desenvolvedor do Office para Visual Studio para criar suplementos que tenham acesso ao modelo de objeto do Outlook e do .NET Framework. No momento da execução, as ferramentas de desenvolvedor do Office para Visual Studio são carregadas para esses suplementos: quando um usuário inicia o Outlook, esse carregador inicia a Common Language Runtime (CLR), o tempo de execução d Visual Studio Tools para Office e, em seguida, carrega o assembly do suplemento. A montagem pode capturar a eventos gerados no Outlook.

O Visual Studio 2012 instala os modelos de suplemento do Office 2010 por padrão. Para usar ferramentas de desenvolvedor do Office para Visual Studio para desenvolver gerenciados suplementos do Outlook 2013, você deve [baixar](https://aka.ms/officedevtoolsforvs2012) modelos do Office 2013.

Para saber mais sobre as ferramentas de desenvolvedor do Office para Visual Studio, confira [configurar o computador para desenvolver soluções de Office](https://docs.microsoft.com/visualstudio/vsto/how-to-configure-a-computer-to-develop-office-solutions?view=vs-2017). Para saber mais sobre a programação de suplementos gerenciados do Outlook, confira [Introdução à programação VSTO suplementos](https://docs.microsoft.com/visualstudio/vsto/getting-started-programming-vsto-add-ins?view=vs-2017).

## <a name="see-also"></a>Confira também

- [Instalar e referenciar o PIA do Outlook](installing-and-referencing-the-outlook-pia.md)

