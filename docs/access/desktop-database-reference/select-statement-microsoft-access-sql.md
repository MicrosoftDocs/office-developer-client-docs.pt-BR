---
title: Declaração SELECT (SQL do Microsoft Access)
TOCTitle: SELECT Statement (Microsoft Access SQL)
ms:assetid: a5c9da94-5f9e-0fc0-767a-4117f38a5ef3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821148(v=office.15)
ms:contentKeyID: 48546837
ms.date: 09/18/2015
mtps_version: v=office.15
dev_langs:
- sql
ms.openlocfilehash: ae7a63a3fe7647dde117db80a52e2322b9af75b9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462669"
---
# <a name="select-statement-microsoft-access-sql"></a><span data-ttu-id="5260c-102">Declaração SELECT (SQL do Microsoft Access)</span><span class="sxs-lookup"><span data-stu-id="5260c-102">SELECT Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="5260c-103">**Aplica-se a:** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5260c-103">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="5260c-104">Instrui o mecanismo de banco de dados do Microsoft Access a retornar informações do banco de dados como um conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="5260c-104">Instructs the Microsoft Access database engine to return information from the database as a set of records.</span></span>

## <a name="syntax"></a><span data-ttu-id="5260c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5260c-105">Syntax</span></span>

<span data-ttu-id="5260c-106">Selecione \[ *predicado* \] { \*  |  *tabela*.\*  |  \[ *tabela*. \] *field1* \[como *alias1* \] \[, \[ *tabela*. \] *field2* \[como *alias2* \] \[,... \] \]} De *tableexpression* \[,... \] \[Na *externaldatabase* \] \[onde …</span><span class="sxs-lookup"><span data-stu-id="5260c-106">SELECT \[*predicate*\] { \* | *table*.\* | \[*table*.\]*field1* \[AS *alias1*\] \[, \[*table*.\]*field2* \[AS *alias2*\] \[, …\]\]} FROM *tableexpression* \[, …\] \[IN *externaldatabase*\] \[WHERE…</span></span> <span data-ttu-id="5260c-107">\]\[Agrupar por …</span><span class="sxs-lookup"><span data-stu-id="5260c-107">\] \[GROUP BY…</span></span> <span data-ttu-id="5260c-108">\]\[HAVING …</span><span class="sxs-lookup"><span data-stu-id="5260c-108">\] \[HAVING…</span></span> <span data-ttu-id="5260c-109">\]\[ORDER BY …</span><span class="sxs-lookup"><span data-stu-id="5260c-109">\] \[ORDER BY…</span></span> <span data-ttu-id="5260c-110">\]\[Com OWNERACCESS OPTION\]</span><span class="sxs-lookup"><span data-stu-id="5260c-110">\] \[WITH OWNERACCESS OPTION\]</span></span>

<span data-ttu-id="5260c-111">A declaração SELECT tem as seguintes partes:</span><span class="sxs-lookup"><span data-stu-id="5260c-111">The SELECT statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5260c-112">Parte</span><span class="sxs-lookup"><span data-stu-id="5260c-112">Part</span></span></p></th>
<th><p><span data-ttu-id="5260c-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="5260c-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5260c-114"><em>predicate</em></span><span class="sxs-lookup"><span data-stu-id="5260c-114"><em>predicate</em></span></span></p></td>
<td><p><span data-ttu-id="5260c-p102">Um dos seguintes predicados: <a href="https://msdn.microsoft.com/library/ff195711(v=office.15)">ALL, DISTINCT, DISTINCTROW ou TOP</a>. O predicado é usado para restringir o número de registros retornados. Se nenhum for especificado, o padrão é ALL.  </span><span class="sxs-lookup"><span data-stu-id="5260c-p102">One of the following predicates: <a href="https://msdn.microsoft.com/library/ff195711(v=office.15)">ALL, DISTINCT, DISTINCTROW, or TOP</a>. You use the predicate to restrict the number of records returned. If none is specified, the default is ALL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><em>*</em></p></td>
<td><p><span data-ttu-id="5260c-118">Especifica que todos os campos da tabela ou tabelas especificadas serão selecionados.</span><span class="sxs-lookup"><span data-stu-id="5260c-118">Specifies that all fields from the specified table or tables are selected.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5260c-119"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="5260c-119"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="5260c-120">O nome da tabela contendo os campos a partir dos quais os registros serão selecionados.</span><span class="sxs-lookup"><span data-stu-id="5260c-120">The name of the table containing the fields from which records are selected.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5260c-121"><em>field1</em>, <em>field2</em></span><span class="sxs-lookup"><span data-stu-id="5260c-121"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="5260c-p103">Os nomes dos campos contendo os dados que você deseja recuperar. Se você incluir mais do que um campo, eles serão recuperados na ordem listada.</span><span class="sxs-lookup"><span data-stu-id="5260c-p103">The names of the fields containing the data you want to retrieve. If you include more than one field, they are retrieved in the order listed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5260c-124"><em>alias1</em>, <em>alias2</em></span><span class="sxs-lookup"><span data-stu-id="5260c-124"><em>alias1</em>, <em>alias2</em></span></span></p></td>
<td><p><span data-ttu-id="5260c-125">Os nomes que serão usados como títulos de coluna em vez dos nomes de coluna originais em <em>table</em>.</span><span class="sxs-lookup"><span data-stu-id="5260c-125">The names to use as column headers instead of the original column names in <em>table</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5260c-126"><em>tableexpression</em></span><span class="sxs-lookup"><span data-stu-id="5260c-126"><em>tableexpression</em></span></span></p></td>
<td><p><span data-ttu-id="5260c-127">O nome da tabela ou tabelas contendo os dados que você deseja recuperar.</span><span class="sxs-lookup"><span data-stu-id="5260c-127">The name of the table or tables containing the data you want to retrieve.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5260c-128"><em>externaldatabase</em></span><span class="sxs-lookup"><span data-stu-id="5260c-128"><em>externaldatabase</em></span></span></p></td>
<td><p><span data-ttu-id="5260c-129">O nome do banco de dados que contém as tabelas em <em>tableexpression</em> se elas não estiverem no banco de dados atual.</span><span class="sxs-lookup"><span data-stu-id="5260c-129">The name of the database containing the tables in <em>tableexpression</em> if they are not in the current database.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="5260c-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="5260c-130">Remarks</span></span>

