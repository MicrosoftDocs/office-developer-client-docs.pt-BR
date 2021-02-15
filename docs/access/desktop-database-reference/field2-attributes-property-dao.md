---
title: Propriedade Field2.Attributes (DAO)
TOCTitle: Attributes Property
ms:assetid: 08ae9b6b-21e4-9b7e-0852-cfc6639027a7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845025(v=office.15)
ms:contentKeyID: 48543102
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052896
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a655cfa5c6f0427b1a26a01f01e991564ab8e387
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292885"
---
# <a name="field2attributes-property-dao"></a><span data-ttu-id="28dc7-102">Propriedade Field2.Attributes (DAO)</span><span class="sxs-lookup"><span data-stu-id="28dc7-102">Field2.Attributes property (DAO)</span></span>


<span data-ttu-id="28dc7-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="28dc7-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="28dc7-104">Define ou retorna um valor que indica uma ou mais características de um objeto **Field2**.</span><span class="sxs-lookup"><span data-stu-id="28dc7-104">Sets or returns a value that indicates one or more characteristics of a **Field2** object.</span></span> <span data-ttu-id="28dc7-105">**Long** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="28dc7-105">Read/write **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="28dc7-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="28dc7-106">Syntax</span></span>

<span data-ttu-id="28dc7-107">*expressão* .Attributes</span><span class="sxs-lookup"><span data-stu-id="28dc7-107">*expression* .Attributes</span></span>

<span data-ttu-id="28dc7-108">*expressão* Uma variável que representa um objeto **Field2**.</span><span class="sxs-lookup"><span data-stu-id="28dc7-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="28dc7-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="28dc7-109">Remarks</span></span>

