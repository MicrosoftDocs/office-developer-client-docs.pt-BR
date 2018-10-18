---
<span data-ttu-id="25a61-101"><<<<<<< Título cabeça: exemplo de propriedade MaxRecords (VB) TOCTitle: exemplo de propriedade MaxRecords (VB) === título: exemplo da propriedade MaxRecords (VB) TOCTitle: exemplo da propriedade MaxRecords (VB)</span><span class="sxs-lookup"><span data-stu-id="25a61-101"><<<<<<< HEAD title: MaxRecords Property Example (VB) TOCTitle: MaxRecords Property Example (VB) ======= title: MaxRecords property example (VB) TOCTitle: MaxRecords property example (VB)</span></span>
>>>>>>> <span data-ttu-id="25a61-102">ms:assetid de mestre: e0b21025-3494-81a7-d656-03b85b0102d2 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250142(v=office.15) ms:contentKeyID: ms.date 48548241: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="25a61-102">master ms:assetid: e0b21025-3494-81a7-d656-03b85b0102d2 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250142(v=office.15) ms:contentKeyID: 48548241 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="25a61-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="25a61-103"><<<<<<< HEAD</span></span>
# <a name="maxrecords-property-example-vb"></a><span data-ttu-id="25a61-104">Exemplo da propriedade MaxRecords (VB)</span><span class="sxs-lookup"><span data-stu-id="25a61-104">MaxRecords Property Example (VB)</span></span>
=======
# <a name="maxrecords-property-example-vb"></a><span data-ttu-id="25a61-105">Exemplo da propriedade MaxRecords (VB)</span><span class="sxs-lookup"><span data-stu-id="25a61-105">MaxRecords property example (VB)</span></span>
>>>>>>> <span data-ttu-id="25a61-106">mestre</span><span class="sxs-lookup"><span data-stu-id="25a61-106">master</span></span>


<span data-ttu-id="25a61-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="25a61-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="25a61-108">Este exemplo usa a propriedade [MaxRecords](maxrecords-property-ado.md) para abrir um [Recordset](recordset-object-ado.md) contendo os 10 títulos mais caros da tabela ***Titles***.</span><span class="sxs-lookup"><span data-stu-id="25a61-108">This example uses the [MaxRecords](maxrecords-property-ado.md) property to open a [Recordset](recordset-object-ado.md) containing the 10 most expensive titles in the ***Titles*** table.</span></span>

```vb 
 
'BeginMaxRecordsVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 Dim rstTitles As ADODB.Recordset 
 Dim Cnxn As ADODB.Connection 
 Dim strCnxn As String 
 Dim strSQLTitles As String 
 
 ' Open a connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 ' Open recordset containing the 10 most expensive 
 ' titles in the Titles table 
 Set rstTitles = New ADODB.Recordset 
 rstTitles.MaxRecords = 10 
 
 strSQLTitles = "SELECT Title, Price FROM Titles ORDER BY Price DESC" 
 rstTitles.Open strSQLTitles, strCnxn, adOpenStatic, adLockReadOnly, adCmdText 
 
 ' Display the contents of the recordset 
 Debug.Print "Top Ten Titles by Price:" 
 
 Do Until rstTitles.EOF 
 Debug.Print " " & rstTitles!Title & " - " & rstTitles!Price 
 rstTitles.MoveNext 
 Loop 
 
 ' clean up 
 rstTitles.Close 
 Cnxn.Close 
 Set rstTitles = Nothing 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rstTitles Is Nothing Then 
 If rstTitles.State = adStateOpen Then rstTitles.Close 
 End If 
 Set rstTitles = Nothing 
 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndMaxRecordsVB 
```

