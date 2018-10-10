---
title: IsolationLevelEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: IsolationLevelEnum
ms:assetid: 438af3f3-65ed-237d-94d8-f3aff6addd3b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249204(v=office.15)
ms:contentKeyID: 48544506
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 80e7d22a5152b24894bf746b939f705739d4220d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465307"
---
# <a name="isolationlevelenum"></a><span data-ttu-id="a8bec-102">IsolationLevelEnum</span><span class="sxs-lookup"><span data-stu-id="a8bec-102">IsolationLevelEnum</span></span>


<span data-ttu-id="a8bec-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a8bec-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a8bec-104">Especifica o nível de isolamento da transação para um objeto [Connection](connection-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="a8bec-104">Specifies the level of transaction isolation for a [Connection](connection-object-ado.md) object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a8bec-105">Constant</span><span class="sxs-lookup"><span data-stu-id="a8bec-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="a8bec-106">Valor</span><span class="sxs-lookup"><span data-stu-id="a8bec-106">Value</span></span></p></th>
<th><p><span data-ttu-id="a8bec-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="a8bec-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a8bec-108"><strong>adXactUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="a8bec-108"><strong>adXactUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="a8bec-109">-1</span><span class="sxs-lookup"><span data-stu-id="a8bec-109">-1</span></span></p></td>
<td><p><span data-ttu-id="a8bec-110">Indica que o provedor está usando um nível de isolamento diferente do especificado, mas que o nível não pode ser determinado.</span><span class="sxs-lookup"><span data-stu-id="a8bec-110">Indicates that the provider is using a different isolation level than specified, but that the level cannot be determined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8bec-111"><strong>adXactChaos</strong></span><span class="sxs-lookup"><span data-stu-id="a8bec-111"><strong>adXactChaos</strong></span></span></p></td>
<td><p><span data-ttu-id="a8bec-112">16</span><span class="sxs-lookup"><span data-stu-id="a8bec-112">16</span></span></p></td>
<td><p><span data-ttu-id="a8bec-113">Indica que as alterações pendentes de transações mais altamente isoladas não podem ser sobregravadas.</span><span class="sxs-lookup"><span data-stu-id="a8bec-113">Indicates that pending changes from more highly isolated transactions cannot be overwritten.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8bec-114"><strong>adXactBrowse</strong></span><span class="sxs-lookup"><span data-stu-id="a8bec-114"><strong>adXactBrowse</strong></span></span></p></td>
<td><p><span data-ttu-id="a8bec-115">256</span><span class="sxs-lookup"><span data-stu-id="a8bec-115">256</span></span></p></td>
<td><p><span data-ttu-id="a8bec-116">Indica que a partir de uma transação você pode visualizar as alterações sem compromisso em outras transações.</span><span class="sxs-lookup"><span data-stu-id="a8bec-116">Indicates that from one transaction you can view uncommitted changes in other transactions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8bec-117"><strong>adXactReadUncommitted</strong></span><span class="sxs-lookup"><span data-stu-id="a8bec-117"><strong>adXactReadUncommitted</strong></span></span></p></td>
<td><p><span data-ttu-id="a8bec-118">256</span><span class="sxs-lookup"><span data-stu-id="a8bec-118">256</span></span></p></td>
<td><p><span data-ttu-id="a8bec-119">O mesmo que <strong>adXactBrowse</strong>.</span><span class="sxs-lookup"><span data-stu-id="a8bec-119">Same as <strong>adXactBrowse</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8bec-120"><strong>adXactCursorStability</strong></span><span class="sxs-lookup"><span data-stu-id="a8bec-120"><strong>adXactCursorStability</strong></span></span></p></td>
<td><p><span data-ttu-id="a8bec-121">4096</span><span class="sxs-lookup"><span data-stu-id="a8bec-121">4096</span></span></p></td>
<td><p><span data-ttu-id="a8bec-122">Indica que a partir de uma transação você pode visualizar as alterações em outras transações apenas depois que forem confirmadas.</span><span class="sxs-lookup"><span data-stu-id="a8bec-122">Indicates that from one transaction you can view changes in other transactions only after they have been committed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8bec-123"><strong>adXactReadCommitted</strong></span><span class="sxs-lookup"><span data-stu-id="a8bec-123"><strong>adXactReadCommitted</strong></span></span></p></td>
<td><p><span data-ttu-id="a8bec-124">4096</span><span class="sxs-lookup"><span data-stu-id="a8bec-124">4096</span></span></p></td>
<td><p><span data-ttu-id="a8bec-125">O mesmo que <strong>adXactCursorStability</strong>.</span><span class="sxs-lookup"><span data-stu-id="a8bec-125">Same as <strong>adXactCursorStability</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8bec-126"><strong>adXactRepeatableRead</strong></span><span class="sxs-lookup"><span data-stu-id="a8bec-126"><strong>adXactRepeatableRead</strong></span></span></p></td>
<td><p><span data-ttu-id="a8bec-127">65536</span><span class="sxs-lookup"><span data-stu-id="a8bec-127">65536</span></span></p></td>
<td><p><span data-ttu-id="a8bec-128">Indica que a partir de uma transação você não pode ver as alterações feitas em outras transações, mas que a repetição da consulta pode recuperar novos objetos <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="a8bec-128">Indicates that from one transaction you cannot see changes made in other transactions, but that requerying can retrieve new <strong>Recordset</strong> objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8bec-129"><strong>adXactIsolated</strong></span><span class="sxs-lookup"><span data-stu-id="a8bec-129"><strong>adXactIsolated</strong></span></span></p></td>
<td><p><span data-ttu-id="a8bec-130">1048576</span><span class="sxs-lookup"><span data-stu-id="a8bec-130">1048576</span></span></p></td>
<td><p><span data-ttu-id="a8bec-131">Indica que as transações são conduzidas no isolamento de outras transações.</span><span class="sxs-lookup"><span data-stu-id="a8bec-131">Indicates that transactions are conducted in isolation of other transactions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8bec-132"><strong>adXactSerializable</strong></span><span class="sxs-lookup"><span data-stu-id="a8bec-132"><strong>adXactSerializable</strong></span></span></p></td>
<td><p><span data-ttu-id="a8bec-133">1048576</span><span class="sxs-lookup"><span data-stu-id="a8bec-133">1048576</span></span></p></td>
<td><p><span data-ttu-id="a8bec-134">O mesmo que <strong>adXactIsolated</strong>.</span><span class="sxs-lookup"><span data-stu-id="a8bec-134">Same as <strong>adXactIsolated</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a8bec-135">**ADO/WFC Equivalente**</span><span class="sxs-lookup"><span data-stu-id="a8bec-135">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="a8bec-136">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="a8bec-136">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a8bec-137">Constante</span><span class="sxs-lookup"><span data-stu-id="a8bec-137">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a8bec-138">AdoEnums.IsolationLevel.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="a8bec-138">AdoEnums.IsolationLevel.UNSPECIFIED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8bec-139">AdoEnums.IsolationLevel.CHAOS</span><span class="sxs-lookup"><span data-stu-id="a8bec-139">AdoEnums.IsolationLevel.CHAOS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8bec-140">AdoEnums.IsolationLevel.BROWSE</span><span class="sxs-lookup"><span data-stu-id="a8bec-140">AdoEnums.IsolationLevel.BROWSE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8bec-141">AdoEnums.IsolationLevel.READUNCOMMITTED</span><span class="sxs-lookup"><span data-stu-id="a8bec-141">AdoEnums.IsolationLevel.READUNCOMMITTED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8bec-142">AdoEnums.IsolationLevel.CURSORSTABILITY</span><span class="sxs-lookup"><span data-stu-id="a8bec-142">AdoEnums.IsolationLevel.CURSORSTABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8bec-143">AdoEnums.IsolationLevel.READCOMMITTED</span><span class="sxs-lookup"><span data-stu-id="a8bec-143">AdoEnums.IsolationLevel.READCOMMITTED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8bec-144">AdoEnums.IsolationLevel.REPEATABLEREAD</span><span class="sxs-lookup"><span data-stu-id="a8bec-144">AdoEnums.IsolationLevel.REPEATABLEREAD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8bec-145">AdoEnums.IsolationLevel.ISOLATED</span><span class="sxs-lookup"><span data-stu-id="a8bec-145">AdoEnums.IsolationLevel.ISOLATED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8bec-146">AdoEnums.IsolationLevel.SERIALIZABLE</span><span class="sxs-lookup"><span data-stu-id="a8bec-146">AdoEnums.IsolationLevel.SERIALIZABLE</span></span></p></td>
</tr>
</tbody>
</table>

