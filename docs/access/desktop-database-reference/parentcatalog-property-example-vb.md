---
<<<<<<< Título cabeça: exemplo de propriedade ParentCatalog (VB) TOCTitle: exemplo de propriedade ParentCatalog (VB) === título: exemplo da propriedade ParentCatalog (VB) TOCTitle: exemplo da propriedade ParentCatalog (VB)
>>>>>>> ms:assetid de mestre: 3bd01153-40b5-1a45-67e2-eb8154c3fe33 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249152(v=office.15) ms:contentKeyID: ms.date 48544295: 18/09/2015 mtps_version: v=office.15
---

<<<<<<< Cabeça
# <a name="parentcatalog-property-example-vb"></a>Exemplo da propriedade ParentCatalog (VB)
=======
# <a name="parentcatalog-property-example-vb"></a>Exemplo da propriedade ParentCatalog (VB)
>>>>>>> mestre


**Aplica-se a**: Access 2013 | Office 2013

O código a seguir demonstra como usar a propriedade [ParentCatalog](parentcatalog-property-adox.md) para acessar uma propriedade específica do provedor-antes de acrescentar uma tabela a um catálogo. A propriedade é AutoIncrement, que cria um campo AutoIncrement em um banco de dados Microsoft Jet.

```vb 
 
' BeginCreateAutoIncrColumnVB 
Sub Main() 
 On Error GoTo CreateAutoIncrColumnError 
 
 Dim cnn As New ADODB.Connection 
 Dim cat As New ADOX.Catalog 
 Dim tbl As New ADOX.Table 
 
 cnn.Open "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\" & _ 
 "Microsoft Office\Office\Samples\Northwind.mdb';" 
 Set cat.ActiveConnection = cnn 
 
 With tbl 
 .Name = "MyContacts" 
 Set .ParentCatalog = cat 
 ' Create fields and append them to the new Table object. 
 .Columns.Append "ContactId", adInteger 
 ' Make the ContactId column and auto incrementing column 
 .Columns("ContactId").Properties("AutoIncrement") = True 
 .Columns.Append "CustomerID", adVarWChar 
 .Columns.Append "FirstName", adVarWChar 
 .Columns.Append "LastName", adVarWChar 
 .Columns.Append "Phone", adVarWChar, 20 
 .Columns.Append "Notes", adLongVarWChar 
 End With 
 
 cat.Tables.Append tbl 
 Debug.Print "Table 'MyContacts' is added." 
 
 ' Delete the table as this is a demonstration. 
 cat.Tables.Delete tbl.Name 
 Debug.Print "Table 'MyContacts' is delete." 
 
 'Clean up 
 cnn.Close 
 Set cat = Nothing 
 Set tbl = Nothing 
 Set cnn = Nothing 
 Exit Sub 
 
CreateAutoIncrColumnError: 
 
 Set cat = Nothing 
 Set tbl = Nothing 
 
 If Not cnn Is Nothing Then 
 If cnn.State = adStateOpen Then cnn.Close 
 End If 
 Set cnn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
 
End Sub 
' EndCreateAutoIncrColumnVB 
```

