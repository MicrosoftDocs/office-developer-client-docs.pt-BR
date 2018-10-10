---
title: Enumeração UpdateCriteriaEnum (DAO)
TOCTitle: UpdateCriteriaEnum Enumeration
ms:assetid: 1f83a0c6-bdc8-9c3e-380b-524f611f6476
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845853(v=office.15)
ms:contentKeyID: 48543644
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7dc671458d53f6e40e27ff2dd338f010c09dc5ba
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463062"
---
# <a name="updatecriteriaenum-enumeration-dao"></a><span data-ttu-id="aed06-102">Enumeração UpdateCriteriaEnum (DAO)</span><span class="sxs-lookup"><span data-stu-id="aed06-102">UpdateCriteriaEnum Enumeration (DAO)</span></span>


<span data-ttu-id="aed06-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="aed06-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="aed06-104">Usada com o método **UpdateOptions** para especificar como uma atualização em lotes é construída.</span><span class="sxs-lookup"><span data-stu-id="aed06-104">Used with the **UpdateOptions** method to specify how a batch update is constructed.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="aed06-105">Nome</span><span class="sxs-lookup"><span data-stu-id="aed06-105">Name</span></span></p></th>
<th><p><span data-ttu-id="aed06-106">Valor</span><span class="sxs-lookup"><span data-stu-id="aed06-106">Value</span></span></p></th>
<th><p><span data-ttu-id="aed06-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="aed06-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aed06-108">dbCriteriaAllCols</span><span class="sxs-lookup"><span data-stu-id="aed06-108">dbCriteriaAllCols</span></span></p></td>
<td><p><span data-ttu-id="aed06-109">4</span><span class="sxs-lookup"><span data-stu-id="aed06-109">4</span></span></p></td>
<td><p><span data-ttu-id="aed06-110">Usa a(s) coluna(s) chave e todas as colunas da cláusula where.</span><span class="sxs-lookup"><span data-stu-id="aed06-110">Uses the key column(s) and all the columns in the where clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aed06-111">dbCriteriaDeleteInsert</span><span class="sxs-lookup"><span data-stu-id="aed06-111">dbCriteriaDeleteInsert</span></span></p></td>
<td><p><span data-ttu-id="aed06-112">16</span><span class="sxs-lookup"><span data-stu-id="aed06-112">16</span></span></p></td>
<td><p><span data-ttu-id="aed06-113">Usa um par de instruções DELETE e INSERT para cada linha modificada.</span><span class="sxs-lookup"><span data-stu-id="aed06-113">Uses a pair of DELETE and INSERT statements for each modified row.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aed06-114">dbCriteriaKey</span><span class="sxs-lookup"><span data-stu-id="aed06-114">dbCriteriaKey</span></span></p></td>
<td><p><span data-ttu-id="aed06-115">1</span><span class="sxs-lookup"><span data-stu-id="aed06-115">1</span></span></p></td>
<td><p><span data-ttu-id="aed06-116">Use apenas a(s) coluna(s) chave na cláusula where.</span><span class="sxs-lookup"><span data-stu-id="aed06-116">Uses just the key column(s) in the where clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aed06-117">dbCriteriaModValues</span><span class="sxs-lookup"><span data-stu-id="aed06-117">dbCriteriaModValues</span></span></p></td>
<td><p><span data-ttu-id="aed06-118">2</span><span class="sxs-lookup"><span data-stu-id="aed06-118">2</span></span></p></td>
<td><p><span data-ttu-id="aed06-119">Usa a(s) coluna(s) chave e todas as colunas atualizadas na cláusula where.</span><span class="sxs-lookup"><span data-stu-id="aed06-119">Uses the key column(s) and all updated columns in the where clause.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aed06-120">dbCriteriaTimestamp</span><span class="sxs-lookup"><span data-stu-id="aed06-120">dbCriteriaTimestamp</span></span></p></td>
<td><p><span data-ttu-id="aed06-121">8</span><span class="sxs-lookup"><span data-stu-id="aed06-121">8</span></span></p></td>
<td><p><span data-ttu-id="aed06-122">Usa apenas a coluna de carimbo de data/hora, se estiver disponível (gerará um erro em tempo de execução se nenhuma coluna de carimbo de data/hora estiver no conjunto de resultados).</span><span class="sxs-lookup"><span data-stu-id="aed06-122">Uses just the timestamp column if available (will generate a run-time error if no timestamp column is in the result set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aed06-123">dbCriteriaUpdate</span><span class="sxs-lookup"><span data-stu-id="aed06-123">dbCriteriaUpdate</span></span></p></td>
<td><p><span data-ttu-id="aed06-124">32</span><span class="sxs-lookup"><span data-stu-id="aed06-124">32</span></span></p></td>
<td><p><span data-ttu-id="aed06-125">Usa uma instrução UPDATE para cada linha modificada.</span><span class="sxs-lookup"><span data-stu-id="aed06-125">Uses an UPDATE statement for each modified row.</span></span></p></td>
</tr>
</tbody>
</table>

