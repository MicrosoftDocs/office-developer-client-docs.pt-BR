---
title: Propriedade Field2.Size (DAO)
TOCTitle: Size Property
ms:assetid: e252759a-cea9-25cb-667d-80b422fbf97e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835700(v=office.15)
ms:contentKeyID: 48548282
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ffca40d22d77a604e4c0b794a8070fb444d44a32
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464472"
---
# <a name="field2size-property-dao"></a>Propriedade Field2.Size (DAO)


**Aplica-se a**: Access 2013 | Office 2013


Define ou retorna um valor que indica o tamanho máximo, em bytes, de um objeto **Field2**.

## <a name="syntax"></a>Sintaxe

*expressão* . Tamanho

*expressão* Uma variável que representa um objeto **Field2** .

## <a name="remarks"></a>Comentários

Para um objeto ainda não acrescentado à coleção **[Fields](fields-collection-dao.md)**, essa propriedade é de leitura/gravação.

Para campos (diferentes dos campos tipo Memorando) que contêm dados de caractere, a propriedade **Size** indica o número máximo de caracteres que o campo pode ter. Para campos numéricos, a propriedade **Size** indica quantos bytes de repositório são necessários.

O uso da propriedade **Size** depende do objeto que contém a coleção **Fields** à qual o objeto **Field2** está acrescentado, como mostrado na tabela a seguir.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objeto acrescentado a</p></th>
<th><p>Uso</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Index</strong></p></td>
<td><p>Sem suporte</p></td>
</tr>
<tr class="even">
<td><p><strong>QueryDef</strong></p></td>
<td><p>Somente leitura</p></td>
</tr>
<tr class="odd">
<td><p><strong>Recordset</strong></p></td>
<td><p>Somente leitura</p></td>
</tr>
<tr class="even">
<td><p><strong>Relação</strong></p></td>
<td><p>Sem suporte</p></td>
</tr>
<tr class="odd">
<td><p><strong>TableDef</strong></p></td>
<td><p>Somente leitura</p></td>
</tr>
</tbody>
</table>


Quando você cria um objeto **Field2** com um tipo de dados diferente de Text, a configuração da propriedade **Type** automaticamente determina a configuração da propriedade **Size**; não é necessário defini-la. Para um objeto **Field2** com o tipo de dados Text, contudo, você pode definir **Size** para qualquer número inteiro até o tamanho máximo permito (255 para bancos de dados do mecanismo de bancos de dados do Microsoft Access). Se você não definir o tamanho, o campo será tão grande quanto o banco de dados permitir.

Para objetos **Field2** Long Binary e Memo, **Size** é sempre definido como 0. Use a propriedade **FieldSize** do objeto **Field2** para determinar o tamanho dos dados em um registro específico. O tamanho máximo de um campo Long Binary ou Memo é limitado apenas pelos recursos do sistema ou pelo tamanho máximo permitido pelo banco de dados.

## <a name="example"></a>Exemplo

Este exemplo demonstra a propriedade **Size** enumerando os nomes e os tamanhos dos objetos **Field2** na tabela Funcionários.

```vb
    Sub SizeX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim fldNew As Field2 
     Dim fldLoop As Field2 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs!Employees 
     
     With tdfEmployees 
     
     ' Create and append a new Field object to the 
     ' Employees table. 
     Set fldNew = .CreateField("FaxPhone") 
     fldNew.Type = dbText 
     fldNew.Size = 20 
     .Fields.Append fldNew 
     
     Debug.Print "TableDef: " & .Name 
     Debug.Print " Field.Name - Field.Type - Field.Size" 
     
     ' Enumerate Fields collection; print field names, 
     ' types, and sizes. 
     For Each fldLoop In .Fields 
     Debug.Print " " & fldLoop.Name & " - " & _ 
     fldLoop.Type & " - " & fldLoop.Size 
     Next fldLoop 
     
     ' Delete new field because this is a demonstration. 
     .Fields.Delete fldNew.Name 
     
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
