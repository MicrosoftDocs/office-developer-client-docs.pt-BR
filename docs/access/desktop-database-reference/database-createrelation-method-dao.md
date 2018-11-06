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
ms.openlocfilehash: 1de2b13892ceda1cf34758414d38e649545f229e
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998270"
---
# <a name="databasecreaterelation-method-dao"></a><span data-ttu-id="2dd87-102">Método Database.CreateRelation (DAO)</span><span class="sxs-lookup"><span data-stu-id="2dd87-102">Database.CreateRelation method (DAO)</span></span>

<span data-ttu-id="2dd87-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="2dd87-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2dd87-p101">Cria um novo objeto **[Relation](relation-object-dao.md)** (apenas espaços de trabalho do Microsoft Access). .</span><span class="sxs-lookup"><span data-stu-id="2dd87-p101">Creates a new **[Relation](relation-object-dao.md)** object (Microsoft Access workspaces only). .</span></span>

## <a name="syntax"></a><span data-ttu-id="2dd87-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2dd87-106">Syntax</span></span>

<span data-ttu-id="2dd87-107">*expressão* . CreateRelation (***nome***, ***tabela***, ***ForeignTable***, ***atributos***)</span><span class="sxs-lookup"><span data-stu-id="2dd87-107">*expression* .CreateRelation(***Name***, ***Table***, ***ForeignTable***, ***Attributes***)</span></span>

<span data-ttu-id="2dd87-108">*expressão* Uma variável que representa um objeto de **banco de dados** .</span><span class="sxs-lookup"><span data-stu-id="2dd87-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="2dd87-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2dd87-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2dd87-110">Nome</span><span class="sxs-lookup"><span data-stu-id="2dd87-110">Name</span></span></p></th>
<th><p><span data-ttu-id="2dd87-111">Obrigatório/opcional</span><span class="sxs-lookup"><span data-stu-id="2dd87-111">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="2dd87-112">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="2dd87-112">Data type</span></span></p></th>
<th><p><span data-ttu-id="2dd87-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="2dd87-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2dd87-114"><em>Nome</em></span><span class="sxs-lookup"><span data-stu-id="2dd87-114"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="2dd87-115">Opcional</span><span class="sxs-lookup"><span data-stu-id="2dd87-115">Optional</span></span></p></td>
<td><p><span data-ttu-id="2dd87-116"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="2dd87-116"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="2dd87-p102">Um <strong>Variant</strong> (subtipo <strong>String</strong>) que denomina exclusivamente o novo objeto <strong>Relation</strong>. Consulte a propriedade <strong><a href="connection-name-property-dao.md">Name</a></strong> para obter detalhes sobre nomes válidos de <strong>Relation</strong>.</span><span class="sxs-lookup"><span data-stu-id="2dd87-p102">A <strong>Variant</strong> (<strong>String</strong> subtype) that uniquely names the new <strong>Relation</strong> object. See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for details on valid <strong>Relation</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2dd87-119"><em>Table</em></span><span class="sxs-lookup"><span data-stu-id="2dd87-119"><em>Table</em></span></span></p></td>
<td><p><span data-ttu-id="2dd87-120">Opcional</span><span class="sxs-lookup"><span data-stu-id="2dd87-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="2dd87-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="2dd87-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="2dd87-p103">Um <strong>Variant</strong> (subtipo <strong>String</strong>) que denomina a tabela primária na relação. Se a tabela não existir antes de você acrescentar o objeto <strong>Relation</strong>, ocorrerá um erro em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="2dd87-p103">A <strong>Variant</strong> (<strong>String</strong> subtype) that names the primary table in the relation. If the table doesn't exist before you append the <strong>Relation</strong> object, a run-time error occurs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2dd87-124"><em>ForeignTable</em></span><span class="sxs-lookup"><span data-stu-id="2dd87-124"><em>ForeignTable</em></span></span></p></td>
<td><p><span data-ttu-id="2dd87-125">Opcional</span><span class="sxs-lookup"><span data-stu-id="2dd87-125">Optional</span></span></p></td>
<td><p><span data-ttu-id="2dd87-126"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="2dd87-126"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="2dd87-p104">Um <strong>Variant</strong> (subtipo <strong>String</strong>) que denomina a tabela externa na relação. Se a tabela não existir antes de você acrescentar o objeto <strong>Relation</strong>, ocorrerá um erro em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="2dd87-p104">A <strong>Variant</strong> (<strong>String</strong> subtype) that names the foreign table in the relation. If the table doesn't exist before you append the <strong>Relation</strong> object, a run-time error occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2dd87-129"><em>Attributes</em></span><span class="sxs-lookup"><span data-stu-id="2dd87-129"><em>Attributes</em></span></span></p></td>
<td><p><span data-ttu-id="2dd87-130">Opcional</span><span class="sxs-lookup"><span data-stu-id="2dd87-130">Optional</span></span></p></td>
<td><p><span data-ttu-id="2dd87-131"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="2dd87-131"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="2dd87-p105">Uma constante ou combinação de constantes que contém informações sobre o tipo de relação. Consulte a propriedade <strong><a href="field-attributes-property-dao.md">Attributes</a></strong> para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="2dd87-p105">A constant or combination of constants that contains information about the relationship type. See the <strong><a href="field-attributes-property-dao.md">Attributes</a></strong> property for details.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="2dd87-134">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="2dd87-134">Return value</span></span>

