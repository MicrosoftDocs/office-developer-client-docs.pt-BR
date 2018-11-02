---
title: Membros do documento (DAO)
TOCTitle: Document Members
ms:assetid: 8de770e6-e4d1-372a-3ef8-8539c921b41f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197365(v=office.15)
ms:contentKeyID: 48546270
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d21151b2a30ec44b717031f2b0b8a8f506f22193
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930417"
---
# <a name="document-members-dao"></a><span data-ttu-id="098ac-102">Membros do documento (DAO)</span><span class="sxs-lookup"><span data-stu-id="098ac-102">Document members (DAO)</span></span>


<span data-ttu-id="098ac-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="098ac-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="098ac-p101">O objeto Document inclui informações sobre uma instância de um objeto. O objeto pode ser um banco de dados, uma tabela, uma consulta ou uma relação salva (apenas bancos de dados do mecanismo de banco de dados do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="098ac-p101">A Document object includes information about one instance of an object. The object can be a database, saved table, query, or relationship (Microsoft Access database engine databases only).</span></span>

## <a name="methods"></a><span data-ttu-id="098ac-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="098ac-106">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="098ac-107">Nome</span><span class="sxs-lookup"><span data-stu-id="098ac-107">Name</span></span></p></th>
<th><p><span data-ttu-id="098ac-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="098ac-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="098ac-109"><strong><a href="document-createproperty-method-dao.md">CreateProperty</a></strong></span><span class="sxs-lookup"><span data-stu-id="098ac-109"><strong><a href="document-createproperty-method-dao.md">CreateProperty</a></strong></span></span></p></td>
<td><p><span data-ttu-id="098ac-110">Cria um novo objeto <strong><a href="property-object-dao.md">Property</a></strong> definido pelo usuário (somente espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="098ac-110">Creates a new user-defined <strong><a href="property-object-dao.md">Property</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="098ac-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="098ac-111">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="098ac-112">Nome</span><span class="sxs-lookup"><span data-stu-id="098ac-112">Name</span></span></p></th>
<th><p><span data-ttu-id="098ac-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="098ac-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="098ac-114"><strong><a href="document-container-property-dao.md">Container</a></strong></span><span class="sxs-lookup"><span data-stu-id="098ac-114"><strong><a href="document-container-property-dao.md">Container</a></strong></span></span></p></td>
<td><p><span data-ttu-id="098ac-p102">Retorna o nome do objeto <strong><a href="container-object-dao.md">Container</a></strong> ao qual um objeto <strong>Document</strong> pertence (apenas espaços de trabalho do Microsoft Access). .</span><span class="sxs-lookup"><span data-stu-id="098ac-p102">Returns the name of the <strong><a href="container-object-dao.md">Container</a></strong> object to which a <strong>Document</strong> object belongs (Microsoft Access workspaces only). .</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="098ac-117"><strong><a href="document-datecreated-property-dao.md">DateCreated</a></strong></span><span class="sxs-lookup"><span data-stu-id="098ac-117"><strong><a href="document-datecreated-property-dao.md">DateCreated</a></strong></span></span></p></td>
<td><p><span data-ttu-id="098ac-p103">Retorna a data e a hora que um objeto foi criado. <strong>Variant</strong> somente leitura.</span><span class="sxs-lookup"><span data-stu-id="098ac-p103">Returns the date and time that an object was created. Read-only <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="098ac-120"><strong><a href="document-lastupdated-property-dao.md">LastUpdated</a></strong></span><span class="sxs-lookup"><span data-stu-id="098ac-120"><strong><a href="document-lastupdated-property-dao.md">LastUpdated</a></strong></span></span></p></td>
<td><p><span data-ttu-id="098ac-p104">Retorna a data e a hora da alteração feita mais recentemente em um objeto. <strong>Variant</strong> somente leitura.</span><span class="sxs-lookup"><span data-stu-id="098ac-p104">Returns the date and time of the most recent change made to an object. Read-only <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="098ac-123"><strong><a href="document-name-property-dao.md">Nome</a></strong></span><span class="sxs-lookup"><span data-stu-id="098ac-123"><strong><a href="document-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="098ac-p105">Retorna o nome do objeto especificado. <strong>String</strong> somente leitura.</span><span class="sxs-lookup"><span data-stu-id="098ac-p105">Returns the name of the specified object. Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="098ac-126"><strong><a href="document-properties-property-dao.md">Propriedades</a></strong></span><span class="sxs-lookup"><span data-stu-id="098ac-126"><strong><a href="document-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="098ac-p106">Retorna a coleção <strong><a href="properties-collection-dao.md">Properties</a></strong> do objeto especificado. Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="098ac-p106">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object. Read-only.</span></span></p></td>
</tr>
</tbody>
</table>

