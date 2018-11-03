---
title: Características de bloqueio e cursor
TOCTitle: Cursor and lock characteristics
ms:assetid: 5f8b6700-14f6-d342-42f6-cc8e89c71a1a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249347(v=office.15)
ms:contentKeyID: 48545164
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2b3d518ccd82ae2dbc3f280954848d58d8e617cd
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944988"
---
# <a name="cursor-and-lock-characteristics"></a><span data-ttu-id="3ba96-102">Características de bloqueio e cursor</span><span class="sxs-lookup"><span data-stu-id="3ba96-102">Cursor and lock characteristics</span></span>

<span data-ttu-id="3ba96-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="3ba96-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3ba96-104">Embora as características de um cursor dependam dos recursos do provedor, as vantagens e desvantagens a seguir em geral se aplicam aos vários tipos de cursores e bloqueios.</span><span class="sxs-lookup"><span data-stu-id="3ba96-104">While the characteristics of a cursor depend upon capabilities of the provider, the following advantages and disadvantages generally apply to the various types of cursors and locks.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3ba96-105">Tipo de cursor ou bloqueio</span><span class="sxs-lookup"><span data-stu-id="3ba96-105">Cursor or lock type</span></span></p></th>
<th><p><span data-ttu-id="3ba96-106">Vantagens</span><span class="sxs-lookup"><span data-stu-id="3ba96-106">Advantages</span></span></p></th>
<th><p><span data-ttu-id="3ba96-107">Desvantagens</span><span class="sxs-lookup"><span data-stu-id="3ba96-107">Disadvantages</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3ba96-108"><strong>adOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="3ba96-108"><strong>adOpenForwardOnly</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="3ba96-109">Baixa necessidade de recursos</span><span class="sxs-lookup"><span data-stu-id="3ba96-109">Low resource requirements</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="3ba96-110">Não é possível rolar para trás</span><span class="sxs-lookup"><span data-stu-id="3ba96-110">Cannot scroll backward</span></span></p></li>
<li><p><span data-ttu-id="3ba96-111">Não há simultaneidade de dados</span><span class="sxs-lookup"><span data-stu-id="3ba96-111">No data concurrency</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ba96-112"><strong>adOpenStatic</strong></span><span class="sxs-lookup"><span data-stu-id="3ba96-112"><strong>adOpenStatic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="3ba96-113">Rolável</span><span class="sxs-lookup"><span data-stu-id="3ba96-113">Scrollable</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="3ba96-114">Não há simultaneidade de dados</span><span class="sxs-lookup"><span data-stu-id="3ba96-114">No data concurrency</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ba96-115"><strong>adOpenKeyset</strong></span><span class="sxs-lookup"><span data-stu-id="3ba96-115"><strong>adOpenKeyset</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="3ba96-116">Alguma simultaneidade de dados</span><span class="sxs-lookup"><span data-stu-id="3ba96-116">Some data concurrency</span></span></p></li>
<li><p><span data-ttu-id="3ba96-117">Rolável</span><span class="sxs-lookup"><span data-stu-id="3ba96-117">Scrollable</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="3ba96-118">Maior necessidade de recursos</span><span class="sxs-lookup"><span data-stu-id="3ba96-118">Higher resource requirements</span></span></p></li>
<li><p><span data-ttu-id="3ba96-119">Não disponível em cenário desconectado</span><span class="sxs-lookup"><span data-stu-id="3ba96-119">Not available in disconnected scenario</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ba96-120"><strong>adOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="3ba96-120"><strong>adOpenDynamic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="3ba96-121">Alta simultaneidade de dados</span><span class="sxs-lookup"><span data-stu-id="3ba96-121">High data concurrency</span></span></p></li>
<li><p><span data-ttu-id="3ba96-122">Rolável</span><span class="sxs-lookup"><span data-stu-id="3ba96-122">Scrollable</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="3ba96-123">Alta necessidade de recursos</span><span class="sxs-lookup"><span data-stu-id="3ba96-123">Highest resource requirements</span></span></p></li>
<li><p><span data-ttu-id="3ba96-124">Não disponível em cenário desconectado</span><span class="sxs-lookup"><span data-stu-id="3ba96-124">Not available in disconnected scenario</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ba96-125"><strong>adLockReadOnly</strong></span><span class="sxs-lookup"><span data-stu-id="3ba96-125"><strong>adLockReadOnly</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="3ba96-126">Baixa necessidade de recursos</span><span class="sxs-lookup"><span data-stu-id="3ba96-126">Low resource requirements</span></span></p></li>
<li><p><span data-ttu-id="3ba96-127">Altamente escalonável</span><span class="sxs-lookup"><span data-stu-id="3ba96-127">Highly scalable</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="3ba96-128">Dados não atualizáveis através do cursor</span><span class="sxs-lookup"><span data-stu-id="3ba96-128">Data not updatable through cursor</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ba96-129"><strong>adLockBatchOptimistic</strong></span><span class="sxs-lookup"><span data-stu-id="3ba96-129"><strong>adLockBatchOptimistic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="3ba96-130">Atualizações em lotes</span><span class="sxs-lookup"><span data-stu-id="3ba96-130">Batch updates</span></span></p></li>
<li><p><span data-ttu-id="3ba96-131">Permite cenários desconectados</span><span class="sxs-lookup"><span data-stu-id="3ba96-131">Allows disconnected scenarios</span></span></p></li>
<li><p><span data-ttu-id="3ba96-132">Outros usuários podem acessar os dados</span><span class="sxs-lookup"><span data-stu-id="3ba96-132">Other users able to access data</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="3ba96-133">Os dados podem ser alterados por vários usuários ao mesmo tempo</span><span class="sxs-lookup"><span data-stu-id="3ba96-133">Data can be changed by multiple users at once</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ba96-134"><strong>adLockPessimistic</strong></span><span class="sxs-lookup"><span data-stu-id="3ba96-134"><strong>adLockPessimistic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="3ba96-135">Os dados não podem ser alterados por outros usuários durante o bloqueio</span><span class="sxs-lookup"><span data-stu-id="3ba96-135">Data cannot be changed by other users while locked</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="3ba96-136">Impede que outros usuários acessem os dados durante o bloqueio</span><span class="sxs-lookup"><span data-stu-id="3ba96-136">Prevents other users from accessing data while locked</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ba96-137"><strong>adLockOptimistic</strong></span><span class="sxs-lookup"><span data-stu-id="3ba96-137"><strong>adLockOptimistic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="3ba96-138">Outros usuários podem acessar os dados</span><span class="sxs-lookup"><span data-stu-id="3ba96-138">Other users able to access data</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="3ba96-139">Os dados podem ser alterados por vários usuários ao mesmo tempo</span><span class="sxs-lookup"><span data-stu-id="3ba96-139">Data can be changed by multiple users at once</span></span></p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>

