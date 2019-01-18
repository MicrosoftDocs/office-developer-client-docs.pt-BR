---
title: Membros de índice (DAO)
TOCTitle: Index Members
ms:assetid: e261c5fa-ca7d-0d63-1c29-48e9231b39d1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835712(v=office.15)
ms:contentKeyID: 48548290
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 895f29a5dd3e7ed267b96d6a46dc2c8710b4998e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709156"
---
# <a name="index-members-dao"></a><span data-ttu-id="a42b5-102">Membros de índice (DAO)</span><span class="sxs-lookup"><span data-stu-id="a42b5-102">Index members (DAO)</span></span>


<span data-ttu-id="a42b5-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="a42b5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a42b5-p101">Os objetos Index especificam a ordem dos registros acessados a partir de tabelas de banco de dados e se registros duplicados são aceitos, fornecendo acesso eficiente aos dados. Para bancos de dados externos, os objetos Index descrevem os índices estabelecidos para tabelas externas (apenas espaços de trabalho do Microsoft Access ).</span><span class="sxs-lookup"><span data-stu-id="a42b5-p101">Index objects specify the order of records accessed from database tables and whether or not duplicate records are accepted, providing efficient access to data. For external databases, Index objects describe the indexes established for external tables (Microsoft Access workspaces only).</span></span>

