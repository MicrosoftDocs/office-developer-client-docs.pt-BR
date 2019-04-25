---
title: Objeto de campo Objetos de Acesso a Dados (DAO)
TOCTitle: Field Object
ms:assetid: 47282ce2-9b49-ccf9-ad37-c4bb25cfd037
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193203(v=office.15)
ms:contentKeyID: 48544587
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: c58896fb0d0a5c5a28844fdd3a6df922dd587f32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293039"
---
# <a name="field-object-dao"></a>Objeto de campo (DAO)

**Aplica-se ao:** Access 2013, Office 2013

Um **objeto** de campo representa uma coluna de dados com um tipo de dados comum e em um conjunto comum de propriedades.

## <a name="remarks"></a>Comentários

As coleções **Fields** dos objetos **Index**, **QueryDef**, **Relation** e **TableDef** contêm as especificações para os campos representados por aqueles objetos. A coleção **Fields** de um objeto **Recordset** representa os objetos **Field** em uma linha de dados ou em um registro. Você usa os objetos **Field** em um objeto **Recordset** para ler e definir valores para os campos no registro atual do objeto **Recordset**.

Nos espaços de trabalho do Microsoft Access, você manipula um campo utilizando um objeto **Field** e seus métodos e propriedades. Por exemplo, você pode:

  - Usar a propriedade **OrdinalPosition** para definir ou retornar a ordem de apresentação do objeto **Field** em uma coleção **Fields**.

  - Usar a propriedade **Value** de um campo em um objeto **Recordset** para definir ou retornar dados armazenados.

  - Usar os métodos **AppendChunk** e **GetChunk** e a propriedade **FieldSize** para obter ou definir um valor em um campo OLE Object ou Memo de um objeto **Recordset**.

  - Usar as propriedades **Type**, **Size** e **Attributes** para determinar o tipo de dados que pode ser armazenado no campo.

  - Usar as propriedades **SourceField** e **SourceTable** para determinar a fonte original dos dados.

  - Usar a propriedade **ForeignName** para definir ou retornar informações sobre um campo externo em um objeto **Relation**.

  - Usar as propriedades **AllowZeroLength**, **DefaultValue**, **Required**, **ValidateOnSet**, **ValidationRule** ou **ValidationText** para definir ou retornar as condições de validação.

  - Usar a propriedade **DefaultValue** de um campo em um objeto **TableDef** para definir o valor padrão desse campo quando novos registros forem adicionados.

Para criar um novo objeto **Field** em um objeto **Index**, **TableDef** ou **Relation**, use o método **CreateField**.

Quando você acessa um objeto **Field** como parte de um objeto **Recordset**, os dados do registro atual ficam visíveis na propriedade **Value** do objeto **Field**. Para manipular dados no objeto **Recordset**, você normalmente não faz referência à coleção **Fields** diretamente; em vez disso, você referencia indiretamente a propriedade **Value** do objeto **Field** na coleção **Fields** do objeto **Recordset**.

Para referir-se a um objeto **Field** de uma coleção pelo número ordinal ou pela configuração da propriedade **Name**, use qualquer uma das formas de sintaxe a seguir:

- **Campos**(0)

- **Campos**("nome")

- **Campos**\!\[nome\]

Com as mesmas formas de sintaxe, você também pode se referir à propriedade **Value** de um objeto **Field** criado e acrescentado à coleção **Fields**. O contexto da referência de campo determinará se você está se referindo ao objeto **Field** ou à propriedade **Value** do objeto **Field**.

## <a name="example"></a>Exemplo

This example shows what properties are valid for a **Field** object depending on where the **Field** resides (for example, the **Fields** collection of a **TableDef**, the **Fields** collection of a **QueryDef**, and so forth). The FieldOutput procedure is required for this procedure to run.

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

This example uses the **CreateField** method to create three **Fields** for a new **TableDef**. It then displays the properties of those **Field** objects that are automatically set by the **CreateField** method. (Properties whose values are empty at the time of **Field** creation are not shown.)

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
