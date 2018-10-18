---
<span data-ttu-id="b954e-101"><<<<<<< Título cabeça: TOCTitle de exemplo de propriedade otimizar (VB): exemplo de propriedade otimizar (VB) === título: (VB) de exemplo da propriedade Optimize TOCTitle: otimizar um exemplo da propriedade (VB)</span><span class="sxs-lookup"><span data-stu-id="b954e-101"><<<<<<< HEAD title: Optimize Property Example (VB) TOCTitle: Optimize Property Example (VB) ======= title: Optimize property example (VB) TOCTitle: Optimize property example (VB)</span></span>
>>>>>>> <span data-ttu-id="b954e-102">ms:assetid de mestre: f4576247-6057-c1fe-013d-74feaab33174 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250240(v=office.15) ms:contentKeyID: ms.date 48548686: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="b954e-102">master ms:assetid: f4576247-6057-c1fe-013d-74feaab33174 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250240(v=office.15) ms:contentKeyID: 48548686 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="b954e-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="b954e-103"><<<<<<< HEAD</span></span>
# <a name="optimize-property-example-vb"></a><span data-ttu-id="b954e-104">Exemplo da propriedade Optimize (VB)</span><span class="sxs-lookup"><span data-stu-id="b954e-104">Optimize Property Example (VB)</span></span>
=======
# <a name="optimize-property-example-vb"></a><span data-ttu-id="b954e-105">Exemplo da propriedade (VB) Optimize</span><span class="sxs-lookup"><span data-stu-id="b954e-105">Optimize property example (VB)</span></span>
>>>>>>> <span data-ttu-id="b954e-106">mestre</span><span class="sxs-lookup"><span data-stu-id="b954e-106">master</span></span>


<span data-ttu-id="b954e-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b954e-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b954e-108">Este exemplo demonstra a propriedade Optimize dinâmica dos objetos [Field](field-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="b954e-108">This example demonstrates the [Field](field-object-ado.md) objects dynamic Optimize property.</span></span> <span data-ttu-id="b954e-109">O campo ***zip*** da tabela dos ***autores*** do banco de dados ***Pubs*** não é indexado.</span><span class="sxs-lookup"><span data-stu-id="b954e-109">The ***zip*** field of the ***Authors*** table in the ***Pubs*** database is not indexed.</span></span> <span data-ttu-id="b954e-110">A propriedade [Optimize](optimize-property-dynamic-ado.md) a definição como **True** no campo ***zip*** autoriza ADO para criar um índice que melhora o desempenho dos métodos [Find](find-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="b954e-110">Setting the [Optimize](optimize-property-dynamic-ado.md) property to **True** on the ***zip*** field authorizes ADO to build an index that improves the performance of the [Find](find-method-ado.md) method.</span></span>

```vb 
 
'BeginOptimizeVB 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
 ' recordset and connection variables 
 Dim Cnxn As ADODB.Connection 
 Dim rstAuthors As ADODB.Recordset 
 Dim strCnxn As String 
 Dim strSQLAuthors As String 
 
 ' Open connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Set Cnxn = New ADODB.Connection 
 Cnxn.Open strCnxn 
 
 ' open recordset client-side to enable index creation 
 Set rstAuthors = New ADODB.Recordset 
 rstAuthors.CursorLocation = adUseClient 
 strSQLAuthors = "SELECT * FROM Authors" 
 rstAuthors.Open strSQLAuthors, Cnxn, adOpenStatic, adLockReadOnly, adCmdText 
 ' Create the index 
 rstAuthors!zip.Properties("Optimize") = True 
 ' Find Akiko Yokomoto 
 rstAuthors.Find "zip = '94595'" 
 
 ' show results 
 Debug.Print rstAuthors!au_fname & " " & rstAuthors!au_lname & " " & _ 
 rstAuthors!address & " " & rstAuthors!city & " " & rstAuthors!State 
 rstAuthors!zip.Properties("Optimize") = False 'Delete the index 
 
 ' clean up 
 rstAuthors.Close 
 Cnxn.Close 
 Set rstAuthors = Nothing 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rstAuthors Is Nothing Then 
 If rstAuthors.State = adStateOpen Then rstAuthors.Close 
 End If 
 Set rstAuthors = Nothing 
 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndOptimizeVB 
```

