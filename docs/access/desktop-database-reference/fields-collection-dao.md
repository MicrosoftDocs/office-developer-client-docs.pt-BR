---
title: Coleção Fields (DAO)
TOCTitle: Fields Collection
ms:assetid: 4be3ba07-20c1-d958-c1b8-7dd8b4731f60
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193530(v=office.15)
ms:contentKeyID: 48544702
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: d87d1535afeaf0740627a7af3852b1929a0e6d50
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713279"
---
# <a name="fields-collection-dao"></a>Coleção Fields (DAO)


**Aplica-se a**: Access 2013, o Office 2013

Uma coleção **Fields** contém todos os objetos **Field** armazenados de um objeto **Index**, **QueryDef**, **Recordset**, **Relation** ou **TableDef**.

## <a name="remarks"></a>Comentários

As coleções **Fields** dos objetos **Index**, **QueryDef**, **Relation** e **TableDef** contêm as especificações para os campos representados por aqueles objetos. A coleção **Fields** de um objeto **Recordset** representa os objetos **Field** em uma linha de dados ou em um registro. Você usa os objetos **Field** em um objeto **Recordset** para ler e definir valores para os campos no registro atual do objeto **Recordset**.

Para se referir a um objeto **Field** de uma coleção pelo número ordinal ou pela configuração da propriedade **Name**, use qualquer uma das formas de sintaxe a seguir:

**Fields**(0)

**Campos** ("nome")

**Campos**\!\[nome\]

Com as mesmas formas de sintaxe, você também pode se referir à propriedade **Value** de um objeto **Field** criado e acrescentado à coleção **Fields**. O contexto da referência de campo determinará se você está se referindo ao objeto **Field** ou à propriedade **Value**do objeto **Field**.

## <a name="example"></a>Exemplo

Este exemplo mostra quais propriedades são válidas para um objeto **Field** dependente no qual o **Field** reside (por exemplo, a coleção **Fields** de um **TableDef**, a coleção **Fields** de um **QueryDef** e assim por diante). O procedimento FieldOutput é exigido para que este procedimento seja executado.

```vb
    Sub FieldX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim fldTableDef As Field 
     Dim fldQueryDef As Field 
     Dim fldRecordset As Field 
     Dim fldRelation As Field 
     Dim fldIndex As Field 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     ' Assign a Field object from different Fields 
     ' collections to object variables. 
     Set fldTableDef = _ 
     dbsNorthwind.TableDefs(0).Fields(0) 
     Set fldQueryDef =dbsNorthwind.QueryDefs(0).Fields(0) 
     Set fldRecordset = rstEmployees.Fields(0) 
     Set fldRelation =dbsNorthwind.Relations(0).Fields(0) 
     Set fldIndex = _ 
     dbsNorthwind.TableDefs(0).Indexes(0).Fields(0) 
     
     ' Print report. 
     FieldOutput "TableDef", fldTableDef 
     FieldOutput "QueryDef", fldQueryDef 
     FieldOutput "Recordset", fldRecordset 
     FieldOutput "Relation", fldRelation 
     FieldOutput "Index", fldIndex 
     
     rstEmployees.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub FieldOutput(strTemp As String, fldTemp As Field) 
     ' Report function for FieldX. 
     
     Dim prpLoop As Property 
     
     Debug.Print "Valid Field properties in " & strTemp 
     
     ' Enumerate Properties collection of passed Field 
     ' object. 
     For Each prpLoop In fldTemp.Properties 
     ' Some properties are invalid in certain 
     ' contexts (the Value property in the Fields 
     ' collection of a TableDef for example). Any 
     ' attempt to use an invalid property will 
     ' trigger an error. 
     On Error Resume Next 
     Debug.Print " " & prpLoop.Name & " = " & _ 
     prpLoop.Value 
     On Error GoTo 0 
     Next prpLoop 
     
    End Sub 
```

<br/>

Este exemplo usa o método **CreateField** para criar três **Fields** para um novo **TableDef**. Em seguida, ele exibe as propriedades daqueles objetos **Field** que são automaticamente definidos pelo método **CreateField**. (As propriedades cujos valores estão vazios no momento da criação do **Field** não são mostradas.)

```vb
    Sub CreateFieldX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfNew As TableDef 
     Dim fldLoop As Field 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     Set tdfNew = dbsNorthwind.CreateTableDef("NewTableDef") 
     
     ' Create and append new Field objects for the new 
     ' TableDef object. 
     With tdfNew 
     ' The CreateField method will set a default Size 
     ' for a new Field object if one is not specified. 
     .Fields.Append .CreateField("TextField", dbText) 
     .Fields.Append .CreateField("IntegerField", dbInteger) 
     .Fields.Append .CreateField("DateField", dbDate) 
     End With 
     
     dbsNorthwind.TableDefs.Append tdfNew 
     
     Debug.Print "Properties of new Fields in " & tdfNew.Name 
     
     ' Enumerate Fields collection to show the properties of 
     ' the new Field objects. 
     For Each fldLoop In tdfNew.Fields 
     Debug.Print " " & fldLoop.Name 
     
     For Each prpLoop In fldLoop.Properties 
     ' Properties that are invalid in the context of 
     ' TableDefs will trigger an error if an attempt 
     ' is made to read their values. 
     On Error Resume Next 
     Debug.Print " " & prpLoop.Name & " - " & _ 
     IIf(prpLoop = "", "[empty]", prpLoop) 
     On Error GoTo 0 
     Next prpLoop 
     
     Next fldLoop 
     
     ' Delete new TableDef because this is a demonstration. 
     dbsNorthwind.TableDefs.Delete tdfNew.Name 
     dbsNorthwind.Close 
     
    End Sub
```