<span data-ttu-id="2dd87-135">Relation</span><span class="sxs-lookup"><span data-stu-id="2dd87-135">Relation</span></span>

## <a name="remarks"></a><span data-ttu-id="2dd87-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="2dd87-136">Remarks</span></span>

<span data-ttu-id="2dd87-p106">O objeto **Relation** fornece informações ao mecanismo de banco de dados do Microsoft Access sobre a relação entre campos em dois objetos **[TableDef](tabledef-object-dao.md)** ou **[QueryDef](querydef-object-dao.md)**. Você pode implementar integridade referencial usando a propriedade **Attributes**.</span><span class="sxs-lookup"><span data-stu-id="2dd87-p106">The **Relation** object provides information to the Microsoft Access database engine about the relationship between fields in two **[TableDef](tabledef-object-dao.md)** or **[QueryDef](querydef-object-dao.md)** objects. You can implement referential integrity by using the **Attributes** property.</span></span>

<span data-ttu-id="2dd87-p107">Se omitir uma ou mais dessas partes opcionais quando usar o método **CreateRelation**, você poderá usar uma instrução de atribuição apropriada para definir ou redefinir a propriedade correspondente antes de acrescentar o novo objeto à coleção. Depois de acrescentar o objeto, você não poderá alterar nenhuma de suas configurações de propriedade. Consulte os tópicos de propriedade individuais para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="2dd87-p107">If you omit one or more of the optional parts when you use the **CreateRelation** method, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the object, you can't alter any of its property settings. See the individual property topics for more details.</span></span>

<span data-ttu-id="2dd87-142">Antes de poder usar o método **[Append](fields-append-method-dao.md)** em um objeto **Relation**, você deve acrescentar os objetos **[Field](field-object-dao.md)** apropriados para definir as tabelas de relações entre chaves primária e estrangeira.</span><span class="sxs-lookup"><span data-stu-id="2dd87-142">Before you can use the **[Append](fields-append-method-dao.md)** method on a **Relation** object, you must append the appropriate **[Field](field-object-dao.md)** objects to define the primary and foreign key relationship tables.</span></span>

<span data-ttu-id="2dd87-143">Se name fizer referência a um objeto que já é um membro da coleção, ou se os nomes de objeto de **campos** fornecidos na coleção **Fields** subordinada forem inválidos, ocorrerá um erro de tempo de execução quando você usa o método **Append** .</span><span class="sxs-lookup"><span data-stu-id="2dd87-143">If name refers to an object that is already a member of the collection or if the **Field** object names provided in the subordinate **Fields** collection are invalid, a run-time error occurs when you use the **Append** method.</span></span>

<span data-ttu-id="2dd87-144">Você não pode estabelecer ou manter uma relação entre uma tabela replicada e uma tabela local.</span><span class="sxs-lookup"><span data-stu-id="2dd87-144">You can't establish or maintain a relationship between a replicated table and a local table.</span></span>

<span data-ttu-id="2dd87-145">Para remover um objeto **Relation** da coleção **[Relations](relations-collection-dao.md)**, use o método **[Delete](fields-delete-method-dao.md)** na coleção.</span><span class="sxs-lookup"><span data-stu-id="2dd87-145">To remove a **Relation** object from the **[Relations](relations-collection-dao.md)** collection, use the **[Delete](fields-delete-method-dao.md)** method on the collection.</span></span>

## <a name="example"></a><span data-ttu-id="2dd87-146">Exemplo</span><span class="sxs-lookup"><span data-stu-id="2dd87-146">Example</span></span>

<span data-ttu-id="2dd87-p108">Este exemplo usa o método **CreateRelation** para criar um objeto **Relation** entre **TableDef** de Funcionários e um novo **TableDef** chamado Departamentos. Este exemplo também demonstra como criar um novo objeto **Relation** também cria qualquer objeto **Indexes** necessários na tabela externa (o Índice DepartmentsEmployees na tabela Funcionários).</span><span class="sxs-lookup"><span data-stu-id="2dd87-p108">This example uses the **CreateRelation** method to create a **Relation** between the Employees **TableDef** and a new **TableDef** called Departments. This example also demonstrates how creating a new **Relation** will also create any necessary **Indexes** in the foreign table (the DepartmentsEmployees Index in the Employees table).</span></span>

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
