---
title: Objeto Index-DAO (objetos de acesso a dados)
TOCTitle: Index object
ms:assetid: 92c32cad-ec8a-1243-1d18-83f50b269ecb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197655(v=office.15)
ms:contentKeyID: 48546380
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ca0a975017b5c5396d23817716689b37433d8f97
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291765"
---
# <a name="index-object-dao"></a><span data-ttu-id="2566e-102">Objeto Index (DAO)</span><span class="sxs-lookup"><span data-stu-id="2566e-102">Index object (DAO)</span></span>

<span data-ttu-id="2566e-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2566e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2566e-p101">Os objetos **Index** especificam a ordem dos registros acessados a partir de tabelas de banco de dados e se registros duplicados são aceitos, fornecendo acesso eficiente aos dados. Para bancos de dados externos, os objetos **Index** descrevem os índices estabelecidos para tabelas externas (apenas espaços de trabalho do Microsoft Access ).</span><span class="sxs-lookup"><span data-stu-id="2566e-p101">**Index** objects specify the order of records accessed from database tables and whether or not duplicate records are accepted, providing efficient access to data. For external databases, **Index** objects describe the indexes established for external tables (Microsoft Access workspaces only).</span></span>

## <a name="remarks"></a><span data-ttu-id="2566e-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="2566e-106">Remarks</span></span>

<span data-ttu-id="2566e-p102">O mecanismo de banco de dados do Microsoft Access usa índices quando ele une tabela e cria objetos **[Recordset](recordset-object-dao.md)**. Os índices determinam a ordem na qual os objetos **Recordset** tipo tabela retornam registros, mas não determinam a ordem na qual o mecanismo de banco de dados do Microsoft Access armazena registros na tabela base nem a ordem na qual qualquer outro tipo de objeto **Recordset** retorna registros.</span><span class="sxs-lookup"><span data-stu-id="2566e-p102">The Microsoft Access database engine uses indexes when it joins tables and creates **[Recordset](recordset-object-dao.md)** objects. Indexes determine the order in which table-type **Recordset** objects return records, but they don't determine the order in which the Microsoft Access database engine stores records in the base table or the order in which any other type of **Recordset** object returns records.</span></span>

<span data-ttu-id="2566e-109">Com um objeto **Index**, você pode:</span><span class="sxs-lookup"><span data-stu-id="2566e-109">With an **Index** object, you can:</span></span>

- <span data-ttu-id="2566e-110">Usar a propriedade **Required** para determinar se os objetos **[Field](field-object-dao.md)** no índice exigem ou não valores que não são Nulos e, em seguida, usar a propriedade **IgnoreNulls** para determinar se os valores nulos têm ou não entradas de índice.</span><span class="sxs-lookup"><span data-stu-id="2566e-110">Use the **Required** property to determine whether the **[Field](field-object-dao.md)** objects in the index require values that are not Null, and then use the **IgnoreNulls** property to determine whether the null values have index entries.</span></span>

- <span data-ttu-id="2566e-111">Usar as propriedades **Primary** e **Unique** para determinar a ordem e a exclusividade do objeto **Index**.</span><span class="sxs-lookup"><span data-stu-id="2566e-111">Use the **Primary** and **Unique** properties to determine the ordering and uniqueness of the **Index** object.</span></span>

<span data-ttu-id="2566e-p103">O mecanismo de banco de dados do Microsoft Access mantém todos os índices da tabela base automaticamente. Ele atualiza os índices sempre que você adiciona, altera ou exclui registros da tabela base. Após a criação do banco de dados, use o método **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** periodicamente para obter atualizações das estatísticas de índice.</span><span class="sxs-lookup"><span data-stu-id="2566e-p103">The Microsoft Access database engine maintains all base table indexes automatically. It updates indexes whenever you add, change, or delete records from the base table. Once you create the database, use the **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** method periodically to bring index statistics up-to-date.</span></span>

<span data-ttu-id="2566e-p104">Ao acessar um objeto **Recordset** tipo tabela, especifique a ordem dos registros utilizando a propriedade **Index** do objeto. Defina essa propriedade para a configuração da propriedade **Name** de um objeto **Index** existente na coleção **Indexes**. Essa coleção está contida no objeto **[TableDef](tabledef-object-dao.md)**, base do objeto **Recordset** que você está preenchendo.</span><span class="sxs-lookup"><span data-stu-id="2566e-p104">When accessing a table-type **Recordset** object, you specify the order of records using the object's **Index** property. Set this property to the **Name** property setting of an existing **Index** object in the **Indexes** collection. This collection is contained by the **[TableDef](tabledef-object-dao.md)** object underlying the **Recordset** object that you're populating.</span></span>

