---
title: Objeto Member (ADO MD)
TOCTitle: Member object (ADO MD)
ms:assetid: d80c024a-07dc-7a35-f8f2-b4d5b19d89e4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250088(v=office.15)
ms:contentKeyID: 48548025
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 380fdf6c15f6774e27221e8500100870d22350c4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709576"
---
# <a name="member-object-ado-md"></a><span data-ttu-id="d2e93-102">Objeto Member (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="d2e93-102">Member object (ADO MD)</span></span>


<span data-ttu-id="d2e93-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="d2e93-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d2e93-104">Representa um membro de um nível em um cubo, os filhos de um membro de um nível ou um membro de uma posição em um eixo de um conjunto de células.</span><span class="sxs-lookup"><span data-stu-id="d2e93-104">Represents a member of a level in a cube, the children of a member of a level, or a member of a position along an axis of a cellset.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2e93-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="d2e93-105">Remarks</span></span>

<span data-ttu-id="d2e93-p101">As propriedades de um **Member** diferem de acordo com o contexto em que ele é usado. Um **Member** de um [Level](level-object-ado-md.md) em um [CubeDef](cubedef-object-ado-md.md) tem uma propriedade [Children](children-property-ado-md.md) que retorna os **members** do nível mais baixo a seguir na hierarquia a partir do **member** atual. Para um **member** de uma [posição](position-object-ado-md.md), a coleção **Children** está sempre vazia. Além disso, a propriedade [Type](type-property-ado-md.md) aplica-se apenas a **members** de um **Level**.</span><span class="sxs-lookup"><span data-stu-id="d2e93-p101">The properties of a **Member** differ depending on the context in which it is used. A **Member** of a [Level](level-object-ado-md.md) in a [CubeDef](cubedef-object-ado-md.md) has a [Children](children-property-ado-md.md) property that returns the **Members** on the next lower level in the hierarchy from the current **Member**. For a **Member** of a [Position](position-object-ado-md.md), the **Children** collection is always empty. Also, the [Type](type-property-ado-md.md) property applies only to **Members** of a **Level**.</span></span>

<span data-ttu-id="d2e93-p102">Um **Member** de uma **Position** tem duas propriedades  [DrilledDown](drilleddown-property-ado-md.md) e [ParentSameAsPrev](parentsameasprev-property-ado-md.md)  que são úteis ao exibir o [Cellset](cellset-object-ado-md.md). Um erro ocorrerá se essas propriedades forem acessadas em um **Member** de um **Level**.</span><span class="sxs-lookup"><span data-stu-id="d2e93-p102">A **Member** of **Position** has two properties — [DrilledDown](drilleddown-property-ado-md.md) and [ParentSameAsPrev](parentsameasprev-property-ado-md.md) — that are useful when displaying the [Cellset](cellset-object-ado-md.md). An error will occur if these properties are accessed on a **Member** of a **Level**.</span></span>

