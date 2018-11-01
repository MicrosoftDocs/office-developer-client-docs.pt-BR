---
title: Propriedade Index.DistinctCount (DAO)
TOCTitle: DistinctCount Property
ms:assetid: 24cb7247-76b4-1fce-c3c4-892f16634eff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191836(v=office.15)
ms:contentKeyID: 48543767
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053119
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 2e609090e66a9bfd5b4b37d8e8e8a5546cc8469a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876886"
---
# <a name="indexdistinctcount-property-dao"></a>Propriedade Index.DistinctCount (DAO)

**Aplica-se a**: Access 2013, o Office 2013

Retorna um valor que indica o número de valores exclusivos para o objeto **[Index](index-object-dao.md)** que estão incluídos na tabela associada (apenas espaços de trabalho do Microsoft Access).

## <a name="syntax"></a>Sintaxe

*expressão* . DistinctCount

*expressão* Uma variável que representa um objeto **Index** .

## <a name="remarks"></a>Comentários

Verifique a propriedade **DistinctCount** para determinar o número de valores, ou chaves, exclusivos em um índice. Qualquer chave é contada somente uma vez, embora possa haver várias ocorrências daquele valor, se o índice permitir valores duplicados. Essas informações são úteis nos aplicativos que tentam otimizar o acesso aos dados, avaliando as informações de índice. O número de valores exclusivos também é conhecido como a cardinalidade de um objeto **Index**.

A propriedade **DistinctCount** nem sempre reflete o número real de chaves em um determinado tempo. Por exemplo, uma alteração causada por uma transação revertida não será refletida imediatamente na propriedade **DistinctCount**. O valor da propriedade **DistinctCount** também não pode refletir a exclusão dos registros com chaves exclusivas. A exatidão do número será verificada imediatamente após o uso do método **[CreateIndex](tabledef-createindex-method-dao.md)**.

## <a name="example"></a>Exemplo

Este exemplo usa a propriedade **DistinctCount** para mostrar como você pode determinar o número de valores exclusivos em um objeto **Index**. Entretanto, esse valor será exato imediatamente depois da criação do **Index**. Ele permanecerá preciso se nenhuma chave for alterada ou se novas chaves forem adicionadas, mas nenhuma chave antiga for excluída; caso contrário, ele não será confiável. (Se esse procedimento for executado várias vezes, será possível ver o efeito nos valores da propriedade **DistinctCount** dos objetos Index existentes.)

```vb
    Sub DistinctCountX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxCountry As Index 
     Dim idxLoop As Index 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create and append new Index object to the Employees 
     ' table. 
     Set idxCountry = .CreateIndex("CountryIndex") 
     idxCountry.Fields.Append _ 
     idxCountry.CreateField("Country") 
     .Indexes.Append idxCountry 
     
     ' The collection must be refreshed for the new 
     ' DistinctCount data to be available. 
     .Indexes.Refresh 
     
     ' Enumerate Indexes collection to show the current 
     ' DistinctCount values. 
     Debug.Print "Indexes before adding new record" 
     For Each idxLoop In .Indexes 
     Debug.Print " DistinctCount = " & _ 
     idxLoop.DistinctCount & ", Name = " & _ 
     idxLoop.Name 
     Next idxLoop 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     ' Add a new record to the Employees table. 
     With rstEmployees 
     .AddNew 
     !FirstName = "April" 
     !LastName = "LaMonte" 
     !Country = "Canada" 
     .Update 
     End With 
     
     ' Enumerate Indexes collection to show the modified 
     ' DistinctCount values. 
     Debug.Print "Indexes after adding new record and " & _ 
     "refreshing Indexes" 
     .Indexes.Refresh 
     For Each idxLoop In .Indexes 
     Debug.Print " DistinctCount = " & _ 
     idxLoop.DistinctCount & ", Name = " & _ 
     idxLoop.Name 
     Next idxLoop 
     
     ' Delete new record because this is a demonstration. 
     With rstEmployees 
     .Bookmark = .LastModified 
     .Delete 
     .Close 
     End With 
     
     ' Delete new Indexes because this is a demonstration. 
     .Indexes.Delete idxCountry.Name 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
