---
title: Membros do documento (DAO)
TOCTitle: Document Members
ms:assetid: 8de770e6-e4d1-372a-3ef8-8539c921b41f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197365(v=office.15)
ms:contentKeyID: 48546270
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cd50ec72113b0615849ff6b8b2e8d73c0e61c3ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293788"
---
# <a name="document-members-dao"></a><span data-ttu-id="09a13-102">Membros do documento (DAO)</span><span class="sxs-lookup"><span data-stu-id="09a13-102">Document members (DAO)</span></span>


<span data-ttu-id="09a13-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="09a13-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="09a13-p101">O objeto Document inclui informações sobre uma instância de um objeto. O objeto pode ser um banco de dados, uma tabela, uma consulta ou uma relação salva (apenas bancos de dados do mecanismo de banco de dados do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="09a13-p101">A Document object includes information about one instance of an object. The object can be a database, saved table, query, or relationship (Microsoft Access database engine databases only).</span></span>

## <a name="methods"></a><span data-ttu-id="09a13-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="09a13-106">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="09a13-107">Nome</span><span class="sxs-lookup"><span data-stu-id="09a13-107">Name</span></span></p></th>
<th><p><span data-ttu-id="09a13-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="09a13-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="09a13-109"><strong><a href="document-createproperty-method-dao.md">CreateProperty</a></strong></span><span class="sxs-lookup"><span data-stu-id="09a13-109"><strong><a href="document-createproperty-method-dao.md">CreateProperty</a></strong></span></span></p></td>
<td><p><span data-ttu-id="09a13-110">Cria um novo objeto <strong><a href="property-object-dao.md">Property</a></strong> definido pelo usuário (apenas espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="09a13-110">Creates a new user-defined <strong><a href="property-object-dao.md">Property</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="09a13-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="09a13-111">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="09a13-112">Nome</span><span class="sxs-lookup"><span data-stu-id="09a13-112">Name</span></span></p></th>
<th><p><span data-ttu-id="09a13-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="09a13-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="09a13-114"><strong><a href="document-container-property-dao.md">Contêiner</a></strong></span><span class="sxs-lookup"><span data-stu-id="09a13-114"><strong><a href="document-container-property-dao.md">Container</a></strong></span></span></p></td>
<td><p><span data-ttu-id="09a13-115">Retorna o nome do objeto <strong><a href="container-object-dao.md">Container</a></strong> ao qual um objeto <strong>Document</strong> pertence (apenas espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="09a13-115">Returns the name of the <strong><a href="container-object-dao.md">Container</a></strong> object to which a <strong>Document</strong> object belongs (Microsoft Access workspaces only).</span></span> <span data-ttu-id="09a13-116">.</span><span class="sxs-lookup"><span data-stu-id="09a13-116">.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09a13-117"><strong><a href="document-datecreated-property-dao.md">DateCreated</a></strong></span><span class="sxs-lookup"><span data-stu-id="09a13-117"><strong><a href="document-datecreated-property-dao.md">DateCreated</a></strong></span></span></p></td>
<td><p><span data-ttu-id="09a13-118">Retorna a data e a hora que um objeto foi criado.</span><span class="sxs-lookup"><span data-stu-id="09a13-118">Returns the date and time that an object was created.</span></span> <span data-ttu-id="09a13-119"><strong>Variant</strong> somente leitura.</span><span class="sxs-lookup"><span data-stu-id="09a13-119">Read-only <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09a13-120"><strong><a href="document-lastupdated-property-dao.md">LastUpdated</a></strong></span><span class="sxs-lookup"><span data-stu-id="09a13-120"><strong><a href="document-lastupdated-property-dao.md">LastUpdated</a></strong></span></span></p></td>
<td><p><span data-ttu-id="09a13-121">Retorna a data e a hora da alteração mais recente feita em um objeto.</span><span class="sxs-lookup"><span data-stu-id="09a13-121">Returns the date and time of the most recent change made to an object.</span></span> <span data-ttu-id="09a13-122"><strong>Variant</strong> somente leitura.</span><span class="sxs-lookup"><span data-stu-id="09a13-122">Read-only <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09a13-123"><strong><a href="document-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="09a13-123"><strong><a href="document-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="09a13-124">Retorna o nome do objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="09a13-124">Returns the name of the specified object.</span></span> <span data-ttu-id="09a13-125"><strong>String</strong> somente leitura.</span><span class="sxs-lookup"><span data-stu-id="09a13-125">Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09a13-126"><strong><a href="document-properties-property-dao.md">Properties</a></strong></span><span class="sxs-lookup"><span data-stu-id="09a13-126"><strong><a href="document-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="09a13-127">Retorna a coleção <strong><a href="properties-collection-dao.md">Properties</a></strong> do objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="09a13-127">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object.</span></span> <span data-ttu-id="09a13-128">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="09a13-128">Read-only.</span></span></p></td>
</tr>
</tbody>
</table>

