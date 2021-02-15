---
title: Objeto Relation (DAO)
TOCTitle: Relation Object
ms:assetid: 46d6dfaf-a97d-3abd-0b4b-396a41eb3be7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193195(v=office.15)
ms:contentKeyID: 48544578
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3eeaf8bf46d8673731243a1161ac578062a01f89
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307032"
---
# <a name="relation-object-dao"></a>Objeto Relation (DAO)


**Aplica-se ao:** Access 2013, Office 2013

Um objeto **Relation** representa uma relação entre campos nas tabelas ou consultas (apenas bancos de dados do mecanismo de banco de dados do Microsoft Access).

## <a name="remarks"></a>Comentários

É possível usar o objeto **Relation** para criar novas relações e examinar relações existentes em seu banco de dados.

Utilizando um objeto **Relation** e suas propriedades, você pode:

  - Especificar uma relação imposta entre os campos nas tabelas de base (mas não uma relação que envolva uma consulta ou uma tabela vinculada).

  - Estabelecer relações não impostas entre qualquer tipo de tabela ou consulta  nativa ou vinculada.

  - Usar a propriedade **Name** para se referir à relação entre os campos na tabela primária referenciada e na tabela externa de referência.

  - Usar a propriedade **Attributes** para determinar se a relação entre os campos da tabela é um-para-um ou um-para-muitos, e como impor a integridade referencial.

  - Usar a propriedade **Attributes** para determinar se o mecanismo de banco de dados do Microsoft Access pode executar operações de atualização em cascata e de exclusão em cascata em tabelas principais e externas.

  - Usar a propriedade **Attributes** para determinar se a relação entre os campos da tabela é junção à esquerda ou junção à direita.

  - Usar a propriedade **Name** de todos os objetos **Field** da coleção **Fields** de um objeto **Relation** para definir ou retornar os nomes dos campos da chave primária da tabela referenciada, ou as configurações da propriedade **ForeignName** dos objetos **Field** para definir ou retornar os nomes dos campos da chave estrangeira da tabela de referência.

Se você fizer alterações que violem as relações estabelecidas para o banco de dados, ocorrerá um erro interceptável. Se você solicitar operações de atualização em cascata ou exclusão em cascata, o mecanismo de banco de dados do Microsoft Access também modificará as tabelas de chave primária ou chave estrangeira para impor as relações estabelecidas.

Por exemplo, o banco de dados Northwind contém uma relação entre uma tabela Pedidos e uma tabela Clientes. O campo CustomerID da tabela Clientes é a chave primária e o campo CustomerID da tabela Pedidos é a chave estrangeira. Para o mecanismo de banco de dados do Microsoft Access aceitar um novo registro na tabela Pedidos, ele procura na tabela Clientes uma correspondência no campo CustomerID da tabela Pedidos. Se não for encontrada uma correspondência, o mecanismo não aceitará o novo registro e ocorrerá um erro interceptável.

Quando você impõe a integridade referencial, um índice exclusivo já deve existir para o campo de chave da tabela referenciada. O mecanismo de banco de dados do Microsoft Access cria automaticamente um índice com a propriedade **Foreign** definida para agir como a chave estrangeira na tabela de referência.

Para criar um novo objeto **Relation**, use o método **CreateRelation**. Para se referir a um objeto **Relation** em uma coleção por seu número ordinal ou pela sua configuração da propriedade **Name**, use qualquer uma das formas de sintaxe a seguir:

**Relations**(0)

**Relations**("name")

 \! Relations \[ name\]

## <a name="example"></a>Exemplo

Este exemplo mostra como um objeto **Relation** existente pode controlar a entrada de dados. O procedimento tenta adicionar um registro com um CódigoDaCategoria propositalmente incorreto; isso dispara a rotina de tratamento de erros.

