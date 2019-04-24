---
title: Propriedade Field. Updatable (DAO)
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
localization_priority: Normal
ms.openlocfilehash: 8678b825f509f483bf70d3aa2f3d767dbf7b0e32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293130"
---
# <a name="fielddataupdatable-property-dao"></a><span data-ttu-id="e9085-102">Propriedade Field. Updatable (DAO)</span><span class="sxs-lookup"><span data-stu-id="e9085-102">Field.DataUpdatable property (DAO)</span></span>


<span data-ttu-id="e9085-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e9085-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="e9085-104">Retorna um valor que indica se os dados no campo representados por um objeto **[Field](field-object-dao.md)** são atualizáveis.</span><span class="sxs-lookup"><span data-stu-id="e9085-104">Returns a value that indicates whether the data in the field represented by a **[Field](field-object-dao.md)** object is updatable.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9085-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e9085-105">Syntax</span></span>

<span data-ttu-id="e9085-106">*expressão* . DataUpdatable</span><span class="sxs-lookup"><span data-stu-id="e9085-106">*expression* .DataUpdatable</span></span>

<span data-ttu-id="e9085-107">*expressão* Uma variável que representa um objeto **Field** .</span><span class="sxs-lookup"><span data-stu-id="e9085-107">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9085-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="e9085-108">Remarks</span></span>

<span data-ttu-id="e9085-p101">Utilize essa propriedade para determinar se você pode alterar a configuração da propriedade **[Value](field-value-property-dao.md)** de um objeto **Field**. Essa propriedade é sempre **False** em um objeto **Field** cuja propriedade **[Attributes](field-attributes-property-dao.md)** é **dbAutoIncrField**.</span><span class="sxs-lookup"><span data-stu-id="e9085-p101">Use this property to determine whether you can change the **[Value](field-value-property-dao.md)** property setting of a **Field** object. This property is always **False** on a **Field** object whose **[Attributes](field-attributes-property-dao.md)** property is **dbAutoIncrField**.</span></span>

<span data-ttu-id="e9085-111">Você pode usar a propriedade **DataUpdatable** nos objetos **Field** que foram acrescentados à coleção **[Fields](fields-collection-dao.md)** dos objetos **[QueryDef](querydef-object-dao.md)**, **[Recordset](recordset-object-dao.md)** e **[Relation](relation-object-dao.md)**, mas não à coleção **Fields** dos objetos **[Index](index-object-dao.md)** ou **[TableDef](tabledef-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="e9085-111">You can use the **DataUpdatable** property on **Field** objects that are appended to the **[Fields](fields-collection-dao.md)** collection of **[QueryDef](querydef-object-dao.md)**, **[Recordset](recordset-object-dao.md)**, and **[Relation](relation-object-dao.md)** objects, but not the **Fields** collection of **[Index](index-object-dao.md)** or **[TableDef](tabledef-object-dao.md)** objects.</span></span>

## <a name="example"></a><span data-ttu-id="e9085-112">Exemplo</span><span class="sxs-lookup"><span data-stu-id="e9085-112">Example</span></span>

<span data-ttu-id="e9085-p102">Este exemplo demonstra a propriedade **DataUpdatable** utilizando o primeiro campo de seis **Recordsets** diferentes. A função DataOutput é exigida para que este procedimento seja executado.</span><span class="sxs-lookup"><span data-stu-id="e9085-p102">This example demonstrates the **DataUpdatable** property using the first field from six different **Recordsets**. The DataOutput function is required for this procedure to run.</span></span>

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

