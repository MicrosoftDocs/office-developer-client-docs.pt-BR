---
title: Propriedade Recordset.BatchCollisionCount (DAO)
TOCTitle: BatchCollisionCount Property
ms:assetid: 9d166463-8313-c0f5-8389-5d5ad933eb33
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198240(v=office.15)
ms:contentKeyID: 48546617
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101181
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: d0c4af9744accd21a91dca2676a08cad3d1cc7e7
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711935"
---
# <a name="recordsetbatchcollisioncount-property-dao"></a><span data-ttu-id="2d3aa-102">Propriedade Recordset.BatchCollisionCount (DAO)</span><span class="sxs-lookup"><span data-stu-id="2d3aa-102">Recordset.BatchCollisionCount property (DAO)</span></span>


<span data-ttu-id="2d3aa-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="2d3aa-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="2d3aa-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2d3aa-104">Syntax</span></span>

<span data-ttu-id="2d3aa-105">*expressão* . BatchCollisionCount</span><span class="sxs-lookup"><span data-stu-id="2d3aa-105">*expression* .BatchCollisionCount</span></span>

<span data-ttu-id="2d3aa-106">*expressão* Uma variável que representa um objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="2d3aa-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d3aa-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="2d3aa-107">Remarks</span></span>

<span data-ttu-id="2d3aa-p101">Essa propriedade indica quantos registros encontraram colisões ou, por outro lado, tiveram falhas na atualização durante a última tentativa de atualização em lote. O valor dessa propriedade corresponde ao número de indicadores na propriedade **[BatchCollisions](recordset-batchcollisions-property-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="2d3aa-p101">This property indicates how many records encountered collisions or otherwise failed to update during the last batch update attempt. The value of this property corresponds to the number of bookmarks in the **[BatchCollisions](recordset-batchcollisions-property-dao.md)** property.</span></span>

<span data-ttu-id="2d3aa-110">Se você definir trabalhar com a propriedade **[Bookmark](recordset-object-dao.md)** do objeto **[Recordset](recordset-bookmark-property-dao.md)** para indicar valores na matriz **BatchCollisions**, poderá mover-se para cada registro com falha para concluir a operação **[Update](recordset-update-method-dao.md)** mais recente no modo em lote.</span><span class="sxs-lookup"><span data-stu-id="2d3aa-110">If you set the working **[Recordset](recordset-object-dao.md)** object's **[Bookmark](recordset-bookmark-property-dao.md)** property to bookmark values in the **BatchCollisions** array, you can move to each record that failed to complete the most recent batch **[Update](recordset-update-method-dao.md)** operation.</span></span>

<span data-ttu-id="2d3aa-p102">Depois que os registros de colisão são corrigidos, você pode chamar novamente o método **Update** no modo em lote. Nesse momento, o DAO tenta outra atualização em lote, e a propriedade **BatchCollisions** reflete novamente o conjunto de registros que falharam na segunda tentativa. Os registros bem-sucedidos na tentativa anterior não são enviados para a tentativa atual, pois eles têm agora uma propriedade **[RecordStatus](recordset-recordstatus-property-dao.md)** de dbRecordUnmodified. Esse processo pode continuar até não haver mais colisões ou até você parar as atualizações e fechar a definição de resultados.</span><span class="sxs-lookup"><span data-stu-id="2d3aa-p102">After the collision records are corrected, a batch-mode **Update** method can be called again. At this point DAO attempts another batch update, and the **BatchCollisions** property again reflects the set of records that failed the second attempt. Any records that succeeded in the previous attempt are not sent in the current attempt, because they now have a **[RecordStatus](recordset-recordstatus-property-dao.md)** property of dbRecordUnmodified. This process can continue as long as collisions occur, or until you abandon the updates and close the result set.</span></span>

## <a name="example"></a><span data-ttu-id="2d3aa-115">Exemplo</span><span class="sxs-lookup"><span data-stu-id="2d3aa-115">Example</span></span>

<span data-ttu-id="2d3aa-116">Este exemplo utiliza a propriedade **BatchCollisionCount** e o método **Update** para demonstrar a atualização em lote em que qualquer colisão é resolvida forçando a atualização em lote.</span><span class="sxs-lookup"><span data-stu-id="2d3aa-116">This example uses the **BatchCollisionCount** property and the **Update** method to demonstrate batch updating where any collisions are resolved by forcing the batch update.</span></span>

```vb 
Sub BatchX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim rstTemp As Recordset 
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

