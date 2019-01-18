---
title: LockTypeEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: LockTypeEnum
ms:assetid: 966b4952-5591-4a99-82d5-99cb9ae3fc72
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249667(v=office.15)
ms:contentKeyID: 48546448
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d4b9dc49e647bdcd3123ade065da0c74538c9a88
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715365"
---
# <a name="locktypeenum"></a><span data-ttu-id="d9304-102">LockTypeEnum</span><span class="sxs-lookup"><span data-stu-id="d9304-102">LockTypeEnum</span></span>

<span data-ttu-id="d9304-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="d9304-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d9304-104">Especifica o tipo de bloqueio colocado nos registros durante a edição.</span><span class="sxs-lookup"><span data-stu-id="d9304-104">Specifies the type of lock placed on records during editing.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d9304-105">Constante</span><span class="sxs-lookup"><span data-stu-id="d9304-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="d9304-106">Valor</span><span class="sxs-lookup"><span data-stu-id="d9304-106">Value</span></span></p></th>
<th><p><span data-ttu-id="d9304-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="d9304-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d9304-108"><strong>adLockBatchOptimistic</strong></span><span class="sxs-lookup"><span data-stu-id="d9304-108"><strong>adLockBatchOptimistic</strong></span></span></p></td>
<td><p><span data-ttu-id="d9304-109">4</span><span class="sxs-lookup"><span data-stu-id="d9304-109">4</span></span></p></td>
<td><p><span data-ttu-id="d9304-p101">Indica as atualizações em lote otimistas. Exigido para o modo de atualização em lote.</span><span class="sxs-lookup"><span data-stu-id="d9304-p101">Indicates optimistic batch updates. Required for batch update mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9304-112"><strong>adLockOptimistic</strong></span><span class="sxs-lookup"><span data-stu-id="d9304-112"><strong>adLockOptimistic</strong></span></span></p></td>
<td><p><span data-ttu-id="d9304-113">3</span><span class="sxs-lookup"><span data-stu-id="d9304-113">3</span></span></p></td>
<td><p><span data-ttu-id="d9304-p102">Indica o bloqueio otimista, registro por registro. O provedor usa os registros de bloqueio otimistas apenas quando você chama o método <a href="update-method-ado.md">Update</a>.</span><span class="sxs-lookup"><span data-stu-id="d9304-p102">Indicates optimistic locking, record by record. The provider uses optimistic locking, locking records only when you call the <a href="update-method-ado.md">Update</a> method.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9304-116"><strong>adLockPessimistic</strong></span><span class="sxs-lookup"><span data-stu-id="d9304-116"><strong>adLockPessimistic</strong></span></span></p></td>
<td><p><span data-ttu-id="d9304-117">2</span><span class="sxs-lookup"><span data-stu-id="d9304-117">2</span></span></p></td>
<td><p><span data-ttu-id="d9304-p103">Indica o bloqueio pessimista, registro por registro. O provedor faz o que for necessário para garantir a edição bem-sucedida dos registros, geralmente bloqueando os registros na fonte de dados imediatamente após a edição.</span><span class="sxs-lookup"><span data-stu-id="d9304-p103">Indicates pessimistic locking, record by record. The provider does what is necessary to ensure successful editing of the records, usually by locking records at the data source immediately after editing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9304-120"><strong>adLockReadOnly</strong></span><span class="sxs-lookup"><span data-stu-id="d9304-120"><strong>adLockReadOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="d9304-121">1</span><span class="sxs-lookup"><span data-stu-id="d9304-121">1</span></span></p></td>
<td><p><span data-ttu-id="d9304-p104">Indica os registros somente leitura. Não é possível alterar os dados.</span><span class="sxs-lookup"><span data-stu-id="d9304-p104">Indicates read-only records. You cannot alter the data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9304-124"><strong>adLockUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="d9304-124"><strong>adLockUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="d9304-125">-1</span><span class="sxs-lookup"><span data-stu-id="d9304-125">-1</span></span></p></td>
<td><p><span data-ttu-id="d9304-p105">Não especifica um tipo de bloqueio. Para clones, o clone é criado com o mesmo tipo de bloqueio que o original.</span><span class="sxs-lookup"><span data-stu-id="d9304-p105">Does not specify a type of lock. For clones, the clone is created with the same lock type as the original.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="d9304-128">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="d9304-128">ADO/WFC equivalent</span></span>

<span data-ttu-id="d9304-129">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="d9304-129">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d9304-130">Constante</span><span class="sxs-lookup"><span data-stu-id="d9304-130">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d9304-131">AdoEnums.LockType.BATCHOPTIMISTIC</span><span class="sxs-lookup"><span data-stu-id="d9304-131">AdoEnums.LockType.BATCHOPTIMISTIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9304-132">AdoEnums.LockType.OPTIMISTIC</span><span class="sxs-lookup"><span data-stu-id="d9304-132">AdoEnums.LockType.OPTIMISTIC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9304-133">AdoEnums.LockType.PESSIMISTIC</span><span class="sxs-lookup"><span data-stu-id="d9304-133">AdoEnums.LockType.PESSIMISTIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9304-134">AdoEnums.LockType.READONLY</span><span class="sxs-lookup"><span data-stu-id="d9304-134">AdoEnums.LockType.READONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9304-135">AdoEnums.LockType.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="d9304-135">AdoEnums.LockType.UNSPECIFIED</span></span></p></td>
</tr>
</tbody>
</table>

