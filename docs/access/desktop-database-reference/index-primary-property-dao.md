---
title: Propriedade Index.Primary (DAO)
TOCTitle: Primary property
ms:assetid: 90eda1cb-cf7f-9682-9b74-81c27a37af16
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197416(v=office.15)
ms:contentKeyID: 48546336
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052908
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ff99f60fce41c7fa7de604a5109e68f6f744e68a
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997641"
---
# <a name="indexprimary-property-dao"></a><span data-ttu-id="9aa5e-102">Propriedade Index.Primary (DAO)</span><span class="sxs-lookup"><span data-stu-id="9aa5e-102">Index.Primary property (DAO)</span></span>

<span data-ttu-id="9aa5e-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="9aa5e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9aa5e-104">Define ou retorna um valor que indica se um objeto **[Index](index-object-dao.md)** representa um índice de chave primária de uma tabela (somente em espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="9aa5e-104">Sets or returns a value that indicates whether an **[Index](index-object-dao.md)** object represents a primary key index for a table (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="9aa5e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9aa5e-105">Syntax</span></span>

<span data-ttu-id="9aa5e-106">*expressão* . Principal</span><span class="sxs-lookup"><span data-stu-id="9aa5e-106">*expression* .Primary</span></span>

<span data-ttu-id="9aa5e-107">*expressão* Uma variável que representa um objeto **Index** .</span><span class="sxs-lookup"><span data-stu-id="9aa5e-107">*expression* A variable that represents an **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9aa5e-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="9aa5e-108">Remarks</span></span>

<span data-ttu-id="9aa5e-p101">A definição da propriedade **Primary** é leitura/gravação para um novo objeto **Index** ainda não acrescentado a uma coleção e somente para um objeto **Index** existente em uma coleção **[Indexes](indexes-collection-dao.md)**. Se o objeto **Index** for acrescentado ao objeto **[TableDef](tabledef-object-dao.md)**, mas o objeto **TableDef** não estiver acrescentado à coleção **[TableDefs](tabledefs-collection-dao.md)**, a propriedade **Index** será leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="9aa5e-p101">The **Primary** property setting is read/write for a new **Index** object not yet appended to a collection and read-only for an existing **Index** object in an **[Indexes](indexes-collection-dao.md)** collection. If the **Index** object is appended to the **[TableDef](tabledef-object-dao.md)** object but the **TableDef** object isn't appended to the **[TableDefs](tabledefs-collection-dao.md)** collection, the **Index** property is read/write.</span></span>

<span data-ttu-id="9aa5e-p102">Um índice de chave primária é composto de um ou vários campos que identificam exclusivamente todos os registros em uma tabela na ordem predefinida. Como o campo índice deve ser exclusivo, a propriedade **[Unique](index-unique-property-dao.md)** do objeto **Index** será definida como **True**. Se o índice de chave primária for composto de mais de um campo, cada campo conterá valores duplicados, mas cada combinação de valores de todos os campos indexados deverá ser exclusiva. Um índice de chave primária é composto de uma chave para tabela e geralmente contém os mesmos campos da chave primária.</span><span class="sxs-lookup"><span data-stu-id="9aa5e-p102">A primary key index consists of one or more fields that uniquely identify all records in a table in a predefined order. Because the index field must be unique, the **[Unique](index-unique-property-dao.md)** property of the **Index** object is set to **True**. If the primary key index consists of more than one field, each field can contain duplicate values, but each combination of values from all the indexed fields must be unique. A primary key index consists of a key for the table and usually contains the same fields as the primary key.</span></span>

