---
title: Propriedade Recordset2.BatchCollisionCount (DAO)
TOCTitle: BatchCollisionCount Property
ms:assetid: 997dfbb3-673c-8813-f51b-ab8d95093c4f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197961(v=office.15)
ms:contentKeyID: 48546514
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 90e1712c8f7341967ed8eabf01d7e498d6c0e4d9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465233"
---
# <a name="recordset2batchcollisioncount-property-dao"></a>Propriedade Recordset2.BatchCollisionCount (DAO)


**Aplica-se a**: Access 2013 | Office 2013

## <a name="syntax"></a>Sintaxe

*expressão* . BatchCollisionCount

*expressão* Uma variável que representa um objeto **Recordset2** .

## <a name="remarks"></a>Comentários

Essa propriedade indica quantos registros encontraram colisões ou falharam na atualização durante a última tentativa de atualização em lotes. O valor dessa propriedade corresponde ao número de indicadores da propriedade **[BatchCollisions](recordset2-batchcollisions-property-dao.md)**.

Se você definir a propriedade [**Bookmark**](recordset2-bookmark-property-dao.md) do objeto de trabalho **Recordset** como os valores do indicador na matriz **BatchCollisions**, poderá mover cada registro com falha para concluir a operação **[Update](recordset2-update-method-dao.md)** do lote mais recente.

Depois que os registros da colisão forem corrigidos, um método **Update** do modo de lotes poderá ser chamado novamente. Nesse ponto, o DAO tentará outra atualização em lotes e a propriedade **BatchCollisions** refletirá novamente o conjunto de registros que falharam na segunda tentativa. Quaisquer registros que foram bem-sucedidos na tentativa anterior não serão enviados na tentativa atual, porque agora possuem a propriedade **[RecordStatus](recordset2-recordstatus-property-dao.md)** de **dbRecordUnmodified**. Esse processo poderá continuar enquanto ocorrem colisões ou até que você desista das atualizações e feche o conjunto de resultados.

## <a name="example"></a>Exemplo

Este exemplo utiliza a propriedade **BatchCollisionCount** e o método **Update** para demonstrar a atualização em lote em que qualquer colisão é resolvida forçando a atualização em lote.

```vb 
Sub BatchX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim rstTemp As Recordset2 
 Dim intLoop As Integer 
 Dim strPrompt As String 
 
 Set wrkMain = CreateWorkspace("ODBCWorkspace", _ 
 "admin", "", dbUseODBC) 
 ' This DefaultCursorDriver setting is required for 
 ' batch updating. 
 wrkMain.DefaultCursorDriver = dbUseClientBatchCursor 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conMain = wrkMain.OpenConnection("Publishers", _ 
 dbDriverNoPrompt, False, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' The following locking argument is required for 
 ' batch updating. It is also required that a table 
 ' with a primary key is used. 
 Set rstTemp = conMain.OpenRecordset( _ 
 "SELECT * FROM roysched", dbOpenDynaset, 0, _ 
 dbOptimisticBatch) 
 
 With rstTemp 
 ' Modify data in local recordset. 
 Do While Not .EOF 
 .Edit 
 If !royalty <= 20 Then 
 !royalty = !royalty - 4 
 Else 
 !royalty = !royalty + 2 
 End If 
 .Update 
 .MoveNext 
 Loop 
 
 ' Attempt a batch update. 
 .Update dbUpdateBatch 
 
 ' If there are collisions, give the user the option 
 ' of forcing the changes or resolving them 
 ' individually. 
 If .BatchCollisionCount > 0 Then 
 strPrompt = "There are collisions. " & vbCr & _ 
 "Do you want the program to force " & _ 
 vbCr & "an update using the local data?" 
 If MsgBox(strPrompt, vbYesNo) = vbYes Then _ 
 .Update dbUpdateBatch, True 
 End If 
 
 .Close 
 End With 
 
 conMain.Close 
 wrkMain.Close 
 
End Sub 
 
```

