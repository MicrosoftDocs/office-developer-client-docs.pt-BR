---
title: Comandos nomeados
TOCTitle: Named Commands
ms:assetid: 1a4d77e0-1736-83ea-a3c6-f5398c0b01e1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248948(v=office.15)
ms:contentKeyID: 48543518
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 940e0ace8577e6fdb7dc01daf3cd67320dfbf18c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25461972"
---
# <a name="named-commands"></a><span data-ttu-id="5a7e3-102">Comandos nomeados</span><span class="sxs-lookup"><span data-stu-id="5a7e3-102">Named Commands</span></span>


<span data-ttu-id="5a7e3-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5a7e3-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5a7e3-p101">Você pode definir a propriedade **Name** em um objeto **Command** e executar o comando chamando-o como se estivesse em um método no objeto **Command**, da propriedade **ActiveConnection**. Isso é esclarecido no exemplo a seguir, no qual o comando é nomeado *GetCustomers*. Observe que o código passa um objeto **Recordset** declarado e instanciado pelo "método" GetCustomers. Você também pode passar parâmetros para o "método" se forem solicitados pelo **Command**.</span><span class="sxs-lookup"><span data-stu-id="5a7e3-p101">You can set the **Name** property on a **Command** object and then execute the command by calling it as if it were a method on the **Command** object **ActiveConnection** property. This is illustrated in the following example, in which the command is named *GetCustomers*. Notice that the code passes in a declared and instantiated **Recordset** object to the GetCustomers "method." You can also pass in parameters to the "method" if they are required by the **Command**.</span></span>

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