> [!NOTE]
> <span data-ttu-id="9aa5e-p103">[!OBSERVAçãO] Não é necessário criar índices para tabelas mas, em tabelas grandes e não indexadas, o acesso a um registro específico pode demorar muito tempo. A propriedade **[Attributes](field-attributes-property-dao.md)** de cada objeto **[Field](field-object-dao.md)** no objeto **Index** determina a ordem dos registros e, como consequência, determina as técnicas de acesso para o uso desse índice. Quando você criar uma nova tabela no banco de dados, será uma boa ideia criar um índice em um ou vários campos que identifiquem exclusivamente cada registro e depois definir a propriedade **Primary** do objeto **Index** como **True**.</span><span class="sxs-lookup"><span data-stu-id="9aa5e-p103">You don't have to create indexes for tables, but in large, unindexed tables, accessing a specific record can take a long time. The **[Attributes](field-attributes-property-dao.md)** property of each **[Field](field-object-dao.md)** object in the **Index** object determines the order of records and consequently determines the access techniques to use for that index. When you create a new table in your database, it's a good idea to create an index on one or more fields that uniquely identify each record, and then set the **Primary** property of the **Index** object to **True**.</span></span>

<span data-ttu-id="9aa5e-118">Quando você definir uma chave primária para uma tabela, a chave primária será automaticamente definida como o índice da chave primária para a tabela.</span><span class="sxs-lookup"><span data-stu-id="9aa5e-118">When you set a primary key for a table, the primary key is automatically defined as the primary key index for the table.</span></span>

## <a name="example"></a><span data-ttu-id="9aa5e-119">Exemplo</span><span class="sxs-lookup"><span data-stu-id="9aa5e-119">Example</span></span>

<span data-ttu-id="9aa5e-p104">Este exemplo usa a propriedade **Primary** para designar um novo objeto **Index** em um novo objeto **TableDef** como o objeto **Index** primário dessa tabela. Observe que a definição da propriedade **Primary** como **True** também define automaticamente as propriedades **Unique** e **Required** como **True**.</span><span class="sxs-lookup"><span data-stu-id="9aa5e-p104">This example uses the **Primary** property to designate a new **Index** in a new **TableDef** as the primary **Index** for that table. Note that setting the **Primary** property to **True** automatically sets **Unique** and **Required** properties to **True** as well.</span></span>

```vb
    Sub PrimaryX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfNew As TableDef 
     Dim idxNew As Index 
     Dim idxLoop As Index 
     Dim fldLoop As Field 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     ' Create and append a new TableDef object to the 
     ' TableDefs collection of the Northwind database. 
     Set tdfNew = dbsNorthwind.CreateTableDef("NewTable") 
     tdfNew.Fields.Append tdfNew.CreateField("NumField", _ 
     dbLong, 20) 
     tdfNew.Fields.Append tdfNew.CreateField("TextField", _ 
     dbText, 20) 
     dbsNorthwind.TableDefs.Append tdfNew 
     
     With tdfNew 
     ' Create and append a new Index object to the 
     ' Indexes collection of the new TableDef object. 
     Set idxNew = .CreateIndex("NumIndex") 
     idxNew.Fields.Append idxNew.CreateField("NumField") 
     idxNew.Primary = True 
     .Indexes.Append idxNew 
     Set idxNew = .CreateIndex("TextIndex") 
     idxNew.Fields.Append idxNew.CreateField("TextField") 
     .Indexes.Append idxNew 
     
     Debug.Print .Indexes.Count & " Indexes in " & _ 
     .Name & " TableDef" 
     
     ' Enumerate Indexes collection. 
     For Each idxLoop In .Indexes 
     
     With idxLoop 
     Debug.Print " " & .Name 
     
     ' Enumerate Fields collection of each Index 
     ' object. 
     Debug.Print " Fields" 
     For Each fldLoop In .Fields 
     Debug.Print " " & fldLoop.Name 
     Next fldLoop 
     
     ' Enumerate Properties collection of each 
     ' Index object. 
     Debug.Print " Properties" 
     For Each prpLoop In .Properties 
     Debug.Print " " & prpLoop.Name & _ 
     " = " & IIf(prpLoop = "", "[empty]", _ 
     prpLoop) 
     Next prpLoop 
     End With 
     
     Next idxLoop 
     
     End With 
     
     dbsNorthwind.TableDefs.Delete tdfNew.Name 
     dbsNorthwind.Close 
     
    End Sub
```
