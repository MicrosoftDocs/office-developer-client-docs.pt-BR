---
title: 'Capítulo 14: Conceitos básicos do ADO MD'
TOCTitle: 'Chapter 14: ADO MD fundamentals'
ms:assetid: 129baa54-0bc1-985d-4bfd-25a1c1c3018e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248899(v=office.15)
ms:contentKeyID: 48543346
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 44a4e666fb615f7d3870acfbd986e93971606d5b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701134"
---
# <a name="chapter-14-ado-md-fundamentals"></a>Capítulo 14: Conceitos básicos do ADO MD

**Aplica-se a**: Access 2013, o Office 2013

O Microsoft ActiveX Data Objects (Multidimensional) (ADO MD) oferece acesso fácil a dados multidimensionais de linguagens como Microsoft Visual Basic, Microsoft Visual C++ e Microsoft Visual J++. O ADO MD amplia o Microsoft ActiveX Data Objects (ADO) para incluir objetos específicos de dados multidimensionais, como os objetos [CubeDef](cubedef-object-ado-md.md) e [Cellset](cellset-object-ado-md.md). Com o ADO MD, você pode procurar esquemas multidimensionais, consultar um cubo e recuperar os resultados.

Como o ADO, o ADO MD usa um provedor de OLE DB subjacente para obter acesso aos dados. Para utilizar o ADO MD, o provedor deve ser um MDP (provedor de dados multidimensionais), como definido na especificação do OLE DB para OLAP. Os MDPs apresentam dados em modos de exibição multidimensionais, ao contrário de TDPs (provedores de dados tabulares) que apresentam dados em modos de exibição tabulares. Consulte a documentação do provedor OLE DB para OLAP para obter informações mais detalhadas sobre a sintaxe e os comportamentos específicos aos quais seu provedor oferece suporte.

Este documento pressupõe que o usuário tenha experiência na linguagem de programação Visual Basic e conhecimento geral sobre ADO e OLAP. Para obter mais informações, consulte o [Guia do programador do ADO](ado-programmer-s-guide.md) e o OLE DB para referência do programador do OLAP. 

Este capítulo aborda os seguintes tópicos:

- [Visão geral de dados e esquemas multidimensionais](overview-of-multidimensional-schemas-and-data.md)
- [Trabalhando com dados multidimensionais](working-with-multidimensional-data.md)
- [Usando o ADO com o ADO MD](using-ado-with-ado-md.md)
- [Programando com o ADO MD](programming-with-ado-md.md)
