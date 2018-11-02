---
title: Objeto CubeDef (ADO MD)
TOCTitle: CubeDef object (ADO MD)
ms:assetid: 199235b7-3d98-f655-27bc-94f66e994e06
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248941(v=office.15)
ms:contentKeyID: 48543502
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9f48b3ea16e45b3bde12ed9f8584c3218f955eba
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922388"
---
# <a name="cubedef-object-ado-md"></a><span data-ttu-id="c59b8-102">Objeto CubeDef (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="c59b8-102">CubeDef object (ADO MD)</span></span>


<span data-ttu-id="c59b8-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="c59b8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c59b8-104">Representa um cubo em um esquema multidimensional, contendo um conjunto de dimensões relacionadas.</span><span class="sxs-lookup"><span data-stu-id="c59b8-104">Represents a cube from a multidimensional schema, containing a set of related dimensions.</span></span>

## <a name="remarks"></a><span data-ttu-id="c59b8-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="c59b8-105">Remarks</span></span>

<span data-ttu-id="c59b8-106">Com as coleções e propriedades de um objeto **CubeDef**, você pode fazer o que segue:</span><span class="sxs-lookup"><span data-stu-id="c59b8-106">With the collections and properties of a **CubeDef** object, you can do the following:</span></span>

  - <span data-ttu-id="c59b8-107">Identificar um **CubeDef** com a propriedade [Name](name-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="c59b8-107">Identify a **CubeDef** with the [Name](name-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="c59b8-108">Retornar uma cadeia de caracteres que descreva o cubo com a propriedade [Description](description-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="c59b8-108">Return a string that describes the cube with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="c59b8-109">Retornar as dimensões do cubo com a coleção [Dimensions](dimensions-collection-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="c59b8-109">Return the dimensions that make up the cube with the [Dimensions](dimensions-collection-ado-md.md) collection.</span></span>

  - <span data-ttu-id="c59b8-110">Obter informações adicionais sobre **CubeDef** com a coleção [Properties](properties-collection-ado.md) do ADO padrão.</span><span class="sxs-lookup"><span data-stu-id="c59b8-110">Obtain additional information about the **CubeDef** with the standard ADO [Properties](properties-collection-ado.md) collection.</span></span>

<span data-ttu-id="c59b8-p101">A coleção **Properties** contém propriedades fornecidas pelo provedor. A tabela a seguir lista propriedades que talvez estejam disponíveis. A lista de propriedades verdadeira pode diferir, de acordo com a implementação do provedor. Consulte a documentação do seu provedor para obter uma lista mais completa de propriedades disponíveis.</span><span class="sxs-lookup"><span data-stu-id="c59b8-p101">The **Properties** collection contains provider-supplied properties. The following table lists properties that might be available. The actual property list may differ depending upon the implementation of the provider. See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c59b8-115">Nome</span><span class="sxs-lookup"><span data-stu-id="c59b8-115">Name</span></span></p></th>
<th><p><span data-ttu-id="c59b8-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="c59b8-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c59b8-117">Nome_do_catálogo</span><span class="sxs-lookup"><span data-stu-id="c59b8-117">CatalogName</span></span></p></td>
<td><p><span data-ttu-id="c59b8-118">O nome do catálogo ao qual este cubo pertence.</span><span class="sxs-lookup"><span data-stu-id="c59b8-118">The name of the catalog to which this cube belongs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c59b8-119">CreatedOn</span><span class="sxs-lookup"><span data-stu-id="c59b8-119">CreatedOn</span></span></p></td>
<td><p><span data-ttu-id="c59b8-120">Data e hora de criação do cubo.</span><span class="sxs-lookup"><span data-stu-id="c59b8-120">Date and time of cube creation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c59b8-121">CubeGUID</span><span class="sxs-lookup"><span data-stu-id="c59b8-121">CubeGUID</span></span></p></td>
<td><p><span data-ttu-id="c59b8-122">GUID do cubo.</span><span class="sxs-lookup"><span data-stu-id="c59b8-122">Cube GUID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c59b8-123">Nome do cubo</span><span class="sxs-lookup"><span data-stu-id="c59b8-123">CubeName</span></span></p></td>
<td><p><span data-ttu-id="c59b8-124">O nome do cubo.</span><span class="sxs-lookup"><span data-stu-id="c59b8-124">The name of the cube.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c59b8-125">CubeType</span><span class="sxs-lookup"><span data-stu-id="c59b8-125">CubeType</span></span></p></td>
<td><p><span data-ttu-id="c59b8-126">O tipo do cubo.</span><span class="sxs-lookup"><span data-stu-id="c59b8-126">The type of the cube.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c59b8-127">DataUpdatedBy</span><span class="sxs-lookup"><span data-stu-id="c59b8-127">DataUpdatedBy</span></span></p></td>
<td><p><span data-ttu-id="c59b8-128">Identificação de usuário da pessoa que realizou a última atualização de dados.</span><span class="sxs-lookup"><span data-stu-id="c59b8-128">User ID of the person doing the last data update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c59b8-129">Description</span><span class="sxs-lookup"><span data-stu-id="c59b8-129">Description</span></span></p></td>
<td><p><span data-ttu-id="c59b8-130">Uma descrição consistente do cubo.</span><span class="sxs-lookup"><span data-stu-id="c59b8-130">A meaningful description of the cube.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c59b8-131">LastSchemaUpdate</span><span class="sxs-lookup"><span data-stu-id="c59b8-131">LastSchemaUpdate</span></span></p></td>
<td><p><span data-ttu-id="c59b8-132">Data e hora da última atualização do esquema.</span><span class="sxs-lookup"><span data-stu-id="c59b8-132">Date and time of last schema update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c59b8-133">SchemaName</span><span class="sxs-lookup"><span data-stu-id="c59b8-133">SchemaName</span></span></p></td>
<td><p><span data-ttu-id="c59b8-134">O nome do esquema ao qual este cubo pertence.</span><span class="sxs-lookup"><span data-stu-id="c59b8-134">The name of the schema to which this cube belongs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c59b8-135">SchemaUpdatedBy</span><span class="sxs-lookup"><span data-stu-id="c59b8-135">SchemaUpdatedBy</span></span></p></td>
<td><p><span data-ttu-id="c59b8-136">Identificação de usuário da pessoa que realizou a última atualização de esquema.</span><span class="sxs-lookup"><span data-stu-id="c59b8-136">User ID of the person doing the last schema update.</span></span></p></td>
</tr>
</tbody>
</table>

