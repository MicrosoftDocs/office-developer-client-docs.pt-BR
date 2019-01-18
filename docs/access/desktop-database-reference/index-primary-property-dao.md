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
localization_priority: Normal
ms.openlocfilehash: da0d28a5599dadc9432b38ab6155e53e884e4838
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713370"
---
# <a name="indexprimary-property-dao"></a>Propriedade Index.Primary (DAO)

**Aplica-se a**: Access 2013, o Office 2013

Define ou retorna um valor que indica se um objeto **[Index](index-object-dao.md)** representa um índice de chave primária de uma tabela (somente em espaços de trabalho do Microsoft Access).

## <a name="syntax"></a>Sintaxe

*expressão* . Principal

*expressão* Uma variável que representa um objeto **Index** .

## <a name="remarks"></a>Comentários

A definição da propriedade **Primary** é leitura/gravação para um novo objeto **Index** ainda não acrescentado a uma coleção e somente para um objeto **Index** existente em uma coleção **[Indexes](indexes-collection-dao.md)**. Se o objeto **Index** for acrescentado ao objeto **[TableDef](tabledef-object-dao.md)**, mas o objeto **TableDef** não estiver acrescentado à coleção **[TableDefs](tabledefs-collection-dao.md)**, a propriedade **Index** será leitura/gravação.

Um índice de chave primária é composto de um ou vários campos que identificam exclusivamente todos os registros em uma tabela na ordem predefinida. Como o campo índice deve ser exclusivo, a propriedade **[Unique](index-unique-property-dao.md)** do objeto **Index** será definida como **True**. Se o índice de chave primária for composto de mais de um campo, cada campo conterá valores duplicados, mas cada combinação de valores de todos os campos indexados deverá ser exclusiva. Um índice de chave primária é composto de uma chave para tabela e geralmente contém os mesmos campos da chave primária.

> [!NOTE]
> [!OBSERVAçãO] Não é necessário criar índices para tabelas mas, em tabelas grandes e não indexadas, o acesso a um registro específico pode demorar muito tempo. A propriedade **[Attributes](field-attributes-property-dao.md)** de cada objeto **[Field](field-object-dao.md)** no objeto **Index** determina a ordem dos registros e, como consequência, determina as técnicas de acesso para o uso desse índice. Quando você criar uma nova tabela no banco de dados, será uma boa ideia criar um índice em um ou vários campos que identifiquem exclusivamente cada registro e depois definir a propriedade **Primary** do objeto **Index** como **True**.

Quando você definir uma chave primária para uma tabela, a chave primária será automaticamente definida como o índice da chave primária para a tabela.

## <a name="example"></a>Exemplo

Este exemplo usa a propriedade **Primary** para designar um novo objeto **Index** em um novo objeto **TableDef** como o objeto **Index** primário dessa tabela. Observe que a definição da propriedade **Primary** como **True** também define automaticamente as propriedades **Unique** e **Required** como **True**.

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
