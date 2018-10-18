---
<span data-ttu-id="18c79-101"><<<<<<< Título cabeça: exemplo de propriedade StayInSync (VB) TOCTitle: exemplo de propriedade StayInSync (VB) === título: exemplo da propriedade StayInSync (VB) TOCTitle: exemplo da propriedade StayInSync (VB)</span><span class="sxs-lookup"><span data-stu-id="18c79-101"><<<<<<< HEAD title: StayInSync Property Example (VB) TOCTitle: StayInSync Property Example (VB) ======= title: StayInSync property example (VB) TOCTitle: StayInSync property example (VB)</span></span>
>>>>>>> <span data-ttu-id="18c79-102">ms:assetid de mestre: 1b35f19a-0104-efd5-5222-55f92e08473b ms:mtpsurl: https://msdn.microsoft.com/library/JJ248952(v=office.15) ms:contentKeyID: ms.date 48543535: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="18c79-102">master ms:assetid: 1b35f19a-0104-efd5-5222-55f92e08473b ms:mtpsurl: https://msdn.microsoft.com/library/JJ248952(v=office.15) ms:contentKeyID: 48543535 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="18c79-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="18c79-103"><<<<<<< HEAD</span></span>
# <a name="stayinsync-property-example-vb"></a><span data-ttu-id="18c79-104">Exemplo da propriedade StayInSync (VB)</span><span class="sxs-lookup"><span data-stu-id="18c79-104">StayInSync Property Example (VB)</span></span>
=======
# <a name="stayinsync-property-example-vb"></a><span data-ttu-id="18c79-105">Exemplo da propriedade StayInSync (VB)</span><span class="sxs-lookup"><span data-stu-id="18c79-105">StayInSync property example (VB)</span></span>
>>>>>>> <span data-ttu-id="18c79-106">mestre</span><span class="sxs-lookup"><span data-stu-id="18c79-106">master</span></span>


<span data-ttu-id="18c79-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="18c79-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="18c79-108">Este exemplo demonstra como a propriedade [StayInSync](stayinsync-property-ado.md) facilita o acesso às linhas em um [Recordset](recordset-object-ado.md) hierárquico.</span><span class="sxs-lookup"><span data-stu-id="18c79-108">This example demonstrates how the [StayInSync](stayinsync-property-ado.md) property facilitates accessing rows in a hierarchical [Recordset](recordset-object-ado.md).</span></span>

<span data-ttu-id="18c79-p101">O loop externo exibe o nome e o sobrenome, o estado e a identificação de cada autor. O **Recordset** acrescentado em cada linha é recuperado da coleção [Fields](fields-collection-ado.md) e atribuído automaticamente a **rstTitleAuthor** pela propriedade **StayInSync** sempre que o **Recordset** pai se move para uma nova linha. O loop interno exibe quatro campos a partir de cada linha no conjunto de registros acrescentado.</span><span class="sxs-lookup"><span data-stu-id="18c79-p101">The outer loop displays each author's first and last name, state, and identification. The appended **Recordset** for each row is retrieved from the [Fields](fields-collection-ado.md) collection and automatically assigned to **rstTitleAuthor** by the **StayInSync** property whenever the parent **Recordset** moves to a new row. The inner loop displays four fields from each row in the appended recordset.</span></span>

```vb 
 
'BeginStayInSyncVB 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 'To integrate this code create a DSN called Pubs 
 'with a user_id = sa and no password 
 
 Dim Cnxn As ADODB.Connection 
 Dim rst As ADODB.Recordset 
 Dim rstTitleAuthor As New ADODB.Recordset 
 Dim strCnxn As String 
 
 ' open connection with Data Shape attributes 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider=MSDataShape;Data Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 ' create recordset 
 Set rst = New ADODB.Recordset 
 rst.StayInSync = True 
 rst.Open "SHAPE {select * from Authors} " & _ 
 "APPEND ( { select * from titleauthor} AS chapTitleAuthor " & _ 
 "RELATE au_id TO au_id) ", Cnxn, , , adCmdText 
 
 Set rstTitleAuthor = rst("chapTitleAuthor").Value 
 Do Until rst.EOF 
 Debug.Print rst!au_fname & " " & rst!au_lname & " " & _ 
 rst!State & " " & rst!au_id 
 
 Do Until rstTitleAuthor.EOF 
 Debug.Print rstTitleAuthor(0) & " " & rstTitleAuthor(1) & " " & _ 
 rstTitleAuthor(2) & " " & rstTitleAuthor(3) 
 rstTitleAuthor.MoveNext 
 Loop 
 
 rst.MoveNext 
 Loop 
 
 ' clean up 
 rst.Close 
 Cnxn.Close 
 Set rst = Nothing 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rst Is Nothing Then 
 If rst.State = adStateOpen Then rst.Close 
 End If 
 Set rst = Nothing 
 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndStayInSyncVB 
```