```vb 
    Sub RelationX() 
     
     Dim dbsNorthwind As Database 
     Dim rstProducts As Recordset 
     Dim prpLoop As Property 
     Dim fldLoop As Field 
     Dim errLoop As Error 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstProducts = dbsNorthwind.OpenRecordset("Products") 
     
     ' Print a report showing all the different parts of 
     ' the relation and where each part is stored. 
     With dbsNorthwind.Relations!CategoriesProducts 
     Debug.Print "Properties of " & .Name & " Relation" 
     Debug.Print " Table = " & .Table 
     Debug.Print " ForeignTable = " & .ForeignTable 
     Debug.Print "Fields of " & .Name & " Relation" 
     With .Fields!CategoryID 
     Debug.Print " " & .Name 
     Debug.Print " Name = " & .Name 
     Debug.Print " ForeignName = " & .ForeignName 
     End With 
     End With 
     
     ' Attempt to add a record that violates the relation. 
     With rstProducts 
     .AddNew 
     !ProductName = "Trygve's Lutefisk" 
     !CategoryID = 10 
     On Error GoTo Err_Relation 
     .Update 
     On Error GoTo 0 
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
     Exit Sub 
     
    Err_Relation: 
     
     ' Notify user of any errors that result from 
     ' the invalid data. 
     If DBEngine.Errors.Count > 0 Then 
     For Each errLoop In DBEngine.Errors 
     MsgBox "Error number: " & errLoop.Number & _ 
     vbCr & errLoop.Description 
     Next errLoop 
     End If 
     
     Resume Next 
     
    End Sub 
```

<br/>

Este exemplo usa o método **CreateRelation** para criar um objeto **Relation** entre o **TableDef** Employees e o novo **TableDef** denominado Departments. Ele também demonstra como a criação de  uma nova **Relação** também criará quaisquer índices necessários na tabela externa (o Índice DepartmentsEmployees na tabela Funcionários).

```vb
    Sub CreateRelationX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim tdfNew As TableDef 
     Dim idxNew As Index 
     Dim relNew As Relation 
     Dim idxLoop As Index 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Add new field to Employees table. 
     Set tdfEmployees = .TableDefs!Employees 
     tdfEmployees.Fields.Append _ 
     tdfEmployees.CreateField("DeptID", dbInteger, 2) 
     
     ' Create new Departments table. 
     Set tdfNew = .CreateTableDef("Departments") 
     
     With tdfNew 
     ' Create and append Field objects to Fields 
     ' collection of the new TableDef object. 
     .Fields.Append .CreateField("DeptID", dbInteger, 2) 
     .Fields.Append .CreateField("DeptName", dbText, 20) 
     
     ' Create Index object for Departments table. 
     Set idxNew = .CreateIndex("DeptIDIndex") 
     ' Create and append Field object to Fields 
     ' collection of the new Index object. 
     idxNew.Fields.Append idxNew.CreateField("DeptID") 
     ' The index in the primary table must be Unique in 
     ' order to be part of a Relation. 
     idxNew.Unique = True 
     .Indexes.Append idxNew 
     End With 
     
     .TableDefs.Append tdfNew 
     
     ' Create EmployeesDepartments Relation object, using 
     ' the names of the two tables in the relation. 
     Set relNew = .CreateRelation("EmployeesDepartments", _ 
     tdfNew.Name, tdfEmployees.Name, _ 
     dbRelationUpdateCascade) 
     
     ' Create Field object for the Fields collection of the 
     ' new Relation object. Set the Name and ForeignName 
     ' properties based on the fields to be used for the 
     ' relation. 
     relNew.Fields.Append relNew.CreateField("DeptID") 
     relNew.Fields!DeptID.ForeignName = "DeptID" 
     .Relations.Append relNew 
     
     ' Print report. 
     Debug.Print "Properties of " & relNew.Name & _ 
     " Relation" 
     Debug.Print " Table = " & relNew.Table 
     Debug.Print " ForeignTable = " & _ 
     relNew.ForeignTable 
     Debug.Print "Fields of " & relNew.Name & " Relation" 
     
     With relNew.Fields!DeptID 
     Debug.Print " " & .Name 
     Debug.Print " Name = " & .Name 
     Debug.Print " ForeignName = " & .ForeignName 
     End With 
     
     Debug.Print "Indexes in " & tdfEmployees.Name & _ 
     " TableDef" 
     For Each idxLoop In tdfEmployees.Indexes 
     Debug.Print " " & idxLoop.Name & _ 
     ", Foreign = " & idxLoop.Foreign 
     Next idxLoop 
     
     ' Delete new objects because this is a demonstration. 
     .Relations.Delete relNew.Name 
     .TableDefs.Delete tdfNew.Name 
     tdfEmployees.Fields.Delete "DeptID" 
     .Close 
     End With 
     
    End Sub
```
