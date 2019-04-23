---
title: Método Recordset. NextRecordset (DAO)
TOCTitle: NextRecordset Method
ms:assetid: 4a3a6176-0aa0-efb6-b175-dbe23e266abc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193483(v=office.15)
ms:contentKeyID: 48544664
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 39e508830b41e7b3f74f548451a30132723d210f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284494"
---
# <a name="recordsetnextrecordset-method-dao"></a>Método Recordset. NextRecordset (DAO)


**Aplica-se ao:** Access 2013, Office 2013

## <a name="syntax"></a>Sintaxe

*expressão* . NextRecordset

*expressão* Uma variável que representa um objeto **Recordset** .

## <a name="return-value"></a>Valor de retorno

Booliano

## <a name="remarks"></a>Comentários

Em um espaço de trabalho ODBCDirect, você pode abrir um **[Recordset](recordset-object-dao.md)** que contém mais de uma consulta seleção no argumento Source de **OpenRecordset**ou a propriedade **[SQL](querydef-sql-property-dao.md)** de um objeto **[QueryDef](querydef-object-dao.md)** de consulta seleção, como no exemplo a seguir.

```sql
    SELECT LastName, FirstName FROM Authors 
    WHERE LastName = 'Smith'; 
    SELECT Title, ISBN FROM Titles 
    WHERE Pub_ID = 9999 
```

O **Recordset** retornado será aberto com os resultados da primeira consulta. Para obter os conjuntos de resultados dos registros das consultas subsequentes, use o método **NextRecordset**.

Se mais registros estiverem disponíveis (isto é, se houver outra consulta seleção na chamada **OpenRecordset** ou na propriedade **SQL**), os registros retornados da próxima consulta serão carregados em **Recordset**, e **NextRecordset** retornará **True**, indicando que os registros estão disponíveis. Quando nenhum registro estiver disponível (isto é, os resultados da última consulta seleção tiverem sido carregados em **Recordset**), em seguida **NextRecordset** retornará **False**, e o **Recordset** estará vazio.

Você não pode usar o método **[Cancel](connection-cancel-method-dao.md)** para retirar o conteúdo de um **Recordset**. Entretanto, **Cancel** também retira qualquer registro adicional ainda não carregado.

## <a name="example"></a>Exemplo

Este exemplo usa o método **NextRecordset** para visualizar os dados de uma consulta SELECT composta. A propriedade **DefaultCursorDriver** deve estar definida como **dbUseODBCCursor** ao executar essas consultas. O método **NextRecordset** retornará **True** mesmo se algumas ou todas as instruções SELECT retornarem registros em branco; ele retornará **False** somente após a verificação de todas as cláusulas SQL individuais.

```vb
    Sub NextRecordsetX() 
     
     Dim wrkODBC As Workspace 
     Dim conPubs As Connection 
     Dim rstTemp As Recordset 
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

Outra forma de cumprir a mesma tarefa é criar uma instrução preparada contendo a instrução SQL composta. A propriedade **CacheSize** do objeto **QueryDef** deve ser definida como 1, e o objeto **Recordset** deve ser somente encaminhamento e somente leitura.

```vb 
Sub NextRecordsetX2() 
 
 Dim wrkODBC As Workspace 
 Dim conPubs As Connection 
 Dim qdfTemp As QueryDef 
 Dim rstTemp As Recordset 
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

