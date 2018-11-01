---
title: Enumeração RelationAttributeEnum (DAO)
TOCTitle: RelationAttributeEnum Enumeration
ms:assetid: ce8d0696-66d7-052f-1313-64baee3442ed
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834499(v=office.15)
ms:contentKeyID: 48547787
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bdb1af980d272f24c5803af9cfba0140dba8b05e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874598"
---
# <a name="relationattributeenum-enumeration-dao"></a><span data-ttu-id="31a3b-102">Enumeração RelationAttributeEnum (DAO)</span><span class="sxs-lookup"><span data-stu-id="31a3b-102">RelationAttributeEnum Enumeration (DAO)</span></span>


<span data-ttu-id="31a3b-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="31a3b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="31a3b-104">Usada com a propriedade **Attributes** para determinar os atributos de um objeto **Relation**.</span><span class="sxs-lookup"><span data-stu-id="31a3b-104">Used with the **Attributes** property to determine attributes of a **Relation** object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="31a3b-105">Nome</span><span class="sxs-lookup"><span data-stu-id="31a3b-105">Name</span></span></p></th>
<th><p><span data-ttu-id="31a3b-106">Valor</span><span class="sxs-lookup"><span data-stu-id="31a3b-106">Value</span></span></p></th>
<th><p><span data-ttu-id="31a3b-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="31a3b-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="31a3b-108">dbRelationDeleteCascade</span><span class="sxs-lookup"><span data-stu-id="31a3b-108">dbRelationDeleteCascade</span></span></p></td>
<td><p><span data-ttu-id="31a3b-109">4096</span><span class="sxs-lookup"><span data-stu-id="31a3b-109">4096</span></span></p></td>
<td><p><span data-ttu-id="31a3b-110">Exclusões em cascata</span><span class="sxs-lookup"><span data-stu-id="31a3b-110">Deletions cascade</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31a3b-111">dbRelationDontEnforce</span><span class="sxs-lookup"><span data-stu-id="31a3b-111">dbRelationDontEnforce</span></span></p></td>
<td><p><span data-ttu-id="31a3b-112">2</span><span class="sxs-lookup"><span data-stu-id="31a3b-112">2</span></span></p></td>
<td><p><span data-ttu-id="31a3b-113">Relação não imposta (nenhuma integridade referencial)</span><span class="sxs-lookup"><span data-stu-id="31a3b-113">Relationship not enforced (no referential integrity)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31a3b-114">dbRelationInherited</span><span class="sxs-lookup"><span data-stu-id="31a3b-114">dbRelationInherited</span></span></p></td>
<td><p><span data-ttu-id="31a3b-115">4</span><span class="sxs-lookup"><span data-stu-id="31a3b-115">4</span></span></p></td>
<td><p><span data-ttu-id="31a3b-116">Existe relação no banco de dados que contém as duas tabelas vinculadas</span><span class="sxs-lookup"><span data-stu-id="31a3b-116">Relationship exists in the database containing the two linked tables</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31a3b-117">dbRelationLeft</span><span class="sxs-lookup"><span data-stu-id="31a3b-117">dbRelationLeft</span></span></p></td>
<td><p><span data-ttu-id="31a3b-118">16777216</span><span class="sxs-lookup"><span data-stu-id="31a3b-118">16777216</span></span></p></td>
<td><p><span data-ttu-id="31a3b-p101">Somente no Microsoft Access. No modo Design, exibe LEFT JOIN como o tipo de junção padrão.</span><span class="sxs-lookup"><span data-stu-id="31a3b-p101">Microsoft Access only. In Design view, display a LEFT JOIN as the default join type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31a3b-121">dbRelationRight</span><span class="sxs-lookup"><span data-stu-id="31a3b-121">dbRelationRight</span></span></p></td>
<td><p><span data-ttu-id="31a3b-122">33554432</span><span class="sxs-lookup"><span data-stu-id="31a3b-122">33554432</span></span></p></td>
<td><p><span data-ttu-id="31a3b-p102">Somente no Microsoft Access. No modo Design, exibe RIGHT JOIN como o tipo de junção padrão.</span><span class="sxs-lookup"><span data-stu-id="31a3b-p102">Microsoft Access only. In Design view, display a RIGHT JOIN as the default join type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31a3b-125">dbRelationUnique</span><span class="sxs-lookup"><span data-stu-id="31a3b-125">dbRelationUnique</span></span></p></td>
<td><p><span data-ttu-id="31a3b-126">1</span><span class="sxs-lookup"><span data-stu-id="31a3b-126">1</span></span></p></td>
<td><p><span data-ttu-id="31a3b-127">Relação um-para-um</span><span class="sxs-lookup"><span data-stu-id="31a3b-127">One-to-one relationship</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31a3b-128">dbRelationUpdateCascade</span><span class="sxs-lookup"><span data-stu-id="31a3b-128">dbRelationUpdateCascade</span></span></p></td>
<td><p><span data-ttu-id="31a3b-129">256</span><span class="sxs-lookup"><span data-stu-id="31a3b-129">256</span></span></p></td>
<td><p><span data-ttu-id="31a3b-130">Atualizações em cascata</span><span class="sxs-lookup"><span data-stu-id="31a3b-130">Updates cascade</span></span></p></td>
</tr>
</tbody>
</table>