> [!NOTE]
> <span data-ttu-id="2566e-p105">[!OBSERVAçãO] Você não tem que criar índices para uma tabela, mas para tabelas grandes e não indexadas, acessar um registro específico ou processar associações pode demorar muito tempo. Por outro lado, ter muitos índices pode tornar mais lentas as atualizações para o banco de dados, pois cada índice de tabela é corrigido.</span><span class="sxs-lookup"><span data-stu-id="2566e-p105">You don't have to create indexes for a table, but for large, unindexed tables, accessing a specific record or processing joins can take a long time. Conversely, having too many indexes can slow down updates to the database as each of the table indexes is amended.</span></span>

<span data-ttu-id="2566e-120">A propriedade **[Attributes](field-attributes-property-dao.md)** de cada objeto **Field** no índice determina a ordem dos registros retornados e consequentemente determina quais técnicas de acesso serão utilizadas para aquele índice.</span><span class="sxs-lookup"><span data-stu-id="2566e-120">The **[Attributes](field-attributes-property-dao.md)** property of each **Field** object in the index determines the order of records returned and consequently determines which access techniques to use for that index.</span></span>

<span data-ttu-id="2566e-p106">Cada objeto **Field** na coleção **Fields** de um objeto **Index** é um componente do índice. Para definir um novo objeto **Index**, defina suas propriedades antes de acrescentá-lo a uma coleção, tornando o objeto **Index** disponível para uso subsequente.</span><span class="sxs-lookup"><span data-stu-id="2566e-p106">Each **Field** object in the **Fields** collection of an **Index** object is a component of the index. To define a new **Index** object, set its properties before you append it to a collection, making the **Index** object available for subsequent use.</span></span>

> [!NOTE]
> <span data-ttu-id="2566e-123">[!OBSERVAçãO] Você pode modificar a configuração da propriedade **Name** de um objeto **Index** existente somente se a configuração da propriedade **[Updatable](connection-updatable-property-dao.md)** do objeto **TableDef** contido for **True**.</span><span class="sxs-lookup"><span data-stu-id="2566e-123">You can modify the **Name** property setting of an existing **Index** object only if the **[Updatable](connection-updatable-property-dao.md)** property setting of the containing **TableDef** object is **True**.</span></span>

<span data-ttu-id="2566e-p107">Quando você define uma chave primária para uma tabela, o mecanismo de banco de dados do Microsoft Access define-a automaticamente como o índice principal. Este consiste em um ou mais campos que identificam todos os registros de uma tabela, de forma exclusiva, em uma ordem predefinida. Como o campo do índice principal deve ser exclusivo, o mecanismo de banco de dados do Microsoft Access define automaticamente a propriedade **Unique** do objeto **Index** principal como **True**. Se o índice principal consistir em mais de um campo, cada campo poderá conter valores duplicados, mas a combinação de valores de todos os campos indexados deve ser exclusiva. Um índice principal consiste em uma chave para a tabela e é sempre composto pelos mesmos campos que a chave primária.</span><span class="sxs-lookup"><span data-stu-id="2566e-p107">When you set a primary key for a table, the Microsoft Access database engine automatically defines it as the primary index. A primary index consists of one or more fields that uniquely identify all records in a table in a predefined order. Because the primary index field must be unique, the Microsoft Access database engine automatically sets the **Unique** property of the primary **Index** object to **True**. If the primary index consists of more than one field, each field can contain duplicate values, but the combination of values from all the indexed fields must be unique. A primary index consists of a key for the table and is always made up of the same fields as the primary key.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2566e-p108">[!IMPORTANTE] Certifique-se de que os dados sejam compatíveis com os atributos do novo índice. Se o índice exigir valores exclusivos, certifique-se de que não haja duplicatas nos registros de dados existentes. Se houver duplicatas, o mecanismo de banco de dados do Microsoft Access não poderá criar o índice ; ocorrerá um erro interceptável quando você tentar usar o método Append no novo índice.</span><span class="sxs-lookup"><span data-stu-id="2566e-p108">Make sure your data complies with the attributes of your new index. If your index requires unique values, make sure that there are no duplicates in existing data records. If duplicates exist, the Microsoft Access database engine can't create the index; a trappable error results when you attempt to use the Append method on the new index.</span></span>

