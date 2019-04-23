---
title: Comandos nomeados
TOCTitle: Named commands
ms:assetid: 1a4d77e0-1736-83ea-a3c6-f5398c0b01e1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248948(v=office.15)
ms:contentKeyID: 48543518
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 40ce95c5879f5da9615c66d132d6c4847fae1569
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288641"
---
# <a name="named-commands"></a>Comandos nomeados


**Aplica-se ao:** Access 2013, Office 2013

Você pode definir a propriedade **Name** em um objeto **Command** e executar o comando chamando-o como se estivesse em um método no objeto **Command**, da propriedade **ActiveConnection**. Isso é esclarecido no exemplo a seguir, no qual o comando é nomeado *GetCustomers*. Observe que o código passa um objeto **Recordset** declarado e instanciado pelo "método" GetCustomers. Você também pode passar parâmetros para o "método" se forem solicitados pelo **Command**.

```vb 
 
'BeginNamedCmd 
 On Error GoTo ErrHandler: 
 
 Dim objConn As New ADODB.Connection 
 Dim objCmd As New ADODB.Command 
 Dim objRs As New ADODB.Recordset 
 
 ' Connect to the data source. 
 Set objConn = GetNewConnection 
 
 objCmd.CommandText = "SELECT CustomerID, CompanyName FROM Customers" 
 objCmd.CommandType = adCmdText 
 
 'Name the command. 
 objCmd.Name = "GetCustomers" 
 
 objCmd.ActiveConnection = objConn 
 
 ' Execute using Command.Name from the Connection. 
 objConn.GetCustomers objRs 
 
 ' Display. 
 Do While Not objRs.EOF 
 Debug.Print objRs(0) & vbTab & objRs(1) 
 objRs.MoveNext 
 Loop 
 
 'clean up 
 objRs.Close 
 objConn.Close 
 Set objRs = Nothing 
 Set objConn = Nothing 
 Set objCmd = Nothing 
 Exit Sub 
 
ErrHandler: 
 'clean up 
 If objRs.State = adStateOpen Then 
 objRs.Close 
 End If 
 
 If objConn.State = adStateOpen Then 
 objConn.Close 
 End If 
 
 Set objRs = Nothing 
 Set objConn = Nothing 
 Set objCmd = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
'EndNamedCmd 
```

