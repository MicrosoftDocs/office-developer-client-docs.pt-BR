---
title: Criando e executando um comando simples
TOCTitle: Creating and Executing a Simple Command
ms:assetid: 9ace1abe-cfae-0677-bc57-5cbda85b79db
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249699(v=office.15)
ms:contentKeyID: 48546547
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 91355c8b24fcd6e797a6610524076b8850b16f57
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462169"
---
# <a name="creating-and-executing-a-simple-command"></a>Criando e executando um comando simples


**Aplica-se a**: Access 2013 | Office 2013

Apesar de não ser uma utilização comum do objeto **Command**, o código a seguir mostra o método básico de utilização do objeto **Command** para executar um comando junto a uma fonte de dados. Nesse caso, trata-se de um comando de retorno de linha, então ele retorna os resultados da execução do comando em um objeto **Recordset**.

```vb 
 
 'BeginBasicCmd 
 On Error GoTo ErrHandler: 
 
 Dim objConn As New ADODB.Connection 
 Dim objCmd As New ADODB.Command 
 Dim objRs As New ADODB.Recordset 
 
 objCmd.CommandText = "SELECT OrderID, OrderDate, " & _ 
 "RequiredDate, ShippedDate " & _ 
 "FROM Orders " & _ 
 "WHERE CustomerID = 'ALFKI' " & _ 
 "ORDER BY OrderID" 
 objCmd.CommandType = adCmdText 
 
 ' Connect to the data source. 
 Set objConn = GetNewConnection 
 objCmd.ActiveConnection = objConn 
 
 ' Execute once and display... 
 Set objRs = objCmd.Execute 
 
 Debug.Print "ALFKI" 
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
'EndBasicCmd 
```

O comando a ser executado é especificado com a propriedade **CommandText**.


> [!NOTE]
> <P>[!OBSERVAçãO] Vários exemplos dessa seção chamam a função utilitária GetNewConnection para estabelecer uma conexão com o provedor de dados. Para evitar redundância, ela será listada apenas uma vez aqui:</P>



```vb 
 
'BeginNewConnection 
Private Function GetNewConnection() As ADODB.Connection 
 Dim oCn As New ADODB.Connection 
 Dim sCnStr As String 
 
 sCnStr = "Provider='SQLOLEDB';Data Source='MySqlServer';" & _ 
 "Integrated Security='SSPI';Database='Northwind';" 
 oCn.Open sCnStr 
 
 If oCn.State = adStateOpen Then 
 Set GetNewConnection = oCn 
 End If 
 
End Function 
'EndNewConnection 
```
