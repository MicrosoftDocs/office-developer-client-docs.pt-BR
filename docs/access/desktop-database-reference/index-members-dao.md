---
title: Membros index (DAO)
TOCTitle: Index Members
ms:assetid: e261c5fa-ca7d-0d63-1c29-48e9231b39d1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835712(v=office.15)
ms:contentKeyID: 48548290
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 895f29a5dd3e7ed267b96d6a46dc2c8710b4998e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291793"
---
# <a name="index-members-dao"></a><span data-ttu-id="cc5f2-102">Membros index (DAO)</span><span class="sxs-lookup"><span data-stu-id="cc5f2-102">Index members (DAO)</span></span>


<span data-ttu-id="cc5f2-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cc5f2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cc5f2-p101">Os objetos Index especificam a ordem dos registros acessados a partir de tabelas de banco de dados e se registros duplicados são aceitos, fornecendo acesso eficiente aos dados. Para bancos de dados externos, os objetos Index descrevem os índices estabelecidos para tabelas externas (apenas espaços de trabalho do Microsoft Access ).</span><span class="sxs-lookup"><span data-stu-id="cc5f2-p101">Index objects specify the order of records accessed from database tables and whether or not duplicate records are accepted, providing efficient access to data. For external databases, Index objects describe the indexes established for external tables (Microsoft Access workspaces only).</span></span>

