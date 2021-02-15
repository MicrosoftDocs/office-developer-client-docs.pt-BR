---
title: IsolationLevelEnum (referência do banco de dados da área de trabalho do Access)
TOCTitle: IsolationLevelEnum
ms:assetid: 438af3f3-65ed-237d-94d8-f3aff6addd3b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249204(v=office.15)
ms:contentKeyID: 48544506
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9f0176772b366b39d368f8bae1e402d420f0136c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291153"
---
# <a name="isolationlevelenum"></a><span data-ttu-id="1f9db-102">IsolationLevelEnum</span><span class="sxs-lookup"><span data-stu-id="1f9db-102">IsolationLevelEnum</span></span>

<span data-ttu-id="1f9db-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1f9db-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1f9db-104">Especifica o nível de isolamento da transação para um objeto [Connection](connection-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="1f9db-104">Specifies the level of transaction isolation for a [Connection](connection-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1f9db-105">Constant</span><span class="sxs-lookup"><span data-stu-id="1f9db-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="1f9db-106">Valor</span><span class="sxs-lookup"><span data-stu-id="1f9db-106">Value</span></span></p></th>
<th><p><span data-ttu-id="1f9db-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="1f9db-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1f9db-108"><strong>adXactUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="1f9db-108"><strong>adXactUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="1f9db-109">-1</span><span class="sxs-lookup"><span data-stu-id="1f9db-109">-1</span></span></p></td>
<td><p><span data-ttu-id="1f9db-110">Indica que o provedor está usando um nível de isolamento diferente do especificado, mas que o nível não pode ser determinado.</span><span class="sxs-lookup"><span data-stu-id="1f9db-110">Indicates that the provider is using a different isolation level than specified, but that the level cannot be determined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f9db-111"><strong>adXactChaos</strong></span><span class="sxs-lookup"><span data-stu-id="1f9db-111"><strong>adXactChaos</strong></span></span></p></td>
<td><p><span data-ttu-id="1f9db-112">16 </span><span class="sxs-lookup"><span data-stu-id="1f9db-112">16</span></span></p></td>
<td><p><span data-ttu-id="1f9db-113">Indica que as alterações pendentes de transações mais altamente isoladas não podem ser sobregravadas.</span><span class="sxs-lookup"><span data-stu-id="1f9db-113">Indicates that pending changes from more highly isolated transactions cannot be overwritten.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f9db-114"><strong>adXactBrowse</strong></span><span class="sxs-lookup"><span data-stu-id="1f9db-114"><strong>adXactBrowse</strong></span></span></p></td>
<td><p><span data-ttu-id="1f9db-115">256</span><span class="sxs-lookup"><span data-stu-id="1f9db-115">256</span></span></p></td>
<td><p><span data-ttu-id="1f9db-116">Indica que a partir de uma transação você pode visualizar as alterações sem compromisso em outras transações.</span><span class="sxs-lookup"><span data-stu-id="1f9db-116">Indicates that from one transaction you can view uncommitted changes in other transactions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f9db-117"><strong>adXactReadUncommitted</strong></span><span class="sxs-lookup"><span data-stu-id="1f9db-117"><strong>adXactReadUncommitted</strong></span></span></p></td>
<td><p><span data-ttu-id="1f9db-118">256</span><span class="sxs-lookup"><span data-stu-id="1f9db-118">256</span></span></p></td>
<td><p><span data-ttu-id="1f9db-119">O mesmo que <strong>adXactBrowse</strong>.</span><span class="sxs-lookup"><span data-stu-id="1f9db-119">Same as <strong>adXactBrowse</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f9db-120"><strong>adXactCursorStability</strong></span><span class="sxs-lookup"><span data-stu-id="1f9db-120"><strong>adXactCursorStability</strong></span></span></p></td>
<td><p><span data-ttu-id="1f9db-121">4096</span><span class="sxs-lookup"><span data-stu-id="1f9db-121">4096</span></span></p></td>
<td><p><span data-ttu-id="1f9db-122">Indica que a partir de uma transação você pode visualizar as alterações em outras transações apenas depois que forem confirmadas.</span><span class="sxs-lookup"><span data-stu-id="1f9db-122">Indicates that from one transaction you can view changes in other transactions only after they have been committed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f9db-123"><strong>adXactReadCommitted</strong></span><span class="sxs-lookup"><span data-stu-id="1f9db-123"><strong>adXactReadCommitted</strong></span></span></p></td>
<td><p><span data-ttu-id="1f9db-124">4096</span><span class="sxs-lookup"><span data-stu-id="1f9db-124">4096</span></span></p></td>
<td><p><span data-ttu-id="1f9db-125">O mesmo que <strong>adXactCursorStability</strong>.</span><span class="sxs-lookup"><span data-stu-id="1f9db-125">Same as <strong>adXactCursorStability</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f9db-126"><strong>adXactRepeatableRead</strong></span><span class="sxs-lookup"><span data-stu-id="1f9db-126"><strong>adXactRepeatableRead</strong></span></span></p></td>
<td><p><span data-ttu-id="1f9db-127">65536</span><span class="sxs-lookup"><span data-stu-id="1f9db-127">65536</span></span></p></td>
<td><p><span data-ttu-id="1f9db-128">Indica que a partir de uma transação você não pode ver as alterações feitas em outras transações, mas que a repetição da consulta pode recuperar novos objetos <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="1f9db-128">Indicates that from one transaction you cannot see changes made in other transactions, but that requerying can retrieve new <strong>Recordset</strong> objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f9db-129"><strong>adXactIsolated</strong></span><span class="sxs-lookup"><span data-stu-id="1f9db-129"><strong>adXactIsolated</strong></span></span></p></td>
<td><p><span data-ttu-id="1f9db-130">1048576</span><span class="sxs-lookup"><span data-stu-id="1f9db-130">1048576</span></span></p></td>
<td><p><span data-ttu-id="1f9db-131">Indica que as transações são conduzidas no isolamento de outras transações.</span><span class="sxs-lookup"><span data-stu-id="1f9db-131">Indicates that transactions are conducted in isolation of other transactions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f9db-132"><strong>adXactSerializable</strong></span><span class="sxs-lookup"><span data-stu-id="1f9db-132"><strong>adXactSerializable</strong></span></span></p></td>
<td><p><span data-ttu-id="1f9db-133">1048576</span><span class="sxs-lookup"><span data-stu-id="1f9db-133">1048576</span></span></p></td>
<td><p><span data-ttu-id="1f9db-134">O mesmo que <strong>adXactIsolated</strong>.</span><span class="sxs-lookup"><span data-stu-id="1f9db-134">Same as <strong>adXactIsolated</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="1f9db-135">Equivalente do ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="1f9db-135">ADO/WFC equivalent</span></span>

<span data-ttu-id="1f9db-136">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="1f9db-136">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1f9db-137">Constant</span><span class="sxs-lookup"><span data-stu-id="1f9db-137">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1f9db-138">AdoEnums.IsolationLevel.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="1f9db-138">AdoEnums.IsolationLevel.UNSPECIFIED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f9db-139">AdoEnums.IsolationLevel.CHAOS</span><span class="sxs-lookup"><span data-stu-id="1f9db-139">AdoEnums.IsolationLevel.CHAOS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f9db-140">AdoEnums.IsolationLevel.BROWSE</span><span class="sxs-lookup"><span data-stu-id="1f9db-140">AdoEnums.IsolationLevel.BROWSE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f9db-141">AdoEnums.IsolationLevel.READUNCOMMITTED</span><span class="sxs-lookup"><span data-stu-id="1f9db-141">AdoEnums.IsolationLevel.READUNCOMMITTED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f9db-142">AdoEnums.IsolationLevel.CURSORSTABILITY</span><span class="sxs-lookup"><span data-stu-id="1f9db-142">AdoEnums.IsolationLevel.CURSORSTABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f9db-143">AdoEnums.IsolationLevel.READCOMMITTED</span><span class="sxs-lookup"><span data-stu-id="1f9db-143">AdoEnums.IsolationLevel.READCOMMITTED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f9db-144">AdoEnums.IsolationLevel.REPEATABLEREAD</span><span class="sxs-lookup"><span data-stu-id="1f9db-144">AdoEnums.IsolationLevel.REPEATABLEREAD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f9db-145">AdoEnums.IsolationLevel.ISOLATED</span><span class="sxs-lookup"><span data-stu-id="1f9db-145">AdoEnums.IsolationLevel.ISOLATED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f9db-146">AdoEnums.IsolationLevel.SERIALIZABLE</span><span class="sxs-lookup"><span data-stu-id="1f9db-146">AdoEnums.IsolationLevel.SERIALIZABLE</span></span></p></td>
</tr>
</tbody>
</table>

