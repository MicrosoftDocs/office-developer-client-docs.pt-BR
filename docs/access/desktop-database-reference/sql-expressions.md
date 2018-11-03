---
title: Expressões SQL (referência de banco de dados da área de trabalho do Access)
TOCTitle: SQL expressions
ms:assetid: 91722f18-8589-d9fc-79ef-0be4ab11f822
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197629(v=office.15)
ms:contentKeyID: 48546349
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 25b7d11430b730b6cedd1d8a084acd4984c5f292
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944143"
---
# <a name="sql-expressions"></a><span data-ttu-id="09c25-102">Expressões SQL</span><span class="sxs-lookup"><span data-stu-id="09c25-102">SQL expressions</span></span>


<span data-ttu-id="09c25-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="09c25-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="09c25-p101">Uma expressão SQL é uma sequência que compõe toda ou parte de uma instrução SQL. Por exemplo, o método **FindFirst** em um objeto **Recordset** usa uma expressão SQL que consiste nos critérios de seleção localizados em uma [cláusula WHERE](https://msdn.microsoft.com/library/ff195245\(v=office.15\)) do SQL.</span><span class="sxs-lookup"><span data-stu-id="09c25-p101">An SQL expression is a string that makes up all or part of an SQL statement. For example, the**FindFirst** method on a **Recordset** object uses an SQL expression consisting of the selection criteria found in an SQL [WHERE clause](https://msdn.microsoft.com/library/ff195245\(v=office.15\)).</span></span>

<span data-ttu-id="09c25-106">O mecanismo de banco de dados do Microsoft Access usa o serviço de expressões do Microsoft Visual Basic for Applications (ou VBA) para executar a avaliação de função e aritmética simple.</span><span class="sxs-lookup"><span data-stu-id="09c25-106">The Microsoft Access database engine uses the Microsoft Visual Basic for Applications (or VBA) expression service to perform simple arithmetic and function evaluation.</span></span> <span data-ttu-id="09c25-107">Todos os operadores usados nas expressões de SQL de mecanismo de banco de dados de Microsoft Access (exceto **[entre](https://msdn.microsoft.com/library/ff192436\(v=office.15\))**, **[no](https://msdn.microsoft.com/library/ff836369\(v=office.15\))** e **[como](https://msdn.microsoft.com/library/ff195752\(v=office.15\))**) são definidos pelo serviço de expressão VBA.</span><span class="sxs-lookup"><span data-stu-id="09c25-107">All of the operators used in Microsoft Access database engine SQL expressions (except **[Between](https://msdn.microsoft.com/library/ff192436\(v=office.15\))**, **[In](https://msdn.microsoft.com/library/ff836369\(v=office.15\))**, and **[Like](https://msdn.microsoft.com/library/ff195752\(v=office.15\))**) are defined by the VBA expression service.</span></span> <span data-ttu-id="09c25-108">Além disso, o serviço de expressões do VBA oferece mais de 100 funções VBA que podem ser utilizadas nas expressões SQL.</span><span class="sxs-lookup"><span data-stu-id="09c25-108">In addition, the VBA expression service offers over 100 VBA functions that you can use in SQL expressions.</span></span> <span data-ttu-id="09c25-109">Por exemplo, você pode usar essas funções VBA para compor uma consulta SQL no modo de Design da consulta do Microsoft Access, e você também pode usar essas funções em uma consulta SQL no método **OpenRecordset** do DAO no Microsoft Visual C++, Microsoft Visual Basic e Microsoft Código do Excel.</span><span class="sxs-lookup"><span data-stu-id="09c25-109">For example, you can use these VBA functions to compose an SQL query in the Microsoft Access query Design view, and you can also use these functions in an SQL query in the DAO **OpenRecordset** method in Microsoft Visual C++, Microsoft Visual Basic, and Microsoft Excel code.</span></span>

