---
title: IsolationLevelEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: IsolationLevelEnum
ms:assetid: 438af3f3-65ed-237d-94d8-f3aff6addd3b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249204(v=office.15)
ms:contentKeyID: 48544506
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 7e32cd3c8ae78199f90fcac8cccdf377bf332d38
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863938"
---
# <a name="isolationlevelenum"></a><span data-ttu-id="9d275-102">IsolationLevelEnum</span><span class="sxs-lookup"><span data-stu-id="9d275-102">IsolationLevelEnum</span></span>

<span data-ttu-id="9d275-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="9d275-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9d275-104">Especifica o nível de isolamento da transação para um objeto [Connection](connection-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="9d275-104">Specifies the level of transaction isolation for a [Connection](connection-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9d275-105">Constant</span><span class="sxs-lookup"><span data-stu-id="9d275-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="9d275-106">Valor</span><span class="sxs-lookup"><span data-stu-id="9d275-106">Value</span></span></p></th>
<th><p><span data-ttu-id="9d275-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="9d275-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9d275-108"><strong>adXactUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="9d275-108"><strong>adXactUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="9d275-109">-1</span><span class="sxs-lookup"><span data-stu-id="9d275-109">-1</span></span></p></td>
<td><p><span data-ttu-id="9d275-110">Indica que o provedor está usando um nível de isolamento diferente do especificado, mas que o nível não pode ser determinado.</span><span class="sxs-lookup"><span data-stu-id="9d275-110">Indicates that the provider is using a different isolation level than specified, but that the level cannot be determined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d275-111"><strong>adXactChaos</strong></span><span class="sxs-lookup"><span data-stu-id="9d275-111"><strong>adXactChaos</strong></span></span></p></td>
<td><p><span data-ttu-id="9d275-112">16</span><span class="sxs-lookup"><span data-stu-id="9d275-112">16</span></span></p></td>
<td><p><span data-ttu-id="9d275-113">Indica que as alterações pendentes de transações mais altamente isoladas não podem ser sobregravadas.</span><span class="sxs-lookup"><span data-stu-id="9d275-113">Indicates that pending changes from more highly isolated transactions cannot be overwritten.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d275-114"><strong>adXactBrowse</strong></span><span class="sxs-lookup"><span data-stu-id="9d275-114"><strong>adXactBrowse</strong></span></span></p></td>
<td><p><span data-ttu-id="9d275-115">256</span><span class="sxs-lookup"><span data-stu-id="9d275-115">256</span></span></p></td>
<td><p><span data-ttu-id="9d275-116">Indica que a partir de uma transação você pode visualizar as alterações sem compromisso em outras transações.</span><span class="sxs-lookup"><span data-stu-id="9d275-116">Indicates that from one transaction you can view uncommitted changes in other transactions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d275-117"><strong>adXactReadUncommitted</strong></span><span class="sxs-lookup"><span data-stu-id="9d275-117"><strong>adXactReadUncommitted</strong></span></span></p></td>
<td><p><span data-ttu-id="9d275-118">256</span><span class="sxs-lookup"><span data-stu-id="9d275-118">256</span></span></p></td>
<td><p><span data-ttu-id="9d275-119">O mesmo que <strong>adXactBrowse</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d275-119">Same as <strong>adXactBrowse</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d275-120"><strong>adXactCursorStability</strong></span><span class="sxs-lookup"><span data-stu-id="9d275-120"><strong>adXactCursorStability</strong></span></span></p></td>
<td><p><span data-ttu-id="9d275-121">4096</span><span class="sxs-lookup"><span data-stu-id="9d275-121">4096</span></span></p></td>
<td><p><span data-ttu-id="9d275-122">Indica que a partir de uma transação você pode visualizar as alterações em outras transações apenas depois que forem confirmadas.</span><span class="sxs-lookup"><span data-stu-id="9d275-122">Indicates that from one transaction you can view changes in other transactions only after they have been committed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d275-123"><strong>adXactReadCommitted</strong></span><span class="sxs-lookup"><span data-stu-id="9d275-123"><strong>adXactReadCommitted</strong></span></span></p></td>
<td><p><span data-ttu-id="9d275-124">4096</span><span class="sxs-lookup"><span data-stu-id="9d275-124">4096</span></span></p></td>
<td><p><span data-ttu-id="9d275-125">O mesmo que <strong>adXactCursorStability</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d275-125">Same as <strong>adXactCursorStability</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d275-126"><strong>adXactRepeatableRead</strong></span><span class="sxs-lookup"><span data-stu-id="9d275-126"><strong>adXactRepeatableRead</strong></span></span></p></td>
<td><p><span data-ttu-id="9d275-127">65536</span><span class="sxs-lookup"><span data-stu-id="9d275-127">65536</span></span></p></td>
<td><p><span data-ttu-id="9d275-128">Indica que a partir de uma transação você não pode ver as alterações feitas em outras transações, mas que a repetição da consulta pode recuperar novos objetos <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d275-128">Indicates that from one transaction you cannot see changes made in other transactions, but that requerying can retrieve new <strong>Recordset</strong> objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d275-129"><strong>adXactIsolated</strong></span><span class="sxs-lookup"><span data-stu-id="9d275-129"><strong>adXactIsolated</strong></span></span></p></td>
<td><p><span data-ttu-id="9d275-130">1048576</span><span class="sxs-lookup"><span data-stu-id="9d275-130">1048576</span></span></p></td>
<td><p><span data-ttu-id="9d275-131">Indica que as transações são conduzidas no isolamento de outras transações.</span><span class="sxs-lookup"><span data-stu-id="9d275-131">Indicates that transactions are conducted in isolation of other transactions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d275-132"><strong>adXactSerializable</strong></span><span class="sxs-lookup"><span data-stu-id="9d275-132"><strong>adXactSerializable</strong></span></span></p></td>
<td><p><span data-ttu-id="9d275-133">1048576</span><span class="sxs-lookup"><span data-stu-id="9d275-133">1048576</span></span></p></td>
<td><p><span data-ttu-id="9d275-134">O mesmo que <strong>adXactIsolated</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d275-134">Same as <strong>adXactIsolated</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="9d275-135">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="9d275-135">ADO/WFC equivalent</span></span>

