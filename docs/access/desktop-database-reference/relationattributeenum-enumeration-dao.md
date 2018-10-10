---
title: Enumeração RelationAttributeEnum (DAO)
TOCTitle: RelationAttributeEnum Enumeration
ms:assetid: ce8d0696-66d7-052f-1313-64baee3442ed
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834499(v=office.15)
ms:contentKeyID: 48547787
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4c4d7a2b622e382461bcf1b4171a5aa85f036854
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464698"
---
# <a name="relationattributeenum-enumeration-dao"></a><span data-ttu-id="3c266-102">Enumeração RelationAttributeEnum (DAO)</span><span class="sxs-lookup"><span data-stu-id="3c266-102">RelationAttributeEnum Enumeration (DAO)</span></span>


<span data-ttu-id="3c266-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3c266-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3c266-104">Usada com a propriedade **Attributes** para determinar os atributos de um objeto **Relation**.</span><span class="sxs-lookup"><span data-stu-id="3c266-104">Used with the **Attributes** property to determine attributes of a **Relation** object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3c266-105">Nome</span><span class="sxs-lookup"><span data-stu-id="3c266-105">Name</span></span></p></th>
<th><p><span data-ttu-id="3c266-106">Valor</span><span class="sxs-lookup"><span data-stu-id="3c266-106">Value</span></span></p></th>
<th><p><span data-ttu-id="3c266-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="3c266-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3c266-108">dbRelationDeleteCascade</span><span class="sxs-lookup"><span data-stu-id="3c266-108">dbRelationDeleteCascade</span></span></p></td>
<td><p><span data-ttu-id="3c266-109">4096</span><span class="sxs-lookup"><span data-stu-id="3c266-109">4096</span></span></p></td>
<td><p><span data-ttu-id="3c266-110">Exclusões em cascata</span><span class="sxs-lookup"><span data-stu-id="3c266-110">Deletions cascade</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c266-111">dbRelationDontEnforce</span><span class="sxs-lookup"><span data-stu-id="3c266-111">dbRelationDontEnforce</span></span></p></td>
<td><p><span data-ttu-id="3c266-112">2</span><span class="sxs-lookup"><span data-stu-id="3c266-112">2</span></span></p></td>
<td><p><span data-ttu-id="3c266-113">Relação não imposta (nenhuma integridade referencial)</span><span class="sxs-lookup"><span data-stu-id="3c266-113">Relationship not enforced (no referential integrity)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c266-114">dbRelationInherited</span><span class="sxs-lookup"><span data-stu-id="3c266-114">dbRelationInherited</span></span></p></td>
<td><p><span data-ttu-id="3c266-115">4</span><span class="sxs-lookup"><span data-stu-id="3c266-115">4</span></span></p></td>
<td><p><span data-ttu-id="3c266-116">Existe relação no banco de dados que contém as duas tabelas vinculadas</span><span class="sxs-lookup"><span data-stu-id="3c266-116">Relationship exists in the database containing the two linked tables</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c266-117">dbRelationLeft</span><span class="sxs-lookup"><span data-stu-id="3c266-117">dbRelationLeft</span></span></p></td>
<td><p><span data-ttu-id="3c266-118">16777216</span><span class="sxs-lookup"><span data-stu-id="3c266-118">16777216</span></span></p></td>
<td><p><span data-ttu-id="3c266-p101">Somente no Microsoft Access. No modo Design, exibe LEFT JOIN como o tipo de junção padrão.</span><span class="sxs-lookup"><span data-stu-id="3c266-p101">Microsoft Access only. In Design view, display a LEFT JOIN as the default join type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c266-121">dbRelationRight</span><span class="sxs-lookup"><span data-stu-id="3c266-121">dbRelationRight</span></span></p></td>
<td><p><span data-ttu-id="3c266-122">33554432</span><span class="sxs-lookup"><span data-stu-id="3c266-122">33554432</span></span></p></td>
<td><p><span data-ttu-id="3c266-p102">Somente no Microsoft Access. No modo Design, exibe RIGHT JOIN como o tipo de junção padrão.</span><span class="sxs-lookup"><span data-stu-id="3c266-p102">Microsoft Access only. In Design view, display a RIGHT JOIN as the default join type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c266-125">dbRelationUnique</span><span class="sxs-lookup"><span data-stu-id="3c266-125">dbRelationUnique</span></span></p></td>
<td><p><span data-ttu-id="3c266-126">1</span><span class="sxs-lookup"><span data-stu-id="3c266-126">1</span></span></p></td>
<td><p><span data-ttu-id="3c266-127">Relação um-para-um</span><span class="sxs-lookup"><span data-stu-id="3c266-127">One-to-one relationship</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c266-128">dbRelationUpdateCascade</span><span class="sxs-lookup"><span data-stu-id="3c266-128">dbRelationUpdateCascade</span></span></p></td>
<td><p><span data-ttu-id="3c266-129">256</span><span class="sxs-lookup"><span data-stu-id="3c266-129">256</span></span></p></td>
<td><p><span data-ttu-id="3c266-130">Atualizações em cascata</span><span class="sxs-lookup"><span data-stu-id="3c266-130">Updates cascade</span></span></p></td>
</tr>
</tbody>
</table>

