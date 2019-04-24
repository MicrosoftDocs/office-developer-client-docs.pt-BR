---
title: Enumeração de UpdateCriteriaEnum (DAO)
TOCTitle: UpdateCriteriaEnum Enumeration
ms:assetid: 1f83a0c6-bdc8-9c3e-380b-524f611f6476
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845853(v=office.15)
ms:contentKeyID: 48543644
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e27eb1bdfb9b393df76af8bdf54bc7f05fd82c2e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306367"
---
# <a name="updatecriteriaenum-enumeration-dao"></a><span data-ttu-id="c24e7-102">Enumeração de UpdateCriteriaEnum (DAO)</span><span class="sxs-lookup"><span data-stu-id="c24e7-102">UpdateCriteriaEnum enumeration (DAO)</span></span>


<span data-ttu-id="c24e7-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c24e7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c24e7-104">Usada com o método **UpdateOptions** para especificar como uma atualização em lotes é construída.</span><span class="sxs-lookup"><span data-stu-id="c24e7-104">Used with the **UpdateOptions** method to specify how a batch update is constructed.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c24e7-105">Nome</span><span class="sxs-lookup"><span data-stu-id="c24e7-105">Name</span></span></p></th>
<th><p><span data-ttu-id="c24e7-106">Valor</span><span class="sxs-lookup"><span data-stu-id="c24e7-106">Value</span></span></p></th>
<th><p><span data-ttu-id="c24e7-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="c24e7-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c24e7-108">dbCriteriaAllCols</span><span class="sxs-lookup"><span data-stu-id="c24e7-108">dbCriteriaAllCols</span></span></p></td>
<td><p><span data-ttu-id="c24e7-109">quatro</span><span class="sxs-lookup"><span data-stu-id="c24e7-109">4</span></span></p></td>
<td><p><span data-ttu-id="c24e7-110">Usa a(s) coluna(s) chave e todas as colunas da cláusula where.</span><span class="sxs-lookup"><span data-stu-id="c24e7-110">Uses the key column(s) and all the columns in the where clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c24e7-111">dbCriteriaDeleteInsert</span><span class="sxs-lookup"><span data-stu-id="c24e7-111">dbCriteriaDeleteInsert</span></span></p></td>
<td><p><span data-ttu-id="c24e7-112">dezesseis</span><span class="sxs-lookup"><span data-stu-id="c24e7-112">16</span></span></p></td>
<td><p><span data-ttu-id="c24e7-113">Usa um par de instruções DELETE e INSERT para cada linha modificada.</span><span class="sxs-lookup"><span data-stu-id="c24e7-113">Uses a pair of DELETE and INSERT statements for each modified row.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c24e7-114">dbCriteriaKey</span><span class="sxs-lookup"><span data-stu-id="c24e7-114">dbCriteriaKey</span></span></p></td>
<td><p><span data-ttu-id="c24e7-115">1</span><span class="sxs-lookup"><span data-stu-id="c24e7-115">1</span></span></p></td>
<td><p><span data-ttu-id="c24e7-116">Use apenas a(s) coluna(s) chave na cláusula where.</span><span class="sxs-lookup"><span data-stu-id="c24e7-116">Uses just the key column(s) in the where clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c24e7-117">dbCriteriaModValues</span><span class="sxs-lookup"><span data-stu-id="c24e7-117">dbCriteriaModValues</span></span></p></td>
<td><p><span data-ttu-id="c24e7-118">duas</span><span class="sxs-lookup"><span data-stu-id="c24e7-118">2</span></span></p></td>
<td><p><span data-ttu-id="c24e7-119">Usa a(s) coluna(s) chave e todas as colunas atualizadas na cláusula where.</span><span class="sxs-lookup"><span data-stu-id="c24e7-119">Uses the key column(s) and all updated columns in the where clause.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c24e7-120">dbCriteriaTimestamp</span><span class="sxs-lookup"><span data-stu-id="c24e7-120">dbCriteriaTimestamp</span></span></p></td>
<td><p><span data-ttu-id="c24e7-121">8</span><span class="sxs-lookup"><span data-stu-id="c24e7-121">8</span></span></p></td>
<td><p><span data-ttu-id="c24e7-122">Usa apenas a coluna de carimbo de data/hora, se estiver disponível (gerará um erro em tempo de execução se nenhuma coluna de carimbo de data/hora estiver no conjunto de resultados).</span><span class="sxs-lookup"><span data-stu-id="c24e7-122">Uses just the timestamp column if available (will generate a run-time error if no timestamp column is in the result set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c24e7-123">dbCriteriaUpdate</span><span class="sxs-lookup"><span data-stu-id="c24e7-123">dbCriteriaUpdate</span></span></p></td>
<td><p><span data-ttu-id="c24e7-124">32</span><span class="sxs-lookup"><span data-stu-id="c24e7-124">32</span></span></p></td>
<td><p><span data-ttu-id="c24e7-125">Usa uma instrução UPDATE para cada linha modificada.</span><span class="sxs-lookup"><span data-stu-id="c24e7-125">Uses an UPDATE statement for each modified row.</span></span></p></td>
</tr>
</tbody>
</table>

