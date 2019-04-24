---
title: CompareEnum (referência do banco de dados de área de trabalho do Access)
TOCTitle: CompareEnum
ms:assetid: 7ac84af6-4f8b-4d1f-7eb3-a015b8b60bc6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249509(v=office.15)
ms:contentKeyID: 48545801
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cd120f726a51c884d063bb03f6d6864ea2d48344
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296063"
---
# <a name="compareenum"></a><span data-ttu-id="f7854-102">CompareEnum</span><span class="sxs-lookup"><span data-stu-id="f7854-102">CompareEnum</span></span>

<span data-ttu-id="f7854-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f7854-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f7854-104">Especifica a posição relativa de dois registros representados por seus indicadores.</span><span class="sxs-lookup"><span data-stu-id="f7854-104">Specifies the relative position of two records represented by their bookmarks.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f7854-105">Constant</span><span class="sxs-lookup"><span data-stu-id="f7854-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="f7854-106">Valor</span><span class="sxs-lookup"><span data-stu-id="f7854-106">Value</span></span></p></th>
<th><p><span data-ttu-id="f7854-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="f7854-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f7854-108"><strong>adCompareEqual</strong></span><span class="sxs-lookup"><span data-stu-id="f7854-108"><strong>adCompareEqual</strong></span></span></p></td>
<td><p><span data-ttu-id="f7854-109">1</span><span class="sxs-lookup"><span data-stu-id="f7854-109">1</span></span></p></td>
<td><p><span data-ttu-id="f7854-110">Indica que os indicadores são iguais.</span><span class="sxs-lookup"><span data-stu-id="f7854-110">Indicates that the bookmarks are equal.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7854-111"><strong>adCompareGreaterThan</strong></span><span class="sxs-lookup"><span data-stu-id="f7854-111"><strong>adCompareGreaterThan</strong></span></span></p></td>
<td><p><span data-ttu-id="f7854-112">duas</span><span class="sxs-lookup"><span data-stu-id="f7854-112">2</span></span></p></td>
<td><p><span data-ttu-id="f7854-113">Indica que o primeiro indicador é após o segundo.</span><span class="sxs-lookup"><span data-stu-id="f7854-113">Indicates that the first bookmark is after the second.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f7854-114"><strong>adCompareLessThan</strong></span><span class="sxs-lookup"><span data-stu-id="f7854-114"><strong>adCompareLessThan</strong></span></span></p></td>
<td><p><span data-ttu-id="f7854-115">,0</span><span class="sxs-lookup"><span data-stu-id="f7854-115">0</span></span></p></td>
<td><p><span data-ttu-id="f7854-116">Indica que o primeiro indicador é antes do segundo.</span><span class="sxs-lookup"><span data-stu-id="f7854-116">Indicates that the first bookmark is before the second.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7854-117"><strong>adCompareNotComparable</strong></span><span class="sxs-lookup"><span data-stu-id="f7854-117"><strong>adCompareNotComparable</strong></span></span></p></td>
<td><p><span data-ttu-id="f7854-118">quatro</span><span class="sxs-lookup"><span data-stu-id="f7854-118">4</span></span></p></td>
<td><p><span data-ttu-id="f7854-119">Indica que os indicadores não podem ser comparados.</span><span class="sxs-lookup"><span data-stu-id="f7854-119">Indicates that the bookmarks cannot be compared.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f7854-120"><strong>adCompareNotEqual</strong></span><span class="sxs-lookup"><span data-stu-id="f7854-120"><strong>adCompareNotEqual</strong></span></span></p></td>
<td><p><span data-ttu-id="f7854-121">3D</span><span class="sxs-lookup"><span data-stu-id="f7854-121">3</span></span></p></td>
<td><p><span data-ttu-id="f7854-122">Indica que os indicadores não são iguais e não estão em ordem.</span><span class="sxs-lookup"><span data-stu-id="f7854-122">Indicates that the bookmarks are not equal and not ordered.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="f7854-123">Equivalente do ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="f7854-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="f7854-124">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="f7854-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f7854-125">Constant</span><span class="sxs-lookup"><span data-stu-id="f7854-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f7854-126">AdoEnums. Compare. EQUAL</span><span class="sxs-lookup"><span data-stu-id="f7854-126">AdoEnums.Compare.EQUAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7854-127">AdoEnums. Compare. GREATERTHAN</span><span class="sxs-lookup"><span data-stu-id="f7854-127">AdoEnums.Compare.GREATERTHAN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f7854-128">AdoEnums. Compare. LESSTHAN</span><span class="sxs-lookup"><span data-stu-id="f7854-128">AdoEnums.Compare.LESSTHAN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7854-129">AdoEnums. Compare. não comparável</span><span class="sxs-lookup"><span data-stu-id="f7854-129">AdoEnums.Compare.NOTCOMPARABLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f7854-130">AdoEnums. Compare. não igual a</span><span class="sxs-lookup"><span data-stu-id="f7854-130">AdoEnums.Compare.NOTEQUAL</span></span></p></td>
</tr>
</tbody>
</table>

