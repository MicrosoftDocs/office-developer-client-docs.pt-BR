---
title: Método Recordset2. CancelUpdate (DAO)
TOCTitle: CancelUpdate Method
ms:assetid: f741dec1-b9a4-506e-74ec-2bc309b0918e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836907(v=office.15)
ms:contentKeyID: 48548761
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 90378dc61d12485a290bbd7857d026a46cd9da96
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307396"
---
# <a name="recordset2cancelupdate-method-dao"></a>Método Recordset2. CancelUpdate (DAO)

**Aplica-se ao:** Access 2013, Office 2013

Cancela as atualizações pendentes para um objeto **[Recordset](recordset-object-dao.md)**.

## <a name="syntax"></a>Sintaxe

*expressão* . CancelUpdate (***UpdateType***)

*expressão* Uma variável que representa um objeto **Recordset2** .

## <a name="parameters"></a>Parâmetros

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome</p></th>
<th><p>Obrigatório/opcional</p></th>
<th><p>Tipo de dados</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>UpdateType</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>Defina como um dos valores <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> .</p><p><strong>Observação</strong>: os valores <EM>dbUpdateRegular</EM> e <EM>dbUpdateBatch</EM> são válidos somente se a atualização em lotes estiver habilitada.</p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Você pode usar o método **CancelUpdate** para cancelar atualizações pendentes que resultam de uma operação **[Edit](recordset2-edit-method-dao.md)** ou **[AddNew](recordset2-addnew-method-dao.md)**. Por exemplo, se um usuário invocar o método **Edit** ou **AddNew** e não tiver invocado ainda o método **Update**, **CancelUpdate** cancelará quaisquer alterações feitas depois que **Edit** ou **AddNew** tiver sido invocado.

Verifique a propriedade **[EditMode](recordset2-editmode-property-dao.md)** do **Recordset** para determinar se existe uma operação pendente que possa ser cancelada.

> [!NOTE]
> [!OBSERVAçãO] Usar o método **CancelUpdate** tem o mesmo efeito de mover para outro registro sem usar o método **[Update](recordset2-update-method-dao.md)**, exceto pelo fato de que o registro atual não muda e várias propriedades, como **[BOF](recordset2-bof-property-dao.md)** e **[EOF](recordset2-eof-property-dao.md)**, não são atualizadas.

## <a name="example"></a>Exemplo

Este exemplo mostra como o método **CancelUpdate** é usado com o método **AddNew**.

```vb
    Sub CancelUpdateX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset2 
       Dim intCommand As Integer 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstEmployees = dbsNorthwind.OpenRecordset( _ 
          "Employees", dbOpenDynaset) 
     
       With rstEmployees 
          .AddNew 
          !FirstName = "Kimberly" 
          !LastName = "Bowen" 
          intCommand = MsgBox("Add new record for " & _ 
             !FirstName & " " & !LastName & "?", vbYesNo) 
          If intCommand = vbYes Then 
             .Update 
             MsgBox "Record added." 
             ' Delete new record because this is a  
             ' demonstration. 
             .Bookmark = .LastModified 
             .Delete 
          Else 
             .CancelUpdate 
             MsgBox "Record not added." 
          End If 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

Este exemplo mostra como o método **CancelUpdate** é usado com o método **Edit**.

```vb
Sub CancelUpdateX2() 
 
   Dim dbsNorthwind As Database 
   Dim rstEmployees As Recordset 
   Dim strFirst As String 
   Dim strLast As String 
   Dim intCommand As Integer 
 
   Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
   Set rstEmployees = dbsNorthwind.OpenRecordset( _ 
      "Employees", dbOpenDynaset) 
 
   With rstEmployees 
      strFirst = !FirstName 
      strLast = !LastName 
      .Edit 
      !FirstName = "Cora" 
      !LastName = "Edmonds" 
      intCommand = MsgBox("Replace current name with " & _ 
         !FirstName & " " & !LastName & "?", vbYesNo) 
      If intCommand = vbYes Then 
         .Update 
         MsgBox "Record modified." 
         ' Restore data because this is a demonstration. 
         .Bookmark = .LastModified 
         .Edit 
         !FirstName = strFirst 
         !LastName = strLast 
         .Update 
      Else 
         .CancelUpdate 
         MsgBox "Record not modified." 
      End If 
      .Close 
   End With 
 
   dbsNorthwind.Close 
 
End Sub 
 
```

