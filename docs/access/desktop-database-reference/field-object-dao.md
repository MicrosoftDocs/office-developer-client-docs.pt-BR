---
title: Objetos de objeto Field - acesso a dados (DAO)
TOCTitle: Field Object
ms:assetid: 47282ce2-9b49-ccf9-ad37-c4bb25cfd037
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193203(v=office.15)
ms:contentKeyID: 48544587
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 644089e9ff4dddf2aed9f767a667cc3d80b6e039
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25924565"
---
# <a name="field-object-dao"></a><span data-ttu-id="a1a92-102">Objeto Field (DAO)</span><span class="sxs-lookup"><span data-stu-id="a1a92-102">Field object (DAO)</span></span>

<span data-ttu-id="a1a92-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="a1a92-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a1a92-104">Um objeto **Field** representa uma coluna de dados com um tipo de dados comum e um conjunto comum de propriedades.</span><span class="sxs-lookup"><span data-stu-id="a1a92-104">A **Field** object represents a column of data with a common data type and a common set of properties.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1a92-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="a1a92-105">Remarks</span></span>

<span data-ttu-id="a1a92-p101">As coleções **Fields** dos objetos **Index**, **QueryDef**, **Relation** e **TableDef** contêm as especificações para os campos representados por aqueles objetos. A coleção **Fields** de um objeto **Recordset** representa os objetos **Field** em uma linha de dados ou em um registro. Você usa os objetos **Field** em um objeto **Recordset** para ler e definir valores para os campos no registro atual do objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="a1a92-p101">The **Fields** collections of **Index**, **QueryDef**, **Relation**, and **TableDef** objects contain the specifications for the fields those objects represent. The **Fields** collection of a **Recordset** object represents the **Field** objects in a row of data, or in a record. You use the **Field** objects in a **Recordset** object to read and set values for the fields in the current record of the **Recordset** object.</span></span>

<span data-ttu-id="a1a92-p102">Nos espaços de trabalho do Microsoft Access, você manipula um campo utilizando um objeto **Field** e seus métodos e propriedades. Por exemplo, você pode:</span><span class="sxs-lookup"><span data-stu-id="a1a92-p102">In a Microsoft Access workspacee, you manipulate a field using a **Field** object and its methods and properties. For example, you can:</span></span>

  - <span data-ttu-id="a1a92-111">Usar a propriedade **OrdinalPosition** para definir ou retornar a ordem de apresentação do objeto **Field** em uma coleção **Fields**.</span><span class="sxs-lookup"><span data-stu-id="a1a92-111">Use the **OrdinalPosition** property to set or return the presentation order of the **Field** object in a **Fields** collection.</span></span>

  - <span data-ttu-id="a1a92-112">Usar a propriedade **Value** de um campo em um objeto **Recordset** para definir ou retornar dados armazenados.</span><span class="sxs-lookup"><span data-stu-id="a1a92-112">Use the **Value** property of a field in a **Recordset** object to set or return stored data.</span></span>

  - <span data-ttu-id="a1a92-113">Usar os métodos **AppendChunk** e **GetChunk** e a propriedade **FieldSize** para obter ou definir um valor em um campo OLE Object ou Memo de um objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="a1a92-113">Use the **AppendChunk** and **GetChunk** methods and the **FieldSize** property to get or set a value in an OLE Object or Memo field of a **Recordset** object.</span></span>

  - <span data-ttu-id="a1a92-114">Usar as propriedades **Type**, **Size** e **Attributes** para determinar o tipo de dados que pode ser armazenado no campo.</span><span class="sxs-lookup"><span data-stu-id="a1a92-114">Use the **Type**, **Size**, and **Attributes** properties to determine the type of data that can be stored in the field.</span></span>

  - <span data-ttu-id="a1a92-115">Usar as propriedades **SourceField** e **SourceTable** para determinar a fonte original dos dados.</span><span class="sxs-lookup"><span data-stu-id="a1a92-115">Use the **SourceField** and **SourceTable** properties to determine the original source of the data.</span></span>

  - <span data-ttu-id="a1a92-116">Usar a propriedade **ForeignName** para definir ou retornar informações sobre um campo externo em um objeto **Relation**.</span><span class="sxs-lookup"><span data-stu-id="a1a92-116">Use the **ForeignName** property to set or return information about a foreign field in a **Relation** object.</span></span>

  - <span data-ttu-id="a1a92-117">Usar as propriedades **AllowZeroLength**, **DefaultValue**, **Required**, **ValidateOnSet**, **ValidationRule** ou **ValidationText** para definir ou retornar as condições de validação.</span><span class="sxs-lookup"><span data-stu-id="a1a92-117">Use the **AllowZeroLength**, **DefaultValue**, **Required**, **ValidateOnSet**, **ValidationRule**, or **ValidationText** properties to set or return validation conditions.</span></span>

  - <span data-ttu-id="a1a92-118">Usar a propriedade **DefaultValue** de um campo em um objeto **TableDef** para definir o valor padrão desse campo quando novos registros forem adicionados.</span><span class="sxs-lookup"><span data-stu-id="a1a92-118">Use the **DefaultValue** property of a field on a **TableDef** object to set the default value for this field when new records are added.</span></span>

