---
<<<<<<< Título cabeça: comando e exemplo de propriedades de CommandText (VB) TOCTitle: comando e exemplo de propriedades de CommandText (VB) === título: exemplo das propriedades Command e CommandText (VB) TOCTitle: Command e CommandText exemplo das propriedades (VB)
>>>>>>> ms:assetid de mestre: 6bf35604-401b-0727-85e8-ac2ecda368df ms:mtpsurl: https://msdn.microsoft.com/library/JJ249425(v=office.15) ms:contentKeyID: ms.date 48545462: 18/09/2015 mtps_version: v=office.15
---

<<<<<<< Cabeça
# <a name="command-and-commandtext-properties-example-vb"></a>Exemplo das propriedades Command e CommandText (VB)
=======
# <a name="command-and-commandtext-properties-example-vb"></a>Exemplo das propriedades Command e CommandText (VB)
>>>>>>> mestre


**Aplica-se a**: Access 2013 | Office 2013

O código a seguir demonstra como usar a propriedade [Command](command-property-adox.md) para atualizar o texto de um procedimento.

```vb 
 
' BeginProcedureTextVB 
Sub Main() 
 On Error GoTo ProcedureTextError 
 
 Dim cnn As New ADODB.Connection 
 Dim cat As New ADOX.Catalog 
 Dim cmd As New ADODB.Command 
 
 ' Open the Connection 
 cnn.Open "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\Microsoft Office\" & _ 
 "Office\Samples\Northwind.mdb';" 
 
 ' Open the catalog 
 Set cat.ActiveConnection = cnn 
 
 ' Get the Command 
 Set cmd = cat.Procedures("CustomerById").Command 
 
 ' Update the CommandText 
 cmd.CommandText = "Select CustomerId, CompanyName, ContactName " & _ 
 "From Customers " & _ 
 "Where CustomerId = [CustId]" 
 
 ' Update the Procedure 
 Set cat.Procedures("CustomerById").Command = cmd 
 
 'Clean up 
 cnn.Close 
 Set cat = Nothing 
 Set cmd = Nothing 
 Set cnn = Nothing 
 Exit Sub 
 
ProcedureTextError: 
 Set cat = Nothing 
 Set cmd = Nothing 
 
 If Not cnn Is Nothing Then 
 If cnn.State = adStateOpen Then cnn.Close 
 End If 
 Set cnn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
' EndProcedureTextVB 
```

