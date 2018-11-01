---
title: Propriedade QueryDef.SQL (DAO)
TOCTitle: SQL Property
ms:assetid: 16446789-c8be-bff0-eddd-b5f6a8530128
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845522(v=office.15)
ms:contentKeyID: 48543429
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053054
f1_categories:
- Office.Version=v15
ms.openlocfilehash: a8e33f1a22e1ffd6dffbb67b8bafd5fae78f39c6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881612"
---
# <a name="querydefsql-property-dao"></a><span data-ttu-id="68874-102">Propriedade QueryDef.SQL (DAO)</span><span class="sxs-lookup"><span data-stu-id="68874-102">QueryDef.SQL Property (DAO)</span></span>

<span data-ttu-id="68874-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="68874-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="68874-104">Define ou retorna a instrução SQL que define a consulta executada por um objeto **[QueryDef](querydef-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="68874-104">Sets or returns the SQL statement that defines the query executed by a **[QueryDef](querydef-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="68874-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="68874-105">Syntax</span></span>

<span data-ttu-id="68874-106">*expressão* . SQL</span><span class="sxs-lookup"><span data-stu-id="68874-106">*expression* .SQL</span></span>

<span data-ttu-id="68874-107">*expressão* Uma variável que representa um objeto **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="68874-107">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="68874-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="68874-108">Remarks</span></span>

<span data-ttu-id="68874-p101">A propriedade **SQL** contém a instrução SQL que determina quantos registros serão selecionados, agrupados e ordenados quando você executar a consulta. Use a consulta para selecionar os registros que serão incluídos em um objeto **[Recordset](recordset-object-dao.md)**. Também é possível definir as consultas ação para modificar dados sem retornar registros.</span><span class="sxs-lookup"><span data-stu-id="68874-p101">The **SQL** property contains the SQL statement that determines how records are selected, grouped, and ordered when you execute the query. You can use the query to select records to include in a **[Recordset](recordset-object-dao.md)** object. You can also define action queries to modify data without returning records.</span></span>

<span data-ttu-id="68874-p102">A sintaxe SQL usada em uma consulta deve estar de acordo com o dialeto SQL do mecanismo de consulta, determinado pelo tipo de espaço de trabalho. Em um espaço de trabalho do Microsoft Access , use o dialeto do Microsoft Access SQL, a não ser que você crie uma consulta de passagem SQL. Nesse caso, você deverá usar o dialeto do servidor. Em um espaço de trabalho do ODBCDirect, use o dialeto SQL do servidor.</span><span class="sxs-lookup"><span data-stu-id="68874-p102">The SQL syntax used in a query must conform to the SQL dialect of the query engine, which is determined by the type of workspace. In a Microsoft Access workspace, use the Microsoft Access SQL dialect, unless you create an SQL pass-through query, in which case you should use the dialect of the server.</span></span>

<span data-ttu-id="68874-p103">Se a instrução SQL incluir os parâmetros da consulta, defina-os antes da execução. Até que você reinicie os parâmetros, os mesmos valores de parâmetro serão aplicados toda vez que a consulta for executada.</span><span class="sxs-lookup"><span data-stu-id="68874-p103">If the SQL statement includes parameters for the query, you must set these before execution. Until you reset the parameters, the same parameter values are applied each time you execute the query.</span></span>

<span data-ttu-id="68874-116">Em um espaço de trabalho do Microsoft Access, o uso de um objeto **QueryDef** é a forma preferencial de executar as operações passagem SQL no mecanismo do banco de dados do Microsoft Access conectado às fontes de dados ODBC.</span><span class="sxs-lookup"><span data-stu-id="68874-116">In a Microsoft Access workspace, using a **QueryDef** object is the preferred way to perform SQL pass-through operations on Microsoft Access database engine-connected ODBC data sources.</span></span> <span data-ttu-id="68874-117">Definindo a propriedade **[Connect](querydef-connect-property-dao.md)** do objeto de **QueryDef** para uma fonte de dados ODBC, você pode usar o SQL não – – – database do Microsoft Access na consulta a serem passados para o servidor externo.</span><span class="sxs-lookup"><span data-stu-id="68874-117">By setting the **QueryDef** object's **[Connect](querydef-connect-property-dao.md)** property to an ODBC data source, you can use non–Microsoft–Access–database SQL in the query to be passed to the external server.</span></span> <span data-ttu-id="68874-118">Por exemplo, use as instruções TRANSACT SQL (com os bancos de dados do Microsoft SQL Server ou do Sybase SQL Server), que o mecanismo do banco de dados do Microsoft Access poderia, de outra forma, não processar.</span><span class="sxs-lookup"><span data-stu-id="68874-118">For example, you can use TRANSACT SQL statements (with Microsoft SQL Server or Sybase SQL Server databases), which the Microsoft Access database engine would otherwise not process.</span></span>

> [!NOTE]
> <span data-ttu-id="68874-119">Se você definir a propriedade como uma cadeia de caracteres concatenada com um valor não inteiro e os parâmetros do sistema especificarem um caractere decimal de fora dos EUA, como uma vírgula (por exemplo, strSQL = "preço &gt; " &amp; lngPrice e lngPrice = 125,50), ocorrerá um erro quando você Tente executar o objeto **QueryDef** em um banco de dados do mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="68874-119">If you set the property to a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error will result when you try to execute the **QueryDef** object in a Microsoft Access database engine database.</span></span> <span data-ttu-id="68874-120">Isso acontecerá porque durante a concatenação, o número será convertido em uma sequência que usa o caractere decimal padrão do sistema e o Microsoft Access SQL aceita somente os caracteres decimais do padrão dos EUA.</span><span class="sxs-lookup"><span data-stu-id="68874-120">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>

## <a name="example"></a><span data-ttu-id="68874-121">Exemplo</span><span class="sxs-lookup"><span data-stu-id="68874-121">Example</span></span>

<span data-ttu-id="68874-p106">Este exemplo demonstra a propriedade **SQL** pela definição e alteração da propriedade **SQL** de um **QueryDef** temporário e comparação dos resultados. A função SQLOutput é necessária para esse procedimento ser executado.</span><span class="sxs-lookup"><span data-stu-id="68874-p106">This example demonstrates the **SQL** property by setting and changing the **SQL** property of a temporary **QueryDef** and comparing the results. The SQLOutput function is required for this procedure to run.</span></span>

```vb
    Sub SQLX() 
     
       Dim dbsNorthwind As Database 
       Dim qdfTemp As QueryDef 
       Dim rstEmployees As Recordset 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set qdfTemp = dbsNorthwind.CreateQueryDef("") 
     
       ' Open Recordset using temporary QueryDef object and  
       ' print report. 
       SQLOutput "SELECT * FROM Employees " & _ 
          "WHERE Country = 'USA' " & _ 
          "ORDER BY LastName", qdfTemp 
     
       ' Open Recordset using temporary QueryDef object and  
       ' print report. 
       SQLOutput "SELECT * FROM Employees " & _ 
          "WHERE Country = 'UK' " & _ 
          "ORDER BY LastName", qdfTemp 
     
       dbsNorthwind.Close 
     
    End Sub 
     
    Function SQLOutput(strSQL As String, qdfTemp As QueryDef) 
     
       Dim rstEmployees As Recordset 
     
       ' Set SQL property of temporary QueryDef object and open  
       ' a Recordset. 
       qdfTemp.SQL = strSQL 
       Set rstEmployees = qdfTemp.OpenRecordset 
     
       Debug.Print strSQL 
     
       With rstEmployees 
          ' Enumerate Recordset. 
          Do While Not .EOF 
             Debug.Print "  " & !FirstName & " " & _ 
                !LastName & ", " & !Country 
             .MoveNext 
          Loop 
          .Close 
       End With 
     
    End Function 
```

<br/>

<span data-ttu-id="68874-p107">Este exemplo usa o método **CopyQueryDef** para criar uma cópia de um **QueryDef** a partir de um **Recordset** existente e modifica a cópia adicionando uma cláusula à propriedade **SQL**. Quando você criar um **QueryDef** permanente, os espaços, os ponto-e-vírgulas ou as alimentações de linha podem ser adicionados à propriedade **SQL**; esses caracteres adicionais devem ser suprimidos antes que qualquer nova cláusula possa ser acrescentada à instrução SQL.</span><span class="sxs-lookup"><span data-stu-id="68874-p107">This example uses the **CopyQueryDef** method to create a copy of a **QueryDef** from an existing **Recordset** and modifies the copy by adding a clause to the **SQL** property. When you create a permanent **QueryDef**, spaces, semicolons, or linefeeds may be added to the **SQL** property; these extra characters must be stripped before any new clauses can be attached to the SQL statement.</span></span>

```vb
    Function CopyQueryNew(rstTemp As Recordset, _ 
       strAdd As String) As QueryDef 
     
       Dim strSQL As String 
       Dim strRightSQL As String 
     
       Set CopyQueryNew = rstTemp.CopyQueryDef 
       With CopyQueryNew 
          ' Strip extra characters. 
          strSQL = .SQL 
          strRightSQL = Right(strSQL, 1) 
          Do While strRightSQL = " " Or strRightSQL = ";" Or _ 
                strRightSQL = Chr(10) Or strRightSQL = vbCr 
             strSQL = Left(strSQL, Len(strSQL) - 1) 
             strRightSQL = Right(strSQL, 1) 
          Loop 
          .SQL = strSQL & strAdd 
       End With 
     
    End Function 
     
    This example shows a possible use of CopyQueryNew(). 
     
    Sub CopyQueryDefX() 
     
       Dim dbsNorthwind As Database 
       Dim qdfEmployees As QueryDef 
       Dim rstEmployees As Recordset 
       Dim intCommand As Integer 
       Dim strOrderBy As String 
       Dim qdfCopy As QueryDef 
       Dim rstCopy As Recordset 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set qdfEmployees = dbsNorthwind.CreateQueryDef( _ 
          "NewQueryDef", "SELECT FirstName, LastName, " & _ 
          "BirthDate FROM Employees") 
       Set rstEmployees = qdfEmployees.OpenRecordset( _ 
          dbOpenForwardOnly) 
     
       Do While True 
          intCommand = Val(InputBox( _ 
             "Choose field on which to order a new " & _ 
             "Recordset:" & vbCr & "1 - FirstName" & vbCr & _ 
             "2 - LastName" & vbCr & "3 - BirthDate" & vbCr & _ 
             "[Cancel - exit]")) 
          Select Case intCommand 
             Case 1 
                strOrderBy = " ORDER BY FirstName" 
             Case 2 
                strOrderBy = " ORDER BY LastName" 
             Case 3 
                strOrderBy = " ORDER BY BirthDate" 
             Case Else 
                Exit Do 
          End Select 
          Set qdfCopy = CopyQueryNew(rstEmployees, strOrderBy) 
          Set rstCopy = qdfCopy.OpenRecordset(dbOpenSnapshot, _ 
             dbForwardOnly) 
          With rstCopy 
             Do While Not .EOF 
                Debug.Print !LastName & ", " & !FirstName & _ 
                   " - " & !BirthDate 
                .MoveNext 
             Loop 
             .Close 
          End With 
          Exit Do 
       Loop 
     
       rstEmployees.Close 
       ' Delete new QueryDef because this is a demonstration. 
       dbsNorthwind.QueryDefs.Delete qdfEmployees.Name 
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="68874-p108">Este exemplo usa os métodos **CreateQueryDef** e **OpenRecordset** e a propriedade **SQL** para fazer uma consulta à tabela de títulos no banco de dados Pubs de amostra do Microsoft SQL Server e retornar o título e o identificador de título do livro com maior volume de vendas. O exemplo, em seguida, faz uma consulta à tabela de autores e instrui o usuário a enviar um cheque-bônus para cada autor com base em sua participação (o bônus total é de $1.000 e cada autor deve receber um percentual dessa quantia).</span><span class="sxs-lookup"><span data-stu-id="68874-p108">This example uses the **CreateQueryDef** and **OpenRecordset** methods and the **SQL** property to query the table of titles in the Microsoft SQL Server sample database Pubs and return the title and title identifier of the best-selling book. The example then queries the table of authors and instructs the user to send a bonus check to each author based on his or her royalty share (the total bonus is $1,000 and each author should receive a percentage of that amount).</span></span>

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

<span data-ttu-id="68874-128">O exemplo a seguir mostra como criar uma consulta parâmetro.</span><span class="sxs-lookup"><span data-stu-id="68874-128">The following example shows how to create a parameter query.</span></span> <span data-ttu-id="68874-129">Uma consulta denominada **' MyQuery '** é criada com dois parâmetros, denominados Param1 e Param2.</span><span class="sxs-lookup"><span data-stu-id="68874-129">A query named **myQuery** is created with two parameters, named Param1 and Param2.</span></span> <span data-ttu-id="68874-130">Para fazer isso, a propriedade SQL da consulta é definida como uma instrução Structured Query Language (SQL) que define os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="68874-130">To do this, the SQL property of the query is set to a Structured Query Language (SQL) statement that defines the parameters.</span></span>

<span data-ttu-id="68874-131">**Código de exemplo fornecido pela** [referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="68874-131">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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

<br/>

<span data-ttu-id="68874-132">O exemplo a seguir mostra como substituir a instrução Structured Query Language (SQL) em uma consulta salva.</span><span class="sxs-lookup"><span data-stu-id="68874-132">The following example shows how to replace the Structured Query Language (SQL) statement in a saved query.</span></span>

```vb
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
