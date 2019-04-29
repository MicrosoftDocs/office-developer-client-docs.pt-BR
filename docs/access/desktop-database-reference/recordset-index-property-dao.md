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
localization_priority: Priority
ms.openlocfilehash: f475635424cfb9ed8ddab4025d6a944bdedd39fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300522"
---
# <a name="recordsetindex-property-dao"></a>Propriedade Recordset.Index (DAO)

**Aplica-se a:** Access 2013, Office 2013

Define ou retorna um valor que indica o nome do objeto **[Index](index-object-dao.md)** atual em um objeto **[Recordset](recordset-object-dao.md)** do tipo tabela (somente em espaços de trabalho do Microsoft Access).

## <a name="syntax"></a>Sintaxe

*expression* .Index

*expression* Uma variável que representa um objeto **Recordset**.

## <a name="remarks"></a>Comentários

Os registros nas tabelas base não estão armazenados em uma ordem específica. A definição da propriedade **Index** altera a ordem dos registros retornada do banco de dados. Não afeta a ordem na qual os registros são armazenados.

O objeto **Index** especificado já deve estar definido. Se você definir a propriedade **Index** como um objeto **Index** que não existe ou se a propriedade **Index** não estiver definida quando você usar o método **[Seek](recordset-seek-method-dao.md)**, ocorrerá um erro interceptável.

Examine a coleção **Indexes** de um objeto **TableDef** para determinar quais objetos **Index** estarão disponíveis para objetos **Recordset** do tipo tabela criados a partir do objeto **TableDef**.

Gere um novo índice da tabela pela criação de um novo objeto **Index**, pela definição de suas propriedades, pelo acréscimo à coleção **Indexes** do objeto base **TableDef** e depois pela reabertura do objeto **Recordset**.

Os registros retornados de um objeto **Recordset** do tipo tabela podem ser ordenados somente pelos índices definidos para o objeto base **TableDef**. Para classificar os registros na mesma ordem, abra um objeto **Recordset** do tipo dynaset, instantâneo ou somente encaminhamento por meio da instrução SQL com uma cláusula ORDER BY.


> [!NOTE]
> - Não é necessário criar índices para tabelas. Em tabelas grandes e não indexadas, o acesso a um registro específico ou a criação do objeto **Recordset** podem demorar muito. Por outro lado, a criação excessiva de índices diminui a velocidade das operações de atualização, acréscimo e exclusão porque todos os índices são atualizados automaticamente.
> - Os registros lidos de tabelas sem índices não são retornados em uma sequência específica.
> - A propriedade **[Attributes](field-attributes-property-dao.md)** de cada objeto **[Field](field-object-dao.md)** no objeto **Index** determina a ordem dos registros e, como consequência, determina as técnicas de acesso para o uso desse índice.
> - Um índice exclusivo ajuda a otimizar a localização de registros.
> - Os índices não têm influência na ordem física de uma tabela base. Os índices só afetarão a forma como os registros serão acessados pelo objeto **Recordset** do tipo tabela quando um índice específico for escolhido ou quando o **Recordset** for aberto.


## <a name="example"></a>Exemplo

Este exemplo usa a propriedade **Index** para definir pedidos de registros diferentes para um **Recordset** do tipo tabela.

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

Este exemplo demonstra o método **Seek** ao permitir que o usuário procure um produto com base em um número de ID.

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

O exemplo a seguir mostra como usar o método Seek para localizar um registro em uma tabela vinculada.

**Código de exemplo fornecido por:** a [Referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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
