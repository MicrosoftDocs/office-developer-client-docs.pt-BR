---
title: Propriedade Recordset2.Sort (DAO)
TOCTitle: Sort Property
ms:assetid: 523a8c29-46e2-564f-205d-03c214f277fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193917(v=office.15)
ms:contentKeyID: 48544842
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a5784054ce195a1a2ea516d4f6a3417c5a8db71c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309266"
---
# <a name="recordset2sort-property-dao"></a>Propriedade Recordset2.Sort (DAO)

**Aplica-se a:** Access 2013, Office 2013 

Define ou retorna a ordem de classificação dos registros em um objeto **[Recordset](recordset-object-dao.md)** (somente em espaços de trabalho do Microsoft Access).

## <a name="syntax"></a>Sintaxe

*expression* .Sort

*expressão* Uma variável que representa **um objeto Recordset2** .

## <a name="remarks"></a>Comentários

Use a propriedade **Sort** com os objetos **Recordset** do tipo dynaset e snapshot.

Quando você definir essa propriedade para um objeto, ocorrerá a classificação durante a criação de um objeto **Recordset** subsequente para esse objeto. A definição da propriedade **Sort** substituirá qualquer ordem de classificação especificada para um objeto **[QueryDef](querydef-object-dao.md)**.

A ordem de classificação padrão é a ascendente (A a Z ou 0 a 100).

A propriedade **Sort** não se aplica a objetos **Recordset** do tipo tabela ou somente encaminhamento. Para classificar o objeto **Recordset** do tipo tabela, use a propriedade **[Index](recordset2-index-property-dao.md)**.

> [!NOTE]
> Em vários casos, é mais rápido abrir um novo objeto **Recordset** usando uma instrução SQL que inclua os critérios de classificação.

## <a name="example"></a>Exemplo

Este exemplo demonstra a propriedade **Sort** pela alteração do seu valor e a criação de um novo **Recordset**. A função SortOutput será necessária para executar esse procedimento.

```vb
    Sub SortX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     Dim rstSortEmployees As Recordset2 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     With rstEmployees 
     SortOutput "Original Recordset:", rstEmployees 
     .Sort = "LastName, FirstName" 
     ' Print report showing Sort property and record order. 
     SortOutput _ 
     "Recordset after changing Sort property:", _ 
     rstEmployees 
     ' Open new Recordset from current one. 
     Set rstSortEmployees = .OpenRecordset 
     ' Print report showing Sort property and record order. 
     SortOutput "New Recordset:", rstSortEmployees 
     rstSortEmployees.Close 
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function SortOutput(strTemp As String, _ 
     rstTemp As Recordset) 
     
     With rstTemp 
     Debug.Print strTemp 
     Debug.Print " Sort = " & _ 
     IIf(.Sort <> "", .Sort, "[Empty]") 
     .MoveFirst 
     
     ' Enumerate Recordset. 
     Do While Not .EOF 
     Debug.Print " " & !LastName & _ 
     ", " & !FirstName 
     .MoveNext 
     Loop 
     
     End With 
     
    End Function 
```

<br/>

Quando você conhecer os dados a serem selecionados, geralmente, será mais eficiente criar um **Recordset** com uma instrução SQL. Este exemplo mostra como você pode criar apenas um **Recordset** e obter os mesmos resultados de um exemplo anterior.

```vb
    Sub SortX2() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     ' Open a Recordset from an SQL statement that specifies a 
     ' sort order. 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("SELECT * " & _ 
     "FROM Employees ORDER BY LastName, FirstName", _ 
     dbOpenDynaset) 
     
     dbsNorthwind.Close 
     
    End Sub
```
