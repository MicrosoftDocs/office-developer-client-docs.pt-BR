---
<span data-ttu-id="c09a6-101"><<<<<<< Título cabeça: exemplo de propriedade IndexNulls (VB) TOCTitle: exemplo de propriedade IndexNulls (VB) === título: exemplo da propriedade IndexNulls (VB) TOCTitle: exemplo da propriedade IndexNulls (VB)</span><span class="sxs-lookup"><span data-stu-id="c09a6-101"><<<<<<< HEAD title: IndexNulls Property Example (VB) TOCTitle: IndexNulls Property Example (VB) ======= title: IndexNulls property example (VB) TOCTitle: IndexNulls property example (VB)</span></span>
>>>>>>> <span data-ttu-id="c09a6-102">ms:assetid de mestre: 69b5661c-931e-3a1c-d60e-96a0f93b9494 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249414(v=office.15) ms:contentKeyID: ms.date 48545417: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="c09a6-102">master ms:assetid: 69b5661c-931e-3a1c-d60e-96a0f93b9494 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249414(v=office.15) ms:contentKeyID: 48545417 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="c09a6-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="c09a6-103"><<<<<<< HEAD</span></span>
# <a name="indexnulls-property-example-vb"></a><span data-ttu-id="c09a6-104">Exemplo da propriedade IndexNulls (VB)</span><span class="sxs-lookup"><span data-stu-id="c09a6-104">IndexNulls Property Example (VB)</span></span>
=======
# <a name="indexnulls-property-example-vb"></a><span data-ttu-id="c09a6-105">Exemplo da propriedade IndexNulls (VB)</span><span class="sxs-lookup"><span data-stu-id="c09a6-105">IndexNulls property example (VB)</span></span>
>>>>>>> <span data-ttu-id="c09a6-106">mestre</span><span class="sxs-lookup"><span data-stu-id="c09a6-106">master</span></span>

<span data-ttu-id="c09a6-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c09a6-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c09a6-108">Este exemplo demonstra a propriedade [IndexNulls](indexnulls-property-adox.md) de um [Índice](index-object-adox.md).</span><span class="sxs-lookup"><span data-stu-id="c09a6-108">This example demonstrates the [IndexNulls](indexnulls-property-adox.md) property of an [Index](index-object-adox.md).</span></span> <span data-ttu-id="c09a6-109">O código cria um novo índice e define o valor de **IndexNulls** com base na entrada do usuário (em uma caixa de listagem chamada List1).</span><span class="sxs-lookup"><span data-stu-id="c09a6-109">The code creates a new index and sets the value of **IndexNulls** based on user input (from a list box named List1).</span></span> <span data-ttu-id="c09a6-110">Em seguida, o **índice** é acrescentada à [tabela](table-object-adox.md) de **funcionários** no [catálogo](catalog-object-adox.md) *Northwind* .</span><span class="sxs-lookup"><span data-stu-id="c09a6-110">Then, the **Index** is appended to the **Employees** [Table](table-object-adox.md) in the *Northwind* [Catalog](catalog-object-adox.md).</span></span> <span data-ttu-id="c09a6-111">O novo **Index** é aplicado a um [Conjunto de registros](recordset-object-ado.md) com base na tabela **Employees**, e o **Recordset** é aberto.</span><span class="sxs-lookup"><span data-stu-id="c09a6-111">The new **Index** is applied to a [Recordset](recordset-object-ado.md) based on the **Employees** table, and the **Recordset** is opened.</span></span> <span data-ttu-id="c09a6-112">Um novo registro é adicionado à tabela **Employees**, com um valor **Null** no campo indexado.</span><span class="sxs-lookup"><span data-stu-id="c09a6-112">A new record is added to the **Employees** table, with a **Null** value in the indexed field.</span></span> <span data-ttu-id="c09a6-113">A exibição desse novo registro depende da definição da propriedade **IndexNulls**.</span><span class="sxs-lookup"><span data-stu-id="c09a6-113">Whether this new record is displayed depends on the setting of the **IndexNulls** property.</span></span>

