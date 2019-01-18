---
title: Método Database.CreateRelation (DAO)
TOCTitle: CreateRelation Method
ms:assetid: e240c7e3-c293-5e19-afcc-34d9a5549c64
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835692(v=office.15)
ms:contentKeyID: 48548279
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052969
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 365835bc579a431d34b65cd27ed4de4e12bca309
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716877"
---
# <a name="databasecreaterelation-method-dao"></a>Método Database.CreateRelation (DAO)

**Aplica-se a**: Access 2013, o Office 2013

Cria um novo objeto **[Relation](relation-object-dao.md)** (apenas espaços de trabalho do Microsoft Access). .

## <a name="syntax"></a>Sintaxe

*expressão* . CreateRelation (***nome***, ***tabela***, ***ForeignTable***, ***atributos***)

*expressão* Uma variável que representa um objeto de **banco de dados** .

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
<th><p>Obrigatório/opcional</p></th>
<th><p>Tipo de dados</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Um <strong>Variant</strong> (subtipo <strong>String</strong>) que denomina exclusivamente o novo objeto <strong>Relation</strong>. Consulte a propriedade <strong><a href="connection-name-property-dao.md">Name</a></strong> para obter detalhes sobre nomes válidos de <strong>Relation</strong>.</p></td>
</tr>
<tr class="even">
<td><p><em>Table</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Um <strong>Variant</strong> (subtipo <strong>String</strong>) que denomina a tabela primária na relação. Se a tabela não existir antes de você acrescentar o objeto <strong>Relation</strong>, ocorrerá um erro em tempo de execução.</p></td>
</tr>
<tr class="odd">
<td><p><em>ForeignTable</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Um <strong>Variant</strong> (subtipo <strong>String</strong>) que denomina a tabela externa na relação. Se a tabela não existir antes de você acrescentar o objeto <strong>Relation</strong>, ocorrerá um erro em tempo de execução.</p></td>
</tr>
<tr class="even">
<td><p><em>Atributos</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Uma constante ou combinação de constantes que contém informações sobre o tipo de relação. Consulte a propriedade <strong><a href="field-attributes-property-dao.md">Attributes</a></strong> para obter detalhes.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Valor de retorno

Relation

## <a name="remarks"></a>Comentários

O objeto **Relation** fornece informações ao mecanismo de banco de dados do Microsoft Access sobre a relação entre campos em dois objetos **[TableDef](tabledef-object-dao.md)** ou **[QueryDef](querydef-object-dao.md)**. Você pode implementar integridade referencial usando a propriedade **Attributes**.

Se omitir uma ou mais dessas partes opcionais quando usar o método **CreateRelation**, você poderá usar uma instrução de atribuição apropriada para definir ou redefinir a propriedade correspondente antes de acrescentar o novo objeto à coleção. Depois de acrescentar o objeto, você não poderá alterar nenhuma de suas configurações de propriedade. Consulte os tópicos de propriedade individuais para obter mais detalhes.

Antes de poder usar o método **[Append](fields-append-method-dao.md)** em um objeto **Relation**, você deve acrescentar os objetos **[Field](field-object-dao.md)** apropriados para definir as tabelas de relações entre chaves primária e estrangeira.

Se name fizer referência a um objeto que já é um membro da coleção, ou se os nomes de objeto de **campos** fornecidos na coleção **Fields** subordinada forem inválidos, ocorrerá um erro de tempo de execução quando você usa o método **Append** .

Você não pode estabelecer ou manter uma relação entre uma tabela replicada e uma tabela local.

Para remover um objeto **Relation** da coleção **[Relations](relations-collection-dao.md)**, use o método **[Delete](fields-delete-method-dao.md)** na coleção.

## <a name="example"></a>Exemplo

Este exemplo usa o método **CreateRelation** para criar um objeto **Relation** entre **TableDef** de Funcionários e um novo **TableDef** chamado Departamentos. Este exemplo também demonstra como criar um novo objeto **Relation** também cria qualquer objeto **Indexes** necessários na tabela externa (o Índice DepartmentsEmployees na tabela Funcionários).

```vb
    Sub CreateRelationX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim tdfNew As TableDef 
     Dim idxNew As Index 
     Dim relNew As Relation 
     Dim idxLoop As Index 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Add new field to Employees table. 
     Set tdfEmployees = .TableDefs!Employees 
     tdfEmployees.Fields.Append _ 
     tdfEmployees.CreateField("DeptID", dbInteger, 2) 
     
     ' Create new Departments table. 
     Set tdfNew = .CreateTableDef("Departments") 
     
     With tdfNew 
     ' Create and append Field objects to Fields 
     ' collection of the new TableDef object. 
     .Fields.Append .CreateField("DeptID", dbInteger, 2) 
     .Fields.Append .CreateField("DeptName", dbText, 20) 
     
     ' Create Index object for Departments table. 
     Set idxNew = .CreateIndex("DeptIDIndex") 
     ' Create and append Field object to Fields 
     ' collection of the new Index object. 
     idxNew.Fields.Append idxNew.CreateField("DeptID") 
     ' The index in the primary table must be Unique in 
     ' order to be part of a Relation. 
     idxNew.Unique = True 
     .Indexes.Append idxNew 
     End With 
     
     .TableDefs.Append tdfNew 
     
     ' Create EmployeesDepartments Relation object, using 
     ' the names of the two tables in the relation. 
     Set relNew = .CreateRelation("EmployeesDepartments", _ 
     tdfNew.Name, tdfEmployees.Name, _ 
     dbRelationUpdateCascade) 
     
     ' Create Field object for the Fields collection of the 
     ' new Relation object. Set the Name and ForeignName 
     ' properties based on the fields to be used for the 
     ' relation. 
     relNew.Fields.Append relNew.CreateField("DeptID") 
     relNew.Fields!DeptID.ForeignName = "DeptID" 
     .Relations.Append relNew 
     
     ' Print report. 
     Debug.Print "Properties of " & relNew.Name & _ 
     " Relation" 
     Debug.Print " Table = " & relNew.Table 
     Debug.Print " ForeignTable = " & _ 
     relNew.ForeignTable 
     Debug.Print "Fields of " & relNew.Name & " Relation" 
     
     With relNew.Fields!DeptID 
     Debug.Print " " & .Name 
     Debug.Print " Name = " & .Name 
     Debug.Print " ForeignName = " & .ForeignName 
     End With 
     
     Debug.Print "Indexes in " & tdfEmployees.Name & _ 
     " TableDef" 
     For Each idxLoop In tdfEmployees.Indexes 
     Debug.Print " " & idxLoop.Name & _ 
     ", Foreign = " & idxLoop.Foreign 
     Next idxLoop 
     
     ' Delete new objects because this is a demonstration. 
     .Relations.Delete relNew.Name 
     .TableDefs.Delete tdfNew.Name 
     tdfEmployees.Fields.Delete "DeptID" 
     .Close 
     End With 
     
    End Sub
```
