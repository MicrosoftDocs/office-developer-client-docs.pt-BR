---
title: Propriedade Relationtable. ForeignTable (DAO)
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
localization_priority: Normal
ms.openlocfilehash: fc7ee9b5bc832cc2a125024c592db2c7b13e72f7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307043"
---
# <a name="relationforeigntable-property-dao"></a><span data-ttu-id="d600e-102">Propriedade Relationtable. ForeignTable (DAO)</span><span class="sxs-lookup"><span data-stu-id="d600e-102">Relation.ForeignTable property (DAO)</span></span>


<span data-ttu-id="d600e-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d600e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d600e-104">Define ou retorna o nome da tabela externa em uma relação (apenas espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="d600e-104">Sets or returns the name of the foreign table in a relationship (Microsoft Access workspaces only).</span></span> <span data-ttu-id="d600e-105">.</span><span class="sxs-lookup"><span data-stu-id="d600e-105"></span></span>

## <a name="syntax"></a><span data-ttu-id="d600e-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d600e-106">Syntax</span></span>

<span data-ttu-id="d600e-107">*expressão* . ForeignTable</span><span class="sxs-lookup"><span data-stu-id="d600e-107">*expression* .ForeignTable</span></span>

<span data-ttu-id="d600e-108">*expressão* Uma variável que representa um objeto **relation** .</span><span class="sxs-lookup"><span data-stu-id="d600e-108">*expression* A variable that represents a **Relation** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d600e-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="d600e-109">Remarks</span></span>

<span data-ttu-id="d600e-110">Essa propriedade é leitura/gravação para um novo objeto **[Relation](relation-object-dao.md)** ainda não acrescentado a uma coleção e somente leitura para um objeto **Relation** existente na coleção **[Relations](relations-collection-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="d600e-110">This property is read/write for a new **[Relation](relation-object-dao.md)** object not yet appended to a collection and read-only for an existing **Relation** object in the **[Relations](relations-collection-dao.md)** collection.</span></span>

<span data-ttu-id="d600e-111">A definição da propriedade **ForeignTable** de um objeto **Relation** é a definição da propriedade **[Name](connection-name-property-dao.md)** de **[TableDef](tabledef-object-dao.md)** ou **[QueryDef](querydef-object-dao.md)** que representa a tabela ou consulta externa; a definição da propriedade **[Table](relation-table-property-dao.md)** é a definição de propriedade **Name** do objeto **TableDef** ou **QueryDef** que representa a tabela primária ou consulta.</span><span class="sxs-lookup"><span data-stu-id="d600e-111">The **ForeignTable** property setting of a **Relation** object is the **[Name](connection-name-property-dao.md)** property setting of the **[TableDef](tabledef-object-dao.md)** or **[QueryDef](querydef-object-dao.md)** object that represents the foreign table or query; the **[Table](relation-table-property-dao.md)** property setting is the **Name** property setting of the **TableDef** or **QueryDef** object that represents the primary table or query.</span></span>

<span data-ttu-id="d600e-p102">Por exemplo, se você tiver uma lista dos códigos de peça válidos (em um campo chamado PartNo) armazenada em uma tabela ValidParts, poderá estabelecer uma relação com uma tabela OrderItem de forma que, se um código de peça for inserido na tabela OrderItem, ele já deverá existir na tabela ValidParts. Se o código de peça não existir na tabela ValidParts e você não tiver definido a propriedade **[Attributes](field-attributes-property-dao.md)** do objeto **Relation** como **dbRelationDontEnforce**, ocorrerá um erro interceptável.</span><span class="sxs-lookup"><span data-stu-id="d600e-p102">For example, if you had a list of valid part codes (in a field named PartNo) stored in a ValidParts table, you could establish a relationship with an OrderItem table such that if a part code were entered into the OrderItem table, it would have to already be in the ValidParts table. If the part code didn't exist in the ValidParts table and you had not set the **[Attributes](field-attributes-property-dao.md)** property of the **Relation** object to **dbRelationDontEnforce**, a trappable error would occur.</span></span>

<span data-ttu-id="d600e-p103">Nesse caso, a tabela ValidParts seria uma tabela primária e, por esse motivo, a propriedade **Table** do objeto **Relation** seria definida como ValidParts e a propriedade **ForeignTable** do objeto **Relation** seria definida como OrderItem. As propriedades **Name** e **ForeignName** do objeto **Field** na coleção **Fields** do objeto **Relation** seriam definidas como PartNo.</span><span class="sxs-lookup"><span data-stu-id="d600e-p103">In this case, the ValidParts table is the primary table, so the **Table** property of the **Relation** object would be set to ValidParts and the **ForeignTable** property of the **Relation** object would be set to OrderItem. The **Name** and **ForeignName** properties of the **Field** object in the **Relation** object's **Fields** collection would be set to PartNo.</span></span>

## <a name="example"></a><span data-ttu-id="d600e-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="d600e-116">Example</span></span>

<span data-ttu-id="d600e-117">Esse exemplo mostra como as propriedades **Table**, **ForeignTable** e **ForeignName** definem os termos de um **Relation** entre as duas tabelas.</span><span class="sxs-lookup"><span data-stu-id="d600e-117">This example shows how the **Table**, **ForeignTable**, and **ForeignName** properties define the terms of a **Relation** between two tables.</span></span>

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
