---
title: Propriedade Field.Attributes (DAO)
TOCTitle: Attributes Property
ms:assetid: 8e6f6afb-1a89-7315-c129-cf7ff19e0ca9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197380(v=office.15)
ms:contentKeyID: 48546287
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: df396935f88301a9fee9df580a5cee01705f68aa
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885777"
---
# <a name="fieldattributes-property-dao"></a><span data-ttu-id="9e57d-102">Propriedade Field.Attributes (DAO)</span><span class="sxs-lookup"><span data-stu-id="9e57d-102">Field.Attributes Property (DAO)</span></span>


<span data-ttu-id="9e57d-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="9e57d-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="9e57d-p101">Define ou retorna um valor que indica uma ou mais características de um objeto **[Field](field-object-dao.md)**. **Long** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="9e57d-p101">Sets or returns a value that indicates one or more characteristics of a **[Field](field-object-dao.md)** object. Read/write **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e57d-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9e57d-106">Syntax</span></span>

<span data-ttu-id="9e57d-107">*expressão* . Atributos</span><span class="sxs-lookup"><span data-stu-id="9e57d-107">*expression* .Attributes</span></span>

<span data-ttu-id="9e57d-108">*expressão* Uma variável que representa um objeto **Field** .</span><span class="sxs-lookup"><span data-stu-id="9e57d-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e57d-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="9e57d-109">Remarks</span></span>

