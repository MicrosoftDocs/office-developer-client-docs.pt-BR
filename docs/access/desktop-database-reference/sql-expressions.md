---
title: Expressões SQL (referência de banco de dados da área de trabalho do Access)
TOCTitle: SQL expressions
ms:assetid: 91722f18-8589-d9fc-79ef-0be4ab11f822
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197629(v=office.15)
ms:contentKeyID: 48546349
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5a8d340f008fd198068d6dacc1b2bf847838ede1
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/07/2018
ms.locfileid: "26025732"
---
# <a name="sql-expressions"></a>Expressões SQL

**Aplica-se a**: Access 2013, o Office 2013

Uma expressão SQL é uma sequência que compõe toda ou parte de uma instrução SQL. Por exemplo, o método **FindFirst** em um objeto **Recordset** usa uma expressão SQL que consiste nos critérios de seleção localizados em uma [cláusula WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) do SQL.

O mecanismo de banco de dados do Microsoft Access usa o serviço de expressões do Microsoft Visual Basic for Applications (ou VBA) para executar a avaliação de função e aritmética simple. Todos os operadores usados nas expressões de SQL de mecanismo de banco de dados de Microsoft Access (exceto **[entre](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/and-operator)**, **[no](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-operator-microsoft-access-sql)** e **[como](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)**) são definidos pelo serviço de expressão VBA. Além disso, o serviço de expressões do VBA oferece mais de 100 funções VBA que podem ser utilizadas nas expressões SQL. Por exemplo, você pode usar essas funções VBA para compor uma consulta SQL no modo de Design da consulta do Microsoft Access, e você também pode usar essas funções em uma consulta SQL no método **OpenRecordset** do DAO no Microsoft Visual C++, Microsoft Visual Basic e Microsoft Código do Excel.

## <a name="see-also"></a>Confira também

- [Conceitos VBA do Access](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/concepts-access-vba-reference)