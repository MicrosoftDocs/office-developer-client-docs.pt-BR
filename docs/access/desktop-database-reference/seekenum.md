---
title: SeekEnum (referência do banco de dados da área de trabalho do Access)
TOCTitle: SeekEnum
ms:assetid: a0574809-db2d-8759-18cc-fb1cf776e8fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249737(v=office.15)
ms:contentKeyID: 48546706
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2f8334cbfc8e0f6a362a36e03984739d1d52b6f6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314655"
---
# <a name="seekenum"></a><span data-ttu-id="52712-102">SeekEnum</span><span class="sxs-lookup"><span data-stu-id="52712-102">SeekEnum</span></span>

<span data-ttu-id="52712-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="52712-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="52712-104">Especifica o tipo de [Seek](seek-method-ado.md) a ser executada.</span><span class="sxs-lookup"><span data-stu-id="52712-104">Specifies the type of [Seek](seek-method-ado.md) to execute.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="52712-105">Constant</span><span class="sxs-lookup"><span data-stu-id="52712-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="52712-106">Valor</span><span class="sxs-lookup"><span data-stu-id="52712-106">Value</span></span></p></th>
<th><p><span data-ttu-id="52712-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="52712-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52712-108">adSeekFirstEQ</span><span class="sxs-lookup"><span data-stu-id="52712-108">adSeekFirstEQ</span></span></p></td>
<td><p><span data-ttu-id="52712-109">1 </span><span class="sxs-lookup"><span data-stu-id="52712-109">1</span></span></p></td>
<td><p><span data-ttu-id="52712-110">Procura a primeira chave igual a <em>KeyValues</em>.</span><span class="sxs-lookup"><span data-stu-id="52712-110">Seeks the first key equal to <em>KeyValues</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52712-111">adSeekLastEQ</span><span class="sxs-lookup"><span data-stu-id="52712-111">adSeekLastEQ</span></span></p></td>
<td><p><span data-ttu-id="52712-112">2 </span><span class="sxs-lookup"><span data-stu-id="52712-112">2</span></span></p></td>
<td><p><span data-ttu-id="52712-113">Procura a última chave igual a <em>KeyValues</em>.</span><span class="sxs-lookup"><span data-stu-id="52712-113">Seeks the last key equal to <em>KeyValues</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52712-114">adSeekAfterEQ</span><span class="sxs-lookup"><span data-stu-id="52712-114">adSeekAfterEQ</span></span></p></td>
<td><p><span data-ttu-id="52712-115">4 </span><span class="sxs-lookup"><span data-stu-id="52712-115">4</span></span></p></td>
<td><p><span data-ttu-id="52712-116">Procura uma chave igual a <em>KeyValues</em> ou apenas depois de onde essa correspondência ocorreu.</span><span class="sxs-lookup"><span data-stu-id="52712-116">Seeks either a key equal to <em>KeyValues</em> or just after where that match would have occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52712-117">adSeekAfter</span><span class="sxs-lookup"><span data-stu-id="52712-117">adSeekAfter</span></span></p></td>
<td><p><span data-ttu-id="52712-118">8 </span><span class="sxs-lookup"><span data-stu-id="52712-118">8</span></span></p></td>
<td><p><span data-ttu-id="52712-119">Procura uma chave depois do local em que uma correspondência com <em>KeyValues</em> ocorreu.</span><span class="sxs-lookup"><span data-stu-id="52712-119">Seeks a key just after where a match with <em>KeyValues</em> would have occurred.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52712-120">adSeekBeforeEQ</span><span class="sxs-lookup"><span data-stu-id="52712-120">adSeekBeforeEQ</span></span></p></td>
<td><p><span data-ttu-id="52712-121">16 </span><span class="sxs-lookup"><span data-stu-id="52712-121">16</span></span></p></td>
<td><p><span data-ttu-id="52712-122">Procura uma chave igual a <em>KeyValues</em> ou apenas antes do local em que essa correspondência ocorreu.</span><span class="sxs-lookup"><span data-stu-id="52712-122">Seeks either a key equal to <em>KeyValues</em> or just before where that match would have occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52712-123">adSeekBefore</span><span class="sxs-lookup"><span data-stu-id="52712-123">adSeekBefore</span></span></p></td>
<td><p><span data-ttu-id="52712-124">32</span><span class="sxs-lookup"><span data-stu-id="52712-124">32</span></span></p></td>
<td><p><span data-ttu-id="52712-125">Procura uma chave antes do local em que uma correspondência com <em>KeyValues</em> ocorreu.</span><span class="sxs-lookup"><span data-stu-id="52712-125">Seeks a key just before where a match with <em>KeyValues</em> would have occurred.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="52712-126">Equivalente do ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="52712-126">ADO/WFC equivalent</span></span>

<span data-ttu-id="52712-127">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="52712-127">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="52712-128">Constant</span><span class="sxs-lookup"><span data-stu-id="52712-128">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52712-129">AdoEnums.Seek.FIRSTEQ</span><span class="sxs-lookup"><span data-stu-id="52712-129">AdoEnums.Seek.FIRSTEQ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52712-130">AdoEnums.Seek.LASTEQ</span><span class="sxs-lookup"><span data-stu-id="52712-130">AdoEnums.Seek.LASTEQ</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52712-131">AdoEnums.Seek.AFTEREQ</span><span class="sxs-lookup"><span data-stu-id="52712-131">AdoEnums.Seek.AFTEREQ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52712-132">AdoEnums.Seek.AFTER</span><span class="sxs-lookup"><span data-stu-id="52712-132">AdoEnums.Seek.AFTER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52712-133">AdoEnums.Seek.BEFOREEQ</span><span class="sxs-lookup"><span data-stu-id="52712-133">AdoEnums.Seek.BEFOREEQ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52712-134">AdoEnums.Seek.BEFORE</span><span class="sxs-lookup"><span data-stu-id="52712-134">AdoEnums.Seek.BEFORE</span></span></p></td>
</tr>
</tbody>
</table>

