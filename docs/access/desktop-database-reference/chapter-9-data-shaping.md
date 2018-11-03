---
title: 'Capítulo 9: Data shaping'
TOCTitle: 'Chapter 9: Data shaping'
ms:assetid: f66a319f-1b3d-c4a3-50b3-af1a47540832
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250253(v=office.15)
ms:contentKeyID: 48548739
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 53a74a53b8c741921ad51ae79ca18e95cda2923d
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936550"
---
# <a name="chapter-9-data-shaping"></a>Capítulo 9: Data shaping

**Aplica-se a**: Access 2013, o Office 2013

*Data shaping* fornece uma maneira para consultar uma fonte de dados e retornar um [Recordset](recordset-object-ado.md) que representa uma relação pai-filho entre dois ou mais entidades lógicas (uma hierarquia). 

Um exemplo clássico dessa relação envolve clientes e pedidos. Para cada cliente em um banco de dados, é possível haver zero ou mais pedidos. O SQL comum permite recuperar os dados com a sintaxe JOIN, mas isso pode ser ineficiente e difícil, pois os dados pai redundantes são repetidos em cada registro retornado para um relacionamento pai-filho específico. O data shaping pode relacionar um único registro pai no **Recordset** pai a vários registros filho no **Recordset** filho, evitando a redundância de um JOIN. A maioria das pessoas considera o modelo de programação de vários **Recordsets** pai-filho mais natural e fácil de trabalhar do que com o único modelo JOIN de **Recordset**.

A sintaxe do data shaping também permite outras possibilidades. Os desenvolvedores podem criar novos objetos **Recordset** sem qualquer fonte de dados subjacente, usando a palavra-chave NEW para descrever os campos dos **Recordsets** pai e filho. O novo objeto **Recordset** pode ser preenchido com dados e mantido de forma persistente. Os desenvolvedores também pode efetuar diversos cálculos ou agregados (por exemplo, SUM, AVG e MAX) nos campos filho. O data shaping também pode criar um **Recordset** pai a partir de um **Recordset** filho, agrupando registros no filho e inserindo uma linha no pai para cada grupo no filho.

Consulte os tópicos a seguir para saber mais sobre o data shaping:

- [Provedores necessários para o data shaping](required-providers-for-data-shaping.md)
- [Cláusula Compute de forma](shape-compute-clause.md)
- [Fabricando Recordsets hierárquicos](fabricating-hierarchical-recordsets.md)
- [Acessando as linhas em um Recordset hierárquico](accessing-rows-in-a-hierarchical-recordset.md)
- [Gramática formal de shape](formal-shape-grammar.md)
- [Funções do Visual Basic for Applications](visual-basic-for-applications-functions.md)
- [Cláusula Append de forma (ADO)](shape-append-clause.md)
- [Data shaping (ADO)](data-shaping.md)
- [Forma comandos em geral (ADO)](shape-commands-in-general.md)

