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
# <a name="indexforeign-property-dao"></a>Propriedade Index.Foreign (DAO)

**Aplica-se a**: Access 2013, o Office 2013

Retorna um valor que indica se um objeto **[Index](index-object-dao.md)** representa uma chave estrangeira em uma tabela (apenas espaços de trabalho Microsoft Access). .

## <a name="syntax"></a>Sintaxe

*expressão* . Externa

*expressão* Uma variável que representa um objeto **Index** .

## <a name="remarks"></a>Comentários

O valor de retorno será um tipo de dados **Boolean** que retornará **True**, se o objeto **Index** representar uma chave estrangeira.

Uma chave estrangeira é composta de um ou vários campos em uma tabela externa que identificam exclusivamente todas as linhas de uma tabela primária.

O mecanismo de banco de dados do Microsoft Access criará um objeto **Index** para a tabela externa e definirá a propriedade **Foreign** quando você criar uma relação que imponha a integridade referencial.

## <a name="example"></a>Exemplo

Este exemplo mostra como a propriedade **Foreign** pode indicar quais objetos **Index** em um **TableDef** são índices de chave estrangeira. Esses índices serão criados pelo mecanismo de banco de dados do Microsoft Access, quando um **Relation** for criado. O nome padrão dos índices de chave estrangeira é o nome da tabela primária acrescido do nome da tabela externa. A função ForeignOutput é necessária para executar esse procedimento.

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
