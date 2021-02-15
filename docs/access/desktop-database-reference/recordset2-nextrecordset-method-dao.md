---
title: Método Recordset2.NextRecordset (DAO)
TOCTitle: NextRecordset Method
ms:assetid: 33288131-d4f3-0159-1736-f401346087f3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192318(v=office.15)
ms:contentKeyID: 48544096
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053575
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 54d0e49dfbe9dc3fb87eb10af9eefe3aa2f83709
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307235"
---
# <a name="recordset2nextrecordset-method-dao"></a><span data-ttu-id="4638b-102">Método Recordset2.NextRecordset (DAO)</span><span class="sxs-lookup"><span data-stu-id="4638b-102">Recordset2.NextRecordset method (DAO)</span></span>


<span data-ttu-id="4638b-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4638b-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="4638b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4638b-104">Syntax</span></span>

<span data-ttu-id="4638b-105">*expressão* . NextRecordset</span><span class="sxs-lookup"><span data-stu-id="4638b-105">*expression* .NextRecordset</span></span>

<span data-ttu-id="4638b-106">*expressão* Uma variável que representa **um objeto Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="4638b-106">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="return-value"></a><span data-ttu-id="4638b-107">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="4638b-107">Return value</span></span>

<span data-ttu-id="4638b-108">Booliano</span><span class="sxs-lookup"><span data-stu-id="4638b-108">Boolean</span></span>

## <a name="remarks"></a><span data-ttu-id="4638b-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="4638b-109">Remarks</span></span>

<span data-ttu-id="4638b-110">Em um espaço de trabalho ODBCDirect, você pode abrir um **Recordset** contendo mais de uma consulta seleção no argumento de origem de **OpenRecordset** ou a propriedade **[SQL](querydef-sql-property-dao.md)** de um objeto **[QueryDef](querydef-object-dao.md)** de consulta seleção, como no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="4638b-110">In an ODBCDirect workspace, you can open a **Recordset** containing more than one select query in the source argument of **OpenRecordset**, or the **[SQL](querydef-sql-property-dao.md)** property of a select query **[QueryDef](querydef-object-dao.md)** object, as in the following example.</span></span>

```sql
    SELECT LastName, FirstName FROM Authors 
    WHERE LastName = 'Smith'; 
    SELECT Title, ISBN FROM Titles 
    WHERE Pub_ID = 9999 
```

<span data-ttu-id="4638b-p101">O **Recordset** retornado será aberto com os resultados da primeira consulta. Para obter os conjuntos de resultados dos registros das consultas subsequentes, use o método **NextRecordset**.</span><span class="sxs-lookup"><span data-stu-id="4638b-p101">The returned **Recordset** will open with the results of the first query. To obtain the result sets of records from subsequent queries, use the **NextRecordset** method.</span></span>

<span data-ttu-id="4638b-p102">Se mais registros estiverem disponíveis (isto é, se houver outra consulta seleção na chamada **OpenRecordset** ou na propriedade **SQL**), os registros retornados da próxima consulta serão carregados em **Recordset**, e **NextRecordset** retornará **True**, indicando que os registros estão disponíveis. Quando nenhum registro estiver disponível (isto é, os resultados da última consulta seleção tiverem sido carregados em **Recordset**), em seguida **NextRecordset** retornará **False**, e o **Recordset** estará vazio.</span><span class="sxs-lookup"><span data-stu-id="4638b-p102">If more records are available (that is, there was another select query in the **OpenRecordset** call or in the **SQL** property), the records returned from the next query will be loaded into the **Recordset**, and **NextRecordset** will return **True**, indicating that the records are available. When no more records are available (that is, results of the last select query have been loaded into the **Recordset**), then **NextRecordset** will return **False**, and the **Recordset** will be empty.</span></span>

<span data-ttu-id="4638b-p103">Você não pode usar o método **[Cancel](connection-cancel-method-dao.md)** para retirar o conteúdo de um **Recordset**. Entretanto, **Cancel** também retira qualquer registro adicional ainda não carregado.</span><span class="sxs-lookup"><span data-stu-id="4638b-p103">You can also use the **[Cancel](connection-cancel-method-dao.md)** method to flush the contents of a **Recordset**. However, **Cancel** also flushes any additional records not yet loaded.</span></span>

## <a name="example"></a><span data-ttu-id="4638b-117">Exemplo</span><span class="sxs-lookup"><span data-stu-id="4638b-117">Example</span></span>

