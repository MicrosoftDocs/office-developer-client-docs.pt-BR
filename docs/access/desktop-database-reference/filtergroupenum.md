---
title: FilterGroupEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: FilterGroupEnum
ms:assetid: 141f8f9a-c188-5937-91cc-3155eaebebd2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248912(v=office.15)
ms:contentKeyID: 48543381
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 5c42b703536e931405325d3a91219a148e6580d1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873282"
---
# <a name="filtergroupenum"></a><span data-ttu-id="0a1b7-102">FilterGroupEnum</span><span class="sxs-lookup"><span data-stu-id="0a1b7-102">FilterGroupEnum</span></span>

<span data-ttu-id="0a1b7-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="0a1b7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0a1b7-104">Especifica o grupo de registros a serem filtrados a partir de um [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="0a1b7-104">Specifies the group of records to be filtered from a [Recordset](recordset-object-ado.md).</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0a1b7-105">Constant</span><span class="sxs-lookup"><span data-stu-id="0a1b7-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="0a1b7-106">Valor</span><span class="sxs-lookup"><span data-stu-id="0a1b7-106">Value</span></span></p></th>
<th><p><span data-ttu-id="0a1b7-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="0a1b7-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0a1b7-108"><strong>adFilterAffectedRecords</strong></span><span class="sxs-lookup"><span data-stu-id="0a1b7-108"><strong>adFilterAffectedRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="0a1b7-109">2</span><span class="sxs-lookup"><span data-stu-id="0a1b7-109">2</span></span></p></td>
<td><p><span data-ttu-id="0a1b7-110">Filtros para visualizar apenas os registros afetados pela última chamada <a href="delete-method-ado-recordset.md">Delete</a>, <a href="resync-method-ado.md">Resync</a>, <a href="updatebatch-method-ado.md">UpdateBatch</a> ou <a href="cancelbatch-method-ado.md">CancelBatch</a>.</span><span class="sxs-lookup"><span data-stu-id="0a1b7-110">Filters for viewing only records affected by the last <a href="delete-method-ado-recordset.md">Delete</a>, <a href="resync-method-ado.md">Resync</a>, <a href="updatebatch-method-ado.md">UpdateBatch</a>, or <a href="cancelbatch-method-ado.md">CancelBatch</a> call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a1b7-111"><strong>adFilterConflictingRecords</strong></span><span class="sxs-lookup"><span data-stu-id="0a1b7-111"><strong>adFilterConflictingRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="0a1b7-112">5</span><span class="sxs-lookup"><span data-stu-id="0a1b7-112">5</span></span></p></td>
<td><p><span data-ttu-id="0a1b7-113">Filtra para visualizar os registros que falharam na última atualização em lote.</span><span class="sxs-lookup"><span data-stu-id="0a1b7-113">Filters for viewing the records that failed the last batch update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a1b7-114"><strong>adFilterFetchedRecords</strong></span><span class="sxs-lookup"><span data-stu-id="0a1b7-114"><strong>adFilterFetchedRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="0a1b7-115">3</span><span class="sxs-lookup"><span data-stu-id="0a1b7-115">3</span></span></p></td>
<td><p><span data-ttu-id="0a1b7-116">Filtra para visualizar os registros na memória cache atual — ou seja, os resultados da última chamada para recuperar os registros do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0a1b7-116">Filters for viewing the records in the current cache — that is, the results of the last call to retrieve records from the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a1b7-117"><strong>adFilterNone</strong></span><span class="sxs-lookup"><span data-stu-id="0a1b7-117"><strong>adFilterNone</strong></span></span></p></td>
<td><p><span data-ttu-id="0a1b7-118">0</span><span class="sxs-lookup"><span data-stu-id="0a1b7-118">0</span></span></p></td>
<td><p><span data-ttu-id="0a1b7-119">Remove o filtro atual e restaura todos os registros para visualização.</span><span class="sxs-lookup"><span data-stu-id="0a1b7-119">Removes the current filter and restores all records for viewing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a1b7-120"><strong>adFilterPendingRecords</strong></span><span class="sxs-lookup"><span data-stu-id="0a1b7-120"><strong>adFilterPendingRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="0a1b7-121">1</span><span class="sxs-lookup"><span data-stu-id="0a1b7-121">1</span></span></p></td>
<td><p><span data-ttu-id="0a1b7-p101">Filtra para visualizar apenas os registros que foram alterados, mas que ainda não foram enviados ao servidor. Aplicável apenas para o modo de atualização em lote.</span><span class="sxs-lookup"><span data-stu-id="0a1b7-p101">Filters for viewing only records that have changed but have not yet been sent to the server. Applicable only for batch update mode.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="0a1b7-124">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="0a1b7-124">ADO/WFC equivalent</span></span>

<span data-ttu-id="0a1b7-125">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="0a1b7-125">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0a1b7-126">Constante</span><span class="sxs-lookup"><span data-stu-id="0a1b7-126">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0a1b7-127">AdoEnums.FilterGroup.AFFECTEDRECORDS</span><span class="sxs-lookup"><span data-stu-id="0a1b7-127">AdoEnums.FilterGroup.AFFECTEDRECORDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a1b7-128">AdoEnums.FilterGroup.CONFLICTINGRECORDS</span><span class="sxs-lookup"><span data-stu-id="0a1b7-128">AdoEnums.FilterGroup.CONFLICTINGRECORDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a1b7-129">AdoEnums.FilterGroup.FETCHEDRECORDS</span><span class="sxs-lookup"><span data-stu-id="0a1b7-129">AdoEnums.FilterGroup.FETCHEDRECORDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a1b7-130">AdoEnums.FilterGroup.NONE</span><span class="sxs-lookup"><span data-stu-id="0a1b7-130">AdoEnums.FilterGroup.NONE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a1b7-131">AdoEnums.FilterGroup.PENDINGRECORDS</span><span class="sxs-lookup"><span data-stu-id="0a1b7-131">AdoEnums.FilterGroup.PENDINGRECORDS</span></span></p></td>
</tr>
</tbody>
</table>

