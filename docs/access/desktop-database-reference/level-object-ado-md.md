---
title: Objeto Level (ADO MD)
TOCTitle: Level object (ADO MD)
ms:assetid: ddbcabce-8777-1068-98a3-be209084f497
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250121(v=office.15)
ms:contentKeyID: 48548160
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 02637a7a7cb312f7749775f4f2bc29dcddd95e66
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923802"
---
# <a name="level-object-ado-md"></a><span data-ttu-id="d820b-102">Objeto Level (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="d820b-102">Level object (ADO MD)</span></span>


<span data-ttu-id="d820b-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="d820b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d820b-104">Contém um conjunto de membros, sendo que cada um tem a mesma ordem em uma hierarquia.</span><span class="sxs-lookup"><span data-stu-id="d820b-104">Contains a set of members, each of which has the same rank within a hierarchy.</span></span>

## <a name="remarks"></a><span data-ttu-id="d820b-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="d820b-105">Remarks</span></span>

<span data-ttu-id="d820b-106">Com as coleções e propriedades de um objeto **Level**, você pode fazer o que segue:</span><span class="sxs-lookup"><span data-stu-id="d820b-106">With the collections and properties of a **Level** object, you can do the following:</span></span>

  - <span data-ttu-id="d820b-107">Identificar o **Level** com as propriedades [Name](name-property-ado-md.md) e [UniqueName](uniquename-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="d820b-107">Identify the **Level** with the [Name](name-property-ado-md.md) and [UniqueName](uniquename-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="d820b-108">Retornar uma cadeia de caracteres para ser usada ao exibir o **Level** com a propriedade [Caption](caption-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="d820b-108">Return a string to use when displaying the **Level** with the [Caption](caption-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="d820b-109">Retornar uma cadeia de caracteres consistente que descreva o **Level** com a propriedade [Description](description-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="d820b-109">Return a meaningful string that describes the **Level** with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="d820b-110">Retornar os objetos [Member](member-object-ado-md.md) que compõem o **Level** com a coleção [Members](members-collection-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="d820b-110">Return the [Member](member-object-ado-md.md) objects that make up the **Level** with the [Members](members-collection-ado-md.md) collection.</span></span>

  - <span data-ttu-id="d820b-111">Retornar o número de níveis a partir da raiz do **Level** com a propriedade [Depth](depth-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="d820b-111">Return the number of levels from the root of the **Level** with the [Depth](depth-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="d820b-112">Usar a coleção [Properties](properties-collection-ado.md) do ADO padrão para obter informações adicionais sobre o objeto **Level**.</span><span class="sxs-lookup"><span data-stu-id="d820b-112">Use the standard ADO [Properties](properties-collection-ado.md) collection to obtain additional information about the **Level** object.</span></span>

<span data-ttu-id="d820b-p101">A coleção **Properties** contém propriedades fornecidas pelo provedor. A tabela a seguir lista propriedades que talvez estejam disponíveis. A lista de propriedades verdadeira pode diferir, de acordo com a implementação do provedor. Consulte a documentação do seu provedor para obter uma lista mais completa de propriedades disponíveis.</span><span class="sxs-lookup"><span data-stu-id="d820b-p101">The **Properties** collection contains provider-supplied properties. The following table lists properties that might be available. The actual property list may differ depending upon the implementation of the provider. See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d820b-117">Nome</span><span class="sxs-lookup"><span data-stu-id="d820b-117">Name</span></span></p></th>
<th><p><span data-ttu-id="d820b-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="d820b-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d820b-119">Nome_do_catálogo</span><span class="sxs-lookup"><span data-stu-id="d820b-119">CatalogName</span></span></p></td>
<td><p><span data-ttu-id="d820b-120">O nome do catálogo ao qual o cubo pertence.</span><span class="sxs-lookup"><span data-stu-id="d820b-120">The name of the catalog to which this cube belongs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d820b-121">Nome do cubo</span><span class="sxs-lookup"><span data-stu-id="d820b-121">CubeName</span></span></p></td>
<td><p><span data-ttu-id="d820b-122">O nome do cubo.</span><span class="sxs-lookup"><span data-stu-id="d820b-122">The name of the cube.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d820b-123">Description</span><span class="sxs-lookup"><span data-stu-id="d820b-123">Description</span></span></p></td>
<td><p><span data-ttu-id="d820b-124">Uma descrição consistente do nível.</span><span class="sxs-lookup"><span data-stu-id="d820b-124">A meaningful description of the level.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d820b-125">DimensionUniqueName</span><span class="sxs-lookup"><span data-stu-id="d820b-125">DimensionUniqueName</span></span></p></td>
<td><p><span data-ttu-id="d820b-126">O nome inequívoco da <a href="dimension-object-ado-md.md">dimensão</a>.</span><span class="sxs-lookup"><span data-stu-id="d820b-126">The unambiguous name of the <a href="dimension-object-ado-md.md">dimension</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d820b-127">HierarchyUniqueName</span><span class="sxs-lookup"><span data-stu-id="d820b-127">HierarchyUniqueName</span></span></p></td>
<td><p><span data-ttu-id="d820b-128">O nome inequívoco da hierarquia.</span><span class="sxs-lookup"><span data-stu-id="d820b-128">The unambiguous name of the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d820b-129">LevelCaption</span><span class="sxs-lookup"><span data-stu-id="d820b-129">LevelCaption</span></span></p></td>
<td><p><span data-ttu-id="d820b-130">Um rótulo ou uma legenda associada ao nível.</span><span class="sxs-lookup"><span data-stu-id="d820b-130">A label or caption associated with the level.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d820b-131">LevelCardinality</span><span class="sxs-lookup"><span data-stu-id="d820b-131">LevelCardinality</span></span></p></td>
<td><p><span data-ttu-id="d820b-132">O número de membros no nível.</span><span class="sxs-lookup"><span data-stu-id="d820b-132">The number of members in the level.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d820b-133">LevelGUID</span><span class="sxs-lookup"><span data-stu-id="d820b-133">LevelGUID</span></span></p></td>
<td><p><span data-ttu-id="d820b-134">O GUID do nível.</span><span class="sxs-lookup"><span data-stu-id="d820b-134">The GUID of the level.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d820b-135">LevelName</span><span class="sxs-lookup"><span data-stu-id="d820b-135">LevelName</span></span></p></td>
<td><p><span data-ttu-id="d820b-136">Nome do nível.</span><span class="sxs-lookup"><span data-stu-id="d820b-136">Name of the level.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d820b-137">LevelNumber</span><span class="sxs-lookup"><span data-stu-id="d820b-137">LevelNumber</span></span></p></td>
<td><p><span data-ttu-id="d820b-138">A distância entre o nível e a raiz da hierarquia.</span><span class="sxs-lookup"><span data-stu-id="d820b-138">The distance between the level and the root of the hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d820b-139">LevelType</span><span class="sxs-lookup"><span data-stu-id="d820b-139">LevelType</span></span></p></td>
<td><p><span data-ttu-id="d820b-140">O tipo do nível.</span><span class="sxs-lookup"><span data-stu-id="d820b-140">The type of level.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d820b-141">LevelUniqueName não</span><span class="sxs-lookup"><span data-stu-id="d820b-141">LevelUniqueName</span></span></p></td>
<td><p><span data-ttu-id="d820b-142">O nome inequívoco do nível.</span><span class="sxs-lookup"><span data-stu-id="d820b-142">The unambiguous name of the level.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d820b-143">SchemaName</span><span class="sxs-lookup"><span data-stu-id="d820b-143">SchemaName</span></span></p></td>
<td><p><span data-ttu-id="d820b-144">O nome do esquema ao qual este cubo pertence.</span><span class="sxs-lookup"><span data-stu-id="d820b-144">The name of the schema to which this cube belongs.</span></span></p></td>
</tr>
</tbody>
</table>

