---
<span data-ttu-id="3d38c-101"><<<<<<< Título cabeça: método Close de Conexão, exemplo de propriedade de tipo de tabela (VB) TOCTitle: método Close de Conexão, exemplo de propriedade de tipo de tabela (VB) === título: método Close de Conexão, exemplo da propriedade Type de tabela (VB) TOCTitle: Método Close de Conexão, exemplo da propriedade Type de tabela (VB)</span><span class="sxs-lookup"><span data-stu-id="3d38c-101"><<<<<<< HEAD title: Connection Close Method, Table Type Property Example (VB) TOCTitle: Connection Close Method, Table Type Property Example (VB) ======= title: Connection Close Method, Table Type property example (VB) TOCTitle: Connection Close Method, Table Type property example (VB)</span></span>
>>>>>>> <span data-ttu-id="3d38c-102">ms:assetid de mestre: cd0bb6ad-af7b-fb9c-d45c-5d4b62459c03 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250019(v=office.15) ms:contentKeyID: ms.date 48547754: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="3d38c-102">master ms:assetid: cd0bb6ad-af7b-fb9c-d45c-5d4b62459c03 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250019(v=office.15) ms:contentKeyID: 48547754 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="3d38c-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="3d38c-103"><<<<<<< HEAD</span></span>
# <a name="connection-close-method-table-type-property-example-vb"></a><span data-ttu-id="3d38c-104">Método Close de conexão, exemplo da propriedade Type de tabela (VB)</span><span class="sxs-lookup"><span data-stu-id="3d38c-104">Connection Close Method, Table Type Property Example (VB)</span></span>
=======
# <a name="connection-close-method-table-type-property-example-vb"></a><span data-ttu-id="3d38c-105">Método Close de Conexão, exemplo da propriedade Type de tabela (VB)</span><span class="sxs-lookup"><span data-stu-id="3d38c-105">Connection Close Method, Table Type property example (VB)</span></span>
>>>>>>> <span data-ttu-id="3d38c-106">mestre</span><span class="sxs-lookup"><span data-stu-id="3d38c-106">master</span></span>

<span data-ttu-id="3d38c-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3d38c-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3d38c-p101">A configuração da propriedade [ActiveConnection](activeconnection-property-adox.md) como **Nothing** deve "fechar" o catálogo. As coleções associadas estarão vazias. Todos os objetos que foram criados com os objetos de esquema no catálogo ficarão órfãos. Todas as propriedades desses objetos que tenham sido armazenadas em cache ainda estarão disponíveis, mas a tentativa de ler propriedades que requeiram uma chamada para o provedor falharão.</span><span class="sxs-lookup"><span data-stu-id="3d38c-p101">Setting the [ActiveConnection](activeconnection-property-adox.md) property to **Nothing** should "close" the catalog. Associated collections will be empty. Any objects that were created from schema objects in the catalog will be orphaned. Any properties on those objects that have been cached will still be available, but attempting to read properties that require a call to the provider will fail.</span></span>

```vb 
 
    ' BeginCloseConnectionVB 
    Sub Main() 
    On Error GoTo CloseConnectionByNothingError 
    
    Dim cnn As New ADODB.Connection 
    Dim cat As New ADOX.Catalog 
    Dim tbl As ADOX.Table 
    
    cnn.Open "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
    "Data Source= 'c:\Program Files\Microsoft Office\" & _ 
    "Office\Samples\Northwind.mdb';" 
    Set cat.ActiveConnection = cnn 
    Set tbl = cat.Tables(0) 
    Debug.Print tbl.Type ' Cache tbl.Type info 
    Set cat.ActiveConnection = Nothing 
    Debug.Print tbl.Type ' tbl is orphaned 
    ' Previous line will succeed if this was cached 
    Debug.Print tbl.Columns(0).DefinedSize 
    ' Previous line will fail if this info has not been cached 
    
    'Clean up 
    cnn.Close 
    Set cat = Nothing 
    Set cnn = Nothing 
    Exit Sub 
    
    CloseConnectionByNothingError: 
    Set cat = Nothing 
    
    If Not cnn Is Nothing Then 
    If cnn.State = adStateOpen Then cnn.Close 
    End If 
    Set cnn = Nothing 
    
    If Err <> 0 Then 
    MsgBox Err.Source & "-->" & Err.Description, , "Error" 
    End If 
    End Sub 
    ' EndCloseConnectionVB 
```

<br/>

<span data-ttu-id="3d38c-112">Fechar um objeto [Connection](connection-object-ado.md) que tenha sido usado para "abrir" o catálogo é o mesmo que configurar a propriedade **ActiveConnection** como **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="3d38c-112">Closing a [Connection](connection-object-ado.md) object that was used to "open" the catalog should have the same effect as setting the **ActiveConnection** property to **Nothing**.</span></span>

```vb
    Sub CloseConnection() 
     On Error GoTo CloseConnectionError 
     
     Dim cnn As New ADODB.Connection 
     Dim cat As New ADOX.Catalog 
     Dim tbl As ADOX.Table 
     
     cnn.Open "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
     "Data Source= 'c:\Program Files\Microsoft Office\" & _ 
     "Office\Samples\Northwind.mdb';" 
     Set cat.ActiveConnection = cnn 
     Set tbl = cat.Tables(0) 
     Debug.Print tbl.Type ' Cache tbl.Type info 
     cnn.Close 
     Debug.Print tbl.Type ' tbl is orphaned 
     ' Previous line will succeed if this was cached 
     Debug.Print tbl.Columns(0).DefinedSize 
     ' Previous line will fail if this info has not been cached 
     
     'Clean up 
     Set cat = Nothing 
     Set cnn = Nothing 
     Exit Sub 
     
    CloseConnectionError: 
     
     Set cat = Nothing 
     
     If Not cnn Is Nothing Then 
     If cnn.State = adStateOpen Then cnn.Close 
     End If 
     Set cnn = Nothing 
     
     If Err <> 0 Then 
     MsgBox Err.Source & "-->" & Err.Description, , "Error" 
     End If 
    End Sub 
    ' EndCloseConnection2VB
```
