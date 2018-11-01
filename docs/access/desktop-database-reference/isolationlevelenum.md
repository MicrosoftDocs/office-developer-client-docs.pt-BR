---
title: IsolationLevelEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: IsolationLevelEnum
ms:assetid: 438af3f3-65ed-237d-94d8-f3aff6addd3b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249204(v=office.15)
ms:contentKeyID: 48544506
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: cb8873a7ddfc62429847b561736df4bfa91d429d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872841"
---
# <a name="isolationlevelenum"></a><span data-ttu-id="dc8e9-102">IsolationLevelEnum</span><span class="sxs-lookup"><span data-stu-id="dc8e9-102">IsolationLevelEnum</span></span>

<span data-ttu-id="dc8e9-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="dc8e9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dc8e9-104">Especifica o nível de isolamento da transação para um objeto [Connection](connection-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="dc8e9-104">Specifies the level of transaction isolation for a [Connection](connection-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dc8e9-105">Constant</span><span class="sxs-lookup"><span data-stu-id="dc8e9-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="dc8e9-106">Valor</span><span class="sxs-lookup"><span data-stu-id="dc8e9-106">Value</span></span></p></th>
<th><p><span data-ttu-id="dc8e9-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="dc8e9-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dc8e9-108"><strong>adXactUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="dc8e9-108"><strong>adXactUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="dc8e9-109">-1</span><span class="sxs-lookup"><span data-stu-id="dc8e9-109">-1</span></span></p></td>
<td><p><span data-ttu-id="dc8e9-110">Indica que o provedor está usando um nível de isolamento diferente do especificado, mas que o nível não pode ser determinado.</span><span class="sxs-lookup"><span data-stu-id="dc8e9-110">Indicates that the provider is using a different isolation level than specified, but that the level cannot be determined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc8e9-111"><strong>adXactChaos</strong></span><span class="sxs-lookup"><span data-stu-id="dc8e9-111"><strong>adXactChaos</strong></span></span></p></td>
<td><p><span data-ttu-id="dc8e9-112">16</span><span class="sxs-lookup"><span data-stu-id="dc8e9-112">16</span></span></p></td>
<td><p><span data-ttu-id="dc8e9-113">Indica que as alterações pendentes de transações mais altamente isoladas não podem ser sobregravadas.</span><span class="sxs-lookup"><span data-stu-id="dc8e9-113">Indicates that pending changes from more highly isolated transactions cannot be overwritten.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc8e9-114"><strong>adXactBrowse</strong></span><span class="sxs-lookup"><span data-stu-id="dc8e9-114"><strong>adXactBrowse</strong></span></span></p></td>
<td><p><span data-ttu-id="dc8e9-115">256</span><span class="sxs-lookup"><span data-stu-id="dc8e9-115">256</span></span></p></td>
<td><p><span data-ttu-id="dc8e9-116">Indica que a partir de uma transação você pode visualizar as alterações sem compromisso em outras transações.</span><span class="sxs-lookup"><span data-stu-id="dc8e9-116">Indicates that from one transaction you can view uncommitted changes in other transactions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc8e9-117"><strong>adXactReadUncommitted</strong></span><span class="sxs-lookup"><span data-stu-id="dc8e9-117"><strong>adXactReadUncommitted</strong></span></span></p></td>
<td><p><span data-ttu-id="dc8e9-118">256</span><span class="sxs-lookup"><span data-stu-id="dc8e9-118">256</span></span></p></td>
<td><p><span data-ttu-id="dc8e9-119">O mesmo que <strong>adXactBrowse</strong>.</span><span class="sxs-lookup"><span data-stu-id="dc8e9-119">Same as <strong>adXactBrowse</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc8e9-120"><strong>adXactCursorStability</strong></span><span class="sxs-lookup"><span data-stu-id="dc8e9-120"><strong>adXactCursorStability</strong></span></span></p></td>
<td><p><span data-ttu-id="dc8e9-121">4096</span><span class="sxs-lookup"><span data-stu-id="dc8e9-121">4096</span></span></p></td>
<td><p><span data-ttu-id="dc8e9-122">Indica que a partir de uma transação você pode visualizar as alterações em outras transações apenas depois que forem confirmadas.</span><span class="sxs-lookup"><span data-stu-id="dc8e9-122">Indicates that from one transaction you can view changes in other transactions only after they have been committed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc8e9-123"><strong>adXactReadCommitted</strong></span><span class="sxs-lookup"><span data-stu-id="dc8e9-123"><strong>adXactReadCommitted</strong></span></span></p></td>
<td><p><span data-ttu-id="dc8e9-124">4096</span><span class="sxs-lookup"><span data-stu-id="dc8e9-124">4096</span></span></p></td>
<td><p><span data-ttu-id="dc8e9-125">O mesmo que <strong>adXactCursorStability</strong>.</span><span class="sxs-lookup"><span data-stu-id="dc8e9-125">Same as <strong>adXactCursorStability</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc8e9-126"><strong>adXactRepeatableRead</strong></span><span class="sxs-lookup"><span data-stu-id="dc8e9-126"><strong>adXactRepeatableRead</strong></span></span></p></td>
<td><p><span data-ttu-id="dc8e9-127">65536</span><span class="sxs-lookup"><span data-stu-id="dc8e9-127">65536</span></span></p></td>
<td><p><span data-ttu-id="dc8e9-128">Indica que a partir de uma transação você não pode ver as alterações feitas em outras transações, mas que a repetição da consulta pode recuperar novos objetos <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="dc8e9-128">Indicates that from one transaction you cannot see changes made in other transactions, but that requerying can retrieve new <strong>Recordset</strong> objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc8e9-129"><strong>adXactIsolated</strong></span><span class="sxs-lookup"><span data-stu-id="dc8e9-129"><strong>adXactIsolated</strong></span></span></p></td>
<td><p><span data-ttu-id="dc8e9-130">1048576</span><span class="sxs-lookup"><span data-stu-id="dc8e9-130">1048576</span></span></p></td>
<td><p><span data-ttu-id="dc8e9-131">Indica que as transações são conduzidas no isolamento de outras transações.</span><span class="sxs-lookup"><span data-stu-id="dc8e9-131">Indicates that transactions are conducted in isolation of other transactions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc8e9-132"><strong>adXactSerializable</strong></span><span class="sxs-lookup"><span data-stu-id="dc8e9-132"><strong>adXactSerializable</strong></span></span></p></td>
<td><p><span data-ttu-id="dc8e9-133">1048576</span><span class="sxs-lookup"><span data-stu-id="dc8e9-133">1048576</span></span></p></td>
<td><p><span data-ttu-id="dc8e9-134">O mesmo que <strong>adXactIsolated</strong>.</span><span class="sxs-lookup"><span data-stu-id="dc8e9-134">Same as <strong>adXactIsolated</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="dc8e9-135">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="dc8e9-135">ADO/WFC equivalent</span></span>

