---
title: Propriedade QueryDef.RecordsAffected (DAO)
TOCTitle: RecordsAffected Property
ms:assetid: 29a864b5-305c-d33f-b2ca-fc9a08baaa5c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192040(v=office.15)
ms:contentKeyID: 48543886
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053082
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 63762814d0eb90cccb86402dbd6284fd873aef73
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887800"
---
# <a name="querydefrecordsaffected-property-dao"></a><span data-ttu-id="38385-102">Propriedade QueryDef.RecordsAffected (DAO)</span><span class="sxs-lookup"><span data-stu-id="38385-102">QueryDef.RecordsAffected Property (DAO)</span></span>


<span data-ttu-id="38385-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="38385-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="38385-104">Retorna o número de registros afetados pelo método **[Execute](querydef-execute-method-dao.md)** chamado mais recentemente.</span><span class="sxs-lookup"><span data-stu-id="38385-104">Returns the number of records affected by the most recently invoked **[Execute](querydef-execute-method-dao.md)** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="38385-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="38385-105">Syntax</span></span>

<span data-ttu-id="38385-106">*expressão* . RecordsAffected</span><span class="sxs-lookup"><span data-stu-id="38385-106">*expression* .RecordsAffected</span></span>

<span data-ttu-id="38385-107">*expressão* Uma variável que representa um objeto **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="38385-107">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="38385-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="38385-108">Remarks</span></span>

<span data-ttu-id="38385-109">Quando você usar o método **Execute** para executar uma consulta ação a partir de um objeto **QueryDef**, a propriedade **RecordsAffected** conterá o número de registros excluídos, atualizados ou inseridos.</span><span class="sxs-lookup"><span data-stu-id="38385-109">When you use the **Execute** method to run an action query from a **QueryDef** object, the **RecordsAffected** property will contain the number of records deleted, updated, or inserted.</span></span>

## <a name="example"></a><span data-ttu-id="38385-110">Exemplo</span><span class="sxs-lookup"><span data-stu-id="38385-110">Example</span></span>

<span data-ttu-id="38385-p101">Este exemplo usa a propriedade **RecordsAffected** com as consultas ação executadas a partir de um objeto **[Database](database-object-dao.md)** e de um objeto **QueryDef**. A função RecordsAffectedOutput é necessária para executar esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="38385-p101">This example uses the **RecordsAffected** property with action queries executed from a **[Database](database-object-dao.md)** object and from a **QueryDef** object. The RecordsAffectedOutput function is required for this procedure to run.</span></span>

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
