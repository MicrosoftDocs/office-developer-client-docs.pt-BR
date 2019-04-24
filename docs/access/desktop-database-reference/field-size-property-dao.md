---
title: Propriedade Field. Size (DAO)
TOCTitle: Size Property
ms:assetid: 15e25201-87b6-f62f-ff18-259414a47891
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845510(v=office.15)
ms:contentKeyID: 48543419
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052878
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 16ce8a9e63c18ded2738035f23e9a1baeff4cc8c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293011"
---
# <a name="fieldsize-property-dao"></a>Propriedade Field. Size (DAO)


**Aplica-se ao:** Access 2013, Office 2013


Define ou retorna um valor que indica o tamanho máximo, em bytes, de um objeto **[Field](field-object-dao.md)**.

## <a name="syntax"></a>Sintaxe

*expressão* . Porte

*expressão* Uma variável que representa um objeto **Field** .

## <a name="remarks"></a>Comentários

Para um objeto ainda não acrescentado à coleção **[Fields](fields-collection-dao.md)**, essa propriedade é de leitura/gravação.

Para os campos (diferentes dos campos de tipo Memorando) que contêm dados do caractere, a propriedade **Size** indica o número máximo de caracteres que o campo pode manter. Para os campos numéricos, a propriedade **Size** indica quantos bytes de repositório serão necessários.

O uso da propriedade **Size** depende do objeto que contém a coleção **Fields** à qual o objeto **Field** foi acrescentado, conforme mostra a tabela a seguir.

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
<td><p><strong>Índice</strong></p></td>
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


Quando você criar um objeto **Field** com um tipo de dados diferente de Texto, a definição da propriedade **[Type](field-type-property-dao.md)** determinará automaticamente a definição da propriedade **Size**; não será necessário defini-la. Para um objeto **Field** com o tipo de dados Texto, no entanto, você deve definir **Size** como um número inteiro até o tamanho de texto máximo (255 para o banco de dados do Microsoft Access). Se você não definir o tamanho, o campo será tão grande quanto o banco de dados permitir.

Para objetos Long Binary e Memo **Field**, **Size** será sempre definido como 0. Use a propriedade **[FieldSize](field-fieldsize-property-dao.md)** do objeto **Field** para determinar o tamanho dos dados em um registro específico. O tamanho máximo de um campo Long Binary ou Memo estará limitado apenas pelos recursos do sistema ou pelo tamanho máximo que o banco de dados permitir.

## <a name="example"></a>Exemplo

Este exemplo demonstra a propriedade **Size** pela enumeração dos nomes e dos tamanhos dos objetos **Field** na tabela Funcionários.

```vb
    Sub SizeX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim fldNew As Field 
     Dim fldLoop As Field 
     
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
