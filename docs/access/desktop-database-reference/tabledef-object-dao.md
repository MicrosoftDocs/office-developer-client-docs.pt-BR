---
title: Objeto TableDef (DAO)
TOCTitle: TableDef Object
ms:assetid: 715146b6-c62a-abff-28ee-e6bbe3c08adf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195790(v=office.15)
ms:contentKeyID: 48545582
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ef0a7c167321a45249fb022e0987a5f8d6364ea0
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462001"
---
# <a name="tabledef-object-dao"></a>Objeto TableDef (DAO)

**Aplica-se a**: Access 2013 | Office 2013

Um objeto **TableDef** representa a definição armazenada de uma tabela base ou de uma tabela vinculada (apenas espaços de trabalho do Microsoft Access).

## <a name="remarks"></a>Comentários

Você manipula uma definição de tabela utilizando um objeto **TableDef** e seus métodos e suas propriedades. Por exemplo, você pode:

- Examinar o campo e a estrutura de índice de qualquer tabela local, vinculada ou externa em um banco de dados.

- Usar as propriedades **Connect** e **SourceTableName** para definir ou retornar informações sobre tabelas vinculadas e usar o método **RefreshLink** para atualizar conexões com as tabelas vinculadas.

- Usar as propriedades **ValidationRule** e **ValidationText** para definir ou retornar condições de validação.

- Use o método **OpenRecordset** para criar uma tabela –, dynaset, dinâmico, instantâneo ou objeto de **Recordset** do tipo somente encaminhamento, com base na definição da tabela.

Para tabelas base, a propriedade **RecordCount** contém o número de registros na tabela de banco de dados especificada. Para tabelas vinculadas, a configuração da propriedade **RecordCount** é sempre – 1.

Para criar um novo objeto **TableDef**, use o método **[CreateTableDef](database-createtabledef-method-dao.md)**.

### <a name="to-add-a-field-to-a-table"></a>Para adicionar um campo a uma tabela

1.  Certifique-se de que quaisquer objetos **[Recordset](recordset-object-dao.md)** baseados na tabela estejam fechados.

2.  Use o método **CreateField** para criar uma variável de objeto **Field** e definir suas propriedades.

3.  Use o método **Append** para adicionar o objeto **Field** à coleção **Fields** do objeto **TableDef**.

Você pode excluir um objeto **Field** de uma coleção **TableDefs** se ele não tiver nenhum índice atribuído a ele, mas os dados do campo não serão perdidos.

### <a name="to-create-a-table-that-is-ready-for-new-records-in-a-database"></a>Para criar uma tabela que esteja pronta para novos registros em um banco de dados

1.  Use o método **CreateTableDef** para criar um objeto **TableDef**.

2.  Defina suas propriedades.

3.  Para cada campo na tabela, use o método **CreateField** para criar uma variável de objeto **Field** e definir suas propriedades.

4.  Use o método **Append** para adicionar campos à coleção **Fields** do objeto **TableDef**.

5.  Use o método **Append** para adicionar o novo objeto **TableDef** à coleção **TableDefs** do objeto **Database**.

Uma tabela vinculada é conectada ao banco de dados pelas propriedades **SourceTableName** e **Connect** do objeto **TableDef**.

### <a name="to-link-a-table-to-a-database"></a>Para vincular uma tabela a um banco de dados

1.  Use o método **CreateTableDef** para criar um objeto **TableDef**.

2.  Defina suas propriedades **Connect** e **SourceTableName** (e, como opção, sua propriedade **Attributes**).

3.  Use o método **Append** para adicioná-lo à coleção **TableDefs** de um **Database**.

Para referir-se a um objeto **TableDef** de uma coleção pelo número ordinal ou pela configuração da propriedade **Name**, use qualquer uma das formas de sintaxe a seguir:

**TableDefs** (0)

**TableDefs** ("nome")

**TableDefs**\!\[nome\]

## <a name="example"></a>Exemplo

Este exemplo cria um novo objeto **TableDef** e o acrescenta à coleção **TableDefs** do objeto Database Northwind. Em seguida, enumeram-se as coleções **TableDefs** e **Properties** do novo **TableDef**.