```vb
    ' IndexNullsVB 
    Sub Main() 
     On Error GoTo IndexNullsXError 
     
     Dim cnn As New ADODB.Connection 
     Dim catNorthwind As New ADOX.Catalog 
     Dim idxNew As New ADOX.Index 
     Dim rstEmployees As New ADODB.Recordset 
     Dim varBookmark As Variant 
     
     ' Connect the catalog. 
     cnn.Open "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
     "Data Source='c:\Program Files\" & _ 
     "Microsoft Office\Office\Samples\Northwind.mdb';" 
     
     Set catNorthwind.ActiveConnection = cnn 
     
     ' Append Country column to new index 
     idxNew.Columns.Append "Country" 
     idxNew.Name = "NewIndex" 
     
     Dim Response 
     Response = MsgBox("Allow 'Null' index? Otherwise ignore 'Null' index.", vbYesNo) 
     '"Allow 'Null' index? Otherwise ignore 'Null' index." 
     ', vbYesNo + vbCritical + vbDefaultButton2,,,, 
     If Response = vbYes Then ' User chose Yes. 
     idxNew.IndexNulls = adIndexNullsAllow 
     Else ' User chose No. 
     idxNew.IndexNulls = adIndexNullsIgnore 
     End If 
     
     'Append new index to Employees table 
     catNorthwind.Tables("Employees").Indexes.Append idxNew 
     
     rstEmployees.Index = idxNew.Name 
     rstEmployees.Open "Employees", cnn, adOpenKeyset, _ 
     adLockOptimistic, adCmdTableDirect 
     
     With rstEmployees 
     ' Add a new record to the Employees table. 
     .AddNew 
     !FirstName = "Gary" 
     !LastName = "Haarsager" 
     .Update 
     
     ' Bookmark the newly added record 
     varBookmark = .Bookmark 
     
     ' Use the new index to set the order of the records. 
     .MoveFirst 
     
     Debug.Print "Index = " & .Index & _ 
     ", IndexNulls = " & idxNew.IndexNulls 
     Debug.Print " Country - Name" 
     
     ' Enumerate the Recordset. The value of the 
     ' IndexNulls property will determine if the newly 
     ' added record appears in the output. 
     Do While Not .EOF 
     Debug.Print " " & _ 
     IIf(IsNull(!Country), "[Null]", !Country) & _ 
     " - " & !FirstName & " " & !LastName 
     .MoveNext 
     Loop 
     
     ' Delete new record because this is a demonstration. 
     .Bookmark = varBookmark 
     .Delete 
     
     .Close 
     End With 
     
     'Clean up 
     Set rstEmployees = Nothing 
     catNorthwind.Tables("Employees").Indexes.Delete idxNew.Name 
     cnn.Close 
     Set cnn = Nothing 
     Set catNorthwind = Nothing 
     Set idxNew = Nothing 
     Exit Sub 
     
    IndexNullsXError: 
     
     If Not rstEmployees Is Nothing Then 
     If rstEmployees.State = adStateOpen Then rstEmployees.Close 
     End If 
     Set rstEmployees = Nothing 
     
     ' Delete new Index because this is a demonstration. 
     If Not catNorthwind Is Nothing Then 
     catNorthwind.Tables("Employees").Indexes.Delete idxNew.Name 
     End If 
     
     If Not cnn Is Nothing Then 
     If cnn.State = adStateOpen Then cnn.Close 
     End If 
     Set cnn = Nothing 
     
     Set catNorthwind = Nothing 
     Set idxNew = Nothing 
     
     If Err <> 0 Then 
     MsgBox Err.Source & "-->" & Err.Description, , "Error" 
     End If 
     
    End Sub 
    ' EndIndexNullsVB
```
