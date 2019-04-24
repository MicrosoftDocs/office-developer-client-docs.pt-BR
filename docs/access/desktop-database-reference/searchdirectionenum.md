---
title: SearchDirectionEnum
TOCTitle: SearchDirectionEnum
ms:assetid: d491000b-47d0-bb28-95ed-7526dbb7c5e9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250064(v=office.15)
ms:contentKeyID: 48547943
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9f9fdf9dd5908b65ae3b6f6ce5a44eba07e4d9bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308803"
---
# <a name="searchdirectionenum"></a><span data-ttu-id="168d3-102">SearchDirectionEnum</span><span class="sxs-lookup"><span data-stu-id="168d3-102">SearchDirectionEnum</span></span>


<span data-ttu-id="168d3-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="168d3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="168d3-104">Especifica a direção de uma pesquisa de registro em um [Recorset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="168d3-104">Specifies the direction of a record search within a [Recordset](recordset-object-ado.md).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="168d3-105">Constant</span><span class="sxs-lookup"><span data-stu-id="168d3-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="168d3-106">Valor</span><span class="sxs-lookup"><span data-stu-id="168d3-106">Value</span></span></p></th>
<th><p><span data-ttu-id="168d3-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="168d3-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="168d3-108"><strong>adSearchBackward</strong></span><span class="sxs-lookup"><span data-stu-id="168d3-108"><strong>adSearchBackward</strong></span></span></p></td>
<td><p><span data-ttu-id="168d3-109">-1</span><span class="sxs-lookup"><span data-stu-id="168d3-109">-1</span></span></p></td>
<td><p><span data-ttu-id="168d3-p101">Pesquisa no sentido contrário, parando no início do <strong>Recordset</strong>. Se não for encontrada uma correspondência, o ponteiro do registro será posicionado em <a href="bof-eof-properties-ado.md">BOF</a>.</span><span class="sxs-lookup"><span data-stu-id="168d3-p101">Searches backward, stopping at the beginning of the <strong>Recordset</strong>. If a match is not found, the record pointer is positioned at <a href="bof-eof-properties-ado.md">BOF</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="168d3-112"><strong>adSearchForward</strong></span><span class="sxs-lookup"><span data-stu-id="168d3-112"><strong>adSearchForward</strong></span></span></p></td>
<td><p><span data-ttu-id="168d3-113">1</span><span class="sxs-lookup"><span data-stu-id="168d3-113">1</span></span></p></td>
<td><p><span data-ttu-id="168d3-p102">Pesquisa para frente, parando no final do <strong>Recordset</strong>. Se não for encontrada uma correspondência, o ponteiro do registro será posicionado em <a href="bof-eof-properties-ado.md">EOF</a>.</span><span class="sxs-lookup"><span data-stu-id="168d3-p102">Searches forward, stopping at the end of the <strong>Recordset</strong>. If a match is not found, the record pointer is positioned at <a href="bof-eof-properties-ado.md">EOF</a>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="168d3-116">Equivalente do ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="168d3-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="168d3-117">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="168d3-117">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="168d3-118">Constant</span><span class="sxs-lookup"><span data-stu-id="168d3-118">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="168d3-119">AdoEnums. SearchDirection. BACKWARD</span><span class="sxs-lookup"><span data-stu-id="168d3-119">AdoEnums.SearchDirection.BACKWARD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="168d3-120">AdoEnums. SearchDirection. FORWARD</span><span class="sxs-lookup"><span data-stu-id="168d3-120">AdoEnums.SearchDirection.FORWARD</span></span></p></td>
</tr>
</tbody>
</table>

