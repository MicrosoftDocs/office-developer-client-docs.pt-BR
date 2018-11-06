---
title: Propriedade Recordset2.Sort (DAO)
TOCTitle: Sort Property
ms:assetid: 523a8c29-46e2-564f-205d-03c214f277fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193917(v=office.15)
ms:contentKeyID: 48544842
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 60d843773c00e7bd40e3e8e28997422fbda3c215
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998305"
---
# <a name="recordset2sort-property-dao"></a>Propriedade Recordset2.Sort (DAO)

**Aplica-se a**: Access 2013, o Office 2013 

Define ou retorna a ordem de classificação para registros em um objeto **[Recordset](recordset-object-dao.md)** (somente em espaços de trabalho do Microsoft Access).

## <a name="syntax"></a>Sintaxe

*expressão* . Classificar

*expressão* Uma variável que representa um objeto **Recordset2** .

## <a name="remarks"></a>Comentários

Você pode usar a propriedade **Sort** com dynaset e instantâneo – objetos **Recordset** do tipo.

Quando você definir essa propriedade para um objeto, ocorrerá a classificação durante a criação de um objeto **Recordset** subsequente para esse objeto. A definição da propriedade **Sort** substituirá qualquer ordem de classificação especificada para um objeto **[QueryDef](querydef-object-dao.md)**.

A ordem de classificação padrão é a ascendente (A a Z ou 0 a 100).

A propriedade **Sort** não se aplica à tabela – ou – tipo forward only objetos **Recordset** . Para classificar um objeto **Recordset** do tipo tabela, use a propriedade **[Index](recordset2-index-property-dao.md)** .

> [!NOTE]
> [!OBSERVAçãO] Em muitos casos, é mais rápido abrir um novo objeto **Recordset** usando uma instrução SQL que inclui os critérios de classificação.

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
