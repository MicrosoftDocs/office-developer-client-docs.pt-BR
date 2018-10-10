---
title: Propriedade Relation.ForeignTable (DAO)
TOCTitle: ForeignTable Property
ms:assetid: 3f896433-2962-1c7c-f5a2-4e030ba8d4a0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192853(v=office.15)
ms:contentKeyID: 48544401
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052989
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 33a7024b25ee74e38874eb7e2b598273f0daf248
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25461959"
---
# <a name="relationforeigntable-property-dao"></a>Propriedade Relation.ForeignTable (DAO)


**Aplica-se a**: Access 2013 | Office 2013

Define ou retorna o nome da tabela externa em uma relação (apenas espaços de trabalho do Microsoft Access). .

## <a name="syntax"></a>Sintaxe

*expressão* . ForeignTable

*expressão* Uma variável que representa um objeto **Relation** .

## <a name="remarks"></a>Comentários

Essa propriedade é leitura/gravação para um novo objeto **[Relation](relation-object-dao.md)** ainda não acrescentado a uma coleção e somente leitura para um objeto **Relation** existente na coleção **[Relations](relations-collection-dao.md)**.

A definição da propriedade **ForeignTable** de um objeto **Relation** é a definição da propriedade **[Name](connection-name-property-dao.md)** de **[TableDef](tabledef-object-dao.md)** ou **[QueryDef](querydef-object-dao.md)** que representa a tabela ou consulta externa; a definição da propriedade **[Table](relation-table-property-dao.md)** é a definição de propriedade **Name** do objeto **TableDef** ou **QueryDef** que representa a tabela primária ou consulta.

Por exemplo, se você tiver uma lista dos códigos de peça válidos (em um campo chamado PartNo) armazenada em uma tabela ValidParts, poderá estabelecer uma relação com uma tabela OrderItem de forma que, se um código de peça for inserido na tabela OrderItem, ele já deverá existir na tabela ValidParts. Se o código de peça não existir na tabela ValidParts e você não tiver definido a propriedade **[Attributes](field-attributes-property-dao.md)** do objeto **Relation** como **dbRelationDontEnforce**, ocorrerá um erro interceptável.

Nesse caso, a tabela ValidParts seria uma tabela primária e, por esse motivo, a propriedade **Table** do objeto **Relation** seria definida como ValidParts e a propriedade **ForeignTable** do objeto **Relation** seria definida como OrderItem. As propriedades **Name** e **ForeignName** do objeto **Field** na coleção **Fields** do objeto **Relation** seriam definidas como PartNo.

## <a name="example"></a>Exemplo

Esse exemplo mostra como as propriedades **Table**, **ForeignTable** e **ForeignName** definem os termos de um **Relation** entre as duas tabelas.

```vb 
    Sub ForeignNameX() 
     
     Dim dbsNorthwind As Database 
     Dim relLoop As Relation 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     Debug.Print "Relation" 
     Debug.Print " Table - Field" 
     Debug.Print " Primary (One) "; 
     Debug.Print ".Table - .Fields(0).Name" 
     Debug.Print " Foreign (Many) "; 
     Debug.Print ".ForeignTable - .Fields(0).ForeignName" 
     
     ' Enumerate the Relations collection of the Northwind 
     ' database to report on the property values of 
     ' the Relation objects and their Field objects. 
     For Each relLoop In dbsNorthwind.Relations 
     With relLoop 
     Debug.Print 
     Debug.Print .Name & " Relation" 
     Debug.Print " Table - Field" 
     Debug.Print " Primary (One) "; 
     Debug.Print .Table & " - " & .Fields(0).Name 
     Debug.Print " Foreign (Many) "; 
     Debug.Print .ForeignTable & " - " & _ 
     .Fields(0).ForeignName 
     End With 
     Next relLoop 
     
     dbsNorthwind.Close 
     
    End Sub
```
