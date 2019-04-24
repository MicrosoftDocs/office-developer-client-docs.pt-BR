---
title: Propriedade Campo2. ForeignName (DAO)
TOCTitle: ForeignName Property
ms:assetid: 76da233a-efb4-63cd-a2a2-d18d9e2fb2fb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196027(v=office.15)
ms:contentKeyID: 48545708
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052932
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a8368165f73fc52c51cf1503da9c2cc02e969bf4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292808"
---
# <a name="field2foreignname-property-dao"></a>Propriedade Campo2. ForeignName (DAO)


**Aplica-se ao:** Access 2013, Office 2013

Define ou retorna um valor que especifica o nome do objeto **Field2** em uma tabela externa que corresponde a um campo em uma tabela principal de uma relação (apenas espaços de trabalho do Microsoft Access).

## <a name="syntax"></a>Sintaxe

*expressão* . ForeignName

*expressão* Uma variável que representa um objeto **campo2** .

## <a name="remarks"></a>Comentários

Se o objeto **[Relation](relation-object-dao.md)** não estiver acrescentado ao **[Database](database-object-dao.md)**, mas o **Field2** for acrescentado ao objeto **Relation**, a propriedade **ForeignName** será de leitura/gravação. Depois que o objeto **Relation** é acrescentado ao banco de dados, a propriedade **ForeignName** é somente leitura.

Somente um objeto **Field2** que pertence à coleção **Fields** de um objeto **Relation** pode aceitar a propriedade **ForeignName**.

As configurações das propriedades **[Name](connection-name-property-dao.md)** e **ForeignName** de um objeto **Field2** especificam os nomes dos campos correspondentes nas tabelas principal e externa de uma relação. As configurações das propriedades **[Table](relation-table-property-dao.md)** e **[ForeignTable](relation-foreigntable-property-dao.md)** de um objeto **Relation** determinam as tabelas principal e externa de uma relação.

Por exemplo, se você tiver uma lista dos códigos de peça válidos (em um campo chamado PartNo) armazenada em uma tabela ValidParts, poderá estabelecer uma relação com uma tabela OrderItem de forma que, se um código de peça for inserido na tabela OrderItem, ele já deverá existir na tabela ValidParts. Se o código de peça não existir na tabela ValidParts e você não tiver definido a propriedade **[Attributes](field-attributes-property-dao.md)** do objeto **Relation** como **dbRelationDontEnforce**, ocorrerá um erro interceptável.

Nesse caso, a tabela ValidParts é a tabela externa, então a propriedade **ForeignTable** do objeto **Relation** será definida como ValidParts e a propriedade **Table** do objeto **Relation** será definida como OrderItem. As propriedades **Name** e **ForeignName** do objeto **Field2** na coleção **Fields** do objeto **Relation** será definida como PartNo.

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
