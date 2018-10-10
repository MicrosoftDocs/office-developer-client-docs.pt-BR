---
title: SearchDirectionEnum
TOCTitle: SearchDirectionEnum
ms:assetid: d491000b-47d0-bb28-95ed-7526dbb7c5e9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250064(v=office.15)
ms:contentKeyID: 48547943
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d0a9954319448a219d9683cfd8133929fb3d184d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462425"
---
# <a name="searchdirectionenum"></a><span data-ttu-id="8301a-102">SearchDirectionEnum</span><span class="sxs-lookup"><span data-stu-id="8301a-102">SearchDirectionEnum</span></span>


<span data-ttu-id="8301a-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8301a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8301a-104">Especifica a direção de uma pesquisa de registro em um [Recorset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="8301a-104">Specifies the direction of a record search within a [Recordset](recordset-object-ado.md).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8301a-105">Constant</span><span class="sxs-lookup"><span data-stu-id="8301a-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="8301a-106">Valor</span><span class="sxs-lookup"><span data-stu-id="8301a-106">Value</span></span></p></th>
<th><p><span data-ttu-id="8301a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="8301a-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8301a-108"><strong>adSearchBackward</strong></span><span class="sxs-lookup"><span data-stu-id="8301a-108"><strong>adSearchBackward</strong></span></span></p></td>
<td><p><span data-ttu-id="8301a-109">-1</span><span class="sxs-lookup"><span data-stu-id="8301a-109">-1</span></span></p></td>
<td><p><span data-ttu-id="8301a-p101">Pesquisa no sentido contrário, parando no início do <strong>Recordset</strong>. Se não for encontrada uma correspondência, o ponteiro do registro será posicionado em <a href="bof-eof-properties-ado.md">BOF</a>.</span><span class="sxs-lookup"><span data-stu-id="8301a-p101">Searches backward, stopping at the beginning of the <strong>Recordset</strong>. If a match is not found, the record pointer is positioned at <a href="bof-eof-properties-ado.md">BOF</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8301a-112"><strong>adSearchForward</strong></span><span class="sxs-lookup"><span data-stu-id="8301a-112"><strong>adSearchForward</strong></span></span></p></td>
<td><p><span data-ttu-id="8301a-113">1</span><span class="sxs-lookup"><span data-stu-id="8301a-113">1</span></span></p></td>
<td><p><span data-ttu-id="8301a-p102">Pesquisa para frente, parando no final do <strong>Recordset</strong>. Se não for encontrada uma correspondência, o ponteiro do registro será posicionado em <a href="bof-eof-properties-ado.md">EOF</a>.</span><span class="sxs-lookup"><span data-stu-id="8301a-p102">Searches forward, stopping at the end of the <strong>Recordset</strong>. If a match is not found, the record pointer is positioned at <a href="bof-eof-properties-ado.md">EOF</a>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8301a-116">**ADO/WFC Equivalente**</span><span class="sxs-lookup"><span data-stu-id="8301a-116">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="8301a-117">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="8301a-117">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8301a-118">Constante</span><span class="sxs-lookup"><span data-stu-id="8301a-118">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8301a-119">AdoEnums.SearchDirection.BACKWARD</span><span class="sxs-lookup"><span data-stu-id="8301a-119">AdoEnums.SearchDirection.BACKWARD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8301a-120">AdoEnums.SearchDirection.FORWARD</span><span class="sxs-lookup"><span data-stu-id="8301a-120">AdoEnums.SearchDirection.FORWARD</span></span></p></td>
</tr>
</tbody>
</table>

