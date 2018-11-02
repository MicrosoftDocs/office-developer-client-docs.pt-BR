---
title: Propriedade Recordset.Sort (DAO)
TOCTitle: Sort Property
ms:assetid: 9be9bf62-f713-537e-4df0-3a54d485a523
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198077(v=office.15)
ms:contentKeyID: 48546582
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053063
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 18547162e7a0d64cc0ac7b0cdb2f0afa79185985
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926259"
---
# <a name="recordsetsort-property-dao"></a>Propriedade Recordset.Sort (DAO)


**Aplica-se a**: Access 2013, o Office 2013

Define ou retorna a ordem de classificação para registros em um objeto **[Recordset](recordset-object-dao.md)** (somente em espaços de trabalho do Microsoft Access).

## <a name="syntax"></a>Sintaxe

*expressão* . Classificar

*expressão* Uma variável que representa um objeto **Recordset** .

## <a name="remarks"></a>Comentários

Você pode usar a propriedade **Sort** com dynaset e instantâneo – objetos **Recordset** do tipo.

Quando você definir essa propriedade para um objeto, ocorrerá a classificação durante a criação de um objeto **Recordset** subsequente para esse objeto. A definição da propriedade **Sort** substituirá qualquer ordem de classificação especificada para um objeto **[QueryDef](querydef-object-dao.md)**.

A ordem de classificação padrão é a ascendente (A a Z ou 0 a 100).

A propriedade **Sort** não se aplica à tabela – ou – tipo forward only objetos **Recordset** . Para classificar um objeto **Recordset** do tipo tabela, use a propriedade **[Index](recordset-index-property-dao.md)** .


> [!NOTE]
> <P>[!OBSERVAçãO] Em muitos casos, é mais rápido abrir um novo objeto <STRONG>Recordset</STRONG> usando uma instrução SQL que inclui os critérios de classificação.</P>



## <a name="example"></a>Exemplo

Este exemplo demonstra a propriedade **Sort** pela alteração do seu valor e a criação de um novo **Recordset**. A função SortOutput será necessária para executar esse procedimento.

```vb
    Sub SortX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim rstSortEmployees As Recordset 
     
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
