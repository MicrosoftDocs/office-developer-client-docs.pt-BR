---
title: Parâmetros do objeto Command
TOCTitle: Command object parameters
ms:assetid: b43bb20e-9d0a-b361-6845-d537ae667f0c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249862(v=office.15)
ms:contentKeyID: 48547218
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4be654479ec4e447a77b6c03f8bb1b7ac3616544
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707966"
---
# <a name="command-object-parameters"></a><span data-ttu-id="76092-102">Parâmetros do objeto Command</span><span class="sxs-lookup"><span data-stu-id="76092-102">Command object parameters</span></span>

<span data-ttu-id="76092-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="76092-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="76092-p101">Um uso mais interessante do objeto **Command** é mostrado no exemplo a seguir, no qual o texto do comando SQL foi modificado para incluir parâmetros. Isso permite reutilizar o comando, passando um valor de parâmetro diferente a cada vez. Como a propriedade **Prepared** no objeto **Command** é definida como **True**, o ADO irá requerer que o provedor compile o comando especificado em **CommandText** antes de executá-lo pela primeira vez. Além disso ele irá reter o comando compilado na memória. Isso faz com que a execução do comando seja ligeiramente mais lenta na primeira vez, devido à sobrecarga necessária para prepará-lo, mas resulta em um ganho de desempenho cada vez que o comando é chamado depois disso. Portanto, os comandos devem ser preparados apenas se forem usados mais de uma vez.</span><span class="sxs-lookup"><span data-stu-id="76092-p101">A more interesting use for the **Command** object is shown in the next example, in which the text of the SQL command has been modified to make it parameterized. This makes it possible to reuse the command, passing in a different value for the parameter each time. Because the **Prepared** property on the **Command** object is set equal to **True**, ADO will require the provider to compile the command specified in **CommandText** before executing it for the first time. It also will retain the compiled command in memory. This slows the execution of the command slightly the first time it is executed because of the overhead required to prepare it, but results in a performance gain each time the command is called thereafter. Thus, commands should be prepared only if they will be used more than once.</span></span>

```vb 
 
'BeginManualParamCmd 
 On Error GoTo ErrHandler: 
 
 Dim objConn As New ADODB.Connection 
 Dim objCmd As New ADODB.Command 
 Dim objParm1 As New ADODB.Parameter 
 Dim objRs As New ADODB.Recordset 
 
 ' Set the CommandText as a parameterized SQL query. 
 objCmd.CommandText = "SELECT OrderID, OrderDate, " & _ 
 "RequiredDate, ShippedDate " & _ 
 "FROM Orders " & _ 
 "WHERE CustomerID = ? " & _ 
 "ORDER BY OrderID" 
 objCmd.CommandType = adCmdText 
 
 ' Prepare command since we will be executing it more than once. 
 objCmd.Prepared = True 
 
 ' Create new parameter for CustomerID. Initial value is ALFKI. 
 Set objParm1 = objCmd.CreateParameter("CustId", adChar, _ 
 adParamInput, 5, "ALFKI") 
 objCmd.Parameters.Append objParm1 
 
 ' Connect to the data source. 
 Set objConn = GetNewConnection 
 objCmd.ActiveConnection = objConn 
 
 ' Execute once and display... 
 Set objRs = objCmd.Execute 
 
 Debug.Print objParm1.Value 
 Do While Not objRs.EOF 
 Debug.Print vbTab & objRs(0) & vbTab & objRs(1) & vbTab & _ 
 objRs(2) & vbTab & objRs(3) 
 objRs.MoveNext 
 Loop 
 
 ' ...then set new param value, re-execute command, and display. 
 objCmd("CustId") = "CACTU" 
 Set objRs = objCmd.Execute 
 
 Debug.Print objParm1.Value 
 Do While Not objRs.EOF 
 Debug.Print vbTab & objRs(0) & vbTab & objRs(1) & vbTab & _ 
 objRs(2) & vbTab & objRs(3) 
 objRs.MoveNext 
 Loop 
 
 'clean up 
 objRs.Close 
 objConn.Close 
 Set objRs = Nothing 
 Set objConn = Nothing 
 Set objCmd = Nothing 
 Set objParm1 = Nothing 
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
 Set objParm1 = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
'EndManualParamCmd 
```

<span data-ttu-id="76092-p102">Nem todos os provedores oferecem suporte para comandos preparados. Nesse caso, o provedor poderá retornar um erro assim que essa propriedade for definida como **True**. Se não retornar um erro, o provedor irá ignorar a solicitação para preparar o comando e definirá a propriedade **Prepared** como **False**.</span><span class="sxs-lookup"><span data-stu-id="76092-p102">Not all providers support prepared commands. If the provider does not support command preparation, it might return an error as soon as this property is set to **True**. If it does not return an error, it ignores the request to prepare the command and sets the **Prepared** property to **False**.</span></span>

