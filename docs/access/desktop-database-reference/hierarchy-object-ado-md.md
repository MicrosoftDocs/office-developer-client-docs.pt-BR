---
title: Objeto Hierarchy (ADO MD)
TOCTitle: Hierarchy Object (ADO MD)
ms:assetid: 26e4e690-59ad-fb87-66b0-f3310df42d0c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249031(v=office.15)
ms:contentKeyID: 48543825
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ad6eb40873d0cd88b441adaa5568ad57dced83c6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869782"
---
# <a name="hierarchy-object-ado-md"></a><span data-ttu-id="e57d3-102">Objeto Hierarchy (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="e57d3-102">Hierarchy Object (ADO MD)</span></span>


<span data-ttu-id="e57d3-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="e57d3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e57d3-p101">Representa uma maneira como os membros de uma [dimensão](dimension-object-ado-md.md) podem ser agregados. É possível agregar uma dimensão juntamente com uma ou mais hierarquias.</span><span class="sxs-lookup"><span data-stu-id="e57d3-p101">Represents one way in which the members of a [dimension](dimension-object-ado-md.md) can be aggregated or "rolled up." A dimension can be aggregated along one or more hierarchies.</span></span>

## <a name="remarks"></a><span data-ttu-id="e57d3-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="e57d3-106">Remarks</span></span>

