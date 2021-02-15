---
title: CursorTypeEnum (referência do banco de dados da área de trabalho do Access)
TOCTitle: CursorTypeEnum
ms:assetid: 7c5fa8b2-85ea-a0a7-41f1-a78650aced3e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249519(v=office.15)
ms:contentKeyID: 48545835
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0bcaaa1298f12d72c5e836dcfe1e74cdcda68d19
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295160"
---
# <a name="cursortypeenum"></a><span data-ttu-id="39c7a-102">CursorTypeEnum</span><span class="sxs-lookup"><span data-stu-id="39c7a-102">CursorTypeEnum</span></span>

<span data-ttu-id="39c7a-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="39c7a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="39c7a-104">Especifica o tipo de cursor usado em um objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="39c7a-104">Specifies the type of cursor used in a [Recordset](recordset-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="39c7a-105">Constant</span><span class="sxs-lookup"><span data-stu-id="39c7a-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="39c7a-106">Valor</span><span class="sxs-lookup"><span data-stu-id="39c7a-106">Value</span></span></p></th>
<th><p><span data-ttu-id="39c7a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="39c7a-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="39c7a-108"><strong>adOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="39c7a-108"><strong>adOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="39c7a-109">2 </span><span class="sxs-lookup"><span data-stu-id="39c7a-109">2</span></span></p></td>
<td><p><span data-ttu-id="39c7a-p101">Usa um cursor dinâmico. As adições, alterações e exclusões feitas por outros usuários estão visíveis e são permitidos todos os tipos de movimento pelo <strong>Recordset</strong>, exceto para os marcadores, se o provedor não oferecer suporte a eles.</span><span class="sxs-lookup"><span data-stu-id="39c7a-p101">Uses a dynamic cursor. Additions, changes, and deletions by other users are visible, and all types of movement through the <strong>Recordset</strong> are allowed, except for bookmarks, if the provider doesn't support them.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39c7a-112"><strong>adOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="39c7a-112"><strong>adOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="39c7a-113">0</span><span class="sxs-lookup"><span data-stu-id="39c7a-113">0</span></span></p></td>
<td><p><span data-ttu-id="39c7a-p102">Padrão. Usa um cursor somente de encaminhamento. Idêntico a um cursor estático, exceto que você pode rolar para frente somente pelos registros. Isso melhora o desempenho quando você precisa fazer apenas uma passagem por um <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="39c7a-p102">Default. Uses a forward-only cursor. Identical to a static cursor, except that you can only scroll forward through records. This improves performance when you need to make only one pass through a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39c7a-118"><strong>adOpenKeyset</strong></span><span class="sxs-lookup"><span data-stu-id="39c7a-118"><strong>adOpenKeyset</strong></span></span></p></td>
<td><p><span data-ttu-id="39c7a-119">1 </span><span class="sxs-lookup"><span data-stu-id="39c7a-119">1</span></span></p></td>
<td><p><span data-ttu-id="39c7a-p103">Usa um cursor de conjunto de chaves. Como um cursor dinâmico, exceto que você não pode ver os registros que outros usuários adicionam, embora os registros que outros usuários excluem estejam inacessíveis a partir do seu <strong>Recordset</strong>. As alterações de dados feitas por outros usuários ainda estão visíveis.</span><span class="sxs-lookup"><span data-stu-id="39c7a-p103">Uses a keyset cursor. Like a dynamic cursor, except that you can't see records that other users add, although records that other users delete are inaccessible from your <strong>Recordset</strong>. Data changes by other users are still visible.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39c7a-123"><strong>adOpenStatic</strong></span><span class="sxs-lookup"><span data-stu-id="39c7a-123"><strong>adOpenStatic</strong></span></span></p></td>
<td><p><span data-ttu-id="39c7a-124">3 </span><span class="sxs-lookup"><span data-stu-id="39c7a-124">3</span></span></p></td>
<td><p><span data-ttu-id="39c7a-p104">Usa um cursor estático. Uma cópia estática de um conjunto de registros que você pode usar para localizar dados ou gerar relatórios. As adições, alterações ou exclusões feitas por outros usuários não estão visíveis.</span><span class="sxs-lookup"><span data-stu-id="39c7a-p104">Uses a static cursor. A static copy of a set of records that you can use to find data or generate reports. Additions, changes, or deletions by other users are not visible.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39c7a-128"><strong>adOpenUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="39c7a-128"><strong>adOpenUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="39c7a-129">-1</span><span class="sxs-lookup"><span data-stu-id="39c7a-129">-1</span></span></p></td>
<td><p><span data-ttu-id="39c7a-130">Não especifica o tipo de cursor.</span><span class="sxs-lookup"><span data-stu-id="39c7a-130">Does not specify the type of cursor.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="39c7a-131">Equivalente do ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="39c7a-131">ADO/WFC equivalent</span></span>

<span data-ttu-id="39c7a-132">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="39c7a-132">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="39c7a-133">Constant</span><span class="sxs-lookup"><span data-stu-id="39c7a-133">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="39c7a-134">AdoEnums.CursorType.DYNAMIC</span><span class="sxs-lookup"><span data-stu-id="39c7a-134">AdoEnums.CursorType.DYNAMIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39c7a-135">AdoEnums.CursorType.FORWARDONLY</span><span class="sxs-lookup"><span data-stu-id="39c7a-135">AdoEnums.CursorType.FORWARDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39c7a-136">AdoEnums.CursorType.KEYSET</span><span class="sxs-lookup"><span data-stu-id="39c7a-136">AdoEnums.CursorType.KEYSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39c7a-137">AdoEnums.CursorType.STATIC</span><span class="sxs-lookup"><span data-stu-id="39c7a-137">AdoEnums.CursorType.STATIC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39c7a-138">AdoEnums.CursorType.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="39c7a-138">AdoEnums.CursorType.UNSPECIFIED</span></span></p></td>
</tr>
</tbody>
</table>

