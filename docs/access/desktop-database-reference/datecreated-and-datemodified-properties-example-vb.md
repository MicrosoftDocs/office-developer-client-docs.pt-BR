---
<<<<<<< Título cabeça: DateCreated e DateModified propriedades exemplo (VB) TOCTitle: DateCreated e DateModified propriedades exemplo (VB) === título: exemplo das propriedades DateCreated e DateModified (VB) TOCTitle: DateCreated e Exemplo das propriedades DateModified (VB)
>>>>>>> ms:assetid de mestre: 5afdb5a9-394f-c38f-83a4-ae7017673c5e ms:mtpsurl: https://msdn.microsoft.com/library/JJ249316(v=office.15) ms:contentKeyID: ms.date 48545063: 18/09/2015 mtps_version: v=office.15
---

<<<<<<< Cabeça
# <a name="datecreated-and-datemodified-properties-example-vb"></a>Exemplo das propriedades DateCreated e DateModified (VB)
=======
# <a name="datecreated-and-datemodified-properties-example-vb"></a>Exemplo das propriedades DateCreated e DateModified (VB)
>>>>>>> mestre


**Aplica-se a**: Access 2013 | Office 2013

Este exemplo demonstra as propriedades [DateCreated](datecreated-property-adox.md) e [DateModified](datemodified-property-adox.md), adicionando um nova [Coluna](column-object-adox.md) a uma [Tabela](table-object-adox.md) existente e criando um novo objeto **Table**. O procedimento DateOutput é necessário para que o exemplo funcione.

```vb 
 
' BeginDateCreatedVB 
Sub Main() 
 On Error GoTo DateCreatedXError 
 
 Dim cat As New ADOX.Catalog 
 Dim tblEmployees As ADOX.Table 
 Dim tblNewTable As ADOX.Table 
 
 ' Connect the catalog. 
 cat.ActiveConnection = "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\" & _ 
 "Microsoft Office\Office\Samples\Northwind.mdb';" 
 
 With cat 
 Set tblEmployees = .Tables("Employees") 
 
 ' Print current information about the Employees table. 
 DateOutput "Current properties", tblEmployees 
 
 ' Create and append column to the Employees table. 
 tblEmployees.Columns.Append "NewColumn", adInteger 
 .Tables.Refresh 
 
 ' Print new information about the Employees table. 
 DateOutput "After creating a new column", tblEmployees 
 
 ' Delete new column because this is a demonstration. 
 tblEmployees.Columns.Delete "NewColumn" 
 
 ' Create and append new Table object to the Northwind database. 
 Set tblNewTable = New ADOX.Table 
 tblNewTable.Name = "NewTable" 
 tblNewTable.Columns.Append "NewColumn", adInteger 
 .Tables.Append tblNewTable 
 .Tables.Refresh 
 
 ' Print information about the new Table object. 
 DateOutput "After creating a new table", .Tables("NewTable") 
 
 ' Delete new Table object because this is a demonstration. 
 .Tables.Delete tblNewTable.Name 
 End With 
 
 'Clean up 
 Set cat.ActiveConnection = Nothing 
 Set cat = Nothing 
 Exit Sub 
 
DateCreatedXError: 
 Set cat = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
 
End Sub 
 
Sub DateOutput(strTemp As String, tblTemp As ADOX.Table) 
 ' Print DateCreated and DateModified information about 
 ' specified Table object. 
 Debug.Print strTemp 
 Debug.Print " Table: " & tblTemp.Name 
 Debug.Print " DateCreated = " & tblTemp.DateCreated 
 Debug.Print " DateModified = " & tblTemp.DateModified 
 Debug.Print 
End Sub 
' EndDateCreatedVB 
```