<span data-ttu-id="e57d3-107">Com as coleções e as propriedades de um objeto **Hierarchy**, você pode fazer o que segue:</span><span class="sxs-lookup"><span data-stu-id="e57d3-107">With the collections and properties of a **Hierarchy** object, you can do the following:</span></span>

  - <span data-ttu-id="e57d3-108">Identificar **Hierarchy** com as propriedades [Name](name-property-ado-md.md) e [UniqueName](uniquename-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="e57d3-108">Identify the **Hierarchy** with the [Name](name-property-ado-md.md) and [UniqueName](uniquename-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="e57d3-109">Retornar uma cadeia de caracteres consistente que descreva **Hierarchy** com a propriedade [Description](description-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="e57d3-109">Return a meaningful string that describes the **Hierarchy** with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="e57d3-110">Retornar os objetos [Level](level-object-ado-md.md) que compõem a **Hierarchy** com a coleção [Levels](levels-collection-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="e57d3-110">Return the [Level](level-object-ado-md.md) objects that make up the **Hierarchy** with the [Levels](levels-collection-ado-md.md) collection.</span></span>

  - <span data-ttu-id="e57d3-111">Usar a coleção [Properties](properties-collection-ado.md) do ADO padrão para obter informações adicionais sobre o objeto **Hierarchy**.</span><span class="sxs-lookup"><span data-stu-id="e57d3-111">Use the standard ADO [Properties](properties-collection-ado.md) collection to obtain additional information about the **Hierarchy** object.</span></span>

<span data-ttu-id="e57d3-p102">A coleção **Properties** contém propriedades fornecidas pelo provedor. A tabela a seguir lista propriedades que talvez estejam disponíveis. A lista de propriedades verdadeira pode diferir, de acordo com a implementação do provedor. Consulte a documentação do seu provedor para obter uma lista mais completa de propriedades disponíveis.</span><span class="sxs-lookup"><span data-stu-id="e57d3-p102">The **Properties** collection contains provider-supplied properties. The following table lists properties that might be available. The actual property list may differ depending upon the implementation of the provider. See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e57d3-116">Nome</span><span class="sxs-lookup"><span data-stu-id="e57d3-116">Name</span></span></p></th>
<th><p><span data-ttu-id="e57d3-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="e57d3-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e57d3-118">AllMember</span><span class="sxs-lookup"><span data-stu-id="e57d3-118">AllMember</span></span></p></td>
<td><p><span data-ttu-id="e57d3-119">O membro de nível mais alto de acúmulo na hierarquia.</span><span class="sxs-lookup"><span data-stu-id="e57d3-119">The member at the highest level of rollup in the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e57d3-120">Nome_do_catálogo</span><span class="sxs-lookup"><span data-stu-id="e57d3-120">CatalogName</span></span></p></td>
<td><p><span data-ttu-id="e57d3-121">O nome do catálogo ao qual o cubo pertence.</span><span class="sxs-lookup"><span data-stu-id="e57d3-121">The name of the catalog to which this cube belongs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e57d3-122">Nome do cubo</span><span class="sxs-lookup"><span data-stu-id="e57d3-122">CubeName</span></span></p></td>
<td><p><span data-ttu-id="e57d3-123">O nome do cubo.</span><span class="sxs-lookup"><span data-stu-id="e57d3-123">The name of the cube.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e57d3-124">DefaultMember</span><span class="sxs-lookup"><span data-stu-id="e57d3-124">DefaultMember</span></span></p></td>
<td><p><span data-ttu-id="e57d3-125">O nome exclusivo do membro padrão desta hierarquia.</span><span class="sxs-lookup"><span data-stu-id="e57d3-125">The unique name of the default member for this hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e57d3-126">Description</span><span class="sxs-lookup"><span data-stu-id="e57d3-126">Description</span></span></p></td>
<td><p><span data-ttu-id="e57d3-127">Uma descrição consistente da hierarquia.</span><span class="sxs-lookup"><span data-stu-id="e57d3-127">A meaningful description of the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e57d3-128">DimensionType</span><span class="sxs-lookup"><span data-stu-id="e57d3-128">DimensionType</span></span></p></td>
<td><p><span data-ttu-id="e57d3-129">O tipo da dimensão ao qual esta hierarquia pertence.</span><span class="sxs-lookup"><span data-stu-id="e57d3-129">The type of dimension to which this hierarchy belongs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e57d3-130">DimensionUniqueName</span><span class="sxs-lookup"><span data-stu-id="e57d3-130">DimensionUniqueName</span></span></p></td>
<td><p><span data-ttu-id="e57d3-131">O nome inequívoco da dimensão.</span><span class="sxs-lookup"><span data-stu-id="e57d3-131">The unambiguous name of the dimension.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e57d3-132">HierarchyCaption</span><span class="sxs-lookup"><span data-stu-id="e57d3-132">HierarchyCaption</span></span></p></td>
<td><p><span data-ttu-id="e57d3-133">Um rótulo ou uma legenda associada à hierarquia.</span><span class="sxs-lookup"><span data-stu-id="e57d3-133">A label or caption associated with the hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e57d3-134">HierarchyCardinality</span><span class="sxs-lookup"><span data-stu-id="e57d3-134">HierarchyCardinality</span></span></p></td>
<td><p><span data-ttu-id="e57d3-135">O número de membros na hierarquia.</span><span class="sxs-lookup"><span data-stu-id="e57d3-135">The number of members in the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e57d3-136">HierarchyGUID</span><span class="sxs-lookup"><span data-stu-id="e57d3-136">HierarchyGUID</span></span></p></td>
<td><p><span data-ttu-id="e57d3-137">O GUID da hierarquia.</span><span class="sxs-lookup"><span data-stu-id="e57d3-137">The GUID of the hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e57d3-138">HierarchyName</span><span class="sxs-lookup"><span data-stu-id="e57d3-138">HierarchyName</span></span></p></td>
<td><p><span data-ttu-id="e57d3-139">O nome da hierarquia.</span><span class="sxs-lookup"><span data-stu-id="e57d3-139">The name of the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e57d3-140">HierarchyUniqueName</span><span class="sxs-lookup"><span data-stu-id="e57d3-140">HierarchyUniqueName</span></span></p></td>
<td><p><span data-ttu-id="e57d3-141">O nome inequívoco da hierarquia.</span><span class="sxs-lookup"><span data-stu-id="e57d3-141">The unambiguous name of the hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e57d3-142">SchemaName</span><span class="sxs-lookup"><span data-stu-id="e57d3-142">SchemaName</span></span></p></td>
<td><p><span data-ttu-id="e57d3-143">O nome do esquema ao qual este cubo pertence.</span><span class="sxs-lookup"><span data-stu-id="e57d3-143">The name of the schema to which this cube belongs.</span></span></p></td>
</tr>
</tbody>
</table>