<span data-ttu-id="a1a92-119">Para criar um novo objeto **Field** em um objeto **Index**, **TableDef** ou **Relation**, use o método **CreateField**.</span><span class="sxs-lookup"><span data-stu-id="a1a92-119">To create a new **Field** object in an **Index**, **TableDef**, or **Relation** object, use the **CreateField** method.</span></span>

<span data-ttu-id="a1a92-p103">Quando você acessa um objeto **Field** como parte de um objeto **Recordset**, os dados do registro atual ficam visíveis na propriedade **Value** do objeto **Field**. Para manipular dados no objeto **Recordset**, você normalmente não faz referência à coleção **Fields** diretamente; em vez disso, você referencia indiretamente a propriedade **Value** do objeto **Field** na coleção **Fields** do objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="a1a92-p103">When you access a **Field** object as part of a **Recordset** object, data from the current record is visible in the **Field** object's **Value** property. To manipulate data in the **Recordset** object, you don't usually reference the **Fields** collection directly; instead, you indirectly reference the **Value** property of the **Field** object in the **Fields** collection of the **Recordset** object.</span></span>

<span data-ttu-id="a1a92-122">Para referir-se a um objeto **Field** de uma coleção pelo número ordinal ou pela configuração da propriedade **Name**, use qualquer uma das formas de sintaxe a seguir:</span><span class="sxs-lookup"><span data-stu-id="a1a92-122">To refer to a **Field** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

- <span data-ttu-id="a1a92-123">**Fields**(0)</span><span class="sxs-lookup"><span data-stu-id="a1a92-123">**Fields**(0)</span></span>

- <span data-ttu-id="a1a92-124">**Campos** ("nome")</span><span class="sxs-lookup"><span data-stu-id="a1a92-124">**Fields**("name")</span></span>

- <span data-ttu-id="a1a92-125">**Campos**\!\[nome\]</span><span class="sxs-lookup"><span data-stu-id="a1a92-125">**Fields**\!\[name\]</span></span>

<span data-ttu-id="a1a92-p104">Com as mesmas formas de sintaxe, você também pode se referir à propriedade **Value** de um objeto **Field** criado e acrescentado à coleção **Fields**. O contexto da referência de campo determinará se você está se referindo ao objeto **Field** ou à propriedade **Value**do objeto **Field**.</span><span class="sxs-lookup"><span data-stu-id="a1a92-p104">With the same syntax forms, you can also refer to the **Value** property of a **Field** object that you create and append to a **Fields** collection. The context of the field reference will determine whether you are referring to the **Field** object or the **Value** property of the **Field** object.</span></span>

## <a name="example"></a><span data-ttu-id="a1a92-128">Exemplo</span><span class="sxs-lookup"><span data-stu-id="a1a92-128">Example</span></span>

<span data-ttu-id="a1a92-p105">Este exemplo mostra quais propriedades são válidas para um objeto **Field** dependente no qual o **Field** reside (por exemplo, a coleção **Fields** de um **TableDef**, a coleção **Fields** de um **QueryDef** e assim por diante). O procedimento FieldOutput é exigido para que este procedimento seja executado.</span><span class="sxs-lookup"><span data-stu-id="a1a92-p105">This example shows what properties are valid for a **Field** object depending on where the **Field** resides (for example, the **Fields** collection of a **TableDef**, the **Fields** collection of a **QueryDef**, and so forth). The FieldOutput procedure is required for this procedure to run.</span></span>

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

<span data-ttu-id="a1a92-p106">Este exemplo usa o método **CreateField** para criar três **Fields** para um novo **TableDef**. Em seguida, ele exibe as propriedades daqueles objetos **Field** que são automaticamente definidos pelo método **CreateField**. (As propriedades cujos valores estão vazios no momento da criação do **Field** não são mostradas.)</span><span class="sxs-lookup"><span data-stu-id="a1a92-p106">This example uses the **CreateField** method to create three **Fields** for a new **TableDef**. It then displays the properties of those **Field** objects that are automatically set by the **CreateField** method. (Properties whose values are empty at the time of **Field** creation are not shown.)</span></span>

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
