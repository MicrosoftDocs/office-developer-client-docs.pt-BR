---
title: CursorOptionEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: CursorOptionEnum
ms:assetid: 3c118c08-02f2-5290-1cef-29e97c35fddc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249155(v=office.15)
ms:contentKeyID: 48544303
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7443e0cb29954fae9dfc193ffc6aa8dee9886089
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701064"
---
# <a name="cursoroptionenum"></a><span data-ttu-id="2e486-102">CursorOptionEnum</span><span class="sxs-lookup"><span data-stu-id="2e486-102">CursorOptionEnum</span></span>

<span data-ttu-id="2e486-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="2e486-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2e486-104">Especifica a funcionalidade para a qual o método [Supports](supports-method-ado.md) deve ser testado.</span><span class="sxs-lookup"><span data-stu-id="2e486-104">Specifies what functionality the [Supports](supports-method-ado.md) method should test for.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2e486-105">Constant</span><span class="sxs-lookup"><span data-stu-id="2e486-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="2e486-106">Valor</span><span class="sxs-lookup"><span data-stu-id="2e486-106">Value</span></span></p></th>
<th><p><span data-ttu-id="2e486-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="2e486-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2e486-108"><strong>adAddNew</strong></span><span class="sxs-lookup"><span data-stu-id="2e486-108"><strong>adAddNew</strong></span></span></p></td>
<td><p><span data-ttu-id="2e486-109">0x1000400</span><span class="sxs-lookup"><span data-stu-id="2e486-109">0x1000400</span></span></p></td>
<td><p><span data-ttu-id="2e486-110">Fornece suporte ao método <a href="addnew-method-ado.md">AddNew</a> para adicionar novos registros.</span><span class="sxs-lookup"><span data-stu-id="2e486-110">Supports the <a href="addnew-method-ado.md">AddNew</a> method to add new records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e486-111"><strong>adApproxPosition</strong></span><span class="sxs-lookup"><span data-stu-id="2e486-111"><strong>adApproxPosition</strong></span></span></p></td>
<td><p><span data-ttu-id="2e486-112">0x4000</span><span class="sxs-lookup"><span data-stu-id="2e486-112">0x4000</span></span></p></td>
<td><p><span data-ttu-id="2e486-113">Fornece suporte às propriedades <a href="absoluteposition-property-ado.md">AbsolutePosition</a> e <a href="absolutepage-property-ado.md">AbsolutePage</a>.</span><span class="sxs-lookup"><span data-stu-id="2e486-113">Supports the <a href="absoluteposition-property-ado.md">AbsolutePosition</a> and <a href="absolutepage-property-ado.md">AbsolutePage</a> properties.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e486-114"><strong>adBookmark</strong></span><span class="sxs-lookup"><span data-stu-id="2e486-114"><strong>adBookmark</strong></span></span></p></td>
<td><p><span data-ttu-id="2e486-115">0x2000</span><span class="sxs-lookup"><span data-stu-id="2e486-115">0x2000</span></span></p></td>
<td><p><span data-ttu-id="2e486-116">Fornece suporte à propriedade <a href="bookmark-property-ado.md">Bookmark</a> para obter acesso a registros específicos.</span><span class="sxs-lookup"><span data-stu-id="2e486-116">Supports the <a href="bookmark-property-ado.md">Bookmark</a> property to gain access to specific records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e486-117"><strong>adDelete</strong></span><span class="sxs-lookup"><span data-stu-id="2e486-117"><strong>adDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="2e486-118">0x1000800</span><span class="sxs-lookup"><span data-stu-id="2e486-118">0x1000800</span></span></p></td>
<td><p><span data-ttu-id="2e486-119">Fornece suporte ao método <a href="delete-method-ado-recordset.md">Delete</a> para excluir registros.</span><span class="sxs-lookup"><span data-stu-id="2e486-119">Supports the <a href="delete-method-ado-recordset.md">Delete</a> method to delete records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e486-120"><strong>adFind</strong></span><span class="sxs-lookup"><span data-stu-id="2e486-120"><strong>adFind</strong></span></span></p></td>
<td><p><span data-ttu-id="2e486-121">0x80000</span><span class="sxs-lookup"><span data-stu-id="2e486-121">0x80000</span></span></p></td>
<td><p><span data-ttu-id="2e486-122">Fornece suporte ao método <a href="find-method-ado.md">Find</a> para localizar uma linha em um <a href="recordset-object-ado.md">Recordset</a>.</span><span class="sxs-lookup"><span data-stu-id="2e486-122">Supports the <a href="find-method-ado.md">Find</a> method to locate a row in a <a href="recordset-object-ado.md">Recordset</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e486-123"><strong>adHoldRecords</strong></span><span class="sxs-lookup"><span data-stu-id="2e486-123"><strong>adHoldRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="2e486-124">0x100</span><span class="sxs-lookup"><span data-stu-id="2e486-124">0x100</span></span></p></td>
<td><p><span data-ttu-id="2e486-125">Recupera mais registros ou alterar a posição seguinte sem confirmar todas as alterações pendentes.</span><span class="sxs-lookup"><span data-stu-id="2e486-125">Retrieves more records or changes the next position without committing all pending changes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e486-126"><strong>adIndex</strong></span><span class="sxs-lookup"><span data-stu-id="2e486-126"><strong>adIndex</strong></span></span></p></td>
<td><p><span data-ttu-id="2e486-127">0x100000</span><span class="sxs-lookup"><span data-stu-id="2e486-127">0x100000</span></span></p></td>
<td><p><span data-ttu-id="2e486-128">Fornece suporte à propriedade <a href="index-property-ado.md">Index</a> para nomear um índice.</span><span class="sxs-lookup"><span data-stu-id="2e486-128">Supports the <a href="index-property-ado.md">Index</a> property to name an index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e486-129"><strong>adMovePrevious</strong></span><span class="sxs-lookup"><span data-stu-id="2e486-129"><strong>adMovePrevious</strong></span></span></p></td>
<td><p><span data-ttu-id="2e486-130">0x200</span><span class="sxs-lookup"><span data-stu-id="2e486-130">0x200</span></span></p></td>
<td><p><span data-ttu-id="2e486-131">Fornece suporte aos métodos <a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a> e <a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a> e aos métodos <a href="move-method-ado.md">Move</a> ou <a href="getrows-method-ado.md">GetRows</a> para mover a posição de registro atual para trás sem exigir indicadores.</span><span class="sxs-lookup"><span data-stu-id="2e486-131">Supports the <a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a> and <a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a> methods, and <a href="move-method-ado.md">Move</a> or <a href="getrows-method-ado.md">GetRows</a> methods to move the current record position backward without requiring bookmarks.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e486-132"><strong>adNotify</strong></span><span class="sxs-lookup"><span data-stu-id="2e486-132"><strong>adNotify</strong></span></span></p></td>
<td><p><span data-ttu-id="2e486-133">0x40000</span><span class="sxs-lookup"><span data-stu-id="2e486-133">0x40000</span></span></p></td>
<td><p><span data-ttu-id="2e486-134">Indica que o provedor de dados subjacente fornece suporte às notificações (o que determina se os eventos <strong>Recordset</strong> são permitidos).</span><span class="sxs-lookup"><span data-stu-id="2e486-134">Indicates that the underlying data provider supports notifications (which determines whether <strong>Recordset</strong> events are supported).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e486-135"><strong>adResync</strong></span><span class="sxs-lookup"><span data-stu-id="2e486-135"><strong>adResync</strong></span></span></p></td>
<td><p><span data-ttu-id="2e486-136">0x20000</span><span class="sxs-lookup"><span data-stu-id="2e486-136">0x20000</span></span></p></td>
<td><p><span data-ttu-id="2e486-137">Fornece suporte ao método <a href="resync-method-ado.md">Resync</a> para atualizar o cursor com os dados visíveis no banco de dados subjacente.</span><span class="sxs-lookup"><span data-stu-id="2e486-137">Supports the <a href="resync-method-ado.md">Resync</a> method to update the cursor with the data that is visible in the underlying database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e486-138"><strong>adSeek</strong></span><span class="sxs-lookup"><span data-stu-id="2e486-138"><strong>adSeek</strong></span></span></p></td>
<td><p><span data-ttu-id="2e486-139">0x200000</span><span class="sxs-lookup"><span data-stu-id="2e486-139">0x200000</span></span></p></td>
<td><p><span data-ttu-id="2e486-140">Fornece suporte ao método <a href="seek-method-ado.md">Seek</a> para localizar uma linha em um <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="2e486-140">Supports the <a href="seek-method-ado.md">Seek</a> method to locate a row in a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e486-141"><strong>adUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="2e486-141"><strong>adUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="2e486-142">0x1008000</span><span class="sxs-lookup"><span data-stu-id="2e486-142">0x1008000</span></span></p></td>
<td><p><span data-ttu-id="2e486-143">Fornece suporte ao método <a href="update-method-ado.md">Update</a> para modificar dados existentes.</span><span class="sxs-lookup"><span data-stu-id="2e486-143">Supports the <a href="update-method-ado.md">Update</a> method to modify existing data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e486-144"><strong>adUpdateBatch</strong></span><span class="sxs-lookup"><span data-stu-id="2e486-144"><strong>adUpdateBatch</strong></span></span></p></td>
<td><p><span data-ttu-id="2e486-145">0x10000</span><span class="sxs-lookup"><span data-stu-id="2e486-145">0x10000</span></span></p></td>
<td><p><span data-ttu-id="2e486-146">Fornece suporte à atualização em lote (métodos <a href="updatebatch-method-ado.md">UpdateBatch</a> e <a href="cancelbatch-method-ado.md">CancelBatch</a>) para transmitir grupos de alterações ao provedor.</span><span class="sxs-lookup"><span data-stu-id="2e486-146">Supports batch updating (<a href="updatebatch-method-ado.md">UpdateBatch</a> and <a href="cancelbatch-method-ado.md">CancelBatch</a> methods) to transmit groups of changes to the provider.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="2e486-147">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="2e486-147">ADO/WFC equivalent</span></span>

