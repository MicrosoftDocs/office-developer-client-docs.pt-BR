---
<span data-ttu-id="da7f2-101"><<<<<<< Título cabeça: OriginalValue e UnderlyingValue propriedades exemplo (VB) TOCTitle: OriginalValue e UnderlyingValue propriedades exemplo (VB) === título: exemplo das propriedades OriginalValue e UnderlyingValue (VB) TOCTitle: Exemplo das propriedades OriginalValue e UnderlyingValue (VB)</span><span class="sxs-lookup"><span data-stu-id="da7f2-101"><<<<<<< HEAD title: OriginalValue and UnderlyingValue Properties Example (VB) TOCTitle: OriginalValue and UnderlyingValue Properties Example (VB) ======= title: OriginalValue and UnderlyingValue properties example (VB) TOCTitle: OriginalValue and UnderlyingValue properties example (VB)</span></span>
>>>>>>> <span data-ttu-id="da7f2-102">ms:assetid de mestre: de88d99d-7f2e-8418-b40f-0375b1d90a8e ms:mtpsurl: https://msdn.microsoft.com/library/JJ250127(v=office.15) ms:contentKeyID: ms.date 48548189: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="da7f2-102">master ms:assetid: de88d99d-7f2e-8418-b40f-0375b1d90a8e ms:mtpsurl: https://msdn.microsoft.com/library/JJ250127(v=office.15) ms:contentKeyID: 48548189 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="da7f2-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="da7f2-103"><<<<<<< HEAD</span></span>
# <a name="originalvalue-and-underlyingvalue-properties-example-vb"></a><span data-ttu-id="da7f2-104">Exemplo das propriedades OriginalValue e UnderlyingValue (VB)</span><span class="sxs-lookup"><span data-stu-id="da7f2-104">OriginalValue and UnderlyingValue Properties Example (VB)</span></span>
=======
# <a name="originalvalue-and-underlyingvalue-properties-example-vb"></a><span data-ttu-id="da7f2-105">Exemplo das propriedades OriginalValue e UnderlyingValue (VB)</span><span class="sxs-lookup"><span data-stu-id="da7f2-105">OriginalValue and UnderlyingValue properties example (VB)</span></span>
>>>>>>> <span data-ttu-id="da7f2-106">mestre</span><span class="sxs-lookup"><span data-stu-id="da7f2-106">master</span></span>

<span data-ttu-id="da7f2-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="da7f2-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="da7f2-108">Este exemplo demonstra as propriedades [OriginalValue](originalvalue-property-ado.md) e [UnderlyingValue](underlyingvalue-property-ado.md) exibindo uma mensagem se os dados de base de um registro forem alterados durante uma atualização em lotes do [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="da7f2-108">This example demonstrates the [OriginalValue](originalvalue-property-ado.md) and [UnderlyingValue](underlyingvalue-property-ado.md) properties by displaying a message if a record's underlying data has changed during a [Recordset](recordset-object-ado.md) batch update.</span></span>

```vb 
 
'BeginOriginalValueVB 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
 Dim Cnxn As ADODB.Connection 
 Dim rstTitles As ADODB.Recordset 
 Dim fldType As ADODB.Field 
 Dim strCnxn As String 
 Dim strSQLTitles As String 
 
 ' Open connection. 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 ' Open recordset for batch update 
 ' using object refs to set properties 
 Set rstTitles = New ADODB.Recordset 
 Set rstTitles.ActiveConnection = Cnxn 
 rstTitles.CursorType = adOpenKeyset 
 rstTitles.LockType = adLockBatchOptimistic 
 strSQLTitles = "titles" 
 rstTitles.Open strSQLTitles 
 
 ' Set field object variable for Type field 
 Set fldType = rstTitles!Type 
 
 ' Change the type of psychology titles 
 Do Until rstTitles.EOF 
 If Trim(fldType) = "psychology" Then 
 fldType = "self_help" 
 End If 
 rstTitles.MoveNext 
 Loop 
 
 ' Similate a change by another user by updating 
 ' data using a command string 
 Cnxn.Execute "UPDATE Titles SET type = 'sociology' " & _ 
 "WHERE type = 'psychology'" 
 
 'Check for changes 
 rstTitles.MoveFirst 
 Do Until rstTitles.EOF 
 If fldType.OriginalValue <> fldType.UnderlyingValue Then 
 MsgBox "Data has changed!" & vbCr & vbCr & _ 
 " Title ID: " & rstTitles!title_id & vbCr & _ 
 " Current value: " & fldType & vbCr & _ 
 " Original value: " & _ 
 fldType.OriginalValue & vbCr & _ 
 " Underlying value: " & _ 
 fldType.UnderlyingValue & vbCr 
 End If 
 rstTitles.MoveNext 
 Loop 
 
 ' Cancel the update because this is a demonstration 
 rstTitles.CancelBatch 
 
 ' Restore original values 
 Cnxn.Execute "UPDATE Titles SET type = 'psychology' " & _ 
 "WHERE type = 'sociology'" 
 
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
'EndOriginalValueVB 
```

