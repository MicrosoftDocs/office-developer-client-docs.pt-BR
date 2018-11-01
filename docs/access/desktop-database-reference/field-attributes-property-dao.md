---
title: Propriedade Field.Attributes (DAO)
TOCTitle: Attributes Property
ms:assetid: 8e6f6afb-1a89-7315-c129-cf7ff19e0ca9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197380(v=office.15)
ms:contentKeyID: 48546287
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: df396935f88301a9fee9df580a5cee01705f68aa
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885777"
---
# <a name="fieldattributes-property-dao"></a>Propriedade Field.Attributes (DAO)


**Aplica-se a**: Access 2013, o Office 2013


Define ou retorna um valor que indica uma ou mais características de um objeto **[Field](field-object-dao.md)**. **Long** de leitura/gravação.

## <a name="syntax"></a>Sintaxe

*expressão* . Atributos

*expressão* Uma variável que representa um objeto **Field** .

## <a name="remarks"></a>Comentários

O valor especifica características do campo representadas pelo objeto **Field** e pode ser uma combinação dessas constantes.

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
<td><p>O campo é classificado em ordem decrescente (Z para A ou 100 para 0); essa opção se aplica a um objeto <strong>Field</strong> em uma coleção <strong>Fields</strong> de um índice <strong>Index</strong>. Se você omitir essa constante, o campo será classificado em ordem crescente (A para Z ou 0 para 100). Esse é o valor padrão para os campos <strong>Index</strong> e <strong>TableDef</strong> (apenas espaços de trabalho do Microsoft Access)..</p></td>
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
<td><p>O campo armazena informações de replicação para réplicas; não é possível excluir esse tipo de campo (apenas espaço de trabalho do Microsoft Access).</p></td>
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


Para um objeto que não está acrescentado a uma coleção, essa propriedade é de leitura/gravação. Para um objeto **Field** acrescentado, a disponibilidade da propriedade **Attributes** depende do objeto que contém a coleção **Fields**.

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

Este exemplo exibe a propriedade **Attributes** dos objetos **Field**, **Relation** e **TableDef** no banco de dados Northwind.

```vb 
Sub AttributesX() 
 
 Dim dbsNorthwind As Database 
 Dim fldLoop As Field 
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

