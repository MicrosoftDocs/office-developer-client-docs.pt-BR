---
title: Propriedade Database.RecordsAffected (DAO)
TOCTitle: RecordsAffected Property
ms:assetid: 1c591231-21dd-f0b1-4ba6-87784c5890d3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845732(v=office.15)
ms:contentKeyID: 48543567
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 346e01359b3ffef50a15ad3a9c3502b1104d6e0f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888992"
---
# <a name="databaserecordsaffected-property-dao"></a><span data-ttu-id="b7b9b-102">Propriedade Database.RecordsAffected (DAO)</span><span class="sxs-lookup"><span data-stu-id="b7b9b-102">Database.RecordsAffected Property (DAO)</span></span>


<span data-ttu-id="b7b9b-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="b7b9b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b7b9b-104">Retorna o número de registros afetados pelo método **[Execute](connection-execute-method-dao.md)** chamado mais recentemente.</span><span class="sxs-lookup"><span data-stu-id="b7b9b-104">Returns the number of records affected by the most recently invoked **[Execute](connection-execute-method-dao.md)** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7b9b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b7b9b-105">Syntax</span></span>

<span data-ttu-id="b7b9b-106">*expressão* . RecordsAffected</span><span class="sxs-lookup"><span data-stu-id="b7b9b-106">*expression* .RecordsAffected</span></span>

<span data-ttu-id="b7b9b-107">*expressão* Uma variável que representa um objeto de **banco de dados** .</span><span class="sxs-lookup"><span data-stu-id="b7b9b-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="example"></a><span data-ttu-id="b7b9b-108">Exemplo</span><span class="sxs-lookup"><span data-stu-id="b7b9b-108">Example</span></span>

<span data-ttu-id="b7b9b-p101">Este exemplo usa a propriedade **RecordsAffected** com as consultas ação executadas a partir de um objeto **Database** e de um objeto **QueryDef**. A função RecordsAffectedOutput é exigida para que esse procedimento seja executado.</span><span class="sxs-lookup"><span data-stu-id="b7b9b-p101">This example uses the **RecordsAffected** property with action queries executed from a **Database** object and from a **QueryDef** object. The RecordsAffectedOutput function is required for this procedure to run.</span></span>

```vb
    Sub RecordsAffectedX() 
     
     Dim dbsNorthwind As Database 
     Dim qdfTemp As QueryDef 
     Dim strSQLChange As String 
     Dim strSQLRestore As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Print report of contents of the Employees 
     ' table. 
     Debug.Print _ 
     "Number of records in Employees table: " & _ 
     .TableDefs!Employees.RecordCount 
     RecordsAffectedOutput dbsNorthwind 
     
     ' Define and execute an action query. 
     strSQLChange = "UPDATE Employees " & _ 
     "SET Country = 'United States' " & _ 
     "WHERE Country = 'USA'" 
     .Execute strSQLChange 
     
     ' Print report of contents of the Employees 
     ' table. 
     Debug.Print _ 
     "RecordsAffected after executing query " & _ 
     "from Database: " & .RecordsAffected 
     RecordsAffectedOutput dbsNorthwind 
     
     ' Define and run another action query. 
     strSQLRestore = "UPDATE Employees " & _ 
     "SET Country = 'USA' " & _ 
     "WHERE Country = 'United States'" 
     Set qdfTemp = .CreateQueryDef("", strSQLRestore) 
     qdfTemp.Execute 
     
     ' Print report of contents of the Employees 
     ' table. 
     Debug.Print _ 
     "RecordsAffected after executing query " & _ 
     "from QueryDef: " & qdfTemp.RecordsAffected 
     RecordsAffectedOutput dbsNorthwind 
     
     .Close 
     
     End With 
     
    End Sub 
     
    Function RecordsAffectedOutput(dbsNorthwind As Database) 
     
     Dim rstEmployees As Recordset 
     
     ' Open a Recordset object from the Employees table. 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     With rstEmployees 
     ' Enumerate Recordset. 
     .MoveFirst 
     Do While Not .EOF 
     Debug.Print " " & !LastName & ", " & !Country 
     .MoveNext 
     Loop 
     .Close 
     End With 
     
    End Function
```
