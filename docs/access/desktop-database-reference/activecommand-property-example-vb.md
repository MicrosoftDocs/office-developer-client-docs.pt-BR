---
title: Exemplo da propriedade ActiveCommand (VB)
TOCTitle: ActiveCommand property example (VB)
ms:assetid: 831032cb-d557-aa98-5637-07bad65f924a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249569(v=office.15)
ms:contentKeyID: 48545999
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 32ab8ba94570c98da03c3effc484490c327fd0a9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282597"
---
# <a name="activecommand-property-example-vb"></a>Exemplo da propriedade ActiveCommand (VB)


**Aplica-se ao:** Access 2013, Office 2013

Este exemplo demonstra a propriedade [ActiveCommand](activecommand-property-ado.md).

Uma sub-rotina recebe um objeto [Recordset](recordset-object-ado.md) cuja propriedade **ActiveCommand** é utilizada para exibir o texto do comando e o parâmetro que criaram o **Recordset**.

```vb 
 
'BeginActiveCommandVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 'recordset and connection variables 
 Dim cmd As ADODB.Command 
 Dim rst As ADODB.Recordset 
 Dim Cnxn As ADODB.Connection 
 Dim strCnxn As String 
 'record variables 
 Dim strPrompt As String 
 Dim strName As String 
 
 Set Cnxn = New ADODB.Connection 
 Set cmd = New ADODB.Command 
 
 strPrompt = "Enter an author's name (e.g., Ringer): " 
 strName = Trim(InputBox(strPrompt, "ActiveCommandX Example")) 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 
 'create SQL command string 
 cmd.CommandText = "SELECT * FROM Authors WHERE au_lname = ?" 
 cmd.Parameters.Append cmd.CreateParameter("LastName", adChar, adParamInput, 20, strName) 
 
 Cnxn.Open strCnxn 
 cmd.ActiveConnection = Cnxn 
 
 'create the recordset by executing command string 
 Set rst = cmd.Execute(, , adCmdText) 
 'see the results 
 Call ActiveCommandXprint(rst) 
 
 ' clean up 
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
'EndActiveCommandVB 
```

A rotina **ActiveCommandXprint** recebe apenas um objeto **Recordset**, ainda assim ela deve imprimir o texto do comando e o parâmetro que criaram o **Recordset**. Isso pode ser feito porque a propriedade **ActiveCommand** do objeto **Recordset** produz o objeto [Command](command-object-ado.md) associado.

A propriedade [CommandText](commandtext-property-ado.md) do objeto **Command** produz o comando com parâmetros que criou o **Recorset**. A coleção [Parameters](parameters-collection-ado.md) do objeto **Command** produz o valor que foi substituído pelo espaço reservado do parâmetro do comando ("**?**").

Finalmente, uma mensagem de erro ou o nome e a ID do autor são impressos.

```vb 
 
'BeginActiveCommandPrintVB 
Public Sub ActiveCommandXprint(rstp As ADODB.Recordset) 
 
 Dim strName As String 
 
 strName = rstp.ActiveCommand.Parameters.Item("LastName").Value 
 
 Debug.Print "Command text = '"; rstp.ActiveCommand.CommandText; "'" 
 Debug.Print "Parameter = '"; strName; "'" 
 
 If rstp.BOF = True Then 
 Debug.Print "Name = '"; strName; "', not found." 
 Else 
 Debug.Print "Name = '"; rstp!au_fname; " "; rstp!au_lname; _ 
 "', author ID = '"; rstp!au_id; "'" 
 End If 
 
 rstp.Close 
 Set rstp = Nothing 
End Sub 
'EndActiveCommandPrintVB 
```

