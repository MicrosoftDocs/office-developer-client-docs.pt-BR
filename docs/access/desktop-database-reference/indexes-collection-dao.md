---
title: Coleção Indexes (DAO)
TOCTitle: Indexes Collection
ms:assetid: 26450e85-c79d-b12a-d760-dfc89c37f36c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191889(v=office.15)
ms:contentKeyID: 48543802
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a809afb8e38cf23faf43d5eb49c5edadaf70b2b1
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/07/2018
ms.locfileid: "26025830"
---
# <a name="indexes-collection-dao"></a><span data-ttu-id="321f5-102">Coleção Indexes (DAO)</span><span class="sxs-lookup"><span data-stu-id="321f5-102">Indexes collection (DAO)</span></span>

<span data-ttu-id="321f5-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="321f5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="321f5-104">Uma coleção **Indexes** contém todos os objetos **Index** armazenados de um objeto **TableDef** (somente espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="321f5-104">An **Indexes** collection contains all the stored **Index** objects of a **TableDef** object (Microsoft Access workspaces only).</span></span>

## <a name="remarks"></a><span data-ttu-id="321f5-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="321f5-105">Remarks</span></span>

<span data-ttu-id="321f5-p101">Quando acessar um objeto Recordset do tipo tabela, use a propriedade **Index** do objeto para especificar a ordem dos registros. Defina essa propriedade para a configuração da propriedade **Name** de um objeto **Index** existente na coleção **Indexes** do objeto **[TableDef](tabledef-object-dao.md)**, subjacente ao objeto **[Recordset](recordset-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="321f5-p101">When you access a table-type Recordset object, use the object's **Index** property to specify the order of records. Set this property to the **Name** property setting of an existing **Index** object in the **Indexes** collection of the **[TableDef](tabledef-object-dao.md)** object underlying the **[Recordset](recordset-object-dao.md)** object.</span></span>

> [!NOTE]
> <span data-ttu-id="321f5-108">[!OBSERVAçãO] É possível usar o método **Append** ou **Delete** numa coleção **Indexes** apenas se a configuração da propriedade **[Updatable](connection-updatable-property-dao.md)** do objeto contentor **TableDef** for **True**.</span><span class="sxs-lookup"><span data-stu-id="321f5-108">You can use the **Append** or **Delete** method on an **Indexes** collection only if the **[Updatable](connection-updatable-property-dao.md)** property setting of the containing **TableDef** object is **True**.</span></span>

<span data-ttu-id="321f5-109">Depois de criar um novo objeto **Index**, você deverá usar o método **Append** para adicioná-lo à coleção **Indexes** do objeto **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="321f5-109">After you create a new **Index** object, you should use the **Append** method to add it to the **TableDef** object's **Indexes** collection.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="321f5-p102">[!IMPORTANTE] Verifique se seus dados são adequados aos atributos de seu novo índice. Se o seu índice exigir valores únicos, assegure que não existam duplicatas nos registros de dados existentes. Se existirem duplicatas, o mecanismo do banco de dados do Microsoft Access não poderá criar o índice; ocorrerá um erro interceptável se você tentar usar o método Append no novo índice.</span><span class="sxs-lookup"><span data-stu-id="321f5-p102">Make sure your data complies with the attributes of your new index. If your index requires unique values, make sure that there are no duplicates in existing data records. If duplicates exist, the Microsoft Access database engine can't create the index; a trappable error results when you attempt to use the Append method on the new index.</span></span>

## <a name="example"></a><span data-ttu-id="321f5-113">Exemplo</span><span class="sxs-lookup"><span data-stu-id="321f5-113">Example</span></span>

<span data-ttu-id="321f5-p103">Este exemplo cria um novo objeto **Index**, acrescenta-o à coleção **Indexes** do **TableDef** Employees e enumera a coleção **Indexes** do **TableDef**. Por último, enumera um **Recordset**, primeiramente usando o **Index** principal em, em seguida, usando o novo **Index**. O procedimento IndexOutput é exigido para a execução deste procedimento.</span><span class="sxs-lookup"><span data-stu-id="321f5-p103">This example creates a new **Index** object, appends it to the **Indexes** collection of the Employees **TableDef**, and then enumerates the **Indexes** collection of the **TableDef**. Finally, it enumerates a **Recordset**, first using the primary **Index**, and then using the new **Index**. The IndexOutput procedure is required for this procedure to run.</span></span>

```vb
    Sub IndexObjectX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxNew As Index 
     Dim idxLoop As Index 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create new index, create and append Field 
     ' objects to its Fields collection. 
     Set idxNew = .CreateIndex("NewIndex") 
     
     With idxNew 
     .Fields.Append .CreateField("Country") 
     .Fields.Append .CreateField("LastName") 
     .Fields.Append .CreateField("FirstName") 
     End With 
     
     ' Add new Index object to the Indexes collection 
     ' of the Employees table collection. 
     .Indexes.Append idxNew 
     .Indexes.Refresh 
     
     Debug.Print .Indexes.Count & " Indexes in " & _ 
     .Name & " TableDef" 
     
     ' Enumerate Indexes collection of Employees 
     ' table. 
     For Each idxLoop In .Indexes 
     Debug.Print " " & idxLoop.Name 
     Next idxLoop 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     ' Print report using old and new indexes. 
     IndexOutput rstEmployees, "PrimaryKey" 
     IndexOutput rstEmployees, idxNew.Name 
     rstEmployees.Close 
     
     ' Delete new Index because this is a 
     ' demonstration. 
     .Indexes.Delete idxNew.Name 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub IndexOutput(rstTemp As Recordset, _ 
     strIndex As String) 
     ' Report function for FieldX. 
     
     With rstTemp 
     ' Set the index. 
     .Index = strIndex 
     .MoveFirst 
     Debug.Print "Recordset = " & .Name & _ 
     ", Index = " & .Index 
     Debug.Print " EmployeeID - Country - Name" 
     
     ' Enumerate the recordset using the specified 
     ' index. 
     Do While Not .EOF 
     Debug.Print " " & !EmployeeID & " - " & _ 
     !Country & " - " & !LastName & ", " & !FirstName 
     .MoveNext 
     Loop 
     
     End With 
     
    End Sub 
```

<br/>

<span data-ttu-id="321f5-p104">Este exemplo usa o método **CreateIndex** para criar dois novos objetos **Index** e acrescenta-os à coleção **Indexes** do objeto **TableDef** de Employees. Em seguida, é enumerada a coleção **Indexes** do objeto **TableDef**, a coleção **Fields** dos novos objetos **Index** e a coleção Properties dos novos objetos **Index**. A função CreateIndexOutput é exigida para a execução deste procedimento.</span><span class="sxs-lookup"><span data-stu-id="321f5-p104">This example uses the **CreateIndex** method to create two new **Index** objects and then appends them to the **Indexes** collection of the Employees **TableDef** object. It then enumerates the **Indexes** collection of the **TableDef** object, the **Fields** collection of the new **Index** objects, and the Properties collection of the new **Index** objects. The CreateIndexOutput function is required for this procedure to run.</span></span>

```vb
    Sub CreateIndexX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxCountry As Index 
     Dim idxFirstName As Index 
     Dim idxLoop As Index 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create first Index object, create and append Field 
     ' objects to the Index object, and then append the 
     ' Index object to the Indexes collection of the 
     ' TableDef. 
     Set idxCountry = .CreateIndex("CountryIndex") 
     With idxCountry 
     .Fields.Append .CreateField("Country") 
     .Fields.Append .CreateField("LastName") 
     .Fields.Append .CreateField("FirstName") 
     End With 
     .Indexes.Append idxCountry 
     
     ' Create second Index object, create and append Field 
     ' objects to the Index object, and then append the 
     ' Index object to the Indexes collection of the 
     ' TableDef. 
     Set idxFirstName = .CreateIndex 
     With idxFirstName 
     .Name = "FirstNameIndex" 
     .Fields.Append .CreateField("FirstName") 
     .Fields.Append .CreateField("LastName") 
     End With 
     .Indexes.Append idxFirstName 
     
     ' Refresh collection so that you can access new Index 
     ' objects. 
     .Indexes.Refresh 
     
     Debug.Print .Indexes.Count & " Indexes in " & _ 
     .Name & " TableDef" 
     
     ' Enumerate Indexes collection. 
     For Each idxLoop In .Indexes 
     Debug.Print " " & idxLoop.Name 
     Next idxLoop 
     
     ' Print report. 
     CreateIndexOutput idxCountry 
     CreateIndexOutput idxFirstName 
     
     ' Delete new Index objects because this is a 
     ' demonstration. 
     .Indexes.Delete idxCountry.Name 
     .Indexes.Delete idxFirstName.Name 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function CreateIndexOutput(idxTemp As Index) 
     
     Dim fldLoop As Field 
     Dim prpLoop As Property 
     
     With idxTemp 
     ' Enumerate Fields collection of Index object. 
     Debug.Print "Fields in " & .Name 
     For Each fldLoop In .Fields 
     Debug.Print " " & fldLoop.Name 
     Next fldLoop 
     
     ' Enumerate Properties collection of Index object. 
     Debug.Print "Properties of " & .Name 
     For Each prpLoop In .Properties 
     Debug.Print " " & prpLoop.Name & " - " & _ 
     IIf(prpLoop = "", "[empty]", prpLoop) 
     Next prpLoop 
     End With 
     
    End Function
```
