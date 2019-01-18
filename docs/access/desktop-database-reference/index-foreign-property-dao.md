---
title: Propriedade Index.Foreign (DAO)
TOCTitle: Foreign Property
ms:assetid: 81272436-a506-4b72-fd28-2d68e76d6d9b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196489(v=office.15)
ms:contentKeyID: 48545943
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052974
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a3c6adfaf9648147a763f997ce2a91aadc4f7637
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707185"
---
# <a name="indexforeign-property-dao"></a><span data-ttu-id="d981d-102">Propriedade Index.Foreign (DAO)</span><span class="sxs-lookup"><span data-stu-id="d981d-102">Index.Foreign property (DAO)</span></span>

<span data-ttu-id="d981d-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="d981d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d981d-p101">Retorna um valor que indica se um objeto **[Index](index-object-dao.md)** representa uma chave estrangeira em uma tabela (apenas espaços de trabalho Microsoft Access). .</span><span class="sxs-lookup"><span data-stu-id="d981d-p101">Returns a value that indicates whether an **[Index](index-object-dao.md)** object represents a foreign key in a table (Microsoft Access workspaces only). .</span></span>

## <a name="syntax"></a><span data-ttu-id="d981d-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d981d-106">Syntax</span></span>

<span data-ttu-id="d981d-107">*expressão* . Externa</span><span class="sxs-lookup"><span data-stu-id="d981d-107">*expression* .Foreign</span></span>

<span data-ttu-id="d981d-108">*expressão* Uma variável que representa um objeto **Index** .</span><span class="sxs-lookup"><span data-stu-id="d981d-108">*expression* A variable that represents an **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d981d-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="d981d-109">Remarks</span></span>

<span data-ttu-id="d981d-110">O valor de retorno será um tipo de dados **Boolean** que retornará **True**, se o objeto **Index** representar uma chave estrangeira.</span><span class="sxs-lookup"><span data-stu-id="d981d-110">The return value is a **Boolean** data type that returns **True** if the **Index** object represents a foreign key.</span></span>

<span data-ttu-id="d981d-111">Uma chave estrangeira é composta de um ou vários campos em uma tabela externa que identificam exclusivamente todas as linhas de uma tabela primária.</span><span class="sxs-lookup"><span data-stu-id="d981d-111">A foreign key consists of one or more fields in a foreign table that uniquely identify all rows in a primary table.</span></span>

<span data-ttu-id="d981d-112">O mecanismo de banco de dados do Microsoft Access criará um objeto **Index** para a tabela externa e definirá a propriedade **Foreign** quando você criar uma relação que imponha a integridade referencial.</span><span class="sxs-lookup"><span data-stu-id="d981d-112">The Microsoft Access database engine creates an **Index** object for the foreign table and sets the **Foreign** property when you create a relationship that enforces referential integrity.</span></span>

## <a name="example"></a><span data-ttu-id="d981d-113">Exemplo</span><span class="sxs-lookup"><span data-stu-id="d981d-113">Example</span></span>

<span data-ttu-id="d981d-p102">Este exemplo mostra como a propriedade **Foreign** pode indicar quais objetos **Index** em um **TableDef** são índices de chave estrangeira. Esses índices serão criados pelo mecanismo de banco de dados do Microsoft Access, quando um **Relation** for criado. O nome padrão dos índices de chave estrangeira é o nome da tabela primária acrescido do nome da tabela externa. A função ForeignOutput é necessária para executar esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="d981d-p102">This example shows how the **Foreign** property can indicate which **Index** objects in a **TableDef** are foreign key indexes. Such indexes are created by the Microsoft Access database engine when a **Relation** is created. The default name for the foreign key indexes is the name of the primary table plus the name of the foreign table. The ForeignOutput function is required for this procedure to run.</span></span>

```vb
    Sub ForeignX() 
     
     Dim dbsNorthwind As Database 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Print report on foreign key indexes from two 
     ' TableDef objects and a QueryDef object. 
     ForeignOutput .TableDefs!Products 
     ForeignOutput .TableDefs!Orders 
     ForeignOutput .TableDefs![Order Details] 
     
     .Close 
     End With 
     
    End Sub 
     
    Function ForeignOutput(tdfTemp As TableDef) 
     
     Dim idxLoop As Index 
     
     With tdfTemp 
     Debug.Print "Indexes in " & .Name & " TableDef" 
     ' Enumerate the Indexes collection of the specified 
     ' TableDef object. 
     For Each idxLoop In .Indexes 
     Debug.Print " " & idxLoop.Name 
     Debug.Print " Foreign = " & idxLoop.Foreign 
     Next idxLoop 
     End With 
     
    End Function
```
