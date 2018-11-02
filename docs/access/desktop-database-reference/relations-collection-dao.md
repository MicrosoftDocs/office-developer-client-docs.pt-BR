---
title: Coleção Relations (DAO)
TOCTitle: Relations Collection
ms:assetid: 8929b5cc-cf52-03f2-8cf5-7f45276d258e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197067(v=office.15)
ms:contentKeyID: 48546153
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 78fdc7fc236a3e366cc97d466deb1e31cc030ac7
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919469"
---
# <a name="relations-collection-dao"></a><span data-ttu-id="fddf5-102">Coleção Relations (DAO)</span><span class="sxs-lookup"><span data-stu-id="fddf5-102">Relations collection (DAO)</span></span>


<span data-ttu-id="fddf5-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="fddf5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fddf5-104">Uma coleção **Relations** contém objetos **Relation** armazenados de um objeto **Database** (somente bancos de dados de mecanismo de banco de dados do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="fddf5-104">A **Relations** collection contains stored **Relation** objects of a **Database** object (Microsoft Access database engine databases only).</span></span>

## <a name="remarks"></a><span data-ttu-id="fddf5-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="fddf5-105">Remarks</span></span>

<span data-ttu-id="fddf5-p101">É possível usar o objeto **Relation** para criar novas relações e examinar relações existentes em seu banco de dados. Para adicionar um objeto **Relation** à coleção **Relations**, crie-o primeiramente com o método **CreateRelation** e, em seguida, acrescente-o à coleção **Relations** com o método **Append**. Isso salvará o objeto **Relation** quando você fechar o objeto **Database**. Para remover um objeto **Relation** da coleção, use o método **Delete**.</span><span class="sxs-lookup"><span data-stu-id="fddf5-p101">You can use the **Relation** object to create new relationships and examine existing relationships in your database. To add a **Relation** object to the **Relations** collection, first create it with the **CreateRelation** method, and then append it to the **Relations** collection with the **Append** method. This will save the **Relation** object when you close the **Database** object. To remove a **Relation** object from the collection, use the **Delete** method.</span></span>

<span data-ttu-id="fddf5-110">Para fazer referência a um objeto **Relation** em uma coleção por seu número ordinal ou por sua configuração de propriedade **Name**, use uma das seguintes formas de sintaxe:</span><span class="sxs-lookup"><span data-stu-id="fddf5-110">To refer to a **Relation** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="fddf5-111">**Relations**(0)</span><span class="sxs-lookup"><span data-stu-id="fddf5-111">**Relations**(0)</span></span>

<span data-ttu-id="fddf5-112">**Relações** ("nome")</span><span class="sxs-lookup"><span data-stu-id="fddf5-112">**Relations**("name")</span></span>

<span data-ttu-id="fddf5-113">**Relações**\!\[nome\]</span><span class="sxs-lookup"><span data-stu-id="fddf5-113">**Relations**\!\[name\]</span></span>

## <a name="example"></a><span data-ttu-id="fddf5-114">Exemplo</span><span class="sxs-lookup"><span data-stu-id="fddf5-114">Example</span></span>

<span data-ttu-id="fddf5-p102">Este exemplo mostra como um objeto **Relation** existente pode controlar a entrada de dados. O procedimento tenta adicionar um registro com uma CategoryID deliberadamente incorreta; isso dispara a rotina de tratamento de erros.</span><span class="sxs-lookup"><span data-stu-id="fddf5-p102">This example shows how an existing **Relation** object can control data entry. The procedure attempts to add a record with a deliberately incorrect CategoryID; this triggers the error-handling routine.</span></span>

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

<span data-ttu-id="fddf5-p103">Este exemplo usa o método **CreateRelation** para criar um objeto **Relation** entre **TableDef** de Funcionários e um novo **TableDef** chamado Departamentos. Este exemplo também demonstra como criar um novo objeto **Relation** também cria qualquer objeto **Indexes** necessários na tabela externa (o Índice DepartmentsEmployees na tabela Funcionários).</span><span class="sxs-lookup"><span data-stu-id="fddf5-p103">This example uses the **CreateRelation** method to create a **Relation** between the Employees **TableDef** and a new **TableDef** called Departments. This example also demonstrates how creating a new **Relation** will also create any necessary **Indexes** in the foreign table (the DepartmentsEmployees Index in the Employees table).</span></span>

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
