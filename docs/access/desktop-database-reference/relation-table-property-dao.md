---
title: Propriedade Relation.Table (DAO)
TOCTitle: Table Property
ms:assetid: cc4f64ef-c4e9-1a14-9263-5f8220d89840
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834423(v=office.15)
ms:contentKeyID: 48547736
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053068
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 91a3262d92350618c2385013983020669b28ea5c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306990"
---
# <a name="relationtable-property-dao"></a>Propriedade Relation.Table (DAO)


**Aplica-se ao:** Access 2013, Office 2013

Indica o nome de uma tabela primária do objeto **[Relation](relation-object-dao.md)**. Isso deve ser igual à definição da propriedade **[Name](connection-name-property-dao.md)** de um objeto **[TableDef](tabledef-object-dao.md)** ou **[QueryDef](querydef-object-dao.md)** (somente em espaços de trabalho do Microsoft Access).

## <a name="syntax"></a>Sintaxe

*expressão* . Tabela

*expressão* Uma variável que representa um **objeto Relation** .

## <a name="remarks"></a>Comentários

A definição da propriedade **Table** é leitura/gravação para um novo objeto **Relation** ainda não acrescentado à coleção e somente leitura para um objeto **Relation** existente em uma coleção **[Relations](relations-collection-dao.md)**.

Use a propriedade **Table** com a propriedade **[ForeignTable](relation-foreigntable-property-dao.md)** para definir um objeto **Relation**, que represente a relação entre os campos de duas tabelas ou consultas. Defina a propriedade **Table** com a configuração da propriedade **Name** do objeto primário **TableDef** ou **QueryDef** e defina a propriedade **ForeignTable** com a configuração da propriedade **Name** do objeto externo (de referência) **TableDef** ou **QueryDef**. A propriedade **[Attributes](field-attributes-property-dao.md)** determina o tipo de relação entre os dois objetos.

Por exemplo, se você tiver uma lista dos códigos de peça válidos (em um campo chamado PartNo) armazenada em uma tabela ValidParts, poderá estabelecer uma relação um-para-muitos com uma tabela OrderItem, de tal forma que, se um código de peça for inserido na tabela OrderItem, ele já deverá existir na tabela ValidParts. Se o código de peça não existir na tabela ValidParts e você não tiver definido a propriedade **Attributes** do objeto **Relation** como **dbRelationDontEnforce**, ocorrerá um erro interceptável.

Nesse caso, a tabela ValidParts seria uma tabela primária e, por esse motivo, a propriedade **Table** do objeto **Relation** seria definida como ValidParts e a propriedade **ForeignTable** do objeto **Relation** seria definida como OrderItem. As propriedades **Name** e **ForeignName** do objeto **[Field](field-object-dao.md)** na coleção [**Fields**](fields-collection-dao.md) do objeto **Relation** seriam definidas como PartNo.

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
