---
title: Membros de Relation (DAO)
TOCTitle: Relation Members
ms:assetid: 9ee36e7d-3825-1de8-65fb-64bbcada847c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198338(v=office.15)
ms:contentKeyID: 48546670
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8d4b1b1a3a06d0605793667f8c9258ea5b6336f5
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923725"
---
# <a name="relation-members-dao"></a><span data-ttu-id="8a9bb-102">Membros de Relation (DAO)</span><span class="sxs-lookup"><span data-stu-id="8a9bb-102">Relation members (DAO)</span></span>


<span data-ttu-id="8a9bb-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="8a9bb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8a9bb-104">Um objeto Relation representa uma relação entre campos nas tabelas ou consultas (apenas bancos de dados do mecanismo de banco de dados do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="8a9bb-104">A Relation object represents a relationship between fields in tables or queries (Microsoft Access database engine databases only).</span></span>

## <a name="methods"></a><span data-ttu-id="8a9bb-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="8a9bb-105">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8a9bb-106">Nome</span><span class="sxs-lookup"><span data-stu-id="8a9bb-106">Name</span></span></p></th>
<th><p><span data-ttu-id="8a9bb-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="8a9bb-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8a9bb-108"><strong><a href="relation-createfield-method-dao.md">CreateField</a></strong></span><span class="sxs-lookup"><span data-stu-id="8a9bb-108"><strong><a href="relation-createfield-method-dao.md">CreateField</a></strong></span></span></p></td>
<td><p><span data-ttu-id="8a9bb-109">Cria um novo objeto <strong><a href="field-object-dao.md">Field</a></strong> (espaços de trabalho do Microsoft Access apenas).</span><span class="sxs-lookup"><span data-stu-id="8a9bb-109">Creates a new <strong><a href="field-object-dao.md">Field</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="8a9bb-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8a9bb-110">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8a9bb-111">Nome</span><span class="sxs-lookup"><span data-stu-id="8a9bb-111">Name</span></span></p></th>
<th><p><span data-ttu-id="8a9bb-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="8a9bb-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8a9bb-113"><strong><a href="relation-attributes-property-dao.md">Atributos</a></strong></span><span class="sxs-lookup"><span data-stu-id="8a9bb-113"><strong><a href="relation-attributes-property-dao.md">Attributes</a></strong></span></span></p></td>
<td><p><span data-ttu-id="8a9bb-p101">Define ou retorna um valor que indica uma ou várias características de um objeto <strong>Relation</strong>. <strong>Long</strong> de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="8a9bb-p101">Sets or returns a value that indicates one or more characteristics of a <strong>Relation</strong> object. Read/write <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8a9bb-116"><strong><a href="relation-fields-property-dao.md">Fields</a></strong></span><span class="sxs-lookup"><span data-stu-id="8a9bb-116"><strong><a href="relation-fields-property-dao.md">Fields</a></strong></span></span></p></td>
<td><p><span data-ttu-id="8a9bb-p102">Retorna uma coleção <strong>Fields</strong> que representa todos os objetos <strong>Field</strong> armazenados para o objeto especificado. Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="8a9bb-p102">Returns a <strong>Fields</strong> collection that represents all stored <strong>Field</strong> objects for the specified object. Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8a9bb-119"><strong><a href="relation-foreigntable-property-dao.md">ForeignTable</a></strong></span><span class="sxs-lookup"><span data-stu-id="8a9bb-119"><strong><a href="relation-foreigntable-property-dao.md">ForeignTable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="8a9bb-p103">Define ou retorna o nome da tabela externa em uma relação (apenas espaços de trabalho do Microsoft Access). .</span><span class="sxs-lookup"><span data-stu-id="8a9bb-p103">Sets or returns the name of the foreign table in a relationship (Microsoft Access workspaces only). .</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8a9bb-122"><strong><a href="relation-name-property-dao.md">Nome</a></strong></span><span class="sxs-lookup"><span data-stu-id="8a9bb-122"><strong><a href="relation-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="8a9bb-p104">Retorna ou define o nome do objeto especificado. <strong>String</strong> de leitura/gravação se o objeto não foi acrescentado a uma coleção. <strong>String</strong> somente leitura se o objeto foi acrescentado a uma coleção.</span><span class="sxs-lookup"><span data-stu-id="8a9bb-p104">Returns or sets the name of the specified object. Read/write <strong>String</strong> if the object has not been appended to a collection. Read-only <strong>String</strong> if the object has been appended to a collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8a9bb-126"><strong><a href="relation-partialreplica-property-dao.md">PartialReplica</a></strong></span><span class="sxs-lookup"><span data-stu-id="8a9bb-126"><strong><a href="relation-partialreplica-property-dao.md">PartialReplica</a></strong></span></span></p></td>
<td><p><span data-ttu-id="8a9bb-p105">Define ou retorna um valor em um objeto <strong>Relation</strong>, indicando se essa relação deverá ser considerada durante o preenchimento de uma réplica parcial a partir de uma réplica completa. (somente em banco de dados do mecanismo de banco de dados do Microsoft Access). <strong>Boolean</strong> de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="8a9bb-p105">Sets or returns a value on a <strong>Relation</strong> object indicating whether that relation should be considered when populating a partial replica from a full replica. (Microsoft Access database engine databases only). Read/write <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8a9bb-130"><strong><a href="relation-properties-property-dao.md">Propriedades</a></strong></span><span class="sxs-lookup"><span data-stu-id="8a9bb-130"><strong><a href="relation-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="8a9bb-p106">Retorna a coleção <strong><a href="properties-collection-dao.md">Properties</a></strong> do objeto especificado. Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="8a9bb-p106">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object. Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8a9bb-133"><strong><a href="relation-table-property-dao.md">Tabela</a></strong></span><span class="sxs-lookup"><span data-stu-id="8a9bb-133"><strong><a href="relation-table-property-dao.md">Table</a></strong></span></span></p></td>
<td><p><span data-ttu-id="8a9bb-p107">Indica o nome de uma tabela primária do objeto <strong><a href="relation-object-dao.md">Relation</a></strong>. Isso deve ser igual à definição da propriedade <strong><a href="connection-name-property-dao.md">Name</a></strong> de um objeto <strong><a href="tabledef-object-dao.md">TableDef</a></strong> ou <strong><a href="querydef-object-dao.md">QueryDef</a></strong> (somente em espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="8a9bb-p107">Indicates the name of a <strong><a href="relation-object-dao.md">Relation</a></strong> object's primary table. This should be equal to the <strong><a href="connection-name-property-dao.md">Name</a></strong> property setting of a <strong><a href="tabledef-object-dao.md">TableDef</a></strong> or <strong><a href="querydef-object-dao.md">QueryDef</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>

