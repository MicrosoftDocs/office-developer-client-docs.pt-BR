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
# <a name="querydefsql-property-dao"></a>Propriedade QueryDef.SQL (DAO)

**Aplica-se a**: Access 2013, o Office 2013

Define ou retorna a instrução SQL que define a consulta executada por um objeto **[QueryDef](querydef-object-dao.md)**.

## <a name="syntax"></a>Sintaxe

*expressão* . SQL

*expressão* Uma variável que representa um objeto **QueryDef** .

## <a name="remarks"></a>Comentários

A propriedade **SQL** contém a instrução SQL que determina quantos registros serão selecionados, agrupados e ordenados quando você executar a consulta. Use a consulta para selecionar os registros que serão incluídos em um objeto **[Recordset](recordset-object-dao.md)**. Também é possível definir as consultas ação para modificar dados sem retornar registros.

A sintaxe SQL usada em uma consulta deve estar de acordo com o dialeto SQL do mecanismo de consulta, determinado pelo tipo de espaço de trabalho. Em um espaço de trabalho do Microsoft Access , use o dialeto do Microsoft Access SQL, a não ser que você crie uma consulta de passagem SQL. Nesse caso, você deverá usar o dialeto do servidor. Em um espaço de trabalho do ODBCDirect, use o dialeto SQL do servidor.

Se a instrução SQL incluir os parâmetros da consulta, defina-os antes da execução. Até que você reinicie os parâmetros, os mesmos valores de parâmetro serão aplicados toda vez que a consulta for executada.

Em um espaço de trabalho do Microsoft Access, o uso de um objeto **QueryDef** é a forma preferencial de executar as operações passagem SQL no mecanismo do banco de dados do Microsoft Access conectado às fontes de dados ODBC. Definindo a propriedade **[Connect](querydef-connect-property-dao.md)** do objeto de **QueryDef** para uma fonte de dados ODBC, você pode usar o SQL não – – – database do Microsoft Access na consulta a serem passados para o servidor externo. Por exemplo, use as instruções TRANSACT SQL (com os bancos de dados do Microsoft SQL Server ou do Sybase SQL Server), que o mecanismo do banco de dados do Microsoft Access poderia, de outra forma, não processar.

> [!NOTE]
> Se você definir a propriedade como uma cadeia de caracteres concatenada com um valor não inteiro e os parâmetros do sistema especificarem um caractere decimal de fora dos EUA, como uma vírgula (por exemplo, strSQL = "preço &gt; " &amp; lngPrice e lngPrice = 125,50), ocorrerá um erro quando você Tente executar o objeto **QueryDef** em um banco de dados do mecanismo de banco de dados do Microsoft Access. Isso acontecerá porque durante a concatenação, o número será convertido em uma sequência que usa o caractere decimal padrão do sistema e o Microsoft Access SQL aceita somente os caracteres decimais do padrão dos EUA.

## <a name="example"></a>Exemplo

Este exemplo demonstra a propriedade **SQL** pela definição e alteração da propriedade **SQL** de um **QueryDef** temporário e comparação dos resultados. A função SQLOutput é necessária para esse procedimento ser executado.

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

Este exemplo usa o método **CopyQueryDef** para criar uma cópia de um **QueryDef** a partir de um **Recordset** existente e modifica a cópia adicionando uma cláusula à propriedade **SQL**. Quando você criar um **QueryDef** permanente, os espaços, os ponto-e-vírgulas ou as alimentações de linha podem ser adicionados à propriedade **SQL**; esses caracteres adicionais devem ser suprimidos antes que qualquer nova cláusula possa ser acrescentada à instrução SQL.

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

Este exemplo usa os métodos **CreateQueryDef** e **OpenRecordset** e a propriedade **SQL** para fazer uma consulta à tabela de títulos no banco de dados Pubs de amostra do Microsoft SQL Server e retornar o título e o identificador de título do livro com maior volume de vendas. O exemplo, em seguida, faz uma consulta à tabela de autores e instrui o usuário a enviar um cheque-bônus para cada autor com base em sua participação (o bônus total é de $1.000 e cada autor deve receber um percentual dessa quantia).

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

O exemplo a seguir mostra como criar uma consulta parâmetro. Uma consulta denominada **' MyQuery '** é criada com dois parâmetros, denominados Param1 e Param2. Para fazer isso, a propriedade SQL da consulta é definida como uma instrução Structured Query Language (SQL) que define os parâmetros.

**Código de exemplo fornecido pela** [referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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

O exemplo a seguir mostra como substituir a instrução Structured Query Language (SQL) em uma consulta salva.

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
