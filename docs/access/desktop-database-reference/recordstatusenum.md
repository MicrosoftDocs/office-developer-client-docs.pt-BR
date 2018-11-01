---
title: RecordStatusEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: RecordStatusEnum
ms:assetid: 302915b8-494d-0be2-6dce-eaf91a0ea8ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249080(v=office.15)
ms:contentKeyID: 48544022
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: fbff4e9ac28b1c5831131183203dd0d975bfb525
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868970"
---
# <a name="recordstatusenum"></a><span data-ttu-id="de3c6-102">RecordStatusEnum</span><span class="sxs-lookup"><span data-stu-id="de3c6-102">RecordStatusEnum</span></span>

<span data-ttu-id="de3c6-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="de3c6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="de3c6-104">Especifica o status de um registro com relação a atualizações de batch e outras operações em massa.</span><span class="sxs-lookup"><span data-stu-id="de3c6-104">Specifies the status of a record with regard to batch updates and other bulk operations.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="de3c6-105">Constante</span><span class="sxs-lookup"><span data-stu-id="de3c6-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="de3c6-106">Valor</span><span class="sxs-lookup"><span data-stu-id="de3c6-106">Value</span></span></p></th>
<th><p><span data-ttu-id="de3c6-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="de3c6-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="de3c6-108"><strong>adRecCanceled</strong></span><span class="sxs-lookup"><span data-stu-id="de3c6-108"><strong>adRecCanceled</strong></span></span></p></td>
<td><p><span data-ttu-id="de3c6-109">0x100</span><span class="sxs-lookup"><span data-stu-id="de3c6-109">0x100</span></span></p></td>
<td><p><span data-ttu-id="de3c6-110">Indica que o registro não foi salvo porque a operação foi cancelada.</span><span class="sxs-lookup"><span data-stu-id="de3c6-110">Indicates that the record was not saved because the operation was canceled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de3c6-111"><strong>adRecCantRelease</strong></span><span class="sxs-lookup"><span data-stu-id="de3c6-111"><strong>adRecCantRelease</strong></span></span></p></td>
<td><p><span data-ttu-id="de3c6-112">0x400</span><span class="sxs-lookup"><span data-stu-id="de3c6-112">0x400</span></span></p></td>
<td><p><span data-ttu-id="de3c6-113">Indica que o novo registro não foi salvo porque o registro existente foi bloqueado.</span><span class="sxs-lookup"><span data-stu-id="de3c6-113">Indicates that the new record was not saved because the existing record was locked.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de3c6-114"><strong>adRecConcurrencyViolation</strong></span><span class="sxs-lookup"><span data-stu-id="de3c6-114"><strong>adRecConcurrencyViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="de3c6-115">0x800</span><span class="sxs-lookup"><span data-stu-id="de3c6-115">0x800</span></span></p></td>
<td><p><span data-ttu-id="de3c6-116">Indica que o registro não foi salvo porque a concorrência otimista estava em uso.</span><span class="sxs-lookup"><span data-stu-id="de3c6-116">Indicates that the record was not saved because optimistic concurrency was in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de3c6-117"><strong>adRecDBDeleted</strong></span><span class="sxs-lookup"><span data-stu-id="de3c6-117"><strong>adRecDBDeleted</strong></span></span></p></td>
<td><p><span data-ttu-id="de3c6-118">0x40000</span><span class="sxs-lookup"><span data-stu-id="de3c6-118">0x40000</span></span></p></td>
<td><p><span data-ttu-id="de3c6-119">Indica que o registro já foi excluído da origem de dados.</span><span class="sxs-lookup"><span data-stu-id="de3c6-119">Indicates that the record has already been deleted from the data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de3c6-120"><strong>adRecDeleted</strong></span><span class="sxs-lookup"><span data-stu-id="de3c6-120"><strong>adRecDeleted</strong></span></span></p></td>
<td><p><span data-ttu-id="de3c6-121">0x4</span><span class="sxs-lookup"><span data-stu-id="de3c6-121">0x4</span></span></p></td>
<td><p><span data-ttu-id="de3c6-122">Indica que o registro foi excluído.</span><span class="sxs-lookup"><span data-stu-id="de3c6-122">Indicates that the record was deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de3c6-123"><strong>adRecIntegrityViolation</strong></span><span class="sxs-lookup"><span data-stu-id="de3c6-123"><strong>adRecIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="de3c6-124">0x1000</span><span class="sxs-lookup"><span data-stu-id="de3c6-124">0x1000</span></span></p></td>
<td><p><span data-ttu-id="de3c6-125">Indica que o registro não foi salvo porque o usuário violou as restrições de integridade.</span><span class="sxs-lookup"><span data-stu-id="de3c6-125">Indicates that the record was not saved because the user violated integrity constraints.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de3c6-126"><strong>adRecInvalid</strong></span><span class="sxs-lookup"><span data-stu-id="de3c6-126"><strong>adRecInvalid</strong></span></span></p></td>
<td><p><span data-ttu-id="de3c6-127">0x10</span><span class="sxs-lookup"><span data-stu-id="de3c6-127">0x10</span></span></p></td>
<td><p><span data-ttu-id="de3c6-128">Indica que o registro não foi salvo porque seu indicador é inválido.</span><span class="sxs-lookup"><span data-stu-id="de3c6-128">Indicates that the record was not saved because its bookmark is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de3c6-129"><strong>adRecMaxChangesExceeded</strong></span><span class="sxs-lookup"><span data-stu-id="de3c6-129"><strong>adRecMaxChangesExceeded</strong></span></span></p></td>
<td><p><span data-ttu-id="de3c6-130">0x2000</span><span class="sxs-lookup"><span data-stu-id="de3c6-130">0x2000</span></span></p></td>
<td><p><span data-ttu-id="de3c6-131">Indica que o registro não foi salvo porque havia muitas alterações pendentes.</span><span class="sxs-lookup"><span data-stu-id="de3c6-131">Indicates that the record was not saved because there were too many pending changes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de3c6-132"><strong>adRecModified</strong></span><span class="sxs-lookup"><span data-stu-id="de3c6-132"><strong>adRecModified</strong></span></span></p></td>
<td><p><span data-ttu-id="de3c6-133">0x2</span><span class="sxs-lookup"><span data-stu-id="de3c6-133">0x2</span></span></p></td>
<td><p><span data-ttu-id="de3c6-134">Indica que o registro foi modificado.</span><span class="sxs-lookup"><span data-stu-id="de3c6-134">Indicates that the record was modified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de3c6-135"><strong>adRecMultipleChanges</strong></span><span class="sxs-lookup"><span data-stu-id="de3c6-135"><strong>adRecMultipleChanges</strong></span></span></p></td>
<td><p><span data-ttu-id="de3c6-136">0x40</span><span class="sxs-lookup"><span data-stu-id="de3c6-136">0x40</span></span></p></td>
<td><p><span data-ttu-id="de3c6-137">Indica que o registro não foi salvo porque teria afetado vários registros.</span><span class="sxs-lookup"><span data-stu-id="de3c6-137">Indicates that the record was not saved because it would have affected multiple records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de3c6-138"><strong>adRecNew</strong></span><span class="sxs-lookup"><span data-stu-id="de3c6-138"><strong>adRecNew</strong></span></span></p></td>
<td><p><span data-ttu-id="de3c6-139">0x1</span><span class="sxs-lookup"><span data-stu-id="de3c6-139">0x1</span></span></p></td>
<td><p><span data-ttu-id="de3c6-140">Indica que o registro é novo.</span><span class="sxs-lookup"><span data-stu-id="de3c6-140">Indicates that the record is new.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de3c6-141"><strong>adRecObjectOpen</strong></span><span class="sxs-lookup"><span data-stu-id="de3c6-141"><strong>adRecObjectOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="de3c6-142">0x4000</span><span class="sxs-lookup"><span data-stu-id="de3c6-142">0x4000</span></span></p></td>
<td><p><span data-ttu-id="de3c6-143">Indica que o registro não foi salvo devido a um conflito com um objeto de repositório aberto.</span><span class="sxs-lookup"><span data-stu-id="de3c6-143">Indicates that the record was not saved because of a conflict with an open storage object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de3c6-144"><strong>adRecOK</strong></span><span class="sxs-lookup"><span data-stu-id="de3c6-144"><strong>adRecOK</strong></span></span></p></td>
<td><p><span data-ttu-id="de3c6-145">0</span><span class="sxs-lookup"><span data-stu-id="de3c6-145">0</span></span></p></td>
<td><p><span data-ttu-id="de3c6-146">Indica que o registro foi atualizado com êxito.</span><span class="sxs-lookup"><span data-stu-id="de3c6-146">Indicates that the record was successfully updated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de3c6-147"><strong>adRecOutOfMemory</strong></span><span class="sxs-lookup"><span data-stu-id="de3c6-147"><strong>adRecOutOfMemory</strong></span></span></p></td>
<td><p><span data-ttu-id="de3c6-148">0x8000</span><span class="sxs-lookup"><span data-stu-id="de3c6-148">0x8000</span></span></p></td>
<td><p><span data-ttu-id="de3c6-149">Indica que o registro não foi salvo porque o computador ficou sem memória.</span><span class="sxs-lookup"><span data-stu-id="de3c6-149">Indicates that the record was not saved because the computer has run out of memory.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de3c6-150"><strong>adRecPendingChanges</strong></span><span class="sxs-lookup"><span data-stu-id="de3c6-150"><strong>adRecPendingChanges</strong></span></span></p></td>
<td><p><span data-ttu-id="de3c6-151">0x80</span><span class="sxs-lookup"><span data-stu-id="de3c6-151">0x80</span></span></p></td>
<td><p><span data-ttu-id="de3c6-152">Indica que o registro não foi salvo porque se refere a uma inserção pendente.</span><span class="sxs-lookup"><span data-stu-id="de3c6-152">Indicates that the record was not saved because it refers to a pending insert.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de3c6-153"><strong>adRecPermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="de3c6-153"><strong>adRecPermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="de3c6-154">0x10000</span><span class="sxs-lookup"><span data-stu-id="de3c6-154">0x10000</span></span></p></td>
<td><p><span data-ttu-id="de3c6-155">Indica que o registro não foi salvo porque o usuário possui permissões insuficientes.</span><span class="sxs-lookup"><span data-stu-id="de3c6-155">Indicates that the record was not saved because the user has insufficient permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de3c6-156"><strong>adRecSchemaViolation</strong></span><span class="sxs-lookup"><span data-stu-id="de3c6-156"><strong>adRecSchemaViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="de3c6-157">0x20000</span><span class="sxs-lookup"><span data-stu-id="de3c6-157">0x20000</span></span></p></td>
<td><p><span data-ttu-id="de3c6-158">Indica que o registro não foi salvo porque viola a estrutura do banco de dados de base.</span><span class="sxs-lookup"><span data-stu-id="de3c6-158">Indicates that the record was not saved because it violates the structure of the underlying database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de3c6-159"><strong>adRecUnmodified</strong></span><span class="sxs-lookup"><span data-stu-id="de3c6-159"><strong>adRecUnmodified</strong></span></span></p></td>
<td><p><span data-ttu-id="de3c6-160">0x8</span><span class="sxs-lookup"><span data-stu-id="de3c6-160">0x8</span></span></p></td>
<td><p><span data-ttu-id="de3c6-161">Indica que o registro não foi modificado.</span><span class="sxs-lookup"><span data-stu-id="de3c6-161">Indicates that the record was not modified.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="de3c6-162">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="de3c6-162">ADO/WFC equivalent</span></span>

