---
title: Objeto QueryDef (DAO)
TOCTitle: QueryDef Object
ms:assetid: 0b3d901c-345d-42a2-f5f1-fb09cc562e27
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845129(v=office.15)
ms:contentKeyID: 48543169
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: a94d34a2dbe8043e6db637b649f59047cf3f1dda
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301054"
---
# <a name="querydef-object-dao"></a><span data-ttu-id="8b76b-102">Objeto QueryDef (DAO)</span><span class="sxs-lookup"><span data-stu-id="8b76b-102">QueryDef object (DAO)</span></span>

<span data-ttu-id="8b76b-103">**Se aplica a:** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8b76b-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="8b76b-104">Um objeto **QueryDef** é uma definição armazenada de uma consulta em um banco de dados do mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="8b76b-104">A **QueryDef** object is a stored definition of a query in a Microsoft Access database engine database.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b76b-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="8b76b-105">Remarks</span></span>

<span data-ttu-id="8b76b-p101">É possível usar o objeto **QueryDef** para definir uma consulta. Por exemplo, você pode:</span><span class="sxs-lookup"><span data-stu-id="8b76b-p101">You can use the **QueryDef** object to define a query. For example, you can:</span></span>

- <span data-ttu-id="8b76b-108">Usar a propriedade **SQL** para definir ou retornar a definição da consulta.</span><span class="sxs-lookup"><span data-stu-id="8b76b-108">Use the **SQL** property to set or return the query definition.</span></span>

- <span data-ttu-id="8b76b-109">Usar a coleção **Parameters** do objeto **QueryDef** para definir ou retornar parâmetros de consulta.</span><span class="sxs-lookup"><span data-stu-id="8b76b-109">Use the **QueryDef** object's **Parameters** collection to set or return query parameters.</span></span>

- <span data-ttu-id="8b76b-110">Usar a propriedade **Type** para retornar um valor que indique se a consulta seleciona ou não registros em uma tabela existente, cria uma nova tabela, insere registros de uma tabela na outra, exclui registros ou atualiza registros.</span><span class="sxs-lookup"><span data-stu-id="8b76b-110">Use the **Type** property to return a value indicating whether the query selects records from an existing table, makes a new table, inserts records from one table into another table, deletes records, or updates records.</span></span>

- <span data-ttu-id="8b76b-111">Usar a propriedade **MaxRecords** para limitar o número de registros retornados de uma consulta.</span><span class="sxs-lookup"><span data-stu-id="8b76b-111">Use the **MaxRecords** property to limit the number of records returned from a query.</span></span>

- <span data-ttu-id="8b76b-p102">Usar a propriedade **ODBCTimeout** para indicar o tempo de espera antes de a consulta retornar os registros. A propriedade **ODBCTimeout** se aplica a qualquer consulta que acesse dados ODBC.</span><span class="sxs-lookup"><span data-stu-id="8b76b-p102">Use the **ODBCTimeout** property to indicate how long to wait before the query returns records. The **ODBCTimeout** property applies to any query that accesses ODBC data.</span></span>

- <span data-ttu-id="8b76b-p103">Usar a propriedade **ReturnsRecords** para indicar que a consulta retorna registros. A propriedade **ReturnsRecords** é válida somente nas consultas passagem SQL.</span><span class="sxs-lookup"><span data-stu-id="8b76b-p103">Use the **ReturnsRecords** property to indicate that the query returns records. The **ReturnsRecords** property is only valid on SQL pass-through queries.</span></span>

- <span data-ttu-id="8b76b-116">Usar a propriedade **Connect** para fazer uma consulta passagem SQL para um banco de dados ODBC.</span><span class="sxs-lookup"><span data-stu-id="8b76b-116">Use the **Connect** property to make an SQL pass-through query to an ODC database.</span></span>

