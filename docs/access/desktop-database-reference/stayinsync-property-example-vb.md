---
title: Exemplo da propriedade StayInSync (VB)
TOCTitle: StayInSync property example (VB)
ms:assetid: 1b35f19a-0104-efd5-5222-55f92e08473b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248952(v=office.15)
ms:contentKeyID: 48543535
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 63066000e5e5d8ff9ff1f52ea71cb76beaa2dff8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885423"
---
# <a name="stayinsync-property-example-vb"></a>Exemplo da propriedade StayInSync (VB)


**Aplica-se a**: Access 2013, o Office 2013

Este exemplo demonstra como a propriedade [StayInSync](stayinsync-property-ado.md) facilita o acesso às linhas em um [Recordset](recordset-object-ado.md) hierárquico.

O loop externo exibe o nome e o sobrenome, o estado e a identificação de cada autor. O **Recordset** acrescentado em cada linha é recuperado da coleção [Fields](fields-collection-ado.md) e atribuído automaticamente a **rstTitleAuthor** pela propriedade **StayInSync** sempre que o **Recordset** pai se move para uma nova linha. O loop interno exibe quatro campos a partir de cada linha no conjunto de registros acrescentado.

```vb 
 
'BeginStayInSyncVB 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 'To integrate this code create a DSN called Pubs 
 'with a user_id = sa and no password 
 
 Dim Cnxn As ADODB.Connection 
 Dim rst As ADODB.Recordset 
 Dim rstTitleAuthor As New ADODB.Recordset 
 Dim strCnxn As String 
 
 ' open connection with Data Shape attributes 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider=MSDataShape;Data Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 ' create recordset 
 Set rst = New ADODB.Recordset 
 rst.StayInSync = True 
 rst.Open "SHAPE {select * from Authors} " & _ 
 "APPEND ( { select * from titleauthor} AS chapTitleAuthor " & _ 
 "RELATE au_id TO au_id) ", Cnxn, , , adCmdText 
 
 Set rstTitleAuthor = rst("chapTitleAuthor").Value 
 Do Until rst.EOF 
 Debug.Print rst!au_fname & " " & rst!au_lname & " " & _ 
 rst!State & " " & rst!au_id 
 
 Do Until rstTitleAuthor.EOF 
 Debug.Print rstTitleAuthor(0) & " " & rstTitleAuthor(1) & " " & _ 
 rstTitleAuthor(2) & " " & rstTitleAuthor(3) 
 rstTitleAuthor.MoveNext 
 Loop 
 
 rst.MoveNext 
 Loop 
 
 ' clean up 
 rst.Close 
 Cnxn.Close 
 Set rst = Nothing 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rst Is Nothing Then 
 If rst.State = adStateOpen Then rst.Close 
 End If 
 Set rst = Nothing 
 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndStayInSyncVB 
```

