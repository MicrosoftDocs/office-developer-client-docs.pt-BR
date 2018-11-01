---
title: Objetos de objeto Index - acesso a dados (DAO)
TOCTitle: Index Object
ms:assetid: 92c32cad-ec8a-1243-1d18-83f50b269ecb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197655(v=office.15)
ms:contentKeyID: 48546380
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5d4ed801dfa746af3ad649738e32cec58afe17f6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877076"
---
# <a name="index-object-dao"></a>Objeto Index (DAO)

**Aplica-se a**: Access 2013, o Office 2013

Os objetos **Index** especificam a ordem dos registros acessados a partir de tabelas de banco de dados e se registros duplicados são aceitos, fornecendo acesso eficiente aos dados. Para bancos de dados externos, os objetos **Index** descrevem os índices estabelecidos para tabelas externas (apenas espaços de trabalho do Microsoft Access ).

## <a name="remarks"></a>Comentários

O mecanismo de banco de dados do Microsoft Access usa índices quando ele une tabela e cria objetos **[Recordset](recordset-object-dao.md)**. Os índices determinam a ordem na qual os objetos **Recordset** tipo tabela retornam registros, mas não determinam a ordem na qual o mecanismo de banco de dados do Microsoft Access armazena registros na tabela base nem a ordem na qual qualquer outro tipo de objeto **Recordset** retorna registros.

Com um objeto **Index**, você pode:

- Usar a propriedade **Required** para determinar se os objetos **[Field](field-object-dao.md)** no índice exigem ou não valores que não são Nulos e, em seguida, usar a propriedade **IgnoreNulls** para determinar se os valores nulos têm ou não entradas de índice.

- Usar as propriedades **Primary** e **Unique** para determinar a ordem e a exclusividade do objeto **Index**.

O mecanismo de banco de dados do Microsoft Access mantém todos os índices da tabela base automaticamente. Ele atualiza os índices sempre que você adiciona, altera ou exclui registros da tabela base. Após a criação do banco de dados, use o método **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** periodicamente para obter atualizações das estatísticas de índice.

Ao acessar um objeto **Recordset** tipo tabela, especifique a ordem dos registros utilizando a propriedade **Index** do objeto. Defina essa propriedade para a configuração da propriedade **Name** de um objeto **Index** existente na coleção **Indexes**. Essa coleção está contida no objeto **[TableDef](tabledef-object-dao.md)**, base do objeto **Recordset** que você está preenchendo.

> [!NOTE]
> <P>[!OBSERVAçãO] Você não tem que criar índices para uma tabela, mas para tabelas grandes e não indexadas, acessar um registro específico ou processar associações pode demorar muito tempo. Por outro lado, ter muitos índices pode tornar mais lentas as atualizações para o banco de dados, pois cada índice de tabela é corrigido.</P>

A propriedade **[Attributes](field-attributes-property-dao.md)** de cada objeto **Field** no índice determina a ordem dos registros retornados e consequentemente determina quais técnicas de acesso serão utilizadas para aquele índice.

Cada objeto **Field** na coleção **Fields** de um objeto **Index** é um componente do índice. Para definir um novo objeto **Index**, defina suas propriedades antes de acrescentá-lo a uma coleção, tornando o objeto **Index** disponível para uso subsequente.

> [!NOTE]
> <P>[!OBSERVAçãO] Você pode modificar a configuração da propriedade <STRONG>Name</STRONG> de um objeto <STRONG>Index</STRONG> existente somente se a configuração da propriedade <STRONG><A href="connection-updatable-property-dao.md">Updatable</A></STRONG> do objeto <STRONG>TableDef</STRONG> contido for <STRONG>True</STRONG>.</P>

Quando você define uma chave primária para uma tabela, o mecanismo de banco de dados do Microsoft Access define-a automaticamente como o índice principal. Este consiste em um ou mais campos que identificam todos os registros de uma tabela, de forma exclusiva, em uma ordem predefinida. Como o campo do índice principal deve ser exclusivo, o mecanismo de banco de dados do Microsoft Access define automaticamente a propriedade **Unique** do objeto **Index** principal como **True**. Se o índice principal consistir em mais de um campo, cada campo poderá conter valores duplicados, mas a combinação de valores de todos os campos indexados deve ser exclusiva. Um índice principal consiste em uma chave para a tabela e é sempre composto pelos mesmos campos que a chave primária.

> [!IMPORTANT]
> [!IMPORTANTE] Certifique-se de que os dados sejam compatíveis com os atributos do novo índice. Se o índice exigir valores exclusivos, certifique-se de que não haja duplicatas nos registros de dados existentes. Se houver duplicatas, o mecanismo de banco de dados do Microsoft Access não poderá criar o índice ; ocorrerá um erro interceptável quando você tentar usar o método Append no novo índice.

Quando você cria uma relação que impõe a integridade referencial, o mecanismo de banco de dados do Microsoft Access cria automaticamente um índice com a propriedade **Foreign** definida como a chave estrangeira na tabela de referência. Depois que você estabelece uma relação de tabela, o mecanismo de banco de dados do Microsoft Access impede que sejam feitas inclusões ou alterações no banco de dados que violem essa relação. Se você definir a propriedade **Attributes** do objeto **[Relation](relation-object-dao.md)** para permitir atualizações em cascata e exclusões em cascata, o mecanismo de banco de dados do Microsoft Access atualizará ou excluirá automaticamente os registros das tabelas relacionadas.

1.  Use o método **CreateIndex** em um objeto **TableDef**.

