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
ms.openlocfilehash: 2028334a2fc1d63262d9f109cb6f76c624b64e3a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464168"
---
# <a name="indexdistinctcount-property-dao"></a><span data-ttu-id="be1d3-102">Propriedade Index.DistinctCount (DAO)</span><span class="sxs-lookup"><span data-stu-id="be1d3-102">Index.DistinctCount Property (DAO)</span></span>

<span data-ttu-id="be1d3-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="be1d3-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="be1d3-104">Retorna um valor que indica o número de valores exclusivos para o objeto **[Index](index-object-dao.md)** que estão incluídos na tabela associada (apenas espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="be1d3-104">Returns a value that indicates the number of unique values for the **[Index](index-object-dao.md)** object that are included in the associated table (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="be1d3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="be1d3-105">Syntax</span></span>

<span data-ttu-id="be1d3-106">*expressão* . DistinctCount</span><span class="sxs-lookup"><span data-stu-id="be1d3-106">*expression* .DistinctCount</span></span>

<span data-ttu-id="be1d3-107">*expressão* Uma variável que representa um objeto **Index** .</span><span class="sxs-lookup"><span data-stu-id="be1d3-107">*expression* A variable that represents an **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="be1d3-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="be1d3-108">Remarks</span></span>

<span data-ttu-id="be1d3-p101">Verifique a propriedade **DistinctCount** para determinar o número de valores, ou chaves, exclusivos em um índice. Qualquer chave é contada somente uma vez, embora possa haver várias ocorrências daquele valor, se o índice permitir valores duplicados. Essas informações são úteis nos aplicativos que tentam otimizar o acesso aos dados, avaliando as informações de índice. O número de valores exclusivos também é conhecido como a cardinalidade de um objeto **Index**.</span><span class="sxs-lookup"><span data-stu-id="be1d3-p101">Check the **DistinctCount** property to determine the number of unique values, or keys, in an index. Any key is counted only once, even though there may be multiple occurrences of that value if the index permits duplicate values. This information is useful in applications that attempt to optimize data access by evaluating index information. The number of unique values is also known as the cardinality of an **Index** object.</span></span>

<span data-ttu-id="be1d3-p102">A propriedade **DistinctCount** nem sempre reflete o número real de chaves em um determinado tempo. Por exemplo, uma alteração causada por uma transação revertida não será refletida imediatamente na propriedade **DistinctCount**. O valor da propriedade **DistinctCount** também não pode refletir a exclusão dos registros com chaves exclusivas. A exatidão do número será verificada imediatamente após o uso do método **[CreateIndex](tabledef-createindex-method-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="be1d3-p102">The **DistinctCount** property won't always reflect the actual number of keys at a particular time. For example, a change caused by a rolled back transaction won't be reflected immediately in the **DistinctCount** property. The **DistinctCount** property value also may not reflect the deletion of records with unique keys. The number will be accurate immediately after you use the **[CreateIndex](tabledef-createindex-method-dao.md)** method.</span></span>

## <a name="example"></a><span data-ttu-id="be1d3-117">Exemplo</span><span class="sxs-lookup"><span data-stu-id="be1d3-117">Example</span></span>

<span data-ttu-id="be1d3-p103">Este exemplo usa a propriedade **DistinctCount** para mostrar como você pode determinar o número de valores exclusivos em um objeto **Index**. Entretanto, esse valor será exato imediatamente depois da criação do **Index**. Ele permanecerá preciso se nenhuma chave for alterada ou se novas chaves forem adicionadas, mas nenhuma chave antiga for excluída; caso contrário, ele não será confiável. (Se esse procedimento for executado várias vezes, será possível ver o efeito nos valores da propriedade **DistinctCount** dos objetos Index existentes.)</span><span class="sxs-lookup"><span data-stu-id="be1d3-p103">This example uses the **DistinctCount** property to show how you can determine the number of unique values in an **Index** object. However, this value is only accurate immediately after creating the **Index**. It will remain accurate if no keys change, or if new keys are added and no old keys are deleted; otherwise, it will not be reliable. (If this procedure is run several times, you can see the effect on the **DistinctCount** property values of the existing Index objects.)</span></span>

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
