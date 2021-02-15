---
title: Objeto Hierarchy (ADO MD)
TOCTitle: Hierarchy object (ADO MD)
ms:assetid: 26e4e690-59ad-fb87-66b0-f3310df42d0c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249031(v=office.15)
ms:contentKeyID: 48543825
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c6668dfd40f7d0d26bcfa2ca4149acdc713e14c6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291926"
---
# <a name="hierarchy-object-ado-md"></a><span data-ttu-id="98009-102">Objeto Hierarchy (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="98009-102">Hierarchy object (ADO MD)</span></span>


<span data-ttu-id="98009-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="98009-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="98009-p101">Representa uma maneira como os membros de uma [dimensão](dimension-object-ado-md.md) podem ser agregados. É possível agregar uma dimensão juntamente com uma ou mais hierarquias.</span><span class="sxs-lookup"><span data-stu-id="98009-p101">Represents one way in which the members of a [dimension](dimension-object-ado-md.md) can be aggregated or "rolled up." A dimension can be aggregated along one or more hierarchies.</span></span>

## <a name="remarks"></a><span data-ttu-id="98009-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="98009-106">Remarks</span></span>

<span data-ttu-id="98009-107">Com as coleções e as propriedades de um objeto **Hierarchy**, você pode fazer o que segue:</span><span class="sxs-lookup"><span data-stu-id="98009-107">With the collections and properties of a **Hierarchy** object, you can do the following:</span></span>

  - <span data-ttu-id="98009-108">Identificar **Hierarchy** com as propriedades [Name](name-property-ado-md.md) e [UniqueName](uniquename-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="98009-108">Identify the **Hierarchy** with the [Name](name-property-ado-md.md) and [UniqueName](uniquename-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="98009-109">Retornar uma cadeia de caracteres consistente que descreva **Hierarchy** com a propriedade [Description](description-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="98009-109">Return a meaningful string that describes the **Hierarchy** with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="98009-110">Retornar os objetos [Level](level-object-ado-md.md) que compõem a **Hierarchy** com a coleção [Levels](levels-collection-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="98009-110">Return the [Level](level-object-ado-md.md) objects that make up the **Hierarchy** with the [Levels](levels-collection-ado-md.md) collection.</span></span>

  - <span data-ttu-id="98009-111">Usar a coleção [Properties](properties-collection-ado.md) do ADO padrão para obter informações adicionais sobre o objeto **Hierarchy**.</span><span class="sxs-lookup"><span data-stu-id="98009-111">Use the standard ADO [Properties](properties-collection-ado.md) collection to obtain additional information about the **Hierarchy** object.</span></span>

<span data-ttu-id="98009-p102">A coleção **Properties** contém propriedades fornecidas pelo provedor. A tabela a seguir lista propriedades que talvez estejam disponíveis. A lista de propriedades verdadeira pode diferir, de acordo com a implementação do provedor. Consulte a documentação do seu provedor para obter uma lista mais completa de propriedades disponíveis.</span><span class="sxs-lookup"><span data-stu-id="98009-p102">The **Properties** collection contains provider-supplied properties. The following table lists properties that might be available. The actual property list may differ depending upon the implementation of the provider. See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="98009-116">Nome</span><span class="sxs-lookup"><span data-stu-id="98009-116">Name</span></span></p></th>
<th><p><span data-ttu-id="98009-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="98009-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="98009-118">AllMember</span><span class="sxs-lookup"><span data-stu-id="98009-118">AllMember</span></span></p></td>
<td><p><span data-ttu-id="98009-119">O membro de nível mais alto de acúmulo na hierarquia.</span><span class="sxs-lookup"><span data-stu-id="98009-119">The member at the highest level of rollup in the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98009-120">CatalogName</span><span class="sxs-lookup"><span data-stu-id="98009-120">CatalogName</span></span></p></td>
<td><p><span data-ttu-id="98009-121">O nome do catálogo ao qual o cubo pertence.</span><span class="sxs-lookup"><span data-stu-id="98009-121">The name of the catalog to which this cube belongs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98009-122">CubeName</span><span class="sxs-lookup"><span data-stu-id="98009-122">CubeName</span></span></p></td>
<td><p><span data-ttu-id="98009-123">O nome do cubo.</span><span class="sxs-lookup"><span data-stu-id="98009-123">The name of the cube.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98009-124">DefaultMember</span><span class="sxs-lookup"><span data-stu-id="98009-124">DefaultMember</span></span></p></td>
<td><p><span data-ttu-id="98009-125">O nome exclusivo do membro padrão desta hierarquia.</span><span class="sxs-lookup"><span data-stu-id="98009-125">The unique name of the default member for this hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98009-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="98009-126">Description</span></span></p></td>
<td><p><span data-ttu-id="98009-127">Uma descrição consistente da hierarquia.</span><span class="sxs-lookup"><span data-stu-id="98009-127">A meaningful description of the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98009-128">DimensionType</span><span class="sxs-lookup"><span data-stu-id="98009-128">DimensionType</span></span></p></td>
<td><p><span data-ttu-id="98009-129">O tipo da dimensão ao qual esta hierarquia pertence.</span><span class="sxs-lookup"><span data-stu-id="98009-129">The type of dimension to which this hierarchy belongs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98009-130">DimensionUniqueName</span><span class="sxs-lookup"><span data-stu-id="98009-130">DimensionUniqueName</span></span></p></td>
<td><p><span data-ttu-id="98009-131">O nome inequívoco da dimensão.</span><span class="sxs-lookup"><span data-stu-id="98009-131">The unambiguous name of the dimension.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98009-132">HierarchyCaption</span><span class="sxs-lookup"><span data-stu-id="98009-132">HierarchyCaption</span></span></p></td>
<td><p><span data-ttu-id="98009-133">Um rótulo ou uma legenda associada à hierarquia.</span><span class="sxs-lookup"><span data-stu-id="98009-133">A label or caption associated with the hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98009-134">HierarchyItudenality</span><span class="sxs-lookup"><span data-stu-id="98009-134">HierarchyCardinality</span></span></p></td>
<td><p><span data-ttu-id="98009-135">O número de membros na hierarquia.</span><span class="sxs-lookup"><span data-stu-id="98009-135">The number of members in the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98009-136">HierarchyGUID</span><span class="sxs-lookup"><span data-stu-id="98009-136">HierarchyGUID</span></span></p></td>
<td><p><span data-ttu-id="98009-137">O GUID da hierarquia.</span><span class="sxs-lookup"><span data-stu-id="98009-137">The GUID of the hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98009-138">HierarchyName</span><span class="sxs-lookup"><span data-stu-id="98009-138">HierarchyName</span></span></p></td>
<td><p><span data-ttu-id="98009-139">O nome da hierarquia.</span><span class="sxs-lookup"><span data-stu-id="98009-139">The name of the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98009-140">HierarchyUniqueName</span><span class="sxs-lookup"><span data-stu-id="98009-140">HierarchyUniqueName</span></span></p></td>
<td><p><span data-ttu-id="98009-141">O nome inequívoco da hierarquia.</span><span class="sxs-lookup"><span data-stu-id="98009-141">The unambiguous name of the hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98009-142">SchemaName</span><span class="sxs-lookup"><span data-stu-id="98009-142">SchemaName</span></span></p></td>
<td><p><span data-ttu-id="98009-143">O nome do esquema ao qual este cubo pertence.</span><span class="sxs-lookup"><span data-stu-id="98009-143">The name of the schema to which this cube belongs.</span></span></p></td>
</tr>
</tbody>
</table>

