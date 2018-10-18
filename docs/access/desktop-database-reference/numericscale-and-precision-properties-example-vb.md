---
<span data-ttu-id="0cb76-101"><<<<<<< Título cabeça: NumericScale e Precision propriedades exemplo (VB) TOCTitle: NumericScale e Precision propriedades exemplo (VB) === título: exemplo das propriedades NumericScale e Precision (VB) TOCTitle: NumericScale e Exemplo das propriedades Precision (VB)</span><span class="sxs-lookup"><span data-stu-id="0cb76-101"><<<<<<< HEAD title: NumericScale and Precision Properties Example (VB) TOCTitle: NumericScale and Precision Properties Example (VB) ======= title: NumericScale and Precision properties example (VB) TOCTitle: NumericScale and Precision properties example (VB)</span></span>
>>>>>>> <span data-ttu-id="0cb76-102">ms:assetid de mestre: 728a76a3-1f80-935b-b6c7-94255ffe0160 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249462(v=office.15) ms:contentKeyID: ms.date 48545610: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="0cb76-102">master ms:assetid: 728a76a3-1f80-935b-b6c7-94255ffe0160 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249462(v=office.15) ms:contentKeyID: 48545610 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="0cb76-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="0cb76-103"><<<<<<< HEAD</span></span>
# <a name="numericscale-and-precision-properties-example-vb"></a><span data-ttu-id="0cb76-104">Exemplo das propriedades NumericScale e Precision (VB)</span><span class="sxs-lookup"><span data-stu-id="0cb76-104">NumericScale and Precision Properties Example (VB)</span></span>
=======
# <a name="numericscale-and-precision-properties-example-vb"></a><span data-ttu-id="0cb76-105">Exemplo das propriedades NumericScale e Precision (VB)</span><span class="sxs-lookup"><span data-stu-id="0cb76-105">NumericScale and Precision properties example (VB)</span></span>
>>>>>>> <span data-ttu-id="0cb76-106">mestre</span><span class="sxs-lookup"><span data-stu-id="0cb76-106">master</span></span>


<span data-ttu-id="0cb76-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0cb76-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0cb76-108">Este exemplo demonstra as propriedades [NumericScale](numericscale-property-adox.md) e [Precision](precision-property-adox.md) do objeto [Column](column-object-adox.md).</span><span class="sxs-lookup"><span data-stu-id="0cb76-108">This example demonstrates the [NumericScale](numericscale-property-adox.md) and [Precision](precision-property-adox.md) properties of the [Column](column-object-adox.md) object.</span></span> <span data-ttu-id="0cb76-109">Este código exibe seu valor para a tabela **Detalhes do pedido** do banco de dados *Northwind* .</span><span class="sxs-lookup"><span data-stu-id="0cb76-109">This code displays their value for the **Order Details** table of the *Northwind* database.</span></span>

```vb 
 
' BeginNumericScalePrecVB 
Sub Main() 
 On Error GoTo NumericScalePrecXError 
 
 Dim cnn As New ADODB.Connection 
 Dim cat As New ADOX.Catalog 
 Dim tblOD As ADOX.Table 
 Dim colLoop As ADOX.Column 
 
 ' Connect the catalog. 
 cnn.Open "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "data source='c:\Program Files\" & _ 
 "Microsoft Office\Office\Samples\Northwind.mdb';" 
 Set cat.ActiveConnection = cnn 
 
 ' Retrieve the Order Details table 
 Set tblOD = cat.Tables("Order Details") 
 
 ' Display numeric scale and precision of 
 ' small integer fields. 
 For Each colLoop In tblOD.Columns 
 If colLoop.Type = adSmallInt Then 
 MsgBox "Column: " & colLoop.Name & vbCr & _ 
 "Numeric scale: " & _ 
 colLoop.NumericScale & vbCr & _ 
 "Precision: " & colLoop.Precision 
 End If 
 Next colLoop 
 
 'Clean up 
 cnn.Close 
 Set cat = Nothing 
 Set cnn = Nothing 
 Exit Sub 
 
NumericScalePrecXError: 
 Set cat = Nothing 
 
 If Not cnn Is Nothing Then 
 If cnn.State = adStateOpen Then cnn.Close 
 End If 
 Set cnn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
' EndNumericScalePrecVB 
```

