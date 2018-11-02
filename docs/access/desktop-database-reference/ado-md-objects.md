---
title: Objetos do ADO MD (referência de banco de dados da área de trabalho do Access)
TOCTitle: ADO MD objects
ms:assetid: 13501e44-70b6-1036-a8b7-c276f187e4f4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248907(v=office.15)
ms:contentKeyID: 48543366
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fca73b9e8a77e102ad694dde8fd9759b20c1fcaf
ms.sourcegitcommit: 48bfe5ab15b11105f4f52937b886c92bdc26525a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25910835"
---
# <a name="ado-md-objects"></a><span data-ttu-id="38d4a-102">Objetos do ADO MD</span><span class="sxs-lookup"><span data-stu-id="38d4a-102">ADO MD objects</span></span>

<span data-ttu-id="38d4a-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="38d4a-103">**Applies to**: Access 2013, Office 2013</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th><span data-ttu-id="38d4a-104">Objeto</span><span class="sxs-lookup"><span data-stu-id="38d4a-104">Object</span></span></th>
<th><span data-ttu-id="38d4a-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="38d4a-105">Description</span></span></th>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38d4a-106"><a href="axis-object-ado-md.md">Eixo</a></span><span class="sxs-lookup"><span data-stu-id="38d4a-106"><a href="axis-object-ado-md.md">Axis</a></span></span></p></td>
<td><p><span data-ttu-id="38d4a-107">Representa um eixo de posição ou de filtro de um conjunto de células, contendo membros selecionados de uma ou mais dimensões.</span><span class="sxs-lookup"><span data-stu-id="38d4a-107">Represents a positional or filter axis of a cellset, containing selected members of one or more dimensions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38d4a-108"><a href="catalog-object-ado-md.md">Catálogo</a></span><span class="sxs-lookup"><span data-stu-id="38d4a-108"><a href="catalog-object-ado-md.md">Catalog</a></span></span></p></td>
<td><p><span data-ttu-id="38d4a-109">Contém informações de esquema multidimensionais (isto é, cubos e dimensões subjacentes, hierarquias, níveis e membros) específicos de um MDP (provedor de dados multidimensionais).</span><span class="sxs-lookup"><span data-stu-id="38d4a-109">Contains multidimensional schema information (that is, cubes and underlying dimensions, hierarchies, levels, and members) specific to a multidimensional data provider (MDP).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38d4a-110"><a href="cell-object-ado-md.md">Cell</a></span><span class="sxs-lookup"><span data-stu-id="38d4a-110"><a href="cell-object-ado-md.md">Cell</a></span></span></p></td>
<td><p><span data-ttu-id="38d4a-111">Representa os dados na interseção de coordenadas de eixo, contidos em um conjunto de células.</span><span class="sxs-lookup"><span data-stu-id="38d4a-111">Represents the data at the intersection of axis coordinates, contained in a cellset.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38d4a-112"><a href="cellset-object-ado-md.md">Conjunto de células</a></span><span class="sxs-lookup"><span data-stu-id="38d4a-112"><a href="cellset-object-ado-md.md">Cellset</a></span></span></p></td>
<td><p><span data-ttu-id="38d4a-p101">Representa os resultados de uma consulta multidimensional. É uma coleção das células selecionadas em cubos ou outros conjuntos de células.</span><span class="sxs-lookup"><span data-stu-id="38d4a-p101">Represents the results of a multidimensional query. It is a collection of cells selected from cubes or other cellsets.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38d4a-115"><a href="cubedef-object-ado-md.md">CubeDef</a></span><span class="sxs-lookup"><span data-stu-id="38d4a-115"><a href="cubedef-object-ado-md.md">CubeDef</a></span></span></p></td>
<td><p><span data-ttu-id="38d4a-116">Representa um cubo em um esquema multidimensional, contendo um conjunto de dimensões relacionadas.</span><span class="sxs-lookup"><span data-stu-id="38d4a-116">Represents a cube from a multidimensional schema, containing a set of related dimensions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38d4a-117"><a href="dimension-object-ado-md.md">Dimensão</a></span><span class="sxs-lookup"><span data-stu-id="38d4a-117"><a href="dimension-object-ado-md.md">Dimension</a></span></span></p></td>
<td><p><span data-ttu-id="38d4a-118">Representa uma das dimensões de um cubo multidimensional, contendo uma ou maishierarquias de membros.</span><span class="sxs-lookup"><span data-stu-id="38d4a-118">Represents one of the dimensions of a multidimensional cube, containing one or more hierarchies of members.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38d4a-119"><a href="hierarchy-object-ado-md.md">Hierarquia</a></span><span class="sxs-lookup"><span data-stu-id="38d4a-119"><a href="hierarchy-object-ado-md.md">Hierarchy</a></span></span></p></td>
<td><p><span data-ttu-id="38d4a-120">Representa uma forma em que os membros de uma dimensão possam ser agregados ou &quot;acumulados. &quot; Uma dimensão possa ser agregada ao longo de uma ou mais hierarquias.</span><span class="sxs-lookup"><span data-stu-id="38d4a-120">Represents one way in which the members of a dimension can be aggregated or &quot;rolled up.&quot; A dimension can be aggregated along one or more hierarchies.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38d4a-121"><a href="level-object-ado-md.md">Nível</a></span><span class="sxs-lookup"><span data-stu-id="38d4a-121"><a href="level-object-ado-md.md">Level</a></span></span></p></td>
<td><p><span data-ttu-id="38d4a-122">Contém um conjunto de membros, sendo que cada um tem a mesma ordem em uma hierarquia.</span><span class="sxs-lookup"><span data-stu-id="38d4a-122">Contains a set of members, each of which has the same rank within a hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38d4a-123"><a href="member-object-ado-md.md">Membro</a></span><span class="sxs-lookup"><span data-stu-id="38d4a-123"><a href="member-object-ado-md.md">Member</a></span></span></p></td>
<td><p><span data-ttu-id="38d4a-124">Representa um membro de um nível em um cubo, os filhos de um membro de um nível ou um membro de uma posição em um eixo de um conjunto de células.</span><span class="sxs-lookup"><span data-stu-id="38d4a-124">Represents a member of a level in a cube, the children of a member of a level, or a member of a position along an axis of a cellset.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38d4a-125"><a href="position-object-ado-md.md">Position</a></span><span class="sxs-lookup"><span data-stu-id="38d4a-125"><a href="position-object-ado-md.md">Position</a></span></span></p></td>
<td><p><span data-ttu-id="38d4a-126">Representa um conjunto de um ou mais membros de diferentes dimensões que define um ponto em um eixo.</span><span class="sxs-lookup"><span data-stu-id="38d4a-126">Represents a set of one or more members of different dimensions that defines a point along an axis.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="38d4a-127">Além disso, o objeto **Catalog** está conectado a um objeto **Connection** do ADO, que está incluído na biblioteca padrão do ADO:</span><span class="sxs-lookup"><span data-stu-id="38d4a-127">Also, the **Catalog** object is connected to an ADO **Connection** object, which is included with the standard ADO library:</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="38d4a-128">Objeto</span><span class="sxs-lookup"><span data-stu-id="38d4a-128">Object</span></span></p></th>
<th><p><span data-ttu-id="38d4a-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="38d4a-129">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="38d4a-130"><a href="connection-object-ado.md">Connection</a></span><span class="sxs-lookup"><span data-stu-id="38d4a-130"><a href="connection-object-ado.md">Connection</a></span></span></p></td>
<td><p><span data-ttu-id="38d4a-131">Representa uma conexão aberta com uma fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="38d4a-131">Represents an open connection to a data source.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="38d4a-p102">Muitos objetos do ADO MD pode estar contidos em uma coleção correspondente. Por exemplo, um objeto [CubeDef](cubedef-object-ado-md.md) pode estar contido em uma coleção [CubeDefs](cubedefs-collection-ado-md.md) de um **Catalog**. Para obter mais informações, consulte [Coleções do ADO MD](ado-md-collections.md).</span><span class="sxs-lookup"><span data-stu-id="38d4a-p102">Many ADO MD objects can be contained in a corresponding collection. For example, a [CubeDef](cubedef-object-ado-md.md) object can be contained in a [CubeDefs](cubedefs-collection-ado-md.md) collection of a **Catalog**. For more information, see [ADO MD Collections](ado-md-collections.md).</span></span>

