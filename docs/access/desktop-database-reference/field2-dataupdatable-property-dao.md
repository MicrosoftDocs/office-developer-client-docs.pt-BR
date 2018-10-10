---
title: Propriedade Field2.DataUpdatable (DAO)
TOCTitle: DataUpdatable Property
ms:assetid: e6619c4e-26b1-777b-f0de-78fed3dbc890
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835966(v=office.15)
ms:contentKeyID: 48548377
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b7360e5ddf45275983521ddf7e1140321cc19630
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462613"
---
# <a name="field2dataupdatable-property-dao"></a>Propriedade Field2.DataUpdatable (DAO)


**Aplica-se a**: Access 2013 | Office 2013


Retorna um valor que indica se os dados no campo representados por um objeto **Field2** são atualizáveis.

## <a name="syntax"></a>Sintaxe

*expressão* . DataUpdatable

*expressão* Uma variável que representa um objeto **Field2** .

## <a name="remarks"></a>Comentários

Utilize essa propriedade para determinar se você pode alterar a configuração da propriedade **[Value](field-value-property-dao.md)** de um objeto **Field2**. Essa propriedade é sempre **False** em um objeto **Field2** cuja propriedade **[Attributes](field-attributes-property-dao.md)** é **dbAutoIncrField**.

Você pode usar a propriedade **DataUpdatable** nos objetos **Field2** que foram acrescentados à coleção **[Fields](fields-collection-dao.md)** dos objetos **[QueryDef](querydef-object-dao.md)**, **[Recordset](recordset-object-dao.md)** e **[Relation](relation-object-dao.md)**, mas não à coleção **Fields** dos objetos **[Index](index-object-dao.md)** ou **[TableDef](tabledef-object-dao.md)**.

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