<span data-ttu-id="d2e93-112">Com as coleções e propriedades de um objeto **Member** de um **Level**, você pode fazer o que segue:</span><span class="sxs-lookup"><span data-stu-id="d2e93-112">With the collections and properties of a **Member** object of a **Level**, you can do the following:</span></span>

  - <span data-ttu-id="d2e93-113">Identificar o **Member** com as propriedades [Name](name-property-ado-md.md) e [UniqueName](uniquename-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="d2e93-113">Identify the **Member** with the [Name](name-property-ado-md.md) and [UniqueName](uniquename-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="d2e93-114">Retornar uma cadeia de caracteres para ser usada ao exibir o **Member** com a propriedade [Caption](caption-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="d2e93-114">Return a string to use when displaying the **Member** with the [Caption](caption-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="d2e93-115">Retornar uma cadeia de caracteres consistente que descreva um **Member** de medida ou fórmula com a propriedade [Description](description-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="d2e93-115">Return a meaningful string that describes a measure or formula **Member** with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="d2e93-116">Determinar a natureza do **Member** com a propriedade [Type](type-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="d2e93-116">Determine the nature of the **Member** with the [Type](type-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="d2e93-117">Obter informações sobre o **Level** do **Member** com as propriedades [LevelDepth](leveldepth-property-ado-md.md) e [LevelName](levelname-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="d2e93-117">Obtain information about the **Level** of the **Member** with the [LevelDepth](leveldepth-property-ado-md.md) and [LevelName](levelname-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="d2e93-118">Obter **Members** relacionados em uma [Hierarchy](hierarchy-object-ado-md.md) com as propriedades [Parent](parent-property-ado-md.md) e [Children](children-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="d2e93-118">Obtain related **Members** in a [Hierarchy](hierarchy-object-ado-md.md) with the [Parent](parent-property-ado-md.md) and [Children](children-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="d2e93-119">Contar os filhos de um **Member** com a propriedade [ChildCount](childcount-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="d2e93-119">Count the children of a **Member** with the [ChildCount](childcount-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="d2e93-120">Usar a coleção [Properties](properties-collection-ado.md) do ADO padrão para obter informações adicionais sobre o objeto **Level**.</span><span class="sxs-lookup"><span data-stu-id="d2e93-120">Use the standard ADO [Properties](properties-collection-ado.md) collection to obtain additional information about the **Level** object.</span></span>

<span data-ttu-id="d2e93-121">Com as coleções e propriedades de um **Member** de uma **Position** ao longo de um [Axis](axis-object-ado-md.md), você pode fazer o que segue:</span><span class="sxs-lookup"><span data-stu-id="d2e93-121">With the collections and properties of a **Member** of a **Position** along an [Axis](axis-object-ado-md.md), you can do the following:</span></span>

  - <span data-ttu-id="d2e93-122">Identificar o **Member** com as propriedades [Name](name-property-ado-md.md) e [UniqueName](uniquename-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="d2e93-122">Identify the **Member** with the [Name](name-property-ado-md.md) and [UniqueName](uniquename-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="d2e93-123">Retornar uma cadeia de caracteres para ser usada ao exibir o **Member** com a propriedade [Caption](caption-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="d2e93-123">Return a string to use when displaying the **Member** with the [Caption](caption-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="d2e93-124">Retornar uma cadeia de caracteres consistente que descreva um **Member** de medida ou fórmula com a propriedade [Description](description-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="d2e93-124">Return a meaningful string that describes a measure or formula **Member** with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="d2e93-125">Obter informações sobre o **Level** do **Member** com as propriedades [LevelDepth](leveldepth-property-ado-md.md) e [LevelName](levelname-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="d2e93-125">Obtain information about the **Level** of the **Member** with the [LevelDepth](leveldepth-property-ado-md.md) and [LevelName](levelname-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="d2e93-126">Contar os filhos de um **Member** com a propriedade [ChildCount](childcount-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="d2e93-126">Count the children of a **Member** with the [ChildCount](childcount-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="d2e93-127">Usar a propriedade [DrilledDown](drilleddown-property-ado-md.md) para determinar se há pelo menos um filho no **Axis** imediatamente depois deste **Member**.</span><span class="sxs-lookup"><span data-stu-id="d2e93-127">Use the [DrilledDown](drilleddown-property-ado-md.md) property to determine whether there is at least one child on the **Axis** immediately following this **Member**.</span></span>

  - <span data-ttu-id="d2e93-128">Usar a propriedade [ParentSameAsPrev](parentsameasprev-property-ado-md.md) para determinar se o pai deste **Member** é o mesmo pai do **Member** imediatamente anterior.</span><span class="sxs-lookup"><span data-stu-id="d2e93-128">Use the [ParentSameAsPrev](parentsameasprev-property-ado-md.md) property to determine whether the parent of this **Member** is the same as the parent of the immediately preceding **Member**.</span></span>

  - <span data-ttu-id="d2e93-129">Usar a coleção [Properties](properties-collection-ado.md) do ADO padrão para obter informações adicionais sobre o objeto **Level**.</span><span class="sxs-lookup"><span data-stu-id="d2e93-129">Use the standard ADO [Properties](properties-collection-ado.md) collection to obtain additional information about the **Level** object.</span></span>

<span data-ttu-id="d2e93-p103">A coleção **Properties** contém propriedades fornecidas pelo provedor. A tabela a seguir lista propriedades que talvez estejam disponíveis. A lista de propriedades verdadeira pode diferir, de acordo com a implementação do provedor. Consulte a documentação do seu provedor para obter uma lista mais completa de propriedades disponíveis.</span><span class="sxs-lookup"><span data-stu-id="d2e93-p103">The **Properties** collection contains provider-supplied properties. The following table lists properties that might be available. The actual property list may differ depending upon the implementation of the provider. See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d2e93-134">Nome</span><span class="sxs-lookup"><span data-stu-id="d2e93-134">Name</span></span></p></th>
<th><p><span data-ttu-id="d2e93-135">Descrição</span><span class="sxs-lookup"><span data-stu-id="d2e93-135">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d2e93-136">Nome_do_catálogo</span><span class="sxs-lookup"><span data-stu-id="d2e93-136">CatalogName</span></span></p></td>
<td><p><span data-ttu-id="d2e93-137">O nome do catálogo ao qual o cubo pertence.</span><span class="sxs-lookup"><span data-stu-id="d2e93-137">The name of the catalog to which this cube belongs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2e93-138">ChildrenCardinality</span><span class="sxs-lookup"><span data-stu-id="d2e93-138">ChildrenCardinality</span></span></p></td>
<td><p><span data-ttu-id="d2e93-139">O número de filhos que o membro tem.</span><span class="sxs-lookup"><span data-stu-id="d2e93-139">The number of children that the member has.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2e93-140">Nome do cubo</span><span class="sxs-lookup"><span data-stu-id="d2e93-140">CubeName</span></span></p></td>
<td><p><span data-ttu-id="d2e93-141">O nome do cubo.</span><span class="sxs-lookup"><span data-stu-id="d2e93-141">The name of the cube.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2e93-142">Descrição</span><span class="sxs-lookup"><span data-stu-id="d2e93-142">Description</span></span></p></td>
<td><p><span data-ttu-id="d2e93-143">Uma descrição consistente do membro.</span><span class="sxs-lookup"><span data-stu-id="d2e93-143">A meaningful description of the member.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2e93-144">DimensionUniqueName</span><span class="sxs-lookup"><span data-stu-id="d2e93-144">DimensionUniqueName</span></span></p></td>
<td><p><span data-ttu-id="d2e93-145">O nome inequívoco da <a href="dimension-object-ado-md.md">dimensão</a>.</span><span class="sxs-lookup"><span data-stu-id="d2e93-145">The unambiguous name of the <a href="dimension-object-ado-md.md">dimension</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2e93-146">HierarchyUniqueName</span><span class="sxs-lookup"><span data-stu-id="d2e93-146">HierarchyUniqueName</span></span></p></td>
<td><p><span data-ttu-id="d2e93-147">O nome inequívoco da hierarquia.</span><span class="sxs-lookup"><span data-stu-id="d2e93-147">The unambiguous name of the hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2e93-148">LevelNumber</span><span class="sxs-lookup"><span data-stu-id="d2e93-148">LevelNumber</span></span></p></td>
<td><p><span data-ttu-id="d2e93-149">A distância entre o nível e a raiz da hierarquia.</span><span class="sxs-lookup"><span data-stu-id="d2e93-149">The distance between the level and the root of the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2e93-150">LevelUniqueName não</span><span class="sxs-lookup"><span data-stu-id="d2e93-150">LevelUniqueName</span></span></p></td>
<td><p><span data-ttu-id="d2e93-151">O nome inequívoco do nível.</span><span class="sxs-lookup"><span data-stu-id="d2e93-151">The unambiguous name of the level.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2e93-152">MemberCaption</span><span class="sxs-lookup"><span data-stu-id="d2e93-152">MemberCaption</span></span></p></td>
<td><p><span data-ttu-id="d2e93-153">Um rótulo ou uma legenda associada ao membro.</span><span class="sxs-lookup"><span data-stu-id="d2e93-153">A label or caption associated with the member.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2e93-154">MemberGUID</span><span class="sxs-lookup"><span data-stu-id="d2e93-154">MemberGUID</span></span></p></td>
<td><p><span data-ttu-id="d2e93-155">O GUID do membro.</span><span class="sxs-lookup"><span data-stu-id="d2e93-155">The GUID of the member.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2e93-156">Nome do membro</span><span class="sxs-lookup"><span data-stu-id="d2e93-156">MemberName</span></span></p></td>
<td><p><span data-ttu-id="d2e93-157">O nome do membro.</span><span class="sxs-lookup"><span data-stu-id="d2e93-157">The name of the member.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2e93-158">MemberOrdinal</span><span class="sxs-lookup"><span data-stu-id="d2e93-158">MemberOrdinal</span></span></p></td>
<td><p><span data-ttu-id="d2e93-159">O número ordinal do membro.</span><span class="sxs-lookup"><span data-stu-id="d2e93-159">The ordinal number of the member.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2e93-160">MemberType</span><span class="sxs-lookup"><span data-stu-id="d2e93-160">MemberType</span></span></p></td>
<td><p><span data-ttu-id="d2e93-161">O tipo do membro.</span><span class="sxs-lookup"><span data-stu-id="d2e93-161">The type of the member.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2e93-162">MemberUniqueName</span><span class="sxs-lookup"><span data-stu-id="d2e93-162">MemberUniqueName</span></span></p></td>
<td><p><span data-ttu-id="d2e93-163">O nome inequívoco do membro.</span><span class="sxs-lookup"><span data-stu-id="d2e93-163">The unambiguous name of the member.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2e93-164">ParentCount</span><span class="sxs-lookup"><span data-stu-id="d2e93-164">ParentCount</span></span></p></td>
<td><p><span data-ttu-id="d2e93-165">A contagem do número de pais que este membro tem.</span><span class="sxs-lookup"><span data-stu-id="d2e93-165">The count of the number of parents that this member has.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2e93-166">ParentLevel</span><span class="sxs-lookup"><span data-stu-id="d2e93-166">ParentLevel</span></span></p></td>
<td><p><span data-ttu-id="d2e93-167">O número do nível do pai do membro.</span><span class="sxs-lookup"><span data-stu-id="d2e93-167">The level number of the member's parent.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2e93-168">ParentUniqueName</span><span class="sxs-lookup"><span data-stu-id="d2e93-168">ParentUniqueName</span></span></p></td>
<td><p><span data-ttu-id="d2e93-169">O nome inequívoco do pai do membro.</span><span class="sxs-lookup"><span data-stu-id="d2e93-169">The unambiguous name of the member's parent.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2e93-170">SchemaName</span><span class="sxs-lookup"><span data-stu-id="d2e93-170">SchemaName</span></span></p></td>
<td><p><span data-ttu-id="d2e93-171">O nome do esquema ao qual este cubo pertence.</span><span class="sxs-lookup"><span data-stu-id="d2e93-171">The name of the schema to which this cube belongs.</span></span></p></td>
</tr>
</tbody>
</table>