<span data-ttu-id="de3c6-163">AdoEnums.RecordStatus.</span><span class="sxs-lookup"><span data-stu-id="de3c6-163">AdoEnums.RecordStatus.</span></span>

<span data-ttu-id="de3c6-164">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="de3c6-164">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="de3c6-165">Constante</span><span class="sxs-lookup"><span data-stu-id="de3c6-165">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="de3c6-166">AdoEnums.RecordStatus.CANCELED</span><span class="sxs-lookup"><span data-stu-id="de3c6-166">AdoEnums.RecordStatus.CANCELED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de3c6-167">AdoEnums.RecordStatus.CANTRELEASE</span><span class="sxs-lookup"><span data-stu-id="de3c6-167">AdoEnums.RecordStatus.CANTRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de3c6-168">AdoEnums.RecordStatus.CONCURRENCYVIOLATION</span><span class="sxs-lookup"><span data-stu-id="de3c6-168">AdoEnums.RecordStatus.CONCURRENCYVIOLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de3c6-169">AdoEnums.RecordStatus.DBDELETED</span><span class="sxs-lookup"><span data-stu-id="de3c6-169">AdoEnums.RecordStatus.DBDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de3c6-170">AdoEnums.RecordStatus.DELETED</span><span class="sxs-lookup"><span data-stu-id="de3c6-170">AdoEnums.RecordStatus.DELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de3c6-171">AdoEnums.RecordStatus.INTEGRITYVIOLATION</span><span class="sxs-lookup"><span data-stu-id="de3c6-171">AdoEnums.RecordStatus.INTEGRITYVIOLATION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de3c6-172">AdoEnums.RecordStatus.INVALID</span><span class="sxs-lookup"><span data-stu-id="de3c6-172">AdoEnums.RecordStatus.INVALID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de3c6-173">AdoEnums.RecordStatus.MAXCHANGESEXCEEDED</span><span class="sxs-lookup"><span data-stu-id="de3c6-173">AdoEnums.RecordStatus.MAXCHANGESEXCEEDED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de3c6-174">AdoEnums.RecordStatus.MODIFIED</span><span class="sxs-lookup"><span data-stu-id="de3c6-174">AdoEnums.RecordStatus.MODIFIED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de3c6-175">AdoEnums.RecordStatus.MULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="de3c6-175">AdoEnums.RecordStatus.MULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de3c6-176">AdoEnums.RecordStatus.NEW</span><span class="sxs-lookup"><span data-stu-id="de3c6-176">AdoEnums.RecordStatus.NEW</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de3c6-177">AdoEnums.RecordStatus.OBJECTOPEN</span><span class="sxs-lookup"><span data-stu-id="de3c6-177">AdoEnums.RecordStatus.OBJECTOPEN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de3c6-178">AdoEnums.RecordStatus.OK</span><span class="sxs-lookup"><span data-stu-id="de3c6-178">AdoEnums.RecordStatus.OK</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de3c6-179">AdoEnums.RecordStatus.OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="de3c6-179">AdoEnums.RecordStatus.OUTOFMEMORY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de3c6-180">AdoEnums.RecordStatus.PENDINGCHANGES</span><span class="sxs-lookup"><span data-stu-id="de3c6-180">AdoEnums.RecordStatus.PENDINGCHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de3c6-181">AdoEnums.RecordStatus.PERMISSIONDENIED</span><span class="sxs-lookup"><span data-stu-id="de3c6-181">AdoEnums.RecordStatus.PERMISSIONDENIED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de3c6-182">AdoEnums.RecordStatus.SCHEMAVIOLATION</span><span class="sxs-lookup"><span data-stu-id="de3c6-182">AdoEnums.RecordStatus.SCHEMAVIOLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de3c6-183">AdoEnums.RecordStatus.UNMODIFIED</span><span class="sxs-lookup"><span data-stu-id="de3c6-183">AdoEnums.RecordStatus.UNMODIFIED</span></span></p></td>
</tr>
</tbody>
</table>

