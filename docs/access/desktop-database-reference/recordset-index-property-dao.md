---
title: Propriedade Recordset.Index (DAO)
TOCTitle: Index Property
ms:assetid: 54626de0-eb51-31f2-bf24-e29cbfbbaa02
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194103(v=office.15)
ms:contentKeyID: 48544895
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052906
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 01a19fd621d8124616872bebc54c6ac9482ffe08
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464901"
---
# <a name="recordsetindex-property-dao"></a><span data-ttu-id="c9dfe-102">Propriedade Recordset.Index (DAO)</span><span class="sxs-lookup"><span data-stu-id="c9dfe-102">Recordset.Index Property (DAO)</span></span>

<span data-ttu-id="c9dfe-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c9dfe-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c9dfe-104">Define ou retorna um valor que indica o nome do objeto **[Index](index-object-dao.md)** atual em um objeto **[Recordset](recordset-object-dao.md)** do tipo tabela (somente nos espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="c9dfe-104">Sets or returns a value that indicates the name of the current **[Index](index-object-dao.md)** object in a table-type **[Recordset](recordset-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="c9dfe-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c9dfe-105">Syntax</span></span>

<span data-ttu-id="c9dfe-106">*expressão* . Índice</span><span class="sxs-lookup"><span data-stu-id="c9dfe-106">*expression* .Index</span></span>

<span data-ttu-id="c9dfe-107">*expressão* Uma variável que representa um objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="c9dfe-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9dfe-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="c9dfe-108">Remarks</span></span>

<span data-ttu-id="c9dfe-p101">Os registros nas tabelas base não estão armazenados em uma ordem específica. A definição da propriedade **Index** altera a ordem dos registros retornada do banco de dados. Não afeta a ordem na qual os registros são armazenados.</span><span class="sxs-lookup"><span data-stu-id="c9dfe-p101">Records in base tables aren't stored in any particular order. Setting the **Index** property changes the order of records returned from the database; it doesn't affect the order in which the records are stored.</span></span>

<span data-ttu-id="c9dfe-p102">O objeto **Index** especificado já deve estar definido. Se você definir a propriedade **Index** como um objeto **Index** que não existe ou se a propriedade **Index** não estiver definida quando você usar o método **[Seek](recordset-seek-method-dao.md)**, ocorrerá um erro interceptável.</span><span class="sxs-lookup"><span data-stu-id="c9dfe-p102">The specified **Index** object must already be defined. If you set the **Index** property to an **Index** object that doesn't exist or if the **Index** property isn't set when you use the **[Seek](recordset-seek-method-dao.md)** method, a trappable error occurs.</span></span>

<span data-ttu-id="c9dfe-113">Examine a coleção **Indexes** de um objeto **TableDef** para determinar quais objetos **Index** estarão disponíveis para objetos **Recordset** do tipo tabela criados a partir do objeto **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="c9dfe-113">Examine the **Indexes** collection of a **TableDef** object to determine what **Index** objects are available to table-type **Recordset** objects created from that **TableDef** object.</span></span>

<span data-ttu-id="c9dfe-114">Gere um novo índice da tabela pela criação de um novo objeto **Index**, pela definição de suas propriedades, pelo acréscimo à coleção **Indexes** do objeto base **TableDef** e depois pela reabertura do objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="c9dfe-114">You can create a new index for the table by creating a new **Index** object, setting its properties, appending it to the **Indexes** collection of the underlying **TableDef** object, and then reopening the **Recordset** object.</span></span>

<span data-ttu-id="c9dfe-115">Os registros retornados de um objeto **Recordset** do tipo tabela podem ser ordenados somente pelos índices definidos para o objeto base **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="c9dfe-115">Records returned from a table-type **Recordset** object can be ordered only by the indexes defined for the underlying **TableDef** object.</span></span> <span data-ttu-id="c9dfe-116">Para classificar registros em alguma outra ordem, você pode abrir um dynaset, instantâneo ou objeto **Recordset** do tipo somente encaminhamento, usando uma instrução SQL com uma cláusula ORDER BY.</span><span class="sxs-lookup"><span data-stu-id="c9dfe-116">To sort records in some other order, you can open a dynaset–, snapshot–, or forward–only–type **Recordset** object by using an SQL statement with an ORDER BY clause.</span></span>


> [!NOTE]
> - <span data-ttu-id="c9dfe-p104">Não é necessário criar índices para tabelas. Em tabelas grandes e não indexadas, o acesso a um registro específico ou a criação do objeto **Recordset** podem demorar muito. Por outro lado, a criação excessiva de índices diminui a velocidade das operações de atualização, acréscimo e exclusão porque todos os índices são atualizados automaticamente.</span><span class="sxs-lookup"><span data-stu-id="c9dfe-p104">You don't have to create indexes for tables. With large, unindexed tables, accessing a specific record or creating a **Recordset** object can take a long time. On the other hand, creating too many indexes slows down update, append, and delete operations because all indexes are automatically updated.</span></span>
> - <span data-ttu-id="c9dfe-120">Os registros lidos de tabelas sem índices não são retornados em uma sequência específica.</span><span class="sxs-lookup"><span data-stu-id="c9dfe-120">Records read from tables without indexes are returned in no particular sequence.</span></span>
> - <span data-ttu-id="c9dfe-121">A propriedade **[Attributes](field-attributes-property-dao.md)** de cada objeto **[Field](field-object-dao.md)** no objeto **Index** determina a ordem dos registros e, como consequência, determina as técnicas de acesso para o uso desse índice.</span><span class="sxs-lookup"><span data-stu-id="c9dfe-121">The **[Attributes](field-attributes-property-dao.md)** property of each **[Field](field-object-dao.md)** object in the **Index** object determines the order of records and consequently determines the access techniques to use for that index.</span></span>
> - <span data-ttu-id="c9dfe-122">Um índice exclusivo ajuda a otimizar a localização de registros.</span><span class="sxs-lookup"><span data-stu-id="c9dfe-122">A unique index helps optimize finding records.</span></span>
> - <span data-ttu-id="c9dfe-123">Índices não afetam a ordem física de uma tabela base, afetam índices apenas como os registros são acessados pelo objeto **Recordset** tipo tabela quando um índice específico é escolhido ou quando o **Recordset** é aberto.</span><span class="sxs-lookup"><span data-stu-id="c9dfe-123">Indexes don't affect the physical order of a base table, indexes affect only how the records are accessed by the table-type **Recordset** object when a particular index is chosen or when **Recordset** is opened.</span></span>


## <a name="example"></a><span data-ttu-id="c9dfe-124">Exemplo</span><span class="sxs-lookup"><span data-stu-id="c9dfe-124">Example</span></span>

<span data-ttu-id="c9dfe-125">Este exemplo usa a propriedade **Index** para definir as ordens de registro diferentes para um **Recordset** do tipo tabela.</span><span class="sxs-lookup"><span data-stu-id="c9dfe-125">This example uses the **Index** property to set different record orders for a table-type **Recordset**.</span></span>

```vb
    Sub IndexPropertyX() 
     
       Dim dbsNorthwind As Database 
       Dim tdfEmployees As TableDef 
       Dim rstEmployees As Recordset 
       Dim idxLoop As Index 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstEmployees = _ 
          dbsNorthwind.OpenRecordset("Employees") 
       Set tdfEmployees = dbsNorthwind.TableDefs!Employees 
     
       With rstEmployees 
     
          ' Enumerate Indexes collection of Employees table. 
          For Each idxLoop In tdfEmployees.Indexes 
             .Index = idxLoop.Name 
             Debug.Print "Index = " & .Index 
             Debug.Print "  EmployeeID - PostalCode - Name" 
             .MoveFirst 
     
             ' Enumerate Recordset to show the order of records. 
             Do While Not .EOF 
                Debug.Print "    " & !EmployeeID & " - " & _ 
                   !PostalCode & " - " & !FirstName & " " & _ 
                   !LastName 
                .MoveNext 
             Loop 
     
          Next idxLoop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="c9dfe-126">Este exemplo demonstra o método **Seek** ao permitir que o usuário procure um produto com base em um número de ID.</span><span class="sxs-lookup"><span data-stu-id="c9dfe-126">This example demonstrates the **Seek** method by allowing the user to search for a product based on an ID number.</span></span>

```vb
    Sub SeekX() 
     
       Dim dbsNorthwind As Database 
       Dim rstProducts As Recordset 
       Dim intFirst As Integer 
       Dim intLast As Integer 
       Dim strMessage As String 
       Dim strSeek As String 
       Dim varBookmark As Variant 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       ' You must open a table-type Recordset to use an index,  
       ' and hence the Seek method. 
       Set rstProducts = _ 
          dbsNorthwind.OpenRecordset("Products", dbOpenTable) 
     
       With rstProducts 
          ' Set the index. 
          .Index = "PrimaryKey" 
     
          ' Get the lowest and highest product IDs. 
          .MoveLast 
          intLast = !ProductID 
          .MoveFirst 
          intFirst = !ProductID 
     
          Do While True 
             ' Display current record information and ask user  
             ' for ID number. 
             strMessage = "Product ID: " & !ProductID & vbCr & _ 
                "Name: " & !ProductName & vbCr & vbCr & _ 
                "Enter a product ID between " & intFirst & _ 
                " and " & intLast & "." 
             strSeek = InputBox(strMessage) 
     
             If strSeek = "" Then Exit Do 
     
             ' Store current bookmark in case the Seek fails. 
             varBookmark = .Bookmark 
     
             .Seek "=", Val(strSeek) 
     
             ' Return to the current record if the Seek fails. 
             If .NoMatch Then 
                MsgBox "ID not found!" 
                .Bookmark = varBookmark 
             End If 
          Loop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="c9dfe-127">O exemplo a seguir mostra como usar o método Seek para localizar um registro em uma tabela vinculada.</span><span class="sxs-lookup"><span data-stu-id="c9dfe-127">The following example shows how to use the Seek method to find a record in a linked table.</span></span>

<span data-ttu-id="c9dfe-128">**Código de exemplo fornecido pela** [referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="c9dfe-128">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Sub TestSeek()
        ' Get the path to the external database that contains
        ' the tblCustomers table we're going to search.
        Dim strMyExternalDatabase
        Dim dbs    As DAO.Database
        Dim dbsExt As DAO.Database
        Dim rst    As DAO.Recordset
        Dim tdf    As DAO.TableDef
        
        Set dbs = CurrentDb()
        Set tdf = dbs.TableDefs("tblCustomers")
        strMyExternalDatabase = Mid(tdf.Connect, 11)
        
        'Open the database that contains the table that is linked
        Set dbsExt = OpenDatabase(strMyExternalDatabase)
        
        'Open a table-type recordset against the external table
        Set rst = dbsExt.OpenRecordset("tblCustomers", dbOpenTable)
        
        'Specify which index to search on
        rst.Index = "PrimaryKey"
        
        'Specify the criteria
        rst.Seek "=", 123
        
        'Check the result
        If rst.NoMatch Then
            MsgBox "Record not found."
        Else
            MsgBox "Customer name: " & rst!CustName
        End If
        
        rst.Close
        dbs.Close
        dbsExt.Close
        Set rst = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
        
        
    End Sub
```