<span data-ttu-id="4638b-p104">Este exemplo usa o método **NextRecordset** para visualizar os dados de uma consulta SELECT composta. A propriedade **DefaultCursorDriver** deve estar definida como **dbUseODBCCursor** ao executar essas consultas. O método **NextRecordset** retornará **True** mesmo se algumas ou todas as instruções SELECT retornarem registros em branco; ele retornará **False** somente após a verificação de todas as cláusulas SQL individuais.</span><span class="sxs-lookup"><span data-stu-id="4638b-p104">This example uses the **NextRecordset** method to view the data from a compound SELECT query. The **DefaultCursorDriver** property must be set to **dbUseODBCCursor** when executing such queries. The **NextRecordset** method will return **True** even if some or all of the SELECT statements return zero records; it will return **False** only after all the individual SQL clauses have been checked.</span></span>

```vb
    Sub NextRecordsetX() 
     
     Dim wrkODBC As Workspace 
     Dim conPubs As Connection 
     Dim rstTemp As Recordset2 
     Dim intCount As Integer 
     Dim booNext As Boolean 
     
     ' Create ODBCDirect Workspace object and open Connection 
     ' object. The DefaultCursorDriver setting is required 
     ' when using compound SQL statements. 
     Set wrkODBC = CreateWorkspace("", _ 
     "admin", "", dbUseODBC) 
     wrkODBC.DefaultCursorDriver = dbUseODBCCursor 
     
     ' Note: The DSN referenced below must be set to 
     ' use Microsoft Windows NT Authentication Mode to 
     ' authorize user access to the Microsoft SQL Server. 
     Set conPubs = wrkODBC.OpenConnection("Publishers", , , _ 
     "ODBC;DATABASE=pubs;DSN=Publishers") 
     
     ' Construct compound SELECT statement. 
     Set rstTemp = conPubs.OpenRecordset("SELECT * " & _ 
     "FROM authors; " & _ 
     "SELECT * FROM stores; " & _ 
     "SELECT * FROM jobs") 
     
     ' Try printing results from each of the three SELECT 
     ' statements. 
     booNext = True 
     intCount = 1 
     With rstTemp 
     Do While booNext 
     Debug.Print "Contents of recordset #" & intCount 
     Do While Not .EOF 
     Debug.Print , .Fields(0), .Fields(1) 
     .MoveNext 
     Loop 
     booNext = .NextRecordset 
     Debug.Print " rstTemp.NextRecordset = " & _ 
     booNext 
     intCount = intCount + 1 
     Loop 
     End With 
     
     rstTemp.Close 
     conPubs.Close 
     wrkODBC.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="4638b-p105">Outra forma de cumprir a mesma tarefa é criar uma instrução preparada contendo a instrução SQL composta. A propriedade **CacheSize** do objeto **QueryDef** deve ser definida como 1, e o objeto **Recordset** deve ser somente encaminhamento e somente leitura.</span><span class="sxs-lookup"><span data-stu-id="4638b-p105">Another way to accomplish the same task would be to create a prepared statement containing the compound SQL statement. The **CacheSize** property of the **QueryDef** object must be set to 1, and the **Recordset** object must be forward-only and read-only.</span></span>

```vb 
Sub NextRecordsetX2() 
 
 Dim wrkODBC As Workspace 
 Dim conPubs As Connection 
 Dim qdfTemp As QueryDef 
 Dim rstTemp As Recordset2 
 Dim intCount As Integer 
 Dim booNext As Boolean 
 
 ' Create ODBCDirect Workspace object and open Connection 
 ' object. The DefaultCursorDriver setting is required 
 ' when using compound SQL statements. 
 Set wrkODBC = CreateWorkspace("", _ 
 "admin", "", dbUseODBC) 
 wrkODBC.DefaultCursorDriver = dbUseODBCCursor 
 
 ' Note: The DSN referenced below must be set to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conPubs = wrkODBC.OpenConnection("Publishers", , , _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' Create a temporary stored procedure with a compound 
 ' SELECT statement. 
 Set qdfTemp = conPubs.CreateQueryDef("", _ 
 "SELECT * FROM authors; " & _ 
 "SELECT * FROM stores; " & _ 
 "SELECT * FROM jobs") 
 ' Set CacheSize and open Recordset object with arguments 
 ' that will allow access to multiple recordsets. 
 qdfTemp.CacheSize = 1 
 Set rstTemp = qdfTemp.OpenRecordset(dbOpenForwardOnly, _ 
 dbReadOnly) 
 
 ' Try printing results from each of the three SELECT 
 ' statements. 
 booNext = True 
 intCount = 1 
 With rstTemp 
 Do While booNext 
 Debug.Print "Contents of recordset #" & intCount 
 Do While Not .EOF 
 Debug.Print , .Fields(0), .Fields(1) 
 .MoveNext 
 Loop 
 booNext = .NextRecordset 
 Debug.Print " rstTemp.NextRecordset = " & _ 
 booNext 
 intCount = intCount + 1 
 Loop 
 End With 
 
 rstTemp.Close 
 qdfTemp.Close 
 conPubs.Close 
 wrkODBC.Close 
 
End Sub 
 
```