<span data-ttu-id="8b76b-p104">Você também pode criar objetos **QueryDef** temporários. Diferente dos objetos **QueryDef** permanentes, os objetos **QueryDef** temporários não são salvos no disco nem acrescentados à coleção **QueryDefs**. Os objetos **QueryDef** temporários são úteis para consultas que você deve executar várias vezes durante o tempo de execução, mas não precisa salvar em disco, particularmente se você criar as instruções SQL durante o tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="8b76b-p104">You can also create temporary **QueryDef** objects. Unlike permanent **QueryDef** objects, temporary **QueryDef** objects are not saved to disk or appended to the **QueryDefs** collection. Temporary **QueryDef** objects are useful for queries that you must run repeatedly during run time but do not not need to save to disk, particularly if you create their SQL statements during run time.</span></span>

<span data-ttu-id="8b76b-p105">Você pode pensar em um objeto **QueryDef** permanente em um espaço de trabalho do Microsoft Access como uma instrução SQL compilada. Se você executar uma consulta a partir de um objeto **QueryDef** permanente, a consulta será executada de forma mais rápida do que se você executar uma instrução SQL equivalente a partir do método **OpenRecordset**. Isso porque o mecanismo de banco de dados do Microsoft Access não precisa compilar a consulta antes de executá-la.</span><span class="sxs-lookup"><span data-stu-id="8b76b-p105">You can think of a permanent **QueryDef** object in a Microsoft Access workspace as a compiled SQL statement. If you execute a query from a permanent **QueryDef** object, the query will run faster than if you run the equivalent SQL statement from the **OpenRecordset** method. This is because the Microsoft Access database engine doesn't need to compile the query before executing it.</span></span>

<span data-ttu-id="8b76b-p106">A forma preferida de usar o dialeto SQL nativo de um mecanismo de banco de dados externo acessado pelo mecanismo de banco de dados do Microsoft Access é por meio dos objetos **QueryDef**. Por exemplo, você pode criar uma consulta do Microsoft SQL Server e armazená-la em um objeto **QueryDef**. Quando você precisar usar uma consulta SQL de um mecanismo de banco de dados que são seja do Microsoft Access, forneça uma sequência de propriedade **Connect** que aponte para a fonte de dados externa. As consultas com propriedades **Connect** válidas ignoram o mecanismo de banco de dados do Microsoft Access e transmitem a consulta diretamente para o servidor de banco de dados externo para processamento.</span><span class="sxs-lookup"><span data-stu-id="8b76b-p106">The preferred way to use the native SQL dialect of an external database engine accessed through the Microsoft Access database engine is through **QueryDef** objects. For example, you can create a Microsoft SQL Server query and store it in a **QueryDef** object. When you need to use a non-Microsoft Access database engine SQL query, you must provide a **Connect** property string that points to the external data source. Queries with valid **Connect** properties bypass the Microsoft Access database engine and pass the query directly to the external database server for processing.</span></span>

<span data-ttu-id="8b76b-127">Para criar um novo objeto **QueryDef**, use o método **CreateQueryDef**.</span><span class="sxs-lookup"><span data-stu-id="8b76b-127">To create a new **QueryDef** object, use the **CreateQueryDef** method.</span></span> <span data-ttu-id="8b76b-128">No espaço de trabalho do Microsoft Access, se você fornecer uma cadeia de caracteres para o argumento name ou se você definir explicitamente a propriedade **name** do novo objeto **QueryDef** a uma cadeia de caracteres de comprimento não zero, você criará um **QueryDef** permanente que será acrescentado automaticamente ao conjunto **QueryDefs** e salvo no disco.</span><span class="sxs-lookup"><span data-stu-id="8b76b-128">In a Microsoft Access workspace, if you supply a string for the  name argument or if you explicitly set the **Name** property of the new **QueryDef** object to a non-zero-length string, you will create a permanent **QueryDef** that will automatically be appended to the **QueryDefs** collection and saved to disk.</span></span> <span data-ttu-id="8b76b-129">Fornecer uma cadeia de carateres de comprimento zero, como argumento name ou definir explicitamente a propriedade**name** como uma cadeia de caracteres de comprimento zero resultará em um objeto **QueryDef** temporário.</span><span class="sxs-lookup"><span data-stu-id="8b76b-129">Supplying a zero-length string as the  name argument or explicitly setting the **Name** property to a zero-length string will result in a temporary **QueryDef** object.</span></span>

