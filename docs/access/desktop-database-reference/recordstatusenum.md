---
title: RecordStatusEnum (referência do banco de dados de área de trabalho do Access)
TOCTitle: RecordStatusEnum
ms:assetid: 302915b8-494d-0be2-6dce-eaf91a0ea8ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249080(v=office.15)
ms:contentKeyID: 48544022
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a83de7730224c5ecd5080c795d38cf2e9a3305a9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309377"
---
# <a name="recordstatusenum"></a><span data-ttu-id="f40b0-102">RecordStatusEnum</span><span class="sxs-lookup"><span data-stu-id="f40b0-102">RecordStatusEnum</span></span>

<span data-ttu-id="f40b0-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f40b0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f40b0-104">Especifica o status de um registro com relação a atualizações de batch e outras operações em massa.</span><span class="sxs-lookup"><span data-stu-id="f40b0-104">Specifies the status of a record with regard to batch updates and other bulk operations.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f40b0-105">Constant</span><span class="sxs-lookup"><span data-stu-id="f40b0-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="f40b0-106">Valor</span><span class="sxs-lookup"><span data-stu-id="f40b0-106">Value</span></span></p></th>
<th><p><span data-ttu-id="f40b0-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="f40b0-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f40b0-108"><strong>adRecCanceled</strong></span><span class="sxs-lookup"><span data-stu-id="f40b0-108"><strong>adRecCanceled</strong></span></span></p></td>
<td><p><span data-ttu-id="f40b0-109">0x100</span><span class="sxs-lookup"><span data-stu-id="f40b0-109">0x100</span></span></p></td>
<td><p><span data-ttu-id="f40b0-110">Indica que o registro não foi salvo porque a operação foi cancelada.</span><span class="sxs-lookup"><span data-stu-id="f40b0-110">Indicates that the record was not saved because the operation was canceled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f40b0-111"><strong>adRecCantRelease</strong></span><span class="sxs-lookup"><span data-stu-id="f40b0-111"><strong>adRecCantRelease</strong></span></span></p></td>
<td><p><span data-ttu-id="f40b0-112">0x400</span><span class="sxs-lookup"><span data-stu-id="f40b0-112">0x400</span></span></p></td>
<td><p><span data-ttu-id="f40b0-113">Indica que o novo registro não foi salvo porque o registro existente foi bloqueado.</span><span class="sxs-lookup"><span data-stu-id="f40b0-113">Indicates that the new record was not saved because the existing record was locked.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f40b0-114"><strong>adRecConcurrencyViolation</strong></span><span class="sxs-lookup"><span data-stu-id="f40b0-114"><strong>adRecConcurrencyViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="f40b0-115">0x800</span><span class="sxs-lookup"><span data-stu-id="f40b0-115">0x800</span></span></p></td>
<td><p><span data-ttu-id="f40b0-116">Indica que o registro não foi salvo porque a concorrência otimista estava em uso.</span><span class="sxs-lookup"><span data-stu-id="f40b0-116">Indicates that the record was not saved because optimistic concurrency was in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f40b0-117"><strong>adRecDBDeleted</strong></span><span class="sxs-lookup"><span data-stu-id="f40b0-117"><strong>adRecDBDeleted</strong></span></span></p></td>
<td><p><span data-ttu-id="f40b0-118">0x40000</span><span class="sxs-lookup"><span data-stu-id="f40b0-118">0x40000</span></span></p></td>
<td><p><span data-ttu-id="f40b0-119">Indica que o registro já foi excluído da origem de dados.</span><span class="sxs-lookup"><span data-stu-id="f40b0-119">Indicates that the record has already been deleted from the data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f40b0-120"><strong>adRecDeleted</strong></span><span class="sxs-lookup"><span data-stu-id="f40b0-120"><strong>adRecDeleted</strong></span></span></p></td>
<td><p><span data-ttu-id="f40b0-121">0x4</span><span class="sxs-lookup"><span data-stu-id="f40b0-121">0x4</span></span></p></td>
<td><p><span data-ttu-id="f40b0-122">Indica que o registro foi excluído.</span><span class="sxs-lookup"><span data-stu-id="f40b0-122">Indicates that the record was deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f40b0-123"><strong>adRecIntegrityViolation</strong></span><span class="sxs-lookup"><span data-stu-id="f40b0-123"><strong>adRecIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="f40b0-124">0x1000</span><span class="sxs-lookup"><span data-stu-id="f40b0-124">0x1000</span></span></p></td>
<td><p><span data-ttu-id="f40b0-125">Indica que o registro não foi salvo porque o usuário violou as restrições de integridade.</span><span class="sxs-lookup"><span data-stu-id="f40b0-125">Indicates that the record was not saved because the user violated integrity constraints.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f40b0-126"><strong>adRecInvalid</strong></span><span class="sxs-lookup"><span data-stu-id="f40b0-126"><strong>adRecInvalid</strong></span></span></p></td>
<td><p><span data-ttu-id="f40b0-127">0x10</span><span class="sxs-lookup"><span data-stu-id="f40b0-127">0x10</span></span></p></td>
<td><p><span data-ttu-id="f40b0-128">Indica que o registro não foi salvo porque seu indicador é inválido.</span><span class="sxs-lookup"><span data-stu-id="f40b0-128">Indicates that the record was not saved because its bookmark is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f40b0-129"><strong>adRecMaxChangesExceeded</strong></span><span class="sxs-lookup"><span data-stu-id="f40b0-129"><strong>adRecMaxChangesExceeded</strong></span></span></p></td>
<td><p><span data-ttu-id="f40b0-130">0x2000</span><span class="sxs-lookup"><span data-stu-id="f40b0-130">0x2000</span></span></p></td>
<td><p><span data-ttu-id="f40b0-131">Indica que o registro não foi salvo porque havia muitas alterações pendentes.</span><span class="sxs-lookup"><span data-stu-id="f40b0-131">Indicates that the record was not saved because there were too many pending changes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f40b0-132"><strong>adRecModified</strong></span><span class="sxs-lookup"><span data-stu-id="f40b0-132"><strong>adRecModified</strong></span></span></p></td>
<td><p><span data-ttu-id="f40b0-133">0x2</span><span class="sxs-lookup"><span data-stu-id="f40b0-133">0x2</span></span></p></td>
<td><p><span data-ttu-id="f40b0-134">Indica que o registro foi modificado.</span><span class="sxs-lookup"><span data-stu-id="f40b0-134">Indicates that the record was modified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f40b0-135"><strong>adRecMultipleChanges</strong></span><span class="sxs-lookup"><span data-stu-id="f40b0-135"><strong>adRecMultipleChanges</strong></span></span></p></td>
<td><p><span data-ttu-id="f40b0-136">0x40</span><span class="sxs-lookup"><span data-stu-id="f40b0-136">0x40</span></span></p></td>
<td><p><span data-ttu-id="f40b0-137">Indica que o registro não foi salvo porque teria afetado vários registros.</span><span class="sxs-lookup"><span data-stu-id="f40b0-137">Indicates that the record was not saved because it would have affected multiple records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f40b0-138"><strong>adRecNew</strong></span><span class="sxs-lookup"><span data-stu-id="f40b0-138"><strong>adRecNew</strong></span></span></p></td>
<td><p><span data-ttu-id="f40b0-139">0x1</span><span class="sxs-lookup"><span data-stu-id="f40b0-139">0x1</span></span></p></td>
<td><p><span data-ttu-id="f40b0-140">Indica que o registro é novo.</span><span class="sxs-lookup"><span data-stu-id="f40b0-140">Indicates that the record is new.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f40b0-141"><strong>adRecObjectOpen</strong></span><span class="sxs-lookup"><span data-stu-id="f40b0-141"><strong>adRecObjectOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="f40b0-142">0x4000</span><span class="sxs-lookup"><span data-stu-id="f40b0-142">0x4000</span></span></p></td>
<td><p><span data-ttu-id="f40b0-143">Indica que o registro não foi salvo devido a um conflito com um objeto de repositório aberto.</span><span class="sxs-lookup"><span data-stu-id="f40b0-143">Indicates that the record was not saved because of a conflict with an open storage object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f40b0-144"><strong>adRecOK</strong></span><span class="sxs-lookup"><span data-stu-id="f40b0-144"><strong>adRecOK</strong></span></span></p></td>
<td><p><span data-ttu-id="f40b0-145">,0</span><span class="sxs-lookup"><span data-stu-id="f40b0-145">0</span></span></p></td>
<td><p><span data-ttu-id="f40b0-146">Indica que o registro foi atualizado com êxito.</span><span class="sxs-lookup"><span data-stu-id="f40b0-146">Indicates that the record was successfully updated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f40b0-147"><strong>adRecOutOfMemory</strong></span><span class="sxs-lookup"><span data-stu-id="f40b0-147"><strong>adRecOutOfMemory</strong></span></span></p></td>
<td><p><span data-ttu-id="f40b0-148">0x8000</span><span class="sxs-lookup"><span data-stu-id="f40b0-148">0x8000</span></span></p></td>
<td><p><span data-ttu-id="f40b0-149">Indica que o registro não foi salvo porque o computador ficou sem memória.</span><span class="sxs-lookup"><span data-stu-id="f40b0-149">Indicates that the record was not saved because the computer has run out of memory.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f40b0-150"><strong>adRecPendingChanges</strong></span><span class="sxs-lookup"><span data-stu-id="f40b0-150"><strong>adRecPendingChanges</strong></span></span></p></td>
<td><p><span data-ttu-id="f40b0-151">0x80</span><span class="sxs-lookup"><span data-stu-id="f40b0-151">0x80</span></span></p></td>
<td><p><span data-ttu-id="f40b0-152">Indica que o registro não foi salvo porque se refere a uma inserção pendente.</span><span class="sxs-lookup"><span data-stu-id="f40b0-152">Indicates that the record was not saved because it refers to a pending insert.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f40b0-153"><strong>adRecPermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="f40b0-153"><strong>adRecPermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="f40b0-154">0x10000</span><span class="sxs-lookup"><span data-stu-id="f40b0-154">0x10000</span></span></p></td>
<td><p><span data-ttu-id="f40b0-155">Indica que o registro não foi salvo porque o usuário possui permissões insuficientes.</span><span class="sxs-lookup"><span data-stu-id="f40b0-155">Indicates that the record was not saved because the user has insufficient permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f40b0-156"><strong>adRecSchemaViolation</strong></span><span class="sxs-lookup"><span data-stu-id="f40b0-156"><strong>adRecSchemaViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="f40b0-157">0x20000</span><span class="sxs-lookup"><span data-stu-id="f40b0-157">0x20000</span></span></p></td>
<td><p><span data-ttu-id="f40b0-158">Indica que o registro não foi salvo porque viola a estrutura do banco de dados de base.</span><span class="sxs-lookup"><span data-stu-id="f40b0-158">Indicates that the record was not saved because it violates the structure of the underlying database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f40b0-159"><strong>adRecUnmodified</strong></span><span class="sxs-lookup"><span data-stu-id="f40b0-159"><strong>adRecUnmodified</strong></span></span></p></td>
<td><p><span data-ttu-id="f40b0-160">0x8</span><span class="sxs-lookup"><span data-stu-id="f40b0-160">0x8</span></span></p></td>
<td><p><span data-ttu-id="f40b0-161">Indica que o registro não foi modificado.</span><span class="sxs-lookup"><span data-stu-id="f40b0-161">Indicates that the record was not modified.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="f40b0-162">Equivalente do ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="f40b0-162">ADO/WFC equivalent</span></span>