<span data-ttu-id="dc8e9-136">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="dc8e9-136">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dc8e9-137">Constante</span><span class="sxs-lookup"><span data-stu-id="dc8e9-137">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dc8e9-138">AdoEnums.IsolationLevel.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="dc8e9-138">AdoEnums.IsolationLevel.UNSPECIFIED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc8e9-139">AdoEnums.IsolationLevel.CHAOS</span><span class="sxs-lookup"><span data-stu-id="dc8e9-139">AdoEnums.IsolationLevel.CHAOS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc8e9-140">AdoEnums.IsolationLevel.BROWSE</span><span class="sxs-lookup"><span data-stu-id="dc8e9-140">AdoEnums.IsolationLevel.BROWSE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc8e9-141">AdoEnums.IsolationLevel.READUNCOMMITTED</span><span class="sxs-lookup"><span data-stu-id="dc8e9-141">AdoEnums.IsolationLevel.READUNCOMMITTED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc8e9-142">AdoEnums.IsolationLevel.CURSORSTABILITY</span><span class="sxs-lookup"><span data-stu-id="dc8e9-142">AdoEnums.IsolationLevel.CURSORSTABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc8e9-143">AdoEnums.IsolationLevel.READCOMMITTED</span><span class="sxs-lookup"><span data-stu-id="dc8e9-143">AdoEnums.IsolationLevel.READCOMMITTED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc8e9-144">AdoEnums.IsolationLevel.REPEATABLEREAD</span><span class="sxs-lookup"><span data-stu-id="dc8e9-144">AdoEnums.IsolationLevel.REPEATABLEREAD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc8e9-145">AdoEnums.IsolationLevel.ISOLATED</span><span class="sxs-lookup"><span data-stu-id="dc8e9-145">AdoEnums.IsolationLevel.ISOLATED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc8e9-146">AdoEnums.IsolationLevel.SERIALIZABLE</span><span class="sxs-lookup"><span data-stu-id="dc8e9-146">AdoEnums.IsolationLevel.SERIALIZABLE</span></span></p></td>
</tr>
</tbody>
</table>

