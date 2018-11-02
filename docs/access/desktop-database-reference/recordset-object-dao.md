---
title: Objeto Recordset (DAO)
TOCTitle: Recordset Object
ms:assetid: 9774232c-e6da-175b-fc7f-ed2ab7908fa0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197799(v=office.15)
ms:contentKeyID: 48546469
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a4ce9b3480cfa2a8eb074065016131e2c82752c3
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921123"
---
# <a name="recordset-object-dao"></a>Objeto Recordset (DAO)

**Aplica-se a**: Access 2013, o Office 2013

Um objeto **Recordset** representa os registros em uma tabela base ou os registros resultantes da execução de uma consulta.

## <a name="remarks"></a>Comentários

Os objetos **Recordset** são usados para manipular dados em um banco de dados no nível do registro. Ao usar objetos de acesso a dados, manipula-se dados quase completamente usando os objetos **Recordset**. Todos os objetos **Recordset** são criados com registros (linhas) e campos (colunas). Há cinco tipos de objetos **Recordset**:

- Recordset do tipo Tabela  representação em código de uma tabela base que pode ser usada para adicionar, alterar ou excluir registros de uma única tabela de banco de dados (somente espaços de trabalho do Microsoft Access).

- Recordset do tipo Dynaset  o resultado de uma consulta que pode ter registros atualizáveis. Um objeto **Recordset** do tipo dynaset é um Recordset dinâmico que pode ser usado para adicionar, alterar ou excluir registros de uma tabela ou de tabelas de banco de dados subjacentes. Um objeto **Recordset** do tipo dynaset pode conter campos de uma ou mais tabelas em um banco de dados. Esse tipo corresponde a um cursor de conjunto de chaves ODBC.

- Recordset do tipo Instantâneo  uma cópia estática de um Recordset que pode ser usada para localizar dados ou gerar relatórios. Um objeto **Recordset** do tipo instantâneo pode conter campos de uma ou mais tabelas em um banco de dados, mas não pode ser atualizado. Esse tipo corresponde a um cursor estático ODBC.

- Recordset do tipo Somente Encaminhamento  idêntico a um instantâneo, exceto pelo fato de não fornecer cursor. Você pode simplesmente rolar para frente por meio dos registros. Isso melhora o desempenho em situações em que é preciso fazer uma única passagem por um conjunto de resultados. Esse tipo corresponde a um cursor somente encaminhamento ODBC.

- Recordset do tipo Dynamic  um conjunto de resultados de consulta de uma ou mais tabelas base nas quais você pode adicionar, alterar ou excluir registros de uma consulta de retorno de linha. Além disso, registros adicionados, alterados e editados por outros usuários nas tabelas base também aparecem no seu **Recordset**. Esse tipo corresponde a um cursor dinâmico ODBC (somente espaços de trabalho ODBCDirect).

> [!NOTE]
> [!OBSERVAçãO] O Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect. Use ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.

Você pode escolher o tipo de objeto **Recordset** que você deseja criar usando o argumento type do método **OpenRecordset** .

Em um espaço de trabalho do Microsoft Access, se você não especificar um tipo de tentativas DAO para criar o tipo de **Recordset** com a maior funcionalidade disponível, iniciando com a tabela. Se esse tipo não estiver disponível, o DAO tentará um dynaset, um instantâneo e, finalmente, um objeto **Recordset** de tipo somente encaminhamento.

Em um espaço de trabalho do ODBCDirect, se você não especificar um tipo de DAO tenta criar o tipo de **Recordset** com a resposta mais rápida de consulta, começando com somente de encaminhamento. Se esse tipo não estiver disponível, o DAO tentará um instantâneo, um dynaset e, finalmente, um objeto **Recordset** do tipo Dynamic.

Ao criar um objeto **Recordset** usando um objeto **[TableDef](tabledef-object-dao.md)** não vinculado em um espaço de trabalho do Microsoft Access, objetos **Recordset** do tipo tabela serão criados. Somente objetos **Recordset** do tipo dynaset ou instantâneo podem ser criados com uma tabela ou tabelas vinculadas ao mecanismo de conexão do banco de dados ODBC ao banco de dados do Microsoft Access.

Um novo objeto **Recordset** é automaticamente adicionado à coleção **Recordsets** quando o objeto é aberto, e é automaticamente removido quando este é fechado.

