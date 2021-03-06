---
title: Expressões SQL (referência do banco de dados da área de trabalho do Access)
TOCTitle: SQL expressions
ms:assetid: 91722f18-8589-d9fc-79ef-0be4ab11f822
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197629(v=office.15)
ms:contentKeyID: 48546349
ms.date: 06/13/2019
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: f38932ed4744e5479c523446f9ab77065f4eb203
ms.sourcegitcommit: d0e1ce095a478d90411abb8c147eb9efe19ffa5f
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/12/2019
ms.locfileid: "34870861"
---
# <a name="sql-expressions"></a>Expressões SQL

**Aplica-se ao:** Access 2013, Office 2013

Uma expressão SQL é uma sequência que compõe toda ou parte de uma instrução SQL. Por exemplo, o método **FindFirst** em um objeto **Recordset** usa uma expressão SQL que consiste nos critérios de seleção localizados em uma [cláusula WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) do SQL.

O mecanismo de banco de dados do Microsoft Access usa o Serviço de Expressão do Microsoft Visual Basic for Applications (VBA) para executar avaliações simples aritméticas e de função. Todos os operadores utilizados nas expressões SQL do mecanismo de banco de dados Microsoft Access (exceto **[Between](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/between-and-operator)**, **[In](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-operator-microsoft-access-sql)** e **[Like](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)**) são definidos pelo serviço de expressões do VBA. 

Além disso, o serviço de expressão do VBA oferece mais de 100 funções do VBA que você pode usar em expressões SQL. Por exemplo, você pode usar essas funções VBA para compor uma consulta SQL no modo de exibição Design da consulta do Microsoft Access e usá-las também em uma consulta SQL no método **OpenRecordset** do DAO no código do Microsoft Visual C++, Microsoft Visual Basic e Microsoft Excel.

## <a name="see-also"></a>Confira também

- [Acessar Conceitos do VBA](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/concepts-access-vba-reference)