<span data-ttu-id="5260c-131">Para executar esta operação, o mecanismo do banco de dados do Microsoft® Jet pesquisa na tabela ou tabelas especificadas, extrai as colunas escolhidas, seleciona linhas que correspondam ao critério e classifica ou agrupa as linhas resultantes na ordem especificada.</span><span class="sxs-lookup"><span data-stu-id="5260c-131">To perform this operation, the Microsoft® Jet database engine searches the specified table or tables, extracts the chosen columns, selects rows that meet the criterion, and sorts or groups the resulting rows into the order specified.</span></span>

<span data-ttu-id="5260c-132">Declarações SELECT não alteram os dados no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="5260c-132">SELECT statements do not change data in the database.</span></span>

<span data-ttu-id="5260c-p104">SELECT é normalmente a primeira palavra em uma declaração SQL. A maior parte das declarações SQL são declarações SELECT ou [SELECT…INTO](select-into-statement-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="5260c-p104">SELECT is usually the first word in an SQL statement. Most SQL statements are either SELECT or [SELECT…INTO](select-into-statement-microsoft-access-sql.md) statements.</span></span>

<span data-ttu-id="5260c-135">A sintaxe mínima para uma declaração SELECT é:</span><span class="sxs-lookup"><span data-stu-id="5260c-135">The minimum syntax for a SELECT statement is:</span></span>

<span data-ttu-id="5260c-136">Selecione os *campos* de *tabela*</span><span class="sxs-lookup"><span data-stu-id="5260c-136">SELECT *fields* FROM *table*</span></span>

<span data-ttu-id="5260c-p105">Você pode usar um asterisco (\*) para selecionar todos os campos em uma tabela. O exemplo a seguir seleciona todos os campos na tabela de Funcionários:</span><span class="sxs-lookup"><span data-stu-id="5260c-p105">You can use an asterisk (\*) to select all fields in a table. The following example selects all of the fields in the Employees table:</span></span>

```sql
SELECT * FROM Employees;
```

<span data-ttu-id="5260c-p106">Se um nome de campo estiver incluído em mais do que uma tabela na cláusula FROM, preceda-o com o nome da tabela e o operador **.** (ponto). No exemplo a seguir, o campo Departamento está presente na tabela de Funcionários e na tabela de Supervisores. A declaração SQL seleciona departamentos a partir da tabela de Funcionários e os nomes de supervisores da tabela de Supervisores:</span><span class="sxs-lookup"><span data-stu-id="5260c-p106">If a field name is included in more than one table in the FROM clause, precede it with the table name and the **.** (dot) operator. In the following example, the Department field is in both the Employees table and the Supervisors table. The SQL statement selects departments from the Employees table and supervisor names from the Supervisors table:</span></span>

```sql
SELECT Employees.Department, Supervisors.SupvName 
FROM Employees INNER JOIN Supervisors 
WHERE Employees.Department = Supervisors.Department;
```

<span data-ttu-id="5260c-p107">Quando um objeto **Recordset** é criado, o mecanismo do banco de dados do Microsoft Jet usa o nome de campo da tabela como o nome do objeto **Field** no objeto **Recordset**. Se você desejar um nome de campo diferente ou um nome que não esteja implícito na expressão usada para gerar o campo, use a palavra reservada AS. O exemplo a seguir usa o título Data de Nascimento para nomear o objeto **Field** retornado no objeto **Recordset** resultante:</span><span class="sxs-lookup"><span data-stu-id="5260c-p107">When a **Recordset** object is created, the Microsoft Jet database engine uses the table's field name as the **Field** object name in the **Recordset** object. If you want a different field name or a name is not implied by the expression used to generate the field, use the AS reserved word. The following example uses the title Birth to name the returned **Field** object in the resulting **Recordset** object:</span></span>

```sql
SELECT BirthDate 
AS Birth FROM Employees;
```

<span data-ttu-id="5260c-p108">Sempre que você usar funções agregadas ou consultas que retornem nomes de objeto **Field** ambíguos ou duplicados, deverá usar a cláusula AS para fornecer um nome alternativo para o objeto **Field**. O exemplo a seguir usa o título HeadCount para nomear o objeto **Field** retornado no objeto **Recordset** resultante:</span><span class="sxs-lookup"><span data-stu-id="5260c-p108">Whenever you use aggregate functions or queries that return ambiguous or duplicate **Field** object names, you must use the AS clause to provide an alternate name for the **Field** object. The following example uses the title HeadCount to name the returned **Field** object in the resulting **Recordset** object:</span></span>

```sql
SELECT COUNT(EmployeeID)
AS HeadCount FROM Employees;
```

<span data-ttu-id="5260c-p109">Você pode usar as outras cláusulas em uma declaração SELECT para restringir e organizar melhor os seus dados retornados. Para saber mais, consulte o tópico de Ajuda para a cláusula que você está usando.</span><span class="sxs-lookup"><span data-stu-id="5260c-p109">You can use the other clauses in a SELECT statement to further restrict and organize your returned data. For more information, see the Help topic for the clause you are using.</span></span>

<span data-ttu-id="5260c-150">**Os links fornecidos pela** comunidade [UtterAccess](https://www.utteraccess.com) .</span><span class="sxs-lookup"><span data-stu-id="5260c-150">**Links provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="5260c-151">UtterAccess é o fórum principal de wiki e a Ajuda do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="5260c-151">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="5260c-152">SQL to VBA Formatter</span><span class="sxs-lookup"><span data-stu-id="5260c-152">SQL to VBA Formatter</span></span>](https://www.utteraccess.com/forum/sql-vba-formatter-t1165308.html)

- [<span data-ttu-id="5260c-153">Exibir Registros com um Intervalo Definido</span><span class="sxs-lookup"><span data-stu-id="5260c-153">Viewing Records Within A Defined Range</span></span>](https://www.utteraccess.com/wiki/index.php/records_within_a_defined_range)

## <a name="example"></a><span data-ttu-id="5260c-154">Exemplo</span><span class="sxs-lookup"><span data-stu-id="5260c-154">Example</span></span>

<span data-ttu-id="5260c-p111">Alguns dos exemplos a seguir assumem a existência de um campo hipotético chamado Salário em uma tabela de Funcionários. Repare que esse campo não existe realmente na tabela de Funcionários do banco de dados da Northwind.</span><span class="sxs-lookup"><span data-stu-id="5260c-p111">Some of the following examples assume the existence of a hypothetical Salary field in an Employees table. Note that this field does not actually exist in the Northwind database Employees table.</span></span>

<span data-ttu-id="5260c-p112">Este exemplo cria um **Recordset** do tipo dynaset com base em uma declaração SQL que seleciona os campos LastName e FirstName de todos os registros da tabela de Funcionários. Ele chama o procedimento EnumFields, que imprime os conteúdos de um objeto **Recordset** na janela **Depurar**.</span><span class="sxs-lookup"><span data-stu-id="5260c-p112">This example creates a dynaset-type **Recordset** based on an SQL statement that selects the LastName and FirstName fields of all records in the Employees table. It calls the EnumFields procedure, which prints the contents of a **Recordset** object to the **Debug** window.</span></span>

```sql
    Sub SelectX1() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Select the last name and first name values of all  
        ' records in the Employees table. 
        Set rst = dbs.OpenRecordset("SELECT LastName, " _ 
            & "FirstName FROM Employees;") 
     
        ' Populate the recordset. 
        rst.MoveLast 
     
        ' Call EnumFields to print the contents of the 
        ' Recordset. 
        EnumFields rst,12 
     
        dbs.Close 
     
    End Sub
```

<span data-ttu-id="5260c-159">Este exemplo conta o número de registros que têm uma entrada no campo PostalCode e nomeia o campo retornado como Registro.</span><span class="sxs-lookup"><span data-stu-id="5260c-159">This example counts the number of records that have an entry in the PostalCode field and names the returned field Tally.</span></span>

```sql
    Sub SelectX2() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Count the number of records with a PostalCode  
        ' value and return the total in the Tally field. 
        Set rst = dbs.OpenRecordset("SELECT Count " _ 
            & "(PostalCode) AS Tally FROM Customers;") 
     
        ' Populate the Recordset. 
        rst.MoveLast 
     
        ' Call EnumFields to print the contents of  
        ' the Recordset. Specify field width = 12. 
        EnumFields rst, 12 
     
        dbs.Close 
     
    End Sub 
```

<span data-ttu-id="5260c-160">Este exemplo mostra o número de funcionários e os salários médio e máximo.</span><span class="sxs-lookup"><span data-stu-id="5260c-160">This example shows the number of employees and the average and maximum salaries.</span></span>

```sql
    Sub SelectX3() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Count the number of employees, calculate the  
        ' average salary, and return the highest salary. 
        Set rst = dbs.OpenRecordset("SELECT Count (*) " _ 
            & "AS TotalEmployees, Avg(Salary) " _ 
            & "AS AverageSalary, Max(Salary) " _ 
            & "AS MaximumSalary FROM Employees;") 
     
        ' Populate the Recordset. 
        rst.MoveLast 
     
        ' Call EnumFields to print the contents of 
        ' the Recordset. Pass the Recordset object and 
        ' desired field width. 
        EnumFields rst, 17 
     
        dbs.Close 
     
    End Sub 
```

<span data-ttu-id="5260c-p113">O procedimento **Sub** EnumFields recebe um objeto **Recordset** do procedimento de chamada. Em seguida, o procedimento formata e imprime os campos do **Recordset** na janela **Depurar**. A variável é o comprimento desejado do campo impresso. Alguns campos podem ser truncados.</span><span class="sxs-lookup"><span data-stu-id="5260c-p113">The **Sub** procedure EnumFields is passed a **Recordset** object from the calling procedure. The procedure then formats and prints the fields of the **Recordset** to the **Debug** window. The variable is the desired printed field width. Some fields may be truncated.</span></span>

```sql
    Sub EnumFields(rst As Recordset, intFldLen As Integer) 
     
        Dim lngRecords As Long, lngFields As Long 
        Dim lngRecCount As Long, lngFldCount As Long 
        Dim strTitle As String, strTemp As String 
     
        ' Set the lngRecords variable to the number of 
        ' records in the Recordset. 
        lngRecords = rst.RecordCount 
     
        ' Set the lngFields variable to the number of 
        ' fields in the Recordset. 
        lngFields = rst.Fields.Count 
     
        Debug.Print "There are " & lngRecords _ 
            & " records containing " & lngFields _ 
            & " fields in the recordset." 
        Debug.Print 
     
        ' Form a string to print the column heading. 
        strTitle = "Record  " 
        For lngFldCount = 0 To lngFields - 1 
            strTitle = strTitle _ 
            & Left(rst.Fields(lngFldCount).Name _ 
            & Space(intFldLen), intFldLen) 
        Next lngFldCount     
     
        ' Print the column heading. 
        Debug.Print strTitle 
        Debug.Print 
     
        ' Loop through the Recordset; print the record 
        ' number and field values. 
        rst.MoveFirst 
     
        For lngRecCount = 0 To lngRecords - 1 
            Debug.Print Right(Space(6) & _ 
                Str(lngRecCount), 6) & "  "; 
     
            For lngFldCount = 0 To lngFields - 1 
                ' Check for Null values. 
                If IsNull(rst.Fields(lngFldCount)) Then 
                    strTemp = "<null>" 
                Else 
                    ' Set strTemp to the field contents.  
                    Select Case _ 
                        rst.Fields(lngFldCount).Type 
                        Case 11 
                            strTemp = "" 
                        Case dbText, dbMemo 
                            strTemp = _ 
                                rst.Fields(lngFldCount) 
                        Case Else 
                            strTemp = _ 
                                str(rst.Fields(lngFldCount)) 
                    End Select 
                End If 
     
                Debug.Print Left(strTemp _  
                    & Space(intFldLen), intFldLen); 
            Next lngFldCount 
     
            Debug.Print 
     
            rst.MoveNext 
     
        Next lngRecCount 
     
    End Sub 
```




