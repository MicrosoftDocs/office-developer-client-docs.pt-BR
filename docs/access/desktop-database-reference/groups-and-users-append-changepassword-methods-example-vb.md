---
title: Exemplo dos métodos Append e ChangePassword de grupos e usuários (VB)
TOCTitle: Groups and Users Append, ChangePassword methods example (VB)
ms:assetid: e9ae5f1c-d1fa-ab58-c889-b4e197cecf4c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250183(v=office.15)
ms:contentKeyID: 48548445
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d3213fd05d8556755adfc52d7a09a91d7f9ed597
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881997"
---
# <a name="groups-and-users-append-changepassword-methods-example-vb"></a>Exemplo dos métodos Append e ChangePassword de grupos e usuários (VB)


**Aplica-se a**: Access 2013, o Office 2013

Este exemplo demonstra o método [Append](append-method-adox-groups.md) de [Grupos](groups-collection-adox.md), bem como o método [Append](append-method-adox-users.md) de [Usuários](users-collection-adox.md) adicionando um novo [Group](group-object-adox.md) e um novo [User](user-object-adox.md) ao sistema. O novo **Group** é acrescentado à coleção **Groups** do novo **User**. Consequentemente, o novo **User** é adicionado ao **Group**. Além disso, o método [ChangePassword](changepassword-method-adox.md) é usado para especificar a senha do **User**.

```vb 
 
' BeginGroupVB 
Sub Main() 
 On Error GoTo GroupXError 
 
 Dim cat As ADOX.Catalog 
 Dim usrNew As ADOX.User 
 Dim usrLoop As ADOX.User 
 Dim grpLoop As ADOX.Group 
 
 Set cat = New ADOX.Catalog 
 
 cat.ActiveConnection = "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\" & _ 
 "Microsoft Office\Office\Samples\Northwind.mdb';" & _ 
 "jet oledb:system database=" & _ 
 "'c:\Program Files\Microsoft Office\Office\system.mdw'" 
 
 With cat 
 'Create and append new group with a string. 
 .Groups.Append "Accounting" 
 
 ' Create and append new user with an object. 
 Set usrNew = New ADOX.User 
 usrNew.Name = "Pat Smith" 
 usrNew.ChangePassword "", "Password1" 
 .Users.Append usrNew 
 
 ' Make the user Pat Smith a member of the 
 ' Accounting group by creating and adding the 
 ' appropriate Group object to the user's Groups 
 ' collection. The same is accomplished if a User 
 ' object representing Pat Smith is created and 
 ' appended to the Accounting group Users collection 
 usrNew.Groups.Append "Accounting" 
 
 ' Enumerate all User objects in the 
 ' catalog's Users collection. 
 For Each usrLoop In .Users 
 Debug.Print " " & usrLoop.Name 
 Debug.Print " Belongs to these groups:" 
 ' Enumerate all Group objects in each User 
 ' object's Groups collection. 
 If usrLoop.Groups.Count <> 0 Then 
 For Each grpLoop In usrLoop.Groups 
 Debug.Print " " & grpLoop.Name 
 Next grpLoop 
 Else 
 Debug.Print " [None]" 
 End If 
 Next usrLoop 
 
 ' Enumerate all Group objects in the default 
 ' workspace's Groups collection. 
 For Each grpLoop In .Groups 
 Debug.Print " " & grpLoop.Name 
 Debug.Print " Has as its members:" 
 ' Enumerate all User objects in each Group 
 ' object's Users collection. 
 If grpLoop.Users.Count <> 0 Then 
 For Each usrLoop In grpLoop.Users 
 Debug.Print " " & usrLoop.Name 
 Next usrLoop 
 Else 
 Debug.Print " [None]" 
 End If 
 Next grpLoop 
 
 ' Delete new User and Group objects because this 
 ' is only a demonstration. 
 ' These two line are commented out because the sub "OwnersX" uses 
 ' the group "Accounting". 
' .Users.Delete "Pat Smith" 
' .Groups.Delete "Accounting" 
 
 End With 
 
 'Clean up 
 Set cat.ActiveConnection = Nothing 
 Set cat = Nothing 
 Set usrNew = Nothing 
 Exit Sub 
 
GroupXError: 
 
 Set cat = Nothing 
 Set usrNew = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
' EndGroupVB 
```

