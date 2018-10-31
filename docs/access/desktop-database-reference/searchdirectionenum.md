---
title: SearchDirectionEnum
TOCTitle: SearchDirectionEnum
ms:assetid: d491000b-47d0-bb28-95ed-7526dbb7c5e9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250064(v=office.15)
ms:contentKeyID: 48547943
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fc3803fe6afb482dc42ca12476024325fc1022ae
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862979"
---
# <a name="searchdirectionenum"></a><span data-ttu-id="ab6d9-102">SearchDirectionEnum</span><span class="sxs-lookup"><span data-stu-id="ab6d9-102">SearchDirectionEnum</span></span>


<span data-ttu-id="ab6d9-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ab6d9-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ab6d9-104">Especifica a direção de uma pesquisa de registro em um [Recorset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="ab6d9-104">Specifies the direction of a record search within a [Recordset](recordset-object-ado.md).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ab6d9-105">Constant</span><span class="sxs-lookup"><span data-stu-id="ab6d9-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="ab6d9-106">Valor</span><span class="sxs-lookup"><span data-stu-id="ab6d9-106">Value</span></span></p></th>
<th><p><span data-ttu-id="ab6d9-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="ab6d9-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ab6d9-108"><strong>adSearchBackward</strong></span><span class="sxs-lookup"><span data-stu-id="ab6d9-108"><strong>adSearchBackward</strong></span></span></p></td>
<td><p><span data-ttu-id="ab6d9-109">-1</span><span class="sxs-lookup"><span data-stu-id="ab6d9-109">-1</span></span></p></td>
<td><p><span data-ttu-id="ab6d9-p101">Pesquisa no sentido contrário, parando no início do <strong>Recordset</strong>. Se não for encontrada uma correspondência, o ponteiro do registro será posicionado em <a href="bof-eof-properties-ado.md">BOF</a>.</span><span class="sxs-lookup"><span data-stu-id="ab6d9-p101">Searches backward, stopping at the beginning of the <strong>Recordset</strong>. If a match is not found, the record pointer is positioned at <a href="bof-eof-properties-ado.md">BOF</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab6d9-112"><strong>adSearchForward</strong></span><span class="sxs-lookup"><span data-stu-id="ab6d9-112"><strong>adSearchForward</strong></span></span></p></td>
<td><p><span data-ttu-id="ab6d9-113">1</span><span class="sxs-lookup"><span data-stu-id="ab6d9-113">1</span></span></p></td>
<td><p><span data-ttu-id="ab6d9-p102">Pesquisa para frente, parando no final do <strong>Recordset</strong>. Se não for encontrada uma correspondência, o ponteiro do registro será posicionado em <a href="bof-eof-properties-ado.md">EOF</a>.</span><span class="sxs-lookup"><span data-stu-id="ab6d9-p102">Searches forward, stopping at the end of the <strong>Recordset</strong>. If a match is not found, the record pointer is positioned at <a href="bof-eof-properties-ado.md">EOF</a>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="ab6d9-116">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="ab6d9-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="ab6d9-117">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="ab6d9-117">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ab6d9-118">Constante</span><span class="sxs-lookup"><span data-stu-id="ab6d9-118">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ab6d9-119">AdoEnums.SearchDirection.BACKWARD</span><span class="sxs-lookup"><span data-stu-id="ab6d9-119">AdoEnums.SearchDirection.BACKWARD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab6d9-120">AdoEnums.SearchDirection.FORWARD</span><span class="sxs-lookup"><span data-stu-id="ab6d9-120">AdoEnums.SearchDirection.FORWARD</span></span></p></td>
</tr>
</tbody>
</table>