> [!NOTE]
> [!OBSERVAçãO] Se você usar variáveis para representar um objeto **Recordset** e um objeto **Database** contendo um **Recordset**, verifique se as variáveis têm o mesmo escopo, ou tempo de vida. Por exemplo, se você declarar uma variável pública que representa um objeto **Recordset**, certifique-se de que a variável que representa o **Database** que contém o **Recordset** também é pública, ou declarada em um procedimento **Sub** ou **Function** usando a palavra-chave **Static**.

Você pode criar quantas variáveis de objeto **Recordset** precisar. Diferentes objetos **Recordset** podem acessar as mesmas tabelas, consultas e campos sem entrar em conflito.

Dynaset, instantâneo e objetos **Recordset** do tipo somente encaminhamento são armazenados na memória local. Se não houver espaço suficiente na memória local para armazenar os dados, o mecanismo de banco de dados do Microsoft Access salvará os dados adicionais no espaço de disco Temporário. Se esse espaço estiver esgotado, ocorrerá um erro interceptável.

A coleção padrão de um objeto **Recordset** é a coleção **Fields**, e a propriedade padrão de um objeto **[Field](field-object-dao.md)** é a propriedade **[Value](field-value-property-dao.md)**. Use os valores padrão para simplificar seu código.

Ao criar um objeto **Recordset**, o registro atual é posicionado no primeiro registro, se houver algum registro. Se não houver registros, a configuração da propriedade **RecordCount** será 0 e as configurações das propriedades **BOF** e **EOF** serão **True**.

É possível usar os métodos **MoveNext**, **MovePrevious**, **MoveFirst** e **MoveLast** para reposicionar o registro atual. objetos **Recordset** oferecem suporte somente para o método **MoveNext**. Ao usar o método Move para visitar cada registro (ou "percorrer" o **Recordset**), é possível usar as propriedades **BOF** e **EOF** para consultar o começo ou o fim de um objeto **Recordset**.

Com os objetos **Recordset** do tipo dynaset e instantâneo em um espaço de trabalho do Microsoft Access, é possível usar os métodos Find, como **FindFirst**, para localizar um registro específico com base em um critério. Se o registro não for localizado, a propriedade **NoMatch** é definida como **True**. Para objetos **Recordset** do tipo tabela, é possível examinar os registros usando o método **Seek**.

A propriedade **Type** indica o tipo de objeto **Recordset** criado, e a propriedade **Updatable** indica se os registros do objeto podem ser alterados.

As informações sobre a estrutura de uma tabela base, como os nomes e tipos de dados de cada objeto **Field** e quaisquer objetos **Index**, estão armazenadas em um objeto **TableDef**.

Para consultar um objeto **Recordset** em uma coleção de acordo com seu número ordinal ou sua configuração de propriedade **Name**, use qualquer um dos formulários de sintaxe a seguir:

- **Recordsets**(0)

- **Conjuntos de registros** ("nome")

- **Conjuntos de registros**\!\[nome\]

> [!NOTE]
> [!OBSERVAçãO] É possível abrir um objeto **Recordset** a partir do mesmo banco de dados ou fonte de dados mais de uma vez criando nomes duplicados na coleção **Recordsets**. Você deve atribuir objetos **Recordsets** para variáveis de objetos e referenciá-los por nome de variável.

## <a name="example"></a>Exemplo

This example demonstrates **Recordset** objects and the **Recordsets** collection by opening four different types of **Recordsets**, enumerating the Recordsets collection of the current **Database**, and enumerating the **Properties** collection of each **Recordset**.

```vb
    Sub RecordsetX() 
     
       Dim dbsNorthwind As Database 
       Dim rstTable As Recordset 
       Dim rstDynaset As Recordset 
       Dim rstSnapshot As Recordset 
       Dim rstForwardOnly As Recordset 
       Dim rstLoop As Recordset 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       With dbsNorthwind 
     
          ' Open one of each type of Recordset object. 
          Set rstTable = .OpenRecordset("Categories", _ 
             dbOpenTable) 
          Set rstDynaset = .OpenRecordset("Employees", _ 
             dbOpenDynaset) 
          Set rstSnapshot = .OpenRecordset("Shippers", _ 
             dbOpenSnapshot) 
          Set rstForwardOnly = .OpenRecordset _  
             ("Employees", dbOpenForwardOnly) 
     
          Debug.Print "Recordsets in Recordsets " & _ 
             "collection of dbsNorthwind" 
     
          ' Enumerate Recordsets collection. 
          For Each rstLoop In .Recordsets 
     
             With rstLoop 
                Debug.Print "  " & .Name 
     
                ' Enumerate Properties collection of each 
                ' Recordset object. Trap for any  
                ' properties whose values are invalid in  
                ' this context. 
                For Each prpLoop In .Properties 
                   On Error Resume Next 
                   If prpLoop <> "" Then Debug.Print _ 
                      "    " & prpLoop.Name & _ 
                      " = " & prpLoop 
                   On Error GoTo 0 
                Next prpLoop 
     
             End With 
     
          Next rstLoop 
     
          rstTable.Close 
          rstDynaset.Close 
          rstSnapshot.Close 
          rstForwardOnly.Close 
     
          .Close 
       End With 
     
    End Sub 
```

