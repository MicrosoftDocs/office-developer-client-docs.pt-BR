---
title: Instrução SELECT (Microsoft Access SQL)
TOCTitle: SELECT statement (Microsoft Access SQL)
ms:assetid: a5c9da94-5f9e-0fc0-767a-4117f38a5ef3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821148(v=office.15)
ms:contentKeyID: 48546837
ms.date: 10/18/2018
mtps_version: v=office.15
dev_langs:
- sql
ms.openlocfilehash: 2b03834914c352a0e9c462c50bee48ac992276e3
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860578"
---
# <a name="select-statement-microsoft-access-sql"></a>Instrução SELECT (Microsoft Access SQL)

**Aplica-se a:** Access 2013 | Office 2013

Instrui o mecanismo de banco de dados do Microsoft Access a retornar informações do banco de dados como um conjunto de registros.

## <a name="syntax"></a>Sintaxe

Selecione \[ *predicado* \] { \*  |  *tabela*.\*  |  \[ *tabela*. \] *field1* \[como *alias1* \] \[, \[ *tabela*. \] *field2* \[como *alias2* \] \[,... \] \]} De *tableexpression* \[,... \] \[Na *externaldatabase* \] \[onde … \]\[Agrupar por … \]\[HAVING … \]\[ORDER BY … \]\[Com OWNERACCESS OPTION\]

A declaração SELECT tem as seguintes partes:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Parte</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>predicate</em></p></td>
<td><p>Um dos seguintes predicados: <a href="https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql">ALL, DISTINCT, DISTINCTROW ou TOP</a>. O predicado é usado para restringir o número de registros retornados. Se nenhum for especificado, o padrão é ALL.  </p></td>
</tr>
<tr class="even">
<td><p><em>*</em></p></td>
<td><p>Especifica que todos os campos da tabela ou tabelas especificadas serão selecionados.</p></td>
</tr>
<tr class="odd">
<td><p><em>table</em></p></td>
<td><p>O nome da tabela contendo os campos a partir dos quais os registros serão selecionados.</p></td>
</tr>
<tr class="even">
<td><p><em>field1</em>, <em>field2</em></p></td>
<td><p>Os nomes dos campos contendo os dados que você deseja recuperar. Se você incluir mais do que um campo, eles serão recuperados na ordem listada.</p></td>
</tr>
<tr class="odd">
<td><p><em>alias1</em>, <em>alias2</em></p></td>
<td><p>Os nomes que serão usados como títulos de coluna em vez dos nomes de coluna originais em <em>table</em>.</p></td>
</tr>
<tr class="even">
<td><p><em>tableexpression</em></p></td>
<td><p>O nome da tabela ou tabelas contendo os dados que você deseja recuperar.</p></td>
</tr>
<tr class="odd">
<td><p><em>externaldatabase</em></p></td>
<td><p>O nome do banco de dados que contém as tabelas em <em>tableexpression</em> se elas não estiverem no banco de dados atual.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Para executar essa operação, o mecanismo de banco de dados Microsoft Jet procura a tabela ou tabelas especificadas, extrai as colunas escolhidas, seleciona linhas que atendam a critério e classifica ou agrupa as linhas resultantes na ordem especificada.

Declarações SELECT não alteram os dados no banco de dados.

SELECT é normalmente a primeira palavra em uma declaração SQL. A maior parte das declarações SQL são declarações SELECT ou [SELECT…INTO](select-into-statement-microsoft-access-sql.md).

A sintaxe mínima para uma declaração SELECT é:

Selecione os *campos* de *tabela*

Você pode usar um asterisco (\*) para selecionar todos os campos em uma tabela. O exemplo a seguir seleciona todos os campos na tabela de Funcionários:

```sql
SELECT * FROM Employees;
```

Se um nome de campo estiver incluído em mais do que uma tabela na cláusula FROM, preceda-o com o nome da tabela e o operador **.** (ponto). No exemplo a seguir, o campo Departamento está presente na tabela de Funcionários e na tabela de Supervisores. A declaração SQL seleciona departamentos a partir da tabela de Funcionários e os nomes de supervisores da tabela de Supervisores:

```sql
SELECT Employees.Department, Supervisors.SupvName 
FROM Employees INNER JOIN Supervisors 
WHERE Employees.Department = Supervisors.Department;
```

Quando um objeto **Recordset** é criado, o mecanismo do banco de dados do Microsoft Jet usa o nome de campo da tabela como o nome do objeto **Field** no objeto **Recordset**. Se você desejar um nome de campo diferente ou um nome que não esteja implícito na expressão usada para gerar o campo, use a palavra reservada AS. O exemplo a seguir usa o título Data de Nascimento para nomear o objeto **Field** retornado no objeto **Recordset** resultante:

```sql
SELECT BirthDate 
AS Birth FROM Employees;
```

Sempre que você usar funções agregadas ou consultas que retornem nomes de objeto **Field** ambíguos ou duplicados, deverá usar a cláusula AS para fornecer um nome alternativo para o objeto **Field**. O exemplo a seguir usa o título HeadCount para nomear o objeto **Field** retornado no objeto **Recordset** resultante:

```sql
SELECT COUNT(EmployeeID)
AS HeadCount FROM Employees;
```

Você pode usar as outras cláusulas em uma declaração SELECT para restringir e organizar melhor os seus dados retornados. Para saber mais, consulte o tópico de Ajuda para a cláusula que você está usando.

**Os links fornecidos pela** comunidade [UtterAccess](https://www.utteraccess.com) . UtterAccess é o fórum principal de wiki e a Ajuda do Microsoft Access.

- [SQL to VBA Formatter](https://www.utteraccess.com/forum/sql-vba-formatter-t1165308.html)

- [Exibir Registros com um Intervalo Definido](https://www.utteraccess.com/wiki/index.php/records_within_a_defined_range)

## <a name="example"></a>Exemplo

Alguns dos exemplos a seguir assumem a existência de um campo hipotético chamado Salário em uma tabela de Funcionários. Repare que esse campo não existe realmente na tabela de Funcionários do banco de dados da Northwind.

Este exemplo cria um **Recordset** do tipo dynaset com base em uma declaração SQL que seleciona os campos LastName e FirstName de todos os registros da tabela de Funcionários. Ele chama o procedimento EnumFields, que imprime os conteúdos de um objeto **Recordset** na janela **Depurar**.

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

<br/>

Este exemplo conta o número de registros que têm uma entrada no campo PostalCode e nomeia o campo retornado como Registro.

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

<br/>

Este exemplo mostra o número de funcionários e os salários médio e máximo.

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

<br/>

O procedimento **Sub** EnumFields recebe um objeto **Recordset** do procedimento de chamada. Em seguida, o procedimento formata e imprime os campos do **Recordset** na janela **Depurar**. A variável é o comprimento desejado do campo impresso. Alguns campos podem ser truncados.

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