## <a name="methods"></a><span data-ttu-id="cc5f2-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="cc5f2-106">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cc5f2-107">Nome</span><span class="sxs-lookup"><span data-stu-id="cc5f2-107">Name</span></span></p></th>
<th><p><span data-ttu-id="cc5f2-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="cc5f2-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cc5f2-109"><strong><a href="index-createfield-method-dao.md">CreateField</a></strong></span><span class="sxs-lookup"><span data-stu-id="cc5f2-109"><strong><a href="index-createfield-method-dao.md">CreateField</a></strong></span></span></p></td>
<td><p><span data-ttu-id="cc5f2-110">Cria um novo objeto <strong><a href="field-object-dao.md">Field</a></strong> (apenas espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="cc5f2-110">Creates a new <strong><a href="field-object-dao.md">Field</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc5f2-111"><strong><a href="index-createproperty-method-dao.md">CreateProperty</a></strong></span><span class="sxs-lookup"><span data-stu-id="cc5f2-111"><strong><a href="index-createproperty-method-dao.md">CreateProperty</a></strong></span></span></p></td>
<td><p><span data-ttu-id="cc5f2-112">Cria um novo objeto <strong><a href="property-object-dao.md">Property</a></strong> definido pelo usuário (apenas espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="cc5f2-112">Creates a new user-defined <strong><a href="property-object-dao.md">Property</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="cc5f2-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cc5f2-113">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cc5f2-114">Nome</span><span class="sxs-lookup"><span data-stu-id="cc5f2-114">Name</span></span></p></th>
<th><p><span data-ttu-id="cc5f2-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="cc5f2-115">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cc5f2-116"><strong><a href="index-clustered-property-dao.md">Clustered</a></strong></span><span class="sxs-lookup"><span data-stu-id="cc5f2-116"><strong><a href="index-clustered-property-dao.md">Clustered</a></strong></span></span></p></td>
<td><p><span data-ttu-id="cc5f2-p102">Define ou retorna um valor que indica se um objeto <strong>Index</strong> representa um índice agrupado para uma tabela (apenas espaços de trabalho do Microsoft Access). <strong>Boolean</strong> de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="cc5f2-p102">Sets or returns a value that indicates whether an <strong>Index</strong> object represents a clustered index for a table (Microsoft Access workspaces only). Read/write <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc5f2-119"><strong><a href="index-distinctcount-property-dao.md">DistinctCount</a></strong></span><span class="sxs-lookup"><span data-stu-id="cc5f2-119"><strong><a href="index-distinctcount-property-dao.md">DistinctCount</a></strong></span></span></p></td>
<td><p><span data-ttu-id="cc5f2-120">Retorna um valor que indica o número de valores exclusivos para o objeto <strong><a href="index-object-dao.md">Index</a></strong> que estão incluídos na tabela associada (apenas espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="cc5f2-120">Returns a value that indicates the number of unique values for the <strong><a href="index-object-dao.md">Index</a></strong> object that are included in the associated table (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc5f2-121"><strong><a href="index-fields-property-dao.md">Fields</a></strong></span><span class="sxs-lookup"><span data-stu-id="cc5f2-121"><strong><a href="index-fields-property-dao.md">Fields</a></strong></span></span></p></td>
<td><p><span data-ttu-id="cc5f2-122">Retorna uma coleção <strong>Fields</strong> que representa todos os objetos <strong>Field</strong> armazenados para o objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="cc5f2-122">Returns a <strong>Fields</strong> collection that represents all stored <strong>Field</strong> objects for the specified object.</span></span> <span data-ttu-id="cc5f2-123">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="cc5f2-123">Read/write.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc5f2-124"><strong><a href="index-foreign-property-dao.md">Externo</a></strong></span><span class="sxs-lookup"><span data-stu-id="cc5f2-124"><strong><a href="index-foreign-property-dao.md">Foreign</a></strong></span></span></p></td>
<td><p><span data-ttu-id="cc5f2-125">Retorna um valor que indica se um objeto <strong><a href="index-object-dao.md">Index</a></strong> representa uma chave estrangeira em uma tabela (apenas espaços de trabalho Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="cc5f2-125">Returns a value that indicates whether an <strong><a href="index-object-dao.md">Index</a></strong> object represents a foreign key in a table (Microsoft Access workspaces only).</span></span> <span data-ttu-id="cc5f2-126">.</span><span class="sxs-lookup"><span data-stu-id="cc5f2-126">.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc5f2-127"><strong><a href="index-ignorenulls-property-dao.md">IgnoreNulls</a></strong></span><span class="sxs-lookup"><span data-stu-id="cc5f2-127"><strong><a href="index-ignorenulls-property-dao.md">IgnoreNulls</a></strong></span></span></p></td>
<td><p><span data-ttu-id="cc5f2-128">Define ou retorna um valor que indica se os registros com valores Null nos campos de índice têm entradas de índice (somente nos espaços de trabalho do Microsoft Access ).</span><span class="sxs-lookup"><span data-stu-id="cc5f2-128">Sets or returns a value that indicates whether records that have Null values in their index fields have index entries (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc5f2-129"><strong><a href="index-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="cc5f2-129"><strong><a href="index-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="cc5f2-p105">Retorna ou define o nome do objeto especificado. <strong>String</strong> de leitura/gravação se o objeto não foi acrescentado a uma coleção. <strong>String</strong> somente leitura se o objeto foi acrescentado a uma coleção.</span><span class="sxs-lookup"><span data-stu-id="cc5f2-p105">Returns or sets the name of the specified object. Read/write <strong>String</strong> if the object has not been appended to a collection. Read-only <strong>String</strong> if the object has been appended to a collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc5f2-133"><strong><a href="index-primary-property-dao.md">Primário</a></strong></span><span class="sxs-lookup"><span data-stu-id="cc5f2-133"><strong><a href="index-primary-property-dao.md">Primary</a></strong></span></span></p></td>
<td><p><span data-ttu-id="cc5f2-134">Define ou retorna um valor que indica se um objeto <strong><a href="index-object-dao.md">Index</a></strong> representa um índice de chave primária de uma tabela (somente em espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="cc5f2-134">Sets or returns a value that indicates whether an <strong><a href="index-object-dao.md">Index</a></strong> object represents a primary key index for a table (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc5f2-135"><strong><a href="index-properties-property-dao.md">Properties</a></strong></span><span class="sxs-lookup"><span data-stu-id="cc5f2-135"><strong><a href="index-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="cc5f2-136">Retorna a coleção <strong><a href="properties-collection-dao.md">Properties</a></strong> do objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="cc5f2-136">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object.</span></span> <span data-ttu-id="cc5f2-137">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="cc5f2-137">Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc5f2-138"><strong><a href="index-required-property-dao.md">Obrigatório</a></strong></span><span class="sxs-lookup"><span data-stu-id="cc5f2-138"><strong><a href="index-required-property-dao.md">Required</a></strong></span></span></p></td>
<td><p><span data-ttu-id="cc5f2-139">Define ou retorna um valor que indica se um objeto <strong><a href="field-object-dao.md">Field</a></strong> requer um valor não Null.</span><span class="sxs-lookup"><span data-stu-id="cc5f2-139">Sets or returns a value that indicates whether a <strong><a href="field-object-dao.md">Field</a></strong> object requires a non-Null value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc5f2-140"><strong><a href="index-unique-property-dao.md">Exclusivo</a></strong></span><span class="sxs-lookup"><span data-stu-id="cc5f2-140"><strong><a href="index-unique-property-dao.md">Unique</a></strong></span></span></p></td>
<td><p><span data-ttu-id="cc5f2-141">Define ou retorna um valor que indica se objeto <strong><a href="index-object-dao.md">Index</a></strong> representa um índice (chave) exclusivo para uma tabela (somente em espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="cc5f2-141">Sets or returns a value that indicates whether an <strong><a href="index-object-dao.md">Index</a></strong> object represents a unique (key) index for a table (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>

