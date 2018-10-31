---
title: CompareEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: CompareEnum
ms:assetid: 7ac84af6-4f8b-4d1f-7eb3-a015b8b60bc6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249509(v=office.15)
ms:contentKeyID: 48545801
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 8c35b04dc1b5aa0a97236ff7ece260018cbe29c3
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860305"
---
# <a name="compareenum"></a><span data-ttu-id="7f4d2-102">CompareEnum</span><span class="sxs-lookup"><span data-stu-id="7f4d2-102">CompareEnum</span></span>

<span data-ttu-id="7f4d2-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7f4d2-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="7f4d2-104">Especifica a posição relativa de dois registros representados por seus indicadores.</span><span class="sxs-lookup"><span data-stu-id="7f4d2-104">Specifies the relative position of two records represented by their bookmarks.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7f4d2-105">Constante</span><span class="sxs-lookup"><span data-stu-id="7f4d2-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="7f4d2-106">Valor</span><span class="sxs-lookup"><span data-stu-id="7f4d2-106">Value</span></span></p></th>
<th><p><span data-ttu-id="7f4d2-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="7f4d2-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7f4d2-108"><strong>adCompareEqual</strong></span><span class="sxs-lookup"><span data-stu-id="7f4d2-108"><strong>adCompareEqual</strong></span></span></p></td>
<td><p><span data-ttu-id="7f4d2-109">1</span><span class="sxs-lookup"><span data-stu-id="7f4d2-109">1</span></span></p></td>
<td><p><span data-ttu-id="7f4d2-110">Indica que os indicadores são iguais.</span><span class="sxs-lookup"><span data-stu-id="7f4d2-110">Indicates that the bookmarks are equal.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f4d2-111"><strong>adCompareGreaterThan</strong></span><span class="sxs-lookup"><span data-stu-id="7f4d2-111"><strong>adCompareGreaterThan</strong></span></span></p></td>
<td><p><span data-ttu-id="7f4d2-112">2</span><span class="sxs-lookup"><span data-stu-id="7f4d2-112">2</span></span></p></td>
<td><p><span data-ttu-id="7f4d2-113">Indica que o primeiro indicador é após o segundo.</span><span class="sxs-lookup"><span data-stu-id="7f4d2-113">Indicates that the first bookmark is after the second.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f4d2-114"><strong>adCompareLessThan</strong></span><span class="sxs-lookup"><span data-stu-id="7f4d2-114"><strong>adCompareLessThan</strong></span></span></p></td>
<td><p><span data-ttu-id="7f4d2-115">0</span><span class="sxs-lookup"><span data-stu-id="7f4d2-115">0</span></span></p></td>
<td><p><span data-ttu-id="7f4d2-116">Indica que o primeiro indicador é antes do segundo.</span><span class="sxs-lookup"><span data-stu-id="7f4d2-116">Indicates that the first bookmark is before the second.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f4d2-117"><strong>adCompareNotComparable</strong></span><span class="sxs-lookup"><span data-stu-id="7f4d2-117"><strong>adCompareNotComparable</strong></span></span></p></td>
<td><p><span data-ttu-id="7f4d2-118">4</span><span class="sxs-lookup"><span data-stu-id="7f4d2-118">4</span></span></p></td>
<td><p><span data-ttu-id="7f4d2-119">Indica que os indicadores não podem ser comparados.</span><span class="sxs-lookup"><span data-stu-id="7f4d2-119">Indicates that the bookmarks cannot be compared.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f4d2-120"><strong>adCompareNotEqual</strong></span><span class="sxs-lookup"><span data-stu-id="7f4d2-120"><strong>adCompareNotEqual</strong></span></span></p></td>
<td><p><span data-ttu-id="7f4d2-121">3</span><span class="sxs-lookup"><span data-stu-id="7f4d2-121">3</span></span></p></td>
<td><p><span data-ttu-id="7f4d2-122">Indica que os indicadores não são iguais e não estão em ordem.</span><span class="sxs-lookup"><span data-stu-id="7f4d2-122">Indicates that the bookmarks are not equal and not ordered.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="7f4d2-123">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="7f4d2-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="7f4d2-124">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="7f4d2-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7f4d2-125">Constante</span><span class="sxs-lookup"><span data-stu-id="7f4d2-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7f4d2-126">AdoEnums.Compare.EQUAL</span><span class="sxs-lookup"><span data-stu-id="7f4d2-126">AdoEnums.Compare.EQUAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f4d2-127">AdoEnums.Compare.GREATERTHAN</span><span class="sxs-lookup"><span data-stu-id="7f4d2-127">AdoEnums.Compare.GREATERTHAN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f4d2-128">AdoEnums.Compare.LESSTHAN</span><span class="sxs-lookup"><span data-stu-id="7f4d2-128">AdoEnums.Compare.LESSTHAN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f4d2-129">AdoEnums.Compare.NOTCOMPARABLE</span><span class="sxs-lookup"><span data-stu-id="7f4d2-129">AdoEnums.Compare.NOTCOMPARABLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f4d2-130">AdoEnums.Compare.NOTEQUAL</span><span class="sxs-lookup"><span data-stu-id="7f4d2-130">AdoEnums.Compare.NOTEQUAL</span></span></p></td>
</tr>
</tbody>
</table>