<span data-ttu-id="28dc7-110">O valor especifica características do campo representadas pelo objeto **Field2** e pode ser uma combinação dessas constantes.</span><span class="sxs-lookup"><span data-stu-id="28dc7-110">The value specifies characteristics of the field represented by the **Field2** object and can be a combination of these constants.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="28dc7-111">Constante</span><span class="sxs-lookup"><span data-stu-id="28dc7-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="28dc7-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="28dc7-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="28dc7-113"><strong>dbAutoIncrField</strong></span><span class="sxs-lookup"><span data-stu-id="28dc7-113"><strong>dbAutoIncrField</strong></span></span></p></td>
<td><p><span data-ttu-id="28dc7-114">O valor do campo para novos registros é automaticamente incrementado em um inteiro Long exclusivo que não pode ser alterado (em um espaço de trabalho do Microsoft Access, aceito somente para tabelas de banco de dados do mecanismo de banco de dados do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="28dc7-114">The field value for new records is automatically incremented to a unique Long integer that can't be changed (in a Microsoft Access workspace, supported only for Microsoft Access database engine database tables).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28dc7-115"><strong>dbDescending</strong></span><span class="sxs-lookup"><span data-stu-id="28dc7-115"><strong>dbDescending</strong></span></span></p></td>
<td><p><span data-ttu-id="28dc7-116">O campo é classificado em ordem decrescente (Z para A ou 100 para 0); essa opção se aplica a um objeto <strong>Field2</strong> em uma coleção <strong>Fields</strong> de um índice <strong>Index</strong>.</span><span class="sxs-lookup"><span data-stu-id="28dc7-116">The field is sorted in descending (Z to A or 100 to 0) order; this option applies only to a <strong>Field2</strong> object in a <strong>Fields</strong> collection of an <strong>Index</strong> object.</span></span> <span data-ttu-id="28dc7-117">Se você omitir essa constante, o campo é classificado em ordem crescente (A até Z ou de 0 a 100).</span><span class="sxs-lookup"><span data-stu-id="28dc7-117">If you omit this constant, the field is sorted in ascending (A to Z or 0 to 100) order.</span></span> <span data-ttu-id="28dc7-118">Este é o valor padrão para <strong>Índice</strong> e campos de <strong>TableDef</strong> (espaços de trabalho apenas do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="28dc7-118">This is the default value for <strong>Index</strong> and <strong>TableDef</strong> fields (Microsoft Access workspaces only)..</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28dc7-119"><strong>dbFixedField</strong></span><span class="sxs-lookup"><span data-stu-id="28dc7-119"><strong>dbFixedField</strong></span></span></p></td>
<td><p><span data-ttu-id="28dc7-120">O tamanho do campo é corrigido (padrão para Campos numéricos).</span><span class="sxs-lookup"><span data-stu-id="28dc7-120">The field size is fixed (default for Numeric fields).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28dc7-121"><strong>dbHyperlinkField</strong></span><span class="sxs-lookup"><span data-stu-id="28dc7-121"><strong>dbHyperlinkField</strong></span></span></p></td>
<td><p><span data-ttu-id="28dc7-122">O campo contém informações sobre o hiperlink (apenas campos Memorando).</span><span class="sxs-lookup"><span data-stu-id="28dc7-122">The field contains hyperlink information (Memo fields only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28dc7-123"><strong>dbSystemField</strong></span><span class="sxs-lookup"><span data-stu-id="28dc7-123"><strong>dbSystemField</strong></span></span></p></td>
<td><p><span data-ttu-id="28dc7-124">O campo armazena informações de replicação para réplicas; não é possível excluir esse tipo de campo (apenas espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="28dc7-124">The field stores replication information for replicas; you can't delete this type of field (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28dc7-125"><strong>dbUpdatableField</strong></span><span class="sxs-lookup"><span data-stu-id="28dc7-125"><strong>dbUpdatableField</strong></span></span></p></td>
<td><p><span data-ttu-id="28dc7-126">O valor de campo pode ser alterado.</span><span class="sxs-lookup"><span data-stu-id="28dc7-126">The field value can be changed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28dc7-127"><strong>dbVariableField</strong></span><span class="sxs-lookup"><span data-stu-id="28dc7-127"><strong>dbVariableField</strong></span></span></p></td>
<td><p><span data-ttu-id="28dc7-128">O tamanho do campo é variável (somente campos de texto).</span><span class="sxs-lookup"><span data-stu-id="28dc7-128">The field size is variable (Text fields only).</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="28dc7-p103">Para um objeto que não está acrescentado a uma coleção, essa propriedade é de leitura/gravação. Para um objeto **Field2** acrescentado, a disponibilidade da propriedade **Attributes** depende do objeto que contém a coleção **Fields**.</span><span class="sxs-lookup"><span data-stu-id="28dc7-p103">For an object not yet appended to a collection, this property is read/write. For an appended **Field2** object, the availability of the **Attributes** property depends on the object that contains the **Fields** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="28dc7-131">Se o objeto Fields pertencer a</span><span class="sxs-lookup"><span data-stu-id="28dc7-131">If the Field object belongs to an</span></span></p></th>
<th><p><span data-ttu-id="28dc7-132">Attributes serão</span><span class="sxs-lookup"><span data-stu-id="28dc7-132">Then Attributes is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="28dc7-133">Objeto do <strong>Índice</strong> </span><span class="sxs-lookup"><span data-stu-id="28dc7-133"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="28dc7-134">Leitura/gravação até o objeto <strong>TableDef</strong> que o objeto do <strong>Índice</strong> é anexado ao seu anexo para o objeto de <strong>Banco de dados</strong>; em seguida, a propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="28dc7-134">Read/write until the <strong>TableDef</strong> object that the <strong>Index</strong> object is appended to is appended to a <strong>Database</strong> object; then the property is read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28dc7-135">
						Objeto <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="28dc7-135"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="28dc7-136">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="28dc7-136">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28dc7-137">
						Objeto <strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="28dc7-137"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="28dc7-138">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="28dc7-138">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28dc7-139">
						Objeto <strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="28dc7-139"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="28dc7-140">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="28dc7-140">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28dc7-141">
						Objeto <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="28dc7-141"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="28dc7-142">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="28dc7-142">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="28dc7-p104">Quando você define vários atributos, é possível combiná-los somando as constantes apropriadas. Qualquer valor inválido é ignorado sem gerar nenhum erro.</span><span class="sxs-lookup"><span data-stu-id="28dc7-p104">When you set multiple attributes, you can combine them by summing the appropriate constants. Any invalid values are ignored without producing an error.</span></span>

## <a name="example"></a><span data-ttu-id="28dc7-145">Exemplo</span><span class="sxs-lookup"><span data-stu-id="28dc7-145">Example</span></span>

<span data-ttu-id="28dc7-146">Este exemplo exibe a propriedade **Attributes** para os objetos **Field2**, **Relation** e **TableDef** no banco de dados Northwind.</span><span class="sxs-lookup"><span data-stu-id="28dc7-146">This example displays the **Attributes** property for **Field2**, **Relation**, and **TableDef** objects in the Northwind database.</span></span>

```vb 
Sub AttributesX() 
 
 Dim dbsNorthwind As Database 
 Dim fldLoop As Field2 
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

