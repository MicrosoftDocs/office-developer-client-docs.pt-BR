---
title: Propriedade Field.DataUpdatable (DAO)
TOCTitle: DataUpdatable Property
ms:assetid: 08ca57b6-2d7c-36b4-7d51-b76ac5467163
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845029(v=office.15)
ms:contentKeyID: 48543104
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052988
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ad3de8bba18b15b15311bf188822a451e74bb24d
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926609"
---
# <a name="fielddataupdatable-property-dao"></a>Propriedade Field.DataUpdatable (DAO)


**Aplica-se a**: Access 2013, o Office 2013


Retorna um valor que indica se os dados no campo representados por um objeto **[Field](field-object-dao.md)** são atualizáveis.

## <a name="syntax"></a>Sintaxe

*expressão* . DataUpdatable

*expressão* Uma variável que representa um objeto **Field** .

## <a name="remarks"></a>Comentários

Utilize essa propriedade para determinar se você pode alterar a configuração da propriedade **[Value](field-value-property-dao.md)** de um objeto **Field**. Essa propriedade é sempre **False** em um objeto **Field** cuja propriedade **[Attributes](field-attributes-property-dao.md)** é **dbAutoIncrField**.

Você pode usar a propriedade **DataUpdatable** nos objetos **Field** que foram acrescentados à coleção **[Fields](fields-collection-dao.md)** dos objetos **[QueryDef](querydef-object-dao.md)**, **[Recordset](recordset-object-dao.md)** e **[Relation](relation-object-dao.md)**, mas não à coleção **Fields** dos objetos **[Index](index-object-dao.md)** ou **[TableDef](tabledef-object-dao.md)**.

## <a name="example"></a>Exemplo

Este exemplo demonstra a propriedade **DataUpdatable** utilizando o primeiro campo de seis **Recordsets** diferentes. A função DataOutput é exigida para que este procedimento seja executado.

```vb 
Sub DataUpdatableX() 
 
 Dim dbsNorthwind As Database 
 Dim rstNorthwind As Recordset 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind 
 ' Open and print report about a table-type Recordset. 
 Set rstNorthwind = .OpenRecordset("Employees") 
 DataOutput rstNorthwind 
 
 ' Open and print report about a dynaset-type Recordset. 
 Set rstNorthwind = .OpenRecordset("Employees", _ 
 dbOpenDynaset) 
 DataOutput rstNorthwind 
 
 ' Open and print report about a snapshot-type Recordset. 
 Set rstNorthwind = .OpenRecordset("Employees", _ 
 dbOpenSnapshot) 
 DataOutput rstNorthwind 
 
 ' Open and print report about a forward-only-type Recordset. 
 Set rstNorthwind = .OpenRecordset("Employees", _ 
 dbOpenForwardOnly) 
 DataOutput rstNorthwind 
 
 ' Open and print report about a Recordset based on 
 ' a select query. 
 Set rstNorthwind = _ 
 .OpenRecordset("Current Product List") 
 DataOutput rstNorthwind 
 
 ' Open and print report about a Recordset based on a 
 ' select query that calculates totals. 
 Set rstNorthwind = .OpenRecordset("Order Subtotals") 
 DataOutput rstNorthwind 
 
 .Close 
 End With 
 
End Sub 
 
Function DataOutput(rstTemp As Recordset) 
 
 With rstTemp 
 Debug.Print "Recordset: " & .Name & ", "; 
 Select Case .Type 
 Case dbOpenTable 
 Debug.Print "dbOpenTable" 
 Case dbOpenDynaset 
 Debug.Print "dbOpenDynaset" 
 Case dbOpenSnapshot 
 Debug.Print "dbOpenSnapshot" 
 Case dbOpenForwardOnly 
 Debug.Print "dbOpenForwardOnly" 
 End Select 
 Debug.Print " Field: " & .Fields(0).Name & ", " & _ 
 "DataUpdatable = " & .Fields(0).DataUpdatable 
 Debug.Print 
 .Close 
 End With 
 
End Function 
 
```

