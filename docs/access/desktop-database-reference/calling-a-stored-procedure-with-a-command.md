---
title: Chamada de um procedimento armazenado com um comando
TOCTitle: Calling a stored procedure with a command
ms:assetid: 19d600d7-f717-39df-11a0-951e3ed0f812
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248944(v=office.15)
ms:contentKeyID: 48543509
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6578dbfc50ae8ffeaa31f49b694b37ba5fd534e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296707"
---
# <a name="calling-a-stored-procedure-with-a-command"></a><span data-ttu-id="963f4-102">Chamada de um procedimento armazenado com um comando</span><span class="sxs-lookup"><span data-stu-id="963f4-102">Calling a stored procedure with a command</span></span>


<span data-ttu-id="963f4-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="963f4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="963f4-p101">Você também pode usar um comando ao chamar um procedimento armazenado. O código a seguir chama um procedimento armazenado no banco de dados de exemplo Northwind, chamado CustOrdersOrders, definido como segue:</span><span class="sxs-lookup"><span data-stu-id="963f4-p101">You can also use a command when calling a stored procedure. The following code calls a stored procedure in the Northwind sample database, called CustOrdersOrders, which is defined as follows:</span></span>

```vb 
 
CREATE PROCEDURE CustOrdersOrders @CustomerID nchar(5) AS 
SELECT OrderID, OrderDate, RequiredDate, ShippedDate 
FROM Orders 
WHERE CustomerID = @CustomerID 
ORDER BY OrderID 
```

<span data-ttu-id="963f4-p102">Esse procedimento armazenado é semelhante ao comando usado em [Parâmetros do objeto Command](command-object-parameters.md), por usar um parâmetro de identificação do cliente e retornar informações sobre os pedidos desse cliente. O código a seguir usa esse procedimento armazenado como a fonte de um **Recordset** do ADO.</span><span class="sxs-lookup"><span data-stu-id="963f4-p102">This stored procedure is similar to the command used in [Command Object Parameters](command-object-parameters.md), in that it takes a customer ID parameter and returns information about that customer's orders. The code below uses this stored procedure as the source for an ADO **Recordset**.</span></span>

<span data-ttu-id="963f4-p103">O uso do procedimento armazenado permite acessar outro recurso do ADO: o método **Refresh** da coleção **Parameters**. Usando esse método, o ADO pode preencher automaticamente todas as informações sobre os parâmetros necessários para o comando em tempo de execução. O desempenho é penalizado quando essa técnica é usada, pois o ADO precisa consultar a fonte de dados para obter as informações sobre os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="963f4-p103">Using the stored procedure allows you to access another capability of ADO: the **Parameters** collection **Refresh** method. By using this method, ADO can automatically fill in all information about the parameters required by the command at run time. There is a performance penalty in using this technique, because ADO must query the data source for the information about the parameters.</span></span>

<span data-ttu-id="963f4-p104">Existem outras diferenças importantes entre o código a seguir e o código de [Parâmetros do objeto Command](command-object-parameters.md), onde os parâmetros foram inseridos manualmente. Em primeiro lugar, este código não define a propriedade **Prepared** como **True**, pois é um procedimento armazenado do SQL Server e é compilado previamente por definição. Em segundo lugar, a propriedade **CommandType** do objeto **Command** mudou para **adCmdStoredProc**, no segundo exemplo, para informar ao ADO que o comando era um procedimento armazenado.</span><span class="sxs-lookup"><span data-stu-id="963f4-p104">Other important differences exist between the code below and the code in [Command Object Parameters](command-object-parameters.md), where the parameters were entered manually. First, this code does not set the **Prepared** property to **True** because it is a SQL Server stored procedure and is precompiled by definition. Second, the **CommandType** property of the **Command** object changed to **adCmdStoredProc** in the second example to inform ADO that the command was a stored procedure.</span></span>

```vb 
 
'BeginAutoParamCmd 
 On Error GoTo ErrHandler: 
 
 Dim objConn As New ADODB.Connection 
 Dim objCmd As New ADODB.Command 
 Dim objParm1 As New ADODB.Parameter 
 Dim objRs As New ADODB.Recordset 
 
 ' Set CommandText equal to the stored procedure name. 
 objCmd.CommandText = "CustOrdersOrders" 
 objCmd.CommandType = adCmdStoredProc 
 
 ' Connect to the data source. 
 Set objConn = GetNewConnection 
 objCmd.ActiveConnection = objConn 
 
 ' Automatically fill in parameter info from stored procedure. 
 objCmd.Parameters.Refresh 
 
 ' Set the param value. 
 objCmd(1) = "ALFKI" 
 
 ' Execute once and display... 
 Set objRs = objCmd.Execute 
 
 Debug.Print objParm1.Value 
 Do While Not objRs.EOF 
 Debug.Print vbTab & objRs(0) & vbTab & objRs(1) & vbTab & _ 
 objRs(2) & vbTab & objRs(3) 
 objRs.MoveNext 
 Loop 
 
 ' ...then set new param value, re-execute command, and display. 
 objCmd(1) = "CACTU" 
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
'EndAutoParamCmd 
```