<span data-ttu-id="2566e-p109">Quando você cria uma relação que impõe a integridade referencial, o mecanismo de banco de dados do Microsoft Access cria automaticamente um índice com a propriedade **Foreign** definida como a chave estrangeira na tabela de referência. Depois que você estabelece uma relação de tabela, o mecanismo de banco de dados do Microsoft Access impede que sejam feitas inclusões ou alterações no banco de dados que violem essa relação. Se você definir a propriedade **Attributes** do objeto **[Relation](relation-object-dao.md)** para permitir atualizações em cascata e exclusões em cascata, o mecanismo de banco de dados do Microsoft Access atualizará ou excluirá automaticamente os registros das tabelas relacionadas.</span><span class="sxs-lookup"><span data-stu-id="2566e-p109">When you create a relationship that enforces referential integrity, the Microsoft Access database engine automatically creates an index with the **Foreign** property, set as the foreign key in the referencing table. After you've established a table relationship, the Microsoft Access database engine prevents additions or changes to the database that violate that relationship. If you set the **Attributes** property of the **[Relation](relation-object-dao.md)** object to allow cascading updates and cascading deletes, the Microsoft Access database engine updates or deletes records in related tables automatically.</span></span>

1.  <span data-ttu-id="2566e-135">Use o método **CreateIndex** em um objeto **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="2566e-135">Use the **CreateIndex** method on a **TableDef** object.</span></span>

2.  <span data-ttu-id="2566e-136">Use o método **CreateField** no objeto **Index** para criar um objeto **Field** para cada campo (coluna) a ser incluído no objeto **Index**.</span><span class="sxs-lookup"><span data-stu-id="2566e-136">Use the **CreateField** method on the **Index** object to create a **Field** object for each field (column) to be included in the **Index** object.</span></span>

3.  <span data-ttu-id="2566e-137">Defina as propriedades **Index** conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="2566e-137">Set **Index** properties as needed.</span></span>

4.  <span data-ttu-id="2566e-138">Acrescente o objeto **Field** na coleção **Fields**.</span><span class="sxs-lookup"><span data-stu-id="2566e-138">Append the **Field** object to the **Fields** collection.</span></span>

5.  <span data-ttu-id="2566e-139">Acrescente o objeto **Index** na coleção **Indexes**.</span><span class="sxs-lookup"><span data-stu-id="2566e-139">Append the **Index** object to the **Indexes** collection.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2566e-140">[!OBSERVAçãO] A propriedade **Clustered** é ignorada para bancos de dados que usam o mecanismo de banco de dados do Microsoft Access, que não aceita índices agrupados.</span><span class="sxs-lookup"><span data-stu-id="2566e-140">The **Clustered** property is ignored for databases that use the Microsoft Access database engine, which doesn't support clustered indexes.</span></span>

## <a name="example"></a><span data-ttu-id="2566e-141">Exemplo</span><span class="sxs-lookup"><span data-stu-id="2566e-141">Example</span></span>

<span data-ttu-id="2566e-p110">Este exemplo cria um novo objeto **Index**, acrescenta-o à coleção **Indexes** do **TableDef** Employees e enumera a coleção **Indexes** do **TableDef**. Por último, enumera um **Recordset**, primeiramente usando o **Index** principal em, em seguida, usando o novo **Index**. O procedimento IndexOutput é exigido para a execução deste procedimento.</span><span class="sxs-lookup"><span data-stu-id="2566e-p110">This example creates a new **Index** object, appends it to the **Indexes** collection of the Employees **TableDef**, and then enumerates the **Indexes** collection of the **TableDef**. Finally, it enumerates a **Recordset**, first using the primary **Index**, and then using the new **Index**. The IndexOutput procedure is required for this procedure to run.</span></span>

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

<span data-ttu-id="2566e-p111">Este exemplo usa o método **CreateIndex** para criar dois novos objetos **Index** e acrescenta-os à coleção **Indexes** do objeto **TableDef** de Employees. Em seguida, é enumerada a coleção **Indexes** do objeto **TableDef**, a coleção **Fields** dos novos objetos **Index** e a coleção Properties dos novos objetos **Index**. A função CreateIndexOutput é exigida para a execução deste procedimento.</span><span class="sxs-lookup"><span data-stu-id="2566e-p111">This example uses the **CreateIndex** method to create two new **Index** objects and then appends them to the **Indexes** collection of the Employees **TableDef** object. It then enumerates the **Indexes** collection of the **TableDef** object, the **Fields** collection of the new **Index** objects, and the Properties collection of the new **Index** objects. The CreateIndexOutput function is required for this procedure to run.</span></span>

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