2.  Use o método **CreateField** no objeto **Index** para criar um objeto **Field** para cada campo (coluna) a ser incluído no objeto **Index**.

3.  Defina as propriedades **Index** conforme necessário.

4.  Acrescente o objeto **Field** na coleção **Fields**.

5.  Acrescente o objeto **Index** na coleção **Indexes**.
    

    > [!NOTE]
    > <P>[!OBSERVAçãO] A propriedade <STRONG>Clustered</STRONG> é ignorada para bancos de dados que usam o mecanismo de banco de dados do Microsoft Access, que não aceita índices agrupados.</P>



## <a name="example"></a>Exemplo

Este exemplo cria um novo objeto **Index**, acrescenta-o à coleção **Indexes** do **TableDef** Employees e enumera a coleção **Indexes** do **TableDef**. Por último, enumera um **Recordset**, primeiramente usando o **Index** principal em, em seguida, usando o novo **Index**. O procedimento IndexOutput é exigido para a execução deste procedimento.

```vb
    Sub IndexObjectX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxNew As Index 
     Dim idxLoop As Index 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create new index, create and append Field 
     ' objects to its Fields collection. 
     Set idxNew = .CreateIndex("NewIndex") 
     
     With idxNew 
     .Fields.Append .CreateField("Country") 
     .Fields.Append .CreateField("LastName") 
     .Fields.Append .CreateField("FirstName") 
     End With 
     
     ' Add new Index object to the Indexes collection 
     ' of the Employees table collection. 
     .Indexes.Append idxNew 
     .Indexes.Refresh 
     
     Debug.Print .Indexes.Count & " Indexes in " & _ 
     .Name & " TableDef" 
     
     ' Enumerate Indexes collection of Employees 
     ' table. 
     For Each idxLoop In .Indexes 
     Debug.Print " " & idxLoop.Name 
     Next idxLoop 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     ' Print report using old and new indexes. 
     IndexOutput rstEmployees, "PrimaryKey" 
     IndexOutput rstEmployees, idxNew.Name 
     rstEmployees.Close 
     
     ' Delete new Index because this is a 
     ' demonstration. 
     .Indexes.Delete idxNew.Name 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub IndexOutput(rstTemp As Recordset, _ 
     strIndex As String) 
     ' Report function for FieldX. 
     
     With rstTemp 
     ' Set the index. 
     .Index = strIndex 
     .MoveFirst 
     Debug.Print "Recordset = " & .Name & _ 
     ", Index = " & .Index 
     Debug.Print " EmployeeID - Country - Name" 
     
     ' Enumerate the recordset using the specified 
     ' index. 
     Do While Not .EOF 
     Debug.Print " " & !EmployeeID & " - " & _ 
     !Country & " - " & !LastName & ", " & !FirstName 
     .MoveNext 
     Loop 
     
     End With 
     
    End Sub 
```

<br/>

Este exemplo usa o método **CreateIndex** para criar dois novos objetos **Index** e acrescenta-os à coleção **Indexes** do objeto **TableDef** de Employees. Em seguida, é enumerada a coleção **Indexes** do objeto **TableDef**, a coleção **Fields** dos novos objetos **Index** e a coleção Properties dos novos objetos **Index**. A função CreateIndexOutput é exigida para a execução deste procedimento.

```vb
    Sub CreateIndexX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxCountry As Index 
     Dim idxFirstName As Index 
     Dim idxLoop As Index 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create first Index object, create and append Field 
     ' objects to the Index object, and then append the 
     ' Index object to the Indexes collection of the 
     ' TableDef. 
     Set idxCountry = .CreateIndex("CountryIndex") 
     With idxCountry 
     .Fields.Append .CreateField("Country") 
     .Fields.Append .CreateField("LastName") 
     .Fields.Append .CreateField("FirstName") 
     End With 
     .Indexes.Append idxCountry 
     
     ' Create second Index object, create and append Field 
     ' objects to the Index object, and then append the 
     ' Index object to the Indexes collection of the 
     ' TableDef. 
     Set idxFirstName = .CreateIndex 
     With idxFirstName 
     .Name = "FirstNameIndex" 
     .Fields.Append .CreateField("FirstName") 
     .Fields.Append .CreateField("LastName") 
     End With 
     .Indexes.Append idxFirstName 
     
     ' Refresh collection so that you can access new Index 
     ' objects. 
     .Indexes.Refresh 
     
     Debug.Print .Indexes.Count & " Indexes in " & _ 
     .Name & " TableDef" 
     
     ' Enumerate Indexes collection. 
     For Each idxLoop In .Indexes 
     Debug.Print " " & idxLoop.Name 
     Next idxLoop 
     
     ' Print report. 
     CreateIndexOutput idxCountry 
     CreateIndexOutput idxFirstName 
     
     ' Delete new Index objects because this is a 
     ' demonstration. 
     .Indexes.Delete idxCountry.Name 
     .Indexes.Delete idxFirstName.Name 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function CreateIndexOutput(idxTemp As Index) 
     
     Dim fldLoop As Field 
     Dim prpLoop As Property 
     
     With idxTemp 
     ' Enumerate Fields collection of Index object. 
     Debug.Print "Fields in " & .Name 
     For Each fldLoop In .Fields 
     Debug.Print " " & fldLoop.Name 
     Next fldLoop 
     
     ' Enumerate Properties collection of Index object. 
     Debug.Print "Properties of " & .Name 
     For Each prpLoop In .Properties 
     Debug.Print " " & prpLoop.Name & " - " & _ 
     IIf(prpLoop = "", "[empty]", prpLoop) 
     Next prpLoop 
     End With 
     
    End Function
```
