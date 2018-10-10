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
# <a name="recordset2batchcollisioncount-property-dao"></a><span data-ttu-id="2c132-102">Propriedade Recordset2.BatchCollisionCount (DAO)</span><span class="sxs-lookup"><span data-stu-id="2c132-102">Recordset2.BatchCollisionCount Property (DAO)</span></span>


<span data-ttu-id="2c132-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2c132-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="2c132-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2c132-104">Syntax</span></span>

<span data-ttu-id="2c132-105">*expressão* . BatchCollisionCount</span><span class="sxs-lookup"><span data-stu-id="2c132-105">*expression* .BatchCollisionCount</span></span>

<span data-ttu-id="2c132-106">*expressão* Uma variável que representa um objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="2c132-106">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c132-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="2c132-107">Remarks</span></span>

<span data-ttu-id="2c132-p101">Essa propriedade indica quantos registros encontraram colisões ou falharam na atualização durante a última tentativa de atualização em lotes. O valor dessa propriedade corresponde ao número de indicadores da propriedade **[BatchCollisions](recordset2-batchcollisions-property-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="2c132-p101">This property indicates how many records encountered collisions or otherwise failed to update during the last batch update attempt. The value of this property corresponds to the number of bookmarks in the **[BatchCollisions](recordset2-batchcollisions-property-dao.md)** property.</span></span>

<span data-ttu-id="2c132-110">Se você definir a propriedade [**Bookmark**](recordset2-bookmark-property-dao.md) do objeto de trabalho **Recordset** como os valores do indicador na matriz **BatchCollisions**, poderá mover cada registro com falha para concluir a operação **[Update](recordset2-update-method-dao.md)** do lote mais recente.</span><span class="sxs-lookup"><span data-stu-id="2c132-110">If you set the working **Recordset** object's **[Bookmark](recordset2-bookmark-property-dao.md)** property to bookmark values in the **BatchCollisions** array, you can move to each record that failed to complete the most recent batch **[Update](recordset2-update-method-dao.md)** operation.</span></span>

<span data-ttu-id="2c132-p102">Depois que os registros da colisão forem corrigidos, um método **Update** do modo de lotes poderá ser chamado novamente. Nesse ponto, o DAO tentará outra atualização em lotes e a propriedade **BatchCollisions** refletirá novamente o conjunto de registros que falharam na segunda tentativa. Quaisquer registros que foram bem-sucedidos na tentativa anterior não serão enviados na tentativa atual, porque agora possuem a propriedade **[RecordStatus](recordset2-recordstatus-property-dao.md)** de **dbRecordUnmodified**. Esse processo poderá continuar enquanto ocorrem colisões ou até que você desista das atualizações e feche o conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="2c132-p102">After the collision records are corrected, a batch-mode **Update** method can be called again. At this point DAO attempts another batch update, and the **BatchCollisions** property again reflects the set of records that failed the second attempt. Any records that succeeded in the previous attempt are not sent in the current attempt, because they now have a **[RecordStatus](recordset2-recordstatus-property-dao.md)** property of **dbRecordUnmodified**. This process can continue as long as collisions occur, or until you abandon the updates and close the result set.</span></span>

## <a name="example"></a><span data-ttu-id="2c132-115">Exemplo</span><span class="sxs-lookup"><span data-stu-id="2c132-115">Example</span></span>

<span data-ttu-id="2c132-116">Este exemplo utiliza a propriedade **BatchCollisionCount** e o método **Update** para demonstrar a atualização em lote em que qualquer colisão é resolvida forçando a atualização em lote.</span><span class="sxs-lookup"><span data-stu-id="2c132-116">This example uses the **BatchCollisionCount** property and the **Update** method to demonstrate batch updating where any collisions are resolved by forcing the batch update.</span></span>

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

