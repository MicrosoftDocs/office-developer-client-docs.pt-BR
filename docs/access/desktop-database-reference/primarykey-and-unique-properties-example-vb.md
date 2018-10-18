---
<<<<<<< Título cabeça: PrimaryKey e exemplo de propriedades exclusivo (VB) TOCTitle: PrimaryKey e exemplo de propriedades exclusivo (VB) === título: exemplo das propriedades PrimaryKey e Unique (VB) TOCTitle: exemplo das propriedades PrimaryKey e Unique (VB)
>>>>>>> ms:assetid de mestre: 888f1a35-b883-2449-3b70-103e5116b29f ms:mtpsurl: https://msdn.microsoft.com/library/JJ249597(v=office.15) ms:contentKeyID: ms.date 48546137: 18/09/2015 mtps_version: v=office.15
---

<<<<<<< Cabeça
# <a name="primarykey-and-unique-properties-example-vb"></a>Exemplo das propriedades PrimaryKey e Unique (VB)
=======
# <a name="primarykey-and-unique-properties-example-vb"></a>Exemplo das propriedades PrimaryKey e Unique (VB)
>>>>>>> mestre


**Aplica-se a**: Access 2013 | Office 2013

Este exemplo demonstra as propriedades [PrimaryKey](primarykey-property-adox.md) e [Unique](unique-property-adox.md) de um [Index](index-object-adox.md). O código cria uma nova tabela com duas colunas. As propriedades **PrimaryKey** e **Unique** são usadas a fim de tornar uma coluna a chave primária para a qual valores duplicados não são permitidos.

```vb 
 
' BeginPrimaryKeyVB 
Sub Main() 
 On Error GoTo PrimaryKeyXError 
 
 Dim catNorthwind As New ADOX.Catalog 
 Dim tblNew As New ADOX.Table 
 Dim idxNew As New ADOX.Index 
 Dim idxLoop As New ADOX.Index 
 Dim colLoop As New ADOX.Column 
 
 ' Connect the catalog 
 catNorthwind.ActiveConnection = "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\" & _ 
 "Microsoft Office\Office\Samples\Northwind.mdb';" 
 
 ' Name new table 
 tblNew.Name = "NewTable" 
 
 ' Append a numeric and a text field to new table. 
 tblNew.Columns.Append "NumField", adInteger, 20 
 tblNew.Columns.Append "TextField", adVarWChar, 20 
 
 ' Append new Primary Key index on NumField column 
 ' to new table 
 idxNew.Name = "NumIndex" 
 idxNew.Columns.Append "NumField" 
 idxNew.PrimaryKey = True 
 idxNew.Unique = True 
 tblNew.Indexes.Append idxNew 
 
 ' Append an index on Textfield to new table. 
 ' Note the different technique: Specifying index and 
 ' column name as parameters of the Append method 
 tblNew.Indexes.Append "TextIndex", "TextField" 
 
 ' Append the new table 
 catNorthwind.Tables.Append tblNew 
 
 With tblNew 
 Debug.Print tblNew.Indexes.Count & " Indexes in " & _ 
 tblNew.Name & " Table" 
 
 ' Enumerate Indexes collection. 
 For Each idxLoop In .Indexes 
 With idxLoop 
 Debug.Print "Index " & .Name 
 Debug.Print " Primary key = " & .PrimaryKey 
 Debug.Print " Unique = " & .Unique 
 
 ' Enumerate Columns collection of each Index 
 ' object. 
 Debug.Print " Columns" 
 For Each colLoop In .Columns 
 Debug.Print " " & colLoop.Name 
 Next colLoop 
 End With 
 Next idxLoop 
 
 End With 
 
 ' Delete new table as this is a demonstration. 
 catNorthwind.Tables.Delete tblNew.Name 
 
 'Clean up 
 Set catNorthwind.ActiveConnection = Nothing 
 Set catNorthwind = Nothing 
 Set tblNew = Nothing 
 Set idxNew = Nothing 
 Set idxLoop = Nothing 
 Set colLoop = Nothing 
 Exit Sub 
 
PrimaryKeyXError: 
 
 Set catNorthwind = Nothing 
 Set tblNew = Nothing 
 Set idxNew = Nothing 
 Set idxLoop = Nothing 
 Set colLoop = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
' EndPrimaryKeyVB 
```

