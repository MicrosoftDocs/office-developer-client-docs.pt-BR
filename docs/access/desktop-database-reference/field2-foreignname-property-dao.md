---
title: Propriedade Field2.ForeignName (DAO)
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
ms.openlocfilehash: eff81bf8d2e7f7f040611ffc1aafdedff1e35ddf
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874045"
---
# <a name="field2foreignname-property-dao"></a><span data-ttu-id="eefd1-102">Propriedade Field2.ForeignName (DAO)</span><span class="sxs-lookup"><span data-stu-id="eefd1-102">Field2.ForeignName Property (DAO)</span></span>


<span data-ttu-id="eefd1-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="eefd1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="eefd1-104">Define ou retorna um valor que especifica o nome do objeto **Field2** em uma tabela externa que corresponde a um campo em uma tabela principal de uma relação (apenas espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="eefd1-104">Sets or returns a value that specifies the name of the **Field2** object in a foreign table that corresponds to a field in a primary table for a relationship (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="eefd1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eefd1-105">Syntax</span></span>

<span data-ttu-id="eefd1-106">*expressão* . ForeignName</span><span class="sxs-lookup"><span data-stu-id="eefd1-106">*expression* .ForeignName</span></span>

<span data-ttu-id="eefd1-107">*expressão* Uma variável que representa um objeto **Field2** .</span><span class="sxs-lookup"><span data-stu-id="eefd1-107">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="eefd1-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="eefd1-108">Remarks</span></span>

<span data-ttu-id="eefd1-p101">Se o objeto **[Relation](relation-object-dao.md)** não estiver acrescentado ao **[Database](database-object-dao.md)**, mas o **Field2** for acrescentado ao objeto **Relation**, a propriedade **ForeignName** será de leitura/gravação. Depois que o objeto **Relation** é acrescentado ao banco de dados, a propriedade **ForeignName** é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="eefd1-p101">If the **[Relation](relation-object-dao.md)** object isn't appended to the **[Database](database-object-dao.md)**, but the **Field2** is appended to the **Relation** object, the **ForeignName** property is read/write. Once the **Relation** object is appended to the database, the **ForeignName** property is read-only.</span></span>

<span data-ttu-id="eefd1-111">Somente um objeto **Field2** que pertence à coleção **Fields** de um objeto **Relation** pode aceitar a propriedade **ForeignName**.</span><span class="sxs-lookup"><span data-stu-id="eefd1-111">Only a **Field2** object that belongs to the **Fields** collection of a **Relation** object can support the **ForeignName** property.</span></span>

<span data-ttu-id="eefd1-p102">As configurações das propriedades **[Name](connection-name-property-dao.md)** e **ForeignName** de um objeto **Field2** especificam os nomes dos campos correspondentes nas tabelas principal e externa de uma relação. As configurações das propriedades **[Table](relation-table-property-dao.md)** e **[ForeignTable](relation-foreigntable-property-dao.md)** de um objeto **Relation** determinam as tabelas principal e externa de uma relação.</span><span class="sxs-lookup"><span data-stu-id="eefd1-p102">The **[Name](connection-name-property-dao.md)** and **ForeignName** property settings for a **Field2** object specify the names of the corresponding fields in the primary and foreign tables of a relationship. The **[Table](relation-table-property-dao.md)** and **[ForeignTable](relation-foreigntable-property-dao.md)** property settings for a **Relation** object determine the primary and foreign tables of a relationship.</span></span>

<span data-ttu-id="eefd1-p103">Por exemplo, se você tiver uma lista dos códigos de peça válidos (em um campo chamado PartNo) armazenada em uma tabela ValidParts, poderá estabelecer uma relação com uma tabela OrderItem de forma que, se um código de peça for inserido na tabela OrderItem, ele já deverá existir na tabela ValidParts. Se o código de peça não existir na tabela ValidParts e você não tiver definido a propriedade **[Attributes](field-attributes-property-dao.md)** do objeto **Relation** como **dbRelationDontEnforce**, ocorrerá um erro interceptável.</span><span class="sxs-lookup"><span data-stu-id="eefd1-p103">For example, if you had a list of valid part codes (in a field named PartNo) stored in a ValidParts table, you could establish a relationship with an OrderItem table such that if a part code were entered into the OrderItem table, it would have to already exist in the ValidParts table. If the part code didn't exist in the ValidParts table and you had not set the **[Attributes](field-attributes-property-dao.md)** property of the **Relation** object to **dbRelationDontEnforce**, a trappable error would occur.</span></span>

<span data-ttu-id="eefd1-p104">Nesse caso, a tabela ValidParts é a tabela externa, então a propriedade **ForeignTable** do objeto **Relation** será definida como ValidParts e a propriedade **Table** do objeto **Relation** será definida como OrderItem. As propriedades **Name** e **ForeignName** do objeto **Field2** na coleção **Fields** do objeto **Relation** será definida como PartNo.</span><span class="sxs-lookup"><span data-stu-id="eefd1-p104">In this case, the ValidParts table is the foreign table, so the **ForeignTable** property of the **Relation** object would be set to ValidParts and the **Table** property of the **Relation** object would be set to OrderItem. The **Name** and **ForeignName** properties of the **Field2** object in the **Relation** object's **Fields** collection would be set to PartNo.</span></span>

## <a name="example"></a><span data-ttu-id="eefd1-118">Exemplo</span><span class="sxs-lookup"><span data-stu-id="eefd1-118">Example</span></span>

<span data-ttu-id="eefd1-119">Esse exemplo mostra como as propriedades **Table**, **ForeignTable** e **ForeignName** definem os termos de um **Relation** entre as duas tabelas.</span><span class="sxs-lookup"><span data-stu-id="eefd1-119">This example shows how the **Table**, **ForeignTable**, and **ForeignName** properties define the terms of a **Relation** between two tables.</span></span>

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
