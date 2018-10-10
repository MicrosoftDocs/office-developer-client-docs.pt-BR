---
title: CursorTypeEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: CursorTypeEnum
ms:assetid: 7c5fa8b2-85ea-a0a7-41f1-a78650aced3e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249519(v=office.15)
ms:contentKeyID: 48545835
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c254c41bb066887e659c86a29ec4a91ca0de9cdd
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464827"
---
# <a name="cursortypeenum"></a><span data-ttu-id="34444-102">CursorTypeEnum</span><span class="sxs-lookup"><span data-stu-id="34444-102">CursorTypeEnum</span></span>


<span data-ttu-id="34444-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="34444-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="34444-104">Especifica o tipo de cursor usado em um objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="34444-104">Specifies the type of cursor used in a [Recordset](recordset-object-ado.md) object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="34444-105">Constant</span><span class="sxs-lookup"><span data-stu-id="34444-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="34444-106">Valor</span><span class="sxs-lookup"><span data-stu-id="34444-106">Value</span></span></p></th>
<th><p><span data-ttu-id="34444-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="34444-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="34444-108"><strong>adOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="34444-108"><strong>adOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="34444-109">2</span><span class="sxs-lookup"><span data-stu-id="34444-109">2</span></span></p></td>
<td><p><span data-ttu-id="34444-p101">Usa um cursor dinâmico. As adições, alterações e exclusões feitas por outros usuários estão visíveis e são permitidos todos os tipos de movimento pelo <strong>Recordset</strong>, exceto para os marcadores, se o provedor não oferecer suporte a eles.</span><span class="sxs-lookup"><span data-stu-id="34444-p101">Uses a dynamic cursor. Additions, changes, and deletions by other users are visible, and all types of movement through the <strong>Recordset</strong> are allowed, except for bookmarks, if the provider doesn't support them.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34444-112"><strong>adOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="34444-112"><strong>adOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="34444-113">0</span><span class="sxs-lookup"><span data-stu-id="34444-113">0</span></span></p></td>
<td><p><span data-ttu-id="34444-p102">Padrão. Usa um cursor somente de encaminhamento. Idêntico a um cursor estático, exceto que você pode rolar para frente somente pelos registros. Isso melhora o desempenho quando você precisa fazer apenas uma passagem por um <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="34444-p102">Default. Uses a forward-only cursor. Identical to a static cursor, except that you can only scroll forward through records. This improves performance when you need to make only one pass through a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34444-118"><strong>adOpenKeyset</strong></span><span class="sxs-lookup"><span data-stu-id="34444-118"><strong>adOpenKeyset</strong></span></span></p></td>
<td><p><span data-ttu-id="34444-119">1</span><span class="sxs-lookup"><span data-stu-id="34444-119">1</span></span></p></td>
<td><p><span data-ttu-id="34444-p103">Usa um cursor de conjunto de chaves. Como um cursor dinâmico, exceto que você não pode ver os registros que outros usuários adicionam, embora os registros que outros usuários excluem estejam inacessíveis a partir do seu <strong>Recordset</strong>. As alterações de dados feitas por outros usuários ainda estão visíveis.</span><span class="sxs-lookup"><span data-stu-id="34444-p103">Uses a keyset cursor. Like a dynamic cursor, except that you can't see records that other users add, although records that other users delete are inaccessible from your <strong>Recordset</strong>. Data changes by other users are still visible.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34444-123"><strong>adOpenStatic</strong></span><span class="sxs-lookup"><span data-stu-id="34444-123"><strong>adOpenStatic</strong></span></span></p></td>
<td><p><span data-ttu-id="34444-124">3</span><span class="sxs-lookup"><span data-stu-id="34444-124">3</span></span></p></td>
<td><p><span data-ttu-id="34444-p104">Usa um cursor estático. Uma cópia estática de um conjunto de registros que você pode usar para localizar dados ou gerar relatórios. As adições, alterações ou exclusões feitas por outros usuários não estão visíveis.</span><span class="sxs-lookup"><span data-stu-id="34444-p104">Uses a static cursor. A static copy of a set of records that you can use to find data or generate reports. Additions, changes, or deletions by other users are not visible.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34444-128"><strong>adOpenUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="34444-128"><strong>adOpenUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="34444-129">-1</span><span class="sxs-lookup"><span data-stu-id="34444-129">-1</span></span></p></td>
<td><p><span data-ttu-id="34444-130">Não especifica o tipo de cursor.</span><span class="sxs-lookup"><span data-stu-id="34444-130">Does not specify the type of cursor.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="34444-131">**ADO/WFC Equivalente**</span><span class="sxs-lookup"><span data-stu-id="34444-131">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="34444-132">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="34444-132">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="34444-133">Constante</span><span class="sxs-lookup"><span data-stu-id="34444-133">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="34444-134">AdoEnums.CursorType.DYNAMIC</span><span class="sxs-lookup"><span data-stu-id="34444-134">AdoEnums.CursorType.DYNAMIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34444-135">AdoEnums.CursorType.FORWARDONLY</span><span class="sxs-lookup"><span data-stu-id="34444-135">AdoEnums.CursorType.FORWARDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34444-136">AdoEnums.CursorType.KEYSET</span><span class="sxs-lookup"><span data-stu-id="34444-136">AdoEnums.CursorType.KEYSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34444-137">AdoEnums.CursorType.STATIC</span><span class="sxs-lookup"><span data-stu-id="34444-137">AdoEnums.CursorType.STATIC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34444-138">AdoEnums.CursorType.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="34444-138">AdoEnums.CursorType.UNSPECIFIED</span></span></p></td>
</tr>
</tbody>
</table>

