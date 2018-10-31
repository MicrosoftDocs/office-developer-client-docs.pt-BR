---
title: LockTypeEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: LockTypeEnum
ms:assetid: 966b4952-5591-4a99-82d5-99cb9ae3fc72
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249667(v=office.15)
ms:contentKeyID: 48546448
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 57cef1ca3a31665db1db517c22756213abf49042
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860529"
---
# <a name="locktypeenum"></a><span data-ttu-id="e05ca-102">LockTypeEnum</span><span class="sxs-lookup"><span data-stu-id="e05ca-102">LockTypeEnum</span></span>

<span data-ttu-id="e05ca-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e05ca-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e05ca-104">Especifica o tipo de bloqueio colocado nos registros durante a edição.</span><span class="sxs-lookup"><span data-stu-id="e05ca-104">Specifies the type of lock placed on records during editing.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e05ca-105">Constante</span><span class="sxs-lookup"><span data-stu-id="e05ca-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="e05ca-106">Valor</span><span class="sxs-lookup"><span data-stu-id="e05ca-106">Value</span></span></p></th>
<th><p><span data-ttu-id="e05ca-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="e05ca-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e05ca-108"><strong>adLockBatchOptimistic</strong></span><span class="sxs-lookup"><span data-stu-id="e05ca-108"><strong>adLockBatchOptimistic</strong></span></span></p></td>
<td><p><span data-ttu-id="e05ca-109">4</span><span class="sxs-lookup"><span data-stu-id="e05ca-109">4</span></span></p></td>
<td><p><span data-ttu-id="e05ca-p101">Indica as atualizações em lote otimistas. Exigido para o modo de atualização em lote.</span><span class="sxs-lookup"><span data-stu-id="e05ca-p101">Indicates optimistic batch updates. Required for batch update mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e05ca-112"><strong>adLockOptimistic</strong></span><span class="sxs-lookup"><span data-stu-id="e05ca-112"><strong>adLockOptimistic</strong></span></span></p></td>
<td><p><span data-ttu-id="e05ca-113">3</span><span class="sxs-lookup"><span data-stu-id="e05ca-113">3</span></span></p></td>
<td><p><span data-ttu-id="e05ca-p102">Indica o bloqueio otimista, registro por registro. O provedor usa os registros de bloqueio otimistas apenas quando você chama o método <a href="update-method-ado.md">Update</a>.</span><span class="sxs-lookup"><span data-stu-id="e05ca-p102">Indicates optimistic locking, record by record. The provider uses optimistic locking, locking records only when you call the <a href="update-method-ado.md">Update</a> method.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e05ca-116"><strong>adLockPessimistic</strong></span><span class="sxs-lookup"><span data-stu-id="e05ca-116"><strong>adLockPessimistic</strong></span></span></p></td>
<td><p><span data-ttu-id="e05ca-117">2</span><span class="sxs-lookup"><span data-stu-id="e05ca-117">2</span></span></p></td>
<td><p><span data-ttu-id="e05ca-p103">Indica o bloqueio pessimista, registro por registro. O provedor faz o que for necessário para garantir a edição bem-sucedida dos registros, geralmente bloqueando os registros na fonte de dados imediatamente após a edição.</span><span class="sxs-lookup"><span data-stu-id="e05ca-p103">Indicates pessimistic locking, record by record. The provider does what is necessary to ensure successful editing of the records, usually by locking records at the data source immediately after editing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e05ca-120"><strong>adLockReadOnly</strong></span><span class="sxs-lookup"><span data-stu-id="e05ca-120"><strong>adLockReadOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="e05ca-121">1</span><span class="sxs-lookup"><span data-stu-id="e05ca-121">1</span></span></p></td>
<td><p><span data-ttu-id="e05ca-p104">Indica os registros somente leitura. Não é possível alterar os dados.</span><span class="sxs-lookup"><span data-stu-id="e05ca-p104">Indicates read-only records. You cannot alter the data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e05ca-124"><strong>adLockUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="e05ca-124"><strong>adLockUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="e05ca-125">-1</span><span class="sxs-lookup"><span data-stu-id="e05ca-125">-1</span></span></p></td>
<td><p><span data-ttu-id="e05ca-p105">Não especifica um tipo de bloqueio. Para clones, o clone é criado com o mesmo tipo de bloqueio que o original.</span><span class="sxs-lookup"><span data-stu-id="e05ca-p105">Does not specify a type of lock. For clones, the clone is created with the same lock type as the original.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="e05ca-128">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="e05ca-128">ADO/WFC equivalent</span></span>

<span data-ttu-id="e05ca-129">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="e05ca-129">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e05ca-130">Constante</span><span class="sxs-lookup"><span data-stu-id="e05ca-130">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e05ca-131">AdoEnums.LockType.BATCHOPTIMISTIC</span><span class="sxs-lookup"><span data-stu-id="e05ca-131">AdoEnums.LockType.BATCHOPTIMISTIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e05ca-132">AdoEnums.LockType.OPTIMISTIC</span><span class="sxs-lookup"><span data-stu-id="e05ca-132">AdoEnums.LockType.OPTIMISTIC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e05ca-133">AdoEnums.LockType.PESSIMISTIC</span><span class="sxs-lookup"><span data-stu-id="e05ca-133">AdoEnums.LockType.PESSIMISTIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e05ca-134">AdoEnums.LockType.READONLY</span><span class="sxs-lookup"><span data-stu-id="e05ca-134">AdoEnums.LockType.READONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e05ca-135">AdoEnums.LockType.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="e05ca-135">AdoEnums.LockType.UNSPECIFIED</span></span></p></td>
</tr>
</tbody>
</table>

