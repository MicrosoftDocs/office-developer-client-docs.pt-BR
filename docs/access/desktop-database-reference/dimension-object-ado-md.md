---
title: Objeto Dimension (ADO MD)
TOCTitle: Dimension object (ADO MD)
ms:assetid: 12f43cfc-c74e-a2e8-7f6e-75fc68472c4b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248902(v=office.15)
ms:contentKeyID: 48543355
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c3d42c01d1d9d4e77169f74afcc97d147d6f5d53
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921184"
---
# <a name="dimension-object-ado-md"></a><span data-ttu-id="65ddc-102">Objeto Dimension (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="65ddc-102">Dimension object (ADO MD)</span></span>


<span data-ttu-id="65ddc-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="65ddc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="65ddc-104">Representa uma das dimensões de um cubo multidimensional, contendo uma ou maishierarquias de membros.</span><span class="sxs-lookup"><span data-stu-id="65ddc-104">Represents one of the dimensions of a multidimensional cube, containing one or more hierarchies of members.</span></span>

## <a name="remarks"></a><span data-ttu-id="65ddc-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="65ddc-105">Remarks</span></span>

<span data-ttu-id="65ddc-106">Com as coleções e propriedades de um objeto **Dimension**, você pode fazer o que segue:</span><span class="sxs-lookup"><span data-stu-id="65ddc-106">With the collections and properties of a **Dimension** object, you can do the following:</span></span>

  - <span data-ttu-id="65ddc-107">Identificar a **Dimension** com as propriedades [Name](name-property-ado-md.md) e [UniqueName](uniquename-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="65ddc-107">Identify the **Dimension** with the [Name](name-property-ado-md.md) and [UniqueName](uniquename-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="65ddc-108">Retornar uma cadeia de caracteres consistente que descreva a **Dimension** com a propriedade [Description](description-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="65ddc-108">Return a meaningful string that describes the **Dimension** with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="65ddc-109">Retornar os objetos [Hierarchy](hierarchy-object-ado-md.md) que compõem a **Dimension** com a coleção [Hierarchies](hierarchies-collection-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="65ddc-109">Return the [Hierarchy](hierarchy-object-ado-md.md) objects that make up the **Dimension** with the [Hierarchies](hierarchies-collection-ado-md.md) collection.</span></span>

  - <span data-ttu-id="65ddc-110">Usar a coleção [Properties](properties-collection-ado.md) do ADO padrão para obter informações adicionais sobre o objeto **Dimension**.</span><span class="sxs-lookup"><span data-stu-id="65ddc-110">Use the standard ADO [Properties](properties-collection-ado.md) collection to obtain additional information about the **Dimension** object.</span></span>

<span data-ttu-id="65ddc-p101">A coleção **Properties** contém propriedades fornecidas pelo provedor. A tabela a seguir lista propriedades que talvez estejam disponíveis. A lista de propriedades verdadeira pode diferir, de acordo com a implementação do provedor. Consulte a documentação do seu provedor para obter uma lista mais completa de propriedades disponíveis.</span><span class="sxs-lookup"><span data-stu-id="65ddc-p101">The **Properties** collection contains provider-supplied properties. The following table lists properties that might be available. The actual property list may differ depending upon the implementation of the provider. See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="65ddc-115">Nome</span><span class="sxs-lookup"><span data-stu-id="65ddc-115">Name</span></span></p></th>
<th><p><span data-ttu-id="65ddc-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="65ddc-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="65ddc-117">Nome_do_catálogo</span><span class="sxs-lookup"><span data-stu-id="65ddc-117">CatalogName</span></span></p></td>
<td><p><span data-ttu-id="65ddc-118">O nome do catálogo ao qual o cubo pertence.</span><span class="sxs-lookup"><span data-stu-id="65ddc-118">The name of the catalog to which this cube belongs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65ddc-119">Nome do cubo</span><span class="sxs-lookup"><span data-stu-id="65ddc-119">CubeName</span></span></p></td>
<td><p><span data-ttu-id="65ddc-120">O nome do cubo.</span><span class="sxs-lookup"><span data-stu-id="65ddc-120">The name of the cube.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65ddc-121">DefaultHierarchy</span><span class="sxs-lookup"><span data-stu-id="65ddc-121">DefaultHierarchy</span></span></p></td>
<td><p><span data-ttu-id="65ddc-122">O nome exclusivo da hierarquia padrão.</span><span class="sxs-lookup"><span data-stu-id="65ddc-122">The unique name of the default hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65ddc-123">Description</span><span class="sxs-lookup"><span data-stu-id="65ddc-123">Description</span></span></p></td>
<td><p><span data-ttu-id="65ddc-124">Uma descrição consistente do cubo.</span><span class="sxs-lookup"><span data-stu-id="65ddc-124">A meaningful description of the cube.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65ddc-125">DimensionCaption</span><span class="sxs-lookup"><span data-stu-id="65ddc-125">DimensionCaption</span></span></p></td>
<td><p><span data-ttu-id="65ddc-126">Um rótulo ou uma legenda associada à dimensão.</span><span class="sxs-lookup"><span data-stu-id="65ddc-126">A label or caption associated with the dimension.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65ddc-127">DimensionCardinality</span><span class="sxs-lookup"><span data-stu-id="65ddc-127">DimensionCardinality</span></span></p></td>
<td><p><span data-ttu-id="65ddc-128">O número de membros na dimensão.</span><span class="sxs-lookup"><span data-stu-id="65ddc-128">The number of members in the dimension.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65ddc-129">DimensionGUID</span><span class="sxs-lookup"><span data-stu-id="65ddc-129">DimensionGUID</span></span></p></td>
<td><p><span data-ttu-id="65ddc-130">O GUID da dimensão.</span><span class="sxs-lookup"><span data-stu-id="65ddc-130">The GUID of the dimension.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65ddc-131">DimensionName</span><span class="sxs-lookup"><span data-stu-id="65ddc-131">DimensionName</span></span></p></td>
<td><p><span data-ttu-id="65ddc-132">O nome da dimensão.</span><span class="sxs-lookup"><span data-stu-id="65ddc-132">The name of the dimension.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65ddc-133">DimensionOrdinal</span><span class="sxs-lookup"><span data-stu-id="65ddc-133">DimensionOrdinal</span></span></p></td>
<td><p><span data-ttu-id="65ddc-134">O número ordinal da dimensão no grupo de dimensões que formam o cubo.</span><span class="sxs-lookup"><span data-stu-id="65ddc-134">The ordinal number of the dimension among the group of dimensions that form the cube.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65ddc-135">DimensionType</span><span class="sxs-lookup"><span data-stu-id="65ddc-135">DimensionType</span></span></p></td>
<td><p><span data-ttu-id="65ddc-136">O tipo da dimensão.</span><span class="sxs-lookup"><span data-stu-id="65ddc-136">The dimension type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65ddc-137">DimensionUniqueName</span><span class="sxs-lookup"><span data-stu-id="65ddc-137">DimensionUniqueName</span></span></p></td>
<td><p><span data-ttu-id="65ddc-138">O nome inequívoco da dimensão.</span><span class="sxs-lookup"><span data-stu-id="65ddc-138">The unambiguous name of the dimension.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65ddc-139">SchemaName</span><span class="sxs-lookup"><span data-stu-id="65ddc-139">SchemaName</span></span></p></td>
<td><p><span data-ttu-id="65ddc-140">O nome do esquema ao qual este cubo pertence.</span><span class="sxs-lookup"><span data-stu-id="65ddc-140">The name of the schema to which this cube belongs.</span></span></p></td>
</tr>
</tbody>
</table>

