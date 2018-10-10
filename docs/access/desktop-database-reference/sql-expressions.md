---
title: Expressões SQL (referência de banco de dados da área de trabalho do Access)
TOCTitle: SQL Expressions
ms:assetid: 91722f18-8589-d9fc-79ef-0be4ab11f822
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197629(v=office.15)
ms:contentKeyID: 48546349
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 328804dc8186c082cf22d409b4071368af8873e2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25461982"
---
# <a name="sql-expressions"></a><span data-ttu-id="92396-102">Expressões SQL</span><span class="sxs-lookup"><span data-stu-id="92396-102">SQL Expressions</span></span>


<span data-ttu-id="92396-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="92396-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="92396-p101">Uma expressão SQL é uma sequência que compõe toda ou parte de uma instrução SQL. Por exemplo, o método **FindFirst** em um objeto **Recordset** usa uma expressão SQL que consiste nos critérios de seleção localizados em uma [cláusula WHERE](https://msdn.microsoft.com/library/ff195245\(v=office.15\)) do SQL.</span><span class="sxs-lookup"><span data-stu-id="92396-p101">An SQL expression is a string that makes up all or part of an SQL statement. For example, the**FindFirst** method on a **Recordset** object uses an SQL expression consisting of the selection criteria found in an SQL [WHERE clause](https://msdn.microsoft.com/library/ff195245\(v=office.15\)).</span></span>

<span data-ttu-id="92396-p102">O mecanismo de banco de dados Microsoft Access usa o serviço de expressões do Microsoft® Visual Basic® for Applications (ou VBA) para executar avaliação simples de aritmética e função. Todos os operadores utilizados nas expressões SQL do mecanismo de banco de dados Microsoft Access (exceto **[Between](https://msdn.microsoft.com/library/ff192436\(v=office.15\))**, **[In](https://msdn.microsoft.com/library/ff836369\(v=office.15\))** e **[Like](https://msdn.microsoft.com/library/ff195752\(v=office.15\))**) são definidos pelo serviço de expressões do VBA. Além disso, o serviço de expressões do VBA oferece mais de 100 funções VBA que podem ser utilizadas nas expressões SQL. Por exemplo, você pode usar essas funções VBA para compor uma consulta SQL na exibição Design da consulta do Microsoft Access e usa-lás também em uma consulta SQL no método **OpenRecordset** do DAO no código do Microsoft Visual C++®, Microsoft Visual Basic e Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="92396-p102">The Microsoft Access database engine uses the Microsoft® Visual Basic® for Applications (or VBA) expression service to perform simple arithmetic and function evaluation. All of the operators used in Microsoft Access database engine SQL expressions (except **[Between](https://msdn.microsoft.com/library/ff192436\(v=office.15\))**, **[In](https://msdn.microsoft.com/library/ff836369\(v=office.15\))**, and **[Like](https://msdn.microsoft.com/library/ff195752\(v=office.15\))**) are defined by the VBA expression service. In addition, the VBA expression service offers over 100 VBA functions that you can use in SQL expressions. For example, you can use these VBA functions to compose an SQL query in the Microsoft Access query Design view, and you can also use these functions in an SQL query in the DAO **OpenRecordset** method in Microsoft Visual C++®, Microsoft Visual Basic, and Microsoft Excel code.</span></span>