<span data-ttu-id="9e57d-110">O valor especifica características do campo representadas pelo objeto **Field** e pode ser uma combinação dessas constantes.</span><span class="sxs-lookup"><span data-stu-id="9e57d-110">The value specifies characteristics of the field represented by the **Field** object and can be a combination of these constants.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9e57d-111">Constant</span><span class="sxs-lookup"><span data-stu-id="9e57d-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="9e57d-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="9e57d-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9e57d-113"><strong>dbAutoIncrField</strong></span><span class="sxs-lookup"><span data-stu-id="9e57d-113"><strong>dbAutoIncrField</strong></span></span></p></td>
<td><p><span data-ttu-id="9e57d-114">O valor do campo para novos registros é automaticamente incrementado em um inteiro Long exclusivo que não pode ser alterado (em um espaço de trabalho do Microsoft Access, aceito somente para tabelas de banco de dados do mecanismo de banco de dados do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="9e57d-114">The field value for new records is automatically incremented to a unique Long integer that can't be changed (in a Microsoft Access workspace, supported only for Microsoft Access database engine database tables).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e57d-115"><strong>dbDescending</strong></span><span class="sxs-lookup"><span data-stu-id="9e57d-115"><strong>dbDescending</strong></span></span></p></td>
<td><p><span data-ttu-id="9e57d-p102">O campo é classificado em ordem decrescente (Z para A ou 100 para 0); essa opção se aplica a um objeto <strong>Field</strong> em uma coleção <strong>Fields</strong> de um índice <strong>Index</strong>. Se você omitir essa constante, o campo será classificado em ordem crescente (A para Z ou 0 para 100). Esse é o valor padrão para os campos <strong>Index</strong> e <strong>TableDef</strong> (apenas espaços de trabalho do Microsoft Access)..</span><span class="sxs-lookup"><span data-stu-id="9e57d-p102">The field is sorted in descending (Z to A or 100 to 0) order; this option applies only to a <strong>Field</strong> object in a <strong>Fields</strong> collection of an <strong>Index</strong> object. If you omit this constant, the field is sorted in ascending (A to Z or 0 to 100) order. This is the default value for <strong>Index</strong> and <strong>TableDef</strong> fields (Microsoft Access workspaces only)..</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e57d-119"><strong>dbFixedField</strong></span><span class="sxs-lookup"><span data-stu-id="9e57d-119"><strong>dbFixedField</strong></span></span></p></td>
<td><p><span data-ttu-id="9e57d-120">O tamanho do campo é fixo (padrão para campos numéricos).</span><span class="sxs-lookup"><span data-stu-id="9e57d-120">The field size is fixed (default for Numeric fields).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e57d-121"><strong>dbHyperlinkField</strong></span><span class="sxs-lookup"><span data-stu-id="9e57d-121"><strong>dbHyperlinkField</strong></span></span></p></td>
<td><p><span data-ttu-id="9e57d-122">O campo contém informações de hiperlink (apenas campos de memorando).</span><span class="sxs-lookup"><span data-stu-id="9e57d-122">The field contains hyperlink information (Memo fields only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e57d-123"><strong>dbSystemField</strong></span><span class="sxs-lookup"><span data-stu-id="9e57d-123"><strong>dbSystemField</strong></span></span></p></td>
<td><p><span data-ttu-id="9e57d-124">O campo armazena informações de replicação para réplicas; não é possível excluir esse tipo de campo (apenas espaço de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="9e57d-124">The field stores replication information for replicas; you can't delete this type of field (Microsoft Access workspace only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e57d-125"><strong>dbUpdatableField</strong></span><span class="sxs-lookup"><span data-stu-id="9e57d-125"><strong>dbUpdatableField</strong></span></span></p></td>
<td><p><span data-ttu-id="9e57d-126">O valor do campo pode ser alterado.</span><span class="sxs-lookup"><span data-stu-id="9e57d-126">The field value can be changed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e57d-127"><strong>dbVariableField</strong></span><span class="sxs-lookup"><span data-stu-id="9e57d-127"><strong>dbVariableField</strong></span></span></p></td>
<td><p><span data-ttu-id="9e57d-128">O tamanho do campo é variável (apenas campos de texto).</span><span class="sxs-lookup"><span data-stu-id="9e57d-128">The field size is variable (Text fields only).</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9e57d-p103">Para um objeto que não está acrescentado a uma coleção, essa propriedade é de leitura/gravação. Para um objeto **Field** acrescentado, a disponibilidade da propriedade **Attributes** depende do objeto que contém a coleção **Fields**.</span><span class="sxs-lookup"><span data-stu-id="9e57d-p103">For an object not yet appended to a collection, this property is read/write. For an appended **Field** object, the availability of the **Attributes** property depends on the object that contains the **Fields** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9e57d-131">Se o objeto Fields pertencer a</span><span class="sxs-lookup"><span data-stu-id="9e57d-131">If the Field object belongs to an</span></span></p></th>
<th><p><span data-ttu-id="9e57d-132">Attributes serão</span><span class="sxs-lookup"><span data-stu-id="9e57d-132">Then Attributes is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9e57d-133">Objeto <strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="9e57d-133"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="9e57d-134">Leitura/gravação até que o objeto <strong>TableDef</strong>, que contém o objeto <strong>Index</strong>, esteja acrescentando ao objeto <strong>Database</strong>; a propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="9e57d-134">Read/write until the <strong>TableDef</strong> object that the <strong>Index</strong> object is appended to is appended to a <strong>Database</strong> object; then the property is read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e57d-135">Objeto <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="9e57d-135"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="9e57d-136">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9e57d-136">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e57d-137">Objeto <strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="9e57d-137"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="9e57d-138">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9e57d-138">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e57d-139">Objeto <strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="9e57d-139"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="9e57d-140">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="9e57d-140">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e57d-141">Objeto <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="9e57d-141"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="9e57d-142">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9e57d-142">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9e57d-p104">Quando você define vários atributos, é possível combiná-los somando as constantes apropriadas. Qualquer valor inválido é ignorado sem gerar nenhum erro.</span><span class="sxs-lookup"><span data-stu-id="9e57d-p104">When you set multiple attributes, you can combine them by summing the appropriate constants. Any invalid values are ignored without producing an error.</span></span>

## <a name="example"></a><span data-ttu-id="9e57d-145">Exemplo</span><span class="sxs-lookup"><span data-stu-id="9e57d-145">Example</span></span>

<span data-ttu-id="9e57d-146">Este exemplo exibe a propriedade **Attributes** dos objetos **Field**, **Relation** e **TableDef** no banco de dados Northwind.</span><span class="sxs-lookup"><span data-stu-id="9e57d-146">This example displays the **Attributes** property for **Field**, **Relation**, and **TableDef** objects in the Northwind database.</span></span>

```vb 
Sub AttributesX() 
 
 Dim dbsNorthwind As Database 
 Dim fldLoop As Field 
 Dim relLoop As Relation 
 Dim tdfloop As TableDef 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind 
 
 ' Display the attributes of a TableDef object's 
 ' fields. 
 Debug.Print "Attributes of fields in " & _ 
 .TableDefs(0).Name & " table:" 
 For Each fldLoop In .TableDefs(0).Fields 
 Debug.Print " " & fldLoop.Name & " = " & _ 
 fldLoop.Attributes 
 Next fldLoop 
 
 ' Display the attributes of the Northwind database's 
 ' relations. 
 Debug.Print "Attributes of relations in " & _ 
 .Name & ":" 
 For Each relLoop In .Relations 
 Debug.Print " " & relLoop.Name & " = " & _ 
 relLoop.Attributes 
 Next relLoop 
 
 ' Display the attributes of the Northwind database's 
 ' tables. 
 Debug.Print "Attributes of tables in " & .Name & ":" 
 For Each tdfloop In .TableDefs 
 Debug.Print " " & tdfloop.Name & " = " & _ 
 tdfloop.Attributes 
 Next tdfloop 
 
 .Close 
 End With 
 
End Sub 
 
```