<span data-ttu-id="2e486-148">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="2e486-148">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2e486-149">Constante</span><span class="sxs-lookup"><span data-stu-id="2e486-149">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2e486-150">AdoEnums.CursorOption.ADDNEW</span><span class="sxs-lookup"><span data-stu-id="2e486-150">AdoEnums.CursorOption.ADDNEW</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e486-151">AdoEnums.CursorOption.APPROXPOSITION</span><span class="sxs-lookup"><span data-stu-id="2e486-151">AdoEnums.CursorOption.APPROXPOSITION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e486-152">AdoEnums.CursorOption.BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="2e486-152">AdoEnums.CursorOption.BOOKMARK</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e486-153">AdoEnums.CursorOption.DELETE</span><span class="sxs-lookup"><span data-stu-id="2e486-153">AdoEnums.CursorOption.DELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e486-154">AdoEnums.CursorOption.FIND</span><span class="sxs-lookup"><span data-stu-id="2e486-154">AdoEnums.CursorOption.FIND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e486-155">AdoEnums.CursorOption.HOLDRECORDS</span><span class="sxs-lookup"><span data-stu-id="2e486-155">AdoEnums.CursorOption.HOLDRECORDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e486-156">AdoEnums.CursorOption.INDEX</span><span class="sxs-lookup"><span data-stu-id="2e486-156">AdoEnums.CursorOption.INDEX</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e486-157">AdoEnums.CursorOption.MOVEPREVIOUS</span><span class="sxs-lookup"><span data-stu-id="2e486-157">AdoEnums.CursorOption.MOVEPREVIOUS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e486-158">AdoEnums.CursorOption.NOTIFY</span><span class="sxs-lookup"><span data-stu-id="2e486-158">AdoEnums.CursorOption.NOTIFY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e486-159">AdoEnums.CursorOption.RESYNC</span><span class="sxs-lookup"><span data-stu-id="2e486-159">AdoEnums.CursorOption.RESYNC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e486-160">AdoEnums.CursorOption.SEEK</span><span class="sxs-lookup"><span data-stu-id="2e486-160">AdoEnums.CursorOption.SEEK</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e486-161">AdoEnums.CursorOption.UPDATE</span><span class="sxs-lookup"><span data-stu-id="2e486-161">AdoEnums.CursorOption.UPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e486-162">AdoEnums.CursorOption.UPDATEBATCH</span><span class="sxs-lookup"><span data-stu-id="2e486-162">AdoEnums.CursorOption.UPDATEBATCH</span></span></p></td>
</tr>
</tbody>
</table>

