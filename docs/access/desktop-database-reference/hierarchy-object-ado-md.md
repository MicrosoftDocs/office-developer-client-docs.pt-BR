---
title: Objeto Hierarchy (ADO MD)
TOCTitle: Hierarchy Object (ADO MD)
ms:assetid: 26e4e690-59ad-fb87-66b0-f3310df42d0c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249031(v=office.15)
ms:contentKeyID: 48543825
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 34513e3188653bdba04add376f06911ce86386bd
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464878"
---
# <a name="hierarchy-object-ado-md"></a><span data-ttu-id="8a2fe-102">Objeto Hierarchy (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="8a2fe-102">Hierarchy Object (ADO MD)</span></span>


<span data-ttu-id="8a2fe-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8a2fe-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8a2fe-p101">Representa uma maneira como os membros de uma [dimensão](dimension-object-ado-md.md) podem ser agregados. É possível agregar uma dimensão juntamente com uma ou mais hierarquias.</span><span class="sxs-lookup"><span data-stu-id="8a2fe-p101">Represents one way in which the members of a [dimension](dimension-object-ado-md.md) can be aggregated or "rolled up." A dimension can be aggregated along one or more hierarchies.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a2fe-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="8a2fe-106">Remarks</span></span>

<span data-ttu-id="8a2fe-107">Com as coleções e as propriedades de um objeto **Hierarchy**, você pode fazer o que segue:</span><span class="sxs-lookup"><span data-stu-id="8a2fe-107">With the collections and properties of a **Hierarchy** object, you can do the following:</span></span>

  - <span data-ttu-id="8a2fe-108">Identificar **Hierarchy** com as propriedades [Name](name-property-ado-md.md) e [UniqueName](uniquename-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="8a2fe-108">Identify the **Hierarchy** with the [Name](name-property-ado-md.md) and [UniqueName](uniquename-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="8a2fe-109">Retornar uma cadeia de caracteres consistente que descreva **Hierarchy** com a propriedade [Description](description-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="8a2fe-109">Return a meaningful string that describes the **Hierarchy** with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="8a2fe-110">Retornar os objetos [Level](level-object-ado-md.md) que compõem a **Hierarchy** com a coleção [Levels](levels-collection-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="8a2fe-110">Return the [Level](level-object-ado-md.md) objects that make up the **Hierarchy** with the [Levels](levels-collection-ado-md.md) collection.</span></span>

  - <span data-ttu-id="8a2fe-111">Usar a coleção [Properties](properties-collection-ado.md) do ADO padrão para obter informações adicionais sobre o objeto **Hierarchy**.</span><span class="sxs-lookup"><span data-stu-id="8a2fe-111">Use the standard ADO [Properties](properties-collection-ado.md) collection to obtain additional information about the **Hierarchy** object.</span></span>

<span data-ttu-id="8a2fe-p102">A coleção **Properties** contém propriedades fornecidas pelo provedor. A tabela a seguir lista propriedades que talvez estejam disponíveis. A lista de propriedades verdadeira pode diferir, de acordo com a implementação do provedor. Consulte a documentação do seu provedor para obter uma lista mais completa de propriedades disponíveis.</span><span class="sxs-lookup"><span data-stu-id="8a2fe-p102">The **Properties** collection contains provider-supplied properties. The following table lists properties that might be available. The actual property list may differ depending upon the implementation of the provider. See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8a2fe-116">Nome</span><span class="sxs-lookup"><span data-stu-id="8a2fe-116">Name</span></span></p></th>
<th><p><span data-ttu-id="8a2fe-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="8a2fe-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8a2fe-118">AllMember</span><span class="sxs-lookup"><span data-stu-id="8a2fe-118">AllMember</span></span></p></td>
<td><p><span data-ttu-id="8a2fe-119">O membro de nível mais alto de acúmulo na hierarquia.</span><span class="sxs-lookup"><span data-stu-id="8a2fe-119">The member at the highest level of rollup in the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8a2fe-120">Nome_do_catálogo</span><span class="sxs-lookup"><span data-stu-id="8a2fe-120">CatalogName</span></span></p></td>
<td><p><span data-ttu-id="8a2fe-121">O nome do catálogo ao qual o cubo pertence.</span><span class="sxs-lookup"><span data-stu-id="8a2fe-121">The name of the catalog to which this cube belongs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8a2fe-122">Nome do cubo</span><span class="sxs-lookup"><span data-stu-id="8a2fe-122">CubeName</span></span></p></td>
<td><p><span data-ttu-id="8a2fe-123">O nome do cubo.</span><span class="sxs-lookup"><span data-stu-id="8a2fe-123">The name of the cube.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8a2fe-124">DefaultMember</span><span class="sxs-lookup"><span data-stu-id="8a2fe-124">DefaultMember</span></span></p></td>
<td><p><span data-ttu-id="8a2fe-125">O nome exclusivo do membro padrão desta hierarquia.</span><span class="sxs-lookup"><span data-stu-id="8a2fe-125">The unique name of the default member for this hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8a2fe-126">Description</span><span class="sxs-lookup"><span data-stu-id="8a2fe-126">Description</span></span></p></td>
<td><p><span data-ttu-id="8a2fe-127">Uma descrição consistente da hierarquia.</span><span class="sxs-lookup"><span data-stu-id="8a2fe-127">A meaningful description of the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8a2fe-128">DimensionType</span><span class="sxs-lookup"><span data-stu-id="8a2fe-128">DimensionType</span></span></p></td>
<td><p><span data-ttu-id="8a2fe-129">O tipo da dimensão ao qual esta hierarquia pertence.</span><span class="sxs-lookup"><span data-stu-id="8a2fe-129">The type of dimension to which this hierarchy belongs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8a2fe-130">DimensionUniqueName</span><span class="sxs-lookup"><span data-stu-id="8a2fe-130">DimensionUniqueName</span></span></p></td>
<td><p><span data-ttu-id="8a2fe-131">O nome inequívoco da dimensão.</span><span class="sxs-lookup"><span data-stu-id="8a2fe-131">The unambiguous name of the dimension.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8a2fe-132">HierarchyCaption</span><span class="sxs-lookup"><span data-stu-id="8a2fe-132">HierarchyCaption</span></span></p></td>
<td><p><span data-ttu-id="8a2fe-133">Um rótulo ou uma legenda associada à hierarquia.</span><span class="sxs-lookup"><span data-stu-id="8a2fe-133">A label or caption associated with the hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8a2fe-134">HierarchyCardinality</span><span class="sxs-lookup"><span data-stu-id="8a2fe-134">HierarchyCardinality</span></span></p></td>
<td><p><span data-ttu-id="8a2fe-135">O número de membros na hierarquia.</span><span class="sxs-lookup"><span data-stu-id="8a2fe-135">The number of members in the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8a2fe-136">HierarchyGUID</span><span class="sxs-lookup"><span data-stu-id="8a2fe-136">HierarchyGUID</span></span></p></td>
<td><p><span data-ttu-id="8a2fe-137">O GUID da hierarquia.</span><span class="sxs-lookup"><span data-stu-id="8a2fe-137">The GUID of the hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8a2fe-138">HierarchyName</span><span class="sxs-lookup"><span data-stu-id="8a2fe-138">HierarchyName</span></span></p></td>
<td><p><span data-ttu-id="8a2fe-139">O nome da hierarquia.</span><span class="sxs-lookup"><span data-stu-id="8a2fe-139">The name of the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8a2fe-140">HierarchyUniqueName</span><span class="sxs-lookup"><span data-stu-id="8a2fe-140">HierarchyUniqueName</span></span></p></td>
<td><p><span data-ttu-id="8a2fe-141">O nome inequívoco da hierarquia.</span><span class="sxs-lookup"><span data-stu-id="8a2fe-141">The unambiguous name of the hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8a2fe-142">SchemaName</span><span class="sxs-lookup"><span data-stu-id="8a2fe-142">SchemaName</span></span></p></td>
<td><p><span data-ttu-id="8a2fe-143">O nome do esquema ao qual este cubo pertence.</span><span class="sxs-lookup"><span data-stu-id="8a2fe-143">The name of the schema to which this cube belongs.</span></span></p></td>
</tr>
</tbody>
</table>

