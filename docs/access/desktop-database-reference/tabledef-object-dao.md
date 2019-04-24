---
title: Objeto TableDef
TOCTitle: TableDef Object
ms:assetid: 715146b6-c62a-abff-28ee-e6bbe3c08adf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195790(v=office.15)
ms:contentKeyID: 48545582
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 6e1182427c688e7c8b5ca53c1f5f4bb208b3609a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308369"
---
# <a name="tabledef-object-dao"></a><span data-ttu-id="85b9b-102">Objeto TableDef</span><span class="sxs-lookup"><span data-stu-id="85b9b-102">TableDef object (DAO)</span></span>

<span data-ttu-id="85b9b-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="85b9b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="85b9b-104">Um objeto **TableDef** representa a definição armazenada de uma tabela vinculada ou uma tabela base (apenas espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="85b9b-104">A **TableDef** object represents the stored definition of a base table or a linked table (Microsoft Access workspaces only).</span></span>

## <a name="remarks"></a><span data-ttu-id="85b9b-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="85b9b-105">Remarks</span></span>

<span data-ttu-id="85b9b-p101">Você manipula uma definição de tabela utilizando um objeto **TableDef** e seus métodos e suas propriedades. Por exemplo, você pode:</span><span class="sxs-lookup"><span data-stu-id="85b9b-p101">You manipulate a table definition using a **TableDef** object and its methods and properties. For example, you can:</span></span>

- <span data-ttu-id="85b9b-108">Examinar o campo e a estrutura de índice de qualquer tabela local, vinculada ou externa em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="85b9b-108">Examine the field and index structure of any local, linked, or external table in a database.</span></span>

- <span data-ttu-id="85b9b-109">Usar as propriedades **Connect** e **SourceTableName** para definir ou retornar informações sobre tabelas vinculadas e usar o método **RefreshLink** para atualizar conexões com as tabelas vinculadas.</span><span class="sxs-lookup"><span data-stu-id="85b9b-109">Use the **Connect** and **SourceTableName** properties to set or return information about linked tables, and use the **RefreshLink** method to update connections to linked tables.</span></span>

- <span data-ttu-id="85b9b-110">Use as propriedades **ValidationRule** e **ValidationText** para definir ou retornar condições de validação.</span><span class="sxs-lookup"><span data-stu-id="85b9b-110">Use the **ValidationRule** and **ValidationText** properties to set or return validation conditions.</span></span>

- <span data-ttu-id="85b9b-111">Use o método **OpenRecordset** para criar uma tabela, dynaset –, dinâmica –, instantânea –, ou objeto tipo-encaminhar– somente **conjunto de registros** com base na definição da tabela.</span><span class="sxs-lookup"><span data-stu-id="85b9b-111">Use the **OpenRecordset** method to create a table–, dynaset–, dynamic–, snapshot–, or forward–only–type **Recordset** object, based on the table definition.</span></span>

<span data-ttu-id="85b9b-112">Para tabelas de base, a propriedade **RecordCount** contém o número de registros da tabela de banco de dados específico.</span><span class="sxs-lookup"><span data-stu-id="85b9b-112">For base tables, the **RecordCount** property contains the number of records in the specified database table.</span></span> <span data-ttu-id="85b9b-113">Para tabelas vinculadas, a configuração **RecordCount** de propriedade é sempre – 1.</span><span class="sxs-lookup"><span data-stu-id="85b9b-113">For linked tables, the **RecordCount** property setting is always –1.</span></span>

<span data-ttu-id="85b9b-114">Para criar um novo objeto **TableDef**, use o \*\* método [CreateTableDef](database-createtabledef-method-dao.md) \*\*.</span><span class="sxs-lookup"><span data-stu-id="85b9b-114">To create a new **TableDef** object, use the **[CreateTableDef](database-createtabledef-method-dao.md)** method.</span></span>

### <a name="to-add-a-field-to-a-table"></a><span data-ttu-id="85b9b-115">Para adicionar um campo a uma tabela</span><span class="sxs-lookup"><span data-stu-id="85b9b-115">To add a field to a table</span></span>

1.  <span data-ttu-id="85b9b-116">Certifique-se de que quaisquer objetos **[Recordset](recordset-object-dao.md)** baseados na tabela estejam fechados.</span><span class="sxs-lookup"><span data-stu-id="85b9b-116">Make sure any **[Recordset](recordset-object-dao.md)** objects based on the table are all closed.</span></span>

2.  <span data-ttu-id="85b9b-117">Use o método **CreateField** para criar uma variável de objeto **Field** e definir suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="85b9b-117">Use the **CreateField** method to create a **Field** object variable and set its properties.</span></span>

3.  <span data-ttu-id="85b9b-118">Use o método **Append** para adicionar o objeto **Field** à coleção **Fields** do objeto **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="85b9b-118">Use the **Append** method to add the **Field** object to the **Fields** collection of the **TableDef** object.</span></span>

<span data-ttu-id="85b9b-119">Você pode excluir um objeto **Field** de uma coleção **TableDefs** se ele não tiver nenhum índice atribuído a ele, mas os dados do campo não serão perdidos.</span><span class="sxs-lookup"><span data-stu-id="85b9b-119">You can delete a **Field** object from a **TableDefs** collection if it doesn't have any indexes assigned to it, but you will lose the field's data.</span></span>

### <a name="to-create-a-table-that-is-ready-for-new-records-in-a-database"></a><span data-ttu-id="85b9b-120">Para criar uma tabela que esteja pronta para novos registros em um banco de dados</span><span class="sxs-lookup"><span data-stu-id="85b9b-120">To create a table that is ready for new records in a database</span></span>

1.  <span data-ttu-id="85b9b-121">Use o método **CreateTableDef** para criar um objeto **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="85b9b-121">Use the **CreateTableDef** method to create a **TableDef** object.</span></span>

2.  <span data-ttu-id="85b9b-122">Defina suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="85b9b-122">Set its properties.</span></span>

3.  <span data-ttu-id="85b9b-123">Para cada campo na tabela, use o método **CreateField** para criar uma variável de objeto **Field** e definir suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="85b9b-123">For each field in the table, use the **CreateField** method to create a **Field** object variable and set its properties.</span></span>

4.  <span data-ttu-id="85b9b-124">Use o método **Append** para adicionar campos à coleção **Fields** do objeto **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="85b9b-124">Use the **Append** method to add the fields to the **Fields** collection of the **TableDef** object.</span></span>

5.  <span data-ttu-id="85b9b-125">Use o método **Append** para adicionar o novo objeto **TableDef** à coleção **TableDefs** do objeto **Database**.</span><span class="sxs-lookup"><span data-stu-id="85b9b-125">Use the **Append** method to add the new **TableDef** object to the **TableDefs** collection of the **Database** object.</span></span>

<span data-ttu-id="85b9b-126">Uma tabela vinculada é conectada ao banco de dados pelas propriedades **SourceTableName** e **Connect** do objeto **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="85b9b-126">A linked table is connected to the database by the **SourceTableName** and **Connect** properties of the **TableDef** object.</span></span>

### <a name="to-link-a-table-to-a-database"></a><span data-ttu-id="85b9b-127">Para vincular uma tabela a um banco de dados</span><span class="sxs-lookup"><span data-stu-id="85b9b-127">To link a table to a database</span></span>

1.  <span data-ttu-id="85b9b-128">Use o método **CreateTableDef** para criar um objeto **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="85b9b-128">Use the **CreateTableDef** method to create a **TableDef** object.</span></span>

2.  <span data-ttu-id="85b9b-129">Defina suas propriedades **Connect** e **SourceTableName** (e, como opção, sua propriedade **Attributes**).</span><span class="sxs-lookup"><span data-stu-id="85b9b-129">Set its **Connect** and **SourceTableName** properties (and optionally, its **Attributes** property).</span></span>

3.  <span data-ttu-id="85b9b-130">Use o método **Append** para adicioná-lo à coleção **TableDefs** de um **Database**.</span><span class="sxs-lookup"><span data-stu-id="85b9b-130">Use the **Append** method to add it to the **TableDefs** collection of a **Database**.</span></span>

<span data-ttu-id="85b9b-131">Para referir-se a um objeto **TableDef** de uma coleção pelo número ordinal ou pela configuração da propriedade **Name**, use qualquer uma das formas de sintaxe a seguir:</span><span class="sxs-lookup"><span data-stu-id="85b9b-131">To refer to a **TableDef** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="85b9b-132">**TableDefs**(0)</span><span class="sxs-lookup"><span data-stu-id="85b9b-132">**TableDefs**(0)</span></span>

<span data-ttu-id="85b9b-133">**TableDefs**("nome")</span><span class="sxs-lookup"><span data-stu-id="85b9b-133">**TableDefs**("name")</span></span>

<span data-ttu-id="85b9b-134">**TableDefs**\!\[nome\]</span><span class="sxs-lookup"><span data-stu-id="85b9b-134">**TableDefs**\!\[name\]</span></span>

## <a name="example"></a><span data-ttu-id="85b9b-135">Exemplo</span><span class="sxs-lookup"><span data-stu-id="85b9b-135">Example</span></span>

<span data-ttu-id="85b9b-p103">Este exemplo cria um novo objeto **TableDef** e o acrescenta à coleção **TableDefs** do objeto Database Northwind. Em seguida, enumeram-se as coleções **TableDefs** e **Properties** do novo **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="85b9b-p103">This example creates a new **TableDef** object and appends it to the **TableDefs** collection of the Northwind Database object. It then enumerates the **TableDefs** collection and the **Properties** collection of the new **TableDef**.</span></span>

```vb
    Sub TableDefX() 
     
       Dim dbsNorthwind As Database 
       Dim tdfNew As TableDef 
       Dim tdfLoop As TableDef 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       ' Create new TableDef object, append Field objects  
       ' to its Fields collection, and append TableDef  
       ' object to the TableDefs collection of the  
       ' Database object. 
       Set tdfNew = dbsNorthwind.CreateTableDef("NewTableDef") 
       tdfNew.Fields.Append tdfNew.CreateField("Date", dbDate) 
       dbsNorthwind.TableDefs.Append tdfNew 
     
       With dbsNorthwind 
          Debug.Print .TableDefs.Count & _ 
             " TableDefs in " & .Name 
     
          ' Enumerate TableDefs collection. 
          For Each tdfLoop In .TableDefs 
             Debug.Print "  " & tdfLoop.Name 
          Next tdfLoop 
     
          With tdfNew 
             Debug.Print "Properties of " & .Name 
     
             ' Enumerate Properties collection of new 
             ' TableDef object, only printing properties 
             ' with non-empty values. 
             For Each prpLoop In .Properties 
                Debug.Print "  " & prpLoop.Name & " - " & _ 
                   IIf(prpLoop = "", "[empty]", prpLoop) 
             Next prpLoop 
     
          End With 
     
          ' Delete new TableDef since this is a  
          ' demonstration. 
          .TableDefs.Delete tdfNew.Name 
          .Close 
       End With 
     
    End Sub 
```

<br/>

<span data-ttu-id="85b9b-138">Este exemplo cria um novo objeto **TableDef** no banco de dados da Northwind.</span><span class="sxs-lookup"><span data-stu-id="85b9b-138">This example creates a new **TableDef** object in the Northwind database.</span></span>

```vb 
Sub CreateTableDefX() 
 
   Dim dbsNorthwind As Database 
   Dim tdfNew As TableDef 
   Dim prpLoop As Property 
 
   Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
   ' Create a new TableDef object. 
   Set tdfNew = dbsNorthwind.CreateTableDef("Contacts") 
 
   With tdfNew 
      ' Create fields and append them to the new TableDef  
      ' object. This must be done before appending the  
      ' TableDef object to the TableDefs collection of the  
      ' Northwind database. 
      .Fields.Append .CreateField("FirstName", dbText) 
      .Fields.Append .CreateField("LastName", dbText) 
      .Fields.Append .CreateField("Phone", dbText) 
      .Fields.Append .CreateField("Notes", dbMemo) 
 
      Debug.Print "Properties of new TableDef object " & _ 
         "before appending to collection:" 
 
      ' Enumerate Properties collection of new TableDef  
      ' object. 
      For Each prpLoop In .Properties 
         On Error Resume Next 
         If prpLoop <> "" Then Debug.Print "  " & _ 
           prpLoop.Name & " = " & prpLoop 
         On Error GoTo 0 
      Next prpLoop 
 
      ' Append the new TableDef object to the Northwind  
      ' database. 
      dbsNorthwind.TableDefs.Append tdfNew 
 
      Debug.Print "Properties of new TableDef object " & _ 
         "after appending to collection:" 
 
      ' Enumerate Properties collection of new TableDef  
      ' object. 
      For Each prpLoop In .Properties 
         On Error Resume Next 
         If prpLoop <> "" Then Debug.Print "  " & _ 
           prpLoop.Name & " = " & prpLoop 
         On Error GoTo 0 
      Next prpLoop 
 
   End With 
 
   ' Delete new TableDef object since this is a  
   ' demonstration. 
   dbsNorthwind.TableDefs.Delete "Contacts" 
 
   dbsNorthwind.Close 
```

<br/>

<span data-ttu-id="85b9b-139">O exemplo a seguir mostra como criar um item de lista.</span><span class="sxs-lookup"><span data-stu-id="85b9b-139">The following example shows how to create a calculated field.</span></span> <span data-ttu-id="85b9b-140">O método CreateField cria um campo denominado **NomeCompleto**.</span><span class="sxs-lookup"><span data-stu-id="85b9b-140">The CreateField method creates a field named **FullName**.</span></span> <span data-ttu-id="85b9b-141">A propriedade de expressão, em seguida, está definida como a expressão que calcula o valor do campo.</span><span class="sxs-lookup"><span data-stu-id="85b9b-141">The Expression property is then set to the expression that calculates the value of the field.</span></span>

<span data-ttu-id="85b9b-142">**Código de exemplo fornecido por:** a [Referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="85b9b-142">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Sub CreateCalculatedField()
        Dim dbs As DAO.Database
        Dim tdf As DAO.TableDef
        Dim fld As DAO.Field2
        
        ' get the database
        Set dbs = CurrentDb()
        
        ' create the table
        Set tdf = dbs.CreateTableDef("tblContactsCalcField")
        
        ' create the fields: first name, last name
        tdf.Fields.Append tdf.CreateField("FirstName", dbText, 20)
        tdf.Fields.Append tdf.CreateField("LastName", dbText, 20)
        
        ' create the calculated field: full name
        Set fld = tdf.CreateField("FullName", dbText, 50)
        fld.Expression = "[FirstName] & "" "" & [LastName]"
        tdf.Fields.Append fld
        
        ' append the table and cleanup
        dbs.TableDefs.Append tdf
        
    Cleanup:
        Set fld = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
    End Sub
```
