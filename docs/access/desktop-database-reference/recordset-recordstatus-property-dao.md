---
title: Propriedade Recordset.RecordStatus (DAO)
TOCTitle: RecordStatus Property
ms:assetid: 6fbd6909-6191-d7be-9a3a-1e9908dacc2b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195591(v=office.15)
ms:contentKeyID: 48545543
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1102617
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ada7c1dfa4b71a0f455a4e596de1bd4a037d5d59
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464255"
---
# <a name="recordsetrecordstatus-property-dao"></a><span data-ttu-id="e2ff4-102">Propriedade Recordset.RecordStatus (DAO)</span><span class="sxs-lookup"><span data-stu-id="e2ff4-102">Recordset.RecordStatus Property (DAO)</span></span>


<span data-ttu-id="e2ff4-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e2ff4-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="e2ff4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e2ff4-104">Syntax</span></span>

<span data-ttu-id="e2ff4-105">*expressão* . RecordStatus</span><span class="sxs-lookup"><span data-stu-id="e2ff4-105">*expression* .RecordStatus</span></span>

<span data-ttu-id="e2ff4-106">*expressão* Uma variável que representa um objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="e2ff4-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2ff4-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="e2ff4-107">Remarks</span></span>

<span data-ttu-id="e2ff4-108">O valor da propriedade **RecordStatus** indica se e como o registro atual será envolvido na próxima atualização em lotes otimista.</span><span class="sxs-lookup"><span data-stu-id="e2ff4-108">The value of the **RecordStatus** property indicates whether and how the current record will be involved in the next optimistic batch update.</span></span>

<span data-ttu-id="e2ff4-p101">Quando um usuário alterar um registro, a propriedade **RecordStatus** desse registro será alterada automaticamente para **dbRecordModified**. De forma similar, caso um registro seja adicionado ou excluído, **RecordStatus** refletirá uma constante adequada. Mais tarde, quando você usar um método **[Update](recordset-update-method-dao.md)** do modo em lotes, o DAO submeterá uma operação adequada para o servidor remoto para cada registro, com base na propriedade **RecordStatus** do registro.</span><span class="sxs-lookup"><span data-stu-id="e2ff4-p101">When a user changes a record, the **RecordStatus** for that record automatically changes to **dbRecordModified**. Similarly, if a record is added or deleted, **RecordStatus** reflects the appropriate constant. When you then use a batch-mode **[Update](recordset-update-method-dao.md)** method, DAO will submit an appropriate operation to the remote server for each record, based on the record's **RecordStatus** property.</span></span>

## <a name="example"></a><span data-ttu-id="e2ff4-112">Exemplo</span><span class="sxs-lookup"><span data-stu-id="e2ff4-112">Example</span></span>

<span data-ttu-id="e2ff4-p102">Este exemplo usa as propriedades **RecordStatus** e **DefaultCursorDriver** para mostrar como as alterações de um **Recordset** local são controladas durante a atualização em lotes. A função RecordStatusOutput é necessária para executar esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="e2ff4-p102">This example uses the **RecordStatus** and **DefaultCursorDriver** properties to show how changes to a local **Recordset** are tracked during batch updating. The RecordStatusOutput function is required for this procedure to run.</span></span>

```vb 
Sub RecordStatusX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim rstTemp As Recordset 
 
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

