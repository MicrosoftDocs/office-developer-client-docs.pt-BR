---
title: EventStatusEnum (referência do banco de dados de área de trabalho do Access)
TOCTitle: EventStatusEnum
ms:assetid: ae1711bc-2af5-04fd-7d8c-222d8afc9d3d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249821(v=office.15)
ms:contentKeyID: 48547059
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 654d2a485c9273072d1daa61321e73418a15e969
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293270"
---
# <a name="eventstatusenum"></a><span data-ttu-id="97b59-102">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="97b59-102">EventStatusEnum</span></span>

<span data-ttu-id="97b59-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="97b59-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="97b59-104">Especifica o status atual da execução de um evento.</span><span class="sxs-lookup"><span data-stu-id="97b59-104">Specifies the current status of the execution of an event.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="97b59-105">Constant</span><span class="sxs-lookup"><span data-stu-id="97b59-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="97b59-106">Valor</span><span class="sxs-lookup"><span data-stu-id="97b59-106">Value</span></span></p></th>
<th><p><span data-ttu-id="97b59-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="97b59-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="97b59-108"><strong>adStatusCancel</strong></span><span class="sxs-lookup"><span data-stu-id="97b59-108"><strong>adStatusCancel</strong></span></span></p></td>
<td><p><span data-ttu-id="97b59-109">quatro</span><span class="sxs-lookup"><span data-stu-id="97b59-109">4</span></span></p></td>
<td><p><span data-ttu-id="97b59-110">Solicita o cancelamento da operação que provocou o evento.</span><span class="sxs-lookup"><span data-stu-id="97b59-110">Requests cancellation of the operation that caused the event to occur.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97b59-111"><strong>adStatusCantDeny</strong></span><span class="sxs-lookup"><span data-stu-id="97b59-111"><strong>adStatusCantDeny</strong></span></span></p></td>
<td><p><span data-ttu-id="97b59-112">3D</span><span class="sxs-lookup"><span data-stu-id="97b59-112">3</span></span></p></td>
<td><p><span data-ttu-id="97b59-113">Indica que a operação não pode solicitar o cancelamento da operação pendente.</span><span class="sxs-lookup"><span data-stu-id="97b59-113">Indicates that the operation cannot request cancellation of the pending operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97b59-114"><strong>adStatusErrorsOccurred</strong></span><span class="sxs-lookup"><span data-stu-id="97b59-114"><strong>adStatusErrorsOccurred</strong></span></span></p></td>
<td><p><span data-ttu-id="97b59-115">duas</span><span class="sxs-lookup"><span data-stu-id="97b59-115">2</span></span></p></td>
<td><p><span data-ttu-id="97b59-116">Indica que a operação que provocou o evento falhou devido a um ou mais erros.</span><span class="sxs-lookup"><span data-stu-id="97b59-116">Indicates that the operation that caused the event failed due to an error or errors.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97b59-117"><strong>adStatusOK</strong></span><span class="sxs-lookup"><span data-stu-id="97b59-117"><strong>adStatusOK</strong></span></span></p></td>
<td><p><span data-ttu-id="97b59-118">1</span><span class="sxs-lookup"><span data-stu-id="97b59-118">1</span></span></p></td>
<td><p><span data-ttu-id="97b59-119">Indica que a operação que provocou o evento foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="97b59-119">Indicates that the operation that caused the event was successful.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97b59-120"><strong>adStatusUnwantedEvent</strong></span><span class="sxs-lookup"><span data-stu-id="97b59-120"><strong>adStatusUnwantedEvent</strong></span></span></p></td>
<td><p><span data-ttu-id="97b59-121">0,5</span><span class="sxs-lookup"><span data-stu-id="97b59-121">5</span></span></p></td>
<td><p><span data-ttu-id="97b59-122">Impede notificações subsequentes antes que o método de evento tenha terminado a execução.</span><span class="sxs-lookup"><span data-stu-id="97b59-122">Prevents subsequent notifications before the event method has finished executing.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="97b59-123">Equivalente do ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="97b59-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="97b59-124">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="97b59-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="97b59-125">Constant</span><span class="sxs-lookup"><span data-stu-id="97b59-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="97b59-126">AdoEnums. EventStatus. CANCEL</span><span class="sxs-lookup"><span data-stu-id="97b59-126">AdoEnums.EventStatus.CANCEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97b59-127">AdoEnums. EventStatus. CANTDENY</span><span class="sxs-lookup"><span data-stu-id="97b59-127">AdoEnums.EventStatus.CANTDENY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97b59-128">AdoEnums. EventStatus. ERRORSOCCURRED</span><span class="sxs-lookup"><span data-stu-id="97b59-128">AdoEnums.EventStatus.ERRORSOCCURRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97b59-129">AdoEnums. EventStatus. OK</span><span class="sxs-lookup"><span data-stu-id="97b59-129">AdoEnums.EventStatus.OK</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97b59-130">AdoEnums. EventStatus. UNWANTEDEVENT</span><span class="sxs-lookup"><span data-stu-id="97b59-130">AdoEnums.EventStatus.UNWANTEDEVENT</span></span></p></td>
</tr>
</tbody>
</table>

