---
title: Exemplo da propriedade SortOrder (VB)
TOCTitle: SortOrder Property Example (VB)
ms:assetid: 97937644-e3ef-06dc-d8ba-55ecaf7ac1ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249675(v=office.15)
ms:contentKeyID: 48546472
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ef0aa4beace636bef859f35c5d2cc354a271e9a1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462685"
---
# <a name="sortorder-property-example-vb"></a>Exemplo da propriedade SortOrder (VB)

**Aplica-se a**: Access 2013 | Office 2013

Este exemplo demonstra a propriedade [SortOrder](sortorder-property-adox.md) de uma [Coluna](column-object-adox.md) que foi anexada à coleção [Columns](columns-collection-adox.md) de um [Índice](index-object-adox.md). O código anexa um índice crescente à coluna Country da tabela **Employees** e exibe os registros. Em seguida, o código anexa um índice decrescente à coluna Country da tabela **Employees** e exibe os registros novamente. A diferença entre os índices crescente e decrescente é mostrada.


```vb 
 
' BeginSortOrderVB 
Sub Main() 
 On Error GoTo SortOrderXError 
 
 Dim cnn As New ADODB.Connection 
 Dim catNorthwind As New ADOX.Catalog 
 Dim idxAscending As New ADOX.Index 
 Dim idxDescending As New ADOX.Index 
 Dim rstEmployees As New ADODB.Recordset 
 
 ' Connect the catalog. 
 cnn.Open "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\" & _ 
 "Microsoft Office\Office\Samples\Northwind.mdb';" 
 Set catNorthwind.ActiveConnection = cnn 
 
 ' Append Country column to new index 
 idxAscending.Columns.Append "Country" 
 idxAscending.Columns("Country").SortOrder = adSortAscending 
 idxAscending.Name = "Ascending" 
 idxAscending.IndexNulls = adIndexNullsAllow 
 
 'Append new index to Employees table 
 catNorthwind.Tables("Employees").Indexes.Append idxAscending 
 
 rstEmployees.Index = idxAscending.Name 
 rstEmployees.Open "Employees", cnn, adOpenKeyset, _ 
 adLockOptimistic, adCmdTableDirect 
 
 With rstEmployees 
 .MoveFirst 
 Debug.Print "Index = " & .Index 
 Debug.Print " Country - Name" 
 
 ' Enumerate the Recordset. The value of the 
 ' IndexNulls property will determine if the newly 
 ' added record appears in the output. 
 Do While Not .EOF 
 Debug.Print " " & !Country & " - " & _ 
 !FirstName & " " & !LastName 
 .MoveNext 
 Loop 
 
 .Close 
 End With 
 
 ' Append Country column to new index 
 idxDescending.Columns.Append "Country" 
 idxDescending.Columns("Country").SortOrder = adSortDescending 
 idxDescending.Name = "Descending" 
 idxDescending.IndexNulls = adIndexNullsAllow 
 
 'Append descending index to Employees table 
 catNorthwind.Tables("Employees").Indexes.Append idxDescending 
 
 rstEmployees.Index = idxDescending.Name 
 rstEmployees.Open "Employees", cnn, adOpenKeyset, _ 
 adLockOptimistic, adCmdTableDirect 
 
 With rstEmployees 
 .MoveFirst 
 Debug.Print "Index = " & .Index 
 Debug.Print " Country - Name" 
 
 ' Enumerate the Recordset. The value of the 
 ' IndexNulls property will determine if the newly 
 ' added record appears in the output. 
 Do While Not .EOF 
 Debug.Print " " & !Country & " - " & _ 
 !FirstName & " " & !LastName 
 .MoveNext 
 Loop 
 
 .Close 
 End With 
 
 ' Delete new Indexes because this is a demonstration. 
 catNorthwind.Tables("Employees").Indexes.Delete idxAscending.Name 
 catNorthwind.Tables("Employees").Indexes.Delete idxDescending.Name 
 
 'Clean up 
 cnn.Close 
 Set catNorthwind = Nothing 
 Set idxAscending = Nothing 
 Set idxDescending = Nothing 
 Set rstEmployees = Nothing 
 Set cnn = Nothing 
 Exit Sub 
 
SortOrderXError: 
 
 Set catNorthwind = Nothing 
 Set idxAscending = Nothing 
 Set idxDescending = Nothing 
 
 If Not rstEmployees Is Nothing Then 
 If rstEmployees.State = adStateOpen Then rstEmployees.Close 
 End If 
 Set rstEmployees = Nothing 
 
 If Not cnn Is Nothing Then 
 If cnn.State = adStateOpen Then cnn.Close 
 End If 
 Set cnn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
' EndSortOrderVB 
```
