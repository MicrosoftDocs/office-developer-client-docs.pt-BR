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
# <a name="sql-expressions"></a><span data-ttu-id="056b3-102">Expressões SQL</span><span class="sxs-lookup"><span data-stu-id="056b3-102">SQL expressions</span></span>

<span data-ttu-id="056b3-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="056b3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="056b3-p101">Uma expressão SQL é uma sequência que compõe toda ou parte de uma instrução SQL. Por exemplo, o método **FindFirst** em um objeto **Recordset** usa uma expressão SQL que consiste nos critérios de seleção localizados em uma [cláusula WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) do SQL.</span><span class="sxs-lookup"><span data-stu-id="056b3-p101">An SQL expression is a string that makes up all or part of an SQL statement. For example, the **FindFirst** method on a **Recordset** object uses an SQL expression consisting of the selection criteria found in an SQL [WHERE clause](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql).</span></span>

<span data-ttu-id="056b3-106">O mecanismo de banco de dados do Microsoft Access usa o serviço de expressões do Microsoft Visual Basic for Applications (ou VBA) para executar a avaliação de função e aritmética simple.</span><span class="sxs-lookup"><span data-stu-id="056b3-106">The Microsoft Access database engine uses the Microsoft Visual Basic for Applications (or VBA) expression service to perform simple arithmetic and function evaluation.</span></span> <span data-ttu-id="056b3-107">Todos os operadores usados nas expressões de SQL de mecanismo de banco de dados de Microsoft Access (exceto **[entre](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/and-operator)**, **[no](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-operator-microsoft-access-sql)** e **[como](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)**) são definidos pelo serviço de expressão VBA.</span><span class="sxs-lookup"><span data-stu-id="056b3-107">All of the operators used in Microsoft Access database engine SQL expressions (except **[Between](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/and-operator)**, **[In](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-operator-microsoft-access-sql)**, and **[Like](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)**) are defined by the VBA expression service.</span></span> <span data-ttu-id="056b3-108">Além disso, o serviço de expressões do VBA oferece mais de 100 funções VBA que podem ser utilizadas nas expressões SQL.</span><span class="sxs-lookup"><span data-stu-id="056b3-108">In addition, the VBA expression service offers over 100 VBA functions that you can use in SQL expressions.</span></span> <span data-ttu-id="056b3-109">Por exemplo, você pode usar essas funções VBA para compor uma consulta SQL no modo de Design da consulta do Microsoft Access, e você também pode usar essas funções em uma consulta SQL no método **OpenRecordset** do DAO no Microsoft Visual C++, Microsoft Visual Basic e Microsoft Código do Excel.</span><span class="sxs-lookup"><span data-stu-id="056b3-109">For example, you can use these VBA functions to compose an SQL query in the Microsoft Access query Design view, and you can also use these functions in an SQL query in the DAO **OpenRecordset** method in Microsoft Visual C++, Microsoft Visual Basic, and Microsoft Excel code.</span></span>

## <a name="see-also"></a><span data-ttu-id="056b3-110">Confira também</span><span class="sxs-lookup"><span data-stu-id="056b3-110">See also</span></span>

- [<span data-ttu-id="056b3-111">Conceitos VBA do Access</span><span class="sxs-lookup"><span data-stu-id="056b3-111">Access VBA Concepts</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/concepts-access-vba-reference)