<span data-ttu-id="9d275-136">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="9d275-136">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9d275-137">Constante</span><span class="sxs-lookup"><span data-stu-id="9d275-137">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9d275-138">AdoEnums.IsolationLevel.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="9d275-138">AdoEnums.IsolationLevel.UNSPECIFIED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d275-139">AdoEnums.IsolationLevel.CHAOS</span><span class="sxs-lookup"><span data-stu-id="9d275-139">AdoEnums.IsolationLevel.CHAOS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d275-140">AdoEnums.IsolationLevel.BROWSE</span><span class="sxs-lookup"><span data-stu-id="9d275-140">AdoEnums.IsolationLevel.BROWSE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d275-141">AdoEnums.IsolationLevel.READUNCOMMITTED</span><span class="sxs-lookup"><span data-stu-id="9d275-141">AdoEnums.IsolationLevel.READUNCOMMITTED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d275-142">AdoEnums.IsolationLevel.CURSORSTABILITY</span><span class="sxs-lookup"><span data-stu-id="9d275-142">AdoEnums.IsolationLevel.CURSORSTABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d275-143">AdoEnums.IsolationLevel.READCOMMITTED</span><span class="sxs-lookup"><span data-stu-id="9d275-143">AdoEnums.IsolationLevel.READCOMMITTED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d275-144">AdoEnums.IsolationLevel.REPEATABLEREAD</span><span class="sxs-lookup"><span data-stu-id="9d275-144">AdoEnums.IsolationLevel.REPEATABLEREAD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d275-145">AdoEnums.IsolationLevel.ISOLATED</span><span class="sxs-lookup"><span data-stu-id="9d275-145">AdoEnums.IsolationLevel.ISOLATED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d275-146">AdoEnums.IsolationLevel.SERIALIZABLE</span><span class="sxs-lookup"><span data-stu-id="9d275-146">AdoEnums.IsolationLevel.SERIALIZABLE</span></span></p></td>
</tr>
</tbody>
</table>

