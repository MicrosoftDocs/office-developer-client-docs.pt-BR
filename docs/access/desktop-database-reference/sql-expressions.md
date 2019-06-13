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
# <a name="sql-expressions"></a><span data-ttu-id="50537-102">Expressões SQL</span><span class="sxs-lookup"><span data-stu-id="50537-102">SQL expressions</span></span>

<span data-ttu-id="50537-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="50537-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="50537-p101">Uma expressão SQL é uma sequência que compõe toda ou parte de uma instrução SQL. Por exemplo, o método **FindFirst** em um objeto **Recordset** usa uma expressão SQL que consiste nos critérios de seleção localizados em uma [cláusula WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) do SQL.</span><span class="sxs-lookup"><span data-stu-id="50537-p101">An SQL expression is a string that makes up all or part of an SQL statement. For example, the **FindFirst** method on a **Recordset** object uses an SQL expression consisting of the selection criteria found in an SQL [WHERE clause](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql).</span></span>

<span data-ttu-id="50537-106">O mecanismo de banco de dados do Microsoft Access usa o Serviço de Expressão do Microsoft Visual Basic for Applications (VBA) para executar avaliações simples aritméticas e de função.</span><span class="sxs-lookup"><span data-stu-id="50537-106">The Microsoft Access database engine uses the Microsoft Visual Basic for Applications (or VBA) expression service to perform simple arithmetic and function evaluation.</span></span> <span data-ttu-id="50537-107">Todos os operadores utilizados nas expressões SQL do mecanismo de banco de dados Microsoft Access (exceto **[Between](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/between-and-operator)**, **[In](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-operator-microsoft-access-sql)** e **[Like](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)**) são definidos pelo serviço de expressões do VBA.</span><span class="sxs-lookup"><span data-stu-id="50537-107">All of the operators used in Microsoft Access database engine SQL expressions (except **[Between](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/between-and-operator)**, **[In](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-operator-microsoft-access-sql)**, and **[Like](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)**) are defined by the VBA expression service.</span></span> 

<span data-ttu-id="50537-108">Além disso, o serviço de expressão do VBA oferece mais de 100 funções do VBA que você pode usar em expressões SQL.</span><span class="sxs-lookup"><span data-stu-id="50537-108">In addition, the VBA expression service offers over 100 VBA functions that you can use in SQL expressions.</span></span> <span data-ttu-id="50537-109">Por exemplo, você pode usar essas funções VBA para compor uma consulta SQL no modo de exibição Design da consulta do Microsoft Access e usá-las também em uma consulta SQL no método **OpenRecordset** do DAO no código do Microsoft Visual C++, Microsoft Visual Basic e Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="50537-109">For example, you can use these VBA functions to compose an SQL query in the Microsoft Access query Design view, and you can also use these functions in an SQL query in the DAO **OpenRecordset** method in Microsoft Visual C++, Microsoft Visual Basic, and Microsoft Excel code.</span></span>

## <a name="see-also"></a><span data-ttu-id="50537-110">Confira também</span><span class="sxs-lookup"><span data-stu-id="50537-110">See also</span></span>

- [<span data-ttu-id="50537-111">Acessar Conceitos do VBA</span><span class="sxs-lookup"><span data-stu-id="50537-111">Access VBA Concepts</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/concepts-access-vba-reference)
