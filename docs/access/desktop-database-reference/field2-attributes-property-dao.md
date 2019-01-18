---
title: Propriedade Field2.Attributes (DAO)
TOCTitle: Attributes Property
ms:assetid: 08ae9b6b-21e4-9b7e-0852-cfc6639027a7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845025(v=office.15)
ms:contentKeyID: 48543102
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052896
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a655cfa5c6f0427b1a26a01f01e991564ab8e387
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700714"
---
# <a name="field2attributes-property-dao"></a>Propriedade Field2.Attributes (DAO)


**Aplica-se a**: Access 2013, o Office 2013


Define ou retorna um valor que indica uma ou mais características de um objeto **Field2**. **Long** de leitura/gravação.

## <a name="syntax"></a>Sintaxe

*expressão* . Atributos

*expressão* Uma variável que representa um objeto **Field2** .

## <a name="remarks"></a>Comentários

O valor especifica características do campo representadas pelo objeto **Field2** e pode ser uma combinação dessas constantes.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constant</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbAutoIncrField</strong></p></td>
<td><p>O valor do campo para novos registros é automaticamente incrementado em um inteiro Long exclusivo que não pode ser alterado (em um espaço de trabalho do Microsoft Access, aceito somente para tabelas de banco de dados do mecanismo de banco de dados do Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbDescending</strong></p></td>
<td><p>O campo é classificado em ordem decrescente (Z para A ou 100 para 0); essa opção se aplica a um objeto <strong>Field2</strong> em uma coleção <strong>Fields</strong> de um índice <strong>Index</strong>. Se você omitir essa constante, o campo será classificado em ordem crescente (A para Z ou 0 para 100). Esse é o valor padrão para os campos <strong>Index</strong> e <strong>TableDef</strong> (apenas espaços de trabalho do Microsoft Access)..</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbFixedField</strong></p></td>
<td><p>O tamanho do campo é fixo (padrão para campos numéricos).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbHyperlinkField</strong></p></td>
<td><p>O campo contém informações de hiperlink (apenas campos de memorando).</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSystemField</strong></p></td>
<td><p>O campo armazena informações de replicação para réplicas; não é possível excluir esse tipo de campo (apenas espaços de trabalho do Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbUpdatableField</strong></p></td>
<td><p>O valor do campo pode ser alterado.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbVariableField</strong></p></td>
<td><p>O tamanho do campo é variável (apenas campos de texto).</p></td>
</tr>
</tbody>
</table>


Para um objeto que não está acrescentado a uma coleção, essa propriedade é de leitura/gravação. Para um objeto **Field2** acrescentado, a disponibilidade da propriedade **Attributes** depende do objeto que contém a coleção **Fields**.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Se o objeto Fields pertencer a</p></th>
<th><p>Attributes serão</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Objeto <strong>Index</strong></p></td>
<td><p>Leitura/gravação até que o objeto <strong>TableDef</strong>, que contém o objeto <strong>Index</strong>, esteja acrescentando ao objeto <strong>Database</strong>; a propriedade é somente leitura.</p></td>
</tr>
<tr class="even">
<td><p>Objeto <strong>QueryDef</strong></p></td>
<td><p>Somente leitura</p></td>
</tr>
<tr class="odd">
<td><p>Objeto <strong>Recordset</strong></p></td>
<td><p>Somente leitura</p></td>
</tr>
<tr class="even">
<td><p>Objeto <strong>Relation</strong></p></td>
<td><p>Sem suporte</p></td>
</tr>
<tr class="odd">
<td><p>Objeto <strong>TableDef</strong></p></td>
<td><p>Leitura/gravação</p></td>
</tr>
</tbody>
</table>


Quando você define vários atributos, é possível combiná-los somando as constantes apropriadas. Qualquer valor inválido é ignorado sem gerar nenhum erro.

## <a name="example"></a>Exemplo

Este exemplo exibe a propriedade **Attributes** para os objetos **Field2**, **Relation** e **TableDef** no banco de dados Northwind.

```vb 
Sub AttributesX() 
 
 Dim dbsNorthwind As Database 
 Dim fldLoop As Field2 
 Dim relLoop As Relation 
 Dim tdfloop As TableDef 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind 
 
 ' Display the attributes of a TableDef object's 
 ' fields. 
 Debug.Print "Attributes of fields in " & _ 
 .TableDefs(0).Name & " table:" 
 For Each fldLoop In .TableDefs(0).Fields 
 Debug.Print " " & fldLoop.Name & " = " & _ 
 fldLoop.Attributes 
 Next fldLoop 
 
 ' Display the attributes of the Northwind database's 
 ' relations. 
 Debug.Print "Attributes of relations in " & _ 
 .Name & ":" 
 For Each relLoop In .Relations 
 Debug.Print " " & relLoop.Name & " = " & _ 
 relLoop.Attributes 
 Next relLoop 
 
 ' Display the attributes of the Northwind database's 
 ' tables. 
 Debug.Print "Attributes of tables in " & .Name & ":" 
 For Each tdfloop In .TableDefs 
 Debug.Print " " & tdfloop.Name & " = " & _ 
 tdfloop.Attributes 
 Next tdfloop 
 
 .Close 
 End With 
 
End Sub 
 
```