<span data-ttu-id="8b76b-130">Para fazer referência a um objeto **QueryDef** em uma coleção por seu número ordinal ou por sua configuração de propriedade **Name**, use uma das seguintes formas de sintaxe:</span><span class="sxs-lookup"><span data-stu-id="8b76b-130">To refer to a **QueryDef** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="8b76b-131">QueryDefs(0)</span><span class="sxs-lookup"><span data-stu-id="8b76b-131">QueryDefs(0)</span></span>

<span data-ttu-id="8b76b-132">QueryDefs("name")</span><span class="sxs-lookup"><span data-stu-id="8b76b-132">QueryDefs("name")</span></span>

<span data-ttu-id="8b76b-133">QueryDefs\!\[ name\]</span><span class="sxs-lookup"><span data-stu-id="8b76b-133">QueryDefs\!![ \[name\]]</span></span>

<span data-ttu-id="8b76b-134">Você pode consultar objetos **QueryDef** temporários apenas pelas variáveis de objeto atribuído a eles.</span><span class="sxs-lookup"><span data-stu-id="8b76b-134">You can refer to temporary **QueryDef** objects only by the object variables that you have assigned to them.</span></span>

<span data-ttu-id="8b76b-135">**Link fornecido pela** comunidade [UtterAccess](https://www.utteraccess.com).</span><span class="sxs-lookup"><span data-stu-id="8b76b-135">**Link provided byCommunity Member Icon** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="8b76b-136">UtterAccess é o fórum principal de wiki e de ajuda do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="8b76b-136">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="8b76b-137">Consultas: Documento SQL para Word</span><span class="sxs-lookup"><span data-stu-id="8b76b-137">Queries: Document SQL to Word</span></span>](https://www.utteraccess.com/wiki/index.php/queries:_document_sql_to_word)

## <a name="example"></a><span data-ttu-id="8b76b-138">Exemplo</span><span class="sxs-lookup"><span data-stu-id="8b76b-138">Example</span></span>

<span data-ttu-id="8b76b-p109">Este exemplo cria um novo objeto **QueryDef** e acrescenta-o à coleção **QueryDefs** do objeto **Database** Northwind. Em seguida, são enumeradas a coleção **QueryDefs** e a coleção **Properties** do novo **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="8b76b-p109">This example creates a new **QueryDef** object and appends it to the **QueryDefs** collection of the Northwind **Database** object. It then enumerates the **QueryDefs** collection and the **Properties** collection of the new **QueryDef**.</span></span>

```vb
    Sub QueryDefX() 
     
       Dim dbsNorthwind As Database 
       Dim qdfNew As QueryDef 
       Dim qdfLoop As QueryDef 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       ' Create new QueryDef object. Because it has a  
       ' name, it is automatically appended to the  
       ' QueryDefs collection. 
       Set qdfNew = dbsNorthwind.CreateQueryDef("NewQueryDef", _ 
             "SELECT * FROM Categories") 
     
       With dbsNorthwind 
          Debug.Print .QueryDefs.Count & _ 
             " QueryDefs in " & .Name 
     
          ' Enumerate QueryDefs collection. 
          For Each qdfLoop In .QueryDefs 
             Debug.Print "  " & qdfLoop.Name 
          Next qdfLoop 
     
          With qdfNew 
             Debug.Print "Properties of " & .Name 
     
             ' Enumerate Properties collection of new  
             ' QueryDef object. 
             For Each prpLoop In .Properties 
                On Error Resume Next 
                Debug.Print "  " & prpLoop.Name & " - " & _ 
                   IIf(prpLoop = "", "[empty]", prpLoop) 
                On Error Goto 0 
             Next prpLoop 
          End With 
     
          ' Delete new QueryDef because this is a  
          ' demonstration. 
          .QueryDefs.Delete qdfNew.Name 
          .Close 
       End With 
     
    End Sub 
```

<br/>

<span data-ttu-id="8b76b-p110">Este exemplo usa o método **CreateQueryDef** para criar e executar um **QueryDef** temporário e um permanente. A função GetrstTemp é exigida para a execução deste procedimento.</span><span class="sxs-lookup"><span data-stu-id="8b76b-p110">This example uses the **CreateQueryDef** method to create and execute both a temporary and a permanent **QueryDef**. The GetrstTemp function is required for this procedure to run.</span></span>

```vb
    Sub CreateQueryDefX() 
     
       Dim dbsNorthwind As Database 
       Dim qdfTemp As QueryDef 
       Dim qdfNew As QueryDef 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       With dbsNorthwind 
          ' Create temporary QueryDef. 
          Set qdfTemp = .CreateQueryDef("", _ 
             "SELECT * FROM Employees") 
          ' Open Recordset and print report. 
          GetrstTemp qdfTemp 
          ' Create permanent QueryDef. 
          Set qdfNew = .CreateQueryDef("NewQueryDef", _ 
             "SELECT * FROM Categories") 
          ' Open Recordset and print report. 
          GetrstTemp qdfNew 
          ' Delete new QueryDef because this is a demonstration. 
          .QueryDefs.Delete qdfNew.Name 
          .Close 
       End With 
     
    End Sub 
     
    Function GetrstTemp(qdfTemp As QueryDef) 
     
       Dim rstTemp As Recordset 
     
       With qdfTemp 
          Debug.Print .Name 
          Debug.Print "  " & .SQL 
          ' Open Recordset from QueryDef. 
          Set rstTemp = .OpenRecordset(dbOpenSnapshot) 
     
          With rstTemp 
             ' Populate Recordset and print number of records. 
             .MoveLast 
             Debug.Print "  Number of records = " & _ 
                .RecordCount 
             Debug.Print 
             .Close 
          End With 
     
       End With 
     
    End Function 
```

<br/>

<span data-ttu-id="8b76b-143">O exemplo a seguir mostra como substituir a instrução Structured Query Language (SQL) em uma consulta salva.</span><span class="sxs-lookup"><span data-stu-id="8b76b-143">The following example shows how to replace the Structured Query Language (SQL) statement in a saved query.</span></span>

<span data-ttu-id="8b76b-144">**Código de exemplo fornecido por:** a [Referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="8b76b-144">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    ‘To change the Where clause in a saved query  
    Dim qdf as QueryDef
    Dim db as Database
    Set db = CurrentDB
    Set qdf = db.QueryDefs("YourQueryName")
    qdf.SQL = ReplaceWhereClause(qdf.SQL, strYourNewWhereClause)
    set qdf = Nothing
    set db = Nothing
    
    Public Function ReplaceWhereClause(strSQL As Variant, strNewWHERE As Variant)
    On Error GoTo Error_Handler
    
    ‘This subroutine accepts a valid SQL string and Where clause, and
    ‘returns the same SQL statement with the original Where clause (if any)
    ‘replaced by the passed in Where clause.
    ‘
    ‘INPUT:
    ‘ strSQL valid SQL string to change
    ‘OUTPUT:
    ‘ strNewWHERE New WHERE clause to insert into SQL statement
    ‘
        Dim strSELECT As String, strWhere As String
        Dim strOrderBy As String, strGROUPBY As String, strHAVING As String
    
        Call ParseSQL(strSQL, strSELECT, strWhere, strOrderBy, _
            strGROUPBY, strHAVING)
    
        ReplaceWhereClause = strSELECT &""& strNewWHERE &""_
            & strGROUPBY &""& strHAVING &""& strOrderBy
    
        Exit_Procedure:
            Exit Function
    
        Error_Handler:
            MsgBox (Err.Number & ": " & Err.Description)
            Resume Exit_Procedure
    
    End Function
```

