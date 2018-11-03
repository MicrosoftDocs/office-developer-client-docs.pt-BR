---
title: Exemplo do método Seek e da propriedade Index (VB)
TOCTitle: Seek method and Index property example (VB)
ms:assetid: c3ddb72c-2b19-53c8-9779-2c503486e44e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249957(v=office.15)
ms:contentKeyID: 48547577
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 41a50e9f115ec308a27a1c7169aaa61a56195dda
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945954"
---
# <a name="seek-method-and-index-property-example-vb"></a>Exemplo do método Seek e da propriedade Index (VB)


**Aplica-se a**: Access 2013, o Office 2013

Este exemplo utiliza o método [Seek](seek-method-ado.md) e a propriedade [Index](index-property-ado.md) do objeto [Recordset](recordset-object-ado.md) em conjunto com um determinado ***Employee ID***, para localizar o nome do funcionário na tabela ***Employees*** do banco de dados Nwind.mdb.

```vb 
 
'BeginSeekVB 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 ' To integrate this code replace the data source 
 ' in the connection string 
 
 'recordset and connection variables 
 Dim rstEmployees As ADODB.Recordset 
 Dim Cnxn As ADODB.Connection 
 Dim strCnxn As String 
 Dim strSQLEmployees As String 
 
 Dim strID As String 
 Dim strPrompt As String 
 strPrompt = "Enter an EmployeeID (e.g., 1 to 9)" 
 
 ' Open connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\Microsoft Office\Office\Samples\northwind.mdb';" 
 Cnxn.Open strCnxn 
 
 ' open recordset server-side for indexing 
 Set rstEmployees = New ADODB.Recordset 
 rstEmployees.CursorLocation = adUseServer 
 strSQLEmployees = "employees" 
 rstEmployees.Open strSQLEmployees, strCnxn, adOpenKeyset, adLockReadOnly, adCmdTableDirect 
 
 ' Does this provider support Seek and Index? 
 If rstEmployees.Supports(adIndex) And rstEmployees.Supports(adSeek) Then 
 rstEmployees.Index = "PrimaryKey" 
 ' Display all the employees 
 rstEmployees.MoveFirst 
 Do While rstEmployees.EOF = False 
 Debug.Print rstEmployees!EmployeeId; ": "; rstEmployees!firstname; " "; _ 
 rstEmployees!LastName 
 rstEmployees.MoveNext 
 Loop 
 
 ' Prompt the user for an EmployeeID between 1 and 9 
 rstEmployees.MoveFirst 
 Do 
 strID = LCase(Trim(InputBox(strPrompt, "Seek Example"))) 
 ' Quit if strID is a zero-length string (CANCEL, null, etc.) 
 If Len(strID) = 0 Then Exit Do 
 If Len(strID) = 1 And strID >= "1" And strID <= "9" Then 
 rstEmployees.Seek Array(strID), adSeekFirstEQ 
 If rstEmployees.EOF Then 
 Debug.Print "Employee not found." 
 Else 
 Debug.Print strID; ": Employee='"; rstEmployees!firstname; " "; _ 
 rstEmployees!LastName; "'" 
 End If 
 End If 
 Loop 
 End If 
 
 ' clean up 
 rstEmployees.Close 
 Cnxn.Close 
 Set rstEmployees = Nothing 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rstEmployees Is Nothing Then 
 If rstEmployees.State = adStateOpen Then rstEmployees.Close 
 End If 
 Set rstEmployees = Nothing 
 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndSeekVB 
```

