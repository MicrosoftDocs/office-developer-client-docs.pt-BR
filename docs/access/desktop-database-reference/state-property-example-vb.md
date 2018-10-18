---
<span data-ttu-id="4f49b-101"><<<<<<< Título cabeça: TOCTitle de exemplo da propriedade de estado (VB): exemplo de propriedade de estado (VB) === título: exemplo da propriedade estado (VB) TOCTitle: exemplo da propriedade estado (VB)</span><span class="sxs-lookup"><span data-stu-id="4f49b-101"><<<<<<< HEAD title: State Property Example (VB) TOCTitle: State Property Example (VB) ======= title: State property example (VB) TOCTitle: State property example (VB)</span></span>
>>>>>>> <span data-ttu-id="4f49b-102">ms:assetid de mestre: e5a9abc6-9be7-5b70-a2da-9b678b3a8421 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250166(v=office.15) ms:contentKeyID: ms.date 48548366: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="4f49b-102">master ms:assetid: e5a9abc6-9be7-5b70-a2da-9b678b3a8421 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250166(v=office.15) ms:contentKeyID: 48548366 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="4f49b-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="4f49b-103"><<<<<<< HEAD</span></span>
# <a name="state-property-example-vb"></a><span data-ttu-id="4f49b-104">Exemplo da propriedade State (VB)</span><span class="sxs-lookup"><span data-stu-id="4f49b-104">State Property Example (VB)</span></span>
=======
# <a name="state-property-example-vb"></a><span data-ttu-id="4f49b-105">Exemplo da propriedade State (VB)</span><span class="sxs-lookup"><span data-stu-id="4f49b-105">State property example (VB)</span></span>
>>>>>>> <span data-ttu-id="4f49b-106">mestre</span><span class="sxs-lookup"><span data-stu-id="4f49b-106">master</span></span>


<span data-ttu-id="4f49b-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="4f49b-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="4f49b-108">Este exemplo utiliza a propriedade [State](state-property-ado.md) para exibir uma mensagem enquanto conexões assíncronas estiverem sendo abertas e comandos assíncronos estiverem sendo executados.</span><span class="sxs-lookup"><span data-stu-id="4f49b-108">This example uses the [State](state-property-ado.md) property to display a message while asynchronous connections are opening and asynchronous commands are executing.</span></span>

```vb 
 
'BeginStateVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 Dim Cnxn1 As ADODB.Connection 
 Dim Cnxn2 As ADODB.Connection 
 Dim cmdChange As ADODB.Command 
 Dim cmdRestore As ADODB.Command 
 Dim strCnxn As String 
 Dim strSQL As String 
 
 ' Open two asynchronous connections, displaying 
 ' a message while connecting 
 Set Cnxn1 = New ADODB.Connection 
 Set Cnxn2 = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 
 Cnxn1.Open strCnxn, , , adAsyncConnect 
 Do Until Cnxn1.State <> adStateConnecting 
 Debug.Print "Opening first connection...." 
 Loop 
 
 Cnxn2.Open strCnxn, , , adAsyncConnect 
 Do Until Cnxn2.State <> adStateConnecting 
 Debug.Print "Opening second connection...." 
 Loop 
 
 ' Create two command objects 
 Set cmdChange = New ADODB.Command 
 cmdChange.ActiveConnection = Cnxn1 
 strSQL = "UPDATE Titles SET type = 'self_help' WHERE type = 'psychology'" 
 cmdChange.CommandText = strSQL 
 
 Set cmdRestore = New ADODB.Command 
 cmdRestore.ActiveConnection = Cnxn2 
 strSQL = "UPDATE Titles SET type = 'psychology' WHERE type = 'self_help'" 
 cmdRestore.CommandText = strSQL 
 
 ' Executing the commands, displaying a message 
 ' while they are executing 
 cmdChange.Execute , , adAsyncExecute 
 Do Until cmdChange.State <> adStateExecuting 
 Debug.Print "Change command executing...." 
 Loop 
 
 cmdRestore.Execute , , adAsyncExecute 
 Do Until cmdRestore.State <> adStateExecuting 
 Debug.Print "Restore command executing...." 
 Loop 
 
 ' clean up 
 Cnxn1.Close 
 Cnxn2.Close 
 Set Cnxn1 = Nothing 
 Set Cnxn2 = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not Cnxn1 Is Nothing Then 
 If Cnxn1.State = adStateOpen Then Cnxn1.Close 
 End If 
 Set Cnxn1 = Nothing 
 
 If Not Cnxn2 Is Nothing Then 
 If Cnxn2.State = adStateOpen Then Cnxn2.Close 
 End If 
 Set Cnxn2 = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndStateVB 
```

