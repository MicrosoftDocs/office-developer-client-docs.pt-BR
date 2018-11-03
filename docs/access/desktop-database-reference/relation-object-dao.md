---
title: Objeto Relation (DAO)
TOCTitle: Relation Object
ms:assetid: 46d6dfaf-a97d-3abd-0b4b-396a41eb3be7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193195(v=office.15)
ms:contentKeyID: 48544578
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 49e8cdb7586af93ca17782ba0cb1071036c38eeb
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936949"
---
# <a name="relation-object-dao"></a><span data-ttu-id="91498-102">Objeto Relation (DAO)</span><span class="sxs-lookup"><span data-stu-id="91498-102">Relation object (DAO)</span></span>


<span data-ttu-id="91498-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="91498-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="91498-104">Um objeto **Relation** representa uma relação entre campos nas tabelas ou consultas (apenas bancos de dados do mecanismo de banco de dados do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="91498-104">A **Relation** object represents a relationship between fields in tables or queries (Microsoft Access database engine databases only).</span></span>

## <a name="remarks"></a><span data-ttu-id="91498-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="91498-105">Remarks</span></span>

<span data-ttu-id="91498-106">É possível usar o objeto **Relation** para criar novas relações e examinar relações existentes em seu banco de dados.</span><span class="sxs-lookup"><span data-stu-id="91498-106">You can use the **Relation** object to create new relationships and examine existing relationships in your database.</span></span>

<span data-ttu-id="91498-107">Utilizando um objeto **Relation** e suas propriedades, você pode:</span><span class="sxs-lookup"><span data-stu-id="91498-107">Using a **Relation** object and its properties, you can:</span></span>

  - <span data-ttu-id="91498-108">Especificar uma relação imposta entre os campos nas tabelas de base (mas não uma relação que envolva uma consulta ou uma tabela vinculada).</span><span class="sxs-lookup"><span data-stu-id="91498-108">Specify an enforced relationship between fields in base tables (but not a relationship that involves a query or a linked table).</span></span>

  - <span data-ttu-id="91498-109">Estabelecer relações não impostas entre qualquer tipo de tabela ou consulta  nativa ou vinculada.</span><span class="sxs-lookup"><span data-stu-id="91498-109">Establish unenforced relationships between any type of table or query— native or linked.</span></span>

  - <span data-ttu-id="91498-110">Usar a propriedade **Name** para se referir à relação entre os campos na tabela primária referenciada e na tabela externa de referência.</span><span class="sxs-lookup"><span data-stu-id="91498-110">Use the **Name** property to refer to the relationship between the fields in the referenced primary table and the referencing foreign table.</span></span>

  - <span data-ttu-id="91498-111">Usar a propriedade **Attributes** para determinar se a relação entre os campos da tabela é um-para-um ou um-para-muitos, e como impor a integridade referencial.</span><span class="sxs-lookup"><span data-stu-id="91498-111">Use the **Attributes** property to determine whether the relationship between fields in the table is one-to-one or one-to-many and how to enforce referential integrity.</span></span>

  - <span data-ttu-id="91498-112">Usar a propriedade **Attributes** para determinar se o mecanismo de banco de dados do Microsoft Access pode executar operações de atualização em cascata e de exclusão em cascata em tabelas principais e externas.</span><span class="sxs-lookup"><span data-stu-id="91498-112">Use the **Attributes** property to determine whether the Microsoft Access database engine can perform cascading update and cascading delete operations on primary and foreign tables.</span></span>

  - <span data-ttu-id="91498-113">Usar a propriedade **Attributes** para determinar se a relação entre os campos da tabela é junção à esquerda ou junção à direita.</span><span class="sxs-lookup"><span data-stu-id="91498-113">Use the **Attributes** property to determine whether the relationship between fields in the table is left join or right join.</span></span>

  - <span data-ttu-id="91498-114">Usar a propriedade **Name** de todos os objetos **Field** da coleção **Fields** de um objeto **Relation** para definir ou retornar os nomes dos campos da chave primária da tabela referenciada, ou as configurações da propriedade **ForeignName** dos objetos **Field** para definir ou retornar os nomes dos campos da chave estrangeira da tabela de referência.</span><span class="sxs-lookup"><span data-stu-id="91498-114">Use the **Name** property of all **Field** objects in the **Fields** collection of a **Relation** object to set or return the names of the fields in the primary key of the referenced table, or the **ForeignName** property settings of the **Field** objects to set or return the names of the fields in the foreign key of the referencing table.</span></span>

<span data-ttu-id="91498-p101">Se você fizer alterações que violem as relações estabelecidas para o banco de dados, ocorrerá um erro interceptável. Se você solicitar operações de atualização em cascata ou exclusão em cascata, o mecanismo de banco de dados do Microsoft Access também modificará as tabelas de chave primária ou chave estrangeira para impor as relações estabelecidas.</span><span class="sxs-lookup"><span data-stu-id="91498-p101">If you make changes that violate the relationships established for the database, a trappable error occurs. If you request cascading update or cascading delete operations, the Microsoft Access database engine also modifies the primary key or foreign key tables to enforce the relationships you establish.</span></span>

<span data-ttu-id="91498-p102">Por exemplo, o banco de dados Northwind contém uma relação entre uma tabela Pedidos e uma tabela Clientes. O campo CustomerID da tabela Clientes é a chave primária e o campo CustomerID da tabela Pedidos é a chave estrangeira. Para o mecanismo de banco de dados do Microsoft Access aceitar um novo registro na tabela Pedidos, ele procura na tabela Clientes uma correspondência no campo CustomerID da tabela Pedidos. Se não for encontrada uma correspondência, o mecanismo não aceitará o novo registro e ocorrerá um erro interceptável.</span><span class="sxs-lookup"><span data-stu-id="91498-p102">For example, the Northwind database contains a relationship between an Orders table and a Customers table. The CustomerID field of the Customers table is the primary key, and the CustomerID field of the Orders table is the foreign key. For the Microsoft Access database engine to accept a new record in the Orders table, it searches the Customers table for a match on the CustomerID field of the Orders table. If the Microsoft Access database engine doesn't find a match, it doesn't accept the new record, and a trappable error occurs.</span></span>

<span data-ttu-id="91498-p103">Quando você impõe a integridade referencial, um índice exclusivo já deve existir para o campo de chave da tabela referenciada. O mecanismo de banco de dados do Microsoft Access cria automaticamente um índice com a propriedade **Foreign** definida para agir como a chave estrangeira na tabela de referência.</span><span class="sxs-lookup"><span data-stu-id="91498-p103">When you enforce referential integrity, a unique index must already exist for the key field of the referenced table. The Microsoft Access database engine automatically creates an index with the **Foreign** property set to act as the foreign key in the referencing table.</span></span>

<span data-ttu-id="91498-p104">Para criar um novo objeto **Relation**, use o método **CreateRelation**. Para se referir a um objeto **Relation** em uma coleção por seu número ordinal ou pela sua configuração da propriedade **Name**, use qualquer uma das formas de sintaxe a seguir:</span><span class="sxs-lookup"><span data-stu-id="91498-p104">To create a new **Relation** object, use the **CreateRelation** method. To refer to a **Relation** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="91498-125">**Relations**(0)</span><span class="sxs-lookup"><span data-stu-id="91498-125">**Relations**(0)</span></span>

<span data-ttu-id="91498-126">**Relações** ("nome")</span><span class="sxs-lookup"><span data-stu-id="91498-126">**Relations**("name")</span></span>

<span data-ttu-id="91498-127">**Relações**\!\[nome\]</span><span class="sxs-lookup"><span data-stu-id="91498-127">**Relations**\!\[name\]</span></span>

## <a name="example"></a><span data-ttu-id="91498-128">Exemplo</span><span class="sxs-lookup"><span data-stu-id="91498-128">Example</span></span>

<span data-ttu-id="91498-p105">Este exemplo mostra como um objeto **Relation** existente pode controlar a entrada de dados. O procedimento tenta adicionar um registro com uma CategoryID deliberadamente incorreta; isso dispara a rotina de tratamento de erros.</span><span class="sxs-lookup"><span data-stu-id="91498-p105">This example shows how an existing **Relation** object can control data entry. The procedure attempts to add a record with a deliberately incorrect CategoryID; this triggers the error-handling routine.</span></span>

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

<span data-ttu-id="91498-131">Este exemplo usa o método **CreateRelation** para criar um objeto **Relation** entre **TableDef** de Funcionários e um novo **TableDef** chamado Departamentos.</span><span class="sxs-lookup"><span data-stu-id="91498-131">This example uses the **CreateRelation** method to create a **Relation** between the Employees **TableDef** and a new **TableDef** called Departments.</span></span> <span data-ttu-id="91498-132">Ele também demonstra como criar um novo **Relation** também criará qualquer necessário **índices** da tabela externa (o índice DepartmentsEmployees na tabela Funcionários).</span><span class="sxs-lookup"><span data-stu-id="91498-132">It also demonstrates how creating a new **Relation** will also create any necessary **Indexes** in the foreign table (the DepartmentsEmployees Index in the Employees table).</span></span>

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
