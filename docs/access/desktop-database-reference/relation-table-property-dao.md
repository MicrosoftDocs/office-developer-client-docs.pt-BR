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
# <a name="relationtable-property-dao"></a><span data-ttu-id="47035-102">Propriedade Relation.Table (DAO)</span><span class="sxs-lookup"><span data-stu-id="47035-102">Relation.Table property (DAO)</span></span>


<span data-ttu-id="47035-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="47035-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="47035-p101">Indica o nome de uma tabela primária do objeto **[Relation](relation-object-dao.md)**. Isso deve ser igual à definição da propriedade **[Name](connection-name-property-dao.md)** de um objeto **[TableDef](tabledef-object-dao.md)** ou **[QueryDef](querydef-object-dao.md)** (somente em espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="47035-p101">Indicates the name of a **[Relation](relation-object-dao.md)** object's primary table. This should be equal to the **[Name](connection-name-property-dao.md)** property setting of a **[TableDef](tabledef-object-dao.md)** or **[QueryDef](querydef-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="47035-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="47035-106">Syntax</span></span>

<span data-ttu-id="47035-107">*expressão* . Tabela</span><span class="sxs-lookup"><span data-stu-id="47035-107">*expression* .Table</span></span>

<span data-ttu-id="47035-108">*expressão* Uma variável que representa um **objeto Relation** .</span><span class="sxs-lookup"><span data-stu-id="47035-108">*expression* A variable that represents a **Relation** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="47035-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="47035-109">Remarks</span></span>

<span data-ttu-id="47035-110">A definição da propriedade **Table** é leitura/gravação para um novo objeto **Relation** ainda não acrescentado à coleção e somente leitura para um objeto **Relation** existente em uma coleção **[Relations](relations-collection-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="47035-110">The **Table** property setting is read/write for a new **Relation** object not yet appended to a collection and read-only for an existing **Relation** object in a **[Relations](relations-collection-dao.md)** collection.</span></span>

<span data-ttu-id="47035-p102">Use a propriedade **Table** com a propriedade **[ForeignTable](relation-foreigntable-property-dao.md)** para definir um objeto **Relation**, que represente a relação entre os campos de duas tabelas ou consultas. Defina a propriedade **Table** com a configuração da propriedade **Name** do objeto primário **TableDef** ou **QueryDef** e defina a propriedade **ForeignTable** com a configuração da propriedade **Name** do objeto externo (de referência) **TableDef** ou **QueryDef**. A propriedade **[Attributes](field-attributes-property-dao.md)** determina o tipo de relação entre os dois objetos.</span><span class="sxs-lookup"><span data-stu-id="47035-p102">Use the **Table** property with the **[ForeignTable](relation-foreigntable-property-dao.md)** property to define a **Relation** object, which represents the relationship between fields in two tables or queries. Set the **Table** property to the **Name** property setting of the primary **TableDef** or **QueryDef** object, and set the **ForeignTable** property to the **Name** property setting of the foreign (referencing) **TableDef** or **QueryDef** object. The **[Attributes](field-attributes-property-dao.md)** property determines the type of relationship between the two objects.</span></span>

<span data-ttu-id="47035-p103">Por exemplo, se você tiver uma lista dos códigos de peça válidos (em um campo chamado PartNo) armazenada em uma tabela ValidParts, poderá estabelecer uma relação um-para-muitos com uma tabela OrderItem, de tal forma que, se um código de peça for inserido na tabela OrderItem, ele já deverá existir na tabela ValidParts. Se o código de peça não existir na tabela ValidParts e você não tiver definido a propriedade **Attributes** do objeto **Relation** como **dbRelationDontEnforce**, ocorrerá um erro interceptável.</span><span class="sxs-lookup"><span data-stu-id="47035-p103">For example, if you had a list of valid part codes (in a field named PartNo) stored in a ValidParts table, you could establish a one-to-many relationship with an OrderItem table such that if a part code were entered into the OrderItem table, it would have to already be in the ValidParts table. If the part code didn't exist in the ValidParts table and you had not set the **Attributes** property of the **Relation** object to **dbRelationDontEnforce**, a trappable error would occur.</span></span>

<span data-ttu-id="47035-p104">Nesse caso, a tabela ValidParts seria uma tabela primária e, por esse motivo, a propriedade **Table** do objeto **Relation** seria definida como ValidParts e a propriedade **ForeignTable** do objeto **Relation** seria definida como OrderItem. As propriedades **Name** e **ForeignName** do objeto **[Field](field-object-dao.md)** na coleção [**Fields**](fields-collection-dao.md) do objeto **Relation** seriam definidas como PartNo.</span><span class="sxs-lookup"><span data-stu-id="47035-p104">In this case, the ValidParts table is the primary table, so the **Table** property of the **Relation** object would be set to ValidParts and the **ForeignTable** property of the **Relation** object would be set to OrderItem. The **Name** and **ForeignName** properties of the **[Field](field-object-dao.md)** object in the **Relation** object's **[Fields](fields-collection-dao.md)** collection would be set to PartNo.</span></span>

## <a name="example"></a><span data-ttu-id="47035-118">Exemplo</span><span class="sxs-lookup"><span data-stu-id="47035-118">Example</span></span>

<span data-ttu-id="47035-119">Esse exemplo mostra como as propriedades **Table**, **ForeignTable** e **ForeignName** definem os termos de um **Relation** entre as duas tabelas.</span><span class="sxs-lookup"><span data-stu-id="47035-119">This example shows how the **Table**, **ForeignTable**, and **ForeignName** properties define the terms of a **Relation** between two tables.</span></span>

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
