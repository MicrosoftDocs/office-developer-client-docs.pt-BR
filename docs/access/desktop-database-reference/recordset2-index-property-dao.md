---
title: Propriedade Recordset2.Index (DAO)
TOCTitle: Index Property
ms:assetid: 614bdf53-aca3-25ef-a23c-50095b345d20
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194872(v=office.15)
ms:contentKeyID: 48545209
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 05a29ff9dbe720fe7c5539639b20e0abdc3c587b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716765"
---
# <a name="recordset2index-property-dao"></a>Propriedade Recordset2.Index (DAO)

**Aplica-se a**: Access 2013, o Office 2013

Define ou retorna um valor que indica o nome do objeto **[Index](index-object-dao.md)** atual em um objeto **[Recordset](recordset-object-dao.md)** do tipo tabela (somente nos espaços de trabalho do Microsoft Access).

## <a name="syntax"></a>Sintaxe

*expressão* . Índice

*expressão* Uma variável que representa um objeto **Recordset2** .

## <a name="remarks"></a>Comentários

Os registros nas tabelas base não estão armazenados em uma ordem específica. A definição da propriedade **Index** altera a ordem dos registros retornada do banco de dados. Não afeta a ordem na qual os registros são armazenados.

O objeto **Index** especificado já deve estar definido. Se você definir a propriedade **Index** como um objeto **Index** que não existe ou se a propriedade **Index** não estiver definida quando você usar o método **[Seek](recordset2-seek-method-dao.md)**, ocorrerá um erro interceptável.

Examine a coleção **Indexes** de um objeto **TableDef** para determinar quais objetos **Index** estarão disponíveis para objetos **Recordset** do tipo tabela criados a partir do objeto **TableDef**.

Gere um novo índice da tabela pela criação de um novo objeto **Index**, pela definição de suas propriedades, pelo acréscimo à coleção **Indexes** do objeto base **TableDef** e depois pela reabertura do objeto **Recordset**.

Os registros retornados de um objeto **Recordset** do tipo tabela podem ser ordenados somente pelos índices definidos para o objeto base **TableDef**. Para classificar registros em alguma outra ordem, você pode abrir um dynaset, instantâneo ou objeto **Recordset** do tipo somente encaminhamento, usando uma instrução SQL com uma cláusula ORDER BY.

> [!NOTE]
> - Não é necessário criar índices para tabelas. Em tabelas grandes e não indexadas, o acesso a um registro específico ou a criação do objeto **Recordset** podem demorar muito. Por outro lado, a criação excessiva de índices diminui a velocidade das operações de atualização, acréscimo e exclusão porque todos os índices são atualizados automaticamente.
> - Os registros lidos de tabelas sem índices não são retornados em uma sequência específica.
> - A propriedade **[Attributes](field-attributes-property-dao.md)** de cada objeto **[Field](field-object-dao.md)** no objeto **Index** determina a ordem dos registros e, como consequência, determina as técnicas de acesso para o uso desse índice.
> - Um índice exclusivo ajuda a otimizar a localização de registros.
> - Os índices não têm influência na ordem física de um tableindexes base. Afetarão somente a forma como os registros serão acessados pelo objeto **Recordset** do tipo tabela quando um índice específico for escolhido ou quando o **Recordset** for aberto.

## <a name="example"></a>Exemplo

Este exemplo usa a propriedade **Index** para definir as ordens de registro diferentes para um **Recordset** do tipo tabela.

```vb
    Sub IndexPropertyX() 
     
       Dim dbsNorthwind As Database 
       Dim tdfEmployees As TableDef 
       Dim rstEmployees As Recordset2 
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

Este exemplo demonstra o método **Seek** permitindo que o usuário procure um produto com base em um número de identificação.

```vb
    Sub SeekX() 
     
       Dim dbsNorthwind As Database 
       Dim rstProducts As Recordset2 
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
