---
title: Coleção Views, exemplo da propriedade CommandText (VB)
TOCTitle: Views Collection, CommandText Property Example (VB)
ms:assetid: 5dacd3c2-a1b2-57a7-1bac-ce0caa7c1a09
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249331(v=office.15)
ms:contentKeyID: 48545120
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a9e290c656d0d66dc180c86429c305588eac26d6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462134"
---
# <a name="views-collection-commandtext-property-example-vb"></a><span data-ttu-id="00653-102">Coleção Views, exemplo da propriedade CommandText (VB)</span><span class="sxs-lookup"><span data-stu-id="00653-102">Views Collection, CommandText Property Example (VB)</span></span>


<span data-ttu-id="00653-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="00653-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="00653-104">O código a seguir demonstra como usar a propriedade [Command](command-property-adox.md) para atualizar o texto de um modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="00653-104">The following code demonstrates how to use the [Command](command-property-adox.md) property to update the text of a view.</span></span>

```vb 
 
' BeginViewsCollectionVB 
Sub Main() 
 On Error GoTo ViewTextError 
 
 Dim cnn As New ADODB.Connection 
 Dim cat As New ADOX.Catalog 
 Dim cmd As New ADODB.Command 
 
 ' Open the Connection 
 cnn.Open _ 
 "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\Microsoft Office\" & _ 
 "Office\Samples\Northwind.mdb';" 
 
 ' Open the catalog 
 Set cat.ActiveConnection = cnn 
 
 ' Get the command 
 Set cmd = cat.Views("AllCustomers").Command 
 
 ' Update the CommandText of the Command 
 cmd.CommandText = _ 
 "Select CustomerId, CompanyName, ContactName From Customers" 
 
 ' Update the View 
 Set cat.Views("AllCustomers").Command = cmd 
 
 'Clean up 
 cnn.Close 
 Set cat = Nothing 
 Set cmd = Nothing 
 Set cnn = Nothing 
 Exit Sub 
 
ViewTextError: 
 
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
' EndViewsCollectionVB 
```

