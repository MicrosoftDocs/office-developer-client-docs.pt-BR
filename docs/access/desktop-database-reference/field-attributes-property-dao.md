---
title: Propriedade de Field.Attributes (DAO)
TOCTitle: Attributes Property
ms:assetid: 8e6f6afb-1a89-7315-c129-cf7ff19e0ca9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197380(v=office.15)
ms:contentKeyID: 48546287
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 010c7a2aea777a93d1ced2d33d8743320dd05ada
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293151"
---
# <a name="fieldattributes-property-dao"></a>Propriedade de Field.Attributes (DAO)


**Aplica-se ao**: Access 2013, Office 2013


Define ou retorna um valor que indica uma ou mais características de um objeto **[Field](field-object-dao.md)**. **Long** de leitura/gravação.

## <a name="syntax"></a>Sintaxe

*expressão* .Attributes

*expressão* Uma variável que representa um objeto de **Campo**.

## <a name="remarks"></a>Comentários

O valor especifica as características do campo representado pelo objeto de **Campo** e pode ser uma combinação dessas constantes.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
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
<td><p>O campo é classificado em ordem decrescente (Z para A ou 100 para 0); essa opção se aplica a um objeto <strong>Field</strong> em uma coleção <strong>Fields</strong> de um índice <strong>Index</strong>. Se você omitir essa constante, o campo é classificado em ordem crescente (A até Z ou de 0 a 100). Este é o valor padrão para <strong>Índice</strong> e campos de <strong>TableDef</strong> (espaços de trabalho apenas do Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbFixedField</strong></p></td>
<td><p>O tamanho do campo é corrigido (padrão para Campos numéricos).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbHyperlinkField</strong></p></td>
<td><p>O campo contém informações sobre o hiperlink (apenas campos Memorando).</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSystemField</strong></p></td>
<td><p>O campo armazena informações de replicação de réplicas; Não é possível excluir esse tipo de campo (espaço de trabalho apenas do Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbUpdatableField</strong></p></td>
<td><p>O valor de campo pode ser alterado.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbVariableField</strong></p></td>
<td><p>O tamanho do campo é variável (somente campos de texto).</p></td>
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
<td><p>Objeto do <strong>Índice</strong> </p></td>
<td><p>Leitura/gravação até o objeto <strong>TableDef</strong> que o objeto do <strong>Índice</strong> é anexado ao seu anexo para o objeto de <strong>Banco de dados</strong>; em seguida, a propriedade é somente leitura.</p></td>
</tr>
<tr class="even">
<td><p>
						Objeto <strong>QueryDef</strong></p></td>
<td><p>Somente leitura</p></td>
</tr>
<tr class="odd">
<td><p>
						Objeto <strong>Recordset</strong></p></td>
<td><p>Somente leitura</p></td>
</tr>
<tr class="even">
<td><p>
						Objeto <strong>Relation</strong></p></td>
<td><p>Sem suporte</p></td>
</tr>
<tr class="odd">
<td><p>
						Objeto <strong>TableDef</strong></p></td>
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

