---
title: Declaração PARAMETERS (Microsoft Access SQL)
TOCTitle: PARAMETERS declaration (Microsoft Access SQL)
ms:assetid: 0dcaad68-6a5f-93dc-e62a-b82b36e1e69c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845220(v=office.15)
ms:contentKeyID: 48543230
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277577
dev_langs:
- sql
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: d78a6c043e99af1ca50ca798b94088400fd09f0d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287864"
---
# <a name="parameters-declaration-microsoft-access-sql"></a>Declaração PARAMETERS (Microsoft Access SQL)


**Aplica-se ao:** Access 2013, Office 2013

Declara o nome e o tipo dos dados de cada parâmetro em uma consulta de parâmetro.

## <a name="syntax"></a>Sintaxe

PARAMETERS *nomear tipo de dados* \[, *nomear tipo de dados* \[, …\]\]

A declaração PARAMETERS tem as seguintes partes:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Sair</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>name</em></p></td>
<td><p>O nome do parâmetro. Atribuído à propriedade <strong>Name</strong> do objeto <strong>Parameter</strong> e usado para identificar esse parâmetro na coleção <strong>Parâmetros</strong>. Você pode usar <em>name</em> como uma sequência exibida em uma caixa de diálogo, enquanto o aplicativo executa a consulta. Use colchetes ([ ]) para isolar o texto que contém espaços ou pontuação. Por exemplo, [Baixo preço] e [Iniciar relatório com qual mês?] são argumentos <em>name</em> válidos.</p></td>
</tr>
<tr class="even">
<td><p><em>tipo de dados</em></p></td>
<td><p>Um dos principais <a href="sql-data-types.md">tipos de dados do Microsoft Access SQL</a> ou seus sinônimos.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Para consultas executadas regularmente, você pode usar uma declaração PARAMETERS para criar uma consulta de parâmetro. Uma consulta de parâmetro pode ajudar a automatizar o processo de alteração dos critérios de consulta. Com uma consulta de parâmetro, seu código precisará fornecer os parâmetros cada vez que a consulta for executada.

A declaração PARAMETERS é opcional, mas, quando incluso, precede qualquer outra instrução, incluindo [SELECT](select-statement-microsoft-access-sql.md).

Se a declaração inclui mais de um parâmetro, separe-os com vírgulas. O exemplo a seguir inclui dois parâmetros:

```sql
PARAMETERS [Low price] Currency, [Beginning date] DateTime;
```

Você pode usar *name* mas não *datatype* em uma cláusula [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) ou [HAVING](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/having-clause-microsoft-access-sql). O exemplo a seguir espera que dois parâmetros sejam fornecidos e, em seguida, aplicar os critérios na tabela Pedidos:

```sql
PARAMETERS [Low price] Currency, 
[Beginning date] DateTime; 
SELECT OrderID, OrderAmount
FROM Orders 
WHERE OrderAmount > [Low price] 
AND OrderDate >= [Beginning date];
```

## <a name="example"></a>Exemplo

Este exemplo exige que o usuário forneça um cargo e use este cargo como critério para a consulta.

Ele é chamado procedimento EnumFields, o qual você pode encontrar no exemplo da [instrução SELECT](select-statement-microsoft-access-sql.md).

```vb
    Sub ParametersX() 
     
        Dim dbs As Database, qdf As QueryDef 
        Dim rst As Recordset 
        Dim strSql As String, strParm As String 
        Dim strMessage As String 
        Dim intCommand As Integer 
         
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("NorthWind.mdb") 
         
        ' Define the parameters clause. 
        strParm = "PARAMETERS [Employee Title] CHAR; " 
     
        ' Define an SQL statement with the parameters 
        ' clause. 
        strSql = strParm & "SELECT LastName, FirstName, " _ 
            & "EmployeeID " _ 
            & "FROM Employees " _ 
            & "WHERE Title =[Employee Title];" 
         
        ' Create a QueryDef object based on the  
        ' SQL statement. 
        Set qdf = dbs.CreateQueryDef _ 
            ("Find Employees", strSql) 
         
        Do While True 
            strMessage = "Find Employees by Job " _ 
                & "title:" & Chr(13) _ 
                & "  Choose Job Title:" & Chr(13) _ 
                & "   1 - Sales Manager" & Chr(13) _ 
                & "   2 - Sales Representative" & Chr(13) _ 
                & "   3 - Inside Sales Coordinator" 
             
            intCommand = Val(InputBox(strMessage)) 
             
            Select Case intCommand 
                Case 1 
                    qdf("Employee Title") = _ 
                        "Sales Manager" 
                Case 2 
                    qdf("Employee Title") = _ 
                        "Sales Representative" 
                Case 3 
                    qdf("Employee Title") = _ 
                        "Inside Sales Coordinator" 
                Case Else 
                    Exit Do 
            End Select 
             
            ' Create a temporary snapshot-type Recordset. 
            Set rst = qdf.OpenRecordset(dbOpenSnapshot) 
     
            ' Populate the Recordset. 
            rst.MoveLast 
                 
            ' Call EnumFields to print the contents of the  
            ' Recordset. Pass the Recordset object and desired 
            ' field width. 
            EnumFields rst, 12 
     
        Loop 
         
        ' Delete the QueryDef because this is a 
        ' demonstration. 
        dbs.QueryDefs.Delete "Find Employees" 
         
        dbs.Close 
     
    End Sub
```
