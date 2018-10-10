---
title: 'Capítulo 14: Fundamentos do ADO MD'
TOCTitle: 'Chapter 14: ADO MD Fundamentals'
ms:assetid: 129baa54-0bc1-985d-4bfd-25a1c1c3018e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248899(v=office.15)
ms:contentKeyID: 48543346
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5d595136c229234dfa0cb04a44fbe45f58cd79fe
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462875"
---
# <a name="chapter-14-ado-md-fundamentals"></a>Capítulo 14: Fundamentos do ADO MD


**Aplica-se a**: Access 2013 | Office 2013

O Microsoft ActiveX Data Objects (Multidimensional) (ADO MD) oferece acesso fácil a dados multidimensionais de linguagens como Microsoft Visual Basic, Microsoft Visual C++ e Microsoft Visual J++. O ADO MD amplia o Microsoft ActiveX Data Objects (ADO) para incluir objetos específicos de dados multidimensionais, como os objetos [CubeDef](cubedef-object-ado-md.md) e [Cellset](cellset-object-ado-md.md). Com o ADO MD, você pode procurar esquemas multidimensionais, consultar um cubo e recuperar os resultados.

Como o ADO, o ADO MD usa um provedor de OLE DB subjacente para obter acesso aos dados. Para utilizar o ADO MD, o provedor deve ser um MDP (provedor de dados multidimensionais), como definido na especificação do OLE DB para OLAP. Os MDPs apresentam dados em modos de exibição multidimensionais, ao contrário de TDPs (provedores de dados tabulares) que apresentam dados em modos de exibição tabulares. Consulte a documentação do provedor OLE DB para OLAP para obter informações mais detalhadas sobre a sintaxe e os comportamentos específicos aos quais seu provedor oferece suporte.

Este documento pressupõe que o usuário tenha experiência na linguagem de programação Visual Basic e conhecimento geral sobre ADO e OLAP. Para obter mais informações, consulte a documentação [Guia de programação do ADO](ado-programmer-s-guide.md) e Referência do programador do OLE DB para OLAP (OLE DB for OLAP Programmer's Reference). Para obter mais informações sobre o ADO MD, consulte os seguintes tópicos:

  - [Visão geral de esquemas e dados multidimensionais](overview-of-multidimensional-schemas-and-data.md)

  - [Trabalhando com dados multidimensionais](working-with-multidimensional-data.md)

  - [Usando o ADO com o ADO MD](using-ado-with-ado-md.md)

  - [Programando com o ADO MD](programming-with-ado-md.md)

