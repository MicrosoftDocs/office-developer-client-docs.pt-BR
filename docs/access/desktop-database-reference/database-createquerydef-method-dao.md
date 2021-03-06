---
title: Método Database.CreateQueryDef (DAO)
TOCTitle: CreateQueryDef Method
ms:assetid: 75ee7cac-dcd0-b4c5-b55b-9cbaaae2cbf0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195966(v=office.15)
ms:contentKeyID: 48545686
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: c19ef8ab8ef2e937ba7467b3695f9aa5780c21c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294978"
---
# <a name="databasecreatequerydef-method-dao"></a>Método Database.CreateQueryDef (DAO)

**Aplica-se ao**: Access 2013, Office 2013

Crie um novo objeto **[QueryDef](querydef-object-dao.md)**.

## <a name="syntax"></a>Sintaxe

*expression* .CreateQueryDef(***Name***, ***SQLText***)

*expressão* Uma variável que representa um objeto **Database**.

## <a name="parameters"></a>Parâmetros

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome</p></th>
<th><p>Necessário/opcional</p></th>
<th><p>Tipo de dados</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Um <strong>Variant</strong> (<strong>String</strong> subtype) que exclusivamente nomeia a nova <strong>QueryDef</strong>.</p></td>
</tr>
<tr class="even">
<td><p><em>SQLText</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Um <strong>Variant</strong> (<strong>String</strong> subtype) que é uma instrução SQL definindo o <strong>QueryDef</strong>. Se você omitir esse argumento, será possível definir o <strong>QueryDef</strong> configurando sua propriedade <strong><a href="querydef-sql-property-dao.md">SQL</a></strong> antes ou depois de acrescentá-lo a uma coleção.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Valor de retorno

QueryDef

## <a name="remarks"></a>Comentários

Em um espaço de trabalho do Microsoft Access, se você fornecer algo diferente de uma cadeia de caracteres de comprimento zero para o nome ao criar um **QueryDef**, o objeto **QueryDef** resultante será automaticamente acrescentado à coleção **[QueryDefs](querydefs-collection-dao.md)**.

Se o objeto especificado por name já for um membro da coleção **QueryDefs**, ocorrerá um erro de tempo de execução. Você pode criar um **QueryDef** temporário usando uma cadeia de caracteres de comprimento zero para o argumento name quando executar o método **CreateQueryDef**. Também é possível realizar isso configurando a propriedade **[Name](querydef-name-property-dao.md)** de um **QueryDef** recém-criado como uma cadeia de caracteres de comprimento zero (""). 

Objetos **QueryDef** temporários são úteis se você desejar usar repetidamente instruções SQL dinâmicas sem ter de criar novos objetos permanentes na coleção **QueryDefs**. Não é possível acrescentar um **QueryDef** temporário a qualquer coleção porque uma cadeia de caracteres de comprimento zero não é um nome válido para um objeto **QueryDef** permanente. Sempre é possível definir as propriedades **Name** e **SQL** do objeto **QueryDef** recém-criado e subsequentemente acrescentar o **QueryDef** à coleção **QueryDefs**.

Para executar a instrução SQL em um objeto **QueryDef**, use o método **[Execute](querydef-execute-method-dao.md)** ou **[OpenRecordset](database-openrecordset-method-dao.md)**.

Usar um objeto **QueryDef** é a maneira preferencial de executar consultas passagem SQL com bancos de dados ODBC.

Para remover um objeto **QueryDef** de uma coleção **QueryDefs** em um banco de dados de mecanismo de banco de dados Microsoft Access, use o método **[Delete](querydefs-delete-method-dao.md)** na coleção.

## <a name="example"></a>Exemplo

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

Este exemplo usa os métodos **CreateQueryDef** e **OpenRecordset** e a propriedade **SQL** para consultar a tabela de títulos no banco de dados de exemplo Pubs do Microsoft SQL Server e retornar o título e o identificador de título do livro mais vendido. Em seguida, o exemplo consulta a tabela de autores e instrui o usuário a enviar um cheque de bonificação para cada autor com base na sua participação nos direitos autorais (o total do prêmio é de $ 1.000 e cada autor receberá uma porcentagem dessa quantia).

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

O exemplo a seguir mostra como criar uma consulta parâmetro. Uma consulta chamada **myQuery** é criada com dois parâmetros, chamados Param1 e Param2. Para fazer isso, a propriedade SQL da consulta está definida como uma declaração de linguagem SQL que define os parâmetros.

**Código de exemplo fornecido por:** a [Referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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
