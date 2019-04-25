---
title: Instrução EXECUTE (Microsoft Access SQL)
TOCTitle: EXECUTE statement (Microsoft Access SQL)
ms:assetid: 9ec4d9ee-db2a-0319-3ccf-c035d67a1496
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198330(v=office.15)
ms:contentKeyID: 48546667
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277471
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: df70d2728732f33161622ce71fc9273bd9f016f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293235"
---
# <a name="execute-statement-microsoft-access-sql"></a><span data-ttu-id="e581b-102">Instrução EXECUTE (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="e581b-102">EXECUTE Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="e581b-103">**Aplica-se ao**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e581b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e581b-104">Utilizada para chamar a execução de um procedimento.</span><span class="sxs-lookup"><span data-stu-id="e581b-104">Used to invoke the execution of a procedure.</span></span>

## <a name="syntax"></a><span data-ttu-id="e581b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e581b-105">Syntax</span></span>

<span data-ttu-id="e581b-106">EXECUTE *procedimento* \[*param1*\[, *param2*\[, …\]\]</span><span class="sxs-lookup"><span data-stu-id="e581b-106">EXECUTE *procedure [param1* \[[, *param2*[, …]]</span></span>

<span data-ttu-id="e581b-107">A instrução EXECUTE tem as seguintes partes:</span><span class="sxs-lookup"><span data-stu-id="e581b-107">The EXECUTE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e581b-108">Sair</span><span class="sxs-lookup"><span data-stu-id="e581b-108">Part</span></span></p></th>
<th><p><span data-ttu-id="e581b-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="e581b-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e581b-110"><em>procedimento</em></span><span class="sxs-lookup"><span data-stu-id="e581b-110"><em>procedure</em></span></span></p></td>
<td><p><span data-ttu-id="e581b-111">O nome do procedimento a ser executado.</span><span class="sxs-lookup"><span data-stu-id="e581b-111">The name of the procedure that is to be executed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e581b-112"><em>param1, param2, …</em></span><span class="sxs-lookup"><span data-stu-id="e581b-112"><em>param1, param2, …</em></span></span></p></td>
<td><p><span data-ttu-id="e581b-113">Valores para os parâmetros definidos pelo procedimento.</span><span class="sxs-lookup"><span data-stu-id="e581b-113">Values for the parameters defined by the procedure.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="example"></a><span data-ttu-id="e581b-114">Exemplo</span><span class="sxs-lookup"><span data-stu-id="e581b-114">Example</span></span>

<span data-ttu-id="e581b-115">Este exemplo chama a consulta CategoryList e o procedimento EnumFields, o que pode ser localizado no exemplo da instrução SELECT.</span><span class="sxs-lookup"><span data-stu-id="e581b-115">This example calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>

```vb
    Sub ProcedureX() 
     
        Dim dbs As Database, rst As Recordset 
        Dim qdf As QueryDef, strSql As String 
         
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        strSql = "PROCEDURE CategoryList; " _ 
            & "SELECT DISTINCTROW CategoryName, " _ 
            & "CategoryID FROM Categories " _ 
            & "ORDER BY CategoryName;" 
         
        ' Create a named QueryDef based on the SQL 
        ' statement. 
        Set qdf = dbs.CreateQueryDef("NewQry", strSql) 
     
        ' Create a temporary snapshot-type Recordset. 
        Set rst = qdf.OpenRecordset(dbOpenSnapshot) 
     
        ' Populate the Recordset. 
        rst.MoveLast 
                 
        ' Call EnumFields to print the contents of the  
        ' Recordset. Pass the Recordset object and desired 
        ' field width. 
        Execute EnumFields rst, 15 
         
        ' Delete the QueryDef because this is a 
        ' demonstration. 
        dbs.QueryDefs.Delete "NewQry" 
         
        dbs.Close 
     
    End Sub
```
