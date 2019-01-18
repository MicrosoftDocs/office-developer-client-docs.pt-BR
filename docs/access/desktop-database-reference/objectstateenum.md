---
title: ObjectStateEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: ObjectStateEnum
ms:assetid: 129d589a-2955-3da9-e60a-7fbfdd6bfbdc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248900(v=office.15)
ms:contentKeyID: 48543347
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b6e346db2fb2dac0695e8c9048a210d8e40e6dc4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712264"
---
# <a name="objectstateenum"></a><span data-ttu-id="0ffbe-102">ObjectStateEnum</span><span class="sxs-lookup"><span data-stu-id="0ffbe-102">ObjectStateEnum</span></span>

<span data-ttu-id="0ffbe-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="0ffbe-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0ffbe-104">Especifica se um objeto está aberto ou fechado, conectando a uma fonte de dados, executando um comando ou recuperando dados.</span><span class="sxs-lookup"><span data-stu-id="0ffbe-104">Specifies whether an object is open or closed, connecting to a data source, executing a command, or retrieving data.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0ffbe-105">Constante</span><span class="sxs-lookup"><span data-stu-id="0ffbe-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="0ffbe-106">Valor</span><span class="sxs-lookup"><span data-stu-id="0ffbe-106">Value</span></span></p></th>
<th><p><span data-ttu-id="0ffbe-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="0ffbe-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0ffbe-108"><strong>adStateClosed</strong></span><span class="sxs-lookup"><span data-stu-id="0ffbe-108"><strong>adStateClosed</strong></span></span></p></td>
<td><p><span data-ttu-id="0ffbe-109">0</span><span class="sxs-lookup"><span data-stu-id="0ffbe-109">0</span></span></p></td>
<td><p><span data-ttu-id="0ffbe-110">Indica que o objeto está fechado.</span><span class="sxs-lookup"><span data-stu-id="0ffbe-110">Indicates that the object is closed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ffbe-111"><strong>adStateOpen</strong></span><span class="sxs-lookup"><span data-stu-id="0ffbe-111"><strong>adStateOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="0ffbe-112">1</span><span class="sxs-lookup"><span data-stu-id="0ffbe-112">1</span></span></p></td>
<td><p><span data-ttu-id="0ffbe-113">Indica que o objeto está aberto.</span><span class="sxs-lookup"><span data-stu-id="0ffbe-113">Indicates that the object is open.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ffbe-114"><strong>adStateConnecting</strong></span><span class="sxs-lookup"><span data-stu-id="0ffbe-114"><strong>adStateConnecting</strong></span></span></p></td>
<td><p><span data-ttu-id="0ffbe-115">2</span><span class="sxs-lookup"><span data-stu-id="0ffbe-115">2</span></span></p></td>
<td><p><span data-ttu-id="0ffbe-116">Indica que o objeto está conectando.</span><span class="sxs-lookup"><span data-stu-id="0ffbe-116">Indicates that the object is connecting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ffbe-117"><strong>adStateExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="0ffbe-117"><strong>adStateExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="0ffbe-118">4</span><span class="sxs-lookup"><span data-stu-id="0ffbe-118">4</span></span></p></td>
<td><p><span data-ttu-id="0ffbe-119">Indica que o objeto está executando um comando.</span><span class="sxs-lookup"><span data-stu-id="0ffbe-119">Indicates that the object is executing a command.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ffbe-120"><strong>adStateFetching</strong></span><span class="sxs-lookup"><span data-stu-id="0ffbe-120"><strong>adStateFetching</strong></span></span></p></td>
<td><p><span data-ttu-id="0ffbe-121">8</span><span class="sxs-lookup"><span data-stu-id="0ffbe-121">8</span></span></p></td>
<td><p><span data-ttu-id="0ffbe-122">Indica que as linhas do objeto estão sendo recuperadas.</span><span class="sxs-lookup"><span data-stu-id="0ffbe-122">Indicates that the rows of the object are being retrieved.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="0ffbe-123">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="0ffbe-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="0ffbe-124">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="0ffbe-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0ffbe-125">Constante</span><span class="sxs-lookup"><span data-stu-id="0ffbe-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0ffbe-126">AdoEnums.ObjectState.CLOSED</span><span class="sxs-lookup"><span data-stu-id="0ffbe-126">AdoEnums.ObjectState.CLOSED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ffbe-127">AdoEnums.ObjectState.OPEN</span><span class="sxs-lookup"><span data-stu-id="0ffbe-127">AdoEnums.ObjectState.OPEN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ffbe-128">AdoEnums.ObjectState.CONNECTING</span><span class="sxs-lookup"><span data-stu-id="0ffbe-128">AdoEnums.ObjectState.CONNECTING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ffbe-129">AdoEnums.ObjectState.EXECUTING</span><span class="sxs-lookup"><span data-stu-id="0ffbe-129">AdoEnums.ObjectState.EXECUTING</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ffbe-130">AdoEnums.ObjectState.FETCHING</span><span class="sxs-lookup"><span data-stu-id="0ffbe-130">AdoEnums.ObjectState.FETCHING</span></span></p></td>
</tr>
</tbody>
</table>

