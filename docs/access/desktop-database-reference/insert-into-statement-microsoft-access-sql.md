---
title: Instrução INSERT INTO (Microsoft Access SQL)
TOCTitle: INSERT INTO statement (Microsoft Access SQL)
ms:assetid: d3e44258-79f2-caba-8629-bde03f898f2d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834799(v=office.15)
ms:contentKeyID: 48547918
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277575
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 1635ff8ad43af45a62cd2223be853cefb5b6e999
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870797"
---
# <a name="insert-into-statement-microsoft-access-sql"></a><span data-ttu-id="a9103-102">Instrução INSERT INTO (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="a9103-102">INSERT INTO statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="a9103-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="a9103-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a9103-p101">Adiciona um registro ou vários registros a uma tabela. Isso é conhecido como uma consulta acréscimo.</span><span class="sxs-lookup"><span data-stu-id="a9103-p101">Adds a record or multiple records to a table. This is referred to as an append query.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9103-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a9103-106">Syntax</span></span>

<span data-ttu-id="a9103-107">**Consulta acréscimo de vários registros**:</span><span class="sxs-lookup"><span data-stu-id="a9103-107">**Multiple-record append query**:</span></span>

<span data-ttu-id="a9103-108">INSERT INTO *destino* \[(*field1*\[, *field2*\[,... \] \])\] \[Na *externaldatabase* \] selecione \[ *fonte*. \] *field1*\[, *field2*\[,... \] De *tableexpression*</span><span class="sxs-lookup"><span data-stu-id="a9103-108">INSERT INTO *target* \[(*field1*\[, *field2*\[, …\]\])\] \[IN *externaldatabase*\] SELECT \[*source*.\]*field1*\[, *field2*\[, …\] FROM *tableexpression*</span></span>

<span data-ttu-id="a9103-109">**Consulta acréscimo de registro único**:</span><span class="sxs-lookup"><span data-stu-id="a9103-109">**Single-record append query**:</span></span>

<span data-ttu-id="a9103-110">INSERT INTO *destino* \[(*field1*\[, *field2*\[,... \] \])\] Valores (*valor1*\[, *value2*\[,... \])</span><span class="sxs-lookup"><span data-stu-id="a9103-110">INSERT INTO *target* \[(*field1*\[, *field2*\[, …\]\])\] VALUES (*value1*\[, *value2*\[, …\])</span></span>

<span data-ttu-id="a9103-111">A instrução INSERT INTO inclui as seguintes partes:</span><span class="sxs-lookup"><span data-stu-id="a9103-111">The INSERT INTO statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a9103-112">Parte</span><span class="sxs-lookup"><span data-stu-id="a9103-112">Part</span></span></p></th>
<th><p><span data-ttu-id="a9103-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="a9103-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a9103-114"><em>destino</em></span><span class="sxs-lookup"><span data-stu-id="a9103-114"><em>target</em></span></span></p></td>
<td><p><span data-ttu-id="a9103-115">O nome da tabela ou da consulta à qual acrescentar registros.</span><span class="sxs-lookup"><span data-stu-id="a9103-115">The name of the table or query to append records to.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9103-116"><em>campo1</em>, <em>campo2</em></span><span class="sxs-lookup"><span data-stu-id="a9103-116"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="a9103-117">Nomes dos campos para acrescentar os dados, se forem seguintes a um argumento <em>target</em> , ou os nomes dos campos de dados serão obtidos, se forem seguintes a um argumento <em>source</em> .</span><span class="sxs-lookup"><span data-stu-id="a9103-117">Names of the fields to append data to, if following a <em>target</em> argument, or the names of fields to obtain data from, if following a <em>source</em> argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9103-118"><em>externaldatabase</em></span><span class="sxs-lookup"><span data-stu-id="a9103-118"><em>externaldatabase</em></span></span></p></td>
<td><p><span data-ttu-id="a9103-p102">O caminho para um banco de dados externo. Para obter a descrição do caminho, consulte a cláusula <a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-clause-microsoft-access-sql">IN</a>.  </span><span class="sxs-lookup"><span data-stu-id="a9103-p102">The path to an external database. For a description of the path, see the <a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-clause-microsoft-access-sql">IN</a> clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9103-121"><em>fonte</em></span><span class="sxs-lookup"><span data-stu-id="a9103-121"><em>source</em></span></span></p></td>
<td><p><span data-ttu-id="a9103-122">O nome da tabela ou da consulta da qual copiar registros.</span><span class="sxs-lookup"><span data-stu-id="a9103-122">The name of the table or query to copy records from.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9103-123"><em>tableexpression</em></span><span class="sxs-lookup"><span data-stu-id="a9103-123"><em>tableexpression</em></span></span></p></td>
<td><p><span data-ttu-id="a9103-p103">O nome da tabela ou tabelas a partir das quais os registros são inseridos. Esse argumento poderá ser um nome de tabela única ou um composto resultante de uma operação <a href="inner-join-operation-microsoft-access-sql.md">INNER JOIN</a>, <a href="left-join-right-join-operations-microsoft-access-sql.md">LEFT JOIN</a> ou <a href="left-join-right-join-operations-microsoft-access-sql.md">RIGHT JOIN</a>, ou de uma consulta salva.  </span><span class="sxs-lookup"><span data-stu-id="a9103-p103">The name of the table or tables from which records are inserted. This argument can be a single table name or a compound resulting from an <a href="inner-join-operation-microsoft-access-sql.md">INNER JOIN</a>, <a href="left-join-right-join-operations-microsoft-access-sql.md">LEFT JOIN</a>, or <a href="left-join-right-join-operations-microsoft-access-sql.md">RIGHT JOIN</a> operation or a saved query.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9103-126"><em>valor1</em>, <em>valor2</em></span><span class="sxs-lookup"><span data-stu-id="a9103-126"><em>value1</em>, <em>value2</em></span></span></p></td>
<td><p><span data-ttu-id="a9103-p104">Os valores para inserir em campos específicos do novo registro. Cada valor é inserido no campo correspondente à posição do valor na lista: o <em>valor1</em> é inserido no <em>campo1</em> do novo registro, o <em>valor2</em> no <em>campo2</em> e assim por diante. É necessário separar os valores com vírgula e delimitar os campos de texto entre aspas (" ").</span><span class="sxs-lookup"><span data-stu-id="a9103-p104">The values to insert into the specific fields of the new record. Each value is inserted into the field that corresponds to the value's position in the list: <em>value1</em> is inserted into <em>field1</em> of the new record, <em>value2</em> into <em>field2</em>, and so on. You must separate values with a comma, and enclose text fields in quotation marks (' ').</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="a9103-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="a9103-130">Remarks</span></span>

<span data-ttu-id="a9103-p105">Você poderá utilizar a instrução INSERT INTO para adicionar registros únicos em uma tabela, usando a sintaxe da consulta acréscimo de registro único, como descrito acima. Nesse caso, seu código vai especificar o nome e o valor para cada campo do registro. Você deverá especificar os campos do registro aos quais vai atribuir um valor e especificar um valor para cada campo. Se você não especificar os campos, o valor padrão ou **Nulo** será inserido nas colunas ausentes. Os registros serão adicionados ao final da tabela.</span><span class="sxs-lookup"><span data-stu-id="a9103-p105">You can use the INSERT INTO statement to add a single record to a table using the single-record append query syntax as shown above. In this case, your code specifies the name and value for each field of the record. You must specify each of the fields of the record that a value is to be assigned to and a value for that field. When you do not specify each field, the default value or **Null** is inserted for missing columns. Records are added to the end of the table.</span></span>

<span data-ttu-id="a9103-136">Você também pode usar INSERT INTO para acrescentar um conjunto de registros de outra tabela ou consulta usando SELECT …</span><span class="sxs-lookup"><span data-stu-id="a9103-136">You can also use INSERT INTO to append a set of records from another table or query by using the SELECT …</span></span> <span data-ttu-id="a9103-137">FROM, como mostrado acima na sintaxe da consulta acréscimo de vários registros.</span><span class="sxs-lookup"><span data-stu-id="a9103-137">FROM clause as shown above in the multiple-record append query syntax.</span></span> <span data-ttu-id="a9103-138">Nesse caso, a cláusula SELECT especifica os campos para acrescentar à tabela especificada *destino* .</span><span class="sxs-lookup"><span data-stu-id="a9103-138">In this case, the SELECT clause specifies the fields to append to the specified *target* table.</span></span>

<span data-ttu-id="a9103-139">A tabela de *origem* ou *destino* pode especificar uma tabela ou consulta.</span><span class="sxs-lookup"><span data-stu-id="a9103-139">The *source* or *target* table may specify a table or a query.</span></span> <span data-ttu-id="a9103-140">Se uma consulta for especificada, o mecanismo do banco de dados do Microsoft Access acrescentará registros a todas as tabelas especificadas pela consulta.</span><span class="sxs-lookup"><span data-stu-id="a9103-140">If a query is specified, the Microsoft Access database engine appends records to any and all tables specified by the query.</span></span>

<span data-ttu-id="a9103-141">A instrução INSERT INTO é opcional, mas se for incluída, prevalecerá sobre a [SELECT](select-statement-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="a9103-141">INSERT INTO is optional but when included, precedes the [SELECT](select-statement-microsoft-access-sql.md) statement.</span></span>

<span data-ttu-id="a9103-142">Se sua tabela de destino incluir uma chave primária, acrescente somente valores não **Nulos** ao campo ou campos dessa chave; caso não o faça, o mecanismo do banco de dados do Microsoft Access não acrescentará os registros.</span><span class="sxs-lookup"><span data-stu-id="a9103-142">If your destination table contains a primary key, make sure you append unique, non-**Null** values to the primary key field or fields; if you do not, the Microsoft Access database engine will not append the records.</span></span>

<span data-ttu-id="a9103-p108">Se acrescentar registros a uma tabela com o campo Numeração Automática e desejar renumerá-los, não inclua esse campo à consulta. Inclua o campo Numeração Automática na consulta somente se desejar manter os valores originais desse campo.</span><span class="sxs-lookup"><span data-stu-id="a9103-p108">If you append records to a table with an AutoNumber field and you want to renumber the appended records, do not include the AutoNumber field in your query. Do include the AutoNumber field in the query if you want to retain the original values from the field.</span></span>

<span data-ttu-id="a9103-145">Use a cláusula IN para acrescentar registros a uma tabela em outro banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a9103-145">Use the IN clause to append records to a table in another database.</span></span>

<span data-ttu-id="a9103-146">Para criar uma nova tabela, use as instruções [SELECT… INTO](select-into-statement-microsoft-access-sql.md), em vez de criar uma consulta Criar Tabela.</span><span class="sxs-lookup"><span data-stu-id="a9103-146">To create a new table, use the [SELECT… INTO](select-into-statement-microsoft-access-sql.md) statement instead to create a make-table query.</span></span>

<span data-ttu-id="a9103-147">Para descobrir quais registros serão acrescentados antes de executar a consulta acréscimo, em primeiro lugar, execute e verifique os resultados de uma consulta seleção, que utiliza os mesmos critérios de seleção.</span><span class="sxs-lookup"><span data-stu-id="a9103-147">To find out which records will be appended before you run the append query, first execute and view the results of a select query that uses the same selection criteria.</span></span>

<span data-ttu-id="a9103-p109">Uma consulta acréscimo copia os registros de uma ou de mais tabelas para outra. As tabelas que englobarem os registros que você anexar não serão afetadas pela consulta acréscimo.</span><span class="sxs-lookup"><span data-stu-id="a9103-p109">An append query copies records from one or more tables to another. The tables that contain the records you append are not affected by the append query.</span></span>

<span data-ttu-id="a9103-p110">Em vez de acrescentar registros existentes de outra tabela, é possível especificar o valor de cada campo em um novo registro único, usando a cláusula VALUES. Se omitir a lista de campos, a cláusula VALUES deverá incluir um valor para cada campo na tabela; caso contrário, a operação INSERT vai falhar. Utilize uma instrução INSERT INTO extra com uma cláusula VALUES para cada registro adicional que desejar criar.</span><span class="sxs-lookup"><span data-stu-id="a9103-p110">Instead of appending existing records from another table, you can specify the value for each field in a single new record using the VALUES clause. If you omit the field list, the VALUES clause must include a value for every field in the table; otherwise, the INSERT operation will fail. Use an additional INSERT INTO statement with a VALUES clause for each additional record you want to create.</span></span>

<span data-ttu-id="a9103-153">**Os links fornecidos pela** comunidade [UtterAccess](https://www.utteraccess.com) .</span><span class="sxs-lookup"><span data-stu-id="a9103-153">**Links provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="a9103-154">UtterAccess é o fórum principal de wiki e a Ajuda do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="a9103-154">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="a9103-155">Como gerar números sequenciais para as instruções INSERT/UPDATE</span><span class="sxs-lookup"><span data-stu-id="a9103-155">Generating sequential numbers for INSERT/UPDATE statements</span></span>](https://www.utteraccess.com/forum/generating-sequential-num-t446039.html)

- [<span data-ttu-id="a9103-156">SQL para Formatador VBA</span><span class="sxs-lookup"><span data-stu-id="a9103-156">SQL to VBA Formatter</span></span>](https://www.utteraccess.com/forum/sql-vba-formatter-t1165308.html)

## <a name="example"></a><span data-ttu-id="a9103-157">Exemplo</span><span class="sxs-lookup"><span data-stu-id="a9103-157">Example</span></span>

<span data-ttu-id="a9103-p112">Este exemplo seleciona todos os registros em uma tabela hipotética Novos Clientes e os adiciona à tabela Clientes. Se as colunas individuais não forem determinadas, os nomes das colunas da tabela SELECT devem corresponder exatamente àqueles na tabela INSERT INTO.</span><span class="sxs-lookup"><span data-stu-id="a9103-p112">This example selects all records in a hypothetical New Customers table and adds them to the Customers table. When individual columns are not designated, the SELECT table column names must match exactly those in the INSERT INTO table.</span></span>

```vb
    Sub InsertIntoX1() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Select all records in the New Customers table  
        ' and add them to the Customers table. 
        dbs.Execute " INSERT INTO Customers " _ 
            & "SELECT * " _ 
            & "FROM [New Customers];" 
             
        dbs.Close 
     
    End Sub
```

<br/>

<span data-ttu-id="a9103-160">Esse exemplo cria um novo registro na tabela Funcionários.</span><span class="sxs-lookup"><span data-stu-id="a9103-160">This example creates a new record in the Employees table.</span></span>

```vb
    Sub InsertIntoX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Create a new record in the Employees table. The  
        ' first name is Harry, the last name is Washington,  
        ' and the job title is Trainee. 
        dbs.Execute " INSERT INTO Employees " _ 
            & "(FirstName,LastName, Title) VALUES " _ 
            & "('Harry', 'Washington', 'Trainee');" 
             
        dbs.Close 
     
    End Sub 
```

