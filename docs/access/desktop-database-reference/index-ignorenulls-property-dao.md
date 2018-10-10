---
title: Propriedade Index.IgnoreNulls (DAO)
TOCTitle: IgnoreNulls Property
ms:assetid: f49f17b8-d7c1-18ab-07a8-e1be61488519
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836698(v=office.15)
ms:contentKeyID: 48548694
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052931
f1_categories:
- Office.Version=v15
ms.openlocfilehash: b6c190b7a61e26ff6e4abedc1a19bde26a1de426
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463826"
---
# <a name="indexignorenulls-property-dao"></a>Propriedade Index.IgnoreNulls (DAO)


**Aplica-se a**: Access 2013 | Office 2013

Define ou retorna um valor que indica se os registros com valores Null nos campos de índice têm entradas de índice (somente nos espaços de trabalho do Microsoft Access ).

## <a name="syntax"></a>Sintaxe

*expressão* . IgnoreNulls

*expressão* Uma variável que representa um objeto **Index** .

## <a name="remarks"></a>Comentários

Essa propriedade é leitura/gravação para um novo objeto **[Index](index-object-dao.md)** ainda não acrescentado a uma coleção e somente leitura para um objeto **Index** existente em uma coleção **[Indexes](indexes-collection-dao.md)**.

Para acelerar o processo de pesquisa dos registros, defina um índice para um campo. Se você permitir entradas **null** em um campo indexado e esperar que muitas das entradas sejam **null**, defina a propriedade **IgnoreNulls** do objeto **Index** como **True** para reduzir a quantidade de espaço usada pelo índice.

A definição da propriedade **IgnoreNulls** e a definição da propriedade **[Required](field-required-property-dao.md)** em conjunto determinam se o registro com o valor de índice **null** terá uma entrada de índice.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Se IgnoreNulls for</p></th>
<th><p>e Required for</p></th>
<th><p>Então</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>True</p></td>
<td><p>False</p></td>
<td><p>Um valor nulo é permitido no campo de índice; nenhuma entrada de índice foi adicionada.</p></td>
</tr>
<tr class="even">
<td><p>False</p></td>
<td><p>False</p></td>
<td><p>Um valor nulo é permitido no campo de índice; entrada de índice adicionada.</p></td>
</tr>
<tr class="odd">
<td><p>True or False</p></td>
<td><p>True</p></td>
<td><p>Um valor nulo não é permitido no campo de índice; nenhuma entrada de índice foi adicionada.</p></td>
</tr>
</tbody>
</table>


## <a name="example"></a>Exemplo

Este exemplo define a propriedade **IgnoreNulls** de um novo **Index** como **True** ou **False** com base na entrada do usuário e depois demonstra o efeito em um **Recordset** com um registro cujo campo de chave contém um valor **Null**.

```vb
    Sub IgnoreNullsX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxNew As Index 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create a new Index object. 
     Set idxNew = .CreateIndex("NewIndex") 
     idxNew.Fields.Append idxNew.CreateField("Country") 
     
     ' Set the IgnoreNulls property of the new Index object 
     ' based on the user's input. 
     Select Case MsgBox("Set IgnoreNulls to True?", _ 
     vbYesNoCancel) 
     Case vbYes 
     idxNew.IgnoreNulls = True 
     Case vbNo 
     idxNew.IgnoreNulls = False 
     Case Else 
     dbsNorthwind.Close 
     End 
     End Select 
     
     ' Append the new Index object to the Indexes 
     ' collection of the Employees table. 
     .Indexes.Append idxNew 
     .Indexes.Refresh 
     End With 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     With rstEmployees 
     ' Add a new record to the Employees table. 
     .AddNew 
     !FirstName = "Gary" 
     !LastName = "Haarsager" 
     .Update 
     
     ' Use the new index to set the order of the records. 
     .Index = idxNew.Name 
     .MoveFirst 
     
     Debug.Print "Index = " & .Index & _ 
     ", IgnoreNulls = " & idxNew.IgnoreNulls 
     Debug.Print " Country - Name" 
     
     ' Enumerate the Recordset. The value of the 
     ' IgnoreNulls property will determine if the newly 
     ' added record appears in the output. 
     Do While Not .EOF 
     Debug.Print " " & _ 
     IIf(IsNull(!Country), "[Null]", !Country) & _ 
     " - " & !FirstName & " " & !LastName 
     .MoveNext 
     Loop 
     
     ' Delete new record because this is a demonstration. 
     .Index = "" 
     .Bookmark = .LastModified 
     .Delete 
     .Close 
     End With 
     
     ' Delete new Index because this is a demonstration. 
     tdfEmployees.Indexes.Delete idxNew.Name 
     dbsNorthwind.Close 
     
    End Sub
```
