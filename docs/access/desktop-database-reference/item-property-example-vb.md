---
title: Exemplo da propriedade Item (VB)
TOCTitle: Item property example (VB)
ms:assetid: e8d17560-8a0d-7045-d8dc-728a85037c0d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250179(v=office.15)
ms:contentKeyID: 48548430
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: df39d66db67652c840980aa01e15cd39a437bc48
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290912"
---
# <a name="item-property-example-vb"></a>Exemplo da propriedade Item (VB)


**Aplica-se ao:** Access 2013, Office 2013

Este exemplo demonstra como a propriedade [Item](item-property-ado.md) acessa membros de uma coleção. O exemplo abre a tabela ***Authors*** do banco de dados ***Pubs*** com um comando parametrizado.

O parâmetro no comando emitido com relação ao banco de dados é acessado a partir da coleção [Parameters](command-object-ado.md) do objeto [Command](parameters-collection-ado.md) por índice e nome. Os campos do [Recordset](recordset-object-ado.md) retornado são então acessados a partir da coleção [Fields](fields-collection-ado.md) desse objeto por índice e nome.

```vb 
 
'BeginItemVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 Dim Cnxn As ADODB.Connection 
 Dim rstAuthors As ADODB.Recordset 
 Dim cmd As ADODB.Command 
 Dim prm As ADODB.Parameter 
 Dim fld As ADODB.Field 
 Dim strCnxn As String 
 
 Dim ix As Integer 
 Dim limit As Long 
 Dim Column(0 To 8) As Variant 
 
 Set Cnxn = New ADODB.Connection 
 Set rstAuthors = New ADODB.Recordset 
 Set cmd = New ADODB.Command 
 
 'Set the array with the Authors table field (column) names 
 Column(0) = "au_id" 
 Column(1) = "au_lname" 
 Column(2) = "au_fname" 
 Column(3) = "phone" 
 Column(4) = "address" 
 Column(5) = "city" 
 Column(6) = "state" 
 Column(7) = "zip" 
 Column(8) = "contract" 
 
 cmd.CommandText = "SELECT * FROM Authors WHERE state = ?" 
 Set prm = cmd.CreateParameter("ItemXparm", adChar, adParamInput, 2, "CA") 
 cmd.Parameters.Append prm 
 ' set connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 cmd.ActiveConnection = Cnxn 
 ' open recordset 
 rstAuthors.Open cmd, , adOpenStatic, adLockReadOnly 
 'Connection and CommandType are omitted because 
 'a Command object is provided 
 
 Debug.Print "The Parameters collection accessed by index..." 
 Set prm = cmd.Parameters.Item(0) 
 Debug.Print "Parameter name = '"; prm.Name; "', value = '"; prm.Value; "'" 
 Debug.Print 
 
 Debug.Print "The Parameters collection accessed by name..." 
 Set prm = cmd.Parameters.Item("ItemXparm") 
 Debug.Print "Parameter name = '"; prm.Name; "', value = '"; prm.Value; "'" 
 Debug.Print 
 
 Debug.Print "The Fields collection accessed by index..." 
 
 rstAuthors.MoveFirst 
 limit = rstAuthors.Fields.Count - 1 
 For ix = 0 To limit 
 Set fld = rstAuthors.Fields.Item(ix) 
 Debug.Print "Field "; ix; ": Name = '"; fld.Name; _ 
 "', Value = '"; fld.Value; "'" 
 Next ix 
 
 Debug.Print 
 
 Debug.Print "The Fields collection accessed by name..." 
 
 rstAuthors.MoveFirst 
 For ix = 0 To 8 
 Set fld = rstAuthors.Fields.Item(Column(ix)) 
 Debug.Print "Field name = '"; fld.Name; "', Value = '"; fld.Value; "'" 
 Next ix 
 
 ' clean up 
 rstAuthors.Close 
 Cnxn.Close 
 Set rstAuthors = Nothing 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rstAuthors Is Nothing Then 
 If rstAuthors.State = adStateOpen Then rstAuthors.Close 
 End If 
 Set rstAuthors = Nothing 
 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 Set cmd = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
 
End Sub 
'EndItemVB 
```

