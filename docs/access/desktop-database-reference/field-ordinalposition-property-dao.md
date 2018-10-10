---
title: Propriedade Field.OrdinalPosition (DAO)
TOCTitle: OrdinalPosition Property
ms:assetid: 07f2344e-2a72-33d8-be47-b37d76ecca47
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845002(v=office.15)
ms:contentKeyID: 48543088
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7151ed1a03c0ce0cf0204716d19bb7cfd2b4f607
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462211"
---
# <a name="fieldordinalposition-property-dao"></a>Propriedade Field.OrdinalPosition (DAO)


**Aplica-se a**: Access 2013 | Office 2013

Define ou retorna a posição relativa de um objeto **[Field](field-object-dao.md)** em uma coleção **[Fields](fields-collection-dao.md)**.

## <a name="syntax"></a>Sintaxe

*expressão* . OrdinalPosition

*expressão* Uma variável que representa um objeto **Field** .

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
<td><p>							Objeto <strong>Index</strong></p></td>
<td><p>Sem suporte</p></td>
</tr>
<tr class="even">
<td><p>							Objeto <strong>QueryDef</strong></p></td>
<td><p>Somente leitura</p></td>
</tr>
<tr class="odd">
<td><p>							Objeto <strong>Recordset</strong></p></td>
<td><p>Somente leitura</p></td>
</tr>
<tr class="even">
<td><p>							Objeto <strong>Relation</strong></p></td>
<td><p>Sem suporte</p></td>
</tr>
<tr class="odd">
<td><p>							Objeto <strong>TableDef</strong></p></td>
<td><p>Leitura/gravação</p></td>
</tr>
</tbody>
</table>


Em geral, a posição ordinal de um objeto que você acrescenta a uma coleção depende da ordem na qual ele é acrescentado. O primeiro objeto acrescentado está na primeira posição (0), o segundo está na segunda posição (1) e assim por diante. O último objeto acrescentado está na posição ordinal count – 1, em que count é o número de objetos na coleção como especificado pela configuração da propriedade **[Count](containers-count-property-dao.md)**.

Use a propriedade **OrdinalPosition** para especificar a posição ordinal dos novos objetos **Field** que é diferente da ordem na qual foram acrescentados à uma coleção. Isso permite especificar a ordem dos campos para tabelas, consultas e recordsets quando você usá-los em um aplicativo. Por exemplo, a ordem na qual os campos são retornados em uma selecionar \* consulta é determinada pelos valores de propriedade **OrdinalPosition** atuais.

Redefina, de forma permanente, a ordem na qual os campos são retornados nos recordsets pela definição da propriedade **OrdinalPosition** para qualquer número inteiro positivo.

Dois ou mais objetos **Field** na mesma coleção podem ter o mesmo valor da propriedade **OrdinalPosition** e, nesse caso, serão colocados em ordem alfabética. Por exemplo, se você tem um campo denominado Idade definido como 4 e definir um segundo campo denominado Peso como 4, Peso será retornado depois de Idade.

Especifique um número maior que o número de campos menos 1. O campo será retornado em uma ordem relativa ao maior número. Por exemplo, se você definir a propriedade **OrdinalPosition** do campo como 20 (e existirem somente cinco campos) e já tiver definido a propriedade **OrdinalPosition** para outros dois campos como 10 e 30, respectivamente, o campo definido como 20 será retornado entre os campos definidos como 10 e 30.


> [!NOTE]
> <P>[!OBSERVAçãO] Mesmo se a coleção <STRONG>Fields</STRONG> de um <STRONG><A href="tabledef-object-dao.md">TableDef</A></STRONG> não tiver sido atualizado, a ordem do campo em um <STRONG><A href="recordset-object-dao.md">Recordset</A></STRONG> aberto a partir de <STRONG>TableDef</STRONG> refletirá os dados de <STRONG>OrdinalPosition</STRONG> do objeto <STRONG>TableDef</STRONG>. Um <STRONG>Recordset</STRONG> tipo tabela terá os mesmos dados de <STRONG>OrdinalPosition</STRONG> que a tabela base, mas nenhum outro tipo de <STRONG>Recordset</STRONG> terá novos dados <STRONG>OrdinalPosition</STRONG> (começando com 0) que seguirão a ordem determinada pelos dados <STRONG>OrdinalPosition</STRONG> de <STRONG>TableDef</STRONG>.</P>



## <a name="example"></a>Exemplo

Este exemplo altera os valores da propriedade **OrdinalPosition** no **TableDef** Funcionários para controlar a ordem **Field** em um **Recordset** resultante. Pela definição de **OrdinalPosition** de todos os **Fields** como 1, qualquer **Recordset** resultante colocará os **Fields** em ordem alfabética. Observe que os valores **OrdinalPosition** em **Recordset** não correspondem aos valores de **TableDef**, mas refletem apenas o resultado final das alterações de **TableDef**.

```vb
    Sub OrdinalPositionX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim aintPosition() As Integer 
     Dim astrFieldName() As String 
     Dim intTemp As Integer 
     Dim fldTemp As Field 
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
