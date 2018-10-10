---
title: Declaração PARAMETERS (Microsoft Access SQL)
TOCTitle: PARAMETERS Declaration (Microsoft Access SQL)
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
ms.openlocfilehash: 8ef554aab94bd5771e1df3313d04a4fbe2c383b8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464058"
---
# <a name="parameters-declaration-microsoft-access-sql"></a><span data-ttu-id="b7cfb-102">Declaração PARAMETERS (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="b7cfb-102">PARAMETERS Declaration (Microsoft Access SQL)</span></span>


<span data-ttu-id="b7cfb-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b7cfb-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b7cfb-104">Declara o nome e o tipo dos dados de cada parâmetro em uma consulta de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="b7cfb-104">Declares the name and data type of each parameter in a parameter query.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7cfb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b7cfb-105">Syntax</span></span>

<span data-ttu-id="b7cfb-106">PARÂMETROS de *tipo de dados de nome* \[, *nome datatype* \[,...\]\]</span><span class="sxs-lookup"><span data-stu-id="b7cfb-106">PARAMETERS *name datatype* \[, *name datatype* \[, …\]\]</span></span>

<span data-ttu-id="b7cfb-107">A declaração PARAMETERS contém estas partes:</span><span class="sxs-lookup"><span data-stu-id="b7cfb-107">The PARAMETERS declaration has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b7cfb-108">Parte</span><span class="sxs-lookup"><span data-stu-id="b7cfb-108">Part</span></span></p></th>
<th><p><span data-ttu-id="b7cfb-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="b7cfb-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b7cfb-110"><em>name</em></span><span class="sxs-lookup"><span data-stu-id="b7cfb-110"><em>name</em></span></span></p></td>
<td><p><span data-ttu-id="b7cfb-p101">O nome do parâmetro. Atribuído à propriedade <strong>Name</strong> do objeto <strong>Parameter</strong> e usado para identificar esse parâmetro na coleção <strong>Parâmetros</strong>. Você pode usar <em>name</em> como uma sequência exibida em uma caixa de diálogo, enquanto o aplicativo executa a consulta. Use colchetes ([ ]) para isolar o texto que contém espaços ou pontuação. Por exemplo, [Baixo preço] e [Iniciar relatório com qual mês?] são argumentos <em>name</em> válidos.</span><span class="sxs-lookup"><span data-stu-id="b7cfb-p101">The name of the parameter. Assigned to the <strong>Name</strong> property of the <strong>Parameter</strong> object and used to identify this parameter in the <strong>Parameters</strong> collection. You can use <em>name</em> as a string that is displayed in a dialog box while your application runs the query. Use brackets ([ ]) to enclose text that contains spaces or punctuation. For example, [Low price] and [Begin report with which month?] are valid <em>name</em> arguments.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7cfb-116"><em>tipo de dados</em></span><span class="sxs-lookup"><span data-stu-id="b7cfb-116"><em>datatype</em></span></span></p></td>
<td><p><span data-ttu-id="b7cfb-117">Um dos principais <a href="sql-data-types.md">tipos de dados do Microsoft Access SQL</a> ou seus sinônimos.</span><span class="sxs-lookup"><span data-stu-id="b7cfb-117">One of the primary <a href="sql-data-types.md">Microsoft Access SQL data types</a> or their synonyms.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b7cfb-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="b7cfb-118">Remarks</span></span>

<span data-ttu-id="b7cfb-p102">Para consultas executadas regularmente, você pode usar uma declaração PARAMETERS para criar uma consulta de parâmetro. Uma consulta de parâmetro pode ajudar a automatizar o processo de alteração dos critérios de consulta. Com uma consulta de parâmetro, seu código precisará fornecer os parâmetros cada vez que a consulta for executada.</span><span class="sxs-lookup"><span data-stu-id="b7cfb-p102">For queries that you run regularly, you can use a PARAMETERS declaration to create a parameter query. A parameter query can help automate the process of changing query criteria. With a parameter query, your code will need to provide the parameters each time the query is run.</span></span>

<span data-ttu-id="b7cfb-122">A declaração PARAMETERS é opcional, mas, quando incluso, precede qualquer outra instrução, incluindo [SELECT](select-statement-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="b7cfb-122">The PARAMETERS declaration is optional but when included precedes any other statement, including [SELECT](select-statement-microsoft-access-sql.md).</span></span>

<span data-ttu-id="b7cfb-p103">Se a declaração incluir mais de um parâmetro, separe-os com vírgulas. O exemplo a seguir inclui dois parâmetros:</span><span class="sxs-lookup"><span data-stu-id="b7cfb-p103">If the declaration includes more than one parameter, separate them with commas. The following example includes two parameters:</span></span>

```sql
PARAMETERS [Low price] Currency, [Beginning date] DateTime;
```

<span data-ttu-id="b7cfb-125">Você pode usar o *nome* , mas não *datatype* em uma cláusula [onde](https://msdn.microsoft.com/library/ff195245\(v=office.15\)) ou [HAVING](https://msdn.microsoft.com/library/ff193795\(v=office.15\)) .</span><span class="sxs-lookup"><span data-stu-id="b7cfb-125">You can use *name* but not *datatype* in a [WHERE](https://msdn.microsoft.com/library/ff195245\(v=office.15\)) or [HAVING](https://msdn.microsoft.com/library/ff193795\(v=office.15\)) clause.</span></span> <span data-ttu-id="b7cfb-126">O exemplo a seguir espera que dois parâmetros sejam fornecidos e, em seguida, aplicar os critérios na tabela Pedidos:</span><span class="sxs-lookup"><span data-stu-id="b7cfb-126">The following example expects two parameters to be provided and then applies the criteria to records in the Orders table:</span></span>

```sql
PARAMETERS [Low price] Currency, 
[Beginning date] DateTime; 
SELECT OrderID, OrderAmount
FROM Orders 
WHERE OrderAmount > [Low price] 
AND OrderDate >= [Beginning date];
```

## <a name="example"></a><span data-ttu-id="b7cfb-127">Exemplo</span><span class="sxs-lookup"><span data-stu-id="b7cfb-127">Example</span></span>

<span data-ttu-id="b7cfb-128">Este exemplo requer que o usuário forneça um cargo e, em seguida, use aquele cargo como o critério para a consulta.</span><span class="sxs-lookup"><span data-stu-id="b7cfb-128">This example requires the user to provide a job title and then uses that job title as the criteria for the query.</span></span>

<span data-ttu-id="b7cfb-129">Este exemplo chama o procedimento EnumFields, que pode ser encontrado no exemplo da [Instrução SELECT](select-statement-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="b7cfb-129">This example calls the EnumFields procedure, which you can find in the [SELECT statement](select-statement-microsoft-access-sql.md) example.</span></span>

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