<span data-ttu-id="f40b0-163">AdoEnums. RecordStatus.</span><span class="sxs-lookup"><span data-stu-id="f40b0-163">AdoEnums.RecordStatus.</span></span>

<span data-ttu-id="f40b0-164">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="f40b0-164">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f40b0-165">Constant</span><span class="sxs-lookup"><span data-stu-id="f40b0-165">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f40b0-166">AdoEnums. RecordStatus. canCELAdo</span><span class="sxs-lookup"><span data-stu-id="f40b0-166">AdoEnums.RecordStatus.CANCELED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f40b0-167">AdoEnums. RecordStatus. CANTRELEASE</span><span class="sxs-lookup"><span data-stu-id="f40b0-167">AdoEnums.RecordStatus.CANTRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f40b0-168">AdoEnums. RecordStatus. CONCURRENCYVIOLATION</span><span class="sxs-lookup"><span data-stu-id="f40b0-168">AdoEnums.RecordStatus.CONCURRENCYVIOLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f40b0-169">AdoEnums. RecordStatus. DBDELETED</span><span class="sxs-lookup"><span data-stu-id="f40b0-169">AdoEnums.RecordStatus.DBDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f40b0-170">AdoEnums. RecordStatus. DELETED</span><span class="sxs-lookup"><span data-stu-id="f40b0-170">AdoEnums.RecordStatus.DELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f40b0-171">AdoEnums. RecordStatus. INTEGRITYVIOLATION</span><span class="sxs-lookup"><span data-stu-id="f40b0-171">AdoEnums.RecordStatus.INTEGRITYVIOLATION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f40b0-172">AdoEnums. RecordStatus. INVALID</span><span class="sxs-lookup"><span data-stu-id="f40b0-172">AdoEnums.RecordStatus.INVALID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f40b0-173">AdoEnums. RecordStatus. MAXCHANGESEXCEEDED</span><span class="sxs-lookup"><span data-stu-id="f40b0-173">AdoEnums.RecordStatus.MAXCHANGESEXCEEDED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f40b0-174">AdoEnums. RecordStatus. MODIFIED</span><span class="sxs-lookup"><span data-stu-id="f40b0-174">AdoEnums.RecordStatus.MODIFIED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f40b0-175">AdoEnums. RecordStatus. MULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="f40b0-175">AdoEnums.RecordStatus.MULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f40b0-176">AdoEnums. RecordStatus. NEW</span><span class="sxs-lookup"><span data-stu-id="f40b0-176">AdoEnums.RecordStatus.NEW</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f40b0-177">AdoEnums. RecordStatus. objectOPEN</span><span class="sxs-lookup"><span data-stu-id="f40b0-177">AdoEnums.RecordStatus.OBJECTOPEN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f40b0-178">AdoEnums. RecordStatus. OK</span><span class="sxs-lookup"><span data-stu-id="f40b0-178">AdoEnums.RecordStatus.OK</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f40b0-179">AdoEnums. RecordStatus. OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="f40b0-179">AdoEnums.RecordStatus.OUTOFMEMORY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f40b0-180">AdoEnums. RecordStatus. PENDINGCHANGES</span><span class="sxs-lookup"><span data-stu-id="f40b0-180">AdoEnums.RecordStatus.PENDINGCHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f40b0-181">AdoEnums. RecordStatus. PERMISSIONDENIED</span><span class="sxs-lookup"><span data-stu-id="f40b0-181">AdoEnums.RecordStatus.PERMISSIONDENIED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f40b0-182">AdoEnums. RecordStatus. SCHEMAVIOLATION</span><span class="sxs-lookup"><span data-stu-id="f40b0-182">AdoEnums.RecordStatus.SCHEMAVIOLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f40b0-183">AdoEnums. RecordStatus. unMODIFIED</span><span class="sxs-lookup"><span data-stu-id="f40b0-183">AdoEnums.RecordStatus.UNMODIFIED</span></span></p></td>
</tr>
</tbody>
</table>

