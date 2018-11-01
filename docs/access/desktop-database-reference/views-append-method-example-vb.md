---
title: Exemplo do método Append de Views (VB)
TOCTitle: Views Append method example (VB)
ms:assetid: 24536276-7da9-6ee8-2e27-39531b12b30f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249016(v=office.15)
ms:contentKeyID: 48543752
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9d81b5d04a37fd5e8f93bcc8814b46376209c105
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874346"
---
# <a name="views-append-method-example-vb"></a><span data-ttu-id="08b10-102">Exemplo do método Append de Views (VB)</span><span class="sxs-lookup"><span data-stu-id="08b10-102">Views Append method example (VB)</span></span>


<span data-ttu-id="08b10-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="08b10-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="08b10-104">O código a seguir demonstra como usar um objeto [Command](command-object-ado.md) e o método [Append](views-collection-adox.md) da coleção [Views](append-method-adox-views.md) para criar um novo modo de exibição na fonte de dados subjacente.</span><span class="sxs-lookup"><span data-stu-id="08b10-104">The following code demonstrates how to use a [Command](command-object-ado.md) object and the [Views](views-collection-adox.md) collection [Append](append-method-adox-views.md) method to create a new view in the underlying data source.</span></span>

```vb 
 
' BeginCreateViewVB 
Sub Main() 
 On Error GoTo CreateViewError 
 
 Dim cmd As New ADODB.Command 
 Dim cat As New ADOX.Catalog 
 
 ' Open the Catalog 
 cat.ActiveConnection = _ 
 "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\Microsoft Office\" & _ 
 "Office\Samples\Northwind.mdb';" 
 
 ' Create the command representing the view. 
 cmd.CommandText = "Select * From Customers" 
 
 ' Create the new View 
 cat.Views.Append "AllCustomers", cmd 
 
 'Clean up 
 Set cat.ActiveConnection = Nothing 
 Set cat = Nothing 
 Set cmd = Nothing 
 Exit Sub 
 
CreateViewError: 
 
 Set cat = Nothing 
 Set cmd = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
' EndCreateViewVB 
```

