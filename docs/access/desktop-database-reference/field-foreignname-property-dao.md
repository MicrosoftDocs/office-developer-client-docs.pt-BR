---
title: Propriedade Field.ForeignName (DAO)
TOCTitle: ForeignName Property
ms:assetid: 5f412ab4-173b-9530-eb4f-71ee30bed9e3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194762(v=office.15)
ms:contentKeyID: 48545157
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7c340eee9972e8247654ec863ba0ef4588ef65f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293102"
---
# <a name="fieldforeignname-property-dao"></a>Propriedade Field.ForeignName (DAO)


**Aplica-se ao:** Access 2013, Office 2013

Define ou retorna um valor que especifica o nome do objeto **[Field](field-object-dao.md)** em uma tabela externa que corresponde a um campo em uma tabela primária de uma relação (somente nos espaços de trabalho do Microsoft Access).

## <a name="syntax"></a>Sintaxe

*expressão* . ForeignName

*expressão* Uma variável que representa um objeto de **Campo**.

## <a name="remarks"></a>Comentários

Se o objeto **[Relation](relation-object-dao.md)** não for acrescentado ao **[Database](database-object-dao.md)**, mas **Field** for acrescentado ao objeto **Relation**, a propriedade **ForeignName** será de leitura/gravação. Assim que o objeto **Relation** for acrescentado ao banco de dados, a propriedade **ForeignName** será somente leitura.

Somente um objeto **Field** que pertence à coleção **Fields** de um objeto **Relation** pode suportar a propriedade **ForeignName**.

As configurações das propriedades **[Name](connection-name-property-dao.md)** e **ForeignName** de um objeto **Field** especificam os nomes dos campos correspondentes nas tabelas primária e externa de uma relação. As configurações das propriedades **[Table](relation-table-property-dao.md)** e **[ForeignTable](relation-foreigntable-property-dao.md)** de um objeto **Relation** determinam as tabelas primária e externa de uma relação.

Por exemplo, se você tiver uma lista dos códigos de peça válidos (em um campo chamado PartNo) armazenada em uma tabela ValidParts, poderá estabelecer uma relação com uma tabela OrderItem de forma que, se um código de peça for inserido na tabela OrderItem, ele já deverá existir na tabela ValidParts. Se o código de peça não existir na tabela ValidParts e você não tiver definido a propriedade **[Attributes](field-attributes-property-dao.md)** do objeto **Relation** como **dbRelationDontEnforce**, ocorrerá um erro interceptável.

Nesse caso, a tabela ValidParts seria uma tabela externa e, por esse motivo, a propriedade **ForeignTable** do objeto **Relation** seria definida como ValidParts e a propriedade **Table** do objeto **Relation** seria definida como OrderItem. As propriedades **Name** e **ForeignName** do objeto **Field** da coleção **Fields** do objeto **Relation** seriam definidas como PartNo.

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
