---
<span data-ttu-id="85396-101"><<<<<<< Título cabeça: exemplo de propriedade DeleteRule (VB) TOCTitle: exemplo de propriedade DeleteRule (VB) === título: exemplo da propriedade DeleteRule (VB) TOCTitle: exemplo da propriedade DeleteRule (VB)</span><span class="sxs-lookup"><span data-stu-id="85396-101"><<<<<<< HEAD title: DeleteRule Property Example (VB) TOCTitle: DeleteRule Property Example (VB) ======= title: DeleteRule property example (VB) TOCTitle: DeleteRule property example (VB)</span></span>
>>>>>>> <span data-ttu-id="85396-102">ms:assetid de mestre: 354e00b6-cecb-1132-6923-fc9e8853fa0e ms:mtpsurl: https://msdn.microsoft.com/library/JJ249114(v=office.15) ms:contentKeyID: ms.date 48544142: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="85396-102">master ms:assetid: 354e00b6-cecb-1132-6923-fc9e8853fa0e ms:mtpsurl: https://msdn.microsoft.com/library/JJ249114(v=office.15) ms:contentKeyID: 48544142 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="85396-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="85396-103"><<<<<<< HEAD</span></span>
# <a name="deleterule-property-example-vb"></a><span data-ttu-id="85396-104">Exemplo da propriedade DeleteRule (VB)</span><span class="sxs-lookup"><span data-stu-id="85396-104">DeleteRule Property Example (VB)</span></span>
=======
# <a name="deleterule-property-example-vb"></a><span data-ttu-id="85396-105">Exemplo da propriedade DeleteRule (VB)</span><span class="sxs-lookup"><span data-stu-id="85396-105">DeleteRule property example (VB)</span></span>
>>>>>>> <span data-ttu-id="85396-106">mestre</span><span class="sxs-lookup"><span data-stu-id="85396-106">master</span></span>


<span data-ttu-id="85396-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="85396-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="85396-p101">Este exemplo demonstra a propriedade [DeleteRule](deleterule-property-adox.md) de um objeto [Key](key-object-adox.md). O código acrescenta uma nova [Tabela](table-object-adox.md) e, em seguida, define uma nova chave primária, definindo **DeleteRule** como **adRICascade**.</span><span class="sxs-lookup"><span data-stu-id="85396-p101">This example demonstrates the [DeleteRule](deleterule-property-adox.md) property of a [Key](key-object-adox.md) object. The code appends a new [Table](table-object-adox.md) and then defines a new primary key, setting **DeleteRule** to **adRICascade**.</span></span>

```vb 
 
' BeginDeleteRuleVB 
Sub Main() 
 On Error GoTo DeleteRuleXError 
 
 Dim kyPrimary As New ADOX.Key 
 Dim cat As New ADOX.Catalog 
 Dim tblNew As New ADOX.Table 
 
 ' Connect the catalog 
 cat.ActiveConnection = "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "data source='c:\Program Files\" & _ 
 "Microsoft Office\Office\Samples\Northwind.mdb';" 
 
 ' Name new table 
 tblNew.Name = "NewTable" 
 
 ' Append a numeric and a text field to new table. 
 tblNew.Columns.Append "NumField", adInteger, 20 
 tblNew.Columns.Append "TextField", adVarWChar, 20 
 
 ' Append the new table 
 cat.Tables.Append tblNew 
 
 ' Define the Primary key 
 kyPrimary.Name = "NumField" 
 kyPrimary.Type = adKeyPrimary 
 kyPrimary.RelatedTable = "Customers" 
 kyPrimary.Columns.Append "NumField" 
 kyPrimary.Columns("NumField").RelatedColumn = "CustomerId" 
 kyPrimary.DeleteRule = adRICascade 
 
 ' Append the primary key 
 cat.Tables("NewTable").Keys.Append kyPrimary 
 Debug.Print "The primary key is appended." 
 
 'Delete the table as this is a demonstration. 
 cat.Tables.Delete tblNew.Name 
 Debug.Print "The primary key is deleted." 
 
 'Clean up 
 Set cat.ActiveConnection = Nothing 
 Set cat = Nothing 
 Set kyPrimary = Nothing 
 Set tblNew = Nothing 
 Exit Sub 
 
DeleteRuleXError: 
 
 Set cat = Nothing 
 Set kyPrimary = Nothing 
 Set tblNew = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
 
End Sub 
' EndDeleteRuleVB 
```

