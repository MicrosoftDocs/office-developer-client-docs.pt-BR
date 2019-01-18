---
title: Objeto CubeDef (ADO MD)
TOCTitle: CubeDef object (ADO MD)
ms:assetid: 199235b7-3d98-f655-27bc-94f66e994e06
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248941(v=office.15)
ms:contentKeyID: 48543502
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c82c95a430da76694fe26300e877e86f86a2eb4b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719901"
---
# <a name="cubedef-object-ado-md"></a><span data-ttu-id="71234-102">Objeto CubeDef (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="71234-102">CubeDef object (ADO MD)</span></span>


<span data-ttu-id="71234-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="71234-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="71234-104">Representa um cubo em um esquema multidimensional, contendo um conjunto de dimensões relacionadas.</span><span class="sxs-lookup"><span data-stu-id="71234-104">Represents a cube from a multidimensional schema, containing a set of related dimensions.</span></span>

## <a name="remarks"></a><span data-ttu-id="71234-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="71234-105">Remarks</span></span>

<span data-ttu-id="71234-106">Com as coleções e propriedades de um objeto **CubeDef**, você pode fazer o que segue:</span><span class="sxs-lookup"><span data-stu-id="71234-106">With the collections and properties of a **CubeDef** object, you can do the following:</span></span>

  - <span data-ttu-id="71234-107">Identificar um **CubeDef** com a propriedade [Name](name-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="71234-107">Identify a **CubeDef** with the [Name](name-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="71234-108">Retornar uma cadeia de caracteres que descreva o cubo com a propriedade [Description](description-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="71234-108">Return a string that describes the cube with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="71234-109">Retornar as dimensões do cubo com a coleção [Dimensions](dimensions-collection-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="71234-109">Return the dimensions that make up the cube with the [Dimensions](dimensions-collection-ado-md.md) collection.</span></span>

  - <span data-ttu-id="71234-110">Obter informações adicionais sobre **CubeDef** com a coleção [Properties](properties-collection-ado.md) do ADO padrão.</span><span class="sxs-lookup"><span data-stu-id="71234-110">Obtain additional information about the **CubeDef** with the standard ADO [Properties](properties-collection-ado.md) collection.</span></span>

<span data-ttu-id="71234-p101">A coleção **Properties** contém propriedades fornecidas pelo provedor. A tabela a seguir lista propriedades que talvez estejam disponíveis. A lista de propriedades verdadeira pode diferir, de acordo com a implementação do provedor. Consulte a documentação do seu provedor para obter uma lista mais completa de propriedades disponíveis.</span><span class="sxs-lookup"><span data-stu-id="71234-p101">The **Properties** collection contains provider-supplied properties. The following table lists properties that might be available. The actual property list may differ depending upon the implementation of the provider. See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="71234-115">Nome</span><span class="sxs-lookup"><span data-stu-id="71234-115">Name</span></span></p></th>
<th><p><span data-ttu-id="71234-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="71234-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="71234-117">Nome_do_catálogo</span><span class="sxs-lookup"><span data-stu-id="71234-117">CatalogName</span></span></p></td>
<td><p><span data-ttu-id="71234-118">O nome do catálogo ao qual este cubo pertence.</span><span class="sxs-lookup"><span data-stu-id="71234-118">The name of the catalog to which this cube belongs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71234-119">CreatedOn</span><span class="sxs-lookup"><span data-stu-id="71234-119">CreatedOn</span></span></p></td>
<td><p><span data-ttu-id="71234-120">Data e hora de criação do cubo.</span><span class="sxs-lookup"><span data-stu-id="71234-120">Date and time of cube creation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71234-121">CubeGUID</span><span class="sxs-lookup"><span data-stu-id="71234-121">CubeGUID</span></span></p></td>
<td><p><span data-ttu-id="71234-122">GUID do cubo.</span><span class="sxs-lookup"><span data-stu-id="71234-122">Cube GUID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71234-123">Nome do cubo</span><span class="sxs-lookup"><span data-stu-id="71234-123">CubeName</span></span></p></td>
<td><p><span data-ttu-id="71234-124">O nome do cubo.</span><span class="sxs-lookup"><span data-stu-id="71234-124">The name of the cube.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71234-125">CubeType</span><span class="sxs-lookup"><span data-stu-id="71234-125">CubeType</span></span></p></td>
<td><p><span data-ttu-id="71234-126">O tipo do cubo.</span><span class="sxs-lookup"><span data-stu-id="71234-126">The type of the cube.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71234-127">DataUpdatedBy</span><span class="sxs-lookup"><span data-stu-id="71234-127">DataUpdatedBy</span></span></p></td>
<td><p><span data-ttu-id="71234-128">Identificação de usuário da pessoa que realizou a última atualização de dados.</span><span class="sxs-lookup"><span data-stu-id="71234-128">User ID of the person doing the last data update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71234-129">Description</span><span class="sxs-lookup"><span data-stu-id="71234-129">Description</span></span></p></td>
<td><p><span data-ttu-id="71234-130">Uma descrição consistente do cubo.</span><span class="sxs-lookup"><span data-stu-id="71234-130">A meaningful description of the cube.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71234-131">LastSchemaUpdate</span><span class="sxs-lookup"><span data-stu-id="71234-131">LastSchemaUpdate</span></span></p></td>
<td><p><span data-ttu-id="71234-132">Data e hora da última atualização do esquema.</span><span class="sxs-lookup"><span data-stu-id="71234-132">Date and time of last schema update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71234-133">SchemaName</span><span class="sxs-lookup"><span data-stu-id="71234-133">SchemaName</span></span></p></td>
<td><p><span data-ttu-id="71234-134">O nome do esquema ao qual este cubo pertence.</span><span class="sxs-lookup"><span data-stu-id="71234-134">The name of the schema to which this cube belongs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71234-135">SchemaUpdatedBy</span><span class="sxs-lookup"><span data-stu-id="71234-135">SchemaUpdatedBy</span></span></p></td>
<td><p><span data-ttu-id="71234-136">Identificação de usuário da pessoa que realizou a última atualização de esquema.</span><span class="sxs-lookup"><span data-stu-id="71234-136">User ID of the person doing the last schema update.</span></span></p></td>
</tr>
</tbody>
</table>

