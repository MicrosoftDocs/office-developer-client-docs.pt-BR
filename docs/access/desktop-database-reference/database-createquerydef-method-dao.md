---
title: Método Database.CreateQueryDef (DAO)
TOCTitle: CreateQueryDef Method
ms:assetid: 75ee7cac-dcd0-b4c5-b55b-9cbaaae2cbf0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195966(v=office.15)
ms:contentKeyID: 48545686
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7e6a6fe546f862f2452ac992c140a63959e48a6b
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919742"
---
# <a name="databasecreatequerydef-method-dao"></a><span data-ttu-id="906ad-102">Método Database.CreateQueryDef (DAO)</span><span class="sxs-lookup"><span data-stu-id="906ad-102">Database.CreateQueryDef method (DAO)</span></span>

<span data-ttu-id="906ad-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="906ad-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="906ad-104">Cria um novo objeto **[QueryDef](querydef-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="906ad-104">Creates a new **[QueryDef](querydef-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="906ad-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="906ad-105">Syntax</span></span>

<span data-ttu-id="906ad-106">*expressão* . CreateQueryDef (***Name***, ***SQLText***)</span><span class="sxs-lookup"><span data-stu-id="906ad-106">*expression* .CreateQueryDef(***Name***, ***SQLText***)</span></span>

<span data-ttu-id="906ad-107">*expressão* Uma variável que representa um objeto de **banco de dados** .</span><span class="sxs-lookup"><span data-stu-id="906ad-107">*expression* A variable that represents a **Database** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="906ad-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="906ad-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="906ad-109">Nome</span><span class="sxs-lookup"><span data-stu-id="906ad-109">Name</span></span></p></th>
<th><p><span data-ttu-id="906ad-110">Obrigatório/Opcional</span><span class="sxs-lookup"><span data-stu-id="906ad-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="906ad-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="906ad-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="906ad-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="906ad-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="906ad-113">Name</span><span class="sxs-lookup"><span data-stu-id="906ad-113">Name</span></span></p></td>
<td><p><span data-ttu-id="906ad-114">Opcional</span><span class="sxs-lookup"><span data-stu-id="906ad-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="906ad-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="906ad-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="906ad-116">Um <strong>Variant</strong> (subtipo <strong>String</strong>) que denomina exclusivamente o novo <strong>QueryDef</strong>.</span><span class="sxs-lookup"><span data-stu-id="906ad-116">A <strong>Variant</strong> (<strong>String</strong> subtype) that uniquely names the new <strong>QueryDef</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="906ad-117">SQLText</span><span class="sxs-lookup"><span data-stu-id="906ad-117">SQLText</span></span></p></td>
<td><p><span data-ttu-id="906ad-118">Opcional</span><span class="sxs-lookup"><span data-stu-id="906ad-118">Optional</span></span></p></td>
<td><p><span data-ttu-id="906ad-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="906ad-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="906ad-p101">Um <strong>Variant</strong> (subtipo <strong>String</strong>) que é uma instrução SQL definindo o <strong>QueryDef</strong>. Se você omitir esse argumento, será possível definir o <strong>QueryDef</strong> configurando sua propriedade <strong><a href="querydef-sql-property-dao.md">SQL</a></strong> antes ou depois de acrescentá-lo a uma coleção.</span><span class="sxs-lookup"><span data-stu-id="906ad-p101">A <strong>Variant</strong> (<strong>String</strong> subtype) that is an SQL statement defining the <strong>QueryDef</strong>. If you omit this argument, you can define the <strong>QueryDef</strong> by setting its <strong><a href="querydef-sql-property-dao.md">SQL</a></strong> property before or after you append it to a collection.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="906ad-122">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="906ad-122">Return value</span></span>

<span data-ttu-id="906ad-123">QueryDef</span><span class="sxs-lookup"><span data-stu-id="906ad-123">QueryDef</span></span>

## <a name="remarks"></a><span data-ttu-id="906ad-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="906ad-124">Remarks</span></span>

<span data-ttu-id="906ad-125">Em um espaço de trabalho do Microsoft Access, se você fornecer algo diferente de uma cadeia de caracteres de comprimento zero para o nome ao criar um **QueryDef**, o objeto **QueryDef** resultante será automaticamente acrescentado à coleção **[QueryDefs](querydefs-collection-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="906ad-125">In a Microsoft Access workspace, if you provide anything other than a zero-length string for the name when you create a **QueryDef**, the resulting **QueryDef** object is automatically appended to the **[QueryDefs](querydefs-collection-dao.md)** collection.</span></span>

<span data-ttu-id="906ad-126">Se o objeto especificado pelo nome, já é um membro da coleção **QueryDefs** , ocorrerá um erro de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="906ad-126">If the object specified by name is already a member of the **QueryDefs** collection, a run-time error occurs.</span></span> <span data-ttu-id="906ad-127">Você pode criar um temporário **QueryDef** usando uma cadeia de caracteres de comprimento zero para o argumento nome quando você executar o método **CreateQueryDef** .</span><span class="sxs-lookup"><span data-stu-id="906ad-127">You can create a temporary **QueryDef** by using a zero-length string for the name argument when you execute the **CreateQueryDef** method.</span></span> <span data-ttu-id="906ad-128">Também é possível realizar isso configurando a propriedade **[Name](querydef-name-property-dao.md)** de um **QueryDef** recém-criado como uma cadeia de caracteres de comprimento zero ("").</span><span class="sxs-lookup"><span data-stu-id="906ad-128">You can also accomplish this by setting the **[Name](querydef-name-property-dao.md)** property of a newly created **QueryDef** to a zero-length string ("").</span></span> 

<span data-ttu-id="906ad-129">Objetos **QueryDef** temporários são úteis se você desejar usar repetidamente instruções SQL dinâmicas sem ter de criar novos objetos permanentes na coleção **QueryDefs**.</span><span class="sxs-lookup"><span data-stu-id="906ad-129">Temporary **QueryDef** objects are useful if you want to repeatedly use dynamic SQL statements without having to create any new permanent objects in the **QueryDefs** collection.</span></span> <span data-ttu-id="906ad-130">Não é possível acrescentar um **QueryDef** temporário a qualquer coleção porque uma cadeia de caracteres de comprimento zero não é um nome válido para um objeto **QueryDef** permanente.</span><span class="sxs-lookup"><span data-stu-id="906ad-130">You can't append a temporary **QueryDef** to any collection because a zero-length string isn't a valid name for a permanent **QueryDef** object.</span></span> <span data-ttu-id="906ad-131">Sempre é possível definir as propriedades **Name** e **SQL** do objeto **QueryDef** recém-criado e subsequentemente acrescentar o **QueryDef** à coleção **QueryDefs**.</span><span class="sxs-lookup"><span data-stu-id="906ad-131">You can always set the **Name** and **SQL** properties of the newly created **QueryDef** object and subsequently append the **QueryDef** to the **QueryDefs** collection.</span></span>

<span data-ttu-id="906ad-132">Para executar a instrução SQL em um objeto **QueryDef**, use o método **[Execute](querydef-execute-method-dao.md)** ou **[OpenRecordset](database-openrecordset-method-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="906ad-132">To run the SQL statement in a **QueryDef** object, use the **[Execute](querydef-execute-method-dao.md)** or **[OpenRecordset](database-openrecordset-method-dao.md)** method.</span></span>

<span data-ttu-id="906ad-133">Usar um objeto **QueryDef** é a maneira preferencial de executar consultas passagem SQL com bancos de dados ODBC.</span><span class="sxs-lookup"><span data-stu-id="906ad-133">Using a **QueryDef** object is the preferred way to perform SQL pass-through queries with ODBC databases.</span></span>

<span data-ttu-id="906ad-134">Para remover um objeto **QueryDef** de uma coleção **QueryDefs** em um banco de dados de mecanismo de banco de dados Microsoft Access, use o método **[Delete](querydefs-delete-method-dao.md)** na coleção.</span><span class="sxs-lookup"><span data-stu-id="906ad-134">To remove a **QueryDef** object from a **QueryDefs** collection in a Microsoft Access database engine database, use the **[Delete](querydefs-delete-method-dao.md)** method on the collection.</span></span>

## <a name="example"></a><span data-ttu-id="906ad-135">Exemplo</span><span class="sxs-lookup"><span data-stu-id="906ad-135">Example</span></span>

<span data-ttu-id="906ad-p104">Este exemplo usa o método **CreateQueryDef** para criar e executar um **QueryDef** temporário e um permanente. A função GetrstTemp é exigida para a execução deste procedimento.</span><span class="sxs-lookup"><span data-stu-id="906ad-p104">This example uses the **CreateQueryDef** method to create and execute both a temporary and a permanent **QueryDef**. The GetrstTemp function is required for this procedure to run.</span></span>

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

<span data-ttu-id="906ad-p105">Este exemplo usa os métodos **CreateQueryDef** e **OpenRecordset** e a propriedade **SQL** para fazer uma consulta à tabela de títulos no banco de dados Pubs de amostra do Microsoft SQL Server e retornar o título e o identificador de título do livro com maior volume de vendas. O exemplo, em seguida, faz uma consulta à tabela de autores e instrui o usuário a enviar um cheque-bônus para cada autor com base em sua participação (o bônus total é de $1.000 e cada autor deve receber um percentual dessa quantia).</span><span class="sxs-lookup"><span data-stu-id="906ad-p105">This example uses the **CreateQueryDef** and **OpenRecordset** methods and the **SQL** property to query the table of titles in the Microsoft SQL Server sample database Pubs and return the title and title identifier of the best-selling book. The example then queries the table of authors and instructs the user to send a bonus check to each author based on his or her royalty share (the total bonus is $1,000 and each author should receive a percentage of that amount).</span></span>

```vb 
Sub ClientServerX2() 
 
   Dim dbsCurrent As Database 
   Dim qdfBestSellers As QueryDef 
   Dim qdfBonusEarners As QueryDef 
   Dim rstTopSeller As Recordset 
   Dim rstBonusRecipients As Recordset 
   Dim strAuthorList As String 
 
   ' Open a database from which QueryDef objects can be  
   ' created. 
   Set dbsCurrent = OpenDatabase("DB1.mdb") 
 
   ' Create a temporary QueryDef object to retrieve 
   ' data from a Microsoft SQL Server database. 
   Set qdfBestSellers = dbsCurrent.CreateQueryDef("") 
   With qdfBestSellers 
      ' Note: The DSN referenced below must be configured to  
      '       use Microsoft Windows NT Authentication Mode to  
      '       authorize user access to the Microsoft SQL Server. 
      .Connect = "ODBC;DATABASE=pubs;DSN=Publishers" 
      .SQL = "SELECT title, title_id FROM titles " & _ 
         "ORDER BY ytd_sales DESC" 
      Set rstTopSeller = .OpenRecordset() 
      rstTopSeller.MoveFirst 
   End With 
 
   ' Create a temporary QueryDef to retrieve data from 
   ' a Microsoft SQL Server database based on the results from 
   ' the first query. 
   Set qdfBonusEarners = dbsCurrent.CreateQueryDef("") 
   With qdfBonusEarners 
      ' Note: The DSN referenced below must be configured to  
      '       use Microsoft Windows NT Authentication Mode to  
      '       authorize user access to the Microsoft SQL Server. 
      .Connect = "ODBC;DATABASE=pubs;DSN=Publishers" 
      .SQL = "SELECT * FROM titleauthor " & _ 
         "WHERE title_id = '" & _ 
         rstTopSeller!title_id & "'" 
      Set rstBonusRecipients = .OpenRecordset() 
   End With 
 
   ' Build the output string. 
   With rstBonusRecipients 
      Do While Not .EOF 
         strAuthorList = strAuthorList & "  " & _ 
            !au_id & ":  $" & (10 * !royaltyper) & vbCr 
         .MoveNext 
      Loop 
   End With 
 
   ' Display results. 
   MsgBox "Please send a check to the following " & _ 
      "authors in the amounts shown:" & vbCr & _ 
      strAuthorList & "for outstanding sales of " & _ 
      rstTopSeller!Title & "." 
 
   rstTopSeller.Close 
   dbsCurrent.Close 
 
End Sub 
```

<br/>

<span data-ttu-id="906ad-140">O exemplo a seguir mostra como criar uma consulta parâmetro.</span><span class="sxs-lookup"><span data-stu-id="906ad-140">The following example shows how to create a parameter query.</span></span> <span data-ttu-id="906ad-141">Uma consulta denominada **' MyQuery '** é criada com dois parâmetros, denominados Param1 e Param2.</span><span class="sxs-lookup"><span data-stu-id="906ad-141">A query named **myQuery** is created with two parameters, named Param1 and Param2.</span></span> <span data-ttu-id="906ad-142">Para fazer isso, a propriedade SQL da consulta é definida como uma instrução Structured Query Language (SQL) que define os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="906ad-142">To do this, the SQL property of the query is set to a Structured Query Language (SQL) statement that defines the parameters.</span></span>

<span data-ttu-id="906ad-143">**Código de exemplo fornecido pela** [referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="906ad-143">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Sub CreateQueryWithParameters()
    
        Dim dbs As DAO.Database
        Dim qdf As DAO.QueryDef
        Dim strSQL As String
    
        Set dbs = CurrentDb
        Set qdf = dbs.CreateQueryDef("myQuery")
        Application.RefreshDatabaseWindow
    
        strSQL = "PARAMETERS Param1 TEXT, Param2 INT; "
        strSQL = strSQL & "SELECT * FROM [Table1] "
        strSQL = strSQL & "WHERE [Field1] = [Param1] AND [Field2] = [Param2];"
        qdf.SQL = strSQL
    
        qdf.Close
        Set qdf = Nothing
        Set dbs = Nothing
    
    End Sub
```
