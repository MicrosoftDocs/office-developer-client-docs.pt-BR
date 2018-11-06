---
title: Método Recordset.CancelUpdate (DAO)
TOCTitle: CancelUpdate method
ms:assetid: efc4f60b-876f-5e11-37fd-0fbbf225b15b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836421(v=office.15)
ms:contentKeyID: 48548590
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053072
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 6cb9823cec79a31f8ae26b2518d4368f6eefe2ce
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25999075"
---
# <a name="recordsetcancelupdate-method-dao"></a>Método Recordset.CancelUpdate (DAO)

**Aplica-se a**: Access 2013, o Office 2013

Cancela quaisquer atualizações pendentes para um objeto **[Recordset](recordset-object-dao.md)**.

## <a name="syntax"></a>Sintaxe

*expressão* . CancelUpdate (***UpdateType***)

*expressão* Uma variável que representa um objeto **Recordset** .

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
<td><p>Defina como um dos valores <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> .</p><p><strong>Observação</strong>: os valores de <EM>dbUpdateRegular</EM> e <EM>dbUpdateBatch</EM> são válidos somente se a atualização em lotes está habilitado.</p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Você pode usar o método **CancelUpdate** para cancelar atualizações pendentes que resultam de uma operação **[Edit](recordset-edit-method-dao.md)** ou **[AddNew](recordset-addnew-method-dao.md)**. Por exemplo, se um usuário invocar o método **Edit** ou **AddNew** e não tiver invocado ainda o método **Update**, **CancelUpdate** cancela quaisquer alterações feitas depois que **Edit** ou **AddNew** tiver sido invocado.

Verifique a propriedade **[EditMode](recordset-editmode-property-dao.md)** do **Recordset** para determinar se existe uma operação pendente que possa ser cancelada.

> [!NOTE]
> [!OBSERVAçãO] Usar o método **CancelUpdate** tem o mesmo efeito de mover para outro registro sem usar o método **[Update](recordset-update-method-dao.md)**, exceto pelo fato de que o registro atual não muda e várias propriedades, como **[BOF](recordset-bof-property-dao.md)** e **[EOF](recordset-eof-property-dao.md)**, não são atualizadas.


## <a name="example"></a>Exemplo

Este exemplo mostra como o método **CancelUpdate** é usado com o método **AddNew**.

```vb
    Sub CancelUpdateX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset 
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

