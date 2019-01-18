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
# <a name="fields-collection-dao"></a><span data-ttu-id="2d9e0-102">Coleção Fields (DAO)</span><span class="sxs-lookup"><span data-stu-id="2d9e0-102">Fields collection (DAO)</span></span>


<span data-ttu-id="2d9e0-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="2d9e0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2d9e0-104">Uma coleção **Fields** contém todos os objetos **Field** armazenados de um objeto **Index**, **QueryDef**, **Recordset**, **Relation** ou **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="2d9e0-104">A **Fields** collection contains all stored **Field** objects of an **Index**, **QueryDef**, **Recordset**, **Relation**, or **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d9e0-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="2d9e0-105">Remarks</span></span>

<span data-ttu-id="2d9e0-p101">As coleções **Fields** dos objetos **Index**, **QueryDef**, **Relation** e **TableDef** contêm as especificações para os campos representados por aqueles objetos. A coleção **Fields** de um objeto **Recordset** representa os objetos **Field** em uma linha de dados ou em um registro. Você usa os objetos **Field** em um objeto **Recordset** para ler e definir valores para os campos no registro atual do objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="2d9e0-p101">The **Fields** collections of the **Index**, **QueryDef**, **Relation**, and **TableDef** objects contain the specifications for the fields those objects represent. The **Fields** collection of a **Recordset** object represents the **Field** objects in a row of data, or in a record. You use the **Field** objects in a **Recordset** object to read and to set values for the fields in the current record of the **Recordset** object.</span></span>

<span data-ttu-id="2d9e0-109">Para se referir a um objeto **Field** de uma coleção pelo número ordinal ou pela configuração da propriedade **Name**, use qualquer uma das formas de sintaxe a seguir:</span><span class="sxs-lookup"><span data-stu-id="2d9e0-109">To refer to a **Field** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="2d9e0-110">**Fields**(0)</span><span class="sxs-lookup"><span data-stu-id="2d9e0-110">**Fields**(0)</span></span>

<span data-ttu-id="2d9e0-111">**Campos** ("nome")</span><span class="sxs-lookup"><span data-stu-id="2d9e0-111">**Fields**("name")</span></span>

<span data-ttu-id="2d9e0-112">**Campos**\!\[nome\]</span><span class="sxs-lookup"><span data-stu-id="2d9e0-112">**Fields**\!\[name\]</span></span>

<span data-ttu-id="2d9e0-p102">Com as mesmas formas de sintaxe, você também pode se referir à propriedade **Value** de um objeto **Field** criado e acrescentado à coleção **Fields**. O contexto da referência de campo determinará se você está se referindo ao objeto **Field** ou à propriedade **Value**do objeto **Field**.</span><span class="sxs-lookup"><span data-stu-id="2d9e0-p102">With the same syntax forms, you can also refer to the **Value** property of a **Field** object that you create and append to a **Fields** collection. The context of the field reference will determine whether you are referring to the **Field** object or the **Value** property of the **Field** object.</span></span>

## <a name="example"></a><span data-ttu-id="2d9e0-115">Exemplo</span><span class="sxs-lookup"><span data-stu-id="2d9e0-115">Example</span></span>

<span data-ttu-id="2d9e0-p103">Este exemplo mostra quais propriedades são válidas para um objeto **Field** dependente no qual o **Field** reside (por exemplo, a coleção **Fields** de um **TableDef**, a coleção **Fields** de um **QueryDef** e assim por diante). O procedimento FieldOutput é exigido para que este procedimento seja executado.</span><span class="sxs-lookup"><span data-stu-id="2d9e0-p103">This example shows what properties are valid for a **Field** object depending on where the **Field** resides (for example, the **Fields** collection of a **TableDef**, the **Fields** collection of a **QueryDef**, and so forth). The FieldOutput procedure is required for this procedure to run.</span></span>

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

<span data-ttu-id="2d9e0-p104">Este exemplo usa o método **CreateField** para criar três **Fields** para um novo **TableDef**. Em seguida, ele exibe as propriedades daqueles objetos **Field** que são automaticamente definidos pelo método **CreateField**. (As propriedades cujos valores estão vazios no momento da criação do **Field** não são mostradas.)</span><span class="sxs-lookup"><span data-stu-id="2d9e0-p104">This example uses the **CreateField** method to create three **Fields** for a new **TableDef**. It then displays the properties of those **Field** objects that are automatically set by the **CreateField** method. (Properties whose values are empty at the time of **Field** creation are not shown.)</span></span>

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
