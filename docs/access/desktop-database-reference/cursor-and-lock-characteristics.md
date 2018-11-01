---
title: Características do cursor e do bloqueio
TOCTitle: Cursor and Lock Characteristics
ms:assetid: 5f8b6700-14f6-d342-42f6-cc8e89c71a1a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249347(v=office.15)
ms:contentKeyID: 48545164
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 85268b9c4b57d92cd8e7df9cd1da01286709f915
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877566"
---
# <a name="cursor-and-lock-characteristics"></a><span data-ttu-id="fe2fb-102">Características do cursor e do bloqueio</span><span class="sxs-lookup"><span data-stu-id="fe2fb-102">Cursor and Lock Characteristics</span></span>


<span data-ttu-id="fe2fb-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="fe2fb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fe2fb-104">Embora as características de um cursor dependam dos recursos do provedor, as vantagens e desvantagens a seguir em geral se aplicam aos vários tipos de cursores e bloqueios.</span><span class="sxs-lookup"><span data-stu-id="fe2fb-104">While the characteristics of a cursor depend upon capabilities of the provider, the following advantages and disadvantages generally apply to the various types of cursors and locks.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fe2fb-105">Tipo de cursor ou bloqueio</span><span class="sxs-lookup"><span data-stu-id="fe2fb-105">Cursor or lock type</span></span></p></th>
<th><p><span data-ttu-id="fe2fb-106">Vantagens</span><span class="sxs-lookup"><span data-stu-id="fe2fb-106">Advantages</span></span></p></th>
<th><p><span data-ttu-id="fe2fb-107">Desvantagens</span><span class="sxs-lookup"><span data-stu-id="fe2fb-107">Disadvantages</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fe2fb-108"><strong>adOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="fe2fb-108"><strong>adOpenForwardOnly</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="fe2fb-109">Baixa necessidade de recursos</span><span class="sxs-lookup"><span data-stu-id="fe2fb-109">Low resource requirements</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="fe2fb-110">Não é possível rolar para trás</span><span class="sxs-lookup"><span data-stu-id="fe2fb-110">Cannot scroll backward</span></span></p></li>
<li><p><span data-ttu-id="fe2fb-111">Não há simultaneidade de dados</span><span class="sxs-lookup"><span data-stu-id="fe2fb-111">No data concurrency</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2fb-112"><strong>adOpenStatic</strong></span><span class="sxs-lookup"><span data-stu-id="fe2fb-112"><strong>adOpenStatic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="fe2fb-113">Rolável</span><span class="sxs-lookup"><span data-stu-id="fe2fb-113">Scrollable</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="fe2fb-114">Não há simultaneidade de dados</span><span class="sxs-lookup"><span data-stu-id="fe2fb-114">No data concurrency</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2fb-115"><strong>adOpenKeyset</strong></span><span class="sxs-lookup"><span data-stu-id="fe2fb-115"><strong>adOpenKeyset</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="fe2fb-116">Alguma simultaneidade de dados</span><span class="sxs-lookup"><span data-stu-id="fe2fb-116">Some data concurrency</span></span></p></li>
<li><p><span data-ttu-id="fe2fb-117">Rolável</span><span class="sxs-lookup"><span data-stu-id="fe2fb-117">Scrollable</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="fe2fb-118">Maior necessidade de recursos</span><span class="sxs-lookup"><span data-stu-id="fe2fb-118">Higher resource requirements</span></span></p></li>
<li><p><span data-ttu-id="fe2fb-119">Não disponível em cenário desconectado</span><span class="sxs-lookup"><span data-stu-id="fe2fb-119">Not available in disconnected scenario</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2fb-120"><strong>adOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="fe2fb-120"><strong>adOpenDynamic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="fe2fb-121">Alta simultaneidade de dados</span><span class="sxs-lookup"><span data-stu-id="fe2fb-121">High data concurrency</span></span></p></li>
<li><p><span data-ttu-id="fe2fb-122">Rolável</span><span class="sxs-lookup"><span data-stu-id="fe2fb-122">Scrollable</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="fe2fb-123">Alta necessidade de recursos</span><span class="sxs-lookup"><span data-stu-id="fe2fb-123">Highest resource requirements</span></span></p></li>
<li><p><span data-ttu-id="fe2fb-124">Não disponível em cenário desconectado</span><span class="sxs-lookup"><span data-stu-id="fe2fb-124">Not available in disconnected scenario</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2fb-125"><strong>adLockReadOnly</strong></span><span class="sxs-lookup"><span data-stu-id="fe2fb-125"><strong>adLockReadOnly</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="fe2fb-126">Baixa necessidade de recursos</span><span class="sxs-lookup"><span data-stu-id="fe2fb-126">Low resource requirements</span></span></p></li>
<li><p><span data-ttu-id="fe2fb-127">Altamente escalonável</span><span class="sxs-lookup"><span data-stu-id="fe2fb-127">Highly scalable</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="fe2fb-128">Dados não atualizáveis através do cursor</span><span class="sxs-lookup"><span data-stu-id="fe2fb-128">Data not updatable through cursor</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2fb-129"><strong>adLockBatchOptimistic</strong></span><span class="sxs-lookup"><span data-stu-id="fe2fb-129"><strong>adLockBatchOptimistic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="fe2fb-130">Atualizações em lotes</span><span class="sxs-lookup"><span data-stu-id="fe2fb-130">Batch updates</span></span></p></li>
<li><p><span data-ttu-id="fe2fb-131">Permite cenários desconectados</span><span class="sxs-lookup"><span data-stu-id="fe2fb-131">Allows disconnected scenarios</span></span></p></li>
<li><p><span data-ttu-id="fe2fb-132">Outros usuários podem acessar os dados</span><span class="sxs-lookup"><span data-stu-id="fe2fb-132">Other users able to access data</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="fe2fb-133">Os dados podem ser alterados por vários usuários ao mesmo tempo</span><span class="sxs-lookup"><span data-stu-id="fe2fb-133">Data can be changed by multiple users at once</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe2fb-134"><strong>adLockPessimistic</strong></span><span class="sxs-lookup"><span data-stu-id="fe2fb-134"><strong>adLockPessimistic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="fe2fb-135">Os dados não podem ser alterados por outros usuários durante o bloqueio</span><span class="sxs-lookup"><span data-stu-id="fe2fb-135">Data cannot be changed by other users while locked</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="fe2fb-136">Impede que outros usuários acessem os dados durante o bloqueio</span><span class="sxs-lookup"><span data-stu-id="fe2fb-136">Prevents other users from accessing data while locked</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe2fb-137"><strong>adLockOptimistic</strong></span><span class="sxs-lookup"><span data-stu-id="fe2fb-137"><strong>adLockOptimistic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="fe2fb-138">Outros usuários podem acessar os dados</span><span class="sxs-lookup"><span data-stu-id="fe2fb-138">Other users able to access data</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="fe2fb-139">Os dados podem ser alterados por vários usuários ao mesmo tempo</span><span class="sxs-lookup"><span data-stu-id="fe2fb-139">Data can be changed by multiple users at once</span></span></p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>

