---
title: Propriedade Field2.OrdinalPosition (DAO)
TOCTitle: OrdinalPosition Property
ms:assetid: 55d89611-ad07-990d-fc33-f81d59472430
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194179(v=office.15)
ms:contentKeyID: 48544937
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052899
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 600fe2855ba10e1ab36413f6395d3455bb7bd00b
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937054"
---
# <a name="field2ordinalposition-property-dao"></a>Propriedade Field2.OrdinalPosition (DAO)


**Aplica-se a**: Access 2013, o Office 2013


Define ou retorna a posição relativa de um objeto **Field2** dentro de uma coleção **[Fields](fields-collection-dao.md)**.

## <a name="syntax"></a>Sintaxe

*expressão* . OrdinalPosition

*expressão* Uma variável que representa um objeto **Field2** .

## <a name="remarks"></a>Comentários

Para um objeto ainda não acrescentado à coleção **Fields**, essa propriedade é de leitura/gravação.

O padrão é 0.

A disponibilidade da propriedade **OrdinalPosition** depende do objeto que contém a coleção **Fields**, conforme mostrado na tabela a seguir.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Se a coleção Fields pertencer a um</p></th>
<th><p>
OrdinalPosition será</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Objeto <strong>index</strong></p></td>
<td><p>Sem suporte</p></td>
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


Em geral, a posição ordinal de um objeto que você acrescenta a uma coleção depende da ordem na qual ele é acrescentado. O primeiro objeto acrescentado está na primeira posição (0), o segundo está na segunda posição (1) e assim por diante. O último objeto acrescentado está na posição ordinal count – 1, em que count é o número de objetos na coleção como especificado pela configuração da propriedade **[Count](containers-count-property-dao.md)**.

Você pode usar a propriedade **OrdinalPosition** para especificar uma posição ordinal para os novos objetos **Field2** que se difere da ordem na qual você acrescenta aqueles objetos a uma coleção. Isso permite que você especifique uma ordem de campo para suas tabelas, consultas e recordsets quando usá-los em um aplicativo. Por exemplo, a ordem na qual os campos são retornados em uma selecionar \* consulta é determinada pelos valores de propriedade **OrdinalPosition** atuais.

Você pode redefinir de modo permanente a ordem na qual os campos serão retornados em recordsets, configurando a propriedade **OrdinalPosition** para qualquer inteiro positivo.

Dois ou mais objetos **Field2** na mesma coleção podem ter o mesmo valor da propriedade **OrdinalPosition**, caso em que eles serão ordenados alfabeticamente. Por exemplo, se você tiver um campo chamado Idade definido como 4 e definir um segundo campo chamado Peso como 4, Peso será retornado depois de Idade.

É possível especificar um número maior que o número de campos menos 1. O campo será retornado em uma ordem relativa ao maior número. Por exemplo, se você definir a propriedade **OrdinalPosition** de um campo como 20 (e se houver apenas 5 campos) e definir a propriedade **OrdinalPosition** de dois outros campos como 10 e 30 respectivamente, o campo definido como 20 será retornado entre os campos definidos como 10 e 30.


> [!NOTE]
> Mesmo que não tenha sido atualizada a coleção **Fields** de um objeto **[TableDef](tabledef-object-dao.md)** , a ordem dos campos em um **[Recordset](recordset-object-dao.md)** aberto a partir de **TableDef** refletirá dados **OrdinalPosition** do objeto **TableDef** . Um **Recordset** tipo tabela terá os mesmos dados de **OrdinalPosition** que a tabela base, mas nenhum outro tipo de **Recordset** terá novos dados **OrdinalPosition** (começando com 0) que seguirão a ordem determinada pelos dados **OrdinalPosition** de **TableDef**.



## <a name="example"></a>Exemplo

Este exemplo altera os valores da propriedade **OrdinalPosition** em **TableDef** de Funcionário para controlar a ordem de **Field2** em um **Recordset** resultante. Configurando a **OrdinalPosition** de todos os **Fields** para 1, qualquer **Recordset** resultante ordenará **Fields** alfabeticamente. Observe que os valores de **OrdinalPosition** no **Recordset** não correspondem aos valores na **TableDef**, mas simplesmente refletem o resultado final das alterações de **TableDef**.

```vb
    Sub OrdinalPositionX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim aintPosition() As Integer 
     Dim astrFieldName() As String 
     Dim intTemp As Integer 
     Dim fldTemp As Field2 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs("Employees") 
     
     With tdfEmployees 
     ' Display and store original OrdinalPosition data. 
     Debug.Print _ 
     "Original OrdinalPosition data in TableDef." 
     ReDim aintPosition(0 To .Fields.Count - 1) As Integer 
     ReDim astrFieldName(0 To .Fields.Count - 1) As String 
     For intTemp = 0 To .Fields.Count - 1 
     aintPosition(intTemp) = _ 
     .Fields(intTemp).OrdinalPosition 
     astrFieldName(intTemp) = .Fields(intTemp).Name 
     Debug.Print , aintPosition(intTemp), _ 
     astrFieldName(intTemp) 
     Next intTemp 
     
     ' Change OrdinalPosition data. 
     For Each fldTemp In .Fields 
     fldTemp.OrdinalPosition = 1 
     Next fldTemp 
     
     ' Open new Recordset object to show how the 
     ' OrdinalPosition data has affected the record order. 
     Debug.Print _ 
     "OrdinalPosition data from resulting Recordset." 
     Set rstEmployees = dbsNorthwind.OpenRecordset( _ 
     "SELECT * FROM Employees") 
     For Each fldTemp In rstEmployees.Fields 
     Debug.Print , fldTemp.OrdinalPosition, fldTemp.Name 
     Next fldTemp 
     rstEmployees.Close 
     
     ' Restore original OrdinalPosition data because this is 
     ' a demonstration. 
     For intTemp = 0 To .Fields.Count - 1 
     .Fields(astrFieldName(intTemp)).OrdinalPosition = _ 
     aintPosition(intTemp) 
     Next intTemp 
     
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