<br/>

Esse exemplo usa o método **OpenRecordset** para abrir cinco diferentes tipos de objetos **Recordset** e exibir seus conteúdos. O procedimento OpenRecordsetOutput é necessário para executar esse procedimento.

```vb
    Sub OpenRecordsetX() 
     
       Dim wrkAcc As Workspace 
       Dim wrkODBC As Workspace 
       Dim dbsNorthwind As Database 
       Dim conPubs As Connection 
       Dim rstTemp As Recordset 
       Dim rstTemp2 As Recordset 
     
       ' Open Microsoft Access and ODBCDirect workspaces, Microsoft  
       ' Access database, and ODBCDirect connection. 
       Set wrkAcc = CreateWorkspace("", "admin", "", dbUseJet) 
       Set wrkODBC = CreateWorkspace("", "admin", "", dbUseODBC) 
       Set dbsNorthwind = wrkAcc.OpenDatabase("Northwind.mdb") 
        
       ' Note: The DSN referenced below must be set to  
       '       use Microsoft Windows NT Authentication Mode to  
       '       authorize user access to the Microsoft SQL Server. 
       Set conPubs = wrkODBC.OpenConnection("", , , _ 
          "ODBC;DATABASE=pubs;DSN=Publishers") 
     
       ' Open five different Recordset objects and display the  
       ' contents of each. 
     
       Debug.Print "Opening forward-only-type recordset " & _ 
          "where the source is a QueryDef object..." 
       Set rstTemp = dbsNorthwind.OpenRecordset( _ 
          "Ten Most Expensive Products", dbOpenForwardOnly) 
       OpenRecordsetOutput rstTemp 
     
       Debug.Print "Opening read-only dynaset-type " & _ 
          "recordset where the source is an SQL statement..." 
       Set rstTemp = dbsNorthwind.OpenRecordset( _ 
          "SELECT * FROM Employees", dbOpenDynaset, dbReadOnly) 
       OpenRecordsetOutput rstTemp 
     
       ' Use the Filter property to retrieve only certain  
       ' records with the next OpenRecordset call. 
       Debug.Print "Opening recordset from existing " & _ 
          "Recordset object to filter records..." 
       rstTemp.Filter = "LastName >= 'M'" 
       Set rstTemp2 = rstTemp.OpenRecordset() 
       OpenRecordsetOutput rstTemp2 
     
       Debug.Print "Opening dynamic-type recordset from " & _ 
          "an ODBC connection..." 
       Set rstTemp = conPubs.OpenRecordset( _ 
          "SELECT * FROM stores", dbOpenDynamic) 
       OpenRecordsetOutput rstTemp 
     
       ' Use the StillExecuting property to determine when the  
       ' Recordset is ready for manipulation. 
       Debug.Print "Opening snapshot-type recordset based " & _ 
          "on asynchronous query to ODBC connection..." 
       Set rstTemp = conPubs.OpenRecordset("publishers", _ 
          dbOpenSnapshot, dbRunAsync) 
       Do While rstTemp.StillExecuting 
          Debug.Print "  [still executing...]" 
       Loop 
       OpenRecordsetOutput rstTemp 
     
       rstTemp.Close 
       dbsNorthwind.Close 
       conPubs.Close 
       wrkAcc.Close 
       wrkODBC.Close 
     
    End Sub 
     
    Sub OpenRecordsetOutput(rstOutput As Recordset) 
     
       ' Enumerate the specified Recordset object. 
       With rstOutput 
          Do While Not .EOF 
             Debug.Print , .Fields(0), .Fields(1) 
             .MoveNext 
          Loop 
       End With 
     
    End Sub 
```

<br/>

Este exemplo abre um objeto **Recordset** do tipo dynamic e enumera seus registros.

