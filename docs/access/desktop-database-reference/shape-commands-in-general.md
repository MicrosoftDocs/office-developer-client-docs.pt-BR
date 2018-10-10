---
title: Comandos shape em geral
TOCTitle: Shape Commands in General
ms:assetid: ad555aa7-bc64-b495-a98d-e927061a5809
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249814(v=office.15)
ms:contentKeyID: 48547039
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 33570bec65de4ff88667ad90b591c4f288c86d96
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463824"
---
# <a name="shape-commands-in-general"></a><span data-ttu-id="750e8-102">Comandos shape em geral</span><span class="sxs-lookup"><span data-stu-id="750e8-102">Shape Commands in General</span></span>


<span data-ttu-id="750e8-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="750e8-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="750e8-104">O data shaping define as colunas de um **Recordset** com formato, as relações entre as entidades representadas pelas colunas e o modo de preenchimento de **Recordset** com dados.</span><span class="sxs-lookup"><span data-stu-id="750e8-104">Data shaping defines the columns of a shaped **Recordset**, the relationships between the entities represented by the columns, and the manner in which the **Recordset** is populated with data.</span></span>

<span data-ttu-id="750e8-105">Um **Recordset** com formato pode consistir nos seguintes tipos de colunas.</span><span class="sxs-lookup"><span data-stu-id="750e8-105">A shaped **Recordset** may consist of the following types of columns.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="750e8-106">Tipo de coluna</span><span class="sxs-lookup"><span data-stu-id="750e8-106">Column type</span></span></p></th>
<th><p><span data-ttu-id="750e8-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="750e8-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="750e8-108">data</span><span class="sxs-lookup"><span data-stu-id="750e8-108">data</span></span></p></td>
<td><p><span data-ttu-id="750e8-109">Campos de um <strong>Recordset</strong> retornados por um comando de consulta para um provedor de dados, uma tabela ou um <strong>Recordset</strong> com formato anterior.</span><span class="sxs-lookup"><span data-stu-id="750e8-109">Fields from a <strong>Recordset</strong> returned by a query command to a data provider, table, or previously shaped <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="750e8-110">chapter</span><span class="sxs-lookup"><span data-stu-id="750e8-110">chapter</span></span></p></td>
<td><p><span data-ttu-id="750e8-p101">Uma referência a outro <strong>Recordset</strong>, denominado <em>capítulo</em>. As colunas de capítulo permitem definir uma relação <em>parent-child</em> em que <em>parent</em> representa o <strong>Recordset</strong> contendo a coluna de capítulo, e <em>child</em> é o <strong>Recordset</strong> representado pelo capítulo.</span><span class="sxs-lookup"><span data-stu-id="750e8-p101">A reference to another <strong>Recordset</strong>, called a <em>chapter</em>. Chapter columns make it possible to define a <em>parent-child</em> relationship where the <em>parent</em> is the <strong>Recordset</strong> containing the chapter column and the <em>child</em> is the <strong>Recordset</strong> represented by the chapter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="750e8-113">aggregate</span><span class="sxs-lookup"><span data-stu-id="750e8-113">aggregate</span></span></p></td>
<td><p><span data-ttu-id="750e8-p102">O valor da coluna é derivado executando uma <em>função de agregação</em> em todas as linhas ou em uma coluna de todas as linhas de um <strong>Recordset</strong> filho. (Consulte Funções agregadas no tópico <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Funções agregadas, a função CALC e a palavra-chave NEW</a>.)</span><span class="sxs-lookup"><span data-stu-id="750e8-p102">The value of the column is derived by executing an <em>aggregate function</em> on all the rows or a column of all the rows of a child <strong>Recordset</strong>. (See Aggregate Functions in the following topic, <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Aggregate Functions, the CALC Function, and the NEW Keyword</a>.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="750e8-116">calculated expression</span><span class="sxs-lookup"><span data-stu-id="750e8-116">calculated expression</span></span></p></td>
<td><p><span data-ttu-id="750e8-p103">O valor da coluna é derivado do cálculo de uma expressão do Visual Basic for Application nas colunas na mesma linha do <strong>Recordset</strong>. A expressão é o argumento para a função CALC. (Consulte Expressão calculada no tópico <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Funções agregadas, a função CALC e a palavra-chave NEW</a> e em <a href="visual-basic-for-applications-functions.md">Funções do Visual Basic for Applications</a>.)</span><span class="sxs-lookup"><span data-stu-id="750e8-p103">The value of the column is derived by calculating a Visual Basic for Applications expression on columns in the same row of the <strong>Recordset</strong>. The expression is the argument to the CALC function. (See Calculated Expression in the following topic, <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Aggregate Functions, the CALC Function, and the NEW Keyword</a> and in <a href="visual-basic-for-applications-functions.md">Visual Basic for Applications Functions</a>.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="750e8-120">new</span><span class="sxs-lookup"><span data-stu-id="750e8-120">new</span></span></p></td>
<td><p><span data-ttu-id="750e8-p104">Campos fabricados vazios, que podem ser preenchidos posteriormente com dados. A coluna é definida com a palavra-chave NEW. (Consulte Palavra-chave NEW no tópico <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Funções agregadas, a função CALC e a palavra-chave NEW</a>.)</span><span class="sxs-lookup"><span data-stu-id="750e8-p104">Empty, fabricated fields, which may be populated with data at a later time. The column is defined with the NEW keyword. (See NEW keyword in the following topic, <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Aggregate Functions, the CALC Function, and the NEW Keyword</a>.)</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="750e8-p105">Um comando shape pode conter uma cláusula especificando um comando de consulta para um provedor de dados subjacente que retornará um objeto **Recordset**. A sintaxe da consulta depende dos requisitos desse provedor. Em geral, será usada a linguagem SQL, embora o ADO não exija nenhuma linguagem de consulta específica.</span><span class="sxs-lookup"><span data-stu-id="750e8-p105">A shape command may contain a clause specifying a query command to an underlying data provider that will return a **Recordset** object. The query's syntax depends on the requirements of the underlying data provider. This will usually be Structured Query Language (SQL), although ADO does not require the use of any particular query language.</span></span>

<span data-ttu-id="750e8-p106">É possível usar uma cláusula SQL JOIN para relacionar duas tabelas; entretanto, um **Recordset** hierárquico pode representar as informações com mais eficiência. Cada linha de um **Recordset** criada por um JOIN repete as informações de uma das tabelas de forma redundante. Um **Recordset** hierárquico possui apenas um **Recordset** pai para cada um dos diversos objetos **Recordset** filho.</span><span class="sxs-lookup"><span data-stu-id="750e8-p106">You could use a SQL JOIN clause to relate two tables; however, a hierarchical **Recordset** may represent the information more efficiently. Each row of a **Recordset** created by a JOIN repeats information redundantly from one of the tables. A hierarchical **Recordset** has only one parent **Recordset** for each of multiple child **Recordset** objects.</span></span>

<span data-ttu-id="750e8-130">Os comandos shape podem ser emitidos por objetos **Recordset** ou definindo a propriedade [CommandText](commandtext-property-ado.md) do objeto [Command](command-object-ado.md) e, em seguida, chamando o método [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="750e8-130">Shape commands can be issued by **Recordset** objects or by setting the [CommandText](commandtext-property-ado.md) property of the [Command](command-object-ado.md) object and then calling the [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) method.</span></span>

<span data-ttu-id="750e8-131">Comandos Shape podem ser aninhados.</span><span class="sxs-lookup"><span data-stu-id="750e8-131">Shape commands can be nested.</span></span> <span data-ttu-id="750e8-132">Ou seja, o *parent-command* *filho-command* próprio poderá ou um outro comando shape.</span><span class="sxs-lookup"><span data-stu-id="750e8-132">That is, the *parent-command* or *child-command* may itself be another shape command.</span></span>

<span data-ttu-id="750e8-133">O provedor de forma sempre retorna um cursor do cliente, mesmo quando o usuário especifica o local de cursor **adUseServer**.</span><span class="sxs-lookup"><span data-stu-id="750e8-133">The shape provider always returns a client cursor, even when the user specifies a cursor location of **adUseServer**.</span></span>

<span data-ttu-id="750e8-134">Para obter informações sobre como navegar em um **Recordset** hierárquico, consulte [Acessando linhas em um conjunto de registros hierárquico](accessing-rows-in-a-hierarchical-recordset.md).</span><span class="sxs-lookup"><span data-stu-id="750e8-134">For information about navigating a hierarchical **Recordset**, see [Accessing Rows in a Hierarchical Recordset](accessing-rows-in-a-hierarchical-recordset.md).</span></span>

<span data-ttu-id="750e8-135">Para obter informações precisas sobre comandos shape sintaticamente corretos, consulte [Gramática formal de shape](formal-shape-grammar.md).</span><span class="sxs-lookup"><span data-stu-id="750e8-135">For precise information about syntactically correct shape commands, see [Formal Shape Grammar](formal-shape-grammar.md).</span></span>

