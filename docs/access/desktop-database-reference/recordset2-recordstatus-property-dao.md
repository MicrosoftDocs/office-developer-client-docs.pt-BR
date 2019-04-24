---
title: Propriedade Recordset2. RecordStatus (DAO)
TOCTitle: RecordStatus Property
ms:assetid: 178872a9-e361-f277-627d-f91b01ceb6d1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845575(v=office.15)
ms:contentKeyID: 48543451
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ae3dc5ba640b4b24a7400fc9e467978777ef6fcc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309363"
---
# <a name="recordset2recordstatus-property-dao"></a><span data-ttu-id="e38d0-102">Propriedade Recordset2. RecordStatus (DAO)</span><span class="sxs-lookup"><span data-stu-id="e38d0-102">Recordset2.RecordStatus property (DAO)</span></span>


<span data-ttu-id="e38d0-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e38d0-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="e38d0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e38d0-104">Syntax</span></span>

<span data-ttu-id="e38d0-105">*expressão* . RecordStatus</span><span class="sxs-lookup"><span data-stu-id="e38d0-105">*expression* .RecordStatus</span></span>

<span data-ttu-id="e38d0-106">*expressão* Uma variável que representa um objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="e38d0-106">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e38d0-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="e38d0-107">Remarks</span></span>

<span data-ttu-id="e38d0-108">O valor da propriedade **RecordStatus** indica se e como o registro atual será envolvido na próxima atualização em lotes otimista.</span><span class="sxs-lookup"><span data-stu-id="e38d0-108">The value of the **RecordStatus** property indicates whether and how the current record will be involved in the next optimistic batch update.</span></span>

<span data-ttu-id="e38d0-p101">Quando um usuário alterar um registro, a propriedade **RecordStatus** desse registro será alterada automaticamente para **dbRecordModified**. De forma similar, caso um registro seja adicionado ou excluído, **RecordStatus** refletirá uma constante adequada. Mais tarde, quando você usar um método **[Update](recordset2-update-method-dao.md)** do modo em lotes, o DAO submeterá uma operação adequada para o servidor remoto para cada registro, com base na propriedade **RecordStatus** do registro.</span><span class="sxs-lookup"><span data-stu-id="e38d0-p101">When a user changes a record, the **RecordStatus** for that record automatically changes to **dbRecordModified**. Similarly, if a record is added or deleted, **RecordStatus** reflects the appropriate constant. When you then use a batch-mode **[Update](recordset2-update-method-dao.md)** method, DAO will submit an appropriate operation to the remote server for each record, based on the record's **RecordStatus** property.</span></span>

## <a name="example"></a><span data-ttu-id="e38d0-112">Exemplo</span><span class="sxs-lookup"><span data-stu-id="e38d0-112">Example</span></span>

<span data-ttu-id="e38d0-p102">Este exemplo usa as propriedades **RecordStatus** e **DefaultCursorDriver** para mostrar como as alterações para um **Recordset** local são controladas durante uma atualização em lote. A função RecordStatusOutput é exigida para que este procedimento seja executado.</span><span class="sxs-lookup"><span data-stu-id="e38d0-p102">This example uses the **RecordStatus** and **DefaultCursorDriver** properties to show how changes to a local **Recordset** are tracked during batch updating. The RecordStatusOutput function is required for this procedure to run.</span></span>

```vb 
Sub RecordStatusX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim rstTemp As Recordset2 
 
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
 ' batch updating. 
 Set rstTemp = conMain.OpenRecordset( _ 
 "SELECT * FROM authors", dbOpenDynaset, 0, _ 
 dbOptimisticBatch) 
 
 With rstTemp 
 .MoveFirst 
 Debug.Print "Original record: " & !au_lname 
 Debug.Print , RecordStatusOutput2(.RecordStatus) 
 
 .Edit 
 !au_lname = "Bowen" 
 .Update 
 Debug.Print "Edited record: " & !au_lname 
 Debug.Print , RecordStatusOutput2(.RecordStatus) 
 
 .AddNew 
 !au_lname = "NewName" 
 .Update 
 Debug.Print "New record: " & !au_lname 
 Debug.Print , RecordStatusOutput2(.RecordStatus) 
 
 .Delete 
 Debug.Print "Deleted record: " & !au_lname 
 Debug.Print , RecordStatusOutput2(.RecordStatus) 
 
 ' Close the local recordset without updating the 
 ' data on the server. 
 .Close 
 End With 
 
 conMain.Close 
 wrkMain.Close 
 
End Sub 
 
Function RecordStatusOutput(lngTemp As Long) As String 
 
 Dim strTemp As String 
 
 strTemp = "" 
 
 ' Construct an output string based on the RecordStatus 
 ' value. 
If lngTemp = dbRecordUnmodified Then _ 
 strTemp = "[dbRecordUnmodified]" 
 If lngTemp = dbRecordModified Then _ 
 strTemp = "[dbRecordModified]" 
 If lngTemp = dbRecordNew Then _ 
 strTemp = "[dbRecordNew]" 
 If lngTemp = dbRecordDeleted Then _ 
 strTemp = "[dbRecordDeleted]" 
 If lngTemp = dbRecordDBDeleted Then _ 
 strTemp = "[dbRecordDBDeleted]" 
 
 RecordStatusOutput = strTemp 
 
End Function 
 
```