```vb
    Sub dbOpenDynamicX() 
     
       Dim wrkMain As Workspace 
       Dim conMain As Connection 
       Dim qdfTemp As QueryDef 
       Dim rstTemp As Recordset 
       Dim strSQL As String 
       Dim intLoop As Integer 
     
       ' Create ODBC workspace and open connection to 
       ' SQL Server database. 
       Set wrkMain = CreateWorkspace("ODBCWorkspace", _ 
          "admin", "", dbUseODBC) 
           
       ' Note: The DSN referenced below must be configured to  
       '       use Microsoft Windows NT Authentication Mode to  
       '       authorize user access to the Microsoft SQL Server.     
       Set conMain = wrkMain.OpenConnection("Publishers", _ 
          dbDriverNoPrompt, False, _ 
          "ODBC;DATABASE=pubs;DSN=Publishers") 
           
       ' Open dynamic-type recordset. 
       Set rstTemp = _ 
          conMain.OpenRecordset("authors", _ 
          dbOpenDynamic) 
     
       With rstTemp 
          Debug.Print "Dynamic-type recordset: " & .Name 
     
          ' Enumerate records. 
          Do While Not .EOF 
             Debug.Print "    " & !au_lname & ", " & _ 
                !au_fname 
             .MoveNext 
          Loop 
     
          .Close 
       End With 
     
       conMain.Close 
       wrkMain.Close 
     
    End Sub 
```

<br/>

Este exemplo abre um objeto **Recordset** do tipo dynaset e mostra a extensão para a qual seus campos são atualizáveis.

```vb
    Sub dbOpenDynasetX() 
     
       Dim dbsNorthwind As Database 
       Dim rstInvoices As Recordset 
       Dim fldLoop As Field 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstInvoices = _ 
          dbsNorthwind.OpenRecordset("Invoices", dbOpenDynaset) 
     
       With rstInvoices 
          Debug.Print "Dynaset-type recordset: " & .Name 
     
          If .Updatable Then 
             Debug.Print "  Updatable fields:" 
     
             ' Enumerate Fields collection of dynaset-type 
             ' Recordset object, print only updatable 
             ' fields. 
             For Each fldLoop In .Fields 
                If fldLoop.DataUpdatable Then 
                   Debug.Print "    " & fldLoop.Name 
                End If 
             Next fldLoop 
     
          End If 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

Este exemplo abre um objeto **Recordset** do tipo somente encaminhamento, demonstra suas características somente leitura e percorre o **Recordset** com o método **MoveNext**.

```vb 
Sub dbOpenForwardOnlyX() 
 
   Dim dbsNorthwind As Database 
   Dim rstEmployees As Recordset 
   Dim fldLoop As Field 
 
   Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
   ' Open a forward-only-type Recordset object. Only the  
   ' MoveNext and Move methods may be used to navigate  
   ' through the recordset. 
   Set rstEmployees = _ 
      dbsNorthwind.OpenRecordset("Employees", _ 
      dbOpenForwardOnly) 
 
   With rstEmployees 
      Debug.Print "Forward-only-type recordset: " & _ 
         .Name & ", Updatable = " & .Updatable 
 
      Debug.Print "  Field - DataUpdatable" 
      ' Enumerate Fields collection, printing the Name and  
      ' DataUpdatable properties of each Field object. 
      For Each fldLoop In .Fields 
         Debug.Print "    " & _ 
            fldLoop.Name & " - " & fldLoop.DataUpdatable 
      Next fldLoop 
 
      Debug.Print "  Data" 
      ' Enumerate the recordset. 
      Do While Not .EOF 
         Debug.Print "    " & !FirstName & " " & _ 
            !LastName 
         .MoveNext 
      Loop 
 
      .Close 
   End With 
 
   dbsNorthwind.Close 
 
End Sub 
```

<br/>

Este exemplo abre um objeto **Recordset** do tipo instantâneo e demonstra suas características somente leitura.

```vb
    Sub dbOpenSnapshotX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstEmployees = _ 
          dbsNorthwind.OpenRecordset("Employees", _ 
          dbOpenSnapshot) 
     
       With rstEmployees 
          Debug.Print "Snapshot-type recordset: " & _ 
             .Name 
     
          ' Enumerate the Properties collection of the 
          ' snapshot-type Recordset object, trapping for 
          ' any properties whose values are invalid in  
          ' this context. 
          For Each prpLoop In .Properties 
             On Error Resume Next 
             Debug.Print "  " & _ 
                prpLoop.Name & " = " & prpLoop 
             On Error Goto 0 
          Next prpLoop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

