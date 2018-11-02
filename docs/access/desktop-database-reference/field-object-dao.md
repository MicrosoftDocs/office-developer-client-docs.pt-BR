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
# <a name="field-object-dao"></a>Objeto Field (DAO)

**Aplica-se a**: Access 2013, o Office 2013

Um objeto **Field** representa uma coluna de dados com um tipo de dados comum e um conjunto comum de propriedades.

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

- **Fields**(0)

- **Campos** ("nome")

- **Campos**\!\[nome\]

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
