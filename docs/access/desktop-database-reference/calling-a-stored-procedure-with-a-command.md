---
title: Chamando um procedimento armazenado com um comando
TOCTitle: Calling a Stored Procedure with a Command
ms:assetid: 19d600d7-f717-39df-11a0-951e3ed0f812
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248944(v=office.15)
ms:contentKeyID: 48543509
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 05e68a18ccd97e33416c4603f033fb91acaf0210
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875998"
---
# <a name="calling-a-stored-procedure-with-a-command"></a>Chamando um procedimento armazenado com um comando


**Aplica-se a**: Access 2013, o Office 2013

Você também pode usar um comando ao chamar um procedimento armazenado. O código a seguir chama um procedimento armazenado no banco de dados de exemplo Northwind, chamado CustOrdersOrders, definido como segue:

```vb 
 
CREATE PROCEDURE CustOrdersOrders @CustomerID nchar(5) AS 
SELECT OrderID, OrderDate, RequiredDate, ShippedDate 
FROM Orders 
WHERE CustomerID = @CustomerID 
ORDER BY OrderID 
```

Esse procedimento armazenado é semelhante ao comando usado em [Parâmetros do objeto Command](command-object-parameters.md), por usar um parâmetro de identificação do cliente e retornar informações sobre os pedidos desse cliente. O código a seguir usa esse procedimento armazenado como a fonte de um **Recordset** do ADO.

O uso do procedimento armazenado permite acessar outro recurso do ADO: o método **Refresh** da coleção **Parameters**. Usando esse método, o ADO pode preencher automaticamente todas as informações sobre os parâmetros necessários para o comando em tempo de execução. O desempenho é penalizado quando essa técnica é usada, pois o ADO precisa consultar a fonte de dados para obter as informações sobre os parâmetros.

Existem outras diferenças importantes entre o código a seguir e o código de [Parâmetros do objeto Command](command-object-parameters.md), onde os parâmetros foram inseridos manualmente. Em primeiro lugar, este código não define a propriedade **Prepared** como **True**, pois é um procedimento armazenado do SQL Server e é compilado previamente por definição. Em segundo lugar, a propriedade **CommandType** do objeto **Command** mudou para **adCmdStoredProc**, no segundo exemplo, para informar ao ADO que o comando era um procedimento armazenado.

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