Este exemplo abre um objeto **Recordset**, define sua propriedade **Index** e enumera seus registros.

```vb
    Sub dbOpenTableX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       ' dbOpenTable is default. 
       Set rstEmployees = _ 
          dbsNorthwind.OpenRecordset("Employees") 
     
       With rstEmployees 
          Debug.Print "Table-type recordset: " & .Name 
     
          ' Use predefined index. 
          .Index = "LastName" 
          Debug.Print "  Index = " & .Index 
     
          ' Enumerate records. 
          Do While Not .EOF 
             Debug.Print "    " & !LastName & ", " & _ 
                !FirstName 
             .MoveNext 
          Loop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

O exemplo a seguir mostra como usar o método Seek para localizar um registro em uma tabela vinculada.

**Código de exemplo fornecido pela** [referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).


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

<br/>

O exemplo a seguir mostra como abrir um Recordset baseado em uma consulta de parâmetro.

```vb
    Dim dbs As DAO.Database
    Dim qdf As DAO.QueryDef
    Dim rst As DAO.Recordset
    
    Set dbs = CurrentDb
    
    'Get the parameter query
    Set qfd = dbs.QueryDefs("qryMyParameterQuery")
    
    'Supply the parameter value
    qdf.Parameters("EnterStartDate") = Date
    qdf.Parameters("EnterEndDate") = Date + 7
    
    'Open a Recordset based on the parameter query
    Set rst = qdf.OpenRecordset()
```

<br/>

O exemplo a seguir mostra como abrir um Recordset baseado em uma tabela ou uma consulta.

```vb
    Dim dbs As DAO.Database
    Dim rsTable As DAO.Recordset
    Dim rsQuery As DAO.Recordset
    
    Set dbs = CurrentDb
    
    'Open a table-type Recordset
    Set rsTable = dbs.OpenRecordset("Table1", dbOpenTable)
    
    'Open a dynaset-type Recordset using a saved query
    Set rsQuery = dbs.OpenRecordset("qryMyQuery", dbOpenDynaset)
```

<br/>

O exemplo a seguir mostra como abrir um Recordset baseado em uma instrução SQL (Structured Query Language).

```vb
    Dim dbs As DAO.Database
    Dim rsSQL As DAO.Recordset
    Dim strSQL As String
    
    Set dbs = CurrentDb
    
    'Open a snapshot-type Recordset based on an SQL statement
    strSQL = "SELECT * FROM Table1 WHERE Field2 = 33"
    Set rsSQL = dbs.OpenRecordset(strSQL, dbOpenSnapshot)
```

<br/>

O exemplo a seguir mostra como usar os métodos FindFirst e FindNext para localizar um registro em um Recordset.

```vb
    Sub FindOrgName()
    
        Dim dbs As DAO.Database
        Dim rst As DAO.Recordset
        
        'Get the database and Recordset
        Set dbs = CurrentDb
        Set rst = dbs.OpenRecordset("tblCustomers")
    
        'Search for the first matching record   
        rst.FindFirst "[OrgName] LIKE '*parts*'"
        
        'Check the result
        If rst.NoMatch Then
            MsgBox "Record not found."
            GotTo Cleanup
        Else
            Do While Not rst.NoMatch
                MsgBox "Customer name: " & rst!CustName
                rst.FindNext "[OrgName] LIKE '*parts*'"
            Loop
    
            'Search for the next matching record
            rst.FindNext "[OrgName] LIKE '*parts*'"
        End If
       
        Cleanup:
            rst.Close
            Set rst = Nothing
            Set dbs = Nothing
    
    End Sub
```

<br/>

O exemplo a seguir mostra como copiar os resultados de uma consulta para uma planilha em uma nova pasta de trabalho do Microsoft Excel.

```vb
    Public Sub CopyDataFromQuery( _
        xlApp As Excel.Application, _
        strQueryName As String)
    
        ' If the xlApp object exists
        If Not xlApp Is Nothing Then
        
            ' If the Workbook exists
            If xlApp.Workbooks.Count = 1 Then
            
                ' Create Recrodset Object from the Query
                Dim rsQuery As DAO.Recordset
                Set rsQuery = Application.CurrentDb.OpenRecordset(strQueryName)
                
                ' Get the Cells object
                Dim Cells As Object
                Set Cells = xlApp.Workbooks(1).ActiveSheet.Cells
                
                ' Copy the Data from the Query into the Sheet
                Cells.CopyFromRecordset rsQuery
                
            End If
        End If
    
    End Sub
```

