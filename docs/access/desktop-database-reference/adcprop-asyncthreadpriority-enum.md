---
title: ADCPROP_ASYNCTHREADPRIORITY_ENUM
TOCTitle: ADCPROP_ASYNCTHREADPRIORITY_ENUM
ms:assetid: b15006dd-22d5-fcf3-8196-9e24ea9d55a7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249844(v=office.15)
ms:contentKeyID: 48547143
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: b84a06efde252ca6c128e0bcc0baccaf3676e06e
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862944"
---
# <a name="adcpropasyncthreadpriorityenum"></a><span data-ttu-id="680d8-102">ADCPROP\_ASYNCTHREADPRIORITY\_ENUM</span><span class="sxs-lookup"><span data-stu-id="680d8-102">ADCPROP\_ASYNCTHREADPRIORITY\_ENUM</span></span>

<span data-ttu-id="680d8-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="680d8-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="680d8-104">Para um objeto do [Recordset](recordset-object-ado.md) RDS, especifica a prioridade de execução do encadeamento assíncrono que recupera os dados.</span><span class="sxs-lookup"><span data-stu-id="680d8-104">For an RDS [Recordset](recordset-object-ado.md) object, specifies the execution priority of the asynchronous thread that retrieves data.</span></span>

<span data-ttu-id="680d8-105">Use essas constantes com o **Recordset** da propriedade dinâmica "**Prioridade de Encadeamento em Segundo Plano**" , que referenciada no Índice de Propriedades Dinâmicas ADO e documentada no [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md).</span><span class="sxs-lookup"><span data-stu-id="680d8-105">Use these constants with the **Recordset** "**Background Thread Priority**" dynamic property, which is referenced in the ADO Dynamic Property Index and documented in the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) documentation.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="680d8-106">Constant</span><span class="sxs-lookup"><span data-stu-id="680d8-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="680d8-107">Valor</span><span class="sxs-lookup"><span data-stu-id="680d8-107">Value</span></span></p></th>
<th><p><span data-ttu-id="680d8-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="680d8-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="680d8-109"><strong>adPriorityAboveNormal</strong></span><span class="sxs-lookup"><span data-stu-id="680d8-109"><strong>adPriorityAboveNormal</strong></span></span></p></td>
<td><p><span data-ttu-id="680d8-110">4</span><span class="sxs-lookup"><span data-stu-id="680d8-110">4</span></span></p></td>
<td><p><span data-ttu-id="680d8-111">Define a prioridade entre normal e mais alta.</span><span class="sxs-lookup"><span data-stu-id="680d8-111">Sets priority between normal and highest.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="680d8-112"><strong>adPriorityBelowNormal</strong></span><span class="sxs-lookup"><span data-stu-id="680d8-112"><strong>adPriorityBelowNormal</strong></span></span></p></td>
<td><p><span data-ttu-id="680d8-113">2</span><span class="sxs-lookup"><span data-stu-id="680d8-113">2</span></span></p></td>
<td><p><span data-ttu-id="680d8-114">Define a prioridade entre mais baixa e normal.</span><span class="sxs-lookup"><span data-stu-id="680d8-114">Sets priority between lowest and normal.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="680d8-115"><strong>adPriorityHighest</strong></span><span class="sxs-lookup"><span data-stu-id="680d8-115"><strong>adPriorityHighest</strong></span></span></p></td>
<td><p><span data-ttu-id="680d8-116">5</span><span class="sxs-lookup"><span data-stu-id="680d8-116">5</span></span></p></td>
<td><p><span data-ttu-id="680d8-117">Define a prioridade para o valor mais alto possível.</span><span class="sxs-lookup"><span data-stu-id="680d8-117">Sets priority to the highest possible.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="680d8-118"><strong>AdPriorityLowest</strong></span><span class="sxs-lookup"><span data-stu-id="680d8-118"><strong>AdPriorityLowest</strong></span></span></p></td>
<td><p><span data-ttu-id="680d8-119">1</span><span class="sxs-lookup"><span data-stu-id="680d8-119">1</span></span></p></td>
<td><p><span data-ttu-id="680d8-120">Define a prioridade para o valor mais baixo possível.</span><span class="sxs-lookup"><span data-stu-id="680d8-120">Sets priority to the lowest possible.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="680d8-121"><strong>adPriorityNormal</strong></span><span class="sxs-lookup"><span data-stu-id="680d8-121"><strong>adPriorityNormal</strong></span></span></p></td>
<td><p><span data-ttu-id="680d8-122">3</span><span class="sxs-lookup"><span data-stu-id="680d8-122">3</span></span></p></td>
<td><p><span data-ttu-id="680d8-123">Define a prioridade como normal.</span><span class="sxs-lookup"><span data-stu-id="680d8-123">Sets priority to normal.</span></span></p></td>
</tr>
</tbody>
</table>

### <a name="adowfc-equivalent"></a><span data-ttu-id="680d8-124">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="680d8-124">ADO/WFC equivalent</span></span>

<span data-ttu-id="680d8-125">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="680d8-125">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="680d8-126">Constante</span><span class="sxs-lookup"><span data-stu-id="680d8-126">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="680d8-127">AdoEnums.AdcPropAsyncThreadPriority.ABOVENORMAL</span><span class="sxs-lookup"><span data-stu-id="680d8-127">AdoEnums.AdcPropAsyncThreadPriority.ABOVENORMAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="680d8-128">AdoEnums.AdcPropAsyncThreadPriority.BELOWNORMAL</span><span class="sxs-lookup"><span data-stu-id="680d8-128">AdoEnums.AdcPropAsyncThreadPriority.BELOWNORMAL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="680d8-129">AdoEnums.AdcPropAsyncThreadPriority.HIGHEST</span><span class="sxs-lookup"><span data-stu-id="680d8-129">AdoEnums.AdcPropAsyncThreadPriority.HIGHEST</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="680d8-130">AdoEnums.AdcPropAsyncThreadPriority.LOWEST</span><span class="sxs-lookup"><span data-stu-id="680d8-130">AdoEnums.AdcPropAsyncThreadPriority.LOWEST</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="680d8-131">AdoEnums.AdcPropAsyncThreadPriority.NORMAL</span><span class="sxs-lookup"><span data-stu-id="680d8-131">AdoEnums.AdcPropAsyncThreadPriority.NORMAL</span></span></p></td>
</tr>
</tbody>
</table>

