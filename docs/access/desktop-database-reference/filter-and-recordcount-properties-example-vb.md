---
<span data-ttu-id="fe49d-101"><<<<<<< Título cabeça: Filter e RecordCount propriedades exemplo (VB) TOCTitle: Filter e RecordCount propriedades exemplo (VB) === título: exemplo das propriedades Filter e RecordCount (VB) TOCTitle: propriedades Filter e RecordCount exemplo (VB)</span><span class="sxs-lookup"><span data-stu-id="fe49d-101"><<<<<<< HEAD title: Filter and RecordCount Properties Example (VB) TOCTitle: Filter and RecordCount Properties Example (VB) ======= title: Filter and RecordCount properties example (VB) TOCTitle: Filter and RecordCount properties example (VB)</span></span>
>>>>>>> <span data-ttu-id="fe49d-102">ms:assetid de mestre: 3da4623e-03e7-27ac-7351-3b22415be0b9 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249167(v=office.15) ms:contentKeyID: ms.date 48544354: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="fe49d-102">master ms:assetid: 3da4623e-03e7-27ac-7351-3b22415be0b9 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249167(v=office.15) ms:contentKeyID: 48544354 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="fe49d-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="fe49d-103"><<<<<<< HEAD</span></span>
# <a name="filter-and-recordcount-properties-example-vb"></a><span data-ttu-id="fe49d-104">Exemplo das propriedades Filter e RecordCount (VB)</span><span class="sxs-lookup"><span data-stu-id="fe49d-104">Filter and RecordCount Properties Example (VB)</span></span>
=======
# <a name="filter-and-recordcount-properties-example-vb"></a><span data-ttu-id="fe49d-105">Exemplo das propriedades Filter e RecordCount (VB)</span><span class="sxs-lookup"><span data-stu-id="fe49d-105">Filter and RecordCount properties example (VB)</span></span>
>>>>>>> <span data-ttu-id="fe49d-106">mestre</span><span class="sxs-lookup"><span data-stu-id="fe49d-106">master</span></span>


<span data-ttu-id="fe49d-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="fe49d-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="fe49d-108">Este exemplo abrir um **conjunto de registros** na tabela editores no banco de dados ***Pubs*** .</span><span class="sxs-lookup"><span data-stu-id="fe49d-108">This example open a **Recordset** on the Publishers table in the ***Pubs*** database.</span></span> <span data-ttu-id="fe49d-109">Em seguida, ele usa a propriedade [Filter](filter-property-ado.md) para limitar o número de registros visíveis aos editores de um(a) determinado(a) país/região.</span><span class="sxs-lookup"><span data-stu-id="fe49d-109">It then uses the [Filter](filter-property-ado.md) property to limit the number of visible records to those publishers in a particular country/region.</span></span> <span data-ttu-id="fe49d-110">A propriedade **RecordCount** é usada para mostrar a diferença entre os conjuntos de registros filtrados e não filtrados.</span><span class="sxs-lookup"><span data-stu-id="fe49d-110">The **RecordCount** property is used to show the difference between the filtered and unfiltered recordsets.</span></span>

```vb 
 
'BeginFilterVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 ' recordset variables 
 Dim rstPublishers As ADODB.Recordset 
 Dim Cnxn As ADODB.Connection 
 Dim strCnxn As String 
 Dim SQLPublishers As String 
 
 ' criteria variables 
 Dim intPublisherCount As Integer 
 Dim strCountry As String 
 Dim strMessage As String 
 
 ' open connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 ' open recordset with data from Publishers table 
 Set rstPublishers = New ADODB.Recordset 
 SQLPublishers = "publishers" 
 rstPublishers.Open SQLPublishers, strCnxn, adOpenStatic, , adCmdTable 
 
 intPublisherCount = rstPublishers.RecordCount 
 
 ' get user input 
 strCountry = Trim(InputBox("Enter a country to filter on (e.g. USA):")) 
 
 If strCountry <> "" Then 
 ' open a filtered Recordset object 
 rstPublishers.Filter = "Country ='" & strCountry & "'" 
 
 If rstPublishers.RecordCount = 0 Then 
 MsgBox "No publishers from that country." 
 Else 
 ' print number of records for the original recordset 
 ' and the filtered recordset 
 strMessage = "Orders in original recordset: " & _ 
 vbCr & intPublisherCount & vbCr & _ 
 "Orders in filtered recordset (Country = '" & _ 
 strCountry & "'): " & vbCr & _ 
 rstPublishers.RecordCount 
 MsgBox strMessage 
 End If 
 End If 
 
 ' clean up 
 rstPublishers.Close 
 Cnxn.Close 
 Set rstPublishers = Nothing 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rstPublishers Is Nothing Then 
 If rstPublishers.State = adStateOpen Then rstPublishers.Close 
 End If 
 Set rstPublishers = Nothing 
 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
 
End Sub 
'EndFilterVB 
```


> [!NOTE]
> <P><span data-ttu-id="fe49d-p102">[!OBSERVAçãO] Quando você sabe quais dados deseja selecionar, em geral é mais eficiente abrir um <STRONG>Recordset</STRONG> com uma instrução SQL. Este exemplo mostra como você pode criar apenas um <STRONG>Recordset</STRONG> e obter registros de um(a) determinado(a) país/região.</span><span class="sxs-lookup"><span data-stu-id="fe49d-p102">When you know the data you want to select, it's usually more efficient to open a <STRONG>Recordset</STRONG> with an SQL statement. This example shows how you can create just one <STRONG>Recordset</STRONG> and obtain records from a particular country/region.</span></span></P>



```vb 
 
'BeginFilter2VB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 Dim rstPublishers As ADODB.Recordset 
 Dim Cnxn As ADODB.Connection 
 Dim strSQLPublishers As String 
 Dim strCnxn As String 
 
 ' open connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 ' open recordset with criteria from Publishers table 
 Set rstPublishers = New ADODB.Recordset 
 strSQLPublishers = "SELECT * FROM publishers WHERE Country = 'USA'" 
 rstPublishers.Open strSQLPublishers, Cnxn, adOpenStatic, adLockReadOnly, adCmdText 
 
 ' print recordset 
 rstPublishers.MoveFirst 
 Do While Not rstPublishers.EOF 
 Debug.Print rstPublishers!pub_name & ", " & rstPublishers!country 
 rstPublishers.MoveNext 
 Loop 
 
 ' clean up 
 rstPublishers.Close 
 Cnxn.Close 
 Set rstPublishers = Nothing 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rstPublishers Is Nothing Then 
 If rstPublishers.State = adStateOpen Then rstPublishers.Close 
 End If 
 Set rstPublishers = Nothing 
 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndFilter2VB 
```

