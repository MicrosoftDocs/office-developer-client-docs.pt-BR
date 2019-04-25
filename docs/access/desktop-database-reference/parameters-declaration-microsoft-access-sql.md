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
# <a name="parameters-declaration-microsoft-access-sql"></a><span data-ttu-id="3bcbf-102">Declaração PARAMETERS (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="3bcbf-102">PARAMETERS Declaration (Microsoft Access SQL)</span></span>


<span data-ttu-id="3bcbf-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3bcbf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3bcbf-104">Declara o nome e o tipo dos dados de cada parâmetro em uma consulta de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="3bcbf-104">Declares the name and data type of each parameter in a parameter query.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bcbf-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3bcbf-105">Syntax</span></span>

<span data-ttu-id="3bcbf-106">PARAMETERS *nomear tipo de dados* \[, *nomear tipo de dados* \[, …\]\]</span><span class="sxs-lookup"><span data-stu-id="3bcbf-106">PARAMETERS *name datatype* \[ [, *name datatype* \[ [, …]]</span></span>

<span data-ttu-id="3bcbf-107">A declaração PARAMETERS tem as seguintes partes:</span><span class="sxs-lookup"><span data-stu-id="3bcbf-107">The PARAMETERS declaration has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3bcbf-108">Sair</span><span class="sxs-lookup"><span data-stu-id="3bcbf-108">Part</span></span></p></th>
<th><p><span data-ttu-id="3bcbf-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="3bcbf-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3bcbf-110"><em>name</em></span><span class="sxs-lookup"><span data-stu-id="3bcbf-110"><em>name</em></span></span></p></td>
<td><p><span data-ttu-id="3bcbf-p101">O nome do parâmetro. Atribuído à propriedade <strong>Name</strong> do objeto <strong>Parameter</strong> e usado para identificar esse parâmetro na coleção <strong>Parâmetros</strong>. Você pode usar <em>name</em> como uma sequência exibida em uma caixa de diálogo, enquanto o aplicativo executa a consulta. Use colchetes ([ ]) para isolar o texto que contém espaços ou pontuação. Por exemplo, [Baixo preço] e [Iniciar relatório com qual mês?] são argumentos <em>name</em> válidos.</span><span class="sxs-lookup"><span data-stu-id="3bcbf-p101">The name of the parameter. Assigned to the <strong>Name</strong> property of the <strong>Parameter</strong> object and used to identify this parameter in the <strong>Parameters</strong> collection. You can use <em>name</em> as a string that is displayed in a dialog box while your application runs the query. Use brackets ([ ]) to enclose text that contains spaces or punctuation. For example, [Low price] and [Begin report with which month?] are valid <em>name</em> arguments.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3bcbf-116"><em>tipo de dados</em></span><span class="sxs-lookup"><span data-stu-id="3bcbf-116"><em>DataType</em></span></span></p></td>
<td><p><span data-ttu-id="3bcbf-117">Um dos principais <a href="sql-data-types.md">tipos de dados do Microsoft Access SQL</a> ou seus sinônimos.</span><span class="sxs-lookup"><span data-stu-id="3bcbf-117">One of the primary <a href="sql-data-types.md">Microsoft Access SQL data types</a> or their synonyms.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="3bcbf-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="3bcbf-118">Remarks</span></span>

<span data-ttu-id="3bcbf-p102">Para consultas executadas regularmente, você pode usar uma declaração PARAMETERS para criar uma consulta de parâmetro. Uma consulta de parâmetro pode ajudar a automatizar o processo de alteração dos critérios de consulta. Com uma consulta de parâmetro, seu código precisará fornecer os parâmetros cada vez que a consulta for executada.</span><span class="sxs-lookup"><span data-stu-id="3bcbf-p102">For queries that you run regularly, you can use a PARAMETERS declaration to create a parameter query. A parameter query can help automate the process of changing query criteria. With a parameter query, your code will need to provide the parameters each time the query is run.</span></span>

<span data-ttu-id="3bcbf-122">A declaração PARAMETERS é opcional, mas, quando incluso, precede qualquer outra instrução, incluindo [SELECT](select-statement-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="3bcbf-122">The PARAMETERS declaration is optional but when included precedes any other statement, including [SELECT](select-statement-microsoft-access-sql.md).</span></span>

<span data-ttu-id="3bcbf-p103">Se a declaração inclui mais de um parâmetro, separe-os com vírgulas. O exemplo a seguir inclui dois parâmetros:</span><span class="sxs-lookup"><span data-stu-id="3bcbf-p103">If the declaration includes more than one parameter, separate them with commas. The following example includes two parameters:</span></span>

```sql
PARAMETERS [Low price] Currency, [Beginning date] DateTime;
```

<span data-ttu-id="3bcbf-p104">Você pode usar *name* mas não *datatype* em uma cláusula [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) ou [HAVING](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/having-clause-microsoft-access-sql). O exemplo a seguir espera que dois parâmetros sejam fornecidos e, em seguida, aplicar os critérios na tabela Pedidos:</span><span class="sxs-lookup"><span data-stu-id="3bcbf-p104">You can use *name* but not *datatype* in a [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) or [HAVING](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/having-clause-microsoft-access-sql) clause. The following example expects two parameters to be provided and then applies the criteria to records in the Orders table:</span></span>

```sql
PARAMETERS [Low price] Currency, 
[Beginning date] DateTime; 
SELECT OrderID, OrderAmount
FROM Orders 
WHERE OrderAmount > [Low price] 
AND OrderDate >= [Beginning date];
```

## <a name="example"></a><span data-ttu-id="3bcbf-127">Exemplo</span><span class="sxs-lookup"><span data-stu-id="3bcbf-127">Example</span></span>

<span data-ttu-id="3bcbf-128">Este exemplo exige que o usuário forneça um cargo e use este cargo como critério para a consulta.</span><span class="sxs-lookup"><span data-stu-id="3bcbf-128">This example requires the user to provide a job title and then uses that job title as the criteria for the query.</span></span>

<span data-ttu-id="3bcbf-129">Ele é chamado procedimento EnumFields, o qual você pode encontrar no exemplo da [instrução SELECT](select-statement-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="3bcbf-129">It calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>

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
