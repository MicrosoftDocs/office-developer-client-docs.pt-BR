---
title: Exemplo das propriedades Command e CommandText (VB)
TOCTitle: Command and CommandText properties example (VB)
ms:assetid: 6bf35604-401b-0727-85e8-ac2ecda368df
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249425(v=office.15)
ms:contentKeyID: 48545462
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e19ac7517e548f1594c0b525671e6aff66eef72c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888507"
---
# <a name="command-and-commandtext-properties-example-vb"></a><span data-ttu-id="f214b-102">Exemplo das propriedades Command e CommandText (VB)</span><span class="sxs-lookup"><span data-stu-id="f214b-102">Command and CommandText properties example (VB)</span></span>


<span data-ttu-id="f214b-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="f214b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f214b-104">O código a seguir demonstra como usar a propriedade [Command](command-property-adox.md) para atualizar o texto de um procedimento.</span><span class="sxs-lookup"><span data-stu-id="f214b-104">The following code demonstrates how to use the [Command](command-property-adox.md) property to update the text of a procedure.</span></span>

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

