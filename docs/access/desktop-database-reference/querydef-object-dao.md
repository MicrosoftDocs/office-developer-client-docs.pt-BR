---
title: Objeto QueryDef (DAO)
TOCTitle: QueryDef Object
ms:assetid: 0b3d901c-345d-42a2-f5f1-fb09cc562e27
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845129(v=office.15)
ms:contentKeyID: 48543169
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 18889846b2f55fa13f9fa5fe002f233c955d9866
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929948"
---
# <a name="querydef-object-dao"></a>Objeto QueryDef (DAO)

**Aplica-se a:** Access 2013 | Office 2013 

Um objeto **QueryDef** é uma definição armazenada de uma consulta em um banco de dados do mecanismo de banco de dados do Microsoft Access ou uma definição temporária de uma consulta em um espaço de trabalho ODBCDirect.

## <a name="remarks"></a>Comentários

É possível usar o objeto **QueryDef** para definir uma consulta. Por exemplo, você pode:

- Usar a propriedade **SQL** para definir ou retornar a definição da consulta.

- Usar a coleção **Parameters** do objeto **QueryDef** para definir ou retornar parâmetros de consulta.

- Usar a propriedade **Type** para retornar um valor que indique se a consulta seleciona ou não registros em uma tabela existente, cria uma nova tabela, insere registros de uma tabela na outra, exclui registros ou atualiza registros.

- Usar a propriedade **MaxRecords** para limitar o número de registros retornados de uma consulta.

- Usar a propriedade **ODBCTimeout** para indicar o tempo de espera antes de a consulta retornar os registros. A propriedade **ODBCTimeout** se aplica a qualquer consulta que acesse dados ODBC.

- Usar a propriedade **ReturnsRecords** para indicar que a consulta retorna registros. A propriedade **ReturnsRecords** é válida somente nas consultas passagem SQL.

- Usar a propriedade **Connect** para fazer uma consulta passagem SQL para um banco de dados ODBC.

Você também pode criar objetos **QueryDef** temporários. Diferente dos objetos **QueryDef** permanentes, os objetos **QueryDef** temporários não são salvos no disco nem acrescentados à coleção **QueryDefs**. Os objetos **QueryDef** temporários são úteis para consultas que você deve executar várias vezes durante o tempo de execução, mas não precisa salvar em disco, particularmente se você criar as instruções SQL durante o tempo de execução.

Você pode pensar em um objeto **QueryDef** permanente em um espaço de trabalho do Microsoft Access como uma instrução SQL compilada. Se você executar uma consulta a partir de um objeto **QueryDef** permanente, a consulta será executada de forma mais rápida do que se você executar uma instrução SQL equivalente a partir do método **OpenRecordset**. Isso porque o mecanismo de banco de dados do Microsoft Access não precisa compilar a consulta antes de executá-la.

A forma preferida de usar o dialeto SQL nativo de um mecanismo de banco de dados externo acessado pelo mecanismo de banco de dados do Microsoft Access é por meio dos objetos **QueryDef**. Por exemplo, você pode criar uma consulta do Microsoft SQL Server e armazená-la em um objeto **QueryDef**. Quando você precisar usar uma consulta SQL de um mecanismo de banco de dados que são seja do Microsoft Access, forneça uma sequência de propriedade **Connect** que aponte para a fonte de dados externa. As consultas com propriedades **Connect** válidas ignoram o mecanismo de banco de dados do Microsoft Access e transmitem a consulta diretamente para o servidor de banco de dados externo para processamento.

Para criar um novo objeto **QueryDef**, use o método **CreateQueryDef**. Em um espaço de trabalho do Microsoft Access, se você fornecer uma cadeia de caracteres para o argumento nome ou se você definir explicitamente a propriedade **Name** do novo objeto **QueryDef** em uma cadeia de comprimento não – zero, você criará um **QueryDef** permanente que será automaticamente ser acrescentado à coleção **QueryDefs** e salvo no disco. Fornecendo uma cadeia de caracteres de comprimento zero como o argumento nome ou explicitamente definir a propriedade **Name** como uma cadeia de caracteres de comprimento zero resultará em um objeto **QueryDef** temporário.

Para referir-se a um objeto **QueryDef** de uma coleção pelo número ordinal ou pela configuração da propriedade **Name**, use qualquer uma das formas de sintaxe a seguir:

QueryDefs(0)

QueryDefs("name")

QueryDefs\! \[ nome\]

Você pode se referir a objetos **QueryDef** temporários somente pelas variáveis de objeto que foram atribuídas a eles.

**Link fornecidos pela** comunidade [UtterAccess](https://www.utteraccess.com) . UtterAccess é o fórum principal de wiki e a Ajuda do Microsoft Access.

- [Consultas: Documento SQL para o Word](https://www.utteraccess.com/wiki/index.php/queries:_document_sql_to_word)

## <a name="example"></a>Exemplo

Este exemplo cria um novo objeto **QueryDef** e o acrescenta à coleção **QueryDefs** do objeto **Database** Northwind. Em seguida, ele enumera a coleção **QueryDefs** e a coleção **Properties** do novo **QueryDef**.

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

Este exemplo usa o método **CreateQueryDef** para criar e executar um **QueryDef** temporário e um permanente. A função GetrstTemp é exigida para a execução deste procedimento.

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

O exemplo a seguir mostra como substituir a instrução Structured Query Language (SQL) em uma consulta salva.

**Código de exemplo fornecido pela** [referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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

