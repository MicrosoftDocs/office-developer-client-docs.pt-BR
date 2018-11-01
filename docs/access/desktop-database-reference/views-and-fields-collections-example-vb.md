---
title: Exemplo de modos de exibição e coleções Fields (VB)
TOCTitle: Views and Fields Collections example (VB)
ms:assetid: 7c166bea-d6a3-0a9d-5220-af72996a76fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249518(v=office.15)
ms:contentKeyID: 48545828
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f5d22d4d5be88063524b2a55bb1703deeb173018
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884622"
---
# <a name="views-and-fields-collections-example-vb"></a><span data-ttu-id="bee75-102">Exemplo de modos de exibição e coleções Fields (VB)</span><span class="sxs-lookup"><span data-stu-id="bee75-102">Views and Fields Collections example (VB)</span></span>


<span data-ttu-id="bee75-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="bee75-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bee75-104">O código a seguir demonstra como usar a propriedade [Command](command-property-adox.md) e o objeto [Recordset](recordset-object-ado.md) para recuperar informações de campo para o modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="bee75-104">The following code demonstrates how to use the [Command](command-property-adox.md) property and the [Recordset](recordset-object-ado.md) object to retrieve field information for the view.</span></span>

```vb 
 
' BeginViewFieldsVB 
Sub ViewFields() 
 On Error GoTo ViewFieldsError 
 
 Dim cnn As New ADODB.Connection 
 Dim rst As New ADODB.Recordset 
 Dim fld As ADODB.Field 
 Dim cat As New ADOX.Catalog 
 
 ' Open the Connection 
 cnn.Open _ 
 "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\Microsoft Office\" & _ 
 "Office\Samples\Northwind.mdb';" 
 
 ' Open the catalog 
 Set cat.ActiveConnection = cnn 
 
 ' Set the Source for the Recordset 
 Set rst.Source = cat.Views("AllCustomers").Command 
 
 ' Retrieve Field information 
 rst.Fields.Refresh 
 For Each fld In rst.Fields 
 Debug.Print fld.Name & ":" & fld.Type 
 Next 
 
 'Clean up 
 cnn.Close 
 Set cat = Nothing 
 Set rst = Nothing 
 Set cnn = Nothing 
 Exit Sub 
 
ViewFieldsError: 
 
 If Not cnn Is Nothing Then 
 If cnn.State = adStateOpen Then cnn.Close 
 End If 
 
 Set cat = Nothing 
 Set rst = Nothing 
 Set cnn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
 
End Sub 
' EndViewFieldsVB 
```

