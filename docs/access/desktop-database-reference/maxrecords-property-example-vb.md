---
<<<<<<< Título cabeça: exemplo de propriedade MaxRecords (VB) TOCTitle: exemplo de propriedade MaxRecords (VB) === título: exemplo da propriedade MaxRecords (VB) TOCTitle: exemplo da propriedade MaxRecords (VB)
>>>>>>> ms:assetid de mestre: e0b21025-3494-81a7-d656-03b85b0102d2 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250142(v=office.15) ms:contentKeyID: ms.date 48548241: 18/09/2015 mtps_version: v=office.15
---

<<<<<<< Cabeça
# <a name="maxrecords-property-example-vb"></a>Exemplo da propriedade MaxRecords (VB)
=======
# <a name="maxrecords-property-example-vb"></a>Exemplo da propriedade MaxRecords (VB)
>>>>>>> mestre


**Aplica-se a**: Access 2013 | Office 2013

Este exemplo usa a propriedade [MaxRecords](maxrecords-property-ado.md) para abrir um [Recordset](recordset-object-ado.md) contendo os 10 títulos mais caros da tabela ***Titles***.

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

