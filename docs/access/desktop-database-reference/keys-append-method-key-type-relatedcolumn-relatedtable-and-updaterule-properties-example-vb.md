---
<span data-ttu-id="06402-101"><<<<<<< Título cabeça: método Append de chaves, tipo de chave, exemplo de propriedades RelatedColumn (VB) TOCTitle: método Append de chaves, tipo de chave, RelatedColumn, RelatedTable e UpdateRule propriedades exemplo (VB) === título: método Append de chaves, chave Exemplo das propriedades RelatedColumn, de tipo TOCTitle (VB): exemplo de propriedades do método Append de chaves, tipo de chave, RelatedColumn, RelatedTable e UpdateRule (VB)</span><span class="sxs-lookup"><span data-stu-id="06402-101"><<<<<<< HEAD title: Keys Append Method, Key Type, RelatedColumn Properties Example (VB) TOCTitle: Keys Append Method, Key Type, RelatedColumn, RelatedTable and UpdateRule Properties Example (VB) ======= title: Keys Append Method, Key Type, RelatedColumn properties example (VB) TOCTitle: Keys Append Method, Key Type, RelatedColumn, RelatedTable and UpdateRule properties example (VB)</span></span>
>>>>>>> <span data-ttu-id="06402-102">ms:assetid de mestre: d1b0508d-ab2c-eece-061c-09c67ea9ecae ms:mtpsurl: https://msdn.microsoft.com/library/JJ250047(v=office.15) ms:contentKeyID: ms.date 48547871: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="06402-102">master ms:assetid: d1b0508d-ab2c-eece-061c-09c67ea9ecae ms:mtpsurl: https://msdn.microsoft.com/library/JJ250047(v=office.15) ms:contentKeyID: 48547871 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="06402-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="06402-103"><<<<<<< HEAD</span></span>
# <a name="keys-append-method-key-type-relatedcolumn-relatedtable-and-updaterule-properties-example-vb"></a><span data-ttu-id="06402-104">Método Append de chaves, tipo de chave, exemplo das propriedades RelatedColumn, RelatedTable e UpdateRule (VB)</span><span class="sxs-lookup"><span data-stu-id="06402-104">Keys Append Method, Key Type, RelatedColumn, RelatedTable and UpdateRule Properties Example (VB)</span></span>
=======
# <a name="keys-append-method-key-type-relatedcolumn-relatedtable-and-updaterule-properties-example-vb"></a><span data-ttu-id="06402-105">Exemplo das propriedades RelatedColumn do método Append, tipo de chave, chaves, RelatedTable e UpdateRule (VB)</span><span class="sxs-lookup"><span data-stu-id="06402-105">Keys Append Method, Key Type, RelatedColumn, RelatedTable and UpdateRule properties example (VB)</span></span>
>>>>>>> <span data-ttu-id="06402-106">mestre</span><span class="sxs-lookup"><span data-stu-id="06402-106">master</span></span>


<span data-ttu-id="06402-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="06402-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="06402-108">O código a seguir demonstra como criar uma nova chave estrangeira.</span><span class="sxs-lookup"><span data-stu-id="06402-108">The following code demonstrates how to create a new foreign key.</span></span> <span data-ttu-id="06402-109">Supõe que existem duas tabelas (**clientes** e **pedidos**).</span><span class="sxs-lookup"><span data-stu-id="06402-109">It assumes two tables (**Customers** and **Orders**) exist.</span></span>

```vb 
 
' BeginCreateKeyVB 
Sub Main() 
 On Error GoTo CreateKeyError 
 
 Dim kyForeign As New ADOX.Key 
 Dim cat As New ADOX.Catalog 
 
 ' Connect the catalog 
 cat.ActiveConnection = "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\Microsoft Office\" & _ 
 "Office\Samples\Northwind.mdb';" 
 
 ' Define the foreign key 
 kyForeign.Name = "CustOrder" 
 kyForeign.Type = adKeyForeign 
 kyForeign.RelatedTable = "Customers" 
 kyForeign.Columns.Append "CustomerId" 
 kyForeign.Columns("CustomerId").RelatedColumn = "CustomerId" 
 kyForeign.UpdateRule = adRICascade 
 
 ' Append the foreign key 
 cat.Tables("Orders").Keys.Append kyForeign 
 
 'Delete the Key as this is a demonstration 
 cat.Tables("Orders").Keys.Delete kyForeign.Name 
 
 'Clean up 
 Set cat.ActiveConnection = Nothing 
 Set cat = Nothing 
 Set kyForeign = Nothing 
 Exit Sub 
 
CreateKeyError: 
 Set cat = Nothing 
 Set kyForeign = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
 
End Sub 
' EndCreateKeyVB 
```

