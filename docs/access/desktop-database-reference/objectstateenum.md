---
title: ObjectStateEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: ObjectStateEnum
ms:assetid: 129d589a-2955-3da9-e60a-7fbfdd6bfbdc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248900(v=office.15)
ms:contentKeyID: 48543347
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4a08713e5363cb023021e2dd5acb6b38431a6b5e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465298"
---
# <a name="objectstateenum"></a><span data-ttu-id="9ebbc-102">ObjectStateEnum</span><span class="sxs-lookup"><span data-stu-id="9ebbc-102">ObjectStateEnum</span></span>


<span data-ttu-id="9ebbc-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="9ebbc-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9ebbc-104">Especifica se um objeto está aberto ou fechado, conectando a uma fonte de dados, executando um comando ou recuperando dados.</span><span class="sxs-lookup"><span data-stu-id="9ebbc-104">Specifies whether an object is open or closed, connecting to a data source, executing a command, or retrieving data.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9ebbc-105">Constante</span><span class="sxs-lookup"><span data-stu-id="9ebbc-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="9ebbc-106">Valor</span><span class="sxs-lookup"><span data-stu-id="9ebbc-106">Value</span></span></p></th>
<th><p><span data-ttu-id="9ebbc-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="9ebbc-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9ebbc-108"><strong>adStateClosed</strong></span><span class="sxs-lookup"><span data-stu-id="9ebbc-108"><strong>adStateClosed</strong></span></span></p></td>
<td><p><span data-ttu-id="9ebbc-109">0</span><span class="sxs-lookup"><span data-stu-id="9ebbc-109">0</span></span></p></td>
<td><p><span data-ttu-id="9ebbc-110">Indica que o objeto está fechado.</span><span class="sxs-lookup"><span data-stu-id="9ebbc-110">Indicates that the object is closed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ebbc-111"><strong>adStateOpen</strong></span><span class="sxs-lookup"><span data-stu-id="9ebbc-111"><strong>adStateOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="9ebbc-112">1</span><span class="sxs-lookup"><span data-stu-id="9ebbc-112">1</span></span></p></td>
<td><p><span data-ttu-id="9ebbc-113">Indica que o objeto está aberto.</span><span class="sxs-lookup"><span data-stu-id="9ebbc-113">Indicates that the object is open.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ebbc-114"><strong>adStateConnecting</strong></span><span class="sxs-lookup"><span data-stu-id="9ebbc-114"><strong>adStateConnecting</strong></span></span></p></td>
<td><p><span data-ttu-id="9ebbc-115">2</span><span class="sxs-lookup"><span data-stu-id="9ebbc-115">2</span></span></p></td>
<td><p><span data-ttu-id="9ebbc-116">Indica que o objeto está conectando.</span><span class="sxs-lookup"><span data-stu-id="9ebbc-116">Indicates that the object is connecting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ebbc-117"><strong>adStateExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="9ebbc-117"><strong>adStateExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="9ebbc-118">4</span><span class="sxs-lookup"><span data-stu-id="9ebbc-118">4</span></span></p></td>
<td><p><span data-ttu-id="9ebbc-119">Indica que o objeto está executando um comando.</span><span class="sxs-lookup"><span data-stu-id="9ebbc-119">Indicates that the object is executing a command.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ebbc-120"><strong>adStateFetching</strong></span><span class="sxs-lookup"><span data-stu-id="9ebbc-120"><strong>adStateFetching</strong></span></span></p></td>
<td><p><span data-ttu-id="9ebbc-121">8</span><span class="sxs-lookup"><span data-stu-id="9ebbc-121">8</span></span></p></td>
<td><p><span data-ttu-id="9ebbc-122">Indica que as linhas do objeto estão sendo recuperadas.</span><span class="sxs-lookup"><span data-stu-id="9ebbc-122">Indicates that the rows of the object are being retrieved.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9ebbc-123">**ADO/WFC Equivalente**</span><span class="sxs-lookup"><span data-stu-id="9ebbc-123">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="9ebbc-124">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="9ebbc-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9ebbc-125">Constante</span><span class="sxs-lookup"><span data-stu-id="9ebbc-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9ebbc-126">AdoEnums.ObjectState.CLOSED</span><span class="sxs-lookup"><span data-stu-id="9ebbc-126">AdoEnums.ObjectState.CLOSED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ebbc-127">AdoEnums.ObjectState.OPEN</span><span class="sxs-lookup"><span data-stu-id="9ebbc-127">AdoEnums.ObjectState.OPEN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ebbc-128">AdoEnums.ObjectState.CONNECTING</span><span class="sxs-lookup"><span data-stu-id="9ebbc-128">AdoEnums.ObjectState.CONNECTING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ebbc-129">AdoEnums.ObjectState.EXECUTING</span><span class="sxs-lookup"><span data-stu-id="9ebbc-129">AdoEnums.ObjectState.EXECUTING</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ebbc-130">AdoEnums.ObjectState.FETCHING</span><span class="sxs-lookup"><span data-stu-id="9ebbc-130">AdoEnums.ObjectState.FETCHING</span></span></p></td>
</tr>
</tbody>
</table>

