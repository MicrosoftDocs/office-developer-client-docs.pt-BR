---
title: ObjectStateEnum (referência do banco de dados de área de trabalho do Access)
TOCTitle: ObjectStateEnum
ms:assetid: 129d589a-2955-3da9-e60a-7fbfdd6bfbdc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248900(v=office.15)
ms:contentKeyID: 48543347
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b6e346db2fb2dac0695e8c9048a210d8e40e6dc4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288522"
---
# <a name="objectstateenum"></a><span data-ttu-id="ce7c9-102">ObjectStateEnum</span><span class="sxs-lookup"><span data-stu-id="ce7c9-102">ObjectStateEnum</span></span>

<span data-ttu-id="ce7c9-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ce7c9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ce7c9-104">Especifica se um objeto está aberto ou fechado, conectando a uma fonte de dados, executando um comando ou recuperando dados.</span><span class="sxs-lookup"><span data-stu-id="ce7c9-104">Specifies whether an object is open or closed, connecting to a data source, executing a command, or retrieving data.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ce7c9-105">Constant</span><span class="sxs-lookup"><span data-stu-id="ce7c9-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="ce7c9-106">Valor</span><span class="sxs-lookup"><span data-stu-id="ce7c9-106">Value</span></span></p></th>
<th><p><span data-ttu-id="ce7c9-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="ce7c9-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ce7c9-108"><strong>adStateClosed</strong></span><span class="sxs-lookup"><span data-stu-id="ce7c9-108"><strong>adStateClosed</strong></span></span></p></td>
<td><p><span data-ttu-id="ce7c9-109">,0</span><span class="sxs-lookup"><span data-stu-id="ce7c9-109">0</span></span></p></td>
<td><p><span data-ttu-id="ce7c9-110">Indica que o objeto está fechado.</span><span class="sxs-lookup"><span data-stu-id="ce7c9-110">Indicates that the object is closed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce7c9-111"><strong>adStateOpen</strong></span><span class="sxs-lookup"><span data-stu-id="ce7c9-111"><strong>adStateOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="ce7c9-112">1</span><span class="sxs-lookup"><span data-stu-id="ce7c9-112">1</span></span></p></td>
<td><p><span data-ttu-id="ce7c9-113">Indica que o objeto está aberto.</span><span class="sxs-lookup"><span data-stu-id="ce7c9-113">Indicates that the object is open.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce7c9-114"><strong>adStateConnecting</strong></span><span class="sxs-lookup"><span data-stu-id="ce7c9-114"><strong>adStateConnecting</strong></span></span></p></td>
<td><p><span data-ttu-id="ce7c9-115">duas</span><span class="sxs-lookup"><span data-stu-id="ce7c9-115">2</span></span></p></td>
<td><p><span data-ttu-id="ce7c9-116">Indica que o objeto está conectando.</span><span class="sxs-lookup"><span data-stu-id="ce7c9-116">Indicates that the object is connecting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce7c9-117"><strong>adStateExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="ce7c9-117"><strong>adStateExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="ce7c9-118">quatro</span><span class="sxs-lookup"><span data-stu-id="ce7c9-118">4</span></span></p></td>
<td><p><span data-ttu-id="ce7c9-119">Indica que o objeto está executando um comando.</span><span class="sxs-lookup"><span data-stu-id="ce7c9-119">Indicates that the object is executing a command.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce7c9-120"><strong>adStateFetching</strong></span><span class="sxs-lookup"><span data-stu-id="ce7c9-120"><strong>adStateFetching</strong></span></span></p></td>
<td><p><span data-ttu-id="ce7c9-121">8</span><span class="sxs-lookup"><span data-stu-id="ce7c9-121">8</span></span></p></td>
<td><p><span data-ttu-id="ce7c9-122">Indica que as linhas do objeto estão sendo recuperadas.</span><span class="sxs-lookup"><span data-stu-id="ce7c9-122">Indicates that the rows of the object are being retrieved.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="ce7c9-123">Equivalente do ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="ce7c9-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="ce7c9-124">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="ce7c9-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ce7c9-125">Constant</span><span class="sxs-lookup"><span data-stu-id="ce7c9-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ce7c9-126">AdoEnums. ObjectState. CLOSED</span><span class="sxs-lookup"><span data-stu-id="ce7c9-126">AdoEnums.ObjectState.CLOSED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce7c9-127">AdoEnums. ObjectState. OPEN</span><span class="sxs-lookup"><span data-stu-id="ce7c9-127">AdoEnums.ObjectState.OPEN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce7c9-128">AdoEnums. ObjectState. CONNECTing</span><span class="sxs-lookup"><span data-stu-id="ce7c9-128">AdoEnums.ObjectState.CONNECTING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce7c9-129">AdoEnums. ObjectState. EXECUting</span><span class="sxs-lookup"><span data-stu-id="ce7c9-129">AdoEnums.ObjectState.EXECUTING</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce7c9-130">AdoEnums. ObjectState. FETCHing</span><span class="sxs-lookup"><span data-stu-id="ce7c9-130">AdoEnums.ObjectState.FETCHING</span></span></p></td>
</tr>
</tbody>
</table>