```vb
    Sub TableDefX() 
     
       Dim dbsNorthwind As Database 
       Dim tdfNew As TableDef 
       Dim tdfLoop As TableDef 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       ' Create new TableDef object, append Field objects  
       ' to its Fields collection, and append TableDef  
       ' object to the TableDefs collection of the  
       ' Database object. 
       Set tdfNew = dbsNorthwind.CreateTableDef("NewTableDef") 
       tdfNew.Fields.Append tdfNew.CreateField("Date", dbDate) 
       dbsNorthwind.TableDefs.Append tdfNew 
     
       With dbsNorthwind 
          Debug.Print .TableDefs.Count & _ 
             " TableDefs in " & .Name 
     
          ' Enumerate TableDefs collection. 
          For Each tdfLoop In .TableDefs 
             Debug.Print "  " & tdfLoop.Name 
          Next tdfLoop 
     
          With tdfNew 
             Debug.Print "Properties of " & .Name 
     
             ' Enumerate Properties collection of new 
             ' TableDef object, only printing properties 
             ' with non-empty values. 
             For Each prpLoop In .Properties 
                Debug.Print "  " & prpLoop.Name & " - " & _ 
                   IIf(prpLoop = "", "[empty]", prpLoop) 
             Next prpLoop 
     
          End With 
     
          ' Delete new TableDef since this is a  
          ' demonstration. 
          .TableDefs.Delete tdfNew.Name 
          .Close 
       End With 
     
    End Sub 
```

<br/>

Este exemplo cria um novo objeto **TableDef** no banco de dados Northwind.

```vb 
Sub CreateTableDefX() 
 
   Dim dbsNorthwind As Database 
   Dim tdfNew As TableDef 
   Dim prpLoop As Property 
 
   Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
   ' Create a new TableDef object. 
   Set tdfNew = dbsNorthwind.CreateTableDef("Contacts") 
 
   With tdfNew 
      ' Create fields and append them to the new TableDef  
      ' object. This must be done before appending the  
      ' TableDef object to the TableDefs collection of the  
      ' Northwind database. 
      .Fields.Append .CreateField("FirstName", dbText) 
      .Fields.Append .CreateField("LastName", dbText) 
      .Fields.Append .CreateField("Phone", dbText) 
      .Fields.Append .CreateField("Notes", dbMemo) 
 
      Debug.Print "Properties of new TableDef object " & _ 
         "before appending to collection:" 
 
      ' Enumerate Properties collection of new TableDef  
      ' object. 
      For Each prpLoop In .Properties 
         On Error Resume Next 
         If prpLoop <> "" Then Debug.Print "  " & _ 
           prpLoop.Name & " = " & prpLoop 
         On Error GoTo 0 
      Next prpLoop 
 
      ' Append the new TableDef object to the Northwind  
      ' database. 
      dbsNorthwind.TableDefs.Append tdfNew 
 
      Debug.Print "Properties of new TableDef object " & _ 
         "after appending to collection:" 
 
      ' Enumerate Properties collection of new TableDef  
      ' object. 
      For Each prpLoop In .Properties 
         On Error Resume Next 
         If prpLoop <> "" Then Debug.Print "  " & _ 
           prpLoop.Name & " = " & prpLoop 
         On Error GoTo 0 
      Next prpLoop 
 
   End With 
 
   ' Delete new TableDef object since this is a  
   ' demonstration. 
   dbsNorthwind.TableDefs.Delete "Contacts" 
 
   dbsNorthwind.Close 
```

<br/>

O exemplo a seguir mostra como criar um campo calculado. O método CreateField cria um campo denominado **FullName**. A propriedade de expressão, em seguida, é definida como a expressão que calcula o valor do campo.

**Código de exemplo fornecido pela** [referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    Sub CreateCalculatedField()
        Dim dbs As DAO.Database
        Dim tdf As DAO.TableDef
        Dim fld As DAO.Field2
        
        ' get the database
        Set dbs = CurrentDb()
        
        ' create the table
        Set tdf = dbs.CreateTableDef("tblContactsCalcField")
        
        ' create the fields: first name, last name
        tdf.Fields.Append tdf.CreateField("FirstName", dbText, 20)
        tdf.Fields.Append tdf.CreateField("LastName", dbText, 20)
        
        ' create the calculated field: full name
        Set fld = tdf.CreateField("FullName", dbText, 50)
        fld.Expression = "[FirstName] & "" "" & [LastName]"
        tdf.Fields.Append fld
        
        ' append the table and cleanup
        dbs.TableDefs.Append tdf
        
    Cleanup:
        Set fld = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
    End Sub
```
