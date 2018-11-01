---
title: ObjectStateEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: ObjectStateEnum
ms:assetid: 129d589a-2955-3da9-e60a-7fbfdd6bfbdc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248900(v=office.15)
ms:contentKeyID: 48543347
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 48fcf6c0135b4704155aa23765e848de5b3e6313
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879953"
---
# <a name="objectstateenum"></a><span data-ttu-id="1501b-102">ObjectStateEnum</span><span class="sxs-lookup"><span data-stu-id="1501b-102">ObjectStateEnum</span></span>

<span data-ttu-id="1501b-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="1501b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1501b-104">Especifica se um objeto está aberto ou fechado, conectando a uma fonte de dados, executando um comando ou recuperando dados.</span><span class="sxs-lookup"><span data-stu-id="1501b-104">Specifies whether an object is open or closed, connecting to a data source, executing a command, or retrieving data.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1501b-105">Constante</span><span class="sxs-lookup"><span data-stu-id="1501b-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="1501b-106">Valor</span><span class="sxs-lookup"><span data-stu-id="1501b-106">Value</span></span></p></th>
<th><p><span data-ttu-id="1501b-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="1501b-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1501b-108"><strong>adStateClosed</strong></span><span class="sxs-lookup"><span data-stu-id="1501b-108"><strong>adStateClosed</strong></span></span></p></td>
<td><p><span data-ttu-id="1501b-109">0</span><span class="sxs-lookup"><span data-stu-id="1501b-109">0</span></span></p></td>
<td><p><span data-ttu-id="1501b-110">Indica que o objeto está fechado.</span><span class="sxs-lookup"><span data-stu-id="1501b-110">Indicates that the object is closed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1501b-111"><strong>adStateOpen</strong></span><span class="sxs-lookup"><span data-stu-id="1501b-111"><strong>adStateOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="1501b-112">1</span><span class="sxs-lookup"><span data-stu-id="1501b-112">1</span></span></p></td>
<td><p><span data-ttu-id="1501b-113">Indica que o objeto está aberto.</span><span class="sxs-lookup"><span data-stu-id="1501b-113">Indicates that the object is open.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1501b-114"><strong>adStateConnecting</strong></span><span class="sxs-lookup"><span data-stu-id="1501b-114"><strong>adStateConnecting</strong></span></span></p></td>
<td><p><span data-ttu-id="1501b-115">2</span><span class="sxs-lookup"><span data-stu-id="1501b-115">2</span></span></p></td>
<td><p><span data-ttu-id="1501b-116">Indica que o objeto está conectando.</span><span class="sxs-lookup"><span data-stu-id="1501b-116">Indicates that the object is connecting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1501b-117"><strong>adStateExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="1501b-117"><strong>adStateExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="1501b-118">4</span><span class="sxs-lookup"><span data-stu-id="1501b-118">4</span></span></p></td>
<td><p><span data-ttu-id="1501b-119">Indica que o objeto está executando um comando.</span><span class="sxs-lookup"><span data-stu-id="1501b-119">Indicates that the object is executing a command.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1501b-120"><strong>adStateFetching</strong></span><span class="sxs-lookup"><span data-stu-id="1501b-120"><strong>adStateFetching</strong></span></span></p></td>
<td><p><span data-ttu-id="1501b-121">8</span><span class="sxs-lookup"><span data-stu-id="1501b-121">8</span></span></p></td>
<td><p><span data-ttu-id="1501b-122">Indica que as linhas do objeto estão sendo recuperadas.</span><span class="sxs-lookup"><span data-stu-id="1501b-122">Indicates that the rows of the object are being retrieved.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="1501b-123">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="1501b-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="1501b-124">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="1501b-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1501b-125">Constante</span><span class="sxs-lookup"><span data-stu-id="1501b-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1501b-126">AdoEnums.ObjectState.CLOSED</span><span class="sxs-lookup"><span data-stu-id="1501b-126">AdoEnums.ObjectState.CLOSED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1501b-127">AdoEnums.ObjectState.OPEN</span><span class="sxs-lookup"><span data-stu-id="1501b-127">AdoEnums.ObjectState.OPEN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1501b-128">AdoEnums.ObjectState.CONNECTING</span><span class="sxs-lookup"><span data-stu-id="1501b-128">AdoEnums.ObjectState.CONNECTING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1501b-129">AdoEnums.ObjectState.EXECUTING</span><span class="sxs-lookup"><span data-stu-id="1501b-129">AdoEnums.ObjectState.EXECUTING</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1501b-130">AdoEnums.ObjectState.FETCHING</span><span class="sxs-lookup"><span data-stu-id="1501b-130">AdoEnums.ObjectState.FETCHING</span></span></p></td>
</tr>
</tbody>
</table>

