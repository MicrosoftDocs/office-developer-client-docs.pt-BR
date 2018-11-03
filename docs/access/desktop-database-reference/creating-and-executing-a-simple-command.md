---
title: Criando e executando um comando simples
TOCTitle: Creating and executing a simple command
ms:assetid: 9ace1abe-cfae-0677-bc57-5cbda85b79db
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249699(v=office.15)
ms:contentKeyID: 48546547
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 333f8481958914eadbd830600c08035acc92b031
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947473"
---
# <a name="creating-and-executing-a-simple-command"></a><span data-ttu-id="9fd09-102">Criando e executando um comando simples</span><span class="sxs-lookup"><span data-stu-id="9fd09-102">Creating and executing a simple command</span></span>


<span data-ttu-id="9fd09-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="9fd09-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9fd09-p101">Apesar de não ser uma utilização comum do objeto **Command**, o código a seguir mostra o método básico de utilização do objeto **Command** para executar um comando junto a uma fonte de dados. Nesse caso, trata-se de um comando de retorno de linha, então ele retorna os resultados da execução do comando em um objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="9fd09-p101">Though not a typical usage of the **Command** object, the following code shows the basic method of using the **Command** object to execute a command against a data source. In this case, it is a row-returning command, so it returns the results of the command execution into a **Recordset** object.</span></span>

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

<span data-ttu-id="9fd09-106">O comando a ser executado é especificado com a propriedade **CommandText**.</span><span class="sxs-lookup"><span data-stu-id="9fd09-106">The command to be executed is specified with the **CommandText** property.</span></span>


> [!NOTE]
> <span data-ttu-id="9fd09-107">Vários exemplos desta seção chamam uma função de utilitário, **GetNewConnection**, para estabelecer uma conexão com o provedor de dados.</span><span class="sxs-lookup"><span data-stu-id="9fd09-107">Several examples in this section call a utility function, **GetNewConnection**, to establish a connection with the data provider.</span></span> <span data-ttu-id="9fd09-108">Para evitar a redundância, ela é listada somente uma vez:</span><span class="sxs-lookup"><span data-stu-id="9fd09-108">To avoid redundancy, it is listed only once:</span></span>

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

