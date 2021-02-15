---
title: Membros Relation (DAO)
TOCTitle: Relation Members
ms:assetid: 9ee36e7d-3825-1de8-65fb-64bbcada847c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198338(v=office.15)
ms:contentKeyID: 48546670
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 84e18afe4a11e53d68397efad71ac6136c779143
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307034"
---
# <a name="relation-members-dao"></a><span data-ttu-id="6f7b8-102">Membros Relation (DAO)</span><span class="sxs-lookup"><span data-stu-id="6f7b8-102">Relation members (DAO)</span></span>


<span data-ttu-id="6f7b8-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6f7b8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6f7b8-104">Um objeto Relation representa uma relação entre campos nas tabelas ou consultas (apenas bancos de dados do mecanismo de banco de dados do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="6f7b8-104">A Relation object represents a relationship between fields in tables or queries (Microsoft Access database engine databases only).</span></span>

## <a name="methods"></a><span data-ttu-id="6f7b8-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="6f7b8-105">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6f7b8-106">Nome</span><span class="sxs-lookup"><span data-stu-id="6f7b8-106">Name</span></span></p></th>
<th><p><span data-ttu-id="6f7b8-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="6f7b8-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6f7b8-108"><strong><a href="relation-createfield-method-dao.md">CreateField</a></strong></span><span class="sxs-lookup"><span data-stu-id="6f7b8-108"><strong><a href="relation-createfield-method-dao.md">CreateField</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6f7b8-109">Cria um novo objeto <strong><a href="field-object-dao.md">Field</a></strong> (apenas espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="6f7b8-109">Creates a new <strong><a href="field-object-dao.md">Field</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="6f7b8-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6f7b8-110">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6f7b8-111">Nome</span><span class="sxs-lookup"><span data-stu-id="6f7b8-111">Name</span></span></p></th>
<th><p><span data-ttu-id="6f7b8-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="6f7b8-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6f7b8-113"><strong><a href="relation-attributes-property-dao.md">Atributos</a></strong></span><span class="sxs-lookup"><span data-stu-id="6f7b8-113"><strong><a href="relation-attributes-property-dao.md">Attributes</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6f7b8-114">Define ou retorna um valor que indica uma ou várias características de um objeto <strong>Relation</strong>.</span><span class="sxs-lookup"><span data-stu-id="6f7b8-114">Sets or returns a value that indicates one or more characteristics of a <strong>Relation</strong> object.</span></span> <span data-ttu-id="6f7b8-115"><strong>Long</strong> de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="6f7b8-115">Read/write <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f7b8-116"><strong><a href="relation-fields-property-dao.md">Fields</a></strong></span><span class="sxs-lookup"><span data-stu-id="6f7b8-116"><strong><a href="relation-fields-property-dao.md">Fields</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6f7b8-117">Retorna uma coleção <strong>Fields</strong> que representa todos os objetos <strong>Field</strong> armazenados para o objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="6f7b8-117">Returns a <strong>Fields</strong> collection that represents all stored <strong>Field</strong> objects for the specified object.</span></span> <span data-ttu-id="6f7b8-118">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="6f7b8-118">Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f7b8-119"><strong><a href="relation-foreigntable-property-dao.md">ForeignTable</a></strong></span><span class="sxs-lookup"><span data-stu-id="6f7b8-119"><strong><a href="relation-foreigntable-property-dao.md">ForeignTable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6f7b8-120">Define ou retorna o nome da tabela externa em uma relação (apenas espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="6f7b8-120">Sets or returns the name of the foreign table in a relationship (Microsoft Access workspaces only).</span></span> <span data-ttu-id="6f7b8-121">.</span><span class="sxs-lookup"><span data-stu-id="6f7b8-121">.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f7b8-122"><strong><a href="relation-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="6f7b8-122"><strong><a href="relation-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6f7b8-p104">Retorna ou define o nome do objeto especificado. <strong>String</strong> de leitura/gravação se o objeto não foi acrescentado a uma coleção. <strong>String</strong> somente leitura se o objeto foi acrescentado a uma coleção.</span><span class="sxs-lookup"><span data-stu-id="6f7b8-p104">Returns or sets the name of the specified object. Read/write <strong>String</strong> if the object has not been appended to a collection. Read-only <strong>String</strong> if the object has been appended to a collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f7b8-126"><strong><a href="relation-partialreplica-property-dao.md">PartialReplica</a></strong></span><span class="sxs-lookup"><span data-stu-id="6f7b8-126"><strong><a href="relation-partialreplica-property-dao.md">PartialReplica</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6f7b8-p105">Define ou retorna um valor em um objeto <strong>Relation</strong>, indicando se essa relação deverá ser considerada durante o preenchimento de uma réplica parcial a partir de uma réplica completa. (somente em banco de dados do mecanismo de banco de dados do Microsoft Access). <strong>Boolean</strong> de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="6f7b8-p105">Sets or returns a value on a <strong>Relation</strong> object indicating whether that relation should be considered when populating a partial replica from a full replica. (Microsoft Access database engine databases only). Read/write <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f7b8-130"><strong><a href="relation-properties-property-dao.md">Properties</a></strong></span><span class="sxs-lookup"><span data-stu-id="6f7b8-130"><strong><a href="relation-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6f7b8-131">Retorna a coleção <strong><a href="properties-collection-dao.md">Properties</a></strong> do objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="6f7b8-131">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object.</span></span> <span data-ttu-id="6f7b8-132">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="6f7b8-132">Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f7b8-133"><strong><a href="relation-table-property-dao.md">Table</a></strong></span><span class="sxs-lookup"><span data-stu-id="6f7b8-133"><strong><a href="relation-table-property-dao.md">Table</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6f7b8-p107">Indica o nome de uma tabela primária do objeto <strong><a href="relation-object-dao.md">Relation</a></strong>. Isso deve ser igual à definição da propriedade <strong><a href="connection-name-property-dao.md">Name</a></strong> de um objeto <strong><a href="tabledef-object-dao.md">TableDef</a></strong> ou <strong><a href="querydef-object-dao.md">QueryDef</a></strong> (somente em espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="6f7b8-p107">Indicates the name of a <strong><a href="relation-object-dao.md">Relation</a></strong> object's primary table. This should be equal to the <strong><a href="connection-name-property-dao.md">Name</a></strong> property setting of a <strong><a href="tabledef-object-dao.md">TableDef</a></strong> or <strong><a href="querydef-object-dao.md">QueryDef</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>

