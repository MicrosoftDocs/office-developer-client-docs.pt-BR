---
title: 'Capítulo 9: Data Shaping'
TOCTitle: 'Chapter 9: Data shaping'
ms:assetid: f66a319f-1b3d-c4a3-50b3-af1a47540832
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250253(v=office.15)
ms:contentKeyID: 48548739
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 43ad9d5e989bc1c6f4a54fb4882cfe3c3e357fd1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721551"
---
# <a name="chapter-9-data-shaping"></a>Capítulo 9: Data Shaping

**Aplica-se a**: Access 2013, o Office 2013

*Data shaping* fornece uma maneira para consultar uma fonte de dados e retornar um [Recordset](recordset-object-ado.md) que representa uma relação pai-filho entre dois ou mais entidades lógicas (uma hierarquia). 

Um exemplo clássico dessa relação envolve clientes e pedidos. Para cada cliente em um banco de dados, é possível haver zero ou mais pedidos. O SQL comum permite recuperar os dados com a sintaxe JOIN, mas isso pode ser ineficiente e difícil, pois os dados pai redundantes são repetidos em cada registro retornado para um relacionamento pai-filho específico. O data shaping pode relacionar um único registro pai no **Recordset** pai a vários registros filho no **Recordset** filho, evitando a redundância de um JOIN. A maioria das pessoas considera o modelo de programação de vários **Recordsets** pai-filho mais natural e fácil de trabalhar do que com o único modelo JOIN de **Recordset**.

A sintaxe do data shaping também permite outras possibilidades. Os desenvolvedores podem criar novos objetos **Recordset** sem qualquer fonte de dados subjacente, usando a palavra-chave NEW para descrever os campos dos **Recordsets** pai e filho. O novo objeto **Recordset** pode ser preenchido com dados e mantido de forma persistente. Os desenvolvedores também pode efetuar diversos cálculos ou agregados (por exemplo, SUM, AVG e MAX) nos campos filho. O data shaping também pode criar um **Recordset** pai a partir de um **Recordset** filho, agrupando registros no filho e inserindo uma linha no pai para cada grupo no filho.

Consulte os tópicos a seguir para saber mais sobre o data shaping:

- [Provedores necessários para Data Shaping](required-providers-for-data-shaping.md)
- [Cláusula de cálculo de forma](shape-compute-clause.md)
- [Fabricação de conjuntos de registros hierárquicos](fabricating-hierarchical-recordsets.md)
- [Acesso de linhas em um conjunto de registros hierárquico](accessing-rows-in-a-hierarchical-recordset.md)
- [Gramática formal de forma](formal-shape-grammar.md)
- [Funções do Visual Basic for Applications](visual-basic-for-applications-functions.md)
- [Cláusula Append de forma (ADO)](shape-append-clause.md)
- [Data shaping (ADO)](data-shaping.md)
- [Forma comandos em geral (ADO)](shape-commands-in-general.md)