## <a name="methods"></a><span data-ttu-id="a42b5-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="a42b5-106">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a42b5-107">Nome</span><span class="sxs-lookup"><span data-stu-id="a42b5-107">Name</span></span></p></th>
<th><p><span data-ttu-id="a42b5-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="a42b5-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a42b5-109"><strong><a href="index-createfield-method-dao.md">CreateField</a></strong></span><span class="sxs-lookup"><span data-stu-id="a42b5-109"><strong><a href="index-createfield-method-dao.md">CreateField</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a42b5-110">Cria um novo objeto <strong><a href="field-object-dao.md">Field</a></strong> (espaços de trabalho do Microsoft Access apenas).</span><span class="sxs-lookup"><span data-stu-id="a42b5-110">Creates a new <strong><a href="field-object-dao.md">Field</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a42b5-111"><strong><a href="index-createproperty-method-dao.md">CreateProperty</a></strong></span><span class="sxs-lookup"><span data-stu-id="a42b5-111"><strong><a href="index-createproperty-method-dao.md">CreateProperty</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a42b5-112">Cria um novo objeto <strong><a href="property-object-dao.md">Property</a></strong> definido pelo usuário (somente espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="a42b5-112">Creates a new user-defined <strong><a href="property-object-dao.md">Property</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="a42b5-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a42b5-113">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a42b5-114">Nome</span><span class="sxs-lookup"><span data-stu-id="a42b5-114">Name</span></span></p></th>
<th><p><span data-ttu-id="a42b5-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="a42b5-115">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a42b5-116"><strong><a href="index-clustered-property-dao.md">Clustered</a></strong></span><span class="sxs-lookup"><span data-stu-id="a42b5-116"><strong><a href="index-clustered-property-dao.md">Clustered</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a42b5-p102">Define ou retorna um valor que indica se um objeto <strong>Index</strong> representa um índice agrupado para uma tabela (apenas espaços de trabalho do Microsoft Access). <strong>Boolean</strong> de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="a42b5-p102">Sets or returns a value that indicates whether an <strong>Index</strong> object represents a clustered index for a table (Microsoft Access workspaces only). Read/write <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a42b5-119"><strong><a href="index-distinctcount-property-dao.md">DistinctCount</a></strong></span><span class="sxs-lookup"><span data-stu-id="a42b5-119"><strong><a href="index-distinctcount-property-dao.md">DistinctCount</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a42b5-120">Retorna um valor que indica o número de valores exclusivos para o objeto <strong><a href="index-object-dao.md">Index</a></strong> que estão incluídos na tabela associada (apenas espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="a42b5-120">Returns a value that indicates the number of unique values for the <strong><a href="index-object-dao.md">Index</a></strong> object that are included in the associated table (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a42b5-121"><strong><a href="index-fields-property-dao.md">Fields</a></strong></span><span class="sxs-lookup"><span data-stu-id="a42b5-121"><strong><a href="index-fields-property-dao.md">Fields</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a42b5-p103">Retorna uma coleção <strong>Fields</strong> que representa todos os objetos <strong>Field</strong> armazenados para o objeto especificado. Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="a42b5-p103">Returns a <strong>Fields</strong> collection that represents all stored <strong>Field</strong> objects for the specified object. Read/write.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a42b5-124"><strong><a href="index-foreign-property-dao.md">Foreign</a></strong></span><span class="sxs-lookup"><span data-stu-id="a42b5-124"><strong><a href="index-foreign-property-dao.md">Foreign</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a42b5-p104">Retorna um valor que indica se um objeto <strong><a href="index-object-dao.md">Index</a></strong> representa uma chave estrangeira em uma tabela (apenas espaços de trabalho Microsoft Access). .</span><span class="sxs-lookup"><span data-stu-id="a42b5-p104">Returns a value that indicates whether an <strong><a href="index-object-dao.md">Index</a></strong> object represents a foreign key in a table (Microsoft Access workspaces only). .</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a42b5-127"><strong><a href="index-ignorenulls-property-dao.md">IgnoreNulls</a></strong></span><span class="sxs-lookup"><span data-stu-id="a42b5-127"><strong><a href="index-ignorenulls-property-dao.md">IgnoreNulls</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a42b5-128">Define ou retorna um valor que indica se os registros com valores Null nos campos de índice têm entradas de índice (somente nos espaços de trabalho do Microsoft Access ).</span><span class="sxs-lookup"><span data-stu-id="a42b5-128">Sets or returns a value that indicates whether records that have Null values in their index fields have index entries (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a42b5-129"><strong><a href="index-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="a42b5-129"><strong><a href="index-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a42b5-p105">Retorna ou define o nome do objeto especificado. <strong>String</strong> de leitura/gravação se o objeto não foi acrescentado a uma coleção. <strong>String</strong> somente leitura se o objeto foi acrescentado a uma coleção.</span><span class="sxs-lookup"><span data-stu-id="a42b5-p105">Returns or sets the name of the specified object. Read/write <strong>String</strong> if the object has not been appended to a collection. Read-only <strong>String</strong> if the object has been appended to a collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a42b5-133"><strong><a href="index-primary-property-dao.md">Primary</a></strong></span><span class="sxs-lookup"><span data-stu-id="a42b5-133"><strong><a href="index-primary-property-dao.md">Primary</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a42b5-134">Define ou retorna um valor que indica se um objeto <strong><a href="index-object-dao.md">Index</a></strong> representa um índice de chave primária de uma tabela (somente em espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="a42b5-134">Sets or returns a value that indicates whether an <strong><a href="index-object-dao.md">Index</a></strong> object represents a primary key index for a table (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a42b5-135"><strong><a href="index-properties-property-dao.md">Propriedades</a></strong></span><span class="sxs-lookup"><span data-stu-id="a42b5-135"><strong><a href="index-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a42b5-p106">Retorna a coleção <strong><a href="properties-collection-dao.md">Properties</a></strong> do objeto especificado. Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="a42b5-p106">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object. Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a42b5-138"><strong><a href="index-required-property-dao.md">Necessário</a></strong></span><span class="sxs-lookup"><span data-stu-id="a42b5-138"><strong><a href="index-required-property-dao.md">Required</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a42b5-139">Define ou retorna um valor que indica se um objeto <strong><a href="field-object-dao.md">Field</a></strong> requer um valor não Null.</span><span class="sxs-lookup"><span data-stu-id="a42b5-139">Sets or returns a value that indicates whether a <strong><a href="field-object-dao.md">Field</a></strong> object requires a non-Null value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a42b5-140"><strong><a href="index-unique-property-dao.md">Unique</a></strong></span><span class="sxs-lookup"><span data-stu-id="a42b5-140"><strong><a href="index-unique-property-dao.md">Unique</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a42b5-141">Define ou retorna um valor que indica se objeto <strong><a href="index-object-dao.md">Index</a></strong> representa um índice (chave) exclusivo para uma tabela (somente em espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="a42b5-141">Sets or returns a value that indicates whether an <strong><a href="index-object-dao.md">Index</a></strong> object represents a unique (key) index for a table (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>

